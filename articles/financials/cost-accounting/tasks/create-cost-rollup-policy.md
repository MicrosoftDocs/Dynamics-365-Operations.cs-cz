--- 
title: "Vytvoření zásad shrnutí nákladů"
description: "Tento postup popisuje způsob vytvoření zásad shrnutí nákladů a vytváření pravidel zásad."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="22b0b-103">Vytvoření zásad shrnutí nákladů</span><span class="sxs-lookup"><span data-stu-id="22b0b-103">Create a cost rollup policy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22b0b-104">Tento postup popisuje způsob vytvoření zásad shrnutí nákladů a vytváření pravidel zásad.</span><span class="sxs-lookup"><span data-stu-id="22b0b-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="22b0b-105">Jako ukázková data pro tento postup slouží data USP2.</span><span class="sxs-lookup"><span data-stu-id="22b0b-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="22b0b-106">Vytvořte zásadu</span><span class="sxs-lookup"><span data-stu-id="22b0b-106">Create a policy</span></span>
1. <span data-ttu-id="22b0b-107">Přejděte na Nákladové účetnictví > Zásady > Zásady shrnutí nákladů.</span><span class="sxs-lookup"><span data-stu-id="22b0b-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="22b0b-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="22b0b-108">Click New.</span></span>
3. <span data-ttu-id="22b0b-109">Do pole Název zásady zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="22b0b-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="22b0b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22b0b-111">V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-112">Vyberte Shrnutí nákladů CC.</span><span class="sxs-lookup"><span data-stu-id="22b0b-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="22b0b-113">V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-114">Vyberte Shrnutí nákladů CC.</span><span class="sxs-lookup"><span data-stu-id="22b0b-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="22b0b-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="22b0b-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="22b0b-116">Vytvoření pravidla pro zásady shrnutí nákladů</span><span class="sxs-lookup"><span data-stu-id="22b0b-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="22b0b-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="22b0b-117">Click New.</span></span>
2. <span data-ttu-id="22b0b-118">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="22b0b-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="22b0b-119">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-120">Vyberte 007.</span><span class="sxs-lookup"><span data-stu-id="22b0b-120">Select 007.</span></span>  
4. <span data-ttu-id="22b0b-121">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-122">Vyberte Shrnutí nákladů CE.</span><span class="sxs-lookup"><span data-stu-id="22b0b-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="22b0b-123">V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-124">V tomto příkladu namapujte sekundární nákladový prvek CC-007 na nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="22b0b-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="22b0b-125">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="22b0b-125">Click New.</span></span>
7. <span data-ttu-id="22b0b-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="22b0b-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="22b0b-127">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-128">Vyberte 008.</span><span class="sxs-lookup"><span data-stu-id="22b0b-128">Select 008.</span></span>  
9. <span data-ttu-id="22b0b-129">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-130">Vyberte Shrnutí nákladů CE.</span><span class="sxs-lookup"><span data-stu-id="22b0b-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="22b0b-131">V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-132">V tomto příkladu namapujte sekundární nákladový prvek CC-008 na nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="22b0b-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="22b0b-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="22b0b-133">Click New.</span></span>
12. <span data-ttu-id="22b0b-134">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="22b0b-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="22b0b-135">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-136">Vyberte 009.</span><span class="sxs-lookup"><span data-stu-id="22b0b-136">Select 009.</span></span>  
14. <span data-ttu-id="22b0b-137">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-138">Vyberte Shrnutí nákladů CE.</span><span class="sxs-lookup"><span data-stu-id="22b0b-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="22b0b-139">V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22b0b-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="22b0b-140">V tomto příkladu namapujte sekundární nákladový prvek CC-009 na nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="22b0b-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="22b0b-141">Pokračujte, dokud všechna nákladová střediska nejsou namapována na odpovídajících sekundární prvky nákladů.</span><span class="sxs-lookup"><span data-stu-id="22b0b-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="22b0b-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="22b0b-142">Click Save.</span></span>


