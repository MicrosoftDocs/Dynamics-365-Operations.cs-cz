--- 
title: "Generování a spuštění předpřipravených sestav"
description: "Použijte tohoto průvodce úkolem ke spuštění předem připravených sestav v centrále z jiných pracovních prostorů a dotazy a prodejní sestavy, které jsou umístěny pod Maloobchodní a velkoobchodní prodej."
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="5f281-103">Generování a spuštění předpřipravených sestav</span><span class="sxs-lookup"><span data-stu-id="5f281-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5f281-104">Použijte tohoto průvodce úkolem ke spuštění předem připravených sestav v centrále z jiných pracovních prostorů a dotazy a prodejní sestavy, které jsou umístěny pod Maloobchodní a velkoobchodní prodej.</span><span class="sxs-lookup"><span data-stu-id="5f281-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="5f281-105">K vytvoření tohoto záznamu jsou použita ukázková data společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="5f281-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="5f281-106">Tento záznam je určen pro roli Správce systému.</span><span class="sxs-lookup"><span data-stu-id="5f281-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="5f281-107">Spuštění sestav z pracovních ploch</span><span class="sxs-lookup"><span data-stu-id="5f281-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="5f281-108">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Produkty a kategorie > Správa kategorií a produktů.</span><span class="sxs-lookup"><span data-stu-id="5f281-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="5f281-109">Kliknutím na šipku rozbalte nebo sbalte oddíl Sestavy.</span><span class="sxs-lookup"><span data-stu-id="5f281-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="5f281-110">Klikněte na Sestava nejlepších produktů.</span><span class="sxs-lookup"><span data-stu-id="5f281-110">Click Top products report.</span></span>
4. <span data-ttu-id="5f281-111">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="5f281-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="5f281-112">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5f281-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="5f281-113">V poli Kanál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f281-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5f281-114">Ve stromovém zobrazení vyberte „Contoso Retail\Contoso Retail USA\Central\Houston“.</span><span class="sxs-lookup"><span data-stu-id="5f281-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="5f281-115">Tím se zobrazí výchozí hierarchie organizace maloobchodu pro účely vykazování maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5f281-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="5f281-116">Přejděte do nabídky Správa organizace > Organizace > Účely organizační hierarchie, vyberte Vykazování maloobchodu a ověřte v poli Přiřazené hierarchie název hierarchie, u které je zaškrtnut Výchozí sloupec.</span><span class="sxs-lookup"><span data-stu-id="5f281-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="5f281-117">Jako součást ukázkových dat (použitých k záznamu tohoto úkolu) si můžete všimnout, že možnost Maloobchody podle regionu je výchozí organizační hierarchie pro účely maloobchodního vykazování.</span><span class="sxs-lookup"><span data-stu-id="5f281-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="5f281-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f281-118">Click OK.</span></span>
9. <span data-ttu-id="5f281-119">Vyberte volbu v poli Zobrazení.</span><span class="sxs-lookup"><span data-stu-id="5f281-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="5f281-120">Vyberte volbu v poli Podle.</span><span class="sxs-lookup"><span data-stu-id="5f281-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="5f281-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f281-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="5f281-122">Sestavy spuštění z dotazů a sestav prodejů jsou umístěny v odkazu aplikace Maloobchodní a velkoobchodní prodej.</span><span class="sxs-lookup"><span data-stu-id="5f281-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="5f281-123">Přejděte na Maloobchodní a velkoobchodní prodej > Dotazy a sestavy > Prodejní sestavy > Prodejní sestava kategorií.</span><span class="sxs-lookup"><span data-stu-id="5f281-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="5f281-124">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="5f281-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="5f281-125">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5f281-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="5f281-126">V poli Kanál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f281-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5f281-127">Ve stromovém zobrazení vyberte „Contoso Retail\Contoso Retail USA\West\Seattle“.</span><span class="sxs-lookup"><span data-stu-id="5f281-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="5f281-128">Tím se zobrazí výchozí hierarchie organizace maloobchodu pro účely vykazování maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5f281-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="5f281-129">Přejděte do nabídky Správa organizace > Organizace > Účely organizační hierarchie, vyberte Vykazování maloobchodu a ověřte v poli Přiřazené hierarchie název hierarchie, u které je zaškrtnut Výchozí sloupec.</span><span class="sxs-lookup"><span data-stu-id="5f281-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="5f281-130">Jako součást ukázkových dat (použitých k záznamu tohoto úkolu) si můžete všimnout, že možnost Maloobchody podle regionu je výchozí organizační hierarchie pro účely maloobchodního vykazování.</span><span class="sxs-lookup"><span data-stu-id="5f281-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="5f281-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f281-131">Click OK.</span></span>
7. <span data-ttu-id="5f281-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f281-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="5f281-133">Exportujte sestavy HQ</span><span class="sxs-lookup"><span data-stu-id="5f281-133">Export an HQ reports</span></span>
1. <span data-ttu-id="5f281-134">Přejděte na Maloobchodní a velkoobchodní prodej > Dotazy a sestavy > Prodejní sestavy > Sestava prodejů organizace.</span><span class="sxs-lookup"><span data-stu-id="5f281-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="5f281-135">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="5f281-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="5f281-136">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5f281-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="5f281-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f281-137">Click OK.</span></span>
5. <span data-ttu-id="5f281-138">Klikněte na Exportovat.</span><span class="sxs-lookup"><span data-stu-id="5f281-138">Click Export.</span></span>
6. <span data-ttu-id="5f281-139">Klikněte na PDF.</span><span class="sxs-lookup"><span data-stu-id="5f281-139">Click PDF.</span></span>


