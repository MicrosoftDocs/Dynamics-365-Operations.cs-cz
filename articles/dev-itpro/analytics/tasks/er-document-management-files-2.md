--- 
title: "Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2 - Rozšíření datového modelu)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a>Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2: Rozšíření datového modelu)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K dokončení těchto kroků je nutné nejprve provést kroky v průvodci záznamem úloh "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 1: Příprava datového modelu).

Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Rozšíření datového modelu na prezentaci souborů správy dokumentů
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.
4. Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".
5. Klikněte na možnost Návrhář.
6. Ve stromovém zobrazení vyberte možnost Faktura odběratele (InvoiceCustomer).
    * Rozšíříme tento datový model, tak aby v něm byly vystaveny všechny soubory, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.  
7. Kliknutím na možnost Nový otevřete dialogové okno.
8. Do pole Název zadejte Přílohy faktury.
    * Přílohy faktury  
9. V poli Typ položky vyberte Seznam záznamů.
10. Klepněte na možnost Přidat.
11. Kliknutím na možnost Nový otevřete dialogové okno.
12. Do pole Název zadejte Obsah souboru.
    * Obsah souboru  
13. V poli Typ položky vyberte Obsahuje.
14. Klepněte na možnost Přidat.
15. Kliknutím na možnost Nový otevřete dialogové okno.
16. Do pole Název zadejte Název souboru.
    * Název souboru  
17. V poli Typ položky vyberte Řetězec.
18. Klepněte na možnost Přidat.

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Mapování nových prvků datového modelu do zdrojových dat aplikace Dynamics 365 for Finance and Operations, edice Enterprise
1. Klikněte na možnost Mapovat model na datový zdroj.
2. Použijte rychlý filtr k filtrování v poli Definice s hodnotou 'InvoiceCustomer'.
    * InvoiceCustomer  
    * Namapujeme nové prvky modelu na příslušné zdroje dat.  
3. Klikněte na možnost Návrhář.
4. Ve stromovém zobrazení vyberte možnost Přílohy faktury.
5. Ve stromovém zobrazení rozbalte možnost Přílohy faktury.
6. Ve stromovém zobrazení vyberte možnost Přílohy faktury\Název souboru.
7. Klikněte na položku Upravit.
8. Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klikněte na položku Uložit.
10. Zavřete stránku.
11. Ve stromové struktuře vyberte Přílohy faktury\Obsah souboru.
12. Klikněte na položku Upravit.
13. Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Klikněte na položku Uložit.
15. Zavřete stránku.
16. Ve stromovém zobrazení vyberte možnost Přílohy faktury.
17. Klikněte na položku Upravit.
18. Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klikněte na položku Uložit.
20. Zavřete stránku.
21. Klikněte na položku Uložit.
22. Zavřete stránku.
23. Zavřete stránku.
24. Zavřete stránku.
25. Klikněte na položku Změnit stav.
26. Klikněte na tlačítko Dokončit.
27. Klikněte na tlačítko OK.


