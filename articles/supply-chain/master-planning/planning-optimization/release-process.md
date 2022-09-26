---
title: Proces a historie vydání modulu Optimalizace plánování
description: Tento článek poskytuje informace o procesu vydání a historii vydání Optimalizace plánování.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2f91c46367ee2f881476a496555f15454c9f6baa
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542313"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Proces a historie vydání modulu Optimalizace plánování

[!include [banner](../../includes/banner.md)]

Společnost Microsoft aktualizuje Optimalizaci plánování každý měsíc. Na základě obchodních požadavků však příležitostně vydáváme další aktualizace mezi naplánovanými vydáními.

Každá verze je publikována do jednotlivých oblastí, kde je Optimalizace plánování k dispozici. Proces obvykle trvá tři dny.

Během aktualizace Optimalizace plánování může hlavní plánování běžet o něco pomaleji než obvykle.

Prostředí využívající Optimalizaci plánování automaticky obdrží nejnovější verzi. Není vyžadována žádná akce uživatele: služba se automaticky aktualizuje. Do prostředí se však nikdy automaticky nepřenáší žádná zásadní změna. Ve výchozím nastavení jsou všechny změny, které jsou považovány za zásadní, vypnuty a musí být explicitně zapnuty ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tyto změny se proto v prostředích nezobrazí, dokud se nerozhodnete je povolit.

Protože se při aktualizaci Optimalizace plánování ve vašem prostředí nezobrazují oznámení, můžete si prohlédnout poznámky k verzi v následující tabulce a určit, kdy byly změny vydány a jaké funkce zavedly. Tato tabulka ukazuje změny, které byly vydány pro Optimalizaci plánování, zda jsou tyto změny přidruženy k funkci ze správy funkcí, a datum vydání.

<!-- KFM: Add this? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> 

| Změny | Podrobnosti správy funkcí | Data vydání |
|---|---|---|
| <p>Vylepšení obecného výkonu, kvality a stability. | Není vyžadována žádná správa funkcí. | 29. srpna – 3. září 2022 |
| <p>Vylepšení obecného výkonu, kvality a stability.<p>[Centralizovaná údržba kalendáře Optimalizace plánování](../supply-chain-calendars-master-planning.md)<p>[Návrhy optimalizace plánování pro optimalizaci stávající nabídky](../action-messages.md)<p>[Podpora Optimalizace plánování u subdodávek](../../production-control/manage-subcontract-work-production.md) | Není vyžadována žádná správa funkcí. | 7. – 11. března 2022 |
| <p>Přidána podpora priority plánování u výrobních zakázek. | K dispozici ve verzi 10.0.25 jako součást funkce *Podpora MRP řízená prioritou pro optimalizaci plánování*. | 12. – 18. listopadu 2021 |
| <p>Vylepšení obecného výkonu, kvality a stability. | Není vyžadována žádná správa funkcí. | 12. – 18. listopadu 2021 |
| <p>Přidána podpora vzorců pro výpočet doby procesu, výrobního postupu s překrýváním a čísla výrobní operace u transakcí požadavků.</p><p>Vylepšené chybové zprávy pro plánování výroby související s časovým limitem, nenalezenou kapacitou a cyklickým postupem.</p><p>Vylepšená konzistence při výpočtu dat příjmu a data vydání u plánovaných objednávek i pevných objednávek.</p><p>Vylepšení obecného výkonu, kvality a stability. | Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování* | 22. – 27. října 2021 |
| <p>Přidána podpora pro zohlednění procenta zmetkovitosti při výpočtu doby zpracování.</p><p>Přidána podpora pro číslo operace a použití materiálů během plánování. | Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování* | 5. – 7. října 2021 |
| <p>Přidána podpora pro typy úloh výrobního postupu: **Fronta předtím**, **Fronta po** a **Doba přepravy**.</p><p>Vylepšení obecného výkonu, kvality a stability. | Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování* | 25. – 30. září 2021 |
| <p>Přidána podpora pro hlavní plány s **Metodou plánování** nastavenou na *Plánování operací*.</p><p>Na stránce **Skupiny postupu** respektujte nastavení zaškrtávacích políček **Aktivace**, **Pracovní čas** a **Kapacita** u řádků, jejichž **Postup/typ práce** má hodnotu *Nastavení* nebo *Zpracování*. </p><p>Vylepšení obecného výkonu, kvality a stability. | <p>Plánování operací je k dispozici ve správě funkcí od verze 10.0.20.</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p>  | 9.–17. září 2021 |
| Vylepšení obecného výkonu, kvality a stability. | Není vyžadována žádná správa funkcí. | 25.–30. srpna 2021 |
| <p>Přidáno pole **Doba realizace** k plánovaným zakázkám.</p><p>Vylepšení obecného výkonu, kvality a stability.</p> | Není vyžadována žádná správa funkcí. | 12.–17. srpna 2021 |
| <p>Přidány požadavky na typ zdroje pro plánování s nekonečnou kapacitou.</p><p>Vylepšená účinnost zdrojů a efektivita kalendáře pro plánování s nekonečnou kapacitou.</p><p>Další informace viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md). | <p>K dispozici ve správě funkcí od verze 10.0.20.</p><p>Název funkce: *Plánování s nekonečnou kapacitou pro Optimalizaci plánování*</p> | 6.–12. července 2021 |
| Obecná vylepšení kvality. | Není vyžadována žádná správa funkcí. | 6.–12. července 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
