---
title: Stav žádosti o nábor
description: Tento článek popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859597"
---
# <a name="recruiting-request-status"></a>Stav žádosti o nábor


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.

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
