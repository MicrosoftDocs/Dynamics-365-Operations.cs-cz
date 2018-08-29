--- 
title: "Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu OpenXML"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="a03f9-103">Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu OpenXML</span><span class="sxs-lookup"><span data-stu-id="a03f9-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a03f9-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje šablonu pro generování elektronických dokladů ve formátu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="a03f9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="a03f9-105">Tato konfigurace se použije ke zpracování plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="a03f9-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="a03f9-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést ve společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="a03f9-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="a03f9-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="a03f9-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="a03f9-108">Je nutné stáhnout a uložit soubor aplikace Microsoft Excel [Šablona sestavy platby](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="a03f9-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="a03f9-109">Odeslání konfigurace modelu platebních dat</span><span class="sxs-lookup"><span data-stu-id="a03f9-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="a03f9-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="a03f9-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a03f9-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="a03f9-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a03f9-112">Vyberte poskytovatele konfigurace pro vzorovou společnost 'Litware, Inc.' Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="a03f9-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="a03f9-113">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="a03f9-113">Click Set active.</span></span>
4. <span data-ttu-id="a03f9-114">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="a03f9-114">Click Repositories.</span></span>
    * <span data-ttu-id="a03f9-115">Vyberte úložiště pro typ Provozní prostředky (pokud je k dispozici).</span><span class="sxs-lookup"><span data-stu-id="a03f9-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="a03f9-116">Pokud k dispozici je, přeskočte následující kroky týkající se vytváření nového úložiště.</span><span class="sxs-lookup"><span data-stu-id="a03f9-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="a03f9-117">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="a03f9-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="a03f9-118">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="a03f9-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="a03f9-119">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="a03f9-119">Click Create repository.</span></span>
8. <span data-ttu-id="a03f9-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a03f9-120">Click OK.</span></span>
9. <span data-ttu-id="a03f9-121">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="a03f9-121">Click Open.</span></span>
10. <span data-ttu-id="a03f9-122">Ve stromovém zobrazení vyberte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="a03f9-123">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="a03f9-123">Click Import.</span></span>
    * <span data-ttu-id="a03f9-124">Importujte tento model dat.</span><span class="sxs-lookup"><span data-stu-id="a03f9-124">Import this data model.</span></span> <span data-ttu-id="a03f9-125">Použije se jako zdroj dat v nové konfiguraci formátu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="a03f9-126">Tento krok vynechejte, je-li tato konfigurace již importována.</span><span class="sxs-lookup"><span data-stu-id="a03f9-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="a03f9-127">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="a03f9-127">Click Yes.</span></span>
13. <span data-ttu-id="a03f9-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-128">Close the page.</span></span>
14. <span data-ttu-id="a03f9-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="a03f9-130">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="a03f9-130">Create a new format configuration</span></span>
1. <span data-ttu-id="a03f9-131">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="a03f9-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="a03f9-132">Ve stromovém zobrazení vyberte „Model platby“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="a03f9-133">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="a03f9-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a03f9-134">V poli Nový zadejte "Formát založený na datovém modelu PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="a03f9-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="a03f9-135">Vytvořte formát, který vychází z modelu dat PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="a03f9-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="a03f9-136">V poli Název zadejte „Ukázková sestava listu“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="a03f9-137">Ukázková sestava listu</span><span class="sxs-lookup"><span data-stu-id="a03f9-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="a03f9-138">V poli Popis zadejte Ukázková sestavu listu pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="a03f9-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="a03f9-139">Ukázková sestavu listu pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="a03f9-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="a03f9-140">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="a03f9-141">Vyberte definici „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="a03f9-142">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="a03f9-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="a03f9-143">Návrh nového dokumentu ve formátu listu OPENXML</span><span class="sxs-lookup"><span data-stu-id="a03f9-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="a03f9-144">Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="a03f9-145">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="a03f9-145">Click Designer.</span></span>
3. <span data-ttu-id="a03f9-146">V podokně akcí klikněte na možnost Importovat.</span><span class="sxs-lookup"><span data-stu-id="a03f9-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="a03f9-147">Klikněte na Import z aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a03f9-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="a03f9-148">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="a03f9-148">Click Attachments.</span></span>
    * <span data-ttu-id="a03f9-149">Připojte existující dokument Excel jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="a03f9-150">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a03f9-150">Click New.</span></span>
