---
title: Odhad a správa nákladů za doručení
description: Systém používá vaše nastavení automatických nákladů k určení odhadu vašich nákladů za doručení. Toto téma vysvětluje, jak můžete definovat různé scénáře a dosáhnout tak přesnějšího odhadu.
author: sherry-zheng
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 510f5fc4910dde2f91fe2d666abb23a9bd7381f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823426"
---
# <a name="estimate-and-manage-landed-costs"></a>Odhad a správa nákladů za doručení

[!include [banner](../../includes/banner.md)]

Systém používá vaše [nastavení automatických nákladů](auto-cost-setup.md) k určení odhadu vašich nákladů za doručení. Kromě toho můžete definovat různé scénáře a dosáhnout tak přesnějšího odhadu. Tyto scénáře jsou uloženy. Můžete je tedy později zkontrolovat a porovnat je se skutečností v sestavě. Můžete také aktualizovat cenu položky.

## <a name="set-up-cost-estimates"></a>Nastavení odhadu nákladů

### <a name="set-up-cost-templates"></a>Nastavit šablony nákladů

Šablony nákladů určují výchozí nastavení, které uživatelé dostávající odhad nemusí nutně znát. Šablony mohou pomoci snížit složitost procesu odhadu minimalizací výběrů, které musí uživatelé udělat, aby získali přesný odhad. Pokud používáte model standardních nákladů, můžete při nastavování nákladů na zboží používat šablony nákladů.

Chcete-li nastavit šablony nákladů, přejděte na stránku **Náklady za doručení \> Nastavení kalkulace \> Šablony nákladů**. Na stránce **Šablony nákladů** se v podokně seznamu vlevo zobrazí všechny aktuální šablony nákladů. Pomocí tlačítek v podokně akcí můžete vytvářet, odstraňovat a upravovat šablony.

V následující tabulce jsou popsána pole, která jsou k dispozici pro každou šablonu.

| Pole | popis |
|---|---|
| Šablona nákladů | Zadejte jedinečný název pro šablonu nákladů. Název obvykle popisuje koeficient faktorů nebo nákladů pro šablonu. |
| popis | Zadejte popis šablony nákladů. |
| Dopravní společnost | Vyberte přepravní společnost, která by měla být aplikována při použití šablony. |
| Způsob dodání | Vyberte způsob doručení, například vzduchem nebo po moři, který by se měl aplikovat při použití šablony. Toto pole pomůže při odhadu nákladů určit automatické náklady spojené se zbožím. |
| Typ přepravního kontejneru | Vyberte typ přepravního kontejneru, který by měl být aplikován při použití šablony. Toto pole pomůže při odhadu nákladů určit automatické náklady spojené se zbožím. |
| Celní deklarant | Celní makléř (dodavatel), který by měl být aplikován při použití šablony. Toto pole pomůže určit automatické náklady spojené s odhadem nákladů. |
| Koeficient | Zadejte koeficient (procento), který by se měl automaticky použít na odhad nákladů při použití šablony. Chcete-li například přidat 10 procent k vypočítanému odhadu nákladů, zadejte *1,10*. |

### <a name="create-a-cost-estimate"></a>Vytvoření odhadu nákladů

Dialogové okno **Odhad nákladů** použijte ke generování nového odhadu nákladů, který je založen na vybrané šabloně nákladů, vybrané sadě položek a dalších podrobnostech cesty. Tato nastavení se poté použijí k určení odhadovaných nákladů na zboží. Tyto odhady nákladů se primárně používají při práci se standardními nákladovými položkami. Přidáním odhadovaných nákladů za doručení ke standardním nákladům na zboží ve skladu byste měli po přidání zboží do cesty zaznamenávat transakce s menšími odchylkami, protože standardní náklady budou odrážet odhady těchto nákladů za doručení.

