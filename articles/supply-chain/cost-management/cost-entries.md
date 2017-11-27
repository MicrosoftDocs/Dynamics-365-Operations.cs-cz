---
title: "Položky nákladů"
description: "Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří. Položka nákladů je záznam, který registruje množství a náklady na danou událost."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d8a443d03f8eb2d6ff44d869964b47b6569ce4c
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="cost-entries"></a><span data-ttu-id="9611b-104">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="9611b-104">Cost entries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9611b-105">Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří.</span><span class="sxs-lookup"><span data-stu-id="9611b-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="9611b-106">Položka nákladů je záznam, který registruje množství a náklady na danou událost.</span><span class="sxs-lookup"><span data-stu-id="9611b-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="9611b-107">Položky nákladů jsou seskupení skladových transakcí, které jsou zaznamenány v aktivních dimenzích finančních zásob.</span><span class="sxs-lookup"><span data-stu-id="9611b-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="9611b-108">Příklad</span><span class="sxs-lookup"><span data-stu-id="9611b-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="9611b-109">Příklad 1: Nejsou vytvořeny žádné položky nákladů</span><span class="sxs-lookup"><span data-stu-id="9611b-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="9611b-110">Je registrována událost deníku převodů.</span><span class="sxs-lookup"><span data-stu-id="9611b-110">A transfer journal event is registered.</span></span> <span data-ttu-id="9611b-111">Událost převede jeden kus zboží A z místa A do místa B. Dimenze zásob skladového místa není považována za součást objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="9611b-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="9611b-112">Událost tedy vytvoří dvě skladové transakce a žádné položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="9611b-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="9611b-113">Příklad 2: Jsou vytvořeny položky nákladů</span><span class="sxs-lookup"><span data-stu-id="9611b-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="9611b-114">Je registrována událost deníku převodů.</span><span class="sxs-lookup"><span data-stu-id="9611b-114">A transfer journal event is registered.</span></span> <span data-ttu-id="9611b-115">Událost převede jeden kus zboží A z pracoviště 1 na pracoviště 2.</span><span class="sxs-lookup"><span data-stu-id="9611b-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="9611b-116">Dimenze zásob pracoviště je považována za součást objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="9611b-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="9611b-117">Událost tedy vytvoří dvě skladové transakce a dvě položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="9611b-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="9611b-118">Příklad 3: Je vytvořena jedna položka nákladů</span><span class="sxs-lookup"><span data-stu-id="9611b-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="9611b-119">Událost příjemky produktu je registrována pro nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9611b-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="9611b-120">Událost registruje 100 kusů položky A za pořizovací cena 10,00 amerických dolarů (USD).</span><span class="sxs-lookup"><span data-stu-id="9611b-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="9611b-121">Vzhledem k tomu, že položka A používá pro sledování účel řízení zásob sériové číslo, bude pro každou přijatou položku vytvořeno jedinečné sériové číslo.</span><span class="sxs-lookup"><span data-stu-id="9611b-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="9611b-122">Událost tedy vytvoří 100 skladových transakcí a jednu položku nákladů.</span><span class="sxs-lookup"><span data-stu-id="9611b-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="9611b-123">Stránka Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="9611b-123">Cost entries page</span></span>
<span data-ttu-id="9611b-124">Nová stránka **Položky nákladů** umožňuje zobrazit a kontrolovat registrace množství a nákladů.</span><span class="sxs-lookup"><span data-stu-id="9611b-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="9611b-125">Tato stránka doplňuje stránky **Skladová transakce** a **Vyrovnání zásob**.</span><span class="sxs-lookup"><span data-stu-id="9611b-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="9611b-126">Záznamy jsou registrovány v chronologickém pořadí pro událost.</span><span class="sxs-lookup"><span data-stu-id="9611b-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="9611b-127">Lze tedy rychle vyhledat a zkontrolovat akumulované náklady na určitou událost nebo všechny události, které se vztahují k dokumentu.</span><span class="sxs-lookup"><span data-stu-id="9611b-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="9611b-128">Zde je příklad:</span><span class="sxs-lookup"><span data-stu-id="9611b-128">Here is an example:</span></span>

