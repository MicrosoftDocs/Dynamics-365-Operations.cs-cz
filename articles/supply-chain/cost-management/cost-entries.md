---
title: Položky nákladů
description: Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří. Položka nákladů je záznam, který registruje množství a náklady na danou událost.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ff771cf44595420ca721605daabaa6b071a4ff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967786"
---
# <a name="cost-entries"></a><span data-ttu-id="79b2d-104">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="79b2d-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79b2d-105">Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří.</span><span class="sxs-lookup"><span data-stu-id="79b2d-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="79b2d-106">Položka nákladů je záznam, který registruje množství a náklady na danou událost.</span><span class="sxs-lookup"><span data-stu-id="79b2d-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="79b2d-107">Položky nákladů jsou seskupení skladových transakcí, které jsou zaznamenány v aktivních dimenzích finančních zásob.</span><span class="sxs-lookup"><span data-stu-id="79b2d-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="79b2d-108">Příklad</span><span class="sxs-lookup"><span data-stu-id="79b2d-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="79b2d-109">Příklad 1: Nejsou vytvořeny žádné položky nákladů</span><span class="sxs-lookup"><span data-stu-id="79b2d-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="79b2d-110">Je registrována událost deníku převodů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-110">A transfer journal event is registered.</span></span> <span data-ttu-id="79b2d-111">Událost převede jeden kus zboží A z místa A do místa B. Dimenze zásob skladového místa není považována za součást objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="79b2d-112">Událost tedy vytvoří dvě skladové transakce a žádné položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="79b2d-113">Příklad 2: Jsou vytvořeny položky nákladů</span><span class="sxs-lookup"><span data-stu-id="79b2d-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="79b2d-114">Je registrována událost deníku převodů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-114">A transfer journal event is registered.</span></span> <span data-ttu-id="79b2d-115">Událost převede jeden kus zboží A z pracoviště 1 na pracoviště 2.</span><span class="sxs-lookup"><span data-stu-id="79b2d-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="79b2d-116">Dimenze zásob pracoviště je považována za součást objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="79b2d-117">Událost tedy vytvoří dvě skladové transakce a dvě položky nákladů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="79b2d-118">Příklad 3: Je vytvořena jedna položka nákladů</span><span class="sxs-lookup"><span data-stu-id="79b2d-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="79b2d-119">Událost příjemky produktu je registrována pro nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="79b2d-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="79b2d-120">Událost registruje 100 kusů položky A za pořizovací cena 10,00 amerických dolarů (USD).</span><span class="sxs-lookup"><span data-stu-id="79b2d-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="79b2d-121">Vzhledem k tomu, že položka A používá pro sledování účel řízení zásob sériové číslo, bude pro každou přijatou položku vytvořeno jedinečné sériové číslo.</span><span class="sxs-lookup"><span data-stu-id="79b2d-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="79b2d-122">Událost tedy vytvoří 100 skladových transakcí a jednu položku nákladů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="79b2d-123">Stránka Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="79b2d-123">Cost entries page</span></span>
<span data-ttu-id="79b2d-124">Nová stránka **Položky nákladů** umožňuje zobrazit a kontrolovat registrace množství a nákladů.</span><span class="sxs-lookup"><span data-stu-id="79b2d-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="79b2d-125">Tato stránka doplňuje stránky **Skladová transakce** a **Vyrovnání zásob**.</span><span class="sxs-lookup"><span data-stu-id="79b2d-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="79b2d-126">Záznamy jsou registrovány v chronologickém pořadí pro událost.</span><span class="sxs-lookup"><span data-stu-id="79b2d-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="79b2d-127">Lze tedy rychle vyhledat a zkontrolovat akumulované náklady na určitou událost nebo všechny události, které se vztahují k dokumentu.</span><span class="sxs-lookup"><span data-stu-id="79b2d-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="79b2d-128">Zde je příklad:</span><span class="sxs-lookup"><span data-stu-id="79b2d-128">Here is an example:</span></span>

