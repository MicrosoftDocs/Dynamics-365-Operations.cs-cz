---
title: Odstraňování potíží s konfigurací skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při konfiguraci aplikace Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993996"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="59d2f-103">Odstraňování potíží s konfigurací skladu</span><span class="sxs-lookup"><span data-stu-id="59d2f-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59d2f-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při konfiguraci aplikace Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="59d2f-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="59d2f-105">Zobrazuje se následující chybová zpráva: „Registrační značka nebo skladové místo nejsou platné.“</span><span class="sxs-lookup"><span data-stu-id="59d2f-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-106">Issue description</span></span>

<span data-ttu-id="59d2f-107">Tato chybová zpráva se zobrazí při skenování ID registrační značky nebo skladového místa.</span><span class="sxs-lookup"><span data-stu-id="59d2f-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-108">Issue resolution</span></span>

<span data-ttu-id="59d2f-109">Ujistěte se, že ID registrační značky není rezervováno něčím jiným.</span><span class="sxs-lookup"><span data-stu-id="59d2f-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="59d2f-110">K tomuto problému docházelo, když hodnota, kterou uživatel naskenoval v aplikaci skladu, byla platným skladovým místem i platným ID registrační značky.</span><span class="sxs-lookup"><span data-stu-id="59d2f-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="59d2f-111">Tento problém byl však vyřešen ve verzi 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="59d2f-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="59d2f-112">Zobrazuje se následující chybová zpráva: „Pro toto skladové místo musí být určena registrační značka.“</span><span class="sxs-lookup"><span data-stu-id="59d2f-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-113">Issue description</span></span>

<span data-ttu-id="59d2f-114">Tato chybová zpráva se zobrazí, pokud vytvoříte převodní příkaz pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku.</span><span class="sxs-lookup"><span data-stu-id="59d2f-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-115">Issue resolution</span></span>

<span data-ttu-id="59d2f-116">Pole **Výchozí skladové místo příjmu** je prázdné pro tranzitní sklad ze skladu.</span><span class="sxs-lookup"><span data-stu-id="59d2f-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="59d2f-117">Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu.</span><span class="sxs-lookup"><span data-stu-id="59d2f-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="59d2f-118">Ujistěte se, že toto umístění je řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="59d2f-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="59d2f-119">Zobrazuje se následující chybová zpráva: „Nelze vytvořit řádek pracovní šablony pro změnu stavu zásob, protože typ práce není platný.</span><span class="sxs-lookup"><span data-stu-id="59d2f-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="59d2f-120">Vyberte jiný typ práce.“</span><span class="sxs-lookup"><span data-stu-id="59d2f-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-121">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-121">Issue description</span></span>

<span data-ttu-id="59d2f-122">U pracovní šablony nemůžete vybrat *Změna stavu zásob* ve sloupci **Typ práce** sekce **Podrobnosti pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="59d2f-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-123">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-123">Issue resolution</span></span>

<span data-ttu-id="59d2f-124">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="59d2f-124">This behavior is by design.</span></span> <span data-ttu-id="59d2f-125">Typ práce *Změna stavu zásob* používají pouze systémové procesy.</span><span class="sxs-lookup"><span data-stu-id="59d2f-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="59d2f-126">Tento údaj nelze nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="59d2f-126">It can't be configured.</span></span> <span data-ttu-id="59d2f-127">Vzhledem k tomu, že seznam typů práce je opraven jako výčet, nelze nadbytečné položky odfiltrovat z rozevírací nabídky **Typ práce**.</span><span class="sxs-lookup"><span data-stu-id="59d2f-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="59d2f-128">Zobrazuje se následující chybová zpráva: „Množství není platné pro jednotku 1%.“</span><span class="sxs-lookup"><span data-stu-id="59d2f-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-129">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-129">Issue description</span></span>

<span data-ttu-id="59d2f-130">Množství není platné pro jednotku *ea* při práci výdeje, která má na jednom místě více registračních značek.</span><span class="sxs-lookup"><span data-stu-id="59d2f-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-131">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-131">Issue resolution</span></span>

