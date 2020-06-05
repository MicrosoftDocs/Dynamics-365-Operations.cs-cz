---
title: Konsolidace dodávek pomocí uvolnění do skladu z pracovní plochy plánování vytížení
description: Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném nákladu a později automaticky konsolidováno do dodávek.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 396a038dbf2f4b6835ecbb5fd8cb39a3a3608af7
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383730"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="0bcbe-103">Konsolidace dodávek pomocí uvolnění do skladu z pracovní plochy plánování vytížení</span><span class="sxs-lookup"><span data-stu-id="0bcbe-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bcbe-104">Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném nákladu a později automaticky konsolidováno do dodávek.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="0bcbe-105">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="0bcbe-105">Make demo data available</span></span>

<span data-ttu-id="0bcbe-106">Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0bcbe-107">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="0bcbe-108">Nastavení zásad konsolidace dodávek a filtry produktů</span><span class="sxs-lookup"><span data-stu-id="0bcbe-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="0bcbe-109">Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="0bcbe-110">Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="0bcbe-111">Vytvoření prodejních objednávek pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="0bcbe-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="0bcbe-112">Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="0bcbe-113">Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="0bcbe-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="0bcbe-114">Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="0bcbe-115">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="0bcbe-116">Vytvoření sady objednávek 1</span><span class="sxs-lookup"><span data-stu-id="0bcbe-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="0bcbe-117">Prodejní objednávka 1-1</span><span class="sxs-lookup"><span data-stu-id="0bcbe-117">Sales order 1-1</span></span>

1. <span data-ttu-id="0bcbe-118">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-119">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0bcbe-120">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0bcbe-121">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-122">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-123">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-124">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="0bcbe-125">Prodejní objednávka 1-2</span><span class="sxs-lookup"><span data-stu-id="0bcbe-125">Sales order 1-2</span></span>

1. <span data-ttu-id="0bcbe-126">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-127">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0bcbe-128">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0bcbe-129">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-130">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-131">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-132">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="0bcbe-133">Prodejní objednávka 1-3</span><span class="sxs-lookup"><span data-stu-id="0bcbe-133">Sales order 1-3</span></span>

1. <span data-ttu-id="0bcbe-134">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-135">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0bcbe-136">**Způsob dodání:** *10*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="0bcbe-137">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-138">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-139">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-140">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="0bcbe-141">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-142">**Číslo položky:** *A0002* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-143">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="0bcbe-144">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0bcbe-145">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci druhého řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="0bcbe-146">Vytvoření sady objednávek 2</span><span class="sxs-lookup"><span data-stu-id="0bcbe-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="0bcbe-147">Prodejní objednávky 2-1 a 2-2</span><span class="sxs-lookup"><span data-stu-id="0bcbe-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="0bcbe-148">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-149">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="0bcbe-150">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-151">**Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="0bcbe-152">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-153">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="0bcbe-154">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-155">**Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="0bcbe-156">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="0bcbe-157">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0bcbe-158">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci druhého řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="0bcbe-159">Vytvoření sady objednávek 3</span><span class="sxs-lookup"><span data-stu-id="0bcbe-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="0bcbe-160">Prodejní objednávky 3-1 a 3-2</span><span class="sxs-lookup"><span data-stu-id="0bcbe-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="0bcbe-161">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-162">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0bcbe-163">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="0bcbe-164">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-165">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-166">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-167">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="0bcbe-168">Prodejní objednávky 3-3 a 3-4</span><span class="sxs-lookup"><span data-stu-id="0bcbe-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="0bcbe-169">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-170">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0bcbe-171">**Žádost zákazníka:** *2*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="0bcbe-172">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-173">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-174">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-175">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="0bcbe-176">Vytvoření sady objednávek 4</span><span class="sxs-lookup"><span data-stu-id="0bcbe-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="0bcbe-177">Prodejní objednávky 4-1 a 4-2</span><span class="sxs-lookup"><span data-stu-id="0bcbe-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="0bcbe-178">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-179">**Účet zákazníka:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="0bcbe-180">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-181">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-182">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-183">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="0bcbe-184">Prodejní objednávky 4-3 a 4-4</span><span class="sxs-lookup"><span data-stu-id="0bcbe-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="0bcbe-185">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-186">**Účet zákazníka:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="0bcbe-187">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-188">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-189">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-190">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="0bcbe-191">Prodejní objednávky 4-5 a 4-6</span><span class="sxs-lookup"><span data-stu-id="0bcbe-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="0bcbe-192">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-193">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0bcbe-194">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-194">**Site:** *6*</span></span>
    - <span data-ttu-id="0bcbe-195">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="0bcbe-196">**Fond:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="0bcbe-197">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-198">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-199">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-200">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="0bcbe-201">Prodejní objednávky 4-7 a 4-8</span><span class="sxs-lookup"><span data-stu-id="0bcbe-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="0bcbe-202">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0bcbe-203">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0bcbe-204">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-204">**Site:** *6*</span></span>
    - <span data-ttu-id="0bcbe-205">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="0bcbe-206">**Fond:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="0bcbe-207">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0bcbe-208">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="0bcbe-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0bcbe-209">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0bcbe-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0bcbe-210">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="0bcbe-211">Pomocí pracovní plochy plánování nákladu můžete vytvářet náklady a uvolňovat je do skladu</span><span class="sxs-lookup"><span data-stu-id="0bcbe-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="0bcbe-212">Chcete-li vytvořit náklad pro každou sadu objednávek, kterou jste vytvořili pro tento scénář, a poté ji uvolnit do skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="0bcbe-213">Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="0bcbe-214">Na kartě **Řádky prodeje** najděte a vyberte všechny řádky prodejních objednávek z jedné ze sad objednávek, které jste pro tento scénář vytvořili.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="0bcbe-215">V podokně akcí na kartě **Nabídka a poptávka** vyberte **Přidat \> Do nového nákladu** a přidejte vybrané řádky prodejní objednávky do nového nákladu.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="0bcbe-216">V dialogovém okně **Přiřazení šablony nákladu** v poli **ID šablony nákladu** vyberte šablonu nákladu, například *Standardní šablona nákladu*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="0bcbe-217">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="0bcbe-218">V části **Náklady** vyhledejte a vyberte náklad, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="0bcbe-219">Vyberte **Uvolnění \> Uvolnění do skladu** pro uvolnění vybraného nákladu do skladu.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="0bcbe-220">Tento postup opakujte pro další tři sady objednávek, které jste vytvořili pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="0bcbe-221">Ověření dodávek</span><span class="sxs-lookup"><span data-stu-id="0bcbe-221">Verify the shipments</span></span>

