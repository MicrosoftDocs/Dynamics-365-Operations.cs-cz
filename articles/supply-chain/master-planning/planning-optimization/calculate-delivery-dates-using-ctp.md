---
title: Výpočet dat dodání prodejní objednávky pomocí CTP
description: Funkce Příslib na základě ověření dostupné kapacity (CTP) vám umožňuje poskytnout zákazníkům realistická data, kdy můžete slíbit konkrétní zboží. Tento článek popisuje, jak nastavit a používat CTP pro každý plánovací modul (optimalizace plánování a vestavěný modul).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 9a2d8a66fe7e68ebd5729a401af3f0efe04051b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229931"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Výpočet dat dodání prodejní objednávky pomocí CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Funkce Příslib na základě ověření dostupné kapacity (CTP) vám umožňuje poskytnout zákazníkům realistická data, kdy můžete slíbit konkrétní zboží. Pro každý prodejní řádek můžete zadat datum, které zohledňuje existující skladové zásoby, výrobní kapacitu a přepravní časy.

CTP rozšiřuje funkci [dostupné k přislíbení](../../sales-marketing/delivery-dates-available-promise-calculations.md) (ATP) s ohledem na informace o kapacitě. Zatímco ATP bere v úvahu pouze dostupnost materiálu a předpokládá nekonečné kapacitní zdroje, CTP zvažuje dostupnost materiálů i kapacity. Poskytuje tedy realističtější obrázek o tom, zda lze poptávku uspokojit v daném časovém rámci.

CTP se chová trochu odlišně na základě toho, který modul plánování používáte (optimalizace plánování, nebo integrovaný modul). Tento článek popisuje, jak jednotlivé moduly. CTP pro optimalizaci plánování aktuálně podporuje pouze podmnožinu scénářů CTP, které jsou podporovány vestavěným modulem.

## <a name="turn-on-ctp-for-planning-optimization"></a>Zapnutí CTP pro optimalizaci plánování

CTP pro integrovaný hlavní plánovací modul je vždy dostupné. Pokud však chcete používat CTP pro optimalizaci plánování, musí být pro váš systém zapnuto. Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Hlavní plánování*
- **Název funkce:** *(Preview) CTP pro optimalizaci plánování*

## <a name="how-ctp-compares-to-atp"></a>Jak se CTP liší od ATP

CTP a ATP jsou podobné, ale CTP může často poskytnout přesnější výsledek, jak ukazuje následující příklad.

Položka A je položka, která se skládá z položek B a C a množství položky A na skladě je 0 (nula). Pokud provedete kontrolu ATP, která bere v úvahu pouze materiály, množství ATP bude také 0 (nula). Pokud však provedete kontrolu CTP, systém zkontroluje dostupnost položek B a C, zkontroluje zdroje, které jsou nutné k tomu, aby se z nich vytvořila položka A, a spočítá, kolik položek A lze vyrobit. Kromě toho může výpočet CTP zkontrolovat zdroje a materiály, které jsou nutné k výrobě většího množství položek B a C a jejich použití k výrobě většího množství položky A.

Výpočet CTP, který bere v úvahu materiály i zdroje, může ukazovat větší množství než výpočet, který kontroluje pouze materiály, zejména pokud je kontrolovaná položka sestavou na zakázku. Jinými slovy, funkce CTP je založena na funkci rozpisu a lze ji spustit pro vybraný řádek prodejní objednávky pro výpočet očekávaného data dodání.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Jak se CTP liší v závislosti na hlavním nástroji plánování, který používáte

Následující tabulka shrnuje rozdíly mezi CTP pro optimalizaci plánování a CTP pro vestavěný modul hlavního plánování.

| Prvek | Optimalizace plánování | Integrovaný hlavní plánovací modul |
|---|---|---|
| Nastavení **Kontrola termínu dodání** pro objednávky, řádky objednávek a produkty | *CTP pro optimalizaci plánování* | *CTP* |
| Čas výpočtu | Výpočet se spouští spuštěním dynamického plánu jako naplánované úlohy. | Výpočet se okamžitě spustí pokaždé, když zadáte nebo aktualizujete řádek prodejní objednávky. |
| Hodnota pole **Stav CTP pro optimalizaci plánování** | <p>Hodnota *Není připraveno* se zobrazuje pro objednávky a řádky objednávek, kde dynamický plán neběžel od vytvoření nebo poslední aktualizace objednávek a řádků.</p><p>Hodnota *Připraveno* se zobrazuje u objednávek a řádků, kde byl CTP použit k výpočtu potvrzených termínů dodání spuštěním dynamického plánu.</p> | Hodnota *Připraveno* se zobrazuje vždy. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Nastavení výchozích metod kontroly data dodání

