---
title: Integrované sklady a pracoviště
description: Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750659"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="d1ed4-103">Integrované sklady a pracoviště</span><span class="sxs-lookup"><span data-stu-id="d1ed4-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="d1ed4-104">Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="d1ed4-105">Provozní pracoviště a sklady jsou obecnými koncepty v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="d1ed4-106">Používají se k modelování dodavatelského řetězce vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="d1ed4-107">Šablony</span><span class="sxs-lookup"><span data-stu-id="d1ed4-107">Templates</span></span>

<span data-ttu-id="d1ed4-108">Při integraci s aplikací Dataverse jsou tyto koncepcy a všechny jeich souvisejíc informace k dispozic v Dataverse pomocí datových tabulek pracovišť a skladů v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="d1ed4-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="d1ed4-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1ed4-109">Finance and Operations apps</span></span> | <span data-ttu-id="d1ed4-110">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d1ed4-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d1ed4-111">popis</span><span class="sxs-lookup"><span data-stu-id="d1ed4-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="d1ed4-112">Weby</span><span class="sxs-lookup"><span data-stu-id="d1ed4-112">Sites</span></span> | <span data-ttu-id="d1ed4-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="d1ed4-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="d1ed4-114">Sklady</span><span class="sxs-lookup"><span data-stu-id="d1ed4-114">Warehouses</span></span> | <span data-ttu-id="d1ed4-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="d1ed4-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]