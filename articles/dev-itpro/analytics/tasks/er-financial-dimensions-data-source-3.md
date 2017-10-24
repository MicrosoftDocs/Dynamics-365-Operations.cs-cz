--- 
title: "Návrh sestavy k používání finančních dimenzí jako zdroje dat pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c67bf235f3514a19893bcefcaae6e3bb11bbb151
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Návrh sestavy k používání finančních dimenzí jako zdroje dat pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 2: Mapování modelu").


## <a name="design-a-report-to-present-financial-dimensions"></a>Návrh sestavy k předložení finančních dimenzí
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.
3. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
4. V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".
    * Použijte model vytvořený předem jako zdroj dat pro novou sestavu.  
5. Do pole Název zadejte 'Sestava deníku hlavní knihy'.
6. V poli Definice datového modelu vyberte Položka.
7. Klepněte na možnost Vytvořit konfiguraci.
8. Klikněte na možnost Návrhář.
9. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
10. Ve stromovém zobrazení vyberte „XML\Prvek“.
11. Do pole Název zadejte Kořen.
12. Klepněte na tlačítko OK.
13. Klepnutím na možnost Přidat otevřete dialogové okno.
14. Ve stromovém zobrazení vyberte „XML\Atribut“.
15. Do pole Název zadejte text „Společnost“.
16. Klepněte na tlačítko OK.
17. Klepnutím na možnost Přidat otevřete dialogové okno.
18. Ve stromovém zobrazení vyberte „XML\Prvek“.
19. Do pole Název zadejte Deník.
20. Klepněte na tlačítko OK.
21. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.
22. Klepnutím na možnost Přidat otevřete dialogové okno.
23. Ve stromovém zobrazení vyberte „XML\Atribut“.
24. Do pole Název zadejte Dávka.
25. Klepněte na tlačítko OK.
26. Klepnutím na možnost Přidat otevřete dialogové okno.
27. Ve stromovém zobrazení vyberte „XML\Prvek“.
28. Do pole Název zadejte Transakce.
29. Klepněte na tlačítko OK.
30. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.
31. Klepnutím na možnost Přidat otevřete dialogové okno.
32. Ve stromovém zobrazení vyberte „XML\Atribut“.
33. Do pole Název zadejte Doklad.
34. Klikněte na tlačítko OK.
35. Klikněte na možnost Přidat atributy.
36. Do pole Název zadejte Datum.
37. Klikněte na tlačítko OK.
38. Klikněte na možnost Přidat atributy.
39. Do pole Název zadejte Měna.
40. Klikněte na tlačítko OK.
41. Klikněte na možnost Přidat atributy.
42. Do pole Název zadejte 'Dt'.
43. Klikněte na tlačítko OK.
44. Klikněte na možnost Přidat atributy.
45. Do pole název zadejte 'Ct'.
46. Klikněte na tlačítko OK.
47. Klepnutím na možnost Přidat otevřete dialogové okno.
48. Ve stromovém zobrazení vyberte „XML\Prvek“.
49. Do pole Název dimenze zadejte Dimenze.
50. Klepněte na tlačítko OK.
51. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.
52. Klepnutím na možnost Přidat otevřete dialogové okno.
53. Ve stromovém zobrazení vyberte „XML\Atribut“.
54. Do pole Název zadejte Kód.
55. Klikněte na tlačítko OK.
56. Klikněte na možnost Přidat atributy.
57. Do pole Název zadejte Hodnota.
58. Klikněte na tlačítko OK.
59. Klikněte na možnost Přidat atributy.
60. Do pole Název zadejte Popis.
61. Klikněte na tlačítko OK.

## <a name="map-report-elements-to-data-sources"></a>Mapování prvků sestavy na zdroje dat
1. Klikněte na kartu Mapování.
2. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.
3. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.
4. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.
5. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.
6. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Popis: Atribut XML'.
7. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Popis: Řetězec'.
8. Klikněte na možnost Vazba.
9. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Hodnota: Atribut XML'.
10. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.
11. Klikněte na možnost Vazba.
12. Ve stromové struktuře vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Rozměry: Prvek XML\Kód: Atribut XML'.
13. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Název: Řetězec'.
14. Klikněte na možnost Vazba.
15. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.
16. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.
17. Klikněte na možnost Vazba.
18. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Ct: Atribut XML'.
19. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.
20. Klikněte na možnost Vazba.
21. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dt: Atribut XML'.
22. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.
23. Klikněte na možnost Vazba.
24. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Měna: Atribut XML'.
25. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.
26. Klikněte na možnost Vazba.
27. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Datum: Atribut XML'.
28. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.
29. Klikněte na možnost Vazba.
30. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Doklad: Atribut XML'.
31. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.
32. Klikněte na možnost Vazba.
33. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.
34. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.
35. Klikněte na možnost Vazba.
36. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Dávka: Atribut XML'.
37. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.
38. Klikněte na možnost Vazba.
39. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.
40. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.
41. Klikněte na možnost Vazba.
42. Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Společnost: Atribut XML'.
43. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.
44. Klikněte na možnost Vazba.
45. Klikněte na položku Uložit.
46. Zavřete stránku.


