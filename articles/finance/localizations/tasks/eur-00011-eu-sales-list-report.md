---
title: EUR-00011 Vygenerování sestavy Souhrnné hlášení (EU)
description: Tento postup vás provede generováním sestavy souhrnného hlášení EU.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 37f1a6e3bf39e16702d1367a325134ec84369945
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407585"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="81d9d-103">EUR-00011 Vygenerování sestavy Souhrnné hlášení (EU)</span><span class="sxs-lookup"><span data-stu-id="81d9d-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81d9d-104">Tento postup vás provede generováním sestavy souhrnného hlášení EU.</span><span class="sxs-lookup"><span data-stu-id="81d9d-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="81d9d-105">To zahrnuje převod interních obchodních transakcí do souhrnného hlášení EU a spuštění sestavy.</span><span class="sxs-lookup"><span data-stu-id="81d9d-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="81d9d-106">Tento postup také zahrnuje vytváření interních obchodních transakcí pro účely ukázky.</span><span class="sxs-lookup"><span data-stu-id="81d9d-106">This procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="81d9d-107">Další informace o výkazu se seznamem prodeje v EU včetně případných požadovaných předpokladů naleznete v nápovědě.</span><span class="sxs-lookup"><span data-stu-id="81d9d-107">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="81d9d-108">Postup se vztahuje na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="81d9d-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="81d9d-109">Postup byl vytvořen použitím ukázkových dat společnosti DEMF a následně Německa jako příklad pro domácí zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="81d9d-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="81d9d-110">Postup také využívá Portugalsko jako příklad země nebo oblasti EU.</span><span class="sxs-lookup"><span data-stu-id="81d9d-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="81d9d-111">Před dokončením tohoto postupu, je nutné konfigurovat vytváření souhrnného hlášení EU.</span><span class="sxs-lookup"><span data-stu-id="81d9d-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="81d9d-112">Tento postup je určen pouze pro účetní.</span><span class="sxs-lookup"><span data-stu-id="81d9d-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="81d9d-113">Vytvoření interních prodejních transakcí pro účely ukázky</span><span class="sxs-lookup"><span data-stu-id="81d9d-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="81d9d-114">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="81d9d-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="81d9d-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="81d9d-115">Click New.</span></span>
3. <span data-ttu-id="81d9d-116">V poli Účet odběratele zadejte „PRT-001“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="81d9d-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d9d-117">Click OK.</span></span>
5. <span data-ttu-id="81d9d-118">Do pole Číslo položky zadejte D0001.</span><span class="sxs-lookup"><span data-stu-id="81d9d-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="81d9d-119">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="81d9d-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="81d9d-120">Klepněte na kartu Nastavení.</span><span class="sxs-lookup"><span data-stu-id="81d9d-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="81d9d-121">V poli Skupina DPH zboží zadejte „FULL“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="81d9d-122">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="81d9d-122">Click Add line.</span></span>
10. <span data-ttu-id="81d9d-123">Do pole Číslo položky zadejte D0003.</span><span class="sxs-lookup"><span data-stu-id="81d9d-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="81d9d-124">V poli Skupina DPH zboží zadejte „RED“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="81d9d-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="81d9d-125">Click Save.</span></span>
13. <span data-ttu-id="81d9d-126">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="81d9d-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="81d9d-127">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="81d9d-127">Click Invoice.</span></span>
15. <span data-ttu-id="81d9d-128">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="81d9d-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="81d9d-129">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="81d9d-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="81d9d-130">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="81d9d-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="81d9d-131">V poli Datum faktury nastavte datum a čas na „01/11/2016“ .</span><span class="sxs-lookup"><span data-stu-id="81d9d-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="81d9d-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d9d-132">Click OK.</span></span>
20. <span data-ttu-id="81d9d-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d9d-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="81d9d-134">Převod interní obchodních transakcí do souhrnného hlášení pro EU</span><span class="sxs-lookup"><span data-stu-id="81d9d-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="81d9d-135">Přejděte na Daně > Deklarace > Zahraniční obchod > Souhrnné hlášení EU.</span><span class="sxs-lookup"><span data-stu-id="81d9d-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="81d9d-136">Klepněte na položku Převod.</span><span class="sxs-lookup"><span data-stu-id="81d9d-136">Click Transfer.</span></span>
3. <span data-ttu-id="81d9d-137">K převodu transakcí zboží vyberte v poli Zboží možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="81d9d-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="81d9d-138">K převodu servisních transakcí vyberte v poli Servis možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="81d9d-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="81d9d-139">Můžete také nastavit další filtry interní obchodních transakcí k převodu.</span><span class="sxs-lookup"><span data-stu-id="81d9d-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="81d9d-140">Klepněte na položku Převod.</span><span class="sxs-lookup"><span data-stu-id="81d9d-140">Click Transfer.</span></span>
    * <span data-ttu-id="81d9d-141">Ověřte, zda byly interní transakce prodeje úspěšně přeneseny do souhrnného hlášení EU.</span><span class="sxs-lookup"><span data-stu-id="81d9d-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="81d9d-142">Generování sestavy souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="81d9d-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="81d9d-143">Klepněte na Sestavování.</span><span class="sxs-lookup"><span data-stu-id="81d9d-143">Click Reporting.</span></span>
