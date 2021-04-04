---
title: Synchronizace produktů v Supply Chain Management do produktů ve Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d3dc21a39c9866d09e500e2f14ff810bac7d57fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261038"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="37b7d-103">Synchronizace produktů v Supply Chain Management do produktů ve Field Service</span><span class="sxs-lookup"><span data-stu-id="37b7d-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37b7d-104">Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="37b7d-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="37b7d-105">Používaná šablona **Produkty Field Service (Supply Chain Management do Field Service)** je založena na šabloně **Produkty (Supply Chain Management do Sales) – Direct** z modulu Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="37b7d-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="37b7d-106">Další informace naleznete v tématu [Produkty (Supply Chain Management do Sales) – přímé](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="37b7d-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="37b7d-107">Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Supply Chain Management do Field Service)** je založena na šabloně **Produkty (Supply Chain Management do Sales) – Direct**.</span><span class="sxs-lookup"><span data-stu-id="37b7d-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="37b7d-108">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="37b7d-108">Templates and tasks</span></span>

<span data-ttu-id="37b7d-109">**Název šablony v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="37b7d-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="37b7d-110">Produkty Field Service (Supply Chain Management do Field Service)</span><span class="sxs-lookup"><span data-stu-id="37b7d-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="37b7d-111">**Název úkolu v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="37b7d-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="37b7d-112">Produkty – produkty</span><span class="sxs-lookup"><span data-stu-id="37b7d-112">Products - Products</span></span>

<span data-ttu-id="37b7d-113">Šablona **Produkty Field Service (Supply Chain Management do Field Service)** obsahuje jedno mapování, které není obsaženo v **Produktech (Supply Chain Management do Sales) – Direct**.</span><span class="sxs-lookup"><span data-stu-id="37b7d-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="37b7d-114">Toto mapování zajišťuje, že povinné poleField Service **typ produktu služba** je správně nastaveno.</span><span class="sxs-lookup"><span data-stu-id="37b7d-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="37b7d-115">Použije se následující mapování hodnoty.</span><span class="sxs-lookup"><span data-stu-id="37b7d-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="37b7d-116">Hodnota **Typ produktu Field Service** se v aplikaci Supply Chain Management v datové entitě **Prodejné vydané produkty** vypočítává takto:</span><span class="sxs-lookup"><span data-stu-id="37b7d-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="37b7d-117">**Zásoby:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = True</span><span class="sxs-lookup"><span data-stu-id="37b7d-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="37b7d-118">**NonInventory:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = False</span><span class="sxs-lookup"><span data-stu-id="37b7d-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="37b7d-119">**Service:** Typ produktu = Service</span><span class="sxs-lookup"><span data-stu-id="37b7d-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="37b7d-120">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="37b7d-120">Template mapping in Data integration</span></span>

<span data-ttu-id="37b7d-121">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="37b7d-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="37b7d-122">Produkty Field Service (Supply Chain Management do Field Service): Products - Products</span><span class="sxs-lookup"><span data-stu-id="37b7d-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="37b7d-123">[![Mapování šablony v integraci dat](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="37b7d-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]