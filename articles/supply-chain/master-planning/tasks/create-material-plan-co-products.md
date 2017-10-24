--- 
title: "Vytvoření materiálového plánu pro vedlejší produkty"
description: "Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Vytvoření materiálového plánu pro vedlejší produkty

[!include[task guide banner](../../includes/task-guide-banner.md)]

Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury. K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.


## <a name="create-requirement-for-a-co-product"></a>Vytvoření požadavku pro vedlejší produkt
1. Přejděte na výchozí řídicí panel.
2. Klikněte na Zpracování a dotaz na prodejní objednávku.
3. Klepněte na možnost Nový.
4. Klikněte na Prodejní objednávka.
5. V poli Účet odběratele zadejte hodnotu.
    * Příklad: US-001  
6. Klikněte na tlačítko OK.
7. Zadejte hodnotu do pole Číslo zboží.
    * Příklad: P6003  
8. Zadejte číslo do pole Množství.
    * Příklad: 50000  
9. Klikněte na položku Uložit.

## <a name="create-a-material-plan-for-co-products"></a>Vytvoření materiálového plánu pro vedlejší produkty
1. Klikněte na Hlavní plánování.
2. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Příklad: MasterPlan  
4. Klikněte na položku Spustit.
5. Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.
6. Klepněte na tlačítko Filtr.
7. V seznamu vyberte řádek pro pole = číslo položky.
8. Zadejte hodnotu do pole Kritéria.
    * Příklad: P6003  
9. Klikněte na tlačítko OK.
10. Klikněte na tlačítko OK.
11. Klikněte na Plánované objednávky.
12. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.
    * Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.  
13. Označte v seznamu vybraný řádek.
    * Vyberte libovolné řádky vrácené filtrem.  
14. Klikněte na odkaz na vybraném řádku v seznamu.
15. Rozbalte nebo sbalte oddíl Doložení.
16. Klikněte na odkaz na vybraném řádku v seznamu.
    * Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.  
17. Zavřete stránku.


