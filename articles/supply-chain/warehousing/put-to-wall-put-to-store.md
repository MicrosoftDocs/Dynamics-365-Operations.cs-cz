---
title: Umístění na zeď - umístění do obchodu
description: Toto téma obsahuje informace o funkci Umístění na zeď - umístění do obchodu. Tato funkce umožňuje zpracovat scénáře, ve kterých musíte produkt konsolidovat do pracovní oblasti předbalení na základě konfigurovatelných kritérií. Pomáhá zkrátit dobu výdeje, protože umožňuje výběry na jednu cílovou registrační značku a může používat více pozic umístění než cluster.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996267"
---
# <a name="put-to-wall---put-to-store"></a>Umístění na zeď - umístění do obchodu

[!include [banner](../includes/banner.md)]

Funkce *Umístění na zeď - umístění do obchodu* umožňuje zpracovat scénáře, ve kterých musíte produkt konsolidovat do pracovní oblasti předbalení na základě konfigurovatelných kritérií. Protože tato funkce umožňuje výběr na jednu cílovou registrační značku a může použít více umístěných pozic než výběr z clusteru, budou společnosti, které dodávají do obchodů nebo zpracovávají malé předměty, těžit ze zkrácené doby výběru.

Pracovní postup této funkce směruje vybraný produkt do třídicího místa pro distribuci do různých typů kontejnerů. Obecně platí, že každé třídicí místo zahrnuje více pozic řazení. Každá pozice řazení je přiřazena podle kritérií stanovených obchodním procesem. Typickými kritérii jsou konečný cíl, dodávka nebo vytížení. Poté, co produkt dorazí, je distribuován do každé pozice řazení podle množství, které je spojeno s objednávkou, místem určení, dodávkou nebo vytížením. Když je kontejner plný nebo kompletní, je přesunut do přechodného skladového místa nebo místa dodání pro další zpracování, v závislosti na obchodním procesu.

Tato skladovací funkce je také označována jinými jmény, jako je umístění na světlo a otevření přestávky.

## <a name="turn-on-the-outbound-sorting-feature"></a>Zapnutí funkce Odchozí třídění

Než budete moci použít funkci *Umístění na zeď - umístění do obchodu*, musí být v systému zapnutá funkce *Odchozí třídění*. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Odchozí třídění*

Funkci *Odchozí třídění* lze použít ve spojení s funkcí *Krokový kód široké vlny organizace*, pokud je zapnutá. Tuto funkci musíte zapnout také v případě, že budete používat předdefinované kódy, které jsou nastaveny v kódech kroků vlny. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Kód kroků vlny napříč organizací*

## <a name="setup"></a>Nastavení

Pro tuto ukázku jsou použita standardní data a sklad Contoso *62*. Používají se také některé dodatky, které jsou uvedeny později.

### <a name="location-type"></a>Typ umístění

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Typy umístění**.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se typ místa k třídění.
1. Nastavte následující hodnoty:

    - **Typ umístění:** *SORT*
    - **Popis:** *Seřadit*

1. Zvolte **Uložit**.

### <a name="warehouse-management-parameters"></a>Parametry řízení skladu

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Ka kartě **Obecné** na pevné záložce **Typy umístění** v poli **Typ místa třídění** zadejte *SORT*.
1. Zvolte **Uložit**.

### <a name="location-profile"></a>Profil umístění

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se typ profilu umístění pro umístění třídění.
1. V záhlaví nastavte následující hodnoty:

    - **ID profilu umístění:** *Třídění*
    - **Název:** *Třídění*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Formát skladového místa:** *PACK*
    - **Typ umístění:** *SORT*
    - **Použít sledování registrační značky:** *Ano*
    - **Povolit smíšené položky:** *Ano*
    - **Povolit smíšené stavy zásob:** *Ano*

1. Zvolte **Uložit**.

