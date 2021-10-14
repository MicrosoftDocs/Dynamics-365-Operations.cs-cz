---
title: Umístění registrační značky místa
description: Určení pozice registrační značky na skladovém místě umožňuje zjistit, kde se registrační značka nachází na skladovém místě pro více palet, například na skladovém místě využívajícím regály o hloubce na dvě palety.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: c19f8dcdb7d84b752e0eec56afdb1a1865cfe00b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567600"
---
# <a name="location-license-plate-positioning"></a>Umístění registrační značky místa

[!include [banner](../includes/banner.md)]

Určení pozice registrační značky na skladovém místě umožňuje zjistit, kde se registrační značka nachází na skladovém místě pro více palet, například na skladovém místě využívajícím regály o hloubce na dvě palety.

Tato funkce přidá pořadové číslo ke každé registrační značce vložené na skladové místo. Toto pořadové číslo se používá k řazení registračních značek na skladovém místě. Tato funkce proto inteligentně podporuje scénáře, kdy odběratelé používají gravitační regálový systém, a proto musí pro účely výdeje vědět, která registrační značka směřuje vpřed.

Toto téma představuje scénář, který ukazuje, jak tuto funkci nastavit a používat.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Zapnutí funkce Určení pozice registrační značky na skladovém místě

Než můžete použít funkci Určení pozice registrační značky na skladovém místě, musíte ji v systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Určení pozice registrační značky na skladovém místě*

## <a name="example-scenario"></a>Příklad

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí hodnot navržených v tomto tématu, musíte používat systém, ve kterém jsou nainstalována ukázková data. Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

### <a name="set-up-the-feature-for-this-scenario"></a>Nastavení funkce pro tento scénář

Chcete-li nastavit funkci *Určení pozice registrační značky na skladovém místě* pro scénář, který je uveden v tomto tématu, proveďte následující procedury.

#### <a name="location-profiles"></a>Profily umístění

Funkci je nutné zapnout v profilu skladového místa pro každé skladové místo, kde má být použita.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. V seznamu profilů skladových míst v levém podokně vyberte možnost **HROMADNÝ-06**.
1. Na záložce s náhledem **Všeobecné** byly k funkci přidány dvě nové možnosti. Nastavte následující hodnoty:

    - **Povolit určení polohy registrační značky:** *Ano*

        Když je u této možnosti vybrána hodnota *Ano*, pozice registrační značky bude zachována pro registrační značky na daném skladovém místě.

    - **Zobrazit pozici LP mobilního zařízení:** *Ano*

        Pokud je u této možnost vybrána hodnota *Ano*, bude se uživatelům mobilních zařízení během úprav a inventur pozice registrační značky zobrazovat. Nastavení této možnosti můžete změnit, pouze když je funkce zapnutá.

1. Zvolte **Uložit**.

#### <a name="location-directives"></a>Směrnice skladového místa

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně zkontrolujte, zda je v poli **Typ pracovního příkazu** nastavena hodnota *Prodejní objednávky*.
1. V seznamu směrnic skladového místa vyberte možnost **61 SO výdejová objednávka**.
1. V podokně akcí vyberte **Upravit**.
1. Na záložce s náhledem **Řádky** vyberte řádek, který má v poli **Pořadové číslo** hodnotu *2*.
1. Na záložce s náhledem **Akce směrnice skladového místa** vyberte řádek, který má hodnotu **Název** u možnosti *Výdej méně než palety* (mělo by se jednat o jediný takový řádek) a změnit u něj hodnotu v poli **Pořadové číslo** na *2*.
1. Klikněte nad mřížkou na **Nový**, přidá se řádek pro novou akci směrnice skladového místa.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** *1*
    - **Název:** *Výdejová pozice 1*

