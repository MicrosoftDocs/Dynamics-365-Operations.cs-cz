--- 
title: "Generování sestav ve formátech Office s integrovanými obrázky"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhnout konfigurace pro elektronické výkaznictví (ER) a vygenerovat tak elektronické dokumenty ve formátu MS Office (Excel nebo Word) s vloženými obrázky."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 5ef7ec2f8b5b7fdf456ebb71b863e620ae21e6b5
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c3499-103">Generování sestav ve formátech Office s integrovanými obrázky</span><span class="sxs-lookup"><span data-stu-id="c3499-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3499-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhnout konfigurace pro elektronické výkaznictví (ER) a vygenerovat tak elektronické dokumenty ve formátu MS Office (Excel nebo Word) s vloženými obrázky.</span><span class="sxs-lookup"><span data-stu-id="c3499-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="c3499-105">V tomto příkladu použijete vytvořené konfigurace ER pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c3499-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="c3499-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 2: konfigurace přehledu).</span><span class="sxs-lookup"><span data-stu-id="c3499-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="c3499-107">Tyto kroky lze provést v rámci společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="c3499-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="c3499-108">Spuštění formátu s počátečním mapováním modelu</span><span class="sxs-lookup"><span data-stu-id="c3499-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="c3499-109">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="c3499-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="c3499-110">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c3499-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="c3499-111">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="c3499-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="c3499-112">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="c3499-112">Click Check.</span></span>
5. <span data-ttu-id="c3499-113">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c3499-113">Click Print test.</span></span>
    * <span data-ttu-id="c3499-114">Spusťte formát pro účely testování.</span><span class="sxs-lookup"><span data-stu-id="c3499-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="c3499-115">V poli Obchodovatelný formát šeku vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="c3499-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="c3499-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c3499-116">Click OK.</span></span>
    * <span data-ttu-id="c3499-117">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c3499-117">Review the created output.</span></span> <span data-ttu-id="c3499-118">Všimněte si, že logo společnosti se zobrazí v sestavě společně s podpisem oprávněné osoby.</span><span class="sxs-lookup"><span data-stu-id="c3499-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="c3499-119">Obrázek podpisu je převzat z pole typu dat Kontejner ze záznamu rozvržení šeku, který je přidružen k vybranému bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="c3499-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="c3499-120">Rozbalte sekci Kopie.</span><span class="sxs-lookup"><span data-stu-id="c3499-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="c3499-121">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c3499-121">Click Edit.</span></span>
10. <span data-ttu-id="c3499-122">V poli Vodoznak zadejte Tisknout vodoznak jako anulovaný.</span><span class="sxs-lookup"><span data-stu-id="c3499-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="c3499-123">Změňte nastavení rozložení vodoznaku tak, aby byl zobrazen text vodoznaku při generování dokumentu v elementu tvaru Excel.</span><span class="sxs-lookup"><span data-stu-id="c3499-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="c3499-124">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c3499-124">Click Print test.</span></span>
12. <span data-ttu-id="c3499-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c3499-125">Click OK.</span></span>
    * <span data-ttu-id="c3499-126">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c3499-126">Review the created output.</span></span> <span data-ttu-id="c3499-127">Všimněte si, že vodoznak je uveden v sestavě v souladu s možností výběru.</span><span class="sxs-lookup"><span data-stu-id="c3499-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="c3499-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-128">Close the page.</span></span>
14. <span data-ttu-id="c3499-129">V podokně akcí klikněte na možnost Spravovat platby.</span><span class="sxs-lookup"><span data-stu-id="c3499-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="c3499-130">Klikněte na možnost Kontroly.</span><span class="sxs-lookup"><span data-stu-id="c3499-130">Click Checks.</span></span>
16. <span data-ttu-id="c3499-131">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="c3499-131">Click Show filters.</span></span>
17. <span data-ttu-id="c3499-132">Použijte následující filtry: zadejte hodnotu filtru "381","385","389" v poli Číslo kontroly za pomocí operátoru filtru „je jeden z“.</span><span class="sxs-lookup"><span data-stu-id="c3499-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="c3499-133">V seznamu označte všechny řádky.</span><span class="sxs-lookup"><span data-stu-id="c3499-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="c3499-134">Klikněte na Tisknout kopii šeku.</span><span class="sxs-lookup"><span data-stu-id="c3499-134">Click Print check copy.</span></span>
    * <span data-ttu-id="c3499-135">Spusťte formát a znovu vytiskněte vybrané šeky.</span><span class="sxs-lookup"><span data-stu-id="c3499-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="c3499-136">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c3499-136">Review the created output.</span></span> <span data-ttu-id="c3499-137">Všimněte si, že vybrané šeky byly znovu vytištěny.</span><span class="sxs-lookup"><span data-stu-id="c3499-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="c3499-138">Logo společnosti a popisky nejsou vytištěny, protože jsou uvedeny na předtištěném formuláři.</span><span class="sxs-lookup"><span data-stu-id="c3499-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="c3499-139">Úprava mapování importovaného modelu dat</span><span class="sxs-lookup"><span data-stu-id="c3499-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="c3499-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-140">Close the page.</span></span>
