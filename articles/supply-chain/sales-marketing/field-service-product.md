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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Synchronizace produktů v aplikaci Finance and Operations do produktů ve službě Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci produktů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.

Používaná šablona **Produkty Field Service (Fin and Ops do Field Service)** je založena na šabloně **Produkty (Fin a Ops do Sales) – Direct** z modulu Prospect to Cash. Další informace naleznete v tématu [Produkty (Fin and Ops na Sales) – přímé](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Fin and Ops do Field Service)** je založena na šabloně **Produkty (Fin a Ops do Sales) – Direct**.

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat:**

- Produkty Field Service (Fin and Ops do Field Service)

**Název úkolu v projektu integrace dat:**

- Produkty – produkty

Šablona **Produkty Field Service (Fin and Ops do Field Service)** zahrnuje jedno mapování, které není zahrnuto do šablony **Produkty (Fin a Ops do Sales) – Direct**. Toto mapování zajišťuje, že povinné poleField Service **typ produktu služba** je správně nastaveno.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Použije se následující mapování hodnoty.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Hodnota **Typ produktu Field Service** se v aplikaci Finance and Operations v datové entitě **Prodejné vydané produkty** vypočítává takto:

- **Zásoby:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = True
- **NonInventory:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = False
- **Service:** Typ produktu = Service

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Produkty Field Service (Fin and Ops do Field Service) : Produkty - Produkty

[![Mapování šablony v integraci dat](./media/FSProduct.png)](./media/FSProduct.png)
