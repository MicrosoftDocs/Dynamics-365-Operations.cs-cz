---
title: Odchozí třídění
description: Toto téma popisuje informace o odchozím třídění. Tato funkce usnadňuje manipulaci s malými kontejnery a pomáhá pracovníkům skladu lépe plánovat a organizovat kapacitu palet v kamionu.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a3644964e43b7a1b34aa3bfab4e9172c1cb55bc8ef1d87cc7b5e2733effcb316
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726506"
---
# <a name="outbound-sorting"></a>Odchozí třídění

[!include [banner](../includes/banner.md)]

Tato funkce usnadňuje manipulaci s malými kontejnery a pomáhá pracovníkům skladu lépe plánovat a organizovat kapacitu palet v kamionu. Pokud používáte odchozí třídění, můžete třídit zabalené kontejnery na správnou paletu poté, co byly v balicí stanici. Můžete také vytvořit hierarchii balení.

Tato funkce umožňuje vytvářet palety z kontejnerů, které jsou zabaleny pomocí funkce balení. Kontejner není odeslán na místo konečného dodání, protože je v původním balicím toku. Místo toho mohou pracovníci uzavřít kontejner a přesunout jej do umístění typu řazení. Poté mohou třídit kontejnery do pozic, z nichž každá má registrační značku (RZ). Po třídění kontejnerů lze vytvořit práci, která odešle celou registrační značku do konečného přepravního doku nebo do skladových míst fáze, podle pokynů pro určování polohy nebo podle vašich vlastních požadavků. Akce uzavření pozice řazení může navíc okamžitě přesunout zásoby na místo konečného dodání a vybrat je do objednávky.

## <a name="turn-on-the-outbound-sorting-feature"></a>Zapnutí funkce Odchozí třídění

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Odchozí třídění*

## <a name="setup"></a>Nastavení

Pro tento scénář musíte použít standardní ukázková data **USMF** demo data a sklad *62*. Musíte také dokončit nastavení, které je popsáno v následujících podkapitolách.

### <a name="set-up-a-wave-template"></a>Nastavení šablony vlny

Toto nastavení automaticky zpracuje vlnu a vytvoří práci při uvolnění řádku do skladu.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V seznamu šablon vyberte **Sklad 62**.
1. Na pevné záložce **Obecné** se ujistěte, že je možnost **Zpracovat vlnu při uvolnění do skladu** nastavená na *Ano*.

### <a name="set-up-a-worker"></a>Nastavení pracovníka

Balicí stanice se považuje za místo. Pracovníci skladu, kteří se přihlásí na balicí stanici, vidí a pracují pouze na zásilkách a kontejnerech, které jsou plánovány v tomto konkrétním místě balení. Uživatel, který se přihlásí do Microsoft Dynamics 365, musí být nastaven jako pracovník řízení skladu. Pokud se jméno uživatele neobjeví v seznamu pracovních uživatelů, přidejte je pomocí následujícího postupu.

> [!NOTE]
> Tyto kroky předpokládají, že uživatel již v systému existuje a byl v systému přidružen jako zaměstnanec nebo pracovník modulu **Lidské zdroje**.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.
1. Zvolte **Nové**.
1. V poli **Pracovník** vyberte cílového uživatele v seznamu zaměstnanců.
1. Zvolte **Zvolit**.
1. V podokně akcí vyberte **Uložit**.
1. Na pevné záložce **Uživatelé** FastTab vyberte **Nový** k vytvoření účtu mobilního zařízení a nastavení následujících hodnot pro tento účet:

    - **ID uživatele:** Zadejte jedinečný identifikátor.
    - **Uživatelské jméno:** Zadejte název pro ID.
    - **Výchozí sklad:** *62*
    - **Název nabídky:** *Hlavní*

