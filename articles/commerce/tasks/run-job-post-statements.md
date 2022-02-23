---
title: Konfigurace a spuštění úlohy pro zaúčtování výkazů
description: Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410815"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurace a spuštění úlohy pro zaúčtování výkazů

[!include [banner](../includes/banner.md)]

Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů. Tato procedura používá v ukázkových datech společnost USRT.

1. Přejděte na Všechny pracovní prostory > .. > Finance obchodu.
2. Klikněte na Zaúčtovat příkazy v dávkách.
    * Vyberte organizační hierarchii a poté ve stromu uzlů organizace vyberte jednotlivý obchod nebo do uzel. Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte uzel.  
    * Kliknutím na šipku přidejte výběr.  
3. Klikněte na kartu Spustit na pozadí. ![Spustit na pozadí](../dev-itpro/media/runbackground.png "Spustit na pozadí") 
4. Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.
![Dávkové zpracování](../dev-itpro/media/batchprocessing.png "Dávkové zpracování a opakování") 
5. Klepněte na tlačítko Opakování.
6. Zadejte datum do pole Počáteční datum.
7. Zadejte čas do pole Počáteční čas.
    * Vyberte, zda chcete ukončit opakování po určitém počtu opakování, v konkrétním datu, nebo nikdy. Poté pomocí výběru různých možností definujte, jak často chcete úlohu provádět.  
8. Klepněte na tlačítko OK.
9. Klepněte na tlačítko OK.

