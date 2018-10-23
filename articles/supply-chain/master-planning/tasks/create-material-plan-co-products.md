--- 
title: "Vytvoření materiálového plánu pro vedlejší produkty"
description: "Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-material-plan-for-co-products"></a>Vytvoření materiálového plánu pro vedlejší produkty

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
1. Zavřete stránku.
2. Zavřete stránku.
3. Klikněte na Hlavní plánování.
4. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
    * Příklad: MasterPlan  
6. Klikněte na položku Spustit.
7. Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.
8. Klepněte na tlačítko Filtr.
9. V seznamu vyberte řádek pro pole = číslo položky.
10. Zadejte hodnotu do pole Kritéria.
    * Příklad: P6003  
11. Klikněte na tlačítko OK.
12. Klikněte na tlačítko OK.
13. Klikněte na Plánované objednávky.
14. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.
    * Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.  
15. Označte v seznamu vybraný řádek.
    * Vyberte libovolné řádky vrácené filtrem.  
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. Rozbalte nebo sbalte oddíl Doložení.
18. Klikněte na odkaz na vybraném řádku v seznamu.
    * Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.  
19. Zavřete stránku.

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
1. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
2. Klikněte na odkaz na vybraném řádku v seznamu.
    * Příklad: MasterPlan  
3. Klikněte na položku Spustit.
4. Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.
5. Klepněte na tlačítko Filtr.
6. V seznamu vyberte řádek pro pole = číslo položky.
7. Zadejte hodnotu do pole Kritéria.
    * Příklad: P6003  
8. Klikněte na tlačítko OK.
9. Klikněte na tlačítko OK.
10. Klikněte na Plánované objednávky.
11. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.
    * Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.  
12. Označte v seznamu vybraný řádek.
    * Vyberte libovolné řádky vrácené filtrem.  
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. Rozbalte nebo sbalte oddíl Doložení.
15. Klikněte na odkaz na vybraném řádku v seznamu.
    * Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.  
16. Zavřete stránku.
17. Klikněte na Hlavní plánování.
18. Přejděte na Hlavní plánování > Nastavení > Parametry hlavního plánování.
19. V poli Zakázat všechny procesy plánování vyberte Ne.
20. Zavřete stránku.


