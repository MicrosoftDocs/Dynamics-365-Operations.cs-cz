---
title: Seskupení vyskladnění
description: Seskupení vyskladnění nabízejí způsob, jak vybrat více registračních značek najednou a poté je vyskladnit do různých umístění. Mohou být velmi užitečné pro maloobchod, kde registrační značky obvykle nejsou plnými paletami zásob.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5f681d08268bdf92212eb5e0c99532bb0827afe7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344163"
---
# <a name="putaway-clusters"></a>Seskupení vyskladnění

[!include [banner](../includes/banner.md)]

Seskupení vyskladnění nabízejí způsob, jak vybrat více registračních značek najednou a poté je vyskladnit do různých umístění. Tento proces se často označuje jako *milk run*. Seskupení vyskladnění mohou být velmi užitečná pro maloobchod, kde registrační značky obvykle nejsou plnými paletami zásob. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Zapnutí funkce seskupení vyskladnění

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Funkce seskupení vyskladnění*

## <a name="setup-for-the-example-scenario"></a>Nastavení pro příkladový scénář

### <a name="cluster-profiles"></a>Profily seskupení

Profil seskupení vyskladnění určuje, kam se položka dostane, na základě umístění, které je položce přiřazeno v době přijetí. Pokud jsou vyžadována různá seskupení, měly by být pro každou položku nabídky mobilního zařízení vytvořena seskupení vyskladnění.

1. Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Profily seskupení**.
1. V podokně akcí zvolte **Nový**.
1. V zobrazení **Záhlaví** nastavte následující hodnoty:

    - **ID profilu seskupení vyskladnění:** *Seskupení vyskladnění*
    - **Název ID profilu seskupení vyskladnění:** *Seskupení vyskladnění*
    - **Typ seskupení:** *Vyskladnění*
    - **Pořadové číslo:** Přijměte výchozí hodnotu.

1. Chcete-li, aby byla dostupná požadovaná pole, na záložce s náhledem **Obecné** vyberte **Uložit**.
1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Načasování přiřazení seskupení:** *Při přijetí*

        Toto pole definuje, zda by mělo být seskupení vyskladnění přiřazeno okamžitě po přijetí zásob, nebo zda by mělo být tříděno později.

    - **Pravidlo přiřazení seskupení:** *Manuální*

        Toto pole definuje, zda má být přiřazení seskupení určeno automaticky systémem nebo ručně uživatelem.

    - **Kód směrnice:** Toto pole nechte prázdné.
    - **Vyhledání seskupení vyskladnění:** *Příjemka*

        K dispozici jsou následující hodnoty:

        - **Příjemka** - Umístění je nalezeno ihned během příjmu.
        - **Uzavření seskupení**- Umístění nalezené, když je seskupení uzavřené.
        - **Nasměrované uživatelem** - Místo je nalezeno, když je registrační značka vybrána ze seskupení vyskladnění. V tomto případě není zadáno žádné umístění, když je vytvořena práce vyskladnění. Během samotného vyskladnění musí uživatel naskenovat registrační značku nebo ID práce, aby zahájil krok vložení. Systém poté znovu vyhledá místo vložení a řekne uživateli, kam má vybrané množství uložit.

    - **Seskupení vyskladnění podle uživatele:** *Ne*

        Toto pole definuje, zda by každé seskupení mělo být pro každého uživatele jedinečné, když jsou seskupení přiřazována automaticky. Je k dispozici pouze v případě, kdy je pole **Pravidlo seskupení vyskladnění** nastaveno na *Automatické*.

    - **Omezení jednotky:** Ponechejte toto pole prázdné.

        Toto pole definuje jednotku, která musí být přijata, aby byl profil platný. Ponecháte-li ho prázdné, jsou platné všechny jednotky.

    - **Přerušení jednotky práce:** *Individuální*

        Toto pole definuje, zda by měly být všechny zásoby sloučeny (pomocí ID sestavení a registrační značky) na jednu registrační značku, když je sestavení uzavřeno, a zda by měly být vyskladněny jako jedna registrační značka nebo samostatně na přijatých registračních značkách. Toto pole není k dispozici, když je pole **Vyhledání sestavení vyskladnění** nastaveno na *Příjemka*.

    - **Seskupení přetrvává jako nadřazená registrační značka:** *Ne*

        Pokud je tato možnost nastavena na *Ano* po dokončení kroku vložení, ID sestavení se stane nadřazenou registrační značkou a všechny položky v ID seskupení budou propojeny s touto nadřazenou registrační značkou.

