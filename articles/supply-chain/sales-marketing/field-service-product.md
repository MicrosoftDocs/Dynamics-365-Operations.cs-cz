---
title: Synchronizace produktů v aplikaci Finance and Operations do produktů ve službě Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 06d7ff272ecb79abded3c3d3ade1f6bc0ef1f095
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742348"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="56e32-103">Synchronizace produktů v aplikaci Finance and Operations do produktů ve službě Field Service</span><span class="sxs-lookup"><span data-stu-id="56e32-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="56e32-104">Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="56e32-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="56e32-105">Používaná šablona **Produkty Field Service (Fin and Ops do Field Service)** je založena na šabloně **Produkty (Fin a Ops do Sales) – Direct** z modulu Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="56e32-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="56e32-106">Další informace naleznete v tématu [Produkty (Fin and Ops na Sales) – přímé](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="56e32-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="56e32-107">Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Fin and Ops do Field Service)** je založena na šabloně **Produkty (Fin a Ops do Sales) – Direct**.</span><span class="sxs-lookup"><span data-stu-id="56e32-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="56e32-108">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="56e32-108">Templates and tasks</span></span>

<span data-ttu-id="56e32-109">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="56e32-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="56e32-110">Produkty Field Service (Fin and Ops do Field Service)</span><span class="sxs-lookup"><span data-stu-id="56e32-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="56e32-111">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="56e32-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="56e32-112">Produkty – produkty</span><span class="sxs-lookup"><span data-stu-id="56e32-112">Products - Products</span></span>

<span data-ttu-id="56e32-113">Šablona **Produkty Field Service (Fin and Ops do Field Service)** zahrnuje jedno mapování, které není zahrnuto do šablony **Produkty (Fin a Ops do Sales) – Direct**.</span><span class="sxs-lookup"><span data-stu-id="56e32-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="56e32-114">Toto mapování zajišťuje, že povinné poleField Service **typ produktu služba** je správně nastaveno.</span><span class="sxs-lookup"><span data-stu-id="56e32-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="56e32-115">Použije se následující mapování hodnoty.</span><span class="sxs-lookup"><span data-stu-id="56e32-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="56e32-116">Hodnota **Typ produktu Field Service** se v aplikaci Finance and Operations v datové entitě **Prodejné vydané produkty** vypočítává takto:</span><span class="sxs-lookup"><span data-stu-id="56e32-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="56e32-117">**Zásoby:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = True</span><span class="sxs-lookup"><span data-stu-id="56e32-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="56e32-118">**NonInventory:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = False</span><span class="sxs-lookup"><span data-stu-id="56e32-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="56e32-119">**Service:** Typ produktu = Service</span><span class="sxs-lookup"><span data-stu-id="56e32-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="56e32-120">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="56e32-120">Template mapping in Data integration</span></span>

<span data-ttu-id="56e32-121">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="56e32-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="56e32-122">Produkty Field Service (Fin and Ops do Field Service) : Produkty - Produkty</span><span class="sxs-lookup"><span data-stu-id="56e32-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="56e32-123">[![Mapování šablony v integraci dat](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="56e32-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
