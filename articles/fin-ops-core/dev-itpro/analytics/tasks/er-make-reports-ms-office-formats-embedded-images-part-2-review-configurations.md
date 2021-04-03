---
title: Revize konfigurací pro generování sestav ve formátech Office s integrovanými obrázky
description: Toto téma popisuje proces navrhování konfigurací elektronického výkaznictví ke generování elektronických dokumentů obsahujících vložené obrázky. (část 1 - Nastavení parametrů).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6aa5c4d45f9139c65f3aaf1ae392829e3e4967df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569430"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="ac367-104">Revize konfigurací pro generování sestav ve formátech Office s integrovanými obrázky</span><span class="sxs-lookup"><span data-stu-id="ac367-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac367-105">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh "Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 1: nastavení parametrů)".</span><span class="sxs-lookup"><span data-stu-id="ac367-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="ac367-106">Tento postup popisuje proces navrhování konfigurací elektronického vykazování (ER) pro generování elektronických dokumentů obsahujících vložené obrázky v aplikaci Microsoft Excel a Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="ac367-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="ac367-107">V tomto příkladu si prohlédnete konfigurace ER pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ac367-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="ac367-108">Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="ac367-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="ac367-109">Kroky lze dokončit za použití datové sady USMF.</span><span class="sxs-lookup"><span data-stu-id="ac367-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="ac367-110">Kontrola importovaného datového modelu</span><span class="sxs-lookup"><span data-stu-id="ac367-110">Review the imported data model</span></span>
1. <span data-ttu-id="ac367-111">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ac367-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ac367-112">Ve stromové struktuře zvolte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="ac367-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="ac367-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="ac367-113">Click Designer.</span></span>
    * <span data-ttu-id="ac367-114">Tento model je určen pro reprezentaci platebních šeků z obchodního hlediska a mapování tohoto modelu ke zdrojům dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="ac367-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="ac367-115">Zkontrolujte tento model návrhářem operací ER.</span><span class="sxs-lookup"><span data-stu-id="ac367-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="ac367-116">Povšimněte si atributů prvků modelu, které jsou uvedeny: struktura, název, popis, datový typ a tak dále.</span><span class="sxs-lookup"><span data-stu-id="ac367-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="ac367-117">Ve stromovém zobrazení rozbalte Kořen.</span><span class="sxs-lookup"><span data-stu-id="ac367-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="ac367-118">Ve stromovém zobrazení vyberte root\cheques.</span><span class="sxs-lookup"><span data-stu-id="ac367-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="ac367-119">Ve stromovém zobrazení rozbalte root\cheques.</span><span class="sxs-lookup"><span data-stu-id="ac367-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="ac367-120">Ve stromovém zobrazení rozbalte root\cheques\attributes.</span><span class="sxs-lookup"><span data-stu-id="ac367-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="ac367-121">Ve stromovém zobrazení rozbalte root\payer.</span><span class="sxs-lookup"><span data-stu-id="ac367-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="ac367-122">Ve stromovém zobrazení vyberte root\istestrun.</span><span class="sxs-lookup"><span data-stu-id="ac367-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="ac367-123">Ve stromovém zobrazení vyberte root\layout.</span><span class="sxs-lookup"><span data-stu-id="ac367-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="ac367-124">Prvek rozvržení tohoto modelu představuje podrobné informace o tisku rozvržení formuláře šeku pro vybraný bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="ac367-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="ac367-125">Dále zahrnuje dva uzly pro Typ datového kontejneru k ukládání obrázků.</span><span class="sxs-lookup"><span data-stu-id="ac367-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="ac367-126">Ve stromovém zobrazení rozbalte root\layout.</span><span class="sxs-lookup"><span data-stu-id="ac367-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="ac367-127">Ve stromovém zobrazení vyberte root\layout\company log.</span><span class="sxs-lookup"><span data-stu-id="ac367-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="ac367-128">Ve stromovém zobrazení rozbalte root\layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="ac367-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="ac367-129">Ve stromovém zobrazení vyberte root\layout\company logo\image.</span><span class="sxs-lookup"><span data-stu-id="ac367-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="ac367-130">Ve stromovém zobrazení vyberte root\layout\company logo\isprinted.</span><span class="sxs-lookup"><span data-stu-id="ac367-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="ac367-131">Ve stromovém zobrazení vyberte root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="ac367-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="ac367-132">Ve stromovém zobrazení rozbalte root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="ac367-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="ac367-133">Ve stromovém zobrazení vyberte root\layout\signature\image.</span><span class="sxs-lookup"><span data-stu-id="ac367-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="ac367-134">Ve stromovém zobrazení vyberte root\layout\signature\isprinted.</span><span class="sxs-lookup"><span data-stu-id="ac367-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="ac367-135">Všimněte si, že dva elementy modelu dat obrázku jsou vázány k polím tabulky s obrázky loga společnosti a podpisu oprávněné osoby v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="ac367-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="ac367-136">Ve stromovém zobrazení rozbalte root\layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="ac367-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="ac367-137">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="ac367-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="ac367-138">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="ac367-138">Click Designer.</span></span>