### <a name="locations"></a>Umístění

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.
1. Zrušte zaškrtnutí políčka **Generovat kontrolní číslice pro místo**.
1. V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:

    - **Sklad:** *62*
    - **Místo:** *Třídění*
    - **ID profilu umístění:** *Třídění*

1. Zvolte **Uložit**.

### <a name="packing-profiles"></a>Profily balení

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.
1. V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:

    - **ID profilu balení:** *Třídění*
    - **Popis:** *Seřadit*
    - **Zásady balení kontejnerů:** Toto pole nechte prázdné.
    - **Režim ID kontejneru:** *Automatický*
    - **Typ kontejneru:** *PALLET 48X48*
    - **Automaticky vytvořit kontejner při uzavření kontejneru:** Toto pole nechte prázdné.

1. Zvolte **Uložit**.

### <a name="wave-step-codes"></a>Kódy kroku vlny

Pokud jste zapnuli funkci *Kód širokého kroku vln organizace*, nastavte následující kód.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny**.
1. V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:

    - **Kód kroku vlny:** *Třídění*
    - **Popis kroku vlny:** *Třídění*
    - **Typ kroku vlny:** *Šablona třídění*

1. Zvolte **Uložit**.

### <a name="outbound-sorting-template"></a>Šablona odchozího třídění

Šablona třídění řídí, zda se vytvářejí pozice třídění, jaká kritéria se používají a další atributy procesu třídění.

1. Přejděte na **Řízení skladu \> Nastavení \> Balení \> Odchozí šablona třídění**.
1. V podokně Akce vyberte možnost **Nový** a vytvořte šablonu třídění.
1. V záhlaví nové šablony nastavte následující hodnoty:

    - **ID odchozí šablony třídění:** *Třídění vlny*
    - **Popis:** *Třídění vlny*
    - **Typ šablony třídění:** *Vlnová poptávka*

        Toto pole definuje proces, pro který se používá šablona třídění. K dispozici jsou následující hodnoty:

        - **Vlnová poptávka** -Šablona třídění se používá pro proces *Umístění na zeď*. Tento typ šablony slouží k obejití balicí stanice a zpracování zásob přímo mimo vlnu. Tento typ můžete použít pouze v případě, že je do šablony vlny zahrnuta metoda **třídění** vlny.
        - **Kontejner** - Šablona třídění se používá pro proces *Budova palety po zabalení*. Tento typ šablony slouží ke zpracování kontejnerů, které jsou uzavřené v balicí stanici, a je třeba je setřídit na palety.

    - **Sklad:** *62*
    - **Místo:** *Třídění*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Ověření řazení:** *Kontrola pozice*.

        Toto pole definuje ověření, které je vyžadováno během třídění. K dispozici jsou následující hodnoty:

        - Žádní
        - Skenování registrační značky
        - Skenování pozice

    - **Vytvořit práci při uzavření pozice:** *Ano*

        Když je tato možnost nastavená na *Ano* a pozice uzavřená, práce bude vytvořena, aby se přesunuly zásoby do konečného místa doručení. Když je nastavená na *Ne*, zásoby budou ihned přiděleny do objednávky při zavření pozice.

    - **Přiřazení pozice:** *Ruční*

        Toto pole definuje typ přiřazení pozice. K dispozici jsou následující hodnoty:

        - **Ruční** - uživatel musí vždy označit, do jaké pozice mají být zásoby setříděny.
        - **Automatický** -systém automaticky navede zásoby do pozice, kdykoli je to možné, na základě přestávek šablony třídění.

    - **Přiřadit kritéria pozice třídění:** *Použít pouze prázdnou pozici*

        Toto pole určuje, zda se při přiřazování zásob, které jsou už přítomny na pozici řazení, vezmou v úvahu zásoby, které již byly k dispozici. K dispozici jsou následující hodnoty:

        - **Použít pouze prázdné místo** - Budou brány v úvahu pozice, které již mají přidružené zásoby
        - **Předpokládejme, že je pozice prázdná** - Veškerý inventář, který je již v pozici, bude při přiřazování ignorován. Budou použity všechny dostupné pozice.

    - **Kód kroku vlny:** *Třídění*

        Pokud je zapnutá funkce *Kód kroku vlny pro celou organizaci*, musí být nastaven také kód vlnového kroku *Seřadit* v kódech vlnových kroků.

    - **Automaticky zavřít pozici třídění:** *Ano*

        Pokud je tato možnost nastavená na *Ano*, bude pozice při řazení automaticky zavřena po dokončení veškeré práce přicházející do pozice.

    - **Počet pozic třídění:** *3*

        Toto pole definuje maximální počet pozic třídění, které systém vytvoří.

    - **Předpona pozice třídění:** *SP-*

        Toto pole definuje předponu, kterou systém přiřadí před číslo pozice.

    - **Automaticky zabalit pozici třídění:** *Ano*

        Je-li tato možnost nastavená na *Ano*, budou zásoby na pozici třídění po uzavření pozice zabaleny do kontejneru.

    - **ID profilu balení:** *Třídění*

        Toto pole definuje profil balení, který se použije při zabalení pozice řazení do kontejneru.

