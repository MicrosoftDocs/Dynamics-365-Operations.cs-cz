---
title: Ruční konsolidace dodávek pomocí stránky konsolidace dodávek
description: Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno pomocí stránky konsolidace dodávek.
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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983006"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="16c1b-103">Ruční konsolidace dodávek pomocí stránky konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="16c1b-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16c1b-104">Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno pomocí stránky **Konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="16c1b-105">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="16c1b-105">Make demo data available</span></span>

<span data-ttu-id="16c1b-106">Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16c1b-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="16c1b-107">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="16c1b-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="16c1b-108">Nastavení zásad konsolidace dodávek a filtry produktů</span><span class="sxs-lookup"><span data-stu-id="16c1b-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="16c1b-109">Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="16c1b-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="16c1b-110">Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.</span><span class="sxs-lookup"><span data-stu-id="16c1b-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="16c1b-111">Vytvoření prodejních objednávek pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="16c1b-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="16c1b-112">Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat.</span><span class="sxs-lookup"><span data-stu-id="16c1b-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="16c1b-113">Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS).</span><span class="sxs-lookup"><span data-stu-id="16c1b-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="16c1b-114">Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.</span><span class="sxs-lookup"><span data-stu-id="16c1b-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="16c1b-115">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="16c1b-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="16c1b-116">Vytvoření prodejních objednávek 1 a 2</span><span class="sxs-lookup"><span data-stu-id="16c1b-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="16c1b-117">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="16c1b-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="16c1b-118">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="16c1b-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="16c1b-119">**Fond:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="16c1b-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="16c1b-120">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="16c1b-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="16c1b-121">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="16c1b-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="16c1b-122">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="16c1b-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="16c1b-123">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="16c1b-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="16c1b-124">Vytvoření prodejních objednávek 3 a 4</span><span class="sxs-lookup"><span data-stu-id="16c1b-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="16c1b-125">Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="16c1b-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="16c1b-126">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="16c1b-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="16c1b-127">**Fond:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="16c1b-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="16c1b-128">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="16c1b-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="16c1b-129">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="16c1b-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="16c1b-130">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="16c1b-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="16c1b-131">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="16c1b-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="16c1b-132">Uvolnění objednávek do skladu</span><span class="sxs-lookup"><span data-stu-id="16c1b-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="16c1b-133">Chcete-li uvolnit každou prodejní objednávku, kterou jste vytvořili pro tento scénář, do skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="16c1b-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="16c1b-134">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="16c1b-135">Vyhledejte a vyberte prodejní objednávku, kterou chcete uvolnit.</span><span class="sxs-lookup"><span data-stu-id="16c1b-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="16c1b-136">V podokně akcí na kartě **Sklad** vyberte **Akce \> Uvolnit do skladu** pro uvolnění vybrané prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="16c1b-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="16c1b-137">Tento postup opakujte pro každou další prodejní objednávku, kterou jste vytvořili pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="16c1b-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="16c1b-138">Konsolidovat dodávky</span><span class="sxs-lookup"><span data-stu-id="16c1b-138">Consolidate shipments</span></span>

1. <span data-ttu-id="16c1b-139">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="16c1b-140">Najděte a vyberte dodávku, která byla vytvořena při uvolnění prodejní objednávky 1 do skladu.</span><span class="sxs-lookup"><span data-stu-id="16c1b-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="16c1b-141">(Její pole **Zásada konsolidace dodávky** by mělo být nastaveno na *Fond objednávek* .)</span><span class="sxs-lookup"><span data-stu-id="16c1b-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="16c1b-142">V podokně akcí na kartě **Dodávky** zvolte **Dodávky \> Konsolidovat dodávky**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="16c1b-143">Ověřte dodávky, které jsou navrženy pro konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="16c1b-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="16c1b-144">Ke konsolidaci by měla být navržena pouze jedna dodávka, která má stejnou zásadu.</span><span class="sxs-lookup"><span data-stu-id="16c1b-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="16c1b-145">Zavřete stránku **Konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="16c1b-146">Najděte a vyberte dodávku, která byla vytvořena při uvolnění prodejní objednávky 3 do skladu.</span><span class="sxs-lookup"><span data-stu-id="16c1b-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="16c1b-147">(Její pole **Zásada konsolidace dodávky** by mělo být nastaveno na *Výchozí* .)</span><span class="sxs-lookup"><span data-stu-id="16c1b-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="16c1b-148">V podokně akcí na kartě **Dodávky** zvolte **Dodávky \> Konsolidovat dodávky**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="16c1b-149">Ověřte, že nejsou navrženy žádné dodávky pro konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="16c1b-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="16c1b-150">Vyberte **Zobrazit filtry**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="16c1b-151">V podokně **Filtry** odeberte filtr **Číslo objednávky** a poté vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="16c1b-152">Ověřte dodávky, které jsou navrženy pro konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="16c1b-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="16c1b-153">Ke konsolidaci by měla být navržena pouze jedna dodávka, která má stejnou zásadu.</span><span class="sxs-lookup"><span data-stu-id="16c1b-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16c1b-154">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="16c1b-154">Additional resources</span></span>

- [<span data-ttu-id="16c1b-155">Zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="16c1b-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="16c1b-156">Konfigurace zásad konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="16c1b-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)