---
title: Stav dokončení
description: Toto téma popisuje sadu možností stavu dokončení pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 67e464262897d89f80bd615156d56cc12a822dd4a0dfa6d5eb206c38ddd61ec5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732866"
---
# <a name="completion-status"></a>Stav dokončení

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje sadu možností stavu dokončení pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmcompletionstatus

Tento výčet poskytuje sadu možností pro hodnoty stavu prověřování kandidátů. 

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 | Nedokončeno | Kandidát dosud neabsolvoval prověřování. |
| 200000001 | Úspěšný | Kandidát úspěšně prošel prověřováním. |
| 200000002 | Chyba | Kandidát selhal při prověřování. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]