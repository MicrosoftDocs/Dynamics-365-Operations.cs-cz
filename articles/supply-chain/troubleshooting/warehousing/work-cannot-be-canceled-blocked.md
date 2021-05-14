---
title: Práce nelze zrušit, protože je blokována
description: Práce nelze zrušit, protože je blokována
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924272"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="362a6-103">Práce nelze zrušit, protože je blokována</span><span class="sxs-lookup"><span data-stu-id="362a6-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="362a6-104">Kód chyby: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="362a6-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="362a6-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="362a6-105">Symptoms</span></span>

<span data-ttu-id="362a6-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="362a6-106">The system shows the following error message:</span></span>

> <span data-ttu-id="362a6-107">Práci %1 nelze zrušit, protože je blokována s typem důvodu %2.</span><span class="sxs-lookup"><span data-stu-id="362a6-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="362a6-108">Než bude práci možné zrušit, musíte zrušit její blokování.</span><span class="sxs-lookup"><span data-stu-id="362a6-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="362a6-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="362a6-109">Cause</span></span>

<span data-ttu-id="362a6-110">Práce je blokována a nelze ji zrušit.</span><span class="sxs-lookup"><span data-stu-id="362a6-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="362a6-111">Na stránce **Práce** na kartě **Obecné** je možnost **Blokováno** nastavena na hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="362a6-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="362a6-112">Toto nastavení označuje, že práce je blokována.</span><span class="sxs-lookup"><span data-stu-id="362a6-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="362a6-113">Na kartě **Důvody blokování** je zobrazeno, proč byla práce zablokována.</span><span class="sxs-lookup"><span data-stu-id="362a6-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="362a6-114">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="362a6-114">Resolution</span></span>

<span data-ttu-id="362a6-115">Chcete-li práci odblokovat, vyberte kartu **Důvody blokování** a potom proveďte jeden z těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="362a6-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="362a6-116">Pokud je pole **Důvod blokování práce** nastaveno na hodnotu *Nedefinovaný důvod*: V podokně akcí na kartě **Práce** ve skupině **Práce** vyberte možnost **Odblokovat práci**.</span><span class="sxs-lookup"><span data-stu-id="362a6-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="362a6-117">Pokud je pole **Důvod blokování práce** nastaveno na hodnotu *Vlna zpracování*: V podokně akcí na kartě **Související informace** ve skupině **Související informace** vyberte možnost **Vlna**.</span><span class="sxs-lookup"><span data-stu-id="362a6-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="362a6-118">V podokně akcí pak na stránce **Vlny** na kartě **Vlna** vyberte ve skupině **Vlna** možnost **Vyčistit data vlny**.</span><span class="sxs-lookup"><span data-stu-id="362a6-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="362a6-119">Alternativní řešení</span><span class="sxs-lookup"><span data-stu-id="362a6-119">Workaround</span></span>

<span data-ttu-id="362a6-120">Pokud předchozí kroky problém nevyřešily, můžete práci zrušit podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="362a6-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="362a6-121">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="362a6-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="362a6-122">V poli **ID práce** zadejte ID práce, kterou chcete zrušit a které aktuálně obsahuje pro možnost **Stav práce** hodnotu *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinované* nebo *Uzavřené*.</span><span class="sxs-lookup"><span data-stu-id="362a6-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="362a6-123">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="362a6-123">Select **OK**.</span></span>
1. <span data-ttu-id="362a6-124">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="362a6-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="362a6-125">Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="362a6-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
