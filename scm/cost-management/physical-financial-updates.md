---
title: "Fyzické a finanční aktualizace"
description: "Toto téma poskytuje přehled typů transakcí, které zvyšují nebo snižují skladové množství."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 07ed503b7c441cb594e8e96ddcd9a81c0745a963
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="e57bb-103">Fyzické a finanční aktualizace</span><span class="sxs-lookup"><span data-stu-id="e57bb-103">Physical and financial updates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e57bb-104">Toto téma poskytuje přehled typů transakcí, které zvyšují nebo snižují skladové množství.</span><span class="sxs-lookup"><span data-stu-id="e57bb-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="e57bb-105">Skladové transakce lze fyzicky nebo finančně aktualizovat v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e57bb-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e57bb-106">Některé typy fyzických a finančních transakcí zvyšují skladové množství, zatímco jiné je snižují.</span><span class="sxs-lookup"><span data-stu-id="e57bb-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="e57bb-107">Fyzické zvýšení</span><span class="sxs-lookup"><span data-stu-id="e57bb-107">Physical increases</span></span>
<span data-ttu-id="e57bb-108">Při zaúčtování fyzické transakce se záznam transakce nachází ve stavu **Přijato**.</span><span class="sxs-lookup"><span data-stu-id="e57bb-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="e57bb-109">Skladové množství fyzicky zvyšují následující transakce:</span><span class="sxs-lookup"><span data-stu-id="e57bb-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="e57bb-110">příjem nákupní objednávky,</span><span class="sxs-lookup"><span data-stu-id="e57bb-110">Purchase order receipt</span></span>
-   <span data-ttu-id="e57bb-111">prodejní objednávka – vrácení dodacího listu,</span><span class="sxs-lookup"><span data-stu-id="e57bb-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="e57bb-112">ohlášení výrobní zakázky jako dokončené,</span><span class="sxs-lookup"><span data-stu-id="e57bb-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="e57bb-113">vedlejší produkt na výdejce výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e57bb-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="e57bb-114">Finanční zvýšení</span><span class="sxs-lookup"><span data-stu-id="e57bb-114">Financial increases</span></span>
<span data-ttu-id="e57bb-115">Při zaúčtování finanční příjmové transakce se záznam transakce zvyšující množství nachází ve stavu **Koupeno**.</span><span class="sxs-lookup"><span data-stu-id="e57bb-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="e57bb-116">Skladové množství finančně zvyšují následující transakce:</span><span class="sxs-lookup"><span data-stu-id="e57bb-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="e57bb-117">Faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="e57bb-117">Vendor invoice</span></span>
-   <span data-ttu-id="e57bb-118">faktura nákupní objednávky pro vrácení,</span><span class="sxs-lookup"><span data-stu-id="e57bb-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="e57bb-119">náklady výrobní zakázky,</span><span class="sxs-lookup"><span data-stu-id="e57bb-119">Production order costing</span></span>
-   <span data-ttu-id="e57bb-120">skladové deníky s kladným množstvím, jako je například pohyb, ztráta a zisk, inventura, kusovníky a převod.</span><span class="sxs-lookup"><span data-stu-id="e57bb-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="e57bb-121">Transakce, které zvyšují množství</span><span class="sxs-lookup"><span data-stu-id="e57bb-121">Transactions that increase quantity</span></span>
<span data-ttu-id="e57bb-122">Transakce zvyšují množství jsou zaúčtovány podle klouzavého průměru nákladové ceny.</span><span class="sxs-lookup"><span data-stu-id="e57bb-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="e57bb-123">Aplikace Dynamics 365 for Finance and Operations vypočítá průběžnou průměrnou nákladovou cenu založenou na cenách jednotlivých transakcí pro jednotlivé dimenze zásob, které jsou finančně sledovány.</span><span class="sxs-lookup"><span data-stu-id="e57bb-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="e57bb-124">Informace o průběžných průměrných nákladových cenách naleznete v tématu [Průběžné průměrné nákladové ceny](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="e57bb-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="e57bb-125">Transakce, které snižují množství</span><span class="sxs-lookup"><span data-stu-id="e57bb-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="e57bb-126">Aplikace Finance and Operations používá vypočtený klouzavý průměr nákladové ceny, když je transakce snižující množství zúčtována, bez ohledu na to, který skladový model je k těmto zásobám přiřazen.</span><span class="sxs-lookup"><span data-stu-id="e57bb-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="e57bb-127">Transakce snižující množství nesmí být označeny pro jinou transakci před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="e57bb-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="e57bb-128">Je-li fyzické množství na skladě záporné, aplikace Finance and Operations použije náklady zásob definované pro danou položku na stránce **Zboží**.</span><span class="sxs-lookup"><span data-stu-id="e57bb-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="e57bb-129">**Poznámka:** Je-li povolena funkce několika pracovišť, náklady budou představovat náklady na zásoby definované pro pracoviště na stránce **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="e57bb-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="e57bb-130">Fyzické výdeje vs finanční výdeje</span><span class="sxs-lookup"><span data-stu-id="e57bb-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="e57bb-131">Při zaúčtování transakce fyzického výdeje se záznam transakce nachází ve stavu **Odečteno**.</span><span class="sxs-lookup"><span data-stu-id="e57bb-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="e57bb-132">Mezi fyzické výdeje patří následující transakce:</span><span class="sxs-lookup"><span data-stu-id="e57bb-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="e57bb-133">výrobní zakázka - deník výdejek,</span><span class="sxs-lookup"><span data-stu-id="e57bb-133">Production order picking list journal</span></span>
-   <span data-ttu-id="e57bb-134">prodejní objednávka – dodací list,</span><span class="sxs-lookup"><span data-stu-id="e57bb-134">Sales order packing slip</span></span>
-   <span data-ttu-id="e57bb-135">nákupní objednávka – vrácení dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="e57bb-135">Purchase order packing slip return</span></span>

<span data-ttu-id="e57bb-136">Při zaúčtování finanční transakce se záznam transakce nachází ve stavu **Prodáno**.</span><span class="sxs-lookup"><span data-stu-id="e57bb-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="e57bb-137">Mezi finanční výdeje patří následující transakce:</span><span class="sxs-lookup"><span data-stu-id="e57bb-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="e57bb-138">Ukončení výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="e57bb-138">Ending a production order</span></span>
-   <span data-ttu-id="e57bb-139">faktura prodejní objednávky,</span><span class="sxs-lookup"><span data-stu-id="e57bb-139">Sales order invoice</span></span>
-   <span data-ttu-id="e57bb-140">Vrácení faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="e57bb-140">Vendor invoice return</span></span>
-   <span data-ttu-id="e57bb-141">skladové deníky se záporným množstvím, jako je například pohyb, ztráta a zisk, inventura, kusovníky a převod.</span><span class="sxs-lookup"><span data-stu-id="e57bb-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="e57bb-142">Transakce snižující množství jsou zaúčtovány podle klouzavého průměru nákladové ceny.</span><span class="sxs-lookup"><span data-stu-id="e57bb-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="e57bb-143">Proces uzávěrky skladu je tedy vyžadován pro vyrovnání výdejových transakcí příjmovými transakcemi podle modelu zásob, která je přiřazen jednotlivým položkám.</span><span class="sxs-lookup"><span data-stu-id="e57bb-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




