---
title: Konfigurace a spuštění úlohy pro zaúčtování výkazů
description: Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfff9e4520659ac1a9d0f85dd0e091f9fa5e2528ff092b650296a47aef9ca7b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765848"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurace a spuštění úlohy pro zaúčtování výkazů

[!include [banner](../includes/banner.md)]

Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů. Tato procedura používá v ukázkových datech společnost USRT.

1. Přejděte na Všechny pracovní prostory > .. > Finance obchodu.
2. Klikněte na Zaúčtovat příkazy v dávkách.
    * Vyberte organizační hierarchii a poté ve stromu uzlů organizace vyberte jednotlivý obchod nebo do uzel. Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte uzel.  
    * Kliknutím na šipku přidejte výběr.  
3. Klikněte na kartu Spustit na pozadí. ![Spustit na pozadí.](../dev-itpro/media/runbackground.png "Spustit na pozadí") 
4. Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.
![Dávkové zpracování.](../dev-itpro/media/batchprocessing.png "Dávkové zpracování a opakování") 
5. Klepněte na tlačítko Opakování.
6. Zadejte datum do pole Počáteční datum.
7. Zadejte čas do pole Počáteční čas.
    * Vyberte, zda chcete ukončit opakování po určitém počtu opakování, v konkrétním datu, nebo nikdy. Poté pomocí výběru různých možností definujte, jak často chcete úlohu provádět.  
8. Klepněte na tlačítko OK.
9. Klepněte na tlačítko OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]