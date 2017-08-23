--- 
title: "Vytvoření formátu k použití souborů pro správu dokumentů ve formátech výstupu pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 47c7bea976d1052f537068b6bcf79c78ac3befbf
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Vytvoření formátu k použití souborů pro správu dokumentů ve formátech výstupu pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 2: Rozšíření datového modelu).

Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="create-a-format-to-process-invoices"></a>Vytvoření formátu pro zpracování faktur
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.
4. Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".
    * Vytvoříte formát pro generování elektronických zpráv s informacemi o všech souborech, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.  
5. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
6. V poli Nový zadejte Formát založený na datovém modelu Faktura odběratele (vlastní).
7. Do pole Název zadejte Vzorová zpráva elektronické faktury.
    * Vzorová zpráva s elektronickou fakturou  
8. V poli Definice datového modelu zadejte nebo vyberte hodnotu.
    * InvoiceCustomer  
9. Klepněte na možnost Vytvořit konfiguraci.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Návrh formátu k vyplnění příloh do generování zprávy ve formátu MIME
1. Klikněte na možnost Návrhář.
2. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
3. Ve stromovém zobrazení vyberte „XML\Prvek“.
4. Do pole Název zadejte Faktura.
    * Faktura  
5. Klikněte na tlačítko OK.
6. Klepnutím na možnost Přidat otevřete dialogové okno.
7. Ve stromovém zobrazení vyberte „XML\Atribut“.
8. Do pole Název zadejte „SalesOrder“.
    * SalesOrder  
9. Klikněte na tlačítko OK.
10. Klikněte na možnost Přidat atributy.
11. Do pole Název zadejte InvoiceNumber.
    * InvoiceNumber  
12. Klikněte na tlačítko OK.
13. Klikněte na možnost Přidat atributy.
14. Do pole Název zadejte InvoiceAmount.
    * InvoiceAmount  
15. Klikněte na tlačítko OK.
16. Klepnutím na možnost Přidat otevřete dialogové okno.
17. Ve stromovém zobrazení vyberte „XML\Prvek“.
18. Do pole Název zadejte „EnclosedDocs“.
    * EnclosedDocs  
19. Klikněte na tlačítko OK.
20. Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs.
21. Klepněte na Přidat prvek.
22. Do pole Název zadejte Dokument.
    * Doklad  
23. Klikněte na tlačítko OK.
24. Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument.
25. Klepnutím na možnost Přidat otevřete dialogové okno.
26. Ve stromovém zobrazení vyberte „XML\Atribut“.
27. Do pole Název zadejte FileName.
    * Název souboru  
28. Klikněte na tlačítko OK.
29. Klepnutím na možnost Přidat otevřete dialogové okno.
30. Ve stromovém zobrazení vyberte „XML\Prvek“.
31. Do pole Název zadejte FileContent.
    * FileContent  
32. Klikněte na tlačítko OK.
33. Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument\FileContent.
34. Klepnutím na možnost Přidat otevřete dialogové okno.
35. Ve stromu vyberte 'Text\Base64'.
36. Klikněte na tlačítko OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Namapování prvků formátu na datový model jako zdroje dat
1. Ve stromovém zobrazení vyberte možnost 'Faktura\SalesOrder'.
2. Klikněte na kartu Mapování.
3. Ve stromovém zobrazení rozbalte „model“.
4. Ve stromové struktuře vyberte 'model\Číslo prodejní objednávky(SalesId)'.
5. Klikněte na možnost Vazba.
6. Ve stromovém zobrazení vyberte možnost Faktura\InvoiceNumber.
7. Ve stromovém zobrazení rozbalte možnost 'model\Základní faktura(InvoiceBase)'.
8. Ve stromové struktuře vyberte model\Základní faktura(InvoiceBase)\Číslo faktury(Id).
9. Klikněte na možnost Vazba.
10. Ve stromovém zobrazení vyberte možnost 'Faktura\InvoiceAmount'.
11. Ve stromové struktuře vyberte 'model\Základní faktura(InvoiceBase)\Částka faktury(Amount)'.
12. Klikněte na možnost Vazba.
13. Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.
14. Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.
15. Ve stromovém zobrazení vyberte možnost 'Faktura\EnclosedDocs\Dokument\FileContent\Base64'.
16. Klikněte na možnost Vazba.
17. Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.
18. Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument\FileName.
19. Klikněte na možnost Vazba.
20. Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.
21. Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument.
22. Klikněte na možnost Vazba.
23. Klikněte na položku Uložit.
24. Zavřete stránku.


