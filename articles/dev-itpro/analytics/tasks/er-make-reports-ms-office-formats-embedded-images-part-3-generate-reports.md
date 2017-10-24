--- 
title: "Generování sestav ve formátu Microsoft Office s integrovanými obrázky pro elektronické výkaznictví (ER)"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4fa27996e59164126f7900edf4a509ca9273e7c1
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="c78f6-103">Generování sestav ve formátu Microsoft Office s integrovanými obrázky pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="c78f6-103">Generate reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c78f6-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhnout konfigurace pro elektronické výkaznictví (ER) a vygenerovat tak elektronické dokumenty ve formátu MS Office (Excel nebo Word) s vloženými obrázky.</span><span class="sxs-lookup"><span data-stu-id="c78f6-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="c78f6-105">V tomto příkladu použijete vytvořené konfigurace ER pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c78f6-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="c78f6-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 2: konfigurace přehledu).</span><span class="sxs-lookup"><span data-stu-id="c78f6-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="c78f6-107">Tyto kroky lze provést v rámci společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="c78f6-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="c78f6-108">Spuštění formátu s počátečním mapováním modelu</span><span class="sxs-lookup"><span data-stu-id="c78f6-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="c78f6-109">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="c78f6-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="c78f6-110">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c78f6-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="c78f6-111">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="c78f6-112">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="c78f6-112">Click Check.</span></span>
5. <span data-ttu-id="c78f6-113">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-113">Click Print test.</span></span>
    * <span data-ttu-id="c78f6-114">Spusťte formát pro účely testování.</span><span class="sxs-lookup"><span data-stu-id="c78f6-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="c78f6-115">V poli Obchodovatelný formát šeku vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="c78f6-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="c78f6-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c78f6-116">Click OK.</span></span>
    * <span data-ttu-id="c78f6-117">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c78f6-117">Review the created output.</span></span> <span data-ttu-id="c78f6-118">Všimněte si, že logo společnosti se zobrazí v sestavě společně s podpisem oprávněné osoby.</span><span class="sxs-lookup"><span data-stu-id="c78f6-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="c78f6-119">Obrázek podpisu je převzat z pole typu dat Kontejner ze záznamu rozvržení šeku, který je přidružen k vybranému bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="c78f6-120">Rozbalte sekci Kopie.</span><span class="sxs-lookup"><span data-stu-id="c78f6-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="c78f6-121">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-121">Click Edit.</span></span>
10. <span data-ttu-id="c78f6-122">V poli Vodoznak zadejte Tisknout vodoznak jako anulovaný.</span><span class="sxs-lookup"><span data-stu-id="c78f6-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="c78f6-123">Změňte nastavení rozložení vodoznaku tak, aby byl zobrazen text vodoznaku při generování dokumentu v elementu tvaru Excel.</span><span class="sxs-lookup"><span data-stu-id="c78f6-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="c78f6-124">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-124">Click Print test.</span></span>
12. <span data-ttu-id="c78f6-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c78f6-125">Click OK.</span></span>
    * <span data-ttu-id="c78f6-126">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c78f6-126">Review the created output.</span></span> <span data-ttu-id="c78f6-127">Všimněte si, že vodoznak je uveden v sestavě v souladu s možností výběru.</span><span class="sxs-lookup"><span data-stu-id="c78f6-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="c78f6-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-128">Close the page.</span></span>
14. <span data-ttu-id="c78f6-129">V podokně akcí klikněte na možnost Spravovat platby.</span><span class="sxs-lookup"><span data-stu-id="c78f6-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="c78f6-130">Klikněte na možnost Kontroly.</span><span class="sxs-lookup"><span data-stu-id="c78f6-130">Click Checks.</span></span>
16. <span data-ttu-id="c78f6-131">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="c78f6-131">Click Show filters.</span></span>
17. <span data-ttu-id="c78f6-132">Použijte následující filtry: zadejte hodnotu filtru "381","385","389" v poli Číslo kontroly za pomocí operátoru filtru „je jeden z“.</span><span class="sxs-lookup"><span data-stu-id="c78f6-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="c78f6-133">V seznamu označte všechny řádky.</span><span class="sxs-lookup"><span data-stu-id="c78f6-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="c78f6-134">Klikněte na Tisknout kopii šeku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-134">Click Print check copy.</span></span>
    * <span data-ttu-id="c78f6-135">Spusťte formát a znovu vytiskněte vybrané šeky.</span><span class="sxs-lookup"><span data-stu-id="c78f6-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="c78f6-136">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c78f6-136">Review the created output.</span></span> <span data-ttu-id="c78f6-137">Všimněte si, že vybrané šeky byly znovu vytištěny.</span><span class="sxs-lookup"><span data-stu-id="c78f6-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="c78f6-138">Logo společnosti a popisky nejsou vytištěny, protože jsou uvedeny na předtištěném formuláři.</span><span class="sxs-lookup"><span data-stu-id="c78f6-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="c78f6-139">Úprava mapování importovaného modelu dat</span><span class="sxs-lookup"><span data-stu-id="c78f6-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="c78f6-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-140">Close the page.</span></span>
2. <span data-ttu-id="c78f6-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-141">Close the page.</span></span>
3. <span data-ttu-id="c78f6-142">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c78f6-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="c78f6-143">Ve stromové struktuře zvolte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="c78f6-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="c78f6-144">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c78f6-144">Click Designer.</span></span>
6. <span data-ttu-id="c78f6-145">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="c78f6-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="c78f6-146">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c78f6-146">Click Designer.</span></span>
    * <span data-ttu-id="c78f6-147">Upravíme vazbu položky podpisu datového modelu a získáme tak obrázek podpisu ze souboru připojeného k záznamu rozvržení šeku, který je přidružen k vybranému bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="c78f6-148">Vypněte Zobrazit podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="c78f6-148">Turn Show details off.</span></span>
