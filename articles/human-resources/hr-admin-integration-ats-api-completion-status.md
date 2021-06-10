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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055357"
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