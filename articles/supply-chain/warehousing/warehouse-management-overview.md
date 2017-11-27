---
title: "Řízení skladu"
description: "Pomocí správy skladu můžete sledovat a automatizovat procesy skladu."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed8baca264e3c277f9c1ff33b20f89f1fd6991c0
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---
# <a name="warehouse-management"></a><span data-ttu-id="21837-103">Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="21837-103">Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="21837-104">Modul Řízení skladu pro aplikaci Dynamics 365 for Finance and Operations, Enterprise Edition umožňuje správu skladových procesů ve výrobních, distribučních a maloobchodních společnostech.</span><span class="sxs-lookup"><span data-stu-id="21837-104">The Warehouse management module for Dynamics 365 for Finance and Operations, Enterprise edition lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="21837-105">Tento modul má celou řadu funkcí pro podporu skladového areálu na optimální úrovni v jakémkoliv čase.</span><span class="sxs-lookup"><span data-stu-id="21837-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="21837-106">Řízení skladu je plně integrováno s ostatními obchodními procesy v aplikaci Finance and Operation, jako je například přeprava, výroba, řízení kvality, nákup, převod, prodej a vrácení.</span><span class="sxs-lookup"><span data-stu-id="21837-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="21837-107">Začínáme</span><span class="sxs-lookup"><span data-stu-id="21837-107">Get started</span></span>
<span data-ttu-id="21837-108">Abyste mohli začít pracovat s modulem Řízení skladu, je třeba dokončit nastavení obecných parametrů skladu pro podporu obchodních procesů vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="21837-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="21837-109">Přejděte na stránku **Parametry řízení skladu** v části **Řízení skladu** > **Nastavení** a nastavte obecné parametry skladu.</span><span class="sxs-lookup"><span data-stu-id="21837-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="21837-110">Je nutné konfigurovat komponenty pro vstupní a výstupní workflowy procesu skladu procesu podle obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="21837-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="21837-111">Nejdůležitější součásti, které je třeba nakonfigurovat, jsou šablony vlny, šablony práce, fondy práce a směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="21837-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="21837-112">Konfigurace skladu</span><span class="sxs-lookup"><span data-stu-id="21837-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="21837-113">Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa</span><span class="sxs-lookup"><span data-stu-id="21837-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="21837-114">Nastavení mobilních zařízení pro práci ve skladu</span><span class="sxs-lookup"><span data-stu-id="21837-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="21837-115">Nastavení směrnice skladového místa pro vyskladnění v rámci nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="21837-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="21837-116">Nastavení šablony práce pro nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="21837-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="21837-117">Procesy řízení skladu</span><span class="sxs-lookup"><span data-stu-id="21837-117">Warehouse management processes</span></span>
- <span data-ttu-id="21837-118">Integrovaná podpora pro zdrojové dokumenty pro prodejní objednávky, vracení, převodní příkazy, výrobní zakázky a kanban</span><span class="sxs-lookup"><span data-stu-id="21837-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="21837-119">Flexibilní podpora workflow příchozího a odchozího materiálu na základě dotazů</span><span class="sxs-lookup"><span data-stu-id="21837-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="21837-120">Úplná integrace s nabídkou výroby a přepravy</span><span class="sxs-lookup"><span data-stu-id="21837-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="21837-121">Úplná kontrola limitů místa uskladnění a objemových metrik místa uskladnění</span><span class="sxs-lookup"><span data-stu-id="21837-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="21837-122">Vlastnosti zásob kontrolované podle stavu zásob</span><span class="sxs-lookup"><span data-stu-id="21837-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="21837-123">Podpora úplných dávek a sériových položek</span><span class="sxs-lookup"><span data-stu-id="21837-123">Full batch and serial item support</span></span>
- <span data-ttu-id="21837-124">Různé funkce příjmu položek</span><span class="sxs-lookup"><span data-stu-id="21837-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="21837-125">Několik strategií výdeje</span><span class="sxs-lookup"><span data-stu-id="21837-125">Multiple picking strategies</span></span>
- <span data-ttu-id="21837-126">Okamžitá podpora pro další generaci čteček čárového kódu</span><span class="sxs-lookup"><span data-stu-id="21837-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="21837-127">Typy palet/kontejneru pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="21837-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="21837-128">Rozšířené možnosti inventury</span><span class="sxs-lookup"><span data-stu-id="21837-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="21837-129">Tisk štítků a směrování popisků s podporou Zebra ZPL</span><span class="sxs-lookup"><span data-stu-id="21837-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="21837-130">Integrace business intelligence do Power BI</span><span class="sxs-lookup"><span data-stu-id="21837-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="21837-131">Ruční a automatický přesun zásob</span><span class="sxs-lookup"><span data-stu-id="21837-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="21837-132">Plně integrované řízení kvality (QMS)</span><span class="sxs-lookup"><span data-stu-id="21837-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="21837-133">Úplná sledovatelnost nakládání pracovníků s materiálem</span><span class="sxs-lookup"><span data-stu-id="21837-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="21837-134">Zpracování výstupní vlny</span><span class="sxs-lookup"><span data-stu-id="21837-134">Outbound wave processing</span></span>
- <span data-ttu-id="21837-135">Ruční balení a podpora automatického vytváření kontejnerů</span><span class="sxs-lookup"><span data-stu-id="21837-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="21837-136">Výdej seskupení</span><span class="sxs-lookup"><span data-stu-id="21837-136">Cluster picking</span></span>
- <span data-ttu-id="21837-137">Jednoduchý cross docking</span><span class="sxs-lookup"><span data-stu-id="21837-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21837-138">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="21837-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="21837-139">Co je nového a na čem se pracuje</span><span class="sxs-lookup"><span data-stu-id="21837-139">What's new and in development</span></span>
<span data-ttu-id="21837-140">Přejděte na [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) a zjistěte, jaké nové funkce se vydávají a jaké se chystají.</span><span class="sxs-lookup"><span data-stu-id="21837-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="21837-141">Blogy</span><span class="sxs-lookup"><span data-stu-id="21837-141">Blogs</span></span>
<span data-ttu-id="21837-142">Názory, novinky a jiné informace o modulu Řízení skladu a jiných řešeních naleznete v [blogu Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="21837-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 


