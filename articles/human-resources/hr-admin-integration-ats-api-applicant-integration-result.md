---
title: Výsledek integrace uchazeče
description: Toto téma popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 157864cd0eee879013724615ce31306c99c5aa68
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125802"
---
# <a name="applicant-integration-result"></a>Výsledek integrace uchazeče

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