1. Dokud je ještě nový řádek vybrán, klikněte na **Upravit dotaz** nad mřížkou.
1. V editoru dotazů klikněte na kartu **Spojení**.
1. Rozbalte spojení tabulky **Skladová místa**, zobrazí se spojení tabulky **Dimenze zásob**.
1. Rozbalte spojení tabulky **Dimenze zásob**, zobrazí se spojení tabulky **Zásoby na skladě**.
1. Vyberte **Dimenze zásob** a poté možnost **Přidat spojení tabulek**.
1. V zobrazeném seznamu tabulek vyberte ve sloupci **Vztah** hodnotu **Registrační značka (registrační značka)**. Poté vyberte možnost **Vybrat** a přidejte **Registrační značku** do spojení tabulek **Dimenze zásob**.
1. Dokud ještě máte vybranou **Registrační značku**, vyberte možnost **Přidat spojení tabulek**.
1. V zobrazeném seznamu tabulek vyberte ve sloupci **Vztah** hodnotu **Určení pozice registrační značky (registrační značka)**. Poté vyberte možnost **Vybrat** a přidejte **Určení pozice registrační značky** do spojení tabulek **Dimenze zásob**.

    ![Spojení tabulek.](media/LpTableJoin.png "Spojení tabulek")

1. Potvrďte aktualizované spojené tabulky kliknutím na **OK** a zavřete editor dotazů.
1. Na pevné záložce **Akce směrnice skladového místa** znovu vyberte **Upravit dotaz** a znovu otevřete editor dotazů.
1. Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *Určení pozice registrační značky na skladovém místě*
    - **Odvozená tabulka:** *Určení pozice registrační značky na skladovém místě*
    - **Pole:** *Pozice LP*
    - **Kritéria:** *1*

    ![Nová oblast.](media/LpPositionCriteria.png "Nová oblast")

1. Výběrem **OK** potvrďte změny a zavřete editor dotazů.

### <a name="set-up-sample-data-for-this-scenario"></a>Nastavení ukázkových dat pro tento scénář

Pro tento scénář se musí uživatel přihlásit ke skladové mobilní aplikaci jako pracovník, který je oprávněn podle nastavení provádět práci ve skladu *61*. Uživatel musí také dokončit transakce.

Protože funkce *Určení pozice registrační značky na skladovém místě* přidá nový identifikátor pro pozice registrační značky na skladovém místě, musíte nejprve vytvořit některá data, jež tento scénář podporují.

#### <a name="spot-count-the-first-location"></a>Inventura prvního skladového místa

1. Otevřete skladovou mobilní aplikaci a přihlaste se do skladu *61*.
1. Přejděte na **Zásoby \> Inventura**.
1. Na stránce **Inventura** nastavte v poli **Skladové místo** hodnotu *01A01R1S1B*.
1. Vyberte **OK**.

    Na stránce se zobrazuje zadané skladové místo. Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“

1. Vyberte **Obnovit**, chcete-li přidat pro dané skladové místo množství.
1. Na stránce **Cyklická inventura: přidání nové LP nebo položky** vyberte pole **Položka** a zadejte hodnotu *A0001*.
1. Vyberte **OK**.
1. Na stránce **Cyklická inventura: Přidání nové LP nebo položky** zadejte do pole **LP** hodnotu *LP1001* (nebo jakékoli jiné číslo registrační značky podle vaší volby).

    Na stránce **Cyklická inventura: Přidání nové LP nebo položky** se zobrazí **Pozice registrační značky 1**.

1. Vyberte **OK**.

    Nyní musíte určit množství položek, jež se pro registrační značku počítá.

1. Nastavte v poli **Množ.** hodnotu *10*.
1. Vyberte **OK**.

    Na stránce se zobrazuje zadané skladové místo. Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“

