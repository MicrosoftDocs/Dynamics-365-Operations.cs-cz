--- 
title: "Vytvoření dávkové úlohy"
description: "Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS)."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a>Vytvoření dávkové úlohy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS). Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil. Dávkovou úlohu můžete nastavit následujícím postupem. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-the-batch-job"></a>Vytvoření dávkové úlohy
1. Přejděte na Správa systému > Dotazy > Dávkové úlohy.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Popis práce.
4. Do pole Plánované počáteční datum a čas zadejte datum a čas.
5. Klikněte na položku Uložit.

## <a name="create-a-recurrence"></a>Vytvoření opakování
1. V podokně akcí klikněte na možnost Dávková úloha.
2. Klepněte na tlačítko Opakování.
    * Pomocí těchto možností zadejte rozsah a vzor opakování.  
3. Klikněte na tlačítko OK.

## <a name="add-alerts"></a>Přidání výstrah
1. V podokně akcí klikněte na možnost Dávková úloha.
2. Klepněte na tlačítko Výstrahy.
    * Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení. Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.   
3. Klikněte na tlačítko OK.


