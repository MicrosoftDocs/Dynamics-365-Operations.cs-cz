---
title: Plná pozice seskupení
description: Tento článek obsahuje informace o funkci Plná pozice seskupení. Tato funkce nabízí alternativu k přísnějšímu vynucování pravidel pracovní přestávky při použití výdejů v seskupení, protože umožňuje větší toleranci chyb ve volumetrických omezeních kontejnerů nebo břemen.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4d46933b7c60317234b8e39cd6dfd63d383de860
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857134"
---
# <a name="cluster-position-full"></a>Plná pozice seskupení

[!include [banner](../includes/banner.md)]

Funkce *Plná pozice seskupení* nabízí alternativu k přísnějšímu vynucování pravidel pracovní přestávky při použití výdejů v seskupení, protože umožňuje větší toleranci chyb ve volumetrických omezeních kontejnerů nebo břemen. V běžném scénáři se ne všechny položky pracovního příkazu vejdou do vybraného kontejneru. Pracovníci skladu, kteří provádějí výdej v seskupení, mají v tomto scénáři několik možností: musí buď změnit velikost kontejneru na větší nebo ve spolupráci se svým nadřízeným přijít s jiným řešením.

Tato funkce zavádí možnost spustit tlačítko **Plná** pro jednu z pracovních jednotek v seskupení. Ve starších verzích byla tato možnost k dispozici pouze pro běžný výdej objednávek, nikoli pro výdej v seskupení. Tato funkce se však liší od standardního tlačítka **Plná** v tom, že zruší zbývající práci. Funkce nenavrhne, aby uživatel přidal do stejného seskupení další přihrádku a automaticky nevytváří novou práci.

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce Plná pozice seskupení

Chcete-li používat funkčnost popsanou v tomto článku, musí být ve vašem systému zapnuta funkce *Plná pozice seskupení*. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Plná pozice seskupení* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Nastavení

