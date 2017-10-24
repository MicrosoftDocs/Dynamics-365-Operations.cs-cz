---
title: "Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný"
description: "Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu je povinná."
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e753edacb0e2e019d701745308e7d9190ef09fe8
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="547fe-104">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný</span><span class="sxs-lookup"><span data-stu-id="547fe-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="547fe-105">Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility.</span><span class="sxs-lookup"><span data-stu-id="547fe-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="547fe-106">Dimenze skladu je povinná.</span><span class="sxs-lookup"><span data-stu-id="547fe-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="547fe-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="547fe-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="547fe-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="547fe-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="547fe-109">Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="547fe-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="547fe-110">Dimenze pracoviště a skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="547fe-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="547fe-111">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="547fe-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="547fe-112">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="547fe-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="547fe-113">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="547fe-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="547fe-114">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="547fe-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="547fe-115">Sklad je nastaven na možnost **Ruční**.</span><span class="sxs-lookup"><span data-stu-id="547fe-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="547fe-116">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="547fe-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="547fe-117">Na pevné záložce **Hlavní plánování** zkontrolujte pole **Ruční**.</span><span class="sxs-lookup"><span data-stu-id="547fe-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="547fe-118">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="547fe-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="547fe-119">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="547fe-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="547fe-120">Zvolte položku a poté v podokně Akce na kartě **Plán** klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="547fe-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="547fe-121">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="547fe-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="547fe-122">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="547fe-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="547fe-123">Na pevné záložce **Hlavní plánování** zkontrolujte skupinu polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="547fe-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="547fe-124">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="547fe-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="547fe-125">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="547fe-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="547fe-126">Zvolte položku a poté v podokně Akce na kartě **Plán** klikněte na možnost **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="547fe-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="547fe-127">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="547fe-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na pokrytí pracoviště a skladu, povinný](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="547fe-129">Viz také</span><span class="sxs-lookup"><span data-stu-id="547fe-129">See also</span></span>
--------

[<span data-ttu-id="547fe-130">Hlavní plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="547fe-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="547fe-131">Hlavní plánování – disponibilita pracoviště, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="547fe-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="547fe-132">Hlavní plánování – disponibilita pracoviště, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="547fe-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="547fe-133">Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="547fe-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="547fe-134">Hlavní plánování – jak se určuje verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="547fe-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