Chcete-li otevřít dialogové okno **Odhad nákladů**, přejděte na uzel **Náklady za doručení \> Periodické úkoly \> Odhad nákladů**. Poté nastavte pole, která jsou popsána v následujících pododdílech. Nakonec výběrem **OK** vytvořte odhad. Poté se zobrazí stránka **Odhad nákladů** (**Náklady za doručení \> Dotazy \> Odhady nákladů**) a zobrazí váš nový odhad, jak je popsáno dále v tomto tématu.

### <a name="settings-on-the-parameters-tab"></a>Nastavení na kartě Parametry

Následující tabulka popisuje pole, která jsou k dispozici na kartě **Parametry** v dialogovém okně **Odhad nákladů**.


| Pole | popis |
|---|---|
| Šablona nákladů | Vyberte šablonu nákladů. Nastavení, která jsou přidružena k vybrané šabloně, se použijí k určení použitých automatických nákladů. |
| Odhad data | Ve výchozím nastavení je toto pole nastaveno na dnešní datum, ale hodnotu můžete změnit. Zadané datum se použije k výběru příslušných prodejních cen, nákupních cen, automatických nákladů a směnného kurzu, pokud je použit přepravní kurz. |
| Měrný systém | Náklady mohou záviset na měření. Když se například použije letecká přeprava, mohou se uplatnit objemové ceny. Pokud cena závisí na měření, zadejte hodnotu tohoto měření. Jinak doporučujeme nastavit toto pole na *1*, pokud si nejste jisti, že pomocí měření nedochází k žádnému rozdělení. Zadejte desetinné číslo. Jednotkou je ta jednotka, která je definována v příslušném záznamu automatických nákladů. |
| Šablona cesty | Vyberte [šablonu cesty](multi-leg-journey-setup.md). Toto pole se používá k určení správných automatických nákladů, které se mají použít. |
| Výchozí přístav | Přístav, ze kterého budou položky odeslány. Toto pole je nastaveno na základě vybrané šablony cesty. |
| Cílový přístav | Přístav, do kterého budou položky odeslány. Toto pole je nastaveno na základě vybrané šablony cesty. |
| Měna | Vyberte měnu, ve které budou položky zakoupeny. |
| Kontejnery | Pokud se obvykle používá více kontejnerů, zadejte počet kontejnerů. Systém poté při odhadu nákladů použije náklady na více kontejnerů. |
| Folia | Pokud se obvykle používá více fólií, zadejte množství. (Množství je obvykle *1*.) |
| Lokalita | Určete místo, kam bude zboží doručeno. |

### <a name="settings-on-the-items-tab"></a>Nastavení na kartě Položky

Na kartě **Položky** můžete do odhadu přidat tolik položek, kolik potřebujete. Pomocí panelu nástrojů přidejte položky do mřížky nebo je odeberte. Výběrem možnosti **Zásoby \> Zobrazit dimenze** na panelu nástrojů otevřete dialogové okno, kde můžete do mřížky přidat sloupce dimenzí nebo sloupce odebrat.

V následující tabulce jsou popsána pole, která jsou k dispozici pro každou položku.

| Pole | popis |
|---|---|
| Č. položky | Vyberte položku, pro kterou chcete určit cenu. (Pokud položka v systému ještě neexistuje, vytvořte fiktivní položku, volitelně ji připojte ke skupině nákladů na položku cesty a poté buď ponechejte cenu prázdnou, nebo vytvořte či změňte cenu.) |
| Účet dodavatele | Vyberte dodavatele, kterého chcete použít pro odhad této položky. Pokud je položce přiřazen výchozí dodavatel, toto pole se nastaví automaticky. |
| Množství | Určete množství, které nakoupíte. |
| Nákladová cena | Systém používá cenová pravidla k nalezení počáteční ceny, ale v případě potřeby tuto cenu můžete přepsat. |
| Prodejní cena | Zadejte očekávanou prodejní cenu zboží. |
| Měrný systém | Zadejte desetinné číslo pro měření zboží. Jednotkou je ta jednotka, která je nastavena pro příslušný vydaný produkt. |
| Aktualizovat hmotnost/objem položky | Zaškrtnutím tohoto políčka aktualizujete měření hmotnosti nebo objemu uvolněného produktu tak, aby odpovídalo hodnotě **Měření**, která je zadána pro tento řádek. |
| (Jiné rozměry) | V závislosti na dimenzích, které jste vybrali k zobrazení, se mohou zobrazit další sloupce s informacemi o každé položce. |

