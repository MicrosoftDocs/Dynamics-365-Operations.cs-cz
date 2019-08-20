---
title: Vytvoření surovin (únor 2016)
description: Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844578"
---
# <a name="create-raw-materials-february-2016"></a>Vytvoření surovin (únor 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů. Je to třetí úloha v řadě Kalkulace kusovníku. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.


## <a name="create-the-first-material"></a>Vytvoření prvního materiálu
1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Číslo produktu.
    * V tomto příkladu zadejte ITEM_A.  
4. V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.
    * Vyberte volbu „STD“. STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.  
5. V poli Skupina zboží zadejte nebo vyberte hodnotu.
    * Vyberte například Audio. To nemá žádný vliv na výpočty nákladů.  
6. V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.
    * Vyberte SiteWH. Pro ukázku se použije pouze Pracoviště a Sklad.  
7. V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.
    * Sledovací dimenze v tomto příkladu nebudou použity. Zvolte Žádné.  
8. Klikněte na tlačítko OK.
9. V podokně akcí klikněte na možnost Spravovat sklad.
10. Klikněte na Výchozí nastavení objednávky.
11. V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
12. V poli Skladové pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
13. V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
14. Zavřete stránku.
15. Zavřete stránku.
16. Klikněte na odkaz na vybraném řádku v seznamu.
    * Klikněte na ITEM_A.  
17. Rozbalte oblast Správa nákladů.
18. Zadejte hodnotu do pole Nákladová skupina.
    * V tomto příkladu zadejte M2.  
19. V podokně akcí klikněte na možnost Spravovat náklady.
20. Klikněte na možnost Cena položky.
21. Klikněte na položku Nová.
22. V poli Verze zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte 10, což je typ výpočtu standardních nákladů.  
23. V poli Lokalita zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
24. Zadejte číslo do pole Cena.
    * V tomto příkladu zadejte 10.  
25. Klikněte na položku Uložit.
26. Klikněte na Aktivovat nezpracované ceny.
27. Zavřete stránku.
28. Zavřete stránku.

## <a name="create-the-second-material"></a>Vytvoření druhého materiálu
1. Klikněte na položku Nová.
2. Zadejte hodnotu do pole Číslo produktu.
    * V tomto příkladu zadejte ITEM_B.  
3. V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.
    * Vyberte volbu „STD“. STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.  
4. V poli Skupina zboží zadejte nebo vyberte hodnotu.
    * Vyberte například Audio. To nemá žádný vliv na výpočty nákladů.  
5. V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.
    * Vyberte SiteWH. Pro tento příklad se použije pouze Pracoviště a Sklad.  
6. V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.
    * Sledovací dimenze v tomto příkladu nebudou použity. Zvolte Žádné.  
7. Klikněte na tlačítko OK.
8. V podokně akcí klikněte na možnost Spravovat sklad.
9. Klikněte na Výchozí nastavení objednávky.
10. V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
11. V poli Skladové pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
12. V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
13. Zavřete stránku.
14. Zavřete stránku.
15. Klikněte na odkaz na vybraném řádku v seznamu.
    * Klikněte na ITEM_B.  
16. Rozbalte oblast Správa nákladů.
17. Zadejte hodnotu do pole Nákladová skupina.
    * V tomto příkladu zadejte M2.  
18. V podokně akcí klikněte na možnost Spravovat náklady.
19. Klikněte na možnost Cena položky.
20. Klikněte na položku Nová.
21. V poli Verze zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte 10. Jedná se o typ výpočtu standardních nákladů.  
22. V poli Lokalita zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
23. Zadejte číslo do pole Cena.
    * Pro ukázku zadejte 10.  
24. Klikněte na položku Uložit.
25. Klikněte na Aktivovat nezpracované ceny.
26. Zavřete stránku.
27. Zavřete stránku.

## <a name="create-the-third-material"></a>Vytvoření třetího materiálu
1. Klikněte na položku Nová.
2. Zadejte hodnotu do pole Číslo produktu.
    * Pro ukázku zadejte ITEM_C  
3. V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.
    * Vyberte volbu „STD“. STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.  
4. V poli Skupina zboží zadejte nebo vyberte hodnotu.
    * Vyberte například Audio. To nemá žádný vliv na výpočty nákladů.  
5. V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.
    * Vyberte SiteWH. Pro ukázku se použije pouze Pracoviště a Sklad.  
6. V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.
    * Sledovací dimenze v tomto příkladu nebudou použity. Zvolte Žádné.  
7. Klikněte na tlačítko OK.
8. V podokně akcí klikněte na možnost Spravovat sklad.
9. Klikněte na Výchozí nastavení objednávky.
10. V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
11. V poli Skladové pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
12. V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
13. Zavřete stránku.
14. Zavřete stránku.
15. Klikněte na odkaz na vybraném řádku v seznamu.
    * Klikněte na ITEM_C.  
16. Rozbalte oblast Správa nákladů.
17. Zadejte hodnotu do pole Nákladová skupina.
    * V tomto příkladu zadejte M1.  
18. V podokně akcí klikněte na možnost Spravovat náklady.
19. Klikněte na možnost Cena položky.
20. Klikněte na položku Nová.
21. V poli Verze zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte 10. Jedná se o typ výpočtu standardních nákladů.  
22. V poli Lokalita zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Pracoviště 1.  
23. Zadejte číslo do pole Cena.
    * V tomto příkladu zadejte 10.  
24. Klikněte na položku Uložit.
25. Klikněte na Aktivovat nezpracované ceny.
26. Zavřete stránku.
27. Zavřete stránku.

