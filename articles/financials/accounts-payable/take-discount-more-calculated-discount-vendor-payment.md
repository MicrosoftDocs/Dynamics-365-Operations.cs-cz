---
title: Použití slevy, která je větší, než vypočítaná sleva pro platbu dodavatele
description: Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře. K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843258"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="9ae24-104">Použití slevy, která je větší, než vypočítaná sleva pro platbu dodavatele</span><span class="sxs-lookup"><span data-stu-id="9ae24-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ae24-105">Tento článek vás provede scénářem, kde je využita platební sleva pro částku vyšší, než je sleva, která byla původně k dispozici na faktuře.</span><span class="sxs-lookup"><span data-stu-id="9ae24-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="9ae24-106">K této situaci může dojít v případě, že organizace sestaví dohodu s dodavatelem, podle které zaplatí menší částku na faktuře.</span><span class="sxs-lookup"><span data-stu-id="9ae24-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="9ae24-107">Dodavatel 3051 umožňuje společnosti Fabrikam přijmout platební slevu 4 %, pokud je faktura splacena do 7 dní.</span><span class="sxs-lookup"><span data-stu-id="9ae24-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="9ae24-108">Dne 29. dubna je zadána faktura na 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="9ae24-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="9ae24-109">Dodavatel umožňuje April využít slevu 60,00 namísto výchozí slevy 40,00, která je k dispozici pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="9ae24-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="9ae24-110">April zaznamená jednorázovou platbu pomocí deníku plateb závazků.</span><span class="sxs-lookup"><span data-stu-id="9ae24-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="9ae24-111">Zadá platby dodavatele a otevře stránku **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="9ae24-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="9ae24-112">Označí fakturu a změní hodnotu v poli **Částka platební slevy** na **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="9ae24-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="9ae24-113">Označit</span><span class="sxs-lookup"><span data-stu-id="9ae24-113">Mark</span></span>     | <span data-ttu-id="9ae24-114">Použít platební slevu</span><span class="sxs-lookup"><span data-stu-id="9ae24-114">Use cash discount</span></span> | <span data-ttu-id="9ae24-115">Doklad</span><span class="sxs-lookup"><span data-stu-id="9ae24-115">Voucher</span></span>   | <span data-ttu-id="9ae24-116">Účet</span><span class="sxs-lookup"><span data-stu-id="9ae24-116">Account</span></span> | <span data-ttu-id="9ae24-117">Datum</span><span class="sxs-lookup"><span data-stu-id="9ae24-117">Date</span></span>      | <span data-ttu-id="9ae24-118">Datum splatnosti</span><span class="sxs-lookup"><span data-stu-id="9ae24-118">Due date</span></span>  | <span data-ttu-id="9ae24-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="9ae24-119">Invoice</span></span> | <span data-ttu-id="9ae24-120">Částka v měně transakce</span><span class="sxs-lookup"><span data-stu-id="9ae24-120">Amount in transaction currency</span></span> | <span data-ttu-id="9ae24-121">Měna</span><span class="sxs-lookup"><span data-stu-id="9ae24-121">Currency</span></span> | <span data-ttu-id="9ae24-122">Částka k vyrovnání</span><span class="sxs-lookup"><span data-stu-id="9ae24-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="9ae24-123">Vybrané</span><span class="sxs-lookup"><span data-stu-id="9ae24-123">Selected</span></span> | <span data-ttu-id="9ae24-124">Normální</span><span class="sxs-lookup"><span data-stu-id="9ae24-124">Normal</span></span>            | <span data-ttu-id="9ae24-125">Fakt-10040</span><span class="sxs-lookup"><span data-stu-id="9ae24-125">Inv-10040</span></span> | <span data-ttu-id="9ae24-126">3051</span><span class="sxs-lookup"><span data-stu-id="9ae24-126">3051</span></span>    | <span data-ttu-id="9ae24-127">29. 6. 2015</span><span class="sxs-lookup"><span data-stu-id="9ae24-127">6/29/2015</span></span> | <span data-ttu-id="9ae24-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="9ae24-128">7/29/2015</span></span> | <span data-ttu-id="9ae24-129">10040</span><span class="sxs-lookup"><span data-stu-id="9ae24-129">10040</span></span>   | <span data-ttu-id="9ae24-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="9ae24-130">1,000.00</span></span>                       | <span data-ttu-id="9ae24-131">USD</span><span class="sxs-lookup"><span data-stu-id="9ae24-131">USD</span></span>      | <span data-ttu-id="9ae24-132">940,00</span><span class="sxs-lookup"><span data-stu-id="9ae24-132">940.00</span></span>           |

<span data-ttu-id="9ae24-133">Informace o slevě se zobrazí v dolní části stránky **Vyrovnat transakce**.</span><span class="sxs-lookup"><span data-stu-id="9ae24-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="9ae24-134">Datum platební slevy</span><span class="sxs-lookup"><span data-stu-id="9ae24-134">Cash discount date</span></span>           | <span data-ttu-id="9ae24-135">12. 7. 2015</span><span class="sxs-lookup"><span data-stu-id="9ae24-135">7/12/2015</span></span> |
| <span data-ttu-id="9ae24-136">Částka platební slevy</span><span class="sxs-lookup"><span data-stu-id="9ae24-136">Cash discount amount</span></span>         | <span data-ttu-id="9ae24-137">60,00</span><span class="sxs-lookup"><span data-stu-id="9ae24-137">60.00</span></span>     |
| <span data-ttu-id="9ae24-138">Použít platební slevu</span><span class="sxs-lookup"><span data-stu-id="9ae24-138">Use cash discount</span></span>            | <span data-ttu-id="9ae24-139">Normální</span><span class="sxs-lookup"><span data-stu-id="9ae24-139">Normal</span></span>    |
| <span data-ttu-id="9ae24-140">Přijatá platební sleva</span><span class="sxs-lookup"><span data-stu-id="9ae24-140">Cash discount taken</span></span>          | <span data-ttu-id="9ae24-141">0,00</span><span class="sxs-lookup"><span data-stu-id="9ae24-141">0.00</span></span>      |
| <span data-ttu-id="9ae24-142">Částka platební slevy k přijetí</span><span class="sxs-lookup"><span data-stu-id="9ae24-142">Cash discount amount to take</span></span> | <span data-ttu-id="9ae24-143">60,00</span><span class="sxs-lookup"><span data-stu-id="9ae24-143">60.00</span></span>     |

<span data-ttu-id="9ae24-144">Potom April zaúčtuje platební deník.</span><span class="sxs-lookup"><span data-stu-id="9ae24-144">April posts the payment journal.</span></span> <span data-ttu-id="9ae24-145">Faktura je plně uhrazena pomocí platby 940,00 a slevy 60,00.</span><span class="sxs-lookup"><span data-stu-id="9ae24-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



