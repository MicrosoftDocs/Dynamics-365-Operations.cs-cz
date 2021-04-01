---
title: Konsolidace dodávek pomocí pracovní plochy dodávek zásilek
description: Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno do dodávek pomocí pracovní plochy konsolidace dodávek.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9b7dc72d789fd331c3636c406ac6a45566ba81ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242174"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="f0fad-103">Konsolidace dodávek pomocí pracovní plochy dodávek zásilek</span><span class="sxs-lookup"><span data-stu-id="f0fad-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0fad-104">Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno do dodávek pomocí pracovní plochy konsolidace dodávek.</span><span class="sxs-lookup"><span data-stu-id="f0fad-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="f0fad-105">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="f0fad-105">Make demo data available</span></span>

<span data-ttu-id="f0fad-106">Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0fad-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f0fad-107">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="f0fad-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="f0fad-108">Nastavení zásad konsolidace dodávek a filtry produktů</span><span class="sxs-lookup"><span data-stu-id="f0fad-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="f0fad-109">Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="f0fad-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="f0fad-110">Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.</span><span class="sxs-lookup"><span data-stu-id="f0fad-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="f0fad-111">Zapnutí funkce rušní konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="f0fad-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="f0fad-112">Než budete moci používat funkci *Ruční konsolidace dodávek*, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="f0fad-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="f0fad-113">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="f0fad-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="f0fad-114">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="f0fad-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f0fad-115">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="f0fad-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f0fad-116">**Název funkce:** *Ruční konsolidace dodávek*</span><span class="sxs-lookup"><span data-stu-id="f0fad-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="f0fad-117">Jak bylo uvedeno v [zásadách konfigurace konsolidace dodávek](configure-shipment-consolidation-policies.md), musíte také zapnout funkci *Konsolidovat dodávku* před vytvořením zásad.</span><span class="sxs-lookup"><span data-stu-id="f0fad-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="f0fad-118">Tento krok byste však již měli dokončit.</span><span class="sxs-lookup"><span data-stu-id="f0fad-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="f0fad-119">Vytvoření prodejních objednávek pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="f0fad-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="f0fad-120">Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat.</span><span class="sxs-lookup"><span data-stu-id="f0fad-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="f0fad-121">Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="f0fad-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="f0fad-122">Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.</span><span class="sxs-lookup"><span data-stu-id="f0fad-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="f0fad-123">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="f0fad-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="f0fad-124">Vytvoření sady objednávek 1</span><span class="sxs-lookup"><span data-stu-id="f0fad-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="f0fad-125">Prodejní objednávky 1-1 a 1-2</span><span class="sxs-lookup"><span data-stu-id="f0fad-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="f0fad-126">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-127">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f0fad-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f0fad-128">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f0fad-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f0fad-129">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-130">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-131">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-132">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="f0fad-133">Prodejní objednávka 1-3</span><span class="sxs-lookup"><span data-stu-id="f0fad-133">Sales order 1-3</span></span>

