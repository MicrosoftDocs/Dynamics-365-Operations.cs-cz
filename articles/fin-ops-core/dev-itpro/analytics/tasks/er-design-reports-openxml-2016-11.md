---
title: Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML (listopad 2016)
description: Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje šablonu pro generování elektronických dokladů ve formátu OPENXML.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcceb0e4d5f3bec54598515da0a5cbd8d11def3d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769848"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML (listopad 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje šablonu pro generování elektronických dokladů ve formátu OPENXML. Tato konfigurace se použije ke zpracování plateb dodavatele.

V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést ve společnosti GBSI.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního". Je třeba mít k dispozici soubor aplikace Excel, který bude importován při vytváření šablony. K tomuto souboru lze přistoupit ze [šablony sestavy platby](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>Odeslání konfigurace modelu platebních dat
1. V navigačním podokně přejděte na **Moduly > Správa organizace > Pracovní prostory > Elektronické vykazování**.
2. V seznamu označte konfiguraci pro vzorovou společnost Litware, Inc. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení za aktivní](er-configuration-provider-mark-it-active-2016-11.md).
3. Vyberte **Nastavit jako aktivní**.
4. Vyberte **Úložiště**. Vyberte úložiště pro typ Provozní prostředky (pokud je k dispozici). Pokud k dispozici je, přeskočte následující kroky týkající se vytváření nového úložiště.  
5. Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.
6. V poli **Typ úložiště konfigurace** zadejte `Operations resourcesdd`.
7. Zvolte **Vytvořit úložiště**.
8. Vyberte **OK**.
9. Zvolte **Otevřít**.
10. Ve stromovém zobrazení vyberte **Model platby**.
11. Vyberte **Import**. Importujte tento model dat. Použije se jako zdroj dat v nové konfiguraci formátu. Tento krok vynechejte, je-li tato konfigurace již importována.  
12. Vyberte **Ano**.
13. Zavřete stránky, dokud se nevrátíte na stránku elektronického výkaznictví.

## <a name="create-a-new-format-configuration"></a>Vytvoření nové konfigurace formátu
1. Vyberte **Konfigurace vykazování**.
2. Ve stromovém zobrazení vyberte **Model platby**.
3. Výběrem možnosti **Vytvořit konfiguraci** otevřete dialogové okno.
4. Do pole **Nový** zadejte `Format based on data model PaymentModel`. Vytvořte formát, který vychází z modelu dat PaymentModel.
5. Do pole **Název** zadejte `Sample worksheet report`. Ukázková sestava listu  
6. Do pole **Popis** zadejte `Sample worksheet report for vendors’ payments`. Ukázková sestavu listu pro platby dodavatelů.  
7. V poli **Definice datového modelu** zadejte nebo vyberte hodnotu. Vyberte definici **CustomerCreditTransferInitiation**.  
8. Vyberte **Vytvořit konfiguraci**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Návrh nového dokumentu ve formátu listu OPENXML
1. Ve stromovém zobrazení vyberte **Model platby\Ukázková sestava listu**.
2. Vyberte možnost **Návrhář**.
3. V podokně akcí klikněte na možnost **Import**.
4. Vyberte možnost **Import z aplikace Excel**.
5. Vyberte **Přílohy**. Připojte existující dokument Excel jako šablonu.  
6. Zvolte **Nové**.
7. Vyberte možnost **Soubor**. Odkažte na existující soubor aplikace Excel.  
8. Zavřete stránku.
9. V poli **Šablona** zadejte nebo vyberte hodnotu. Určete, že chcete použít připojený soubor aplikace Excel jako šablonu.  
10. Vyberte **OK**. Všimněte si, že komponenty formátu ER byly vytvořeny v navrženém formátu v závislosti na struktuře odkazovaného dokumentu aplikace MS Excel (rozsahy s názvy).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Vytvoření nového zdroje dat pro výpočet součtů podle kódů měn
1. Zvolte kartu **Mapování**.
2. Výběrem možnosti **Přidat kořen** otevřete dialogové okno.
3. Ve stromovém zobrazení vyberte možnost **Funkce\Seskupit podle**.
4. Do pole **Název** zadejte `PaymentByCurrency`.
5. Vyberte možnost **Upravit skupinu podle**.
6. Ve stromové struktuře rozbalte **model**a pak vyberte **model\Platby**.
7. Vyberte **Přidat pole do**.
8. Vyberte možnost **Skupina Co**.
9. Ve stromové struktuře rozbalte **model\Platby**a pak vyberte **model\Platby\Měna**.
10. Vyberte **Přidat pole do**.
11. Vyberte **Seskupená pole**.
12. Ve stromovém zobrazení vyberte **model\Platby\Požadovaná částka(InstructedAmount)**.
13. Vyberte možnost **Přidat pole do** a poté vyberte **Pole agregace**.
14. Vyberte volbu v poli **Metoda**. Vyberte funkci **Agregace SUM**.  
15. Do pole **Název** zadejte `TotalInstructuredAmount`.
16. Zvolte **Uložit**.
17. Zavřete stránku.
18. Vyberte **OK**.

