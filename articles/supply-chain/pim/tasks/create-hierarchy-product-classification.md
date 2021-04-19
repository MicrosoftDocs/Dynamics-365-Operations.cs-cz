---
title: Vytvoření hierarchie klasifikace produktu
description: Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.
author: ShylaThompson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4e2fdc62d7faa73efa78092d7754d3fa1213a94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809367"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="5b7a7-103">Vytvoření hierarchie klasifikace produktu</span><span class="sxs-lookup"><span data-stu-id="5b7a7-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b7a7-104">Tento postup popisuje, jak vytvořit novou hierarchii kategorií a přiřadit typ hierarchie kódů komodit.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="5b7a7-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5b7a7-106">Tento postup je určen pro správce kategorií.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="5b7a7-107">Vytvoření nové hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="5b7a7-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="5b7a7-108">Přejděte na **Navigační podokno > Moduly > Řízení informací o produktech > Nastavení > Kategorie a atributy > Hierarchie kategorií**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="5b7a7-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-109">Click **New**.</span></span>
3. <span data-ttu-id="5b7a7-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="5b7a7-111">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5b7a7-112">Klepněte na volbu **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="5b7a7-113">Vytvoření hierarchie</span><span class="sxs-lookup"><span data-stu-id="5b7a7-113">Build the hierarchy</span></span>
1. <span data-ttu-id="5b7a7-114">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-114">Click **New** category node.</span></span>
2. <span data-ttu-id="5b7a7-115">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="5b7a7-116">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="5b7a7-117">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="5b7a7-118">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-118">Click **New** category node.</span></span>
6. <span data-ttu-id="5b7a7-119">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="5b7a7-120">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="5b7a7-121">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="5b7a7-122">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-122">Click **New** category node.</span></span>
10. <span data-ttu-id="5b7a7-123">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="5b7a7-124">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="5b7a7-125">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="5b7a7-126">Klikněte na **Nový** uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-126">Click **New** category node.</span></span>
14. <span data-ttu-id="5b7a7-127">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="5b7a7-128">Zadejte hodnotu do pole **Kód**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="5b7a7-129">Do pole **Popisný název** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="5b7a7-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="5b7a7-131">Klasifikace hierarchie</span><span class="sxs-lookup"><span data-stu-id="5b7a7-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="5b7a7-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="5b7a7-133">V **podokně akcí** klikněte na možnost **Hierar chie kategorií**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="5b7a7-134">Klikněte na možnost **Přidružit typ hierarchie**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="5b7a7-135">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-135">Click **New**.</span></span>
5. <span data-ttu-id="5b7a7-136">V poli **Typ hierarchie kategorií** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="5b7a7-137">Vyberte **typ hierarchie kategorií kódů komodity pro klasifikaci produktu**.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="5b7a7-138">V poli **Hierarchie kategorií** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5b7a7-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5b7a7-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5b7a7-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5b7a7-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]