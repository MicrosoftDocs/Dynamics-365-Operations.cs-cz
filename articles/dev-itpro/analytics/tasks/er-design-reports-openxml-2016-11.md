--- 
title: "Návrh konfigurace pro generování sestav ve formátu OpenXML pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje šablonu pro generování elektronických dokladů ve formátu OPENXML."
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
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: cs-cz
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Návrh konfigurace pro generování sestav ve formátu OpenXML pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje šablonu pro generování elektronických dokladů ve formátu OPENXML. Tato konfigurace se použije ke zpracování plateb dodavatele.



V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést ve společnosti GBSI.



K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního". Je nutné stáhnout a uložit soubor aplikace Microsoft Excel [Šablona sestavy platby](https://go.microsoft.com/fwlink/?linkid=862266). 

## <a name="upload-the-payments-data-model-configuration"></a>Odeslání konfigurace modelu platebních dat
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Označte v seznamu vybraný řádek.
    * Vyberte poskytovatele konfigurace pro vzorovou společnost 'Litware, Inc.' Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".  
3. Klikněte na možnost Nastavit jako aktivní.
4. Klikněte na možnost Úložiště.
    * Vyberte úložiště pro typ Provozní prostředky (pokud je k dispozici). Pokud k dispozici je, přeskočte následující kroky týkající se vytváření nového úložiště.  
5. Klepnutím na možnost Přidat otevřete dialogové okno.
6. V poli Typ úložiště konfigurace zadejte "Provozní prostředky".
7. Klikněte na Vytvořit úložiště.
8. Klikněte na tlačítko OK.
9. Klikněte na možnost Otevřít.
10. Ve stromovém zobrazení vyberte „Model platby“.
11. Klepněte na tlačítko Importovat.
    * Importujte tento model dat. Použije se jako zdroj dat v nové konfiguraci formátu. Tento krok vynechejte, je-li tato konfigurace již importována.  
12. Klepněte na tlačítko Ano.
13. Zavřete stránku.
14. Zavřete stránku.

## <a name="create-a-new-format-configuration"></a>Vytvoření nové konfigurace formátu
1. Klikněte na Konfigurace výkaznictví.
2. Ve stromovém zobrazení vyberte „Model platby“.
3. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
4. V poli Nový zadejte "Formát založený na datovém modelu PaymentModel".
    * Vytvořte formát, který vychází z modelu dat PaymentModel.  
5. V poli Název zadejte „Ukázková sestava listu“.
    * Ukázková sestava listu  
6. V poli Popis zadejte Ukázková sestavu listu pro platby dodavatelů.
    * Ukázková sestavu listu pro platby dodavatelů.  
7. V poli Definice datového modelu zadejte nebo vyberte hodnotu.
    * Vyberte definici „CustomerCreditTransferInitiation“.  
8. Klepněte na možnost Vytvořit konfiguraci.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Návrh nového dokumentu ve formátu listu OPENXML
1. Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.
2. Klikněte na možnost Návrhář.
3. V podokně akcí klikněte na možnost Importovat.
4. Klikněte na Import z aplikace Excel.
5. Klikněte na Přílohy.
    * Připojte existující dokument Excel jako šablonu.  
6. Klikněte na položku Nová.
7. Klepněte na volby Soubor.
    * Odkažte na existující soubor aplikace Excel.  
8. Zavřete stránku.
9. V poli Šablona zadejte nebo vyberte hodnotu.
    * Určete, že chcete použít připojený soubor aplikace Excel jako šablonu.  
10. Klikněte na tlačítko OK.
    * Všimněte si, že komponenty formátu ER byly vytvořeny v navrženém formátu v závislosti na struktuře odkazovaného dokumentu aplikace MS Excel (rozsahy s názvy).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Vytvoření nového zdroje dat pro výpočet součtů podle kódů měn
1. Klikněte na kartu Mapování.
2. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
3. Ve stromovém zobrazení vyberte možnost „Funkce\Seskupit podle “.
4. Do pole Název zadejte PaymentByCurrency.
    * PaymentByCurrency  
5. Klikněte na „Upravit skupinu podle“.
6. Ve stromovém zobrazení rozbalte „model“.
7. Ve stromovém zobrazení vyberte „model\Platby“.
8. Klikněte na „Přidat pole do“.
9. Klikněte na „Skupina Co“.
10. Ve stromovém zobrazení rozbalte „model\Platby“.
11. Ve stromovém zobrazení vyberte „model\Platby\Měna“.
12. Klikněte na „Přidat pole do“.
13. Klikněte na „Seskupená pole“.
14. Ve stromovém zobrazení vyberte „model\Platby\Požadovaná částka(InstructedAmount)“.
15. Klikněte na „Přidat pole do“.
16. Klikněte na „Seskupená pole“.
17. Vyberte volbu v poli Metoda.
    * Vyberte funkci agregace SUM.  
18. Do pole Název zadejte TotalInstructuredAmount.
    * TotalInstructuredAmount  
19. Klikněte na položku Uložit.
20. Zavřete stránku.
21. Klikněte na tlačítko OK.