Systém může použít libovolnou z několika metod k výpočtu odhadů data dodání pro každou objednávku a řádek objednávky. Měli byste nastavit metodu řízení data doručení, kterou chcete nejčastěji používat, jako globální výchozí metodu. Můžete také nastavit jednotlivá přepsání pro každý produkt. Později budete moci přepsat výchozí metody pro každou objednávku nebo řádek objednávky, jak budete potřebovat.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Nastavení výchozí globální kontroly data dodání

Výchozí metoda kontroly data dodání bude použita na všechny nové řádky objednávky, kde se nepoužije přepsání. Chcete-li ji vybrat, postupujte takto.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
1. Na kartě **Zásilky** na pevné záložce **Kontrola doručení** v poli **Kontrola termínu dodání** vyberte metodu, kterou chcete použít jako výchozí metodu pro vaši společnost:

    - *Žádný* – Nepočítat data dodání.
    - *Doba realizace prodeje* – doba realizace prodeje je doba mezi vytvořením prodejní objednávky a expedici položek. Výpočet data dodání je založen na výchozím počtu dnů a nezohledňuje skladovou dostupnost, známou poptávku ani plánovanou dodávku.
    - *ATP* – ATP je množství položky, které je k dispozici a může být odběrateli slíbeno k určitému datu. Výpočet množství ATP zahrnuje nepotvrzené zásoby, doby realizace, plánované příjmy a výdeje.
    - *ATP + rezerva výdeje* – datum expedice odpovídá datu ATP navýšenému o rezervu výdeje pro položku. Rezerva výdeje je doba potřebná k přípravě položek na expedici.
    - *CTP* – Použít výpočet CTP, který poskytuje vestavěný modul hlavního plánování. Pokud používáte optimalizaci plánování, metoda kontroly data dodání *CTP* není povolena, a pokud je vybrána, způsobí při spuštění výpočtu chybu.
    - *CTP pro optimalizaci plánování* – Použijte výpočet CTP, který poskytuje Optimalizace plánování. Tato možnost nemá žádný efekt, pokud používáte integrovaný hlavní plánovací modul.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Nastavení přepsání kontroly data dodání pro jednotlivé produkty

