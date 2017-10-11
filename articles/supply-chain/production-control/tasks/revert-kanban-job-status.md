--- 
title: "Vrátit stav kanbanové úlohy"
description: "Tato procedura se zaměřuje na vrácení zpět nesprávného stavu kanbanové úlohy."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 00b6ae872e60a322c994420ab69236abef7fb312
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="revert-kanban-job-status"></a>Vrátit stav kanbanové úlohy

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

