---
title: Objednávky zákazníka v Modern POS (MPOS)
description: Toto téma obsahuje informace o objednávkách odběratele v Modern POS (MPOS). Objednávky odběratele jsou označovány také jako speciální objednávky. Téma obsahuje diskuzi o souvisejících parametrech a transakčních tocích.
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a6fdc7b8d7ad65c9e4bf1d3b932b62918dea6e77
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710252"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="1b26a-105">Objednávky zákazníka v Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="1b26a-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b26a-106">Toto téma obsahuje informace o objednávkách odběratele v Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="1b26a-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="1b26a-107">Objednávky odběratele jsou označovány také jako speciální objednávky.</span><span class="sxs-lookup"><span data-stu-id="1b26a-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="1b26a-108">Téma obsahuje diskuzi o souvisejících parametrech a transakčních tocích.</span><span class="sxs-lookup"><span data-stu-id="1b26a-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="1b26a-109">Ve světě omni-channel commerce celá řada maloobchodních prodejců poskytuje možnost objednávek odběratele neboli speciálních objednávek, aby splnili různé požadavky týkající se produktu a plnění.</span><span class="sxs-lookup"><span data-stu-id="1b26a-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="1b26a-110">Zde jsou některé typické scénáře:</span><span class="sxs-lookup"><span data-stu-id="1b26a-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="1b26a-111">Zákazník chce, aby produkty byly doručeny k určitému datu na konkrétní adresu.</span><span class="sxs-lookup"><span data-stu-id="1b26a-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="1b26a-112">Zákazník chce vyzvednout výrobky ve skladu nebo z místa, které se liší od skladu nebo místa, kde zákazník tyto produkty zakoupil.</span><span class="sxs-lookup"><span data-stu-id="1b26a-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="1b26a-113">Zákazník chce, aby zakoupené produkty vyzvedl někdo jiný.</span><span class="sxs-lookup"><span data-stu-id="1b26a-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="1b26a-114">Maloobchodní prodejci také používají objednávky odběratele pro minimalizaci ztrát prodeje, které by jinak výpadky zásob mohly způsobit, protože zboží lze doručit nebo vyzvednout v jiném čase nebo na jiném místě.</span><span class="sxs-lookup"><span data-stu-id="1b26a-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="1b26a-115">Nastavení objednávek odběratele</span><span class="sxs-lookup"><span data-stu-id="1b26a-115">Set up customer orders</span></span>

<span data-ttu-id="1b26a-116">Zde jsou některé parametry, které lze nastavit na stránce **Parametry Commerce** za účelem definování způsobu plnění objednávek odběratele:</span><span class="sxs-lookup"><span data-stu-id="1b26a-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="1b26a-117">**Výchozí procento zálohy** – Zadejte částku, kterou musí zákazník zaplatit jako zálohu před tím, než může objednávku potvrdit.</span><span class="sxs-lookup"><span data-stu-id="1b26a-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="1b26a-118">Výchozí minimální záloha se vypočítá jako procento z hodnoty objednávky.</span><span class="sxs-lookup"><span data-stu-id="1b26a-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="1b26a-119">V závislosti na oprávněních může zaměstnanec obchodu přepsat částku pomocí možnosti **Přepsání zálohy**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="1b26a-120">**Procento poplatku za zrušení** – Pokud se použije poplatek při zrušení objednávky odběratele, určete výši tohoto poplatku.</span><span class="sxs-lookup"><span data-stu-id="1b26a-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="1b26a-121">**Kód poplatku za zrušení** – Pokud bude použit poplatek při zrušení objednávky odběratele, tento poplatek se projeví v kódu poplatku na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="1b26a-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="1b26a-122">Použijte tento parametr k definování kódu poplatku za zrušení.</span><span class="sxs-lookup"><span data-stu-id="1b26a-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="1b26a-123">**Kód dopravného** – Prodejce můžete účtovat dodatečný poplatek za dodání zboží zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="1b26a-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="1b26a-124">Výše tohoto dopravného se odrazí v kódu nákladů na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="1b26a-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="1b26a-125">Tento parametr použijte k mapování kódu dopravného na dopravné v objednávce odběratele.</span><span class="sxs-lookup"><span data-stu-id="1b26a-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="1b26a-126">**Refundovat dopravné** – Určete, zda je dopravné přidružené k objednávce odběratele vratné.</span><span class="sxs-lookup"><span data-stu-id="1b26a-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="1b26a-127">**Maximální částka bez schválení** -Pokud je dopravné vratné, určete maximální částku refundace dopravného napříč vratkami.</span><span class="sxs-lookup"><span data-stu-id="1b26a-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="1b26a-128">Pokud dojde k překročení této částky, bude vyžadováno přepsání manažerem, aby bylo možné pokračovat s refundací.</span><span class="sxs-lookup"><span data-stu-id="1b26a-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="1b26a-129">Pro následující scénáře může refundace dopravného překročit původně zaplacenou částku:</span><span class="sxs-lookup"><span data-stu-id="1b26a-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="1b26a-130">Poplatky jsou použity na úrovni záhlaví prodejní objednávky a při vrácení určitého množství produktu nelze určit maximální refundaci dopravného povolenou pro produkty a množství takovým způsobem, který by byl použitelný pro všechny zákazníky.</span><span class="sxs-lookup"><span data-stu-id="1b26a-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="1b26a-131">Pro každou instanci expedice vzniká dopravné.</span><span class="sxs-lookup"><span data-stu-id="1b26a-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="1b26a-132">Pokud zákazník vrací produkty vícekrát a zásady prodejce určují, že prodejce ponese náklady dopravného za vrácení, budou poplatky za dopravné vratek vyšší než skutečné dopravné.</span><span class="sxs-lookup"><span data-stu-id="1b26a-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    

