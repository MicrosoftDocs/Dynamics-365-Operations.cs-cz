---
title: Vytvoření zásad shrnutí nákladů
description: Tento postup popisuje způsob vytvoření zásad shrnutí nákladů a vytváření pravidel zásad.
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
ms.openlocfilehash: 5f1fa434061832bd306cef13afc46c7f3adab0c0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "362595"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="8c822-103">Vytvoření zásad shrnutí nákladů</span><span class="sxs-lookup"><span data-stu-id="8c822-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c822-104">Tento postup popisuje způsob vytvoření zásad shrnutí nákladů a vytváření pravidel zásad.</span><span class="sxs-lookup"><span data-stu-id="8c822-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="8c822-105">Jako ukázková data pro tento postup slouží data USP2.</span><span class="sxs-lookup"><span data-stu-id="8c822-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8c822-106">Vytvořte zásadu</span><span class="sxs-lookup"><span data-stu-id="8c822-106">Create a policy</span></span>
1. <span data-ttu-id="8c822-107">Přejděte na Nákladové účetnictví > Zásady > Zásady shrnutí nákladů.</span><span class="sxs-lookup"><span data-stu-id="8c822-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="8c822-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8c822-108">Click New.</span></span>
3. <span data-ttu-id="8c822-109">Do pole Název zásady zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8c822-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="8c822-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8c822-111">V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-112">Vyberte Shrnutí nákladů CC.</span><span class="sxs-lookup"><span data-stu-id="8c822-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="8c822-113">V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-114">Vyberte Shrnutí nákladů CC.</span><span class="sxs-lookup"><span data-stu-id="8c822-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="8c822-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8c822-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="8c822-116">Vytvoření pravidla pro zásady shrnutí nákladů</span><span class="sxs-lookup"><span data-stu-id="8c822-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="8c822-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8c822-117">Click New.</span></span>
2. <span data-ttu-id="8c822-118">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8c822-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8c822-119">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-120">Vyberte 007.</span><span class="sxs-lookup"><span data-stu-id="8c822-120">Select 007.</span></span>  
4. <span data-ttu-id="8c822-121">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-122">Vyberte Shrnutí nákladů CE.</span><span class="sxs-lookup"><span data-stu-id="8c822-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="8c822-123">V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-124">V tomto příkladu namapujte sekundární nákladový prvek CC-007 na nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="8c822-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="8c822-125">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8c822-125">Click New.</span></span>
7. <span data-ttu-id="8c822-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8c822-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8c822-127">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-128">Vyberte 008.</span><span class="sxs-lookup"><span data-stu-id="8c822-128">Select 008.</span></span>  
9. <span data-ttu-id="8c822-129">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-130">Vyberte Shrnutí nákladů CE.</span><span class="sxs-lookup"><span data-stu-id="8c822-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="8c822-131">V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-132">V tomto příkladu namapujte sekundární nákladový prvek CC-008 na nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="8c822-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="8c822-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8c822-133">Click New.</span></span>
12. <span data-ttu-id="8c822-134">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8c822-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8c822-135">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-136">Vyberte 009.</span><span class="sxs-lookup"><span data-stu-id="8c822-136">Select 009.</span></span>  
14. <span data-ttu-id="8c822-137">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-138">Vyberte Shrnutí nákladů CE.</span><span class="sxs-lookup"><span data-stu-id="8c822-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="8c822-139">V poli Prvek druhotných nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c822-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8c822-140">V tomto příkladu namapujte sekundární nákladový prvek CC-009 na nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="8c822-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="8c822-141">Pokračujte, dokud všechna nákladová střediska nejsou namapována na odpovídajících sekundární prvky nákladů.</span><span class="sxs-lookup"><span data-stu-id="8c822-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="8c822-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8c822-142">Click Save.</span></span>

