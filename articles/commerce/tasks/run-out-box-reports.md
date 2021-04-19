---
title: Generování a spuštění předpřipravených sestav
description: Použijte tohoto průvodce úkolem ke spuštění předem připravených sestav v centrále z jiných pracovních prostorů a dotazy a prodejní sestavy, které jsou umístěny pod Velkoobchodní prodej.
author: ashishmsft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db75b09f1ae1f83a88a5e5eaef0c8c1b8eab5901
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804130"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="9b71e-103">Generování a spuštění předpřipravených sestav</span><span class="sxs-lookup"><span data-stu-id="9b71e-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b71e-104">Použijte tohoto průvodce úkolem ke spuštění předem připravených sestav v centrále z jiných pracovních prostorů a dotazy a prodejní sestavy, které jsou umístěny pod Velkoobchodní prodej.</span><span class="sxs-lookup"><span data-stu-id="9b71e-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="9b71e-105">K vytvoření tohoto záznamu jsou použita ukázková data společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="9b71e-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="9b71e-106">Tento záznam je určen pro roli Správce systému.</span><span class="sxs-lookup"><span data-stu-id="9b71e-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="9b71e-107">Spuštění sestav z pracovních ploch</span><span class="sxs-lookup"><span data-stu-id="9b71e-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="9b71e-108">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Produkty a kategorie > Správa kategorií a produktů.</span><span class="sxs-lookup"><span data-stu-id="9b71e-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="9b71e-109">Kliknutím na šipku rozbalte nebo sbalte oddíl Sestavy.</span><span class="sxs-lookup"><span data-stu-id="9b71e-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="9b71e-110">Klikněte na Sestava nejlepších produktů.</span><span class="sxs-lookup"><span data-stu-id="9b71e-110">Click Top products report.</span></span>
4. <span data-ttu-id="9b71e-111">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="9b71e-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="9b71e-112">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9b71e-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="9b71e-113">V poli Kanál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9b71e-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9b71e-114">Ve stromovém zobrazení vyberte „Contoso Retail\Contoso Retail USA\Central\Houston“.</span><span class="sxs-lookup"><span data-stu-id="9b71e-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="9b71e-115">Tím se zobrazí výchozí hierarchie organizace maloobchodu pro účely vykazování velkoobchodu.</span><span class="sxs-lookup"><span data-stu-id="9b71e-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="9b71e-116">Přejděte do nabídky Správa organizace > Organizace > Účely organizační hierarchie, vyberte Vykazování velkoobchodu a ověřte v poli Přiřazené hierarchie název hierarchie, u které je zaškrtnut Výchozí sloupec.</span><span class="sxs-lookup"><span data-stu-id="9b71e-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="9b71e-117">Jako součást ukázkových dat (použitých k záznamu tohoto úkolu) si můžete všimnout, že možnost Obchody podle regionu je výchozí organizační hierarchie pro účely obchodního vykazování.</span><span class="sxs-lookup"><span data-stu-id="9b71e-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="9b71e-118">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9b71e-118">Click OK.</span></span>
9. <span data-ttu-id="9b71e-119">Vyberte volbu v poli Zobrazení.</span><span class="sxs-lookup"><span data-stu-id="9b71e-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="9b71e-120">Vyberte volbu v poli Podle.</span><span class="sxs-lookup"><span data-stu-id="9b71e-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="9b71e-121">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9b71e-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="9b71e-122">Spouštění sestav z dotazů a prodejních sestav</span><span class="sxs-lookup"><span data-stu-id="9b71e-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="9b71e-123">Přejděte na Maloobchodní a velkoobchodní prodej > Dotazy a sestavy > Prodejní sestavy > Prodejní sestava kategorií.</span><span class="sxs-lookup"><span data-stu-id="9b71e-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="9b71e-124">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="9b71e-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="9b71e-125">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9b71e-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="9b71e-126">V poli Kanál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9b71e-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9b71e-127">Ve stromovém zobrazení vyberte „Contoso Retail\Contoso Retail USA\West\Seattle“.</span><span class="sxs-lookup"><span data-stu-id="9b71e-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="9b71e-128">Tím se zobrazí výchozí hierarchie organizace maloobchodu pro účely vykazování velkoobchodu.</span><span class="sxs-lookup"><span data-stu-id="9b71e-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="9b71e-129">Přejděte do nabídky Správa organizace > Organizace > Účely organizační hierarchie, vyberte Vykazování velkoobchodu a ověřte v poli Přiřazené hierarchie název hierarchie, u které je zaškrtnut Výchozí sloupec.</span><span class="sxs-lookup"><span data-stu-id="9b71e-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="9b71e-130">Jako součást ukázkových dat (použitých k záznamu tohoto úkolu) si můžete všimnout, že možnost Obchody podle regionu je výchozí organizační hierarchie pro účely obchodního vykazování.</span><span class="sxs-lookup"><span data-stu-id="9b71e-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="9b71e-131">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9b71e-131">Click OK.</span></span>
7. <span data-ttu-id="9b71e-132">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9b71e-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="9b71e-133">Exportujte sestavy HQ</span><span class="sxs-lookup"><span data-stu-id="9b71e-133">Export an HQ reports</span></span>
1. <span data-ttu-id="9b71e-134">Přejděte na Maloobchodní a velkoobchodní prodej > Dotazy a sestavy > Prodejní sestavy > Sestava prodejů organizace.</span><span class="sxs-lookup"><span data-stu-id="9b71e-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="9b71e-135">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="9b71e-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="9b71e-136">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9b71e-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="9b71e-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9b71e-137">Click OK.</span></span>
5. <span data-ttu-id="9b71e-138">Klikněte na Exportovat.</span><span class="sxs-lookup"><span data-stu-id="9b71e-138">Click Export.</span></span>
6. <span data-ttu-id="9b71e-139">Klikněte na PDF.</span><span class="sxs-lookup"><span data-stu-id="9b71e-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]