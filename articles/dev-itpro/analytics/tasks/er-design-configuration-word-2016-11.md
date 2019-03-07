---
title: Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word
description: Následující kroky vysvětlují, jak uživatel v roli správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formáty elektronického výkaznictví pro generování sestav v podobě souborů aplikace Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "362342"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="fa719-103">Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="fa719-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa719-104">Následující kroky vysvětlují, jak uživatel v roli správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formáty elektronického výkaznictví pro generování sestav v podobě souborů aplikace Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="fa719-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="fa719-105">Tyto kroky lze provést v rámci společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="fa719-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="fa719-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh s názvem „Vytvoření konfigurace ER pro generování sestav ve formátu OPENXML“.</span><span class="sxs-lookup"><span data-stu-id="fa719-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="fa719-107">Předem musíte také stáhnout a uložit následující šablony pro vzorovou sestavu:</span><span class="sxs-lookup"><span data-stu-id="fa719-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="fa719-108">Šablona sestavy platby</span><span class="sxs-lookup"><span data-stu-id="fa719-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="fa719-109">Vázaná šablona sestavy platby</span><span class="sxs-lookup"><span data-stu-id="fa719-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="fa719-110">Tento postup je určený pro funkci, která byla přidána do Microsoft Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="fa719-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="fa719-111">Volba existující konfigurace sestavy ER</span><span class="sxs-lookup"><span data-stu-id="fa719-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="fa719-112">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fa719-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fa719-113">Ujistěte se, že je poskytovatel konfigurace ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="fa719-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="fa719-114">zvolen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="fa719-114">is selected as active.</span></span>  
2. <span data-ttu-id="fa719-115">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fa719-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="fa719-116">Znovu použijeme existující konfiguraci ER, která byla původně vytvořena ke generování výstupu sestavy ve formátu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="fa719-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="fa719-117">Ve stromovém zobrazení rozbalte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="fa719-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="fa719-118">Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="fa719-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="fa719-119">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="fa719-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="fa719-120">Výměna šablony aplikace Excel za šablonu aplikace Word</span><span class="sxs-lookup"><span data-stu-id="fa719-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="fa719-121">V současné době se používá dokument Excel jako šablona pro generování výstupu ve formátu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="fa719-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="fa719-122">Budeme importovat šablonu sestavy ve formátu Word.</span><span class="sxs-lookup"><span data-stu-id="fa719-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="fa719-123">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="fa719-123">Click Attachments.</span></span>
    * <span data-ttu-id="fa719-124">Nahraďte existující šablonu aplikace Excel za šablonu Word s názvem SampleVendPaymDocReport.docx, kterou jste předtím stáhli.</span><span class="sxs-lookup"><span data-stu-id="fa719-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="fa719-125">Všimněte si, že tato šablona obsahuje pouze rozvržení dokumentu, který chceme generovat jako ER výstup.</span><span class="sxs-lookup"><span data-stu-id="fa719-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="fa719-126">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="fa719-126">Click Delete.</span></span>
3. <span data-ttu-id="fa719-127">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="fa719-127">Click Yes.</span></span>
4. <span data-ttu-id="fa719-128">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fa719-128">Click New.</span></span>
5. <span data-ttu-id="fa719-129">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="fa719-129">Click File.</span></span>
6. <span data-ttu-id="fa719-130">Klikněte na tlačítko Procházet.</span><span class="sxs-lookup"><span data-stu-id="fa719-130">Click Browse.</span></span> <span data-ttu-id="fa719-131">Vyhledejte a zvolte soubor SampleVendPaymDocReport.docx, který jste předtím stáhli.</span><span class="sxs-lookup"><span data-stu-id="fa719-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="fa719-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa719-132">Click OK.</span></span>
    * <span data-ttu-id="fa719-133">Vyberte šablonu, kterou jste stáhli v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="fa719-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="fa719-134">V poli Šablona zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa719-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="fa719-135">Rozšíření šablony aplikace Word přidáním vlastní části XML</span><span class="sxs-lookup"><span data-stu-id="fa719-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="fa719-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fa719-136">Click Save.</span></span>
    * <span data-ttu-id="fa719-137">Kromě uložení změn v konfiguraci aktualizuje připojenou šablonu aplikace Word rovněž akce Uložit.</span><span class="sxs-lookup"><span data-stu-id="fa719-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="fa719-138">Struktura navrženého formátu je přenesena do připojeného dokumentu aplikace Word jako nová vlastní část XML s názvem 'Sestava'.</span><span class="sxs-lookup"><span data-stu-id="fa719-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="fa719-139">Všimněte si, že připojená šablona aplikace Word obsahuje nejen rozvržení dokumentu, který chceme generovat jako ER výstup, ale zároveň i strukturu dat, která budou ER předána do této šablony za běhu.</span><span class="sxs-lookup"><span data-stu-id="fa719-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="fa719-140">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="fa719-140">Click Attachments.</span></span>
    * <span data-ttu-id="fa719-141">Nyní je třeba navázat prvky vlastní části XML Sestava na části dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="fa719-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="fa719-142">Pokud jste obeznámeni s dokumenty Word, které lze navrhovat jako formuláře obsahující ovládací prvky obsahu provázané s prvky vlastních částí XML, projděte si všechny kroky dalšího dílčího úkolu pro vytvoření takového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="fa719-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="fa719-143">Další informace naleznete na odkazu https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="fa719-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="fa719-144">V opačném případě přeskočte všechny kroky v dalším dílčím úkolu.</span><span class="sxs-lookup"><span data-stu-id="fa719-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="fa719-145">Získání aplikace Word s vlastní částí XML pro provedení vazby dat</span><span class="sxs-lookup"><span data-stu-id="fa719-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="fa719-146">Otevřete teno dokument v aplikaci Word a proveďte následující:  – Otevřete kartu Vývojář v aplikaci Word (přizpůsobte si pás karet, pokud není ještě povolena).</span><span class="sxs-lookup"><span data-stu-id="fa719-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="fa719-147">- Vyberte podokno mapování XML.</span><span class="sxs-lookup"><span data-stu-id="fa719-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="fa719-148">- Vyberte ve vyhledávacím poli vlastní část XML ‘Sestava’.</span><span class="sxs-lookup"><span data-stu-id="fa719-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="fa719-149">- Proveďte mapování prvků vybrané vlastní části XML a ovládacích prvků obsahu dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="fa719-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="fa719-150">- Uložte aktualizovaný dokument Word na místní disk.</span><span class="sxs-lookup"><span data-stu-id="fa719-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="fa719-151">Odeslání šablony Word s vlastní částí XML navázanou na ovládací prvky obsahu</span><span class="sxs-lookup"><span data-stu-id="fa719-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="fa719-152">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="fa719-152">Click Delete.</span></span>
