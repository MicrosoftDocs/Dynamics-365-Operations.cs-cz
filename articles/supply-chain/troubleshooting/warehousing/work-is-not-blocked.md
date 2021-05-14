---
title: Práce není blokována
description: Práce není blokována
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924197"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="72b68-103">Práce není blokována</span><span class="sxs-lookup"><span data-stu-id="72b68-103">Work isn't blocked</span></span>

<span data-ttu-id="72b68-104">Kód chyby: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="72b68-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="72b68-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="72b68-105">Symptoms</span></span>

<span data-ttu-id="72b68-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="72b68-106">The system shows the following error message:</span></span>

> <span data-ttu-id="72b68-107">Práce s ID %1 není blokována.</span><span class="sxs-lookup"><span data-stu-id="72b68-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="72b68-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="72b68-108">Cause</span></span>

<span data-ttu-id="72b68-109">Možnost **Blokovaná vlna** na vlně je nastavena na hodnotu *Ne*.</span><span class="sxs-lookup"><span data-stu-id="72b68-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="72b68-110">Práci nelze odblokovat, protože aktuálně není blokována.</span><span class="sxs-lookup"><span data-stu-id="72b68-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="72b68-111">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="72b68-111">Resolution</span></span>

 <span data-ttu-id="72b68-112">Práci lze odblokovat pouze v případě, že je možnost **Blokovaná vlna** nastavena na hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="72b68-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
