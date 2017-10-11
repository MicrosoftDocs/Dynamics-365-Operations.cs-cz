--- 
title: "Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022"
description: "Tento postup ukazuje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16c2af862a73047a2e6ebdc056275392fa8a0d93
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022. 

K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.

Toto je pátý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="create-payment-lines"></a>Vytvoření řádků platby
1. Přejděte na Závazky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. V poli Název zadejte nebo vyberte hodnotu.
5. Klikněte na položku Řádky.
6. Klikněte na Návrh platby.
7. Klikněte na Vytvořit návrh plateb.
8. Rozbalte oddíl Záznamy k zahrnutí.
9. Klepněte na tlačítko Filtr.
10. V seznamu vyberte řádek pro tabulku dodavatelů a pole Účet dodavatele.
11. V poli Kritéria zadejte nebo vyberte hodnotu.
    * Můžete použít všechna kritéria pro výběr transakcí dodavatele k zaplacení. Pro tento příklad použijte DE-001 jako účet dodavatele.  
12. Klikněte na tlačítko OK.
13. Klikněte na tlačítko OK.
14. Klikněte na Vytvořit platby.

## <a name="generate-an-iso20022-payment-file"></a>Vygenerování souboru platby ISO20022

