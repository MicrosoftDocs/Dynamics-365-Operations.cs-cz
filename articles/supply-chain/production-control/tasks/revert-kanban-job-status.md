---
title: Vrátit stav kanbanové úlohy
description: Tato procedura se zaměřuje na vrácení zpět nesprávného stavu kanbanové úlohy.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 771c3b95be05904c84483473a533c708964fbe62
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574394"
---
# <a name="revert-kanban-job-status"></a>Vrátit stav kanbanové úlohy

[!include [banner](../../includes/banner.md)]

Tato procedura se zaměřuje na vrácení zpět nesprávného stavu kanbanové úlohy. To je užitečné v případě, že operátor stroje aktualizuje nesprávné úlohu nebo omylem nastaví nesprávný stav. V tomto postupu kanbanová úloha je registrována jako připravená omylem a stav se vrátí. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tato procedura je určena pro vedoucího dílny nebo operátora stroje pracující ve společnosti s lean manufacturing.


## <a name="open-process-board-for-the-work-cell"></a>Otevřít desku procesů pro pracovní buňku
1. Přejděte na kanbanovou desku pro úlohy procesu.
2. V poli Pracovní buňka zadejte nebo vyberte hodnotu.
    * Vyberte pracovní buňku 1260.  

## <a name="prepare-kanban-job"></a>Připravit kanbanovou úlohu
1. Klepněte na Připravit.
    * Pokud nemůžete kliknout na Připravit, protože se možnost zobrazuje šedě, zajistěte, aby vybraná kanbanová úloha měla stav Plánováno, který je označen ikonou prázdného kanbanu. Pokud se příprava nezdaří, zkontrolujte, zda jsou všechny materiály k dispozici na výdejce.  
2. Vyberte připravenou úlohu na seznamu.
    * Vyberte první úlohu, kterou jste právě připravili.  
    * Všimněte si, že jsou připraveny úlohy stavu, které jsou označeny trojúhelníkem uvnitř ikony kanbanu.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Vrátit zpět stav připravené kanbanové úlohy
1. Označte v seznamu vybraný řádek.
    * Vyberte první úlohu, která byla připravena.  
2. V podokně akcí klikněte na možnost Vyrobit.
3. Klikněte na Vrátit na stav zpět.
    * Můžete vybrat alternativní kanbanové pravidlo při splnění následujících podmínek:  - Strategie doplnění je stejná pro obě pravidla.  - Verze výrobního toku je stejná pro obě pravidla.  - Produkt, který se dodává, je stejný pro obě pravidla.  - Všechny podřízené činnosti, které jsou konfigurovány pro poslední aktivitu kanbanových pravidel musí být stejné pro obě pravidla.  - Stejné zadané dimenze zásob musí být nakonfigurovány pro obě pravidla.  - Stav manipulační jednotky musí být Nepřiřazeno.  - Konfigurace pro kanbany událostí se musí shodovat.  
    * Ujistěte se, že nový stav je Plánováno.  
4. Klikněte na tlačítko OK.
5. Odznačte vybraný řádek na seznamu.
    * Vyberte stejnou úlohu.  
    * Všimněte si, že stav úlohy pro kanbanovou úlohu bude vrácen zpět na Plánováno, což je označeno ikonou prázdného kanbanu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]