---
title: Frekvence prověřování
description: Toto téma popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba1fba598bca088e67d8cb2865d1ea9baa97f19e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801256"
---
# <a name="screening-frequency"></a>Frekvence prověřování

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.

Fyzický název: mshr_hcmfrequencyunit

Tento výčet poskytuje sadu možností pro hodnoty frekvence prověřování. 

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 Pouze jednorázově | Screening je vyžadován pouze jednou. |
| 200000001 denně | Četnost prověřování se počítá ve dnech. |
| 200000002 týdně | Četnost prověřování se počítá v týdnech. |
| 200000003 měsíčně | Četnost prověřování se počítá v měsících. |
| 200000004 ročně | Četnost prověřování se počítá v letech. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]