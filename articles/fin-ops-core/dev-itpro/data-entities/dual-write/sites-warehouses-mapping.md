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
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173055"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="a7cb9-103">Integrované sklady a pracoviště</span><span class="sxs-lookup"><span data-stu-id="a7cb9-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a7cb9-104">Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a7cb9-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="a7cb9-105">Provozní pracoviště a sklady jsou obecnými koncepty v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a7cb9-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="a7cb9-106">Používají se k modelování dodavatelského řetězce vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="a7cb9-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="a7cb9-107">Šablony</span><span class="sxs-lookup"><span data-stu-id="a7cb9-107">Templates</span></span>

<span data-ttu-id="a7cb9-108">Při integraci s aplikací Common Data Service jsou tyto koncepcy a všechny jeich souvisejíc informace k dispozic v Common Data Service pomocí datových entit pracovišť a skladů v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="a7cb9-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="a7cb9-109">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a7cb9-109">Finance and Operations apps</span></span> | <span data-ttu-id="a7cb9-110">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a7cb9-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a7cb9-111">Popis</span><span class="sxs-lookup"><span data-stu-id="a7cb9-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="a7cb9-112">Weby</span><span class="sxs-lookup"><span data-stu-id="a7cb9-112">Sites</span></span> | <span data-ttu-id="a7cb9-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="a7cb9-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="a7cb9-114">Sklady</span><span class="sxs-lookup"><span data-stu-id="a7cb9-114">Warehouses</span></span> | <span data-ttu-id="a7cb9-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="a7cb9-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

