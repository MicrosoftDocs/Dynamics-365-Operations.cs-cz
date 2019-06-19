---
title: EUR-00002 Generování prohlášení Intrastat EU
description: Tento postup vás provede kroky nutnými k exportu prohlášení systému Intrastat ve formátu elektronického souboru a náhledu dat výkazu ve formátu aplikace Excel.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1236f27a3a5c208ffec41374a6593d1f0e7c4433
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566781"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="eaebe-103">EUR-00002 Generování prohlášení Intrastat EU</span><span class="sxs-lookup"><span data-stu-id="eaebe-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eaebe-104">Tento postup vás provede kroky nutnými k exportu prohlášení systému Intrastat ve formátu elektronického souboru a náhledu dat výkazu ve formátu aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="eaebe-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="eaebe-105">Před provedením tohoto postupu je nutné převést transakce do systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="eaebe-106">Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="eaebe-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="eaebe-107">Importování konfigurací s nastavením</span><span class="sxs-lookup"><span data-stu-id="eaebe-107">Import configurations with settings</span></span>
1. <span data-ttu-id="eaebe-108">Přejděte na Pracovní prostory > Elektronické sestavy</span><span class="sxs-lookup"><span data-stu-id="eaebe-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="eaebe-109">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="eaebe-109">Click Set active.</span></span>
3. <span data-ttu-id="eaebe-110">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="eaebe-110">Click Repositories.</span></span>
4. <span data-ttu-id="eaebe-111">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="eaebe-111">Click Open.</span></span>
5. <span data-ttu-id="eaebe-112">Otevřete filtr sloupce Název konfigurace.</span><span class="sxs-lookup"><span data-stu-id="eaebe-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="eaebe-113">Použijte filtr v poli Název konfigurace, s hodnotou Intrastat (DE) a za použití operátoru filtru "začíná".</span><span class="sxs-lookup"><span data-stu-id="eaebe-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="eaebe-114">Musíte vybrat název konfigurace platný pro zemi vaší právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="eaebe-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="eaebe-115">Tento postup používá jako příklad právnickou osobu (DEMF) pro Německo a měla by být proto zvolena možnost "Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="eaebe-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="eaebe-116">Klikněte na položku Import a poté na možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="eaebe-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="eaebe-117">Otevřete filtr sloupce Název konfigurace.</span><span class="sxs-lookup"><span data-stu-id="eaebe-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="eaebe-118">Použijte filtr v poli Název konfigurace, s hodnotou Sestava Intrastat a za použití operátoru filtru "začíná".</span><span class="sxs-lookup"><span data-stu-id="eaebe-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="eaebe-119">Klikněte na položku Import a poté na možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="eaebe-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="eaebe-120">Nastavení parametrů zahraničního obchodu</span><span class="sxs-lookup"><span data-stu-id="eaebe-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="eaebe-121">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="eaebe-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="eaebe-122">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="eaebe-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="eaebe-123">V poli Mapování formátu souboru zadejte nebo vyberte hodnotu Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="eaebe-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="eaebe-124">V poli Mapování formátu sestavy zadejte nebo vyberte hodnotu Sestava Intrastat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="eaebe-125">Rozbalte položku Pravidla zaokrouhlování.</span><span class="sxs-lookup"><span data-stu-id="eaebe-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="eaebe-126">Měli byste nastavit pravidla zaokrouhlení, která jsou platná ve vaší zemi/oblasti pro vykazování v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="eaebe-127">V poli Pravidlo zaokrouhlování zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="eaebe-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="eaebe-128">Zadejte přesnost zaokrouhlení, například zadejte hodnotu 0,01.</span><span class="sxs-lookup"><span data-stu-id="eaebe-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="eaebe-129">Do pole Počet desetinných míst částky zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="eaebe-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="eaebe-130">Například zadejte 2.</span><span class="sxs-lookup"><span data-stu-id="eaebe-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="eaebe-131">Vyberte možnost v poli Zaokrouhlování pod 1 kg.</span><span class="sxs-lookup"><span data-stu-id="eaebe-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="eaebe-132">Vyberte například 'Zaokrouhlování nahoru na 1 kg'.</span><span class="sxs-lookup"><span data-stu-id="eaebe-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="eaebe-133">V poli Pravidlo zaokrouhlování zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="eaebe-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="eaebe-134">Například zadejte hodnotu 1 pro zaokrouhlování hmotnosti na celé číslo.</span><span class="sxs-lookup"><span data-stu-id="eaebe-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="eaebe-135">Rozbalte oddíl Minimální limit.</span><span class="sxs-lookup"><span data-stu-id="eaebe-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="eaebe-136">Zadejte číslo do pole Hmotnost.</span><span class="sxs-lookup"><span data-stu-id="eaebe-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="eaebe-137">Například zadejte hodnotu 10 jako minimální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="eaebe-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="eaebe-138">Zadejte číslo do pole Částka.</span><span class="sxs-lookup"><span data-stu-id="eaebe-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="eaebe-139">Například zadejte hodnotu 200 jako minimální částku.</span><span class="sxs-lookup"><span data-stu-id="eaebe-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="eaebe-140">V poli Komodita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="eaebe-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="eaebe-141">Nastavení komprese pro systém Intrastat</span><span class="sxs-lookup"><span data-stu-id="eaebe-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="eaebe-142">Přejděte na Daň > Nastavení > Zahraniční obchod > Komprese Intrastat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="eaebe-143">Klepněte na tlačítko Odebrat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-143">Click Remove.</span></span>
3. <span data-ttu-id="eaebe-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaebe-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eaebe-145">V oddílu Dostupné vyberte například Zboží.</span><span class="sxs-lookup"><span data-stu-id="eaebe-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="eaebe-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="eaebe-147">Generování prohlášení Intrastat</span><span class="sxs-lookup"><span data-stu-id="eaebe-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="eaebe-148">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat</span><span class="sxs-lookup"><span data-stu-id="eaebe-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="eaebe-149">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="eaebe-149">Click Validate.</span></span>
    * <span data-ttu-id="eaebe-150">Ověření se provádí podle pole Zkontrolovat nastavení na stránce Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="eaebe-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="eaebe-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaebe-151">Click OK.</span></span>
