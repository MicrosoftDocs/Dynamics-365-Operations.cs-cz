---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 2 - Konfigurace výpočtů)
description: Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9314a8cd5838333a20dd59dfb52f80a43d89b8c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684684"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 2 - Konfigurace výpočtů)

[!include [banner](../../includes/banner.md)]

Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu. Tyto kroky lze provést v rámci libovolné společnosti.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 1: Vytvoření formátu).

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Vytvoření konfigurace formátu pro přidání podrobností o počítání a sčítání
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
4. Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).
    * Předpokládejme třeba, že potřebujete přizpůsobit formát poskytovaný společností Microsoft přidáním řádků se souhrnnými údaji na konci sestavy Intrastat. Je třeba to provést odvozením vlastní instance konfigurace Intrastat z instance Microsoft k provádění změn.  
5. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
6. V poli Nový zadejte „Odvodit z názvu: Intrastat (DE), Microsoft“.
7. Do pole Název zadejte hodnotu Intrastat (DE) s výpočty a součty.
8. Klepněte na možnost Vytvořit konfiguraci.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Konfigurace sestavy na provádění výpočtů a součtů na základě podrobností výstupu
1. Klikněte na možnost Návrhář.
2. Vyberte možnost Ano v poli Podrobnosti výstupu shromažďování.
    * Tento příznak bude při spuštění aktivovat proces shromažďování podrobnosti výstupu pro generování souboru Intrastat.  
    * Potřebujete provést výpočet pro různé pokyny Intrastat, takže přidejte vyhrazené vyčíslení modelu k seznamu zdrojů dat této konfigurace formátu.  
3. Klikněte na kartu Mapování.
4. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
5. Ve stromovém zobrazení vyberte možnost Datový model\Výčet.
6. Do pole Název zadejte Směr.
7. V poli Výčet modelu zadejte nebo vyberte hodnotu.
    * Vyberte hodnotu Směr.  
8. Klikněte na tlačítko OK.
9. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
10. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
11. Do pole Název zadejte '$BlockName'.
12. Klikněte na možnost Upravit vzorec.
13. Do pole Vzorec zadejte '"block"'.
14. Klikněte na položku Uložit.
15. Zavřete stránku.
16. Klikněte na tlačítko OK.
17. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
18. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
19. Do pole Název zadejte '$RecName'.
20. Klikněte na možnost Upravit vzorec.
21. Do pole Vzorec zadejte '"record"'.
22. Klikněte na položku Uložit.
23. Zavřete stránku.
24. Klikněte na tlačítko OK.
25. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
26. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
27. Do pole Název zadejte '$InvName'.
28. Klikněte na možnost Upravit vzorec.
29. Do pole Vzorec zadejte '"InvoicedAmountEUR"'.
30. Klikněte na položku Uložit.
31. Zavřete stránku.
32. Klikněte na tlačítko OK.
33. Ve stromovém zobrazení vyberte 'Intrastat\Data'.
34. Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat"
35. Klikněte na možnost Přidat datový zdroj.
    * $BlockName  
36. Klepněte na tlačítko Uložit.
37. Zavřete stránku.
38. Klepněte na tlačítko Upravit pro pole Hodnota klíče shromážděných dat.
39. Do pole Vzorec zadejte 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Klikněte na položku Uložit.
41. Zavřete stránku.
    * Spočítejte řádky této sekvence. Výsledky budou použity s názvem "blok" nezávisle pro různé pokyny. Hodnota "Import" se použije pro všechny příchozí transakce Intrastat. Hodnota "Export" se použije pro všechny odchozí transakce Intrastat. Zvažte použití virtuální tabulky aplikace Excel. Pro každou transakci vytvořte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export".  
42. Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí“.
43. Ve stromovém zobrazení vyberte 'Intrastat\Data: Pořadí\Příjezdy?'.
44. Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat".
    * Spočítejte řádky této sekvence. Výsledky budou uloženy do paměti s názvem "záznam".  
45. Ve stromovém zobrazení vyberte '$RecName'.
46. Klikněte na možnost Přidat datový zdroj.
47. Klepněte na tlačítko Uložit.
48. Zavřete stránku.
49. Klepněte na tlačítko Upravit pro pole 'Hodnota klíče shromážděných dat'
50. Do pole Vzorec zadejte "Intrastat.CommodityRecord.CommodityCode".
51. Klikněte na položku Uložit.
52. Zavřete stránku.
    * Spočítejte řádky této sekvence. Výsledky budou použity s názvem "záznam" nezávisle pro různé kódy komodit. Zvažte použití virtuální tabulky aplikace Excel. Pro každou transakci použijte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export", a ve druhém záznamu bloku hodnota kódu komodity.  
53. Ve stromovém zobrazení vyberte 'Intrastat\Data: Pořadí\Expedice?'.
54. Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat"
55. Ve stromovém zobrazení vyberte '$RecName'.
56. Klikněte na možnost Přidat datový zdroj.
57. Klepněte na tlačítko Uložit.
58. Zavřete stránku.
59. Klepněte na tlačítko Upravit pro pole 'Hodnota klíče shromážděných dat'.
60. Do pole Vzorec zadejte "Intrastat.CommodityRecord.CommodityCode".
61. Klepněte na tlačítko Uložit.
62. Zavřete stránku.
63. Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí\Expedice: Pořadí?“.
64. Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí\Expedice: Pořadí?\Záznam = Intrastat.CommodityRecord“.
65. Klikněte na kartu Formát.
66. Ve stromové struktuře vyberte "Intrastat\Data\Expedice\Záznam\Částka faktury EUR".
67. Klikněte na kartu Mapování.
68. Klepněte na tlačítko Upravit pro pole 'Název klíče shromážděných dat'.
69. Ve stromovém zobrazení vyberte '$InvName'.
70. Klikněte na možnost Přidat datový zdroj.
71. Klikněte na položku Uložit.
72. Zavřete stránku.
    * Sečtěte hodnoty fakturované částky pro řádky této sekvence. Výsledky budou použity s názvem "InvoicedAmountEUR" nezávisle pro různé pokyny Intrastat a kódy komodit. Zvažte vytvoření virtuální tabulky aplikace Excel. Pro každou transakci vytvořte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export". Druhý blok "záznam" je vyplněn hodnotou kódu komodity a třetí sloupec, který "InvoicedAmountEUR" je vyplněn hodnotou částky faktury.  
73. Ve stromovém zobrazení rozbalte „Intrastat\Data\Příjezdy?“.
74. Ve stromovém zobrazení rozbalte „Intrastat\Data\Příjezdy?\Záznam = Intrastat.CommodityRecord“.
75. Klikněte na kartu Formát.
76. Ve stromové struktuře vyberte "Intrastat\Data\Příjezdy\Záznam\Částka faktury EUR".
77. Klikněte na kartu Mapování.
78. Klepněte na tlačítko Upravit pro pole 'Název klíče shromážděných dat'.
79. Ve stromovém zobrazení vyberte '$InvName'.
80. Klikněte na možnost Přidat datový zdroj.
81. Klikněte na položku Uložit.
82. Zavřete stránku.
83. Klikněte na položku Uložit.
84. Zavřete stránku.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]