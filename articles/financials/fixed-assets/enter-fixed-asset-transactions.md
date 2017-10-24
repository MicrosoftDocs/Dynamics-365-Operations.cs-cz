---
title: "Transakce dlouhodobého majetku"
description: "Tento článek popisuje různé dostupné metody pro vytvoření transakcí dlouhodobého majetku."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="0b552-103">Transakce dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="0b552-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0b552-104">Tento článek popisuje různé dostupné metody pro vytvoření transakcí dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="0b552-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="0b552-105">Dlouhodobý majetek lze nastavit pro účely integrace se závazky, pohledávkami, zprostředkováním a zajištěním zdrojů a hlavní knihou.</span><span class="sxs-lookup"><span data-stu-id="0b552-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="0b552-106">Položky lze rovněž převádět ve správě zásob na dlouhodobý majetek pro vnitřní použití.</span><span class="sxs-lookup"><span data-stu-id="0b552-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="0b552-107">Závazky</span><span class="sxs-lookup"><span data-stu-id="0b552-107">Accounts payable</span></span>
<span data-ttu-id="0b552-108">Transakce s dlouhodobým majetkem lze zadat na stránce Doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="0b552-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="0b552-109">Tuto stránku lze otevřít ze stránky Deník faktur.</span><span class="sxs-lookup"><span data-stu-id="0b552-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="0b552-110">Stránku Doklad deníku můžete otevřít také ze stránky Deník schválených faktur.</span><span class="sxs-lookup"><span data-stu-id="0b552-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="0b552-111">V poli Typ protiúčtu vyberte možnost Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="0b552-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="0b552-112">Pak v poli Protiúčet vyberte číslo dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="0b552-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="0b552-113">Na kartě Dlouhodobý majetek zadejte hodnoty do polí Typ transakce a Kniha.</span><span class="sxs-lookup"><span data-stu-id="0b552-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="0b552-114">Pohledávky</span><span class="sxs-lookup"><span data-stu-id="0b552-114">Accounts receivable</span></span>
<span data-ttu-id="0b552-115">Transakce s dlouhodobým majetkem lze zadat na stránce Volná faktura.</span><span class="sxs-lookup"><span data-stu-id="0b552-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="0b552-116">Na stránce Volná faktura v mřížce Řádky faktury vyberte položku řádku.</span><span class="sxs-lookup"><span data-stu-id="0b552-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="0b552-117">Klikněte na pevnou záložku Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="0b552-117">Click the Line details FastTab.</span></span> <span data-ttu-id="0b552-118">Zadejte číslo dlouhodobého majetku a knihu transakce vyřazení.</span><span class="sxs-lookup"><span data-stu-id="0b552-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="0b552-119">U faktur s volným textem je druh transakce s dlouhodobým majetkem vždy definován jako možnost Vyřazení – odprodej.</span><span class="sxs-lookup"><span data-stu-id="0b552-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="0b552-120">Zásobování a zdroje</span><span class="sxs-lookup"><span data-stu-id="0b552-120">Procurement and sourcing</span></span>
<span data-ttu-id="0b552-121">Transakce s dlouhodobým majetkem lze zadat na stránce Nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="0b552-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="0b552-122">Zadejte požadované informace pro vytvoření nákupní objednávky a klikněte na OK.</span><span class="sxs-lookup"><span data-stu-id="0b552-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="0b552-123">Na stránce Nákupní objednávka klikněte na pevnou záložku Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="0b552-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="0b552-124">Potom na kartě Dlouhodobý majetek zadejte informace o dlouhodobém majetku.</span><span class="sxs-lookup"><span data-stu-id="0b552-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="0b552-125">Chcete-li zaúčtovat transakci pořízení pro existující položku dlouhodobého majetku, určete číslo položky dlouhodobého majetku, knihu a typ transakce.</span><span class="sxs-lookup"><span data-stu-id="0b552-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="0b552-126">Dlouhodobý majetek nelze zaúčtovat, pokud chybí některá z těchto informací.</span><span class="sxs-lookup"><span data-stu-id="0b552-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="0b552-127">Chcete-li zaúčtovat transakci pořízení pro novou položku dlouhodobého majetku, vyberte možnost Nový dlouhodobý majetek? a potom vyberte skupinu pevného majetku, do níž má být nová položka majetku přiřazena.</span><span class="sxs-lookup"><span data-stu-id="0b552-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="0b552-128">Pokud se však položka nachází ve skupině skladových modelů, která používá skladový model standardních nákladů, nebudou žádná z polí dlouhodobého majetku pro daný řádek dostupná.</span><span class="sxs-lookup"><span data-stu-id="0b552-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="0b552-129">Dále volby definované na stránce Parametry dlouhodobého majetku určují, zda můžete zaúčtovat transakce pořízení z nákupních modulů.</span><span class="sxs-lookup"><span data-stu-id="0b552-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="0b552-130">Pokud se pro pořízení dlouhodobého majetku použije nákupní objednávka nebo skladový deník dlouhodobého majetku, bude ovlivněna hodnota zásob.</span><span class="sxs-lookup"><span data-stu-id="0b552-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="0b552-131">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="0b552-131">General ledger</span></span>
<span data-ttu-id="0b552-132">Kterýkoliv typ transakce s dlouhodobým majetkem lze zaúčtovat na stránce Hlavní deník.</span><span class="sxs-lookup"><span data-stu-id="0b552-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="0b552-133">K zaúčtování transakcí můžete také použít deníky ve formuláři Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="0b552-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="0b552-134">Volby pro zadání typů transakcí s dlouhodobým majetkem</span><span class="sxs-lookup"><span data-stu-id="0b552-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="0b552-135">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="0b552-135">Transaction type</span></span>                    | <span data-ttu-id="0b552-136">Modul</span><span class="sxs-lookup"><span data-stu-id="0b552-136">Module</span></span>                   | <span data-ttu-id="0b552-137">Možnosti</span><span class="sxs-lookup"><span data-stu-id="0b552-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="0b552-138">Pořízení, Oprava pořizovací ceny</span><span class="sxs-lookup"><span data-stu-id="0b552-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="0b552-139">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="0b552-139">Fixed assets</span></span>             | <span data-ttu-id="0b552-140">Dlouhodobý majetek, Skladový deník dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="0b552-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="0b552-141">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="0b552-141">General ledger</span></span>           | <span data-ttu-id="0b552-142">Hlavní deník</span><span class="sxs-lookup"><span data-stu-id="0b552-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="0b552-143">Závazky</span><span class="sxs-lookup"><span data-stu-id="0b552-143">Accounts payable</span></span>         | <span data-ttu-id="0b552-144">Deník faktur, Deník schválených faktur</span><span class="sxs-lookup"><span data-stu-id="0b552-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="0b552-145">Zásobování a zdroje</span><span class="sxs-lookup"><span data-stu-id="0b552-145">Procurement and sourcing</span></span> | <span data-ttu-id="0b552-146">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="0b552-146">Purchase order</span></span>                            |
| <span data-ttu-id="0b552-147">Odpisy</span><span class="sxs-lookup"><span data-stu-id="0b552-147">Depreciation</span></span>                        | <span data-ttu-id="0b552-148">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="0b552-148">Fixed assets</span></span>             | <span data-ttu-id="0b552-149">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="0b552-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="0b552-150">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="0b552-150">General ledger</span></span>           | <span data-ttu-id="0b552-151">Hlavní deník</span><span class="sxs-lookup"><span data-stu-id="0b552-151">General journal</span></span>                           |
| <span data-ttu-id="0b552-152">Vyřazení</span><span class="sxs-lookup"><span data-stu-id="0b552-152">Disposal</span></span>                            | <span data-ttu-id="0b552-153">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="0b552-153">Fixed assets</span></span>             | <span data-ttu-id="0b552-154">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="0b552-154">Fixed assets</span></span>                              |
| <span data-ttu-id="0b552-155">** **</span><span class="sxs-lookup"><span data-stu-id="0b552-155">** **</span></span>                               | <span data-ttu-id="0b552-156">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="0b552-156">General ledger</span></span>           | <span data-ttu-id="0b552-157">Hlavní deník</span><span class="sxs-lookup"><span data-stu-id="0b552-157">General journal</span></span>                           |
| <span data-ttu-id="0b552-158">** **</span><span class="sxs-lookup"><span data-stu-id="0b552-158">** **</span></span>                               | <span data-ttu-id="0b552-159">Pohledávky</span><span class="sxs-lookup"><span data-stu-id="0b552-159">Accounts receivable</span></span>      | <span data-ttu-id="0b552-160">Volné faktury</span><span class="sxs-lookup"><span data-stu-id="0b552-160">Free text invoice</span></span>                         |



<span data-ttu-id="0b552-161">Další informace naleznete v tématu [Integrace dlouhodobého majetku](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="0b552-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




