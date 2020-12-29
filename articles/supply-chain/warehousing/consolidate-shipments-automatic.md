---
title: Konsolidace dodávek při jejich uvolnění do skladu pomocí automatického uvolnění prodejních objednávek
description: Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném periodickém postupu automatizovaného uvolnění do skladu.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac3ab25dc1355ee15e1209950ff0f3b3933b7095
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424156"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="282b0-103">Konsolidace dodávek při jejich uvolnění do skladu pomocí automatického uvolnění prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="282b0-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="282b0-104">Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném periodickém postupu automatizovaného uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="282b0-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="282b0-105">Objednávky budou automaticky konsolidovány do dodávek na základě pravidel definovaných jako zásady konsolidace dodávek.</span><span class="sxs-lookup"><span data-stu-id="282b0-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="282b0-106">Během scénáře vytvoříte sady prodejních objednávek a uvolníte každou sadu do skladu.</span><span class="sxs-lookup"><span data-stu-id="282b0-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="282b0-107">Poté zkontrolujete dodávky, které jsou vytvořeny nebo aktualizovány během konsolidace dodávek, na základě nakonfigurovaných zásad.</span><span class="sxs-lookup"><span data-stu-id="282b0-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="282b0-108">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="282b0-108">Make demo data available</span></span>

<span data-ttu-id="282b0-109">Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="282b0-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="282b0-110">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="282b0-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="282b0-111">Nastavení zásad konsolidace dodávek a filtry produktů</span><span class="sxs-lookup"><span data-stu-id="282b0-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="282b0-112">Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="282b0-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="282b0-113">Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.</span><span class="sxs-lookup"><span data-stu-id="282b0-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="282b0-114">Vytvoření prodejních objednávek pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="282b0-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="282b0-115">Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat.</span><span class="sxs-lookup"><span data-stu-id="282b0-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="282b0-116">Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="282b0-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="282b0-117">Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.</span><span class="sxs-lookup"><span data-stu-id="282b0-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="282b0-118">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="282b0-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="282b0-119">Vytvoření sady objednávek 1</span><span class="sxs-lookup"><span data-stu-id="282b0-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="282b0-120">Prodejní objednávka 1-1</span><span class="sxs-lookup"><span data-stu-id="282b0-120">Sales order 1-1</span></span>

1. <span data-ttu-id="282b0-121">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="282b0-122">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="282b0-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="282b0-123">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="282b0-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="282b0-124">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-125">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-126">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="282b0-127">Prodejní objednávka 1-2</span><span class="sxs-lookup"><span data-stu-id="282b0-127">Sales order 1-2</span></span>

1. <span data-ttu-id="282b0-128">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="282b0-129">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="282b0-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="282b0-130">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="282b0-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="282b0-131">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-132">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-133">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="282b0-134">Prodejní objednávka 1-3</span><span class="sxs-lookup"><span data-stu-id="282b0-134">Sales order 1-3</span></span>

1. <span data-ttu-id="282b0-135">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="282b0-136">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="282b0-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="282b0-137">**Způsob dodání:** *10*</span><span class="sxs-lookup"><span data-stu-id="282b0-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="282b0-138">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-139">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-140">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="282b0-141">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-142">**Číslo položky:** *A0002* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-143">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="282b0-144">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="282b0-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="282b0-145">Vytvoření sady objednávek 2</span><span class="sxs-lookup"><span data-stu-id="282b0-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="282b0-146">Prodejní objednávky 2-1 a 2-2</span><span class="sxs-lookup"><span data-stu-id="282b0-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="282b0-147">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="282b0-148">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="282b0-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="282b0-149">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-150">**Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)</span><span class="sxs-lookup"><span data-stu-id="282b0-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="282b0-151">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="282b0-152">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-153">**Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)</span><span class="sxs-lookup"><span data-stu-id="282b0-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="282b0-154">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="282b0-155">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="282b0-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="282b0-156">Vytvoření sady objednávek 3</span><span class="sxs-lookup"><span data-stu-id="282b0-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="282b0-157">Prodejní objednávka 3-1</span><span class="sxs-lookup"><span data-stu-id="282b0-157">Sales order 3-1</span></span>

