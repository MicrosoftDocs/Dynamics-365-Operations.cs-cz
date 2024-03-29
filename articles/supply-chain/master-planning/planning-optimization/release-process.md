---
title: Proces a historie vydání modulu Optimalizace plánování
description: Tento článek poskytuje informace o procesu vydání a historii vydání Optimalizace plánování.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682553"
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
| <p>[Kódy dispozice dávky](../../inventory/batch-disposition-codes.md)</p><p>Zahrňte do hlavních plánů zásoby na skladě a parametry transakcí se zásobami</p><p>Vylepšení obecného výkonu, kvality a stability</p> | Není vyžadována žádná správa funkcí | 10. – 14. října 2022 |
| <p>[Plánování zdrojů s omezenou kapacitou](finite-capacity.md)</p><p>Vylepšení obecného výkonu, kvality a stability</p> | Není vyžadována žádná správa funkcí | 19. – 23. září 2022 |
| Vylepšení obecného výkonu, kvality a stability | Není vyžadována žádná správa funkcí | 29. srpna – 3. září 2022 |
| <p>[Centralizovaná údržba kalendáře](../supply-chain-calendars-master-planning.md)</p><p>[Návrhy na optimalizaci stávající nabídky](../action-messages.md)</p><p>[Podpora subdodávek](../../production-control/manage-subcontract-work-production.md)</p><p>Vylepšení obecného výkonu, kvality a stability</p> | Není vyžadována žádná správa funkcí | 7. – 11. března 2022 |
| Podpora priority plánování u výrobních zakázek | K dispozici ve verzi 10.0.25 jako součást funkce *Podpora MRP řízená prioritou pro optimalizaci plánování*. | 12. – 18. listopadu 2021 |
| Vylepšení obecného výkonu, kvality a stability | Není vyžadována žádná správa funkcí | 12. – 18. listopadu 2021 |
| <p>Podpora vzorců pro výpočet doby procesu, výrobního postupu s překrýváním a čísla výrobní operace u transakcí požadavků</p><p>Vylepšené chybové zprávy pro plánování výroby související s časovým limitem, nenalezenou kapacitou a cyklickým postupem</p><p>Vylepšená konzistence při výpočtu dat příjmu a data vydání u plánovaných objednávek i pevných objednávek</p><p>Vylepšení obecného výkonu, kvality a stability</p> | Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování* | 22. – 27. října 2021 |
| <p>Podpora pro zohlednění procenta zmetkovitosti při výpočtu doby zpracování</p><p>Podpora pro číslo operace a použití materiálů během plánování</p> | Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování* | 5. – 7. října 2021 |
| <p>Podpora pro typy úloh výrobního postupu: **Fronta předtím**, **Fronta po** a **Doba přepravy**</p><p>Vylepšení obecného výkonu, kvality a stability</p> | Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování* | 25. – 30. září 2021 |
| <p>Podpora pro hlavní plány s **Metodou plánování** nastavenou na *Plánování operací*</p><p>Na stránce **Skupiny postupu** respektujte nastavení zaškrtávacích políček **Aktivace**, **Pracovní čas** a **Kapacita** u řádků, jejichž **Postup/typ práce** má hodnotu *Nastavení* nebo *Zpracování* </p><p>Vylepšení obecného výkonu, kvality a stability</p> | <p>Plánování operací je k dispozici ve správě funkcí od verze 10.0.20</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p> | 9.–17. září 2021 |
| Vylepšení obecného výkonu, kvality a stability | Není vyžadována žádná správa funkcí | 25.–30. srpna 2021 |
| <p>Přidáno pole **Doba realizace** k plánovaným zakázkám.</p><p>Vylepšení obecného výkonu, kvality a stability.</p> | Není vyžadována žádná správa funkcí | 12.–17. srpna 2021 |
| <p>Přidány požadavky na typ zdroje pro plánování s nekonečnou kapacitou</p><p>Vylepšená účinnost zdrojů a efektivita kalendáře pro plánování s nekonečnou kapacitou</p><p>Další informace viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md)</p> | <p>K dispozici ve správě funkcí od verze 10.0.20</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p> | 6.–12. července 2021 |
| Obecná vylepšení kvality | Není vyžadována žádná správa funkcí | 6.–12. července 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
