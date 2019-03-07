---
title: Nákladová cena vrácení a ID vrácené šarže
description: Můžete chtít, aby se náklady na vrácené produkty rovnaly nákladům na produkty v době, kdy jste produkty prodali zákazníkovi. To lze provést pomocí **ID vrácené šarže**.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "335133"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="2d8a3-104">Nákladová cena vrácení a ID vrácené šarže</span><span class="sxs-lookup"><span data-stu-id="2d8a3-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="2d8a3-105">Náklady na produkty, které byly vráceny do zásob, se vypočítávají s použitím aktuálních nákladů produktů.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="2d8a3-106">Můžete však požadovat, aby se náklady na vrácené produkty rovnaly nákladům na produkty v době, kdy jste produkty prodali zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="2d8a3-107">To lze provést pomocí **ID vrácené šarže** na pevné záložce **Podrobnosti řádku** ve formuláři **prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="2d8a3-108">Představte si například následující příklady:</span><span class="sxs-lookup"><span data-stu-id="2d8a3-108">For example, consider the following scenario.</span></span> <span data-ttu-id="2d8a3-109">Vystavíte fakturu odběrateli.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-109">You invoice a customer.</span></span> <span data-ttu-id="2d8a3-110">Pak vám odběratel vrátí dodané produkty.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="2d8a3-111">Vrátíte produkty do zásob.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-111">You return the products to stock.</span></span> <span data-ttu-id="2d8a3-112">V takovém případě, když odběrateli účtujete vrácené produkty, jsou náklady na tyto produkty vypočteny s použitím aktuálních nákladů na produkty.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="2d8a3-113">Pokud však použijete pole **ID vrácené šarže**, jsou náklady na vracené výrobky vypočteny s použitím nákladů na faktuře původního prodeje odběrateli.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="2d8a3-114">Chcete-li použít jiné než aktuální náklady za zboží vrácené od odběratele, použijte některou z následujících metod.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="2d8a3-115">Metoda č. 1: Ručně zadejte náklady na vrácení</span><span class="sxs-lookup"><span data-stu-id="2d8a3-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="2d8a3-116">Ve výchozím nastavení při přidání položky do vratky budou položky vráceny do zásob s aktuální nákladovou cenou.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="2d8a3-117">Při určení jiné ceny nákladů vrácení postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="2d8a3-118">Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="2d8a3-119">V **podokně akcí** ve skupině **Nový** klepněte na možnost **Vratka**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="2d8a3-120">Ve formuláři **Vytvořit vratku** vyberte účet zákazníka a klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="2d8a3-121">Ve formuláři **vratka – číslo RMA: %1, %2** vyberte položku a poté zadejte záporné množství do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="2d8a3-122">Klikněte na pevnou záložku **Podrobnosti řádku**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="2d8a3-123">Na kartě **Obecné** zadejte hodnotu v poli **Upřednostňovaný kalendář**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="2d8a3-124">Tato hodnota se používá při vrácení zboží do zásob.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="2d8a3-125">Pokud nezadáte hodnotu, aktuální nákladová cena je použita při vrácení zboží do zásob.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="2d8a3-126">Metoda č. 2: Automatické generování nákladové ceny na základě řádku faktury odběratele</span><span class="sxs-lookup"><span data-stu-id="2d8a3-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="2d8a3-127">Toto je preferovaná metoda používaná k vytvoření řádků vratky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="2d8a3-128">Pokud chcete použít náklady na produkty v době prodeje produktů odběrateli, vytvořte vratku a zadejte řádku prodeje do vratky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="2d8a3-129">Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="2d8a3-130">V **podokně akcí** ve skupině **Nový** klepněte na možnost **Vratka**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="2d8a3-131">Ve formuláři **Vytvořit vratku** vyberte účet zákazníka a klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="2d8a3-132">Ve formuláři **vratka – číslo RMA: %1, %2** v **podokně akcí** klepněte na tlačítko **najít prodejní objednávku**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="2d8a3-133">Ve formuláři **najít prodejní objednávku** vyberte řádek faktury k vrácení a klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="2d8a3-134">Na pevné záložce **podrobnosti řádku** na kartě **Obecné** se v poli **ID vrácené šarže** zobrazí hodnota z původní řádky objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="2d8a3-135">V poli **náklady na vrácení** se dále zobrazí hodnot nákladů z původní řádky prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="2d8a3-136">Příklad výpočtu nákladů</span><span class="sxs-lookup"><span data-stu-id="2d8a3-136">Cost calculation example</span></span>

