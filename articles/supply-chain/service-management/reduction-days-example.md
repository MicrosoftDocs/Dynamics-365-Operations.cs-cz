---
title: Příklad dnů snížení
description: Příklad dnů snížení
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836055"
---
# <a name="reduction-days-example"></a><span data-ttu-id="57873-103">Příklad dnů snížení</span><span class="sxs-lookup"><span data-stu-id="57873-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="57873-104">Vytvořili jste transakci předplatného pro předplatné zákaznické údržby podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="57873-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57873-105">Od data</span><span class="sxs-lookup"><span data-stu-id="57873-105">From date</span></span></p></th>
<th><p><span data-ttu-id="57873-106">Do data</span><span class="sxs-lookup"><span data-stu-id="57873-106">To date</span></span></p></th>
<th><p><span data-ttu-id="57873-107">Předplatné</span><span class="sxs-lookup"><span data-stu-id="57873-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="57873-108">Typ předplatného</span><span class="sxs-lookup"><span data-stu-id="57873-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="57873-109">Project</span><span class="sxs-lookup"><span data-stu-id="57873-109">Project</span></span></p></th>
<th><p><span data-ttu-id="57873-110">Kategorie</span><span class="sxs-lookup"><span data-stu-id="57873-110">Category</span></span></p></th>
<th><p><span data-ttu-id="57873-111">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="57873-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="57873-112">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="57873-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57873-113">01. března 2011</span><span class="sxs-lookup"><span data-stu-id="57873-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="57873-114">31. března 2011</span><span class="sxs-lookup"><span data-stu-id="57873-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="57873-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="57873-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="57873-116"><strong>Řádné</strong></span><span class="sxs-lookup"><span data-stu-id="57873-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="57873-117">9013</span><span class="sxs-lookup"><span data-stu-id="57873-117">9013</span></span></p></td>
<td><p><span data-ttu-id="57873-118">Dílčí kategorie 2</span><span class="sxs-lookup"><span data-stu-id="57873-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="57873-119">EUR</span><span class="sxs-lookup"><span data-stu-id="57873-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="57873-120">200,00</span><span class="sxs-lookup"><span data-stu-id="57873-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57873-121">Zákazník ohlásí, že nevyžaduje disponibilitu služeb po dobu dvou dnů (10. a 11. března).</span><span class="sxs-lookup"><span data-stu-id="57873-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="57873-122">Souhlasíte se snížením předplatného o tyto dva dny.</span><span class="sxs-lookup"><span data-stu-id="57873-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="57873-123">Vytvoříte novou transakci typu **Dny omezení** podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="57873-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57873-124">Od data</span><span class="sxs-lookup"><span data-stu-id="57873-124">From date</span></span></p></th>
<th><p><span data-ttu-id="57873-125">Do data</span><span class="sxs-lookup"><span data-stu-id="57873-125">To date</span></span></p></th>
<th><p><span data-ttu-id="57873-126">Předplatné</span><span class="sxs-lookup"><span data-stu-id="57873-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="57873-127">Typ předplatného</span><span class="sxs-lookup"><span data-stu-id="57873-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="57873-128">Project</span><span class="sxs-lookup"><span data-stu-id="57873-128">Project</span></span></p></th>
<th><p><span data-ttu-id="57873-129">Kategorie</span><span class="sxs-lookup"><span data-stu-id="57873-129">Category</span></span></p></th>
<th><p><span data-ttu-id="57873-130">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="57873-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="57873-131">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="57873-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57873-132">10. března 2011</span><span class="sxs-lookup"><span data-stu-id="57873-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="57873-133">11. března 2011</span><span class="sxs-lookup"><span data-stu-id="57873-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="57873-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="57873-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="57873-135"><strong>Dny omezení</strong></span><span class="sxs-lookup"><span data-stu-id="57873-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="57873-136">9013</span><span class="sxs-lookup"><span data-stu-id="57873-136">9013</span></span></p></td>
<td><p><span data-ttu-id="57873-137">Dílčí kategorie 2</span><span class="sxs-lookup"><span data-stu-id="57873-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="57873-138">EUR</span><span class="sxs-lookup"><span data-stu-id="57873-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="57873-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="57873-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57873-140">Při fakturaci transakcí pro březen 2011 je prodejní cena 200 EUR snížena o částku 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="57873-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="57873-141">Fakturovatelná částka pro transakci předplatného je tedy 187,10 EUR a obě transakce budou fakturovány celkovou částkou 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="57873-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="57873-142">Viz také</span><span class="sxs-lookup"><span data-stu-id="57873-142">See also</span></span>

[<span data-ttu-id="57873-143">Snížení počtu dnů u poplatků za odběr</span><span class="sxs-lookup"><span data-stu-id="57873-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]