---
title: Vytvoření kanbanového pravidla s použitím události řádku kanbanu
description: Tímto postupem vytvoříte kanbanové pravidlo pomocí nastavení události řádku kanbanu s cílem spustit vyžádání z aktivity procesu.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7aaf959db0f0a136fc615f9a57ec787ef6cf2ad
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579153"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Vytvoření kanbanového pravidla s použitím události řádku kanbanu

[!include [banner](../../includes/banner.md)]

Tímto postupem vytvoříte kanbanové pravidlo pomocí nastavení události řádku kanbanu s cílem spustit vyžádání z aktivity procesu. Kanbanové pravidlo je spuštěno aktivitou procesu kanbanu s množstvím vždy rovným nebo větším, než 25. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.


## <a name="create-a-kanban-rule"></a>Vytvoření kanbanového pravidla
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
2. Klikněte na položku Nová.
3. V poli Strategie doplnění vyberte „Událost“.
    * Tím se vygenerují kanbany přímo z poptávky. Ty slouží k nastavení pravidel definující scénář režimu rozpadu pro objednávku.  
4. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Zadejte nebo vyberte možnost SpeakerAssemblyAndPolish. První aktivita pravidla výrobního kanbanu musí být aktivita procesu ve výrobním toku. Vyberete-li aktivitu, data platnosti aktivity budou zkopírovány do dat platnosti kanbanového pravidla.  
5. Rozbalte sekci Podrobnosti.
6. Zadejte hodnotu L0001 do pole Produkt.
7. Rozbalte sekci Události.
8. V poli Událost řádku kanban vyberte možnost „Automatická“.
    * To generuje kanbany události na vyžádání.  Toto pole slouží ke konfiguraci kanbanových pravidel, která doplní materiál potřebný pro navazující aktivitu procesu. Vyberete-li Automaticky, kanbany události jsou vytvořeny s poptávky. Toto nastavení se doporučuje při spuštění výroby ve stejný den.  
9. Nastavte minimální množství události na „25“.
    * Kanbany události jsou generovány, když je výše požadavku rovna nebo vyšší než v tomto poli. To je užitečné, když se mají v jednom stroji generovat množství objednávky nižší, než v tomto poli, a v jiném stroji vyšší, než v tomto poli.  
10. Klikněte na položku Uložit.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Vytvoření prodejní objednávky a spuštění kanbanu řetězce
1. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
    * Vyberte účet odběratele US-003, Forest Wholesales.  
4. Klikněte na tlačítko OK.
5. Do pole Číslo položky zadejte L0001.
    * L0001 je zboží, pro které jste vytvořili kanbanové pravidlo.  
6. Nastavte množství na hodnotu 27.
    * Protože 27 je vyšší, než minimální množství 25 v kanbanovém pravidle, spustí se tak kanbanová událost.  
7. Zadejte do pole Místo hodnotu „1“.
8. V poli Sklad zadejte nebo vyberte hodnotu.
    * Vyberte sklad 13.  
9. Klikněte na položku Uložit.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Zobrazení kanbanu generovaného pravidlem kanbanu
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Rozbalte sekci Kanbany.
    * Všimněte si, že kanban pro 27 byl vytvořen pro zpracování aktivity na základě vytvořeného kanbanového pravidla.  
    * Jde o poslední krok.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]