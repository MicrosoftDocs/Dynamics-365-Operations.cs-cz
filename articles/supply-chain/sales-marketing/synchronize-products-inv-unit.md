---
title: Synchronizace produktů s jednotkou zásob z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "359237"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Synchronizace produktů ve skladové jednotce z aplikace Finance and Operations do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů se skladovou jednotkou z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Používaná šablona **Produkty Field Service (z aplikace Finance and Operations do služby Field Service)** je založena na šabloně **Produkty (z aplikace Finance and Operations do Sales) – Direct** z modulu Prospect to Cash. Další informace naleznete v tématu [Produkty (Finance and Operations do Sales) – přímé](products-template-mapping-direct.md).

Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Finance and Operations do Field Service)** a je založeno na šabloně **Field Service (Finance and Operations do Sales) – přímé**.

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat:**

- Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej)

**Název úkolu v projektu integrace dat:**

- Produkty

Šablona **Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service)** šablona obsahuje jedno mapování, které není zahrnuto v šabloně **Produkty Field Service (Finance and Operations do Field Service**. Toto mapování zajišťuje, že je zahrnuta skladová jednotka potřebná pro synchronizaci úrovně zásob.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Produkty Field Service s jednotkou zásob (Finance and Operations do Field Service): produkty

[![Mapování šablony v integraci dat](./media/FSProduct1.png)](./media/FSProduct1.png)