1. V podokně akcí vyberte **Upravit dotaz** k určení kritérií, která se používají pro tuto šablonu třídění.
1. V dialogovém okně dotazu na kartě **Třídění** přidejte tlačítkem **Nový** řádek a pak nastavte následující hodnoty.

    - **Tabulka:** *Podrobnosti nákladu*
    - **Odvozená tabulka:** *Podrobnosti nákladu*
    - **Pole:** *ID dodávky*
    - **Směr hledání:** *Vzestupně*

1. Vyberte **OK**.
1. Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“ Vyberte **Ano**.

    Aktivuje se tlačítko **Zalomení odchozích šablon třídění** v podokně akcí.

1. V podokně akcí vyberte možnost **Zalomení odchozích šablon třídění**.
1. Zaškrtněte políčko **Seskupit podle pole** pro seskupení podle ID zásilky.

    Toto nastavení vytvoří jednu pozici třídění pro každou zásilku, která je kontejnerem ve vlně.

1. Vyberte **OK**.

### <a name="wave-process-methods"></a>Metody zpracování vlny

1. Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.
1. V podokně Akce vyberte možnost **Obnovit metody**.

    Metoda **třídění** je přidána do seznamu dostupných metod a je pro ni vybrán typ vlnové šablony *Expedice*.

### <a name="wave-templates"></a>Šablony vlny

Upravte vlnovou šablonu, která se používá pro třídění požadavků na vlnu.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V poli **Typ šablony vlny** vyberte *Expedice*.
1. Vyberte existující šablonu **Výchozí dodání 62**.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Obecné** proveďte následující změny:

    - Nastavte možnost **Zpracovat vlnu při uvolnění do skladu** na *Ne*.
    - Nastavte možnost **Přiřadit k otevřeným vlnám** na *Ano*.

1. Na pevné záložce **Metody** nastavte metodu **třídění**:

    1. V mřížce **Zbývající metody** vyberte **třídění**.
    2. Tlačítkem s šipkou doprava přesuňte metodu **třídění** do mřížky **Vybrané metody**.
    3. V mřížce **Vybrané metody** vyberte **třídění**.
    4. Nastavte hodnotu pole **Kód kroku vlny** na *Třídění*.

1. Zvolte **Uložit**.

### <a name="mobile-device-menu-items"></a>Položky nabídky mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Název položky nabídky:** *Třídění*
    - **Titul:** *Třídění*
    - **Režim:** *Nepřímý*
    - **Použít existující práci:** *Ne*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Kód aktivity:** *Odchozí třídění*
    - **Použít průvodce procesem:** *Ano* (výchozí hodnota)
    - **ID odchozí šablony třídění:** *Třídění vlny*

