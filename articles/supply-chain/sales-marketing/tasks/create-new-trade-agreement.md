---
title: Vytvoření nové obchodní smlouvy
description: Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e49793fc7f6b3f37bafae05770d4b23d24171329
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974878"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="3e91e-103">Vytvoření nové obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="3e91e-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e91e-104">Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.</span><span class="sxs-lookup"><span data-stu-id="3e91e-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="3e91e-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="3e91e-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="3e91e-106">Při použití vlastních dat před zahájením tohoto průvodce ověřte, že existuje název deníku obchodních smluv, kde je výchozí vztah je nastaven na „Cena (prodej)“.</span><span class="sxs-lookup"><span data-stu-id="3e91e-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="3e91e-107">Vytvoření a zaúčtování nového deníku obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="3e91e-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="3e91e-108">Přejděte do **navigačního podokna > Moduly > Prodej a marketing > Ceny a slevy > Deníky smluv o obchodu**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="3e91e-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-109">Click **New**.</span></span>
3. <span data-ttu-id="3e91e-110">V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3e91e-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3e91e-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="3e91e-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3e91e-112">V **podokně akcí** klikněte na možnost **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="3e91e-113">V poli **Kód účtu** vyberte možnost Tabulka.</span><span class="sxs-lookup"><span data-stu-id="3e91e-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="3e91e-114">V tomto příkladu aktualizujete cenu pro určitého odběratele, což znamená, že je nutné vybrat tabulku.</span><span class="sxs-lookup"><span data-stu-id="3e91e-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="3e91e-115">Pokud byste aktualizovali katalogovou cenu produktu, vybrali byste Vše, aby nová cena platila pro všechny odběratele.</span><span class="sxs-lookup"><span data-stu-id="3e91e-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="3e91e-116">Pokud byste používali různé ceny v různých segmentech odběratelů, vybrali byste možnost Skupina.</span><span class="sxs-lookup"><span data-stu-id="3e91e-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="3e91e-117">Chcete-li vybrat skupinu, musíte nastavit možnost Cenové skupiny odběratele.</span><span class="sxs-lookup"><span data-stu-id="3e91e-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="3e91e-118">V poli **Výběr účtu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3e91e-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3e91e-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="3e91e-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="3e91e-120">V poli **Kód položky** vyberte položku Tabulka.</span><span class="sxs-lookup"><span data-stu-id="3e91e-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="3e91e-121">Při zadávání typu obchodní smlouvy Cena (prodej) je nutné vybrat pouze „Tabulka“ v poli **Kód položky**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="3e91e-122">Důvodem je skutečnost, že cena je absolutní hodnota a nesmí být stejná pro všechny produkty nebo skupinu produktů.</span><span class="sxs-lookup"><span data-stu-id="3e91e-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="3e91e-123">V poli **Vztah položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3e91e-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3e91e-124">V seznamu vyberte produkt, který chcete do smlouvy zahrnout.</span><span class="sxs-lookup"><span data-stu-id="3e91e-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="3e91e-125">Poznamenejte produkt, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="3e91e-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="3e91e-126">V poli **Od** zadejte minimální množství.</span><span class="sxs-lookup"><span data-stu-id="3e91e-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="3e91e-127">Pokud odběratel musí objednávat minimální množství, je třeba zde zadat množství, jinak nebude mít na novou cenu nárok.</span><span class="sxs-lookup"><span data-stu-id="3e91e-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="3e91e-128">Zadáním hodnoty do pole **Do** určete maximální množství, nad které nebude cena ve smlouvě platit.</span><span class="sxs-lookup"><span data-stu-id="3e91e-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="3e91e-129">Pokud nabízíte ceny a slevy založené na několika množstevních kategoriích, zadejte každou množstevní kategorii jako pár minimálního a maximálního množství do polí **Od** a **Do**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="3e91e-130">Zadejte cenu do pole **Částka v měně.**</span><span class="sxs-lookup"><span data-stu-id="3e91e-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="3e91e-131">V části **Detaily** zadejte do pole **Od data** datum, od kterého bude tato smlouva platná.</span><span class="sxs-lookup"><span data-stu-id="3e91e-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="3e91e-132">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-132">Click **Save**.</span></span>
16. <span data-ttu-id="3e91e-133">Klikněte na tlačítko **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-133">Click **Validate**.</span></span>
17. <span data-ttu-id="3e91e-134">Klikněte na možnost **Ověřit vybrané řádky.**</span><span class="sxs-lookup"><span data-stu-id="3e91e-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="3e91e-135">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-135">Click **OK**.</span></span>
19. <span data-ttu-id="3e91e-136">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-136">Click **Post**.</span></span>
20. <span data-ttu-id="3e91e-137">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="3e91e-138">Zobrazení obchodních smluv pro produkt</span><span class="sxs-lookup"><span data-stu-id="3e91e-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="3e91e-139">Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="3e91e-140">V seznamu najděte a vyberte produkt, jehož cenu jste právě aktualizovali.</span><span class="sxs-lookup"><span data-stu-id="3e91e-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="3e91e-141">V **podokně akcí** klikněte na možnost **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="3e91e-142">Klikněte na možnost **Zobrazit obchodní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="3e91e-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="3e91e-143">Zkontrolujte podrobnosti obchodní smlouvy o cenách, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="3e91e-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="3e91e-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3e91e-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e91e-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3e91e-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="3e91e-146">Dokument Whitepaper</span><span class="sxs-lookup"><span data-stu-id="3e91e-146">Whitepaper</span></span>
<span data-ttu-id="3e91e-147">Chcete-li získat další informace, stáhněte si následující dokument whitepaper (napsaný na podporu AX2012, ale stále platí pro Dynamics 365 Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="3e91e-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>
- [<span data-ttu-id="3e91e-148">Obchod. smlouvy</span><span class="sxs-lookup"><span data-stu-id="3e91e-148">Trade agreements</span></span>](https://mbs.microsoft.com/files/public/CS/AX2012R3/TradeagreementsinAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="3e91e-149">Blogy komunity</span><span class="sxs-lookup"><span data-stu-id="3e91e-149">Community blogs</span></span>
- [<span data-ttu-id="3e91e-150">Prodejní ceny v Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e91e-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
