---
title: Nelze aktualizovat množství zásob z důvodu nedostatečných transakcí
description: Skladové množství -1% nelze aktualizovat, protože není dostatek skladových transakcí pro položku %2, které mají zadané dimenze.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475747"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Systém nemůže aktualizovat množství zásob z důvodu nedostatečných transakcí

## <a name="symptoms"></a>Příznaky

K tomuto problému může dojít, pokud systém nemůže aktualizovat množství zásob, protože není k dispozici dostatek transakcí zásob, které mají zadané dimenze. Zobrazí se následující chybová zpráva:

> Množství zásob -%1 nelze aktualizovat z důvodu nedostatečných transakcí zásob pro položku %2 s rozměry Velikost =%3, Barva =%4, Dodatky =%5, Místo =%6, Sklad =%7, Umístění =%8, Stav zásob = K dispozici, Registrační značka =%9, Číslo šarže =%10 pro referenční ID %11 na ID šarže %12.

## <a name="resolution"></a>Řešení

Ujistěte se, že žádné transakce zásob fyzicky nerezervují množství. Například tyto transakce mohou otevřít objednávky kvality, záznamy blokující zásoby nebo výstupní objednávky.
