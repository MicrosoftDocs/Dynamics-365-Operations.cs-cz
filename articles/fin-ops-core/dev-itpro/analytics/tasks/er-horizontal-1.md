---
title: Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 1 - Formát návrhu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) pro generování sestav jako soubory listů OPENXML (Excel). (část 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551769"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 1 - Formát návrhu)

[!include [banner](../../includes/banner.md)]

Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků je nutné nejprve dokončit tyto tři průvodce:

"ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního"

"Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 1 - návrh datového modelu)"

"Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 2 - mapování modelu)"

Musíte též stáhnout a uložit místní kopii šablony se vzorovou sestavou, kterou naleznete zde [Vzorová sestava webové služby finančích dimenzí](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.

## <a name="create-a-new-report-configuration"></a>Vytvoření nové konfigurace sestavy

1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromu vyberte možnost `Financial dimensions sample model`.
3. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
4. Do pole Nový zadejte `Format based on data model Financial dimensions sample model`.
    * Použijte model vytvořený předem jako zdroj dat pro novou sestavu.  
5. Do pole Název zadejte `Sample report with horizontally expandable ranges`.
    * Ukázková sestava s vodorovně rozbalitelnými rozsahy  
6. Do pole Popis zadejte `To make Excel output with dynamically adding columns`.
    * Nastavení výstupu aplikace Excel s dynamickým přidáváním sloupců  
7. V poli Definice datového modelu vyberte Položka.
8. Klepněte na možnost Vytvořit konfiguraci.

## <a name="design-the-report-format"></a>Návrh formátu sestavy

1. Klikněte na možnost Návrhář.
2. Zapněte přepínač `Show details`.
3. V podokně akcí klikněte na možnost Importovat.
4. Klikněte na Import z aplikace Excel.
5. Klikněte na Přílohy.
    * Importujte šablonu sestavy. Použijte soubor aplikace Excel, který jste pro ten účel stáhli.  
6. Klikněte na možnost Nový.
7. Klepněte na volby Soubor.
8. Zavřete stránku.
9. V poli Šablona zadejte nebo vyberte hodnotu.
    * Vyberte staženou šablonu.  
10. Klikněte na tlačítko OK.
    * Přidejte nový rozsah k dynamickému vytvoření výstupu aplikace Excel s tolika sloupci, kolik jste vybrali (ve formuláři dialogového okna uživatele) pro finanční dimenze. Každá buňka v každém sloupci bude představovat název jedné finanční dimenze.  
11. Klepnutím na možnost Přidat otevřete dialogové okno.
12. Ve stromu vyberte možnost `Excel\Range`.
13. V poli rozsah aplikace Excel zadejte `DimNames`.
    * DimNames  
14. V poli Směr replikace vyberte hodnotu `Horizontal`.
15. Klepněte na tlačítko OK.
16. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. Klikněte na Přesunout nahoru.
18. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. Klepněte na tlačítko Vyjmout.
20. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. Klepněte na tlačítko Vložit.
22. Ve stromu rozbalte uzel `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. Ve stromu rozbalte uzel `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. Ve stromu rozbalte uzel `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * Přidejte nový rozsah k dynamickému vytvoření výstupu aplikace Excel s tolika sloupci, kolik jste vybrali (ve formuláři dialogového okna uživatele) pro finanční dimenze. Každá buňka v každém sloupci bude představovat hodnotu jedné finanční dimenze pro každou transakci výkaznictví.  
26. Klikněte na Přidat rozsah.
27. V poli rozsah aplikace Excel zadejte `DimValues`.
    * DimValues  
28. V poli Směr replikace vyberte hodnotu `Horizontal`.
29. Klepněte na tlačítko OK.
30. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. Klepněte na tlačítko Vyjmout.
32. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. Klepněte na tlačítko Vložit.
34. Ve stromu rozbalte uzel `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>Mapování prvků formátu na zdroje dat

1. Klikněte na kartu Mapování.
2. Ve stromu rozbalte uzel `model: Data model Financial dimensions sample model`.
3. Ve stromu rozbalte uzel `model: Data model Financial dimensions sample model\Journal: Record list`.
4. Ve stromu rozbalte uzel `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. Ve stromu rozbalte uzel `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. Klikněte na možnost Vazba.
9. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. Klikněte na možnost Vazba.
12. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. Klikněte na možnost Vazba.
15. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. Klikněte na možnost Vazba.
18. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. Klikněte na možnost Vazba.
21. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. Klikněte na možnost Vazba.
24. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. Klikněte na možnost Vazba.
27. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. Klikněte na možnost Vazba.
30. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. Klikněte na možnost Vazba.
33. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. Klikněte na možnost Vazba.
36. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Journal: Record list`.
38. Klikněte na možnost Vazba.
39. Ve stromu rozbalte uzel `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. Klikněte na možnost Vazba.
43. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. Klikněte na možnost Vazba.
46. Ve stromu vyberte možnost `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. Ve stromu vyberte možnost `model: Data model Financial dimensions sample model\Company: String`.
48. Klikněte na možnost Vazba.
49. Klikněte na tlačítko Uložit.
50. Zavřete stránku.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