## <a name="map-format-components-to-data-sources"></a>Mapování součástí formátu na zdroje dat
1. Ve stromovém zobrazení vyberte **model\Platby\Strana příkazce(InitiatingParty)\Název** a **Excel\ReportHeader\CompanyName**.
2. Vyberte možnost **vazba**.
3. Ve stromovém zobrazení vyberte **model\Platby\Účet věřitele\Identifikace\ID zdroje(SourceID)** a **Excel\PaymLines\VendAccountName**.
4. Vyberte možnost **vazba**.
5. Ve stromovém zobrazení vyberte **model\Platby\Účet věřitele\Název** a **Excel\PaymLines\VendName**.
6. Vyberte možnost **vazba**.
7. Ve stromovém zobrazení vyberte **model\Platby\Agent věřitele(CreditorAgent)\Název** a **Excel\PaymLines\Bank**.
8. Vyberte možnost **vazba**.
9. Ve stromovém zobrazení vyberte **model\Platby\Agent věřitele(CreditorAgent)\Směrový kód(RoutingNumber)** a **Excel\PaymLines\RoutingNumber**.
10. Vyberte možnost **vazba**.
11. Ve stromovém zobrazení vyberte **model\Platby\Účet věřitele(CreditorAccount)\Identifikace\Číslo** a **Excel\PaymLines\AccountNumber**.
12. Vyberte možnost **vazba**.
13. Ve stromovém zobrazení vyberte **model\Platby\Požadovaná částka(InstructedAmount)** a **Excel\PaymLines\Debit**.
14. Vyberte možnost **vazba**.
15. Ve stromovém zobrazení vyberte **model\Platby\Měna** a **Excel\PaymLines\Currency**.
16. Vyberte možnost **vazba**.
17. Ve stromové struktuře vyberte **PaymentByCurrency\grouped\Currency** a **Excel\SummaryLines\SummaryCurrency**.
18. Vyberte možnost **vazba**.
19. Ve stromové struktuře vyberte **PaymentByCurrency\aggregated\TotalInstructuredAmount** a **Excel\SummaryLines\SummaryAmount**.
20. Vyberte možnost **vazba**.
21. Ve stromové struktuře vyberte **PaymentByCurrency** a **Excel\SummaryLines**.
22. Vyberte možnost **vazba**.
23. Ve stromovém zobrazení vyberte **model\Platby** a **Excel\PaymLines**.
24. Vyberte možnost **vazba**.
25. Zvolte **Uložit** a poté zavřete stránku.

## <a name="use-the-created-configuration-for-payments-processing"></a>Použití vytvořené konfigurace pro zpracování plateb
1. Vyberte **Změnit stav**.
2. Zvolte **Dokončit**.
3. Vyberte **OK**.
4. V navigačním podokně přejděte na **Moduly > Závazky > Nastavení platby > Metody platby**.
5. Použijte rychlý filtr k filtrování v poli **Metoda platby** s hodnotou **Elektronická**.
6. Vyberte možnost **Upravit**.
7. Rozbalte oddíl **Formáty souborů**.
8. Vyberte možnost **Ano** v poli **Obecné elektronické výkaznictví**.
9. V poli **Exportovat konfiguraci formátu** zadejte nebo vyberte hodnotu. Vyberte konfiguraci **Ukázková sestava listu**.  
10. Zvolte **Uložit**.
11. Zavřete stránku.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Použití vytvořené konfigurace pro testování zpracování deníků plateb
1. V navigačním podokně přejděte na **Moduly > Závazky > Platby > Deník plateb**.
2. Zvolte **Nový** pro vytvoření nového deníku plateb.
3. Zadejte text **VendPay** do pole **Název**.
4. Vybrat **řádky**.
5. Zadejte hodnotu `GB_SI_000001` do pole **Účet**.
6. Nastavte **Má dáti** na `1000`.
7. Zvolte **Nové**.
8. Zadejte hodnotu `GB_SI_000005` do pole **Účet**.
9. Nastavte **Má dáti** na `2000`.
10. Zadejte `EUR` do pole **Měna**.
11. Zadejte hodnoty `GBSI OPER` do pole **Protiúčet**.
12. Do pole **Metoda platby** zadejte `Electronic`.
13. Zvolte **Uložit**.
14. Vyberte **Generovat platby**.
15. Do pole **Metoda platby** zadejte `Electronic`.
16. Do pole **Název souboru** zadejte `Payments`.
17. V poli **Bankovní účet** zadejte `GBSI OPER`.
18. Vyberte **OK** a potom znovu **OK**. Zkontrolujte vytvořený list, včetně podrobností na řádcích platby, stejně tak jako součty pro každý kód měny používaný v této platební zprávě.  

