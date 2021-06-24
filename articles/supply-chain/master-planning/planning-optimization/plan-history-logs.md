---
title: Zobrazení historie plánu a protokolů plánování
description: Toto téma vysvětluje, jak zobrazit historii úloh plánování, které jsou spouštěny funkcí Optimalizace plánování.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187240"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="ca75d-103">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="ca75d-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca75d-104">Toto téma vysvětluje, jak zobrazit historii úloh plánování, které jsou spouštěny funkcí Optimalizace plánování v aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ca75d-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ca75d-105">Chcete-li zobrazit historii plánu, otevřete plán tak, že přejdete na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány** a vyberete **Historie**.</span><span class="sxs-lookup"><span data-stu-id="ca75d-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="ca75d-106">V rámci historie jsou uvedeny všechny úlohy pro vybraný plán.</span><span class="sxs-lookup"><span data-stu-id="ca75d-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="ca75d-107">Seznam obsahuje dokončené a aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="ca75d-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="ca75d-108">Historie úloh pro hlavní plánovací běhy Optimalizace plánování udržuje maximálně 60 záznamů na hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="ca75d-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="ca75d-109">Kdykoli spustíte nový výpočet hlavního plánování, bude odstraněn nejstarší záznam historie tohoto plánu.</span><span class="sxs-lookup"><span data-stu-id="ca75d-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="ca75d-110">Kromě toho, že se zobrazuje počáteční čas a stav úloh, můžete zobrazit protokol pro určitou práci.</span><span class="sxs-lookup"><span data-stu-id="ca75d-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="ca75d-111">Protokol obsahuje další informace a upozornění.</span><span class="sxs-lookup"><span data-stu-id="ca75d-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="ca75d-112">Některé úlohy nemají protokol.</span><span class="sxs-lookup"><span data-stu-id="ca75d-112">Not all jobs have a log.</span></span> <span data-ttu-id="ca75d-113">Chcete-li zobrazit protokol pro úlohu, vyberte možnost **protokol**.</span><span class="sxs-lookup"><span data-stu-id="ca75d-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="ca75d-114">Položky protokolu se ukládají po dobu pouze 30 dní po datu dokončení úlohy, poté se automaticky smažou.</span><span class="sxs-lookup"><span data-stu-id="ca75d-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="ca75d-115">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="ca75d-115">Related resources</span></span>

- [<span data-ttu-id="ca75d-116">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="ca75d-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="ca75d-117">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="ca75d-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="ca75d-118">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="ca75d-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="ca75d-119">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="ca75d-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="ca75d-120">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="ca75d-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]