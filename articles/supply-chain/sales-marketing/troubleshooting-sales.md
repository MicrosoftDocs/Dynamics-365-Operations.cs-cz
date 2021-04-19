---
title: Řešení problémů s prodejními objednávkami
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními objednávkami.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824719"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="36fa2-103">Řešení problémů s prodejními objednávkami</span><span class="sxs-lookup"><span data-stu-id="36fa2-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="36fa2-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="36fa2-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="36fa2-105">Daňové informace se neaktualizují, pokud změním umístění v záhlaví prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="36fa2-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="36fa2-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-106">Issue description</span></span>

<span data-ttu-id="36fa2-107">Pokud se pracoviště, sklad nebo adresa dodání změní buď v záhlaví prodejní objednávky, nebo na úrovni řádku, informace o dani případu se pro řádky automaticky neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="36fa2-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="36fa2-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-108">Issue resolution</span></span>

<span data-ttu-id="36fa2-109">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="36fa2-109">This behavior is by design.</span></span> <span data-ttu-id="36fa2-110">K problému dochází, protože ani doručovací adresa, pracoviště a sklad se na úrovni řádku automaticky nezmění.</span><span class="sxs-lookup"><span data-stu-id="36fa2-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="36fa2-111">Musíte je aktualizovat ručně.</span><span class="sxs-lookup"><span data-stu-id="36fa2-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="36fa2-112">Pokud existují dvě obchodní smlouvy pro stejné období nebo překrývající se období, je vždy vybrán stejný řádek smlouvy.</span><span class="sxs-lookup"><span data-stu-id="36fa2-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="36fa2-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-113">Issue description</span></span>

<span data-ttu-id="36fa2-114">Pokud jsou definovány dvě obchodní smlouvy pro stejné období nebo překrývající se období, zdá se, že stejná obchodní smlouva je vybrána pokaždé, když vytvoříte řádky prodejní objednávky, které obsahují tyto položky.</span><span class="sxs-lookup"><span data-stu-id="36fa2-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="36fa2-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-115">Issue resolution</span></span>