Chcete-li zobrazit nebo upravit podrobnosti o objemu anebo hmotnosti položky, vyberte položku v mřížce a poté použijte pole v dolní části stránky.

## <a name="manage-estimated-costs"></a>Správa odhadovaných nákladů

Chcete-li zobrazit a upravit odhady nákladů, které jste vytvořili, přejděte na uzel **Náklady za doručení \> Dotazy \> Odhady nákladů**. Na stránce **Odhady nákladů** se v podokně seznamu vlevo zobrazí všechny aktuální odhady nákladů. K práci s vybraným odhadem můžete použít tlačítka v podokně akcí. Všimněte si, že ve stránce **Odhady nákladů** nemůžete vytvořit nový odhad nákladů. Místo toho použijte dialogové okno **Odhad nákladů** (**Náklady za doručení \> Periodické úkoly \> Odhad nákladů**), jak je popsáno výše v tomto tématu.

Stránka **Odhady nákladů** ukazuje, jak byly odvozeny jednotlivé odhadované náklady. Ukazuje také odhadované náklady za doručení pro každou položku. Odhad nákladů můžete upravit změnou nákladové ceny anebo měny spojené s různým zbožím. Můžete také upravit přidružené náklady na cestu na úrovni cesty i na úrovni kontejneru. Když použijete tuto stránku k úpravě nákladů, zobrazí se výzva k přepočtu odhadovaných nákladů pro položky v odhadu nákladů. Až budete připraveni, můžete pomocí odhadů aktualizovat nákladovou cenu položek v šabloně nákladů.

### <a name="information-on-the-header"></a>Informace v záhlaví

Horní část stránky **Odhady nákladů** zobrazuje nastavení, která byla použita ke generování vybraného odhadu nákladů, jak je popsáno v předchozí části. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Nastavení a tlačítka na záložce Řádky

Záložka **Řádky** uvádí každou položku, která je zahrnuta v aktuálním odhadu. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý řádek.

| Pole | popis |
|---|---|
| Účet dodavatele | Účet dodavatele, který je přidružený k položce. |
| Č. položky | Číslo položky. |
| Množství | Počet položek, které se používají k určení ceny. |
| Nákladová cena | Nákladová cena podle obchodní smlouvy. Tato hodnota je zobrazena v místní měně. |
| Měrný systém | Individuální měření. Jednotkou je ta jednotka, která je definována pro příslušný vydaný produkt. |
| Odhadované náklady na doručení | Odhadované náklady za doručení pro celkové množství. |
| Na jednotku | Odhadované náklady za doručení dělené množstvím. |
| (Jiné rozměry) | V závislosti na dimenzích, které jste vybrali k zobrazení, se mohou zobrazit další sloupce s informacemi o každé položce. |

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na panelu nástrojů na záložce **Řádky**.

| Tlačítko | popis |
|---|---|
| Přidat | Přidejte položky do odhadu nákladů. Po přidání položek musíte vybrat příkaz **Přepočítat** v podokně akcí. |
| Odebrat | Odeberte položky z odhadu nákladů. Po odebrání položek musíte vybrat příkaz **Přepočítat** v podokně akcí. |
| Náklady na cestu | Otevřete stránku, kde můžete zobrazit a upravit různé typy nákladů na cestu pro položku. |
| Zásoby \> Zobrazit dimenze | Otevřete dialogové okno, kde můžete do mřížky přidat sloupce dimenze nebo sloupce odebrat. |

### <a name="settings-on-the-general-fasttab"></a>Nastavení na záložce Obecné

