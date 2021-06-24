---
title: Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný
description: Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility. Dimenze skladu je povinná.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 132a7171488b3c4da8ef13e11bed87c78071744d
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187451"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="dd974-104">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný</span><span class="sxs-lookup"><span data-stu-id="dd974-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd974-105">Toto téma popisuje, jak je plánována položka, která má pracoviště a sklad, jako dimenze disponibility.</span><span class="sxs-lookup"><span data-stu-id="dd974-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="dd974-106">Dimenze skladu je povinná.</span><span class="sxs-lookup"><span data-stu-id="dd974-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="dd974-107">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="dd974-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="dd974-108">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="dd974-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="dd974-109">Skladová dimenze je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="dd974-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="dd974-110">Dimenze pracoviště a skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="dd974-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="dd974-111">Pro disponibilitu lze nastavit také další dimenze.</span><span class="sxs-lookup"><span data-stu-id="dd974-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="dd974-112">Ty však nejsou ovlivněny funkcí více pracovišť.</span><span class="sxs-lookup"><span data-stu-id="dd974-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="dd974-113">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="dd974-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="dd974-114">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="dd974-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="dd974-115">Sklad je nastaven na možnost **Ruční**.</span><span class="sxs-lookup"><span data-stu-id="dd974-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="dd974-116">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="dd974-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="dd974-117">Na pevné záložce **Hlavní plánování** zkontrolujte pole **Ruční**.</span><span class="sxs-lookup"><span data-stu-id="dd974-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="dd974-118">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="dd974-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="dd974-119">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="dd974-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="dd974-120">Zvolte položku a poté v podokně akcí na kartě **Plán** klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="dd974-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="dd974-121">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="dd974-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="dd974-122">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="dd974-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="dd974-123">Na pevné záložce **Hlavní plánování** zkontrolujte skupinu polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="dd974-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="dd974-124">Výchozí typ objednávky je nastaven na možnost Výroba, Nákupní objednávka nebo Kanban.</span><span class="sxs-lookup"><span data-stu-id="dd974-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="dd974-125">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="dd974-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="dd974-126">Zvolte položku a poté v podokně akcí na kartě **Plán** klikněte na možnost **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="dd974-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="dd974-127">Ve formuláři **Výchozí nastavení objednávky** zkontrolujte pole **Výchozí typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="dd974-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Požadavek na pokrytí pracoviště a skladu, povinný](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a><span data-ttu-id="dd974-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="dd974-129">Additional resources</span></span>

[<span data-ttu-id="dd974-130">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="dd974-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="dd974-131">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="dd974-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="dd974-132">Hlavní plánování pro disponibilitu pracoviště, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="dd974-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="dd974-133">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="dd974-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="dd974-134">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="dd974-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]