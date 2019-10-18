---
title: Úprava formátů pro generování dokumentů s daty aplikace
description: K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 3 - úprava modelu a mapování).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbed62c80c14e7cfe96d38d43a5db39b0469d939
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184915"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Úprava formátů pro generování dokumentů s daty aplikace

[!include [task guide banner](../../includes/task-guide-banner.md)]

K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 3: úprava modelu a mapování).

Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace. V tomto postupu budete upravovat konfigurace ER tak, aby se nepoužívaly výhradně ke generování elektronických dokumentů, ale také k aktualizaci dat aplikace. Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady DEMF.


## <a name="modify-format-to-collect-details-of-reporting"></a>Upravte formát kvůli shromažďování podrobností o vykazování
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Intrastat (model).
3. Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).
4. Klikněte na možnost Návrhář.
5. Ve stromovém zobrazení rozbalte Soubor.
6. Ve stromovém zobrazení rozbalte File\Declaration.
7. Ve stromovém zobrazení vyberte File\Declaration\Data.
8. V poli Násobnost vyberte Jeden-n.
    * Nakonfigurujte tento prvek formátu pro archivaci detailů o procesu vykazování Intrastat. Tato položka reprezentuje záznam záhlaví archivu.  
9. Ve stromovém zobrazení rozbalte File\Declaration\Data.
10. Ve stromovém zobrazení vyberte File\Declaration\Data\Item.
11. V poli Násobnost vyberte Jeden-0.
    * Nakonfigurujte tento prvek formátu pro archivaci detailů o procesu vykazování Intrastat. Tato položka bude představovat seznam archivovaných řádků.  
12. Ve stromovém zobrazení rozbalte File\Declaration\Data\Item.
13. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim1.
14. Vyberte možnost Ano v poli Vyloučeno.
    * Tato data nebudou postoupena k archivaci, takže tento prvek formátu můžete vyloučit z datového zdroje pro podrobnosti vykazování Intrastat.  
15. Ve stromovém zobrazení rozbalte File\Declaration\Data\Item\Dim1.
16. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim1\property.
17. Vyberte možnost Ano v poli Vyloučeno.
18. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim1\date.
19. Vyberte možnost Ano v poli Vyloučeno.
20. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim2.
21. Vyberte možnost Ano v poli Vyloučeno.
22. Ve stromovém zobrazení rozbalte File\Declaration\Data\Item\Dim2.
23. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim2\property.
24. Vyberte možnost Ano v poli Vyloučeno.
25. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim2\code.
26. Vyberte možnost Ano v poli Vyloučeno.
27. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim3.
    * Více prvků formátu mohou mít stejný název. Například Dim. Nelze je explicitně rozlišit při použití tohoto formátu jako zdroje dat pro archivaci podrobnosti vykazování Intrastat, takže je nutné definovat alternativní názvy těchto prvků formátu.   
28. Do pole Název zadejte „Částka“.
    * Množství  
29. V poli Násobnost vyberte Přesně jeden.
30. Ve stromovém zobrazení vyberte File\Declaration\Data\Item\Dim4.
31. Do pole Název zadejte „Položka“.
    * Zboží  
32. V poli Násobnost vyberte Přesně jeden.
    * Kromě elementů formátu návrhu je nutné archivovat následující podrobnosti o vykazování Intrastat: jedinečnou identifikaci záznamu každé hlášené položky zboží a název vytvořeného souboru. Vzhledem k tomu, že se tato data nevyplní sama v sestavě Intrastat, je nutné přidat formát, který u těchto prvků podrobností slouží jako položky datového zdroje.  
33. Ve stromovém zobrazení vyberte File\Declaration\Data.
34. Klepnutím na možnost Přidat otevřete dialogové okno.
35. Ve stromovém zobrazení vyberte Data source\Item.
36. Do pole Název zadejte Název souboru.
    * Název souboru  
37. V poli Typ dat vyberte Řetězec.
38. Klikněte na tlačítko OK.
39. Ve stromovém zobrazení vyberte File\Declaration\Data\Item.
40. Klepněte na položku Přidat položku.
41. Do pole Název zadejte ID záznamu komodity.
    * ID záznamu komodity  
