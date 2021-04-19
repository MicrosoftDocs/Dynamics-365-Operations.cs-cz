---
title: Konsolidace dodávek při jejich uvolnění do skladu pomocí automatického uvolnění prodejních objednávek
description: Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném periodickém postupu automatizovaného uvolnění do skladu.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 82a95ecf196ef7c33831da7f4d03df629b17fa53
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807553"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="a894e-103">Konsolidace dodávek při jejich uvolnění do skladu pomocí automatického uvolnění prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="a894e-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a894e-104">Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném periodickém postupu automatizovaného uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="a894e-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="a894e-105">Objednávky budou automaticky konsolidovány do dodávek na základě pravidel definovaných jako zásady konsolidace dodávek.</span><span class="sxs-lookup"><span data-stu-id="a894e-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="a894e-106">Během scénáře vytvoříte sady prodejních objednávek a uvolníte každou sadu do skladu.</span><span class="sxs-lookup"><span data-stu-id="a894e-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="a894e-107">Poté zkontrolujete dodávky, které jsou vytvořeny nebo aktualizovány během konsolidace dodávek, na základě nakonfigurovaných zásad.</span><span class="sxs-lookup"><span data-stu-id="a894e-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="a894e-108">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="a894e-108">Make demo data available</span></span>

<span data-ttu-id="a894e-109">Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a894e-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a894e-110">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="a894e-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="a894e-111">Nastavení zásad konsolidace dodávek a filtry produktů</span><span class="sxs-lookup"><span data-stu-id="a894e-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="a894e-112">Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="a894e-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="a894e-113">Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.</span><span class="sxs-lookup"><span data-stu-id="a894e-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="a894e-114">Vytvoření prodejních objednávek pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="a894e-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="a894e-115">Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat.</span><span class="sxs-lookup"><span data-stu-id="a894e-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="a894e-116">Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="a894e-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="a894e-117">Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.</span><span class="sxs-lookup"><span data-stu-id="a894e-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="a894e-118">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="a894e-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="a894e-119">Vytvoření sady objednávek 1</span><span class="sxs-lookup"><span data-stu-id="a894e-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="a894e-120">Prodejní objednávka 1-1</span><span class="sxs-lookup"><span data-stu-id="a894e-120">Sales order 1-1</span></span>

1. <span data-ttu-id="a894e-121">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a894e-122">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a894e-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a894e-123">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a894e-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a894e-124">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-125">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-126">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="a894e-127">Prodejní objednávka 1-2</span><span class="sxs-lookup"><span data-stu-id="a894e-127">Sales order 1-2</span></span>

1. <span data-ttu-id="a894e-128">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a894e-129">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a894e-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a894e-130">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a894e-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a894e-131">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-132">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-133">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="a894e-134">Prodejní objednávka 1-3</span><span class="sxs-lookup"><span data-stu-id="a894e-134">Sales order 1-3</span></span>

1. <span data-ttu-id="a894e-135">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a894e-136">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a894e-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a894e-137">**Způsob dodání:** *10*</span><span class="sxs-lookup"><span data-stu-id="a894e-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="a894e-138">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-139">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-140">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a894e-141">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-142">**Číslo položky:** *A0002* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-143">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a894e-144">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a894e-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="a894e-145">Vytvoření sady objednávek 2</span><span class="sxs-lookup"><span data-stu-id="a894e-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="a894e-146">Prodejní objednávky 2-1 a 2-2</span><span class="sxs-lookup"><span data-stu-id="a894e-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="a894e-147">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a894e-148">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a894e-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a894e-149">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-150">**Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)</span><span class="sxs-lookup"><span data-stu-id="a894e-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="a894e-151">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a894e-152">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-153">**Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)</span><span class="sxs-lookup"><span data-stu-id="a894e-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="a894e-154">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a894e-155">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a894e-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="a894e-156">Vytvoření sady objednávek 3</span><span class="sxs-lookup"><span data-stu-id="a894e-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="a894e-157">Prodejní objednávka 3-1</span><span class="sxs-lookup"><span data-stu-id="a894e-157">Sales order 3-1</span></span>

