--- 
title: "Úprava formátu opětovným použitím šablony aplikace Microsoft Excel pro elektronické výkaznictví (ER)"
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
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a><span data-ttu-id="6c153-103">Úprava formátu opětovným použitím šablony aplikace Microsoft Excel pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="6c153-103">Modify a format by reapplying a Microsoft Excel template for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c153-104">K provedení kroků v tomto postupu musíte nejprve dokončit průvodce záznamem úloh s názvem „ER – návrh konfigurace pro generování sestav ve formátu OPENXML“.</span><span class="sxs-lookup"><span data-stu-id="6c153-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="6c153-105">Tento postup popisuje, jak změnit konfiguraci formátu elektronického vykazování (ER) opakovaným použitím šablony aplikace Microsoft Excel, která byla změněna.</span><span class="sxs-lookup"><span data-stu-id="6c153-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="6c153-106">V tomto postupu naimportujete upravenou šablonu aplikace Excel do konfigurace formátu ER, která byla vytvořena pro vzorovou společnost Litware, Inc., a poté vygenerujete elektronické dokumenty.</span><span class="sxs-lookup"><span data-stu-id="6c153-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="6c153-107">Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="6c153-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="6c153-108">Tyto kroky lze dokončit za použití datové sady GBSI.</span><span class="sxs-lookup"><span data-stu-id="6c153-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="6c153-109">Předtím, než začnete, si stáhněte a uložte soubor SampleVendPaymWsReport2.xlsx, který je uveden v tématu nápovědy, Změna formátu elektronického vykazování opakovaným použitím šablony Excel (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="6c153-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="6c153-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6c153-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6c153-111">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní.</span><span class="sxs-lookup"><span data-stu-id="6c153-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="6c153-112">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.</span><span class="sxs-lookup"><span data-stu-id="6c153-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="6c153-113">Vyberte formát ER</span><span class="sxs-lookup"><span data-stu-id="6c153-113">Select the ER format</span></span>
1. <span data-ttu-id="6c153-114">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6c153-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="6c153-115">Ve stromovém zobrazení rozbalte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="6c153-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="6c153-116">Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="6c153-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="6c153-117">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="6c153-117">Click Attachments.</span></span>
    * <span data-ttu-id="6c153-118">Všimněte si, že soubor SampleVendPaymWsReport.xlsx aplikace Excel aktuálně slouží jako šablona pro zpracování deníku plateb.</span><span class="sxs-lookup"><span data-stu-id="6c153-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="6c153-119">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="6c153-119">Click Open.</span></span>
    * <span data-ttu-id="6c153-120">Klepnutím na tlačítko Otevřít prozkoumejte rozvržení šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="6c153-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="6c153-121">Prohlédněte si šablonu.</span><span class="sxs-lookup"><span data-stu-id="6c153-121">Review the template.</span></span> <span data-ttu-id="6c153-122">Všimněte si, že aktuálně zahrnuje následující informace pro každý řádek platby: číslo účtu dodavatele, jméno dodavatele, banku, směrovací číslo, číslo účtu, částku má dáti, dal a měnu.</span><span class="sxs-lookup"><span data-stu-id="6c153-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="6c153-123">V tomto příkladu chceme doplnit tento seznam přidáním podrobných informací o datu platby.</span><span class="sxs-lookup"><span data-stu-id="6c153-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="6c153-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c153-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="6c153-125">Znovu použijte novou šablonu aplikace Excel pro formát ER</span><span class="sxs-lookup"><span data-stu-id="6c153-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="6c153-126">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c153-126">Click Designer.</span></span>
    * <span data-ttu-id="6c153-127">Otevřete pracovní verzi vybraného formátu ER pro vaše úpravy.</span><span class="sxs-lookup"><span data-stu-id="6c153-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="6c153-128">V podokně akcí klikněte na možnost Importovat.</span><span class="sxs-lookup"><span data-stu-id="6c153-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="6c153-129">Klikněte na Aktualizace z aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="6c153-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="6c153-130">Klepněte na Aktualizovat šablony a vyberte soubor SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="6c153-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="6c153-131">Klepněte na tlačítko Aktualizovat šablonu a vyhledejte dříve stažený soubor SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="6c153-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="6c153-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c153-132">Click OK.</span></span>
    * <span data-ttu-id="6c153-133">Je použita šablona SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="6c153-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="6c153-134">Struktura formátu ER je synchronizována s obsahem šablony, jejíž prvky jsou přidány do formátu ER.</span><span class="sxs-lookup"><span data-stu-id="6c153-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="6c153-135">Existující prvky ve formátu ER, které nejsou zahrnuty v šablony jsou odebrány z definice formátu.</span><span class="sxs-lookup"><span data-stu-id="6c153-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="6c153-136">Ve stromovém zobrazení vyberte Excel.</span><span class="sxs-lookup"><span data-stu-id="6c153-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="6c153-137">Poznámka: pole Šablona nyní obsahuje odkaz na novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="6c153-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="6c153-138">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="6c153-138">Click Attachments.</span></span>
7. <span data-ttu-id="6c153-139">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="6c153-139">Click Open.</span></span>
    * <span data-ttu-id="6c153-140">Klepnutím na tlačítko Otevřít prozkoumejte rozvržení upravené šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="6c153-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="6c153-141">Prohlédněte si šablonu.</span><span class="sxs-lookup"><span data-stu-id="6c153-141">Review the template.</span></span> <span data-ttu-id="6c153-142">Všimněte si, že nyní obsahuje jeden řádek pro datum platby.</span><span class="sxs-lookup"><span data-stu-id="6c153-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="6c153-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c153-143">Close the page.</span></span>
9. <span data-ttu-id="6c153-144">Ve stromovém zobrazení rozbalte Excel.</span><span class="sxs-lookup"><span data-stu-id="6c153-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="6c153-145">Ve stromové struktuře rozbalte 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="6c153-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="6c153-146">Ve stromovém zobrazení vyberte Excel\PaymLines\PaymDate.</span><span class="sxs-lookup"><span data-stu-id="6c153-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="6c153-147">Všimněte si, že formát ER nyní obsahuje více položek.</span><span class="sxs-lookup"><span data-stu-id="6c153-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="6c153-148">Buňka, PaymDate, byla přidána do šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="6c153-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="6c153-149">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="6c153-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="6c153-150">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="6c153-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="6c153-151">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="6c153-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="6c153-152">Ve stromovém zobrazení vyberte „model\Platby\Datum transakce(TransactionDate)“.</span><span class="sxs-lookup"><span data-stu-id="6c153-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="6c153-153">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="6c153-153">Click Bind.</span></span>
    * <span data-ttu-id="6c153-154">Určete, jaká data budou za běhu přidána do nové buňky.</span><span class="sxs-lookup"><span data-stu-id="6c153-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="6c153-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6c153-155">Click Save.</span></span>
18. <span data-ttu-id="6c153-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c153-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="6c153-157">Povolte použití upravené pracovní verze formátu ER při zpracování deníku plateb</span><span class="sxs-lookup"><span data-stu-id="6c153-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="6c153-158">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6c153-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="6c153-159">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="6c153-159">Click User parameters.</span></span>
3. <span data-ttu-id="6c153-160">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="6c153-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="6c153-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c153-161">Click OK.</span></span>
5. <span data-ttu-id="6c153-162">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="6c153-162">Click Edit.</span></span>
6. <span data-ttu-id="6c153-163">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="6c153-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="6c153-164">Použijte upravené pracovní verze formátu ER při zpracování deníku plateb</span><span class="sxs-lookup"><span data-stu-id="6c153-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="6c153-165">Zkontrolujte vytvořený seznam včetně nových podrobností o řádcích platby – datum platby.</span><span class="sxs-lookup"><span data-stu-id="6c153-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


