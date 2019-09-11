---
title: Přehled hlavního plánování a funkce více pracovišť
description: Hlavní plánování bere v úvahu nastavení dimenzí zásob pracoviště a skladu.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865393"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="cc937-103">Přehled hlavního plánování a funkce více pracovišť</span><span class="sxs-lookup"><span data-stu-id="cc937-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc937-104">Hlavní plánování bere v úvahu nastavení dimenzí zásob pracoviště a skladu.</span><span class="sxs-lookup"><span data-stu-id="cc937-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="cc937-105">Dimenze pracoviště je povinná a dimenzi skladu lze nastavit jako povinnou.</span><span class="sxs-lookup"><span data-stu-id="cc937-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="cc937-106">Když je dimenze povinná, je nutné zadat její hodnotu ve všech skladových transakcích.</span><span class="sxs-lookup"><span data-stu-id="cc937-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="cc937-107">Proto jsou při hlavním plánování známy pracoviště a sklad pro počáteční požadavek.</span><span class="sxs-lookup"><span data-stu-id="cc937-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="cc937-108">Dimenze pracoviště je také konzistentní, aby se při rozpadu poptávky nižší úrovně nezměnila hodnota pracoviště.</span><span class="sxs-lookup"><span data-stu-id="cc937-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="cc937-109">Pokud není sklad nastavený jako povinný, je možné jej odvodit z počátečního požadavku.</span><span class="sxs-lookup"><span data-stu-id="cc937-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="cc937-110">Plánovací modul musí na základě nastavení definovaných pro položku, jednotlivé sklady a podrobností řádku objednávky určit, který sklad se má použít.</span><span class="sxs-lookup"><span data-stu-id="cc937-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="cc937-111">Následující témata popisují, jak plánovací modul určuje používaný sklad při definici různých nastavení.</span><span class="sxs-lookup"><span data-stu-id="cc937-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="cc937-112">Hlavní plánování – disponibilita pracoviště a skladu, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="cc937-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="cc937-113">Hlavní plánování – disponibilita pracoviště, sklad povinný</span><span class="sxs-lookup"><span data-stu-id="cc937-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="cc937-114">Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="cc937-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="cc937-115">Hlavní plánování – disponibilita pracoviště, sklad není povinný</span><span class="sxs-lookup"><span data-stu-id="cc937-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="cc937-116">Hlavní plánování – jak se určuje verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="cc937-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