2. <span data-ttu-id="c3499-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-141">Close the page.</span></span>
3. <span data-ttu-id="c3499-142">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c3499-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="c3499-143">Ve stromové struktuře zvolte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="c3499-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="c3499-144">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c3499-144">Click Designer.</span></span>
6. <span data-ttu-id="c3499-145">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="c3499-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="c3499-146">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c3499-146">Click Designer.</span></span>
    * <span data-ttu-id="c3499-147">Upravíme vazbu položky podpisu datového modelu a získáme tak obrázek podpisu ze souboru připojeného k záznamu rozvržení šeku, který je přidružen k vybranému bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="c3499-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="c3499-148">Vypněte Zobrazit podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="c3499-148">Turn Show details off.</span></span>
9. <span data-ttu-id="c3499-149">Ve stromové struktuře rozbalte Rozvržení.</span><span class="sxs-lookup"><span data-stu-id="c3499-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="c3499-150">Ve stromovém zobrazení rozbalte layout\signature.</span><span class="sxs-lookup"><span data-stu-id="c3499-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="c3499-151">Ve stromovém zobrazení vyberte layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp.</span><span class="sxs-lookup"><span data-stu-id="c3499-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="c3499-152">Ve stromovém zobrazení rozbalte Chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="c3499-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="c3499-153">Ve stromovém zobrazení rozbalte chequesaccount\<Relations.</span><span class="sxs-lookup"><span data-stu-id="c3499-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="c3499-154">Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout.</span><span class="sxs-lookup"><span data-stu-id="c3499-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="c3499-155">Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout\<Relations.</span><span class="sxs-lookup"><span data-stu-id="c3499-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="c3499-156">Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout\<Relations\<Document.</span><span class="sxs-lookup"><span data-stu-id="c3499-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="c3499-157">Ve stromovém zobrazení vyberte chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer().</span><span class="sxs-lookup"><span data-stu-id="c3499-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="c3499-158">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c3499-158">Click Bind.</span></span>
19. <span data-ttu-id="c3499-159">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c3499-159">Click Save.</span></span>
20. <span data-ttu-id="c3499-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-160">Close the page.</span></span>
21. <span data-ttu-id="c3499-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-161">Close the page.</span></span>
22. <span data-ttu-id="c3499-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-162">Close the page.</span></span>
23. <span data-ttu-id="c3499-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="c3499-164">Spuštění formátu pomocí upraveného mapování modelu</span><span class="sxs-lookup"><span data-stu-id="c3499-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="c3499-165">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="c3499-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="c3499-166">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="c3499-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c3499-167">Můžete například filtrovat v poli Bankovní účet pomocí hodnoty „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="c3499-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="c3499-168">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="c3499-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="c3499-169">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="c3499-169">Click Check.</span></span>
5. <span data-ttu-id="c3499-170">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c3499-170">Click Print test.</span></span>
6. <span data-ttu-id="c3499-171">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c3499-171">Click OK.</span></span>
    * <span data-ttu-id="c3499-172">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c3499-172">Review the created output.</span></span> <span data-ttu-id="c3499-173">Všimněte si, že obrázek z přílohy správy dokumentů je zobrazen jako podpis oprávněné osoby.</span><span class="sxs-lookup"><span data-stu-id="c3499-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="c3499-174">Použití dokumentu MS Word jako šablony v importovaném formátu</span><span class="sxs-lookup"><span data-stu-id="c3499-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="c3499-175">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-175">Close the page.</span></span>
2. <span data-ttu-id="c3499-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-176">Close the page.</span></span>
3. <span data-ttu-id="c3499-177">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c3499-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="c3499-178">Ve stromové struktuře rozbalte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="c3499-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="c3499-179">Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="c3499-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="c3499-180">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c3499-180">Click Designer.</span></span>
7. <span data-ttu-id="c3499-181">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="c3499-181">Click Attachments.</span></span>
8. <span data-ttu-id="c3499-182">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="c3499-182">Click Delete.</span></span>
9. <span data-ttu-id="c3499-183">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="c3499-183">Click Yes.</span></span>
10. <span data-ttu-id="c3499-184">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c3499-184">Click New.</span></span>
11. <span data-ttu-id="c3499-185">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="c3499-185">Click File.</span></span>
    * <span data-ttu-id="c3499-186">Klepněte na tlačítko Procházet a vyberte předem stažený soubor Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="c3499-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="c3499-187">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-187">Close the page.</span></span>
13. <span data-ttu-id="c3499-188">V poli Šablona zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c3499-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="c3499-189">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c3499-189">Click Save.</span></span>
15. <span data-ttu-id="c3499-190">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-190">Close the page.</span></span>
16. <span data-ttu-id="c3499-191">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c3499-191">Click Edit.</span></span>
17. <span data-ttu-id="c3499-192">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="c3499-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="c3499-193">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3499-193">Close the page.</span></span>
19. <span data-ttu-id="c3499-194">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="c3499-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="c3499-195">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c3499-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="c3499-196">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="c3499-196">Click Check.</span></span>
22. <span data-ttu-id="c3499-197">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c3499-197">Click Print test.</span></span>
23. <span data-ttu-id="c3499-198">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c3499-198">Click OK.</span></span>
    * <span data-ttu-id="c3499-199">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c3499-199">Review the created output.</span></span> <span data-ttu-id="c3499-200">Všimněte si, že výstup byl vygenerován jako dokument aplikace Word s vloženými obrázky loga společnosti, podpisem oprávněné osoby a vybraným textem vodoznaku.</span><span class="sxs-lookup"><span data-stu-id="c3499-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


