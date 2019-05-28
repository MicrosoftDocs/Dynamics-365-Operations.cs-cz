---
title: Změna kanbanových pravidel pro úlohu procesu
description: Tato procedura se zaměřuje na změnu použitého kanbanového pravidla pro daný kanban.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554265"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Změna kanbanových pravidel pro úlohu procesu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura se zaměřuje na změnu použitého kanbanového pravidla pro daný kanban. To je užitečné pro nastavení úrovní prostředků vytížení nebo v případě rozúčtování. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tato procedura je určena pro plánovače, který pracuje ve společnosti se štíhlou výrobou a odpovídá za hodnotový proud.


## <a name="copy-kanban-rule"></a>Zkopírujte kanbanové pravidlo
1. Otevřete Kanbanová pravidla.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte Kanbanové pravidlo události 000022 pro L0001.  
3. Klepněte na Duplicitní kanbanové pravidlo.
4. Klikněte na tlačítko OK.

## <a name="change-kanban-rule"></a>Změňte kanbanové pravidlo
1. Zavřete stránku.
2. Přejděte na Plánování kanbanové úlohy.
3. Označte v seznamu vybraný řádek.
    * Vyberte řádek s kanbanem 000177.  
4. Klikněte na Použít alternativní kanbanové pravidlo.
5. Klepněte na tlačítko Další.
6. V poli Kanbanové pravidlo zadejte nebo vyberte hodnotu.
    * Vyberte kanbanové pravidlo, které bylo vytvořeno dříve. Jedná se o kanbanové pravidlo s nejvyšším číslem.  
7. Klepněte na tlačítko Dokončit.
    * Kanbanová úloha používá jiné kanbanové pravidlo. To může být užitečné na úrovni pracovních buněk vytížení.  

