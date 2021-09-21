---
title: Zásoby na skladě se nezohledňují pro zboží nad dávkami
description: Některé šablony slotů nezohledňují aktuální zásoby na skladě pro zboží nad dávkami. Číslo šarže nebo sériové číslo musí být uvedeno v objednávce.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475796"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Šablony slotů nezohledňují zásoby na skladě pro zboží nad dávkami

## <a name="symptoms"></a>Příznaky

Šablony slottingu, které mají kritérium slotu *Zohlednění stavu na skladě*, nezohledňují aktuální zásoby na skladě pro položky *batch-above*. Zvažují to pouze v případě, že je na řádku prodejní objednávky uvedeno číslo dávky.

Když však použijete položky *batch-below*, aktuální zásoby na skladu jsou očekávány.

Další informace viz [Skladový slotting](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Řešení

Záhlaví šablony slottingu lze definovat pro strategii poptávky *Objednáno*, *Rezervováno* nebo *Uvolněno*. Pro strategii poptávky *Objednáno* platí stejné požadavky na hierarchii rezervací, jaké platí pro rezervaci nebo uvolnění do procesů skladu. Proto pro položky, které mají hierarchii reservací *batch-above* a *serial-below*, musí být na objednávce poptávky (prodej nebo převod) zadáno číslo dávky nebo sériové číslo.

Případně strategie poptávky *Rezervováno* lze použít k výběru čísla dávky nebo sériového čísla před generováním poptávky skladového slottingu.
