---
title: Frekvence prověřování
description: Tento článek popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.
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
ms.openlocfilehash: 506de0b9208d146e2a02bf1019bbc4056ba862c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868181"
---
# <a name="screening-frequency"></a>Frekvence prověřování


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.

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
