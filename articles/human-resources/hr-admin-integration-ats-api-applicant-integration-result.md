---
title: Výsledek integrace uchazeče
description: Tento článek popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702221"
---
# <a name="applicant-integration-result"></a>Výsledek integrace uchazeče


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmapplicantintegrationresult

Tento výčet poskytuje stav záznamu kandidáta.

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 | Nezpracováno | Kandidát stále přichází v úvahu. |
| 200000001 | Zařazeno | Kandidát byl přijat. |
| 200000002 | Nepřijat/a | Bylo rozhodnuto nezaměstnat kandidáta. |
| 200000003 | Zamítnuto | Kandidát byl vyloučen z úvahy. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
