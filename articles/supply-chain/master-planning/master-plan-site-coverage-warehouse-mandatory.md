---
title: Hlavní plánování pro disponibilitu pracoviště, povinný sklad
description: Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility. Sklad je povinná dimenze.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b1890f14351734c26952511f6245efe4cce5f3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424048"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="5a098-104">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="5a098-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a098-105">Toto téma popisuje, jak je plánována položka, která má pracoviště jako dimenzi disponibility.</span><span class="sxs-lookup"><span data-stu-id="5a098-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="5a098-106">Sklad je povinná dimenze.</span><span class="sxs-lookup"><span data-stu-id="5a098-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="5a098-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="5a098-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="5a098-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="5a098-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="5a098-109">Toto nastavení nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="5a098-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="5a098-110">Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="5a098-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="5a098-111">Dimenze pracovišť je nastavená pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="5a098-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="5a098-112">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="5a098-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="5a098-113">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="5a098-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="5a098-114">Skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="5a098-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="5a098-115">Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="5a098-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="5a098-116">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="5a098-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="5a098-117">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="5a098-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="5a098-118">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="5a098-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="5a098-119">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="5a098-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5a098-120">Vyberte položku a poté klikněte na volbu **Plán &gt; Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="5a098-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="5a098-121">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="5a098-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="5a098-122">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="5a098-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5a098-123">Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="5a098-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="5a098-124">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="5a098-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="5a098-125">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="5a098-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5a098-126">Vyberte položku a poté klikněte na volbu **Plán &gt; Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="5a098-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="5a098-127">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="5a098-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na disponibilitu skladu pracoviště je povinný](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="5a098-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5a098-129">Additional resources</span></span>
--------

[<span data-ttu-id="5a098-130">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="5a098-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="5a098-131">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný</span><span class="sxs-lookup"><span data-stu-id="5a098-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5a098-132">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="5a098-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5a098-133">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="5a098-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5a098-134">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="5a098-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