1. V podokně akcí vyberte **Uložit**.
1. Zobrazí se dialogové okno **Nastavit heslo**, ve kterém můžete vytvořit jednoduché heslo, pomocí něhož se uživatel může přihlásit k mobilní aplikaci. Nastavte následující hodnoty:

    - **Heslo:** Zadejte jednoduché heslo.
    - **Potvrdit heslo:** Znovu zadejte stejné heslo.

1. Zvolte **Nastavit heslo**.

    Oznámení v Centru akcí vás informuje, že pro uživatele, kterého jste vytvořili, bylo nastaveno heslo.

### <a name="create-a-location-type"></a>Vytvoření typu umístění

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Typy umístění**.
1. V podokně akcí vyberte **Nový** k vytvoření typu umístění a nastavte pro něj následující hodnoty:

    - **Typ umístění:** *SORT*
    - **Popis:** *Seřadit*

1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-warehouse-management-parameters"></a>Nastavení parametrů pro řízení skladu

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Ka kartě **Obecné** na pevné záložce **Typy umístění** nastavte hodnotu pole **Typ místa třídění** na *SORT*.
1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-a-location-profile"></a>Nastavení profilu skladového místa

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **ID profilu umístění:** *Třídění*
    - **Název:** *Třídění*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Formát umístění:** *ASRB* (ulička, stojan, police a přihrádka)
    - **Typ umístění:** *SORT*
    - **Použít sledování registrační značky:** *Ano*
    - **Povolit smíšené položky:** *Ano* (Když tuto možnost nastavíte na *Ano*, možnost **Povolit smíšené dávky zásob** se automaticky nastaví na *Ano* a nelze ji změnit samostatně.)

1. Zvolte **Uložit**.

### <a name="set-up-a-location"></a>Nastavení skladového místa

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.
1. V záhlaví zrušte zaškrtnutí políčka **Generovat kontrolní číslice pro místo**.
1. V podokně akcí vyberte **Nový** k vytvoření skladového místa a nastavte pro něj následující hodnoty:

    - **Sklad:** *62*
    - **Skladové místo:** *SORT*
    - **ID profilu umístění:** *TŘÍDĚNǏ*

1. Zvolte **Uložit**.

### <a name="set-up-an-outbound-sorting-template"></a>Nastavte odchozí šablonu třídění

Odchozí šablona třídění určuje, zda se práce vytváří mimo místo třídění a zda se třídění provádí ručně nebo automaticky.

Pro tento scénář vytvoříte odchozí šablonu třídění pro sestavení palet za balicí stanicí.

1. Přejděte na **Řízení skladu \> Nastavení \> Balení \> Odchozí šablona třídění**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nové šablony nastavte následující hodnoty:

    - **ID odchozí šablony třídění:** *AutoWork*
    - **Popis:** *Automatické vytvoření práce*
    - **Typ odchozí šablony třídění:** *Kontejner*
    - **Sklad:** *62*
    - **Skladové místo:** *SORT*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Ověření řazení:** *Kontrola pozice*.
    - **Vytvořit práci při uzavření pozice:** *Ano*

        Když je tato možnost nastavená na *Ano* a pozice uzavřená, práce bude vytvořena, aby se přesunuly zásoby do konečného místa doručení. Když je nastavená na *Ne*, zásoby budou ihned přiděleny do objednávky při zavření pozice.

    - **Přiřazení pozice:** *Automaticky*

        Pokud je pole nastaveno na *Ruční*, uživatel musí vždy označit, do jaké pozice mají být zásoby setříděny. Pokud je nastavená na *Automaticky*, systém automaticky navede zásoby do pozice, kdykoli je to možné, na základě přestávek šablony třídění.

1. V podokně akcí zvolte možnost **Uložit**. Tím se zpřístupní možnost **Upravit dotaz**.
1. V podokně Akce vyberte možnost **Upravit dotaz**.
1. V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má následující hodnoty:

    - **Tabulka:** *Dodávky*
    - **Odvozená tabulka:** *Dodávky*
    - **Pole:** *Služba dopravce*

        Po výběru této hodnoty se vám může zobrazit následující zpráva: „Služba dopravce není indexové pole. Chcete k němu přidat třídění?“ Vyberte **Ano**.

    - **Směr hledání:** *Vzestupně*

