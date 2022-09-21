---
title: Konfigurace zásad konsolidace dodávek
description: Tento článek vysvětluje, jak nastavit výchozí a vlastní zásady konsolidace dodávek.
author: Mirzaab
ms.date: 09/07/2022
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
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427975"
---
# <a name="configure-shipment-consolidation-policies"></a>Konfigurace zásad konsolidace dodávek

[!include [banner](../includes/banner.md)]

Proces konsolidace dodávek, který používá zásady konsolidace dodávek, umožňuje automatizovanou konsolidaci dodávek během automatizovaného a ručního uvolnění do skladu. Po zapnutí této funkce musíte nakonfigurovat počáteční zásady. Pokud nejsou nakonfigurovány žádné zásady, vygeneruje každý řádek prodeje samostatnou dodávku, která má jeden řádek vytížení.

Scénáře uvedené v tomto článku ukazují, jak nastavit výchozí a vlastní zásady konsolidace dodávek.

> [!WARNING]
> Pokud upgradujete systém Microsoft Dynamics 365 Supply Chain Management, kde jste používali starší funkci konsolidace zásilek, může konsolidace přestat fungovat podle očekávání, pokud se nebudete řídit zde uvedenými radami.
>
> U instalací Supply Chain Management, kde je funkce *Zásady konsolidace zásilek*, aktivujete konsolidaci zásilek pomocí nastavení **Konsolidovat zásilku při uvolnění do skladu** pro každý jednotlivý sklad. Tato funkce je povinná od verze 10.0.29. Když je zapnutá, nastavení **Konsolidovat zásilku při uvolnění do skladu** se skryje a funkce je nahrazena *zásadami konsolidace zásilek*, které jsou popsány v tomto článku. Každá zásada stanoví pravidla konsolidace a obsahuje dotaz pro kontrolu, kde se tato zásada použije. Při prvním zapnutí této funkce nebudou definovány žádné zásady konsolidace zásilek na stránce **Zásady konsolidace zásilek**. Pokud nejsou definovány žádné zásady, systém použije starší chování. Proto každý stávající sklad nadále respektuje své nastavení **Konsolidovat zásilku při uvolnění do skladu**, i když je toto nastavení nyní skryté. Jakmile však vytvoříte alespoň jednu zásadu konsolidace zásilek, nastavení **Konsolidovat zásilku při uvolnění do skladu** již nemá žádný vliv a funkčnost konsolidace je zcela řízena zásadami.
>
> Poté, co definujete alespoň jednu zásadu konsolidace zásilek, systém zkontroluje zásady konsolidace pokaždé, když je objednávka uvolněna do skladu. Systém zpracovává zásady pomocí hodnocení, které je definováno hodnotou **Posloupnost zásad** každých zásad. Použije první zásadu, pokud dotaz odpovídá nové objednávce. Pokud objednávce neodpovídají žádné dotazy, vygeneruje každý řádek objednávky samostatnou dodávku, která má jeden řádek vytížení. Proto jako záložní řešení doporučujeme vytvořit výchozí zásadu, která bude platit pro všechny sklady a skupiny podle čísla objednávky. Nastavte tuto záložní politiku co nejvyšší hodnotu **Posloupnost zásad**, aby byla zpracována jako poslední.
>
> Chcete-li reprodukovat starší chování, musíte vytvořit zásadu, která se neseskupuje podle čísla objednávky a která má kritéria dotazu zahrnující všechny relevantní sklady.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Zapnutí funkce zásad konsolidace dodávek

Chcete-li používat funkci *Zásady konsolidace dodávek*, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Zásady konsolidace dodávek* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a>Nastavení výchozích zásad konsolidace

