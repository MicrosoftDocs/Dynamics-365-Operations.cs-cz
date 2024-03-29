---
title: Podpora duální měny pro daň
description: Tento článek vysvětluje, jak rozšířit funkci účtování duálních měn v daňové doméně a dopad na výpočet a zaúčtování daně
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 13d70d964a83c2efba090244d549bdb38ad25af2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909033"
---
# <a name="dual-currency-support-for-sales-tax"></a>Podpora duální měny pro DPH
[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak rozšířit funkci účtování duálních měn pro DPH a dopad na výpočet, zaúčtování a vypořádání DPH.

Funkce duální měny pro Dynamics 365 Finance byla představena ve verzi 8.1 (říjen 2018). Mění, jakým způsobem se počítají účtovací položky v měně vykazování.

V předchozích verzích byly transakce převedeny na měnu vykazování v následujícím pořadí: 

- Celková transakce byla vypočtena v měně transakce > částka transakce byla převedena na zúčtovací měnu > částka zúčtovací měny byla převedena na měnu vykazování

Po povolení duální funkce měny byly transakce převedeny na měnu vykazování v následujícím pořadí:

- Částka v měně transakce > Částka v měně pro vykazování

Další informace o duální měně naleznete v [Duální měně](dual-currency.md).

V důsledku podpory duálních měn jsou v modulu Správa funkcí k dispozici dvě nové funkce: 

- Převod DPH (novinka ve verzi 10.0.13)
- Zadejte finanční dimenze do realizovaných účtů zisků / ztrát úpravy měny pro zúčtování DPH (nové ve verzi 10.0.17)

Podpora dvojí měny pro DPH zajišťuje, že daně budou vypočítány přesně v měně daně a že zůstatek vyrovnání DPH je vypočítán přesně v zúčtovací měně i v měně vykazování.

## <a name="sales-tax-conversion"></a>Převod DPH

**Parametr převodu DPH** poskytuje dvě možnosti převodu částky daně z transakční měny na daňovou měnu. 

- Zúčtovací měna: cesta bude "Částka v měně transakce > Částka v zúčtovací měně > Částka v měně daně". Typ směnného kurzu zúčtovací měny (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.
- Měna vykazování: cesta bude "Částka v měně transakce > Částka v měně vykazování > Částka v měně daně". Typ směnného kurzu měny vykazování (konfigurován v nastavení hlavní knihy) bude použit pro převod měny.

### <a name="example"></a>Příklad

Jedná se o jednoduchý příklad, který demonstruje tyto funkce:

Nastavení měny pro hlavní knihu a daň

| Měna transakce | Zúčtovací měna | Měna pro vykazování | Měna daně |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | USD                 | GBP                | GBP          |

Směnný kurz

| Z měny | Na měnu | Koeficient | Směnný kurz |
| ------------- | ----------- | ------ | ------------- |
| EUR           | USD         | 1      | 1.11          |
| EUR           | GBP         | 1      | 0.83          |
| USD           | GBP         | 1      | 0.75          |

Výpočet částky daně v různých možnostech parametrů

Částka daně = 100 EUR

| Parametry převodu DPH | Měna transakce (EUR) | Zúčtovací měna (USD) | Měna vykazování (GBP) | Měna daně (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Zúčtovací měna             | 100                        | 111                       | 83                       | **83.25**          |
| Měna pro vykazování              | 100                        | 111                       | 83                       | **83**             |

Tento parametr lze nakonfigurovat podle potřeby finančního úřadu na základě kompatibility.


### <a name="upgrade-consideration"></a>Předpoklady upgradu

Tato funkce bude použita pouze pro nové transakce. V případě daňové transakce, která je již uložena v tabulce TAXTRANS, ale ještě nebyla vyrovnána, systém nepřepočítá částku daně v daňové měně, protože směnný kurz v určitém časovém bodu zaúčtování daně již chybí.

Chcete-li zabránit předchozímu scénáři, doporučujeme změnit hodnotu tohoto parametru v novém (čistém) období vyrovnání daně, které neobsahuje žádné transakce nevyrovnané daně. Chcete-li tuto hodnotu změnit uprostřed období daňového vyrovnání, spusťte před změnou hodnoty tohoto parametru program "Vyrovnat a zaúčtovat DPH" pro období aktuálního vyrovnání.

Tato funkce přidá účetní položky, které objasňují zisky a ztráty ze směnných kurzů. Záznamy budou provedeny na účtech realizovaných zisků a ztrát s množstvím úprav měny, když se provede přecenění během vyrovnání DPH. Další informace viz [Automatický zůstatek vypořádání daně v měně vykazování](#tax-settlement-auto-balance-in-reporting-currency) dále v tomto článku.

> [!NOTE]
> Během vypořádání jsou informace o finančních dimenzích převzaty z účtů DPH, což jsou účty rozvahy, a zadány do účtů zisků a ztrát s množstvím úpravy měny, což jsou účty výkazu zisků a ztrát. Protože omezení hodnoty finančních dimenzí se liší mezi účty rozvahy a účty výkazu zisku a ztráty, může během procesu vypořádání a zaúčtování DPH dojít k chybě. Chcete-li se vyhnout nutnosti upravovat struktury účtů, můžete zapnout funkci „Vyplnit finanční dimenze do realizovaných účtů zisků / ztrát z vyrovnání měny pro zúčtování DPH“. Tato funkce vynutí odvození finančních dimenzí na účty zisků / ztrát s úpravou měny. 

## <a name="track-reporting-currency-tax-amount"></a>Sledovat částku daně v měně vykazování

Do tabulek souvisejících s daní byla přidána tři nová pole pro sledování částek v měně vykazování. Tato pole se nacházejí v tabulkách TAXUNCOMMITTED a TAXTRANS:

- TaxAmountRep: částka daně v měně vykazování
- TaxBaseAmountRep: částka základu v měně vykazování
- TaxInCostPriceRep: neodečitatelná částka v měně vykazování

U daně uložené pouze v tabulce TAXUNCOMMITTED, ale dosud nezaúčtované, systém přepočítá částku daně v měně vykazování v okamžiku zaúčtování a uloží do tabulky TAXTRANS.

Tato verze nebude zahrnovat změny v sestavách a formulářích, které zobrazují částku daně v měně vykazování. Změny v sestavách a formulářích budou dodány v budoucí verzi.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Automatický zůstatek pro vyrovnání daně v měně vykazování

Není-li vyrovnání daně v měně vykazování rovnoměrně vyrovnáno, jako například cesta převodu DPH je „zúčtovací měna“ nebo změna směnného kurzu v jednom období vyrovnání daně, systém automaticky vygeneruje účetní položky k úpravě odchylky částky daně a k její kompenzaci na účet realizovaných zisků/ztrát, který je konfigurován v nastavení hlavní knihy.

Chcete-li předvést tuto funkci pomocí předchozího příkladu, Předpokládejme, že data v tabulce TAXTRANS v okamžiku zaúčtování jsou následující:

| Parametry převodu DPH | Měna transakce (EUR) | Zúčtovací měna (USD) | Měna vykazování (GBP) | Měna daně (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Zúčtovací měna             | 100                        | 111                       | 83                       | **83.25**          |
| Měna pro vykazování              | 100                        | 111                       | 83                       | **83**             |

Při spuštění programu vyrovnání DPH na konci měsíce bude účetní položka vypadat takto.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Scénář: převod DPH = "zúčtovací měna"

| Hlavní účet           | Měna transakce (GBP) | Zúčtovací měna (USD) | Měna vykazování (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Závazky / pohledávky daně | -83,25                     | -111                      | -83,25                   |
| Vyrovnání daně         | 83.25                      | 111                       | 83.25                    |
| Realizovaný zisk/ztráta     | 0                          | 0                         | -0,25                    |
| Závazky / pohledávky daně | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Scénář: převod DPH = "měna vykazování"


| Hlavní účet           | Měna transakce (GBP) | Zúčtovací měna (USD) | Měna vykazování (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Závazky / pohledávky daně | -83                        | -110,67                   | -83                      |
| Vyrovnání daně         | 83                         | 110.67                    | 83                       |
| Realizovaný zisk/ztráta     | 0                          | 0.33                      | 0                        |
| Závazky / pohledávky daně | 0                          | -0,33                     | 0                        |



Další informace naleznete v následujících tématech:

- [Duální měna](dual-currency.md)
- [Přehled DPH](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
