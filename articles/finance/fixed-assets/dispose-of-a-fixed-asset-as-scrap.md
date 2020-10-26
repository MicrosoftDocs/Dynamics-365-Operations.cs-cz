---
title: Zlikvidovat dlouhodobý majetek jako odpad
description: V tématu je popsán postup při odstranění transakcí dlouhodobého majetku, který byl odstraněn jako odpad.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 371cc2efa64916698da8e4230825c3c949920698
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975237"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="6c3d4-103">Zlikvidovat dlouhodobý majetek jako odpad</span><span class="sxs-lookup"><span data-stu-id="6c3d4-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c3d4-104">V tématu je popsán postup při odstranění transakcí dlouhodobého majetku, který byl odstraněn jako odpad.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="6c3d4-105">Typy transakcí, které lze eliminovat, zahrnují pořízení majetku a kumulované transakce odpisů a další transakce dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="6c3d4-106">Eliminace těchto transakcí má vliv na rozvahové účty, jako je například množství úpravy pořizovací ceny, množství úpravy odpisů, přecenění, navýšení a odpisy.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="6c3d4-107">Transakce</span><span class="sxs-lookup"><span data-stu-id="6c3d4-107">Transaction</span></span>                                         | <span data-ttu-id="6c3d4-108">Má dáti (MD)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-108">Debit (Dr.)</span></span> | <span data-ttu-id="6c3d4-109">Dal (D)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="6c3d4-110">MD akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="6c3d4-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="6c3d4-111">X</span><span class="sxs-lookup"><span data-stu-id="6c3d4-111">X</span></span>           |              |
| <span data-ttu-id="6c3d4-112">D zisk/ztráta z dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="6c3d4-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="6c3d4-113">X</span><span class="sxs-lookup"><span data-stu-id="6c3d4-113">X</span></span>            |
| <span data-ttu-id="6c3d4-114">MD zisk/ztráta z dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="6c3d4-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="6c3d4-115">X</span><span class="sxs-lookup"><span data-stu-id="6c3d4-115">X</span></span>           |              |
| <span data-ttu-id="6c3d4-116">D Účet pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="6c3d4-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="6c3d4-117">X</span><span class="sxs-lookup"><span data-stu-id="6c3d4-117">X</span></span>            |
| <span data-ttu-id="6c3d4-118">MD dlouhodobý majetek – zisk/ztráta (zůstatková účetní hodnota \[hodnota NBV\])</span><span class="sxs-lookup"><span data-stu-id="6c3d4-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="6c3d4-119">X</span><span class="sxs-lookup"><span data-stu-id="6c3d4-119">X</span></span>           |              |
| <span data-ttu-id="6c3d4-120">D zisk/ztráta z dlouhodobého majetku (zůstatková účetní hodnota)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="6c3d4-121">X</span><span class="sxs-lookup"><span data-stu-id="6c3d4-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="6c3d4-122">Doporučujeme, abyste úzce spolupracovali s vedoucím finančního oddělení nebo s kontrolorem, který bude identifikovat správné účty, které by měly být použity pro každý typ transakce, a také ověření, zda proces vyřazení a jím generované transakce aktualizují tyto účty správně.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="6c3d4-123">Před vyřazením dlouhodobého majetku jako odpadu je nutné vytvořit účty hlavní knihy, které jsou spojeny s pořizovací hodnotou majetku, odpisy pro aktuální rok, odpisy za předchozí roky a zůstatkovou účetní hodnotou majetku.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="6c3d4-124">Typy transakcí dlouhodobého majetku jsou uvedeny na stránce **Účetní profil dlouhodobého majetku** .</span><span class="sxs-lookup"><span data-stu-id="6c3d4-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="6c3d4-125">Přejděte na **Dlouhodobý majetek \> Nastavení \> Účetní profily dlouhodobého majetku** a pak na pevné záložce **Vyřazení** vyberte **Odpad** v poli nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles** , and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="6c3d4-126">Následující ilustrace znázorňuje seznam typů transakcí dlouhodobého majetku na stránce **Účetní profily dlouhodobého majetku** .</span><span class="sxs-lookup"><span data-stu-id="6c3d4-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="6c3d4-127">[![Likvidace majetku jako odpad, obr. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="6c3d4-128">Pro následující příklad byl dlouhodobý majetek pořízen 1. ledna 2018 a bude zlikvidován 31. března 2019.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="6c3d4-129">**Pořizovací cena:** 24 000,00 USD</span><span class="sxs-lookup"><span data-stu-id="6c3d4-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="6c3d4-130">**Životnost:** dva roky</span><span class="sxs-lookup"><span data-stu-id="6c3d4-130">**Service life:** Two years</span></span>
- <span data-ttu-id="6c3d4-131">**Metoda odpisování:** Lineární doba životnosti</span><span class="sxs-lookup"><span data-stu-id="6c3d4-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="6c3d4-132">**Částka odpisu** : 1 000,00 USD za měsíc</span><span class="sxs-lookup"><span data-stu-id="6c3d4-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="6c3d4-133">Zůstatková účetní hodnota dlouhodobého majetku se vypočte podle následujícího vzorce:</span><span class="sxs-lookup"><span data-stu-id="6c3d4-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="6c3d4-134">Zůstatková účetní hodnota = Pořizovací cena – odpisy</span><span class="sxs-lookup"><span data-stu-id="6c3d4-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="6c3d4-135">V tomto příkladu byl dlouhodobý majetek pořízen a odepisován po dobu 15 měsíců od ledna 2018 do března 2019.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="6c3d4-136">Z toho vyplývá, že zůstatková účetní hodnota majetku je 9 000,00 USD (24 000,00 USD – 15 000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="6c3d4-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="6c3d4-137">[![Příklad odpisu dlouhodobého majetku](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="6c3d4-138">Chcete-li vytvořit deník likvidace, přejděte na **Dlouhodobý majetek \> Položky deníku \> Deník dlouhodobého majetku** a poté v podokně akcí vyberte možnost **Řádky** .</span><span class="sxs-lookup"><span data-stu-id="6c3d4-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal** , and then, on the Action Pane, select **Lines** .</span></span> <span data-ttu-id="6c3d4-139">Vyberte **Vyřazení – likvidace** a poté vyberte ID dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-139">Select **Disposal – scrap** , and then select a fixed asset ID.</span></span> <span data-ttu-id="6c3d4-140">Chcete-li majetek úplně vyřadit, nezadávejte hodnotu do pole **Má dáti** nebo **Dal** .</span><span class="sxs-lookup"><span data-stu-id="6c3d4-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="6c3d4-141">[![Deník dlouhodobého majetku](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="6c3d4-142">Transakce likvidace dlouhodobého majetku mění hodnoty polí pro knihu dlouhodobého majetku následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="6c3d4-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="6c3d4-143">V části **Zůstatek** je pole **Stav** aktualizováno na **Zlikvidovaný** .</span><span class="sxs-lookup"><span data-stu-id="6c3d4-143">In the **Balance** section, the **Status** field is updated to **Scrapped** .</span></span>
- <span data-ttu-id="6c3d4-144">V oddílu **Výdej** je pole **Datum vyřazení** nastaveno na datum, kdy byl majetek zlikvidován.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="6c3d4-145">[![Podrobnosti deníku dlouhodobého majetku](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="6c3d4-146">Zůstatek dlouhodobého majetku je zobrazen na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="6c3d4-147">[![Zůstatek dlouhodobého majetku](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="6c3d4-148">Na následující ilustraci je zobrazen zaúčtovaný doklad.</span><span class="sxs-lookup"><span data-stu-id="6c3d4-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="6c3d4-149">[![Zůstatková účetní hodnota](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="6c3d4-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
