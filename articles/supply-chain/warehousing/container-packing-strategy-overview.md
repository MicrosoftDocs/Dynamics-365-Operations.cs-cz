---
title: Strategie balení kontejnerů
description: Toto téma popisuje rozdíly mezi strategiemi balení kontejnerů a poskytuje příklady.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292754"
---
# <a name="container-packing-strategies"></a>Strategie balení kontejnerů

*Strategie balení kontejnerů* je strategie, kterou můžete použít k definování přidělení položek napříč kontejnery. Toto téma vysvětluje rozdíly mezi strategiemi *Zabalit do všech otevřených kontejnerů* a *Zabalit pouze do aktuálního kontejneru*.

- **Zabalit do všech otevřených kontejnerů** - Systém musí zkontrolovat všechny otevřené kontejnery, které již byly vytvořeny během cyklu kontejnerizace, aby se ujistil, že se položka vejde do jednoho z nich. Během balení systém kontroluje každou položku, aby určil, zda se vejde do některého z dříve vytvořených kontejnerů. Pokud se položka nevejde do existujícího kontejneru, systém vytvoří nový kontejner a pokračuje, dokud nedokončí zabalení celé objednávky.

    Například *n* objednaných položek vyžaduje kontejnerizaci. V nejhorším případě pokaždé, když systém zpracuje položku, která se nevejde do žádného existujícího kontejneru, provede celkem (\[(*n* - 1) × (*n* + 1)\] ÷ 2) kontrol, zda se položka vejde do existujících kontejnerů.

- **Zabalit pouze do aktuálního kontejneru** – Systém musí zkontrolovat pouze naposledy vytvořený kontejner, aby se ujistil, že se do něho položka vejde. Během balení systém kontroluje každou položku, aby určil, zda se vejde do naposledy vytvořeného kontejneru. Pokud se položka nevejde do kontejneru, systém vytvoří nový kontejner a pokračuje, dokud nedokončí zabalení celé objednávky.

    Například *n* objednaných položek vyžaduje kontejnerizaci. V nejhorším případě systém udělá celkem (*n* - 1) kontrol, zda se předmět vejde do kontejnerů.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Příklad postupu pro strategie balení kontejnerů

Pro kontejnerizaci jste nastavili následující položky.

| Zboží | Fyzické rozměry (šířka × hloubka × výška) | Váha |
|---|---|---|
| Kabel HDMI 6' | 1 × 1 × 1 | 1 |
| Kabel HDMI 12' | 2 × 1 × 1 | 1 |
| Kabel HDMI 18' | 3 × 1 × 1 | 2 |

Také nastavíte následující pole, které bude použito pro balení.

| Kontejner | Fyzické rozměry (délka × šířka × výška) | Váha | Objem |
|---|---|---|---|
| Střední box | 6 × 3 × 2 | 10 | 100 |

Nakonec nastavíte objednávku, která obsahuje následující produkty a množství.

| Řádek prodejní objednávky | Množství |
|---|---|
| Kabel HDMI 12' | 9 |
| Kabel HDMI 18' | 8 |
| Kabel HDMI 6' | 13 |

Následující tabulka shrnuje, jak kontejnerizace funguje, když používáte strategii *Zabalit do všech otevřených kontejnerů* a když použijete strategii *Zabalit pouze do aktuálního kontejneru*.