1. Zvolte **Uložit**.

### <a name="mobile-device-menu"></a>Nabídka mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V seznamu nabídek vyberte možnost **Odchozí**.
1. V podokně akcí vyberte **Upravit**.
1. V mřížce **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky **Třídění**, kterou jste právě vytvořili.
1. Stisknutím tlačítka se šipkou doprava přesuňte **Třídění** do mřížky **Struktura nabídky**. Tímto způsobem se přidá nová položka nabídky do nabídky **Odchozí**.
1. Zvolte **Uložit**.

### <a name="location-directives"></a>Směrnice skladového místa

Musíte vytvořit směrnice o umístění, které budou řídit práci vytvořenou po dokončení třídění.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V poli **Typ pořadí pracovních činností** vyberte možnost *Výběr seřazených zásob*.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Posloupnost:** *1*
    - **Název:** *Umístění k nákladním dveřím*

1. Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:

    - **Typ práce:** *Vložit*
    - **Lokalita:** *6*
    - **Sklad:** *62*
    - **Kód směrnice:** Toto pole nechte prázdné.
    - **Více skladových jednotek:** *Ne*

1. Chcete-li, aby byla dostupná záložka s náhledem **Řádky**, klikněte na **Uložit**.
1. Na pevné záložce **Řádky** vyberte **Nový** a pak nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Pořadové číslo:** *1*
    - **Od množství:** *0*
    - **Do množství:** *1000000*

1. Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa**, klikněte na **Uložit**.
1. Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Pořadové číslo:** *1*
    - **Název:** *Portál*

1. Vyberte možnost **Uložit**, chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na pevné záložce **Akce směrnice skladového místa**.
1. Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.
1. V dialogovém okně dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*. Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.
1. Úpravu potvrďte výběrem tlačítka **OK**.

### <a name="work-classes"></a>Pracovní třídy

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **ID pracovní třídy:** *Třídění*
    - **Popis:** *Třídění*
    - **Typ pracovního příkazu:** *Výběr tříděných zásob*

1. Zvolte **Uložit**.

### <a name="work-templates"></a>Šablony práce

1. Přejděte do nabídky Řízení skladu **Nastavení \> Práce \> Pracovní šablony**.
1. V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.
1. V mřížce vyberte pracovní šablonu **62 výdejů do balení**.
1. V podokně akcí vyberte **Zalomení pracovních hlaviček**.
1. V podokně akcí vyberte **Upravit**.
1. Na řádku, kde je pole **Název pole** nastaveno na *ID dodávky* zrušte zaškrtnutí políčka **Seskupit podle tohoto pole**.
1. Vyberte **Uložit** a zavřete dialogové okno **Zalomení pracovních hlaviček**.
1. V poli **Typ pořadí pracovních činností** vyberte možnost *Výběr seřazených zásob*.
1. Zvolte **Nová** pro vytvoření šablony práce.
1. V části **Přehled** nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Šablona práce:** *Seřazený výběr*
    - **Popis šablony práce:** *Seřazený výběr*

1. Chcete-li, aby byla dostupná část **Podrobnosti šablony práce**, klikněte na **Uložit**.
1. V části **Podrobnosti pracovní šablony** vytvoříte dva řádky. Klikněte na **Nový** a poté nastavte následující hodnoty pro řádek 1:

    - **Typ práce:** *Výdej*
    - **Povinné:** Vybráno (= *Ano*)
    - **ID pracovní třídy:** *Třídění*

1. Znovu klikněte na **Nový** a poté nastavte následující hodnoty pro řádek 2:

    - **Typ práce:** *Vložit*
    - **Povinné:** Vybráno (= *Ano*)
    - **ID pracovní třídy:** *Třídění*

1. Zvolte **Uložit**.

## <a name="example-scenario"></a>Příklad

