---
title: Výsledek integrace uchazeče
description: Toto téma popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8bef974abff18d7c07ecd679b7e01b31ea1459c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053892"
---
# <a name="applicant-integration-result"></a>Výsledek integrace uchazeče

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.

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