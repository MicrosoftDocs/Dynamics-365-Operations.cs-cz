---
title: Automatizace dodávek na zakázku
description: Tento článek popisuje, jak nastavit a používat různá vylepšení, která jsou přidána funkcí automatizace dodávek na zakázku.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220526"
---
# <a name="make-to-order-supply-automation"></a>Automatizace dodávek na zakázku

[!include [banner](../includes/banner.md)]

Funkce *Automatizace dodávek na zakázku* několik vylepšení do Microsoft Dynamics 365 Supply Chain Management. Tato vylepšení vám umožňují provádět následující úkony:

- Zobrazit zatížení kapacity zdrojů po uživatelem definovanou dobu, a umožnit tak dlouhodobé vyhodnocení zatížení kapacity.
- Zvýšit flexibilitu řízením tolerance zpoždění (záporné dny) pro každý hlavní plán.
- Udržovat produkty dostupné pro objednávky na poslední chvíli a optimalizovat využití stávající nabídky navázáním nejnovější možné nabídky na poptávku namísto použití první možné nabídky.
- Udržovat přiřazování komponent flexibilní pro výrobní zakázky po potvrzení, aby se systém mohl optimalizovat pro změny poptávky na poslední chvíli. Jinými slovy, omezit označování na jednu úroveň.
- Řídit zásady plnění pro každou prodejní objednávku. Výchozí nastavení jsou převzata ze zákaznického nastavení.
- Vylepšovat tok mezipodnikových informací. Nákupní objednávky jsou aktualizovány tak, aby obsahovaly pole pro způsob dodání, dodací podmínky a externí číslo položky. Tato změna zajišťuje, že do dodavatelské společnosti se dostanou podrobné informace o poptávce.

Tento článek popisuje, jak nastavit a používat jednotlivá vylepšení.

> [!NOTE]
> Všechna vylepšení popsaná v tomto článku platí pro systémy, které používají integrované hlavní plánování. Následující dvě vylepšení jsou také podporována doplňkem Optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management:
>
> - Tolerance zpoždění u hlavních plánů
> - Kontrola nad sekvencí doložení, která se používá během hlavního plánování

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Zapnutí funkce automatizace dodávek na zakázku

Než budete moci používat funkci popsanou v tomto článku, musíte ji v systému zapnout. Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kde je tato funkce uvedena následovně:

- **Modul:** *Hlavní plánování*
- **Název funkce:** *Automatizace dodávek na zakázku*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Nastavení počtu dní, které se mají zobrazovat na stránce Vytížení kapacity

Stránka **Vytížení kapacity** umožňuje zkontrolovat dostupnou kapacitu zdroje. Funkce *Automatizace dodávek na zakázku* vylepšuje stránku **Vytížení kapacity** přidáním pole **Počet dní**. Toto pole můžete použít k omezení počtu dní, po které se bude mřížka **Přehled** zobrazovat. Hodnota, kterou nastavíte, se uloží do paměti. Pokud tedy stránku opustíte a poté se vrátíte později, mřížka **Přehled** bude stále zobrazovat počet dní, které jste naposledy zadali.

Chcete-li otevřít stránku **Vytížení kapacity**, abyste mohli zkontrolovat dostupnou kapacitu pro jednotlivé zdroje, postupujte takto.

1. Přejděte na **Správa organizace \> Zdroje \> Zdroje**.
1. Vyberte zdroj, který chcete zkontrolovat.
1. V podokně akcí na kartě **Zdroj** ve skupině **Zobrazit** vyberte **Vytížení kapacity**.
1. Použijte filtr **Počet dní** k omezení počtu dní, po které se bude mřížka **Přehled** zobrazovat.

Chcete-li otevřít stránku **Vytížení kapacity**, abyste mohli zkontrolovat dostupnou kapacitu pro skupinu zdrojů, postupujte takto.

1. Přejděte na **Správa organizace \> Zdroje \> Skupiny zdrojů.**
1. Vyberte skupinu zdrojů, kterou chcete zkontrolovat.
1. V podokně akcí na kartě **Skupina zdrojů** ve skupině **Zobrazit** vyberte **Vytížení kapacity**.
1. Použijte filtr **Počet dní** k omezení počtu dní, po které se bude mřížka **Přehled** zobrazovat.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Aplikování jedné úroveň značení, když potvrzujete plánované objednávky

