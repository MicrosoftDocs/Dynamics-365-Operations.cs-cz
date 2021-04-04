---
title: Úprava formátů opětovným použitím šablon aplikace Excel
description: K provedení kroků v tomto postupu musíte nejprve dokončit průvodce záznamem úloh s názvem „ER – návrh konfigurace pro generování sestav ve formátu OPENXML“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ca6707095765c25851ee864a99844a82844fae1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564307"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="41a9a-103">Úprava formátů opětovným použitím šablon aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="41a9a-103">Modify formats by reapplying Excel templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41a9a-104">K provedení kroků v tomto postupu musíte nejprve dokončit průvodce záznamem úloh s názvem „ER – návrh konfigurace pro generování sestav ve formátu OPENXML“.</span><span class="sxs-lookup"><span data-stu-id="41a9a-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="41a9a-105">Tento postup popisuje, jak změnit konfiguraci formátu elektronického vykazování (ER) opakovaným použitím šablony aplikace Microsoft Excel, která byla změněna.</span><span class="sxs-lookup"><span data-stu-id="41a9a-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="41a9a-106">V tomto postupu naimportujete upravenou šablonu aplikace Excel do konfigurace formátu ER, která byla vytvořena pro vzorovou společnost Litware, Inc., a poté vygenerujete elektronické dokumenty.</span><span class="sxs-lookup"><span data-stu-id="41a9a-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="41a9a-107">Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="41a9a-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="41a9a-108">Tyto kroky lze dokončit za použití datové sady GBSI.</span><span class="sxs-lookup"><span data-stu-id="41a9a-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="41a9a-109">Předtím, než začnete, si stáhněte a uložte soubor SampleVendPaymWsReport2.xlsx, který je uveden v tématu nápovědy, Změna formátu elektronického vykazování opakovaným použitím šablony Excel (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="41a9a-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="41a9a-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="41a9a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="41a9a-111">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní.</span><span class="sxs-lookup"><span data-stu-id="41a9a-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="41a9a-112">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu Vytvoření poskytovatele konfigurace a jeho označení jako aktivního.</span><span class="sxs-lookup"><span data-stu-id="41a9a-112">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="41a9a-113">Vyberte formát ER</span><span class="sxs-lookup"><span data-stu-id="41a9a-113">Select the ER format</span></span>
1. <span data-ttu-id="41a9a-114">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="41a9a-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="41a9a-115">Ve stromovém zobrazení rozbalte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="41a9a-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="41a9a-116">Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="41a9a-117">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="41a9a-117">Click Attachments.</span></span>
    * <span data-ttu-id="41a9a-118">Všimněte si, že soubor SampleVendPaymWsReport.xlsx aplikace Excel aktuálně slouží jako šablona pro zpracování deníku plateb.</span><span class="sxs-lookup"><span data-stu-id="41a9a-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="41a9a-119">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="41a9a-119">Click Open.</span></span>
    * <span data-ttu-id="41a9a-120">Klepnutím na tlačítko Otevřít prozkoumejte rozvržení šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="41a9a-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="41a9a-121">Prohlédněte si šablonu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-121">Review the template.</span></span> <span data-ttu-id="41a9a-122">Všimněte si, že aktuálně zahrnuje následující informace pro každý řádek platby: číslo účtu dodavatele, jméno dodavatele, banku, směrovací číslo, číslo účtu, částku má dáti, dal a měnu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="41a9a-123">V tomto příkladu chceme doplnit tento seznam přidáním podrobných informací o datu platby.</span><span class="sxs-lookup"><span data-stu-id="41a9a-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="41a9a-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="41a9a-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="41a9a-125">Znovu použijte novou šablonu aplikace Excel pro formát ER</span><span class="sxs-lookup"><span data-stu-id="41a9a-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="41a9a-126">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="41a9a-126">Click Designer.</span></span>
    * <span data-ttu-id="41a9a-127">Otevřete pracovní verzi vybraného formátu ER pro vaše úpravy.</span><span class="sxs-lookup"><span data-stu-id="41a9a-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="41a9a-128">V podokně akcí klikněte na možnost Importovat.</span><span class="sxs-lookup"><span data-stu-id="41a9a-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="41a9a-129">Klikněte na Aktualizace z aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="41a9a-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="41a9a-130">Klepněte na 'Aktualizovat šablony' a vyberte soubor SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="41a9a-130">Click 'Update template', and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="41a9a-131">Klepněte na tlačítko Aktualizovat šablonu a vyhledejte dříve stažený soubor SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="41a9a-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="41a9a-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="41a9a-132">Click OK.</span></span>
    * <span data-ttu-id="41a9a-133">Je použita šablona SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="41a9a-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="41a9a-134">Struktura formátu ER je synchronizována s obsahem šablony, jejíž prvky jsou přidány do formátu ER.</span><span class="sxs-lookup"><span data-stu-id="41a9a-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="41a9a-135">Existující prvky ve formátu ER, které nejsou zahrnuty v šablony jsou odebrány z definice formátu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-135">Any existing elements in the ER format that aren't included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="41a9a-136">Ve stromovém zobrazení vyberte Excel.</span><span class="sxs-lookup"><span data-stu-id="41a9a-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="41a9a-137">Poznámka: pole Šablona nyní obsahuje odkaz na novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="41a9a-138">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="41a9a-138">Click Attachments.</span></span>
