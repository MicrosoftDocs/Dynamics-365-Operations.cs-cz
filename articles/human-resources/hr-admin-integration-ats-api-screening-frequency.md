---
title: Frekvence prověřování
description: Toto téma popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ad81fba659a5bb22ab5131519036e156a43a486
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464543"
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