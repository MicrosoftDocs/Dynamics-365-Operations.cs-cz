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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="0807e-103">Návrh konfigurace pro generování sestav ve formátu OpenXML pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="0807e-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0807e-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje šablonu pro generování elektronických dokladů ve formátu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="0807e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="0807e-105">Tato konfigurace se použije ke zpracování plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0807e-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="0807e-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést ve společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="0807e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="0807e-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="0807e-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="0807e-108">Je třeba mít k dispozici soubor aplikace Excel, který bude importován při vytváření šablony.</span><span class="sxs-lookup"><span data-stu-id="0807e-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="0807e-109">Tento soubor lze otevřít z adresy https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="0807e-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="0807e-110">Odeslání konfigurace modelu platebních dat</span><span class="sxs-lookup"><span data-stu-id="0807e-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="0807e-111">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0807e-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0807e-112">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0807e-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0807e-113">Vyberte poskytovatele konfigurace pro vzorovou společnost 'Litware, Inc.' Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="0807e-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="0807e-114">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="0807e-114">Click Set active.</span></span>
4. <span data-ttu-id="0807e-115">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="0807e-115">Click Repositories.</span></span>
    * <span data-ttu-id="0807e-116">Vyberte úložiště pro typ Provozní prostředky (pokud je k dispozici).</span><span class="sxs-lookup"><span data-stu-id="0807e-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="0807e-117">Pokud k dispozici je, přeskočte následující kroky týkající se vytváření nového úložiště.</span><span class="sxs-lookup"><span data-stu-id="0807e-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="0807e-118">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0807e-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="0807e-119">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="0807e-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="0807e-120">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="0807e-120">Click Create repository.</span></span>
8. <span data-ttu-id="0807e-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0807e-121">Click OK.</span></span>
9. <span data-ttu-id="0807e-122">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="0807e-122">Click Open.</span></span>
10. <span data-ttu-id="0807e-123">Ve stromovém zobrazení vyberte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="0807e-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="0807e-124">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="0807e-124">Click Import.</span></span>
    * <span data-ttu-id="0807e-125">Importujte tento model dat.</span><span class="sxs-lookup"><span data-stu-id="0807e-125">Import this data model.</span></span> <span data-ttu-id="0807e-126">Použije se jako zdroj dat v nové konfiguraci formátu.</span><span class="sxs-lookup"><span data-stu-id="0807e-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="0807e-127">Tento krok vynechejte, je-li tato konfigurace již importována.</span><span class="sxs-lookup"><span data-stu-id="0807e-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="0807e-128">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="0807e-128">Click Yes.</span></span>
13. <span data-ttu-id="0807e-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-129">Close the page.</span></span>
14. <span data-ttu-id="0807e-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="0807e-131">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="0807e-131">Create a new format configuration</span></span>
1. <span data-ttu-id="0807e-132">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0807e-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="0807e-133">Ve stromovém zobrazení vyberte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="0807e-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="0807e-134">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0807e-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="0807e-135">V poli Nový zadejte "Formát založený na datovém modelu PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="0807e-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="0807e-136">Vytvořte formát, který vychází z modelu dat PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="0807e-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="0807e-137">V poli Název zadejte „Ukázková sestava listu“.</span><span class="sxs-lookup"><span data-stu-id="0807e-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="0807e-138">Ukázková sestava listu</span><span class="sxs-lookup"><span data-stu-id="0807e-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="0807e-139">V poli Popis zadejte Ukázková sestavu listu pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="0807e-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="0807e-140">Ukázková sestavu listu pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="0807e-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="0807e-141">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0807e-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="0807e-142">Vyberte definici „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="0807e-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="0807e-143">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="0807e-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="0807e-144">Návrh nového dokumentu ve formátu listu OPENXML</span><span class="sxs-lookup"><span data-stu-id="0807e-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="0807e-145">Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="0807e-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="0807e-146">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="0807e-146">Click Designer.</span></span>
3. <span data-ttu-id="0807e-147">V podokně akcí klikněte na možnost Importovat.</span><span class="sxs-lookup"><span data-stu-id="0807e-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="0807e-148">Klikněte na Import z aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="0807e-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="0807e-149">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="0807e-149">Click Attachments.</span></span>
    * <span data-ttu-id="0807e-150">Připojte existující dokument Excel jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="0807e-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="0807e-151">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0807e-151">Click New.</span></span>
