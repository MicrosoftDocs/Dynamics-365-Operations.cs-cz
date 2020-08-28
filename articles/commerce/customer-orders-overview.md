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
ms.openlocfilehash: 87d1217204e0c5cb22f567793b043bf399ca5685
ms.sourcegitcommit: b07434f2bd6db67d8dd712f096329acc902751ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699362"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="64ff4-105">Objednávky zákazníka v Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="64ff4-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64ff4-106">Toto téma obsahuje informace o objednávkách odběratele v Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="64ff4-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="64ff4-107">Objednávky odběratele jsou označovány také jako speciální objednávky.</span><span class="sxs-lookup"><span data-stu-id="64ff4-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="64ff4-108">Téma obsahuje diskuzi o souvisejících parametrech a transakčních tocích.</span><span class="sxs-lookup"><span data-stu-id="64ff4-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="64ff4-109">Ve světě omni-channel commerce celá řada maloobchodních prodejců poskytuje možnost objednávek odběratele neboli speciálních objednávek, aby splnili různé požadavky týkající se produktu a plnění.</span><span class="sxs-lookup"><span data-stu-id="64ff4-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="64ff4-110">Zde jsou některé typické scénáře:</span><span class="sxs-lookup"><span data-stu-id="64ff4-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="64ff4-111">Zákazník chce, aby produkty byly doručeny k určitému datu na konkrétní adresu.</span><span class="sxs-lookup"><span data-stu-id="64ff4-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="64ff4-112">Zákazník chce vyzvednout výrobky ve skladu nebo z místa, které se liší od skladu nebo místa, kde zákazník tyto produkty zakoupil.</span><span class="sxs-lookup"><span data-stu-id="64ff4-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="64ff4-113">Zákazník chce, aby zakoupené produkty vyzvedl někdo jiný.</span><span class="sxs-lookup"><span data-stu-id="64ff4-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="64ff4-114">Maloobchodní prodejci také používají objednávky odběratele pro minimalizaci ztrát prodeje, které by jinak výpadky zásob mohly způsobit, protože zboží lze doručit nebo vyzvednout v jiném čase nebo na jiném místě.</span><span class="sxs-lookup"><span data-stu-id="64ff4-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="64ff4-115">Nastavení objednávek odběratele</span><span class="sxs-lookup"><span data-stu-id="64ff4-115">Set up customer orders</span></span>

