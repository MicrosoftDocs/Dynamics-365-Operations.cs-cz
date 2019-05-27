---
title: Vytvoření zásad chování nákladů a jejich přiřazení jednotce řízení nákladů
description: Chování nákladů je klasifikace nákladů jako fixních nebo variabilních.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7b39b7649aaef0d354b61e3d70b6cac887282ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543880"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="94f70-103">Vytvoření zásad chování nákladů a jejich přiřazení jednotce řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="94f70-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94f70-104">Chování nákladů je klasifikace nákladů jako fixních nebo variabilních.</span><span class="sxs-lookup"><span data-stu-id="94f70-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="94f70-105">Zásady a odpovídající pravila musí být přiděleny jednotce řízení nákladů, aby mohly zásady vstoupit v platnost.</span><span class="sxs-lookup"><span data-stu-id="94f70-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="94f70-106">Tento postup slouží k vytváření zásady a její přidělení k jednotce pro řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="94f70-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="94f70-107">Vytvoření hierarchie chování nákladů</span><span class="sxs-lookup"><span data-stu-id="94f70-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="94f70-108">Přejděte na Nákladové účetnictví > Dimenze > Hierarchie dimenzí.</span><span class="sxs-lookup"><span data-stu-id="94f70-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="94f70-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-109">Click New.</span></span>
3. <span data-ttu-id="94f70-110">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="94f70-110">Click Create.</span></span>
4. <span data-ttu-id="94f70-111">V poli Název hierarchie dimenzí zadejte Hierarchie chování nákladů.</span><span class="sxs-lookup"><span data-stu-id="94f70-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="94f70-112">V poli Dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-113">Vyberte Prvky nákladů.</span><span class="sxs-lookup"><span data-stu-id="94f70-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="94f70-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="94f70-114">Click Save.</span></span>
7. <span data-ttu-id="94f70-115">Klikněte na Zobrazit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="94f70-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="94f70-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-116">Click New.</span></span>
9. <span data-ttu-id="94f70-117">Do pole Název uzlu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="94f70-118">Zadejte Pevné náklady.</span><span class="sxs-lookup"><span data-stu-id="94f70-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="94f70-119">Ve stromové struktuře vyberte Hierarchie chování nákladů.</span><span class="sxs-lookup"><span data-stu-id="94f70-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="94f70-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-120">Click New.</span></span>
12. <span data-ttu-id="94f70-121">Do pole Název uzlu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="94f70-122">Zadejte variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="94f70-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="94f70-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="94f70-123">Click Save.</span></span>
14. <span data-ttu-id="94f70-124">Ve stromové struktuře vyberte Hierarchie chování nákladů\Pevné náklady.</span><span class="sxs-lookup"><span data-stu-id="94f70-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="94f70-125">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-125">Click New.</span></span>
16. <span data-ttu-id="94f70-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="94f70-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="94f70-127">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-128">Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.</span><span class="sxs-lookup"><span data-stu-id="94f70-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="94f70-129">V poli Po člen dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-130">Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.</span><span class="sxs-lookup"><span data-stu-id="94f70-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="94f70-131">Ve stromové struktuře vyberte Hierarchie chování nákladů\Variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="94f70-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="94f70-132">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-132">Click New.</span></span>
21. <span data-ttu-id="94f70-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="94f70-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="94f70-134">V poli Od členu dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-135">Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.</span><span class="sxs-lookup"><span data-stu-id="94f70-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="94f70-136">V poli Po člen dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-137">Rozsah členů dimenze může obsahovat mezery, ale členové se nesmí překrývat.</span><span class="sxs-lookup"><span data-stu-id="94f70-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="94f70-138">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="94f70-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="94f70-139">Vytvoření zásad a pravidel</span><span class="sxs-lookup"><span data-stu-id="94f70-139">Create the policy and rules</span></span>
1. <span data-ttu-id="94f70-140">Přejděte na Nákladové účetnictví > Zásady > Zásady chování nákladů.</span><span class="sxs-lookup"><span data-stu-id="94f70-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="94f70-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-141">Click New.</span></span>
3. <span data-ttu-id="94f70-142">Do pole Název zásady zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="94f70-143">V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-144">Vyberte hierarchii zásady, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="94f70-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="94f70-145">V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-146">Vyberte organizaci.</span><span class="sxs-lookup"><span data-stu-id="94f70-146">Select Organization.</span></span>  
6. <span data-ttu-id="94f70-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="94f70-147">Click Save.</span></span>
7. <span data-ttu-id="94f70-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-148">Click New.</span></span>
8. <span data-ttu-id="94f70-149">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="94f70-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="94f70-150">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-151">Rozbalte hierarchii a vyberte Variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="94f70-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="94f70-152">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="94f70-153">Výchozí procentuální hodnota proměnné je 100 procent.</span><span class="sxs-lookup"><span data-stu-id="94f70-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="94f70-154">Klikněte na Přiřazení zásady pro kontrolní jednotky nákladů.</span><span class="sxs-lookup"><span data-stu-id="94f70-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="94f70-155">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="94f70-155">Click New.</span></span>
13. <span data-ttu-id="94f70-156">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="94f70-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="94f70-157">Zadejte datum do pole Platné od data účtování.</span><span class="sxs-lookup"><span data-stu-id="94f70-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="94f70-158">Pravidla jsou platná od data a platnost pravidla může ukončit uživatel nebo systém v případě vytvoření novější verze.</span><span class="sxs-lookup"><span data-stu-id="94f70-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="94f70-159">V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="94f70-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="94f70-160">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="94f70-160">Click Save.</span></span>

