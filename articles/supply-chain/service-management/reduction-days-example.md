---
title: Příklad dnů snížení
description: Příklad dnů snížení
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 509d1a9e2abd79938376209d8feab1b935394833
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010515"
---
# <a name="reduction-days-example"></a><span data-ttu-id="f0d85-103">Příklad dnů snížení</span><span class="sxs-lookup"><span data-stu-id="f0d85-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f0d85-104">Vytvořili jste transakci předplatného pro předplatné zákaznické údržby podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="f0d85-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="f0d85-105">Od data</span><span class="sxs-lookup"><span data-stu-id="f0d85-105">From date</span></span></p></th>
<th><p><span data-ttu-id="f0d85-106">Do data</span><span class="sxs-lookup"><span data-stu-id="f0d85-106">To date</span></span></p></th>
<th><p><span data-ttu-id="f0d85-107">Předplatné</span><span class="sxs-lookup"><span data-stu-id="f0d85-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="f0d85-108">Typ předplatného</span><span class="sxs-lookup"><span data-stu-id="f0d85-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="f0d85-109">Project</span><span class="sxs-lookup"><span data-stu-id="f0d85-109">Project</span></span></p></th>
<th><p><span data-ttu-id="f0d85-110">Kategorie</span><span class="sxs-lookup"><span data-stu-id="f0d85-110">Category</span></span></p></th>
<th><p><span data-ttu-id="f0d85-111">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="f0d85-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="f0d85-112">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="f0d85-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0d85-113">01. března 2011</span><span class="sxs-lookup"><span data-stu-id="f0d85-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="f0d85-114">31. března 2011</span><span class="sxs-lookup"><span data-stu-id="f0d85-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="f0d85-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="f0d85-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="f0d85-116"><strong>Řádné</strong></span><span class="sxs-lookup"><span data-stu-id="f0d85-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d85-117">9013</span><span class="sxs-lookup"><span data-stu-id="f0d85-117">9013</span></span></p></td>
<td><p><span data-ttu-id="f0d85-118">Dílčí kategorie 2</span><span class="sxs-lookup"><span data-stu-id="f0d85-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="f0d85-119">EUR</span><span class="sxs-lookup"><span data-stu-id="f0d85-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="f0d85-120">200,00</span><span class="sxs-lookup"><span data-stu-id="f0d85-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f0d85-121">Zákazník ohlásí, že nevyžaduje disponibilitu služeb po dobu dvou dnů (10. a 11. března).</span><span class="sxs-lookup"><span data-stu-id="f0d85-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="f0d85-122">Souhlasíte se snížením předplatného o tyto dva dny.</span><span class="sxs-lookup"><span data-stu-id="f0d85-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="f0d85-123">Vytvoříte novou transakci typu **Dny omezení** podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="f0d85-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="f0d85-124">Od data</span><span class="sxs-lookup"><span data-stu-id="f0d85-124">From date</span></span></p></th>
<th><p><span data-ttu-id="f0d85-125">Do data</span><span class="sxs-lookup"><span data-stu-id="f0d85-125">To date</span></span></p></th>
<th><p><span data-ttu-id="f0d85-126">Předplatné</span><span class="sxs-lookup"><span data-stu-id="f0d85-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="f0d85-127">Typ předplatného</span><span class="sxs-lookup"><span data-stu-id="f0d85-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="f0d85-128">Project</span><span class="sxs-lookup"><span data-stu-id="f0d85-128">Project</span></span></p></th>
<th><p><span data-ttu-id="f0d85-129">Kategorie</span><span class="sxs-lookup"><span data-stu-id="f0d85-129">Category</span></span></p></th>
<th><p><span data-ttu-id="f0d85-130">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="f0d85-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="f0d85-131">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="f0d85-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0d85-132">10. března 2011</span><span class="sxs-lookup"><span data-stu-id="f0d85-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="f0d85-133">11. března 2011</span><span class="sxs-lookup"><span data-stu-id="f0d85-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="f0d85-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="f0d85-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="f0d85-135"><strong>Dny omezení</strong></span><span class="sxs-lookup"><span data-stu-id="f0d85-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d85-136">9013</span><span class="sxs-lookup"><span data-stu-id="f0d85-136">9013</span></span></p></td>
<td><p><span data-ttu-id="f0d85-137">Dílčí kategorie 2</span><span class="sxs-lookup"><span data-stu-id="f0d85-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="f0d85-138">EUR</span><span class="sxs-lookup"><span data-stu-id="f0d85-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="f0d85-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="f0d85-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f0d85-140">Při fakturaci transakcí pro březen 2011 je prodejní cena 200 EUR snížena o částku 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="f0d85-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="f0d85-141">Fakturovatelná částka pro transakci předplatného je tedy 187,10 EUR a obě transakce budou fakturovány celkovou částkou 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="f0d85-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0d85-142">Viz také</span><span class="sxs-lookup"><span data-stu-id="f0d85-142">See also</span></span>

[<span data-ttu-id="f0d85-143">Snížení počtu dnů u poplatků za odběr</span><span class="sxs-lookup"><span data-stu-id="f0d85-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