## <a name="map-format-components-to-data-sources"></a>Mapování součástí formátu na zdroje dat
1. Ve stromovém zobrazení rozbalte „model“.
2. Ve stromovém zobrazení rozbalte „model\Platby“.
3. Ve stromovém zobrazení rozbalte „model\Platby\Strana příkazce(InitiatingParty)“.
4. Ve stromovém zobrazení vyberte „model\Platby\Strana příkazce(InitiatingParty)\Název“.
5. Ve stromové struktuře rozbalte 'Excel\ReportHeader'.
6. Ve stromové struktuře zvolte 'Excel\ReportHeader\CompanyName'.
7. Klikněte na možnost Vazba.
8. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.
9. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Identifikace“.
10. Ve stromovém zobrazení vyberte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace\ID zdroje(SourceID)“.
11. Ve stromové struktuře rozbalte 'Excel\PaymLines'.
12. Ve stromové struktuře zvolte 'Excel\PaymLines\VendAccountName'.
13. Klikněte na možnost Vazba.
14. Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Název“.
15. Ve stromové struktuře zvolte 'Excel\PaymLines\VendName'.
16. Klikněte na možnost Vazba.
17. Ve stromovém zobrazení rozbalte „model\Platby\Agent věřitele(CreditorAgent)“.
18. Ve stromovém zobrazení vyberte „model\Platby\Agent věřitele(CreditorAgent)\Název“.
19. Ve stromové struktuře zvolte 'Excel\PaymLines\Banka'.
20. Klikněte na možnost Vazba.
21. Ve stromovém zobrazení vyberte „model\Platby\Agent věřitele(CreditorAgent)\Směrový kód(RoutingNumber)“.
22. Ve stromové struktuře zvolte 'Excel\PaymLines\RoutingNumber'.
23. Klikněte na možnost Vazba.
24. Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)“.
25. Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace“.
26. Ve stromovém zobrazení vyberte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace\Číslo“.
27. Ve stromové struktuře zvolte 'Excel\PaymLines\AccountNumber'.
28. Klikněte na možnost Vazba.
29. Ve stromovém zobrazení vyberte „model\Platby\Požadovaná částka(InstructedAmount)“.
30. Ve stromové struktuře zvolte 'Excel\PaymLines\MD'.
31. Klikněte na možnost Vazba.
32. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.
33. Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)“.
34. Ve stromovém zobrazení rozbalte „model\Platby\Agent věřitele(CreditorAgent)“.
35. Ve stromovém zobrazení vyberte „model\Platby\Měna“.
36. Ve stromové struktuře zvolte 'Excel\PaymLines\Měna'.
37. Klikněte na možnost Vazba.
38. Ve stromu rozbalte PaymentByCurrency.
39. Ve stromu rozbalte PaymentByCurrency\seskupeno.
40. Ve stromovém zobrazení vyberte „PaymentByCurrency\seskupeno\Měna“.
41. Ve stromové struktuře rozbalte 'Excel\SummaryLines'.
42. Ve stromové struktuře zvolte 'Excel\SummaryLines\SummaryCurrency'.
43. Klikněte na možnost Vazba.
44. Ve stromu rozbalte PaymentByCurrency\agregováno.
45. Ve stromovém zobrazení vyberte „PaymentByCurrency\agregováno\TotalInstructuredAmount“.
46. Ve stromové struktuře zvolte 'Excel\SummaryLines\SummaryAmount'.
47. Klikněte na možnost Vazba.
48. Ve stromu vyberte PaymentByCurrency.
49. Ve stromové struktuře zvolte 'Excel\SummaryLines'.
50. Klikněte na možnost Vazba.
51. Ve stromovém zobrazení vyberte „model\Platby“.
52. Ve stromové struktuře zvolte 'Excel\PaymLines'.
53. Klikněte na možnost Vazba.
54. Klikněte na položku Uložit.
55. Zavřete stránku.

## <a name="use-the-created-configuration-for-payments-processing"></a>Použití vytvořené konfigurace pro zpracování plateb
1. Klikněte na položku Změnit stav.
2. Klikněte na tlačítko Dokončit.
3. Klikněte na tlačítko OK.
4. Zavřete stránku.
5. Zavřete stránku.
6. Přejděte do nabídky Závazky > Nastavení platby > Metody platby.
7. Použijte rychlý filtr k filtrování v poli Metoda platby s hodnotou 'Elektronická'.
    * Elektronicky  
8. Klikněte na položku Upravit.
9. Rozbalte oddíl Formáty souborů.
10. Vyberte možnost Ano v poli Obecné elektronické výkaznictví.
11. V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.
    * Vyberte konfiguraci Ukázková sestava listu.  
12. Klikněte na položku Uložit.
13. Zavřete stránku.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Použití vytvořené konfigurace pro testování zpracování deníků plateb
1. Přejděte na Závazky > Platby > Deník plateb.
2. Klikněte na položku Nová.
    * Vytvořte nový deník plateb.  
3. Zadejte text „VendPay“ do pole Název.
    * VendPay  
4. Klikněte na položku Řádky.
5. Zadejte hodnoty „GB_SI_000001“ do pole Účet.
    * GB_SI_000001  
6. Nastavte Má dáti na 1000.
7. Klikněte na položku Nová.
8. Zadejte hodnoty „GB_SI_000005“ do pole Účet.
    * GB_SI_000005  
9. Nastavte Má dáti na 2000.
10. Zadejte hodnotu EUR do pole Měna.
    * EUR  
11. Zadejte hodnotu „GBSI OPER“ do pole Protiúčet.
    * GBSI OPER  
12. V poli Způsob platby zadejte „Elektronicky“.
    * Elektronicky  
13. Klikněte na položku Uložit.
14. Klepněte na Generovat platby.
15. V poli Způsob platby zadejte „Elektronicky“.
    * Elektronicky  
16. Do pole Název souboru zadejte 'Platby'.
    * Zadejte například Platby.  
17. V poli Bankovní účet zadejte „GBSI OPER“.
    * GBSI OPER  
18. Klikněte na tlačítko OK.
19. Klikněte na tlačítko OK.
    * Zkontrolujte vytvořený list, včetně podrobností na řádcích platby, stejně tak jako součty pro každý kód měny používaný v této platební zprávě.  


