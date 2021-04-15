---
title: Stav pozice v žádosti o nábor
description: Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789724"
---
# <a name="recruiting-request-position-status"></a>Stav pozice v žádosti o nábor

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.

Fyzický název: mshr_hcmrecruitingrequestpositionstatus

Tento výčet poskytuje sadu možností pro stavové hodnoty každé pozice a požadavek na nábor v entitě RecruitingRequestPosition.

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 | Otevřená | Pozice v požadavku na nábor je pro nábor otevřená. To neznamená, že pro pozici není aktuálně aktivní přiřazení pozice. V době náboru může být na pozici zaměstnanec. Označuje pouze to, že pozice je k dispozici pro nábor v kontextu požadavku na nábor. |
| 200000001 | Obsazená | Pro zařazení na pozici byl vybrán pracovník. |
| 200000002 | Zrušená | Žádost o nábor na tuto pozici byla zrušena. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]