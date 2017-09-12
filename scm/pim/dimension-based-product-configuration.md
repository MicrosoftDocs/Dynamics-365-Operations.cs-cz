---
title: "Konfigurace produktu založené na dimenzích"
description: "Konfigurace produktu založená na dimenzích představuje jednoduché řešení pro vytváření mnoho variant produktu z jednoho hlavního produktu a příslušných kusovníků."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 89f01401f1d937a72ae7e59b784cf034b48aaf1f
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="7e430-103">Konfigurace produktu založené na dimenzích</span><span class="sxs-lookup"><span data-stu-id="7e430-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7e430-104">Konfigurace produktu založená na dimenzích představuje jednoduché řešení pro vytváření mnoho variant produktu z jednoho hlavního produktu a příslušných kusovníků.</span><span class="sxs-lookup"><span data-stu-id="7e430-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="7e430-105">Konfigurace produktu založená na dimenzích je jednou ze tři předdefinovaných technologií konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="7e430-106">Zbývající dvě technologie jsou předdefinované varianty a konfigurace založená na omezeních.</span><span class="sxs-lookup"><span data-stu-id="7e430-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="7e430-107">Všechny tři technologie používají základní produkt jako výchozí bod a umožňují uživateli vytvořit mnoho variant produktu pro jeden základní produkt.</span><span class="sxs-lookup"><span data-stu-id="7e430-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="7e430-108">Klíčové koncepty</span><span class="sxs-lookup"><span data-stu-id="7e430-108">Key concepts</span></span>
<span data-ttu-id="7e430-109">Konfigurace produktu založená na dimenzích vychází z následujících klíčových konceptů:</span><span class="sxs-lookup"><span data-stu-id="7e430-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="7e430-110">Základní produkty</span><span class="sxs-lookup"><span data-stu-id="7e430-110">Product masters</span></span>
-   <span data-ttu-id="7e430-111">Konfigurační dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="7e430-111">Configuration product dimension</span></span>
-   <span data-ttu-id="7e430-112">Konfigurační skupiny</span><span class="sxs-lookup"><span data-stu-id="7e430-112">Configuration groups</span></span>
-   <span data-ttu-id="7e430-113">Kusovník</span><span class="sxs-lookup"><span data-stu-id="7e430-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="7e430-114">Konfigurační postup</span><span class="sxs-lookup"><span data-stu-id="7e430-114">Configuration route</span></span>
-   <span data-ttu-id="7e430-115">Konfigurační pravidla</span><span class="sxs-lookup"><span data-stu-id="7e430-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="7e430-116">Základní produkty</span><span class="sxs-lookup"><span data-stu-id="7e430-116">Product masters</span></span>

<span data-ttu-id="7e430-117">Základní produkt je výchozím bodem pro všechny procesy konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="7e430-118">Pro konfiguraci produktu založenou na dimenzích je vyžadován základní produkt s konkrétní technologií konfigurace a skupina dimenzí produktu, která zahrnuje konfigurační dimenzi produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="7e430-119">Konfigurační dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="7e430-119">Configuration product dimension</span></span>

<span data-ttu-id="7e430-120">Konfigurační dimenze produktu se používá k identifikaci variant produktu pro základní produkt s technologií konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="7e430-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="7e430-121">Hodnotu dimenze pro konfiguraci zadává uživatel a měla by pomoci k určení individuálních variant produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="7e430-122">Konfigurační skupiny</span><span class="sxs-lookup"><span data-stu-id="7e430-122">Configuration groups</span></span>

