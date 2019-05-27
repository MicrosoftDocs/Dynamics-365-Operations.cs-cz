---
title: Příklad dnů snížení
description: Příklad dnů snížení
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564501"
---
# <a name="reduction-days-example"></a><span data-ttu-id="a34b9-103">Příklad dnů snížení</span><span class="sxs-lookup"><span data-stu-id="a34b9-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a34b9-104">Vytvořili jste transakci předplatného pro předplatné zákaznické údržby podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="a34b9-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="a34b9-105">Od data</span><span class="sxs-lookup"><span data-stu-id="a34b9-105">From date</span></span></p></th>
<th><p><span data-ttu-id="a34b9-106">Do data</span><span class="sxs-lookup"><span data-stu-id="a34b9-106">To date</span></span></p></th>
<th><p><span data-ttu-id="a34b9-107">Předplatné</span><span class="sxs-lookup"><span data-stu-id="a34b9-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a34b9-108">Typ předplatného</span><span class="sxs-lookup"><span data-stu-id="a34b9-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a34b9-109">Project</span><span class="sxs-lookup"><span data-stu-id="a34b9-109">Project</span></span></p></th>
<th><p><span data-ttu-id="a34b9-110">Kategorie</span><span class="sxs-lookup"><span data-stu-id="a34b9-110">Category</span></span></p></th>
<th><p><span data-ttu-id="a34b9-111">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="a34b9-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a34b9-112">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="a34b9-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a34b9-113">01. března 2011</span><span class="sxs-lookup"><span data-stu-id="a34b9-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="a34b9-114">31. března 2011</span><span class="sxs-lookup"><span data-stu-id="a34b9-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="a34b9-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="a34b9-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a34b9-116"><strong>Řádné</strong></span><span class="sxs-lookup"><span data-stu-id="a34b9-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="a34b9-117">9013</span><span class="sxs-lookup"><span data-stu-id="a34b9-117">9013</span></span></p></td>
<td><p><span data-ttu-id="a34b9-118">Dílčí kategorie 2</span><span class="sxs-lookup"><span data-stu-id="a34b9-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a34b9-119">EUR</span><span class="sxs-lookup"><span data-stu-id="a34b9-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="a34b9-120">200,00</span><span class="sxs-lookup"><span data-stu-id="a34b9-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a34b9-121">Zákazník ohlásí, že nevyžaduje disponibilitu služeb po dobu dvou dnů (10. a 11. března).</span><span class="sxs-lookup"><span data-stu-id="a34b9-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="a34b9-122">Souhlasíte se snížením předplatného o tyto dva dny.</span><span class="sxs-lookup"><span data-stu-id="a34b9-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="a34b9-123">Vytvoříte novou transakci typu **Dny omezení** podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="a34b9-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="a34b9-124">Od data</span><span class="sxs-lookup"><span data-stu-id="a34b9-124">From date</span></span></p></th>
<th><p><span data-ttu-id="a34b9-125">Do data</span><span class="sxs-lookup"><span data-stu-id="a34b9-125">To date</span></span></p></th>
<th><p><span data-ttu-id="a34b9-126">Předplatné</span><span class="sxs-lookup"><span data-stu-id="a34b9-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a34b9-127">Typ předplatného</span><span class="sxs-lookup"><span data-stu-id="a34b9-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a34b9-128">Project</span><span class="sxs-lookup"><span data-stu-id="a34b9-128">Project</span></span></p></th>
<th><p><span data-ttu-id="a34b9-129">Kategorie</span><span class="sxs-lookup"><span data-stu-id="a34b9-129">Category</span></span></p></th>
<th><p><span data-ttu-id="a34b9-130">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="a34b9-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a34b9-131">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="a34b9-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a34b9-132">10. března 2011</span><span class="sxs-lookup"><span data-stu-id="a34b9-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="a34b9-133">11. března 2011</span><span class="sxs-lookup"><span data-stu-id="a34b9-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="a34b9-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="a34b9-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a34b9-135"><strong>Dny omezení</strong></span><span class="sxs-lookup"><span data-stu-id="a34b9-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="a34b9-136">9013</span><span class="sxs-lookup"><span data-stu-id="a34b9-136">9013</span></span></p></td>
<td><p><span data-ttu-id="a34b9-137">Dílčí kategorie 2</span><span class="sxs-lookup"><span data-stu-id="a34b9-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a34b9-138">EUR</span><span class="sxs-lookup"><span data-stu-id="a34b9-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="a34b9-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="a34b9-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a34b9-140">Při fakturaci transakcí pro březen 2011 je prodejní cena 200 EUR snížena o částku 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="a34b9-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="a34b9-141">Fakturovatelná částka pro transakci předplatného je tedy 187,10 EUR a obě transakce budou fakturovány celkovou částkou 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="a34b9-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="a34b9-142">Viz také</span><span class="sxs-lookup"><span data-stu-id="a34b9-142">See also</span></span>

[<span data-ttu-id="a34b9-143">Snížení počtu dnů u poplatků za odběr</span><span class="sxs-lookup"><span data-stu-id="a34b9-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


