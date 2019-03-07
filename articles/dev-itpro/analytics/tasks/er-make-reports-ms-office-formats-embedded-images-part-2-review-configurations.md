---
title: Revize konfigurací pro generování sestav ve formátech Office s integrovanými obrázky
description: K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 1 - nastavení parametrů).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3462f16ad7638071ab0aa2175d0bc291eeae89
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "331407"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="a4770-103">Revize konfigurací pro generování sestav ve formátech Office s integrovanými obrázky</span><span class="sxs-lookup"><span data-stu-id="a4770-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4770-104">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 1: nastavení parametrů).</span><span class="sxs-lookup"><span data-stu-id="a4770-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="a4770-105">Tento postup popisuje proces navrhování konfigurací elektronického vykazování (ER) pro generování elektronických dokumentů obsahujících vložené obrázky v aplikaci Microsoft Excel a Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="a4770-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="a4770-106">V tomto příkladu si prohlédnete konfigurace ER pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a4770-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="a4770-107">Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="a4770-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="a4770-108">Kroky lze dokončit za použití datové sady USMF.</span><span class="sxs-lookup"><span data-stu-id="a4770-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="a4770-109">Kontrola importovaného datového modelu</span><span class="sxs-lookup"><span data-stu-id="a4770-109">Review the imported data model</span></span>
1. <span data-ttu-id="a4770-110">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="a4770-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a4770-111">Ve stromové struktuře zvolte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="a4770-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="a4770-112">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="a4770-112">Click Designer.</span></span>
    * <span data-ttu-id="a4770-113">Tento model je určen pro reprezentaci platebních šeků z obchodního hlediska a mapování tohoto modelu ke zdrojům dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="a4770-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="a4770-114">Zkontrolujte tento model návrhářem operací ER.</span><span class="sxs-lookup"><span data-stu-id="a4770-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="a4770-115">Povšimněte si atributů prvků modelu, které jsou uvedeny: struktura, název, popis, datový typ a tak dále.</span><span class="sxs-lookup"><span data-stu-id="a4770-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="a4770-116">Ve stromovém zobrazení rozbalte Kořen.</span><span class="sxs-lookup"><span data-stu-id="a4770-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="a4770-117">Ve stromovém zobrazení vyberte root\cheques.</span><span class="sxs-lookup"><span data-stu-id="a4770-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="a4770-118">Ve stromovém zobrazení rozbalte root\cheques.</span><span class="sxs-lookup"><span data-stu-id="a4770-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="a4770-119">Ve stromovém zobrazení rozbalte root\cheques\attributes.</span><span class="sxs-lookup"><span data-stu-id="a4770-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="a4770-120">Ve stromovém zobrazení rozbalte root\payer.</span><span class="sxs-lookup"><span data-stu-id="a4770-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="a4770-121">Ve stromovém zobrazení vyberte root\istestrun.</span><span class="sxs-lookup"><span data-stu-id="a4770-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="a4770-122">Ve stromovém zobrazení vyberte root\layout.</span><span class="sxs-lookup"><span data-stu-id="a4770-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="a4770-123">Prvek rozvržení tohoto modelu představuje podrobné informace o tisku rozvržení formuláře šeku pro vybraný bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="a4770-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="a4770-124">Dále zahrnuje dva uzly pro Typ datového kontejneru k ukládání obrázků.</span><span class="sxs-lookup"><span data-stu-id="a4770-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="a4770-125">Ve stromovém zobrazení rozbalte root\layout.</span><span class="sxs-lookup"><span data-stu-id="a4770-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="a4770-126">Ve stromovém zobrazení vyberte root\layout\company log.</span><span class="sxs-lookup"><span data-stu-id="a4770-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="a4770-127">Ve stromovém zobrazení rozbalte root\layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="a4770-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="a4770-128">Ve stromovém zobrazení vyberte root\layout\company logo\image.</span><span class="sxs-lookup"><span data-stu-id="a4770-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="a4770-129">Ve stromovém zobrazení vyberte root\layout\company logo\isprinted.</span><span class="sxs-lookup"><span data-stu-id="a4770-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="a4770-130">Ve stromovém zobrazení vyberte root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="a4770-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="a4770-131">Ve stromovém zobrazení rozbalte root\layout\signature.</span><span class="sxs-lookup"><span data-stu-id="a4770-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="a4770-132">Ve stromovém zobrazení vyberte root\layout\signature\image.</span><span class="sxs-lookup"><span data-stu-id="a4770-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="a4770-133">Ve stromovém zobrazení vyberte root\layout\signature\isprinted.</span><span class="sxs-lookup"><span data-stu-id="a4770-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="a4770-134">Všimněte si, že dva elementy modelu dat obrázku jsou vázány k polím tabulky s obrázky loga společnosti a podpisu oprávněné osoby v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="a4770-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="a4770-135">Ve stromovém zobrazení rozbalte root\layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="a4770-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="a4770-136">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="a4770-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="a4770-137">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="a4770-137">Click Designer.</span></span>
