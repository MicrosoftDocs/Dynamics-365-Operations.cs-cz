---
title: Řešení problémů s příjemkami a fakturací produktů
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s příjemkami a fakturací produktů.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424238"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="e3d0e-103">Řešení problémů s příjemkami a fakturací produktů</span><span class="sxs-lookup"><span data-stu-id="e3d0e-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="e3d0e-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s příjemkami a fakturací produktů.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="e3d0e-105">Nemohu zaúčtovat více než jednu fakturu za řádek nákupní objednávky, který obsahuje položky založené na kategoriích.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="e3d0e-106">Množství je povinné, pokud chcete zaúčtovat faktury.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="e3d0e-107">Pokud tedy bylo celé množství řádku fakturováno pouze za částečnou částku, nebudete moci zbývající částku fakturovat na jiné faktuře.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="e3d0e-108">Během potvrzení nákupní objednávky se mi zobrazí chyba „Odkaz na objekt není nastaven“ nebo během zaúčtování faktury dodavatele dojde k výjimce „Byla vyvolána výjimka cílem vyvolání“.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="e3d0e-109">K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="e3d0e-110">Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="e3d0e-111">Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="e3d0e-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="e3d0e-112">Nemohu konsolidovat více příjemek produktu do jedné nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="e3d0e-113">Nelze sloučit více příjemek produktu do jedné nákupní objednávky, pokud mají různé řádky příjemek produktu různá data zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="e3d0e-114">V dřívějších verzích Microsoft Dynamics 365 Supply Chain Management byla konsolidace v této situaci povolena.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="e3d0e-115">Tento postup je však náchylný k chybám.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-115">However, the practice is prone to error.</span></span> <span data-ttu-id="e3d0e-116">Datum zaúčtování na řádcích nákupní objednávky, které jsou vytvořeny, by se nemělo lišit od účetního data na řádcích příjemky produktu, ze kterých byly tyto řádky nákupní objednávky vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="e3d0e-117">(Datum účtování na řádcích nákupní objednávky odpovídá datu účtování v záhlaví nákupní objednávky.) Konsolidace více příjemek produktu do jedné nákupní objednávky proto již není povolena.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="e3d0e-118">Datum účtování se používá například pro rozpočtové rezervace a břemeno.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="e3d0e-119">Proto by mělo být uchováno během přechodu z příjemky produktu na nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="e3d0e-120">Když jsou zrušeny příjemky produktu, lze transakce zaúčtovat na pozastavený účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e3d0e-121">Popis problému</span><span class="sxs-lookup"><span data-stu-id="e3d0e-121">Issue description</span></span>

<span data-ttu-id="e3d0e-122">Pokud je příjemka produktu zrušena, systém umožňuje zaúčtování transakcí na pozastavené účty hlavní knihy, i když jsou pozastaveny hlavní účty.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="e3d0e-123">Reprodukování problému</span><span class="sxs-lookup"><span data-stu-id="e3d0e-123">Reproduce the issue</span></span>

<span data-ttu-id="e3d0e-124">Následující postup ukazuje jeden způsob, jak reprodukovat problém.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="e3d0e-125">Na stránce **Parametry závazků** na kartě **Obecné** se ujistěte, že možnost **Zaúčtovat příjemku produktu do hlavní knihy** je nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="e3d0e-126">Vytvořte nákupní objednávku a přidejte řádek objednávky s množstvím *1 000* pro produkt.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="e3d0e-127">Potvrďte nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="e3d0e-128">Zaúčtujte příjemku produktu a zkontrolujte doklady.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="e3d0e-129">Pozastavte příslušné hlavní účty, *200140* a *140200*.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="e3d0e-130">Zrušte zaúčtovanou příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="e3d0e-131">Všimněte si, že transakce lze zaúčtovat na pozastavené účty hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e3d0e-132">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="e3d0e-132">Issue resolution</span></span>

