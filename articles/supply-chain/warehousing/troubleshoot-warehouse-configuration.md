---
title: Odstraňování potíží s konfigurací skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při konfiguraci aplikace Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814385"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="4810c-103">Odstraňování potíží s konfigurací skladu</span><span class="sxs-lookup"><span data-stu-id="4810c-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4810c-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při konfiguraci aplikace Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4810c-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="4810c-105">Zobrazuje se následující chybová zpráva: „Registrační značka nebo skladové místo nejsou platné.“</span><span class="sxs-lookup"><span data-stu-id="4810c-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-106">Issue description</span></span>

<span data-ttu-id="4810c-107">Tato chybová zpráva se zobrazí při skenování ID registrační značky nebo skladového místa.</span><span class="sxs-lookup"><span data-stu-id="4810c-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-108">Issue resolution</span></span>

<span data-ttu-id="4810c-109">Ujistěte se, že ID registrační značky není rezervováno něčím jiným.</span><span class="sxs-lookup"><span data-stu-id="4810c-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="4810c-110">K tomuto problému docházelo, když hodnota, kterou uživatel naskenoval v mobilní aplikaci Řízení skladu, byla platným skladovým místem i platným ID registrační značky.</span><span class="sxs-lookup"><span data-stu-id="4810c-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="4810c-111">Tento problém byl však vyřešen ve verzi 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="4810c-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="4810c-112">Zobrazuje se následující chybová zpráva: „Pro toto skladové místo musí být určena registrační značka.“</span><span class="sxs-lookup"><span data-stu-id="4810c-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-113">Issue description</span></span>

<span data-ttu-id="4810c-114">Tato chybová zpráva se zobrazí, pokud vytvoříte převodní příkaz pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku.</span><span class="sxs-lookup"><span data-stu-id="4810c-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-115">Issue resolution</span></span>

<span data-ttu-id="4810c-116">Pole **Výchozí skladové místo příjmu** je prázdné pro tranzitní sklad ze skladu.</span><span class="sxs-lookup"><span data-stu-id="4810c-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="4810c-117">Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu.</span><span class="sxs-lookup"><span data-stu-id="4810c-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="4810c-118">Ujistěte se, že toto umístění je řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="4810c-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="4810c-119">Zobrazuje se následující chybová zpráva: „Nelze vytvořit řádek pracovní šablony pro změnu stavu zásob, protože typ práce není platný.</span><span class="sxs-lookup"><span data-stu-id="4810c-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="4810c-120">Vyberte jiný typ práce.“</span><span class="sxs-lookup"><span data-stu-id="4810c-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-121">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-121">Issue description</span></span>

<span data-ttu-id="4810c-122">U pracovní šablony nemůžete vybrat *Změna stavu zásob* ve sloupci **Typ práce** sekce **Podrobnosti pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="4810c-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-123">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-123">Issue resolution</span></span>

<span data-ttu-id="4810c-124">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="4810c-124">This behavior is by design.</span></span> <span data-ttu-id="4810c-125">Typ práce *Změna stavu zásob* používají pouze systémové procesy.</span><span class="sxs-lookup"><span data-stu-id="4810c-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="4810c-126">Tento údaj nelze nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="4810c-126">It can't be configured.</span></span> <span data-ttu-id="4810c-127">Vzhledem k tomu, že seznam typů práce je opraven jako výčet, nelze nadbytečné položky odfiltrovat z rozevírací nabídky **Typ práce**.</span><span class="sxs-lookup"><span data-stu-id="4810c-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="4810c-128">Zobrazuje se následující chybová zpráva: „Množství není platné pro jednotku 1%.“</span><span class="sxs-lookup"><span data-stu-id="4810c-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-129">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-129">Issue description</span></span>

<span data-ttu-id="4810c-130">Množství není platné pro jednotku *ea* při práci výdeje, která má na jednom místě více registračních značek.</span><span class="sxs-lookup"><span data-stu-id="4810c-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-131">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-131">Issue resolution</span></span>

<span data-ttu-id="4810c-132">Ověřte, že pole **ID skupiny pořadí jednotek** a **Převody jednotek** na uvolněném produktu nebo variantě produktu jsou nastavena správně.</span><span class="sxs-lookup"><span data-stu-id="4810c-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="4810c-133">Upozorňujeme, že ve verzi 10.0.15 byla vylepšena chybová zpráva (viz [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="4810c-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="4810c-134">Nová chybová zpráva zní: „Množství není platné.</span><span class="sxs-lookup"><span data-stu-id="4810c-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="4810c-135">Očekáváno %1 %2."</span><span class="sxs-lookup"><span data-stu-id="4810c-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="4810c-136">Ve směrnicích skladového místa pro práci vložení prodejní objednávky neuvádí možnost více SKU vyhodnocení více akcí směrnic skladového místa.</span><span class="sxs-lookup"><span data-stu-id="4810c-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-137">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-137">Issue description</span></span>

<span data-ttu-id="4810c-138">Směrnice skladového místa typu pracovního příkazu *Prodejní objednávky* a typu práce *Vložení* nehodnotí více akcí směrnic skladového místa, když je vybrána možnost **Vícenásobné SKU**.</span><span class="sxs-lookup"><span data-stu-id="4810c-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="4810c-139">Vyhodnocuje se pouze první akce směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="4810c-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-140">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-140">Issue resolution</span></span>

