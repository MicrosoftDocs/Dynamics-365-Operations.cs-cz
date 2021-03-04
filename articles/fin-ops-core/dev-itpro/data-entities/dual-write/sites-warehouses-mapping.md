---
title: Integrované sklady a pracoviště
description: Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Dataverse.
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
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679313"
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