---
title: Vytvoření kusovníku pro základní produkt založený na dimenzích
description: V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffe30f1b5aae3e954b527e84648f4dbb4b181513
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986897"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="60286-103">Vytvoření kusovníku pro základní produkt založený na dimenzích</span><span class="sxs-lookup"><span data-stu-id="60286-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60286-104">V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů.</span><span class="sxs-lookup"><span data-stu-id="60286-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="60286-105">První 4 záznamy jsou věnovány nastavení data potřebného k dokončení tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="60286-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="60286-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="60286-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="60286-107">Tento úkol obvykle zpracovává návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="60286-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="60286-108">Výběr produktu</span><span class="sxs-lookup"><span data-stu-id="60286-108">Select the product</span></span>
1. <span data-ttu-id="60286-109">Klikněte na možnost Údržba uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="60286-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="60286-110">Klepněte na možnost Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="60286-110">Click Released products.</span></span>
3. <span data-ttu-id="60286-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="60286-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="60286-112">Vyhledejte uvolněný základní produkt s konfigurací založenou na dimenzích, kterou jste vytvořili v rámci příručky pro první úlohy v tomto pořadí.</span><span class="sxs-lookup"><span data-stu-id="60286-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="60286-113">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="60286-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="60286-114">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="60286-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="60286-115">Vytvoření nového kusovníku a verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="60286-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="60286-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="60286-116">Click New.</span></span>
2. <span data-ttu-id="60286-117">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="60286-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="60286-118">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="60286-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="60286-119">Nastavení pracoviště</span><span class="sxs-lookup"><span data-stu-id="60286-119">Setting a site</span></span>  
    * <span data-ttu-id="60286-120">V tomto postupu nebudeme nastavovat konkrétní pracoviště pro kusovník.</span><span class="sxs-lookup"><span data-stu-id="60286-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="60286-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="60286-121">Click OK.</span></span>
5. <span data-ttu-id="60286-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="60286-122">Click New.</span></span>
    * <span data-ttu-id="60286-123">V tomto postupu přidáme čtyři řádky do kusovníku.</span><span class="sxs-lookup"><span data-stu-id="60286-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="60286-124">Dva řádky představují možnosti pro kabel a dva řádky představují možnosti pro kabinet.</span><span class="sxs-lookup"><span data-stu-id="60286-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="60286-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="60286-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="60286-126">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-127">Vyberte číslo položky A0001, kabely HDMI 6'.</span><span class="sxs-lookup"><span data-stu-id="60286-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="60286-128">V poli Konfigurační skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-129">Vyberte skupinu konfigurace kabelu vytvořenou v příručce 4 v tomto pořadí.</span><span class="sxs-lookup"><span data-stu-id="60286-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="60286-130">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="60286-130">Click New.</span></span>
    * <span data-ttu-id="60286-131">Vyberte číslo položky A0002, kabely HDMI 12'.</span><span class="sxs-lookup"><span data-stu-id="60286-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="60286-132">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="60286-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="60286-133">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="60286-134">V poli Konfigurační skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-135">Vyberte znovu skupinu konfigurace kabelu.</span><span class="sxs-lookup"><span data-stu-id="60286-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="60286-136">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="60286-136">Click New.</span></span>
14. <span data-ttu-id="60286-137">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="60286-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="60286-138">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-139">Výběr číslo položky D0002 kabinet.</span><span class="sxs-lookup"><span data-stu-id="60286-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="60286-140">V poli Konfigurační skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-141">Vyberte skupinu konfigurace kabinetu pro tento řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="60286-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="60286-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="60286-142">Click New.</span></span>
18. <span data-ttu-id="60286-143">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="60286-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="60286-144">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-145">Vyberte číslo položky M0007 standardní kabinet jako poslední řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="60286-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="60286-146">V poli Konfigurační skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="60286-147">Vyberte skupinu konfigurace kabinetu pro poslední řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="60286-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="60286-148">Schválit a aktivovat</span><span class="sxs-lookup"><span data-stu-id="60286-148">Approve and activate</span></span>
1. <span data-ttu-id="60286-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="60286-149">Close the page.</span></span>
2. <span data-ttu-id="60286-150">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="60286-150">Click Approve.</span></span>
3. <span data-ttu-id="60286-151">V poli Schválil(a) zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="60286-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="60286-152">Vyberte Ano v poli Chcete kusovník také schválit? .</span><span class="sxs-lookup"><span data-stu-id="60286-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="60286-153">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="60286-153">Click OK.</span></span>
6. <span data-ttu-id="60286-154">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="60286-154">Click Activate.</span></span>