<span data-ttu-id="e3d0e-133">Transakce lze zaúčtovat na pozastavené účty hlavní knihy, když jsou zrušeny příjemky produktu, protože toto chování umožňuje správné zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="e3d0e-134">Číslo dokladu příjemky produktu je spotřebováno, i když se během příjmu produktu nevygeneruje žádný finanční doklad.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="e3d0e-135">Pokud je možnost **Časově rozlišit pasiva na příjemce produktu** nastavena na *Ne* pro skupinu modelů položek, nedojde k účtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="e3d0e-136">Fyzická událost však bude zaznamenána pro účely účtování v dílčí hlavní knize a tato událost vyžaduje číslo dokladu.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="e3d0e-137">Toto číslo dokladu je číslo dokladu, na které se odkazuje v transakcích zásob.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="e3d0e-138">Doporučujeme nastavit možnost **Časově rozlišit pasiva na příjemce produktu** na *Ano*, jak je popsáno v následujícím příspěvku na blogu: [Zaúčtování vedlejších nákladů v době příjemky produktu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="e3d0e-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="e3d0e-139">Nastavení možnosti Zaúčtovat na účet poplatků v hlavní knize není zapnuto.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e3d0e-140">Popis problému</span><span class="sxs-lookup"><span data-stu-id="e3d0e-140">Issue description</span></span>

<span data-ttu-id="e3d0e-141">K tomuto problému dochází, když je nákupní objednávka fakturována, pokud je možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano* na kartě **Faktura** stránky **Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="e3d0e-142">Reprodukování problému</span><span class="sxs-lookup"><span data-stu-id="e3d0e-142">Reproduce the issue</span></span>

<span data-ttu-id="e3d0e-143">Následující postup ukazuje jeden způsob, jak reprodukovat problém.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="e3d0e-144">Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="e3d0e-145">Na kartě **Faktura** nastavte možnost **Zaúčtovat na účet poplatků v hlavní knize** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="e3d0e-146">Přejděte na **Řízení zásob \> Nastavit \> Zaúčtování \> Zaúčtování**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="e3d0e-147">Na kartě **Nákupní objednávka** se ujistěte, že jste odstranili všechny řádky v nákupních výdajích za produkt.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="e3d0e-148">Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="e3d0e-149">Vytvoření nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-149">Create a purchase order.</span></span> <span data-ttu-id="e3d0e-150">V poli **Účet dodavatele** vyberte *1001 kancelářské potřeby Acme*.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="e3d0e-151">Přidejte řádek nákupní objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="e3d0e-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="e3d0e-152">**Číslo položky:** *Laserový projektor D0011*</span><span class="sxs-lookup"><span data-stu-id="e3d0e-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="e3d0e-153">**Lokalita:** *1*</span><span class="sxs-lookup"><span data-stu-id="e3d0e-153">**Site:** *1*</span></span>
    - <span data-ttu-id="e3d0e-154">**Sklad:** *11*</span><span class="sxs-lookup"><span data-stu-id="e3d0e-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="e3d0e-155">**Množství:** *4*</span><span class="sxs-lookup"><span data-stu-id="e3d0e-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="e3d0e-156">V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="e3d0e-157">V podokně Akce na kartě **Přijmout** ve skupině **Generovat** zvolte **Příjemka produktu**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="e3d0e-158">V dialogovém okně **Zaúčtování příjemky produktu** v poli **Příjemka produktu** zadejte libovolné číslo a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="e3d0e-159">V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="e3d0e-160">V poli **Číslo** zadejte libovolné číslo jako číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="e3d0e-161">Aktualizujte stav párování a zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="e3d0e-162">Všimněte si, že nyní při generování faktury z nákupní objednávky se zobrazí následující chyba: „Číslo účtu pro typ transakce nákupního výdaje za produkt neexistuje.“</span><span class="sxs-lookup"><span data-stu-id="e3d0e-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e3d0e-163">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="e3d0e-163">Issue resolution</span></span>

<span data-ttu-id="e3d0e-164">To závisí na nastavení parametrů pro faktury a skupiny faktur.</span><span class="sxs-lookup"><span data-stu-id="e3d0e-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="e3d0e-165">Další informace najdete v následujícím příspěvku na blogu: [Účtování nákladů nákupu a odchylky zásob](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="e3d0e-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
