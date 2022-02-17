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
ms.openlocfilehash: 27c6c62f3ac312ee502df969f25f1b16761cba03
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067797"
---
# <a name="screening-frequency-generate-from"></a>Generovat frekvenci prověřování z


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
