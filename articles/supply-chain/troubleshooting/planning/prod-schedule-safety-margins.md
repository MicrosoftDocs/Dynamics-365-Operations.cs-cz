---
title: Plánování výroby nezohledňuje bezpečnostní rezervy
description: Plánování výroby nezohledňuje bezpečnostní rezervy, které jsou nastaveny na pokrytí položky pro doloženou dodávku
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475775"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Plánování výroby nezohledňuje bezpečnostní rezervy

## <a name="symptoms"></a>Příznaky

Hlavní plánování zohledňuje bezpečnostní rezervy. Při plánování plánovaných výrobních zakázek jsou však bezpečnostní rezervy ignorovány.

## <a name="resolution"></a>Řešení

Rezervy se berou v úvahu pouze během hlavního plánování, nikoli během manuálního plánování. Rezervy jsou navrženy tak, aby fungovaly jako nárazník během fáze plánování a aby poskytly určitou „rezervu“ pro skutečný proces.

Chcete-li dosáhnout požadovaného výsledku, můžete odstranit rezervu. Postup musí být poté aktualizován tak, aby obsahoval požadovaný čas (například jako čas fronty). Hlavní plánování i manuální plánování by pak mělo přinést stejný výsledek.
