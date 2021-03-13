---
title: Stav pozice v žádosti o nábor
description: Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126043"
---
# <a name="recruiting-request-position-status"></a>Stav pozice v žádosti o nábor

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
