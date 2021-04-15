---
title: Použití větší slevy, než je vypočítaná, pro platbu dodavatele
description: Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře. K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810239"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="a4f8a-104">Použití větší slevy, než je vypočítaná, pro platbu dodavatele</span><span class="sxs-lookup"><span data-stu-id="a4f8a-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4f8a-105">Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="a4f8a-106">K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="a4f8a-107">Dodavatel 3051 umožňuje společnosti Fabrikam přijmout platební slevu 4 %, pokud je faktura splacena do 7 dní.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="a4f8a-108">Dne 29. dubna je zadána faktura na 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="a4f8a-109">Dodavatel umožňuje April využít slevu 60,00 namísto výchozí slevy 40,00, která je k dispozici pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="a4f8a-110">April zaznamená jednorázovou platbu pomocí deníku plateb závazků.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="a4f8a-111">Zadá platby dodavatele a otevře stránku **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="a4f8a-112">Označí fakturu a změní hodnotu v poli **Částka platební slevy** na **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="a4f8a-113">Označit</span><span class="sxs-lookup"><span data-stu-id="a4f8a-113">Mark</span></span>     | <span data-ttu-id="a4f8a-114">Použít platební slevu</span><span class="sxs-lookup"><span data-stu-id="a4f8a-114">Use cash discount</span></span> | <span data-ttu-id="a4f8a-115">Doklad</span><span class="sxs-lookup"><span data-stu-id="a4f8a-115">Voucher</span></span>   | <span data-ttu-id="a4f8a-116">Účet</span><span class="sxs-lookup"><span data-stu-id="a4f8a-116">Account</span></span> | <span data-ttu-id="a4f8a-117">Datum</span><span class="sxs-lookup"><span data-stu-id="a4f8a-117">Date</span></span>      | <span data-ttu-id="a4f8a-118">Datum splatnosti</span><span class="sxs-lookup"><span data-stu-id="a4f8a-118">Due date</span></span>  | <span data-ttu-id="a4f8a-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="a4f8a-119">Invoice</span></span> | <span data-ttu-id="a4f8a-120">Částka v měně transakce</span><span class="sxs-lookup"><span data-stu-id="a4f8a-120">Amount in transaction currency</span></span> | <span data-ttu-id="a4f8a-121">Měna</span><span class="sxs-lookup"><span data-stu-id="a4f8a-121">Currency</span></span> | <span data-ttu-id="a4f8a-122">Částka k vyrovnání</span><span class="sxs-lookup"><span data-stu-id="a4f8a-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="a4f8a-123">Vybrané</span><span class="sxs-lookup"><span data-stu-id="a4f8a-123">Selected</span></span> | <span data-ttu-id="a4f8a-124">Normální</span><span class="sxs-lookup"><span data-stu-id="a4f8a-124">Normal</span></span>            | <span data-ttu-id="a4f8a-125">Fakt-10040</span><span class="sxs-lookup"><span data-stu-id="a4f8a-125">Inv-10040</span></span> | <span data-ttu-id="a4f8a-126">3051</span><span class="sxs-lookup"><span data-stu-id="a4f8a-126">3051</span></span>    | <span data-ttu-id="a4f8a-127">29. 6. 2015</span><span class="sxs-lookup"><span data-stu-id="a4f8a-127">6/29/2015</span></span> | <span data-ttu-id="a4f8a-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="a4f8a-128">7/29/2015</span></span> | <span data-ttu-id="a4f8a-129">10040</span><span class="sxs-lookup"><span data-stu-id="a4f8a-129">10040</span></span>   | <span data-ttu-id="a4f8a-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="a4f8a-130">1,000.00</span></span>                       | <span data-ttu-id="a4f8a-131">USD</span><span class="sxs-lookup"><span data-stu-id="a4f8a-131">USD</span></span>      | <span data-ttu-id="a4f8a-132">940,00</span><span class="sxs-lookup"><span data-stu-id="a4f8a-132">940.00</span></span>           |

<span data-ttu-id="a4f8a-133">Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="a4f8a-134">Pole</span><span class="sxs-lookup"><span data-stu-id="a4f8a-134">Field</span></span>                        | <span data-ttu-id="a4f8a-135">Hodnota</span><span class="sxs-lookup"><span data-stu-id="a4f8a-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="a4f8a-136">Dat. plat. slevy</span><span class="sxs-lookup"><span data-stu-id="a4f8a-136">Cash discount date</span></span>           | <span data-ttu-id="a4f8a-137">12. 7. 2015</span><span class="sxs-lookup"><span data-stu-id="a4f8a-137">7/12/2015</span></span> |
| <span data-ttu-id="a4f8a-138">Částka platební slevy</span><span class="sxs-lookup"><span data-stu-id="a4f8a-138">Cash discount amount</span></span>         | <span data-ttu-id="a4f8a-139">60.00</span><span class="sxs-lookup"><span data-stu-id="a4f8a-139">60.00</span></span>     |
| <span data-ttu-id="a4f8a-140">Použít platební slevu</span><span class="sxs-lookup"><span data-stu-id="a4f8a-140">Use cash discount</span></span>            | <span data-ttu-id="a4f8a-141">Normální</span><span class="sxs-lookup"><span data-stu-id="a4f8a-141">Normal</span></span>    |
| <span data-ttu-id="a4f8a-142">Přijatá platební sleva</span><span class="sxs-lookup"><span data-stu-id="a4f8a-142">Cash discount taken</span></span>          | <span data-ttu-id="a4f8a-143">0,00</span><span class="sxs-lookup"><span data-stu-id="a4f8a-143">0.00</span></span>      |
| <span data-ttu-id="a4f8a-144">Částka platební slevy k přijetí</span><span class="sxs-lookup"><span data-stu-id="a4f8a-144">Cash discount amount to take</span></span> | <span data-ttu-id="a4f8a-145">60,00</span><span class="sxs-lookup"><span data-stu-id="a4f8a-145">60.00</span></span>     |

<span data-ttu-id="a4f8a-146">Potom April zaúčtuje platební deník.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-146">April posts the payment journal.</span></span> <span data-ttu-id="a4f8a-147">Faktura je plně uhrazena pomocí platby 940,00 a slevy 60,00.</span><span class="sxs-lookup"><span data-stu-id="a4f8a-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]