---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)
description: Tento článek popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 4)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
ms.openlocfilehash: 7610e71346b57a7e624424418b22b40e51f9bb95
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290597"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)

[!include [banner](../../includes/banner.md)]

Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v postupu „Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 3: Používání výpočtů k vytvoření výstupu)“.

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Testování této konfigurace pro generování sestav Intrastat
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Klikněte na Konfigurace výkaznictví.
3. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
4. Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).
5. Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
6. V podokně akcí klikněte na možnost Konfigurace.
7. Klikněte na Parametry uživatelů.
8. Vyberte možnost Ano v poli Nastavení běhu.
9. Klikněte na tlačítko OK.
10. Klikněte na položku Upravit.
11. Vyberte možnost Ano v poli Koncept běhu.
12. Klikněte na položku Uložit.
13. Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.
14. Rozbalte část Elektronické výkaznictví.
15. Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.
16. Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.
17. Klepněte na tlačítko Uložit.
18. Zavřete stránku.
19. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.
20. Klepněte na Výstup.
21. Klikněte na možnost Sestava.
    * Spusťte proces generování sestavy Intrastat.  
22. V poli Datum od nastavte datum a čas na „2000-01-01“ .
    * Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.  
23. V poli Datum do nastavte datum a čas na „2022-12-31“ .
    * Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.  
24. V poli Směr vyberte hodnotu Dovoz.
25. Vyberte možnost Ano v poli Generovat soubor.
26. Klikněte na tlačítko OK.
    * Prohlédněte si vytvořený výstup souhrnných řádků v databázi.  
27. Klikněte na položku Nová.
28. Označte v seznamu vybraný řádek.
29. V poli Směr vyberte hodnotu Expedice.
30. V poli Číslo zboží zadejte nebo vyberte hodnotu.
31. V poli Komodita zadejte nebo vyberte hodnotu.
32. Nastavte hodnotu Váha na 10.
33. Nastavte hodnotu Částka k fakturaci na 10000.
34. Nastavte hodnotu Statistická částka na 10000.
35. Klepněte na Výstup.
36. Klikněte na možnost Sestava.
37. V poli Směr vyberte hodnotu Expedice.
38. Klikněte na tlačítko OK.
    * Prohlédněte si vytvořený výstup souhrnných řádků v databázi. Všimněte si, že byl změněn ve srovnání s prvním spuštěním.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Spuštění této konfigurace v režimu ladění ke kontrole společného počítání a sčítání dat
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
3. Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).
4. Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
5. V podokně akcí klikněte na možnost Konfigurace.
6. Klikněte na Parametry uživatelů.
7. Vyberte možnost Ano v poli Spustit v režimu ladění.
8. Klikněte na tlačítko OK.
9. Zavřete stránku.
10. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.
11. Klepněte na Výstup.
12. Klikněte na možnost Sestava.
13. Klikněte na tlačítko OK.
14. Zavřete stránku.
15. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
16. Ve stromovém zobrazení rozbalte „Modul Intrastat“.
17. Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).
18. Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
19. Klikněte na Protokoly ladění.
    * Všimněte si, že záznam protokolu ladění byl vytvořen pro proces spuštění vybrané konfigurace.  
20. Klikněte na možnost Připojit.
21. Klikněte na možnost Otevřít.
    * Zkontrolujte vytvořený soubor XML, který obsahuje podrobnosti o počítání a sčítání, které byly shromážděny během provádění vybrané konfigurace.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