23. <span data-ttu-id="ac367-139">Ve stromovém zobrazení rozbalte chequesselected.</span><span class="sxs-lookup"><span data-stu-id="ac367-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="ac367-140">Ve stromové struktuře rozbalte Rozvržení.</span><span class="sxs-lookup"><span data-stu-id="ac367-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="ac367-141">Ve stromovém zobrazení rozbalte layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="ac367-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="ac367-142">Ve stromovém zobrazení rozbalte layout\signature.</span><span class="sxs-lookup"><span data-stu-id="ac367-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="ac367-143">Ve stromovém zobrazení rozbalte layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="ac367-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="ac367-144">Přepnutím aktivujte 'Zobrazit podrobnosti'.</span><span class="sxs-lookup"><span data-stu-id="ac367-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="ac367-145">Všimněte si, že prvek datového modelu šeků má vazbu na tabulku TmpChequePrintout, která za běhu bude obsahovat záznamy šeků, které uživatel vybral pro tisk.</span><span class="sxs-lookup"><span data-stu-id="ac367-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="ac367-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac367-146">Close the page.</span></span>
30. <span data-ttu-id="ac367-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac367-147">Close the page.</span></span>
31. <span data-ttu-id="ac367-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac367-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="ac367-149">Kontrola importovaného formátu</span><span class="sxs-lookup"><span data-stu-id="ac367-149">Review the imported format</span></span>
1. <span data-ttu-id="ac367-150">Ve stromové struktuře rozbalte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="ac367-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="ac367-151">Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="ac367-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="ac367-152">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="ac367-152">Click Designer.</span></span>
4. <span data-ttu-id="ac367-153">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="ac367-153">Click Attachments.</span></span>
5. <span data-ttu-id="ac367-154">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="ac367-154">Click Open.</span></span>
    * <span data-ttu-id="ac367-155">Otevřete připojenou šablonu sestavy v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="ac367-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="ac367-156">Zkontrolujte šablonu Excel připojené sestavy, která bude použita pro tisk šeků.</span><span class="sxs-lookup"><span data-stu-id="ac367-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="ac367-157">Šablona obsahuje dva šeky na každé stránce a je určena pro tisk šeků na předtištěném formuláři.</span><span class="sxs-lookup"><span data-stu-id="ac367-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="ac367-158">Všimněte si, že jsou vloženy dva prázdné obrázky.</span><span class="sxs-lookup"><span data-stu-id="ac367-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="ac367-159">Tyto prázdné obrázky jsou logo společnosti a podpis osoby, která autorizovala platbu.</span><span class="sxs-lookup"><span data-stu-id="ac367-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="ac367-160">Ověřte, že jsou obrázky pojmenovány v aplikaci Excel jako CompLogo a SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="ac367-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="ac367-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac367-161">Close the page.</span></span>
7. <span data-ttu-id="ac367-162">Ve stromovém zobrazení rozbalte Sestava.</span><span class="sxs-lookup"><span data-stu-id="ac367-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="ac367-163">Ve stromovém zobrazení rozbalte Report\ChequeLines.</span><span class="sxs-lookup"><span data-stu-id="ac367-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="ac367-164">Ve stromovém zobrazení vyberte Report\ChequeLines\CompLogo.</span><span class="sxs-lookup"><span data-stu-id="ac367-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="ac367-165">Přepnutím aktivujte 'Zobrazit podrobnosti'.</span><span class="sxs-lookup"><span data-stu-id="ac367-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="ac367-166">Všimněte si, že prvek buňky ve formátu 'CompLogo' představuje položku Excel, která slouží k načtení obrázku loga společnosti v sestavě.</span><span class="sxs-lookup"><span data-stu-id="ac367-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="ac367-167">Tento prvek formátu má vazbu na element datového modelu obrázku, který za běhu obsahuje obrázek loga společnosti v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="ac367-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="ac367-168">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="ac367-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="ac367-169">Klikněte na Úprava povolena.</span><span class="sxs-lookup"><span data-stu-id="ac367-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="ac367-170">Poznámka: můžete nastavit element buňky ve formátu "CompLogo" tak, aby již nebyl povolen.</span><span class="sxs-lookup"><span data-stu-id="ac367-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="ac367-171">V takovém případě se na přidruženém prvku obrázku Excel skryje logo společnosti ve vygenerované sestavě.</span><span class="sxs-lookup"><span data-stu-id="ac367-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="ac367-172">Pokud se u povoleného výrazu vrátí hodnota TRUE, a definovaná vazba nepřinese žádný obrázek, přidružený prvek obrázku Excel bude obsahovat obrázek, který byl uložen v šabloně aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ac367-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="ac367-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac367-173">Close the page.</span></span>
14. <span data-ttu-id="ac367-174">Ve stromovém zobrazení rozbalte Štítky: Kontejner.</span><span class="sxs-lookup"><span data-stu-id="ac367-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="ac367-175">Některé popisky, které jsou uvedeny v předtištěném formuláři šeků, budou zahrnuty do sestavy při jejím vytvoření pro účely testování.</span><span class="sxs-lookup"><span data-stu-id="ac367-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="ac367-176">Tyto štítky se však nevytisknou během skutečného tisku, protože předtištěný formulář je již obsahuje.</span><span class="sxs-lookup"><span data-stu-id="ac367-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="ac367-177">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac367-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]