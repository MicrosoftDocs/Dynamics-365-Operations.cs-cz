---
title: Stav pozice v žádosti o nábor
description: Tento článek popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846392"
---
# <a name="recruiting-request-position-status"></a>Stav pozice v žádosti o nábor


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.

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
