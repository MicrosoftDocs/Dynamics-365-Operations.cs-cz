---
title: Synchronizace produktů ve skladové jednotce z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 741b823d6cc5dbd23cda4f07e463f28d6bbe77d6
ms.sourcegitcommit: a2f9dce06322dada6b5f1c82051ef2359f8c0f12
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/24/2020
ms.locfileid: "3081857"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="e1cb3-103">Synchronizace produktů ve skladové jednotce z aplikace Supply Chain Management do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="e1cb3-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e1cb3-104">Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="e1cb3-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="e1cb3-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="e1cb3-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="e1cb3-106">Použitá šablona **Produkty Field Service s jednotkou zásob (Supply Chain Management Field Service)** je založena na šabloně **Produkty Field Service ( Supply Chain Management do Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="e1cb3-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="e1cb3-107">Více informací naleznete v části [Synchronizace produktů ve službě Supply Chain Management s produkty v aplikaci Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="e1cb3-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="e1cb3-108">V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:</span><span class="sxs-lookup"><span data-stu-id="e1cb3-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="e1cb3-109">**Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)**</span><span class="sxs-lookup"><span data-stu-id="e1cb3-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="e1cb3-110">**Produkty Field Service (Supply Chain Management do Field Service)**</span><span class="sxs-lookup"><span data-stu-id="e1cb3-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="e1cb3-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="e1cb3-111">Templates and tasks</span></span>

<span data-ttu-id="e1cb3-112">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="e1cb3-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="e1cb3-113">Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)</span><span class="sxs-lookup"><span data-stu-id="e1cb3-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="e1cb3-114">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="e1cb3-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="e1cb3-115">Produkty</span><span class="sxs-lookup"><span data-stu-id="e1cb3-115">Products</span></span>

<span data-ttu-id="e1cb3-116">Použitá šablona **Produkty Field Service s jednotkou zásob (Supply Chain Management Field Service)** zahrnuje jedno mapování, které není zahrnuto v šabloně **Produkty Field Service ( Supply Chain Management do Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="e1cb3-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="e1cb3-117">Toto mapování zajišťuje, že je zahrnuta skladová jednotka potřebná pro synchronizaci úrovně zásob.</span><span class="sxs-lookup"><span data-stu-id="e1cb3-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e1cb3-118">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="e1cb3-118">Template mapping in Data integration</span></span>

<span data-ttu-id="e1cb3-119">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="e1cb3-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="e1cb3-120">Produkty Field Service s jednotkou zásob (Supply Chain Management do Field Service): Products</span><span class="sxs-lookup"><span data-stu-id="e1cb3-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="e1cb3-121">[![Mapování šablony v integraci dat](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="e1cb3-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