7. <span data-ttu-id="41a9a-139">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="41a9a-139">Click Open.</span></span>
    * <span data-ttu-id="41a9a-140">Klepnutím na tlačítko Otevřít prozkoumejte rozvržení upravené šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="41a9a-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="41a9a-141">Prohlédněte si šablonu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-141">Review the template.</span></span> <span data-ttu-id="41a9a-142">Všimněte si, že nyní obsahuje jeden řádek pro datum platby.</span><span class="sxs-lookup"><span data-stu-id="41a9a-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="41a9a-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="41a9a-143">Close the page.</span></span>
9. <span data-ttu-id="41a9a-144">Ve stromovém zobrazení rozbalte Excel.</span><span class="sxs-lookup"><span data-stu-id="41a9a-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="41a9a-145">Ve stromové struktuře rozbalte 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="41a9a-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="41a9a-146">Ve stromovém zobrazení vyberte Excel\PaymLines\PaymDate.</span><span class="sxs-lookup"><span data-stu-id="41a9a-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="41a9a-147">Všimněte si, že formát ER nyní obsahuje více položek.</span><span class="sxs-lookup"><span data-stu-id="41a9a-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="41a9a-148">Buňka, PaymDate, byla přidána do šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="41a9a-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="41a9a-149">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="41a9a-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="41a9a-150">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="41a9a-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="41a9a-151">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="41a9a-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="41a9a-152">Ve stromovém zobrazení vyberte „model\Platby\Datum transakce(TransactionDate)“.</span><span class="sxs-lookup"><span data-stu-id="41a9a-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="41a9a-153">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="41a9a-153">Click Bind.</span></span>
    * <span data-ttu-id="41a9a-154">Určete, jaká data budou za běhu přidána do nové buňky.</span><span class="sxs-lookup"><span data-stu-id="41a9a-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="41a9a-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="41a9a-155">Click Save.</span></span>
18. <span data-ttu-id="41a9a-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="41a9a-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="41a9a-157">Povolte použití upravené pracovní verze formátu ER při zpracování deníku plateb</span><span class="sxs-lookup"><span data-stu-id="41a9a-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="41a9a-158">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="41a9a-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="41a9a-159">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="41a9a-159">Click User parameters.</span></span>
3. <span data-ttu-id="41a9a-160">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="41a9a-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="41a9a-161">Click OK.</span></span>
5. <span data-ttu-id="41a9a-162">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="41a9a-162">Click Edit.</span></span>
6. <span data-ttu-id="41a9a-163">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="41a9a-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="41a9a-164">Použijte upravené pracovní verze formátu ER při zpracování deníku plateb</span><span class="sxs-lookup"><span data-stu-id="41a9a-164">Use the modified draft version of the ER format for payment journal processing</span></span>

<span data-ttu-id="41a9a-165">Zkontrolujte vytvořený seznam včetně nových podrobností o řádcích platby – datum platby.</span><span class="sxs-lookup"><span data-stu-id="41a9a-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]