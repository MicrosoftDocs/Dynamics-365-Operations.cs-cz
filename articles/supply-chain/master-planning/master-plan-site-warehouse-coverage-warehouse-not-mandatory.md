---
title: Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný
description: Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu není povinná.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6b9814a0a5a069d945c7888da17348ecfe4d4a7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187523"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="d0c36-104">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="d0c36-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0c36-105">Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility.</span><span class="sxs-lookup"><span data-stu-id="d0c36-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="d0c36-106">Dimenze skladu není povinná.</span><span class="sxs-lookup"><span data-stu-id="d0c36-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="d0c36-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d0c36-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d0c36-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="d0c36-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="d0c36-109">Toto nastavení nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="d0c36-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="d0c36-110">Dimenze skladu není povinná.</span><span class="sxs-lookup"><span data-stu-id="d0c36-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="d0c36-111">Sklad může být znám, ale při výpočtu během hlavního plánování se nepoužije.</span><span class="sxs-lookup"><span data-stu-id="d0c36-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="d0c36-112">Dimenze pracoviště a skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="d0c36-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="d0c36-113">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="d0c36-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="d0c36-114">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="d0c36-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="d0c36-115">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="d0c36-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d0c36-116">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="d0c36-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d0c36-117">Sklad je nastaven na možnost Ruční.</span><span class="sxs-lookup"><span data-stu-id="d0c36-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="d0c36-118">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d0c36-119">Na pevné záložce **Hlavní plánování** zkontrolujte pole **Ruční**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="d0c36-120">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="d0c36-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="d0c36-121">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d0c36-122">Zvolte položku a poté v podokně akcí na kartě **Plán** klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="d0c36-123">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="d0c36-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d0c36-124">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d0c36-125">Na pevné záložce **Hlavní plánování** zkontrolujte skupinu polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d0c36-126">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="d0c36-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="d0c36-127">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d0c36-128">Zvolte položku a poté v podokně akcí na kartě **Plán** klikněte na možnost **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="d0c36-129">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d0c36-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na pracoviště a sklad, sklad není](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a><span data-ttu-id="d0c36-131">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d0c36-131">Additional resources</span></span>

[<span data-ttu-id="d0c36-132">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="d0c36-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d0c36-133">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="d0c36-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d0c36-134">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný</span><span class="sxs-lookup"><span data-stu-id="d0c36-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d0c36-135">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="d0c36-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d0c36-136">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="d0c36-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]