--- 
title: "Úprava formátů opětovným použitím šablon aplikace Excel"
description: "K provedení kroků v tomto postupu musíte nejprve dokončit průvodce záznamem úloh s názvem „ER – návrh konfigurace pro generování sestav ve formátu OPENXML“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Úprava formátů opětovným použitím šablon aplikace Excel

[!include [task guide banner](../../includes/task-guide-banner.md)]

K provedení kroků v tomto postupu musíte nejprve dokončit průvodce záznamem úloh s názvem „ER – návrh konfigurace pro generování sestav ve formátu OPENXML“.

Tento postup popisuje, jak změnit konfiguraci formátu elektronického vykazování (ER) opakovaným použitím šablony aplikace Microsoft Excel, která byla změněna. V tomto postupu naimportujete upravenou šablonu aplikace Excel do konfigurace formátu ER, která byla vytvořena pro vzorovou společnost Litware, Inc., a poté vygenerujete elektronické dokumenty. Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Tyto kroky lze dokončit za použití datové sady GBSI. Předtím, než začnete, si stáhněte a uložte soubor SampleVendPaymWsReport2.xlsx, který je uveden v tématu nápovědy, Změna formátu elektronického vykazování opakovaným použitím šablony Excel (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template/).

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.  

## <a name="select-the-er-format"></a>Vyberte formát ER
1. Klikněte na Konfigurace výkaznictví.
2. Ve stromovém zobrazení rozbalte „Model platby“.
3. Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.
4. Klikněte na Přílohy.
    * Všimněte si, že soubor SampleVendPaymWsReport.xlsx aplikace Excel aktuálně slouží jako šablona pro zpracování deníku plateb.   
5. Klikněte na možnost Otevřít.
    * Klepnutím na tlačítko Otevřít prozkoumejte rozvržení šablony Excel.  
    * Prohlédněte si šablonu. Všimněte si, že aktuálně zahrnuje následující informace pro každý řádek platby: číslo účtu dodavatele, jméno dodavatele, banku, směrovací číslo, číslo účtu, částku má dáti, dal a měnu. V tomto příkladu chceme doplnit tento seznam přidáním podrobných informací o datu platby.   
6. Zavřete stránku.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Znovu použijte novou šablonu aplikace Excel pro formát ER
1. Klikněte na možnost Návrhář.
    * Otevřete pracovní verzi vybraného formátu ER pro vaše úpravy.  
2. V podokně akcí klikněte na možnost Importovat.
3. Klikněte na Aktualizace z aplikace Excel.
    * Klepněte na Aktualizovat šablony a vyberte soubor SampleVendPaymWsReport2.xlsx.  
    * Klepněte na tlačítko Aktualizovat šablonu a vyhledejte dříve stažený soubor SampleVendPaymWsReport2.xlsx.  
4. Klikněte na tlačítko OK.
    * Je použita šablona SampleVendPaymWsReport2.xlsx. Struktura formátu ER je synchronizována s obsahem šablony, jejíž prvky jsou přidány do formátu ER. Existující prvky ve formátu ER, které nejsou zahrnuty v šablony jsou odebrány z definice formátu.  
5. Ve stromovém zobrazení vyberte Excel.
    * Poznámka: pole Šablona nyní obsahuje odkaz na novou šablonu.   
6. Klikněte na Přílohy.
7. Klikněte na možnost Otevřít.
    * Klepnutím na tlačítko Otevřít prozkoumejte rozvržení upravené šablony Excel.  
    * Prohlédněte si šablonu. Všimněte si, že nyní obsahuje jeden řádek pro datum platby.   
8. Zavřete stránku.
9. Ve stromovém zobrazení rozbalte Excel.
10. Ve stromové struktuře rozbalte 'Excel\PaymLines'.
11. Ve stromovém zobrazení vyberte Excel\PaymLines\PaymDate.
    * Všimněte si, že formát ER nyní obsahuje více položek. Buňka, PaymDate, byla přidána do šablony Excel.  
12. Klikněte na kartu Mapování.
13. Ve stromovém zobrazení rozbalte „model“.
14. Ve stromovém zobrazení rozbalte „model\Platby“.
15. Ve stromovém zobrazení vyberte „model\Platby\Datum transakce(TransactionDate)“.
16. Klikněte na možnost Vazba.
    * Určete, jaká data budou za běhu přidána do nové buňky.  
17. Klikněte na položku Uložit.
18. Zavřete stránku.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Povolte použití upravené pracovní verze formátu ER při zpracování deníku plateb
1. V podokně akcí klikněte na možnost Konfigurace.
2. Klikněte na Parametry uživatelů.
3. Vyberte možnost Ano v poli Nastavení běhu.
4. Klikněte na tlačítko OK.
5. Klikněte na položku Upravit.
6. Vyberte možnost Ano v poli Koncept běhu.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Použijte upravené pracovní verze formátu ER při zpracování deníku plateb
    * Zkontrolujte vytvořený seznam včetně nových podrobností o řádcích platby – datum platby.  


