---
title: Integrované sklady a pracoviště
description: Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997617"
---
# <a name="integrated-sites-and-warehouses"></a>Integrované sklady a pracoviště

[!include [banner](../../includes/banner.md)]



Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service. Provozní pracoviště a sklady jsou obecnými koncepty v aplikaci Supply Chain Management. Používají se k modelování dodavatelského řetězce vaší společnosti.

## <a name="templates"></a>Šablony

Při integraci s aplikací Common Data Service jsou tyto koncepcy a všechny jeich souvisejíc informace k dispozic v Common Data Service pomocí datových entit pracovišť a skladů v následující tabulce.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365 | Popis
--------------------------|---------------------------|---
Weby | msdyn_operationalsites | 
Sklady | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

