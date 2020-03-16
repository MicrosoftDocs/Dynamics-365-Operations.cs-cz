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
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Synchronizace produktů ve skladové jednotce z aplikace Supply Chain Management do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.

[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Použitá šablona **Produkty Field Service s jednotkou zásob (Supply Chain Management Field Service)** je založena na šabloně **Produkty Field Service ( Supply Chain Management do Field Service)**. Více informací naleznete v části [Synchronizace produktů ve službě Supply Chain Management s produkty v aplikaci Field Service](field-service-product.md).

V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami: 
- **Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)**
- **Produkty Field Service (Supply Chain Management do Field Service)** 

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat:**

- Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)

**Název úkolu v projektu integrace dat:**

- Produkty

Použitá šablona **Produkty Field Service s jednotkou zásob (Supply Chain Management Field Service)** zahrnuje jedno mapování, které není zahrnuto v šabloně **Produkty Field Service ( Supply Chain Management do Field Service)**. Toto mapování zajišťuje, že je zahrnuta skladová jednotka potřebná pro synchronizaci úrovně zásob.

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Produkty Field Service s jednotkou zásob (Supply Chain Management do Field Service): Products

[![Mapování šablony v integraci dat](./media/FSProduct1.png)](./media/FSProduct1.png)