1. Vyberte **OK**.
1. Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“ Vyberte **Ano**.

    Aktivuje se tlačítko **Zalomení odchozích šablon třídění** v podokně akcí.

1. V podokně akcí vyberte možnost **Zalomení odchozích šablon třídění**.
1. V dialogovém okně **Odchozí kritéria třídění** nastavte následující hodnoty:

    - **Název referenční tabulky:** *Zásilky*
    - **Název referenčního pole:** *Přepravní služba*
    - **Seskupit podle pole:** Zaškrtněte toto políčko pro seskupení dodávek podle přepravní služby.

1. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.

### <a name="set-up-container-packing-policies"></a>Nastavení zásad balení kontejneru

1. Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Zásady balení kontejneru**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nové zásady nastavte následující hodnoty:

    - **Zásady balení kontejnerů:** *Třídit*
    - **Popis:** *Seřadit*

1. Na pevné záložce **Přehled** nastavte následující hodnoty:

    - **Sklad:** *62*
    - **Výchozí místo pro třídění:** *SORT*
    - **Hmotnost/jedn.:** *kg*
    - **Zásady uzavírání kontejnerů:** *Automatické vydání*
    - **Zásady uvolňování kontejnerů:** *Přiřadit kontejner k odchozí poloze třídění*

1. Zvolte **Uložit**.

### <a name="set-up-packing-profiles"></a>Nastavení profilů balení

Vytvořte nový profil balení, který bude použit spolu s funkcí třídění.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.
1. V podokně akcí vyberte **Nový** k vytvoření řádky a nastavte pro ni následující hodnoty:

    - **ID profilu balení:** *Třídění*
    - **Popis:** *Seřadit*
    - **Zásady balení kontejnerů:** *Třídit*
    - **Režim ID kontejneru:** *Automatický*
    - **Typ kontejneru:** *Velká krabice*
    - **Automatické vytvoření kontejneru při uzavření kontejneru:** Vymazáno (= *Ne*)

1. Zvolte **Uložit**.

### <a name="set-up-work-classes"></a>Nastavení tříd práce

Nastavte pracovní třídu, která bude použita společně s tříděním.

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.
1. V podokně akcí vyberte **Nový** k vytvoření pracovní třídy k třídění a nastavte pro něj následující hodnoty:

    - **ID pracovní třídy:** *Třídění*
    - **Popis:** *Seřadit*
    - **Typ pracovního příkazu:** *Výběr tříděných zásob*

1. Zvolte **Uložit**.

### <a name="set-up-mobile-device-menu-items"></a>Vytvoření položek nabídky mobilního zařízení

#### <a name="set-up-a-new-pallet-menu-item"></a>Nastavení položky nabídky nové palety

Vytvořte položku nabídky mobilního zařízení pro vtvoření palet během třídění.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Název položky nabídky:** *Sestavení palety*
    - **Název:** *Sestavení palety*
    - **Režim:** *Nepřímý*
    - **Použít existující práci:** *Ne*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Kód aktivity:** *Odchozí třídění*

        Když je toto pole nastaveno na *Odchozí třídění*, zobrazí se pole **ID šablony odchozího třídění**.

    - **Použít průvodce procesem:** *Ano*

        Když je hodnota v poli **Kód aktivity** nastavená na *Odchozí třídění*, je tato možnost automaticky nastavena na *Ano*.

    - **ID odchozí šablony třídění:** *AutoWork*

1. Zvolte **Uložit**.

#### <a name="set-up-a-new-loading-menu-item"></a>Nastavení nové položky nabídky načtení

Dále vytvořte položku nabídky, která uživatelům umožní přesunout setříděné skladové položky do místa expedice.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Název položky nabídky:** *Načíst z třídění*
    - **Název:** *Načíst z třídění*
    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*

