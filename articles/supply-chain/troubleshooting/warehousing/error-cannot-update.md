---
title: Dojde k chybě, když je místo vybráno během registrace výběrového seznamu
description: Dojde k chybě, když je místo vybráno během registrace výběrového seznamu.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef34b4fdcc572c56319f6cbf4913d822d8857595
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474957"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Dojde k chybě, když je místo vybráno během registrace výběrového seznamu

Číslo článku znalostní báze: 4613106

## <a name="symptoms"></a>Příznaky

K tomuto problému dochází, když je váš systém nakonfigurován tak, aby automaticky rezervoval prodejní objednávky. Pokud se pokusíte vybrat umístění pro řádek registrace výběrového seznamu, zobrazí se při použití procesů rezervace skladu (WMS) následující chybová zpráva:

> Množství nelze aktualizovat pomocí nových dimenzí

K tomuto problému může dojít, protože na zadaném místě nemáte dostatek skladových zásob.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen.

Ve scénářích, kde použijete proces rezervace na úrovni skladu, pokud nebudou zásoby po ruce rezervovány na všech úrovních dimenze skladu a v zadaném umístění nemáte dostatečné zásoby po ruce, doporučujeme použít proces ruční rezervace z vychystávací linky. Poté můžete použít funkci *Rezervní šarže* pro distribuci nižších rezervací, jako například umístění, pro všechna dostupná množství na skladě.
