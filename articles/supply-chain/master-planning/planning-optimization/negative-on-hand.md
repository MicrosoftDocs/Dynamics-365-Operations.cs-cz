---
title: Plánování se záporným množstvím na skladě
description: Toto téma vysvětluje, jak je při použití optimalizace plánování zpracováno záporné množství na skladě.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8803b0b90f22711b844442d16f717ab87dabf041
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209851"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Plánování se záporným množstvím na skladě

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Pokud systém zobrazí záporné celkové množství na skladě, modul plánování zpracuje toto množství jako hodnotu 0 (nula), aby se zabránilo překročení dodávky. Tato funkce funguje zde:

1. Funkce optimalizace plánování agreguje množství na skladě na nejnižší úrovni dimenzí disponibility. (Pokud například *skladové místo* není dimenze disponibility, optimalizace plánování agreguje množství na skladě na úrovni *skladu*.)
1. Pokud je celkové množství na skladě na nejnižší úrovni dimenzí disponibility záporné, systém předpokládá, že množství na skladě je skutečně 0 (nula).

> [!IMPORTANT]
> Plánovací systém může být pouze tak přesný jako vstupní data. Pokud jsou vstupní data nepřesná, záporné záznamy na skladě budou označovat, že informace o zásobách v Microsoft Dynamics 365 Supply Chain Management nejsou synchronizované se skutečným světem. Z toho vyplývá, že výsledkem plánování bude chyba. Chcete-li získat přesný výsledek plánování, měli byste minimalizovat počet záznamů, které zobrazují záporné množství na skladě.

## <a name="example-1"></a>Příklad 1

Sklad 13 je nakonfigurován následujícím způsobem:

- **Kód disponibility:** Min./Max.
- **Minimum:** 15 kusů (KS)
- **Maximum:** 25 kusů

Nejnižší úroveň dimenzí disponibility je *sklad*a následující množství na skladě se zaznamenávají na úrovni *skladového místa*:

- **Pracoviště 1, sklad 13, skl. místo 1** 20 kusů.
- **Pracoviště 1, sklad 13, skl. místo 2:** &minus;8 ks.

Proto je celkové množství na skladě pro sklad 13 12 kusů. (= 20 ks. &minus; 8 ks.).

V tomto případě plánovací modul využívá celkové množství na skladě 12 ks. pro sklad 13.

Výsledkem je plánovaná objednávka na 13 kusů. (= 25 ks. &minus;12 kusů.) pro doplnění skladu 13 z 12 ks. na 25 ks.

## <a name="example-2"></a>Příklad 2

Sklad 13 je nakonfigurován následujícím způsobem:

- **Kód disponibility:** Min./Max.
- **Minimum:** 15 ks.
- **Maximum:** 25 ks.

Nejnižší úroveň dimenzí disponibility je *sklad*a následující množství na skladě se zaznamenávají na úrovni *skladového místa*:

- **Pracoviště 1, sklad 13, skl. místo 1** 4 ks.
- **Pracoviště 1, sklad 13, skl. místo 2:** &minus;8 ks.

Proto je celkové množství na skladě pro sklad 13 je &minus;4 ks. (= 4 ks. &minus; 8 ks.). Jinými slovy, jedná se o méně než 0 (nula).

V tomto případě plánovací modul předpokládá, že množství na skladě pro sklad 13 je 0 ks. místo &minus;4 ks.

Výsledkem je plánovaná objednávka na 25 kusů. (= 25 ks. &minus;0 kusů.) pro doplnění skladu 13 z 0 ks. na 25 ks.

## <a name="related-resources"></a>Související prostředky

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Začínáme s optimalizací plánování](get-started.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Zrušení úlohy plánování](cancel-planning-job.md)
