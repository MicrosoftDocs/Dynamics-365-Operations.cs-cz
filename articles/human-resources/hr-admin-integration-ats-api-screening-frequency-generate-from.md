---
title: Generovat frekvenci prověřování z
description: Toto téma popisuje stav nastavený pro možnost generování četnosti prověřování Dynamics 365 Human Resources.
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
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126139"
---
# <a name="screening-frequency-generate-from"></a>Generovat frekvenci prověřování z

Toto téma popisuje stav nastavený pro možnost generování četnosti prověřování Dynamics 365 Human Resources.

Fyzický název: mshr_hcmfrequencygeneratefrom

Tento výčet poskytuje sadu možností hodnot pro určení data zahájení výpočtu pro další požadovaný screening.

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 Nevybráno | Nebyla vybrána žádná hodnota. |
| 200000001 Datum dokončení | Výpočet se provádí od posledního dokončeného data prověření. |
| 200000002 Datum je povinné | Výpočet se provádí od posledního požadovaného data prověření. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