9. <span data-ttu-id="c78f6-149">Ve stromové struktuře rozbalte Rozvržení.</span><span class="sxs-lookup"><span data-stu-id="c78f6-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="c78f6-150">Ve stromovém zobrazení rozbalte layout\signature.</span><span class="sxs-lookup"><span data-stu-id="c78f6-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="c78f6-151">Ve stromovém zobrazení vyberte layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp.</span><span class="sxs-lookup"><span data-stu-id="c78f6-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="c78f6-152">Ve stromovém zobrazení rozbalte Chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="c78f6-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="c78f6-153">Ve stromovém zobrazení rozbalte chequesaccount\<Relations.</span><span class="sxs-lookup"><span data-stu-id="c78f6-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="c78f6-154">Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout.</span><span class="sxs-lookup"><span data-stu-id="c78f6-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="c78f6-155">Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout\<Relations.</span><span class="sxs-lookup"><span data-stu-id="c78f6-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="c78f6-156">Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout\<Relations\<Document.</span><span class="sxs-lookup"><span data-stu-id="c78f6-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="c78f6-157">Ve stromovém zobrazení vyberte chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer().</span><span class="sxs-lookup"><span data-stu-id="c78f6-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="c78f6-158">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="c78f6-158">Click Bind.</span></span>
19. <span data-ttu-id="c78f6-159">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-159">Click Save.</span></span>
20. <span data-ttu-id="c78f6-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-160">Close the page.</span></span>
21. <span data-ttu-id="c78f6-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-161">Close the page.</span></span>
22. <span data-ttu-id="c78f6-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-162">Close the page.</span></span>
23. <span data-ttu-id="c78f6-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="c78f6-164">Spuštění formátu pomocí upraveného mapování modelu</span><span class="sxs-lookup"><span data-stu-id="c78f6-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="c78f6-165">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="c78f6-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="c78f6-166">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="c78f6-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c78f6-167">Můžete například filtrovat v poli Bankovní účet pomocí hodnoty „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="c78f6-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="c78f6-168">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="c78f6-169">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="c78f6-169">Click Check.</span></span>
5. <span data-ttu-id="c78f6-170">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-170">Click Print test.</span></span>
6. <span data-ttu-id="c78f6-171">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c78f6-171">Click OK.</span></span>
    * <span data-ttu-id="c78f6-172">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c78f6-172">Review the created output.</span></span> <span data-ttu-id="c78f6-173">Všimněte si, že obrázek z přílohy správy dokumentů je zobrazen jako podpis oprávněné osoby.</span><span class="sxs-lookup"><span data-stu-id="c78f6-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="c78f6-174">Použití dokumentu MS Word jako šablony v importovaném formátu</span><span class="sxs-lookup"><span data-stu-id="c78f6-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="c78f6-175">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-175">Close the page.</span></span>
2. <span data-ttu-id="c78f6-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-176">Close the page.</span></span>
3. <span data-ttu-id="c78f6-177">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c78f6-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="c78f6-178">Ve stromové struktuře rozbalte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="c78f6-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="c78f6-179">Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="c78f6-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="c78f6-180">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c78f6-180">Click Designer.</span></span>
7. <span data-ttu-id="c78f6-181">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="c78f6-181">Click Attachments.</span></span>
8. <span data-ttu-id="c78f6-182">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-182">Click Delete.</span></span>
9. <span data-ttu-id="c78f6-183">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="c78f6-183">Click Yes.</span></span>
10. <span data-ttu-id="c78f6-184">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c78f6-184">Click New.</span></span>
11. <span data-ttu-id="c78f6-185">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="c78f6-185">Click File.</span></span>
    * <span data-ttu-id="c78f6-186">Klepněte na tlačítko Procházet a vyberte předem stažený soubor Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="c78f6-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="c78f6-187">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-187">Close the page.</span></span>
13. <span data-ttu-id="c78f6-188">V poli Šablona zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="c78f6-189">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-189">Click Save.</span></span>
15. <span data-ttu-id="c78f6-190">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-190">Close the page.</span></span>
16. <span data-ttu-id="c78f6-191">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c78f6-191">Click Edit.</span></span>
17. <span data-ttu-id="c78f6-192">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="c78f6-193">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-193">Close the page.</span></span>
19. <span data-ttu-id="c78f6-194">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="c78f6-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="c78f6-195">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c78f6-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="c78f6-196">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="c78f6-196">Click Check.</span></span>
22. <span data-ttu-id="c78f6-197">Klikněte na možnost Tisk testu.</span><span class="sxs-lookup"><span data-stu-id="c78f6-197">Click Print test.</span></span>
23. <span data-ttu-id="c78f6-198">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c78f6-198">Click OK.</span></span>
    * <span data-ttu-id="c78f6-199">Prohlédněte si vytvořený výstup.</span><span class="sxs-lookup"><span data-stu-id="c78f6-199">Review the created output.</span></span> <span data-ttu-id="c78f6-200">Všimněte si, že výstup byl vygenerován jako dokument aplikace Word s vloženými obrázky loga společnosti, podpisem oprávněné osoby a vybraným textem vodoznaku.</span><span class="sxs-lookup"><span data-stu-id="c78f6-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


