---
title: Proces a historie vydání modulu Optimalizace plánování
description: Toto téma poskytuje informace o procesu vydání a historii vydání Optimalizace plánování.
author: crytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1bf08fc75aa2c05b2f2974ee46ec16609505f696
ms.sourcegitcommit: b5f2d88ff4e0a234fa6b9ee33516425e54ff2c3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/21/2021
ms.locfileid: "7506776"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Proces a historie vydání modulu Optimalizace plánování

[!include [banner](../../includes/banner.md)]

Společnost Microsoft aktualizuje Optimalizaci plánování každý měsíc. Na základě obchodních požadavků však příležitostně vydáváme další aktualizace mezi naplánovanými vydáními.

Každá verze je publikována do jednotlivých oblastí, kde je Optimalizace plánování k dispozici. Proces obvykle trvá tři dny.

Během aktualizace Optimalizace plánování může hlavní plánování běžet o něco pomaleji než obvykle.

Prostředí využívající Optimalizaci plánování automaticky obdrží nejnovější verzi. Není vyžadována žádná akce uživatele: služba se automaticky aktualizuje. Do prostředí se však nikdy automaticky nepřenáší žádná zásadní změna. Ve výchozím nastavení jsou všechny změny, které jsou považovány za zásadní, vypnuty a musí být explicitně zapnuty ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tyto změny se proto v prostředích nezobrazí, dokud se nerozhodnete je povolit.

Protože se při aktualizaci Optimalizace plánování ve vašem prostředí nezobrazují oznámení, můžete si prohlédnout poznámky k verzi v následující tabulce a určit, kdy byly změny vydány a jaké funkce zavedly. Tato tabulka ukazuje změny, které byly vydány pro Optimalizaci plánování, zda jsou tyto změny přidruženy k funkci ze správy funkcí, a datum vydání.

| Změny | Podrobnosti správy funkcí | Data vydání |
|---|---|---|
| <p>Přidána podpora pro hlavní plány s **Metodou plánování** nastavenou na *Plánování operací*.</p><p>Na stránce **Skupiny postupu** respektujte nastavení zaškrtávacích políček **Aktivace**, **Pracovní čas** a **Kapacita** u řádků, jejichž **Postup/typ práce** má hodnotu *Nastavení* nebo *Zpracování*. </p><p>Vylepšení obecného výkonu, kvality a stability. | <p>Plánování operací je k dispozici ve správě funkcí od verze 10.0.20.</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p>  | 9.–17. září 2021 |
| Vylepšení obecného výkonu, kvality a stability. | Není vyžadována žádná správa funkcí. | 25.–30. srpna 2021 |
| <p>Přidáno pole **Doba realizace** k plánovaným zakázkám.</p><p>Vylepšení obecného výkonu, kvality a stability.</p> | Není vyžadována žádná správa funkcí. | 12.–17. srpna 2021 |
| <p>Přidány požadavky na typ zdroje pro plánování s nekonečnou kapacitou.</p><p>Vylepšená účinnost zdrojů a efektivita kalendáře pro plánování s nekonečnou kapacitou.</p><p>Další informace viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md). | <p>K dispozici ve správě funkcí od verze 10.0.20.</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p> | 6.–12. července 2021 |
| Obecná vylepšení kvality. | Není vyžadována žádná správa funkcí. | 6.–12. července 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
