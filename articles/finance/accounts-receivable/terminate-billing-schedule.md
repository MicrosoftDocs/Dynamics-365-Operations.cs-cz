---
title: Ukončení plánů fakturace
description: Toto téma vysvětluje, jak ukončit plány fakturace a řádky plánu fakturace ve Fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: df81cc888e893c6a4a127e1a43426a0a0b56f0d1
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470449"
---
# <a name="terminate-billing-schedules"></a>Ukončení plánů fakturace

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak ukončit plány fakturace a řádky plánu fakturace ve Fakturaci předplatného. Když ukončujete plán fakturace, musí být ve stavu **Aktivní**. Nemůže mít stav **Pozastaveno**. Obdobně když ukončujete řádek plánu fakturace, musí být ve stavu **Aktivní**. Sekce záhlaví plánu fakturace není ovlivněna, když ukončíte řádek plánu fakturace.

Chcete-li ukončit plán fakturace nebo řádek plánu fakturace, přejděte na jedno z následujících míst:

- Stránka se seznamem **Všechny/aktivní plány fakturace**
- Konkrétní plán fakturace na stránce **Všechny plány fakturace**
- Konkrétní řádek plánu fakturace na stránce **Všechny plány fakturace**

> [!NOTE]
> Pokud chcete ukončit několik plánů fakturace současně, použijte stránku **Zpracování hromadného ukončení**.

## <a name="terminate-a-billing-schedule-or-line"></a>Ukončení plánu fakturace nebo jeho řádku

Chcete-li ukončit plán fakturace nebo řádek plánu fakturace, postupujte takto.

1. Vyberte plán fakturace nebo řádek plánu fakturace a poté vyberte **Ukončit**. 
2. Nastavte pole **Datum ukončení**, **Typ ukončení** a **Kód důvodu**.
3. Nastavte pole **Možnost kreditu** na **Vydat dobropis**.
4. Vyberte možnost **Ukončit**.

Stav plánu fakturace se změní v závislosti na typu ukončení, který jste vybrali. Pokud jste vybrali jako typ ukončení **Zbývající účet**, má stav všech řádků v plánu fakturace hodnotu **Poslední vyúčtování**. Stav plánu fakturace zůstává **Aktivní** až do zpracování poslední faktury. Po zpracování poslední faktury se stav aktualizuje na **Ukončeno**. Pokud jste vybrali jako typ ukončení **Upravit plán**, stav plánu fakturace se okamžitě aktualizuje na **Ukončeno**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Ukončení plánu fakturace nebo jeho řádku a žádost o vrácení peněz

Chcete-li ukončit plán fakturace nebo jeho řádek a požádat o vrácení peněz, postupujte takto.

1. Vyberte plán fakturace nebo řádek plánu fakturace a poté vyberte **Ukončit**.
2. Nastavte pole **Datum ukončení**, **Typ ukončení**, **Kód důvodu** a **Možnost kreditu**.
3. Vyberte příkaz **Ukončit s vrácením peněz**. Zobrazí se stránka **Zpracování hromadného ukončení**, která je filtrována tak, aby zobrazovala plán fakturace.
4. Po výběru příkazu **Zobrazit náhled** zobrazíte řádky plánu účtování, a potí vyberte **Zpracovat**.

Po zpracování kreditu otevřete stránku **Zobrazit detail fakturace** a zkontrolujte kredit, který byl použit na plán fakturace. Pokud je částka kreditu větší než 0 (nula), všechny budoucí nevyfakturované řádky budou odstraněny a nahrazeny řádky s podrobností fakturace, které zobrazují záporné částky za kredit, který byl použit pro plán fakturace.

### <a name="view-example"></a>Zobrazit příklad

Plán fakturace obsahuje následující informace:

- Počáteční datum je 1. ledna 2020.
- Datum ukončení je 31. prosince 2020.
- Částka zúčtovacího období je 100,00 měsíčně.
- Faktury byly vytvořeny za zúčtovací období od ledna do července.
- Datum ukončení smlouvy je 15. června 2020.

Po zpracování úpravy kreditu budou ze stránky **Zobrazit detail fakturace** odstraněna všechna budoucí fakturační období (srpen až prosinec) . Po červencovém fakturačním období je přidán řádek úpravy kreditu:

