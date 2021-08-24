---
title: Definování mapování modelů elektronického výkaznictví a výběr zdrojů dat
description: Toto téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vybrat zdroje dat pro datový model Elektronické výkaznictví.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69fb025b273aca6a0cf7733732f2849686eaa470ded6804a10b793cff9837562
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717538"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>Definování mapování modelů elektronického výkaznictví a výběr zdrojů dat

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vybrat zdroje dat pro datový model Elektronické výkaznictví. Zdroje dat budou v době návrhu vázány k jednotlivých součástem vybraného datového modelu a za běhu vyplní obchodní data do datového modelu. V tomto příkladu budete vybírat zdroje dat pro existující datový model, který byl vytvořen pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření nového datového modelu".


## <a name="open-the-electronic-reporting-configurations-tree"></a>Otevření stromu konfigurací elektronického výkaznictví
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.

## <a name="insert-a-new-model-mapping"></a>Vložení nového mapování modelu
1. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.
2. Klikněte na možnost Návrhář.
3. Klikněte na možnost Mapovat model na datový zdroj.
4. Klikněte na položku Nová.
    * Tím vytvoříte nový záznam, který namapuje datový model na zdroje dat. V tomto příkladu namapujete datový model na zdroje dat pro požadovaný typ platby: peněžní převod.     Pro konkrétní datový model lze navrhnout více mapování. Například můžete vytvořit mapování pro různé typy plateb, jako je například pro přímý debet nebo peněžní převody. V tomto příkladu vytvoříte mapování pro peněžní převody.  
5. Zadejte text „Mapování Dal“ do pole Název.
    * Mapování Dal  
6. V poli Popis zadejte „Model platby pro mapování Dal“.
    * Model platby pro mapování Dal  
7. Zadejte hodnotu CustomerCreditTransferInitiation do pole Definice.
    * CustomerCreditTransferInitiation  
8. ResolveChanges Definice.
9. Klikněte na položku Uložit.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Definování požadovaných zdrojů dat pro aktuální mapování modelu
1. Klikněte na možnost Návrhář.
2. Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.
3. Klikněte na možnost Přidat kořen.
    * Zadejte tento zdroj dat pro přístup k platebním transakcím.  
4. Zadejte text „Transakce“ do pole Název.
    * Transakce  
5. Zadejte text „Transakce“ do pole Popisek.
    * Transakce  
6. V poli Nápověda zadejte text „Řádky deníku hlavní knihy“.
    * Řádky deníku hlavní knihy  
7. Vyberte možnost Ano v poli Zeptat se na dotaz.
    * Vyberte možnost Ano.  
8. Do pole Tabulka zadejte hodnotu „LedgerJournalTrans“.
    * LedgerJournalTrans  
9. Klikněte na tlačítko OK.
    * Vyberte tabulku LedgerJournalTrans jako zdroj dat pro aktuální datový model.  
10. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
11. Klepněte na možnost Přidat.
    * Kliknutím na tlačítko Přidat přidejte nové vypočítané pole.  
12. Zadejte text „$EndToEndID“ do pole Název.
    * $EndToEndID  
13. Klikněte na možnost Upravit vzorec.
14. Ve stromovém zobrazení vyberte možnost „Řetězec\SLOUČIT“.
15. Klikněte na možnost Přidat funkci.
16. Ve stromovém zobrazení rozbalte možnost Transakce.
17. Ve stromovém zobrazení vyberte možnost „Transakce\Doklad“.
18. Klikněte na možnost Přidat datový zdroj.
19. V poli Vzorec zadejte 'CONCATENATE(Transactions.Voucher, "-", '.
    * Na konci receptury zadejte [ , “-“, ].  
20. Ve stromovém zobrazení vyberte možnost „Řetězec\TEXT“.
21. Klikněte na možnost Přidat funkci.
22. Ve stromovém zobrazení vyberte možnost "Transakce\ID záznamu(RecId)".
23. Klikněte na možnost Přidat datový zdroj.
24. V poli Vzorec zadejte 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.
    * Na konci receptury zadejte [))].  
