---
title: Zaúčtování online prodeje a plateb
description: Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140776"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="69623-103">Zaúčtování online prodeje a plateb</span><span class="sxs-lookup"><span data-stu-id="69623-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69623-104">Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.</span><span class="sxs-lookup"><span data-stu-id="69623-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="69623-105">Účtování online prodejů a plateb je dvoustupňový proces.</span><span class="sxs-lookup"><span data-stu-id="69623-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="69623-106">Probíhá přijímání dat obchodní transakce online do HQ.</span><span class="sxs-lookup"><span data-stu-id="69623-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="69623-107">Synchronizace objednávek za účelem vytvoření prodejních objednávek v HQ.</span><span class="sxs-lookup"><span data-stu-id="69623-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="69623-108">Přenášení dat online transakce lze provést buď ručním spuštěním úlohy P nebo vytvořením opakující se dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="69623-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="69623-109">Ruční spuštění úlohy P.</span><span class="sxs-lookup"><span data-stu-id="69623-109">Manually running the P-job</span></span>

1. <span data-ttu-id="69623-110">Přejděte na Všechny pracovní prostory > Maloobchodní a velkoobchodní IT.</span><span class="sxs-lookup"><span data-stu-id="69623-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="69623-111">Klikněte na Plán distribuce</span><span class="sxs-lookup"><span data-stu-id="69623-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="69623-112">Vyberte P-0001.</span><span class="sxs-lookup"><span data-stu-id="69623-112">Select P-0001.</span></span>
4. <span data-ttu-id="69623-113">V případě potřeby upravte skupiny databáze kanálů.</span><span class="sxs-lookup"><span data-stu-id="69623-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="69623-114">Klikněte na možnost Spustit.</span><span class="sxs-lookup"><span data-stu-id="69623-114">Click Run now.</span></span>
6. <span data-ttu-id="69623-115">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="69623-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="69623-116">Plánování opakované úlohy P.</span><span class="sxs-lookup"><span data-stu-id="69623-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="69623-117">Přejděte na Všechny pracovní prostory > Maloobchodní a velkoobchodní IT.</span><span class="sxs-lookup"><span data-stu-id="69623-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="69623-118">Klikněte na Plán distribuce</span><span class="sxs-lookup"><span data-stu-id="69623-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="69623-119">Vyberte P-0001.</span><span class="sxs-lookup"><span data-stu-id="69623-119">Select P-0001.</span></span>
4. <span data-ttu-id="69623-120">Klikněte na Vytvořit dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="69623-120">Click Create batch job.</span></span>
5. <span data-ttu-id="69623-121">Klikněte na Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="69623-121">Click Run in the background.</span></span>
5. <span data-ttu-id="69623-122">Povolte Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="69623-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="69623-123">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="69623-123">Click Recurrence..</span></span>
7. <span data-ttu-id="69623-124">Vyberte možnost Bez koncového data.</span><span class="sxs-lookup"><span data-stu-id="69623-124">Select the No end date option.</span></span>
8. <span data-ttu-id="69623-125">Do pole Počet zadejte interval mezi spuštěními v minutách.</span><span class="sxs-lookup"><span data-stu-id="69623-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="69623-126">Obvykle by to bylo 5-10.</span><span class="sxs-lookup"><span data-stu-id="69623-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="69623-127">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="69623-127">Click OK.</span></span>
10. <span data-ttu-id="69623-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="69623-128">Click OK.</span></span>

<span data-ttu-id="69623-129">Objednávky lze synchronizovat buď ručně spuštěním úlohy „Synchronizace objednávek“ nebo vytvořením opakované dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="69623-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="69623-130">Ruční spuštění synchronizace objednávek</span><span class="sxs-lookup"><span data-stu-id="69623-130">Manually running order synchronization</span></span> 

<span data-ttu-id="69623-131">Chcete-li ručně spustit úlohu „Synchronizovat objednávky“, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="69623-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="69623-132">Přejděte na Všechny pracovní prostory > Uložit finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="69623-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="69623-133">Klikněte na Synchronizovat objednávky.</span><span class="sxs-lookup"><span data-stu-id="69623-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="69623-134">Vyberte „Obchody podle regionu“ v poli Organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="69623-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="69623-135">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod online nebo vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="69623-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="69623-136">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="69623-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="69623-137">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="69623-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="69623-138">Zakažte Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="69623-138">Disable Batch processing</span></span>
6. <span data-ttu-id="69623-139">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="69623-139">Click Recurrence.</span></span>
7. <span data-ttu-id="69623-140">Vyberte možnost Konec po</span><span class="sxs-lookup"><span data-stu-id="69623-140">Select End After option</span></span>
8. <span data-ttu-id="69623-141">Do pole Konec po zadejte hodnotu 1.</span><span class="sxs-lookup"><span data-stu-id="69623-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="69623-142">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="69623-142">Click OK.</span></span>
10. <span data-ttu-id="69623-143">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="69623-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="69623-144">Plánování opakované synchronizace objednávek</span><span class="sxs-lookup"><span data-stu-id="69623-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="69623-145">Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.</span><span class="sxs-lookup"><span data-stu-id="69623-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="69623-146">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="69623-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="69623-147">Přejděte na Všechny pracovní prostory > Uložit finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="69623-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="69623-148">Klikněte na Synchronizovat objednávky.</span><span class="sxs-lookup"><span data-stu-id="69623-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="69623-149">Vyberte „Obchody podle regionu“ v poli Organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="69623-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="69623-150">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod online nebo vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="69623-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="69623-151">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="69623-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="69623-152">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="69623-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="69623-153">Povolte Dávkové zpracování</span><span class="sxs-lookup"><span data-stu-id="69623-153">Enable Batch processing</span></span>
6. <span data-ttu-id="69623-154">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="69623-154">Click Recurrence.</span></span>
7. <span data-ttu-id="69623-155">Vyberte možnost Bez koncového data.</span><span class="sxs-lookup"><span data-stu-id="69623-155">Select the No end date option.</span></span>
8. <span data-ttu-id="69623-156">Do pole Počet zadejte interval mezi spuštěními v minutách.</span><span class="sxs-lookup"><span data-stu-id="69623-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="69623-157">Obvykle by to bylo 2-20.</span><span class="sxs-lookup"><span data-stu-id="69623-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="69623-158">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="69623-158">Click OK.</span></span>
10. <span data-ttu-id="69623-159">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="69623-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="69623-160">Datové entity zahrnuté do procesu</span><span class="sxs-lookup"><span data-stu-id="69623-160">Data entities involved in the process</span></span>

- <span data-ttu-id="69623-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="69623-161">RetailTransactionTable</span></span>
- <span data-ttu-id="69623-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="69623-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="69623-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="69623-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="69623-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="69623-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="69623-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="69623-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="69623-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="69623-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="69623-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="69623-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="69623-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="69623-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="69623-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="69623-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="69623-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="69623-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="69623-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="69623-171">RetailTransactionAttributeTrans</span></span>
