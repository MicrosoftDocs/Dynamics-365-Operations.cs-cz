---
title: Stav práce z hlediska přesčasů
description: Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 29d3c4fd37a219b520172c6866c5fec488c698f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064984"
---
# <a name="job-exempt-status"></a>Stav práce z hlediska přesčasů


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.

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