23. <span data-ttu-id="a4770-138">Ve stromovém zobrazení rozbalte chequesselected.</span><span class="sxs-lookup"><span data-stu-id="a4770-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="a4770-139">Ve stromové struktuře rozbalte Rozvržení.</span><span class="sxs-lookup"><span data-stu-id="a4770-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="a4770-140">Ve stromovém zobrazení rozbalte layout\company logo.</span><span class="sxs-lookup"><span data-stu-id="a4770-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="a4770-141">Ve stromovém zobrazení rozbalte layout\signature.</span><span class="sxs-lookup"><span data-stu-id="a4770-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="a4770-142">Ve stromovém zobrazení rozbalte layout\watermark.</span><span class="sxs-lookup"><span data-stu-id="a4770-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="a4770-143">Přepnutím aktivujte 'Zobrazit podrobnosti'.</span><span class="sxs-lookup"><span data-stu-id="a4770-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="a4770-144">Všimněte si, že prvek datového modelu šeků má vazbu na tabulku TmpChequePrintout, která za běhu bude obsahovat záznamy šeků, které uživatel vybral pro tisk.</span><span class="sxs-lookup"><span data-stu-id="a4770-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="a4770-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a4770-145">Close the page.</span></span>
30. <span data-ttu-id="a4770-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a4770-146">Close the page.</span></span>
31. <span data-ttu-id="a4770-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a4770-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="a4770-148">Kontrola importovaného formátu</span><span class="sxs-lookup"><span data-stu-id="a4770-148">Review the imported format</span></span>
1. <span data-ttu-id="a4770-149">Ve stromové struktuře rozbalte Model pro šeky.</span><span class="sxs-lookup"><span data-stu-id="a4770-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="a4770-150">Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.</span><span class="sxs-lookup"><span data-stu-id="a4770-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="a4770-151">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="a4770-151">Click Designer.</span></span>
4. <span data-ttu-id="a4770-152">Klikněte na Přílohy.</span><span class="sxs-lookup"><span data-stu-id="a4770-152">Click Attachments.</span></span>
5. <span data-ttu-id="a4770-153">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="a4770-153">Click Open.</span></span>
    * <span data-ttu-id="a4770-154">Otevřete připojenou šablonu sestavy v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="a4770-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="a4770-155">Zkontrolujte šablonu Excel připojené sestavy, která bude použita pro tisk šeků.</span><span class="sxs-lookup"><span data-stu-id="a4770-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="a4770-156">Šablona obsahuje dva šeky na každé stránce a je určena pro tisk šeků na předtištěném formuláři.</span><span class="sxs-lookup"><span data-stu-id="a4770-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="a4770-157">Všimněte si, že jsou vloženy dva prázdné obrázky.</span><span class="sxs-lookup"><span data-stu-id="a4770-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="a4770-158">Tyto prázdné obrázky jsou logo společnosti a podpis osoby, která autorizovala platbu.</span><span class="sxs-lookup"><span data-stu-id="a4770-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="a4770-159">Ověřte, že jsou obrázky pojmenovány v aplikaci Excel jako CompLogo a SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="a4770-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="a4770-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a4770-160">Close the page.</span></span>
7. <span data-ttu-id="a4770-161">Ve stromovém zobrazení rozbalte Sestava.</span><span class="sxs-lookup"><span data-stu-id="a4770-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="a4770-162">Ve stromovém zobrazení rozbalte Report\ChequeLines.</span><span class="sxs-lookup"><span data-stu-id="a4770-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="a4770-163">Ve stromovém zobrazení vyberte Report\ChequeLines\CompLogo.</span><span class="sxs-lookup"><span data-stu-id="a4770-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="a4770-164">Přepnutím aktivujte 'Zobrazit podrobnosti'.</span><span class="sxs-lookup"><span data-stu-id="a4770-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="a4770-165">Všimněte si, že prvek buňky ve formátu CompLogo představuje položku Excel, která slouží k načtení obrázku loga společnosti v sestavě.</span><span class="sxs-lookup"><span data-stu-id="a4770-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="a4770-166">Tento prvek formátu má vazbu na element datového modelu obrázku, který za běhu obsahuje obrázek loga společnosti v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="a4770-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="a4770-167">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="a4770-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="a4770-168">Klikněte na Úprava povolena.</span><span class="sxs-lookup"><span data-stu-id="a4770-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="a4770-169">Poznámka: můžete nastavit element buňky ve formátu "CompLogo" tak, aby již nebyl povolen.</span><span class="sxs-lookup"><span data-stu-id="a4770-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="a4770-170">V takovém případě se na přidruženém prvku obrázku Excel skryje logo společnosti ve vygenerované sestavě.</span><span class="sxs-lookup"><span data-stu-id="a4770-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="a4770-171">Pokud se u povoleného výrazu vrátí hodnota TRUE, a definovaná vazba nepřinese žádný obrázek, přidružený prvek obrázku Excel bude obsahovat obrázek, který byl uložen v šabloně aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a4770-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="a4770-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a4770-172">Close the page.</span></span>
14. <span data-ttu-id="a4770-173">Ve stromovém zobrazení rozbalte Štítky: Kontejner.</span><span class="sxs-lookup"><span data-stu-id="a4770-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="a4770-174">Některé popisky, které jsou uvedeny v předtištěném formuláři šeků, budou zahrnuty do sestavy při jejím vytvoření pro účely testování.</span><span class="sxs-lookup"><span data-stu-id="a4770-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="a4770-175">Tyto štítky se však nevytisknou během skutečného tisku, protože předtištěný formulář je již obsahuje.</span><span class="sxs-lookup"><span data-stu-id="a4770-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="a4770-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a4770-176">Close the page.</span></span>

