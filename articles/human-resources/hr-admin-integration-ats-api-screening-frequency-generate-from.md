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
ms.openlocfilehash: 7b87bff6925721a20ad9d8bf92e64113d30333defd2d6708b445bcd2126e485a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766235"
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