<span data-ttu-id="64ff4-116">Zde jsou některé parametry, které lze nastavit na stránce **Parametry Commerce** za účelem definování způsobu plnění objednávek odběratele:</span><span class="sxs-lookup"><span data-stu-id="64ff4-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="64ff4-117">**Výchozí procento zálohy** – Zadejte částku, kterou musí zákazník zaplatit jako zálohu před tím, než může objednávku potvrdit.</span><span class="sxs-lookup"><span data-stu-id="64ff4-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="64ff4-118">Výchozí minimální záloha se vypočítá jako procento z hodnoty objednávky.</span><span class="sxs-lookup"><span data-stu-id="64ff4-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="64ff4-119">V závislosti na oprávněních může zaměstnanec obchodu přepsat částku pomocí možnosti **Přepsání zálohy**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="64ff4-120">**Procento poplatku za zrušení** – Pokud se použije poplatek při zrušení objednávky odběratele, určete výši tohoto poplatku.</span><span class="sxs-lookup"><span data-stu-id="64ff4-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="64ff4-121">**Kód poplatku za zrušení** – Pokud bude použit poplatek při zrušení objednávky odběratele, tento poplatek se projeví v kódu poplatku na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="64ff4-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="64ff4-122">Použijte tento parametr k definování kódu poplatku za zrušení.</span><span class="sxs-lookup"><span data-stu-id="64ff4-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="64ff4-123">**Kód dopravného** – Prodejce můžete účtovat dodatečný poplatek za dodání zboží zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="64ff4-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="64ff4-124">Výše tohoto dopravného se odrazí v kódu nákladů na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="64ff4-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="64ff4-125">Tento parametr použijte k mapování kódu dopravného na dopravné v objednávce odběratele.</span><span class="sxs-lookup"><span data-stu-id="64ff4-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="64ff4-126">**Refundovat dopravné** – Určete, zda je dopravné přidružené k objednávce odběratele vratné.</span><span class="sxs-lookup"><span data-stu-id="64ff4-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="64ff4-127">**Maximální částka bez schválení** -Pokud je dopravné vratné, určete maximální částku refundace dopravného napříč vratkami.</span><span class="sxs-lookup"><span data-stu-id="64ff4-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="64ff4-128">Pokud dojde k překročení této částky, bude vyžadováno přepsání manažerem, aby bylo možné pokračovat s refundací.</span><span class="sxs-lookup"><span data-stu-id="64ff4-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="64ff4-129">Pro následující scénáře může refundace dopravného překročit původně zaplacenou částku:</span><span class="sxs-lookup"><span data-stu-id="64ff4-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="64ff4-130">Poplatky jsou použity na úrovni záhlaví prodejní objednávky a při vrácení určitého množství produktu nelze určit maximální refundaci dopravného povolenou pro produkty a množství takovým způsobem, který by byl použitelný pro všechny zákazníky.</span><span class="sxs-lookup"><span data-stu-id="64ff4-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="64ff4-131">Pro každou instanci expedice vzniká dopravné.</span><span class="sxs-lookup"><span data-stu-id="64ff4-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="64ff4-132">Pokud zákazník vrací produkty vícekrát a zásady prodejce určují, že prodejce ponese náklady dopravného za vrácení, budou poplatky za dopravné vratek vyšší než skutečné dopravné.</span><span class="sxs-lookup"><span data-stu-id="64ff4-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    
- <span data-ttu-id="64ff4-133">**Chování při výpočtu daně** - **Přepočítat** je výchozí a tradiční nastavení způsobu přepočtu daní při importu objednávky do administrativní podpory.</span><span class="sxs-lookup"><span data-stu-id="64ff4-133">**Tax calculation behavior** - **Recalculate** is the default and traditional setting for how taxes are recalculated when the order is imported into the back office.</span></span> <span data-ttu-id="64ff4-134">**Nepočítat** zakáže přepočet daně až do doby, než bude příkaz upraven v administrativní podpoře, když je přepočet proveden.</span><span class="sxs-lookup"><span data-stu-id="64ff4-134">**Don't recalculate** disables tax recalculation until or unless the order is edited in the back office, when recalculation is triggered.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="64ff4-135">Toky transakcí pro objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="64ff4-135">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="64ff4-136">Vytvoření objednávky odběratele v Modern POS</span><span class="sxs-lookup"><span data-stu-id="64ff4-136">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="64ff4-137">Přidejte zákazníka do transakce</span><span class="sxs-lookup"><span data-stu-id="64ff4-137">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="64ff4-138">Přidejte produkty do košíku.</span><span class="sxs-lookup"><span data-stu-id="64ff4-138">Add products to the cart.</span></span>
3. <span data-ttu-id="64ff4-139">Klikněte na tlačítko **Vytvořit objednávku odběratele** a potom vyberte typ objednávky.</span><span class="sxs-lookup"><span data-stu-id="64ff4-139">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="64ff4-140">Typ objednávky může být buď **Objednávka odběratele** nebo **Nabídka**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-140">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="64ff4-141">Klikněte na tlačítko **Odeslat vybrané** nebo **Odeslat vše** k dodání výrobků na adresu z účtu odběratele, zadejte požadované datum expedice a určete dopravné.</span><span class="sxs-lookup"><span data-stu-id="64ff4-141">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="64ff4-142">Klikněte na tlačítko **Vyzvednout vybrané** nebo **Vyzvednout vše** pro výběr produktů, které bude být vyzvednuty z aktuálního skladu nebo jiného skladu v určité datum.</span><span class="sxs-lookup"><span data-stu-id="64ff4-142">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="64ff4-143">Pokud je požadována záloha, vyberte částku zálohy.</span><span class="sxs-lookup"><span data-stu-id="64ff4-143">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="64ff4-144">Úprava existující objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="64ff4-144">Edit an existing customer order</span></span>

