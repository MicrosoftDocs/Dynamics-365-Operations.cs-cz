--- 
title: "Mapování datového modelu na zvolené zdroje dat pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo návrháře elektronického výkaznictví může mapovat datový model elektronického výkaznictví (ER) na vybrané zdroje dat Dynamics 365 for Finance and Operations, Enterprise edition (říjen 2016)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 13b7fe7f7bfe24bd275428e931993aa46ecb9945
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a>Mapování datového modelu na zvolené zdroje dat pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo návrháře elektronického výkaznictví může mapovat datový model elektronického výkaznictví (ER) na vybrané zdroje dat Dynamics 365 for Finance and Operations. Toto mapování modelu bude později použito jako zdroj dat v konfiguraci formátu, která se použije ke správě dokumentů elektronické platby. V tomto příkladu namapujete datový model pro vzorovou společnost Litware, Inc. na zdroje dat. Aby bylo možné tyto kroky provést, musíte nejprve dokončit kroky postupu „Volba zdroje dat pro mapování modelu“.


## <a name="open-er-configurations-tree"></a>Otevření stromu konfigurací elektronického vykazování
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace.

## <a name="select-created-model-mapping"></a>Volba vytvořeného mapování modelu
1. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.
    * Ujistěte se, že byla předem vytvořena konfigurace modelu „Platby (zjednodušený model)“. V opačném případě nyní přestaňte a vraťte se po dokončení průvodce záznamem úloh ‘Vytvoření nové konfigurace s datovým modelem zvolené domény‘.  
2. Klikněte na Návrhář modelů.
3. Klikněte na možnost Mapovat model na datový zdroj.
4. Vyberte záznam „Mapování Dal“.
    * Mapování Dal  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Vytvoření vazby vytvořených zdrojů dat s prvky datového modelu
