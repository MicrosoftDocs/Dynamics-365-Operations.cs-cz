--- 
title: "Úprava modelu a mapování pro generování dokumentů s aktualizací dat aplikace pro elektronické výkaznictví (ER)"
description: "K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 2 - generování dokumentů)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: a29e273e5ef377826c0002a9a0a956defef6aa77
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Úprava modelu a mapování pro generování dokumentů s aktualizací dat aplikace pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 2: generování dokumentů). 

Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace. V tomto postupu budete upravovat konfigurace ER tak, aby se začaly používat výhradně ke generování elektronických dokumentů a k aktualizaci dat aplikace. Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady DEMF.


## <a name="modify-data-model"></a>Upravit model dat
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení vyberte Intrastat (modul).
    * Údaje se rozšiřují v závislosti na způsobu použití datového modelu. Kromě použití jako zdroje dat pro vygenerování sestavy Intrastat se datový model použije ke shromáždění podrobností o procesu vykazování Intrastat. Údaje se poté použijí k aktualizaci dat aplikace.   
3. Klikněte na možnost Návrhář.
4. Kliknutím na možnost Nový otevřete dialogové okno.
5. Do pole Nový uzel zadejte Kořen modelu.
6. Do pole Název zadejte Pro aktualizaci dat aplikace.
    * Pro aktualizaci dat aplikace  
7. Klepněte na možnost Přidat.
8. Ve stromovém zobrazení vyberte Pro aktualizaci dat aplikace.
    * Tato nová kořenová položka bude přidána pro určení toku dat při přesunu dat ze sestavy Intrastat (použité jako datový zdroj) do tabulek aplikace (cíl aktualizace). Mějte na paměti, že pro získávání dat, která byla zanesena do odchozího dokumentu musí být použita jiná kořenová položka, než pro získávání dat z dokumentu, který se používá k aktualizaci dat aplikace.   
9. Kliknutím na možnost Nový otevřete dialogové okno.
10. Do pole Název zadejte Záhlaví archivu.
    * Záhlaví archivu  
11. V poli Typ položky vyberte Seznam záznamů.
12. Klepněte na možnost Přidat.
    * Vzhledem k tomu, že chcete vytvořit záznam pro každou vygenerovanou sestavu Intrastat, je nutné pro to vytvořit novou položku.  
13. Kliknutím na možnost Nový otevřete dialogové okno.
14. Do pole Název zadejte Název souboru.
    * Název souboru  
15. V poli Typ položky vyberte Řetězec.
16. Klepněte na možnost Přidat.
17. Kliknutím na možnost Nový otevřete dialogové okno.
18. Do pole Název zadejte Počet řádků.
    * Počet řádků  
19. V poli Typ položky vyberte Celé číslo.
20. Klepněte na možnost Přidat.
    * Přidáním této položky můžete reprezentovat počet transakcí Intrastat, které jsou uvedeny vykázány při aktuálním procesu vykazování.  
21. Kliknutím na možnost Nový otevřete dialogové okno.
22. Do pole Název zadejte Řádky archivu.
    * Řádky archivu  
23. V poli Typ položky vyberte Seznam záznamů.
24. Klepněte na možnost Přidat.
    * Přidáním této položky můžete reprezentovat seznam transakcí Intrastat, které jsou uvedeny vykázány při aktuálním procesu vykazování.  
25. Kliknutím na možnost Nový otevřete dialogové okno.
26. Do pole Název zadejte „Částka“.
    * Množství  
27. V poli Typ položky vyberte Reálný.
28. Klepněte na možnost Přidat.
29. Kliknutím na možnost Nový otevřete dialogové okno.
30. Do pole Název zadejte ID záznamu komodity.
    * ID záznamu komodity  
31. V poli Typ položky vyberte Int64.
32. Klepněte na možnost Přidat.
33. Kliknutím na možnost Nový otevřete dialogové okno.
34. Do pole Název zadejte Číslo položky.
    * Č. položky  
35. V poli Typ položky vyberte Řetězec.
36. Klepněte na možnost Přidat.
37. Klikněte na položku Uložit.
38. Zavřete stránku.

## <a name="modify-model-mapping"></a>Úprava mapování modelu
1. Ve stromovém zobrazení rozbalte Intrastat (model).
2. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (mapping).
    * Upravte stávající mapování modelu a začněte je používat pro aktualizaci dat aplikace a k archivaci podrobností vykazování Intrastat.  
3. Klikněte na možnost Návrhář.
4. Klikněte na položku Nová.
5. Do pole Název zadejte Aktualizovat archiv.
    * Aktualizace archivu  