1. <span data-ttu-id="f0fad-134">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-135">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f0fad-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f0fad-136">**Způsob dodání:** *10*</span><span class="sxs-lookup"><span data-stu-id="f0fad-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="f0fad-137">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-138">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-139">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-140">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="f0fad-141">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-142">**Číslo položky:** *A0002* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-143">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="f0fad-144">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f0fad-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f0fad-145">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci druhého řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="f0fad-146">Vytvoření sady objednávek 2</span><span class="sxs-lookup"><span data-stu-id="f0fad-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="f0fad-147">Prodejní objednávky 2-1 a 2-2</span><span class="sxs-lookup"><span data-stu-id="f0fad-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="f0fad-148">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-149">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="f0fad-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="f0fad-150">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f0fad-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f0fad-151">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-152">**Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)</span><span class="sxs-lookup"><span data-stu-id="f0fad-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="f0fad-153">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-154">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="f0fad-155">Přidejte druhý řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-156">**Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)</span><span class="sxs-lookup"><span data-stu-id="f0fad-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="f0fad-157">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="f0fad-158">**Způsob doručení:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f0fad-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f0fad-159">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci druhého řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="f0fad-160">Vytvoření sady objednávek 3</span><span class="sxs-lookup"><span data-stu-id="f0fad-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="f0fad-161">Prodejní objednávky 3-1 a 3-2</span><span class="sxs-lookup"><span data-stu-id="f0fad-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="f0fad-162">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-163">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f0fad-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f0fad-164">**Žádost zákazníka:** *1*</span><span class="sxs-lookup"><span data-stu-id="f0fad-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="f0fad-165">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-166">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-167">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-168">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="f0fad-169">Prodejní objednávky 3-3 a 3-4</span><span class="sxs-lookup"><span data-stu-id="f0fad-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="f0fad-170">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-171">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f0fad-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f0fad-172">**Žádost zákazníka:** *2*</span><span class="sxs-lookup"><span data-stu-id="f0fad-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="f0fad-173">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-174">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-175">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-176">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="f0fad-177">Vytvoření sady objednávek 4</span><span class="sxs-lookup"><span data-stu-id="f0fad-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="f0fad-178">Prodejní objednávky 4-1 a 4-2</span><span class="sxs-lookup"><span data-stu-id="f0fad-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="f0fad-179">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-180">**Účet zákazníka:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="f0fad-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="f0fad-181">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-182">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-183">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-184">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="f0fad-185">Prodejní objednávky 4-3 a 4-4</span><span class="sxs-lookup"><span data-stu-id="f0fad-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="f0fad-186">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-187">**Účet zákazníka:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="f0fad-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="f0fad-188">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-189">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-190">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-191">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="f0fad-192">Prodejní objednávky 4-5 a 4-6</span><span class="sxs-lookup"><span data-stu-id="f0fad-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="f0fad-193">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-194">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f0fad-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f0fad-195">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="f0fad-195">**Site:** *6*</span></span>
    - <span data-ttu-id="f0fad-196">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="f0fad-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f0fad-197">**Fond:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="f0fad-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="f0fad-198">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-199">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-200">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-201">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="f0fad-202">Prodejní objednávky 4-7 a 4-8</span><span class="sxs-lookup"><span data-stu-id="f0fad-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="f0fad-203">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f0fad-204">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f0fad-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f0fad-205">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="f0fad-205">**Site:** *6*</span></span>
    - <span data-ttu-id="f0fad-206">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="f0fad-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f0fad-207">**Fond:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="f0fad-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="f0fad-208">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f0fad-209">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f0fad-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f0fad-210">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f0fad-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f0fad-211">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="f0fad-212">Uvolnění objednávek do skladu</span><span class="sxs-lookup"><span data-stu-id="f0fad-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="f0fad-213">Chcete-li uvolnit každou prodejní objednávku, kterou jste vytvořili pro tento scénář, do skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f0fad-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="f0fad-214">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f0fad-215">Vyhledejte a vyberte prodejní objednávku, kterou chcete uvolnit.</span><span class="sxs-lookup"><span data-stu-id="f0fad-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="f0fad-216">V podokně akcí na kartě **Sklad** vyberte **Akce \> Uvolnit do skladu** pro uvolnění vybrané prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="f0fad-217">Tento postup opakujte pro každou další prodejní objednávku, kterou jste vytvořili pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="f0fad-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="f0fad-218">Konsolidace dodávek pomocí pracovní plochy konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="f0fad-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="f0fad-219">Přejděte na **Řízení skladu \> Uvolnění do skladu \> Pracovní plocha konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="f0fad-220">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f0fad-221">V dialogovém okně editoru dotazů na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f0fad-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="f0fad-222">**Tabulka:** *Prodejní objednávky*</span><span class="sxs-lookup"><span data-stu-id="f0fad-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="f0fad-223">**Pole:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="f0fad-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="f0fad-224">**Kritéria:** Zadejte čárkami oddělený seznam čísel prodejních objednávek pro každou sadu objednávek, kterou jste vytvořili pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="f0fad-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="f0fad-225">Vyberte **OK**, uložte svůj dotaz a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="f0fad-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="f0fad-226">V podokně akcí klikněte na možnost **Konsolidovat dodávky**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="f0fad-227">Vyberte všechny dodávky a poté vyberte v podokně akcí možnost **Konsolidovat**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="f0fad-228">Ověření dodávek</span><span class="sxs-lookup"><span data-stu-id="f0fad-228">Verify the shipments</span></span>

