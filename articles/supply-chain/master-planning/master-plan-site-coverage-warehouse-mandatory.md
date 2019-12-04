---
title: Hlavní plánování pro disponibilitu pracoviště, povinný sklad
description: Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility. Sklad je povinná dimenze.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 132817fefb9592764d1adaf9f714c27108ce88ae
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815104"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="aa029-104">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="aa029-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa029-105">Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility.</span><span class="sxs-lookup"><span data-stu-id="aa029-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="aa029-106">Sklad je povinná dimenze.</span><span class="sxs-lookup"><span data-stu-id="aa029-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="aa029-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="aa029-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="aa029-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="aa029-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="aa029-109">Toto nastavení nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="aa029-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="aa029-110">Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="aa029-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="aa029-111">Dimenze pracovišť je nastavená pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="aa029-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="aa029-112">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="aa029-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="aa029-113">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="aa029-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="aa029-114">Skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="aa029-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="aa029-115">Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="aa029-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="aa029-116">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="aa029-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="aa029-117">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="aa029-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="aa029-118">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="aa029-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="aa029-119">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="aa029-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="aa029-120">Vyberte položku a poté klikněte na volbu **Plán &gt; Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="aa029-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="aa029-121">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="aa029-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="aa029-122">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="aa029-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="aa029-123">Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="aa029-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="aa029-124">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="aa029-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="aa029-125">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="aa029-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="aa029-126">Vyberte položku a poté klikněte na volbu **Plán &gt; Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="aa029-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="aa029-127">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="aa029-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na disponibilitu skladu pracoviště je povinný](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="aa029-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="aa029-129">Additional resources</span></span>
--------

[<span data-ttu-id="aa029-130">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="aa029-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="aa029-131">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný</span><span class="sxs-lookup"><span data-stu-id="aa029-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="aa029-132">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="aa029-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="aa029-133">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="aa029-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="aa029-134">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="aa029-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



