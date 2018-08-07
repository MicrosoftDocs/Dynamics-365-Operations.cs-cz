---
title: "Uvolnění výrobní zakázky"
description: "Tato procedura popisuje způsob uvolnění výrobní zakázky."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 6e628d8564c093c5d75fffe268b2107262d508c3
ms.contentlocale: cs-cz
ms.lasthandoff: 02/06/2018

---
# <a name="release-a-production-order"></a>Uvolnění výrobní zakázky

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

