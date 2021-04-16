---
title: Vytvoření zásad distribuce nákladů a jejich přiřazení jednotce řízení nákladů
description: Pravidla pro rozdělení nákladů se používají k rozdělení nákladů, které byly finančně vypočítány z hromadného nákladového střediska.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 736b537958f65fb54d0829cfbcc819fd315b530c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810119"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="cec66-103">Vytvoření zásad distribuce nákladů a jejich přiřazení jednotce řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="cec66-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cec66-104">Pravidla pro rozdělení nákladů se používají k rozdělení nákladů, které byly finančně vypočítány z hromadného nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="cec66-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="cec66-105">Nákladový účetní zajišťuje, že jsou náklady distribuovány do nákladových středisek na základě vybraného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="cec66-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="cec66-106">Kontrolní jednotce nákladů jsou přiřazeny zásada a odpovídajících pravidla.</span><span class="sxs-lookup"><span data-stu-id="cec66-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="cec66-107">Tento průvodce záznamem úloh slouží jako příklad toho, jak vytvořit zásadu distribuce nákladů a odpovídajících pravidel.</span><span class="sxs-lookup"><span data-stu-id="cec66-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="cec66-108">Vytvořte zásadu</span><span class="sxs-lookup"><span data-stu-id="cec66-108">Create a policy</span></span>
1. <span data-ttu-id="cec66-109">Přejděte na Nákladové účetnictví > Zásady > Zásady distribuce nákladů.</span><span class="sxs-lookup"><span data-stu-id="cec66-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="cec66-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cec66-110">Click New.</span></span>
3. <span data-ttu-id="cec66-111">Do pole Název zásady zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="cec66-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cec66-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cec66-113">V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-114">Vyberte organizaci.</span><span class="sxs-lookup"><span data-stu-id="cec66-114">Select Organization.</span></span>  
6. <span data-ttu-id="cec66-115">V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-116">Vyberte CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="cec66-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="cec66-117">V poli Statistická dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-118">Vyberte Statistické prvky.</span><span class="sxs-lookup"><span data-stu-id="cec66-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="cec66-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cec66-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="cec66-120">Vytvoření pravidel zásady</span><span class="sxs-lookup"><span data-stu-id="cec66-120">Create rules for the policy</span></span>
1. <span data-ttu-id="cec66-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cec66-121">Click New.</span></span>
2. <span data-ttu-id="cec66-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cec66-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="cec66-123">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-124">Rozbalte hierarchii a vyberte 094.</span><span class="sxs-lookup"><span data-stu-id="cec66-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="cec66-125">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-126">Vyberte Další provozní výdaje a poté vyberte 605110 čištění.</span><span class="sxs-lookup"><span data-stu-id="cec66-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="cec66-127">V poli Chování nákladů vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="cec66-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="cec66-128">Vyberte Pevné náklady.</span><span class="sxs-lookup"><span data-stu-id="cec66-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="cec66-129">V poli Základ přidělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="cec66-130">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cec66-130">Click New.</span></span>
8. <span data-ttu-id="cec66-131">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cec66-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="cec66-132">V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-133">Rozbalte hierarchii a vyberte 094.</span><span class="sxs-lookup"><span data-stu-id="cec66-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="cec66-134">V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cec66-135">Vyberte Další provozní výdaje a poté vyberte 605150 Renta.</span><span class="sxs-lookup"><span data-stu-id="cec66-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="cec66-136">V poli Chování nákladů vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="cec66-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="cec66-137">Vyberte Pevné náklady.</span><span class="sxs-lookup"><span data-stu-id="cec66-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="cec66-138">V poli Základ přidělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="cec66-139">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cec66-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="cec66-140">Přiřazení pravidel k jednotce pro řízení nákladů</span><span class="sxs-lookup"><span data-stu-id="cec66-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="cec66-141">Klikněte na Přiřazení zásady pro kontrolní jednotky nákladů.</span><span class="sxs-lookup"><span data-stu-id="cec66-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="cec66-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cec66-142">Click New.</span></span>
3. <span data-ttu-id="cec66-143">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cec66-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cec66-144">Zadejte datum do pole Platné od data účtování.</span><span class="sxs-lookup"><span data-stu-id="cec66-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="cec66-145">Vyberte platný fiskální rok – 1. září.</span><span class="sxs-lookup"><span data-stu-id="cec66-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="cec66-146">V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cec66-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="cec66-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cec66-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]