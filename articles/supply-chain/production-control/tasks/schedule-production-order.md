--- 
title: "Naplánování výrobní zakázky"
description: "Tato procedura popisuje způsob plánování výrobní zakázky."
author: johanhoffmann
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 6cbbf509c9e60040e08ab7932fcb0e8eed5ddd22
ms.contentlocale: cs-cz
ms.lasthandoff: 02/06/2018

---
# <a name="schedule-a-production-order"></a>Naplánování výrobní zakázky

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob plánování výrobní zakázky. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o třetí proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.


## <a name="schedule-a-production-order"></a>Naplánování výrobní zakázky
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
    * Vyberte výrobní zakázku, která má stav Odhadováno.  
2. V podokně akcí klikněte na možnost Plán.
3. Klikněte na Plánovat úlohy.
    * Parametry pro plánování se nastavují na této stránce. Můžete nastavit parametry pro konkrétní uživatelé nebo u všech uživatelů.  
4. V poli Způsob plánování vyberte „Vpřed ode dneška“.
5. Do pole Datum plánování zadejte datum.
6. Zaškrtněte políčko Omezená kapacita, nebo jeho zaškrtnutí zrušte.
7. Zaškrtněte políčko Omezený materiál, nebo jeho zaškrtnutí zrušte.
8. Klikněte na tlačítko OK.

## <a name="view-the-scheduling-results"></a>Zobrazte výsledky plánování
1. V podokně akcí klikněte na položku Výrobní zakázka.
2. Klikněte na Všechny úlohy.
    * Tato stránka zobrazuje naplánované úlohy, které jste právě vygenerovali.  
3. Rozbalte nebo sbalte oddíl Plánování.
    * Na pevné záložce Plánování můžete zobrazit plánované datum a čas.  
4. Klepněte na možnost Dotazy.
5. Klikněte na možnost Vytížení kapacity.
    * Na stránce Vytížení kapacity se zobrazí kapacita rezervovaná pomocí plánování práce, celkový počet hodin, které jsou aktuálně rezervovány u prostředku a počet hodin, které jsou nadále k dispozici pro plánování úlohy u prostředku.  
6. Zavřete stránku.
7. Zavřete stránku.