1. Vyberte **Obnovit**, chcete-li přidat pro dané skladové další místo množství.
1. Na stránce **Cyklická inventura: přidání nové LP nebo položky** vyberte pole **Položka** a zadejte hodnotu *A0002*.
1. Vyberte **OK**.
1. Na stránce **Cyklická inventura: Přidání nové LP nebo položky** vyberte pole **LP** a zadejte hodnotu *LP1002* (nebo jakékoli jiné číslo registrační značky dle vašeho výběru. Podmínkou je, že se číslo musí lišit od čísla registrační značky, které jste zadali dříve).
1. Změňte pozici registrační značky zadáním hodnoty **2** do pole *Pozice LP*.
1. Vyberte **OK**.
1. Určete množství položky k počítání na registrační značce nastavením hodnoty **10** v poli *Množ.*
1. Vyberte **OK**.

    Na stránce se zobrazuje zadané skladové místo. Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“

1. Vyberte **OK**.

Práce je nyní dokončena.

#### <a name="spot-count-the-second-location"></a>Inventura druhého skladového místa

1. Na stránce **Inventura** nastavte v poli **Skladové místo** hodnotu *01A01R1S2B*.
1. Vyberte **OK**.

    Na stránce se zobrazuje zadané skladové místo. Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“

1. Vyberte **Obnovit**, chcete-li přidat pro dané skladové místo množství.
1. Na stránce **Cyklická inventura: přidání nové LP nebo položky** vyberte pole **Položka** a zadejte hodnotu *A0002*.
1. Vyberte **OK**.
1. Na stránce **Cyklická inventura: Přidání nové LP nebo položky** vyberte pole **LP** a zadejte hodnotu *LP1003* (nebo jakékoli jiné číslo registrační značky dle vašeho výběru. Podmínkou je, že se číslo musí lišit od obou čísel registračních značek z předchozí procedury).

    Na stránce **Cyklická inventura: Přidání nové LP nebo položky** se zobrazí **Pozice registrační značky 1**.

1. Vyberte **OK**.
1. Určete množství položky k počítání na registrační značce nastavením hodnoty **10** v poli *Množ.*
1. Vyberte **OK**.

    Na stránce se zobrazuje zadané skladové místo. Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“

1. Vyberte **OK**.

Práce je nyní dokončena.

#### <a name="work-details"></a>Podrobnosti o práci

> [!NOTE]
> Inventury z mobilní aplikace vytvářejí v systému Microsoft Dynamics 365 práci inventury. Práce vyžaduje, aby byly počty přijaty před zaúčtováním do zásob.

1. Přihlaste se do Dynamics 365 Supply Chain Management.
1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Na kartě **Přehled** vyhledejte řádky, které mají následující hodnoty:

    - **Typ pracovního příkazu:** *Cyklická inventura*
    - **Sklad:** *61*
    - **Stav práce:** *Čeká na kontrolu*

    Pro tyto řádky by měla být vytvořena dvě ID práce. Počty k oběma těmto ID práce je nutné přijmout.

1. V mřížce vyberte první ID práce pro typ pracovního příkazu *Cyklická inventura*.
1. V podokně Akce na kartě **Práce** ve skupině **Práce** vyberte **Cyklická inventura**.

    Zobrazí se dva řádky, jeden pro každou položku a registrační značku. Hodnoty v polích **Napočítané množství**, **Skladové místo**, **Registrační značka** a **Položka** by měly odpovídat položkám množství vytvořeným na mobilním zařízení. Pokud kterékoli z těchto polí nevidíte, vyberte možnost **Zobrazit dimenze** v podokně Akce a přidejte je do mřížky.

1. Vyberte oba řádky.
1. V podokně Akce klikněte na možnost **Přijmout množství**.
1. Zobrazí se zpráva „Zaúčtování – deník“. Vybrat **Podrobnosti zprávy**, zobrazí se číslo, pod kterým proběhlo zaúčtování do deníku.
1. Zavřete podrobnosti zprávy.
1. Obnovte stránku **Práce**.

    První ID práce bylo uzavřeno a již se nezobrazuje.

    > [!TIP]
    > Chcete-li zobrazit uzavřenou práci, zaškrtněte políčko **Zobrazovat uzavřené** nad mřížkou.

    Nyní přijmete práci pro registrační značku ve skladovém místě *01A01R1S2B*.

