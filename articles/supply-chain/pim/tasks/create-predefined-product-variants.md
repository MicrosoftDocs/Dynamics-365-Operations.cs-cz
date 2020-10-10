---
title: Vytváření předdefinovaných variant produktů
description: Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6009f6de76155ea7c2982b28fe4505232447c9c8
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895298"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="d6db0-103">Vytváření předdefinovaných variant produktů</span><span class="sxs-lookup"><span data-stu-id="d6db0-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6db0-104">Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="d6db0-105">K vytvoření tohoto postupu je použita ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="d6db0-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="d6db0-106">Vytvoření základního produktu</span><span class="sxs-lookup"><span data-stu-id="d6db0-106">Create a product master</span></span>
1. <span data-ttu-id="d6db0-107">Přejděte do nabídky Řízení informací o produktech > Produkty > Základní produkty.</span><span class="sxs-lookup"><span data-stu-id="d6db0-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="d6db0-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d6db0-108">Click New.</span></span>
3. <span data-ttu-id="d6db0-109">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="d6db0-110">Ruční zadání čísla produktu je povinné, pouze není-li nastavena číselná řada pro pole čísla produktu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="d6db0-111">Jinak řečeno tento krok přeskočte, je-li pro dané pole nastavena číselná řada.</span><span class="sxs-lookup"><span data-stu-id="d6db0-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="d6db0-112">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="d6db0-113">V poli Skupina dimenze produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="d6db0-114">Vyberte skupinu dimenzí produktu SizeCol (velikost a barva).</span><span class="sxs-lookup"><span data-stu-id="d6db0-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="d6db0-115">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d6db0-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="d6db0-116">Přidání dimenzí produktu</span><span class="sxs-lookup"><span data-stu-id="d6db0-116">Add product dimensions</span></span>
1. <span data-ttu-id="d6db0-117">Klikněte na Dimenze produktu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="d6db0-118">Tento příklad ukazuje, jak zadávat dimenze produktu ručně.</span><span class="sxs-lookup"><span data-stu-id="d6db0-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="d6db0-119">Rovněž je možné vybrat velikost, barvu nebo skupinu stylů, která obsahuje hodnoty dimenze produktu, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="d6db0-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="d6db0-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d6db0-120">Click New.</span></span>
3. <span data-ttu-id="d6db0-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d6db0-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d6db0-122">V poli Velikost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="d6db0-123">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d6db0-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d6db0-124">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="d6db0-124">Click New.</span></span>
7. <span data-ttu-id="d6db0-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d6db0-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d6db0-126">V poli Velikost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="d6db0-127">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d6db0-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="d6db0-128">Klikněte na kartu Barvy.</span><span class="sxs-lookup"><span data-stu-id="d6db0-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="d6db0-129">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d6db0-129">Click New.</span></span>
12. <span data-ttu-id="d6db0-130">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d6db0-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="d6db0-131">V poli Barva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="d6db0-132">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d6db0-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="d6db0-133">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="d6db0-133">Click New.</span></span>
16. <span data-ttu-id="d6db0-134">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d6db0-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d6db0-135">V poli Barva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="d6db0-136">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d6db0-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="d6db0-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d6db0-137">Click Save.</span></span>
20. <span data-ttu-id="d6db0-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d6db0-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="d6db0-139">Vytvoření variant produktů</span><span class="sxs-lookup"><span data-stu-id="d6db0-139">Generate product variants</span></span>
1. <span data-ttu-id="d6db0-140">Klikněte na Varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-140">Click Product variants.</span></span>
2. <span data-ttu-id="d6db0-141">Klikněte na Návrhy variant.</span><span class="sxs-lookup"><span data-stu-id="d6db0-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="d6db0-142">Klikněte na Vybrat vše.</span><span class="sxs-lookup"><span data-stu-id="d6db0-142">Click Select all.</span></span>
    * <span data-ttu-id="d6db0-143">V tomto příkladu jsou vybrány všechny možné varianty.</span><span class="sxs-lookup"><span data-stu-id="d6db0-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="d6db0-144">Pokud se použije pouze podmnožina možných kombinací dimenzí produktu pro vytváření variant, můžete vybrat jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="d6db0-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="d6db0-145">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="d6db0-145">Click Create.</span></span>
    * <span data-ttu-id="d6db0-146">Popisy je možné generovat pro všechny vaše varianty na základě kombinace hodnot dimenze produktu.</span><span class="sxs-lookup"><span data-stu-id="d6db0-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="d6db0-147">Popisy jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="d6db0-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="d6db0-148">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d6db0-148">Click Save.</span></span>

