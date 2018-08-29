--- 
title: "Návrh konfigurací pro generování sestav ve formátech Office s integrovanými obrázky"
description: "Kroky v tomto tématu popisují informace o navrhování konfigurací elektronického výkaznictví, které generují elektronické dokumenty ve formátech in Microsoft Office formats (Excel a Word) obsahující vložené obrázky."
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="39fa0-103">Návrh konfigurací pro generování sestav ve formátech Office s integrovanými obrázky</span><span class="sxs-lookup"><span data-stu-id="39fa0-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39fa0-104">K provedení kroků v tomto postupu musíte nejprve dokončit postup "Elektronické výkaznictví - Vytvoření poskytovatele konfigurace a jeho označení jako aktivního."</span><span class="sxs-lookup"><span data-stu-id="39fa0-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="39fa0-105">Tento postup vysvětluje proces navrhování konfigurací elektronického výkaznictví pro generování dokumentů v aplikacích Microsoft Excel nebo Word obsahujících vložené obrázky.</span><span class="sxs-lookup"><span data-stu-id="39fa0-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="39fa0-106">V tomto postupu vytvoříte požadované konfigurace elektronického výkaznictví pro vzorovou společnost Litware, Inc. Tyto kroky lze dokončit pomocí sady dat USMF.</span><span class="sxs-lookup"><span data-stu-id="39fa0-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="39fa0-107">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="39fa0-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="39fa0-108">Dříve než začnete, stáhněte a uložte soubory uvedené v tématu nápovědy [Vložení obrázků a tvarů v obchodních dokumentech generovaných pomocí nástroje pro elektronické výkaznictví](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="39fa0-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="39fa0-109">Soubory jsou: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png a Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="39fa0-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="39fa0-110">Kontrola předpokladů</span><span class="sxs-lookup"><span data-stu-id="39fa0-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="39fa0-111">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="39fa0-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="39fa0-112">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní.</span><span class="sxs-lookup"><span data-stu-id="39fa0-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="39fa0-113">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního."</span><span class="sxs-lookup"><span data-stu-id="39fa0-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="39fa0-114">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="39fa0-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="39fa0-115">Přidání nové konfigurace ER modelu</span><span class="sxs-lookup"><span data-stu-id="39fa0-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="39fa0-116">Namísto vytváření nových modelů můžete načíst dříve uložený konfigurační soubor modelu ER (Model pro cheques.xml).</span><span class="sxs-lookup"><span data-stu-id="39fa0-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="39fa0-117">Tento soubor obsahuje ukázkový datový model pro platby šekem a mapování datového modelu na datové komponenty aplikace Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="39fa0-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="39fa0-118">Na pevné záložce Verze klepněte na tlačítko Exchange.</span><span class="sxs-lookup"><span data-stu-id="39fa0-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="39fa0-119">Klikněte na Načíst ze souboru XML.</span><span class="sxs-lookup"><span data-stu-id="39fa0-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="39fa0-120">Klepněte na tlačítko Procházet a vyberte Model pro cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="39fa0-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="39fa0-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="39fa0-121">Click OK.</span></span>  
 6. <span data-ttu-id="39fa0-122">Načtený model bude použit jako datový zdroj informací pro generování dokumentů, které obsahují obrázky v aplikaci Excel a Word.</span><span class="sxs-lookup"><span data-stu-id="39fa0-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="39fa0-123">Přidání nové konfigurace formátu ER</span><span class="sxs-lookup"><span data-stu-id="39fa0-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="39fa0-124">Namísto vytváření nových formátů můžete načíst dříve uložený konfigurační soubor formátu ER (Tisk šeků format.xml).</span><span class="sxs-lookup"><span data-stu-id="39fa0-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="39fa0-125">Tento soubor obsahuje ukázkové rozložení formátu tisku šeků pomocí předtištěného formuláře a mapování tohoto formátu na model pro datový model šeků.</span><span class="sxs-lookup"><span data-stu-id="39fa0-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="39fa0-126">Klikněte na Směna.</span><span class="sxs-lookup"><span data-stu-id="39fa0-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="39fa0-127">Klikněte na Načíst ze souboru XML.</span><span class="sxs-lookup"><span data-stu-id="39fa0-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="39fa0-128">Klepněte na tlačítko Procházet a vyberte soubor Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="39fa0-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="39fa0-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="39fa0-129">Click OK.</span></span>  
 6. <span data-ttu-id="39fa0-130">Ve stromové struktuře rozbalte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="39fa0-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="39fa0-131">Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="39fa0-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="39fa0-132">Načtený formát bude použit jako datový zdroj informací pro generování dokumentů, které obsahují obrázky v aplikaci Excel a Word.</span><span class="sxs-lookup"><span data-stu-id="39fa0-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="39fa0-133">Konfigurace parametrů uživatele ER</span><span class="sxs-lookup"><span data-stu-id="39fa0-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="39fa0-134">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="39fa0-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="39fa0-135">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="39fa0-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="39fa0-136">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="39fa0-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="39fa0-137">Zapněte příznak 'Spusťte koncept' tak, aby se spustila pracovní verze ve vybraném formátu namísto dokončené.</span><span class="sxs-lookup"><span data-stu-id="39fa0-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="39fa0-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="39fa0-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="39fa0-139">Konfigurovat parametry správy Pokladny a banky</span><span class="sxs-lookup"><span data-stu-id="39fa0-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="39fa0-140">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="39fa0-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="39fa0-141">Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="39fa0-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="39fa0-142">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="39fa0-143">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="39fa0-143">Click Check.</span></span>  
 5. <span data-ttu-id="39fa0-144">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="39fa0-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="39fa0-145">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-145">Click Edit.</span></span>  
 7. <span data-ttu-id="39fa0-146">Vyberte Ano v poli Firemní logo.</span><span class="sxs-lookup"><span data-stu-id="39fa0-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="39fa0-147">Klikněte na Firemní logo.</span><span class="sxs-lookup"><span data-stu-id="39fa0-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="39fa0-148">Klikněte na tlačítko Změnit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-148">Click Change.</span></span>  
 10. <span data-ttu-id="39fa0-149">Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="39fa0-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="39fa0-150">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-150">Click Save.</span></span>  
 12. <span data-ttu-id="39fa0-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39fa0-151">Close the page.</span></span>  
 13. <span data-ttu-id="39fa0-152">Rozbalte sekci Podpis.</span><span class="sxs-lookup"><span data-stu-id="39fa0-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="39fa0-153">Vyberte možnost Ano v poli Tisk prvního podpisu.</span><span class="sxs-lookup"><span data-stu-id="39fa0-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="39fa0-154">Klikněte na tlačítko Změnit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-154">Click Change.</span></span>  
 16. <span data-ttu-id="39fa0-155">Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="39fa0-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="39fa0-156">Rozbalte sekci Kopie.</span><span class="sxs-lookup"><span data-stu-id="39fa0-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="39fa0-157">Vyberte volbu v poli Vodoznak.</span><span class="sxs-lookup"><span data-stu-id="39fa0-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="39fa0-158">Vyberte možnost Ano v poli Obecný formát exportu.</span><span class="sxs-lookup"><span data-stu-id="39fa0-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="39fa0-159">Vyberte konfiguraci 'Formulář pro tisk šeků'.</span><span class="sxs-lookup"><span data-stu-id="39fa0-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="39fa0-160">Nyní bude vybraný formát ER použit pro tisk šeků.</span><span class="sxs-lookup"><span data-stu-id="39fa0-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="39fa0-161">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-161">Click Attach.</span></span>  
 23. <span data-ttu-id="39fa0-162">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39fa0-162">Click New.</span></span>  
 24. <span data-ttu-id="39fa0-163">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="39fa0-163">Click File.</span></span>  
 25. <span data-ttu-id="39fa0-164">Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="39fa0-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="39fa0-165">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39fa0-165">Close the page.</span></span>  
 27. <span data-ttu-id="39fa0-166">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39fa0-166">Close the page.</span></span>  
 28. <span data-ttu-id="39fa0-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39fa0-167">Close the page.</span></span>  
 29. <span data-ttu-id="39fa0-168">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="39fa0-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="39fa0-169">Vyberte možnost Ano v poli Povolit vytváření verifikačních transakcí v neaktivních bankovních účtech:.</span><span class="sxs-lookup"><span data-stu-id="39fa0-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="39fa0-170">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="39fa0-170">Click Save.</span></span>  
 32. <span data-ttu-id="39fa0-171">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39fa0-171">Close the page.</span></span>  

