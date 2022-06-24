---
title: Tvorba a zpracování vlny
description: Tento článek popisuje, jak vytvořit, zpracovat a vydat vlnu a vytvořit tak výdej nákladu, dodávku, výrobní zakázku nebo kanbanovou objednávku.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3347db6395b7da396c42f84881060f476346d2e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851268"
---
# <a name="wave-creation-and-processing"></a>Tvorba a zpracování vlny

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvořit, zpracovat a vydat vlnu a vytvořit tak výdej nákladu, dodávku, výrobní zakázku nebo kanbanovou objednávku. Můžete vytvářet vlny pro následující typy objednávek:

- **Prodejní objednávky** – pomocí vln expedice můžete zahrnout řádky z prodejní objednávky. Při vydání prodejní objednávky do skladu lze řádky prodejní objednávky zahrnout do vlny.
- **Výrobní zakázky** – pomocí vln výroby můžete zahrnout řádky z kusovníku (BOM) pro produkt.
- **Kanbanové objednávky** – vlny kanbanu zahrnují řádky výdejky z objednávek kanbanu.

V případě prodejních objednávek a zakázek kanbanu je třeba vyhradit zásoby před vydáním objednávky do skladu. V opačném případě položky nebo řádky přidělení nelze zpracovat ve vlně. Výrobní zakázky jsou však mírně pružnější. U výrobních zakázek můžete zvolit jednu z následujících možností:

- Požadujte, aby byl veškerý materiál vyhrazen před tím, než je možné výrobní zakázku uvolnit do skladu.
- Povolte vydání výrobních zakázek do skladu, i když nelze mít vyhrazeny všechny materiály. Pokud vyberete tuto možnost, je nutné ručně opakovat proces vydání do skladu, jakmile budou k dispozici další materiály. Například je to užitečné v případě, kdy vlastníte materiály potřebné k zahájení výroby, a můžete počkat, než budou k dispozici další materiály.

