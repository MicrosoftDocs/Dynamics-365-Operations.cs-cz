---
title: Naplánování vytvoření práce během vlny
description: Tento článek popisuje, jak nastavit a používat metodu zpracování ve vlnách Zpracovat vytvoření práce.
author: Mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8b4505d66c37134bc8f672b38d195f4f677df9bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852063"
---
# <a name="schedule-work-creation-during-wave"></a>Naplánování vytvoření práce během vlny

[!include [banner](../../includes/banner.md)]

Použijte funkci *Naplánovat vytvoření práce* jako součást vašeho procesu vln, která pomáhá zvýšit propustnost zpracování ve vlnách tím, že systém vytvoří práci pomocí paralelního zpracování.

Když je funkce povolena, automaticky se vytvoří plánovaná práce, kterou systém nakonec zpracuje a vytvoří skutečnou práci. Pokud počet linek zatížení ve vlnách dosáhne předem stanovené prahové hodnoty, systém vytvoří skutečnou práci rychleji použitím paralelního, asynchronního zpracování.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Ve správě funkcí zapněte funkce plánovaného vytváření práce

Chcete-li používat funkce popsané v tomto článku, musí být pro váš systém zapnuty. Použijte pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce v následujícím pořadí:

1. **Blokování práce v celé organizaci** - Vyžadováno pro ruční i automatickou konfiguraci plánovaného vytváření práce. (Od Supply Chain Management verze 10.0.21 je tato funkce povinná, takže je ve výchozím nastavení zapnutá a nelze ji znovu vypnout.)
1. **Plánování vytváření práce** - Vyžadováno pro ruční i automatickou konfiguraci plánovaného vytváření práce.
1. **Metoda vlny Plánování vytváření práce v celé organizaci** - Vyžadováno pro ruční i automatickou konfiguraci plánovaného vytváření práce. Tuto funkci nepotřebujete, pokud budete používat pouze manuální konfiguraci.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Automatická konfigurace plánovaného vytváření práce

Pokud povolíte funkci *Metoda vlny „Plánování vytváření práce“ v celé organizaci*, ve vašem systému se automaticky stane následující:

- Metoda vlny *Plánování vytvoření práce* (`WHSScheduleWorkCreationWaveStepMethod`) je přidána a nakonfigurována pro paralelní běh napříč všemi právnickými osobami.
- Šablony vln ze všech právnických osob, které mají **Typ šablony vlny** nastaven na *Expedice* a **Stav šablony** nastaven na *Platný* , bude mít metodu *Vytvoření práce* nahrazenou metodou *Plánování vytvoření práce*. Avšak šablony vlny z právnických osob, kde je povoleno opakování metody *Vytvořit práci*, nebudou upraveny.
- Konfigurace úkolů pro metodu *Plánování vytvoření práce* bude vytvořena metoda pro všechny sklady ze všech právnických osob, které mají povolenou možnost **Použít procesy řízení skladu**. To znamená, že metoda *Plánování vytvoření práce* bude nyní běžet paralelně ve výchozím nastavení. Stávající sklady, u kterých měníte **Použití procesů řízení skladu** z *Ne* na *Ano*, ve výchozím nastavení tuto metodu také spustí paralelně.
- Všechny právnické osoby budou zpracovávat vlny v dávkách a možnost **Čekat na zámek (ms)** bude nastavena na výchozí hodnotu *60 000* ms, pokud byla dříve nastavena na *0* ms.
- Všechny nové šablony vln, které vytvoříte, budou mít metodu vlny *Plánování vytvoření práce* místo metody *Vytvořit práci*.

Stávající konfigurace úloh a zpracování vln budou také zachovány pro všechny právnické osoby, které jsou již nakonfigurovány pro zpracování vln v dávkách, a pro všechny sklady, které jsou již nakonfigurovány pro paralelní použití *Plánování vytvoření práce*.

V případě potřeby můžete ručně vrátit některá nebo všechna nastavení provedená automaticky, když jste povolili funkci *Metoda vlny Plánování vytváření práce v celé organizaci*, následujícím způsobem:

- Pro šablony vln přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**. Nahraďte metodu *Plánování vytvoření práce* za *Vytvořit práci*.
- Pro parametry skladu přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**. Na kartě **Zpracování vln** použijte preferované hodnoty pro možnosti **Zpracovat vlnu v dávce** a **Čekat na zámek (ms)**.
- Pro metody vlny přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**. V podokně akcí vyberte `WHSScheduleWorkCreationWaveStepMethod` a pak **Konfigurace úlohy**. Podle potřeby upravte nebo odstraňte počet dávkových úkolů a přiřazenou skupinu vln pro každý uvedený sklad.

