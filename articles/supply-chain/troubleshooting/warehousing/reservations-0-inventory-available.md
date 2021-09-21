---
title: Nelze provádět rezervace skladu, protože v zásobách je k dispozici 0,00
description: Obdržíte chybu, že systém nemůže provádět rezervace, protože v zásobách je k dispozici jen 0,00. Tento problém je pravděpodobně způsoben otevřenou prací.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475827"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Systém nemůže provádět rezervace, protože v zásobách je k dispozici 0,00

## <a name="symptoms"></a>Příznaky

K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze. Zobrazí se následující chybová zpráva:

> Fyzicky na skladě Místo =%1, Sklad =%2, Stav zásob = Dostupné, Číslo šarže =%3, Majitel =%4: %5 nelze rezervovat, protože v zásobách je k dispozici pouze 0,00.

## <a name="resolution"></a>Řešení

Tento problém je pravděpodobně způsoben otevřenou prací. Buď dokončete práci, nebo přijměte bez vytvoření práce. Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství. Například tyto transakce mohou být otevřené objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.
