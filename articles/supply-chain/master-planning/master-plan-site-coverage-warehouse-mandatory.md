---
title: "Hlavní plánování pro disponibilitu pracoviště, povinný sklad"
description: "Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility. Sklad je povinná dimenze."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 14df626025a22237afe30cc5b08d42b475fc3a4f
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="57e3d-104">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="57e3d-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="57e3d-105">Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility.</span><span class="sxs-lookup"><span data-stu-id="57e3d-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="57e3d-106">Sklad je povinná dimenze.</span><span class="sxs-lookup"><span data-stu-id="57e3d-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="57e3d-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="57e3d-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="57e3d-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="57e3d-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="57e3d-109">Toto nastavení nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="57e3d-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="57e3d-110">Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="57e3d-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="57e3d-111">Dimenze pracovišť je nastavená pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="57e3d-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="57e3d-112">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="57e3d-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="57e3d-113">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="57e3d-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="57e3d-114">Skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="57e3d-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="57e3d-115">Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="57e3d-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="57e3d-116">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="57e3d-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="57e3d-117">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="57e3d-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="57e3d-118">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="57e3d-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="57e3d-119">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="57e3d-120">Vyberte položku a poté klikněte na volbu **Plán &gt; Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="57e3d-121">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="57e3d-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="57e3d-122">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="57e3d-123">Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="57e3d-124">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="57e3d-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="57e3d-125">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="57e3d-126">Vyberte položku a poté klikněte na volbu **Plán &gt; Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="57e3d-127">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="57e3d-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na disponibilitu skladu pracoviště je povinný](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="57e3d-129">Viz také</span><span class="sxs-lookup"><span data-stu-id="57e3d-129">See also</span></span>
--------

[<span data-ttu-id="57e3d-130">Hlavní plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="57e3d-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="57e3d-131">Hlavní plánování – disponibilita pracoviště a skladu, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="57e3d-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="57e3d-132">Hlavní plánování – disponibilita pracoviště, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="57e3d-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="57e3d-133">Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="57e3d-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="57e3d-134">Hlavní plánování – jak se určuje verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="57e3d-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