Tato část poskytuje pokyny a příklad, který ukazuje, jak nastavit a používat funkci *Plná pozice seskupení*.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s [příkladovým scénářem](#example-scenario) pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tento příklad můžete také použít jako průvodce pro použití této funkce ve výrobě. V takovém případě však musíte každé nastavení, které je zde popsáno, nahradit vlastními hodnotami.

### <a name="cluster-profiles"></a>Profily seskupení

Musíte určit, zda se ID seskupení generují automaticky, kolik pozic se používá, kdy jsou seskupení rozdělena a jak je práce výdeje řazena a ověřována.

1. Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Profily seskupení**.
1. V podokně seznamu vyberte záznam **Vytvořit seskupení**.
1. Na záložce s náhledem **Obecné** ověřte následující hodnoty:

    - **Generovat ID seskupení:** – Vyberte *Ano*.
    - **Aktivovat pozice:** *Ano*
    - **Počet pozic:** *2*
    - **Název pozice:** *Číselná*
    - **Rozdělit seskupení u:** *Vložení*
    - **Typ ověření řazení:** *Skenování pozice*

1. Na záložce s náhledem **Řazení seskupení**. Mřížka by měla být prázdná (to znamená, že by neměla obsahovat žádné řádky).

### <a name="work-templates"></a>Šablony práce

Musíte definovat, jak je vytvořena práce výdeje pro výdej v seskupení.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V horní části stránky nastavte pole **Typ pracovního příkjazu** na *Prodejní objednávky*.
1. Ujistěte se, že jsou uvedeny následující pracovní šablony z ukázkových dat. Pokud nejsou k dispozici, nebudete moci scénář dokončit.

    - Fáze 61 PO
    - Výdej v seskupení 61 PO

### <a name="location-directives"></a>Směrnice skladového místa

Musíte určit, odkud jsou položky vyskladněny a kam jsou vydány.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V záhlaví seznamu nastavte pole **Typ pracovního příkazu** na *Prodejní objednávky*.
1. Ujistěte se, že jsou uvedeny následující směrnice prodejní objednávky z ukázkových dat. Pokud nejsou k dispozici, nebudete moci scénář dokončit.

    - Výdej v seskupení 61
    - Výdej v seskupení 61

### <a name="mobile-device-menu-items"></a>Položky nabídky mobilního zařízení

Musíte nakonfigurovat položku nabídky mobilního zařízení pro použití stávající práce, která se řídí výdejem v seskupení. V položce nabídky mobilního zařízení pro výdej v seskupení musí být zapnutý parametr **Umožnit rozdělení práce** a musí být přidána třída práce *Výdej PO*.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně seznamu vyberte záznam **Vytvoření výdeje v seskupení**.
1. V podokně Akce vyberte **Upravit**.
1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Řídí:** *Výdej v seskupení*
    - **Generovat registrační značky:** *Ano*
    - **Umožnit rozdělení práce** *Ano*
    - **ID profilu seskupení:** *Vytvořit seskupení*

    Potvrďte výchozí hodnoty pro všechna ostatní pole.

1. Na záložce s náhledem **Pracovní třídy** podle potřeby přidejte následující dva řádky:

    - Řádek 1 (obvykle v ukázkových datech):

        - **ID pracovní třídy:** *Prodej* 
        - **Typ pracovního příkazu:** *Prodejní objednávky*

    - Řádek 2 (pravděpodobně není v ukázkových datech):

        - **ID pracovní třídy:** *Výdej PO*
        - **Typ pracovního příkazu:** *Prodejní objednávky*

1. Jděte na **Nastavení potvrzení práce** v podokně Akce.
1. Vyberte možnost **Upravit**.
1. Na řádek v mřížce zadejte následující hodnoty.
    - **Typ práce:** - *Výdej*
    - **Potvrzení produktu** - *Zaškrtněte políčko*

1. Vyberte **Uložit** v podokně Akce a zavřete stránku.

## <a name="create-picking-work"></a>Vytvořit práci výdeje

Než budete moci začít s výdejem seskupení, musíte vytvořit nějakou výstupní práci. Dříve vytvořený profil seskupení určuje dvě pozice clusteru. Proto musí být pro výdej prodejní objednávky vytvořena alespoň dvě ID práce. V tomto scénáři dojde k transakcím ve skladu *61* a budou používat položky *L0101* a *T0100*. Ukázková data by měla mít dostatek těchto položek na skladě. Ujistěte se, že máte dostatek zásob k dokončení transakcí.

### <a name="create-sales-order-1"></a>Vytvoření prodejní objednávky 1

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Volbou **Nová** vytvořte prodejní objednávku 1.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-010*
    - **Sklad:** *61*

1. Vyberte **OK**.
1. Otevře se nová prodejní objednávka. Na pevné záložce **Řádky prodejní objednávky** přidejte řádek s následujícím nastavením:

    - **Číslo položky:** *T0100*
    - **Množství:** *5*

1. Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.
1. Na záložce s náhledem **Řádky prodejní objednávky** přidejte druhý řádek s následujícím nastavením:

    - **Číslo položky:** *L0101*
    - **Množství:** *20*

1. Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.
1. Pro každý řádek, který jste právě přidali, rezervujte zásoby podle následujících pokynů:

    1. Vyberte řádek, pro který chcete provést rezervaci.
    2. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
    3. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.
    4. Zavřete stránku **Rezervace**.

1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Když je dokončeno uvolnění, obdržíte informační zprávy znázorňující ID vlny a ID nákladu, jež byly vytvořeny.

### <a name="create-sales-order-2"></a>Vytvoření prodejní objednávky 2

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Volbou **Nová** vytvořte prodejní objednávku 2.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-011*
    - **Sklad:** *61*

1. Vyberte **OK**.
1. Otevře se nová prodejní objednávka. Na pevné záložce **Řádky prodejní objednávky** přidejte řádek s následujícím nastavením:

    - **Číslo položky:** *L0101*
    - **Množství:** *20*

1. Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.
1. Na záložce s náhledem **Řádky prodejní objednávky** přidejte druhý řádek s následujícím nastavením:

    - **Číslo položky:** *T0100*
    - **Množství:** *2*

1. Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.
1. Pro každý řádek, který jste právě přidali, rezervujte zásoby podle následujících pokynů:

    1. Vyberte řádek, pro který chcete provést rezervaci.
    2. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
    3. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.
    4. Zavřete stránku **Rezervace**.

1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Když je dokončeno uvolnění, obdržíte informační zprávy znázorňující ID vlny a ID nákladu, jež byly vytvořeny.

### <a name="get-work-ids-and-license-plate-numbers"></a>Získání ID práce a registračních značek vozidel

Měla by být vytvořena dvě ID práce, z nichž každé má dva řádky výdeje. Podle těchto pokynů vyhledejte ID práce a registrační značky vozidel.

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. V mřížce **Přehled** prohledejte sloupec **Číslo objednávky** pro dvě prodejní objednávky, které jste právě vytvořili. Pro každou prodejní objednávku si poznamenejte odpovídající ID práce.
1. Výběrem řádku pro každou prodejní objednávku v něm zobrazíte související informace v mřížce **Řádky**. Poznamenejte si skladové místo, ze kterého bude každá položka vydána.
1. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Zásoby na skladě**.
1. V podokně Akce volbou **Dimenze** otevřete dialogové okno **Zobrazení dimenzí**.
1. Ujistěte se, že jsou zaškrtnuta políčka **Registrační značka**, **Sklad** a **Číslo položky** a poté vyberte **OK**.
1. V podokně **Filtr** nastavte následující filtry:

    - **Číslo položky** – **je jedním z** – *L0101* a *T100*
    - **Sklad** – **začíná na** – *61*

1. Poznamenejte si zobrazené hodnoty pro **registrační značku**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Příklad

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Spuštění toku mobilního zařízení – nastavení potvrzení práce pro produkt

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel skladu *61*.
1. Jděte na **Odchozí \> Vytvoření výdeje v seskupení**.

    Zobrazí se stránka **ÚKOL: Přiřadit práci seskupení**.

1. Zadejte ID práce pro prodejní objednávku 1 a přiřaďte jej k pozici seskupení 1.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zadejte ID práce pro prodejní objednávku 2 a přiřaďte jej k pozici seskupení 2.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Zobrazí se stránka **ÚKOL: Vytvoření výdeje v seskupení: výdej**, která obsahuje *Položka L0101 2 PL* .

Protože profil seskupení nastavil počet pozic na 2, systém vás automaticky přesměruje na první konsolidovaný výdej: dvě palety (PL) položky *L0101*.

Během následujících kroků můžete kdykoli vybrat kartu **Podrobnosti** pro zobrazení dalších informací o úkolu, například výdejního skladovacího místa.

1. Nastavte pole **POLOŽKA** na *L0101*. Tím se potvrdí číslo položky, které je pro tuto položku nabídky požadováno (to jste nakonfigurovali dříve výběrem **Nastavení potvrzení práce** na stránce **Položka nabídky mobilního zařízení**, když jste vytvořili tuto položku nabídky).
1. Zadejte registrační značku vozidla, která je přidružena k položce ve skladovém místě, ze kterého probíhá výdej. Vyberete si dvě palety.
1. Nastavte pole **REGISTRAČNÍ ZNAČKA** na *REGISTRAČNÍ ZNAČKA\_VÝDEJ\_01*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Zobrazí se stránka **ÚKOL: Seřadit: Vytvoření výdeje v seskupení**. Zde seřadíte dvě vyskladněné palety do pozice pro výdej. Tato pozice může být břemeno nebo kontejner, který se používá k oddělení vyskladněných zásob podle prodejní objednávky.

1. Zobrazte podrobnosti pro položku (*L0101*) a množství (*20* ks), které jsou seřazeny na pozici 1 (pro prodejní objednávku 1).
1. Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *1*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zobrazte podrobnosti pro položku (*L0101*) a množství (*20* ks), které jsou seřazeny na pozici 2 (pro prodejní objednávku 2).
1. Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *2*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Zobrazí se stránka **ÚKOL: Vytvoření výdeje v seskupení: výdej**, která obsahuje *Položka T0100 7 ks* .

V tomto scénáři pozice 1 nemůže přijmout celé množství položek, které je třeba vyskladnit, aby byla splněna prodejní objednávka 1. Pozice musí být označena jako plná. V tomto scénáři provedete částečné vyskladnění druhé položky. Druhá položka bude částečně vyskladněna pro pozici 1 a bude vytvořena nová práce pro vyskladnění zbývajícího množství pro splnění objednávky.

1. Stiskněte tlačítko nabídky (tzv. „hamburgerové tlačítko“ nebo „hamburger“) a vyberte **Plná pozice**.
1. Určete pozici, která je plná, a vyberte *1*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zadejte množství k vyskladnění, které lze ještě vyskladnit do pozice 1. Systém může určit, které číslo položky je vyskladňováno.
1. Zadejte *2*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Potvrďte číslo položky a dokončete vyskladnění zbývající položky do pozice 2.
1. Nastavte pole **POLOŽKA** na *T0100*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zadejte registrační značku vozidla, ze které je položka vyskladňována, nastavením pole **REGISTRAČNÍ ZNAČKA** na *LPREPL04*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zobrazte podrobnosti pro položku (*T0100*) a množství (*2* ks), které jsou seřazeny na pozici 2 (pro prodejní objednávku 2).
1. Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *2*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zobrazte podrobnosti pro položku (*T0100*) a množství (*2* ks), které jsou seřazeny na pozici 1 (pro prodejní objednávku 1).
1. Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *1*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Zobrazí se stránka **ÚKOL: Vytvoření výdeje v seskupení: vložení**.

V tomto scénáři byl proveden výdej v seskupení a uživatel je nasměrován k zaskladnění vyskladněních položek z pozice 1 a pozice 2 do přechodného skladového místa *FÁZE01*.

1. Zkontrolujte informace na stránce. Ukazuje, že celkové množství *44* bude zaskladněno do přechodného skladového místa.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Zobrazí se zpráva „Seskupení dokončeno“.

Nyní můžete pomocí položky nabídky **Prodejní výdej** vyskladnit zbývající množství. Poté můžete pomocí položky nabídky **Nakládání prodeje** přesunout položky z přechodného skladového místa do překladišť.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]