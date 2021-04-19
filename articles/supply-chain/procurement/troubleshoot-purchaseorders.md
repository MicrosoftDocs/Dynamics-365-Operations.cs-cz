---
title: Řešení problému s nákupními objednávkami
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s nákupními objednávkami.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 964f31c21faae6a947174f637624aca917881297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841448"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="0f6ba-103">Řešení problému s nákupními objednávkami</span><span class="sxs-lookup"><span data-stu-id="0f6ba-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="0f6ba-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s nákupními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="0f6ba-105">Akce může být dokončena až po úplném distribuci čísla řádku.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="0f6ba-106">K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="0f6ba-107">Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="0f6ba-108">Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="0f6ba-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="0f6ba-109">Když se nákupní objednávky importují prostřednictvím správy dat, čísla řádků nákupní objednávky nenásledují přírůstek definovaný v systémových parametrech.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f6ba-110">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-110">Issue description</span></span>

<span data-ttu-id="0f6ba-111">Ve výchozím nastavení automaticky generovaná čísla řádků pro řádky nákupní objednávky, které se importují prostřednictvím datové entity *Řádky nákupní objednávky V2* nepoužívají přírůstek čísla řádku systému, který je zadán v systémových parametrech.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="0f6ba-112">Pokud ručně vytvoříte nákupní objednávku a přidáte řádky prostřednictvím uživatelského rozhraní, budou čísla řádků správně zvýšena.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="0f6ba-113">Pokud však používáte Data management framework (DMF), nejsou správně zvýšena.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="0f6ba-114">K tomuto problému dochází, protože při importu řádků pomocí DMF, pokud čísla řádků již nejsou přiřazena v importované entitě, systém používá k jejich přiřazení metodu DMF.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="0f6ba-115">Tato metoda vždy zvyšuje čísla řádků o jedno.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="0f6ba-116">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-116">Issue workaround</span></span>

<span data-ttu-id="0f6ba-117">Ujistěte se, že požadovaná čísla řádků jsou již uvedena v polích čísel řádků datové entity při importu řádků nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="0f6ba-118">V tomto případě DMF nepřepíše čísla řádků.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="0f6ba-119">Z účtu faktury není vyplněna výchozí daňová skupina a výchozí platební sleva.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="0f6ba-120">Pokud používáte účet faktury, který se liší od účtu zákazníka, nevyplní se při vytvoření nákupní objednávky výchozí daňová skupina a výchozí platební sleva z účtu faktury.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="0f6ba-121">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-121">This behavior is by design.</span></span> <span data-ttu-id="0f6ba-122">Výchozí hodnoty pro daňovou skupinu, platební slevy a další informace o cenách jsou založeny na účtu zákazníka, nikoli na účtu faktury.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="0f6ba-123">Během potvrzení nákupní objednávky se mi zobrazí chyba „Odkaz na objekt není nastaven“ nebo během zaúčtování faktury dodavatele dojde k výjimce „Byla vyvolána výjimka cílem vyvolání“.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="0f6ba-124">K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="0f6ba-125">Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="0f6ba-126">Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="0f6ba-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="0f6ba-127">Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f6ba-128">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-128">Issue description</span></span>

<span data-ttu-id="0f6ba-129">Zobrazí se následující chyba: „Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.“</span><span class="sxs-lookup"><span data-stu-id="0f6ba-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f6ba-130">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-130">Issue resolution</span></span>

<span data-ttu-id="0f6ba-131">K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="0f6ba-132">Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="0f6ba-133">Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="0f6ba-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="0f6ba-134">Mohu zobrazit pouze nákupní objednávky, které jsem vytvořil/a?</span><span class="sxs-lookup"><span data-stu-id="0f6ba-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="0f6ba-135">Tato funkce není aktuálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="0f6ba-136">Mohu rezervovat zásoby a vytvořit transakce proti registrovaným zásobám na nákupní objednávce?</span><span class="sxs-lookup"><span data-stu-id="0f6ba-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f6ba-137">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-137">Issue description</span></span>

<span data-ttu-id="0f6ba-138">I když jsou položky ve stavu *Registrováno* na nákupní objednávce, zásoby si stále můžete rezervovat.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="0f6ba-139">Jinými slovy můžete vytvářet transakce proti registrovaným zásobám.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="0f6ba-140">Reprodukování problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-140">Reproduce the issue</span></span>

<span data-ttu-id="0f6ba-141">Následující postup ukazuje jeden způsob, jak reprodukovat problém.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="0f6ba-142">Vytvoření nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-142">Create a purchase order.</span></span>
2. <span data-ttu-id="0f6ba-143">Zaregistrujte řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="0f6ba-144">Všimněte si, že můžete generovat rezervace nebo transakce proti registrovaným zásobám.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f6ba-145">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-145">Issue resolution</span></span>

<span data-ttu-id="0f6ba-146">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-146">This behavior is by design.</span></span> <span data-ttu-id="0f6ba-147">Očekává se, že registrované položky fyzicky dorazily do skladu nebo zásob a že jsou proto k dispozici k rezervaci.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="0f6ba-148">Nákupní objednávky neodrážejí jazykové nastavení právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f6ba-149">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-149">Issue description</span></span>