*Označení* slouží k propojení nabídky a poptávky. Připomíná to *doložení*, které označuje, jak hlavní plánování očekává pokrytí poptávky. Označení je však trvalejší než doložení. Funkce *Automatizace dodávek na zakázku* přidává možnost omezit označování zásob na jedinou úroveň, když jsou plánované objednávky potvrzeny. Přidává následující nové možnosti do pole **Aktualizovat označení** v dialogovém okně **Potvrzování**, když potvrzujete plánovanou objednávku:

- *Jednoúrovňový standard* – Používá se jednoúrovňové značení. Jednoúrovňové značení označuje pouze hlavní položku, nikoli její součásti kusovníku. Proto můžete po potvrzení zachovat flexibilní přiřazení komponent pro výrobní zakázky. Jednoúrovňové značení umožňuje systému optimalizovat změny poptávky na poslední chvíli. Ve *standardním* jednoúrovňovém značení jsou objednávky požadavků označeny proti jejich objednávkám plnění, ale objednávky plnění nejsou označeny, pokud mají zbývající množství.
- *Jednoúrovňové rozšířené* – Používá se jednoúrovňové značení. V *rozšířeném* jednoúrovňovém značení jsou objednávky požadavků označeny proti jejich objednávkám plnění a objednávky plnění jsou vždy označeny bez ohledu na zbývající množství.

Tyto možnosti jsou také dostupné v poli **Aktualizovat značení** na kartě **Standardní aktualizace** stránky **Parametry hlavního plánování**, kde definujete výchozí výběr pro dialogové okno **Potvrzování**.

