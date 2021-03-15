---
title: Stav práce z hlediska přesčasů
description: Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125562"
---
# <a name="job-exempt-status"></a>Stav práce z hlediska přesčasů

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