<span data-ttu-id="36fa2-116">Pokud pro dané datum existuje více než jedna obchodní smlouva, je vždy vybrána obchodní smlouva, která má nejnižší cenu.</span><span class="sxs-lookup"><span data-stu-id="36fa2-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="36fa2-117">Další informace získáte stažením následujícího dokumentu whitepaper: [Obchodní smlouvy v Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="36fa2-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="36fa2-118">Mohu propojit nákupní objednávku s prodejní objednávkou, abych splnil/a poptávku?</span><span class="sxs-lookup"><span data-stu-id="36fa2-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="36fa2-119">Můžete vytvořit nákupní objednávku z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="36fa2-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="36fa2-120">Další informace najdete ve [Vytvoření nákupní objednávky z prodejní objednávky](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="36fa2-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="36fa2-121">Nemohu zrušit ani odstranit vratku nebo prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="36fa2-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="36fa2-122">Můžete zrušit pouze prodejní objednávky a vratky, které jsou ve stavu *Vytvořeno*.</span><span class="sxs-lookup"><span data-stu-id="36fa2-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="36fa2-123">Další informace naleznete v tématu [Zrušení vratky](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="36fa2-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="36fa2-124">Při pokusu o zrušení prodejní objednávky se zobrazí chyba „Nelze odebrat rezervace, protože existuje práce, která závisí na rezervacích“.</span><span class="sxs-lookup"><span data-stu-id="36fa2-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="36fa2-125">Kód chyby: WAX4661</span><span class="sxs-lookup"><span data-stu-id="36fa2-125">Error code: WAX4661</span></span>

<span data-ttu-id="36fa2-126">Pokud je práce přidružená k prodejní objednávce, nemůžete zrušit prodejní objednávku, dokud nebude práce zrušena a stornována.</span><span class="sxs-lookup"><span data-stu-id="36fa2-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="36fa2-127">Tento požadavek platí, i když je práce přidružená k prodejní objednávce uzavřena.</span><span class="sxs-lookup"><span data-stu-id="36fa2-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="36fa2-128">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="36fa2-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="36fa2-129">Zrušte práci a vložte zásoby zpět na požadované místo.</span><span class="sxs-lookup"><span data-stu-id="36fa2-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="36fa2-130">Přejděte na příslušné vytížení prodejní objednávky a vyberte buď **Snížit vyskladněné množství** na řádku vytížení nebo **Stornovat práci** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="36fa2-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="36fa2-131">Práce má nyní stav *Zrušeno* a automaticky se vytvoří a zpracuje nová práce přesunu zásob, aby se zásoby vrátily zpět na místo, které bylo popsáno v době zrušení.</span><span class="sxs-lookup"><span data-stu-id="36fa2-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="36fa2-132">Odstraňte vytížení.</span><span class="sxs-lookup"><span data-stu-id="36fa2-132">Delete the load.</span></span> <span data-ttu-id="36fa2-133">Dodávka je také odstraněna.</span><span class="sxs-lookup"><span data-stu-id="36fa2-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="36fa2-134">Nyní byste měli být schopni přejít k prodejní objednávce a zrušit ji.</span><span class="sxs-lookup"><span data-stu-id="36fa2-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="36fa2-135">Nemohu zrušit mezipodnikovou nákupní objednávku, která je propojena s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="36fa2-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="36fa2-136">Popis problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-136">Issue description</span></span>

<span data-ttu-id="36fa2-137">Pokud se pokusíte zrušit mezipodnikovou nákupní objednávku, která je propojena s prodejní objednávkou, může se zobrazit následující chybová zpráva: „Množství nelze snížit, protože zbývající množství aktualizace mění znaménko.“</span><span class="sxs-lookup"><span data-stu-id="36fa2-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="36fa2-138">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-138">Issue resolution</span></span>

<span data-ttu-id="36fa2-139">Tento problém byl opraven v Microsoft Dynamics 365 Supply Chain Management verze 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="36fa2-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="36fa2-140">V této a novějších verzích můžete nyní zrušit mezipodnikovou nákupní objednávku, která je propojena s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="36fa2-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="36fa2-141">Mohu obnovit fakturovanou prodejní objednávku, která byla odstraněna?</span><span class="sxs-lookup"><span data-stu-id="36fa2-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="36fa2-142">Popis problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-142">Issue description</span></span>

<span data-ttu-id="36fa2-143">Fakturovaná prodejní objednávka byla omylem odstraněna a chcete ji obnovit nebo zobrazit její podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="36fa2-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="36fa2-144">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="36fa2-144">Issue resolution</span></span>

<span data-ttu-id="36fa2-145">Pokud byla odstraněná prodejní objednávka již fakturována, přejděte na **Účet zákazníka \> Transakce \> Původní dokument \> Zobrazit podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="36fa2-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="36fa2-146">Najděte fakturu, kterou hledáte, a jejím výběrem zobrazíte její podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="36fa2-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="36fa2-147">Mezi tyto podrobnosti patří odkaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="36fa2-147">These details include the sales order reference.</span></span> <span data-ttu-id="36fa2-148">Na této stránce byste také měli mít přístup k podrobnostem prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="36fa2-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="36fa2-149">Termín záhlaví prodejní objednávky nelze najít v datové entitě SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="36fa2-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="36fa2-150">Pole termínu neexistuje v entitě *SalesOrderHeaderV2Entity*.</span><span class="sxs-lookup"><span data-stu-id="36fa2-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="36fa2-151">Musím odstranit osamocené záznamy prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="36fa2-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="36fa2-152">Chcete-li vyčistit osamocené záznamy prodejní objednávky, spusťte periodickou úlohu *Odstranění prodejní objednávky* přechodem na jedno z následujících míst:</span><span class="sxs-lookup"><span data-stu-id="36fa2-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="36fa2-153">Prodej a marketing \> Periodické úkoly \> Vyčistit \> Odstranit prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="36fa2-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="36fa2-154">Retail a Commerce \> Retail a Commerce IT \> Vyčistit \> Odstranit prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="36fa2-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="36fa2-155">Existuje způsob, jak vypočítat provize z faktur, které již byly zaúčtovány?</span><span class="sxs-lookup"><span data-stu-id="36fa2-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="36fa2-156">Supply Chain Management aktuálně nepodporuje výpočet provizí za zaúčtované faktury.</span><span class="sxs-lookup"><span data-stu-id="36fa2-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="36fa2-157">V mezipodnikovém procesu není položka sady podporována.</span><span class="sxs-lookup"><span data-stu-id="36fa2-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="36fa2-158">Položka sady není pro nákupní objednávku k dispozici, protože pokud prozkoumáte řádky prodejní objednávky pro položku sady, zjistíte, že množství je *0* (nula) a stav je *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="36fa2-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="36fa2-159">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="36fa2-159">This behavior is by design.</span></span> <span data-ttu-id="36fa2-160">Prodejní objednávka nakupuje pouze komponenty položky sady.</span><span class="sxs-lookup"><span data-stu-id="36fa2-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="36fa2-161">Nezakupuje samotnou položku sady.</span><span class="sxs-lookup"><span data-stu-id="36fa2-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="36fa2-162">Pokud si musíte koupit sadu, zvažte, zda ji musíte označit jako položku sady, protože tato funkce je navržena pro scénáře rozpoznávání výnosů.</span><span class="sxs-lookup"><span data-stu-id="36fa2-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="36fa2-163">Další informace o položkách sady naleznete v tématu [Sady](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="36fa2-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]