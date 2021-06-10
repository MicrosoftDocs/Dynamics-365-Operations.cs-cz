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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053844"
---
# <a name="job-exempt-status"></a>Stav práce z hlediska přesčasů

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