1. <span data-ttu-id="a894e-158">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a894e-159">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a894e-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a894e-160">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-161">**Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)</span><span class="sxs-lookup"><span data-stu-id="a894e-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="a894e-162">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a894e-163">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-164">**Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)</span><span class="sxs-lookup"><span data-stu-id="a894e-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="a894e-165">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a894e-166">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a894e-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="a894e-167">Tato objednávka je totožná se dvěma objednávkami, které jste vytvořili pro sadu objednávek 2.</span><span class="sxs-lookup"><span data-stu-id="a894e-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="a894e-168">Je však uvedena jako vlastní sada objednávek, protože ji později v tomto scénáři uvolníte samostatně.</span><span class="sxs-lookup"><span data-stu-id="a894e-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="a894e-169">Vytvoření sady objednávek 4</span><span class="sxs-lookup"><span data-stu-id="a894e-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="a894e-170">Prodejní objednávka 4-1</span><span class="sxs-lookup"><span data-stu-id="a894e-170">Sales order 4-1</span></span>

1. <span data-ttu-id="a894e-171">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a894e-172">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a894e-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a894e-173">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="a894e-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="a894e-174">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-175">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-176">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="a894e-177">Vytvoření sady objednávek 5</span><span class="sxs-lookup"><span data-stu-id="a894e-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="a894e-178">Prodejní objednávky 5-1 a 5-2</span><span class="sxs-lookup"><span data-stu-id="a894e-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="a894e-179">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a894e-180">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a894e-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a894e-181">**Žádost zákazníka:** *2*</span><span class="sxs-lookup"><span data-stu-id="a894e-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="a894e-182">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-183">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-184">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="a894e-185">Prodejní objednávka 5-3</span><span class="sxs-lookup"><span data-stu-id="a894e-185">Sales order 5-3</span></span>

