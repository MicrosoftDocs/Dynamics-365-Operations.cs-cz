--- 
title: "Návrh datového model k používání finančních dimenzí jako zdroje dat pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví."
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
ms.openlocfilehash: d8a03c4b85666975a7b42d46f3afdd35019e9b93
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Návrh datového model k používání finančních dimenzí jako zdroje dat pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".


## <a name="create-a-new-data-model"></a>Vytvoření nového datového modelu
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel 'Litware, Inc.' je k dispozici a označen jako aktivní.  
2. Klikněte na Konfigurace výkaznictví.
3. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
4. V poli Název zadejte Vzorový model finančních dimenzí.
5. Klepněte na možnost Vytvořit konfiguraci.
6. Klikněte na možnost Návrhář.
7. Kliknutím na možnost Nový otevřete dialogové okno.
8. Do pole Název zadejte Položka.
9. Klepněte na možnost Přidat.
10. Kliknutím na možnost Nový otevřete dialogové okno.
11. Do pole Název zadejte text „Společnost“.
12. Klepněte na možnost Přidat.
    * Přidáme do našeho modelu nový seznam záznamů. Tento seznam bude uvádět (pro všechny sestavy ER používající tento model jako zdroj dat) nastavení pro vybrané finanční dimenze. Každá finanční dimenze se zobrazí v tomto seznamu jako záznam s odpovídajícími poli představujícími nastavení dimenze.  
13. Kliknutím na možnost Nový otevřete dialogové okno.
14. Do pole Název dimenze zadejte Nastavení dimenze.
15. V poli Typ položky vyberte Seznam záznamů.
16. Klepněte na možnost Přidat.
17. Kliknutím na možnost Nový otevřete dialogové okno.
18. Do pole Název zadejte Kód.
19. V poli Typ položky vyberte Řetězec.
20. Klepněte na možnost Přidat.
21. Kliknutím na možnost Nový otevřete dialogové okno.
22. Do pole Název zadejte název.
23. Klepněte na možnost Přidat.
24. Ve stromovém zobrazení vyberte 'Položka'.
25. Kliknutím na možnost Nový otevřete dialogové okno.
26. Do pole Název zadejte Deník.
27. V poli Typ položky vyberte Seznam záznamů.
28. Klepněte na možnost Přidat.
29. Kliknutím na možnost Nový otevřete dialogové okno.
30. Do pole Název zadejte Dávka.
31. V poli Typ položky vyberte Řetězec.
32. Klepněte na možnost Přidat.
33. Kliknutím na možnost Nový otevřete dialogové okno.
34. Do pole Název zadejte Transakce.
35. V poli Typ položky vyberte Seznam záznamů.
36. Klepněte na možnost Přidat.
37. Kliknutím na možnost Nový otevřete dialogové okno.
38. Do pole Název zadejte Datum.
39. V poli Typ položky vyberte Datum.
40. Klepněte na možnost Přidat.
41. Kliknutím na možnost Nový otevřete dialogové okno.
42. Do pole Název zadejte Má dáti.
43. V poli Typ položky vyberte Reálný.
44. Klepněte na možnost Přidat.
45. Kliknutím na možnost Nový otevřete dialogové okno.
46. Do pole Název zadejte Dal.
47. Klepněte na možnost Přidat.
48. Kliknutím na možnost Nový otevřete dialogové okno.
49. Do pole Název zadejte Měna.
50. V poli Typ položky vyberte Řetězec.
51. Klepněte na možnost Přidat.
52. Kliknutím na možnost Nový otevřete dialogové okno.
53. Do pole Název zadejte Doklad.
54. Klepněte na možnost Přidat.
55. Kliknutím na možnost Nový otevřete dialogové okno.
56. Do pole Název zadejte Data dimenze.
57. V poli Typ položky vyberte Seznam záznamů.
58. Klepněte na možnost Přidat.
    * Přidali jsme do našeho modelu nový seznam záznamů. Tento seznam bude uvádět (pro všechny sestavy ER používající tento model jako zdroj dat) hodnoty vybraných finančních dimenzích. Každá finanční dimenze se zobrazí v tomto seznamu jako záznam s odpovídajícími poli představujícími hodnoty dimenze. Název dimenze bude také prezentován v tomto záznamu jako pole, které se má v případě potřeby použít pro účely výběru.  
59. Kliknutím na možnost Nový otevřete dialogové okno.
60. Do pole Název zadejte Kód.
61. V poli Typ položky vyberte Řetězec.
62. Klepněte na možnost Přidat.
63. Kliknutím na možnost Nový otevřete dialogové okno.
64. Do pole Název zadejte Popis.
65. Klepněte na možnost Přidat.
66. Kliknutím na možnost Nový otevřete dialogové okno.
67. Do pole Název zadejte název.
68. Klepněte na možnost Přidat.
69. Klikněte na položku Uložit.
70. Zavřete stránku.


