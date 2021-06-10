---
title: Generovat frekvenci prověřování z
description: Toto téma popisuje stav nastavený pro možnost generování četnosti prověřování Dynamics 365 Human Resources.
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
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054085"
---
# <a name="screening-frequency-generate-from"></a>Generovat frekvenci prověřování z

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]