<span data-ttu-id="0bcbe-222">Následující postup umožňuje ověřit dodávky, které byly vytvořeny nebo aktualizovány v důsledku konsolidace dodávky.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="0bcbe-223">Použijte ho ke kontrole každé sady objednávek, kterou jste vytvořili pro tento scénář, a poté zkontrolujte následující pododdíly, abyste se ujistili, že jste dosáhli očekávaných výsledků.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="0bcbe-224">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="0bcbe-225">Najděte a vyberte požadovanou dodávku.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="0bcbe-226">Pokud byla při vytváření nebo aktualizaci dodávky použita zásada konsolidace, měli byste ji vidět v poli **Zásada konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="0bcbe-227">Uvolněte sadu objednávek 1 v jednom nákladu</span><span class="sxs-lookup"><span data-stu-id="0bcbe-227">Release order set 1 in one load</span></span>

<span data-ttu-id="0bcbe-228">Měly být vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="0bcbe-229">První dodávka obsahuje tři řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="0bcbe-230">Druhá dodávka, která nepoužívá způsob dopravy *Airways*, byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="0bcbe-231">Uvolněte sadu objednávek 2 v jednom nákladu</span><span class="sxs-lookup"><span data-stu-id="0bcbe-231">Release order set 2 in one load</span></span>

<span data-ttu-id="0bcbe-232">Měly být vytvořeny tři dodávky:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="0bcbe-233">První dodávka obsahuje položky *Hořlavý*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="0bcbe-234">Každá ze dvou dalších zásilek obsahuje jeden řádek, který má položku *Explozivní*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="0bcbe-235">Uvolněte sadu objednávek 3 v jednom nákladu</span><span class="sxs-lookup"><span data-stu-id="0bcbe-235">Release order set 3 in one load</span></span>

<span data-ttu-id="0bcbe-236">Měly být vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="0bcbe-237">První dodávka obsahuje řádky objednávky z prodejní objednávky, kde je pole **Žádost zákazníka** nastaveno na *1*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="0bcbe-238">Druhá dodávka obsahuje řádky objednávky z prodejní objednávky, kde je pole **Žádost zákazníka** nastaveno na *2*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="0bcbe-239">Uvolněte sadu objednávek 4 v jednom nákladu</span><span class="sxs-lookup"><span data-stu-id="0bcbe-239">Release order set 4 in one load</span></span>

<span data-ttu-id="0bcbe-240">Měly být vytvořeny čtyři dodávky:</span><span class="sxs-lookup"><span data-stu-id="0bcbe-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="0bcbe-241">Řádky ze dvou objednávek pro účet zákazníka *US-003* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="0bcbe-242">Řádky ze dvou objednávek pro účet zákazníka *US-004* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="0bcbe-243">Řádky z objednávek 4-5 a 4-6 pro účet zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="0bcbe-244">Řádky z objednávek 4-7 a 4-8 pro účet zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="0bcbe-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bcbe-245">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0bcbe-245">Additional resources</span></span>

- [<span data-ttu-id="0bcbe-246">Zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="0bcbe-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="0bcbe-247">Konfigurace zásad konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="0bcbe-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
