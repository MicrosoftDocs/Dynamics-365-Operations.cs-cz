---
title: Provádění úloh kanbanových procesů
description: Tento postup se zaměřuje na realizaci úloh kanbanových procesů.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ebae3fac556348aafa595e6e21caf9cd6b44ba4
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149014"
---
# <a name="execute-kanban-process-jobs"></a>Provádění úloh kanbanových procesů

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na realizaci úloh kanbanových procesů. První úloha je dokončena s očekávaným množstvím a bez chyb. Druhá úloha je dokončena s chybami. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro operátora stroje.


## <a name="select-a-kanban-job"></a>Vyberte kanbanovou úlohu.
1. Přejděte na Řízení výroby > Kanban > Kanbanová deska pro úlohy zpracování.
2. V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klepněte na řádek se skupinou prostředků 1250. To způsobí filtrování seznamu úloh a zobrazíte tak pouze úlohy pro pracovní buňku 1250.
    * Označte řádek, který má stav plánované úlohy.  

## <a name="complete-a-job-with-expected-quantity"></a>Dokončení úlohy s očekávaným množstvím
1. Rozbalte nebo sbalte oddíl Podrobnosti.
    * Tento oddíl uvádí důležité informace o číslu karty, číslu položky, objednaném množství a názvu aktivity.  
2. Rozbalte nebo sbalte oddíl Pokyny pro výrobu.
    * Tyto pokyny popisují výrobní pokyny pro aktivitu. Pokyny mohou být text, obrázky, výkresy nebo další dokumenty.  
3. Klikněte na položku Spustit.
    * Vyberte úlohu, která není dokončena. Pomocí ikony Stav v poli Stav úlohy můžete zobrazit stav úlohy.      
4. Klikněte na tlačítko Dokončit.
    * Dokončení úlohy proběhne s očekávanou kvalitou.  

## <a name="complete-a-job-with-errors"></a>Dokončení úlohy s chybami
1. Klikněte na položku Spustit.
    * Po dokončení úlohy se automaticky vybere následující úloha v seznamu. Z tohoto důvodu nemusíte vybírat úlohu před klepnutím na tlačítko Spustit.  
2. V podokně akcí klikněte na možnost Vyrobit.
3. Klikněte na Dokončení (podrobnosti).
4. Označte na seznamu vybraný řádek.
5. V poli Chyba v množství zadejte číslo.
6. V poli Bezchybné množství zadejte číslo.
7. Klikněte na tlačítko OK.