- 16. června – 31. července s výší kreditu 150,00

Pokud je použita funkce nevyfakturovaných příjmů, stránka **Audit zápisu do deníku nevyfakturovaných výnosů** se aktualizuje o záznam ukončení.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Ukončení plánu fakturace nebo jeho řádku bez použití kreditu

Chcete-li ukončit plán fakturace nebo jeho řádek bez použití kreditu, postupujte takto.

1. Vyberte plán fakturace nebo řádek plánu fakturace a poté vyberte **Ukončit**.
2. Nastavte pole **Datum ukončení**.
3. Nastavte **Typ ukončení** na **Žádná úprava**. Pole **Možnost kreditu** se automaticky nastaví na **Žádný kredit**.
3. Nastavte pole **Kód důvodu**.
4. Do pole **Poznámky k ukončení** zadejte libovolné další požadované poznámky.
5. Vyberte možnost **Ukončit**. 

Po zpracování ukončení jsou odstraněny všechny řádky podrobností o fakturaci po datu ukončení. (Tyto řádky zahrnují řádek, který obsahuje datum ukončení.) Pro ukončené řádky nelze vytvářet faktury. Pokud je ukončení odebráno, všechny ukončené řádky jsou přidány zpět do stránky **Zobrazit fakturační údaje** a budou k dispozici pro fakturaci.

## <a name="fields"></a>Pole

Stránka **Zobrazit fakturační údaje** obsahuje následující pole.

| Pole | Popis |
|-------|-------------| 
| Datum výpovědi | Vyberte datum, kdy chcete plán fakturace nebo jeho řádek ukončit. |
| Typ ukončení | <p>Vyberte typ ukončení:</p><ul><li>**Upravit plán** – Přerušte fakturační období pro řádek k datu ukončení a změňte stav řádku na **Poslední vyúčtování**. Pokud pro řádkovou položku existuje plán odkladu, upraví se zrušením částky, která již nesmí být rozpoznána. Pokud datum zahájení fakturace spadá až za datum ukončení, zbývající fakturační období se odstraní.</li><li>**Zbývající účet** – Přidejte zbývající částku za fakturační období do období ukončení a změňte stav řádku na **Poslední vyúčtování**. Pokud pro řádkovou položku existuje plán odkladu, datum ukončení odkladu se aktualizuje. Pokud datum zahájení fakturace spadá až za datum ukončení, celková částka všech zbývajících fakturačních období se přičte k fakturačnímu období a zbývající fakturační období se odstraní.</li><li>**Žádná úprava** – Ukončete fakturační období řádku k určenému datu ukončení. Nejsou prováděny žádné úpravy. Když je vybrán tento typ ukončení, pole **Možnost kreditu** se nastaví na **Žádný kredit** a pole **Poměrně denně** na **Ne**. Obě tato pole je poté možné pouze číst a nelze je změnit.</li></ul> |
| Možnost kreditu | <p>Vyberte, jak bude kredit použit, když ukončíte řádek plánu fakturace:</p><ul><li>**Úprava kreditu** – Vytvořte úpravu kreditu pro plán fakturace, když je řádek ukončen. Úprava kreditu se objeví v budoucím fakturačním období plánu fakturace. Při úpravě se také automaticky upraví částka faktury pro další fakturační období, dokud nebude dokončeno použití kreditu v plánu fakturace.</li><li>**Vydat dobropis** – Vytvořte dobropis, když je plán fakturace nebo jeho řádek ukončen.</li><li>**Žádný kredit** – Když je plán fakturace nebo jeho řádek ukončen, nevytvoří se úprava kreditu ani dobropis. Tato možnost je dostupná pouze v případě, kdy použijete ukončení typu **Žádná úprava** k ukončení plánu fakturace.</li></ul><p>Výchozí možnost je převzata ze stránky **Parametry opakované fakturace smlouvy**.</p> |
| Kód důvodu | Vyberte kód důvodu ukončení. |
| Popis důvodu | Popis kódu důvodu. |
| Poznámky k ukončení | Zadejte případné poznámky k ukončení. |

<!--## Additional information-->
