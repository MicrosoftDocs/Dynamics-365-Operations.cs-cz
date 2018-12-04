--- 
title: "Použití konfigurací mapování modelu pro agregované výpočty na úrovni databáze"
description: "Tento postup poskytuje informace o způsobu navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: a462a3997644a494b5cea89c9530ddba67c32450
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Použití konfigurací mapování modelu pro agregované výpočty na úrovni databáze

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup poskytuje informace o způsobu navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům. V tomto postupu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. 

Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití libovolné datové sady.

 Provedení těchto kroků vyžaduje provedení kroků v postupu ER vylepšuje efektivitu souhrnných výpočtů provedením na úrovni databáze (část 1: Příprava konfigurace).

1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
3. Ve stromové struktuře vyberte 'Intrastat model\Intrastat sample mapping'.
4. Klikněte na možnost Návrhář.
5. Klikněte na možnost Návrhář.
6. Ve stromové struktuře vyberte Dynamics 365 for Operations\Záznamy tabulky.
7. Klikněte na možnost Přidat kořen.
    * Přidáte nový zdroj dat představující záznamy, které chcete seskupit.  
8. Zadejte text „Transakce“ do pole Název.
    * Transakce  
9. Do pole Tabulka zadejte hodnotu „Intrastat“.
    * Systém Intrastat  
10. Klikněte na tlačítko OK.
11. Ve stromovém zobrazení vyberte možnost „Funkce\Seskupit podle “.
    * Tento typ zdroje dat slouží k zavedení nového zdroje dat za běhu pro seskupení záznamů a výpočet požadovaných seskupení.  
12. Klikněte na možnost Přidat kořen.
13. Do pole Název zadejte TransactionsGroups.
    * TransactionsGroups  
14. Klikněte na „Upravit skupinu podle“.
15. Ve stromovém zobrazení vyberte možnost „Transakce“.
    * Vyberte přidaný zdroj dat typu Seznam záznamů, který představuje záznamy pro seskupení  
16. Klikněte na „Přidat pole do“.
17. Klikněte na „Skupina Co“.
18. Ve stromovém zobrazení rozbalte možnost Transakce.
19. Ve stromovém zobrazení vyberte možnost 'Transactions\Direction'.
20. Klikněte na „Přidat pole do“.
21. Klikněte na „Seskupená pole“.
    * Vyberte pole, pro určení úrovně seskupení. Na základě tohoto výběru zdroj dat vrátí v době běhu tolik skupin transakcí, kolik je kódů směrování splněných v tabulce Intrastat.  
22. Ve stromovém zobrazení vyberte možnost 'Transactions\Invoice amount(AmountMST)'.
    * Vyberte pole pro určení zdroje k výpočtu seskupení.  
23. Klikněte na „Přidat pole do“.
24. Klikněte na „Seskupená pole“.
25. Označte v seznamu vybraný řádek.
26. V poli Metoda vyberte možnost Součet.
    * Vyberte typ seskupení.  
27. Do pole Název napište 'SumOfAmountMST'.
    * Zadejte název tohoto seskupení v konfigurovaném zdroji dat.  
28. Klikněte na položku Uložit.
    * Pole Provedení v označuje, že toto seskupení bude provedeno v době běhu v databázi SQL.  
29. Zavřete stránku.
30. Klikněte na tlačítko OK.
31. Ve stromu rozbalte 'Totals'.
32. Ve stromu rozbalte 'TransactionsGroups'.
33. Ve stromovém zobrazení rozbalte 'TransactionsGroups\aggregated'.
34. Ve stromovém zobrazení vyberte 'TransactionsGroups\aggregated\SumOfAmountMST'.
35. Ve stromovém zobrazení vyberte 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.
36. Klikněte na možnost Vazba.
    * Na základě tohoto nastavení tento zdroj dat vypočítá součet hodnot v poli 'AmountMST' pro jednotlivé skupiny transakcí. Tento výpočet seskupení bude k dispozici jako položka TransactionsGroups.aggregated.TotalAmount.  
37. Ve stromu rozbalte 'TransactionsGroups'.
38. Ve stromovém zobrazení vyberte 'TransactionsGroups'.
39. Klikněte na položku Upravit.
40. Klikněte na „Upravit skupinu podle“.
41. Ve stromovém zobrazení rozbalte možnost Transakce.
42. Ve stromovém zobrazení vyberte možnost 'Transactions\Invoice amount(AmountMST)'.
43. Klikněte na „Přidat pole do“.
44. Klikněte na „Seskupená pole“.
45. Označte v seznamu vybraný řádek.
46. V poli Metoda vyberte možnost Max.
47. V poli název zadejte 'MaxOfAmountMST'.
48. Klikněte na položku Uložit.
    * V současné době lze přeložit provedení zdrojů dat GROUPBY na úrovni databáze SQL s určitými omezeními. Převod lze provést buď pro zdroje dat typu Seznam záznamů, nebo pro zdroje dat vyjádřené jako výraz pomocí funkce FILTER. Lze jej provést také, pouze pokud je nakonfigurována jedna agregace pro jedno pole záznamů seskupení.  
    * Všimněte si, že i když bylo pro pole AmountMST nakonfigurováno více seskupení, pole Provedení v stále označuje, že bude toto seskupení provedeno v době běhu v databázi SQL. Důvodem je skutečnost, že pouze jedno seskupení má vazbu na položku datového modelu a bude použito při spuštění k získání dat z tohoto zdroje dat.  
49. Zavřete stránku.
50. Klikněte na tlačítko OK.
51. Ve stromu rozbalte 'TransactionsGroups'.
52. Ve stromovém zobrazení rozbalte 'TransactionsGroups\aggregated'.
53. Ve stromovém zobrazení vyberte 'TransactionsGroups\aggregated\MaxOfAmountMST'.
54. Ve stromovém zobrazení vyberte 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.
55. Klikněte na možnost Vazba.
56. Ve stromu rozbalte 'TransactionsGroups'.
57. Ve stromovém zobrazení vyberte 'TransactionsGroups'.
58. Klikněte na položku Upravit.
59. Klikněte na „Upravit skupinu podle“.
    * Poznámka: pole 'Provedení v' označuje, že toto seskupení se provede v době běhu v paměti vzhledem k tomu, že obě seskupení stejného pole jsou vázána na položky datového modelu.   
60. V seznamu označte všechny řádky nebo jejich označení zrušte.
61. Klikněte na tlačítko Odstranit.
62. Klepněte na tlačítko Ano.
63. Klikněte na tlačítko Odstranit.
64. Klepněte na tlačítko Ano.
65. Klikněte na „Přidat pole do“.
66. Klikněte na „Skupina Co“.
67. Ve stromovém zobrazení rozbalte 'Commodity record(Intrastat)'.
68. Klikněte na položku Uložit.
    * Poznámka: pole 'Provedení v' označuje, že toto seskupení se provede při spuštění v paměti i v případě, že neexistují žádná seskupení definovaná ve vybraném zdroji dat a vybraný zdroj dat tabulky záznamů typu se vztahuje na stejnou tabulku 'systému Intrastat. Důvodem je skutečnost, že zdroj dat obsahuje některá vypočítaná pole, která nelze ještě převést na úrovni databáze SQL.  


