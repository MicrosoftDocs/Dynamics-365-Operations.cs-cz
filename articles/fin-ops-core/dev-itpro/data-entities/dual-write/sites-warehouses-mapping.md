---
title: Integrované sklady a pracoviště
description: Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750659"
---
# <a name="integrated-sites-and-warehouses"></a>Integrované sklady a pracoviště

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Dataverse. Provozní pracoviště a sklady jsou obecnými koncepty v aplikaci Supply Chain Management. Používají se k modelování dodavatelského řetězce vaší společnosti.

## <a name="templates"></a>Šablony

Při integraci s aplikací Dataverse jsou tyto koncepcy a všechny jeich souvisejíc informace k dispozic v Dataverse pomocí datových tabulek pracovišť a skladů v následující tabulce.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365 | popis
--------------------------|---------------------------|---
Weby | msdyn_operationalsites | 
Sklady | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]