1. Na kartě **Přehled** vyberte druhé ID práce pro typ pracovního příkazu *Cyklická inventura*.
1. V podokně Akce na kartě **Práce** ve skupině **Práce** vyberte **Cyklická inventura**.

    Je zobrazen jeden řádek pro položku a registrační značku. Hodnoty v polích **Napočítané množství**, **Skladové místo**, **Registrační značka** a **Položka** by měly odpovídat položkám množství vytvořeným na mobilním zařízení.

1. Vyberte řádek.
1. V podokně Akce klikněte na možnost **Přijmout množství**.
1. Zobrazí se zpráva „Zaúčtování – deník“. Vybrat **Podrobnosti zprávy**, zobrazí se číslo, pod kterým proběhlo zaúčtování do deníku.
1. Zavřete podrobnosti zprávy.
1. Obnovte stránku **Práce**.

    Druhé ID práce bylo uzavřeno a již se nezobrazuje.

    > [!TIP]
    > Chcete-li zobrazit uzavřenou práci, zaškrtněte políčko **Zobrazovat uzavřené** nad mřížkou.

#### <a name="on-hand-by-location"></a>Množství na skladě podle místa

1. Přejděte na **Řízení skladu \> Dotazy a sestavy \> Množství na skladě podle skladového místa**.
1. Nastavte následující hodnoty:

    - **Lokalita:** *6*
    - **Sklad:** *61*
    - **Obnovit napříč skladovými místy:** *Ano*

1. Všimněte si, že skladové místo *01A01R1S1B* má dvě registrační značky:

    - **A0001**, kde je v poli **Pozice LP** zadána hodnota *1*
    - **A0002**, kde je v poli **Pozice LP** zadána hodnota *2*

1. Všimněte si, že skladové místo *01A01R1S2B* má jednu registrační značku:

    - **A0002**, kde je v poli **Pozice LP** zadána hodnota *1*

### <a name="sales-order-scenario"></a>Scénář prodejní objednávky

Po nastavení funkce *Určení pozice registrační značky na skladovém místě* a přípravě inventury musíte vytvořit prodejní objednávku, aby se vygenerovala práce výdeje, která nasměruje pracovníka skladu k výdeji položky *A0002* z místa se zásobami, kde je ID palety na pozici *1*.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-004*
    - **Sklad:** *61*

1. Vyberte **OK**.
1. Na záložce s náhledem **Řádky prodejní objednávky** se do mřížky přidá nový řádek. Na tomto novém řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *1*

1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob pro řádek objednávky.
1. Zavřete stránku **Rezervace**.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**

    Zobrazí se informační zpráva indikující ID vlny a ID dodávky, jež byly vytvořeny pro tuto objednávku.

1. Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Sklad** vyberte nad mřížkou možnost **Podrobnosti práce**.
1. Zobrazí se stránka **Práce**, na níž je zobrazena práce, která byla vytvořena pro řádek prodeje. Poznamenejte si ID zobrazené práce.

### <a name="sales-picking-scenario"></a>Scénář výdeje pro prodej

1. Otevřete mobilní aplikaci a přihlaste se do skladu *61*.
1. Přejděte do **Výstupní \> Prodejní výdej**.
1. Na stránce **Naskenujte ID práce / ID registrační značky** vyberte pole **ID** a zadejte ID práce z řádku prodeje.
1. Všimněte si, že výdejová práce vás nasměruje k výdeji položky *A0002* z místa *01A01R1S2B*. Tuto instrukci obdržíte, protože položka *A0002* je na registrační značce, jež je na daném skladovém místě v pozici *1*.

    ![Pozice 1 skladového místa.](media/LocationLicensePlatePositioning.png "Pozice 1 skladového místa")

1. Zadejte ID registrační značky vtvořené pro dané skladové místo a poté podle pokynů proveďte výdej prodejní objednávky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]