1. Na pevné záložce **Obecné** nastavte hodnotu v poli **Řídí:** na *Řízeno systémem*.
1. Na pevné záložce **Pracovní třídy** vyberte **Nový** a pak nastavte následující hodnoty.

    - **ID pracovní třídy:** *SORT*
    - **Typ pracovního příkazu:** *Výběr tříděných zásob*

1. Zvolte **Uložit**.

### <a name="set-up-the-mobile-device-menu"></a>Nastavení nabídky mobilního zařízení

Nyní musíte nové položky nabídky přidat do nabídky mobilního zařízení.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. Vyberte nabídku **Odchozí**.
1. V podokně akcí vyberte **Upravit**.
1. Ve sloupci **Dostupné nabídky a položky nabídky** najděte a vyberte **Sestavení palety**.
1. Stisknutím tlačítka se šipkou doprava přesuňte **Sestavení palety** do sloupce **Struktura nabídky**.
1. Použijte tlačítka se šipkou nahoru a dolů pro přesunutí položky nabídky **Sestavení palety** na požadovanou pozici v nabídce mobilního zařízení.
1. Zvolte **Uložit**.
1. Opakujte tento postup pro přidání položky nabídky **Načíst z třídění** do nabídky **Odchozí**.

### <a name="set-up-location-directives"></a>Nastavit směrnice skladových míst

*Směrnice skladového místa* jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob. Nyní musíte vytvořit pravidlo pro správu třídění.

#### <a name="set-up-a-single-sku-directive"></a>Nastavení směrnice jedné skladové jednotky

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Posloupnost:** *1*
    - **Název:** *Portál*

1. Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:

    - **Typ práce:** *Vložit*
    - **Lokalita:** *6*
    - **Sklad:** *62*
    - **Více skladových jednotek:** *Ne*

1. Chcete-li, aby byl dostupný panel nástrojů na pevné záožce **Řádky**, klikněte na **Uložit**.
1. Na pevné záložce **Řádky** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Posloupnost:** *1*
    - **Od:** *0*
    - **Do:** *1,000,000*

1. Chcete-li, aby byl dostupný panel nástrojů na pevné záložce **Akce směrnice skladového místa**, klikněte na **Uložit**.
1. Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Posloupnost:** *1*
    - **Název:** *Portál*

1. Zvolte **Uložit**.
1. Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.
1. V editoru dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*. Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.
1. Výběrem **OK** uložte nastavení a zavřete editor dotazů.

#### <a name="set-up-a-multiple-sku-directive"></a>Nastavení směrnice více skladových jednotek

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Posloupnost:** *2*
    - **Název:** *Více nákladových bran*

1. Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:

    - **Typ práce:** *Vložit*
    - **Lokalita:** *6*
    - **Sklad:** *62*
    - **Více SKU:** *Ano*

1. Chcete-li, aby byl dostupný panel nástrojů na pevné záožce **Řádky**, klikněte na **Uložit**.
1. Na pevné záložce **Řádky** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Posloupnost:** *1*
    - **Od:** *0*
    - **Do:** *1,000,000*

1. Chcete-li, aby byl dostupný panel nástrojů na pevné záložce **Akce směrnice skladového místa**, klikněte na **Uložit**.
1. Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Posloupnost:** *1*
    - **Název:** *Více nákladových bran*

1. Zvolte **Uložit**.
1. Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.
1. V editoru dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*. Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.
1. Výběrem **OK** uložte nastavení a zavřete editor dotazů.

### <a name="set-up-work-templates"></a>Nastavit šablony práce

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.
1. V podokně Akce vyberte možnost **Nový** a vytvořte šablonu práce.
1. Na kartě **Přehled** natavte následující hodnoty:

    - **Posloupnost:** *1*
    - **Šablona práce:** *Třídění*
    - **Popis šablony práce:** *Třídění*

