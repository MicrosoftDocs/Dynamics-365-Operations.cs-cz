---
title: Naplánování výrobní zakázky
description: Tato procedura popisuje způsob plánování výrobní zakázky.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3956be08b08e974f1cbd269d97699d60769d6eac28bd2700313cf587c25474ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773999"
---
# <a name="schedule-a-production-order"></a>Naplánování výrobní zakázky

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]