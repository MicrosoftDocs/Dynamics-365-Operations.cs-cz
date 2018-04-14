--- 
title: "Vytvoření čísla produktu pro nakonfigurované varianty produktu"
description: "Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4f1ae1e447813ac6d6514314fedb03b2d40d75a2
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-product-number-for-configured-product-variants"></a><span data-ttu-id="05942-103">Vytvoření čísla produktu pro nakonfigurované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="05942-103">Create a product number for configured product variants</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05942-104">Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="05942-105">Tato procedura také ukazuje, jak lze vytvářet názvosloví konfigurace komponenty modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="05942-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="05942-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="05942-107">Základnímu produktu D0004 je přiřazeno nové názvosloví čísla produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="05942-108">Tento úkol obvykle provádí návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="05942-109">Vytvoření názvosloví čísla produktu</span><span class="sxs-lookup"><span data-stu-id="05942-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="05942-110">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="05942-111">Klikněte na Zobrazit názvosloví produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="05942-112">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="05942-112">Click New.</span></span>
4. <span data-ttu-id="05942-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="05942-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="05942-114">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="05942-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="05942-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-115">Click Add.</span></span>
7. <span data-ttu-id="05942-116">Klikněte na Číslo základního produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-116">Click Product master number.</span></span>
8. <span data-ttu-id="05942-117">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-117">Click Add.</span></span>
9. <span data-ttu-id="05942-118">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="05942-118">Click Text constant.</span></span>
10. <span data-ttu-id="05942-119">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="05942-120">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="05942-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="05942-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-121">Click Add.</span></span>
13. <span data-ttu-id="05942-122">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="05942-122">Click Configuration.</span></span>
14. <span data-ttu-id="05942-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="05942-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="05942-124">Přiřazení názvosloví čísla produktu základnímu produktu</span><span class="sxs-lookup"><span data-stu-id="05942-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="05942-125">Klikněte na Základní produkty.</span><span class="sxs-lookup"><span data-stu-id="05942-125">Click Product masters.</span></span>
2. <span data-ttu-id="05942-126">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="05942-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="05942-127">Můžete například filtrovat pole Číslo produktu pomocí hodnoty „D“.</span><span class="sxs-lookup"><span data-stu-id="05942-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="05942-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="05942-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="05942-129">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="05942-129">Click Edit.</span></span>
5. <span data-ttu-id="05942-130">Vyberte možnost Ano v poli Použít názvosloví.</span><span class="sxs-lookup"><span data-stu-id="05942-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="05942-131">V poli Názvosloví čísla varianty produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="05942-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="05942-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="05942-132">Close the page.</span></span>
8. <span data-ttu-id="05942-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="05942-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="05942-134">Vytvoření názvosloví pro komponentu modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="05942-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="05942-135">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="05942-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="05942-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="05942-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="05942-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="05942-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="05942-138">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="05942-138">Click Edit.</span></span>
5. <span data-ttu-id="05942-139">Vyberte možnost Ano v poli Použít konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="05942-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="05942-140">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-140">Click Add.</span></span>
7. <span data-ttu-id="05942-141">Klikněte na Hodnota atributu dávky.</span><span class="sxs-lookup"><span data-stu-id="05942-141">Click Attribute value.</span></span>
8. <span data-ttu-id="05942-142">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="05942-143">V poli Atribut zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="05942-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="05942-144">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-144">Click Add.</span></span>
11. <span data-ttu-id="05942-145">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="05942-145">Click Text constant.</span></span>
12. <span data-ttu-id="05942-146">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="05942-147">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="05942-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="05942-148">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-148">Click Add.</span></span>
15. <span data-ttu-id="05942-149">Klikněte na Hodnota atributu dávky.</span><span class="sxs-lookup"><span data-stu-id="05942-149">Click Attribute value.</span></span>
16. <span data-ttu-id="05942-150">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="05942-151">V poli Atribut zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="05942-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="05942-152">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-152">Click Add.</span></span>
19. <span data-ttu-id="05942-153">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="05942-153">Click Text constant.</span></span>
20. <span data-ttu-id="05942-154">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="05942-155">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="05942-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="05942-156">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-156">Click Add.</span></span>
23. <span data-ttu-id="05942-157">Klikněte na Hodnota atributu dávky.</span><span class="sxs-lookup"><span data-stu-id="05942-157">Click Attribute value.</span></span>
24. <span data-ttu-id="05942-158">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="05942-159">V poli Atribut zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="05942-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="05942-160">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-160">Click Add.</span></span>
27. <span data-ttu-id="05942-161">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="05942-161">Click Text constant.</span></span>
28. <span data-ttu-id="05942-162">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="05942-163">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="05942-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="05942-164">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-164">Click Add.</span></span>
31. <span data-ttu-id="05942-165">Klikněte na Hodnota atributu dávky.</span><span class="sxs-lookup"><span data-stu-id="05942-165">Click Attribute value.</span></span>
32. <span data-ttu-id="05942-166">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="05942-167">V poli Atribut zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="05942-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="05942-168">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-168">Click Add.</span></span>
35. <span data-ttu-id="05942-169">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="05942-169">Click Text constant.</span></span>
36. <span data-ttu-id="05942-170">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="05942-171">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="05942-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="05942-172">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="05942-172">Click Add.</span></span>
39. <span data-ttu-id="05942-173">Klikněte na Hodnota číselné řady.</span><span class="sxs-lookup"><span data-stu-id="05942-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="05942-174">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="05942-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="05942-175">V poli Číselná řada zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="05942-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="05942-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="05942-176">Close the page.</span></span>
43. <span data-ttu-id="05942-177">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="05942-177">Close the page.</span></span>
44. <span data-ttu-id="05942-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="05942-178">Close the page.</span></span>