1. Chcete-li, aby byla dostupná záložka s náhledem **Podrobnosti šablony práce**, klikněte na **Uložit**.
1. Na pevné záložce **Podrobnosti pracovní šablony** vyberte **Nový**, chcete-li přidat řádek a poté pro něj nastavit následující hodnoty:

    - **Typ práce:** *Výdej*
    - **ID pracovní třídy:** *SORT*

1. Vyberte **Nový** pro přidání druhého řádku a pak pro něho nastavte tyto hodnoty:

    - **Typ práce:** *Vložit*
    - **ID pracovní třídy:** *SORT*

1. Zvolte **Uložit**.

## <a name="scenario"></a>Scénář

Tento scénář simuluje situaci, kdy by se balené kontejnery měly automaticky třídit do různých pozic (palet) po balicí stanici, v závislosti na službě přepravce. Poté, co jsou všechny položky z nákladu zabaleny a roztříděny podle adresy, budou palety přemístěny k nákladové bráně.

### <a name="create-sales-orders-and-picking-work"></a>Vytvoření prodejních objednávek a výběr práce

#### <a name="create-sales-order-1"></a>Vytvoření prodejní objednávky 1

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-005*
    - **Sklad:** *62*

1. Zvolte **OK** a zavřete dialogové okno.

    Otevře se nová prodejní objednávka.

1. Přepněte na zobrazení **Záhlaví**.
1. Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:

    - **Dopravce dodávky:** *Letecká přeprava*
    - **Služba dopravce:** *Air*

1. Přepněte do zobrazení **Řádky**.
1. Pokud se do mřížky na pevné záložce **Řádky prodejní objednávky** automaticky nepřidá prázdný řádek, vyberte **Přidat řádek**.
1. Na novém řádku objednávky nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *2*

1. V době, kdy je vybrán nový řádek na pevné záložce **Řádky prodejní objednávky**, vyberte v nabídce **Zásoby** nad mřížkou možnost **Rezervace**.
1. Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku. Poznamenejte si čísla ID vlny a ID dodávky.

#### <a name="sales-order-2"></a>Prodejní objednávka 2

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-006*
    - **Sklad:** *62*

1. Zvolte **OK** a zavřete dialogové okno.
1. Otevře se nová prodejní objednávka. Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**. Na tomto řádku objednávky nastavte následující hodnoty:

    - **Položka:** *A0001*
    - **Množství:** *1*

1. Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** nastavte pole **Způsob dodání** na *Flowe-STD*.
1. Na pevné záložce **Řádky prodejní objednávky** vyberte **Přidat řádek** a pak na druhém řádku objednávky nastavte následující hodnoty:

    - **Položka:** *A0002*
    - **Množství:** *1*

1. Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** změňte hodnotu pole **Způsob dodání** na *Air C-Air*.
1. Na pevné záložce **Řádky prodejní objednávky** vyberte první řádek objednávky. Pak v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. Na pevné záložce **Řádky prodejní objednávky** vyberte druhý řádek objednávky. Pak v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku. Všimněte si, že byla vytvořena dvě identifikační čísla vln a dvě identifikační čísla zásilek, jedno pro každý režim doručení pro řádky prodejních objednávek.

#### <a name="get-the-work-ids-from-the-work-details"></a>Získání ID práce z podrobností o práci

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Na této stránce jsou uvedena ID práce, která byla vytvořena z prodejních objednávek. Pomocí ID vlny a ID zásilky z prodejních objednávek, které jste vytvořili, vyhledejte pracovní ID pro každou vlnu a zásilku. Poznamenejte si tato ID práce, protože je budete potřebovat v dalších krocích. Všimněte si, že pro druhou prodejní objednávku byla vytvořena dvě ID práce. Pokud jsou různé položky vybrány z různých umístění, vygenerují se samostatná ID slov.

### <a name="pick-items-for-the-sales-orders"></a>Vyberte položky pro prodejní objednávky

Vytvořené dílo dokončete pomocí mobilního zařízení k přesunutí položek do balicí stanice.

1. Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Prodejní výdej**.
1. V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 1.
1. Vyberte **OK**.
1. Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku, která byla vytvořena pro prodejní objednávku 1. Všimněte si, že se zobrazí místo výběru (*hromadně-001*), položka (*A0001*) a množství (*2 ks*).
1. Vyberte **OK**.
1. Zkontrolujte informace na stránce **prodejní objednávky: vložení**. V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.
1. Vyberte **OK**.

    Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva Práce dokončena, která uvádí, že bylo dokončeno ID práce z prodejní objednávky 1.

    Nyní si vyberete prodejní objednávku 2.

1. V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 2, kde na řádku 1 je položka *A0001*.
1. Vyberte **OK**.
1. Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku. Všimněte si, že se zobrazí místo výběru (*hromadně-001*), položka (*A0001*) a množství (*1 ks*).
1. Vyberte **OK**.
1. Zkontrolujte informace na stránce **prodejní objednávky: vložení**. V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.
1. Vyberte **OK**.

    Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“. Tato zpráva označuje, že ID práce z řádku 1 prodejní objednávky 2 bylo dokončeno.

1. V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 2, kde na řádku 2 je položka *A0002*.
1. Vyberte **OK**.
1. Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku. Všimněte si, že se zobrazí místo výběru (*hromadně-002*), položka (*A0001*) a množství (*1 ks*).
1. Vyberte **OK**.
1. Zkontrolujte informace na stránce **prodejní objednávky: vložení**. V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.
1. Vyberte **OK**.

    Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“. Tato zpráva označuje, že ID práce z řádku 2 prodejní objednávky 2 bylo dokončeno.

### <a name="pack-sales-orders-into-containers"></a>Balení prodejních objednávek do kontejnerů

#### <a name="pack-sales-order-1-into-containers"></a>Balení prodejní objednávky 1 do kontejnerů

1. Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Balení**.

    Otevře se dialogové okno **Vybrat balicí stanici**. Ve výchozím nastavení by mělo být v poli **Pracovník** nastaveno jméno pracovníka, kterého jste nastavili dříve.

1. Chcete-li zobrazit a pracovat na zásilkách a kontejnerech, které jsou plánovány na konkrétním místě balení, nastavte následující hodnoty:

    - **Lokalita:** *6*
    - **Sklad:** *62*
    - **Místo:** *balení*
    - **ID profilu balení:** *Třídění*

1. Zvolte **OK** a zavřete dialogové okno.
1. Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku pro prodejní objednávku 1. Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.
1. V podokně akcí zvolte **Nový kontejner**.
1. Přijměte všechna výchozí nastavení a vyberte možnost **OK**. Poznamenejte si ID kontejneru.
1. Na pevné záložce **Balení položky** nastavte následující hodnoty:

    - **Množství:** *1*
    - **Identifikátor:** Položka *A0001*

1. V podokně akcí zvolte **Zavřít kontejner**.
1. V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.
1. Vyberte **OK**. Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.
1. Vytvořte druhý kontejner a přidejte druhou položku z registrační značky pro prodejní objednávku 1 do nového kontejneru.
1. V podokně akcí zvolte **Nový kontejner**.
1. Přijměte všechna výchozí nastavení a vyberte možnost **OK**. Poznamenejte si ID kontejneru.
1. Na pevné záložce **Balení položky** nastavte následující hodnoty:

    - **Množství:** *1*
    - **Identifikátor:** Položka *A0001*

1. V podokně akcí zvolte **Zavřít kontejner**.
1. V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.
1. Vyberte **OK**. Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.

#### <a name="pack-sales-order-2-into-containers"></a>Balení prodejní objednávky 2 do kontejnerů

1. Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku řádek 1 prodejní objednávky 2. Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.
1. V podokně akcí zvolte **Nový kontejner**.
1. Přijměte všechna výchozí nastavení a vyberte možnost **OK**. Poznamenejte si ID kontejneru.
1. Na pevné záložce **Balení položky** nastavte následující hodnoty:

    - **Množství:** *1*
    - **Identifikátor:** Položka *A0001*

