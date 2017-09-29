---
title: "Použití slevy, která je větší, než vypočítaná sleva pro platbu dodavatele"
description: "Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře. K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 39830014593b7b1bc2868afffcca0f77a0c8a029
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="81bd2-104">Použití slevy, která je větší, než vypočítaná sleva pro platbu dodavatele</span><span class="sxs-lookup"><span data-stu-id="81bd2-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="81bd2-105">Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře.</span><span class="sxs-lookup"><span data-stu-id="81bd2-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="81bd2-106">K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře.</span><span class="sxs-lookup"><span data-stu-id="81bd2-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="81bd2-107">Dodavatel 3051 umožňuje společnosti Fabrikam přijmout platební slevu 4 %, pokud je faktura splacena do 7 dní.</span><span class="sxs-lookup"><span data-stu-id="81bd2-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="81bd2-108">Dne 29. dubna je zadána faktura na 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="81bd2-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="81bd2-109">Dodavatel umožňuje April využít slevu 60,00 namísto výchozí slevy 40,00, která je k dispozici pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="81bd2-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="81bd2-110">April zaznamená jednorázovou platbu pomocí deníku plateb závazků.</span><span class="sxs-lookup"><span data-stu-id="81bd2-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="81bd2-111">Zadá platby dodavatele a otevře stránku **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="81bd2-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="81bd2-112">Označí fakturu a změní hodnotu v poli **Částka platební slevy** na **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="81bd2-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>
| <span data-ttu-id="81bd2-113">Označit</span><span class="sxs-lookup"><span data-stu-id="81bd2-113">Mark</span></span>     | <span data-ttu-id="81bd2-114">Použít platební slevu</span><span class="sxs-lookup"><span data-stu-id="81bd2-114">Use cash discount</span></span> | <span data-ttu-id="81bd2-115">Doklad</span><span class="sxs-lookup"><span data-stu-id="81bd2-115">Voucher</span></span>   | <span data-ttu-id="81bd2-116">Účet</span><span class="sxs-lookup"><span data-stu-id="81bd2-116">Account</span></span> | <span data-ttu-id="81bd2-117">Datum</span><span class="sxs-lookup"><span data-stu-id="81bd2-117">Date</span></span>      | <span data-ttu-id="81bd2-118">Datum splatnosti</span><span class="sxs-lookup"><span data-stu-id="81bd2-118">Due date</span></span>  | <span data-ttu-id="81bd2-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="81bd2-119">Invoice</span></span> | <span data-ttu-id="81bd2-120">Částka v měně transakce</span><span class="sxs-lookup"><span data-stu-id="81bd2-120">Amount in transaction currency</span></span> | <span data-ttu-id="81bd2-121">Měna</span><span class="sxs-lookup"><span data-stu-id="81bd2-121">Currency</span></span> | <span data-ttu-id="81bd2-122">Částka k vyrovnání</span><span class="sxs-lookup"><span data-stu-id="81bd2-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="81bd2-123">Vybrané</span><span class="sxs-lookup"><span data-stu-id="81bd2-123">Selected</span></span> | <span data-ttu-id="81bd2-124">Normální</span><span class="sxs-lookup"><span data-stu-id="81bd2-124">Normal</span></span>            | <span data-ttu-id="81bd2-125">Fakt-10040</span><span class="sxs-lookup"><span data-stu-id="81bd2-125">Inv-10040</span></span> | <span data-ttu-id="81bd2-126">3051</span><span class="sxs-lookup"><span data-stu-id="81bd2-126">3051</span></span>    | <span data-ttu-id="81bd2-127">29. 6. 2015</span><span class="sxs-lookup"><span data-stu-id="81bd2-127">6/29/2015</span></span> | <span data-ttu-id="81bd2-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="81bd2-128">7/29/2015</span></span> | <span data-ttu-id="81bd2-129">10040</span><span class="sxs-lookup"><span data-stu-id="81bd2-129">10040</span></span>   | <span data-ttu-id="81bd2-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="81bd2-130">1,000.00</span></span>                       | <span data-ttu-id="81bd2-131">USD</span><span class="sxs-lookup"><span data-stu-id="81bd2-131">USD</span></span>      | <span data-ttu-id="81bd2-132">940,00</span><span class="sxs-lookup"><span data-stu-id="81bd2-132">940.00</span></span>           |

<span data-ttu-id="81bd2-133">Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="81bd2-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>
|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="81bd2-134">Datum platební slevy</span><span class="sxs-lookup"><span data-stu-id="81bd2-134">Cash discount date</span></span>           | <span data-ttu-id="81bd2-135">12. 7. 2015</span><span class="sxs-lookup"><span data-stu-id="81bd2-135">7/12/2015</span></span> |
| <span data-ttu-id="81bd2-136">Částka platební slevy</span><span class="sxs-lookup"><span data-stu-id="81bd2-136">Cash discount amount</span></span>         | <span data-ttu-id="81bd2-137">60,00</span><span class="sxs-lookup"><span data-stu-id="81bd2-137">60.00</span></span>     |
| <span data-ttu-id="81bd2-138">Použít platební slevu</span><span class="sxs-lookup"><span data-stu-id="81bd2-138">Use cash discount</span></span>            | <span data-ttu-id="81bd2-139">Normální</span><span class="sxs-lookup"><span data-stu-id="81bd2-139">Normal</span></span>    |
| <span data-ttu-id="81bd2-140">Přijatá platební sleva</span><span class="sxs-lookup"><span data-stu-id="81bd2-140">Cash discount taken</span></span>          | <span data-ttu-id="81bd2-141">0,00</span><span class="sxs-lookup"><span data-stu-id="81bd2-141">0.00</span></span>      |
| <span data-ttu-id="81bd2-142">Částka platební slevy k přijetí</span><span class="sxs-lookup"><span data-stu-id="81bd2-142">Cash discount amount to take</span></span> | <span data-ttu-id="81bd2-143">60,00</span><span class="sxs-lookup"><span data-stu-id="81bd2-143">60.00</span></span>     |

<span data-ttu-id="81bd2-144">Potom April zaúčtuje platební deník.</span><span class="sxs-lookup"><span data-stu-id="81bd2-144">April posts the payment journal.</span></span> <span data-ttu-id="81bd2-145">Faktura je plně uhrazena pomocí platby 940,00 a slevy 60,00.</span><span class="sxs-lookup"><span data-stu-id="81bd2-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




