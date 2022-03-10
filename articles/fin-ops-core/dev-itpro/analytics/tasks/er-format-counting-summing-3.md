---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 3 - Použití výpočtů k vytvoření výstupu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a59dc2ff4e4e2092911e0aec092ae8182f7601413fc220fda47766a3a0bc061
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718278"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 3 - Použití výpočtů k vytvoření výstupu)

[!include [banner](../../includes/banner.md)]

Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu. Tyto kroky lze provést v rámci libovolné společnosti.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 2: Konfigurace výpočtů).

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Konfigurace sestavy na používání informací o počítání a sčítání
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
4. Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).
5. Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
6. Klikněte na možnost Návrhář.
7. Klikněte na kartu Mapování.
8. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
    * Přidejte nový zdroj dat, abyste získali seznam bloků uložených do paměti.  
9. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
10. Do pole Název zadejte '$BlocksList'.
    * $BlocksList  
11. Klikněte na možnost Upravit vzorec.
12. Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COLLECTEDLIST'.
13. Klikněte na možnost Přidat funkci.
14. Klikněte na možnost Přidat datový zdroj.
15. Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', '.
    * COLLECTEDLIST('$BlockName',  
16. Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', "*")'.
    * COLLECTEDLIST('$BlockName', "*")  
17. Klepněte na tlačítko Uložit.
    * Vzorec "*" znamená, že všechny bloky budou zahrnuty do seznamu pro tento záznam.  
18. Zavřete stránku.
19. Klikněte na tlačítko OK.
20. Klikněte na kartu Formát.
21. Ve stromovém zobrazení vyberte 'Intrastat\Data'.
22. Klepnutím na možnost Přidat otevřete dialogové okno.
23. Ve stromovém zobrazení vyberte 'Text\Pořadí'.
24. Do pole Název zadejte 'Součty podle bloků'.
    * Součty podle bloků  
25. V poli speciální znaky vyberte "Nový řádek – Windows (CR LF)".
26. Klepněte na tlačítko OK.
27. Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků'.
28. Klepnutím na možnost Přidat otevřete dialogové okno.
29. Ve stromovém zobrazení vyberte „Text\Řetězec“.
30. Do pole Název zadejte Kód bloku.
    * Kód bloku  
31. Klikněte na tlačítko OK.
32. Klepněte na tlačítko Přidat řetězec.
33. Do pole Název zadejte Počítání řádků.
    * Počítání řádků  
34. Klikněte na tlačítko OK.
35. Klepněte na tlačítko Přidat řetězec.
36. Do pole Název zadejte „Celková částka“.
    * Celková částka  
37. Klikněte na tlačítko OK.
38. Klikněte na kartu Mapování.
39. Ve stromovém zobrazení vyberte '$BlocksList'.
40. Klikněte na možnost Vazba.
    * Vytvořte souhrnný řádek pro každý blok uložený do paměti.  
41. Klikněte na kartu Formát.
42. Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Kód bloku'.
43. Klikněte na kartu Mapování.
44. Klikněte na možnost Upravit vzorec.
45. Do pole Vzorec zadejte '"ID bloku: " & '.
    * "ID bloku: " &  
46. Ve stromovém zobrazení rozbalte '$BlocksList'.
47. Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'
48. Klikněte na možnost Přidat datový zdroj.
49. Klikněte na položku Uložit.
50. Zavřete stránku.
51. Klikněte na kartu Formát.
52. Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Počítání řádků'.
53. Klikněte na kartu Mapování.
54. Klikněte na možnost Upravit vzorec.
    * Vytvořte výstup pro počet řádků pro každý blok prezentovaný v této sestavě.  
55. V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku:" & '.
    * "Počet řádků v tomto bloku: " &  
56. V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT('.
    * "Počet řádků v tomto bloku: " & TEXT(  
57. Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COUNTIFS'.
58. Klikněte na možnost Přidat funkci.
59. Klikněte na možnost Přidat datový zdroj.
60. V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '.
    * "Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName',  
61. Ve stromovém zobrazení rozbalte '$BlocksList'.
62. Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'
63. Klikněte na možnost Přidat datový zdroj.
64. V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.
    * "Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Ve stromovém zobrazení vyberte '$RecName'.
66. Klikněte na možnost Přidat datový zdroj.
67. V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Klikněte na položku Uložit.
69. Zavřete stránku.
70. Klikněte na kartu Formát.
71. Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Celková částka'.
72. Klikněte na kartu Mapování.
73. Klikněte na možnost Upravit vzorec.
    * Vytvořte výstup, který bude představovat součet fakturované částky pro každý blok v této sestavě.  
74. Do pole Vzorec zadejte '"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Klikněte na položku Uložit.
76. Zavřete stránku.
77. Klikněte na položku Uložit.
78. Zavřete stránku.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]