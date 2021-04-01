---
title: Odstraňování potíží se sestavením nákladu a dodávkami
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími se setavením a dodávkami nákladu v Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: c7dc9cc9de4d5089d497c36759931669ee2e9e55
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259499"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="05d0d-103">Odstraňování potíží se sestavením nákladu a dodávkami</span><span class="sxs-lookup"><span data-stu-id="05d0d-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05d0d-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími se setavením a dodávkami nákladu v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="05d0d-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="05d0d-105">Zobrazuje se následující chybová zpráva: „Nelze vytvořit řádek nákladu pro tento řádek objednávky, protože obsahuje neplatné dimenze inventáře ...“</span><span class="sxs-lookup"><span data-stu-id="05d0d-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="05d0d-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-106">Issue description</span></span>

<span data-ttu-id="05d0d-107">Při pokusu o uvolnění objednávky prodejní vratky do skladu se zobrazí následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="05d0d-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="05d0d-108">Nelze vytvořit řádek nákladu pro tento řádek objednávky, protože obsahuje neplatné dimenze inventáře.</span><span class="sxs-lookup"><span data-stu-id="05d0d-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="05d0d-109">V hierarchii rezervací nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí umístění.</span><span class="sxs-lookup"><span data-stu-id="05d0d-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="05d0d-110">Odeberte neplatné rozměry z řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="05d0d-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05d0d-111">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-111">Issue resolution</span></span>

<span data-ttu-id="05d0d-112">Produkt bohužel nepodporuje zpracování nákladu pro proces vrácení prodeje.</span><span class="sxs-lookup"><span data-stu-id="05d0d-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="05d0d-113">Proto nemůžete uvolnit objednávku prodejní vratky do skladu.</span><span class="sxs-lookup"><span data-stu-id="05d0d-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="05d0d-114">V transakcích prodejní objednávky nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí **umístění** v hierarchii rezervací.</span><span class="sxs-lookup"><span data-stu-id="05d0d-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="05d0d-115">Řešením je odebrání neplatných rozměrů z řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="05d0d-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="05d0d-116">Zobrazuje se následující chybová zpráva: „Jeden z řádků je již na nákladu.</span><span class="sxs-lookup"><span data-stu-id="05d0d-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="05d0d-117">Nelze uvolnit do skladu."</span><span class="sxs-lookup"><span data-stu-id="05d0d-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="05d0d-118">Popis problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-118">Issue description</span></span>

<span data-ttu-id="05d0d-119">Pokud ručně vytvoříte náklady nebo nastavíte proces tak, aby se náklady již vytvořily před zadáním řádku prodejní objednávky, předpokládá se, že následné vydání bude provedeno ručně a že bude použita cesta a hodnocení z nákladu.</span><span class="sxs-lookup"><span data-stu-id="05d0d-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="05d0d-120">V jiném možném scénáři se pokoušíte provést automatické uvolnění do skladu, ale vlnovému procesu se nepodařilo vytvořit práci.</span><span class="sxs-lookup"><span data-stu-id="05d0d-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="05d0d-121">Proto je stále vytvořena otevřená zásilka nebo náklad.</span><span class="sxs-lookup"><span data-stu-id="05d0d-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="05d0d-122">Tato otevřená zásilka nebo náklad poté blokuje následné pokusy o automatické uvolnění objednávky, dokud otevřenou zásilku nebo náklad nezrušíte nebo ručně nezpracujete vlnu.</span><span class="sxs-lookup"><span data-stu-id="05d0d-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05d0d-123">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-123">Issue resolution</span></span>

