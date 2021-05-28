---
title: Při importu záznamů prognózy poptávky nemůžete aktualizovat předpokládané jednotkové náklady
description: Když použijete datové entity k importu záznamů prognózy poptávky, nákladová cena pro stávající záznamy se neaktualizuje tak, aby odpovídala importovaným datům.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026341"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Při importu záznamů prognózy poptávky nemůžete aktualizovat předpokládané jednotkové náklady

Číslo článku znalostní báze: 4614109

## <a name="symptoms"></a>Příznaky

Když použijete datové entity k importu záznamů prognózy poptávky, hodnota **Prognózovaná jednotková cena** pro stávající záznamy se neaktualizuje tak, aby odpovídala importovaným datům.

## <a name="cause"></a>Příčina

**Předpokládané jednotkové náklady** je pole jen pro čtení. Hodnota je založena na jednotkové ceně produktu a nelze ji nastavit přímo pomocí importu.

## <a name="resolution"></a>Rozlišení

Protože je pole jen pro čtení, nemůžete pro něj importovat hodnoty. Hodnota bude vypočítána podle stávající obchodní logiky.
