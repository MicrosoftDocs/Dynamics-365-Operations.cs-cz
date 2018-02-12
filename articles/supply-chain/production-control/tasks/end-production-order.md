---
title: "Ukončení výrobní zakázky"
description: "Tato procedura popisuje způsob ukončení výrobní zakázky."
author: johanhoffmann
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
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 75b91ea330258a5b57e9e58cb32539d57e458f28
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="end-a-production-order"></a>Ukončení výrobní zakázky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob ukončení výrobní zakázky. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o poslední proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.


## <a name="end-a-production-order"></a>Ukončení výrobní zakázky
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
    * Vyberte výrobní zakázku, která má stav Vykázáno jako dokončený.  
2. V podokně akcí klikněte na položku Výrobní zakázka.
3. Klepněte na tlačítko Konec.
    * Na této stránce můžete potvrdit, že chcete ukončit výrobní zakázku.  
4. Klikněte na záložku Obecné.
5. Do pole Datum zadejte datum.
6. V poli Metoda odpadu vyberte „Přidělení“
    * Pokud vyberete Metodu přidělení, náklady za sešrotovaný materiál budou přidány k dokončenému zboží.  
7. Klikněte na tlačítko OK.

## <a name="validate-calculation-results"></a>Ověření výsledků výpočtu
1. V podokně akcí klikněte na možnost Spravovat náklady.
2. Klikněte na Zobrazit porovnání nákladů.
    * Po ukončení výrobní zakázky budete mít můžete porovnat odhadovanou cenu nákladu proti skutečné ceně nákladů, abyste získali přehled o výrobních odchylkách.  

