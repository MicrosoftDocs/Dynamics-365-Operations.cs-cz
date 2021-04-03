---
title: Plánovaný cross docking
description: Toto téma popisuje cross docking s rozšířeným plánováním, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti. Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556259"
---
# <a name="planned-cross-docking"></a>Cross docking s plánováním

[!include [banner](../includes/banner.md)]

Toto téma popisuje cross docking s rozšířeným plánováním. Cross docking s rozšířeným plánováním je skladový proces, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti. Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.

Cross docking umožňuje pracovníkům přeskočit zaskladnění zásob na vstupu a jejich výdej na výstupu, když jsou již zásoby označeny pro výstupní objednávku. Tím se všude tam, kde je to možné, minimalizuje počet operací se zásobami. Protože se redukuje množství interakce se systémem, lze též dosáhnout dalších časových i prostorových úspor ve skladu.

Před spuštěním cross dockingu musí uživatel nakonfigurovat novou šablonu pro cross docking, jež bude splňovat požadavky na zdroj dodávky a další. Po vytvoření odchozí objednávky musí být řádek označen proti příchozí objednávce obsahující stejnou položku.

V době přijetí příchozí objednávky nastavení cross dockingu automaticky identifikuje potřebu cross dockingu a na základě nastavení směrnice skladového místa vytvoří příslušný pohyb pro požadované množství.

> [!NOTE]
> U transakcí se zásobami se **neprovede** zrušení registrace, je-li zrušena crossdockingová úloha, a to ani v případě, že je nastavení této funkcionality v parametrech správy skladu zapnuto.

## <a name="turn-on-the-planned-cross-docking-features"></a>Zapnutí funkcí Cross docking s plánováním

Pokud váš systém ještě neobsahuje funkce popsané v tomto tématu, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapínejte následující funkce v následujícím pořadí:

1. *Plánovaný cross docking*
2. *Šablony cross dockingu se směrnicemi skladového místa*

## <a name="setup"></a>Nastavení

### <a name="regenerate-load-posting-methods"></a>Obnovte metody účtování nákladu

Cross docking s plánováním se implementuje jako metoda účtování nákladu. Po zapnutí funkce je nutné obnovit metody.

1. Přejděte do **Řízení skladu \> Nastavení \> Metody účtování nákladů**.
1. V podokně Akce vyberte možnost **Obnovit metody**.

    Po dokončení obnovy byste měli vidět metodu, jež má v poli **Název metody** hodnotu *planCrossDocking*.

1. Zavřete stránku.

### <a name="create-a-cross-docking-template"></a>Vytvoření šablony cross dockingu

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Šablony cross dockingu**.
1. V podokně Akce vyberte možnost **Nový** a vytvořte šablonu.
1. V záhlaví nastavte následující hodnoty:

    - **Posloupnost:** *1*

        Toto pole definuje pořadí, ve kterém budou šablony vyhodnocovány.

    - **ID šablony cross dockingu:** *51*
    - **Popis:** *Sklad 51*
    - **Zásady uvolnění poptávky:** *Před přijetím dodávky*
    - **Sklad:** *51*

