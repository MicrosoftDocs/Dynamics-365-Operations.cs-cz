---
title: Integrované sklady a pracoviště
description: Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770974"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="43e2f-103">Integrované sklady a pracoviště</span><span class="sxs-lookup"><span data-stu-id="43e2f-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43e2f-104">Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="43e2f-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="43e2f-105">Provozní pracoviště a sklady jsou obecnými koncepty v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="43e2f-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="43e2f-106">Používají se k modelování dodavatelského řetězce vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="43e2f-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="43e2f-107">Šablony</span><span class="sxs-lookup"><span data-stu-id="43e2f-107">Templates</span></span>

<span data-ttu-id="43e2f-108">Při integraci s aplikací Common Data Service jsou tyto koncepcy a všechny jeich souvisejíc informace k dispozic v Common Data Service pomocí datových entit pracovišť a skladů v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="43e2f-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="43e2f-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43e2f-109">Finance and Operations apps</span></span> | <span data-ttu-id="43e2f-110">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="43e2f-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="43e2f-111">Popis</span><span class="sxs-lookup"><span data-stu-id="43e2f-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="43e2f-112">Weby</span><span class="sxs-lookup"><span data-stu-id="43e2f-112">Sites</span></span> | <span data-ttu-id="43e2f-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="43e2f-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="43e2f-114">Sklady</span><span class="sxs-lookup"><span data-stu-id="43e2f-114">Warehouses</span></span> | <span data-ttu-id="43e2f-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="43e2f-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

