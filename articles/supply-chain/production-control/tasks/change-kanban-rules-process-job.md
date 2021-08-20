---
title: Změna kanbanových pravidel pro úlohu procesu
description: Tato procedura se zaměřuje na změnu použitého kanbanového pravidla pro daný kanban.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a76d003b60f699e5e8315a4a61390443567cacb2a13bc3735da578c0d8bc26a4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772441"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Změna kanbanových pravidel pro úlohu procesu

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]