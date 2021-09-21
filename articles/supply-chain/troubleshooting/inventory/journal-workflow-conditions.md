---
title: Podmínky workflow deníku zásob platí na úrovni deníku, nikoli na úrovni řádku
description: Podmínky workflowu deníku zásob platí pouze na úrovni deníku, nikoli na úrovni řádků.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475795"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Podmínky workflow deníku zásob platí na úrovni deníku, nikoli na úrovni řádku

## <a name="symptoms"></a>Příznaky

K tomuto problému může dojít, pokud se například pokusíte nastavit podmínku workflowu deníku zásob na částku nákladů. Nastavíte podmínku tak, aby byl krok 1 spuštěn pouze v případě, že částka nákladů bude nižší než 100. Pak nastavíte jinou podmínku tak, aby byl krok 2 spuštěn pouze v případě, že částka nákladů bude vyšší nebo rovna 100. Poté, když je spuštěn workflow, se v historii pracovního postupu zobrazuje pouze jeden řádek a první podmínka se vždy vyhodnotí jako *skutečný*, bez ohledu na hodnotu, která je zadána.

## <a name="workaround"></a>Alternativní řešení

V aktuální verzi platí podmínky workflowu deníku zásob pouze na úrovni deníku, nikoli na úrovni řádků. Toto chování je záměrné. Doporučujeme nastavit kritéria podmínky pouze na atributy na úrovni deníku.
