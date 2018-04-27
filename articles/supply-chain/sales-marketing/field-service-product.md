---
title: "Synchronizace produktů v aplikaci Finance and Operations do produktů ve službě Field Service"
description: "Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: cs-cz
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="f85dd-103">Synchronizace produktů v aplikaci Finance and Operations do produktů ve službě Field Service</span><span class="sxs-lookup"><span data-stu-id="f85dd-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f85dd-104">Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f85dd-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f85dd-105">Používaná šablona **Produkty Field Service (Fin and Ops do Field Service)** je založena na šabloně **Produkty (Fin a Ops do Sales) – Direct** z modulu Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="f85dd-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="f85dd-106">Další informace naleznete v tématu [Produkty (Fin and Ops na Sales) – přímé](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="f85dd-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="f85dd-107">Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Fin and Ops do Field Service)** je založena na šabloně **Produkty (Fin a Ops do Sales) – Direct**.</span><span class="sxs-lookup"><span data-stu-id="f85dd-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f85dd-108">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="f85dd-108">Templates and tasks</span></span>

<span data-ttu-id="f85dd-109">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="f85dd-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="f85dd-110">Produkty Field Service (Fin and Ops do Field Service)</span><span class="sxs-lookup"><span data-stu-id="f85dd-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="f85dd-111">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="f85dd-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="f85dd-112">Produkty – produkty</span><span class="sxs-lookup"><span data-stu-id="f85dd-112">Products - Products</span></span>

<span data-ttu-id="f85dd-113">Šablona **Produkty Field Service (Fin and Ops do Field Service)** zahrnuje jedno mapování, které není zahrnuto do šablony **Produkty (Fin a Ops do Sales) – Direct**.</span><span class="sxs-lookup"><span data-stu-id="f85dd-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="f85dd-114">Toto mapování zajišťuje, že povinné poleField Service **typ produktu služba** je správně nastaveno.</span><span class="sxs-lookup"><span data-stu-id="f85dd-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="f85dd-115">Použije se následující mapování hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f85dd-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="f85dd-116">Hodnota **Typ produktu Field Service** se v aplikaci Finance and Operations v datové entitě **Prodejné vydané produkty** vypočítává takto:</span><span class="sxs-lookup"><span data-stu-id="f85dd-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="f85dd-117">**Zásoby:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = True</span><span class="sxs-lookup"><span data-stu-id="f85dd-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="f85dd-118">**NonInventory:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = False</span><span class="sxs-lookup"><span data-stu-id="f85dd-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="f85dd-119">**Service:** Typ produktu = Service</span><span class="sxs-lookup"><span data-stu-id="f85dd-119">**Service:** Product type = Service</span></span>