<span data-ttu-id="7e430-123">Konfigurační skupiny se definují v centrálním úložišti a lze je použít pro všechny modely konfigurace produktu založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="7e430-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="7e430-124">Konfigurační skupiny jsou připojeny k jednotlivým řádkům kusovníku a společně tvoří skupinu řádků, které se vzájemně vylučují.</span><span class="sxs-lookup"><span data-stu-id="7e430-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="7e430-125">To znamená, že pro jednu variantu produktu lze vybrat pouze jeden řádek v určité skupině.</span><span class="sxs-lookup"><span data-stu-id="7e430-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="7e430-126">Kusovník</span><span class="sxs-lookup"><span data-stu-id="7e430-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="7e430-127">Kusovník představuje stavební kameny konfigurace produktu založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="7e430-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="7e430-128">Musí obsahovat všechny jiné produkty, které lze použít v kterékoli variantě produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="7e430-129">Každý řádek v kusovníku může odkazovat na konfigurační skupinu.</span><span class="sxs-lookup"><span data-stu-id="7e430-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="7e430-130">Pokud řádek neodkazuje na konfigurační skupinu, zahrne se do všech variant produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="7e430-131">Konfigurační postup</span><span class="sxs-lookup"><span data-stu-id="7e430-131">Configuration route</span></span>

<span data-ttu-id="7e430-132">Konfigurační postup určuje pořadí skupin konfigurace, ve kterém se uživateli zobrazují během procesu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="7e430-133">Konfigurační pravidla</span><span class="sxs-lookup"><span data-stu-id="7e430-133">Configuration rules</span></span>

<span data-ttu-id="7e430-134">Konfigurační pravidla představují mechanismus, který zajišťuje, že produkt zahrnutý v jedné konfigurační skupině v kusovníku vynutí buď zahrnutí, nebo vyloučení produktu v jiné konfigurační skupině ve stejném kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7e430-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="7e430-135">Proces modelování produktu</span><span class="sxs-lookup"><span data-stu-id="7e430-135">Product modeling process</span></span>
<span data-ttu-id="7e430-136">Přirozená sekvence vytváření modelu produktu začíná pro produkty založené na dimenzích určením odpovídajících konfiguračních skupin.</span><span class="sxs-lookup"><span data-stu-id="7e430-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="7e430-137">Je důležité zajistit, aby se všechny produkty, které se použijí v kusovníku, uvolnily společnosti, pro kterou se model produktu vytváří.</span><span class="sxs-lookup"><span data-stu-id="7e430-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="7e430-138">Pomocí těchto stavebních bloků může uživatel vytvořit kusovník a přiřadit konfigurační skupiny všem odpovídajícím řádkům kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7e430-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="7e430-139">Po dokončení kusovníku lze definovat konfigurační postup pro řazení konfiguračních skupin ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="7e430-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="7e430-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Proces modelování produktu založeného na dimenzích](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Proces modelování produktu založeného na dimenzích\[/caption\] Pokud existují určité produkty z různých konfiguračních skupin, které se musí nebo nesmí použít společně, můžete vytvořit konfigurační pravidla, která vynutí tyto vztahy produktů.</span><span class="sxs-lookup"><span data-stu-id="7e430-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimension-based product modeling process\[/caption\] If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="7e430-141">Poté, co se kusovník provázal se základním produktem založeným na dimenzích pomocí verze kusovníku a oba jsou schválené a aktivované, lze vytvořit konfiguraci produktu zadat název pro každou konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7e430-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="7e430-142">Konfigurace lze definovat předtím, než se vygenerují transakce, nebo to lze provést, jakmile dojde k potřebě určité konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7e430-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="7e430-143">Předpokládané použití</span><span class="sxs-lookup"><span data-stu-id="7e430-143">Suggested use</span></span>

<span data-ttu-id="7e430-144">Technologie konfigurace založené na dimenzích je nejvhodnější pro produkty s omezenou variabilitou a kombinací standardní velikosti, barvy a stylu dimenzí produktu. Konfigurace není vhodná pro identifikaci konkrétní varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="7e430-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="7e430-145">Příkladem může být jízdní kolo s výškou rámu, velikostí kola, typem brzd a různým vybavením.</span><span class="sxs-lookup"><span data-stu-id="7e430-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>




