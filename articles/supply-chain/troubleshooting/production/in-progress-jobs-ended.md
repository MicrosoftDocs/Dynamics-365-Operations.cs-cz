---
title: Probíhající úlohy jsou ukončeny při vykazování částečného množství u poslední úlohy
description: Když použijete zařízení úkolového lístku k nahlášení částečného množství na posledním úkolu ve výrobní zakázce, automaticky se ukončí všechny předchozí úkoly na této zakázce, které mají stav Probíhá.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475838"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Předchozí probíhající úlohy jsou ukončeny při vykazování částečného množství u poslední úlohy

## <a name="symptoms"></a>Příznaky

Když použijete zařízení úkolového lístku k nahlášení částečného množství na posledním úkolu ve výrobní zakázce, automaticky se ukončí všechny předchozí úkoly na této zakázce, které mají stav Probíhá.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Na stránce **Výchozí hodnoty výrobní zakázky** na kartě **Nahlásit jako dokončené** je možnost s názvem **Ukončení tech. postupu**. Pokud je toto téma nastaveno na *Ano*, deník karet postupů se zaúčtuje, když pracovník použije zařízení úkolového lístku nebo terminál úkolového lístku k nahlášení poslední operace. Tento deník označuje všechny operace jako dokončené a ukončí všechny produkční úlohy. Když je možnost **Ukončení tech. postupu** nastavena na *Ano*, systém nezohledňuje stav úlohy, který pracovník vybral, když ohlásil poslední operaci. Systém také nezvažuje, zda pracovník hlásí úplné nebo částečné množství.
