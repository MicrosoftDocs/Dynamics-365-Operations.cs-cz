---
title: Zrušení plánovací úlohy
description: Toto téma vysvětluje způsob zrušení aktivní plánovací úlohy, která používá funkci optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773920"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="02645-103">Zrušení plánovací úlohy</span><span class="sxs-lookup"><span data-stu-id="02645-103">Cancel a planning job</span></span>

<span data-ttu-id="02645-104">V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete zrušit aktivní plánovací úlohy, která používá funkci optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="02645-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="02645-105">Chcete-li zrušit aktivní plánovací úlohu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="02645-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="02645-106">Lze zrušit pouze aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="02645-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="02645-107">Přejděte na **Hlavní plánování \> Nastavení \> Plány**.</span><span class="sxs-lookup"><span data-stu-id="02645-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="02645-108">Vyberte příslušný plán pro spuštění plánování.</span><span class="sxs-lookup"><span data-stu-id="02645-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="02645-109">Zvolte možnost **Historie**.</span><span class="sxs-lookup"><span data-stu-id="02645-109">Select **History**.</span></span>
4. <span data-ttu-id="02645-110">Vybrat plánovací úlohu ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="02645-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="02645-111">Vyberte možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="02645-111">Select **Cancel**.</span></span>

<span data-ttu-id="02645-112">Stav úlohy bude **Probíhá zrušení**, dokud služba optimalizace plánování nepotvrdí, že úloha byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="02645-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="02645-113">Stav se změní na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="02645-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="02645-114">Chcete-li zobrazit změny stavu, je nutné aktualizovat stránku výběrem tlačítka **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="02645-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="02645-115">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="02645-115">Related resources</span></span>

[<span data-ttu-id="02645-116">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="02645-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="02645-117">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="02645-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="02645-118">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="02645-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="02645-119">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="02645-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="02645-120">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="02645-120">Apply filters to a plan</span></span>](plan-filters.md)
