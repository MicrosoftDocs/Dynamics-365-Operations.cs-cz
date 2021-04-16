---
title: Vytvoření zásad přidělování nákladů a jejich přiřazení jednotce řízení nákladů
description: Tento postup slouží k vytváření a přiřazení zásady přidělení nákladů a odpovídajících pravidel k jednotce pro řízení nákladů.
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cff10132e8007be885e9c69d97cf96c30d69f50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822848"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="1f3b8-103">Vytvoření zásad přidělování nákladů a jejich přiřazení jednotce řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="1f3b8-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f3b8-104">Tento postup slouží k vytváření a přiřazení zásady přidělení nákladů a odpovídajících pravidel k jednotce pro řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="1f3b8-105">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="1f3b8-106">Vytvořte zásadu</span><span class="sxs-lookup"><span data-stu-id="1f3b8-106">Create a policy</span></span>
1. <span data-ttu-id="1f3b8-107">Přejděte na Nákladové účetnictví > Zásady > Zásady přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="1f3b8-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-108">Click New.</span></span>
3. <span data-ttu-id="1f3b8-109">Do pole Název zásady zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="1f3b8-110">V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="1f3b8-111">Vyberte organizaci.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-111">Select Organization.</span></span>  
5. <span data-ttu-id="1f3b8-112">V poli Statistická dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="1f3b8-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="1f3b8-114">Vytvoření pravidel přidělení</span><span class="sxs-lookup"><span data-stu-id="1f3b8-114">Create allocation rules</span></span>
1. <span data-ttu-id="1f3b8-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-115">Click New.</span></span>
2. <span data-ttu-id="1f3b8-116">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="1f3b8-117">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="1f3b8-118">V poli Chování nákladů vyberte Celkem.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="1f3b8-119">V poli Základ přidělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="1f3b8-120">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-120">Click New.</span></span>
7. <span data-ttu-id="1f3b8-121">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1f3b8-122">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="1f3b8-123">V poli Chování nákladů vyberte Celkem.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="1f3b8-124">V poli Základ přidělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="1f3b8-125">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-125">Click New.</span></span>
12. <span data-ttu-id="1f3b8-126">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1f3b8-127">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="1f3b8-128">V poli Chování nákladů vyberte Celkem.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="1f3b8-129">V poli Základ přidělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="1f3b8-130">Pokračujte dokud nevytvoříte všechna pravidla.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="1f3b8-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="1f3b8-132">Přiřazení zásady ke kontrolní jednotce nákladů</span><span class="sxs-lookup"><span data-stu-id="1f3b8-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="1f3b8-133">Klikněte na Přiřazení zásady pro kontrolní jednotky nákladů.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="1f3b8-134">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-134">Click New.</span></span>
3. <span data-ttu-id="1f3b8-135">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1f3b8-136">Zadejte datum do pole Platné od data účtování.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="1f3b8-137">Pravidla mají časovou platnost.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-137">The rules are date-effective.</span></span> <span data-ttu-id="1f3b8-138">Uživatel nebo systém můžete platnost pravidel ukončit při vytvoření novější verze.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="1f3b8-139">V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="1f3b8-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1f3b8-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]