7. <span data-ttu-id="0807e-152">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="0807e-152">Click File.</span></span>
    * <span data-ttu-id="0807e-153">Odkažte na existující soubor aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="0807e-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="0807e-154">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-154">Close the page.</span></span>
9. <span data-ttu-id="0807e-155">V poli Šablona zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0807e-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="0807e-156">Určete, že chcete použít připojený soubor aplikace Excel jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="0807e-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="0807e-157">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0807e-157">Click OK.</span></span>
    * <span data-ttu-id="0807e-158">Všimněte si, že komponenty formátu ER byly vytvořeny v navrženém formátu v závislosti na struktuře odkazovaného dokumentu aplikace MS Excel (rozsahy s názvy).</span><span class="sxs-lookup"><span data-stu-id="0807e-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="0807e-159">Vytvoření nového zdroje dat pro výpočet součtů podle kódů měn</span><span class="sxs-lookup"><span data-stu-id="0807e-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="0807e-160">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="0807e-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0807e-161">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0807e-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="0807e-162">Ve stromovém zobrazení vyberte možnost „Funkce\Seskupit podle “.</span><span class="sxs-lookup"><span data-stu-id="0807e-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="0807e-163">Do pole Název zadejte PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="0807e-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="0807e-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="0807e-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="0807e-165">Klikněte na „Upravit skupinu podle“.</span><span class="sxs-lookup"><span data-stu-id="0807e-165">Click Edit group by.</span></span>