Tento scénář simuluje situaci, kdy sklad ukládá malé položky na jednotlivých místech a musí je zabalit do krabic před odesláním a kde funkce balicí stanice není opravdu vhodná. Pracovníci vybírají objednávky pro více zákazníků a různé adresy současně, aby se zvýšila rychlost výběru. Po dokončení výdejů dorazí pracovníci na místo třídění, kde lze vybrané položky podle požadovaných kritérií třídit do správného pole. V tomto příkladu bude k určení správného pole použito ID zásilky, protože každá zásilka má jinou adresu. Poté, co jsou všechny položky z nákladu zabaleny a tříděny podle dodávky, budou krabice přesunuty do pracovní oblasti a nakonec naloženy na nákladní automobil.

Před zahájením scénáře se ujistěte, že všechny standardní funkce skladu jsou správně nastaveny pro váš sklad. Pro tento účel se používá standardní sklad Contoso *62*. Standardní konfigurace se nezměnily, kromě toho, co je popsáno v nastavení.

### <a name="create-demand"></a>Vytvoření poptávky

Předtím, než bude možné tuto funkčnost prokázat, musíte vytvořit určitou poptávku. V tomto scénáři vytvoříte tři prodejní objednávky pro tři různé zákazníky pro simulaci různých dodacích adres. Tímto způsobem vytvoříte tři samostatné zásilky.

Než začnete vytvářet prodejní objednávky a zásilky, zajistěte, aby skladová místa pro výdej měla dostatečné množství zásob pro všechny položky v objednávce. Zkontrolujte nastavení směrnice skladového místa pro určení, která výdejní skladová místa se použijí pro výdej prodejní objednávky. Pokud musíte upravit zásoby, můžete vytvořit ruční pohyby, použít doplnění nebo využít jakýkoli jiný tok. Pak rezervujte zásoby.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Výběrem možnosti **Nová** vytvořte prodejní objednávku pro objednávku 1.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Zákazník:** *US-001*
    - **Sklad:** *62*

1. Vyberte **OK**.
1. Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek. Nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *5*

1. Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *10*

1. Opakujte následující kroky pro každý řádek prodeje v objednávce, abyste pro ně vyhradili zásoby:

    1. Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.
    1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.
    1. Zvolte **Uložit**.

1. Výběrem možnosti **Nová** vytvořte prodejní objednávku pro objednávku 2.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Zákazník:** *US-004*
    - **Sklad:** *62*

1. Vyberte **OK**.
1. Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek. Nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *7*

1. Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *3*

1. Opakujte následující kroky pro každý řádek prodeje v objednávce, abyste pro ně vyhradili zásoby:

    1. Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.
    1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.
    1. Zvolte **Uložit**.

1. Výběrem možnosti **Nová** vytvořte prodejní objednávku pro objednávku 3.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Zákazník:** *US-007*
    - **Sklad:** *62*

1. Vyberte **OK**.
1. Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek. Nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *8*

1. Chcete-li rezervovat zásoby pro řádek prodejní objednávky, postupujte následovně:

    1. Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.
    1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.
    1. Zvolte **Uložit**.

Chcete-li uvolnit každou prodejní objednávku do skladu, proveďte následující postup. Budou vytvořeny tři různé zásilky. Poté přidáte všechny tři zásilky do jedné nové vlny.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V mřížce vyberte první prodejní objednávku, kterou jste vytvořili.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Zobrazí se informační zpráva, která uvádí ID vlny a ID objednávky, které byly vytvořeny.

1. Opakováním předchozích kroků uvolněte prodejní objednávky 2 a 3 do skladu. Všimněte si, že informační zpráva, kterou obdržíte, označuje, že zásilka byla přidána do vlny, která byla vytvořena při uvolnění prodejní objednávky 1.
1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte ID vlny, které bylo vytvořeno při uvolnění prodejních objednávek, k otevření stránky **Vlny**. Tato stránka zobrazuje podrobnosti o vlně. Na pevné záložce **Vlnové linie** se zobrazí zásilky, které byly vytvořeny.

    Nyní musíte vytvořit práci, která přinese položky z míst výběru do místa třídění.

