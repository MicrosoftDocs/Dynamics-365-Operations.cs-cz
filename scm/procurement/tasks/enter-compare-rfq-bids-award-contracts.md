--- 
title: "Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy"
description: "Tento postup popisuje, jak zadat odpovědi na požadavek na nabídku, hodnocení a porovnání nabídek, a poté přijmout nabídku některého z dodavatelů."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="97eb1-103">Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy</span><span class="sxs-lookup"><span data-stu-id="97eb1-103">Enter and compare RFQ bids and award contracts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97eb1-104">Tento postup popisuje, jak zadat odpovědi na požadavek na nabídku, hodnocení a porovnání nabídek, a poté přijmout nabídku některého z dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="97eb1-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="97eb1-105">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="97eb1-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="97eb1-106">Než začnete, musíte mít požadavek na nabídku se dvěma řádky, které byly odeslány nejméně dvěma dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="97eb1-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="97eb1-107">Pro vytvoření je nezbytným předpokladem vytvoření postupu "Vytvořit požadavek na nabídku".</span><span class="sxs-lookup"><span data-stu-id="97eb1-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="97eb1-108">Je nutné nastavit kritéria hodnocení před spuštěním tohoto procesu.</span><span class="sxs-lookup"><span data-stu-id="97eb1-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="97eb1-109">Zadání odpovědi od dodavatele</span><span class="sxs-lookup"><span data-stu-id="97eb1-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="97eb1-110">Přejděte na Zásobování a zdroje > Požadavky na nabídky > Všechny požadavky na nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="97eb1-111">Vyberte požadavek na nabídku, který má stav Odesláno, a klepněte na odkaz u čísla případu s požadavkem na nabídku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="97eb1-112">Požadavek na nabídku byl odeslán nejméně 2 dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="97eb1-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="97eb1-113">Klepnutím na záhlaví přejděte na seznam dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="97eb1-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="97eb1-114">Vyberte dodavatele, pro kterého chcete zadat odpověď na požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="97eb1-115">Klikněte na Zadat odpověď.</span><span class="sxs-lookup"><span data-stu-id="97eb1-115">Click Enter reply.</span></span>
6. <span data-ttu-id="97eb1-116">V podokně akcí klikněte na možnost Odpovědět.</span><span class="sxs-lookup"><span data-stu-id="97eb1-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="97eb1-117">Klikněte na Kopírovat data do odpovědi.</span><span class="sxs-lookup"><span data-stu-id="97eb1-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="97eb1-118">Touto akcí zkopírujete vybraná data, jako například množství z případu požadavku na nabídku do odpovědi na požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="97eb1-119">Také můžete tuto akci vynechat a vyplnit všechna pole s odpovědí ručně při úpravách odpovědi.</span><span class="sxs-lookup"><span data-stu-id="97eb1-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="97eb1-120">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="97eb1-120">Click Edit.</span></span>
9. <span data-ttu-id="97eb1-121">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="97eb1-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="97eb1-122">Vyberte jiný řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="97eb1-123">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="97eb1-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="97eb1-124">Hodnocení nabídky</span><span class="sxs-lookup"><span data-stu-id="97eb1-124">Score the bid</span></span>
1. <span data-ttu-id="97eb1-125">Klepnutím na záhlaví přejděte na hodnocení nabídek.</span><span class="sxs-lookup"><span data-stu-id="97eb1-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="97eb1-126">Rozbalte oddíl Hodnocení nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="97eb1-127">V poli Hodnocení zadejte číslo jednoho z kritérií hodnocení.</span><span class="sxs-lookup"><span data-stu-id="97eb1-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="97eb1-128">Pokud umístíte kurzor myši na některé z kritérií hodnocení, zobrazí se popisek pole s rozsahem požadovaných bodů.</span><span class="sxs-lookup"><span data-stu-id="97eb1-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="97eb1-129">V této ukázce můžete přidat číslo do libovolného kritéria v rozmezí 1 až 5.</span><span class="sxs-lookup"><span data-stu-id="97eb1-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="97eb1-130">Vyberte jiné kritérium hodnocení.</span><span class="sxs-lookup"><span data-stu-id="97eb1-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="97eb1-131">V poli Hodnocení zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="97eb1-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="97eb1-132">Rozbalte oddíl Dotazníky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="97eb1-133">Má-li případ požadavku na nabídku dotazník, který byl odeslán dodavatelům, můžete zadat jejich odpovědi v části dotazníku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="97eb1-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="97eb1-135">Zadání odpovědi pro jiného dodavatele</span><span class="sxs-lookup"><span data-stu-id="97eb1-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="97eb1-136">Vyberte dalšího dodavatele vymazáním dodavatele, pro kterého jste právě zadali odpověď a vyberte řádek u dalšího dodavatele.</span><span class="sxs-lookup"><span data-stu-id="97eb1-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="97eb1-137">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="97eb1-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="97eb1-138">Klikněte na Zadat odpověď.</span><span class="sxs-lookup"><span data-stu-id="97eb1-138">Click Enter reply.</span></span>
4. <span data-ttu-id="97eb1-139">Klikněte na Kopírovat data do odpovědi.</span><span class="sxs-lookup"><span data-stu-id="97eb1-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="97eb1-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="97eb1-140">Click Edit.</span></span>
6. <span data-ttu-id="97eb1-141">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="97eb1-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="97eb1-142">Vyberte jiný řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="97eb1-143">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="97eb1-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="97eb1-144">Hodnocení druhé nabídky</span><span class="sxs-lookup"><span data-stu-id="97eb1-144">Score the second bid</span></span>
1. <span data-ttu-id="97eb1-145">Klepnutím na záhlaví přejděte na hodnocení nabídek.</span><span class="sxs-lookup"><span data-stu-id="97eb1-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="97eb1-146">V poli Hodnocení zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="97eb1-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="97eb1-147">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="97eb1-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="97eb1-148">V poli Hodnocení zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="97eb1-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="97eb1-149">Porovnání odpovědí</span><span class="sxs-lookup"><span data-stu-id="97eb1-149">Compare the replies</span></span>
1. <span data-ttu-id="97eb1-150">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="97eb1-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="97eb1-151">Klikněte na Porovnat odpovědi.</span><span class="sxs-lookup"><span data-stu-id="97eb1-151">Click Compare replies.</span></span>
3. <span data-ttu-id="97eb1-152">Do pole Rozsah zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="97eb1-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="97eb1-153">Na této stránce se zobrazí nabídky se záhlavím a řádky a celkovým hodnocením na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="97eb1-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="97eb1-154">Porovnat řádky můžete seřazením v mřížce tak, aby byly porovnatelné řádky vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="97eb1-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="97eb1-155">Informace zahrnují také následující:  Množství: množství nabízené dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="97eb1-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="97eb1-156">Toto množství se nemusí rovnat množství zadanému v RFQ.</span><span class="sxs-lookup"><span data-stu-id="97eb1-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="97eb1-157">Čistá částka: cena nabízená dodavatelem po odečtení všech slev za položky na řádku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="97eb1-158">Odchylka: počet dnů, o které se datum dodání v záhlaví nabídky nebo řádku liší od požadovaného data dodání v záhlaví RFQ nebo řádku RFQ.</span><span class="sxs-lookup"><span data-stu-id="97eb1-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="97eb1-159">Pro každou nabídku můžete zadat hodnocení.</span><span class="sxs-lookup"><span data-stu-id="97eb1-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="97eb1-160">Vyberte řádek záhlaví pro jinou objednávku, kterou chcete ohodnotit.</span><span class="sxs-lookup"><span data-stu-id="97eb1-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="97eb1-161">Do pole Rozsah zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="97eb1-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="97eb1-162">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="97eb1-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="97eb1-163">Odmítnutí nabídky</span><span class="sxs-lookup"><span data-stu-id="97eb1-163">Reject a bid</span></span>
1. <span data-ttu-id="97eb1-164">Vyberte řádek záhlaví pro objednávku, kterou chcete odmítnout.</span><span class="sxs-lookup"><span data-stu-id="97eb1-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="97eb1-165">V každém okamžiku můžete je možné pouze přijetí, odmítnutí nebo návrat jedné nabídky nebo řádků v rámci nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="97eb1-166">Vyberte Zaškrtnout políčko.</span><span class="sxs-lookup"><span data-stu-id="97eb1-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="97eb1-167">Pokud označíte pole Označit v záhlaví nabídky, budou označeny také všechny řádky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="97eb1-168">Můžete se také rozhodnout označit dílčí sadu řádků v rámci nabídky a odmítnout je nebo je přijmout.</span><span class="sxs-lookup"><span data-stu-id="97eb1-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="97eb1-169">Lze potvrdit nabídku jednoho dodavatele pro některé řádky v požadavku na nabídku a potom udělit jiné řádky požadavku na nabídku jinému dodavateli. Musíte tak ale učinit ve 2 krocích vždy po jedné nabídce.</span><span class="sxs-lookup"><span data-stu-id="97eb1-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="97eb1-170">Pokud existují řádky alternativy, můžete pouze přijmout buď původní řádek nabídky nebo jeho alternativu, ne však obojí.</span><span class="sxs-lookup"><span data-stu-id="97eb1-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="97eb1-171">Klikněte na tlačítko Zamítnout.</span><span class="sxs-lookup"><span data-stu-id="97eb1-171">Click Reject.</span></span>
4. <span data-ttu-id="97eb1-172">Klepnutím na možnost Parametry otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="97eb1-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="97eb1-173">V poli Odmítnutí důvodu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="97eb1-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="97eb1-174">Důvod pro odmítnutí bude uložen v odpovědi.</span><span class="sxs-lookup"><span data-stu-id="97eb1-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="97eb1-175">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="97eb1-175">Click OK.</span></span>
7. <span data-ttu-id="97eb1-176">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="97eb1-176">Click OK.</span></span>
8. <span data-ttu-id="97eb1-177">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-177">Close the page.</span></span>
9. <span data-ttu-id="97eb1-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-178">Close the page.</span></span>
10. <span data-ttu-id="97eb1-179">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="97eb1-180">Přijetí nabídky</span><span class="sxs-lookup"><span data-stu-id="97eb1-180">Accept a bid</span></span>
1. <span data-ttu-id="97eb1-181">Vyberte nabídku, kterou chcete přijmout, a klepněte na odkaz v poli Požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="97eb1-182">V podokně akcí klikněte na možnost Odpovědět.</span><span class="sxs-lookup"><span data-stu-id="97eb1-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="97eb1-183">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="97eb1-183">Click Accept.</span></span>
    * <span data-ttu-id="97eb1-184">Pokud jste označili určité řádky a jiné nikoli, akce přijetí bude obsahovat pouze označené řádky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="97eb1-185">Pokud chcete přijmout všechny řádky v nabídce, řádky není třeba označit.</span><span class="sxs-lookup"><span data-stu-id="97eb1-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="97eb1-186">Klepnutím na možnost Parametry otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="97eb1-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="97eb1-187">Tímto způsobem lze zaznamenat důvod pro přijetí nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="97eb1-188">Důvod bude uložen v nabídce.</span><span class="sxs-lookup"><span data-stu-id="97eb1-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="97eb1-189">V poli Potvrzení důvodu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="97eb1-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="97eb1-190">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="97eb1-190">Click OK.</span></span>