<span data-ttu-id="05d0d-124">Můžete uvolnit ze stránky prodejní objednávky nebo automatické uvolnění lze provést ze stránky prodejní objednávky, pouze pokud před vydáním do skladu neexistuje žádný náklad.</span><span class="sxs-lookup"><span data-stu-id="05d0d-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="05d0d-125">Po zpracování vlny se náklad automaticky vytvoří.</span><span class="sxs-lookup"><span data-stu-id="05d0d-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="05d0d-126">Zobrazuje se následující chybová zpráva: „Opravu poznámky k dodání nelze zpracovat.</span><span class="sxs-lookup"><span data-stu-id="05d0d-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="05d0d-127">Poznámka k dodání obsahuje pouze položky, které podléhají procesům správy skladu, protože tyto nejsou opravou poznámky k dodání podporovány. "</span><span class="sxs-lookup"><span data-stu-id="05d0d-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="05d0d-128">Popis problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-128">Issue description</span></span>

<span data-ttu-id="05d0d-129">Po vystavení poznámky k dodání ji nemůžete zrušit, protože tlačítko **Zrušení** není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="05d0d-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="05d0d-130">Poznámku k dodání také nemůžete opravit.</span><span class="sxs-lookup"><span data-stu-id="05d0d-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="05d0d-131">Pokud se pokusíte, zobrazí se tato chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="05d0d-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05d0d-132">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-132">Issue resolution</span></span>

<span data-ttu-id="05d0d-133">Chcete-li opravit odeslané dodací listy pro položky, které jsou povoleny pro pokročilou správu skladu (WMS), musíte zaúčtování provést z nákladu, nikoli přímo z objednávky.</span><span class="sxs-lookup"><span data-stu-id="05d0d-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="05d0d-134">Jak mohu vytvořit práci z odchozích nákladů namísto vln?</span><span class="sxs-lookup"><span data-stu-id="05d0d-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="05d0d-135">Popis problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-135">Issue description</span></span>

<span data-ttu-id="05d0d-136">Zde je jeden způsob, jak tento problém reprodukovat.</span><span class="sxs-lookup"><span data-stu-id="05d0d-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="05d0d-137">Vytvoření odchozího nákladu pomocí prodejní objednávky nebo převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="05d0d-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="05d0d-138">Uvolnit vytížení do skladu</span><span class="sxs-lookup"><span data-stu-id="05d0d-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="05d0d-139">Všimněte si, že zatím nebyla vygenerována žádná práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="05d0d-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05d0d-140">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-140">Issue resolution</span></span>

<span data-ttu-id="05d0d-141">Pokud musí být práce generována okamžitě po uvolnění nákladu, musíte odpovídajícím způsobem nakonfigurovat šablonu vln.</span><span class="sxs-lookup"><span data-stu-id="05d0d-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="05d0d-142">Na šabloně vlny nastavte následující možnosti na *Ano*:</span><span class="sxs-lookup"><span data-stu-id="05d0d-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="05d0d-143">Automatizovat vytvoření vlny</span><span class="sxs-lookup"><span data-stu-id="05d0d-143">Automate wave creation</span></span>
- <span data-ttu-id="05d0d-144">Zpracovat vlnu při uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="05d0d-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="05d0d-145">Automatizovat uvolnění vlny</span><span class="sxs-lookup"><span data-stu-id="05d0d-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="05d0d-146">Částečně odeslaný náklad nemohu znovu uvolnit.</span><span class="sxs-lookup"><span data-stu-id="05d0d-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="05d0d-147">Popis problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-147">Issue description</span></span>

<span data-ttu-id="05d0d-148">Částečně odeslaný náklad nemůžete uvolnit do skladu.</span><span class="sxs-lookup"><span data-stu-id="05d0d-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="05d0d-149">Když provedete uvolnění do skladu, zobrazí se zpráva „Operace dokončena“, ale nic se nestane a pro zbývající množství se nevytvoří žádná práce.</span><span class="sxs-lookup"><span data-stu-id="05d0d-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="05d0d-150">K tomuto problému dochází, když použijete funkci transportu nákladu a dojde k neúplné rezervaci.</span><span class="sxs-lookup"><span data-stu-id="05d0d-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05d0d-151">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="05d0d-151">Issue resolution</span></span>

<span data-ttu-id="05d0d-152">[Problém KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Částečně odeslané náklady lze znovu zařadit do vlny a zpracovat“) je opraven [vydaná verze 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="05d0d-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]