1. V podokně akcí klikněte na možnost **Zpracovat**.

    Během zpracování vlny použije metoda třídění šablonu řazení k přiřazení inventáře k pozicím třídění. Po dokončení zpracování vlny obdržíte informační zprávu, která uvádí, že vlna byla zaúčtována a práce vytvořena.

1. V podokně akcí na kartě **Vlna** ve skupině **Související informace** vyberte **Práce** k zobrazení práce, která byla vytvořena pro tuto vlnu. Poznamenejte si ID práce.
1. Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.
1. V levém sloupci můžete zobrazit odchozí pozici třídění, která byla vytvořena pro každou zásilku.
1. Na pevné záložce **Seřadit kritéria pozice** můžete zobrazit ID zásilky pro tuto pozici.

Bylo vytvořeno jedno ID práce pro přenesení zásob z míst výběru do místa třídění. K dokončení práce budete potřebovat ID práce, které bylo vytvořeno během zpracování vlny.

### <a name="sales-order-picking-to-the-sorting-location"></a>Výběr prodejní objednávky do místa třídění

1. Přihlaste se do mobilní aplikace jako pracovník ve skladu *62*.
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Prodejní výdej**.
1. Vyberte pole **ID** a zadejte ID práce ze zpracování vlny.
1. Potvrďte zadání.

    Dále se zobrazí výzva k zadání cílové registrační značky (LP). Všimněte si, že řádek 1 z prodejní objednávky 1 je to, co musí být vybráno a přidáno na cílovou registrační značku. Zobrazí se číslo položky, množství, popis položky a místo výběru.

1. V poli **Cílová RZ** zadejte číslo registrační značky.

    Vyberete všechny řádky, které byly vytvořeny ze zpracované vlny, do stejné cílové poznávací značky.

1. Potvrďte zadání.

    Mobilní aplikace nyní představují řadu stránek **Výběr**, které vás nasměrují na místo výdeje a na položku a množství, které je třeba vybrat. Po přidání vybrané položky do poznávací značky potvrdíte výběr. Poslední stránkou bude práce umístění vybraných položek do místa třídění.

1. Potvrďte první práci vyskladnění.
1. Zobrazí se další práce vyskladnění. Potvrďte vyskladnění.
1. Pokračujte v potvrzení zbývající práce vyskladnění.
1. Posledním krokem je dokončení práce vložení. Potvrďte odložení do místa třídění.

    Zobrazí se zpráva „Práce dokončena“.

1. Ukončete **prodejní výběr** v mobilní aplikaci.

### <a name="sortingput-to-wall"></a>Třídění / umístění na zeď

Nyní, když byly veškeré zásoby vloženy do místa třídění, musí být roztříděny do správné pozice třídění.

1. Přihlaste se do mobilní aplikace.
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Třídit** pro zahájení třídění položek.
1. V poli **LP / CON** zadejte cílovou poznávací značku práce s vybranou prodejní objednávkou.
1. Potvrďte zadání.
1. Nejprve zadejte číslo položky k třídění.
1. Systém určuje první polohu řazení, která by měla být zobrazena. Potvrďte polohu třídění.
1. Budete vyzváni k přiřazení registrační značky k pozici třídění. Vyberte pole **RZ**, zadejte číslo registrační značky a potvrďte zadání.

    Protože pozice třídění souvisí s ID dodávky, roztřídíte vybrané položky seřadíte do registrační značky, která je specifická pro odchozí zásilku a prodejní objednávku.

    Na další stránce jsou uvedeny hodnoty ID položky, množství, ID pozice třídění a ID registrační značky "od" (výběr) a "do" (třídění). Informace na této stránce vás vyzývají k třídění zadané položky a množství z registrační značky výběru do registrační značky třídění.

