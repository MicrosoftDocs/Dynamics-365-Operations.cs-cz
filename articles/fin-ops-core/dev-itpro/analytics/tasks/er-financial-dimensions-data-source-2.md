---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 2 - mapování modelu)
description: Toto téma popisuje, jak nakonfigurovat model elektronického výkaznictví (ER) tak, aby používal finanční dimenze jako zdroj dat pro zprávy ER. (část 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093230"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 2 - mapování modelu)

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví. Tyto kroky lze provést v rámci libovolné společnosti.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 1: návrh datového modelu").


## <a name="add-required-data-sources-to-model-mapping"></a>Přidání požadovaných zdrojů dat k mapování modelu
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.
3. Klikněte na možnost Návrhář.
4. Klikněte na možnost Mapovat model na datový zdroj.
5. Klikněte na položku Nová.
6. V poli Definice vyberte Položka.
7. Do pole Název zadejte Mapování dat dimenzí.
8. Do pole Popis zadejte Mapování dat dimenzí.
9. Klikněte na položku Uložit.
10. Klikněte na možnost Návrhář.
11. Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Tabulka'.
12. Klikněte na možnost Přidat kořen.
13. Do pole Název zadejte text „Společnost“.
14. Do pole Tabulka zadejte hodnotu „CompanyInfo“.
15. Klepněte na tlačítko OK.
16. Ve stromovém zobrazení vyberte Funkce\Podrobnosti o finančních dimenzích.
17. Klikněte na možnost Přidat kořen.
    * Tento zdroj dat určuje, jak bude definován obor finančních dimenzí pro jakoukoli sestavu, která bude používat tento model jako zdroj dat.  
18. Zadejte hodnotu do pole Název.
19. Vyberte možnost Ano v poli Zeptat se na dimenze.
    * Vyberte možnost Ano, chcete-li povolit uživateli výběr dimenzí v operačním času ve formuláři Uživatelské dialogové okno. Pokud je nastavena na hodnotu Ne, všechny finanční dimenze aktuální instance budou použity ve výchozím nastavení.  
20. V poli Finanční dimenze vyberte "Právnická osoba".
    * Vyberte Vše, chcete-li povolit uživateli výběr požadovaných dimenzí pro aktuální instanci ve vyhledávacím poli.  Vyberte Právnická osoba, chcete-li povolit uživateli výběr dimenzí pro společnost ve vyhledávacím poli.  Vyberte dimenzi, abyste uživateli povolili výběr dimenzí pomocí jedné sady dimenzí.  
21. Vyberte možnost Ano v poli Zeptat se na hlavní účet.
    * Nastavte v poli 'Zeptat se na hlavní účet' hodnotu Ano, chcete-li umožnit uživatelům vybrat hlavní účet jako součást seznamu dimenzí.   Je-li nastavena na hodnotu Ne, hlavní účet nebude zahrnut do seznamu dimenzí a je povolena možnost "Je hlavní účet povinný". Pokud je možnost 'Je hlavní účet povinný' nastavena na hodnotu Ano, zahrňte hlavní účet do seznamu dimenzí nezávisle na výběru uživatele.  
22. Klepněte na tlačítko OK.
![Stránka Návrhář mapování modelu ER](../media/er-financial-dimensions-guides-model-mapping1.png)
23. Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.
24. Klikněte na možnost Přidat kořen.
25. Do pole Název zadejte 'LedgerJournal'.
26. Vyberte možnost Ano v poli Zeptat se na dotaz.
27. Do pole Tabulka zadejte hodnotu 'LedgerJournalTable'.
28. Klepněte na tlačítko OK.
![Stránka Návrhář mapování modelu ER](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>Namapování prvků datového modelu na přidané zdroje dat
1. Ve stromovém zobrazení rozbalte 'Deník'.
2. Ve stromovém zobrazení rozbalte 'Deník\Transakce'.
3. Ve stromovém zobrazení rozbalte 'Deník\Transakce\Data dimenzí'.
4. Ve stromovém zobrazení rozbalte 'Nastavení dimenzí'.
5. Ve stromovém zobrazení rozbalte 'LedgerJournal'.
6. Ve stromovém zobrazení rozbalteLedgerJournal\<Relation.
7. Ve stromovém zobrazení rozbalte LedgerJournal\<Vztahy\LedgerJournalTrans.
8. Ve stromovém zobrazení vyberte LedgerJourna\\<Relations\LedgerJournalTrans\Voucher.
9. Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Doklad'.
10. Klikněte na možnost Vazba.
11. Ve stromovém zobrazení vyberte 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).
    * Všimněte si, že pro jakýkoli odkaz na finanční dimenze, na které je nastaven, jako je například LedgerDimension, je k dispozici odpovídající položka zdroje dat (LedgerDimension.Dimension). Tato položka zdroje dat nabízí finanční dimenze této sady dimenzí jako seznam záznamů.  
12. Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).
13. Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.
14. Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.
15. Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.
16. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.
17. Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí\Název'.
18. Klikněte na možnost Vazba.
19. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.
20. Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí\Popis'.
21. Klikněte na možnost Vazba.
22. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.
23. Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí\Kód'.
24. Klikněte na možnost Vazba.
25. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.
26. Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí'.
27. Klikněte na možnost Vazba.
![Stránka Návrhář mapování modelu ER](../media/er-financial-dimensions-guides-model-mapping3.png)
28. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).
29. Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Má dáti'.
30. Klikněte na možnost Vazba.
31. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).
32. Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Datum'.
33. Klikněte na možnost Vazba.
34. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).
35. Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Měna'.
36. Klikněte na možnost Vazba.
37. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).
38. Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Dal'.
39. Klikněte na možnost Vazba.
40. Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans.
41. Ve stromovém zobrazení vyberte možnost 'Deník\Transakce'.
42. Klikněte na možnost Vazba.
43. Ve stromovém zobrazení vyberte 'LedgerJournal\Číslo dávky deníku(JournalNum)'.
44. Ve stromovém zobrazení vyberte možnost 'Deník\Dávka'.
45. Klikněte na možnost Vazba.
46. Ve stromovém zobrazení vyberte 'LedgerJournal'.
47. Ve stromovém zobrazení vyberte 'Deník'.
48. Klikněte na možnost Vazba.
49. Ve stromovém zobrazení rozbalte 'Dimenze'.
50. Ve stromovém zobrazení rozbalte 'Dimenze\Hlavní účet a dimenze'.
51. Ve stromovém zobrazení rozbalte 'Dimenze\Hlavní účet a dimenze\Definice'.
52. Ve stromové struktuře vyberte 'Dimenze\Hlavní účet a dimenze\Defince\Název'.
53. Ve stromovém zobrazení vyberte 'Nastavení dimenzí\Kód'.
54. Klikněte na možnost Vazba.
55. Ve stromové struktuře vyberte 'Dimenze\Hlavní účet a dimenze\Definice\Název sloupce sestavy'.
56. Ve stromovém zobrazení vyberte 'Nastavení dimenzí\Název'.
57. Klikněte na možnost Vazba.
58. Ve stromovém zobrazení vyberte 'Dimenze\Hlavní účet a dimenze'.
59. Ve stromovém zobrazení vyberte 'Nastavení dimenzí'.
60. Klikněte na možnost Vazba.
61. Ve stromovém zobrazení vyberte 'Společnost'.
62. Klikněte na položku Upravit.
63. V poli expressionAsStringText zadejte 'Company.'find()'.'name()''.
    * Company.'find()'.'name()'  
64. Klepněte na tlačítko Uložit.
![Stránka Návrhář mapování modelu ER](../media/er-financial-dimensions-guides-model-mapping4.png)
65. Zavřete stránku.
66. Klepněte na tlačítko Uložit.
67. Zavřete stránku.

## <a name="complete-this-draft-models-version"></a>Dokončení tohoto konceptu verze modelu
1. Zavřete stránku.
2. Zavřete stránku.
3. Klikněte na položku Změnit stav.
4. Klikněte na tlačítko Dokončit.
5. Klepněte na tlačítko OK.
![Stránka Návrhář mapování modelu ER](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]