7. <span data-ttu-id="97eb1-191">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="97eb1-191">Click OK.</span></span>
    * <span data-ttu-id="97eb1-192">Po klepnutí na tlačítko OK vytvoříte nákupní objednávku na základě řádků, které jsou zahrnuty v přijetí požadavku na nabídku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="97eb1-193">Pokud existují jiné nabídky, které nebyly zpracovány (přijaty, odmítnuty nebo vráceny), systém zobrazí výzvu k odmítnutí zbývajících nabídek.</span><span class="sxs-lookup"><span data-stu-id="97eb1-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="97eb1-194">Zobrazení nákupní objednávky, která byla vytvořena</span><span class="sxs-lookup"><span data-stu-id="97eb1-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="97eb1-195">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="97eb1-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="97eb1-196">Klikněte na Nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-196">Click Purchase order.</span></span>
    * <span data-ttu-id="97eb1-197">Zde je vidět nákupní objednávka, která byla vygenerována po přijetí nabídky.</span><span class="sxs-lookup"><span data-stu-id="97eb1-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="97eb1-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-198">Close the page.</span></span>
4. <span data-ttu-id="97eb1-199">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-199">Close the page.</span></span>
5. <span data-ttu-id="97eb1-200">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-200">Close the page.</span></span>
6. <span data-ttu-id="97eb1-201">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97eb1-201">Close the page.</span></span>


