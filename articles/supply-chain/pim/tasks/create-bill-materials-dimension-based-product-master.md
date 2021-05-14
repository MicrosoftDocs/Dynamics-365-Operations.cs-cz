---
title: Vytvoření kusovníku pro základní produkt založený na dimenzích
description: V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920698"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="04e64-103">Vytvoření kusovníku pro základní produkt založený na dimenzích</span><span class="sxs-lookup"><span data-stu-id="04e64-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04e64-104">V tomto postupu je vhodné mít dokončené 4 předchozí průvodce v tomto pořadí z osmi záznamů.</span><span class="sxs-lookup"><span data-stu-id="04e64-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="04e64-105">První 4 záznamy jsou věnovány nastavení data potřebného k dokončení tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="04e64-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="04e64-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="04e64-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="04e64-107">Tento úkol obvykle zpracovává návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="04e64-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="04e64-108">Výběr produktu</span><span class="sxs-lookup"><span data-stu-id="04e64-108">Select the product</span></span>

1. <span data-ttu-id="04e64-109">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="04e64-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="04e64-110">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="04e64-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="04e64-111">Vyhledejte uvolněný základní produkt s konfigurací založenou na dimenzích, kterou jste vytvořili v rámci příručky pro první úlohy v tomto pořadí.</span><span class="sxs-lookup"><span data-stu-id="04e64-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="04e64-112">V podokně akcí zvolte **Technik**.</span><span class="sxs-lookup"><span data-stu-id="04e64-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="04e64-113">Vyberte **Verze kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="04e64-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="04e64-114">Vytvoření nového kusovníku a verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="04e64-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="04e64-115">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04e64-115">Select **New**.</span></span>
1. <span data-ttu-id="04e64-116">Vyberte **Kusovník a verze kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="04e64-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="04e64-117">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="04e64-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="04e64-118">Nastavení pracoviště</span><span class="sxs-lookup"><span data-stu-id="04e64-118">Setting a site</span></span>  
    * <span data-ttu-id="04e64-119">V tomto postupu nebudeme nastavovat konkrétní pracoviště pro kusovník.</span><span class="sxs-lookup"><span data-stu-id="04e64-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="04e64-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e64-120">Select **OK**.</span></span>
1. <span data-ttu-id="04e64-121">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04e64-121">Select **New**.</span></span>
    * <span data-ttu-id="04e64-122">V tomto postupu přidáme čtyři řádky do kusovníku.</span><span class="sxs-lookup"><span data-stu-id="04e64-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="04e64-123">Dva řádky představují možnosti pro kabel a dva řádky představují možnosti pro kabinet.</span><span class="sxs-lookup"><span data-stu-id="04e64-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="04e64-124">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="04e64-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="04e64-125">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-126">Vyberte číslo položky A0001, kabely HDMI 6'.</span><span class="sxs-lookup"><span data-stu-id="04e64-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="04e64-127">V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-128">Vyberte skupinu konfigurace kabelu vytvořenou v příručce 4 v tomto pořadí.</span><span class="sxs-lookup"><span data-stu-id="04e64-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="04e64-129">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04e64-129">Select **New**.</span></span>
    * <span data-ttu-id="04e64-130">Vyberte číslo položky A0002, kabely HDMI 12'.</span><span class="sxs-lookup"><span data-stu-id="04e64-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="04e64-131">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="04e64-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="04e64-132">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="04e64-133">V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-134">Vyberte znovu skupinu konfigurace kabelu.</span><span class="sxs-lookup"><span data-stu-id="04e64-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="04e64-135">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04e64-135">Select **New**.</span></span>
1. <span data-ttu-id="04e64-136">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="04e64-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="04e64-137">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-138">Výběr číslo položky D0002 kabinet.</span><span class="sxs-lookup"><span data-stu-id="04e64-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="04e64-139">V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-140">Vyberte skupinu konfigurace kabinetu pro tento řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="04e64-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="04e64-141">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04e64-141">Select **New**.</span></span>
1. <span data-ttu-id="04e64-142">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="04e64-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="04e64-143">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-144">Vyberte číslo položky M0007 standardní kabinet jako poslední řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="04e64-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="04e64-145">V poli **Konfigurační skupina** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="04e64-146">Vyberte skupinu konfigurace kabinetu pro poslední řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="04e64-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="04e64-147">Schválit a aktivovat</span><span class="sxs-lookup"><span data-stu-id="04e64-147">Approve and activate</span></span>

1. <span data-ttu-id="04e64-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="04e64-148">Close the page.</span></span>
1. <span data-ttu-id="04e64-149">Vyberte **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="04e64-149">Select **Approve**.</span></span>
1. <span data-ttu-id="04e64-150">V poli **Schválil(a)** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04e64-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="04e64-151">Vyberte *Ano* v poli **Chcete kusovník také schválit?**.</span><span class="sxs-lookup"><span data-stu-id="04e64-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="04e64-152">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e64-152">Select **OK**.</span></span>
1. <span data-ttu-id="04e64-153">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="04e64-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]