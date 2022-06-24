---
title: Výsledek integrace uchazeče
description: Tento článek popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 84f0ba9b197866935535a68006cfdb8c18fa3ad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902307"
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