| Zabalit do všech otevřených kontejnerů | Zabalte do aktuálního kontejneru |
|---|---|
| <p>Kabel HDMI 12':</p><ol><li>Vytvoření nového kontejneru CONT0001.</li><li>Vložte 9 ea do kontejneru CONT0001.</li></ol> | <p>Kabel HDMI 12':</p><ol><li>Vytvoření nového kontejneru CONT0001.</li><li>Vložte 9 ea do kontejneru CONT0001.</li></ol> |
| <p>Kabel HDMI 18':</p><ol><li>Zkontrolujte, zda se položka vejde do kontejneru CONT0001.</li><li>Vytvoření nového kontejneru CONT0002.</li><li>Vložte 5 ea do kontejneru CONT0002.</li><li>Vytvoření nového kontejneru CONT0003.</li><li>Vložte 3 ea do kontejneru CONT0003.</li></ol> | <p>Kabel HDMI 18':</p><ol><li>Zkontrolujte, zda se položka vejde do kontejneru CONT0001.</li><li>Vytvoření nového kontejneru CONT0002.</li><li>Vložte 5 ea do kontejneru CONT0002.</li><li>Vytvoření nového kontejneru CONT0003.</li><li>Vložte 3 ea do kontejneru CONT0003.</li></ol> |
| <p>Kabel HDMI 6':</p><ol><li>Zkontrolujte, zda se položka vejde do kontejneru CONT0001.</li><li>Vložte 1 ea do kontejneru CONT0001.</li><li>Zkontrolujte, zda se položka vejde do kontejneru CONT0002.</li><li>Zkontrolujte, zda se položka vejde do kontejneru CONT0003.</li><li>Vložte 4 ea do kontejneru CONT0003.</li><li>Vytvoření nového kontejneru CONT0004.</li><li>Vložte 8 ea do kontejneru CONT0004.</li></ol> | <p>Kabel HDMI 6':</p><ol><li>Zkontrolujte, zda se položka vejde do kontejneru CONT0003.</li><li>Vložte 4 ea do kontejneru CONT0003.</li><li>Vytvoření nového kontejneru CONT0004.</li><li>Vložte 9 ea do kontejneru CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Příklad scénáře: Balení jednotlivých objednávek na kontejner

Tato část představuje scénář, kdy je systém nastaven na konsolidaci více objednávek do jedné zásilky. Proto bude kontejnerizace provedena z prodejní objednávky, aby bylo zajištěno, že každá objednávka, která obsahuje více produktů, je zabalena do vlastního kontejneru.

Tato funkce umožňuje zpracovávat scénáře, kdy musíte do každého kontejneru zabalit pouze jednu prodejní objednávku, aby distribuční centrum mohlo provést cross docking plných kontejnerů mezi maloobchodními prodejnami. Kromě scénářů maloobchodu (objednávka na maloobchod a dodávka do distribučního centra pro cross-docking) se tato technika také běžně používá v štíhlých dodavatelských řetězcích (prodejní objednávka na výrobní linku just-in-time).

Tento scénář ukazuje, jak můžete pomocí aplikace snížit počet kontejnerů, které jsou vyhodnocovány během balení pomocí strategi *Zabalit pouze do aktuálního kontejneru* pro kontejnerizaci.

### <a name="prerequisites"></a>Předpoklady

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Zapněte ve svém systému funkci Konsolidovat zásilky

