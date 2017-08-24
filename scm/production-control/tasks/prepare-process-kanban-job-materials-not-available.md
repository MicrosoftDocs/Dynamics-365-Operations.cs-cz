--- 
title: "Příprava kanbanové úlohy procesu, když pro pracovní buňku nejsou k dispozici materiály"
description: "Tento postup se zaměřuje na přípravu zpracování kanbanové úlohy, když nejsou k dispozici některé materiály pro pracovní buňku, a je tak nutné vybrat materiály ze skladu."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4899c1d0baebb451e665853767e64f660ca25ca6
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Příprava kanbanové úlohy procesu, když pro pracovní buňku nejsou k dispozici materiály

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


