---
title: Rozdíly mezi integrovaným hlavním plánováním a optimalizací plánování
description: Toto téma uvádí funkce, které Optimalizace plánování zatím nepodporuje a které nejsou uvedeny na stránce Analýza přizpůsobení optimalizace plánování.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344947"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Rozdíly mezi integrovaným hlavním plánováním a optimalizací plánování

[!include [banner](../../includes/banner.md)]

Výsledky optimalizace plánování se mohou lišit od výsledků z integrovaného hlavního plánovače. Rozdíly mohou být způsobeny chystanými funkcemi. Toto téma uvádí funkce, které Optimalizace plánování zatím nepodporuje a které nejsou uvedeny na stránce **[Analýza přizpůsobení optimalizace plánování](planning-optimization-fit-analysis.md)**.

| Funkce | Aktuální chování v optimalizaci plánování |
|---|---|
| Produkty se skutečnou hmotností | Produkty se skutečnou hmotností jsou považovány za obvyklé produkty.|
| Rozšiřitelné rozměry | Rozšiřitelné rozměry jsou u plánovaných objednávek prázdné, i když je zaškrtnuto políčko **Plán pokrytí podle dimenze** na stránce **Skupiny dimenzí úložiště** nebo **Skupiny sledovacích dimenzí**. |
| Filtrovaná výrobní spuštění | Podrobnosti viz [Plánování výroby - filtry](production-planning.md#filters). |
| Plánování prognóz | Plánování prognóz není podporováno. Doporučujeme použít hlavní plánování, kde je k hlavnímu plánu přiřazen model prognózy. |
| Číselné sekvence pro plánované objednávky | Posloupnosti čísel pro plánované objednávky nejsou podporovány. Plánovaná čísla objednávek jsou generována na straně služby. |
| Naplánujte kopírování, odstranění plánu a vyčištění verze plánu | <p>Následující položky jsou zakázány v **Hlavní plánování \> Hlavní plánování \> Udržujte plány** v navigačním podokně:</p><ul><li>Kopie plánu</li><li>Odstranit plán</li><li>Vyčištění verze plánu</li></ul> |
| Vratky | K vratkám se nepřihlíží. |
| Plánování souvisejících funkcí | Podrobnosti viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md#limitations). |
| Dopravní kalendáře | Hodnota ve sloupci **Přepravní kalendář** na stránce **Způsoby dodání** je ignorována. |

## <a name="additional-resources"></a>Další prostředky

- [Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)
- [Parametry, které optimalizace plánování nepoužívá](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