2. <span data-ttu-id="fa719-153">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="fa719-153">Click Yes.</span></span>
    * <span data-ttu-id="fa719-154">Přidejte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="fa719-154">Add a new template.</span></span> <span data-ttu-id="fa719-155">Pokud jste dokončili kroky uvedené v předchozím dílčím úkolu, vyberte dokument aplikace Word, který jste připravili a uložili místně.</span><span class="sxs-lookup"><span data-stu-id="fa719-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="fa719-156">V opačném případě vyberte dříve staženou šablonu MS Word SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="fa719-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="fa719-157">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fa719-157">Click New.</span></span>
4. <span data-ttu-id="fa719-158">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="fa719-158">Click File.</span></span>
5. <span data-ttu-id="fa719-159">Klikněte na tlačítko Procházet.</span><span class="sxs-lookup"><span data-stu-id="fa719-159">Click Browse.</span></span> <span data-ttu-id="fa719-160">Vyhledejte a zvolte soubor SampleVendPaymDocReportBounded.docx, který jste předtím stáhli.</span><span class="sxs-lookup"><span data-stu-id="fa719-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="fa719-161">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa719-161">Click OK.</span></span>
6. <span data-ttu-id="fa719-162">V poli Šablona zvolte dokument, který jste stáhli v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="fa719-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="fa719-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fa719-163">Click Save.</span></span>
8. <span data-ttu-id="fa719-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fa719-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="fa719-165">Spuštění formátu pro vytvoření výstupu ve Wordu</span><span class="sxs-lookup"><span data-stu-id="fa719-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="fa719-166">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fa719-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="fa719-167">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="fa719-167">Click User parameters.</span></span>
3. <span data-ttu-id="fa719-168">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="fa719-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="fa719-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa719-169">Click OK.</span></span>
5. <span data-ttu-id="fa719-170">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="fa719-170">Click Edit.</span></span>
6. <span data-ttu-id="fa719-171">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="fa719-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="fa719-172">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fa719-172">Click Save.</span></span>
8. <span data-ttu-id="fa719-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fa719-173">Close the page.</span></span>
9. <span data-ttu-id="fa719-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fa719-174">Close the page.</span></span>
10. <span data-ttu-id="fa719-175">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="fa719-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="fa719-176">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="fa719-176">Click Lines.</span></span>
12. <span data-ttu-id="fa719-177">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="fa719-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="fa719-178">Klikněte na Stav platby.</span><span class="sxs-lookup"><span data-stu-id="fa719-178">Click Payment status.</span></span>
14. <span data-ttu-id="fa719-179">Klikněte na možnost Žádný.</span><span class="sxs-lookup"><span data-stu-id="fa719-179">Click None.</span></span>
15. <span data-ttu-id="fa719-180">Klepněte na Generovat platby.</span><span class="sxs-lookup"><span data-stu-id="fa719-180">Click Generate payments.</span></span>
16. <span data-ttu-id="fa719-181">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa719-181">Click OK.</span></span>
17. <span data-ttu-id="fa719-182">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fa719-182">Click OK.</span></span>
    * <span data-ttu-id="fa719-183">Analyzujte vygenerovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="fa719-183">Analyze the generated output.</span></span> <span data-ttu-id="fa719-184">Povšimnete si, že vytvořený výstup je ve formátu aplikace Word a obsahuje podrobnosti o zpracovaných platbách.</span><span class="sxs-lookup"><span data-stu-id="fa719-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

