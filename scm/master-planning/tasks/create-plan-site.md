--- 
title: "Vytvoření plánu pro pracoviště"
description: "Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d89d34d4d429faf87c70943961f7141a6258d482
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-plan-for-a-site"></a>Vytvoření plánu pro pracoviště

[!include[task guide banner](../../includes/task-guide-banner.md)]

Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky. Po vytvoření zdrojových návrhy poté vyhledá objednávky pro pracoviště, pro které realizuje plánování a potvrdí objednávky počínaje od těch nejnaléhavějších. Nejvíce naléhavé objednávky jsou ty, které je třeba potvrdit k aktuálnímu datu. Pro tyto úkoly použijte ukázková data společnosti USMF.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Vytváření materiálů a plánu kapacity pro položku
1. Klikněte na Hlavní plánování.
    * Je nutné přejít na výchozí řídicí panel.  
2. Klikněte na položku Spustit.
3. Rozbalte oddíl Záznamy k zahrnutí.
4. Klepněte na tlačítko Filtr.
5. Označte v seznamu vybraný řádek.
6. Zadejte hodnotu do pole Kritéria.
    * Příklad: D0001  
7. Klikněte na tlačítko OK.
8. Klikněte na tlačítko OK.
    * Tento proces může trvat několik minut.  
9. Aktualizujte stránku.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Identifikace naléhavých plánovaných objednávek pro položku
1. Otevřete filtrování sloupce s číslem položky.
2. Použijte filtr v poli Číslo položky, s hodnotou D0001 a za použití operátoru filtru "začíná".
3. Otevřete filtr sloupce Datum objednávky.
4. Použijte filtr v poli "Datum objednávky" s hodnotou aktuálního data za pomoci operátoru filtru "je přesně".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Potvrzení všech naléhavých objednávek pro položku
1. V seznamu označte všechny řádky nebo jejich označení zrušte.
2. Klikněte na položku Potvrdit.
3. Klikněte na tlačítko OK.