<span data-ttu-id="2d8a3-137">Používáte-li pole **ID vrácené šarže** na řádku objednávky k určení nákladů na vrácení, použijí se náklady řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="2d8a3-138">Pokud spustíte funkci uzávěrky nebo přepočtu skladu, náklady se upraví na řádku původní prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="2d8a3-139">Náklady řádku objednávky se automaticky nastaví tak, aby odrážely stejnou cenu za kus.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="2d8a3-140">Vytvořte a vydejte produkt s názvem test.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="2d8a3-141">Ve formuláři **uvolnění podrobností produktu** zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="2d8a3-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="2d8a3-142">Na pevné záložce **řízení nákladů** v poli **skupinu položek** vyberte skupinu **části**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="2d8a3-143">Na pevné záložce **Obecné**, v poli **Skupina modelů položky** vyberte **DEF**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="2d8a3-144">Na pevné záložce **Nákup** v poli **cena** zadejte 10,00 jako nákladovou cenu položky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="2d8a3-145">V **podokně akcí** klikněte na možnost **Skupiny dimenze**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="2d8a3-146">V poli **Skupina dimenze úložiště** vyberte **Pouze pracoviště a sklad**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="2d8a3-147">V poli **Skupina sledovací dimenze** vyberte **Žádné aktivní sledovací dimenze**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="2d8a3-148">Vytvořte nákupní objednávku pro 10 kusů zkušební položky po 6,00 za kus a potom zaúčtujte faktury pro nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="2d8a3-149">Vytvořte druhou nákupní objednávku pro 10 kusů zkušební položky po 8,00 za kus a potom zaúčtujte faktury pro nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="2d8a3-150">Zaúčtujte fakturu prodejní objednávky na prodej pěti kusů zkušební položky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="2d8a3-151">V takovém případě jsou na řádku prodejní objednávky vypočítány náklady na 35,00 (5 kusů \*7,00 průměrné náklady na úkolové práce).</span><span class="sxs-lookup"><span data-stu-id="2d8a3-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="2d8a3-152">Vytvořte novou vratku pro vybraného odběratele.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-152">Create a return order for the customer.</span></span> <span data-ttu-id="2d8a3-153">Ve formuláři **najít prodejní objednávku** vyberte řádek faktury a klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="2d8a3-154">Ve formuláři **vratka – číslo RMA: %1, %2** ověřte, že vratka je vygenerována pro vrácení testovacího zboží.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="2d8a3-155">Množství vratky je nastaveno na hodnotu -5,00.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="2d8a3-156">Pole **ID vrácené šarže** zobrazí ID šarže.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="2d8a3-157">Toto ID šarže je převzato z původní prodejní objednávky položky, která byla prodána zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="2d8a3-158">V poli **náklady na vrácení** se dále zobrazí nákladová cena z původní řádky prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="2d8a3-159">Zaregistrujte příjem vrácených položek.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="2d8a3-160">Zaúčtujte dodací list pro vrácené položky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="2d8a3-161">Zaúčtujte fakturu pro objednávku vratky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-161">Post an invoice for the return order.</span></span> <span data-ttu-id="2d8a3-162">Na stránce se seznamem **všechny prodejní objednávky** vyberte požadovanou prodejní objednávku, pro kterou je typ objednávky **vratka**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="2d8a3-163">Otevřete formulář **Skladové transakce**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="2d8a3-164">Ověřte, že je vratka účtována na 7,00 za kus pomocí hodnoty v poli **Náklady na vrácení**, za celkem 35,00 v poli **částka nákladů**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="2d8a3-165">Můžete otevřít formulář **skladové transakce** z formuláře **vratka – číslo RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="2d8a3-166">V mřížce **Řádky** klikněte na **Sklad** \> **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="2d8a3-167">V modulu Řízení zásob a skladu použijte formulář **závěrka a oprava** a spusťte formulář ke spuštění **3. závěrky**.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="2d8a3-168">Tato akce, nastaví náklady pro původní řádek prodeje, který byl vypočítán při -35,00 (5 kusů \* 7,00) k -30,00 (5 kusů \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="2d8a3-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="2d8a3-169">Je to proto, že skupina skladových modelů používá metodu první do skladu, první ze skladu (FIFO), a náklady 6,00 za kus z první nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="2d8a3-170">Kromě toho tato akce upraví náklady na vrácení řádku prodeje tak, aby odpovídal ceně za kus v původním řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="2d8a3-171">Proto náklady řádku vrácenky budou upraveny z 35,00 na 30,00.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