-   <span data-ttu-id="79b2d-129">Události příjemky produktu je registrována pro zboží A. Sto kusů je přijato za pořizovací cenu 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="79b2d-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="79b2d-130">Několik dní po registraci události faktury se náklady zvýší na 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="79b2d-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="79b2d-131">Celková částka je tedy 1 100 USD.</span><span class="sxs-lookup"><span data-stu-id="79b2d-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="79b2d-132">Je vytvořen druhý doklad na rozdíl 100 USD.</span><span class="sxs-lookup"><span data-stu-id="79b2d-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="79b2d-133">O několik dní později jsou v nákupní objednávce registrovány vedlejší náklady ve výši 15,00 USD k pokrytí nákladů na přepravu.</span><span class="sxs-lookup"><span data-stu-id="79b2d-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="79b2d-134">Doklad</span><span class="sxs-lookup"><span data-stu-id="79b2d-134">Voucher</span></span> | <span data-ttu-id="79b2d-135">Datum</span><span class="sxs-lookup"><span data-stu-id="79b2d-135">Date</span></span>       | <span data-ttu-id="79b2d-136">Odkaz</span><span class="sxs-lookup"><span data-stu-id="79b2d-136">Reference</span></span>      | <span data-ttu-id="79b2d-137">Počet</span><span class="sxs-lookup"><span data-stu-id="79b2d-137">Number</span></span> | <span data-ttu-id="79b2d-138">ID šarže</span><span class="sxs-lookup"><span data-stu-id="79b2d-138">Lot ID</span></span>  | <span data-ttu-id="79b2d-139">Množství</span><span class="sxs-lookup"><span data-stu-id="79b2d-139">Quantity</span></span> | <span data-ttu-id="79b2d-140">Částka</span><span class="sxs-lookup"><span data-stu-id="79b2d-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="79b2d-141">00001</span><span class="sxs-lookup"><span data-stu-id="79b2d-141">00001</span></span>   | <span data-ttu-id="79b2d-142">01. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="79b2d-142">01-01-2015</span></span> | <span data-ttu-id="79b2d-143">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="79b2d-143">Purchase order</span></span> | <span data-ttu-id="79b2d-144">100001</span><span class="sxs-lookup"><span data-stu-id="79b2d-144">100001</span></span> | <span data-ttu-id="79b2d-145">0000101</span><span class="sxs-lookup"><span data-stu-id="79b2d-145">0000101</span></span> | <span data-ttu-id="79b2d-146">100,00</span><span class="sxs-lookup"><span data-stu-id="79b2d-146">100.00</span></span>   | <span data-ttu-id="79b2d-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="79b2d-147">1000.00</span></span> |
| <span data-ttu-id="79b2d-148">00002</span><span class="sxs-lookup"><span data-stu-id="79b2d-148">00002</span></span>   | <span data-ttu-id="79b2d-149">20. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="79b2d-149">20-01-2015</span></span> | <span data-ttu-id="79b2d-150">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="79b2d-150">Purchase order</span></span> | <span data-ttu-id="79b2d-151">100001</span><span class="sxs-lookup"><span data-stu-id="79b2d-151">100001</span></span> | <span data-ttu-id="79b2d-152">0000101</span><span class="sxs-lookup"><span data-stu-id="79b2d-152">0000101</span></span> |          | <span data-ttu-id="79b2d-153">100,00</span><span class="sxs-lookup"><span data-stu-id="79b2d-153">100.00</span></span>  |
| <span data-ttu-id="79b2d-154">00003</span><span class="sxs-lookup"><span data-stu-id="79b2d-154">00003</span></span>   | <span data-ttu-id="79b2d-155">31. 01. 2015</span><span class="sxs-lookup"><span data-stu-id="79b2d-155">31-01-2015</span></span> | <span data-ttu-id="79b2d-156">Úprava</span><span class="sxs-lookup"><span data-stu-id="79b2d-156">Adjustment</span></span>     | <span data-ttu-id="79b2d-157">100001</span><span class="sxs-lookup"><span data-stu-id="79b2d-157">100001</span></span> | <span data-ttu-id="79b2d-158">0000101</span><span class="sxs-lookup"><span data-stu-id="79b2d-158">0000101</span></span> |          | <span data-ttu-id="79b2d-159">15:00</span><span class="sxs-lookup"><span data-stu-id="79b2d-159">15.00</span></span>   |

<span data-ttu-id="79b2d-160">Stránka **Položky nákladů** umožňuje filtrovat podle ID doklad a data dokladu.</span><span class="sxs-lookup"><span data-stu-id="79b2d-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="79b2d-161">Položky nákladů jsou k dispozici pouze pro [objekty nákladů](cost-object.md) nebo uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="79b2d-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="79b2d-162">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="79b2d-162">Additional resources</span></span>
--------

[<span data-ttu-id="79b2d-163">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="79b2d-163">Cost objects</span></span>](cost-object.md)