## <a name="disable-option-to-pay-later"></a><span data-ttu-id="1b26a-133">Zákaz možnost platit později</span><span class="sxs-lookup"><span data-stu-id="1b26a-133">Disable option to pay later</span></span>

<span data-ttu-id="1b26a-134">V aplikaci Commerce verze 10.0.12 a novější mohou obchodníci odebrat možnost platit později, když je na POS vytvořena objednávka zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1b26a-134">In Commerce version 10.0.12 and later, merchants can remove the option to pay later when a customer order is created at the POS.</span></span> <span data-ttu-id="1b26a-135">Chcete-li tuto možnost deaktivovat, otevřete **Funkční profil** pro kanál, ve kterém není platba později povolena, a poté vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-135">To disable the option, open the **Functionality profile** for the channel that paying later is not allowed in, and then select **Edit**.</span></span> <span data-ttu-id="1b26a-136">Na kartě **Obecné** vyberte rozevírací seznam pro **Požadovat platbu za plnění**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-136">On the **General** tab, select the dropdown for **Require payment for fulfillment**.</span></span> <span data-ttu-id="1b26a-137">Pokud platby na POS nejsou povoleny později, vyberte **Vyžaduje se karta** a vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-137">If paying later should not be allowed at the POS, select **Card required** and select **Save**.</span></span> <span data-ttu-id="1b26a-138">Spusťte plán distribuce **1070** k synchronizování této změny s kanálem.</span><span class="sxs-lookup"><span data-stu-id="1b26a-138">Run the **1070** distribution schedule to synchronize this change to the channel.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="1b26a-139">Toky transakcí pro objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="1b26a-139">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="1b26a-140">Vytvoření objednávky odběratele v Modern POS</span><span class="sxs-lookup"><span data-stu-id="1b26a-140">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="1b26a-141">Přidejte zákazníka do transakce</span><span class="sxs-lookup"><span data-stu-id="1b26a-141">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="1b26a-142">Přidejte produkty do košíku.</span><span class="sxs-lookup"><span data-stu-id="1b26a-142">Add products to the cart.</span></span>
3. <span data-ttu-id="1b26a-143">Klikněte na tlačítko **Vytvořit objednávku odběratele** a potom vyberte typ objednávky.</span><span class="sxs-lookup"><span data-stu-id="1b26a-143">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="1b26a-144">Typ objednávky může být buď **Objednávka odběratele** nebo **Nabídka**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-144">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="1b26a-145">Klikněte na tlačítko **Odeslat vybrané** nebo **Odeslat vše** k dodání výrobků na adresu z účtu odběratele, zadejte požadované datum expedice a určete dopravné.</span><span class="sxs-lookup"><span data-stu-id="1b26a-145">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="1b26a-146">Klikněte na tlačítko **Vyzvednout vybrané** nebo **Vyzvednout vše** pro výběr produktů, které bude být vyzvednuty z aktuálního skladu nebo jiného skladu v určité datum.</span><span class="sxs-lookup"><span data-stu-id="1b26a-146">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="1b26a-147">Pokud je požadována záloha, vyberte částku zálohy.</span><span class="sxs-lookup"><span data-stu-id="1b26a-147">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="1b26a-148">Úprava existující objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="1b26a-148">Edit an existing customer order</span></span>

