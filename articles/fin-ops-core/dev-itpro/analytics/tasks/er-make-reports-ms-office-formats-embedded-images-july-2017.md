---
title: Návrh konfigurací pro generování sestav ve formátech Office s integrovanými obrázky
description: Toto téma popisuje proces navrhování konfigurací, které generují elektronické dokumenty ve formátech Excel a Word, které obsahují vestavěné obrázky.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944550"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="be41c-103">Návrh konfigurací pro generování sestav ve formátech Office s integrovanými obrázky</span><span class="sxs-lookup"><span data-stu-id="be41c-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be41c-104">K provedení kroků v tomto postupu musíte nejprve dokončit postup "Elektronické výkaznictví - Vytvoření poskytovatele konfigurace a jeho označení jako aktivního."</span><span class="sxs-lookup"><span data-stu-id="be41c-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="be41c-105">Tento postup vysvětluje proces navrhování konfigurací elektronického výkaznictví pro generování dokumentů v aplikacích Microsoft Excel nebo Word obsahujících vložené obrázky.</span><span class="sxs-lookup"><span data-stu-id="be41c-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="be41c-106">V tomto postupu vytvoříte požadované konfigurace elektronického výkaznictví pro vzorovou společnost Litware, Inc. Tyto kroky lze dokončit pomocí sady dat USMF.</span><span class="sxs-lookup"><span data-stu-id="be41c-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="be41c-107">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="be41c-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="be41c-108">Před přihlášením je také nutné stáhnout a uložit následující soubory:</span><span class="sxs-lookup"><span data-stu-id="be41c-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="be41c-109">popis</span><span class="sxs-lookup"><span data-stu-id="be41c-109">Description</span></span>                                          | <span data-ttu-id="be41c-110">Název souboru</span><span class="sxs-lookup"><span data-stu-id="be41c-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="be41c-111">Konfigurace datového modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="be41c-111">ER data model configuration</span></span>                          | [<span data-ttu-id="be41c-112">Model pro cheques.xml</span><span class="sxs-lookup"><span data-stu-id="be41c-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="be41c-113">Konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="be41c-113">ER format configuration</span></span>                              | [<span data-ttu-id="be41c-114">format.xml pro tisk šeků</span><span class="sxs-lookup"><span data-stu-id="be41c-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="be41c-115">Obrázek loga společnosti</span><span class="sxs-lookup"><span data-stu-id="be41c-115">Company logo image</span></span>                                   | [<span data-ttu-id="be41c-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="be41c-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="be41c-117">Podpisový obrázek</span><span class="sxs-lookup"><span data-stu-id="be41c-117">Signature image</span></span>                                      | [<span data-ttu-id="be41c-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="be41c-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="be41c-119">Alternativní podpisový obrázek</span><span class="sxs-lookup"><span data-stu-id="be41c-119">Alternative signature image</span></span>                          | [<span data-ttu-id="be41c-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="be41c-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="be41c-121">Šablona Microsoft Word pro tisk platebních šeků</span><span class="sxs-lookup"><span data-stu-id="be41c-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="be41c-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="be41c-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="be41c-123">Kontrola předpokladů</span><span class="sxs-lookup"><span data-stu-id="be41c-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="be41c-124">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="be41c-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="be41c-125">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní.</span><span class="sxs-lookup"><span data-stu-id="be41c-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="be41c-126">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="be41c-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="be41c-127">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="be41c-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="be41c-128">Přidání nové konfigurace ER modelu</span><span class="sxs-lookup"><span data-stu-id="be41c-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="be41c-129">Namísto vytváření nových modelů můžete načíst dříve uložený konfigurační soubor modelu ER (Model pro cheques.xml).</span><span class="sxs-lookup"><span data-stu-id="be41c-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="be41c-130">Tento soubor obsahuje ukázkový datový model pro platby šekem a mapování datového modelu na datové komponenty aplikace Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="be41c-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="be41c-131">Na pevné záložce Verze klepněte na tlačítko Exchange.</span><span class="sxs-lookup"><span data-stu-id="be41c-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="be41c-132">Klikněte na Načíst ze souboru XML.</span><span class="sxs-lookup"><span data-stu-id="be41c-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="be41c-133">Klepněte na tlačítko Procházet a vyberte Model pro cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="be41c-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="be41c-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be41c-134">Click OK.</span></span>  
 6. <span data-ttu-id="be41c-135">Načtený model bude použit jako datový zdroj informací pro generování dokumentů, které obsahují obrázky v aplikaci Excel a Word.</span><span class="sxs-lookup"><span data-stu-id="be41c-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="be41c-136">Přidání nové konfigurace formátu ER</span><span class="sxs-lookup"><span data-stu-id="be41c-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="be41c-137">Namísto vytváření nových formátů můžete načíst dříve uložený konfigurační soubor formátu ER (Tisk šeků format.xml).</span><span class="sxs-lookup"><span data-stu-id="be41c-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="be41c-138">Tento soubor obsahuje ukázkové rozložení formátu tisku šeků pomocí předtištěného formuláře a mapování tohoto formátu na model pro 'datový model šeků'.</span><span class="sxs-lookup"><span data-stu-id="be41c-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="be41c-139">Klikněte na Směna.</span><span class="sxs-lookup"><span data-stu-id="be41c-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="be41c-140">Klikněte na Načíst ze souboru XML.</span><span class="sxs-lookup"><span data-stu-id="be41c-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="be41c-141">Klepněte na tlačítko Procházet a vyberte soubor Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="be41c-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="be41c-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be41c-142">Click OK.</span></span>  
 6. <span data-ttu-id="be41c-143">Ve stromové struktuře rozbalte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="be41c-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="be41c-144">Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="be41c-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="be41c-145">Načtený formát bude použit jako datový zdroj informací pro generování dokumentů, které obsahují obrázky v aplikaci Excel a Word.</span><span class="sxs-lookup"><span data-stu-id="be41c-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="be41c-146">Konfigurace parametrů uživatele ER</span><span class="sxs-lookup"><span data-stu-id="be41c-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="be41c-147">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="be41c-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="be41c-148">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="be41c-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="be41c-149">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="be41c-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="be41c-150">Zapněte příznak 'Spusťte koncept' tak, aby se spustila pracovní verze ve vybraném formátu namísto dokončené.</span><span class="sxs-lookup"><span data-stu-id="be41c-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="be41c-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be41c-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="be41c-152">Konfigurovat parametry správy Pokladny a banky</span><span class="sxs-lookup"><span data-stu-id="be41c-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="be41c-153">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="be41c-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="be41c-154">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="be41c-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="be41c-155">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="be41c-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="be41c-156">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="be41c-156">Click Check.</span></span>  
 5. <span data-ttu-id="be41c-157">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="be41c-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="be41c-158">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="be41c-158">Click Edit.</span></span>  
 7. <span data-ttu-id="be41c-159">Vyberte Ano v poli Firemní logo.</span><span class="sxs-lookup"><span data-stu-id="be41c-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="be41c-160">Klikněte na Firemní logo.</span><span class="sxs-lookup"><span data-stu-id="be41c-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="be41c-161">Klikněte na tlačítko Změnit.</span><span class="sxs-lookup"><span data-stu-id="be41c-161">Click Change.</span></span>  
 10. <span data-ttu-id="be41c-162">Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="be41c-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="be41c-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be41c-163">Click Save.</span></span>  
 12. <span data-ttu-id="be41c-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be41c-164">Close the page.</span></span>  
 13. <span data-ttu-id="be41c-165">Rozbalte sekci Podpis.</span><span class="sxs-lookup"><span data-stu-id="be41c-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="be41c-166">Vyberte možnost Ano v poli Tisk prvního podpisu.</span><span class="sxs-lookup"><span data-stu-id="be41c-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="be41c-167">Klikněte na tlačítko Změnit.</span><span class="sxs-lookup"><span data-stu-id="be41c-167">Click Change.</span></span>  
 16. <span data-ttu-id="be41c-168">Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="be41c-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="be41c-169">Rozbalte sekci Kopie.</span><span class="sxs-lookup"><span data-stu-id="be41c-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="be41c-170">Vyberte volbu v poli Vodoznak.</span><span class="sxs-lookup"><span data-stu-id="be41c-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="be41c-171">Vyberte možnost Ano v poli Obecný formát exportu.</span><span class="sxs-lookup"><span data-stu-id="be41c-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="be41c-172">Vyberte konfiguraci 'Formulář pro tisk šeků'.</span><span class="sxs-lookup"><span data-stu-id="be41c-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="be41c-173">Nyní bude vybraný formát ER použit pro tisk šeků.</span><span class="sxs-lookup"><span data-stu-id="be41c-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="be41c-174">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="be41c-174">Click Attach.</span></span>  
 23. <span data-ttu-id="be41c-175">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be41c-175">Click New.</span></span>  
 24. <span data-ttu-id="be41c-176">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="be41c-176">Click File.</span></span>  
 25. <span data-ttu-id="be41c-177">Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="be41c-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="be41c-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be41c-178">Close the page.</span></span>  
 27. <span data-ttu-id="be41c-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be41c-179">Close the page.</span></span>  
 28. <span data-ttu-id="be41c-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be41c-180">Close the page.</span></span>  
 29. <span data-ttu-id="be41c-181">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="be41c-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="be41c-182">Vyberte možnost Ano v poli Povolit vytváření verifikačních transakcí v neaktivních bankovních účtech:.</span><span class="sxs-lookup"><span data-stu-id="be41c-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="be41c-183">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be41c-183">Click Save.</span></span>  
 32. <span data-ttu-id="be41c-184">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be41c-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
