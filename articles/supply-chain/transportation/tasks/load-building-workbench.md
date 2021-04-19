---
title: Pracovní plocha sestavení vytížení
description: Toto téma popisuje, jak pracovat s pracovní plochou sestavení vytížení.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8633adbab43c95366d42cf409f5e508771c906
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809031"
---
# <a name="load-building-workbench"></a><span data-ttu-id="99a4f-103">Pracovní plocha sestavení vytížení</span><span class="sxs-lookup"><span data-stu-id="99a4f-103">Load building workbench</span></span>

<span data-ttu-id="99a4f-104">Pracovní plocha sestavení vytížení vám umožňuje při vytváření vytížení použít strategie vytváření vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="99a4f-105">Vytváření strategie sestavení vytížení</span><span class="sxs-lookup"><span data-stu-id="99a4f-105">Create a load building strategy</span></span>

<span data-ttu-id="99a4f-106">Strategie sestavení vytížení používáte k automatickému sestavení vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="99a4f-107">Tato funkce může být prospěšná v následujících situacích:</span><span class="sxs-lookup"><span data-stu-id="99a4f-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="99a4f-108">Pokud pravidelně dodáváte konkrétní sadu produktů, strategie vytížení pomáhají šetřit čas, protože nemusíte pokaždé vytvářet stejné vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="99a4f-109">Chcete-li se vyhnout napůl plným vytížením, abyste maximalizovali účinnost, mohou strategie vytížení pomoci naplnit každé vytížení co nejvíce.</span><span class="sxs-lookup"><span data-stu-id="99a4f-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="99a4f-110">Třída strategie sestavení vytížení, která je pojmenována `TMSLoadBuildingVolumeStrategy`, poskytuje strategii sestavení vytížení, která je pojmenována *Strategie sestavení vytížení na základě objemu*.</span><span class="sxs-lookup"><span data-stu-id="99a4f-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="99a4f-111">Tato strategie umožňuje použít maximální hodnoty zadané pro výšku a hmotnost v šabloně vytížení nebo přepsat nastavení zadáním nových hodnot.</span><span class="sxs-lookup"><span data-stu-id="99a4f-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="99a4f-112">Tato strategie je jedinou strategií, která je zahrnuta ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="99a4f-113">(Můžete však mít některé vlastní strategie.)</span><span class="sxs-lookup"><span data-stu-id="99a4f-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="99a4f-114">K použití předdefinované strategie *Strategie sestavení vytížení na základě objemu* ji vyberte v poli **Strategie sestavení vytížení** na stránce **Pracovní plocha sestavení vytížení** (**Řízení dopravy &gt; Plánování &gt; Pracovní plocha sestavení vytížení**).</span><span class="sxs-lookup"><span data-stu-id="99a4f-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="99a4f-115">Pro vytvoření strategie sestavení vytížení postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="99a4f-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="99a4f-116">Přejděte na **Řízení dopravy &gt; Nastavení &gt; Sestavení vytížení &gt; Strategie sestavení vytížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="99a4f-117">V podokně akcí vyberte **Generovat seznam tříd**, abyste se ujistili, že máte nejnovější verze všech dostupných tříd.</span><span class="sxs-lookup"><span data-stu-id="99a4f-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="99a4f-118">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="99a4f-119">Zadejte jedinečný název strategie, vyberte pro ni třídu strategie sestavení vytížení a zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="99a4f-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="99a4f-120">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="99a4f-121">V podokně akcí zvolte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="99a4f-122">Na stránce **Parametry strategie sestavení vytížení** vyberte v seznamu možnost **Objemová kapacita**, v poli **Hodnota** zadejte procento z celkové objemové kapacity vytížení, které by se mělo použít pro novou strategii sestavení vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="99a4f-123">Vyberte v seznamu možnost **Hmotnostní kapacita**, v poli **Hodnota** zadejte procento z celkové hmotnostní kapacity vytížení, které by se mělo použít pro novou strategii sestavení vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="99a4f-124">Zavřete stránku **Parametry strategie sestavení zatížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="99a4f-125">Zavřete stránku **Parametry sestavení zatížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="99a4f-126">Nyní můžete strategii sestavení vytížení přiřadit k šabloně sestavení vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="99a4f-127">Případně ji můžete použít přímo v pracovní ploše sestavení vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="99a4f-128">Použití strategie sestavení vytížení na pracovní ploše sestavení vytížení</span><span class="sxs-lookup"><span data-stu-id="99a4f-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="99a4f-129">Přejděte do **Správa přepravy &gt; Plánování &gt; Pracovní plocha sestavení vytížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="99a4f-130">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="99a4f-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="99a4f-131">Vyberte strategii v poli **Strategie sestavení vytížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="99a4f-132">Pokud jste definovali šablonu sestavení vytížení a přiřadili k ní strategii pro sestavení vytížení, v podokně akcí na kartě **Správa šablon** vyberte **Použít šablonu**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="99a4f-133">Pak v rozevíracím dialogovém okně **Použít šablonu sestavení vytížení** vyberte šablonu v poli **Název šablony sestavení vytížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="99a4f-134">Na záložce s náhledem **Řada šablon vytížení** vyberte jednu nebo více [šablon vytížení](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="99a4f-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="99a4f-135">Pracovní plocha se pokusí přizpůsobit vytížení do těchto typů kontejnerů v pořadí, které je zde uvedeno.</span><span class="sxs-lookup"><span data-stu-id="99a4f-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="99a4f-136">Obvykle byste měli umístit nejmenší kontejnery na začátek seznamu, abyste se ujistili, že je vybrán nejmenší možný kontejner jako první.</span><span class="sxs-lookup"><span data-stu-id="99a4f-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="99a4f-137">V podokně akcí klikněte na možnost **Navrhnout vytížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="99a4f-138">Zkontrolujte navrhovaná vytížení a navrhované řádky vytížení.</span><span class="sxs-lookup"><span data-stu-id="99a4f-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="99a4f-139">V podokně akcí vyberte **Vytvořit zatížení** a vytvořte vytížení, která jsou založena na řádcích zdrojového dokumentu na záložce s náhledem **Navrhované řádky vytížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="99a4f-140">Zavřete stránku **Pracovní plocha sestavení zatížení**.</span><span class="sxs-lookup"><span data-stu-id="99a4f-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]