Můžete přiřadit přepsání pro konkrétní produkty, kde chcete použít jinou metodu řízení data dodání, než je ta, která je nastavena jako vaše globální výchozí metoda.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt, který chcete nastavit.
1. V podokně akcí, na kartě **Spravovat sklad**, ve skupině **Nastavení objednávky**, vyberte **Výchozí nastavení objednávky**.
1. Na stránce **Výchozí nastavení objednávky** na pevné záložce **Prodejní objednávka** nastavte **Přepsat kontrolu doručení** na *Ano*.
1. V poli **Kontrola data dodání** vyberte metodu, kterou chcete pro vybraný produkt použít. Stejné možnosti, které jsou popsány v části [Nastavit globální výchozí ovládací prvek data doručení](#global-default) jsou k dispozici.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Plánování CTP pro výpočty optimalizace plánování

Když používáte CTP pro optimalizaci plánování, musíte spustit dynamický plán, který spustí systém, aby provedl výpočty CTP, a poté nastavte potvrzená data odeslání a přijetí pro všechny relevantní objednávky. Plán musí obsahovat všechny položky, pro které jsou vyžadována potvrzená data odeslání a přijetí. (Když použijete CTP pro vestavěný plánovací modul, výpočty CTP se okamžitě provedou lokálně. Proto nemusíte spouštět dynamický plán, abyste viděli výsledky CTP.)

Abyste zajistili, že data budou pro všechny uživatele k dispozici včas, doporučujeme nastavit dávkové úlohy pro spouštění příslušných plánů na opakovaném základě. Například dávková úloha, která je nastavena tak, aby spouštěla dynamický plán každých 30 minut, nastaví potvrzené odeslání a data příjmu každých 30 minut. Proto uživatelé, kteří zadávají a importují objednávky, budou muset čekat maximálně 30 minut, než obdrží potvrzenou zásilku a obdrží data.

Chcete-li nastavit dávkovou úlohu pro spouštění dynamického plánu podle pravidelného plánu, postupujte takto.

1. Přejděte na **Hlavní plánování \> Hlavní plánování \> Spustit \> Hlavní plánování**.
1. V dialogovém okně **Hlavní plánování** na pevné záložce **Parametry** nastavte **Hlavní plán** na dynamický plán, který chcete spustit.
1. Na pevné záložce **Spustit na pozadí** nastavte možnost **Dávkové zpracování** na *Ano*.
1. Vyberte **Opakování** a podle potřeby nastavte plán.
1. Zvolte **OK** pro uložení plánu.
1. Vyberte **OK**, dávková úloha se vytvoří a dialogové okno se zavře.

## <a name="use-ctp-for-built-in-master-planning"></a>Použít CTP pro integrované hlavní plánování

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Vytvoření nové objednávky pomocí CTP pro integrované hlavní plánování

Pokaždé, když přidáte novou prodejní objednávku nebo řádek objednávky, systém k ní přiřadí výchozí metodu řízení data dodání. Hlavička objednávky vždy začíná globální výchozí metodou. Pokud je k objednané položce přiřazeno přepsání, nový řádek objednávky toto přepsání použije. Jinak bude nový řádek objednávky také používat globální výchozí metodu. Proto byste měli nastavit výchozí metody, aby odpovídaly metodě řízení data doručení, kterou používáte nejčastěji. Po vytvoření objednávky můžete podle potřeby přepsat výchozí metodu na úrovni záhlaví objednávky nebo řádku objednávky. Více informací viz [Nastavení výchozí metody kontroly data dodání](#default-methods) a [Změna existujících prodejních objednávek tak, aby používaly CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Zobrazení potvrzených dat dodání, když používáte CTP pro integrované hlavní plánování

Pokud používáte vestavěný modul hlavního plánování, výpočty CTP se aplikují na objednávky a řádky objednávek, kde pole **Kontrola data dodání** je nastaveno na *CTP*.

Pro prodejní řádky které používají CTP pro vestavěné hlavní plánování, systém automaticky nastaví pole **Potvrzené datum expedice** a **Potvrzené datum přijetí** pokaždé, když uložíte prodejní řádek. Pokud později provedete relevantní změnu na prodejním řádku (například změnou jejího množství nebo místa), data se okamžitě přepočítají.

- Chcete-li zobrazit potvrzená data dodání pro řádek prodejní objednávky, otevřete prodejní objednávku a vyberte prodejní řádek. Poté na záložce s náhledem **Údaje řádku** na kartě **Doručení** zkontrolujte hodnoty **Potvrzené datum expedice** a **Potvrzené datum příjmu**.
- Chcete-li zobrazit potvrzená data dodání pro celou objednávku, otevřete prodejní objednávku a vyberte zobrazení **Záhlaví**. Poté na záložce s náhledem **Doručení** zkontrolujte hodnoty **Potvrzené datum** expedice a **Potvrzené datum příjmu**.

## <a name="use-ctp-for-planning-optimization"></a>Použití CTP pro optimalizaci plánování

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Vytvoření nové objednávky pomocí CTP pro optimalizaci plánování

Pokaždé, když přidáte novou prodejní objednávku nebo řádek objednávky, systém k ní přiřadí výchozí metodu řízení data dodání. Hlavička objednávky vždy začíná globální výchozí metodou. Pokud je k objednané položce přiřazeno přepsání, nový řádek objednávky toto přepsání použije. Jinak bude nový řádek objednávky také používat globální výchozí metodu. Proto byste měli nastavit výchozí metody, aby odpovídaly metodě řízení data doručení, kterou používáte nejčastěji. Po vytvoření objednávky můžete podle potřeby přepsat výchozí metodu na úrovni záhlaví objednávky nebo řádku objednávky. Více informací viz [Nastavení výchozí metody kontroly data dodání](#default-methods) a [Změna existujících prodejních objednávek tak, aby používaly CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Zobrazení potvrzených dat doručení při použití CTP pro optimalizaci plánování

Pokud používáte optimalizaci plánování, výpočty CTP se aplikují na objednávky a řádky objednávek, kde pole **Kontrola data dodání** je nastaveno na *CTP pro optimalizaci plánování*.

Pro prodejní řádky, které používají CTP pro optimalizaci plánování, budou pole **Potvrzené datum expedice** a **Potvrzené datum přijetí** prázdná, dokud nespustíte příslušný dynamický plán (obvykle pomocí periodické dávkové úlohy). Poté jsou automaticky nastaveny. Další informace naleznete v tématu [Výpočty plánování CTP pro optimalizaci plánování](#batch-job).

Pole **CTP pro stav optimalizace plánování** označuje, zda již byla vypočtena potvrzená data pro každý řádek, který používá CTP pro optimalizaci plánování. Pole zobrazuje hodnotu *Není připraveno* pro řádky a objednávky, kde potvrzené dodací termíny ještě nebyly vypočteny nebo již nejsou platné z důvodu jiných změn. Ukazuje hodnotu *Připraveno* pro řádky a objednávky, které byly vypočteny. Můžete zobrazit stav pro každý řádek a pro celou objednávku.

- Chcete-li zobrazit stav pro řádek prodejní objednávky, otevřete prodejní objednávku a vyberte prodejní řádek. Poté na pevné záložce **Údaje řádku** na kartě **Dodávka** zkontrolujte hodnotu **Stav CTP pro optimalizace plánování**. Pole **Potvrzené datum expedice** a **Potvrzené datum přijetí** pro řádek jsou také zobrazena na této kartě po jejich výpočtu.
- Chcete-li zobrazit stav pro celou objednávku, otevřete prodejní objednávku a vyberte zobrazení **Záhlaví**. Poté na pevné záložce **Dodávka** zkontrolujte hodnotu **Stav CTP pro optimalizace plánování**. Pole **Potvrzené datum expedice** a **Potvrzené datum přijetí** pro objednávku jsou také zobrazena na této kartě po jejich výpočtu.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Pokud aktualizujete řádek prodejní objednávky poté, co CTP pro optimalizaci plánování pro něj vypočítala potvrzená data, systém tato data vymaže až do příštího spuštění příslušného dynamického plánu.
> - Pokud upravíte související nastavení, které by mohlo ovlivnit existující potvrzená data (například změnou dodacích lhůt, rezervací nebo označení), měli byste vymazat potvrzená data pro příslušné existující objednávky. Tato akce způsobí změnu stavu každého příslušného řádku na *Není připraveno*. Tato změna zase způsobí, že systém přepočítá potvrzená data při příštím spuštění dynamického plánu.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Změna existujících prodejních objednávek tak, aby používaly CTP

Můžete změnit hodnotu **Kontrola data dodání** pro jakoukoli otevřenou objednávku kdykoli. Hodnotu můžete změnit na úrovni záhlaví nebo pro každý řádek podle potřeby.

### <a name="change-to-ctp-at-the-order-header-level"></a>Změna na CTP na úrovni záhlaví objednávky

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Chcete-li změnit objednávku tak, aby používala CTP na úrovni záhlaví objednávky, postupujte takto.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.
1. Otevřete prodejní objednávku, kterou chcete nastavit, nebo vytvořte novou.
1. Vyberte **Záhlaví**, aby se otevřely údaje záhlaví na stránce **Údaje prodejní objednávky**.
1. Na pevné záložce **Dodání** nastavte pole **Kontrola data dodání** na jednu z následujících hodnot v závislosti na plánovacím modulu, který používáte:

    - *CTP* – Použít výpočet CTP, který poskytuje vestavěný modul hlavního plánování. Pokud používáte optimalizaci plánování, metoda kontroly data doručení *CTP* není povolena. Pokud tedy vyberete tuto hodnotu, dojde při výpočtu k chybě.
    - *CTP pro optimalizaci plánování* – Použijte výpočet CTP, který poskytuje Optimalizace plánování. Toto nastavení nemá žádný efekt, pokud používáte integrovaný hlavní plánovací modul.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Výběrem **OK** použijte změny.

### <a name="change-to-ctp-at-the-order-line-level"></a>Změna na CTP na úrovni řádku objednávky

Pokud jste vytvořili řádek objednávky pomocí jiné metody řízení data dodání, můžete kdykoli přejít na CTP. Změny, které provedete na úrovni řádku, neovlivní žádné další řádky. Mohou však způsobit, že se celková data dodání objednávky posunou dopředu nebo dozadu, v závislosti na tom, jak se změní každý aktualizovaný výpočet řádku. <!-- KFM: Confirm this intro at next revision -->

Chcete-li změnit objednávku tak, aby používala CTP pro integrované hlavní plánování na úrovni řádku, postupujte takto.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.
1. Otevřete prodejní objednávku, kterou chcete nastavit, nebo vytvořte novou.
1. Na stránce **Údaje prodejní objednávky** na pevné záložce **Řádek prodejní objednávky** vyberte řádek prodejní objednávky, který chcete nastavit.
1. Na pevné záložce **Údaje řádku** na kartě **Dodání** nastavte pole **Kontrola data dodání** na jednu z následujících hodnot v závislosti na plánovacím modulu, který používáte:

    - *CTP* – Použít výpočet CTP, který poskytuje vestavěný modul hlavního plánování. Pokud používáte optimalizaci plánování, metoda kontroly data doručení *CTP* není povolena. Pokud tedy vyberete tuto hodnotu, dojde při výpočtu k chybě.
    - *CTP pro optimalizaci plánování* – Použijte výpočet CTP, který poskytuje Optimalizace plánování. Toto nastavení nemá žádný efekt, pokud používáte integrovaný hlavní plánovací modul.

    Zobrazí se dialogové okno **Dostupné termíny odeslání a příjmu** s dostupnými daty odeslání a příjmu. Toto dialogové okno funguje pro řádky objednávky stejně jako pro záhlaví objednávky, jak je popsáno v předchozí části.

1. V podokně akcí vyberte **Uložit**.