Záložka **Všeobecné** zobrazuje podrobnosti o položce, která je aktuálně vybrána na záložce **Řádky**. Velká část těchto informací se opakuje na záložce **Řádky** a lze je upravovat na obou místech. Zde jsou však k dispozici také další podrobnosti. Hodnoty dalších polí jsou založeny na nastavení příslušného vydaného produktu.

### <a name="settings-on-the-dimension-fasttab"></a>Nastavení na záložce Dimenze

Záložka **Dimenze** zobrazuje hodnoty pro všechny dostupné dimenze inventáře pro položku, která je vybrána na záložce **Řádky**, a to bez ohledu na dimenze, které jste se tam rozhodli zobrazit. Všechny zde zobrazené hodnoty pocházejí z příslušné šablony odhadu nákladů. V šabloně odhadu nákladů jsou volitelné.

### <a name="buttons-on-the-action-pane"></a>Tlačítka v podokně akcí

Tlačítka v podokně akcí na stránce **Odhady nákladů** můžete použít pro práci s vybraným odhadem nákladů. V následující tabulce jsou popsána dostupná tlačítka.

| Akce | popis |
|---|---|
| Dotaz na náklady | Zobrazí všechny náklady na cestu. Podle potřeby si můžete zobrazit náklady na úrovni jednotlivé položky. |
| Aktualizovat standardní náklady | <p>Aktualizujte standardní cenu pomocí výchozí verze výpočtu nákladů, která je definována ve stránce **Parametry nákladů za doručení**. Tuto verzi můžete přepsat.</p><p>**Poznámka:** Pokud má položka několik dimenzí položky (například různé velikosti, barvy a konfigurace), ale tyto dimenze nebyly pro odhad vybrány, vytvoří systém pro každou kombinaci nezpracovanou cenu.</p><p>**Důležité:** Vytvoří se rozpis ceny a použije se k určení standardní odchylky nákladů za doručení.</p> |
| Náklady na cestu | Zobrazte a upravte náklady na cestu pro veškeré zboží v zásilce. |
| Přepočítat | Aktualizujte odhadované náklady za doručení po aktualizaci, přidání nebo odebrání nákladů na cestu. |
| Uzamknout | Uzamkněte záznam odhadu nákladů, aby nebylo možné provádět žádné další změny. |

## <a name="item-cost-price-update"></a>Aktualizace nákladové ceny položky

Periodická úloha **Aktualizace nákladové ceny položky** aktualizuje všechny odhady nákladů, které odpovídají filtrům nastaveným při spuštění úlohy. Efekt je podobný účinku výběru možnosti **Aktualizovat standardní náklady** v podokně akcí pro jeden odhad. V tomto případě se však aktualizace vztahuje na všechny odpovídající odhady.

Pokud chcete spustit periodickou úlohu, postupujte takto:

1. Přejděte do uzlu **Náklady za doručení \> Periodické úlohy \> Aktualizace nákladové ceny položky**.
1. V dialogovém okně **Aktualizovat nákladovou cenu z odhadu** nastavte podle potřeby následující pole, abyste omezili rozsah aktualizace:

    - **Verze** - Aktualizujte pouze odhady, které používají zadanou verzi kalkulace.
    - **Místo** - Aktualizujte pouze odhady, které používají zadané místo.
    - **Šablona nákladů** - Aktualizujte pouze odhady, které používají zadanou šablonu.
    - **Do přístavu** - Aktualizujte pouze odhady, které používají zadaný přístav „do“.
    - **Předpokládané datum** - Aktualizujte pouze odhady, které mají zadané datum.

1. Nastavte možnosti na záložkách **Záznamy k zahrnutí** a **Spustit na pozadí** jako obvykle pro pravidelné úkoly.
1. Tlačítkem **OK** spustíte úlohu.

> [!NOTE]
> Tato periodická úloha se provede úspěšně pouze za předpokladu, že jsou k dispozici následující informace:
>
> - Každý relevantní produkt musí mít definovány údaje **Celková hloubka**, **Celková šířka** a **Celková výška**.
> - Každý příslušný dodavatel musí mít definován údaj **Z přístavu**.