1. <span data-ttu-id="64ff4-145">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-145">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="64ff4-146">Vyhledejte a vyberte objednávku, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="64ff4-146">Find and select the order to edit.</span></span> <span data-ttu-id="64ff4-147">V dolní části stránky klikněte na **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-147">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="64ff4-148">Vyzvednutí objednávky</span><span class="sxs-lookup"><span data-stu-id="64ff4-148">Pick up an order</span></span>

1. <span data-ttu-id="64ff4-149">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="64ff4-150">Vyberte objednávku, která má být vyzvednuta.</span><span class="sxs-lookup"><span data-stu-id="64ff4-150">Select the order to pick up.</span></span> <span data-ttu-id="64ff4-151">V dolní části stránky klikněte na **Výdej a balení**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-151">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="64ff4-152">Klikněte na **Vyzvednutí**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-152">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="64ff4-153">Zrušení objednávky</span><span class="sxs-lookup"><span data-stu-id="64ff4-153">Cancel an order</span></span>

1. <span data-ttu-id="64ff4-154">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-154">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="64ff4-155">Vyberte objednávku, kterou chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="64ff4-155">Select the order to cancel.</span></span> <span data-ttu-id="64ff4-156">V dolní části stránky klikněte na **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-156">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="64ff4-157">Vytvořit vratku</span><span class="sxs-lookup"><span data-stu-id="64ff4-157">Create a return order</span></span>

1. <span data-ttu-id="64ff4-158">Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="64ff4-159">Vyberte objednávku k vrácení, vyberte fakturu pro objednávku a poté vyberte produktovou řadu pro zboží k vrácení.</span><span class="sxs-lookup"><span data-stu-id="64ff4-159">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="64ff4-160">V dolní části stránky klikněte na **Vratka**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-160">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="64ff4-161">Asynchronní tok transakcí pro objednávky odběratele</span><span class="sxs-lookup"><span data-stu-id="64ff4-161">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="64ff4-162">Objednávky odběratele lze vytvořit z klienta pokladního místa buď v synchronním nebo asynchronním režimu.</span><span class="sxs-lookup"><span data-stu-id="64ff4-162">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="64ff4-163">Povolení vytvoření objednávky odběratele v asynchronním režimu</span><span class="sxs-lookup"><span data-stu-id="64ff4-163">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="64ff4-164">Klikněte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Profil POS** &gt; **Profily POS** &gt; **Funkční profily**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-164">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="64ff4-165">Na pevné záložce **Obecné** nastavte možnost **Vytvořit objednávku odběratele v asynchronním režimu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="64ff4-165">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="64ff4-166">Když je možnost **Vytvořit objednávku odběratele v asynchronním režimu** nastavena na **Ano**, objednávky odběratelů se vždy vytvářejí v asynchronním režimu, i když je k dispozici služba Retail Transaction Service (RTS).</span><span class="sxs-lookup"><span data-stu-id="64ff4-166">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="64ff4-167">Pokud nastavíte tuto možnost na **Ne**, objednávky odběratelů jsou vždy vytvářeny v synchronním režimu pomocí služby RTS.</span><span class="sxs-lookup"><span data-stu-id="64ff4-167">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="64ff4-168">Při vytváření objednávek odběratelů v asynchronním režimu jsou objednávky vyžádány a vloženy do aplikace Commerce pomocí úloh na vyžádání (úlohy P).</span><span class="sxs-lookup"><span data-stu-id="64ff4-168">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="64ff4-169">Odpovídající prodejní objednávky se vytvoří buď při manuálním spuštění možnosti **Synchronizovat objednávky** nebo pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="64ff4-169">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64ff4-170">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="64ff4-170">Additional resources</span></span>

[<span data-ttu-id="64ff4-171">Hybridní objednávky zákazníka</span><span class="sxs-lookup"><span data-stu-id="64ff4-171">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