7. <span data-ttu-id="a03f9-151">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="a03f9-151">Click File.</span></span>
    * <span data-ttu-id="a03f9-152">Odkažte na existující soubor aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a03f9-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="a03f9-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-153">Close the page.</span></span>
9. <span data-ttu-id="a03f9-154">V poli Šablona zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="a03f9-155">Určete, že chcete použít připojený soubor aplikace Excel jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="a03f9-156">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a03f9-156">Click OK.</span></span>
    * <span data-ttu-id="a03f9-157">Všimněte si, že komponenty formátu ER byly vytvořeny v navrženém formátu v závislosti na struktuře odkazovaného dokumentu aplikace MS Excel (rozsahy s názvy).</span><span class="sxs-lookup"><span data-stu-id="a03f9-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="a03f9-158">Vytvoření nového zdroje dat pro výpočet součtů podle kódů měn</span><span class="sxs-lookup"><span data-stu-id="a03f9-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="a03f9-159">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="a03f9-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a03f9-160">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="a03f9-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="a03f9-161">Ve stromovém zobrazení vyberte možnost „Funkce\Seskupit podle “.</span><span class="sxs-lookup"><span data-stu-id="a03f9-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="a03f9-162">Do pole Název zadejte PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="a03f9-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="a03f9-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="a03f9-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="a03f9-164">Klikněte na „Upravit skupinu podle“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-164">Click Edit group by.</span></span>