## <a name="manually-configure-scheduled-work-creation"></a>Ruční konfigurace plánovaného vytváření práce

Pokud jste nepovolili [funkci *Metoda vlny „Plánování vytvoření práce“ v celé organizaci*](#Auto-enable-schedule-work-creation), pak můžete použít postupy uvedené v této části k ruční konfiguraci plánovaného vytvoření práce podle potřeby.

### <a name="manually-enable-batch-processing-of-waves"></a>Ručně povolte dávkové zpracování ve vlnách

Chcete-li využít výhod paralelní asynchronní metody k vytvoření skladové práce, musí být váš vlnový proces spuštěn dávkově. Nastavení:

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Obecné** nastavte **Zpracovat vlny v dávce** na *ano*. Volitelně můžete také vybrat vyhrazenou **skupinu dávek pro zpracování ve vlnách**, abyste zabránili tomu, aby vaše dávkové zpracování fronty běželo souběžně s jinými procesy.
1. Nastavte **Doba čekání na zámek (ms)**, což platí, když systém zpracovává několik vln současně. U většiny větších procesů mávání doporučujeme hodnotu *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Ručně povolte novou metodu kroku vlny pro existující šablony vln

Začněte tím, že vytvoříte novou metodu kroku vlny a povolíte ji pro paralelní asynchronní zpracování úloh.

1. Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.
1. Vyberte **Znovu generovat metodu** a všimněte si, že krok *WHSScheduleWorkCreationWaveStepMethod* byl přidán do seznamu metod zpracování ve vlnách, které můžete použít ve svých šablonách přepravních vln.
1. Vyberte záznam pomocí **názvu metody** *WHSScheduleWorkCreationWaveStepMethod* a vyberte **Konfigurace úlohy**.
1. Pokud chcete do mřížky přidat nový řádek, vyberte **Nový** v podokně úloh a použijte následující nastavení:

    - **Sklad** - Vyberte sklad, který budete používat k naplánování zpracování práce plánu.
    - **Maximální počet dávkových úloh** - Určete maximální počet dávkových úloh. Ve většině případů by tato hodnota měla být v rozsahu od 8 do 16, doporučujeme vám však experimentovat s optimálním nastavením na základě vašich scénářů.
    - **Skupina dávek pro zpracování ve vlnách** - Vyberte vyhrazenou skupinu dávek pro zpracování ve vlnách pro optimalizaci zpracování dávkové fronty.

Nyní jste připraveni aktualizovat stávající šablonu vln (nebo vytvořit novou), abyste mohli použít metodu zpracování ve vlnách *Naplánovat vytvoření práce*.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V podokně úlohy vyberte **Upravit**.
1. V podokně seznamu vyberte šablonu vln, kterou chcete aktualizovat (pokud testujete pomocí ukázkových dat, můžete použít *Výchozí nastavení 24*).
1. Rozbalte kartu s náhledem **Metody** a vyberte řádek s mřížkou **Název** *naplánovat vytvoření práce* v mřížce **Zbývající metody**.
1. Vyberte šipku směřující ke sloupci **Vybrané metody** pro přesun vybraného řádku do tohoto sloupce. (Můžete mít pouze jednu vybranou metodu v jednom okamžiku, která používá `WHSScheduleWorkCreationWaveStepMethod` nebo `createWork`, takže existující řádek s **názvem metody** `createWork` se automaticky přesune do mřížky **Zbývající metody**.)

## <a name="set-wave-task-processing-threshold-data"></a>Nastavení prahových dat zpracování vlnové úlohy

Systém vytvoří výchozí prahová data zpracování vlnových úloh při prvním spuštění vlnového procesu pomocí jakéhokoli zpracování založeného na úlohách. Data se používají k řízení, kdy zpracování ve vlnách bude probíhat asynchronně a bude založeno na úkolech, což mu umožní paralelně zpracovávat a vytvářet práci.

Výchozí data budou zpočátku používat prahovou hodnotu 15 pro minimální počet řádků zatížení (`MINIMUMWAVELOADLINES`). To znamená, že když systém zpracovává vlnu s více než 15 řádky zatížení, použije asynchronní zpracování úloh. Tato data můžete ručně vložit/aktualizovat do tabulky `WHSWaveTaskProcessingThresholdParameters` ve vašich testovacích prostředích. Pokud potřebujete toto nastavení změnit v produkčním prostředí, musíte kontaktovat podporu Microsoftu a požádat o aktualizaci.

## <a name="work-with-the-scheduled-work-creation"></a>Práce s plánovaným vytvořením práce

Podrobnosti o tom, jak pracovat s plánovaným vytvořením práce, najdete v části [Tvorba a zpracování vln](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
