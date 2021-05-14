---
title: Zásilku nemůžete potvrdit, protože je prázdná
description: Zásilku nemůžete potvrdit, protože je prázdná
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938433"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="68b6a-103">Zásilku nemůžete potvrdit, protože je prázdná</span><span class="sxs-lookup"><span data-stu-id="68b6a-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="68b6a-104">Kód chyby: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="68b6a-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="68b6a-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="68b6a-105">Symptoms</span></span>

<span data-ttu-id="68b6a-106">Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="68b6a-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="68b6a-107">Řádek nákladu pro položku %1 a dodávka %2 byly aktualizovány tak, aby měly nulové množství kvůli nastavení nedostatečné dodávky, které neumožňuje odeslat jakékoliv množství pro tuto položku.</span><span class="sxs-lookup"><span data-stu-id="68b6a-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="68b6a-108">Proto nemůžete potvrdit dodání pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="68b6a-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="68b6a-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="68b6a-109">Cause</span></span>

<span data-ttu-id="68b6a-110">Systém vyhodnotí, zda je vybrané množství v očekávaných mezích, na základě vybraného množství, množství načtené linky a procenta nedostatečného doručení.</span><span class="sxs-lookup"><span data-stu-id="68b6a-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="68b6a-111">Pokud systém zjistí, že vybrané množství na řádku nákladu je 0 (nula), nemůžete dodávku potvrdit.</span><span class="sxs-lookup"><span data-stu-id="68b6a-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="68b6a-112">Například k tomuto problému může dojít, pokud byla práce zrušena a procento nedoručení na řádku nákladu je 100 procent.</span><span class="sxs-lookup"><span data-stu-id="68b6a-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="68b6a-113">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="68b6a-113">Resolution</span></span>

<span data-ttu-id="68b6a-114">Zkontrolujte řádky nákladu a ujistěte se, že procento a množství podlimitního doručení je v souladu s vybranou prací.</span><span class="sxs-lookup"><span data-stu-id="68b6a-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="68b6a-115">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="68b6a-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="68b6a-116">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="68b6a-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="68b6a-117">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento pro snížení dodávky.</span><span class="sxs-lookup"><span data-stu-id="68b6a-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="68b6a-118">Upravte hodnotu pole **Nedostatečné doručení** nebo **Množství** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="68b6a-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="68b6a-119">Pokud problém stále není vyřešen, možná budete muset dokončit další vychystávací práce pro související prodejní objednávky nebo objednávky přenosu, dokud nebude dostupné množství v souladu s nákladem nebo zásilkou.</span><span class="sxs-lookup"><span data-stu-id="68b6a-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