2. <span data-ttu-id="81d9d-144">V poli Období vykazování vyberte „Měsíční“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="81d9d-145">V poli Datum od nastavte datum a čas na „01/01/2016“ .</span><span class="sxs-lookup"><span data-stu-id="81d9d-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="81d9d-146">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="81d9d-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="81d9d-147">Vyberte možnost Ano v poli Generovat sestavu.</span><span class="sxs-lookup"><span data-stu-id="81d9d-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="81d9d-148">V poli Název souboru zadejte „EUSalesList“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="81d9d-149">V poli Název souboru sestavy zadejte „EUSalesList“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="81d9d-150">Do pole ID registrace souhrnného hlášení EU zadejte „123“.</span><span class="sxs-lookup"><span data-stu-id="81d9d-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="81d9d-151">Toto pole je k dispozici jen pro Německo.</span><span class="sxs-lookup"><span data-stu-id="81d9d-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="81d9d-152">Můžete také nastavit další filtry interní obchodních transakcí k převodu pro zahrnutí v sestavě.</span><span class="sxs-lookup"><span data-stu-id="81d9d-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="81d9d-153">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d9d-153">Click OK.</span></span>
    * <span data-ttu-id="81d9d-154">Ověřte, že se zobrazí místní podokno pro potvrzení, že soubor a kontrolní sestava jsou stahovány.</span><span class="sxs-lookup"><span data-stu-id="81d9d-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="81d9d-155">Označit řádky souhrnného hlášení EU jako Ohlášeno</span><span class="sxs-lookup"><span data-stu-id="81d9d-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="81d9d-156">Klepněte na položku Označit.</span><span class="sxs-lookup"><span data-stu-id="81d9d-156">Click Mark.</span></span>
2. <span data-ttu-id="81d9d-157">Klepněte na Označit jako ohlášené.</span><span class="sxs-lookup"><span data-stu-id="81d9d-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="81d9d-158">V seznamu vyberte řádek pro pole Datum fakturace.</span><span class="sxs-lookup"><span data-stu-id="81d9d-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="81d9d-159">Zadejte hodnotu „01/01/2016…01/31/2016“ do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="81d9d-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="81d9d-160">V seznamu vyberte řádek pro pole Stav vykazování.</span><span class="sxs-lookup"><span data-stu-id="81d9d-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="81d9d-161">Vyberte volbu „Zahrnuto“ v poli Kritérium.</span><span class="sxs-lookup"><span data-stu-id="81d9d-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="81d9d-162">Můžete také nastavit další filtry interní obchodních transakcí k převodu pro označení jako Hlášeno.</span><span class="sxs-lookup"><span data-stu-id="81d9d-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="81d9d-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d9d-163">Click OK.</span></span>
8. <span data-ttu-id="81d9d-164">Vyberte volbu „Hlášeno“ v poli Výběr.</span><span class="sxs-lookup"><span data-stu-id="81d9d-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="81d9d-165">Označit řádky souhrnného hlášení EU jako Uzavřeno</span><span class="sxs-lookup"><span data-stu-id="81d9d-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="81d9d-166">Klepněte na položku Označit.</span><span class="sxs-lookup"><span data-stu-id="81d9d-166">Click Mark.</span></span>
2. <span data-ttu-id="81d9d-167">Klepněte na Označit jako uzavřené.</span><span class="sxs-lookup"><span data-stu-id="81d9d-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="81d9d-168">V seznamu označte řádek pro pole Datum fakturace.</span><span class="sxs-lookup"><span data-stu-id="81d9d-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="81d9d-169">Zadejte hodnotu „01/01/2016…01/31/2016“ do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="81d9d-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="81d9d-170">V seznamu označte řádek pro pole Stav vykazování.</span><span class="sxs-lookup"><span data-stu-id="81d9d-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="81d9d-171">Vyberte volbu „Hlášeno“ v poli Kritérium.</span><span class="sxs-lookup"><span data-stu-id="81d9d-171">In the Criteria field, select 'Reported'.</span></span>
    * <span data-ttu-id="81d9d-172">Můžete také nastavit další filtry interní obchodních transakcí k převodu pro označení jako Uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="81d9d-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="81d9d-173">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d9d-173">Click OK.</span></span>
8. <span data-ttu-id="81d9d-174">Vyberte volbu „Uzavřeno“ v poli Výběr.</span><span class="sxs-lookup"><span data-stu-id="81d9d-174">In the Selection field, select 'Closed'.</span></span>