1. V podokně akcí zvolte **Zavřít kontejner**.
1. V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.
1. Vyberte **OK**. Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.
1. V poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku řádek 2 prodejní objednávky 2. Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.
1. V podokně akcí zvolte **Nový kontejner**.
1. Přijměte všechna výchozí nastavení a vyberte možnost **OK**. Poznamenejte si ID kontejneru.
1. Na pevné záložce **Balení položky** nastavte následující hodnoty:

    - **Množství:** *1*
    - **Pole identifikátoru:** Položka *A0002*

1. V podokně akcí zvolte **Zavřít kontejner**.
1. V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.
1. Vyberte **OK**. Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.

Chcete-li zobrazit podrobnosti o kontejneru, přejděte na **Řízení skladu \> Balení a kontejnerizace \> Kontejnery** a vyhledejte ID kontejnerů, které byly vytvořeny během balení.

### <a name="sort-the-containers"></a>Třídění kontejnerů

> [!IMPORTANT]
> Jakmile přejdete na položku nabídky **Sestavení palety** v mobilní aplikaci pro odchozí třídění, uvidíte tlačítko označené jako **Plné**. *Tlačítko **Plné** nepoužívejte pro seřazení nebo uzavření pozice.*
>
> Tlačítko **Plné** je ve výchozím nastavení k dispozici a nelze jej na stránce deaktivovat ani odebrat. Nepoužívá se pro funkci *Odchozí třídění*.

#### <a name="sort-the-first-container"></a>Třídění prvního kontejneru

1. Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Sestavení palety**.
1. Do pole **Registrační značka/kontejner** zadejte ID prvního kontejneru spojeného s prodejní objednávkou 1.
1. Vyberte **OK**.
1. Protože v současné době neexistují žádné pozice řazení, musíte nějakou zadat. Do pole **ID pozice třídění** zadejte *SP01*.
1. Protože k pozici řazení není aktuálně přiřazen žádná RZ *SP01*, musíte ji zadat. Do pole **LP** zadejte hodnotu *PLP01*.
1. Vyberte **OK**.
1. Protože je zapnuto ověření pozice řazení, musíte znovu zadat ID pozice řazení. Do pole **ID pozice třídění** zadejte *SP01*.
1. Vyberte **OK**.

    Zobrazí se zpráva „Práce dokončena“.

> [!TIP]
> Pokud chcete zobrazit pozici třídění a registrační značku, kterou obsahuje, přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.
>
> Na stránce **Přiřazení pozice odchozího třídění** se zobrazují všechny aktuálně aktivní pozice třídění. Pole **Seřadit transakce pozic** zobrazuje RP, která je přidružena jednotlivým pozicím třídění, a kontejnery, které jsou v poloze třídění. Momentálně existuje jedna pozice třídění a na pevné záložce **Seřadit kritéria pozice** se zobrazuje kritérium **Zásilka - Dopravní služba - Letecká doprava**.

#### <a name="sort-the-remaining-containers"></a>Třídění zbývajících kontejnerů

1. Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Sestavení palety**.
1. Do pole **Registrační značka/kontejner** zadejte ID druhého kontejneru spojeného s prodejní objednávkou 1.
1. Vyberte **OK**. Protože je šablona třídění nastavena na automatické třídění a pozice třídění, která již obsahuje kritéria pro přiřazení, již existuje, jste automaticky přesměrováni na správnou pozici třídění.
1. Vyberte **OK**.
1. Potvrďte ID pozice třídění a označte, že jsou zásoby na správném místě. Do pole **ID pozice třídění** zadejte *SP01*.
1. Vyberte **OK**.

    Práce na druhém kontejneru byla dokončena z prodejní objednávky 1. Nyní budete třídit zbývající kontejnery z prodejní objednávky 2.

