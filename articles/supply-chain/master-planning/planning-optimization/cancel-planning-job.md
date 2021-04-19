---
title: Zrušení plánovací úlohy
description: Toto téma vysvětluje způsob zrušení aktivní plánovací úlohy, která používá funkci optimalizace plánování.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833322"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="bfbcf-103">Zrušení plánovací úlohy</span><span class="sxs-lookup"><span data-stu-id="bfbcf-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bfbcf-104">V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete zrušit aktivní plánovací úlohy, která používá funkci optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="bfbcf-105">Pokud v dialogovém okně vyberete možnost **Zrušit**, když je úloha optimalizace plánování spuštěna přímo z uživatelského rozhraní (ne na pozadí), nebude úloha optimalizace plánování stornována.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="bfbcf-106">I v případě, že se zobrazí upozornění typu "Operace byla zrušena", budete přesto potřebovat následující postup pro zrušení úlohy plánování s optimalizací plánování.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="bfbcf-107">Chcete-li zrušit aktivní plánovací úlohu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="bfbcf-108">Lze zrušit pouze aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="bfbcf-109">Přejděte na **Hlavní plánování \> Nastavení \> Plány**.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="bfbcf-110">Vyberte příslušný plán pro spuštění plánování.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="bfbcf-111">Zvolte možnost **Historie**.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-111">Select **History**.</span></span>
4. <span data-ttu-id="bfbcf-112">Vybrat plánovací úlohu ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="bfbcf-113">Vyberte možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-113">Select **Cancel**.</span></span>

<span data-ttu-id="bfbcf-114">Stav úlohy bude **Probíhá zrušení**, dokud služba optimalizace plánování nepotvrdí, že úloha byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="bfbcf-115">Stav se změní na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="bfbcf-116">Chcete-li zobrazit změny stavu, je nutné aktualizovat stránku výběrem tlačítka **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="bfbcf-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfbcf-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="bfbcf-117">Additional resources</span></span>

[<span data-ttu-id="bfbcf-118">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="bfbcf-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="bfbcf-119">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="bfbcf-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="bfbcf-120">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="bfbcf-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="bfbcf-121">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="bfbcf-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="bfbcf-122">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="bfbcf-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]