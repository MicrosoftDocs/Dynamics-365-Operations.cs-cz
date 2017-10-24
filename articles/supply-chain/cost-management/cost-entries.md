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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 38fedcb2f482296b1c88dda98d34dd8b7debf555
ms.contentlocale: cs-cz
ms.lasthandoff: 10/13/2017

---

# <a name="cost-entries"></a><span data-ttu-id="0eb75-104">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="0eb75-104">Cost entries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0eb75-105">Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří.</span><span class="sxs-lookup"><span data-stu-id="0eb75-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="0eb75-106">Položka nákladů je záznam, který registruje množství a náklady na danou událost.</span><span class="sxs-lookup"><span data-stu-id="0eb75-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="0eb75-107">Položky nákladů jsou seskupení skladových transakcí, které jsou zaznamenány v aktivních dimenzích finančních zásob.</span><span class="sxs-lookup"><span data-stu-id="0eb75-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="0eb75-108">Příklad</span><span class="sxs-lookup"><span data-stu-id="0eb75-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="0eb75-109">Příklad 1: Nejsou vytvořeny žádné položky nákladů</span><span class="sxs-lookup"><span data-stu-id="0eb75-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="0eb75-110">Je registrována událost deníku převodů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-110">A transfer journal event is registered.</span></span> <span data-ttu-id="0eb75-111">Událost převede jeden kus zboží A z místa A do místa B. Dimenze zásob skladového místa není považována za součást objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="0eb75-112">Událost tedy vytvoří dvě skladové transakce a žádné položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="0eb75-113">Příklad 2: Jsou vytvořeny položky nákladů</span><span class="sxs-lookup"><span data-stu-id="0eb75-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="0eb75-114">Je registrována událost deníku převodů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-114">A transfer journal event is registered.</span></span> <span data-ttu-id="0eb75-115">Událost převede jeden kus zboží A z pracoviště 1 na pracoviště 2.</span><span class="sxs-lookup"><span data-stu-id="0eb75-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="0eb75-116">Dimenze zásob pracoviště je považována za součást objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="0eb75-117">Událost tedy vytvoří dvě skladové transakce a dvě položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="0eb75-118">Příklad 3: Je vytvořena jedna položka nákladů</span><span class="sxs-lookup"><span data-stu-id="0eb75-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="0eb75-119">Událost příjemky produktu je registrována pro nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="0eb75-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="0eb75-120">Událost registruje 100 kusů položky A za pořizovací cena 10,00 amerických dolarů (USD).</span><span class="sxs-lookup"><span data-stu-id="0eb75-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="0eb75-121">Vzhledem k tomu, že položka A používá pro sledování účel řízení zásob sériové číslo, bude pro každou přijatou položku vytvořeno jedinečné sériové číslo.</span><span class="sxs-lookup"><span data-stu-id="0eb75-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="0eb75-122">Událost tedy vytvoří 100 skladových transakcí a jednu položku nákladů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="0eb75-123">Stránka Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="0eb75-123">Cost entries page</span></span>
<span data-ttu-id="0eb75-124">Nová stránka **Položky nákladů** umožňuje zobrazit a kontrolovat registrace množství a nákladů.</span><span class="sxs-lookup"><span data-stu-id="0eb75-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="0eb75-125">Tato stránka doplňuje stránky **Skladová transakce** a **Vyrovnání zásob**.</span><span class="sxs-lookup"><span data-stu-id="0eb75-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="0eb75-126">Záznamy jsou registrovány v chronologickém pořadí pro událost.</span><span class="sxs-lookup"><span data-stu-id="0eb75-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="0eb75-127">Lze tedy rychle vyhledat a zkontrolovat akumulované náklady na určitou událost nebo všechny události, které se vztahují k dokumentu.</span><span class="sxs-lookup"><span data-stu-id="0eb75-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="0eb75-128">Zde je příklad:</span><span class="sxs-lookup"><span data-stu-id="0eb75-128">Here is an example:</span></span>

