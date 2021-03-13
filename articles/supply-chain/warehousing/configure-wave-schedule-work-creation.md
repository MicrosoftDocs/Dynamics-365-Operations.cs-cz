---
title: Naplánování vytvoření práce během vlny
description: Toto téma popisuje, jak nastavit a používat metodu zpracování ve vlnách Zpracovat vytvoření práce.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078240"
---
# <a name="schedule-work-creation-during-wave"></a>Naplánování vytvoření práce během vlny

[!include [banner](../includes/banner.md)]

Použijte funkci *Naplánovat vytvoření práce* jako součást vašeho procesu vln, která pomáhá zvýšit propustnost zpracování ve vlnách tím, že systém vytvoří práci pomocí paralelního zpracování.

Když je funkce povolena, automaticky se vytvoří plánovaná práce, kterou systém nakonec zpracuje a vytvoří skutečnou práci. Pokud počet linek zatížení ve vlnách dosáhne předem stanovené prahové hodnoty, systém vytvoří skutečnou práci rychleji použitím paralelního, asynchronního zpracování.

## <a name="enable-the-schedule-work-creation-feature"></a>Povolení funkce Naplánovat vytvoření práce

### <a name="enable-the-feature-in-feature-management"></a>Povolení funkce ve správě funkcí

Než můžete použít funkci *Naplánovat vytvoření práce*, musíte ji v systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Vytvoření plánu práce*

> [!NOTE]
> Funkce *Blokování v celé organizaci* musí být povolena, než budete moci povolit *Naplánování vytvoření práce*.

### <a name="manually-enable-batch-processing-of-waves"></a>Ručně povolte dávkové zpracování ve vlnách

Chcete-li využít výhod paralelní asynchronní metody k vytvoření skladové práce, musí být váš vlnový proces spuštěn dávkově. Nastavení:

1. Přejděte do nabídky  **Řízení skladu \> Nastavení \> Parametry řízení skladu**.

1. Na kartě **Obecné** nastavte **Zpracovat vlny v dávce** na *ano*. Volitelně můžete také vybrat vyhrazenou **skupinu dávek pro zpracování ve vlnách**, abyste zabránili tomu, aby vaše dávkové zpracování fronty běželo souběžně s jinými procesy.

1. Nastavte **Doba čekání na zámek (ms)**, což platí, když systém zpracovává několik vln současně. U většiny větších procesů mávání doporučujeme hodnotu *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Ručně povolte novou metodu kroku vlny pro existující šablony vln

Začněte tím, že vytvoříte novou metodu kroku vlny a povolíte ji pro paralelní asynchronní zpracování úloh.

1. Přejděte na  **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování ve vlnách**.

1. Vyberte  **Znovu generovat metodu** a všimněte si, že krok *WHSScheduleWorkCreationWaveStepMethod* byl přidán do seznamu metod zpracování ve vlnách, které můžete použít ve svých šablonách přepravních vln.

1. Vyberte záznam pomocí **názvu metody** *WHSScheduleWorkCreationWaveStepMethod* a vyberte **Konfigurace úlohy**.

1. Pokud chcete do mřížky přidat nový řádek, vyberte **Nový** v podokně úloh a použijte následující nastavení:

    - **Sklad** - Vyberte sklad, který budete používat k naplánování zpracování práce plánu.

    - **Maximální počet dávkových úloh** - Určete maximální počet dávkových úloh. Ve většině případů by tato hodnota měla být v rozsahu od 8 do 16, doporučujeme vám však experimentovat s optimálním nastavením na základě vašich scénářů.

    - **Skupina dávek pro zpracování ve vlnách** - Vyberte vyhrazenou skupinu dávek pro zpracování ve vlnách pro optimalizaci zpracování dávkové fronty.

Nyní jste připraveni aktualizovat stávající šablonu vln (nebo vytvořit novou), abyste mohli použít metodu zpracování ve vlnách *Naplánovat vytvoření práce*.

1. Přejděte na  **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.

1. V podokně úlohy vyberte **Upravit**.

1. V podokně seznamu vyberte šablonu vln, kterou chcete aktualizovat (pokud testujete pomocí ukázkových dat, můžete použít *Výchozí nastavení 24*).

1. Rozbalte kartu s náhledem **Metody** a vyberte řádek s mřížkou **Název** *naplánovat vytvoření práce* v mřížce **Zbývající metody**.

1. Vyberte šipku směřující ke sloupci **Vybrané metody** pro přesun vybraného řádku do tohoto sloupce. (Můžete mít pouze jednu vybranou metodu v jednom okamžiku, která používá *WHSScheduleWorkCreationWaveStepMethod* nebo *createWork*, takže existující řádek s **názvem metody** *createWork* se automaticky přesune do mřížky **Zbývající metody**.)

## <a name="set-wave-task-processing-threshold-data"></a>Nastavení prahových dat zpracování vlnové úlohy

Systém vytvoří výchozí prahová data zpracování vlnových úloh při prvním spuštění vlnového procesu pomocí jakéhokoli zpracování založeného na úlohách. Data se používají k řízení, kdy zpracování ve vlnách bude probíhat asynchronně a bude založeno na úkolech, což mu umožní paralelně zpracovávat a vytvářet práci.

Výchozí data budou zpočátku používat prahovou hodnotu 15 pro minimální počet řádků zatížení (MINIMUMWAVELOADLINES). To znamená, že když systém zpracovává vlnu s více než 15 řádky zatížení, použije asynchronní zpracování úloh. Tyto údaje můžete ručně vložit / aktualizovat v tabulce **WHSWaveTaskProcessingThresholdParameters** ve vašem zkušebním prostředí, ale pokud toto nastavení potřebujete změnit v provozním prostředí, musíte zažádat o aktualizaci podporu Microsoftu.

## <a name="work-with-the-feature"></a>Práce s funkcí

Když je povolena funkce *Naplánovat vytvoření práce*, zpracování ve vlnách vytvoří plánovanou práci, která bude nakonec použita v novém procesu vytváření práce. Během vytváření práce bude práce blokována pomocí funkce *Blokování práce v celé organizaci*.

Následující vývojový diagram ukazuje, jak se během zpracování ve vlnách vytváří plánovaná práce.

![Naplánovat vytvoření práce](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Plánovaná práce

Stránka **Podrobnosti o plánované práci** (**Řízení skladu \> Práce \> Podrobnosti plánované práce**) zobrazuje informace o plánované práci, která je původně vytvořena během zpracování ve vlnách. K dispozici jsou následující hodnoty **stavu procesu**:

- **Ve frontě** - Plánovaná práce čeká na použití k vytvoření práce.
- **Dokončeno** - Plánovaná práce byla použita k vytvoření práce.
- **Selhání** - Zpracování ve vlnách selhalo. Všimněte si, že plánovaná práce může být ve stavu **Selhání** s nebo bez související skutečné práce. Když selže proces vytváření skutečné práce, zůstane skutečná práce ve stavu *Zrušeno*.

### <a name="batch-job-for-the-work-creation-process"></a>Dávková úloha pro proces vytváření práce

Chcete-li zobrazit dávkové úlohy pro zpracování ve vlnách, vyberte **Dávkové úlohy** v podokně akcí na straně **Všechny vlny**.

Odtud můžete zobrazit všechny podrobnosti dávkové úlohy pro každé ID dávkové úlohy.