1. Potvrďte polohu třídění.
1. Seřaďte položky na první pozici třídění. Po dokončení vás systém přesměruje na další pozici třídění.
1. Tento postup opakujte pro všechny vybrané řádky v pracovním příkazu. Tento proces byste také měli použít, pokud existuje více řádků vyskladnění, které mají stejné číslo položky.

    Když tento proces opakujete pro všechny položky, systém vyhodnotí kritéria z další naskenované položky (pracovní linky) a určí, do které pozice se má třídit. Budete automaticky nasměrováni, abyste položku umístili na správnou pozici. V závislosti na nastavení potvrzení budete také vyzváni k potvrzení této akce zadáním čísla pozice nebo ID registrační značky.

    > [!NOTE]
    > Pokud je zapnuto automatické třídění, není ruční přepsání k dispozici.

1. Až skončíte, v Microsoft Dynamics 365 Supply Chain Management otevřete stránku **Přiřazení pozice odchozího třídění** a zkontrolujte stav pozic.

    - Pokud jsou pozice zavřené automaticky, vyberte **Zobrazit uzavřené** k zobrazení uzavřených pozic.
    - Všimněte si, že jsou zobrazeny transakce pozic třídění. Zobrazí se položka a množství, které byly zpracovány prostřednictvím pozice.

    Když nastavíte šablonu pro odchozí třídění, nastavte možnost **Automaticky zavřít pozici třídění** na *Ano*. Pozice se proto automaticky uzavře po uložení posledních očekávaných zásob. Pozice třídění jsou ve stavu **Zavřeno** a byla vytvořena práce na přesunutí tříděného inventáře do umístění k *nákladovým dveřím*.

1. Dokončete práci výběru tříděných zásob a přesuňte zásoby do místa dodání. Až budou zásoby připravené, potvrďte jejich odeslání.

> [!NOTE]
> Aby byly práce výběru seřazených zásob správně zpracována, měla by pro proces pohybu a naložení položka nabídky mobilního zařízení, která má ID pracovní třídy, kde je pole **Typ pracovního příkazu** nastaveno na *Seřazený výběr zásob*.

### <a name="manually-close-a-position-optional"></a>Ruční uzavření pozice (volitelné)

Pokud by se měly pozice třídění uzavřít ručně, musí být možnost **Automaticky zavřít pozici třídění** pro šablonu odchozího třídění nastavena na *Ne* a uzavření musí být provedeno před přesunutím zásob do oblasti nákladové brány. Pozice lze uzavřít různými způsoby:

- Prostřednictvím skladové aplikace:

    - Uživatel může naskenovat jednu z položek, které jsou již na dané pozici, a poté vybrat **Zavřít** pro uzavření pozice.
    - Pokud uživatel prohledá kontejner, který již byl roztříděn, zobrazí se chybová zpráva. Uživatel však stále může pokračovat k zavření pozice.

- Ze stránky Microsoft Dynamics 365 Supply Chain Management **Přiřazení pozice odchozího třídění**:

    - Uživatel si může vybrat záznam pozice odchozího třídění a poté vybrat **Zavřít pozici** v podokně akcí.

## <a name="tips"></a>Tipy

- Položky nemohou být přesouvány mezi pozicemi poté, co byly přiřazeny k jedné z nich. Systém vyhodnotí, jaké množství jednotlivého zboží by mělo jít na konkrétní pozici.
- Šablonu třídění lze nakonfigurovat tak, aby automaticky vytvořila kontejnery po uzavření pozic. Tento přístup vytvoří standardní strukturu ID kontejneru, která je založena na určeném profilu balení.

> [!IMPORTANT]
> Po vytvoření pohybu z místa třídění nesmíte práci zrušit. V opačném případě bude pozice a kontejnery v ní odstraněny ze systému a nebudou k dispozici pro další zpracování. Budou odstraněny rovněž zásoby.
