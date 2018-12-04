--- 
title: "Převedení materiálu s kanbanovými úlohami"
description: "Tento postup se zaměřuje na provádění kanbanové úlohy pro výběr umožňující převod materiálu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a2db7b9fb960beb5b4a851aabb9f28a0f9e3d3da
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="transfer-materials-with-kanban-jobs"></a>Převedení materiálu s kanbanovými úlohami

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na provádění kanbanové úlohy pro výběr umožňující převod materiálu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup je určen pro pracovníka skladu.


## <a name="display-transfer-jobs"></a>Zobrazení úloh převodu
1. Přejděte na Řízení výroby > Kanban > Kanbanová deska pro úlohy převodu.
2. Rozbalte nebo sbalte oddíl Filtry.
    * V části Filtry můžete určit, jaké úlohy chcete zobrazit filtrováním výrobního toku, názvu aktivity, původu (ze skladu a umístění) a cíle (do skladu a umístění).  
3. Zadejte hodnotu 11 do pole Ze skladu.
4. Zadejte hodnotu 12 do pole Do umístění.

## <a name="start-a-transfer-job"></a>Zahájit úlohu převodu
1. Odznačte případně vybraný řádek na seznamu.
2. Vyberte ze seznamu řádek 4.
    * Vyberte první úlohu se stavem Neplánováno. Ujistěte se, že se jedná o jedinou vybranou úlohu.  
3. Klikněte na položku Spustit.
    * Všimněte si, že ikona označuje, zda je úloha spuštěna.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Výběr druhé úlohy převodu a změna množství
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Můžete mít vybraných více úloh, ale nyní vyberte řádek 5.  
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Ujistěte se, že je vybrána pouze úloha v předchozím kroku. Zrušte všechny ostatní úlohy.  
3. Poznamenejte si hodnotu v poli Množství úlohy pro pozdější potřebu.
4. Nastavte Množství úlohy na „30“.
    * Všimněte si upozornění. Nemáte oprávnění převést 30. Podle nastavení kanbanového pravidla lze převést pouze původní množství.  
5. Použijte hodnotu pole Množství úlohy, kterou jste si dříve zapsali.
    * Nastavte Množství úlohy na předchozí hodnotu.  

## <a name="start-the-second-transfer-job"></a>Spuštění druhé úlohy převodu
1. Klikněte na položku Spustit.
    * Tato akce spustí převod úlohy z řádku 5.  

## <a name="complete-both-transfer-jobs"></a>Dokončení obou úloh převodu
1. Vyberte ze seznamu řádek 4.
    * Nyní jsou vybrány dvě úlohy převodu – na řádku 4 a 5.  
2. Klikněte na tlačítko Dokončit.
    * Tímto dokončíte převod obou úloh.  


