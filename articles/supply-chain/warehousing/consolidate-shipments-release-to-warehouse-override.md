---
title: Konsolidace dodávek, když je zásada konsolidace dodávek přepsána ze stránky Uvolnění do skladu
description: Toto téma představuje scénář, ve kterém musí být jeden nebo více řádků prodeje ručně uvolněn do skladu ze stránky uvolnění do skladu a před uvolněním musí být přepsána zásada konsolidace dodávek definovaná systémem.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: be573f3a137fbd74ba2f5d8bb346e4bb9f9116c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237100"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="f57e0-103">Konsolidace dodávek, když je zásada konsolidace dodávek přepsána ze stránky Uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="f57e0-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f57e0-104">Toto téma představuje scénář, ve kterém musí být jeden nebo více řádků prodeje ručně uvolněn do skladu ze stránky **uvolnění do skladu** a před uvolněním musí být přepsána zásada konsolidace dodávek definovaná systémem.</span><span class="sxs-lookup"><span data-stu-id="f57e0-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="f57e0-105">Může být vyžadováno přepsání zásady konsolidace dodávek, pokud například objednávka, která není obvykle konsolidována s otevřenými dodávkami, musí být konsolidována s otevřenými dodávkami.</span><span class="sxs-lookup"><span data-stu-id="f57e0-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="f57e0-106">Během scénáře vytvoříte sadu prodejních objednávek a poté před uvolněním objednávek do skladu přepíšete výchozí zásadu konsolidace dodávek.</span><span class="sxs-lookup"><span data-stu-id="f57e0-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="f57e0-107">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="f57e0-107">Make demo data available</span></span>

<span data-ttu-id="f57e0-108">Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f57e0-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f57e0-109">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="f57e0-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="f57e0-110">Nastavení zásad konsolidace dodávek a filtry produktů</span><span class="sxs-lookup"><span data-stu-id="f57e0-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="f57e0-111">Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány.</span><span class="sxs-lookup"><span data-stu-id="f57e0-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="f57e0-112">Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.</span><span class="sxs-lookup"><span data-stu-id="f57e0-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="f57e0-113">Vytvoření prodejních objednávek pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="f57e0-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="f57e0-114">Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte tři identické prodejní objednávky, které mají následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f57e0-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f57e0-115">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="f57e0-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="f57e0-116">Přidejte řádek objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="f57e0-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f57e0-117">**Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)</span><span class="sxs-lookup"><span data-stu-id="f57e0-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f57e0-118">**Množství:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f57e0-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f57e0-119">Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="f57e0-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="f57e0-120">Uvolněte prodejní objednávky ze stránky Uvolnění do skladu</span><span class="sxs-lookup"><span data-stu-id="f57e0-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="f57e0-121">Postupujte podle těchto kroků a přepište zásadu konsolidace dodávek během uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="f57e0-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="f57e0-122">Přejděte na **Řízení skladu \> Uvolnění do skladu \> Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="f57e0-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="f57e0-123">V horním podokně vyberte první prodejní objednávku, kterou jste vytvořili pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="f57e0-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="f57e0-124">Vyberte **Přidat** a přidejte řádek do vydání do skladu.</span><span class="sxs-lookup"><span data-stu-id="f57e0-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="f57e0-125">Všimněte si, že *Výchozí* zásada konsolidace dodávek je použita ve spodním podokně.</span><span class="sxs-lookup"><span data-stu-id="f57e0-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="f57e0-126">Ve spodním podokně zvolte **Vybrat zásady konsolidace dodávky**.</span><span class="sxs-lookup"><span data-stu-id="f57e0-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="f57e0-127">Vyberte zásadu, která umožňuje konsolidaci s ostatními otevřenými dodávkami stejné zásady.</span><span class="sxs-lookup"><span data-stu-id="f57e0-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="f57e0-128">Například vyberte zásadu *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="f57e0-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="f57e0-129">Vyberte **Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="f57e0-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f57e0-130">Vyberte druhou a třetí prodejní objednávku, které jste vytvořili pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="f57e0-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="f57e0-131">Vyberte **Přidat** a přidejte řádky do vydání do skladu.</span><span class="sxs-lookup"><span data-stu-id="f57e0-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="f57e0-132">Všimněte si, že *Výchozí* zásada je použita ve spodním podokně.</span><span class="sxs-lookup"><span data-stu-id="f57e0-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="f57e0-133">Vyberte druhý řádek a poté v poli **Vybrat novou zásadu konsolidace dodávek** vyberte zásadu *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="f57e0-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="f57e0-134">Vyberte **Uvolnění do skladu** pro obě řádky.</span><span class="sxs-lookup"><span data-stu-id="f57e0-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="f57e0-135">Ověření dodávek</span><span class="sxs-lookup"><span data-stu-id="f57e0-135">Verify the shipments</span></span>

<span data-ttu-id="f57e0-136">Měly být vytvořeny dvě dodávky:</span><span class="sxs-lookup"><span data-stu-id="f57e0-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="f57e0-137">První dodávka obsahuje dva řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="f57e0-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="f57e0-138">Druhá dodávka obsahuje jeden řádek a byla vytvořena pomocí zásady konsolidace dodávek *Výchozí*.</span><span class="sxs-lookup"><span data-stu-id="f57e0-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="f57e0-139">Použijte tyto kroky ke kontrole vytvořených dodávek.</span><span class="sxs-lookup"><span data-stu-id="f57e0-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="f57e0-140">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="f57e0-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="f57e0-141">Najděte a vyberte požadovanou dodávku.</span><span class="sxs-lookup"><span data-stu-id="f57e0-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="f57e0-142">V poli **Zásady konsolidace dodávek** zkontrolujte zásadu konsolidace použitou při vytvoření dodávky.</span><span class="sxs-lookup"><span data-stu-id="f57e0-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f57e0-143">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f57e0-143">Additional resources</span></span>

- [<span data-ttu-id="f57e0-144">Zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="f57e0-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="f57e0-145">Konfigurace zásad konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="f57e0-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]