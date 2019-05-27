---
title: Vytvoření hierarchie klasifikace produktu
description: Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568413"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="fe2e9-103">Vytvoření hierarchie klasifikace produktu</span><span class="sxs-lookup"><span data-stu-id="fe2e9-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe2e9-104">Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="fe2e9-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fe2e9-106">Tento postup je určen pro správce kategorií.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="fe2e9-107">Vytvoření nové hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="fe2e9-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="fe2e9-108">Přejděte do nabídky Řízení informací o produktech > Nastavení > Kategorie a atributy > Hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="fe2e9-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-109">Click New.</span></span>
3. <span data-ttu-id="fe2e9-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fe2e9-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fe2e9-112">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="fe2e9-113">Vytvoření hierarchie</span><span class="sxs-lookup"><span data-stu-id="fe2e9-113">Build the hierarchy</span></span>
1. <span data-ttu-id="fe2e9-114">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-114">Click New category node.</span></span>
2. <span data-ttu-id="fe2e9-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="fe2e9-116">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="fe2e9-117">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="fe2e9-118">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-118">Click New category node.</span></span>
6. <span data-ttu-id="fe2e9-119">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="fe2e9-120">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="fe2e9-121">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="fe2e9-122">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-122">Click New category node.</span></span>
10. <span data-ttu-id="fe2e9-123">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="fe2e9-124">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="fe2e9-125">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="fe2e9-126">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-126">Click New category node.</span></span>
14. <span data-ttu-id="fe2e9-127">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="fe2e9-128">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="fe2e9-129">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="fe2e9-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="fe2e9-131">Klasifikace hierarchie</span><span class="sxs-lookup"><span data-stu-id="fe2e9-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="fe2e9-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="fe2e9-133">V podokně akcí klikněte na možnost Hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="fe2e9-134">Klikněte na možnost Přidružit typ hierarchie.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="fe2e9-135">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-135">Click New.</span></span>
5. <span data-ttu-id="fe2e9-136">V poli Typ hierarchie kategorií vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="fe2e9-137">Vyberte typ hierarchie kategorií kódů komodity pro klasifikaci produktu.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="fe2e9-138">V poli Hierarchie kategorií kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fe2e9-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fe2e9-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="fe2e9-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fe2e9-141">Close the page.</span></span>

