---
title: Hlavní plánování pro disponibilitu pracoviště, sklad není povinný
description: Toto téma popisuje, jak je plánována položka, která pro pokrytí nastavenou dimenzí pracoviště.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40ea467b9dcac20e163f8b6e6f91b238d40278f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833514"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="d486e-103">Hlavní plánování pro disponibilitu pracoviště, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="d486e-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d486e-104">Toto téma popisuje, jak je plánována položka, která má pro pokrytí nastavenou dimenzi pracoviště.</span><span class="sxs-lookup"><span data-stu-id="d486e-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="d486e-105">Pro tento scénář hlavního plánování platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d486e-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d486e-106">Dimenze pracoviště je nastavena jako povinná a musí být zadána v transakci poptávky.</span><span class="sxs-lookup"><span data-stu-id="d486e-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="d486e-107">Dimenze skladu není povinná.</span><span class="sxs-lookup"><span data-stu-id="d486e-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="d486e-108">Sklad může být znám, ale při výpočtu během hlavního plánování se nepoužije.</span><span class="sxs-lookup"><span data-stu-id="d486e-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="d486e-109">Dimenze pracovišť je nastavená pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="d486e-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="d486e-110">Skladová dimenze není nastavena pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="d486e-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="d486e-111">Nabídka a poptávka se tedy vyhodnocuje souhrnně podle pracovišť a případně podle dalších dimenzí nastavených pro plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="d486e-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="d486e-112">Následující obrázek ilustruje postup hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="d486e-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d486e-113">V obrázku jsou odkazy na následující parametry (v popisu je informace, kde je najdete):</span><span class="sxs-lookup"><span data-stu-id="d486e-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d486e-114">Je definovaná disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="d486e-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="d486e-115">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="d486e-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d486e-116">Vyberte položku a poté klikněte na volbu **Plán &gt; Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="d486e-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="d486e-117">Pro sklad jsou definovány vztahy doplnění.</span><span class="sxs-lookup"><span data-stu-id="d486e-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d486e-118">Klikněte postupně na možnosti **Řízení zásob &gt; Nastavení &gt; Rozdělení zásob &gt; Sklady**.</span><span class="sxs-lookup"><span data-stu-id="d486e-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d486e-119">Na kartě **Hlavní plánování** se podívejte do skupiny polí **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="d486e-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d486e-120">Výchozí typ objednávky je nastaven na výrobu, nákupní objednávky nebo kanban.</span><span class="sxs-lookup"><span data-stu-id="d486e-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="d486e-121">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty&gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="d486e-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d486e-122">Vyberte položku a poté klikněte na volbu **Plán &gt; Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d486e-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="d486e-123">Ve formuláři **nastavení výchozí objednávky**, viz pole **typ výchozí objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d486e-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Požadavek na disponibilitu skladu pracoviště není povinný](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="d486e-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d486e-125">Additional resources</span></span>
--------

[<span data-ttu-id="d486e-126">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="d486e-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d486e-127">Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný</span><span class="sxs-lookup"><span data-stu-id="d486e-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d486e-128">Hlavní plánování pro disponibilitu pracoviště, povinný sklad</span><span class="sxs-lookup"><span data-stu-id="d486e-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d486e-129">Hlavní plánování pro disponibilitu pracoviště, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="d486e-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d486e-130">Určení verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="d486e-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]