-   <span data-ttu-id="9611b-129">Události příjemky produktu je registrována pro zboží A. Sto kusů je přijato za pořizovací cenu 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="9611b-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="9611b-130">Několik dní po registraci události faktury se náklady zvýší na 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="9611b-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="9611b-131">Celková částka je tedy 1 100 USD.</span><span class="sxs-lookup"><span data-stu-id="9611b-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="9611b-132">Je vytvořen druhý doklad na rozdíl 100 USD.</span><span class="sxs-lookup"><span data-stu-id="9611b-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="9611b-133">O několik dní později jsou v nákupní objednávce registrovány vedlejší náklady ve výši 15,00 USD k pokrytí nákladů na přepravu.</span><span class="sxs-lookup"><span data-stu-id="9611b-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="9611b-134">Doklad</span><span class="sxs-lookup"><span data-stu-id="9611b-134">Voucher</span></span> | <span data-ttu-id="9611b-135">Datum</span><span class="sxs-lookup"><span data-stu-id="9611b-135">Date</span></span>       | <span data-ttu-id="9611b-136">Odkaz</span><span class="sxs-lookup"><span data-stu-id="9611b-136">Reference</span></span>      | <span data-ttu-id="9611b-137">Počet</span><span class="sxs-lookup"><span data-stu-id="9611b-137">Number</span></span> | <span data-ttu-id="9611b-138">ID šarže</span><span class="sxs-lookup"><span data-stu-id="9611b-138">Lot ID</span></span>  | <span data-ttu-id="9611b-139">Množství</span><span class="sxs-lookup"><span data-stu-id="9611b-139">Quantity</span></span> | <span data-ttu-id="9611b-140">Částka</span><span class="sxs-lookup"><span data-stu-id="9611b-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="9611b-141">00001</span><span class="sxs-lookup"><span data-stu-id="9611b-141">00001</span></span>   | <span data-ttu-id="9611b-142">01. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="9611b-142">01-01-2015</span></span> | <span data-ttu-id="9611b-143">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="9611b-143">Purchase order</span></span> | <span data-ttu-id="9611b-144">100001</span><span class="sxs-lookup"><span data-stu-id="9611b-144">100001</span></span> | <span data-ttu-id="9611b-145">0000101</span><span class="sxs-lookup"><span data-stu-id="9611b-145">0000101</span></span> | <span data-ttu-id="9611b-146">100,00</span><span class="sxs-lookup"><span data-stu-id="9611b-146">100.00</span></span>   | <span data-ttu-id="9611b-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="9611b-147">1000.00</span></span> |
| <span data-ttu-id="9611b-148">00002</span><span class="sxs-lookup"><span data-stu-id="9611b-148">00002</span></span>   | <span data-ttu-id="9611b-149">20. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="9611b-149">20-01-2015</span></span> | <span data-ttu-id="9611b-150">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="9611b-150">Purchase order</span></span> | <span data-ttu-id="9611b-151">100001</span><span class="sxs-lookup"><span data-stu-id="9611b-151">100001</span></span> | <span data-ttu-id="9611b-152">0000101</span><span class="sxs-lookup"><span data-stu-id="9611b-152">0000101</span></span> |          | <span data-ttu-id="9611b-153">100,00</span><span class="sxs-lookup"><span data-stu-id="9611b-153">100.00</span></span>  |
| <span data-ttu-id="9611b-154">00003</span><span class="sxs-lookup"><span data-stu-id="9611b-154">00003</span></span>   | <span data-ttu-id="9611b-155">31. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="9611b-155">31-01-2015</span></span> | <span data-ttu-id="9611b-156">Úprava</span><span class="sxs-lookup"><span data-stu-id="9611b-156">Adjustment</span></span>     | <span data-ttu-id="9611b-157">100001</span><span class="sxs-lookup"><span data-stu-id="9611b-157">100001</span></span> | <span data-ttu-id="9611b-158">0000101</span><span class="sxs-lookup"><span data-stu-id="9611b-158">0000101</span></span> |          | <span data-ttu-id="9611b-159">15:00</span><span class="sxs-lookup"><span data-stu-id="9611b-159">15.00</span></span>   |

<span data-ttu-id="9611b-160">Stránka **Položky nákladů** umožňuje filtrovat podle ID doklad a data dokladu.</span><span class="sxs-lookup"><span data-stu-id="9611b-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="9611b-161">Položky nákladů jsou k dispozici pouze pro [objekty nákladů](cost-object.md) nebo uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="9611b-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="see-also"></a><span data-ttu-id="9611b-162">Viz také</span><span class="sxs-lookup"><span data-stu-id="9611b-162">See also</span></span>
--------

[<span data-ttu-id="9611b-163">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="9611b-163">Cost objects</span></span>](cost-object.md)