4. <span data-ttu-id="eaebe-152">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-152">Click Update.</span></span>
5. <span data-ttu-id="eaebe-153">Klikněte na Minimální limit.</span><span class="sxs-lookup"><span data-stu-id="eaebe-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="eaebe-154">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="eaebe-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="eaebe-155">V tomto příkladu zadejte 1. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="eaebe-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="eaebe-156">Vyberte Ano v poli Komprese.</span><span class="sxs-lookup"><span data-stu-id="eaebe-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="eaebe-157">Zadejte datum do pole Koncové datum.</span><span class="sxs-lookup"><span data-stu-id="eaebe-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="eaebe-158">V tomto příkladu zadejte 31. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="eaebe-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="eaebe-159">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaebe-159">Click OK.</span></span>
10. <span data-ttu-id="eaebe-160">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-160">Click Update.</span></span>
11. <span data-ttu-id="eaebe-161">Klikněte na Komprese.</span><span class="sxs-lookup"><span data-stu-id="eaebe-161">Click Compress.</span></span>
    * <span data-ttu-id="eaebe-162">Tato komprese proběhne podle nastavení komprese v systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="eaebe-163">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="eaebe-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="eaebe-164">V tomto příkladu zadejte 1. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="eaebe-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="eaebe-165">Zadejte datum do pole Koncové datum.</span><span class="sxs-lookup"><span data-stu-id="eaebe-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="eaebe-166">V tomto příkladu zadejte 31. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="eaebe-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="eaebe-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaebe-167">Click OK.</span></span>
15. <span data-ttu-id="eaebe-168">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="eaebe-168">Click Update.</span></span>
16. <span data-ttu-id="eaebe-169">Klikněte na Znovu vygenerovat číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="eaebe-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="eaebe-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaebe-170">Click OK.</span></span>
18. <span data-ttu-id="eaebe-171">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="eaebe-171">Click Output.</span></span>
19. <span data-ttu-id="eaebe-172">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="eaebe-172">Click Report.</span></span>
20. <span data-ttu-id="eaebe-173">V poli Od data zadejte první datum období vykazování.</span><span class="sxs-lookup"><span data-stu-id="eaebe-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="eaebe-174">Například můžete nastavit datum na 1. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="eaebe-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="eaebe-175">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="eaebe-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="eaebe-176">V tomto příkladu zadejte 31. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="eaebe-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="eaebe-177">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="eaebe-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="eaebe-178">Zadejte hodnotu do pole Název souboru.</span><span class="sxs-lookup"><span data-stu-id="eaebe-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="eaebe-179">Vyberte možnost Ano v poli Generovat sestavu.</span><span class="sxs-lookup"><span data-stu-id="eaebe-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="eaebe-180">Zadejte hodnotu do pole Název souboru sestavy.</span><span class="sxs-lookup"><span data-stu-id="eaebe-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="eaebe-181">Vyberte volbu v poli Směr.</span><span class="sxs-lookup"><span data-stu-id="eaebe-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="eaebe-182">V tomto příkladu vyberte Expedice.</span><span class="sxs-lookup"><span data-stu-id="eaebe-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="eaebe-183">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaebe-183">Click OK.</span></span>