1. Do pole **Registrační značka / kontejner** zadejte ID kontejneru z prodejní objednávky 2, která obsahuje zboží *A0001*. Protože se služba operátora liší, budete vyzváni k zadání nové pozice řazení a přiřazení RZ této poloze. Použijte pozici třídění *SP02* a RZ *PLP02*.
1. Vyberte **OK**.
1. Potvrďte pozici třídění zadáním *SP02* do pole **ID polohy třídění**.
1. Vyberte **OK**.

    Práce na kontejneru byla dokončena.

1. Do pole **Registrační značka / kontejner** zadejte ID zbývajícího kontejneru z prodejní objednávky 2, která obsahuje zboží *A0002*. Protože služba operátora je stejná jako služba operátora pro prodejní objednávku 1, systém zobrazí existující pozici řazení, která má odpovídající kritéria.
1. Vyberte **OK**.
1. Potvrďte pozici třídění zadáním *SP01* do pole **ID pozice třídění**.
1. Vyberte **OK**.

    Práce na kontejneru byla dokončena.

### <a name="close-the-outbound-sorting-positions"></a>Zavřete odchozí pozice třídění

Po roztřídění všech zásob musí být pozice před vytvořením práce uzavřena. Vytvoří se práce výběru seřazených zásob pro převedení zásob k nákladové bráně.

#### <a name="close-a-position-from-the-mobile-device"></a>Zavřete pozici z mobilního zařízení

1. Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Sestavení palety**.
1. Do pole **Registrační značka / kontejner** zadejte ID kontejneru tříděné do pozice *SP01*.
1. Vyberte **OK**.
1. Zobrazí se následující zpráva: "Kontejner je již zařazen na pozici SP01. Uzavřít pozici?" Vyberte **Zavřít**.

    Práce je dokončena.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Uzavřete pozici z přiřazení odchozí pozice třídění

1. Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.
1. V levém sloupci vyberte možnost **SP02**. Tento řádek pro odchozí třídění je ten, který uzavřete.
1. V podokně akcí zvolte **Zavřít pozici**. Záznam pozice třídění je uzavřen a již se nezobrazuje.

    > [!TIP]
    > Chcete-li zobrazit všechny záznamy uzavřené polohy, zaškrtněte políčko **Zobrazit uzavřené**.

### <a name="sorted-inventory-picking"></a>Výdej setříděných zásob

Musíte dokončit práci výběru tříděných zásob. Po dokončení budou zásoby vybrány do prodejní objednávky. V tomto okamžiku platí všechny ostatní skladové procesy.

1. Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Načíst z třídění**.
1. Zadejte cílové ID LP z první pozice třídění, *SP01*. Nastavte pole **ID** na *PLP01*.
1. Vyberte **OK**.
1. Na stránce **Výběr seřazených zásob: Vybrat** se zobrazuje práce výběru, kterou je potřeba provést. Vyberte z umístění *SORT* a cílového RZ *PLP01*, který má více položek a množství *3*.
1. Vyberte **OK**.
1. Na stránce **Výběr seřazených zásob: Vložit** se zobrazuje práce vložení, kterou je potřeba provést. Vložte do umístění *Nákladová brána* a cílového RZ *PLP01*, který má více položek a množství *3*.
1. Vyberte **OK**.

    Práce je dokončena.

1. Zadejte cílové ID registrační značky ze druhé pozice třídění, *SP02*. Nastavte pole **ID** na *PLP02*.
1. Vyberte **OK**.
1. Na stránce **Výběr seřazených zásob: Vybrat** se zobrazuje práce výběru, kterou je potřeba provést. Vyberte z umístění *SORT* a cílového RZ *PLP02*, který má více položek a množství *1*.
1. Vyberte **OK**.
1. Na stránce **Výběr seřazených zásob: Vložit** se zobrazuje práce vložení, kterou je potřeba provést. Vložte do umístění *Nákladová brána* a cílového RZ *PLP02*, který má více položek a množství *1*.
1. Vyberte **OK**.

    Práce je dokončena.

Odteď platí všechny ostatní skladové procesy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]