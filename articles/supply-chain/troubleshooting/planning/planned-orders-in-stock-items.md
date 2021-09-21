---
title: Plánované objednávky jsou generovány na skladě s výrobními zakázkami
description: Plánované objednávky se generují, i když máte položky na skladě a výrobní zakázky pro ně již existují
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
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475845"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Plánované objednávky jsou generovány na skladě s výrobními zakázkami

## <a name="symptoms"></a>Příznaky

Plánované objednávky se generují, i když máme položky na skladě a výrobní zakázky pro ně již existují.

## <a name="resolution"></a>Řešení

Tento problém můžete vyřešit zvýšením hodnoty **Pozitivní dny** pro příslušné skupiny na stránce **Skupina pokrytí**. Tato změna způsobí, že systém určí, zda lze pro poptávku použít zásoby na skladě. Pak nebude vygenerována nová plánovaná objednávka pro položky, které jsou na skladě.