Tento scénář používá funkci *Konsolidovat zásilky*. Pokud tato funkce ve vašem systému již není k dispozici, musíte ji zapnout pomocí [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Tento scénář odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.

### <a name="inspect-or-create-container-types"></a>Zkontrolujte nebo vytvořte typy kontejnerů

Chcete-li zkontrolovat typy kontejnerů nebo vytvořit nové typy kontejnerů, pokud jsou požadovány, postupujte takto.

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Typy kontejnerů**.
1. Ujistěte se, že ve vašich ukázkových datech je k dispozici každý z následujících typů kontejnerů. Podle potřeby upravte nebo vytvořte typy kontejnerů.

    - typ kontejneru 1:

        - **Kód typu kontejneru:** *Velká krabice*
        - **Popis:** *Velká krabice*
        - **Maximální čistá hmotnost** *100*
        - **Objem** *400*
        - **Délka:** *4*
        - **Šířka:** *10*
        - **Výška:** *10*

    - typ kontejneru 2:

        - **Kód typu kontejneru:** *Střední krabice*
        - **Popis:** *Střední box*
        - **Maximální čistá hmotnost** *50*
        - **Objem** *200*
        - **Délka:** *2*
        - **Šířka:** *10*
        - **Výška:** *10*

    - typ kontejneru 3:

        - **Kód typu kontejneru:** *Malá krabice*
        - **Popis:** *Malá krabice*
        - **Maximální čistá hmotnost** *20*
        - **Objem** *100*
        - **Délka:** *1*
        - **Šířka:** *10*
        - **Výška:** *10*

### <a name="inspect-or-create-container-groups"></a>Zkontrolujte nebo vytvořte skupiny kontejnerů

Chcete-li zkontrolovat skupiny kontejnerů nebo vytvořit nové skupiny kontejnerů, pokud jsou požadovány, postupujte takto.

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Skupiny kontejnerů**.
1. Ujistěte se, že ve vašich ukázkových datech je k dispozici každá z následujících skupin kontejnerů. Pokud není k dispozici, vyberte **Nový** a vytvořte jej.

    - **ID skupiny kontejnerů:** *Krabice*
    - **Popis:** *Velikosti krabic*

1. Na pevné záložce **Podrobnosti** pro skupinu kontejnerů *Krabice* se ujistěte, že existují následující řádky. Pokud ne, vyberte **Nový** a přidejte je.

    - Řádek 1:

        - **Pořadové číslo:** *1*
        - **Typ kontejneru:** *Velká krabice*
        - **Procento využití kontejneru:** *100*

    - Řádek 2:

        - **Pořadové číslo:** *2*
        - **Typ kontejneru:** *Střední krabice*
        - **Procento využití kontejneru:** *100*

    - Řádek 3:

        - **Pořadové číslo:** *3*
        - **Typ kontejneru:** *Malá krabice*
        - **Procento využití kontejneru:** *100*

### <a name="create-a-new-container-build-template"></a>Vytvořte novou šablonu sestavení kontejneru

Chcete-li vytvořit novou šablonu sestavení kontejneru, postupujte podle následujících pokynů.

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Šablona sestavení kontejneru**.
1. Vyberte **Nový** k vytvoření šablony sestavení kontejneru, která má následující nastavení:

    - **Pořadové číslo:** *1*
    - **ID šablony kontejneru:** *Krabice*
    - **ID skupiny kontejnerů:** *Krabice*
    - **Základní typy dotazů:** *Řádek přidělení prodeje*
    - **Kód kroku vlny:** *234*
    - **Povolit rozdělení výdejů:** *Ano*
    - **Strategie balení kontejneru:** *Zabalit pouze do aktuálního kontejneru*
    - **Balení podle direktivní jednotky:** *Ne*

1. Zatímco je stále vybrán řádek pro novou šablonu, vyberte v podokně akcí možnost **Upravit dotaz**.
1. Zobrazí se standardní dialogové okno editoru dotazů. Na kartě **Řazení** vyberte **Přidat** a přidejte řádek, který má následující nastavení:

    - **Tabulka:** *Dočasné pracovní transakce*
    - **Odvozená tabulka:** *Dočasné pracovní transakce*
    - **Pole:** *Číslo objednávky*
    - **Směr hledání:** *Vzestupně*

    > [!IMPORTANT]
    > Chcete-li se vyhnout cyklování nad všemi ostatními otevřenými kontejnery a urychlit proces kontrolou jednoho kontejneru po druhém, použijte strategii *Zabalit pouze do aktuálního kontejneru* kromě třídění podle čísla objednávky. Tato kombinace bude fungovat jako pracovní přestávka na pracovní šabloně.

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Zatímco je stále vybrán řádek pro novou šablonu, vyberte v podokně akcí možnost **Omezení kombinování obsahu kontejnerů**.

    Nyní přidáte omezení, které vloží položky z jedné objednávky do jednoho kontejneru. Položky z jakékoli jiné objednávky budou vloženy do samostatného kontejneru.

1. Vyberte **Nový** k vytvoření omezení kombinování, které má následující nastavení:

    - **Tabulka:** *Prodejní objednávky*
    - **Výběr pole:** *SalesId* (Pole se zobrazí jako *Prodejní objednávka* v mřížce.)

1. Zvolte **OK** pro přidání omezení.
1. Zavřete stránku.

### <a name="set-up-a-wave-template-for-containerization"></a>Nastavení šablony vlny pro rozdělení do kontejnerů

Chcete-li nastavit šablonu vlny, postupujte následujícím způsobem.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V podokně seznamů nastavte v poli **Typ šablony vlny** na hodnotu *Dodávka*.
1. Vyberte šablonu **Kontejnerizace 63** v seznamu.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Metody** ve sloupci **Vybrané metody** najděte následující řádek:

    - **Název metody:** *kontejnerizace*
    - **Název:** *Kontejnerizace*

1. Nastavte pole **Kód kroku vlny** pro řádek na *234*.

### <a name="set-up-a-work-template"></a>Nastavit šablonu práce

Chcete-li nastavit šablonu práce, postupujte následujícím způsobem.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Pole **Typ pracovního příkazu** nastavte na *Prodejní objednávky*.
1. V mřížce **Přehled** vyhledejte a vyberte pracovní šablonu, která by měla být použita pro balení jednorázových objednávek na kontejner. V tomto scénáři vyberte šablonu **63 vydat pro kontejner**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. Zobrazí se standardní dialogové okno editoru dotazů. Na kartě **Řazení** přidejte následující řádky:

    - Řádek 1:

        - **Tabulka:** *Dočasné pracovní transakce*
        - **Odvozená tabulka:** *Dočasné pracovní transakce*
        - **Pole:** *ID dodávky*
        - **Směr hledání:** *Vzestupně*

    - Řádek 2:

        - **Tabulka:** *Dočasné pracovní transakce*
        - **Odvozená tabulka:** *Dočasné pracovní transakce*
        - **Pole:** *Číslo objednávky*
        - **Směr hledání:** *Vzestupně*

    - Řádek 3:

        - **Tabulka:** *Dočasné pracovní transakce*
        - **Odvozená tabulka:** *Dočasné pracovní transakce*
        - **Pole:** *ID kontejneru*
        - **Směr hledání:** *Vzestupně*

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“ Pokračujte výběrem tlačítka **Ano**.
1. Zatímco šablona **63 Výdej do kontejneru** je stále vybrána, vyberte **Přerušení pracovního záhlaví** v podokně akcí.

    Nyní použijete nastavení pro přerušení práce tak, aby každý kontejner v objednávce byl propojen s jedním pracovním příkazem.

1. Zaškrtněte políčko **Seskupit podle tohoto pole** pro každý řádek na stránce **Přerušení pracovního záhlaví** (**ID zásilky**, **Číslo objednávky** a **ID kontejneru**).
1. Zavřete stránku.

### <a name="set-up-shipment-consolidation-policies"></a>Nastavit zásady konsolidace dodávek

Pokud chcete nastavit zásady konsolidace dodávky, postupujte následovně.

1. Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.
1. V podokně seznamu nastavte pole **Typ zásad** na *Prodejní objednávky*.
1. Vyberte **Výchozí** zásady v seznamu.
1. V podokně akcí vyberte **Upravit**.
1. Na záložce s náhledem **Pole konsolidace** v seznamu **Vybraná pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Číslo objednávky*.
1. Vyberte tlačítko **Odebrat** ![Levá šipka](media/backward-button.png) a přesuňte do seznamu **Zbývající pole**.
1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-physical-dimensions-for-the-product"></a>Nastavit fyzické rozměry produktu.

Chcete-li nastavit fyzické dimenze pro produkty, které budou použity v tomto scénáři, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt, kde je pole **Číslo položky** nastaveno na *A0001*.
1. V podokně Akce na kartě **Správa zásob** ve skupině **Sklad** vyberte **Fyzické rozměry**.
1. Na stránce **Fyzické rozměry** byste měli vidět následující řádek v mřížce:

    - **Jednotka:** *ks*
    - **Hrubá hmotnost:** *3.00*
    - **Šířka:** *2.00*
    - **Hloubka:** *2.00*
    - **Výška:** *4.00*
    - **Objem** *16.00*

1. Zavřete stránku.
1. Vyberte produkt, kde je pole **Číslo položky** nastaveno na *A0002*.
1. V podokně Akce na kartě **Správa zásob** ve skupině **Sklad** vyberte **Fyzické rozměry**.
1. Na stránce **Fyzické rozměry** byste měli vidět následující řádek v mřížce:

    - **Jednotka:** *ks*
    - **Hrubá hmotnost:** *4.00*
    - **Šířka:** *3.00*
    - **Hloubka:** *1.00*
    - **Výška:** *3.00*
    - **Objem** *9.00*

### <a name="create-sales-order-1"></a>Vytvoření prodejní objednávky 1

Chcete-li vytvořit prodejní objednávku, postupujte následujícím způsobem.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. Zobrazí se dialogové okno pro vytvoření nové prodejní objednávky. Nastavte následující hodnoty:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *63*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Na kartě s náhledem **Řádky prodejní objednávky** přidejte následující prodejní řádky:

    - Řádek 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *2*

    - Řádek 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *2*

1. Vyberte první řádek a poté vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**. Poté stránku zavřete.
1. Opakujte předchozí dva kroky pro druhý řádek.
1. Zavřete stránku.

### <a name="create-sales-order-2"></a>Vytvoření prodejní objednávky 2

Chcete-li vytvořit druhou prodejní objednávku, postupujte následujícím způsobem.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. Zobrazí se dialogové okno pro vytvoření nové prodejní objednávky. Nastavte následující hodnoty:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *63*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Na kartě s náhledem **Řádky prodejní objednávky** přidejte následující prodejní řádky:

    - Řádek 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *4*

    - Řádek 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *4*

1. Vyberte první řádek a poté vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**. Poté stránku zavřete.
1. Opakujte předchozí dva kroky pro druhý řádek.
1. Zavřete stránku.

### <a name="create-the-load"></a>Vytvoření vytížení

Chcete-li vytvořit náklad pro každou sadu objednávek, kterou jste vytvořili pro tento scénář, a poté ji uvolnit do skladu, postupujte takto.

1. Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.
1. Na kartě **Řádky prodeje** najděte a vyberte všechny řádky prodejních objednávek z prodejních objednávek, které jste pro tento scénář vytvořili.
1. V podokně Akce na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do nového vytížení**. Vybrané řádky objednávky se přidají k novému nákladu.
1. V dialogovém okně **Přiřazení šablony nákladu** v poli **ID šablony nákladu** vyberte šablonu nákladu, například *Kontejner 40'*.
1. Zvolte **OK** a zavřete dialogové okno.
1. V části **Náklady** vyhledejte a vyberte náklad, který jste právě vytvořili.
1. Vyberte **Uvolnění \> Uvolnění do skladu**.
1. V dialogovém okně **Uvolnění do skladu** vyberte **OK** pro uvolnění vybraného nákladu do skladu.

### <a name="verify-the-shipments-and-containers"></a>Ověřte zásilky a kontejnery

Následující postup vám umožní ověřit vytvořené zásilky. Použijte jej ke kontrole objednávky, kterou jste vytvořili pro tento scénář, abyste se ujistili, že jste získali očekávané výsledky.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Najděte a vyberte zásilku, která byla vytvořena pro náklad, který jste právě uvolnili.
1. V podokně akcí na kartě **Doprava** vyberte **Zobrazit kontejnery**.
1. Potvrďte, že položky z prodejních objednávek byly kontejnerizovány do dvou různých kontejnerů.

## <a name="additional-resources"></a>Další prostředky

- [Vytváření kontejnerů](wave-containerization.md)
