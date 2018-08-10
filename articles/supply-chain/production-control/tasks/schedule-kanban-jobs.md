--- 
title: "Plánování kanbanových úloh"
description: "Tento postup se zaměřuje na plánování zpracování kanbanových úloh pro konkrétní pracovní buňku."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f36544993a9280ae10489a19252bc105abd40ac9
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-kanban-jobs"></a>Plánování kanbanových úloh

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na plánování zpracování kanbanových úloh pro konkrétní pracovní buňku. Postup "Příprava procesní kanbanové úlohy, pokud nejsou materiály k dispozici" je předpokladem pro vytvoření tohoto postupu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tato úloha je určena pro dílenského nadřízeného a plánovače výroby pracujícího s kanbany.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Vyberte kanbanové úlohy pro pracovní buňku
1. Přejděte na Řízení výroby > Kanban > Plánování kanbanové úlohy.
2. Rozbalte okno s fakty Kapacita období
    * Rozbalte okno s fakty pro kanban.  
3. V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Označte v seznamu vybraný řádek.
    * Vyberte pracovní buňku 1250. To způsobí filtrování zobrazení a zobrazíte tak pouze úlohy pro pracovní buňku 1250.  
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klepněte na tlačítko Vybrat.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Naplánování kanbanové úlohy v prvním dostupném období
1. Označte v seznamu vybraný řádek.
    * Vyberte první řádek v seznamu, který má stav Neplánováno. Tečkovaná ikona v poli Stav úlohy označuje neplánovanou úlohu.  
2. Klikněte na Plánovat.
    * To způsobí naplánování kanbanové úlohy v prvním dostupném období.  
    * Všimněte si, že kanbanová úloha se přesunula na konec seznamu, protože byla přidána k období počínajícího dnešním dnem.  
    * Pokud období začínající dneškem je plně rezervováno, úloha bude přesunuta do prvního volného období.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Naplánování dvou kanbanových úloh na určitý den
1. Vyberte ze seznamu řádek 1.
    * Měli byste dohlédnout na to, aby první řádek měl stav Neplánováno v poli Stav úlohy.  
2. Vyberte ze seznamu řádek 2.
    * Měli byste dohlédnout na to, aby druhý řádek měl stav Neplánováno v poli Stav úlohy. Nyní máte vybrané první dvě úlohy.  
3. Kliknutím na Plánováno od data otevřete dialogové okno.
4. Označte nebo odznačte pole Přepsat reakci na nedostatek kapacity.
    * Tato možnost umožňuje přepsat výchozí reakci na nedostatek kapacity.  
5. V poli Reakce na nedostatek kapacity vyberte Přidat do požadovaného období.
    * Touto možností zajistíte, aby úloha byla přidána do požadovaného období bez ohledu na to, zda je pracovní buňka přetížena.  
6. Klikněte na Plánovat.
    * Všimněte si, že obě úlohy jsou přidány do požadovaného období.  
    * V části Kapacita období můžete vidět zatížení pro jednotlivá období. Pole Spotřeba zobrazí plánovanou spotřebu v tomto období. Pokud je plánovaná spotřeba větší, než kapacita dostupná v tomto období, bude vybrán stav Přetížení spotřeby.  


