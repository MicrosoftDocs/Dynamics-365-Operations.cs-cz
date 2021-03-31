---
title: Vytvoření subdodavatelské pracovní buňky pro lean manufacturing
description: K modelování práce subdodávky pro lean manufacturing je nutné vytvořit pracovní buňku přidruženou k dodavateli, který zajišťuje práci.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 236ce97fcf4ca76f07ae5f9308cf45240590b399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228532"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="bc149-103">Vytvoření subdodavatelské pracovní buňky pro lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="bc149-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc149-104">K modelování práce subdodávky pro lean manufacturing je nutné vytvořit pracovní buňku přidruženou k dodavateli, který zajišťuje práci.</span><span class="sxs-lookup"><span data-stu-id="bc149-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="bc149-105">Pracovní buňka subdodavatele je připojena k dodavateli prostřednictvím přidružení prostředků typu Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="bc149-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="bc149-106">Pokud použijete tento záznam v ukázkové společnosti USMF, můžete vybrat účet dodavatele ID 1002 a pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="bc149-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="bc149-107">Vytvoření prostředků dodavatele</span><span class="sxs-lookup"><span data-stu-id="bc149-107">Create a vendor resource</span></span>
1. <span data-ttu-id="bc149-108">Přejděte na Prostředky.</span><span class="sxs-lookup"><span data-stu-id="bc149-108">Go to Resources.</span></span>
2. <span data-ttu-id="bc149-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bc149-109">Click New.</span></span>
3. <span data-ttu-id="bc149-110">Zadejte hodnotu do pole Prostředek.</span><span class="sxs-lookup"><span data-stu-id="bc149-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="bc149-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="bc149-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bc149-112">V poli Typ vyberte možnost Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="bc149-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="bc149-113">V poli Dodavatel kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="bc149-114">Vytvoření skupiny prostředků</span><span class="sxs-lookup"><span data-stu-id="bc149-114">Create the resource group</span></span>
1. <span data-ttu-id="bc149-115">Přejděte do Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="bc149-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="bc149-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bc149-116">Click New.</span></span>
3. <span data-ttu-id="bc149-117">Zadejte hodnotu do pole Skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="bc149-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="bc149-118">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="bc149-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bc149-119">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bc149-120">Vyberte pracoviště, do kterého má být přidělena pracovní buňka.</span><span class="sxs-lookup"><span data-stu-id="bc149-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="bc149-121">Teoreticky pracoviště může představovat jedno pracoviště, které je ovládáno dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="bc149-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="bc149-122">Ale ve většině případů jsou prostředky subdodavatele pouze přidělovány k pracovišti, které si objednalo subdodavatelskou práci.</span><span class="sxs-lookup"><span data-stu-id="bc149-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="bc149-123">Všimněte si, že vstupní a výstupní sklady pracovních buněk subdodavatele musí být na stejném pracovišti.</span><span class="sxs-lookup"><span data-stu-id="bc149-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="bc149-124">Zadejte hodnotu do pole Pracoviště.</span><span class="sxs-lookup"><span data-stu-id="bc149-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="bc149-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="bc149-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="bc149-126">Zaškrtněte políčko Pracovní buňka nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="bc149-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="bc149-127">V poli Vstupní sklad klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bc149-128">Vyberte sklad a umístění, které se používají k fázování materiálu pro dodavatelem řízenou pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="bc149-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="bc149-129">V mnoha případech jsou sklad a umístění modelovány s použitím samostatného skladu pro dodavatele a jednoho místa na každou pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="bc149-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="bc149-130">V poli Vstupní umístění klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bc149-131">V poli Výstupní sklad klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bc149-132">Definujte sklad a umístění, kde se materiál zaúčtuje při zaúčtování subdodavatelských aktivit pracovní buňky.</span><span class="sxs-lookup"><span data-stu-id="bc149-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="bc149-133">Sklad a umístění mohou být v místě dodavatele, pokud dodavatel vykáže kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="bc149-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="bc149-134">Případně sklad a umístění mohou být skladovým místem příjmu, které je přidruženo k dalšímu kroku výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="bc149-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="bc149-135">V poli Výstupní umístění klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="bc149-136">Rozbalte nebo sbalte oddíl Kalendáře.</span><span class="sxs-lookup"><span data-stu-id="bc149-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="bc149-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bc149-137">Click Add.</span></span>
15. <span data-ttu-id="bc149-138">V poli Kalendář kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bc149-139">Přidružte kalendář pracovní doby pracovní buňky ke skupině prostředků.</span><span class="sxs-lookup"><span data-stu-id="bc149-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="bc149-140">Pro kritické zdroje doporučujeme definovat určité kalendáře, které představují přesné pracovní doby a související kapacity pracovní buňky nebo pracoviště dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bc149-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="bc149-141">Rozbalte nebo sbalte oddíl Prostředky.</span><span class="sxs-lookup"><span data-stu-id="bc149-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="bc149-142">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bc149-142">Click Add.</span></span>
    * <span data-ttu-id="bc149-143">Skupina prostředků subdodavatelské musí mít přidružené prostředky typu Dodavatel, které odkazují skupinu prostředků k účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="bc149-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="bc149-144">V poli Prostředky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bc149-145">Vyberte nebo zadejte zdroje dodavatele vytvořené v předchozím podúkolu.</span><span class="sxs-lookup"><span data-stu-id="bc149-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="bc149-146">Rozbalte nebo sbalte část Kapacita pracovní buňky.</span><span class="sxs-lookup"><span data-stu-id="bc149-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="bc149-147">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bc149-147">Click Add.</span></span>
    * <span data-ttu-id="bc149-148">Pracovní buňka musí mít určenou kapacitu.</span><span class="sxs-lookup"><span data-stu-id="bc149-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="bc149-149">V tomto příkladu vytvoříme kapacitu prostupnosti 100 kusů pro každý standardní pracovní den.</span><span class="sxs-lookup"><span data-stu-id="bc149-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="bc149-150">V poli Model výrobního toku klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="bc149-151">V poli Období kapacity vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="bc149-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="bc149-152">V poli Průměrné množství propustnosti zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bc149-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="bc149-153">V poli Jednotka klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc149-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="bc149-154">Vyřešit změny jednotky.</span><span class="sxs-lookup"><span data-stu-id="bc149-154">ResolveChanges the Unit.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]