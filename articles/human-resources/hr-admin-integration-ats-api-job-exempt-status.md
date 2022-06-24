---
title: Stav práce z hlediska přesčasů
description: Tento článek popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894665"
---
# <a name="job-exempt-status"></a>Stav práce z hlediska přesčasů


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.

Fyzický název: cdm_jobexemptstatus

Tento výčet specifikuje sadu možností pro hodnoty stavu práce z hlediska přesčasů podle zákona FLSA. To je k dispozici v existující sadě možností cdm_jobexemptstatus.

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 | Osvobození | Práce je vyjmuta z přesčasů podle pokynů FLSA. |
| 200000001 | Neosvobozené | Práce není vyjmuta z přesčasů podle pokynů FLSA. |
| 200000002 | Nevztahuje se | Pokyny ohledně stavu FLSA se na práci nevztahují. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