<span data-ttu-id="f0fad-229">Následující postup umožňuje ověřit dodávky, které byly vytvořeny nebo aktualizovány v důsledku konsolidace dodávky.</span><span class="sxs-lookup"><span data-stu-id="f0fad-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="f0fad-230">Použijte ho ke kontrole každé sady objednávek, kterou jste vytvořili pro tento scénář, a poté zkontrolujte následující pododdíly, abyste se ujistili, že jste dosáhli očekávaných výsledků.</span><span class="sxs-lookup"><span data-stu-id="f0fad-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="f0fad-231">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="f0fad-232">Najděte a vyberte požadovanou dodávku.</span><span class="sxs-lookup"><span data-stu-id="f0fad-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="f0fad-233">Pokud byla při vytváření nebo aktualizaci dodávky použita zásada konsolidace, měli byste ji vidět v poli **Zásada konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="f0fad-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="f0fad-234">Související dodávky pro sadu objednávek 1</span><span class="sxs-lookup"><span data-stu-id="f0fad-234">Related shipments for order set 1</span></span>

<span data-ttu-id="f0fad-235">Měly být vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="f0fad-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="f0fad-236">První dodávka obsahuje tři řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="f0fad-237">Druhá dodávka, která nepoužívá způsob dopravy *Airways*, byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="f0fad-238">Související dodávky pro sadu objednávek 2</span><span class="sxs-lookup"><span data-stu-id="f0fad-238">Related shipments for order set 2</span></span>

<span data-ttu-id="f0fad-239">Měly být vytvořeny tři dodávky:</span><span class="sxs-lookup"><span data-stu-id="f0fad-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="f0fad-240">První dodávka obsahuje položky *Hořlavý*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="f0fad-241">Každá ze dvou dalších zásilek obsahuje jeden řádek, který má položku *Explozivní*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="f0fad-242">Související dodávky pro sadu objednávek 3</span><span class="sxs-lookup"><span data-stu-id="f0fad-242">Related shipments for order set 3</span></span>

<span data-ttu-id="f0fad-243">Měly být vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="f0fad-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="f0fad-244">První dodávka obsahuje řádky objednávky z prodejní objednávky, kde je pole **Žádost zákazníka** nastaveno na *1*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="f0fad-245">Druhá dodávka obsahuje řádky objednávky z prodejní objednávky, kde je pole **Žádost zákazníka** nastaveno na *2*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="f0fad-246">Související dodávky pro sadu objednávek 4</span><span class="sxs-lookup"><span data-stu-id="f0fad-246">Related shipments for order set 4</span></span>

<span data-ttu-id="f0fad-247">Měly být vytvořeny čtyři dodávky:</span><span class="sxs-lookup"><span data-stu-id="f0fad-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="f0fad-248">Řádky ze dvou objednávek pro zákazníka *US-003* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f0fad-249">Řádky ze dvou objednávek pro zákazníka *US-004* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f0fad-250">Řádky z objednávek 4-5 a 4-6 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f0fad-251">Řádky z objednávek 4-7 a 4-8 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="f0fad-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0fad-252">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f0fad-252">Additional resources</span></span>

- [<span data-ttu-id="f0fad-253">Zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="f0fad-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="f0fad-254">Konfigurace zásad konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="f0fad-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]