1. <span data-ttu-id="a894e-186">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a894e-187">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a894e-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a894e-188">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="a894e-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="a894e-189">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-190">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-191">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="a894e-192">Vytvoření sady objednávek 6</span><span class="sxs-lookup"><span data-stu-id="a894e-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="a894e-193">Prodejní objednávky 6-1 a 6-2</span><span class="sxs-lookup"><span data-stu-id="a894e-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="a894e-194">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a894e-195">**Účet zákazníka:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="a894e-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="a894e-196">**Žádost zákazníka:** *2*</span><span class="sxs-lookup"><span data-stu-id="a894e-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="a894e-197">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-198">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-199">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="a894e-200">Prodejní objednávky 6-3 a 6-4</span><span class="sxs-lookup"><span data-stu-id="a894e-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="a894e-201">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a894e-202">**Účet zákazníka:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="a894e-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="a894e-203">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="a894e-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="a894e-204">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-205">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-206">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="a894e-207">Prodejní objednávky 6-5 a 6-6</span><span class="sxs-lookup"><span data-stu-id="a894e-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="a894e-208">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a894e-209">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a894e-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a894e-210">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="a894e-210">**Site:** *6*</span></span>
    - <span data-ttu-id="a894e-211">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="a894e-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a894e-212">**Fond:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="a894e-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="a894e-213">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-214">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-215">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="a894e-216">Prodejní objednávky 6-7 a 6-8</span><span class="sxs-lookup"><span data-stu-id="a894e-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="a894e-217">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a894e-218">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a894e-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a894e-219">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="a894e-219">**Site:** *6*</span></span>
    - <span data-ttu-id="a894e-220">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="a894e-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a894e-221">**Fond:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="a894e-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="a894e-222">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a894e-223">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="a894e-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a894e-224">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a894e-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="a894e-225">Automatické uvolnění prodejních objednávek do skladu</span><span class="sxs-lookup"><span data-stu-id="a894e-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="a894e-226">U každé sady prodejních objednávek, které jste vytvořili dříve, dokončíte postup automatického uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="a894e-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="a894e-227">V každém případě budete pracovat prostřednictvím [základního postupu uvolnění do skladu](#release-procedure), který je uveden zde.</span><span class="sxs-lookup"><span data-stu-id="a894e-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="a894e-228">Základní postup uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="a894e-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="a894e-229">U každé sady prodejních objednávek, které jste vytvořili dříve, dokončíte tři postupy, které jsou popsány v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="a894e-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="a894e-230">Aktualizace šablony vln, která bude použita během uvolnění</span><span class="sxs-lookup"><span data-stu-id="a894e-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="a894e-231">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="a894e-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a894e-232">Nastavte pole **Typ šablony vln** na *Expedice*.</span><span class="sxs-lookup"><span data-stu-id="a894e-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="a894e-233">Najděte a vyberte šablonu vlny přidruženou ke skladu, který jste použili v sadách objednávek, které jste pro tento scénář vytvořili.</span><span class="sxs-lookup"><span data-stu-id="a894e-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="a894e-234">Pokud jste například použili sklad *24*, vybere šablonu vlny **Výchozí expedice 24**.</span><span class="sxs-lookup"><span data-stu-id="a894e-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="a894e-235">Pokud jste použili sklad *61*, vybere šablonu vlny **Expedice 61**.</span><span class="sxs-lookup"><span data-stu-id="a894e-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="a894e-236">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="a894e-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a894e-237">Nastavte možnost **Zpracovat vlnu při uvolnění do skladu** na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="a894e-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="a894e-238">Uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="a894e-238">Release to the warehouse</span></span>

1. <span data-ttu-id="a894e-239">Přejděte na **Řízení skladu \> Uvolnění do skladu \> Automatické uvolnění prodejních objednávek**.</span><span class="sxs-lookup"><span data-stu-id="a894e-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="a894e-240">Nastavte pole **Množství k uvolnění** na *Vše*.</span><span class="sxs-lookup"><span data-stu-id="a894e-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="a894e-241">Na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr** a otevřete dialogové okno dotazu.</span><span class="sxs-lookup"><span data-stu-id="a894e-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="a894e-242">Na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="a894e-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="a894e-243">**Tabulka:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="a894e-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="a894e-244">**Odvozená tabulka:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="a894e-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="a894e-245">**Pole:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="a894e-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="a894e-246">**Kritéria:** Zadejte čárkami oddělený seznam čísel prodejních objednávek z požadované sady objednávek.</span><span class="sxs-lookup"><span data-stu-id="a894e-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="a894e-247">Vyberte **OK** a uložte dotaz.</span><span class="sxs-lookup"><span data-stu-id="a894e-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="a894e-248">Vyberte **OK** a zahajte postup *Automatické uvolnění do skladu*.</span><span class="sxs-lookup"><span data-stu-id="a894e-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="a894e-249">Kontrola dodávky, která je vytvořena nebo aktualizována</span><span class="sxs-lookup"><span data-stu-id="a894e-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="a894e-250">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="a894e-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="a894e-251">Najděte a vyberte požadovanou dodávku.</span><span class="sxs-lookup"><span data-stu-id="a894e-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="a894e-252">Pokud byla při vytváření nebo aktualizaci dodávky použita zásada konsolidace, měli byste ji vidět v poli **Zásada konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="a894e-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="a894e-253">Uvolnění prodejních objednávek ze sady objednávek 1</span><span class="sxs-lookup"><span data-stu-id="a894e-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="a894e-254">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 1.</span><span class="sxs-lookup"><span data-stu-id="a894e-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="a894e-255">Po dokončení byste měli vidět, že byly vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="a894e-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="a894e-256">První dodávka obsahuje tři řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="a894e-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="a894e-257">Druhá dodávka, která nepoužívá způsob dopravy *Airways*, byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="a894e-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="a894e-258">Uvolnění prodejních objednávek ze sady objednávek 2</span><span class="sxs-lookup"><span data-stu-id="a894e-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="a894e-259">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 2.</span><span class="sxs-lookup"><span data-stu-id="a894e-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="a894e-260">Po dokončení byste měli vidět, že byly vytvořeny tři dodávky:</span><span class="sxs-lookup"><span data-stu-id="a894e-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="a894e-261">První dodávka obsahuje položky *Hořlavý*.</span><span class="sxs-lookup"><span data-stu-id="a894e-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="a894e-262">Každá ze dvou dalších zásilek obsahuje jeden řádek, který má položku *Explozivní*.</span><span class="sxs-lookup"><span data-stu-id="a894e-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="a894e-263">Uvolnění prodejních objednávek ze sady objednávek 3</span><span class="sxs-lookup"><span data-stu-id="a894e-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="a894e-264">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 3.</span><span class="sxs-lookup"><span data-stu-id="a894e-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="a894e-265">Po dokončení byste měli vidět, že došlo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="a894e-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="a894e-266">Byla aktualizována jedna existující dodávka (dodávka, která byla vytvořena při uvolnění sady objednávek 2 do skladu).</span><span class="sxs-lookup"><span data-stu-id="a894e-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="a894e-267">Byl přidán řádek s položkou *Hořlavý*.</span><span class="sxs-lookup"><span data-stu-id="a894e-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="a894e-268">Byla vytvořena jedna nová dodávka, která obsahuje položku *Explozivní*.</span><span class="sxs-lookup"><span data-stu-id="a894e-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="a894e-269">Uvolnění prodejních objednávek ze sady objednávek 4</span><span class="sxs-lookup"><span data-stu-id="a894e-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="a894e-270">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 4.</span><span class="sxs-lookup"><span data-stu-id="a894e-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="a894e-271">Až skončíte, měli byste vidět, že jedna existující dodávka (kde je pole **Žádost zákazníka** nastaveno na *1*) byla aktualizována.</span><span class="sxs-lookup"><span data-stu-id="a894e-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="a894e-272">Byl k ní přidán jeden nový řádek.</span><span class="sxs-lookup"><span data-stu-id="a894e-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="a894e-273">Uvolnění prodejních objednávek ze sady objednávek 5</span><span class="sxs-lookup"><span data-stu-id="a894e-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="a894e-274">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 5.</span><span class="sxs-lookup"><span data-stu-id="a894e-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="a894e-275">Po dokončení byste měli vidět, že došlo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="a894e-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="a894e-276">Jedna existující dodávka (kde je pole **Žádost zákazníka** nastaveno na *1*) byla aktualizována.</span><span class="sxs-lookup"><span data-stu-id="a894e-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="a894e-277">Řádek z prodejní objednávky 5-3 (kde je pole **Žádost zákazníka** nastaveno na *1*) byl k ní přidán.</span><span class="sxs-lookup"><span data-stu-id="a894e-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="a894e-278">Byla vytvořena jedna nová dodávka, kde řádky z prodejních objednávek 5-1 a 5-2 jsou seskupeny do jedné dodávky.</span><span class="sxs-lookup"><span data-stu-id="a894e-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="a894e-279">Uvolnění prodejních objednávek ze sady objednávek 6</span><span class="sxs-lookup"><span data-stu-id="a894e-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="a894e-280">Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 6.</span><span class="sxs-lookup"><span data-stu-id="a894e-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="a894e-281">Po dokončení byste měli vidět, že byly vytvořeny čtyři dodávky:</span><span class="sxs-lookup"><span data-stu-id="a894e-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="a894e-282">Řádky ze dvou objednávek pro zákazníka *US-003* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="a894e-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a894e-283">Řádky ze dvou objednávek pro zákazníka *US-004* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="a894e-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a894e-284">Řádky z objednávek 6-5 a 6-6 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="a894e-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a894e-285">Řádky z objednávek 6-7 a 6-8 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="a894e-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a894e-286">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a894e-286">Additional resources</span></span>

- [<span data-ttu-id="a894e-287">Zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="a894e-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="a894e-288">Konfigurace zásad konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="a894e-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]