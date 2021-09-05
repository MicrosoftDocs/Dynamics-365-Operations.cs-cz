---
title: Proces a historie vydání modulu Optimalizace plánování
description: Toto téma poskytuje informace o procesu vydání a historii vydání Optimalizace plánování.
author: crytt
ms.date: 8/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fcd18341629afcf3092a457ae711e27b0bbfeb2a
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394407"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Proces a historie vydání modulu Optimalizace plánování

[!include [banner](../../includes/banner.md)]

Společnost Microsoft aktualizuje Optimalizaci plánování každý měsíc. Na základě obchodních požadavků však příležitostně vydáváme další aktualizace mezi naplánovanými vydáními.

Každá verze je publikována do jednotlivých oblastí, kde je Optimalizace plánování k dispozici. Proces obvykle trvá tři dny.

Během aktualizace Optimalizace plánování může hlavní plánování běžet o něco pomaleji než obvykle.

Prostředí využívající Optimalizaci plánování automaticky obdrží nejnovější verzi. Není vyžadována žádná akce uživatele: služba se automaticky aktualizuje. Do prostředí se však nikdy automaticky nepřenáší žádná zásadní změna. Ve výchozím nastavení jsou všechny změny, které jsou považovány za zásadní, vypnuty a musí být explicitně zapnuty ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tyto změny se proto v prostředích nezobrazí, dokud se nerozhodnete je povolit.

Protože se při aktualizaci Optimalizace plánování ve vašem prostředí nezobrazují oznámení, můžete si prohlédnout poznámky k verzi v následující tabulce a určit, kdy byly změny vydány a jaké funkce zavedly. Tato tabulka ukazuje změny, které byly vydány pro Optimalizaci plánování, zda jsou tyto změny přidruženy k funkci ze správy funkcí, a datum vydání.

| Změny | Podrobnosti správy funkcí | Datum vydání |
|---|---|---|
| <p>Přidáno pole **Doba realizace** k plánovaným zakázkám.</p><p>Vylepšení obecného výkonu, kvality a stability.</p> | Není vyžadována žádná správa funkcí. | 16. srpna 2021 |
| <p>Přidány požadavky na typ zdroje pro plánování s nekonečnou kapacitou.</p><p>Vylepšená účinnost zdrojů a efektivita kalendáře pro plánování s nekonečnou kapacitou.</p><p>Další informace viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md). | <p>K dispozici ve správě funkcí od verze 10.0.20.</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p> | 6. července 2021 |
| Obecná vylepšení kvality. | Není vyžadována žádná správa funkcí. | 6. července 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