1. Fungování šablony určuje nastavení na záložce s náhledem **Plánování**. Nastavte následující hodnoty:

    - **Požadavky poptávky:** *Žádné*

        Toto pole určuje požadavky poptávky na zásoby. Pokud musí být poptávka před uvolněním spojena s dodávkou, vyberte možnost *Označení*. Pokud musí být poptávka před uvolněním rezervována na základě objednávky, vyberte možnost *Rezervace objednávky*.

    - **Typ vyhledávání:** *Umístění dodávky*

        Toto pole definuje, zda by měla práce cross dockingu používat přípravná/nákladová skladová místa z dodávky, případně zda by měla používat směrnice skladového místa a na jejich základě vyhledat vlastní přípravná/nákladová skladová místa.

    - **Šablona práce:** Toto pole ponechte prázdné.

        Toto pole definuje šablonu práce, která by měla být použita při vytváření práce cross dockingu.

    - **Znovu ověřit při přijetí dodávky:** *Ne*

        Tato volba určuje, zda má být dodávka během příjmu znovu ověřena. Pokud je u této možnosti nastavena hodnota *Ano*, proběhne kontrola maximálního časového úseku i počtu dní vypršení platnosti.

    - **Kód směrnice** Toto pole nechte prázdné.

        Tato možnost umožňuje systému používat direktivy umístění, aby pomohla určit nejlepší umístění pro přesun zásob cross-docking. Můžete jej nastavit přiřazením kódu direktivy ke každé příslušné šabloně cross-dockingu. Každý kód direktivy označuje jedinečnou direktivu umístění.

    - **Ověření časového úseku:** *Ano*

        Tato možnost určuje, zda se má vyhodnocovat maximální časový úsek, když dojde k výběru zdroje dodávky. Pokud je u této možnosti zadána hodnota *Ano*, budou k dispozici pole týkající se maximálního a minimálního časového úseku.

    - **Maximální časový úsek:** *5*

        Toto pole určuje maximální období, jež smí uplynout mezi doručením dodávky a odesláním poptávky.

    - **Jednotka maximálního časového úseku:** *Dny*
    - **Minimální časový úsek:** *0*

        Toto pole určuje minimální období, jež smí uplynout mezi doručením dodávky a odesláním poptávky.

    - **Jednotka minimálního časového úseku:** *Dny*
    - **Rozsah dnů vypršení platnosti:** *0*

        *Kritéria FEFO (First expiry first out):* Toto pole určuje maximální počet dní mezi datem expirace šarže, která vyprší jako první, jež je aktuálně ve skladu, a šarží, která je přijímána.

1. Na záložce s náhledem **Zdroje dodávek** se určují typy dodávek, které jsou pro tuto šablonu platné. Klikněte na **Nový** a poté nastavte následující hodnoty:

    - **Pořadové číslo:** *1*
    - **Zdroj dodávky:** *Nákupní objednávka*

### <a name="create-a-work-class"></a>Vytvoření pracovní třídy

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.
1. V podokně Akce vyberte možnost **Nový** a vytvořte třídu práce.
1. Nastavte následující hodnoty:

    - **ID pracovní třídy:** *CrossDock*
    - **Popis:** *Cross Dock*
    - **Typ pracovního příkazu:** *Cross docking*

### <a name="create-a-work-template"></a>Vytvoření šablony práce

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V poli **Typ pracovního příkazu** nastavte možnost *Cross docking*.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do tabulky **Přehled**.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** *1*
    - **Šablona práce:** *51 Cross Dock*
    - **Popis šablony práce:** *51 Cross Dock*

1. Chcete-li, aby byla dostupná záložka s náhledem **Podrobnosti šablony práce**, klikněte na **Uložit**.
1. Na záložce s náhledem **Podrobnosti šablony práce** přidejte řádek do mřížky výběrem možnosti **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Typ práce:** *Výdej*
    - **ID pracovní třídy:** *CrossDock*

1. Chcete-li přidat další řádek, klikněte znovu na **Nový** a zadejte následující hodnoty:

    - **Typ práce:** *Vložit*
    - **ID pracovní třídy:** *CrossDock*

1. Vyberte **Uložit** a ujistěte se, že máte zaškrtnuté políčko **Platné** pro šablonu *51 Cross Dock*.

> [!NOTE]
> ID třídy práce pro typy práce *Výdej* a *Zaskladnění* se musí shodovat.

### <a name="create-location-directives"></a>Vytvoření směrnic skladového místa

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně nastavte v poli **Typ pracovního příkazu** hodnotu *Cross docking*.
1. V podokně Akce klikněte na **Nový** a poté nastavte následující hodnoty:

    - **Pořadové číslo:** *1*
    - **Název:** *51 Cross Dock Put*
    - **Typ práce:** *Vložit*
    - **Lokalita:** *5*
    - **Sklad:** *51*

