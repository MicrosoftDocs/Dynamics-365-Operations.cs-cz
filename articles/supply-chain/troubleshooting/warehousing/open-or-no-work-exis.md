---
title: Zásilku nemůžete potvrdit z důvodu nedokončené nebo chybějící práce
description: Zásilku nemůžete potvrdit z důvodu nedokončené nebo chybějící práce
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938435"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="cfb66-103">Zásilku nemůžete potvrdit z důvodu nedokončené nebo chybějící práce</span><span class="sxs-lookup"><span data-stu-id="cfb66-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="cfb66-104">Kód chyby: WAX515</span><span class="sxs-lookup"><span data-stu-id="cfb66-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="cfb66-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="cfb66-105">Symptoms</span></span>

<span data-ttu-id="cfb66-106">Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="cfb66-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="cfb66-107">Expedici pro vytížení %1 nebylo možné potvrdit, protože musí být dokončena veškerá práce pro vytížení.</span><span class="sxs-lookup"><span data-stu-id="cfb66-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="cfb66-108">Proto nemůžete potvrdit dodání pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="cfb66-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="cfb66-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="cfb66-109">Cause</span></span>

<span data-ttu-id="cfb66-110">Náklad nebo zásilka je aktuálně ve stavu, kdy se potvrzení zásilky nezdaří.</span><span class="sxs-lookup"><span data-stu-id="cfb66-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="cfb66-111">Než budete moci zásilku potvrdit, pro dodávku musí existovat alespoň nějaká práce a veškerá tato práce musí mít stav *Uzavřeno* nebo *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="cfb66-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="cfb66-112">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="cfb66-112">Resolution</span></span>

<span data-ttu-id="cfb66-113">Zkontrolujte související prodejní objednávky nebo objednávky přenosu pro dodávku nebo zásilku a ujistěte se, že všechny související práce byly dokončeny nebo zrušeny.</span><span class="sxs-lookup"><span data-stu-id="cfb66-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="cfb66-114">Se zásilkami a dodávkami můžete pracovat na několika stránkách.</span><span class="sxs-lookup"><span data-stu-id="cfb66-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="cfb66-115">V následujících podsekcích je uvedeno několik příkladů.</span><span class="sxs-lookup"><span data-stu-id="cfb66-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="cfb66-116">Stránka se všemi zásilkami</span><span class="sxs-lookup"><span data-stu-id="cfb66-116">All loads page</span></span>

1. <span data-ttu-id="cfb66-117">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="cfb66-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cfb66-118">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="cfb66-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="cfb66-119">V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="cfb66-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="cfb66-120">Zkontrolujte stav každého pracovního ID.</span><span class="sxs-lookup"><span data-stu-id="cfb66-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="cfb66-121">Sleddujte každé ID práce, které nemá stav *Uzavřeno* nebo *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="cfb66-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="cfb66-122">Když má každé ID práce status *Uzavřeno* nebo *Zrušeno*, zkuste zásilku potvrdit znovu.</span><span class="sxs-lookup"><span data-stu-id="cfb66-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="cfb66-123">Stránka se všemi dodávkami</span><span class="sxs-lookup"><span data-stu-id="cfb66-123">All shipments page</span></span>

1. <span data-ttu-id="cfb66-124">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="cfb66-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="cfb66-125">Vyberte dodávku, kterou nelze potvrdit.</span><span class="sxs-lookup"><span data-stu-id="cfb66-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="cfb66-126">V podokně akcí na kartě **Dodávky** ve skupině **Práce** vyberte **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="cfb66-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="cfb66-127">Zkontrolujte stav každého pracovního ID.</span><span class="sxs-lookup"><span data-stu-id="cfb66-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="cfb66-128">Sleddujte každé ID práce, které nemá stav *Uzavřeno* nebo *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="cfb66-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="cfb66-129">Když má každé ID práce status *Uzavřeno* nebo *Zrušeno*, zkuste zásilku potvrdit znovu.</span><span class="sxs-lookup"><span data-stu-id="cfb66-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="cfb66-130">Stránka se všemi prácemi</span><span class="sxs-lookup"><span data-stu-id="cfb66-130">All work page</span></span>

1. <span data-ttu-id="cfb66-131">Přejděte do **Řízení skladu \> Práce\> Všechny práce**.</span><span class="sxs-lookup"><span data-stu-id="cfb66-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="cfb66-132">Vyberte práci pro číslo objednávky, u které nelze zásilku potvrdit.</span><span class="sxs-lookup"><span data-stu-id="cfb66-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="cfb66-133">V podokně akcí na kartě **Dodávky** ve skupině **Dodávky** vyberte **Potvrdit dodávku**.</span><span class="sxs-lookup"><span data-stu-id="cfb66-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="cfb66-134">Zkontrolujte stav každého pracovního ID.</span><span class="sxs-lookup"><span data-stu-id="cfb66-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="cfb66-135">Sleddujte každé ID práce, které nemá stav *Uzavřeno* nebo *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="cfb66-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="cfb66-136">Když má každé ID práce status *Uzavřeno* nebo *Zrušeno*, zkuste zásilku potvrdit znovu.</span><span class="sxs-lookup"><span data-stu-id="cfb66-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
