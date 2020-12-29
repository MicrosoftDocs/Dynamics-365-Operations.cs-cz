---
title: Uvolnění výrobní zakázky
description: Tato procedura popisuje způsob uvolnění výrobní zakázky.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beef850e7e58fb58db545c0be5990b52619070d3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423509"
---
# <a name="release-a-production-order"></a>Uvolnění výrobní zakázky

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob uvolnění výrobní zakázky. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o čtvrtou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.

1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
    * V mřížce vyberte výrobní zakázku, která má stav Naplánováno.  
2. V podokně akcí klikněte na možnost Výrobní zakázka.
3. Klikněte na Uvolnit
    * Na této stránce můžete potvrdit uvolnění vybraného rozsahu výrobních zakázek. Klepněte na tlačítko Vybrat, pokud chcete přidat objednávky.  
    * Krok Uvolnění určuje, kdy je výrobní zakázka uvolněna do výrobní dílny, aby operátoři dílny mohli ohlásit postup ve výrobních úlohách. Je možné vydat výrobní doklady mohou obsahovat důležité informace o zpracování úlohy. Skladová práce pro výdej suroviny je vytvořena pro položky, které jsou nastaveny pro skladový proces.  
4. Klepněte na kartuObecné.
    * Vyberte výrobní sestavy, které mají být vytištěny. Sestava úkolových lístků vytiskne stránku pro každou naplánovanou úlohu a vyžaduje, aby byla výrobní zakázka plánována na úrovni projektu. Sestava obsahuje informace o plánovaném počátečním a koncovém čase, množství k výrobě, a informaci o zdrojích, které zpracovávají úlohu. Sestava Úloha postupu shromažďuje stejné informace na stejné stránce, ale nevytiskne stránku pro každou úlohu. Sestava Karta postupu zobrazí pouze operace, ale nikoli úlohy. Tato sestava tedy nevyžaduje plánování úloh, ale lze ji použít při plánování výrobních zakázek na úrovni operací.  
5. Klikněte na pole Tisk karty postupu.
6. Klepněte na tlačítko OK.
7. Zavřete stránku.

