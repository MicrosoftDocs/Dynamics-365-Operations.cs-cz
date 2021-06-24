---
title: Množství nelze při zrušení prodejní objednávky snížit
description: Množství nelze při zrušení prodejní objednávky snížit.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230829"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="6d73a-103">Množství nelze při zrušení prodejní objednávky snížit</span><span class="sxs-lookup"><span data-stu-id="6d73a-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="6d73a-104">Kód chyby: SYS138831</span><span class="sxs-lookup"><span data-stu-id="6d73a-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="6d73a-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="6d73a-105">Symptoms</span></span>

<span data-ttu-id="6d73a-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="6d73a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6d73a-107">Množství nelze snížit.</span><span class="sxs-lookup"><span data-stu-id="6d73a-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="6d73a-108">Počet transakcí zásob u objednávky je příliš nízký, protože na množství nebo její část odkazuje výstupní objednávka nebo výrobní zakázka nebo je označeno vůči jiným transakcím.</span><span class="sxs-lookup"><span data-stu-id="6d73a-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="6d73a-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="6d73a-109">Cause</span></span>

<span data-ttu-id="6d73a-110">Pokud je práce přidružená k prodejní objednávce, nemůžete zrušit prodejní objednávku, dokud nebude práce zrušena a stornována.</span><span class="sxs-lookup"><span data-stu-id="6d73a-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="6d73a-111">Tento požadavek platí, i když je práce přidružená k prodejní objednávce uzavřena.</span><span class="sxs-lookup"><span data-stu-id="6d73a-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="6d73a-112">Řešení</span><span class="sxs-lookup"><span data-stu-id="6d73a-112">Resolution</span></span>

<span data-ttu-id="6d73a-113">Chcete-li problém opravit, proveďte následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="6d73a-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="6d73a-114">Zrušte otevřenou práci.</span><span class="sxs-lookup"><span data-stu-id="6d73a-114">Cancel open work.</span></span>
1. <span data-ttu-id="6d73a-115">Odstraňte vytížení.</span><span class="sxs-lookup"><span data-stu-id="6d73a-115">Delete the load.</span></span>
1. <span data-ttu-id="6d73a-116">Snižte vyskladněné množství.</span><span class="sxs-lookup"><span data-stu-id="6d73a-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="6d73a-117">Zrušení otevřené práce</span><span class="sxs-lookup"><span data-stu-id="6d73a-117">Cancel open work</span></span>

<span data-ttu-id="6d73a-118">Chcete-li zrušit otevřenou práci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6d73a-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="6d73a-119">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6d73a-120">V poli **ID práce** zadejte ID práce, kterou chcete zrušit a které aktuálně obsahuje pro možnost **Stav práce** hodnotu *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinované* nebo *Uzavřené*.</span><span class="sxs-lookup"><span data-stu-id="6d73a-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="6d73a-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-121">Select **OK**.</span></span>
1. <span data-ttu-id="6d73a-122">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="6d73a-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="6d73a-123">Odstranění vytížení</span><span class="sxs-lookup"><span data-stu-id="6d73a-123">Delete the load</span></span>

<span data-ttu-id="6d73a-124">Chcete-li odstranit vytížení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="6d73a-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="6d73a-125">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6d73a-126">Otevřete příslušnou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="6d73a-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="6d73a-127">Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="6d73a-128">Na stránce **Práce** v podokně Akce na kartě **Práce** ve skupině **Práce** vyberte příkaz **Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="6d73a-129">Potvrďte, že se pole **Stav práce** nastaví na *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="6d73a-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="6d73a-130">Zavřete stránku **Práce**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="6d73a-131">Na stránce podrobností prodejní objednávky na záložce s náhledem **Řádky prodejní objednávky** vyberte **Sklad \> Načíst podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="6d73a-132">V podokně Akce zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="6d73a-133">Výběrem **Ano** potvrďte, že chcete odstranit vytížení.</span><span class="sxs-lookup"><span data-stu-id="6d73a-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="6d73a-134">Zavřete stránku **Vytížení**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="6d73a-135">Snížení vyskladněného množství</span><span class="sxs-lookup"><span data-stu-id="6d73a-135">Reduce the picked quantity</span></span>

<span data-ttu-id="6d73a-136">Po zrušení všech prací snižte vyskladněné množství podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="6d73a-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="6d73a-137">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6d73a-138">Otevřete příslušnou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="6d73a-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="6d73a-139">Na záložce s náhledem **Řádky prodejní objednávky** vyberte v panelu nástrojů **Aktualizovat řádek \> Vydat**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="6d73a-140">Na stránce **Vydat** v části **Transakce** vyberte řádek, kde je pole **Stav výdeje** nastaveno na *Vydáno*.</span><span class="sxs-lookup"><span data-stu-id="6d73a-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="6d73a-141">V části **Transakce** vyberte v panelu nástrojů **Přidat řádek výdeje**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="6d73a-142">V části **Řádky výdeje** vyberte v panelu nástrojů **Potvrdit výběr všech**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="6d73a-143">Zavřete stránku **Vydat**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="6d73a-144">Na stránce podrobností prodejní objednávky v podokně akcí na kartě **Prodejní objednávka** ve skupině **Udržovat** vyberte **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="6d73a-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="6d73a-145">Vyberte možnost **Ano** k potvrzení, že chcete prodejní objednávku zrušit.</span><span class="sxs-lookup"><span data-stu-id="6d73a-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
