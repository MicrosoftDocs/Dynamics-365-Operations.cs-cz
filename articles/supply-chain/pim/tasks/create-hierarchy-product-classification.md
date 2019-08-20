---
title: Vytvoření hierarchie klasifikace produktu
description: Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faf43eb15283ffd7e36ad38728f166884dddcd85
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844818"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="07e16-103">Vytvoření hierarchie klasifikace produktu</span><span class="sxs-lookup"><span data-stu-id="07e16-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07e16-104">Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.</span><span class="sxs-lookup"><span data-stu-id="07e16-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="07e16-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="07e16-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07e16-106">Tento postup je určen pro správce kategorií.</span><span class="sxs-lookup"><span data-stu-id="07e16-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="07e16-107">Vytvoření nové hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="07e16-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="07e16-108">Přejděte na **Navigační podokno > Moduly > Řízení informací o produktech > Nastavení > Kategorie a atributy > Hierarchie kategorií**.</span><span class="sxs-lookup"><span data-stu-id="07e16-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="07e16-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="07e16-109">Click **New**.</span></span>
3. <span data-ttu-id="07e16-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="07e16-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="07e16-111">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="07e16-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="07e16-112">Klepněte na volbu **Nový**.</span><span class="sxs-lookup"><span data-stu-id="07e16-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="07e16-113">Vytvoření hierarchie</span><span class="sxs-lookup"><span data-stu-id="07e16-113">Build the hierarchy</span></span>
1. <span data-ttu-id="07e16-114">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="07e16-114">Click **New** category node.</span></span>
2. <span data-ttu-id="07e16-115">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="07e16-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="07e16-116">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="07e16-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="07e16-117">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="07e16-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="07e16-118">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="07e16-118">Click **New** category node.</span></span>
6. <span data-ttu-id="07e16-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="07e16-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="07e16-120">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="07e16-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="07e16-121">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="07e16-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="07e16-122">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="07e16-122">Click **New** category node.</span></span>
10. <span data-ttu-id="07e16-123">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="07e16-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="07e16-124">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="07e16-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="07e16-125">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="07e16-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="07e16-126">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="07e16-126">Click **New** category node.</span></span>
14. <span data-ttu-id="07e16-127">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="07e16-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="07e16-128">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="07e16-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="07e16-129">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="07e16-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="07e16-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="07e16-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="07e16-131">Klasifikace hierarchie</span><span class="sxs-lookup"><span data-stu-id="07e16-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="07e16-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="07e16-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="07e16-133">V **podokně akcí** klikněte na možnost **Hierar chie kategorií**.</span><span class="sxs-lookup"><span data-stu-id="07e16-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="07e16-134">Klikněte na možnost **Přidružit typ hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="07e16-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="07e16-135">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="07e16-135">Click **New**.</span></span>
5. <span data-ttu-id="07e16-136">V poli **Typ hierarchie kategorií** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="07e16-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="07e16-137">Vyberte **typ hierarchie kategorií kódů komodity pro klasifikaci produktu**.</span><span class="sxs-lookup"><span data-stu-id="07e16-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="07e16-138">V poli **Hierarchie kategorií** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="07e16-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="07e16-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="07e16-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="07e16-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="07e16-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="07e16-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="07e16-141">Close the page.</span></span>

