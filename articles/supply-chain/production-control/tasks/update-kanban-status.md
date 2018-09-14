--- 
title: Aktualizace stavu kanbanu
description: "Pokud dojde omylem k vyprázdnění kanbanu nebo přijatý kanban musí být prázdný, je nutné aktualizovat stav kanbanu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="update-kanban-status"></a>Aktualizace stavu kanbanu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pokud dojde omylem k vyprázdnění kanbanu nebo přijatý kanban musí být prázdný, je nutné aktualizovat stav kanbanu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro vedoucího dílny.


## <a name="find-the-kanban"></a>Vyhledejte kanban.
1. Přejděte na Řízení výroby > Kanban > Kanbany.
2. Otevřete filtr sloupce Stav manipulační jednotky.
3. Klikněte na tlačítko Vymazat.
    * To obnoví hodnoty filtrů.  
4. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo karty pomocí hodnoty „000149“.

## <a name="change-emptied-status-to-received-status"></a>Změna stavu Vyprázdněno na Přijato
1. Klikněte na Stornovat prázdnou manipulační jednotku.
2. Klikněte na tlačítko OK.
    * Všimněte si, že stav manipulační jednotky je Přijato.  

## <a name="change-received-status-to-emptied-status"></a>Změna stavu Přijato na Vyprázdněno
1. Klikněte na Prázdný kanban.
2. Označte v seznamu vybraný řádek.
    * Všimněte si, že stav manipulační jednotky je Vyprázdněno.  


