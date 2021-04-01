---
title: Zrušení plánovací úlohy
description: Toto téma vysvětluje způsob zrušení aktivní plánovací úlohy, která používá funkci optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5aadf7fb94bb2d836892064837f9cb1c5790d657
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238007"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="39f4d-103">Zrušení plánovací úlohy</span><span class="sxs-lookup"><span data-stu-id="39f4d-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39f4d-104">V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete zrušit aktivní plánovací úlohy, která používá funkci optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="39f4d-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="39f4d-105">Pokud v dialogovém okně vyberete možnost **Zrušit**, když je úloha optimalizace plánování spuštěna přímo z uživatelského rozhraní (ne na pozadí), nebude úloha optimalizace plánování stornována.</span><span class="sxs-lookup"><span data-stu-id="39f4d-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="39f4d-106">I v případě, že se zobrazí upozornění typu "Operace byla zrušena", budete přesto potřebovat následující postup pro zrušení úlohy plánování s optimalizací plánování.</span><span class="sxs-lookup"><span data-stu-id="39f4d-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="39f4d-107">Chcete-li zrušit aktivní plánovací úlohu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="39f4d-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="39f4d-108">Lze zrušit pouze aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="39f4d-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="39f4d-109">Přejděte na **Hlavní plánování \> Nastavení \> Plány**.</span><span class="sxs-lookup"><span data-stu-id="39f4d-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="39f4d-110">Vyberte příslušný plán pro spuštění plánování.</span><span class="sxs-lookup"><span data-stu-id="39f4d-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="39f4d-111">Zvolte možnost **Historie**.</span><span class="sxs-lookup"><span data-stu-id="39f4d-111">Select **History**.</span></span>
4. <span data-ttu-id="39f4d-112">Vybrat plánovací úlohu ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="39f4d-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="39f4d-113">Vyberte možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="39f4d-113">Select **Cancel**.</span></span>

<span data-ttu-id="39f4d-114">Stav úlohy bude **Probíhá zrušení**, dokud služba optimalizace plánování nepotvrdí, že úloha byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="39f4d-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="39f4d-115">Stav se změní na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="39f4d-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="39f4d-116">Chcete-li zobrazit změny stavu, je nutné aktualizovat stránku výběrem tlačítka **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="39f4d-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39f4d-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="39f4d-117">Additional resources</span></span>

[<span data-ttu-id="39f4d-118">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="39f4d-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="39f4d-119">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="39f4d-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="39f4d-120">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="39f4d-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="39f4d-121">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="39f4d-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="39f4d-122">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="39f4d-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]