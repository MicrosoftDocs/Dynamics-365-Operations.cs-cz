---
title: Vytvoření kanbanového pravidla pro více aktivit
description: Tento postup popisuje, jak vytvořit kanbanové pravidlo, které zahrnuje více aktivit z výrobního toku.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f55034f4f0557023ce0c659c1e8258214cf8bfa3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569232"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Vytvoření kanbanového pravidla pro více aktivit

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak vytvořit kanbanové pravidlo, které zahrnuje více aktivit z výrobního toku. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF. Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.


## <a name="create-a-new-kanban-rule"></a>Vytvořit nové kanbanové pravidlo
1. Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.
2. Klikněte na položku Nová.
3. V poli Strategie doplnění vyberte „Plánováno“.
4. V poli První aktivita plánu zadejte nebo vyberte hodnotu.
    * Vyberte možnost SpeakerAssemblyAndPolish.  
5. Označte pole Více aktivit.
    * Cílem je zahrnout více než jednu aktivitu v kanbanovém pravidle. Cestu ve výrobním toku zvolíte při výběru poslední aktivity plánu.  
6. V poli Poslední aktivita plánu zadejte nebo vyberte hodnotu.
    * Vyberte hodnotu „SpeakerTestAndPackaging“. Po výběru hodnoty se automaticky otevře stránka. Vybrat kanbanový tok SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Klikněte na tlačítko OK.  
7. Rozbalte sekci Podrobnosti.
8. V poli Produkt zadejte nebo vyberte hodnotu.
    * Vyberte položku L0006.  

## <a name="create-kanban-and-view-jobs"></a>Vytvoření kanbanu a zobrazení úloh
1. Rozbalte sekci Kanbany.
2. Klepněte na možnost Přidat.
3. Do pole Počet nových kanbanů zadejte „1“.
    * Dojde k vytvoření 1 kanbanu.  
4. Nastavte Celkové množství produktu na 3.
    * Kanban zpracuje 3 produkty.  
5. Do pole Datum/čas splatnosti zadejte datum a čas.
    * Lze zadat hodnotu Dnes.  
6. Klikněte na položku Vytvořit.
7. Klepněte na možnost Podrobnosti.
    * Všimněte si, že kanban má od výrobního toku dvě úlohy pro zpracování. První je SpeakerAssemblyAndPolish a druhá SpeakerTestAndPackaging.  
    * Poslední krok!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]