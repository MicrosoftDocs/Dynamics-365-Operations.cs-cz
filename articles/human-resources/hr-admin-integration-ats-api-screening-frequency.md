---
title: Frekvence prověřování
description: Toto téma popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 83cb31f3bf9d77bca0aef36fb53d90f7ccb8fff9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068552"
---
# <a name="screening-frequency"></a>Frekvence prověřování


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
