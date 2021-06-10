---
title: Stav žádosti o nábor
description: Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059177"
---
# <a name="recruiting-request-status"></a>Stav žádosti o nábor

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.

Fyzický název: mshr_hcmrecruitingrequeststatus

Tento výčet poskytuje sadu možností pro stavové hodnoty RecruitingRequest.

| Hodnota | Štítek | popis |
| --- | --- | --- |
| 200000000 | Koncept | Žádost je ve stavu konceptu a není připravena na aktivní nábor. |
| 200000001 | Probíhá kontrola | Žádost byla odeslána a je směrována ke schválení pomocí pracovního postupu. K dispozici je pouze v případě, že je povolen pracovní postup. |
| 200000002 | Čeká na zpracování | Požadavek čeká na provedení pracovního postupu. K dispozici je pouze v případě, že je povolen pracovní postup. |
| 200000003 | Zrušená | Požadavek byl zrušen. K dispozici je pouze v případě, že je povolen pracovní postup. |
| 200000004 | Zamítnutý | Žádost byla zamítnuta. K dispozici je pouze v případě, že je povolen pracovní postup. |
| 200000005 | Aktivní | Jakýkoli pracovní postup je dokončen a schválen a požadavek je připraven k aktivnímu náboru. |
| 200000006 | Uzavřený | Žádost o nábor je uzavřena. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]