25. Klikněte na položku Uložit.
    * Ověřte, že ve vytvořené receptuře nejsou žádné chyby. Podívejte se na kartu CHYBY pod ovládacím prvkem editoru receptury.  
26. Zavřete stránku.
27. Klikněte na tlačítko OK.
    * Přidejte vypočítané pole k tomuto datovému zdroji.  
28. Klepněte na možnost Přidat.
    * Kliknutím na tlačítko Přidat přidejte nové vypočítané pole.  
29. Do pole Název zadejte „$Amount“.
    * $Částka  
30. Klikněte na možnost Upravit vzorec.
31. Ve stromovém zobrazení rozbalte možnost Transakce.
32. Ve stromovém zobrazení vyberte možnost "Transakce\Má dáti(AmountCurDebit)".
33. Klikněte na možnost Přidat datový zdroj.
34. V poli Vzorec zadejte 'Transactions.AmountCurDebit - '.
    * Na konci receptury zadejte [ - ].  
35. Ve stromovém zobrazení vyberte možnost "Transakce\Dal(AmountCurCredit)".
36. Klikněte na možnost Přidat datový zdroj.
37. Klikněte na položku Uložit.
38. Zavřete stránku.
39. Klikněte na tlačítko OK.
    * Tím se přidá vypočtené pole $Amount k vybranému zdroji dat pro aktuální datový model.  
40. Ve stromovém zobrazení vyberte možnost Transactions\$Amount.
41. Ve stromovém zobrazení rozbalte možnost Transakce.
42. Ve stromové struktuře rozbalte nebo sbalte Transactions\$Amount.
43. Ve stromové struktuře rozbalte nebo sbalte 'Transakce'.
44. Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.
45. Klikněte na možnost Přidat kořen.
    * Zadejte tento zdroj dat pro přístup k podrobnostem o bankovním účtu společnosti.  
46. Zadejte text „BankAccount“ do pole Název.
    * Bankovní účet  
47. Zadejte text „Bankovní účet“ do pole Popisek.
    * Bankovní účet  
48. Zadejte text „Bankovní účet“ do pole Nápověda.
    * Bankovní účet  
49. Vyberte možnost Ano v poli Zeptat se na dotaz.
    * Vyberte možnost Ano.  
50. Do pole Tabulka zadejte hodnotu „BankAccountTable“.
    * BankAccountTable  
51. Klikněte na tlačítko OK.
    * Vyberte tabulku BankAccountTable jako zdroj dat pro aktuální datový model.  
52. Klikněte na možnost Přidat kořen.
    * Zadejte tento zdroj dat pro přístup k požadavkům společnosti.  
53. Do pole Název zadejte text „Společnost“.
    * Společnost  
54. Zadejte hodnotu do pole Popisek.
    * Informace o společnosti  
55. Do pole Nápověda zadejte „Informace o společnosti“.
    * Informace o společnosti  
56. Vyberte možnost Ano v poli Zeptat se na dotaz.
    * Vyberte možnost Ano.  
57. Do pole Tabulka zadejte hodnotu „CompanyInfo“.
    * CompanyInfo  
58. Klikněte na tlačítko OK.
    * Vyberte tabulku CompanyInfo jako zdroj dat pro aktuální datový model.  
59. Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.
60. Klikněte na možnost Přidat kořen.
    * Vložte vypočítané pole jako nový zdroj dat.  
61. Do pole Název zadejte „ProcessingDateTime“.
    * ProcessingDateTime  
62. Do pole Popisek zadejte „Datum a čas zpracování“.
    * Datum a čas zpracování  
63. Klikněte na možnost Upravit vzorec.
64. Ve stromové struktuře vyberte 'Datum/čas\SESSIONNOW'.
65. Klikněte na možnost Přidat funkci.
66. Klikněte na položku Uložit.
67. Zavřete stránku.
68. Klikněte na tlačítko OK.
    * Přidejte vypočítané pole ProcessingDateTime jako zdroj dat pro aktuální model data.  
69. Klikněte na položku Uložit.
70. Zavřete stránku.
71. Zavřete stránku.
72. Zavřete stránku.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]