1. Klikněte na možnost Návrhář.
2. Ve stromovém zobrazení vyberte možnost „Datum a čas zpracování(ProcessingDateTime)“.
3. Ve stromovém zobrazení vyberte možnost „Datum zpracování(ProcessingDateTime)“.
4. Klikněte na možnost Vazba.
5. Ve stromovém zobrazení vyberte „Identifikace zprávy o platbě(MessageIdentification)“.
6. Ve stromovém zobrazení rozbalte možnost Transakce.
7. Ve stromovém zobrazení vyberte „Transakce\Číslo dávky deníku(JournalNum)“.
8. Klikněte na možnost Vazba.
9. Ve stromu vyberte „Platby“.
10. Ve stromovém zobrazení vyberte možnost „Transakce“.
11. Klikněte na možnost Vazba.
12. Ve stromovém zobrazení rozbalte „Platby= Transakce“.
13. Ve stromovém zobrazení rozbalte „Platby= Transakce\Věřitel“.
14. Ve stromovém zobrazení rozbalte „Platby= Transakce\Věřitel\Účet“.
15. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Účet\Kód měny(Měna)“.
16. Ve stromovém zobrazení rozbalte „Transakce\vendBankAccountInTransactionCompany()“.
17. Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)“.
18. Klikněte na možnost Vazba.
19. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Účet\Kód IBAN (IBAN)“.
20. Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)“.
21. Klikněte na možnost Vazba.
22. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Účet\Číslo“.
23. Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Číslo bankovního účtu(AccountNum)“.
24. Klikněte na možnost Vazba.
25. Ve stromovém zobrazení rozbalte „Platby= Transakce\Věřitel\Zástupce“.
26. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Zástupce\Jméno“.
27. Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Název“.
28. Klikněte na možnost Vazba.
29. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Zástupce\Směrový kód(RoutingNumber)“.
30. Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Směrový kód(RegistrationNum)“.
31. Klikněte na možnost Vazba.
32. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Zástupce\Kód SWIFT(SWIFT)“.
33. Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Kód SWIFT(SWIFTNo)“.
34. Klikněte na možnost Vazba.
35. Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Název“.
36. Ve stromovém zobrazení rozbalte „Transakce\findVendTable()“.
37. Ve stromovém zobrazení vyberte „Transakce\findVendTable()\name()'.
38. Klikněte na možnost Vazba.
39. Ve stromovém zobrazení vyberte „Platby= Transakce\Kód měny(Měna)“.
40. Ve stromovém zobrazení rozbalte Transactions\>Relations.
41. Ve stromovém zobrazení rozbalte Transactions\>Relations\Currency table(Currency).
42. Ve stromovém zobrazení vyberte Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO).
43. Klikněte na možnost Vazba.
44. Ve stromovém zobrazení rozbalte „Platby= Transakce\Dlužník“.
45. Ve stromovém zobrazení rozbalte „Platby= Transakce\Dlužník\Účet“.
46. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Účet\Kód měny(Měna)“.
47. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)“.
48. Ve stromovém zobrazení rozbalte „Bankovní účet(BankAccount)“.
49. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Měna(CurrencyCode)“.
50. Klikněte na možnost Vazba.
51. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\IBAN“.
52. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Účet\Kód IBAN(IBAN)“.
53. Klikněte na možnost Vazba.
54. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Účet\Číslo“.
55. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Číslo bankovního účtu(AccountNum)“.
56. Klikněte na možnost Vazba.
57. Ve stromovém zobrazení rozbalte „Platby= Transakce\Dlužník\Zástupce“.
58. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Zástupce\Jméno“.
59. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Název“.
60. Klikněte na možnost Vazba.
61. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Zástupce\Směrový kód(RoutingNumber)“.
62. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Směrový kód(RegistrationNum)“.
63. Klikněte na možnost Vazba.
64. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Zástupce\Kód SWIFT(SWIFT)“.
65. Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Kód SWIFT(SWIFTNo)“.
66. Klikněte na možnost Vazba.
67. Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Název“.
68. Ve stromovém zobrazení vyberte „Informace o společnosti(Společnost)“.
69. Ve stromovém zobrazení rozbalte „Informace o společnosti(Společnost)“.
70. Ve stromovém zobrazení vyberte „Informace o společnosti(Společnost)\Název“.
71. Klikněte na možnost Vazba.
72. Ve stromovém zobrazení vyberte „Platby= Transakce\Popis“.
73. Ve stromovém zobrazení vyberte „Transakce\Popis(Txt)“.
74. Klikněte na možnost Vazba.
75. Ve stromovém zobrazení vyberte „Platby= Transakce\Koncový identifikační kód(End2EndID)“.
76. Ve stromovém zobrazení vyberte možnost 'Transactions\$EndToEndID.
77. Klikněte na možnost Vazba.
78. Ve stromovém zobrazení vyberte „Platby= Transakce\Požadovaná částka(InstructedAmount)“.
79. Ve stromovém zobrazení vyberte možnost Transactions\$Amount.
80. Klikněte na možnost Vazba.
81. Ve stromovém zobrazení vyberte „Platby= Transakce\Datum transakce(TransactionDate)“.
82. Ve stromovém zobrazení vyberte „Transakce\Datum(TransDate)“.
83. Klikněte na možnost Vazba.

## <a name="validate-created-mapping"></a>Ověření vytvořeného mapování
1. Klikněte na tlačítko Ověřit.
    * Ověřte nové mapování, abyste se ujistili, že všechny vazby jsou v pořádku.  
2. Kliknutím na šipku rozbalte nebo sbalte oddíl Seznam chyb.
3. Klikněte na položku Uložit.
4. Zavřete stránku.
5. Zavřete stránku.
6. Zavřete stránku.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Změna stavu aktuální verze konfigurace modelu
1. Klikněte na položku Změnit stav.
    * Změňte stav navržené konfigurace modelu z Návrh na Dokočeno, aby byla konfigurace dostupná pro návrh formátu platby.  
2. Klikněte na tlačítko Dokončit.
    * Zvolte Dokončeno.  
3. Zadejte nějakou hodnotu do pole Popis.
    * Například 'verze 1'.  
4. Klikněte na tlačítko OK.
5. Vyberte dokončenou verzi aktuální konfigurace.
    * Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.  


