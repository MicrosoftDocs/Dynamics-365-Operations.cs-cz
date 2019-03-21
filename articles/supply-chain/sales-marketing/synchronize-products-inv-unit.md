---
title: Synchronizace produktů s jednotkou zásob z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2019
ms.locfileid: "836295"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cca6d-103">Synchronizace produktů ve skladové jednotce z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="cca6d-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cca6d-104">Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="cca6d-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cca6d-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="cca6d-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="cca6d-106">Použitá šablona **Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service)** je založena na šabloně **Produkty Field Service (Finance and Operations do Field Service**.</span><span class="sxs-lookup"><span data-stu-id="cca6d-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="cca6d-107">Další informace naleznete v tématu [Produkty Field Service (Finance and Operations do Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="cca6d-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="cca6d-108">V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:</span><span class="sxs-lookup"><span data-stu-id="cca6d-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="cca6d-109">**Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej)**</span><span class="sxs-lookup"><span data-stu-id="cca6d-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="cca6d-110">**Produkty Field Service (Finance and Operations do Field Service)**</span><span class="sxs-lookup"><span data-stu-id="cca6d-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="cca6d-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="cca6d-111">Templates and tasks</span></span>

<span data-ttu-id="cca6d-112">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="cca6d-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cca6d-113">Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej)</span><span class="sxs-lookup"><span data-stu-id="cca6d-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="cca6d-114">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="cca6d-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cca6d-115">Produkty</span><span class="sxs-lookup"><span data-stu-id="cca6d-115">Products</span></span>

<span data-ttu-id="cca6d-116">Šablona **Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service)** šablona obsahuje jedno mapování, které není zahrnuto v šabloně **Produkty Field Service (Finance and Operations do Field Service**.</span><span class="sxs-lookup"><span data-stu-id="cca6d-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="cca6d-117">Toto mapování zajišťuje, že je zahrnuta skladová jednotka potřebná pro synchronizaci úrovně zásob.</span><span class="sxs-lookup"><span data-stu-id="cca6d-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cca6d-118">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="cca6d-118">Template mapping in Data integration</span></span>

<span data-ttu-id="cca6d-119">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="cca6d-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="cca6d-120">Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service): produkty</span><span class="sxs-lookup"><span data-stu-id="cca6d-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="cca6d-121">[![Mapování šablony v integraci dat](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="cca6d-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