1. Na záložce s náhledem **Řazení seskupení** můžete definovat kritéria třídění vyskladnění. Vyberte **Nový** na panelu nástrojů pro přidání řádku a pak nastavte tyto hodnoty:

    - **Pořadové číslo:** Přijměte výchozí hodnotu.
    - **Název pole:** *WMSLocationId*

        Toto pole definuje pole, které by tento řádek měl použít jako kritérium řazení.

    - **Řazení:** *Vzestupně*

        Toto pole určuje, zda se třídění provede vzestupně nebo sestupně.

1. Na záložce s náhledem **Pracovní šablona sestavení** vyberte v panelu nástrojů **Nový**, chcete-li přidat řádek a poté nastavte následující hodnoty:

    - **Typ pracovního příkazu:** *Nákupní objednávky*
    - **Pracovní šablona:** *61 PO Direct*

1. V podokně akcí vyberte **Uložit** a potom vyberte **Upravit dotaz**.
1. V dialogovém okně **Seskupení vyskladnění** na kartě **Oblast** vyberte **Přidat** a přidejte druhý řádek do dotazu. Poté aktualizujte řádky dotazu, jak je znázorněno v následující tabulce.

    | Tabulka | Odvozená tabulka | Pole | Kritéria |
    |---|---|---|---|
    | Práce | Práce | Sklad | *61* |
    | Práce | Práce | ID práce | Pole ponechejte prázdné. |

1. Vyberte **OK**, uložte dotaz a zavřete dialogové okno.
1. V podokně akcí zvolte **Uložit** a zavřete stránku.

> [!IMPORTANT]
> Pole v profilu seskupení, která se při zobrazování zobrazují šedě, když je možnost **Vygenerovat ID seskupení** nastavena na *Ano*, nejsou k dispozici a při použití této funkce nebudou brány v úvahu.

### <a name="mobile-device-menu-items"></a>Položky nabídky mobilního zařízení

Pro tuto funkci jsou k dispozici dvě nové položky nabídky mobilního zařízení. Položka nabídky **Přijmout a setřídit seskupení** se používá k třídění přijatých zásob do seskupení vyskladnění při příjmu. Položka nabídky **Seskupení vyskladnění** slouží k vyskladnění sestavení po jeho přiřazení.

#### <a name="receive-and-sort-cluster"></a>Přijmout a setřídit seskupení

Vytvořte novou položku nabídky mobilního zařízení pro příjem zásob a řazení do seskupení. Tato položka nabídky vytvoří příchozí práci po přijetí zásob, což znamená, že se položka nabídky příjmu použije pro seskupení vyskladnění.

> [!NOTE]
> Položku nabídky **Přijmout a setřídit seskupení** lze použít s následujícími položkami nabídky příjmu:
>
> - Přijetí řádku nákupní objednávky
> - Přijetí položky nákupní objednávky
> - Přijetí položky nákladu

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V zobrazení **Záhlaví** nastavte následující hodnoty:

    - **Název položky nabídky:** *Přijmout a setřídit seskupení*
    - **Název:** *Přijmout a setřídit seskupení*
    - **Režim:** *Práce*
    - **Použít existující práci:** *Ne*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Proces tvorby práce:** *Příjem položky nákupní objednávky*
    - **Generovat registrační značky:** *Ano*
    - **Přiřadit seskupení vyskladnění:** *Ano*

        > [!NOTE]
        > Možnost **Přiřadit seskupení vyskladnění** je k dispozici pouze pro jednokrokovou aktivitu *Proces tvorby práce* pro příjem.

    Potvrďte výchozí hodnoty ve všech zbývajících polích.

