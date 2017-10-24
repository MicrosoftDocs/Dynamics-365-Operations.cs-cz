--- 
title: "Návrh formátu pro použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v sestavách aplikace Excel pro elektronické výkaznictví (ER)"
description: "Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Návrh formátu pro použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v sestavách aplikace Excel pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy. Tyto kroky lze provést v rámci libovolné společnosti.

K provedení těchto kroků je nutné nejprve dokončit tyto tři průvodce: 

ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního

Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 1: návrh datového modelu)

Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 2: mapování modelu)

Je nutné stáhnout a uložit místní kopii šablony se vzorovou sestavou dostupnou zde: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx

Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="create-a-new-report-configuration"></a>Vytvoření nové konfigurace sestavy
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.
3. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
4. V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".
    * Použijte model vytvořený předem jako zdroj dat pro novou sestavu.  
5. Do pole Název zadejte Ukázková sestava s vodorovně rozbalitelnými rozsahy.
    * Ukázková sestava s vodorovně rozbalitelnými rozsahy  
6. Do pole Popis zadejte "Nastavení výstupu aplikace Excel s dynamickým přidáváním sloupců".
    * Nastavení výstupu aplikace Excel s dynamickým přidáváním sloupců  
7. V poli Definice datového modelu vyberte Položka.
8. Klepněte na možnost Vytvořit konfiguraci.

## <a name="design-the-report-format"></a>Návrh formátu sestavy
1. Klikněte na možnost Návrhář.
2. Zapněte přepínač "Zobrazit detaily".
3. V podokně akcí klikněte na možnost Importovat.
4. Klikněte na Import z aplikace Excel.
5. Klikněte na Přílohy.
    * Importujte šablonu sestavy. Použijte soubor aplikace Excel, který jste pro ten účel stáhli.  
6. Klikněte na položku Nová.
7. Klepněte na volby Soubor.
8. Zavřete stránku.
9. V poli Šablona zadejte nebo vyberte hodnotu.
    * Vyberte staženou šablonu.  
10. Klikněte na tlačítko OK.
    * Přidejte nový rozsah k dynamickému vytvoření výstupu aplikace Excel s tolika sloupci, kolik jste vybrali (ve formuláři dialogového okna uživatele) pro finanční dimenze. Každá buňka pro každý sloupec bude představovat název jedné finanční dimenze.  
11. Klepnutím na možnost Přidat otevřete dialogové okno.
12. Ve stromovém zobrazení vyberte možnost „Excel\Rozsah“.
13. V poli rozsah aplikace Excel zadejte "DimNames".
    * DimNames  
14. V poli Směr replikace vyberte hodnotu Vodorovně.
15. Klepněte na tlačítko OK.
16. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
17. Klikněte na Přesunout nahoru.
18. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Cell<DimNames>.
19. Klepněte na tlačítko Vyjmout.
20. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
21. Klepněte na tlačítko Vložit.
22. Ve stromovém zobrazení rozbalte Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
23. Ve stromovém zobrazení rozbalte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
24. Ve stromovém zobrazení rozbalte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
25. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
    * Přidejte nový rozsah k dynamickému vytvoření výstupu aplikace Excel s tolika sloupci, kolik jste vybrali (ve formuláři dialogového okna uživatele) pro finanční dimenze. Každá buňka pro každý sloupec bude představovat hodnotu jedné finanční dimenze pro každou transakci výkaznictví.  
26. Klikněte na Přidat rozsah.
27. V poli rozsah aplikace Excel zadejte "DimValues".
    * DimValues  
28. V poli Směr replikace vyberte hodnotu Vodorovně.
29. Klepněte na tlačítko OK.
30. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>.
31. Klepněte na tlačítko Vyjmout.
32. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.
33. Klepněte na tlačítko Vložit.
34. Ve stromovém zobrazení rozbalte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.

## <a name="map-format-elements-to-data-sources"></a>Mapování prvků formátu na zdroje dat
1. Klikněte na kartu Mapování.
2. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.
3. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.
4. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.
5. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.
6. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.
7. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.
8. Klikněte na možnost Vazba.
9. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.
10. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.
11. Klikněte na možnost Vazba.
12. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>.
13. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.
14. Klikněte na možnost Vazba.
15. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>.
16. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.
17. Klikněte na možnost Vazba.
18. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>.
19. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.
20. Klikněte na možnost Vazba.
21. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>.
22. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.
23. Klikněte na možnost Vazba.
24. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>.
25. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.
26. Klikněte na možnost Vazba.
27. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>.
28. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.
29. Klikněte na možnost Vazba.
30. Ve stromovém zobrazení zvolte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
31. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.
32. Klikněte na možnost Vazba.
33. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>.
34. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.
35. Klikněte na možnost Vazba.
36. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
37. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.
38. Klikněte na možnost Vazba.
39. Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Nastavení dimenzí: Seznam záznamů'.
40. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Nastavení dimenzí: Seznam záznamů\Kód: Řetězec'.
41. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>.
42. Klikněte na možnost Vazba.
43. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Nastavení dimenzí: Seznam záznamů'.
44. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
45. Klikněte na možnost Vazba.
46. Ve stromovém zobrazení vyberte Excel = "SampleFinDimWsReport"\Cell<CompanyName>.
47. Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.
48. Klikněte na možnost Vazba.
49. Klikněte na položku Uložit.
50. Zavřete stránku.


