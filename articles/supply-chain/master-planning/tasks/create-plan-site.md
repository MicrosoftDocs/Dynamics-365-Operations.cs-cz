---
title: Vytvoření plánu pro pracoviště
description: Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52721d948554d4853f9e1d4dec45e45e619a4829
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423831"
---
# <a name="create-a-plan-for-a-site"></a>Vytvoření plánu pro pracoviště

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]