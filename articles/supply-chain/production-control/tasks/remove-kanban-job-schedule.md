--- 
title: "Odebrání kanbanové úlohy z plánu"
description: "Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Odebrání kanbanové úlohy z plánu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro dílenského nadřízeného nebo plánovače výroby.


## <a name="find-a-planned-kanban-job"></a>Vyhledání plánované kanbanové úlohy
1. Přejděte na Řízení výroby > Kanban > Plánování kanbanové úlohy.
2. V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte pracovní buňku 1250.  
4. Klepněte na tlačítko Vybrat.
5. V poli Zobrazit stav úlohy vyberte hodnotu Plánováno.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Odebrání plánované kanbanové úlohy z plánu
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte úlohu se stavem Plánováno, například práci ze dne 19. prosince 2012.  
2. V podokně akcí klikněte na položku Plán.
3. Klikněte na Vrátit stav úlohy.
4. Klikněte na tlačítko OK.
    * Tím vrátíte aktuální stav úlohy ze stavu Plánováno na Neplánováno a odeberete ji z panelu procesů.   


