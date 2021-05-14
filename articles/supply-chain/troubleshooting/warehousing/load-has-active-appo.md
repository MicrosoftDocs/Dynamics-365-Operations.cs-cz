---
title: Zásilku nemůžete potvrdit kvůli problému s kalendářem
description: Zásilku nemůžete potvrdit kvůli problému s kalendářem
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938436"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="be465-103">Zásilku nemůžete potvrdit kvůli problému s kalendářem</span><span class="sxs-lookup"><span data-stu-id="be465-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="be465-104">Kód chyby: TRX2716</span><span class="sxs-lookup"><span data-stu-id="be465-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="be465-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="be465-105">Symptoms</span></span>

<span data-ttu-id="be465-106">Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="be465-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="be465-107">Typ kalendáře %1 vyžaduje, aby byla schůzka %2 zaregistrována a zarezervována.</span><span class="sxs-lookup"><span data-stu-id="be465-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="be465-108">Proto nemůžete potvrdit dodání pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="be465-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="be465-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="be465-109">Cause</span></span>

<span data-ttu-id="be465-110">Aktivní události pro načtení existují.</span><span class="sxs-lookup"><span data-stu-id="be465-110">Active appointments for the load exist.</span></span> <span data-ttu-id="be465-111">Například existuje pravidlo, které vyžaduje přihlášení řidiče.</span><span class="sxs-lookup"><span data-stu-id="be465-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="be465-112">Náklad je proto aktuálně ve stavu, kdy se potvrzení zásilky nezdaří.</span><span class="sxs-lookup"><span data-stu-id="be465-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="be465-113">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="be465-113">Resolution</span></span>

<span data-ttu-id="be465-114">Musíte prozkoumat a opravit všechny problémy s aktivními událostmi, které jsou spojeny s nákladem.</span><span class="sxs-lookup"><span data-stu-id="be465-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="be465-115">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="be465-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="be465-116">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="be465-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="be465-117">V podokně akcí na kartě **Přeprava** ve skupině **Události** vyberte **Plánování událostí**.</span><span class="sxs-lookup"><span data-stu-id="be465-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="be465-118">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="be465-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="be465-119">Ujistěte se, že check-in/check-out řidiče pro událost dokončen.</span><span class="sxs-lookup"><span data-stu-id="be465-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="be465-120">Dokončete nebo zrušte schůzku.</span><span class="sxs-lookup"><span data-stu-id="be465-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="be465-121">Zakažte možnost **Vyžaduje se přihlášení řidiče** souvisejícího pravidla události.</span><span class="sxs-lookup"><span data-stu-id="be465-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