-   <span data-ttu-id="0eb75-129">Události příjemky produktu je registrována pro zboží A. Sto kusů je přijato za pořizovací cenu 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="0eb75-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="0eb75-130">Několik dní po registraci události faktury se náklady zvýší na 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="0eb75-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="0eb75-131">Celková částka je tedy 1 100 USD.</span><span class="sxs-lookup"><span data-stu-id="0eb75-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="0eb75-132">Je vytvořen druhý doklad na rozdíl 100 USD.</span><span class="sxs-lookup"><span data-stu-id="0eb75-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="0eb75-133">O několik dní později jsou v nákupní objednávce registrovány vedlejší náklady ve výši 15,00 USD k pokrytí nákladů na přepravu.</span><span class="sxs-lookup"><span data-stu-id="0eb75-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="0eb75-134">Doklad</span><span class="sxs-lookup"><span data-stu-id="0eb75-134">Voucher</span></span> | <span data-ttu-id="0eb75-135">Datum</span><span class="sxs-lookup"><span data-stu-id="0eb75-135">Date</span></span>       | <span data-ttu-id="0eb75-136">Odkaz</span><span class="sxs-lookup"><span data-stu-id="0eb75-136">Reference</span></span>      | <span data-ttu-id="0eb75-137">Počet</span><span class="sxs-lookup"><span data-stu-id="0eb75-137">Number</span></span> | <span data-ttu-id="0eb75-138">ID šarže</span><span class="sxs-lookup"><span data-stu-id="0eb75-138">Lot ID</span></span>  | <span data-ttu-id="0eb75-139">Množství</span><span class="sxs-lookup"><span data-stu-id="0eb75-139">Quantity</span></span> | <span data-ttu-id="0eb75-140">Částka</span><span class="sxs-lookup"><span data-stu-id="0eb75-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="0eb75-141">00001</span><span class="sxs-lookup"><span data-stu-id="0eb75-141">00001</span></span>   | <span data-ttu-id="0eb75-142">01. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="0eb75-142">01-01-2015</span></span> | <span data-ttu-id="0eb75-143">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="0eb75-143">Purchase order</span></span> | <span data-ttu-id="0eb75-144">100001</span><span class="sxs-lookup"><span data-stu-id="0eb75-144">100001</span></span> | <span data-ttu-id="0eb75-145">0000101</span><span class="sxs-lookup"><span data-stu-id="0eb75-145">0000101</span></span> | <span data-ttu-id="0eb75-146">100,00</span><span class="sxs-lookup"><span data-stu-id="0eb75-146">100.00</span></span>   | <span data-ttu-id="0eb75-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="0eb75-147">1000.00</span></span> |
| <span data-ttu-id="0eb75-148">00002</span><span class="sxs-lookup"><span data-stu-id="0eb75-148">00002</span></span>   | <span data-ttu-id="0eb75-149">20. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="0eb75-149">20-01-2015</span></span> | <span data-ttu-id="0eb75-150">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="0eb75-150">Purchase order</span></span> | <span data-ttu-id="0eb75-151">100001</span><span class="sxs-lookup"><span data-stu-id="0eb75-151">100001</span></span> | <span data-ttu-id="0eb75-152">0000101</span><span class="sxs-lookup"><span data-stu-id="0eb75-152">0000101</span></span> |          | <span data-ttu-id="0eb75-153">100,00</span><span class="sxs-lookup"><span data-stu-id="0eb75-153">100.00</span></span>  |
| <span data-ttu-id="0eb75-154">00003</span><span class="sxs-lookup"><span data-stu-id="0eb75-154">00003</span></span>   | <span data-ttu-id="0eb75-155">31. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="0eb75-155">31-01-2015</span></span> | <span data-ttu-id="0eb75-156">Úprava</span><span class="sxs-lookup"><span data-stu-id="0eb75-156">Adjustment</span></span>     | <span data-ttu-id="0eb75-157">100001</span><span class="sxs-lookup"><span data-stu-id="0eb75-157">100001</span></span> | <span data-ttu-id="0eb75-158">0000101</span><span class="sxs-lookup"><span data-stu-id="0eb75-158">0000101</span></span> |          | <span data-ttu-id="0eb75-159">15:00</span><span class="sxs-lookup"><span data-stu-id="0eb75-159">15.00</span></span>   |

<span data-ttu-id="0eb75-160">Stránka **Položky nákladů** umožňuje filtrovat podle ID doklad a data dokladu.</span><span class="sxs-lookup"><span data-stu-id="0eb75-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="0eb75-161">Položky nákladů jsou k dispozici pouze pro [objekty nákladů](cost-object.md) nebo uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="0eb75-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="see-also"></a><span data-ttu-id="0eb75-162">Viz také</span><span class="sxs-lookup"><span data-stu-id="0eb75-162">See also</span></span>
--------

[<span data-ttu-id="0eb75-163">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="0eb75-163">Cost objects</span></span>](cost-object.md)




