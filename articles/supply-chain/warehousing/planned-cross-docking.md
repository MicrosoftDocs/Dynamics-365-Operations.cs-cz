---
title: Plánovaný cross docking
description: Tento článek popisuje cross docking s rozšířeným plánováním, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti. Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: b530cc1403458775fd330e826a32417d3b03bf25
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334558"
---
# <a name="planned-cross-docking"></a>Cross docking s plánováním

[!include [banner](../includes/banner.md)]

Tento článek popisuje cross docking s rozšířeným plánováním. Cross docking s rozšířeným plánováním je skladový proces, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti. Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.

Cross docking umožňuje pracovníkům přeskočit zaskladnění zásob na vstupu a jejich výdej na výstupu, když jsou již zásoby označeny pro výstupní objednávku. Tím se všude tam, kde je to možné, minimalizuje počet operací se zásobami. Protože se redukuje množství interakce se systémem, lze též dosáhnout dalších časových i prostorových úspor ve skladu.

Před spuštěním cross dockingu musíte nakonfigurovat novou šablonu pro cross docking, jež bude splňovat požadavky na zdroj dodávky a další. Po vytvoření odchozí objednávky musí být řádek označen proti příchozí objednávce obsahující stejnou položku. Můžete vybrat pole kódu směrnice v šabloně cross-dockingu, podobně jako u způsobu nastavení objednávek doplňování a nákupu.

V době přijetí příchozí objednávky nastavení cross dockingu automaticky identifikuje potřebu cross dockingu a na základě nastavení směrnice skladového místa vytvoří příslušný pohyb pro požadované množství.

> [!NOTE]
> U transakcí se zásobami se *neprovede* zrušení registrace, je-li zrušena crossdockingová úloha, a to ani v případě, že je nastavení této funkcionality v parametrech správy skladu zapnuto.

## <a name="turn-on-the-planned-cross-docking-features"></a>Zapnutí funkcí Cross docking s plánováním

Pokud používáte Supply Chain Management verze 10.0.28 nebo starší, možná budete muset povolit plánovaný cross docking, než jej budete moci používat. Přejděte na [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce v následujícím pořadí:

1. *Plánovaný cross docking*<br>(Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout.)
1. *Šablony cross dockingu se směrnicemi skladového místa*<br>(Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta.)
    > [!NOTE]
    > Tato funkce umožňuje zadat pole **Kód směrnice** v šabloně cross dockingu, podobně jako při nastavování šablon doplňování. Povolení této funkce vám zabrání v přidání kódu směrnice na řádky pracovní šablony cross dockingu pro finální řádek *Vložit*. Tím je zajištěno, že konečné umístění vložení lze určit během vytváření práce před zvážením pracovních šablon.

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

    - **Kód směrnice:** Toto pole nechte prázdné

        Tato možnost je povolena pomocí funkce *Šablony cross dockingu se směrnicemi skladového místa* (od verze Supply Chain Management verze 10.0.29 je tato funkce ve výchozím nastavení zapnuta). Systém využívá směrnice umístění k určování nejlepšího umístění pro přesun zásob cross-docking. Můžete jej nastavit přiřazením kódu direktivy ke každé příslušné šabloně cross-dockingu. Pokud je nastaven kód šablony, systém nebude při generování práce hledat směrnice skladového místa podle kódu směrnice. Tímto způsobem můžete omezit směrnice umístění, které se používají pro konkrétní šablonu cross dockingu.

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

> [!NOTE]
> Můžete určit dotaz pro řízení toho, kdy dojde k použití určité šablony cross dockingu. Dotaz na šablony cross dockingu má pouze tabulku *InventTable* (položky) a vnitřní spojení s tabulkou *WHSInventTable* (položky WMS). Pokud chcete do dotazu přidat další tabulky, můžete se k nim připojit pouze pomocí spojení *existuje* nebo *neexistuje*. Když filtrujete záznamy na spojených tabulkách, načte se záznam z hlavní tabulky pro každý odpovídající záznam ve spojené tabulce. Pokud je typ spojení *existuje*, hledání skončí po nalezení první shody. Pokud například připojíte tabulku řádku prodejní objednávky k tabulce položek, systém ověří a vrátí položky, pro které má definovanou podmínku alespoň jeden řádek prodejní objednávky. V zásadě jsou data načítána z nadřazené tabulky (položek), nikoli z podřízené tabulky (řádek prodejní objednávky). Filtrování podle zdrojových dokumentů, jako jsou řádky prodejní objednávky nebo zákazníci, proto nelze provést ihned bez úprav.

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
1. Volitelné: Vyberte příkaz **Upravit dotaz** chcete-li nastavit kritéria pro řízení toho, kdy a kde se používá šablona práce.

    Můžete určit dotaz pro řízení toho, kdy dojde k použití určité šablony práce. Můžete například určit, že šablonu lze použít pouze pro práci na konkrétním místě. Pokud chcete, aby se šablona práce cross dockingu použila na konkrétním místě, musíte filtrovat podle pole **Počáteční poloha**, nikoli **Umístění**, protože vytvoření práce pro příchozí procesy (nákup, cross docking a doplňování) začíná od řádku vložení. Když je vytvořena práce, direktiva umístění nastaví pole **Umístění** na umístění vložení. Místo vyzvednutí je však uloženo v poli **Počáteční poloha**.

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

![Práce cross docking dokončena.](media/PlannedCrossDockingWork.png "Práce cross docking dokončena")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