1. Chcete-li, aby byla dostupná záložka s náhledem **Řádky**, klikněte na **Uložit**.
1. Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Od množství:** *1*
    - **Do množství:** *1000000*

1. Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa**, klikněte na **Uložit**.
1. Na záložce s náhledem **Akce směrnice skladového místa** přidejte řádek do mřížky výběrem možnosti **Nová**.
1. Na novém řádku nastavte následující hodnoty:

    - **Název:** *Portál*
    - **Využití pevného skladového místa:** *Pevná a nepevná skladová místa*

1. Vyberte možnost **Uložit**, chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na nástrojové liště **Akce směrnice skladového místa**.
1. Vyberte **Upravit dotaz**, otevře se editor dotazů.
1. Ujistěte se, že jsou na kartě **Oblast** nakonfigurovány následující dva řádky:

    - Řádek 1:

        - **Tabulka:** *umístění*
        - **Odvozená tabulka:** *Skladová místa*
        - **Pole:** *Sklad*
        - **Kritéria:** *51*

    - Řádek 2:

        - **Tabulka:** *umístění*
        - **Odvozená tabulka:** *Skladová místa*
        - **Pole:** *Skladové místo*
        - **Kritéria:** *Portál*

1. Vyberte **OK** a editor dotazu zavřete.

### <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V seznamu položek nabídky v levém podokně vyberte **Nákupní vyskladnění**.
1. Vyberte možnost **Upravit**.
1. Na záložce s náhledem **Pracovní třídy** přidejte řádek do mřížky výběrem možnosti **Nová**.
1. Na novém řádku nastavte následující hodnoty:

    - **ID pracovní třídy:** *CrossDock*
    - **Typ pracovního příkazu:** *Cross docking*

1. Zvolte **Uložit**.

## <a name="scenario"></a>Scénář

### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

Pomocí následujících kroků vytvořte objednávku jako zdroj dodávky.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:

    - **Účet dodavatele:** *104*
    - **Sklad:** *51*

1. Vybrat **OK** a poznamenejte si číslo objednávky.
1. Na záložce s náhledem **Řádky objednávky** se přidá nový řádek. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *5*

### <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku

Pomocí následujících kroků vytvořte prodejní objednávku jako zdroj poptávky.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-002*
    - **Sklad:** *51*

1. Vyberte **OK**.
1. Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *3*

### <a name="create-planned-cross-docking"></a>Vytvoření cross dockingu s plánováním

Pomocí těchto kroků vytvořte z prodejní objednávky cross docking s plánováním.

1. Na stránce **Podrobnosti prodejní objednávky** pro prodejní objednávku, kterou jste právě vytvořili, vyberte v podokně Akce na kartě **Sklad** ve skupině **Akce** položku **Uvolnění do skladu**.

    Akce uvolnění do skladu vytvoří řádek dodávky a nákladu pro řádek prodejní objednávky. Pokusí se také o přidělení zásob.
    
    Zobrazí se informační zpráva. Zobrazí se také následující varovná zpráva: „Pro vlnu XXXX nebyla vytvořena žádná práce. Podrobnosti najdete v protokolu historie vytváření práce.“ Toto chování je očekávané, protože ve skladu nejsou žádné zásoby.

1. Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Sklad** vyberte možnost **Podrobnosti dodávky**.

    Zobrazí se stránka **Podrobnosti dodávky**, na níž je dodávka, která byla vytvořena pro prodejní objednávku.

1. Na záložce s náhledem **Řádky nákladu** si všimněte, že je v poli **Množství pro cross docking s plánováním** zadána hodnota *3*. Protože ve skladu nebyly žádné zásoby, ale platný zdroj dodávky dorazí během časového úseku definováno v šabloně cross dockingu, bylo vytvořeno množství pro cross docking.
1. Na záložce s náhledem **Řádky nákladu** vyberte položku **Cross docking s plánováním**. Zobrazí se podrobnosti vytvořeného cross dockingu.

