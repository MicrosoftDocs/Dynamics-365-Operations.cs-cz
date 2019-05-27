---
title: Příprava kanbanové úlohy procesu, když pro pracovní buňku nejsou k dispozici materiály
description: Tento postup se zaměřuje na přípravu zpracování kanbanové úlohy, když nejsou k dispozici některé materiály pro pracovní buňku, a je tak nutné vybrat materiály ze skladu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7e7eb46bda13ef7e72189f921686a9889a8773c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559064"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Příprava kanbanové úlohy procesu, když pro pracovní buňku nejsou k dispozici materiály

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na přípravu zpracování kanbanové úlohy, když nejsou k dispozici některé materiály pro pracovní buňku, a je tak nutné vybrat materiály ze skladu. Postup "Příprava procesní kanbanové úlohy, pokud jsou materiály k dispozici" je předpokladem pro vytvoření tohoto postupu. Tento postup je určen pro operátora stroje. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte na Řízení výroby > Kanban > Kanbanová deska pro úlohy zpracování.
2. V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte pracovní buňku 1250.  
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte Kanban 000356.  
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * V seznamu zrušte výběr řádku 4. nebo vyberte řádek 4, pokud jste nedokončili úkolu "Příprava procesní kanbanové úlohy, jakmile jsou materiály k dispozici."  
6. Přepněte rozšíření oddílu Výdejka.
    * Ikona Žádný záznam ve stavu dodávky udává, že 48 z každé položky P0002 chybí pro pracovní buňku.  

## <a name="transfer-materials-to-work-cell"></a>Převod materiálů do pracovní buňky
1. Přepněte rozšíření oddílu Úlohy převodů.
2. Použijte rychlý filtr k filtrování v poli Číslo položky na základě hodnoty P0002.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na položku Spustit.
    * Probíhá přenos.  
5. Klikněte na tlačítko Dokončit.
    * Položka P0002 je nyní k dispozici na výdejce pro kanbanovou úlohu. To znamená, že můžeme připravit kanban se všemi potřebnými materiály.  
6. Klepněte na Připravit.
    * Všimněte si, že ikona ve stavu úlohy označuje, že úloha je nyní připravena.  

