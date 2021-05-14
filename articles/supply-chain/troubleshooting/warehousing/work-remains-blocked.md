---
title: Práce zůstává blokována
description: Práce zůstává blokována
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924123"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="24c43-103">Práce zůstává blokována</span><span class="sxs-lookup"><span data-stu-id="24c43-103">Work remains blocked</span></span>

<span data-ttu-id="24c43-104">Kód chyby: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="24c43-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="24c43-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="24c43-105">Symptoms</span></span>

<span data-ttu-id="24c43-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="24c43-106">The system shows the following error message:</span></span>

> <span data-ttu-id="24c43-107">Práce %1 zůstává blokována, protože související vlna %2 má stav %3.</span><span class="sxs-lookup"><span data-stu-id="24c43-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="24c43-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="24c43-108">Cause</span></span>

<span data-ttu-id="24c43-109">Práce se aktuálně zpracovává na vlně a nelze ji odblokovat, jak naznačuje jedna z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="24c43-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="24c43-110">Na kartě **Důvody blokování** je pole **Důvod blokování práce** pro jeden nebo více řádků nastaveno na hodnotu *Vlna zpracování*.</span><span class="sxs-lookup"><span data-stu-id="24c43-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="24c43-111">Pokud vyberte možnost **Vlna** ve skupině **Související informace** na kartě **Související informace** podokna akcí, je pole **Stav vlny** nastaveno na hodnotu *Zpracování*.</span><span class="sxs-lookup"><span data-stu-id="24c43-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="24c43-112">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="24c43-112">Resolution</span></span>

<span data-ttu-id="24c43-113">V podokně akcí na kartě **Související informace** ve skupině **Související informace** vyberte možnost **Vlna**.</span><span class="sxs-lookup"><span data-stu-id="24c43-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="24c43-114">V podokně akcí pak na stránce **Vlny** na kartě **Vlna** vyberte ve skupině **Vlna** možnost **Vyčistit data vlny**.</span><span class="sxs-lookup"><span data-stu-id="24c43-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="24c43-115">Alternativní řešení</span><span class="sxs-lookup"><span data-stu-id="24c43-115">Workaround</span></span>

<span data-ttu-id="24c43-116">Pokud předchozí kroky problém nevyřešily, můžete práci zrušit podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="24c43-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="24c43-117">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="24c43-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="24c43-118">V poli **ID práce** zadejte ID práce, kterou chcete zrušit a které aktuálně obsahuje pro možnost **Stav práce** hodnotu *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinované* nebo *Uzavřené*.</span><span class="sxs-lookup"><span data-stu-id="24c43-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="24c43-119">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="24c43-119">Select **OK**.</span></span>
1. <span data-ttu-id="24c43-120">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="24c43-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="24c43-121">Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="24c43-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