1. V podokně akcí vyberte **Uložit**.

#### <a name="cluster-putaway"></a>Odložení seskupení

Vytvořte novou položku nabídky mobilního zařízení pro vyskladnění sestavení po jeho přiřazení.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V zobrazení **Záhlaví** nastavte následující hodnoty:

    - **Název položky nabídky:** *Vyskladnění seskupení*
    - **Název:** *Vyskladnění seskupení*
    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*

1. Na pevné záložce **Obecné** nastavte hodnotu v poli **Řídí:** na *Vyskladnění seskupení*. Potvrďte výchozí hodnoty ve všech zbývajících polích.
1. Na záložce s náhledem **Pracovní třídy** nastavte platnou pracovní třídu pro tuto položku nabídky mobilního zařízení:

    - **ID pracovní třídy:** *Nákup*
    - **Typ pracovního příkazu:** *Nákupní objednávky*

1. V podokně akcí vyberte **Uložit**.

### <a name="mobile-device-menu"></a>Nabídka mobilního zařízení

Přidejte položky nabídky, které jste právě vytvořili, do příchozí nabídky mobilní aplikace.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V podokně akcí vyberte **Upravit**.
1. V seznamu nabídek vyberte možnost **Vstupní**.
1. V seznamu **Dostupné nabídky a položky nabídky** najděte a vyberte **Přijmout a setřídit seskupení**.
1. Stisknutím tlačítka se šipkou doprava přesuňte vybranou položku nabídky do seznamu **Struktura nabídky**.
1. Pomocí šipky nahoru nebo šipky dolů přesuňte položku nabídky na požadované místo v nabídce.
1. V podokně akcí vyberte **Uložit**.
1. Chcete-li přidat zbývající položky nabídky, zopakujte kroky 4 až 7.

    - Přiřadit seskupení
    - Odložení seskupení

## <a name="example-scenario"></a>Příklad

Tento scénář simuluje zpracování seskupení vyskladnění.

### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:

    - **Účet dodavatele:** *1001*
    - **Sklad:** *61*

1. Vyberte **OK**.

    Zobrazí se stránka **Všechny nákupní objednávky**.

1. Na stránce **Všechny nákupní objednávky** na záložce s náhledem **Řádky nákupní objednávky** použijte tlačítko **Přidat řádek** pro přidání následujících řádků:

    - Řádek nákupní objednávky 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *10*

    - Řádek nákupní objednávky 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *20*

    - Řádek nákupní objednávky 3:

        - **Číslo položky:** *M9215*
        - **Množství:** *30*

1. V podokně akcí vyberte **Uložit**.
1. Poznamenejte si číslo nákupní objednávky.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Přijetí zásob a jejich vyskladnění z mobilního zařízení

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Příjem a třídění zásob do seskupení

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel, který je nastaven pro sklad *61*.
1. V hlavní nabídce vyberte **Příchozí**.
1. V nabídce **Příchozí** vyberte **Přijímat a setřídit seskupení**.
1. V poli **Ponum** zadejte číslo nákupní objednávky.
1. Vyberte tlačítko **OK** (tlačítko zaškrtnutí).
1. Vyberte pole **Položka**, zadejte číslo položky *A0001* a poté zvolte **OK**..
1. Vyberte pole **Množství**, zadejte *10* pomocí číselné klávesnice a poté vyberte tlačítko zaškrtnutí.
1. Na stránce s úkolem **Množství** vyberte **OK** (tlačítko zaškrtnutí) k potvrzení zadaného množství.
1. Na stránce s úkolem **Položka** vyberte **OK** a potvrďte, že položka *A0001* byla zadána.
1. Vyberte pole **ID seskupení** a zadejte hodnotu pro přiřazení ID pro seskupení, který vytváříte.

    ID, které zde zadáte, bude použito při přijetí dvou zbývajících položek v nákupní objednávce.

