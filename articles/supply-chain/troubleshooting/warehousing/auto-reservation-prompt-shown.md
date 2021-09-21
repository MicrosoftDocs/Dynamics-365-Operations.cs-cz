---
title: Výzva k automatické rezervaci se zobrazuje i u dostupných zásob
description: Když však použijete stejnou položku ve skladu, kde nejsou povoleny procesy skladu, zobrazí se výzva k automatické rezervaci. Zadejte všechny dimenze nad Umístění.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475833"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Výzva k automatické rezervaci čísla dávky se zobrazuje i u dostupných zásob

## <a name="symptoms"></a>Příznaky

Když používáte položku, která má hierarchii rezervací *batch-above* ve skladu, který nemá povolené procesy skladu a je povolena automatická rezervace, zobrazí se výzva k automatické rezervaci čísla dávky, i když je pro vyzvednutí k dispozici pouze jedna dávka.

Když však použijete stejnou položku ve skladu, kde jsou povoleny procesy skladu, výzva k automatické rezervaci se nezobrazí.

## <a name="resolution"></a>Řešení

Pokud je hierarchie rezervací definována jako *batch-above* nebo *serial-above*, odkazovaná dimenze (**Číslo dávky** nebo **Sériové číslo**) musí být vždy uvedeno na objednávkách poptávky. Procesy skladu mohou být schopny doplnit informace, pokud je k dispozici jedna dávka nebo sériové číslo. Protože však sklad nemá povoleny procesy skladu, musí uživatel vždy zadat všechny dimenze nad **skladovým místem**.