1. <span data-ttu-id="1b26a-149">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="1b26a-150">Vyhledejte a vyberte objednávku, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="1b26a-150">Find and select the order to edit.</span></span> <span data-ttu-id="1b26a-151">V dolní části stránky klikněte na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-151">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="1b26a-152">Vyzvednutí objednávky</span><span class="sxs-lookup"><span data-stu-id="1b26a-152">Pick up an order</span></span>

1. <span data-ttu-id="1b26a-153">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-153">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="1b26a-154">Vyberte objednávku, která má být vyzvednuta.</span><span class="sxs-lookup"><span data-stu-id="1b26a-154">Select the order to pick up.</span></span> <span data-ttu-id="1b26a-155">V dolní části stránky klikněte na **Výdej a balení**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-155">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="1b26a-156">Klikněte na **Vyzvednutí**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-156">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="1b26a-157">Zrušení objednávky</span><span class="sxs-lookup"><span data-stu-id="1b26a-157">Cancel an order</span></span>

1. <span data-ttu-id="1b26a-158">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="1b26a-159">Vyberte objednávku, kterou chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="1b26a-159">Select the order to cancel.</span></span> <span data-ttu-id="1b26a-160">V dolní části stránky klikněte na **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-160">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="1b26a-161">Vytvořit vratku</span><span class="sxs-lookup"><span data-stu-id="1b26a-161">Create a return order</span></span>

1. <span data-ttu-id="1b26a-162">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-162">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="1b26a-163">Vyberte objednávku k vrácení, vyberte fakturu pro objednávku a poté vyberte produktovou řadu pro zboží k vrácení.</span><span class="sxs-lookup"><span data-stu-id="1b26a-163">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="1b26a-164">V dolní části stránky klikněte na **Vratka**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-164">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="1b26a-165">Asynchronní tok transakcí pro objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="1b26a-165">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="1b26a-166">Objednávky odběratele lze vytvořit z klienta pokladního místa buď v synchronním nebo asynchronním režimu.</span><span class="sxs-lookup"><span data-stu-id="1b26a-166">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="1b26a-167">Povolení vytvoření objednávky odběratele v asynchronním režimu</span><span class="sxs-lookup"><span data-stu-id="1b26a-167">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="1b26a-168">Klikněte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Profil POS** &gt; **Profily POS** &gt; **Funkční profily**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-168">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="1b26a-169">Na pevné záložce **Obecné** nastavte možnost **Vytvořit objednávku odběratele v asynchronním režimu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1b26a-169">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="1b26a-170">Když je možnost **Vytvořit objednávku odběratele v asynchronním režimu** nastavena na **Ano**, objednávky odběratelů se vždy vytvářejí v asynchronním režimu, i když je k dispozici služba Retail Transaction Service (RTS).</span><span class="sxs-lookup"><span data-stu-id="1b26a-170">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="1b26a-171">Pokud nastavíte tuto možnost na **Ne**, objednávky odběratelů jsou vždy vytvářeny v synchronním režimu pomocí služby RTS.</span><span class="sxs-lookup"><span data-stu-id="1b26a-171">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="1b26a-172">Při vytváření objednávek odběratelů v asynchronním režimu jsou objednávky vyžádány a vloženy do aplikace Commerce pomocí úloh na vyžádání (úlohy P).</span><span class="sxs-lookup"><span data-stu-id="1b26a-172">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="1b26a-173">Odpovídající prodejní objednávky se vytvoří buď při manuálním spuštění možnosti **Synchronizovat objednávky** nebo pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="1b26a-173">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b26a-174">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1b26a-174">Additional resources</span></span>

[<span data-ttu-id="1b26a-175">Hybridní objednávky zákazníka</span><span class="sxs-lookup"><span data-stu-id="1b26a-175">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