Pokud pracujete s novým systémem nebo systémem, kde jste právě zapnuli funkci *Zásady konsolidace zásilek* poprvé, postupujte podle následujících kroků a nastavte své počáteční zásady konsolidace zásilek.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. V podokně akcí vyberte možnost **Vytvořit výchozí nastavení** a vytvořte následující zásady:

    - Zásady s názvem *Výchozí* pro typ zásady *Prodejní objednávky*.
    - Zásady s názvem *Výchozí* pro typ zásady *Vydání převodního příkazu*.
    - Zásady s názvem *CrossOrder* pro typ zásady *Vydání převodního příkazu*. (Tato zásada je vytvořena pouze v případě, že jste měli alespoň jeden sklad, kde je starší nastavení **Konsolidovat zásilku při uvolnění do skladu** zapnuté.)
    - Zásady s názvem *CrossOrder* pro typ zásady *Prodejní objednávky*. (Tato zásada je vytvořena pouze v případě, že jste měli alespoň jeden sklad, kde je starší nastavení **Konsolidovat zásilku při uvolnění do skladu** zapnuté.)

    > [!NOTE]
    > - Obě zásady *CrossOrder* považují stejnou sadu polí za dřívější logiku. Berou však v úvahu i pole s číslem objednávky. (Toto pole se používá ke konsolidaci řádků do dodávek na základě faktorů, jako je sklad, způsob dopravy dodávky a adresa.)
    > - Obě zásady *Výchozí* považují stejnou sadu polí za dřívější logiku. Berou však v úvahu i pole s číslem objednávky. (Toto pole se používá ke konsolidaci řádků do dodávek na základě faktorů, jako je číslo objednávky, sklad, způsob dopravy dodávky a adresa.)

1. Když systém vygeneroval zásadu *CrossOrder* pro typ zásady *Prodejní objednávky*, vyberte ji a poté na podokně akcí vyberte **Upravit dotaz**. V editoru dotazů můžete vidět, pro který z vašich skladů bylo nastavení **Konsolidovat zásilku při uvolnění do skladu** dříve aktivováno. Proto tato zásada reprodukuje vaše předchozí nastavení pro tyto sklady.
1. Přizpůsobte nové výchozí zásady podle potřeby přidáním nebo odebráním polí nebo úpravou dotazů. Můžete také přidat tolik nových zásad, kolik potřebujete. Příklady, které ukazují, jak přizpůsobit a nakonfigurovat zásady, naleznete v příkladu scénáře dále v tomto článku.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Scénář: Konfigurace vlastních zásad konsolidace dodávek

Tento scénář poskytuje příklad, který ukazuje, jak nastavit vlastní zásady konsolidace zásilek a poté je otestovat pomocí ukázkových dat. Vlastní zásady mohou podporovat složité obchodní požadavky, kde konsolidace dodávek závisí na několika podmínkách. Pro každou příkladovou zásadu dále v tomto scénáři je uveden stručný popis obchodního případu. Tyto příkladové zásady by měly být nastaveny v posloupnosti, která zajišťuje vyhodnocení dotazů v podobě pyramidy. (Jinými slovy, zásady, které mají nejvíce podmínek, by měly být vyhodnoceny jako zásady s nejvyšší prioritou.)

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Tento scénář odkazuje na hodnoty a záznamy, které jsou součástí standardních [ukázkových dat](../../fin-ops-core/fin-ops/get-started/demo-data.md) poskytovaných pro Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na *USMF*, než začnete.

### <a name="prepare-master-data-for-this-scenario"></a>Příprava hlavních dat pro tento scénář

Než budete moci procházet cvičeními v tomto scénáři, musíte připravit hlavní data, která jsou nezbytná pro filtrování, jak je popsáno v následujících pododdílech. (Tyto předpoklady platí také pro scénáře uvedené v části [Příkladové scénáře použití zásad konsolidace dodávek](#example-scenarios) .)

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

Obvykle lze tento obchodní případ řešit pomocí výchozích zásad, které jste vytvořili v části [Nastavení úvodních zásad konsolidace](#initial-policies). Podobné zásady však můžete vytvořit také ručně pomocí těchto kroků.

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

Následující scénáře ilustrují, jak byste mohli použít zásady konsolidace dodávek, které jste vytvořili při čtení tohoto článku. Každý scénář vás provede procesem konsolidace dodávek, který používá zásady konsolidace dodávek během automatizovaného nebo ručního uvolnění do skladu:

- Scénář 1: [Konsolidace dodávek při jejich uvolnění do skladu pomocí automatického uvolnění prodejních objednávek](../warehousing/consolidate-shipments-automatic.md)
- Scénář 2: [Konsolidace dodávek, když je zásada konsolidace dodávek přepsána ze stránky Uvolnění do skladu](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Scénář 3: [Konsolidace dodávek pomocí uvolnění do skladu z pracovní plochy plánování vytížení](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Scénář 4: [Konsolidace dodávek pomocí pracovní plochy dodávek zásilek](../warehousing/consolidate-shipments-manual-workbench.md)
- Scénář 5: [Ruční konsolidace dodávek pomocí stránky konsolidace dodávek](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Další prostředky

- [Přehled zásad konsolidace dodávek](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
