---
title: Položky hlavního plánování nemůžete filtrovat podle jejich souvisejících hodnot skupiny pokrytí
description: Položky hlavního plánování nemůžete filtrovat podle jejich souvisejících hodnot skupiny pokrytí.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049457"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Položky hlavního plánování nemůžete filtrovat podle jejich souvisejících hodnot skupiny pokrytí

Číslo článku znalostní báze: 4612572

## <a name="symptoms"></a>Příznaky

Chcete filtrovat položky, které budou zahrnuty do dávkové úlohy hlavního plánování, na základě hodnot souvisejících záznamů z tabulky pokrytí položek. (Například chcete filtrovat položky podle jejich hodnot **Prodejce** a/nebo **Skupina pokrytí**). Nastavení filtru pro dávkovou úlohu vám umožní vytvořit spojení z tabulky **Položky** do tabulky **Pokrytí položky** a poté v dotazu zadejte hodnoty polí z tabulky pokrytí položky. Po dokončení tohoto nastavení však systém stále vytváří plánované objednávky pro celé pokrytí položky, nejen pro položky, které odpovídají zadaným hodnotám polí z tabulky pokrytí položky.

## <a name="resolution"></a>Řešení

Filtr dávkové úlohy může filtrovat pouze na položky. I když můžete propojení tabulky **Pokrytí položky**, nastavení filtru, které v této tabulce provedete, neovlivní výstup dotazu. Za běhu systém spustí plánování pro všechny skupiny pokrytí a všechny varianty, které mají filtrované položky. Poté, co je položka již zahrnuta v běhu, žádné skupiny pokrytí, které jsou zahrnuty ve filtru položek, neovlivní výstup plánování.
