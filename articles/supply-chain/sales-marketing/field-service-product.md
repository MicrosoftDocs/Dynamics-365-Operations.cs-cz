---
title: Synchronizace produktů v Supply Chain Management do produktů ve Field Service
description: Tento článek popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860544"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Synchronizace produktů v Supply Chain Management do produktů ve Field Service

[!include[banner](../includes/banner.md)]

Tento článek popisuje šablony a základní úkol, které se používají k synchronizaci produktů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.

Používaná šablona **Produkty Field Service (Supply Chain Management do Field Service)** je založena na šabloně **Produkty (Supply Chain Management do Sales) – Direct** z modulu Prospect to Cash. Další informace naleznete v tématu [Produkty (Supply Chain Management do Sales) – přímé](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Tento článek pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Supply Chain Management do Field Service)** je založena na šabloně **Produkty (Supply Chain Management do Sales) – Direct**.

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

[![Mapování šablony v integraci dat.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]