Další informace naleznete v tématu [Označování zásob s optimalizací plánování](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Nastavení tolerance zpoždění (záporné dny) na úrovni hlavního plánu

Funkce *Automatizace dodávek na zakázku* přidává možnost konfigurovat toleranci zpoždění (záporné dny) na úrovni hlavního plánu. Nastavení je k dispozici také na úrovni pokrytí položky a skupiny pokrytí. Pokud jsou záporné dny přiřazeny na více než jedné úrovni, systém rozhodne, které nastavení použít, na základě následující hierarchie:

- Pokud jsou záporné dny nakonfigurovány na stránce **Hlavní plány**, toto nastavení přepíše všechna ostatní nastavení záporných dnů, když plán běží.
- Pokud jsou záporné dny nakonfigurovány na stránce **Pokrytí položky**, toto nastavení přepíše nastavení skupiny pokrytí.
- Negativní dny, které jsou nakonfigurovány na stránce **Skupiny pokrytí**, se použijí pouze v případě, že pro relevantní položku nebo hlavní plán nebyly nakonfigurovány záporné dny.

Chcete-li nastavit záporné dny pro hlavní plán, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte v podokně seznamu hlavní plán nebo vytvořte nový.
1. Na kartě s náhledem **Ochranné lhůty ve dnech** nastavte možnost **Záporné dny** na *Ano*.
1. V poli vedle zadejte počet záporných dní, které se mají povolit.

Další informace o tom, jak používat záporné dny, viz [Tolerance zpoždění (záporné dny)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Kontrola sekvence doložení, která se používá během hlavního plánování

Hlavní plánování využívá *sekvenci doložení* k určení, která nabídka pokryje kterou poptávku. Funkce *Automatizace dodávek na zakázku* přidává novou možnost **Použít nejnovější možnou zásobu**, která vám dává větší kontrolu nad sekvencí doložení. Nová možnost umožňuje udržovat produkty dostupné pro objednávky na poslední chvíli a optimalizovat využití stávající nabídky navázáním nejnovější možné nabídky na poptávku namísto použití první možné nabídky.

Pořadí doložení můžete nastavit na úrovni hlavního plánu, pokrytí položky nebo skupiny pokrytí. Pokud je sekvence doložení nastavena na více než jedné úrovni, systém rozhodne, které nastavení použít, na základě následující hierarchie:

- Pokud je na stránce **Hlavní plány** nastavena sekvence doložení, toto nastavení přepíše všechna ostatní nastavení sekvence doložení, když plán běží.
- Pokud je sekvence doložení nastavena na stránce **Pokrytí položky**, toto nastavení přepíše nastavení skupiny pokrytí.
- Sekvence doložení, která je nastavena na stránce **Skupiny pokrytí**, se použije pouze v případě, že nastavení sekvence doložení nebyla nakonfigurována pro relevantní položku nebo hlavní plán.

Chcete-li nastavit doložení na úrovni skupiny pokrytí, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility**.
1. Vyberte v podokně seznamu skupinu nebo vytvořte novou.
1. Na pevné záložce **Obecné** v části **Sekvence doložení** použijte pole **Spotřebovat zásoby na skladě** a **Použít nejnovější zásobu** pro konfiguraci sekvence doložení. Tabulka dále v této části ukazuje, jak jsou tato nastavení kombinována, aby definovala vaši sekvenci doložení.

Chcete-li nastavit doložení na úrovni skupiny pokrytí položky, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt v mřížce nebo vytvořte nový.
1. V podokně akcí na kartě **Plánování** vyberte **Disponibilita položky**.
1. Stránka **Pokrytí položky** obsahuje řádky, které umožňují definovat pravidla pokrytí, která se vztahují na položku v každém skladu. Vyberte stávající řádek v mřížce nebo vytvořte nový.
1. Na kartě **Obecné** zaškrtněte políčko **Přepsat sekvenci doložení**.
1. Použijte pole **Spotřebovat zásoby na skladě** a **Použít nejnovější zásobu** pro konfiguraci sekvence doložení. Tabulka dále v této části ukazuje, jak jsou tato nastavení kombinována, aby definovala vaši sekvenci doložení.

Chcete-li nastavit doložení na úrovni hlavního plánu, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte v podokně seznamu hlavní plán nebo vytvořte nový.
1. Na pevné záložce **Obecné** nastavte možnost **Přepsat pořadí doložení** na *Ano*.
1. Použijte pole **Spotřebovat zásoby na skladě** a **Použít nejnovější zásobu** pro konfiguraci sekvence doložení. Tabulka dále v této části ukazuje, jak jsou tato nastavení kombinována, aby definovala vaši sekvenci doložení.

Následující tabulka ukazuje, jak se nastavení **Spotřebovat zásoby na skladě** a **Použít nejnovější zásobu** zkombinují, aby se vytvořila vaše sekvence doložení.

| | Použít nejnovější zásobu = Ano | Použít nejnovější zásobu = Ne |
|---|---|---|
| **Spotřebovat zásoby na skladě** = *Před veškerými zásobami* | <ol><li>Na skladě</li><li>Stávající zásoby, které mohou uspokojit datum poptávky</li><li>Stávající zásoby, které nemohou splnit datum poptávky, ale stále v záporných dnech</li><li>Vytvoření nové zásoby (plánované pořadí)</li></ol> | <ol><li>Na skladě</li><li>Stávající zásoby, které mohou uspokojit datum poptávky</li><li>Stávající zásoby, které nemohou splnit datum poptávky, ale stále v záporných dnech</li><li>Vytvoření nové zásoby (plánované pořadí)</li></ol> |
| **Spotřebovat zásoby na skladě** = *Po veškerých zásobách* | <ol><li>Stávající zásoby, které mohou uspokojit datum poptávky</li><li>Na skladě</li><li>Stávající zásoby, které nemohou splnit datum poptávky, ale stále v záporných dnech</li><li>Vytvoření nové zásoby (plánované pořadí)</li></ol> | <ol><li>Stávající zásoby, které mohou uspokojit datum poptávky</li><li>Stávající zásoby, které nemohou splnit datum poptávky, ale stále v záporných dnech</li><li>Na skladě</li><li>Vytvoření nové zásoby (plánované pořadí)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Kontrola a nastavení zásady plnění, které se vztahují na každou prodejní objednávku

Zásady plnění řídí procento celkové ceny nebo množství nebo cenu objednávky, která musí být fyzicky rezervována, aby bylo možné uvolnit prodejní objednávku do skladu. Můžete nastavit globální výchozí zásady plnění a poté je podle potřeby přepsat pro konkrétní zákazníky. Funkce *Automatizace dodávek na zakázku* přidává možnost zobrazit, jaké výchozí zásady se skutečně vztahují na jakoukoli objednávku, a podle potřeby použít přepsání specifické pro objednávku.

- Chcete-li nastavit výchozí globální zásady plnění pro prodejní objednávky, přejděte na **Pohledávky \> Nastavení \> Parametry pohledávek**. Poté na kartě **Správa skladu** nastavte pole **Zásady plnění prodejních objednávek** na název zásady, kterou chcete použít. 
- Chcete-li nastavit zásady plnění specifické pro zákazníka pro prodejní objednávky, přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci**. Poté na kartě **Správa skladu** nastavte pole **Zásady plnění** na název zásady, kterou chcete použít.

Chcete-li zobrazit výchozí zásady, které se vztahují na jakoukoli objednávku, a použít přepsání specifické pro objednávku, postupujte takto.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Otevřete prodejní objednávku, kterou chcete zkontrolovat nebo upravit.
1. Vyberte zobrazení **Záhlaví**.
1. Na pevné záložce **Sklad** zkontrolujte a upravte následující pole podle potřeby:

    - **Zásady plnění objednávek** – Vyberte zásady plnění, které se mají použít pro vybranou objednávku. Výchozí zásada bude přepsána. Chcete-li použít výchozí zásady plnění, které jsou uvedeny v poli **Výchozí zásady plnění**, nechte toto pole prázdné.
    - **Výchozí zásady plnění** – Toto pole zobrazuje výchozí zásady plnění, které se použijí v případě, že je pole **Zásady plnění objednávek** prázdné. Toto pole je určeno pouze ke čtení. Pokud je prázdné, nejsou definovány žádné zásady plnění specifické pro zákazníka nebo globální výchozí zásady.

    Pokud je prázdné pole **Výchozí zásady plnění** i **Výchozí zásady plnění**, neplatí žádné zásady plnění. Mohou však platit i jiná omezení, která mohou vyžadovat, aby byly před uvolněním prodejní objednávky splněny rezervace nebo jiné podmínky.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Nastavte režim dodání a podmínky na jednotlivých řádcích nákupní objednávky

Všechny nákupní objednávky zahrnují nastavení **Podmínky doručení** a **Způsob doručení** v záhlaví objednávky. Funkce *Automatizace dodávek na zakázku* přidává tato nastavení do každého řádku objednávky. Proto můžete definovat přepsání hodnoty **Podmínky doručení** nebo **Způsob doručení** pro kterýkoli nebo všechny řádky objednávky podle potřeby. Pro řádky, kde není definováno žádné přepsání, se použije hodnota z hlavičky. Můžete určit, zda má změna hodnoty jednoho nebo obou těchto polí v záhlaví objednávky také aktualizovat všechny řádky.

Chcete-li určit, co se má stát s nastavením řádku, pokud uživatel změní hodnotu **Podmínky doručení** nebo **Způsob doručení** v záhlaví objednávky, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.
1. Na kartě **Obecné** na pevné záložce **Výchozí hodnoty a parametry** vyberte odkaz **Aktualizovat řádky objednávky**.
1. V dialogovém okně **Aktualizovat řádky objednávky** v polích **Aktualizace dodacích podmínek** a **Aktualizovat způsob doručení** vyberte jednu z následujících hodnot:

    - *Nikdy* – Nikdy neaktualizovat řádky objednávky po změně nastavení v záhlaví objednávky.
    - *Vždy* – Vždy aktualizovat všechny řádky objednávky po změně nastavení v záhlaví objednávky.
    - *Dotázat se* – Pokud uživatel změní jedno nebo obě nastavení v záhlaví objednávky, otevřete dialogové okno s dotazem, zda chce uživatel aktualizovat všechny řádky tak, aby odpovídaly změně jednoho nebo obou nastavení.

Chcete-li nastavit informace o doručení v záhlaví nákupní objednávky, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Otevřete nákupní objednávku, kterou chcete upravit.
1. Vyberte zobrazení **Záhlaví**.
1. Na pevné záložce **Doručení** nastavte pole **Způsob doručení** a **Podmínky doručení** podle potřeby.
1. V závislosti na nastavení na stránce **Parametry nákupu a zajišťování zdrojů** můžete být dotázáni, zda chcete změny použít na všechny řádky objednávky.

Chcete-li nastavit přepsání údajů pro řádek nákupní objednávky, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Otevřete nákupní objednávku, kterou chcete upravit.
1. Vyberte zobrazení **Řádky**.
1. Na pevné záložce **Řádky nákupní objednávky** vyberte řádek, který chcete upravit.
1. Na pevné záložce **Údaje řádku** na kartě **Doručení** nastavte pole **Způsob doručení** a **Podmínky doručení** podle potřeby. Chcete-li použít odpovídající nastavení v záhlaví, vymažte jedno nebo obě pole.

U mezipodnikových zakázek hodnoty pro pole **Způsob doručení** a **Podmínky doručení** na každém řádku nákupní objednávky budou synchronizována mezi nákupní objednávkou a související prodejní objednávkou.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Synchronizace externích ID položek a popisů pro mezipodnikové objednávky

Pro mezipodnikové zakázky funkce *Automatizace dodávek na zakázku* umožňuje synchronizaci externích ID položek a textových popisů na řádcích nákupní objednávky se souvisejícími řádky mezipodnikových prodejních objednávek bez ohledu na to, zda je nákupní objednávka určena pro přímé dodání. Tato funkce také přidává možnost zadat konečný účet externího zákazníka na mezipodnikové nákupní objednávce. Systém pak automaticky převezme externí ID položek a textové popisy z externího záznamu zákazníka namísto (interního) mezipodnikového záznamu dodavatele.

Chcete-li nastavit mezipodnikového dodavatele pro synchronizaci externích ID položek a názvů položek mezi mezipodnikovými nákupními objednávkami a jejich souvisejícími mezipodnikovými prodejními objednávkami, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**.
1. Vyberte mezipodnikového dodavatele, kterého chcete nastavit.
1. Na panelu akcí na kartě **Obecné** ve skupině **Nastavení** vyberte možnost **Mezipodnikové**.
1. Na stránce **Mezipodnikové** na kartě **Zásady nákupní objednávky** v části **Mezipodniková nákupní objednávka -\> Mezipodniková prodejní objednávka** vyberte zaškrtávací políčko **Externí ID položky a název položky**.

Chcete-li zadat konečný účet externího zákazníka pro mezipodnikovou nákupní objednávku, postupujte následovně. Pole **Zákaznický účet** platí pouze pro mezipodnikové nákupní objednávky. Pomocí něj uveďte číslo účtu zákazníka, který nakonec zboží obdrží. Když je toto pole nastaveno, řádky nákupní objednávky převezmou externí popisy položek a čísla ze zadaného zákaznického účtu namísto mezipodnikového dodavatele, který je uveden v nákupní objednávce. Pokud později změníte zákaznický účet, externí popisy položek a ID budou aktualizovány tak, aby odpovídaly hodnotám pro nový účet. Externí popisy položek a ID pro každý řádek budou také synchronizovány s odpovídající mezipodnikovou prodejní objednávkou.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Otevřete nákupní objednávku, kterou chcete nastavit, nebo vytvořte novou.
1. Vyberte zobrazení **Záhlaví**.
1. V části **Reference** nastavte pole **Zákaznický účet** na příslušný externí zákaznický účet.

Chcete-li zadat externí ID položek a textové popisy pro řádek nákupní objednávky pro mezipodnikovou objednávku, postupujte takto. Hodnoty, které nastavíte, budou synchronizovány se souvisejícími mezipodnikovými řádky prodejní objednávky bez ohledu na to, zda je nákupní objednávka určena pro přímé dodání.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Otevřete nákupní objednávku, kterou chcete nastavit, nebo vytvořte novou.
1. Vyberte zobrazení **Řádky**.
1. Na pevné záložce **Řádky nákupní objednávky** vyberte řádek, který chcete upravit.
1. Na pevné záložce **Údaje řádku** na kartě **Obecné** v části **Řádek objednávky** v poli **Text** uveďte externí popis položky, která je uvedena na vybraném řádku objednávky. Tato hodnota bude synchronizována s řádkem související mezipodnikové prodejní objednávky.
1. V části **Reference** v poli **Externí** zadejte externí ID položky pro položku, která je uvedena na vybraném řádku objednávky. Tato hodnota bude synchronizována s řádkem související mezipodnikové prodejní objednávky.

Další informace naleznete v článku [Vytvoření faktury a mezipodnikové prodejní objednávky pro externího zákazníka](../sales-marketing/intercompany-sales-order-for-external-customer.md).
