---
title: Konfigurace zásad konsolidace dodávek
description: Toto téma vysvětluje, jak nastavit výchozí a vlastní zásady konsolidace dodávek.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f2705300925ae475f00861327b9cea9a97416011
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578673"
---
# <a name="configure-shipment-consolidation-policies"></a>Konfigurace zásad konsolidace dodávek

[!include [banner](../includes/banner.md)]

Proces konsolidace dodávek, který používá zásady konsolidace dodávek, umožňuje automatizovanou konsolidaci dodávek během automatizovaného a ručního uvolnění do skladu. Po zapnutí této funkce musíte nakonfigurovat počáteční zásady. Pokud nejsou nakonfigurovány žádné zásady, vygeneruje každý řádek prodeje samostatnou dodávku, která má jeden řádek vytížení.

Scénáře uvedené v tomto tématu ukazují, jak nastavit výchozí a vlastní zásady konsolidace dodávek.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Zapnutí funkce zásad konsolidace dodávek

> [!IMPORTANT]
> V [prvním scénáři](#scenario-1), který je popsán v tomto tématu, nejprve nastavíte sklad tak, aby používal dřívější funkci konsolidace dodávek. Poté zpřístupníte zásady konsolidace dodávek. Tímto způsobem můžete vyzkoušet, jak scénář upgradu funguje. Pokud chcete použít prostředí s ukázkovými daty pro projití prvního scénáře, nezapínejte tuto funkci dříve, než provedete scénář.

Než budete moci používat funkci *Zásady konsolidace dodávek*, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Konsolidace dodávky*

## <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Každý scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>Scénář 1: Konfigurace výchozích zásad konsolidace dodávek

Existují dvě situace, kdy musíte po zapnutí funkce *Zásady konsolidace dodávek* nakonfigurovat minimální počet výchozích zásad:

- Upgradujete prostředí, které již obsahuje data.
- Nastavujete úplně nové prostředí.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Upgradujte prostředí, ve kterém jsou sklady již nakonfigurovány pro konsolidaci mezi objednávkami

Když spustíte tento postup, funkce *Zásady konsolidace dodávek* by měla být vypnuta, aby se simulovalo prostředí, ve kterém již byla použita základní funkce konsolidace mezi objednávkami. Poté tuto funkci zapnete pomocí správy funkcí, abyste se naučili, jak nastavit zásady konsolidace dodávek po upgradu.

Postupujte podle těchto kroků a nastavte výchozí zásady konsolidace dodávek v prostředí, ve kterém jsou již sklady nakonfigurovány pro konsolidaci mezi objednávkami.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. V seznamu vyhledejte a otevřete požadovaný záznam skladu (například sklad *24* v ukázkových datech **USMF**).
1. V podokně akcí vyberte **Upravit**.
1. Na záložce s náhledem **Sklad** nastavte možnost **Konsolidovat dodávku při uvolnění do skladu** na *Ano*.
1. Opakujte kroky 2 až 4 pro všechny ostatní sklady, kde je vyžadována konsolidace.
1. Zavřete stránku.
1. Použijte [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pro zapnutí funkce *Zásady konsolidace dodávek*. V pracovním prostoru **Správa funkcí** je funkce pojmenována jako *Konsolidace dodávek*.
1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**. Možná budete muset obnovit svůj prohlížeč, abyste mohli zobrazit novou položku **Zásad konsolidace dodávek** po zapnutí funkce.
1. V podokně akcí vyberte možnost **Vytvořit výchozí nastavení** a vytvořte následující zásady:

    - Zásada **CrossOrder** pro typ zásady *Prodejní objednávky* (za předpokladu, že máte alespoň jeden sklad, který je nastaven pro použití funkce dřívější konsolidace)
    - **Výchozí** zásada pro typ zásady *Prodejní objednávky*
    - **Výchozí** zásada pro typ zásady *Vydání transferu*
    - Zásada **CrossOrder** pro typ zásady *Vydání transferu* (za předpokladu, že máte alespoň jeden sklad, který je nastaven pro použití funkce dřívější konsolidace)

    > [!NOTE]
    > - Obě zásady **CrossOrder** považují stejnou sadu polí za dřívější logiku, s výjimkou pole pro číslo objednávky. (Toto pole se používá ke konsolidaci řádků do dodávek na základě faktorů, jako je sklad, způsob dopravy dodávky a adresa.)
    > - Obě zásady **Výchozí** považují stejnou sadu polí za dřívější logiku, včetně pole pro číslo objednávky. (Toto pole se používá ke konsolidaci řádků do dodávek na základě faktorů, jako je číslo objednávky, sklad, způsob dopravy dodávky a adresa.)

1. Vyberte zásady **CrossOrder** pro typ zásady *Prodejní objednávky* a poté na podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů si všimněte skladů, u kterých je možnost **Konsolidovat dodávku při uvolnění do skladu** nastavena na *Ano*. Proto jsou zahrnuty v dotazu.

### <a name="create-default-policies-for-a-new-environment"></a>Vytvoření výchozích zásad pro nové prostředí

Postupujte podle těchto kroků a nastavte výchozí zásady konsolidace dodávek ve zcela novém prostředí.

1. Použijte [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pro zapnutí funkce *Zásady konsolidace dodávek*, pokud jste ji již nezapnuli. V pracovním prostoru **Správa funkcí** je funkce pojmenována jako *Konsolidace dodávek*.
1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. V podokně akcí vyberte možnost **Vytvořit výchozí nastavení** a vytvořte následující zásady:

    - **Výchozí** zásada pro typ zásady *Prodejní objednávky*
    - **Výchozí** zásada pro typ zásady *Vydání transferu*

    > [!NOTE]
    > Obě zásady **Výchozí** považují stejnou sadu polí za dřívější logiku, včetně pole pro číslo objednávky. (Toto pole se používá ke konsolidaci řádků do dodávek na základě faktorů, jako je číslo objednávky, sklad, způsob dopravy dodávky a adresa.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>Scénář 2: Konfigurace vlastních zásad konsolidace dodávek

Tento scénář ukazuje, jak nastavit vlastní zásady konsolidace dodávek. Vlastní zásady mohou podporovat složité obchodní požadavky, kde konsolidace dodávek závisí na několika podmínkách. Pro každou příkladovou zásadu dále v tomto scénáři je uveden stručný popis obchodního případu. Tyto příkladové zásady by měly být nastaveny v posloupnosti, která zajišťuje vyhodnocení dotazů v podobě pyramidy. (Jinými slovy, zásady, které mají nejvíce podmínek, by měly být vyhodnoceny jako zásady s nejvyšší prioritou.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Zapněte funkci a připravte hlavní data pro tento scénář

Než budete moci procházet cvičeními v tomto scénáři, musíte zapnout funkci a připravit hlavní data, která jsou nezbytná pro filtrování, jak je popsáno v následujících pododdílech. (Tyto předpoklady platí také pro scénáře uvedené v části [Příkladové scénáře použití zásad konsolidace dodávek](#example-scenarios) .)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Zapněte funkci a vytvořte výchozí zásady

Použijte správu funkcí pro zapnutí funkce, pokud jste ji ještě nezapnuli, a vytvořte výchozí zásady konsolidace, které jsou popsány ve [scénáři 1](#scenario-1).

#### <a name="create-two-new-product-filter-codes"></a>Vytvoření dvou nových kódů filtrů produktu

1. Přejděte na **Řízení skladu \> Nastavit \> Filtry produktů \> Filtry produktů** a přidejte dva filtry produktů:

    - Filtr produktu 1:

        - **Kód filtru:** *Hořlavý*
        - **Název filtru:** *Kód 4*

    - Filtr produktu 2:

        - **Kód filtru:** *Explozivní*
        - **Název filtru:** *Kód 4*

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete produkt s číslem položky *M9200*. (Produkt, který vyberete, musí být povolen pro rozšířené procesy skladu \[WMS\] a tento produkt je předem povolen pro procesy WMS v ukázkových datech **USMF**.)
1. Na záložce s náhledem **Sklad** nastavte pole **Kód 4** na *Hořlavý*.
1. Zavřete stránku.
1. Otevřete produkt s číslem položky *M9201*. (Tento produkt je také předem povolen pro procesy WMS v ukázkových datech **USMF**.)
1. Na záložce s náhledem **Sklad** nastavte pole **Kód 4** na *Explozivní*.
1. Zavřete stránku.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Vytvoření způsobu dopravy dodávky

1. Přejděte do **Správa přepravy \> Nastavení \> Dopravci \> Způsob**.
1. Vytvořte způsob dopravy, který bude použit v dotazech konsolidace, a pojmenujte ho *Airways*.
1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Dopravci dodávky**.
1. Vytvořte dopravce, který má následující nastavení:

    - **Dopravce dodávky:** *Airways*
    - **Název:** *Airways*
    - **Způsob:** *Airways*

1. Na záložce s náhledem **Služby** pro nového dopravce přidejte řádek, který má následující nastavení:

    - **Služba dopravce:** *Air*
    - **Způsob přepravy:** *Air*

1. V podokně akcí vyberte **Uložit**.

    > [!NOTE]
    > Když uložíte nového dopravce, pole **Způsob doručení** pro nový řádek v mřížce **Služby** je automaticky nastaveno na *Airwa-Air*. Když používáte způsob dodání *Airwa-Air* pro prodejní objednávku, způsob přepravy *Airways* bude použit pro související dodávky.

#### <a name="create-an-order-pool"></a>Vytvoření fondu objednávek

1. Přejděte na **Prodej a marketing \> Nastavení \> Prodejní objednávky \> Fondy objednávek**.
1. Vytvořte fond objednávek, který bude použit pro dotaz konsolidace. Tento fond objednávek by měl mít následující nastavení:

    - **Fond:** Zadejte celé číslo, které ještě nepoužívá žádný jiný fond.
    - **Název:** *ShipCons*

1. Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.
1. Otevřete zákazníka, který má číslo účtu *US-003*.
1. Na záložce s náhledem **Výchozí nastavení prodejních objednávek** nastavte pole **Fond prodejních objednávek** na fond objednávek, který jste právě vytvořili.
1. Zavřete stránku a opakujte kroky 4 a 5 pro zákazníka, který má číslo účtu *US-004*.

### <a name="create-example-policy-1"></a>Vytvoření vzorové zásady 1

V tomto příkladu vytvoříte zásadu *Zákazník+Způsob*, kterou lze použít pro následující obchodní případ:

- Zásada se bude dotazovat na konkrétní zákaznický účet (*US-001*) a konkrétní způsob doručení (*Airwa-Air*).
- Konsolidace s otevřenými dodávkami je vypnuta.
- Konsolidace se provádí podle ID objednávky. (Jinými slovy, budou existovat samostatné dodávky na objednávku, sklad atd.)

Postupujte podle těchto kroků a vytvořte zásadu konsolidace dodávek pro tento obchodní případ.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. Nastavte pole **Typ zásady** na *Prodejní objednávky*.
1. V podokně akcí vyberte **Nový** a vytvořte zásadu, která má následující nastavení:

    - **Název zásady:** *CustomerMode*
    - **Popis zásady:** *Účet zákazníka a způsob doručení*

1. Opusťte možnost **Konsolidace s otevřenými dodávkami** nastavenou na *Ne*.
1. V podokně akcí vyberte **Uložit**.
1. Na záložce s náhledem **Pole konsolidace** v seznamu **Zbývající pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Způsob doručení*.
1. Klepněte na tlačítko **Přidat** ![Šipka vpravo.](media/forward-button.png) přesuňte pole do seznamu **Vybraná pole**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** v mřížce vyhledejte řádek, kde je pole **Pole** nastaveno na *Účet zákazníka* a nastavte pole **Kritéria** pro tento řádek na *US-001*.
1. Vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:

    - **Tabulka:** *Řádky objednávek*
    - **Odvozená tabulka:** *Řádky objednávek*
    - **Pole:** *Způsob dodání*
    - **Kritéria:** *Airwa-Air*

1. Zvolte **OK** a zavřete dialogové okno.

> [!NOTE]
> Pro tento obchodní případ nebudou řádky objednávky pro zákazníka *US-001*, který používá způsob doručení *Airwa-Air*, konsolidovány napříč objednávkami. Tato zásada je určena k použití v posloupnosti jako první, v případech, kdy jsou dodávky pro všechny ostatní způsoby dodání pro tohoto zákazníka konsolidovány.

### <a name="create-example-policy-2"></a>Vytvoření vzorové zásady 2

V tomto příkladu vytvoříte zásadu *Nebezpečné zboží*, kterou lze použít pro následující obchodní případ:

- Zásada se bude dotazovat na konkrétní kód filtru (*nebezpečný*) a konkrétní způsob doručení (*Airwa-Air*).
- Konsolidace s otevřenými dodávkami je zapnuta.
- Konsolidace se provádí napříč objednávkami. (Jinými slovy, budou existovat samostatné dodávky podle účtu, skladu a podobně, ale pouze v rámci skupiny položek, která je určena v dotazu.)

Postupujte podle těchto kroků a vytvořte zásadu konsolidace dodávek pro tento obchodní případ.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. Nastavte pole **Typ zásady** na *Prodejní objednávky*.
1. V podokně akcí vyberte **Nový** a vytvořte zásadu, která má následující nastavení:

    - **Název zásady:** *Typ položky*
    - **Popis zásady:** *Konsolidace stejného typu položky napříč objednávkami*

1. Nastavte možnost **Konsolidace s otevřenými dodávkami** na *Ano*.
1. V podokně akcí vyberte **Uložit**.
1. Na záložce s náhledem **Pole konsolidace** v seznamu **Zbývající pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Způsob doručení*.
1. Klepněte na tlačítko **Přidat** ![Šipka vpravo.](media/forward-button.png) přesuňte pole do seznamu **Vybraná pole**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Propojení tabulek** rozbalte a vyberte ve stromu **Tabulky \> Načíst podrobnosti**.
1. Zvolte **Přidat propojení tabulek**.
1. V mřížce vztahů, která se zobrazí, najděte a vyberte řádek, ve kterém je pole **Vztah** nastaveno na *Číslo položky skladu (číslo položky)* a poté zvolte **Vybrat**. 
1. Na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:

    - **Tabulka:** *Číslo položky skladu*
    - **Odvozená tabulka:** *Číslo položky skladu*
    - **Pole:** *Kód 4*
    - **Kritéria:** *Hořlavý*

1. Zvolte **OK** a zavřete dialogové okno.

> [!NOTE]
> Pro tento obchodní případ budou všechny řádky objednávek, kde položky mají specifický kód filtru (tedy kód filtru, kde je pole **Kód 4** nastaveno na *Hořlavý*) konsolidovány s dalšími položkami stejného typu napříč objednávkami. Pokud existuje otevřená dodávka pro stejný účet, sklad a skupinu položek, budou k ní připojeny nové řádky.

### <a name="create-example-policy-3"></a>Vytvoření vzorové zásady 3

V tomto příkladu vytvoříte zásadu *Požadavky zákazníků*, kterou lze použít pro následující obchodní případ:

- Zásada se bude dotazovat na konkrétní zákaznický účet.
- Konsolidace s otevřenými dodávkami je zapnuta.
- Konsolidace se provádí napříč objednávkami, ale je založena na požadavcích zákazníka. (Jinými slovy, více objednávek bude seskupeno do dodávek na základě stejného čísla požadavku zákazníka a skladu.)

Postupujte podle těchto kroků a vytvořte zásadu konsolidace dodávek pro tento obchodní případ.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. Nastavte pole **Typ zásady** na *Prodejní objednávky*.
1. V podokně akcí vyberte **Nový** a vytvořte zásadu, která má následující nastavení:

    - **Název zásady:** *CustomerOrderNo*
    - **Popis zásady:** *Konsolidace řádek na základě nákupní objednávky zákazníka*

1. Nastavte možnost **Konsolidace s otevřenými dodávkami** na *Ano*.
1. V podokně akcí vyberte **Uložit**.
1. Na záložce s náhledem **Pole konsolidace** v seznamu **Zbývající pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Požadavek zákazníka*.
1. Klepněte na tlačítko **Přidat** ![Šipka vpravo.](media/forward-button.png) přesuňte pole do seznamu **Vybraná pole**.
1. V seznamu **Zbývající pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Způsob doručení*.
1. Klepněte na tlačítko **Přidat** ![Šipka vpravo.](media/forward-button.png) přesuňte pole do seznamu **Vybraná pole**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** vyhledejte řádek, kde je pole **Pole** nastaveno na *Účet zákazníka* a nastavte pole **Kritéria** pro tento řádek na *US-001*.
1. Zvolte **OK** a zavřete dialogové okno.

> [!NOTE]
> V tomto obchodním případě budou všechny řádky objednávek, kde prodejní objednávky mají stejné číslo požadavku zákazníka, konsolidovány do jedné dodávky, bez ohledu na číslo prodejní objednávky. (Číslo požadavku zákazníka se používá jako číslo nákupní objednávky zákazníka \[PO\].) Pokud existuje otevřená dodávka pro stejný účet, sklad a požadavek zákazníka, budou k ní připojeny nové řádky. Tuto zásadu lze použít, pokud zákazník odešle další řádky objednávek, které mají stejné číslo nákupní objednávky několikrát během dne, a chce, aby byly všechny řádky seskupeny do jedné dodávky. (Jinými slovy, bude existovat jeden přepravní doklad a jeden dodací list.)

### <a name="create-example-policy-4"></a>Vytvoření vzorové zásady 4

V tomto příkladu vytvoříte zásadu *Zákazníci umožňující konsolidaci*, kterou lze použít pro následující obchodní případ:

- Zásady se budou dotazovat na konkrétní fond objednávek, aby bylo možné identifikovat zákazníky, kteří přijímají konsolidované dodávky.
- Konsolidace s otevřenými dodávkami je vypnuta.
- Konsolidace se provádí napříč objednávkami pomocí polí vybraných ve výchozí zásadě CrossOrder (k replikaci předchozího zaškrtávacího políčka **Konsolidovat dodávku při uvolnění do skladu**).

- Pravidlo na prodejní objednávce můžete přepsat výběrem jiného fondu objednávek.

Postupujte podle těchto kroků a vytvořte zásadu konsolidace dodávek pro tento obchodní případ.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. Nastavte pole **Typ zásady** na *Prodejní objednávky*.
1. V podokně akcí vyberte **Nový** a vytvořte zásadu, která má následující nastavení:

    - **Název zásady:** *Fond objednávek*
    - **Popis zásady:** *Konsolidace napříč objednávkami na základě fondu objednávek*

1. Opusťte možnost **Konsolidace s otevřenými dodávkami** nastavenou na *Ne*.
1. V podokně akcí vyberte **Uložit**.
1. Na záložce s náhledem **Pole konsolidace** v seznamu **Zbývající pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Způsob doručení*.
1. Klepněte na tlačítko **Přidat** ![Šipka vpravo.](media/forward-button.png) přesuňte pole do seznamu **Vybraná pole**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:

    - **Tabulka:** *Prodejní objednávky*
    - **Odvozená tabulka:** *Prodejní objednávky*
    - **Pole:** *Fond*
    - **Kritéria:** *ShipCons*

1. Zvolte **OK** a zavřete dialogové okno.

> [!NOTE]
> V tomto obchodním případě budou všechny řádky objednávek, ve kterých prodejní objednávky patří do stejného fondu objednávek, konsolidovány do jedné dodávky napříč prodejními objednávkami na stejný účet, sklad a způsob dopravy. Místo fondu objednávek můžete použít jakékoli jiné pole k rozlišení skupiny zákazníků a ve výchozím nastavení použít záhlaví prodejní objednávky. Tento přístup můžete použít, pokud zákazník, nikoli sklad, řídí potřebu konsolidace. (V dřívější logice konsolidace vedl sklad potřebu konsolidace.)

### <a name="create-example-policy-5"></a>Vytvoření vzorové zásady 5

V tomto příkladu vytvoříte zásadu *Sklady umožňující konsolidaci*, kterou lze použít pro následující obchodní případ:

- Zásady se budou dotazovat na konkrétní fond objednávek, aby bylo možné identifikovat sklady, které mohou konsolidovat dodávky.
- Konsolidace s otevřenými dodávkami je vypnuta.
- Konsolidace se provádí napříč objednávkami pomocí polí vybraných ve výchozí zásadě CrossOrder (k replikaci předchozího zaškrtávacího políčka **Konsolidovat dodávku při uvolnění do skladu**).

Obvykle lze tento obchodní případ řešit pomocí výchozích zásad, které jste vytvořili ve [scénáři 1](#scenario-1). Podobné zásady však můžete vytvořit také ručně pomocí těchto kroků.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. Nastavte pole **Typ zásady** na *Prodejní objednávky*.
1. V podokně akcí vyberte **Nový** a vytvořte zásadu, která má následující nastavení:

    - **Název zásady:** *Napříč objednávkami*
    - **Popis zásady:** *Konsolidace napříč objednávkami pro konkrétní sklady*

1. Opusťte možnost **Konsolidace s otevřenými dodávkami** nastavenou na *Ne*.
1. V podokně akcí vyberte **Uložit**.
1. Na záložce s náhledem **Pole konsolidace** v poli **Zbývající pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Způsob doručení*.
1. Klepněte na tlačítko **Přidat** ![Šipka vpravo.](media/forward-button.png) přesuňte pole do seznamu **Vybraná pole**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** vyhledejte řádek, kde je pole **Pole** nastaveno na *Sklad* a nastavte pole **Kritéria** pro tento řádek na *61, 63*.
1. Zvolte **OK** a zavřete dialogové okno.

### <a name="set-the-order"></a>Nastavení objednávky

Nyní, když jste vytvořili všechny své zásady, musíte stanovit pořadí, v jakém budou použity. Chcete-li použít přístup podobný pyramidám, kde jsou zásady, které mají nejvíce podmínek, vyhodnoceny jako zásady s nejvyšší prioritou, postupujte podle těchto kroků.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. Nastavte pole **Typ zásady** na *Prodejní objednávky*.
1. Vyberte všechny zásady, které jsou uvedeny v levém sloupci, a poté použijte tlačítka **Nahoru** a **Dolů** v podokně akcí k uspořádání zásad v následujícím pořadí:

    1. CustomerMode
    1. Typ položky
    1. CustomerOrderNo
    1. Fond objednávek
    1. Napříč objednávkami
    1. Výchozí

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Příklad scénářů použití zásad konsolidace dodávek

Následující scénáře ilustrují, jak byste mohli použít zásady konsolidace dodávek, které jste vytvořili při čtení tohoto tématu. Každý scénář vás provede procesem konsolidace dodávek, který používá zásady konsolidace dodávek během automatizovaného nebo ručního uvolnění do skladu:

- Scénář 1: [Konsolidace dodávek při jejich uvolnění do skladu pomocí automatického uvolnění prodejních objednávek](../warehousing/consolidate-shipments-automatic.md)
- Scénář 2: [Konsolidace dodávek, když je zásada konsolidace dodávek přepsána ze stránky Uvolnění do skladu](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Scénář 3: [Konsolidace dodávek pomocí uvolnění do skladu z pracovní plochy plánování vytížení](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Scénář 4: [Konsolidace dodávek pomocí pracovní plochy dodávek zásilek](../warehousing/consolidate-shipments-manual-workbench.md)
- Scénář 5: [Ruční konsolidace dodávek pomocí stránky konsolidace dodávek](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Další prostředky

- [Zásady konsolidace dodávek](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]