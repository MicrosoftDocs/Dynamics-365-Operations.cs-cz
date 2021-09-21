---
title: Problémy převodu měny obchodní smlouvy
description: Ceny obchodních smluv se nepřepočítají podle měny, když se měna liší od nákupní objednávky
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475760"
---
# <a name="trade-agreement-currency-conversion-issues"></a>Problémy převodu měny obchodní smlouvy

## <a name="symptoms"></a>Příznaky

Ceny obchodních smluv se nepřepočítají podle měny, když se měna liší od nákupní objednávky.

## <a name="resolution"></a>Řešení

Funkce *Obecná měna* umožňuje definovat ceny a slevy pouze v jedné měně. Poté můžete převádět na jiné měny podle potřeby. Po dokončení převodu může funkce navíc automaticky použít inteligentní zaokrouhlování.
