---
title: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
description: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938434"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="69f2a-103">Zásilku nemůžete potvrdit, protože položky nebyly vybrány</span><span class="sxs-lookup"><span data-stu-id="69f2a-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="69f2a-104">Kód chyby: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="69f2a-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="69f2a-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="69f2a-105">Symptoms</span></span>

<span data-ttu-id="69f2a-106">Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="69f2a-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="69f2a-107">Některé položky, které jsou nezbytné pro vytížení %1, dosud nebyly vyzvednuty a přesunuty na konečné skladové místo.</span><span class="sxs-lookup"><span data-stu-id="69f2a-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="69f2a-108">Proto nemůžete potvrdit dodání pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="69f2a-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="69f2a-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="69f2a-109">Cause</span></span>

<span data-ttu-id="69f2a-110">Dodávku nebo zásilku nelze v aktuálním stavu potvrdit, protože může existovat jedna z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="69f2a-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="69f2a-111">Související práce ještě nebyly vybrány a přesunuty na konečné místo dodání.</span><span class="sxs-lookup"><span data-stu-id="69f2a-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="69f2a-112">Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.</span><span class="sxs-lookup"><span data-stu-id="69f2a-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="69f2a-113">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="69f2a-113">Resolution</span></span>

<span data-ttu-id="69f2a-114">Zkontrolujte související prodejní objednávky nebo objednávky přenosu pro dodávku nebo zásilku.</span><span class="sxs-lookup"><span data-stu-id="69f2a-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="69f2a-115">Ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.</span><span class="sxs-lookup"><span data-stu-id="69f2a-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="69f2a-116">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="69f2a-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="69f2a-117">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="69f2a-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="69f2a-118">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.</span><span class="sxs-lookup"><span data-stu-id="69f2a-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="69f2a-119">Poznamenejte si hodnotu pole **Množství vytvořených prací**.</span><span class="sxs-lookup"><span data-stu-id="69f2a-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="69f2a-120">V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="69f2a-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="69f2a-121">Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.</span><span class="sxs-lookup"><span data-stu-id="69f2a-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="69f2a-122">Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.</span><span class="sxs-lookup"><span data-stu-id="69f2a-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
