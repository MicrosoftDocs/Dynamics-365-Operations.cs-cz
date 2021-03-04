---
title: Odebrání kanbanové úlohy z plánu
description: Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423508"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Odebrání kanbanové úlohy z plánu

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]