<span data-ttu-id="4810c-141">Ve verzi 10.0.15 byla přidána nová funkce *Vyhodnocení všech akcí pro směrnice skladového místa vícenásobného SKU* (viz [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="4810c-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="4810c-142">Tato funkce vyhodnocuje všechny akce pro směrnice skladového místa vícenásobného SKU.</span><span class="sxs-lookup"><span data-stu-id="4810c-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="4810c-143">Pokud požadujete tuto funkci, použijte [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k jejímu zapnutí.</span><span class="sxs-lookup"><span data-stu-id="4810c-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="4810c-144">K částečnému výdeji nemohu použít mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="4810c-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-145">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-145">Issue description</span></span>

<span data-ttu-id="4810c-146">U prodejních objednávek a převodních příkazů nemůžete položky přeskočit a provést částečný výdej.</span><span class="sxs-lookup"><span data-stu-id="4810c-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-147">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-147">Issue resolution</span></span>

<span data-ttu-id="4810c-148">Na stránce **Položky nabídky mobilního zařízení** příkapro každou položku nabídky, která je nastavena na zpracování prodejních objednávek nebo převodních příkazů, nastavte možnost **Povolit rozdělení práce** na záložce s náhledem **Obecné** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="4810c-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="4810c-149">Jak mohu provést změnu stavu zásob u práce částečného množství?</span><span class="sxs-lookup"><span data-stu-id="4810c-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-150">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-150">Issue description</span></span>

<span data-ttu-id="4810c-151">Chcete provést změnu stavu zásob u částečného množství dávky.</span><span class="sxs-lookup"><span data-stu-id="4810c-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-152">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-152">Issue resolution</span></span>

<span data-ttu-id="4810c-153">Chcete-li pracovníkům umožnit tuto změnu, můžete vytvořit položku nabídky pro mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="4810c-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="4810c-154">Na stránce **Položky nabídky mobilního zařízení** vytvořte (nebo upravte) položku nabídky, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="4810c-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="4810c-155">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="4810c-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="4810c-156">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="4810c-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="4810c-157">**Proces tvorby práce:** *Pohyb*</span><span class="sxs-lookup"><span data-stu-id="4810c-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="4810c-158">**Zobrazit stav zásob:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="4810c-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="4810c-159">Na stránce můžete podle potřeby nastavit další pole.</span><span class="sxs-lookup"><span data-stu-id="4810c-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="4810c-160">Profil správy dokování profilu umístění nebrání smíšení typů zásob.</span><span class="sxs-lookup"><span data-stu-id="4810c-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4810c-161">Popis problému</span><span class="sxs-lookup"><span data-stu-id="4810c-161">Issue description</span></span>

<span data-ttu-id="4810c-162">Používáte *zásady konsolidace dodávky*.</span><span class="sxs-lookup"><span data-stu-id="4810c-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="4810c-163">Nastavili jste *profil správy doku* pro *profil umístění*, ale když je práce vytvořena, typy zásob se v konečném umístění smíchají.</span><span class="sxs-lookup"><span data-stu-id="4810c-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4810c-164">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="4810c-164">Issue resolution</span></span>

<span data-ttu-id="4810c-165">Profily správy doků vyžadují, aby byla práce předem rozdělena.</span><span class="sxs-lookup"><span data-stu-id="4810c-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="4810c-166">Jinými slovy, profil správy doku očekává, že pracovní záhlaví nebude mít více umístění pro vložení.</span><span class="sxs-lookup"><span data-stu-id="4810c-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="4810c-167">Aby profil správy doku mohl efektivně spravovat míchání zásob, musí být nastaveno zalomení pracovní hlavičky.</span><span class="sxs-lookup"><span data-stu-id="4810c-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="4810c-168">V tomto příkladu je náš profil správy doku nakonfigurován tak, že hodnota **Typy zásob, které by se neměly kombinovat** je nastavena na *ID zásilky* a nastavíme pro ni zalomení pracovní hlavičky:</span><span class="sxs-lookup"><span data-stu-id="4810c-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="4810c-169">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="4810c-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4810c-170">Vyberte **Typ pracovního příkazu** pro úpravu (například *Nákupní objednávky*).</span><span class="sxs-lookup"><span data-stu-id="4810c-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="4810c-171">Vyberte pracovní šablonu, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="4810c-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="4810c-172">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="4810c-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="4810c-173">Otevřete kartu **Řazení** a přidejte řádek s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="4810c-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="4810c-174">**Tabulka** - *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="4810c-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="4810c-175">**Odvozená tabulka** - *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="4810c-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="4810c-176">**Pole** - *ID dodávky*</span><span class="sxs-lookup"><span data-stu-id="4810c-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="4810c-177">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4810c-177">Select **OK**.</span></span>
1. <span data-ttu-id="4810c-178">Vrátíte se na stránku **Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="4810c-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="4810c-179">V podokně akcí vyberte **Zalomení pracovních hlaviček**.</span><span class="sxs-lookup"><span data-stu-id="4810c-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="4810c-180">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="4810c-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4810c-181">Zaškrtněte políčko spojené s **Název pole** *ID zásilky*.</span><span class="sxs-lookup"><span data-stu-id="4810c-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="4810c-182">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4810c-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