1. <span data-ttu-id="282b0-158">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="282b0-159">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="282b0-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="282b0-160">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-161">**Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)</span><span class="sxs-lookup"><span data-stu-id="282b0-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="282b0-162">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="282b0-163">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-164">**Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)</span><span class="sxs-lookup"><span data-stu-id="282b0-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="282b0-165">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="282b0-166">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="282b0-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="282b0-167">Tato objednávka je totožná se dvěma objednávkami, které jste vytvořili pro sadu objednávek 2.</span><span class="sxs-lookup"><span data-stu-id="282b0-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="282b0-168">Je však uvedena jako vlastní sada objednávek, protože ji později v tomto scénáři uvolníte samostatně.</span><span class="sxs-lookup"><span data-stu-id="282b0-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="282b0-169">Vytvoření sady objednávek 4</span><span class="sxs-lookup"><span data-stu-id="282b0-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="282b0-170">Prodejní objednávka 4-1</span><span class="sxs-lookup"><span data-stu-id="282b0-170">Sales order 4-1</span></span>

1. <span data-ttu-id="282b0-171">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="282b0-172">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="282b0-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="282b0-173">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="282b0-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="282b0-174">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-175">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-176">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="282b0-177">Vytvoření sady objednávek 5</span><span class="sxs-lookup"><span data-stu-id="282b0-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="282b0-178">Prodejní objednávky 5-1 a 5-2</span><span class="sxs-lookup"><span data-stu-id="282b0-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="282b0-179">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="282b0-180">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="282b0-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="282b0-181">**Žádost zákazníka:** *2*</span><span class="sxs-lookup"><span data-stu-id="282b0-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="282b0-182">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-183">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-184">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="282b0-185">Prodejní objednávka 5-3</span><span class="sxs-lookup"><span data-stu-id="282b0-185">Sales order 5-3</span></span>

