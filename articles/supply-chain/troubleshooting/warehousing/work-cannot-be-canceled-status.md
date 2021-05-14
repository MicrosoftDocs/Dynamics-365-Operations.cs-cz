---
title: Práce nelze zrušit kvůli jejímu stavu
description: Práce nelze zrušit kvůli jejímu stavu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924248"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="df711-103">Práce nelze zrušit kvůli jejímu stavu</span><span class="sxs-lookup"><span data-stu-id="df711-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="df711-104">Kód chyby: WAX2190</span><span class="sxs-lookup"><span data-stu-id="df711-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="df711-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="df711-105">Symptoms</span></span>

<span data-ttu-id="df711-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="df711-106">The system shows the following error message:</span></span>

> <span data-ttu-id="df711-107">Nelze zrušit práci %1, protože má stav %2.</span><span class="sxs-lookup"><span data-stu-id="df711-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="df711-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="df711-108">Cause</span></span>

<span data-ttu-id="df711-109">Práce nemůže být zrušena v aktuálním stavu.</span><span class="sxs-lookup"><span data-stu-id="df711-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="df711-110">Záhlaví práce nebo řádky práce nemají očekávanou hodnotu **Stav práce**.</span><span class="sxs-lookup"><span data-stu-id="df711-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="df711-111">Pole **Stav práce** v záhlaví práce není nastaveno na hodnotu *Otevřeno* nebo *Probíhá*.</span><span class="sxs-lookup"><span data-stu-id="df711-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="df711-112">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="df711-112">Resolution</span></span>

<span data-ttu-id="df711-113">Chcete-li zrušit práci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="df711-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="df711-114">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="df711-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="df711-115">Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="df711-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="df711-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="df711-116">Select **OK**.</span></span>
1. <span data-ttu-id="df711-117">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="df711-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="df711-118">Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="df711-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