6. <span data-ttu-id="0807e-166">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="0807e-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="0807e-167">Ve stromovém zobrazení vyberte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="0807e-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="0807e-168">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="0807e-168">Click Add field to.</span></span>
9. <span data-ttu-id="0807e-169">Klikněte na „Skupina Co“.</span><span class="sxs-lookup"><span data-stu-id="0807e-169">Click What to group.</span></span>
10. <span data-ttu-id="0807e-170">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="0807e-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="0807e-171">Ve stromovém zobrazení vyberte „model\Platby\Měna“.</span><span class="sxs-lookup"><span data-stu-id="0807e-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="0807e-172">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="0807e-172">Click Add field to.</span></span>
13. <span data-ttu-id="0807e-173">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="0807e-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="0807e-174">Ve stromovém zobrazení vyberte „model\Platby\Požadovaná částka(InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="0807e-175">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="0807e-175">Click Add field to.</span></span>
16. <span data-ttu-id="0807e-176">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="0807e-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="0807e-177">Vyberte volbu v poli Metoda.</span><span class="sxs-lookup"><span data-stu-id="0807e-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="0807e-178">Vyberte funkci agregace SUM.</span><span class="sxs-lookup"><span data-stu-id="0807e-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="0807e-179">Do pole Název zadejte TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="0807e-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="0807e-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="0807e-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="0807e-181">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0807e-181">Click Save.</span></span>
20. <span data-ttu-id="0807e-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-182">Close the page.</span></span>
21. <span data-ttu-id="0807e-183">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0807e-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="0807e-184">Mapování součástí formátu na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="0807e-184">Map format components to data sources</span></span>
1. <span data-ttu-id="0807e-185">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="0807e-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="0807e-186">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="0807e-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="0807e-187">Ve stromovém zobrazení rozbalte „model\Platby\Strana příkazce(InitiatingParty)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="0807e-188">Ve stromovém zobrazení vyberte „model\Platby\Strana příkazce(InitiatingParty)\Název“.</span><span class="sxs-lookup"><span data-stu-id="0807e-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="0807e-189">Ve stromové struktuře rozbalte 'Excel\ReportHeader'.</span><span class="sxs-lookup"><span data-stu-id="0807e-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="0807e-190">Ve stromové struktuře zvolte 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="0807e-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="0807e-191">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-191">Click Bind.</span></span>
8. <span data-ttu-id="0807e-192">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="0807e-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="0807e-193">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Identifikace“.</span><span class="sxs-lookup"><span data-stu-id="0807e-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="0807e-194">Ve stromovém zobrazení vyberte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace\ID zdroje(SourceID)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="0807e-195">Ve stromové struktuře rozbalte 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="0807e-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="0807e-196">Ve stromové struktuře zvolte 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="0807e-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="0807e-197">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-197">Click Bind.</span></span>
14. <span data-ttu-id="0807e-198">Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Název“.</span><span class="sxs-lookup"><span data-stu-id="0807e-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="0807e-199">Ve stromové struktuře zvolte 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="0807e-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="0807e-200">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-200">Click Bind.</span></span>
17. <span data-ttu-id="0807e-201">Ve stromovém zobrazení rozbalte „model\Platby\Agent věřitele(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="0807e-202">Ve stromovém zobrazení vyberte „model\Platby\Agent věřitele(CreditorAgent)\Název“.</span><span class="sxs-lookup"><span data-stu-id="0807e-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="0807e-203">Ve stromové struktuře zvolte 'Excel\PaymLines\Banka'.</span><span class="sxs-lookup"><span data-stu-id="0807e-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="0807e-204">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-204">Click Bind.</span></span>
21. <span data-ttu-id="0807e-205">Ve stromovém zobrazení vyberte „model\Platby\Agent věřitele(CreditorAgent)\Směrový kód(RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="0807e-206">Ve stromové struktuře zvolte 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="0807e-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="0807e-207">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-207">Click Bind.</span></span>
24. <span data-ttu-id="0807e-208">Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="0807e-209">Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace“.</span><span class="sxs-lookup"><span data-stu-id="0807e-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="0807e-210">Ve stromovém zobrazení vyberte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace\Číslo“.</span><span class="sxs-lookup"><span data-stu-id="0807e-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="0807e-211">Ve stromové struktuře zvolte 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="0807e-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="0807e-212">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-212">Click Bind.</span></span>
29. <span data-ttu-id="0807e-213">Ve stromovém zobrazení vyberte „model\Platby\Požadovaná částka(InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="0807e-214">Ve stromové struktuře zvolte 'Excel\PaymLines\MD'.</span><span class="sxs-lookup"><span data-stu-id="0807e-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="0807e-215">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-215">Click Bind.</span></span>
32. <span data-ttu-id="0807e-216">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="0807e-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="0807e-217">Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="0807e-218">Ve stromovém zobrazení rozbalte „model\Platby\Agent věřitele(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="0807e-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="0807e-219">Ve stromovém zobrazení vyberte „model\Platby\Měna“.</span><span class="sxs-lookup"><span data-stu-id="0807e-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="0807e-220">Ve stromové struktuře zvolte 'Excel\PaymLines\Měna'.</span><span class="sxs-lookup"><span data-stu-id="0807e-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="0807e-221">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-221">Click Bind.</span></span>
38. <span data-ttu-id="0807e-222">Ve stromu rozbalte PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="0807e-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="0807e-223">Ve stromu rozbalte PaymentByCurrency\seskupeno.</span><span class="sxs-lookup"><span data-stu-id="0807e-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="0807e-224">Ve stromovém zobrazení vyberte „PaymentByCurrency\seskupeno\Měna“.</span><span class="sxs-lookup"><span data-stu-id="0807e-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="0807e-225">Ve stromové struktuře rozbalte 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="0807e-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="0807e-226">Ve stromové struktuře zvolte 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="0807e-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="0807e-227">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-227">Click Bind.</span></span>
44. <span data-ttu-id="0807e-228">Ve stromu rozbalte PaymentByCurrency\agregováno.</span><span class="sxs-lookup"><span data-stu-id="0807e-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="0807e-229">Ve stromovém zobrazení vyberte „PaymentByCurrency\agregováno\TotalInstructuredAmount“.</span><span class="sxs-lookup"><span data-stu-id="0807e-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="0807e-230">Ve stromové struktuře zvolte 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="0807e-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="0807e-231">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-231">Click Bind.</span></span>
48. <span data-ttu-id="0807e-232">Ve stromu vyberte PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="0807e-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="0807e-233">Ve stromové struktuře zvolte 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="0807e-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="0807e-234">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-234">Click Bind.</span></span>
51. <span data-ttu-id="0807e-235">Ve stromovém zobrazení vyberte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="0807e-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="0807e-236">Ve stromové struktuře zvolte 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="0807e-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="0807e-237">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="0807e-237">Click Bind.</span></span>
54. <span data-ttu-id="0807e-238">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0807e-238">Click Save.</span></span>
55. <span data-ttu-id="0807e-239">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="0807e-240">Použití vytvořené konfigurace pro zpracování plateb</span><span class="sxs-lookup"><span data-stu-id="0807e-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="0807e-241">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="0807e-241">Click Change status.</span></span>
2. <span data-ttu-id="0807e-242">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="0807e-242">Click Complete.</span></span>
3. <span data-ttu-id="0807e-243">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0807e-243">Click OK.</span></span>
4. <span data-ttu-id="0807e-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-244">Close the page.</span></span>
5. <span data-ttu-id="0807e-245">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-245">Close the page.</span></span>
6. <span data-ttu-id="0807e-246">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="0807e-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="0807e-247">Použijte rychlý filtr k filtrování v poli Metoda platby s hodnotou 'Elektronická'.</span><span class="sxs-lookup"><span data-stu-id="0807e-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="0807e-248">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="0807e-248">Electronic</span></span>  
8. <span data-ttu-id="0807e-249">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="0807e-249">Click Edit.</span></span>
9. <span data-ttu-id="0807e-250">Rozbalte oddíl Formáty souborů.</span><span class="sxs-lookup"><span data-stu-id="0807e-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="0807e-251">Vyberte možnost Ano v poli Obecné elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0807e-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="0807e-252">V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0807e-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="0807e-253">Vyberte konfiguraci Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="0807e-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="0807e-254">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0807e-254">Click Save.</span></span>
13. <span data-ttu-id="0807e-255">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0807e-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="0807e-256">Použití vytvořené konfigurace pro testování zpracování deníků plateb</span><span class="sxs-lookup"><span data-stu-id="0807e-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="0807e-257">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="0807e-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="0807e-258">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0807e-258">Click New.</span></span>
    * <span data-ttu-id="0807e-259">Vytvořte nový deník plateb.</span><span class="sxs-lookup"><span data-stu-id="0807e-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="0807e-260">Zadejte text „VendPay“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="0807e-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="0807e-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="0807e-261">VendPay</span></span>  
4. <span data-ttu-id="0807e-262">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="0807e-262">Click Lines.</span></span>
5. <span data-ttu-id="0807e-263">Zadejte hodnoty „GB_SI_000001“ do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="0807e-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="0807e-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="0807e-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="0807e-265">Nastavte Má dáti na 1000.</span><span class="sxs-lookup"><span data-stu-id="0807e-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="0807e-266">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0807e-266">Click New.</span></span>
8. <span data-ttu-id="0807e-267">Zadejte hodnoty „GB_SI_000005“ do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="0807e-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="0807e-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="0807e-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="0807e-269">Nastavte Má dáti na 2000.</span><span class="sxs-lookup"><span data-stu-id="0807e-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="0807e-270">Zadejte hodnotu EUR do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="0807e-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="0807e-271">EUR</span><span class="sxs-lookup"><span data-stu-id="0807e-271">EUR</span></span>  
11. <span data-ttu-id="0807e-272">Zadejte hodnotu „GBSI OPER“ do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="0807e-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="0807e-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="0807e-273">GBSI OPER</span></span>  
12. <span data-ttu-id="0807e-274">V poli Způsob platby zadejte „Elektronicky“.</span><span class="sxs-lookup"><span data-stu-id="0807e-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="0807e-275">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="0807e-275">Electronic</span></span>  
13. <span data-ttu-id="0807e-276">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0807e-276">Click Save.</span></span>
14. <span data-ttu-id="0807e-277">Klepněte na Generovat platby.</span><span class="sxs-lookup"><span data-stu-id="0807e-277">Click Generate payments.</span></span>
15. <span data-ttu-id="0807e-278">V poli Způsob platby zadejte „Elektronicky“.</span><span class="sxs-lookup"><span data-stu-id="0807e-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="0807e-279">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="0807e-279">Electronic</span></span>  
16. <span data-ttu-id="0807e-280">Do pole Název souboru zadejte 'Platby'.</span><span class="sxs-lookup"><span data-stu-id="0807e-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0807e-281">Zadejte například Platby.</span><span class="sxs-lookup"><span data-stu-id="0807e-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="0807e-282">V poli Bankovní účet zadejte „GBSI OPER“.</span><span class="sxs-lookup"><span data-stu-id="0807e-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="0807e-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="0807e-283">GBSI OPER</span></span>  
18. <span data-ttu-id="0807e-284">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0807e-284">Click OK.</span></span>
19. <span data-ttu-id="0807e-285">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0807e-285">Click OK.</span></span>
    * <span data-ttu-id="0807e-286">Zkontrolujte vytvořený list, včetně podrobností na řádcích platby, stejně tak jako součty pro každý kód měny používaný v této platební zprávě.</span><span class="sxs-lookup"><span data-stu-id="0807e-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