1. <span data-ttu-id="282b0-186">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="282b0-187">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="282b0-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="282b0-188">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="282b0-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="282b0-189">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-190">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-191">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="282b0-192">Vytvoření sady objednávek 6</span><span class="sxs-lookup"><span data-stu-id="282b0-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="282b0-193">Prodejní objednávky 6-1 a 6-2</span><span class="sxs-lookup"><span data-stu-id="282b0-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="282b0-194">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="282b0-195">**Účet zákazníka:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="282b0-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="282b0-196">**Žádost zákazníka:** *2*</span><span class="sxs-lookup"><span data-stu-id="282b0-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="282b0-197">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-198">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-199">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="282b0-200">Prodejní objednávky 6-3 a 6-4</span><span class="sxs-lookup"><span data-stu-id="282b0-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="282b0-201">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="282b0-202">**Účet zákazníka:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="282b0-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="282b0-203">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="282b0-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="282b0-204">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-205">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-206">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="282b0-207">Prodejní objednávky 6-5 a 6-6</span><span class="sxs-lookup"><span data-stu-id="282b0-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="282b0-208">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="282b0-209">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="282b0-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="282b0-210">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="282b0-210">**Site:** *6*</span></span>
    - <span data-ttu-id="282b0-211">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="282b0-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="282b0-212">**Fond:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="282b0-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="282b0-213">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-214">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-215">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="282b0-216">Prodejní objednávky 6-7 a 6-8</span><span class="sxs-lookup"><span data-stu-id="282b0-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="282b0-217">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="282b0-218">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="282b0-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="282b0-219">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="282b0-219">**Site:** *6*</span></span>
    - <span data-ttu-id="282b0-220">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="282b0-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="282b0-221">**Fond:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="282b0-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="282b0-222">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="282b0-223">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="282b0-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="282b0-224">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="282b0-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="282b0-225">Automatické uvolnění prodejních objednávek do skladu</span><span class="sxs-lookup"><span data-stu-id="282b0-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="282b0-226">U každé sady prodejních objednávek, které jste vytvořili dříve, dokončíte postup automatického uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="282b0-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="282b0-227">V každém případě budete pracovat prostřednictvím [základního postupu uvolnění do skladu](#release-procedure), který je uveden zde.</span><span class="sxs-lookup"><span data-stu-id="282b0-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="282b0-228">Základní postup uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="282b0-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="282b0-229">U každé sady prodejních objednávek, které jste vytvořili dříve, dokončíte tři postupy, které jsou popsány v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="282b0-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="282b0-230">Aktualizace šablony vln, která bude použita během uvolnění</span><span class="sxs-lookup"><span data-stu-id="282b0-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="282b0-231">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="282b0-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="282b0-232">Nastavte pole **Typ šablony vln** na *Expedice*.</span><span class="sxs-lookup"><span data-stu-id="282b0-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="282b0-233">Najděte a vyberte šablonu vlny přidruženou ke skladu, který jste použili v sadách objednávek, které jste pro tento scénář vytvořili.</span><span class="sxs-lookup"><span data-stu-id="282b0-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="282b0-234">Pokud jste například použili sklad *24*, vybere šablonu vlny **Výchozí expedice 24**.</span><span class="sxs-lookup"><span data-stu-id="282b0-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="282b0-235">Pokud jste použili sklad *61*, vybere šablonu vlny **Expedice 61**.</span><span class="sxs-lookup"><span data-stu-id="282b0-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="282b0-236">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="282b0-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="282b0-237">Nastavte možnost **Zpracovat vlnu při uvolnění do skladu** na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="282b0-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="282b0-238">Uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="282b0-238">Release to the warehouse</span></span>

1. <span data-ttu-id="282b0-239">Přejděte na **Řízení skladu \> Uvolnění do skladu \> Automatické uvolnění prodejních objednávek**.</span><span class="sxs-lookup"><span data-stu-id="282b0-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="282b0-240">Nastavte pole **Množství k uvolnění** na *Vše*.</span><span class="sxs-lookup"><span data-stu-id="282b0-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="282b0-241">Na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr** a otevřete dialogové okno dotazu.</span><span class="sxs-lookup"><span data-stu-id="282b0-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="282b0-242">Na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="282b0-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="282b0-243">**Tabulka:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="282b0-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="282b0-244">**Odvozená tabulka:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="282b0-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="282b0-245">**Pole:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="282b0-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="282b0-246">**Kritéria:** Zadejte čárkami oddělený seznam čísel prodejních objednávek z požadované sady objednávek.</span><span class="sxs-lookup"><span data-stu-id="282b0-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="282b0-247">Vyberte **OK** a uložte dotaz.</span><span class="sxs-lookup"><span data-stu-id="282b0-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="282b0-248">Vyberte **OK** a zahajte postup *Automatické uvolnění do skladu*.</span><span class="sxs-lookup"><span data-stu-id="282b0-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="282b0-249">Kontrola dodávky, která je vytvořena nebo aktualizována</span><span class="sxs-lookup"><span data-stu-id="282b0-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="282b0-250">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="282b0-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="282b0-251">Najděte a vyberte požadovanou dodávku.</span><span class="sxs-lookup"><span data-stu-id="282b0-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="282b0-252">Pokud byla při vytváření nebo aktualizaci dodávky použita zásada konsolidace, měli byste ji vidět v poli **Zásada konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="282b0-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="282b0-253">Uvolnění prodejních objednávek ze sady objednávek 1</span><span class="sxs-lookup"><span data-stu-id="282b0-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="282b0-254">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 1.</span><span class="sxs-lookup"><span data-stu-id="282b0-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="282b0-255">Po dokončení byste měli vidět, že byly vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="282b0-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="282b0-256">První dodávka obsahuje tři řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="282b0-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="282b0-257">Druhá dodávka, která nepoužívá způsob dopravy *Airways*, byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="282b0-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="282b0-258">Uvolnění prodejních objednávek ze sady objednávek 2</span><span class="sxs-lookup"><span data-stu-id="282b0-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="282b0-259">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 2.</span><span class="sxs-lookup"><span data-stu-id="282b0-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="282b0-260">Po dokončení byste měli vidět, že byly vytvořeny tři dodávky:</span><span class="sxs-lookup"><span data-stu-id="282b0-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="282b0-261">První dodávka obsahuje položky *Hořlavý*.</span><span class="sxs-lookup"><span data-stu-id="282b0-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="282b0-262">Každá ze dvou dalších zásilek obsahuje jeden řádek, který má položku *Explozivní*.</span><span class="sxs-lookup"><span data-stu-id="282b0-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="282b0-263">Uvolnění prodejních objednávek ze sady objednávek 3</span><span class="sxs-lookup"><span data-stu-id="282b0-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="282b0-264">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 3.</span><span class="sxs-lookup"><span data-stu-id="282b0-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="282b0-265">Po dokončení byste měli vidět, že došlo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="282b0-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="282b0-266">Byla aktualizována jedna existující dodávka (dodávka, která byla vytvořena při uvolnění sady objednávek 2 do skladu).</span><span class="sxs-lookup"><span data-stu-id="282b0-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="282b0-267">Byl přidán řádek s položkou *Hořlavý*.</span><span class="sxs-lookup"><span data-stu-id="282b0-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="282b0-268">Byla vytvořena jedna nová dodávka, která obsahuje položku *Explozivní*.</span><span class="sxs-lookup"><span data-stu-id="282b0-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="282b0-269">Uvolnění prodejních objednávek ze sady objednávek 4</span><span class="sxs-lookup"><span data-stu-id="282b0-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="282b0-270">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 4.</span><span class="sxs-lookup"><span data-stu-id="282b0-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="282b0-271">Až skončíte, měli byste vidět, že jedna existující dodávka (kde je pole **Žádost zákazníka** nastaveno na *1*) byla aktualizována.</span><span class="sxs-lookup"><span data-stu-id="282b0-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="282b0-272">Byl k ní přidán jeden nový řádek.</span><span class="sxs-lookup"><span data-stu-id="282b0-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="282b0-273">Uvolnění prodejních objednávek ze sady objednávek 5</span><span class="sxs-lookup"><span data-stu-id="282b0-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="282b0-274">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 5.</span><span class="sxs-lookup"><span data-stu-id="282b0-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="282b0-275">Po dokončení byste měli vidět, že došlo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="282b0-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="282b0-276">Jedna existující dodávka (kde je pole **Žádost zákazníka** nastaveno na *1*) byla aktualizována.</span><span class="sxs-lookup"><span data-stu-id="282b0-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="282b0-277">Řádek z prodejní objednávky 5-3 (kde je pole **Žádost zákazníka** nastaveno na *1*) byl k ní přidán.</span><span class="sxs-lookup"><span data-stu-id="282b0-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="282b0-278">Byla vytvořena jedna nová dodávka, kde řádky z prodejních objednávek 5-1 a 5-2 jsou seskupeny do jedné dodávky.</span><span class="sxs-lookup"><span data-stu-id="282b0-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="282b0-279">Uvolnění prodejních objednávek ze sady objednávek 6</span><span class="sxs-lookup"><span data-stu-id="282b0-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="282b0-280">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 6.</span><span class="sxs-lookup"><span data-stu-id="282b0-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="282b0-281">Po dokončení byste měli vidět, že byly vytvořeny čtyři dodávky:</span><span class="sxs-lookup"><span data-stu-id="282b0-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="282b0-282">Řádky ze dvou objednávek pro zákazníka *US-003* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="282b0-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="282b0-283">Řádky ze dvou objednávek pro zákazníka *US-004* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="282b0-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="282b0-284">Řádky z objednávek 6-5 a 6-6 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="282b0-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="282b0-285">Řádky z objednávek 6-7 a 6-8 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="282b0-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="282b0-286">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="282b0-286">Additional resources</span></span>

- [<span data-ttu-id="282b0-287">Zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="282b0-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="282b0-288">Konfigurace zásad konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="282b0-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