6. <span data-ttu-id="a03f9-165">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="a03f9-166">Ve stromovém zobrazení vyberte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="a03f9-167">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-167">Click Add field to.</span></span>
9. <span data-ttu-id="a03f9-168">Klikněte na „Skupina Co“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-168">Click What to group.</span></span>
10. <span data-ttu-id="a03f9-169">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="a03f9-170">Ve stromovém zobrazení vyberte „model\Platby\Měna“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="a03f9-171">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-171">Click Add field to.</span></span>
13. <span data-ttu-id="a03f9-172">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="a03f9-173">Ve stromovém zobrazení vyberte „model\Platby\Požadovaná částka(InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="a03f9-174">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-174">Click Add field to.</span></span>
16. <span data-ttu-id="a03f9-175">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="a03f9-176">Vyberte volbu v poli Metoda.</span><span class="sxs-lookup"><span data-stu-id="a03f9-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="a03f9-177">Vyberte funkci agregace SUM.</span><span class="sxs-lookup"><span data-stu-id="a03f9-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="a03f9-178">Do pole Název zadejte TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="a03f9-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="a03f9-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="a03f9-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="a03f9-180">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a03f9-180">Click Save.</span></span>
20. <span data-ttu-id="a03f9-181">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-181">Close the page.</span></span>
21. <span data-ttu-id="a03f9-182">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a03f9-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="a03f9-183">Mapování součástí formátu na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="a03f9-183">Map format components to data sources</span></span>
1. <span data-ttu-id="a03f9-184">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="a03f9-185">Ve stromovém zobrazení rozbalte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="a03f9-186">Ve stromovém zobrazení rozbalte „model\Platby\Strana příkazce(InitiatingParty)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="a03f9-187">Ve stromovém zobrazení vyberte „model\Platby\Strana příkazce(InitiatingParty)\Název“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="a03f9-188">Ve stromové struktuře rozbalte 'Excel\ReportHeader'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="a03f9-189">Ve stromové struktuře zvolte 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="a03f9-190">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-190">Click Bind.</span></span>
8. <span data-ttu-id="a03f9-191">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="a03f9-192">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Identifikace“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="a03f9-193">Ve stromovém zobrazení vyberte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace\ID zdroje(SourceID)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="a03f9-194">Ve stromové struktuře rozbalte 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="a03f9-195">Ve stromové struktuře zvolte 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="a03f9-196">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-196">Click Bind.</span></span>
14. <span data-ttu-id="a03f9-197">Ve stromovém zobrazení vyberte „model\Platby\Věřitel\Název“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="a03f9-198">Ve stromové struktuře zvolte 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="a03f9-199">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-199">Click Bind.</span></span>
17. <span data-ttu-id="a03f9-200">Ve stromovém zobrazení rozbalte „model\Platby\Agent věřitele(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="a03f9-201">Ve stromovém zobrazení vyberte „model\Platby\Agent věřitele(CreditorAgent)\Název“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="a03f9-202">Ve stromové struktuře zvolte 'Excel\PaymLines\Banka'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="a03f9-203">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-203">Click Bind.</span></span>
21. <span data-ttu-id="a03f9-204">Ve stromovém zobrazení vyberte „model\Platby\Agent věřitele(CreditorAgent)\Směrový kód(RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="a03f9-205">Ve stromové struktuře zvolte 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="a03f9-206">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-206">Click Bind.</span></span>
24. <span data-ttu-id="a03f9-207">Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="a03f9-208">Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="a03f9-209">Ve stromovém zobrazení vyberte „model\Platby\Účet věřitele (Účet věřitele)\Identifikace\Číslo“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="a03f9-210">Ve stromové struktuře zvolte 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="a03f9-211">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-211">Click Bind.</span></span>
29. <span data-ttu-id="a03f9-212">Ve stromovém zobrazení vyberte „model\Platby\Požadovaná částka(InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="a03f9-213">Ve stromové struktuře zvolte 'Excel\PaymLines\MD'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="a03f9-214">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-214">Click Bind.</span></span>
32. <span data-ttu-id="a03f9-215">Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="a03f9-216">Ve stromovém zobrazení rozbalte „model\Platby\Účet věřitele (Účet věřitele)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="a03f9-217">Ve stromovém zobrazení rozbalte „model\Platby\Agent věřitele(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="a03f9-218">Ve stromovém zobrazení vyberte „model\Platby\Měna“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="a03f9-219">Ve stromové struktuře zvolte 'Excel\PaymLines\Měna'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="a03f9-220">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-220">Click Bind.</span></span>
38. <span data-ttu-id="a03f9-221">Ve stromu rozbalte PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="a03f9-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="a03f9-222">Ve stromu rozbalte PaymentByCurrency\seskupeno.</span><span class="sxs-lookup"><span data-stu-id="a03f9-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="a03f9-223">Ve stromovém zobrazení vyberte „PaymentByCurrency\seskupeno\Měna“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="a03f9-224">Ve stromové struktuře rozbalte 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="a03f9-225">Ve stromové struktuře zvolte 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="a03f9-226">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-226">Click Bind.</span></span>
44. <span data-ttu-id="a03f9-227">Ve stromu rozbalte PaymentByCurrency\agregováno.</span><span class="sxs-lookup"><span data-stu-id="a03f9-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="a03f9-228">Ve stromovém zobrazení vyberte „PaymentByCurrency\agregováno\TotalInstructuredAmount“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="a03f9-229">Ve stromové struktuře zvolte 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="a03f9-230">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-230">Click Bind.</span></span>
48. <span data-ttu-id="a03f9-231">Ve stromu vyberte PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="a03f9-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="a03f9-232">Ve stromové struktuře zvolte 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="a03f9-233">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-233">Click Bind.</span></span>
51. <span data-ttu-id="a03f9-234">Ve stromovém zobrazení vyberte „model\Platby“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="a03f9-235">Ve stromové struktuře zvolte 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="a03f9-236">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="a03f9-236">Click Bind.</span></span>
54. <span data-ttu-id="a03f9-237">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a03f9-237">Click Save.</span></span>
55. <span data-ttu-id="a03f9-238">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="a03f9-239">Použití vytvořené konfigurace pro zpracování plateb</span><span class="sxs-lookup"><span data-stu-id="a03f9-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="a03f9-240">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="a03f9-240">Click Change status.</span></span>
2. <span data-ttu-id="a03f9-241">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="a03f9-241">Click Complete.</span></span>
3. <span data-ttu-id="a03f9-242">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a03f9-242">Click OK.</span></span>
4. <span data-ttu-id="a03f9-243">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-243">Close the page.</span></span>
5. <span data-ttu-id="a03f9-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-244">Close the page.</span></span>
6. <span data-ttu-id="a03f9-245">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="a03f9-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="a03f9-246">Použijte rychlý filtr k filtrování v poli Metoda platby s hodnotou 'Elektronická'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="a03f9-247">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="a03f9-247">Electronic</span></span>  
8. <span data-ttu-id="a03f9-248">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="a03f9-248">Click Edit.</span></span>
9. <span data-ttu-id="a03f9-249">Rozbalte oddíl Formáty souborů.</span><span class="sxs-lookup"><span data-stu-id="a03f9-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="a03f9-250">Vyberte možnost Ano v poli Obecné elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="a03f9-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="a03f9-251">V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="a03f9-252">Vyberte konfiguraci Ukázková sestava listu.</span><span class="sxs-lookup"><span data-stu-id="a03f9-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="a03f9-253">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a03f9-253">Click Save.</span></span>
13. <span data-ttu-id="a03f9-254">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a03f9-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="a03f9-255">Použití vytvořené konfigurace pro testování zpracování deníků plateb</span><span class="sxs-lookup"><span data-stu-id="a03f9-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="a03f9-256">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="a03f9-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="a03f9-257">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a03f9-257">Click New.</span></span>
    * <span data-ttu-id="a03f9-258">Vytvořte nový deník plateb.</span><span class="sxs-lookup"><span data-stu-id="a03f9-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="a03f9-259">Zadejte text „VendPay“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="a03f9-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="a03f9-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="a03f9-260">VendPay</span></span>  
4. <span data-ttu-id="a03f9-261">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="a03f9-261">Click Lines.</span></span>
5. <span data-ttu-id="a03f9-262">Zadejte hodnoty „GB_SI_000001“ do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="a03f9-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="a03f9-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="a03f9-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="a03f9-264">Nastavte Má dáti na 1000.</span><span class="sxs-lookup"><span data-stu-id="a03f9-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="a03f9-265">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a03f9-265">Click New.</span></span>
8. <span data-ttu-id="a03f9-266">Zadejte hodnoty „GB_SI_000005“ do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="a03f9-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="a03f9-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="a03f9-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="a03f9-268">Nastavte Má dáti na 2000.</span><span class="sxs-lookup"><span data-stu-id="a03f9-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="a03f9-269">Zadejte hodnotu EUR do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="a03f9-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="a03f9-270">EUR</span><span class="sxs-lookup"><span data-stu-id="a03f9-270">EUR</span></span>  
11. <span data-ttu-id="a03f9-271">Zadejte hodnotu „GBSI OPER“ do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="a03f9-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="a03f9-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="a03f9-272">GBSI OPER</span></span>  
12. <span data-ttu-id="a03f9-273">V poli Způsob platby zadejte „Elektronicky“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="a03f9-274">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="a03f9-274">Electronic</span></span>  
13. <span data-ttu-id="a03f9-275">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a03f9-275">Click Save.</span></span>
14. <span data-ttu-id="a03f9-276">Klepněte na Generovat platby.</span><span class="sxs-lookup"><span data-stu-id="a03f9-276">Click Generate payments.</span></span>
15. <span data-ttu-id="a03f9-277">V poli Způsob platby zadejte „Elektronicky“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="a03f9-278">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="a03f9-278">Electronic</span></span>  
16. <span data-ttu-id="a03f9-279">Do pole Název souboru zadejte 'Platby'.</span><span class="sxs-lookup"><span data-stu-id="a03f9-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="a03f9-280">Zadejte například Platby.</span><span class="sxs-lookup"><span data-stu-id="a03f9-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="a03f9-281">V poli Bankovní účet zadejte „GBSI OPER“.</span><span class="sxs-lookup"><span data-stu-id="a03f9-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="a03f9-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="a03f9-282">GBSI OPER</span></span>  
18. <span data-ttu-id="a03f9-283">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a03f9-283">Click OK.</span></span>
19. <span data-ttu-id="a03f9-284">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a03f9-284">Click OK.</span></span>
    * <span data-ttu-id="a03f9-285">Zkontrolujte vytvořený list, včetně podrobností na řádcích platby, stejně tak jako součty pro každý kód měny používaný v této platební zprávě.</span><span class="sxs-lookup"><span data-stu-id="a03f9-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