<span data-ttu-id="59d2f-132">Ověřte, že pole **ID skupiny pořadí jednotek** a **Převody jednotek** na uvolněném produktu nebo variantě produktu jsou nastavena správně.</span><span class="sxs-lookup"><span data-stu-id="59d2f-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="59d2f-133">Upozorňujeme, že ve verzi 10.0.15 byla vylepšena chybová zpráva (viz [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="59d2f-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="59d2f-134">Nová chybová zpráva zní: „Množství není platné.</span><span class="sxs-lookup"><span data-stu-id="59d2f-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="59d2f-135">Očekáváno %1 %2."</span><span class="sxs-lookup"><span data-stu-id="59d2f-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="59d2f-136">Ve směrnicích skladového místa pro práci vložení prodejní objednávky neuvádí možnost více SKU vyhodnocení více akcí směrnic skladového místa.</span><span class="sxs-lookup"><span data-stu-id="59d2f-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-137">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-137">Issue description</span></span>

<span data-ttu-id="59d2f-138">Směrnice skladového místa typu pracovního příkazu *Prodejní objednávky* a typu práce *Vložení* nehodnotí více akcí směrnic skladového místa, když je vybrána možnost **Vícenásobné SKU**.</span><span class="sxs-lookup"><span data-stu-id="59d2f-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="59d2f-139">Vyhodnocuje se pouze první akce směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="59d2f-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-140">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-140">Issue resolution</span></span>

<span data-ttu-id="59d2f-141">Ve verzi 10.0.15 byla přidána nová funkce *Vyhodnocení všech akcí pro směrnice skladového místa vícenásobného SKU* (viz [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="59d2f-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="59d2f-142">Tato funkce vyhodnocuje všechny akce pro směrnice skladového místa vícenásobného SKU.</span><span class="sxs-lookup"><span data-stu-id="59d2f-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="59d2f-143">Pokud požadujete tuto funkci, použijte [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k jejímu zapnutí.</span><span class="sxs-lookup"><span data-stu-id="59d2f-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="59d2f-144">K částečnému výdeji nemohu použít aplikaci skladu.</span><span class="sxs-lookup"><span data-stu-id="59d2f-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-145">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-145">Issue description</span></span>

<span data-ttu-id="59d2f-146">U prodejních objednávek a převodních příkazů nemůžete položky přeskočit a provést částečný výdej.</span><span class="sxs-lookup"><span data-stu-id="59d2f-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-147">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-147">Issue resolution</span></span>

<span data-ttu-id="59d2f-148">Na stránce **Položky nabídky mobilního zařízení** příkapro každou položku nabídky, která je nastavena na zpracování prodejních objednávek nebo převodních příkazů, nastavte možnost **Povolit rozdělení práce** na záložce s náhledem **Obecné** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="59d2f-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="59d2f-149">Jak mohu provést změnu stavu zásob u práce částečného množství?</span><span class="sxs-lookup"><span data-stu-id="59d2f-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="59d2f-150">Popis problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-150">Issue description</span></span>

<span data-ttu-id="59d2f-151">Chcete provést změnu stavu zásob u částečného množství dávky.</span><span class="sxs-lookup"><span data-stu-id="59d2f-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="59d2f-152">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="59d2f-152">Issue resolution</span></span>

<span data-ttu-id="59d2f-153">Chcete-li pracovníkům umožnit tuto změnu, můžete vytvořit položku nabídky pro aplikaci skladu.</span><span class="sxs-lookup"><span data-stu-id="59d2f-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="59d2f-154">Na stránce **Položky nabídky mobilního zařízení** vytvořte (nebo upravte) položku nabídky, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="59d2f-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="59d2f-155">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="59d2f-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="59d2f-156">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="59d2f-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="59d2f-157">**Proces tvorby práce:** *Pohyb*</span><span class="sxs-lookup"><span data-stu-id="59d2f-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="59d2f-158">**Zobrazit stav zásob:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="59d2f-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="59d2f-159">Na stránce můžete podle potřeby nastavit další pole.</span><span class="sxs-lookup"><span data-stu-id="59d2f-159">You can set other fields on the page as you require.</span></span>
