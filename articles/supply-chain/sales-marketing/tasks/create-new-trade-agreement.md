---
title: Vytvoření nové obchodní smlouvy
description: Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 592b3d0265a3be92a5a823c6aabdd40b4e3f0a27
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919934"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="7d0bd-103">Vytvoření nové obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="7d0bd-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d0bd-104">Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="7d0bd-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7d0bd-106">Při použití vlastních dat před zahájením tohoto průvodce ověřte, že existuje název deníku obchodních smluv, kde je výchozí vztah je nastaven na „Cena (prodej)“.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>

## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="7d0bd-107">Vytvoření a zaúčtování nového deníku obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="7d0bd-107">Create and post a new trade agreement journal</span></span>

1. <span data-ttu-id="7d0bd-108">Přejděte do **navigačního podokna > Moduly > Prodej a marketing > Ceny a slevy > Deníky smluv o obchodu**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="7d0bd-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-109">Click **New**.</span></span>
3. <span data-ttu-id="7d0bd-110">V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7d0bd-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7d0bd-112">V **podokně akcí** klikněte na možnost **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="7d0bd-113">V poli **Kód účtu** vyberte možnost Tabulka.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="7d0bd-114">V tomto příkladu aktualizujete cenu pro určitého odběratele, což znamená, že je nutné vybrat tabulku.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="7d0bd-115">Pokud byste aktualizovali katalogovou cenu produktu, vybrali byste Vše, aby nová cena platila pro všechny odběratele.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="7d0bd-116">Pokud byste používali různé ceny v různých segmentech odběratelů, vybrali byste možnost Skupina.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="7d0bd-117">Chcete-li vybrat skupinu, musíte nastavit možnost Cenové skupiny odběratele.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="7d0bd-118">V poli **Výběr účtu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7d0bd-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="7d0bd-120">V poli **Kód položky** vyberte položku Tabulka.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="7d0bd-121">Při zadávání typu obchodní smlouvy Cena (prodej) je nutné vybrat pouze „Tabulka“ v poli **Kód položky**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="7d0bd-122">Důvodem je skutečnost, že cena je absolutní hodnota a nesmí být stejná pro všechny produkty nebo skupinu produktů.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="7d0bd-123">V poli **Vztah položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7d0bd-124">V seznamu vyberte produkt, který chcete do smlouvy zahrnout.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="7d0bd-125">Poznamenejte produkt, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="7d0bd-126">V poli **Od** zadejte minimální množství.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="7d0bd-127">Pokud odběratel musí objednávat minimální množství, je třeba zde zadat množství, jinak nebude mít na novou cenu nárok.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="7d0bd-128">Zadáním hodnoty do pole **Do** určete maximální množství, nad které nebude cena ve smlouvě platit.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="7d0bd-129">Pokud nabízíte ceny a slevy založené na několika množstevních kategoriích, zadejte každou množstevní kategorii jako pár minimálního a maximálního množství do polí **Od** a **Do**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="7d0bd-130">Zadejte cenu do pole **Částka v měně.**</span><span class="sxs-lookup"><span data-stu-id="7d0bd-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="7d0bd-131">V části **Detaily** zadejte do pole **Od data** datum, od kterého bude tato smlouva platná.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="7d0bd-132">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-132">Click **Save**.</span></span>
16. <span data-ttu-id="7d0bd-133">Klikněte na tlačítko **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-133">Click **Validate**.</span></span>
17. <span data-ttu-id="7d0bd-134">Klikněte na možnost **Ověřit vybrané řádky.**</span><span class="sxs-lookup"><span data-stu-id="7d0bd-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="7d0bd-135">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-135">Click **OK**.</span></span>
19. <span data-ttu-id="7d0bd-136">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-136">Click **Post**.</span></span>
20. <span data-ttu-id="7d0bd-137">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="7d0bd-138">Zobrazení obchodních smluv pro produkt</span><span class="sxs-lookup"><span data-stu-id="7d0bd-138">View trade agreements for a product</span></span>

1. <span data-ttu-id="7d0bd-139">Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="7d0bd-140">V seznamu najděte a vyberte produkt, jehož cenu jste právě aktualizovali.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="7d0bd-141">V **podokně akcí** klikněte na možnost **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="7d0bd-142">Klikněte na možnost **Zobrazit obchodní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="7d0bd-143">Zkontrolujte podrobnosti obchodní smlouvy o cenách, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-143">Review the details of the price trade agreement you have just created.</span></span>

5. <span data-ttu-id="7d0bd-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d0bd-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="7d0bd-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="7d0bd-146">Dokument Whitepaper</span><span class="sxs-lookup"><span data-stu-id="7d0bd-146">Whitepaper</span></span>

<span data-ttu-id="7d0bd-147">Chcete-li získat další informace, stáhněte si následující dokument whitepaper (napsaný na podporu AX2012, ale stále platí pro Dynamics 365 Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7d0bd-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>

- [<span data-ttu-id="7d0bd-148">Obchod. smlouvy</span><span class="sxs-lookup"><span data-stu-id="7d0bd-148">Trade agreements</span></span>](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="7d0bd-149">Blogy komunity</span><span class="sxs-lookup"><span data-stu-id="7d0bd-149">Community blogs</span></span>

- [<span data-ttu-id="7d0bd-150">Prodejní ceny v Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d0bd-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]