42. V poli Typ dat vyberte Int64.
43. Klikněte na tlačítko OK.
44. Klikněte na kartu Mapování.
45. Ve stromovém zobrazení vyberte File\Declaration\Data\File name.
46. Klikněte na možnost Vazba.
47. Ve stromovém zobrazení rozbalte „model“.
48. Ve stromovém zobrazení rozbalte model\Transactions.
49. Ve stromovém zobrazení vyberte File\Declaration\Data\Item =  model.Transactions\Commodity rec id.
50. Ve stromovém zobrazení vyberte možnost model\Transactions\Commodity rec id.
51. Klikněte na možnost Vazba.
52. Klikněte na položku Uložit.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Upravte formát kvůli zapamatování podrobností o vykazování
1. Klikněte na Mapovat formát na model.
2. Klikněte na položku Nová.
3. V poli Definice zadejte nebo vyberte kořenovou položku Pro aktualizaci dat aplikace.
    * Pro aktualizaci dat aplikace  
4. Do pole Název zadejte Mapování pro aktualizaci dat.
    * Mapování pro aktualizaci dat  
5. Klikněte na položku Uložit.
    * Toto mapování definuje to, jak jsou podrobné informace o hlášení Intrastat shromážděny v datovém modelu – strukturu, která je určena výběrem kořenové položky Pro aktualizaci dat aplikace. Tyto podrobnosti, mapování modelu se shodnou kořenovou položkou Pro aktualizaci dat aplikace a směr K cíli se použijí pro aktualizaci dat aplikace. Aktualizace dat aplikace začne ihned po vygenerování odchozí sestavy Intrastat. Všimněte si, že aktualizaci dat aplikace lze přeskočit při spuštění, ale datový model musí být prázdný (obsahovat prázdný seznam záznamů).   
6. Klikněte na možnost Návrhář.
    * Všimněte si, že je standardně přidán formát odchozí sestavy Intrastat jako zdroj dat pro toto mapování modelu.  
    * Připojte prvky požadované sestavy (předkládané jako datový zdroj) k prvkům datového modelu, který je filtrován na základě kořenové položky vybraného modelu.  
7. Ve stromovém zobrazení rozbalte Záhlaví archivu.
8. Ve stromovém zobrazení rozbalte Archive header\Archive lines.
9. Ve stromové struktuře rozbalte Formát.
10. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration).
11. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data).
12. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item).
13. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount).
14. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item).
15. Ve stromovém zobrazení vyberte Archive header\Number of lines.
16. Klikněte na položku Upravit.
17. Ve stromu vyberte možnost List\COUNT.
18. Klikněte na možnost Přidat funkci.
19. Ve stromové struktuře rozbalte Formát.
20. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration).
21. Ve stromovém zobrazení rozbalte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data).
22. Ve stromovém zobrazení vyberte 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item).
23. Klikněte na možnost Přidat datový zdroj.
24. V poli Receptura zadejte COUNT(format.Declaration.Data.Item).
    * COUNT(format.Declaration.Data.Item)  
25. Klikněte na položku Uložit.
26. Zavřete stránku.
27. Ve stromovém zobrazení vyberte Archive header\File name.
28. Ve stromovém zobrazení vyberte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name).
29. Klikněte na možnost Vazba.
30. Ve stromovém zobrazení vyberte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number).
31. Ve stromovém zobrazení vyberte Archive header\Archive lines\Item number.
32. Klikněte na možnost Vazba.
33. Ve stromovém zobrazení vyberte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value).
34. Ve stromovém zobrazení vyberte Archive header\Archive lines\Amount.
35. Klikněte na možnost Vazba.
36. Ve stromovém zobrazení vyberte format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec id: Item Int64(Commodity rec id).
37. Ve stromovém zobrazení vyberte Archive header\Archive lines\Commodity rec id.
38. Klikněte na možnost Vazba.
39. Ve stromovém zobrazení rozbalte Archive header\Archive lines.
40. Ve stromovém zobrazení vyberte 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item).
41. Klikněte na možnost Vazba.
42. Ve stromovém zobrazení vyberte Záhlaví archivu.
43. Ve stromovém zobrazení vyberte 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data).
44. Klikněte na možnost Vazba.
45. Klikněte na položku Uložit.
46. Zavřete stránku.
47. Zavřete stránku.
48. Zavřete stránku.

