---
title: "Synchronizace produktů s jednotkou zásob z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci produktů s jednotkou zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cc40a-103">Synchronizace produktů s jednotkou zásob z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="cc40a-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cc40a-104">Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci produktů s jednotkou zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="cc40a-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cc40a-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="cc40a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="cc40a-106">Používaná šablona **Produkty Field Service (z aplikace Finance and Operations do služby Field Service)** je založena na šabloně **Produkty (z aplikace Finance and Operations do Sales) – Direct** z modulu Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="cc40a-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="cc40a-107">Další informace naleznete v tématu [Produkty (Finance and Operations do Sales) – přímé](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="cc40a-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="cc40a-108">Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Finance and Operations do Field Service)** a je založeno na šabloně **Field Service (Finance and Operations do Sales) – přímé**.</span><span class="sxs-lookup"><span data-stu-id="cc40a-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cc40a-109">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="cc40a-109">Templates and tasks</span></span>

<span data-ttu-id="cc40a-110">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="cc40a-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cc40a-111">Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej)</span><span class="sxs-lookup"><span data-stu-id="cc40a-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="cc40a-112">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="cc40a-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cc40a-113">Produkty</span><span class="sxs-lookup"><span data-stu-id="cc40a-113">Products</span></span>

<span data-ttu-id="cc40a-114">Šablona **Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service)** šablona obsahuje jedno mapování, které není zahrnuto v šabloně **Produkty Field Service (Finance and Operations do Field Service**.</span><span class="sxs-lookup"><span data-stu-id="cc40a-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="cc40a-115">Toto mapování zajišťuje, že je zahrnuta skladová jednotka potřebná pro synchronizaci úrovně zásob.</span><span class="sxs-lookup"><span data-stu-id="cc40a-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cc40a-116">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="cc40a-116">Template mapping in Data integration</span></span>

<span data-ttu-id="cc40a-117">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="cc40a-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="cc40a-118">Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service): produkty</span><span class="sxs-lookup"><span data-stu-id="cc40a-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="cc40a-119">[![Mapování šablony v integraci dat](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="cc40a-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>