1. Vyberte **OK**.

    Zobrazí se stránka s úkolem **Ponum** a pak se zobrazí zpráva „Práce dokončena“.

    Položka *A0001* nyní byla přijat do umístění *RECV* a přiřazena k ID seskupení, které jste zadali v kroku 10.

1. Opakováním kroků 4 až 11 přijměte zbývající dvě položky z nákupní objednávky a přiřaďte je k ID seskupení:

    - Množství *20* pro položku *A0002*
    - Množství *30* pro položku *M9215*

#### <a name="close-the-cluster"></a>Zavřete seskupení

Než bude možné položky v seskupení vyskladnit, musí být seskupení uzavřeno.

1. V části Supply Chain Management přejděte na **Řízení skladu \> Práce \> Odchozí \> Pracovní seskupení**.
1. Na stránce **Pracovní seskupení** v sekci **Pracovní seskupení** vyhledejte pole **ID seskupení** pro ID seskupení, které jste zadali dříve.
1. Pokud se seskupení nezobrazí, mohl být již uzavřeno. Chcete-li zjistit, zda bylo seskupení uzavřeno, vyberte zaškrtávací políčko **Zobrazit uzavřenou práci** a vyhledejte ID seskupení, které jste zadali dříve. Potom proveďte jeden z následujících kroků:

    - Pokud by bylo seskupení uzavřeno, přeskočte zbývající kroky tohoto postupu a přejděte k dalšímu postupu, [Vyskladnění seskupení](#put-the-cluster-away).
    - Pokud seskupení nebylo uzavřeno, postupujte podle zbývajících kroků tohoto postupu a ručně jej zavřete. Poté se přesuňte na následující postup.

1. V sekci **Pracovní seskupení** vyberte ID seskupení, které jste zadali dříve.
1. V podokně akcí zvolte **Zavřít seskupení**.

    Poté, co bylo seskupení uzavřeno, již se dále nezobrazuje v sekci **Pracovní seskupení** (pokud není zvoleno zaškrtávací políčko **Zobrazit uzavřenou práci**).

#### <a name="put-the-cluster-away"></a>Vyskladnění seskupení

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel, který je nastaven pro sklad *61*.
1. V hlavní nabídce vyberte **Příchozí**.
1. V nabídce **Příchozí** zvolte **Vyskladnění seskupení**.
1. Vyberte **ID seskupení** a zadejte ID seskupení, které jste dříve zadali pro uzavřené seskupení.
1. Vyberte **OK**.

    Zobrazí se stránka **Vyskladnění seskupení: Výdej** Zobrazuje ID seskupení, místo výdeje, položky (zobrazí se hodnota *Násobek*) a celkové množství v seskupení, které je třeba vydat.

1. Vyberte **OK**.

    Zobrazí se stránka **Vyskladnění seskupení: Vložení** Pokyny **Vložení** identifikují ID seskupení, místo vložení, položky, celkové množství a ID registrační značky pro položky, které byly přijaty v seskupení.

    Máte standardní možnosti, jak tento krok přepsat nebo předat.

    ![Vyskladnění seskupení: Stránka vložení.](media/Cluster_putaway-Put.png "Vyskladnění seskupení: Stránka vložení")

1. Zvolte **OK** a potvrďte vyskladnění seskupení.

    Zobrazí se zpráva „Seskupení dokončeno“.

## <a name="notes-and-tips"></a>Poznámky a tipy

V případech, kdy se ID seskupení stane nadřazenou registrační značkou pro vnořenou paletu, je při skenování ID seskupení pozice vložení automaticky dána. Žádná další registrační značka nesmí být skenována, i když je generování poznávací značky nastaveno na ruční.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]