## <a name="process-the-cross-docking"></a>Zpracování cross dockingu

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Přijetí nákupní objednávky ve skladové mobilní aplikaci

Systém obdrží množství 5 z nákupní objednávky do přijímacího skladového místa a vytvoří dvě různé práce.

První ID práce, jež vznikne, má v poli **Typ pracovního příkazu** hodnotu *Cross docking* a souvisí s prodejní objednávkou. Obsahuje množství 3 a je směrováno do skladového místa konečného dodání, takže lze dodávku okamžitě expedovat.

Druhé ID práce, jež vznikne, má v poli **Typ pracovního příkazu** hodnotu *Nákupní objednávky* a souvisí s nákupní objednávkou. Má zbývající množství 2, které neprošlo cross dockingem a je nasměrováno k zaskladnění na skladové místo.

1. Přihlaste se do mobilního zařízení pro uživatele ve skladu *51*.
1. Přejděte do **Vstupní \> Příjem nákupu**.
1. V poli **Č. nákup. obj.** zadejte číslo nákupní objednávky.
1. Do pole **Množ.** zadejte hodnotu *5*.
1. Vyberte **OK**.
1. Na další stránce nastavte u pole **Položka** hodnotu *A0001*.
1. Vyberte **OK**.
1. Na další stránce potvrďte hodnoty **Č. nákup. obj.**, **Položka**, a **Množ.** kliknutím na **OK**.

    Zobrazí se zpráva „Práce dokončena“.

1. Kliknutím na **Storno** okno opusťte.

### <a name="put-away-to-cross-docking-and-bulk"></a>Zaskladnění na cross docking a hromadné skladové místo

V současné době mají obě ID práce stejnou cílovou registrační značku. Chcete-li provést další kroky, musíte získat ID práce a ID cílové registrační značky. Tyto informace můžete získat z podrobností práce k řádku nákupní objednávky a z řádku prodejní objednávky. Alternativně můžete přejít do **Řízení skladu \> Práce \> Podrobnosti práce**. Vyfiltrujte si pouze práce, kde je u položky **Sklad** hodnota *51*.

1. Na mobilním zařízení přejděte na **Vstupní \> Zaskladnění nákupu** a zadejte cílovou registrační značku podle práce.
1. Do pole **ID** zadejte ID cílové registrační značky z podrobností práce.

    Stránka výdeje pomocí cross dockingu zobrazuje místo výdeje (*RECV*), cílovou registrační značku (*registrační značka*), položku (*A0001*) a množství (*3*).

1. Vyberte **OK**.
1. V poli **Cílová LP** zadejte cílovou registrační značku pro ID registrační značky, jež by měla být zaskladněna (cross docking) na skladové místo pro dodávku. Můžete vybrat libovolné ID registrační značky dle svého výběru.
1. Vyberte **OK**.
1. Na následující stránce zadejte do pole **ID** ID cílové registrační značky.
1. Vyberte **OK**.
1. Potvrďte práci pro výdej zbývajícího množství 2 a poté klikněte na **OK**.
1. Na další stránce klikněte na **Hotovo**. Tím ukončíte proces výdeje a zahájíte proces zaskladnění.

    Mobilní aplikace vám poskytne skladové místo a registrační značku, do níž chcete položku umístit.

1. Potvrďte hromadné úložiště pro **Zaskladnění** kliknutím na **OK**.
1. Na další stránce potvrďte cross docking **Zaskladnění** kliknutím na **OK**.

    Zobrazí se zpráva „Práce dokončena“.

1. Kliknutím na **Storno** okno opusťte.

Následující obrázek ukazuje, jak by se dokončená práce cross dockingu mohla v systému Microsoft Dynamics 365 Supply Chain Management zobrazit.

![Práce cross docking dokončena](media/PlannedCrossDockingWork.png "Práce cross docking dokončena")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]