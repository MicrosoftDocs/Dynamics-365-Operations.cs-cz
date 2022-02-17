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
ms.openlocfilehash: da91084d30873b79033d789beab829da9fbdb010
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065539"
---
# <a name="completion-status"></a>Stav dokončení


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
