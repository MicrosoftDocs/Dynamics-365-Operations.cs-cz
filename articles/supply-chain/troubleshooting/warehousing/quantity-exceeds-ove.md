---
title: Dodávku nemůžete potvrdit, protože množství překračuje procento navýšení dodávky
description: Dodávku nemůžete potvrdit, protože množství překračuje procento navýšení dodávky
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938437"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="2ed2f-103">Dodávku nemůžete potvrdit, protože množství překračuje procento navýšení dodávky</span><span class="sxs-lookup"><span data-stu-id="2ed2f-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="2ed2f-104">Kód chyby: WAX1687</span><span class="sxs-lookup"><span data-stu-id="2ed2f-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="2ed2f-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="2ed2f-105">Symptoms</span></span>

<span data-ttu-id="2ed2f-106">Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="2ed2f-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="2ed2f-107">Dodávku pro náklad %1 nelze potvrdit, protože množství pro položku %2 překračuje procento definované pro navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="2ed2f-108">Proto nemůžete potvrdit dodání pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="2ed2f-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="2ed2f-109">Cause</span></span>

<span data-ttu-id="2ed2f-110">Množství nákladu nebo dodávky bylo vyskladněno pouze částečně.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="2ed2f-111">Množství aktuálně převyšuje vybrané množství o procento, které je mimo povolené procento pro navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="2ed2f-112">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="2ed2f-112">Resolution</span></span>

<span data-ttu-id="2ed2f-113">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="2ed2f-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="2ed2f-114">Nastavte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-114">Set the load line quantity.</span></span>
- <span data-ttu-id="2ed2f-115">Nastavte procento navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="2ed2f-116">Nastavení množství řádku nákladu</span><span class="sxs-lookup"><span data-stu-id="2ed2f-116">Set the load line quantity</span></span>

<span data-ttu-id="2ed2f-117">Chcete-li nastavit množství řádku nákladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="2ed2f-118">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2ed2f-119">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="2ed2f-120">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="2ed2f-121">Na záložce s náhledem **Detaily řádku** vyberte možnost **Objednat**.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="2ed2f-122">V poli **Množství** nastavte hodnotu na vyskladněné množství (tj. na hodnotu **Množství vytvořené prací**), aby mohlo dojít k potvrzení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="2ed2f-123">Nastavení procenta navýšení dodávky</span><span class="sxs-lookup"><span data-stu-id="2ed2f-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="2ed2f-124">Chcete-li nastavit procenta snížení dodávky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="2ed2f-125">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2ed2f-126">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="2ed2f-127">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="2ed2f-128">Na záložce s náhledem **Detaily řádku** vyberte možnost **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="2ed2f-129">V poli **Navýšení dodávky** nastavte hodnotu na větší procento, které odpovídá množství, které bylo vybráno oproti množství naložení, aby mohlo dojít k potvrzení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2ed2f-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