Můžete určit, která z těchto možností výrobní zakázky se má ve výchozím nastavení použít, pomocí pole **Požadavek na rezervaci materiálu** na stránce **Parametry řízení výroby**. Nastavení pro každou jednotlivou výrobní zakázku lze však podle potřeby změnit. Další informace viz [Parametry skladu pro zpracování vlny](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Vytvoření a zpracování vlny

Následující diagram ukazuje postup pro vytvoření, zpracování a uvolnění vln expedice. Čísla odpovídají sekcím dále v této sekci.

![Proces vytvoření vlny.](media/wave-processing-diagram.png "Proces vytvoření vlny")

### <a name="prerequisites"></a>Předpoklady

Než začnete, musí být k dispozici šablona pro typ vlny, kterou chcete vytvořit (expedice, výroba nebo kanban). Šablona vlny má mnoho nastavení, podle kterých bude vlna generována a zpracována, včetně kroků, které je třeba provést ručně a které se provádějí automaticky. Další informace naleznete v tématu [Šablony vlny](wave-templates.md).

### <a name="create-a-wave"></a>Vytvořit vlnu

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Automatické vytváření vln na základě skladu a typu objednávky

Chcete-li vlny vytvořit automaticky, nastavte [šablony vlny](wave-templates.md), které platí pro každý příslušný typ objednávky a sklad. Ujistěte se, že každá šablona má možnost **Automatizovat vytvoření vlny** nastavenu na *Ano*.

#### <a name="manually-create-waves"></a>Ruční vytvoření vln

Chcete-li vlnu vytvořit ručně, postupujte následovně:

1. Ujistěte se, že relevantní [šablony vlny](wave-templates.md) nejsou nastaveny na automatické vytváření vln pro sklady a typy objednávek, kde to chcete provést ručně.
1. V závislosti na typu vlny, kterou chcete vytvořit, proveďte jeden z následujících kroků:

    - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny expedice** \> **Všechny vlny**. V podokně akcí vyberte **Vlna**.
    - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny výroby** \> **Všechny vlny výroby**. V podokně akcí vyberte **Vlna výroby**.
    - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny kanbanu** \> **Všechny vlny kanbanu**. V podokně akcí vyberte **Vytvořit vlnu**.

1. Do pole **Popis** zadejte stručný popis vlny. Ten by měl označovat to, co chcete zpracovat ve vlně.

1. V poli **Název šablony vlny** vyberte šablonu vlny pro typ vlny, kterou chcete vytvořit. Šablona vlny obsahuje metody vlny, které budou provádět akce, jako například vytváření práce pro vlnu. Šablona vlny pro vlny expedice může například obsahovat metody vytváření nákladů, přidělování řádků k vlnám, doplnění a vytvoření výdeje pro vlnu.

1. Pokud chcete použít atributy vln jako další kritéria dotazu pro vlnu, vyberte atributy v polích **Atributy vlny**.

### <a name="specify-what-to-include-in-a-wave"></a>Zadání obsahu vlny

Po vytvoření vlny do ní můžete začít přidávat obsah.

> [!NOTE]
> V případě potřeby můžete do vlny přidat řádky i poté, co byla zpracována, dokud není uvolněna.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Automatické zadání obsahu vlny

Chcete-li vlny vytvořit automaticky, nastavte [šablony vlny](wave-templates.md), které platí pro každý příslušný typ objednávky a sklad. Ujistěte se, že každá šablona má možnost **Automatizovat vytvoření vlny** nastavenu na *Ano*. Alternativně by vaše šablona mohla automaticky přiřadit řádky do jakékoli kvalifikované otevřené vlny, pokud je možnost **Přiřaďte k otevřeným vlnám** nastavena na *Ano*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Ruční zadání obsahu vlny

Když je vlna vytvořena, ale ještě nebyla vydána, můžete ručně určit, co má obsahovat. Ruční přidání řádků do vlny:

1. V závislosti na typu vlny, do které chcete přidat řádky, proveďte jeden z následujících kroků:

    - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny expedice** \> **Všechny vlny**. V podokně akcí vyberte **Vlna**.
    - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny výroby** \> **Všechny vlny výroby**. V podokně akcí vyberte **Vlna výroby**.
    - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny kanbanu** \> **Všechny vlny kanbanu**. V podokně akcí vyberte **Vytvořit vlnu**.

1. Vyberte vlnu. V podokně akcí vyberte některou z následujících možností:

      - **Spravovat dodávky**
      - **Spravovat výroby**
      - **Spravovat seznamy výdejek kanbanových úloh**

1. V horní části okna vyberte řádek, který chcete přidat do vlny, a poté vyberte **Přidat do vlny**. Řádek se přesune na záložku s náhledem **Řádky vlny**.

    Tento krok zopakujte pro každý řádek, který chcete přidat. Chcete-li přidat všechny řádky, vyberte **Přidat vše**.

    > [!TIP]
    > U vln dodávek můžete rychle vyhledat určitou objednávku výběrem vlastního filtru v poli **Kód filtru vlny**. Kódy filtru vlny obsahují kritéria dotazu pro dodávky, které jsou vytvořeny ve formuláři **Filtry vlny**. Toto pole není k dispozici pro vlny výroby nebo vlny kanbanu.
    > Zelené znaménko zaškrtnutí ve sloupci **Pro vlnu** označuje, že dodávka byla přidána do vlny.

### <a name="process-the-wave-to-create-the-picking-work"></a>Zpracování vlny a vytvoření výdeje

Poté, co byla vytvořena vlna, která obsahuje všechny požadované řádky, jste připraveni ji zpracovat a vytvořit odpovídající práci výdeje.

#### <a name="automatically-process-a-wave"></a>Automatické zpracování vlny

Chcete-li automaticky zpracovat vlnu, nastavte příslušné [šablony vlny](wave-templates.md) s potřebnými možnostmi automatického zpracování.

#### <a name="manually-process-a-wave"></a>Ruční zpracování vlny

Vlnu můžete zpracovat pouze v případě, že **Stav vlny** je *Vytvořeno*. Po zpracování vlny se **Stav vlny** změní na *Pozastaveno*.

Chcete-li ručně zpracovat vlnu, která má veškerý požadovaný obsah, postupujte takto:

1. V závislosti na typu vlny, kterou chcete zpracovat, proveďte jeden z následujících kroků:

    - Vyberte **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny expedice** \> **Všechny vlny**. V podokně akcí vyberte **Vlna**.
    - Vyberte **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny výroby** \> **Všechny vlny výroby**. V podokně akcí vyberte **Vlna výroby**.
    - Vyberte **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny kanbanu** \> **Všechny vlny kanbanu**. V podokně akcí vyberte **Vytvořit vlnu**.

1. Vyberte vlnu pro zpracování. V podokně akcí klikněte na možnost **Zpracovat**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Vydání vlny do skladu a následné zahájení vydání a balení

Před vydáním vlny je nutné ji zpracovat. Po vydání vlny bude ve skladu k dispozici možnost vydání. Vlnu po uvolnění můžete zrušit a přidat další řádky, ale řádky již nelze změnit.

#### <a name="automatically-release-a-wave"></a>Automatické uvolnění vlny

Chcete-li automaticky zpracovat vlnu, nastavte příslušné [šablony vlny](wave-templates.md) s potřebnými možnostmi automatického zpracování.

#### <a name="manually-release-a-wave"></a>Ruční uvolnění vlny

Chcete-li vlnu vydat ručně, postupujte následovně:

1. V závislosti na typu vlny, kterou chcete uvolnit, proveďte jeden z následujících kroků:

      - Vyberte **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny expedice** \> **Všechny vlny**. V podokně akcí vyberte **Vlna**.
      - Vyberte **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny výroby** \> **Všechny vlny výroby**. V podokně akcí vyberte **Vlna výroby**.
      - Vyberte **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny kanbanu** \> **Všechny vlny kanbanu**. V podokně akcí vyberte **Vytvořit vlnu**.

1. Vyberte vlnu pro vydání. V podokně akcí vyberte **Uvolnit vlnu**.

## <a name="containerize-a-wave"></a>Rozdělení vlny do kontejnerů

Automatizované vytváření kontejnerů vytvoří kontejnery a práci výdeje pro dodávky při zpracování vlny. Podrobnosti o nastavení najdete v části [Vytváření kontejnerů](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Práce s plánovaným vytvořením práce

Když je povolena funkce *Naplánovat vytvoření práce*, zpracování ve vlnách vytvoří plánovanou práci, která bude nakonec použita v novém procesu vytváření práce. Během vytváření práce bude práce blokována pomocí funkce *Blokování práce v celé organizaci*. Další informace viz [Plánování vytváření práce během vlny](configure-wave-schedule-work-creation.md).

Následující vývojový diagram ukazuje, jak se během zpracování ve vlnách vytváří plánovaná práce.

![Naplánovat vytvoření práce.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Plánovaná práce

Stránka **Podrobnosti o plánované práci** (**Řízení skladu \> Práce \> Podrobnosti plánované práce**) zobrazuje informace o plánované práci, která je původně vytvořena během zpracování ve vlnách. K dispozici jsou následující hodnoty **stavu procesu**:

- **Ve frontě** - Plánovaná práce čeká na použití k vytvoření práce.
- **Dokončeno** - Plánovaná práce byla použita k vytvoření práce.
- **Selhání** - Zpracování ve vlnách selhalo. Všimněte si, že plánovaná práce může být ve stavu **Selhání** s nebo bez související skutečné práce. Když selže proces vytváření skutečné práce, zůstane skutečná práce ve stavu *Zrušeno*.

### <a name="batch-job-for-the-work-creation-process"></a>Dávková úloha pro proces vytváření práce

Chcete-li zobrazit dávkové úlohy pro zpracování ve vlnách, vyberte **Dávkové úlohy** v podokně akcí na straně **Všechny vlny**.

Odtud můžete zobrazit všechny podrobnosti dávkové úlohy pro každé ID dávkové úlohy.

## <a name="cancel-a-wave"></a>Zrušení vlny

V případě potřeby můžete zrušit vlnu, která byla zpracována. Pokud chcete zrušit vlnu a vytvořený výdej, postupujte takto:

1. V závislosti na typu vlny, kterou chcete zrušit, proveďte jeden z následujících kroků:

      - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny expedice** \> **Všechny vlny**.
      - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny výroby** \> **Všechny vlny výroby**.
      - Přejděte na **Řízení skladu** \> **Společné** \> **Vlny** \> **Vlny kanbanu** \> **Všechny vlny kanbanu**.

1. Vyberte vlnu, kterou chcete zrušit. V podokně akcí na kartě **Práce** zvolte **Zrušit**.

## <a name="review-wave-batch-job-details"></a>Kontrola podrobností dávkové úlohy vlny

Na stránce **Podrobnosti dávkové úlohy vlny** můžete zkontrolovat dávkové úlohy a souvisejících úkoly spojené s jakoukoli vlnou. To je užitečné zejména při řešení problémů s vlnou, která selhala. Bez této funkce budou mít přístup k podrobnostem dávkové úlohy obvykle pouze správci. Stránku **Podrobnosti dávkové úlohy vlny** lze zpřístupnit uživatelům bez oprávnění správce a poskytuje zobrazení dávkových úloh a souvisejících úkolů pouze pro čtení.

### <a name="turn-the-wave-batch-job-details-page-on-or-off"></a>Zapnutí nebo vypnutí stránky podrobností dávkové úlohy vlny

Od verze Supply Chain Management 10.0.25 je stránka **Podrobnosti dávkové úlohy vlny** ve výchozím nastavení zapnuta. Správci mohou tuto funkci zapnout nebo vypnout vyhledáním funkce *Podrobnosti dávkové úlohy vlny* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="use-the-wave-batch-job-details-page"></a>Použití stránky podrobností dávkové úlohy vlny

Stránka **Podrobnosti dávkové úlohy vlny** kombinuje dávkové úlohy a úkoly dávkových úloh, což vám umožňuje prozkoumat všechny kroky vlny, aniž byste museli procházet sem a tam mezi jednou dávkovou úlohou a seznamem dávkových úkolů. Stránka také poskytuje přístup k dávkovému protokolu a pokud máte požadovaná oprávnění, poskytuje odkaz na stránku **Dávkové úlohy**.

Chcete-li otevřít tuto stránku, vyberte vlnu na kterékoli z několika různých stránek vln a poté vyberte **Podrobnosti dávkové úlohy vlny** z podokna akcí.

## <a name="review-load-validation-and-error-messages"></a>Kontrola ověření vytížení a chybové zprávy

Během zpracování vlny systém ověřuje a zobrazuje stav pro každý řádek vytížení ve vlně. Pokud se neobjeví žádná varování, pokračuje k dalšímu kroku vlny. Pokud se objeví varování, zobrazí se po dokončení ověření celé vlny následující chyba:

> Nalezeny neplatné řádky zatížení ve vlně. Odstraňte neplatné řádky zatížení.

Poté budete moci zkontrolovat konečný stav každého řádku zatížení ve vlně a opravit všechna varování, než to zkusíte znovu. To vám umožní řešit všechna varování najednou před opětovným zpracováním vlny. (V předchozích verzích systém přestal zpracovávat vlnu po prvním varování, takže varování bylo možné opravit pouze jedno po druhém.)

Způsob, jakým systém zobrazuje vaše stavové zprávy o zpracování vln, závisí na tom, jak jste nastavili možnost **Vytvořit protokol historie zpracování vln** na stránce **Parametry řízení skladu**.

- Když je možnost **Vytvořit protokol historie zpracování vln** nastavena na *Ne*, jsou stavové zprávy řádku zatížení zobrazeny v **informačním protokolu**.
- Když je možnost **Vytvořit protokol historie zpracování vln** nastavena na *Ano*, jsou stavové zprávy řádku zatížení zobrazeny na stránce **Protokol historie zpracování vln**. Chcete-li zobrazit protokol, přejděte na **Řízení skladu \> Odchozí vlny \> Protokol historie zpracování vln**.

## <a name="additional-resources"></a>Další prostředky

- [Příklad konfigurace zpracování vlny](tasks/configure-wave-processing.md)
- [Šablony vlny](wave-templates.md)
- [Vytváření kontejnerů](wave-containerization.md)