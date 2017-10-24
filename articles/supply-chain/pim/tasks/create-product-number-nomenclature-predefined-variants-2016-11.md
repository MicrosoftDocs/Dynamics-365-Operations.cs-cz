--- 
title: "Vytvoření čísla produktu pro předdefinované varianty produktu"
description: "Tato příručka ukazuje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="065b5-103">Vytvoření čísla produktu pro předdefinované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="065b5-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="065b5-104">Tato příručka ukazuje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="065b5-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="065b5-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="065b5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="065b5-106">Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost.</span><span class="sxs-lookup"><span data-stu-id="065b5-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="065b5-107">Tento úkol obvykle provádí návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="065b5-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="065b5-108">Vytvoření názvosloví čísla produktu</span><span class="sxs-lookup"><span data-stu-id="065b5-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="065b5-109">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="065b5-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="065b5-110">Klikněte na Zobrazit názvosloví produktu.</span><span class="sxs-lookup"><span data-stu-id="065b5-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="065b5-111">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="065b5-111">Click New.</span></span>
4. <span data-ttu-id="065b5-112">V poli Název zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například ColorSize.</span><span class="sxs-lookup"><span data-stu-id="065b5-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="065b5-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="065b5-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="065b5-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="065b5-114">Click Add.</span></span>
7. <span data-ttu-id="065b5-115">Klikněte na Číslo základního produktu.</span><span class="sxs-lookup"><span data-stu-id="065b5-115">Click Product master number.</span></span>
8. <span data-ttu-id="065b5-116">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="065b5-116">Click Add.</span></span>
9. <span data-ttu-id="065b5-117">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="065b5-117">Click Text constant.</span></span>
10. <span data-ttu-id="065b5-118">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="065b5-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="065b5-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="065b5-119">Click Add.</span></span>
12. <span data-ttu-id="065b5-120">Klikněte na Barva.</span><span class="sxs-lookup"><span data-stu-id="065b5-120">Click Color.</span></span>
13. <span data-ttu-id="065b5-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="065b5-121">Click Add.</span></span>
14. <span data-ttu-id="065b5-122">Klikněte na Textová konstanta.</span><span class="sxs-lookup"><span data-stu-id="065b5-122">Click Text constant.</span></span>
15. <span data-ttu-id="065b5-123">Zadejte hodnotu do pole Text.</span><span class="sxs-lookup"><span data-stu-id="065b5-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="065b5-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="065b5-124">Click Add.</span></span>
17. <span data-ttu-id="065b5-125">Klepněte na Velikost.</span><span class="sxs-lookup"><span data-stu-id="065b5-125">Click Size.</span></span>
18. <span data-ttu-id="065b5-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="065b5-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="065b5-127">Přiřazení názvosloví základnímu produktu</span><span class="sxs-lookup"><span data-stu-id="065b5-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="065b5-128">Klikněte na Skupiny dimenzí produktů.</span><span class="sxs-lookup"><span data-stu-id="065b5-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="065b5-129">Vyberte skupinu dimenzí produktu SizeCol.</span><span class="sxs-lookup"><span data-stu-id="065b5-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="065b5-130">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="065b5-130">Click Edit.</span></span>
4. <span data-ttu-id="065b5-131">Vyberte možnost Ano v poli Použít názvosloví.</span><span class="sxs-lookup"><span data-stu-id="065b5-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="065b5-132">V poli Názvosloví čísla varianty produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="065b5-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="065b5-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="065b5-133">Close the page.</span></span>


