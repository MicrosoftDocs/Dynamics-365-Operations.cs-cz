---
title: Synchronizace produktů v Supply Chain Management do produktů ve Field Service
description: Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909984"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Synchronizace produktů v Supply Chain Management do produktů ve Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.

Používaná šablona **Produkty Field Service (Supply Chain Management do Field Service)** je založena na šabloně **Produkty (Supply Chain Management do Sales) – Direct** z modulu Prospect to Cash. Další informace naleznete v tématu [Produkty (Supply Chain Management do Sales) – přímé](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Supply Chain Management do Field Service)** je založena na šabloně **Produkty (Supply Chain Management do Sales) – Direct**.

## <a name="templates-and-tasks"></a>Šablony a úkoly

**Název šablony v integraci dat**

- Produkty Field Service (Supply Chain Management do Field Service)

**Název úkolu v projektu integrace dat**

- Produkty – produkty

Šablona **Produkty Field Service (Supply Chain Management do Field Service)** obsahuje jedno mapování, které není obsaženo v **Produktech (Supply Chain Management do Sales) – Direct**. Toto mapování zajišťuje, že povinné poleField Service **typ produktu služba** je správně nastaveno.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Použije se následující mapování hodnoty.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Hodnota **Typ produktu Field Service** se v aplikaci Supply Chain Management v datové entitě **Prodejné vydané produkty** vypočítává takto:

- **Zásoby:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = True
- **NonInventory:** Typ produktu = skupina modelu Produkt a položka, Produkt na skladě = False
- **Service:** Typ produktu = Service

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Produkty Field Service (Supply Chain Management do Field Service): Products - Products

[![Mapování šablony v integraci dat](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]