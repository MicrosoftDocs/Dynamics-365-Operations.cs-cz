---
title: Vytváření předdefinovaných variant produktů
description: Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf1e41d0071a4c78d2a0f43548e44ae9d426580
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844770"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="73a03-103">Vytváření předdefinovaných variant produktů</span><span class="sxs-lookup"><span data-stu-id="73a03-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73a03-104">Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="73a03-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="73a03-105">K vytvoření tohoto postupu je použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="73a03-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="73a03-106">Vytvoření základního produktu</span><span class="sxs-lookup"><span data-stu-id="73a03-106">Create a product master</span></span>
1. <span data-ttu-id="73a03-107">Přejděte do nabídky Řízení informací o produktech > Produkty > Základní produkty.</span><span class="sxs-lookup"><span data-stu-id="73a03-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="73a03-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="73a03-108">Click New.</span></span>
3. <span data-ttu-id="73a03-109">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="73a03-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="73a03-110">Ruční zadání čísla produktu je povinné, pouze není-li nastavena číselná řada pro pole čísla produktu.</span><span class="sxs-lookup"><span data-stu-id="73a03-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="73a03-111">Jinak řečeno tento krok přeskočte, je-li pro dané pole nastavena číselná řada.</span><span class="sxs-lookup"><span data-stu-id="73a03-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="73a03-112">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73a03-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="73a03-113">V poli Skupina dimenze produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73a03-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="73a03-114">Vyberte skupinu dimenzí produktu SizeCol (velikost a barva).</span><span class="sxs-lookup"><span data-stu-id="73a03-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="73a03-115">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="73a03-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="73a03-116">Přidání dimenzí produktu</span><span class="sxs-lookup"><span data-stu-id="73a03-116">Add product dimensions</span></span>
1. <span data-ttu-id="73a03-117">Klikněte na Dimenze produktu.</span><span class="sxs-lookup"><span data-stu-id="73a03-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="73a03-118">Tento příklad ukazuje, jak zadávat dimenze produktu ručně.</span><span class="sxs-lookup"><span data-stu-id="73a03-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="73a03-119">Rovněž je možné vybrat velikost, barvu nebo skupinu stylů, která obsahuje hodnoty dimenze produktu, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="73a03-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="73a03-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="73a03-120">Click New.</span></span>
3. <span data-ttu-id="73a03-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="73a03-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="73a03-122">V poli Velikost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73a03-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="73a03-123">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="73a03-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="73a03-124">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="73a03-124">Click New.</span></span>
7. <span data-ttu-id="73a03-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="73a03-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="73a03-126">V poli Velikost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73a03-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="73a03-127">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="73a03-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="73a03-128">Klikněte na kartu Barvy.</span><span class="sxs-lookup"><span data-stu-id="73a03-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="73a03-129">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="73a03-129">Click New.</span></span>
12. <span data-ttu-id="73a03-130">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="73a03-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="73a03-131">V poli Barva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73a03-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="73a03-132">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="73a03-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="73a03-133">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="73a03-133">Click New.</span></span>
16. <span data-ttu-id="73a03-134">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="73a03-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="73a03-135">V poli Barva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73a03-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="73a03-136">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="73a03-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="73a03-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="73a03-137">Click Save.</span></span>
20. <span data-ttu-id="73a03-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="73a03-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="73a03-139">Vytvoření variant produktů</span><span class="sxs-lookup"><span data-stu-id="73a03-139">Generate product variants</span></span>
1. <span data-ttu-id="73a03-140">Klikněte na Varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="73a03-140">Click Product variants.</span></span>
2. <span data-ttu-id="73a03-141">Klikněte na Návrhy variant.</span><span class="sxs-lookup"><span data-stu-id="73a03-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="73a03-142">Klikněte na Vybrat vše.</span><span class="sxs-lookup"><span data-stu-id="73a03-142">Click Select all.</span></span>
    * <span data-ttu-id="73a03-143">V tomto příkladu jsou vybrány všechny možné varianty.</span><span class="sxs-lookup"><span data-stu-id="73a03-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="73a03-144">Pokud se použije pouze podmnožina možných kombinací dimenzí produktu pro vytváření variant, můžete vybrat jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="73a03-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="73a03-145">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="73a03-145">Click Create.</span></span>
    * <span data-ttu-id="73a03-146">Popisy je možné generovat pro všechny vaše varianty na základě kombinace hodnot dimenze produktu.</span><span class="sxs-lookup"><span data-stu-id="73a03-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="73a03-147">Popisy jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="73a03-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="73a03-148">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="73a03-148">Click Save.</span></span>

