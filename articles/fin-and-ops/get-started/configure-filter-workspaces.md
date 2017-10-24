---
title: "Konfigurace a filtrování pracovních prostorů"
description: "V tomto článku je přehled o tom, jak konfigurovat a filtrovat pracovní prostory."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754cd81a4550318de7003d847fafb2bcc7414b32
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="configure-and-filter-workspaces"></a><span data-ttu-id="c02bf-103">Konfigurace a filtrování pracovních prostorů</span><span class="sxs-lookup"><span data-stu-id="c02bf-103">Configure and filter workspaces</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c02bf-104">V tomto článku je přehled o tom, jak konfigurovat a filtrovat pracovní prostory.</span><span class="sxs-lookup"><span data-stu-id="c02bf-104">This article provides an overview about how to configure and filter workspaces.</span></span>

<a name="configuring-a-workspace"></a><span data-ttu-id="c02bf-105">Konfigurace pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="c02bf-105">Configuring a workspace</span></span>
-----------------------

<span data-ttu-id="c02bf-106">Aktualizováním nastavení, které platí pro celý pracovní prostor, můžete změnit vzhled a chování některých pracovních prostorů.</span><span class="sxs-lookup"><span data-stu-id="c02bf-106">You can change the appearance and behavior of some workspaces by updating settings that apply to the whole workspace.</span></span> <span data-ttu-id="c02bf-107">Pokud lze pracovní prostor konfigurovat, podokno akcí obsahuje tlačítko pro změny konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c02bf-107">When a workspace can be configured, the Action Pane includes a button that instructs you to click it to make configuration changes.</span></span> <span data-ttu-id="c02bf-108">Například na následujícím obrázku je tlačítko s názvem **Konfigurovat můj pracovní prostor**.</span><span class="sxs-lookup"><span data-stu-id="c02bf-108">For example, in the following illustration, the button is named **Configure my workspace**.</span></span> 

<span data-ttu-id="c02bf-109">[![Konfigurace a filtrování pracovních prostorů](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="c02bf-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span></span>   

<span data-ttu-id="c02bf-110">Při kliknutí na toto tlačítko se zobrazí dialogové okno, kde můžete upravit předdefinovaná nastavení pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="c02bf-110">When you click the button, a dialog appears, where you can modify the predefined settings for the workspace.</span></span> <span data-ttu-id="c02bf-111">Specifická nastavení, která se zobrazí v tomto dialogovém okně, budou u každého pracovního prostoru jiná a závisí na konkrétních ovládacích prvcích a obchodních datech, která jsou v pracovním prostoru k dispozici.</span><span class="sxs-lookup"><span data-stu-id="c02bf-111">The specific settings that you see in this dialog vary by workspace, and depend on the specific controls and business data that are available in the workspace.</span></span> 

<span data-ttu-id="c02bf-112">[![Konfigurace mého pracovního prostoru](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="c02bf-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span></span>

## <a name="filtering-a-workspace"></a><span data-ttu-id="c02bf-113">Filtrování pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="c02bf-113">Filtering a workspace</span></span>
<span data-ttu-id="c02bf-114">Mnoho pracovních prostorů umožňuje filtrovat obsah, který se v nich má zobrazit.</span><span class="sxs-lookup"><span data-stu-id="c02bf-114">Many workspaces let you filter the content that appears in them.</span></span> <span data-ttu-id="c02bf-115">Ovládací prvky, které jsou k dispozici, mohou umožňovat filtrování veškerého obsahu v pracovním prostoru nebo pouze obsahu v určité části pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="c02bf-115">The controls that are available might let you filter all the content in the workspace or only the content in a specific section of the workspace.</span></span> <span data-ttu-id="c02bf-116">Filtry pracovního prostoru mohou mít podobu vyhledávání, polí se seznamem, polí s volným textem nebo jiných typů ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="c02bf-116">The filters on workspaces can be lookups, combo boxes, free-form text fields, or other types of controls.</span></span> <span data-ttu-id="c02bf-117">Každý typ filtru má však stejný účinek, jak je popsáno v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="c02bf-117">However, every type of filter has the same effects, as described in the following sections.</span></span>

### <a name="workspace-wide-filters"></a><span data-ttu-id="c02bf-118">Filtry celého pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="c02bf-118">Workspace-wide filters</span></span>

<span data-ttu-id="c02bf-119">Celý pracovní prostor můžete filtrovat pomocí filtru celého pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="c02bf-119">You can filter the whole workspace by using a workspace-wide filter.</span></span> <span data-ttu-id="c02bf-120">Filtr celého pracovního prostoru je zobrazený v horním levém rohu pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="c02bf-120">A workspace-wide filter appears in the upper-left corner of the workspace.</span></span> <span data-ttu-id="c02bf-121">Když vyberete konkrétní hodnotu v rozevíracím seznamu, obsah pracovního prostoru bude filtrován na základě tohoto výběru.</span><span class="sxs-lookup"><span data-stu-id="c02bf-121">When you select a specific value in the drop-down list, the contents of the workspace are filtered based on that selection.</span></span> 

<span data-ttu-id="c02bf-122">[![Filtr pracovního prostoru](./media/workspace-filter.png)](./media/workspace-filter.png)</span><span class="sxs-lookup"><span data-stu-id="c02bf-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span></span> 

<span data-ttu-id="c02bf-123">Po kliknutí na tlačítko k otevření filtru se zobrazí několik možností.</span><span class="sxs-lookup"><span data-stu-id="c02bf-123">When you click to open the filter, you're presented with several options.</span></span> 

<span data-ttu-id="c02bf-124">[![Rozšířený filtr pracovního prostoru](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span><span class="sxs-lookup"><span data-stu-id="c02bf-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span></span> 

<span data-ttu-id="c02bf-125">Vyberte požadovanou možnost k filtrování pracovního prostoru na základě této možnosti.</span><span class="sxs-lookup"><span data-stu-id="c02bf-125">Select an option to filter the workspace based on that option.</span></span>

### <a name="workspace-section-filters"></a><span data-ttu-id="c02bf-126">Filtry části pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="c02bf-126">Workspace section filters</span></span>

<span data-ttu-id="c02bf-127">Pokud jednotlivé části pracovního prostoru mají filtry, můžete filtrovat každou část samostatně.</span><span class="sxs-lookup"><span data-stu-id="c02bf-127">If individual sections of the workspace have filters, you can filter each section separately.</span></span> <span data-ttu-id="c02bf-128">Na následujícím obrázku (pole obsahující text „Filtr“) je příklad filtru pole s volným textem.</span><span class="sxs-lookup"><span data-stu-id="c02bf-128">In the following illustration, the filter (the field that contains the text "Filter") is an example of a free-form text field filter.</span></span> 

<span data-ttu-id="c02bf-129">[![Konfigurace a filtrování pracovních prostorů](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span><span class="sxs-lookup"><span data-stu-id="c02bf-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span></span> 

<span data-ttu-id="c02bf-130">Stejně jako v případě filtru celého pracovního prostoru vyberte nebo zadejte do pole hodnotu k filtrování obsahu části.</span><span class="sxs-lookup"><span data-stu-id="c02bf-130">As with a workspace-wide filter, select or enter a value in the field to filter the contents of the section.</span></span>




