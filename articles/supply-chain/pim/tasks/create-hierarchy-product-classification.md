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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "346817"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="2af1c-103">Vytvoření hierarchie klasifikace produktu</span><span class="sxs-lookup"><span data-stu-id="2af1c-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2af1c-104">Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.</span><span class="sxs-lookup"><span data-stu-id="2af1c-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="2af1c-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="2af1c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2af1c-106">Tento postup je určen pro správce kategorií.</span><span class="sxs-lookup"><span data-stu-id="2af1c-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="2af1c-107">Vytvoření nové hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="2af1c-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="2af1c-108">Přejděte do nabídky Řízení informací o produktech > Nastavení > Kategorie a atributy > Hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="2af1c-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="2af1c-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2af1c-109">Click New.</span></span>
3. <span data-ttu-id="2af1c-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2af1c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2af1c-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="2af1c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2af1c-112">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="2af1c-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="2af1c-113">Vytvoření hierarchie</span><span class="sxs-lookup"><span data-stu-id="2af1c-113">Build the hierarchy</span></span>
1. <span data-ttu-id="2af1c-114">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="2af1c-114">Click New category node.</span></span>
2. <span data-ttu-id="2af1c-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2af1c-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="2af1c-116">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="2af1c-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="2af1c-117">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2af1c-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="2af1c-118">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="2af1c-118">Click New category node.</span></span>
6. <span data-ttu-id="2af1c-119">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2af1c-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="2af1c-120">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="2af1c-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="2af1c-121">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2af1c-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="2af1c-122">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="2af1c-122">Click New category node.</span></span>
10. <span data-ttu-id="2af1c-123">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2af1c-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="2af1c-124">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="2af1c-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="2af1c-125">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2af1c-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="2af1c-126">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="2af1c-126">Click New category node.</span></span>
14. <span data-ttu-id="2af1c-127">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2af1c-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="2af1c-128">Zadejte hodnotu do pole Kód.</span><span class="sxs-lookup"><span data-stu-id="2af1c-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="2af1c-129">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2af1c-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="2af1c-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2af1c-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="2af1c-131">Klasifikace hierarchie</span><span class="sxs-lookup"><span data-stu-id="2af1c-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="2af1c-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2af1c-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="2af1c-133">V podokně akcí klikněte na možnost Hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="2af1c-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="2af1c-134">Klikněte na možnost Přidružit typ hierarchie.</span><span class="sxs-lookup"><span data-stu-id="2af1c-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="2af1c-135">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2af1c-135">Click New.</span></span>
5. <span data-ttu-id="2af1c-136">V poli Typ hierarchie kategorií vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="2af1c-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="2af1c-137">Vyberte typ hierarchie kategorií kódů komodity pro klasifikaci produktu.</span><span class="sxs-lookup"><span data-stu-id="2af1c-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="2af1c-138">V poli Hierarchie kategorií kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="2af1c-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2af1c-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2af1c-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2af1c-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2af1c-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2af1c-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2af1c-141">Close the page.</span></span>

