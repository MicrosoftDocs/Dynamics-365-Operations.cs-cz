---
title: Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný
description: Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu není povinná.
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45796049cddef137eb2ca1e4331197e4b4a65071
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546287"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="fd37d-104">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="fd37d-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd37d-105">Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility.</span><span class="sxs-lookup"><span data-stu-id="fd37d-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="fd37d-106">Dimenze skladu není povinná.</span><span class="sxs-lookup"><span data-stu-id="fd37d-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="fd37d-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="fd37d-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="fd37d-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="fd37d-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="fd37d-109">Toto nastavení nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="fd37d-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="fd37d-110">Dimenze skladu není povinná.</span><span class="sxs-lookup"><span data-stu-id="fd37d-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="fd37d-111">Sklad může být znám, ale při výpočtu během hlavního plánování se nepoužije.</span><span class="sxs-lookup"><span data-stu-id="fd37d-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="fd37d-112">Dimenze pracoviště a skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="fd37d-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="fd37d-113">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="fd37d-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="fd37d-114">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="fd37d-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="fd37d-115">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="fd37d-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="fd37d-116">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="fd37d-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="fd37d-117">Sklad je nastaven na možnost Ruční.</span><span class="sxs-lookup"><span data-stu-id="fd37d-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="fd37d-118">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="fd37d-119">Na pevné záložce **Hlavní plánování** zkontrolujte pole **Ruční**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="fd37d-120">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="fd37d-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="fd37d-121">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="fd37d-122">Zvolte položku a poté v podokně Akce na kartě **Plán** klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="fd37d-123">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="fd37d-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="fd37d-124">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="fd37d-125">Na pevné záložce **Hlavní plánování** zkontrolujte skupinu polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="fd37d-126">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="fd37d-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="fd37d-127">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="fd37d-128">Zvolte položku a poté v podokně Akce na kartě **Plán** klikněte na možnost **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="fd37d-129">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="fd37d-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na pracoviště a sklad, sklad není](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)


-



<a name="additional-resources"></a><span data-ttu-id="fd37d-131">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="fd37d-131">Additional resources</span></span>
--------

[<span data-ttu-id="fd37d-132">Hlavní plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="fd37d-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="fd37d-133">Hlavní plánování – disponibilita pracoviště a skladu, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="fd37d-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="fd37d-134">Hlavní plánování – disponibilita pracoviště, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="fd37d-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="fd37d-135">Hlavní plánování – disponibilita pracoviště, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="fd37d-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="fd37d-136">Hlavní plánování – jak se určuje verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="fd37d-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



