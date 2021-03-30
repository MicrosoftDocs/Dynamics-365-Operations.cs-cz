---
title: Synchronizace produktů ve skladové jednotce z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 87daaa3d2b516581e9925fe6b769683942893ff6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206912"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="57d60-103">Synchronizace produktů ve skladové jednotce z aplikace Supply Chain Management do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="57d60-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="57d60-104">Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="57d60-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="57d60-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="57d60-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="57d60-106">Použitá šablona **Produkty Field Service s jednotkou zásob (Supply Chain Management Field Service)** je založena na šabloně **Produkty Field Service ( Supply Chain Management do Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="57d60-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="57d60-107">Více informací naleznete v části [Synchronizace produktů ve službě Supply Chain Management s produkty v aplikaci Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="57d60-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="57d60-108">V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:</span><span class="sxs-lookup"><span data-stu-id="57d60-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="57d60-109">**Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)**</span><span class="sxs-lookup"><span data-stu-id="57d60-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="57d60-110">**Produkty Field Service (Supply Chain Management do Field Service)**</span><span class="sxs-lookup"><span data-stu-id="57d60-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="57d60-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="57d60-111">Templates and tasks</span></span>

<span data-ttu-id="57d60-112">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="57d60-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="57d60-113">Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)</span><span class="sxs-lookup"><span data-stu-id="57d60-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="57d60-114">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="57d60-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="57d60-115">Produkty</span><span class="sxs-lookup"><span data-stu-id="57d60-115">Products</span></span>

<span data-ttu-id="57d60-116">Použitá šablona **Produkty Field Service s jednotkou zásob (Supply Chain Management Field Service)** zahrnuje jedno mapování, které není zahrnuto v šabloně **Produkty Field Service (Supply Chain Management to Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="57d60-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="57d60-117">Toto mapování zajišťuje, že je zahrnuta skladová jednotka potřebná pro synchronizaci úrovně zásob.</span><span class="sxs-lookup"><span data-stu-id="57d60-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="57d60-118">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="57d60-118">Template mapping in Data integration</span></span>

<span data-ttu-id="57d60-119">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="57d60-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="57d60-120">Produkty Field Service s jednotkou zásob (Supply Chain Management do Field Service): Products</span><span class="sxs-lookup"><span data-stu-id="57d60-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="57d60-121">[![Mapování šablony v integraci dat](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="57d60-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]