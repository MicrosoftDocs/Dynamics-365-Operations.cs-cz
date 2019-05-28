---
title: Vytvoření kanbanového pravidla události řádku kusovníku
description: Tato úloha je zaměřena na nastavení potřebné k vytvoření kanbanového pravidla události s cílem zajistit zásobování pro řádky výrobního kusovníku v kombinovaném provozním prostředí štíhlé a klasické výroby.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a4252548fd030f2a044436ff607da5125d2854
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551922"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>Vytvoření kanbanového pravidla události řádku kusovníku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato úloha je zaměřena na nastavení potřebné k vytvoření kanbanového pravidla události s cílem zajistit zásobování pro řádky výrobního kusovníku v kombinovaném provozním prostředí štíhlé a klasické výroby. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku.


## <a name="create-a-new-kanban-rule"></a>Vytvořit nové kanbanové pravidlo
1. Přejděte na Řízení výroby > Pravidelné úlohy > Výpočet kanbanového množství > Kanbanová pravidla.
2. Klikněte na položku Nová.
3. V poli Typ vyberte Výběr.
    * Typ Výběr se používá k vytvoření kanbanů převodu.  
4. V poli Strategie doplnění vyberte „Událost“.
    * Strategie Událost je vybrána s cílem vytvořit převod kanbanů na základě události. Později v rámci průvodce úkolu ji spustíme odhadem výrobní zakázky.  
5. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Zadejte nebo vyberte ReplenishSpeakerComponents. Tato aktivita převodu má přijímací sklad (výstupní) a umístění 12, což znamená, že materiál se přesune do umístění 12 ve skladu 12.  
6. Rozbalte sekci Podrobnosti.
7. V poli Produkt zadejte nebo vyberte M0001.
8. Rozbalte sekci Události.
9. V poli Událost řádku kusovníku vyberte možnost „Automatická“.
    * Pokud je pole Událost řádku kusovníku nastavena na Automaticky, vytvoří se kanban pro splnění požadavků na materiál pro řádky Kusovník výrobní zakázky.  
10. Zavřete stránku.

## <a name="create-and-modify-a-new-production-order"></a>Vytvoření a úprava nové výrobní zakázky
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
2. Klikněte na možnost Nová výrobní zakázka.
3. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Zadejte nebo vyberte hodnotu „L0001“. Použijeme položku L0001, protože položka M0001 je zahrnuta v kusovníku pro položku L0001.  
4. Klikněte na položku Vytvořit.
5. V seznamu klikněte na odkaz na řádku pro L0001
6. Klikněte na položku Kusovník.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klikněte na položku Upravit.
9. V poli Typ řádku vyberte „Doložená dodávka“.
    * Doložená dodávka je vybrána k aktivaci vytvoření dodávek pro kanban.  
10. Vyberte Ne v poli Spotřeba prostředku.
    * Zrušením zaškrtnutí políčka Spotřeba prostředku umožňuje změnit sklad.  
11. Rozbalte oblast Dimenze zásob.
12. Zadejte hodnotu 12 do pole Sklad.
    * Sklad je nastaven na 12, protože se jedná o výstupní sklad pro aktivitu Výběr.  
13. Zadejte hodnotu 12 do pole Umístění.
    * Umístění je nastaveno na 12, protože se jedná o výstupní umístění pro aktivitu Výběr.  
14. Zavřete stránku.
15. Zavřete stránku.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Odhad výrobní zakázky a zobrazení vytvořeného kanbanu
1. Klepněte na Odhad.
    * Odhadování výrobní zakázky spustí vytváření přidruženého kanbanu a poskytnutí zboží M0001.  
2. Klikněte na tlačítko OK.
3. Zavřete stránku.
4. Zavřete stránku.
5. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
6. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte kanbanové pravidlo události vytvořené pro zboží M0001.  
7. Rozbalte sekci Kanbany.
8. Označte v seznamu vybraný řádek.
    * Všimněte si kanbanu vytvořeného pro dodání zboží M0001 pro odhadovanou výrobní zakázku.  
    * Poslední krok!  