6. V poli Směr vyberte hodnotu Do cíle.
7. Klikněte na položku Uložit.
    * Toto nové mapování určuje tok dat při přesunu dat (podrobnosti sestavy Intrastat) z datového modelu do tabulek aplikace (cíl aktualizace). Mějte na paměti, že pro získávání dat z aplikace pro proces vykazování musí být použita jiná kořenová položka modelu, než pro použití dat z modelu dat pro aktualizaci dat aplikace.   
8. Klikněte na možnost Návrhář.
9. Ve stromovém zobrazení vyberte Data model\Data model.
    * Přidejte požadovaný zdroj dat. Jedná se o datový model, který obsahuje podrobnosti o nahlášených transakcích systému Intrastat, které musí být archivovány.  
10. Klikněte na možnost Přidat kořen.
11. Do pole Název zadejte Model.
    * model  
12. V poli Definice zadejte nebo vyberte hodnotu Pro aktualizaci dat aplikace.
    * Pro aktualizaci dat aplikace  
13. Klikněte na tlačítko OK.
14. Ve stromovém zobrazení rozbalte „model“.
15. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
16. Ve stromovém zobrazení vyberte model\Archive header.
17. Klepněte na možnost Přidat.
    * Vzhledem k tomu, že chcete vytvořit výčet nahlášené transakce Intrastat pro archivaci, je nutné přidat odpovídacími zdroje dat.  
18. Do pole Název zadejte Výčet řádků.
    * Řádky z výčtu  
19. Klikněte na možnost Upravit vzorec.
20. Ve stromovém zobrazení vyberte List\ENUMERATE.
21. Klikněte na možnost Přidat funkci.
22. Ve stromovém zobrazení rozbalte „model“.
23. Ve stromovém zobrazení rozbalte možnost model\Archive header.
24. Ve stromovém zobrazení vyberte model\Archive header\Archive lines.
25. Klikněte na možnost Přidat datový zdroj.
26. V poli Receptura zadejte ENUMERATE(model.'Archive header'.'Archive lines').
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. Klikněte na položku Uložit.
28. Zavřete stránku.
29. Klikněte na tlačítko OK.
30. Klikněte na možnost Přidat cíl.
    * Přidejte tabulky aplikace jako požadované cíle, které vyžadují aktualizace podrobností archivace nahlášených transakcí Intrastat.  
31. Do pole Název zadejte Archiv.
    * Archivovat  
32. Do pole Tabulka zadejte IntrastatArchiveGeneral.
    * IntrastatArchiveGeneral  
    * Ponechte akci záznamu Vložit, aby bylo možné přidat záznamy během archivace podrobností pro každý proces vykazování Intrastat.  
33. Vyberte možnost Ano v poli Informační protokol o záznamu.
    * Výběrem možnosti Ano získáte informace o problémech s aktualizací dat aplikace.  
34. Vyberte možnost Ano v poli Ověření akce přeskočení záznamu.
    * Výběrem možnosti Ano potlačíte chyby v ověření prázdného pole ID archivu Intrastat. Tato akce proběhne po přidání záznamů na základě nastavení pořadového čísla pro tuto tabulku ve formuláři Parametry zahraničního obchodu.  
35. Klikněte na tlačítko OK.
    * Vytvořte vazbu přidaného zdroje dat (filtrovaný model založený na vybrané kořenové položce) s prvky z přidaného cíle.  
36. Ve stromovém zobrazení rozbalte Archiv.
37. Ve stromovém zobrazení rozbalte Archive\<Relations.
38. Ve stromovém zobrazení rozbalte Archive\<Relations\IntrastatArchiveDetail.
39. Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST).
40. Ve stromovém zobrazení rozbalte model\Archive header\Enumerated lines.
41. Ve stromovém zobrazení rozbalte model\Archive header\Enumerated lines\Value.
42. Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Amount.
43. Klikněte na možnost Vazba.
44. Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity).
45. Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Commodity rec id.
46. Klikněte na možnost Vazba.
47. Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId).
48. Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Item number.
49. Klikněte na možnost Vazba.
50. Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber).
51. Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Number.
52. Klikněte na možnost Vazba.
53. Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail.
54. Ve stromovém zobrazení vyberte model\Archive header\Enumerated line.
55. Klikněte na možnost Vazba.
56. Ve stromovém zobrazení vyberte Archive\File name(FileName).
57. Ve stromovém zobrazení vyberte model\Archive header\File name.
58. Klikněte na možnost Vazba.
59. Ve stromovém zobrazení vyberte Archive\Number of lines(NumberOfLines).
60. Ve stromovém zobrazení vyberte model\Archive header\Number of lines.
61. Klikněte na možnost Vazba.
62. Ve stromu vyberte Archiv.
63. Ve stromovém zobrazení vyberte model\Archive header.
64. Klikněte na možnost Vazba.
65. Klikněte na položku Uložit.
66. Zavřete stránku.
67. Zavřete stránku.