<span data-ttu-id="0f6ba-150">Název produktu na nákupní objednávce se zobrazuje v jazyce systému místo v jazyce nastaveném pro právnickou osobu, kde byla vytvořena nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="0f6ba-151">Reprodukování problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-151">Reproduce the issue</span></span>

<span data-ttu-id="0f6ba-152">Následující postup ukazuje jeden způsob, jak reprodukovat problém.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="0f6ba-153">Nastavte jazyk systému na *EN-US* (americká angličtina).</span><span class="sxs-lookup"><span data-stu-id="0f6ba-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="0f6ba-154">Ujistěte se, že existuje produkt, kde jsou udržovány jazyky *EN-US* a *DE* (němčina) pro překlady názvu produktu.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="0f6ba-155">Změňte jazyk právnické osoby na *DE*.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="0f6ba-156">V právnické osobě, kde je jako jazyk nastaveno *DE*, vytvořte nákupní objednávku, která zahrnuje produkt.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="0f6ba-157">Všimněte si, že název produktu je stále zobrazen v americké angličtině (systémový jazyk).</span><span class="sxs-lookup"><span data-stu-id="0f6ba-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f6ba-158">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-158">Issue resolution</span></span>

<span data-ttu-id="0f6ba-159">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-159">This behavior is by design.</span></span> <span data-ttu-id="0f6ba-160">Na nákupních objednávkách je produkt vždy zobrazen v systémovém jazyce.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="0f6ba-161">Při vytvoření deníku potvrzení se použije jazyk nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="0f6ba-162">Seznam schválených dodavatelů podle entity produktu neumožňuje změnu data účinnosti.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f6ba-163">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-163">Issue description</span></span>

<span data-ttu-id="0f6ba-164">Produkt má schváleného dodavatele, který má například datum účinnosti 11. ledna 2018 (*01/11/2018*) a datum vypršení platnosti *Nikdy*.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="0f6ba-165">Pokud se pokusíte změnit datum účinnosti na 10. ledna 2018 (*01/10/2018*) nebo 12. ledna 2018 (*01/12/2018*), zobrazí se následující chyba:</span><span class="sxs-lookup"><span data-stu-id="0f6ba-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="0f6ba-166">Nelze vytvořit záznam v seznamu schválených dodavatelů (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="0f6ba-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="0f6ba-167">Hodnota „Vypršení platnosti“ musí být větší nebo rovna hodnotě „Datum platnosti“.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f6ba-168">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-168">Issue resolution</span></span>

<span data-ttu-id="0f6ba-169">Můžete prodloužit pouze období, pro které je dodavatel schválen.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="0f6ba-170">Platí následující pravidla:</span><span class="sxs-lookup"><span data-stu-id="0f6ba-170">The following rules apply:</span></span>

- <span data-ttu-id="0f6ba-171">Chcete-li změnit datum účinnosti tak, aby bylo dřívější než kterýkoli z existujících záznamů (období) pro dodavatele položky, datum vypršení platnosti nového období musí být před všemi daty vypršení platnosti v existujících záznamech.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="0f6ba-172">Chcete-li změnit datum vypršení platnosti tak, aby bylo pozdější než kterékoli z existujících období, datum platnosti musí být po posledním datu vypršení platnosti v jakémkoli existujícím záznamu.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="0f6ba-173">Chcete-li snížit celkovou dobu, po kterou je dodavatel schválen, musíte odstranit nebo upravit existující záznamy.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="0f6ba-174">Případně můžete použít přepínač **zkrátit** během importu.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="0f6ba-175">Tento přepínač odstraní všechny existující záznamy v tabulce pro schválené dodavatele podle položek.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="0f6ba-176">Pro příklad scénáře, který je popsán v popisu problému, kde má záznam datum účinnosti *01/11/2018* a datum vypršení platnosti *Nikdy*, můžete importovat nový záznam, který má datum účinnosti *01/10/2018* a datum vypršení platnosti *Nikdy*.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="0f6ba-177">Nelze však zkrátit období tak, aby bylo datum účinnosti aktualizováno na *01/12/2018* prostřednictvím správy dat.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="0f6ba-178">Tuto změnu musíte provést prostřednictvím uživatelského rozhraní.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="0f6ba-179">Po změně dodací adresy v záhlaví nákupní objednávky se název dodávky nesynchronizuje.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0f6ba-180">Popis problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-180">Issue description</span></span>

<span data-ttu-id="0f6ba-181">Adresa v záhlaví nákupní objednávky se aktualizuje na adresu, která není doručovací adresou.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="0f6ba-182">I když je adresa na nákupní objednávce aktualizována, název dodávky není aktualizován na základě aktualizované adresy.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0f6ba-183">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="0f6ba-183">Issue resolution</span></span>

<span data-ttu-id="0f6ba-184">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-184">This behavior is by design.</span></span> <span data-ttu-id="0f6ba-185">Vybraná adresa musí být klasifikována jako doručovací adresa.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="0f6ba-186">Jinak se název doručení neaktualizuje na základě vybrané adresy.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="0f6ba-187">Mohu najít uživatele, který zrušil nákupní objednávku?</span><span class="sxs-lookup"><span data-stu-id="0f6ba-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="0f6ba-188">Tyto informace jsou sledovány pouze v případě, že je u objednávky možné provádět změny.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="0f6ba-189">Pokud používáte správu změn, můžete vidět, kdo změnu (zrušení) odeslal a kdo ji schválil.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]