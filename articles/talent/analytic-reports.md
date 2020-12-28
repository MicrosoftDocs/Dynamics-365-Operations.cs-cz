---
title: Použití analytických sestav v aplikaci Attract
description: V tomto tématu je popsána analytická sestava pro přehled procesu náboru v aplikaci Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460597"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="20268-103">Použití analytických sestav v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="20268-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20268-104">Analytické sestavy v aplikaci Microsoft Dynamics 365 Talent: Attract poskytují vestavěné řešení (OOTB) pro přehledy náborových procesů.</span><span class="sxs-lookup"><span data-stu-id="20268-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="20268-105">Mezi dostupné funkce patří:</span><span class="sxs-lookup"><span data-stu-id="20268-105">Availabe features include:</span></span>

- <span data-ttu-id="20268-106">**Analytika práce** – Klikněte na kartu **Analytika** v rámci práce pro metriky na uchazečích o práci.</span><span class="sxs-lookup"><span data-stu-id="20268-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="20268-107">**Centrum analýz:** Klikněte na **Analytika** na levém navigačním panelu pro agregované metriky napříč pracemi.</span><span class="sxs-lookup"><span data-stu-id="20268-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="20268-108">**Zabezpečení specifické pro uživatele** – Přístup k sestavám je ovládán [rolí](security-attract.md) aplikace Attract a rolí účastníka na práci.</span><span class="sxs-lookup"><span data-stu-id="20268-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="20268-109">**Křížové filtrování:** Klikněte na vizuální prvky v rámci sestavy a zobrazte další metriky filtrované podle zvoleného data.</span><span class="sxs-lookup"><span data-stu-id="20268-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="20268-110">Tato funkce je aktuálně v [náhledu](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="20268-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="20268-111">Chcete-li to vyzkoušet, musíte mít [**doplněk komplexního náboru**](attract-comprehensive-hiring.md)pronájem.</span><span class="sxs-lookup"><span data-stu-id="20268-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="20268-112">Všechny sestavy veřejné verze Preview jsou zobrazeny v angličtině.</span><span class="sxs-lookup"><span data-stu-id="20268-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="20268-113">Sestavy se obnovují každé 3 hodiny.</span><span class="sxs-lookup"><span data-stu-id="20268-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="20268-114">Čas poslední aktualizace (v místním časovém pásmu) je umístěn v horní části sestavy.</span><span class="sxs-lookup"><span data-stu-id="20268-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="20268-115">Časy aktualizace jsou přibližné a liší se v závislosti na objemu dat a vytížení zdrojů ve vaší oblasti.</span><span class="sxs-lookup"><span data-stu-id="20268-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="20268-116">Analytika práce</span><span class="sxs-lookup"><span data-stu-id="20268-116">Job Analytics</span></span>

<span data-ttu-id="20268-117">Sestavy analytiky práce jsou snímkem procesu náboru pro práci.</span><span class="sxs-lookup"><span data-stu-id="20268-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="20268-118">Mezi klíčové metriky patří:</span><span class="sxs-lookup"><span data-stu-id="20268-118">Key metrics include:</span></span>

- <span data-ttu-id="20268-119">Aktivní uchazeči podle fáze</span><span class="sxs-lookup"><span data-stu-id="20268-119">Active applicants by stage</span></span>
- <span data-ttu-id="20268-120">Zdroj uchazečů</span><span class="sxs-lookup"><span data-stu-id="20268-120">Applicant source</span></span>
- <span data-ttu-id="20268-121">Typ uchazeče (interní nebo externí)</span><span class="sxs-lookup"><span data-stu-id="20268-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="20268-122">Centrum analytiky</span><span class="sxs-lookup"><span data-stu-id="20268-122">Analytics Hub</span></span>

<span data-ttu-id="20268-123">Sestavy centra analytiky agregují data napříč pracemi za účelem odhalení trendů v náborovém procesu.</span><span class="sxs-lookup"><span data-stu-id="20268-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="20268-124">Attract zahrnuje dvě OOTB sestavy: Souhrn profilace a trychtýřovou analýzu.</span><span class="sxs-lookup"><span data-stu-id="20268-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="20268-125">Souhrn profilace</span><span class="sxs-lookup"><span data-stu-id="20268-125">Pipeline Summary</span></span>

<span data-ttu-id="20268-126">Sestava souhrnu profilace agreguje data pro otevřené práce.</span><span class="sxs-lookup"><span data-stu-id="20268-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="20268-127">Mezi klíčové metriky patří:</span><span class="sxs-lookup"><span data-stu-id="20268-127">Key metrics include:</span></span>

- <span data-ttu-id="20268-128">Uchazeči napříč všemi pracemi podle fáze</span><span class="sxs-lookup"><span data-stu-id="20268-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="20268-129">Zdroj uchazečů</span><span class="sxs-lookup"><span data-stu-id="20268-129">Applicant source</span></span>
- <span data-ttu-id="20268-130">Otevřené pracovní pozice podle úrovně služebního věku</span><span class="sxs-lookup"><span data-stu-id="20268-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="20268-131">Trychtýřová analýza</span><span class="sxs-lookup"><span data-stu-id="20268-131">Funnel Analysis</span></span>

<span data-ttu-id="20268-132">Sestava trychtýřové analýzy agreguje data pro úlohy, které byly uzavřeny jako vyplněné.</span><span class="sxs-lookup"><span data-stu-id="20268-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="20268-133">Mezi klíčové metriky patří:</span><span class="sxs-lookup"><span data-stu-id="20268-133">Key metrics include:</span></span>

- <span data-ttu-id="20268-134">Čas do náboru</span><span class="sxs-lookup"><span data-stu-id="20268-134">Time to hire</span></span>
- <span data-ttu-id="20268-135">Metriky převodu (při najetí myší)</span><span class="sxs-lookup"><span data-stu-id="20268-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="20268-136">Míra přijetí nabídky</span><span class="sxs-lookup"><span data-stu-id="20268-136">Offer acceptance rate</span></span>

<span data-ttu-id="20268-137">Poznámka: Chcete-li získat nejpřesnější vykazování doby do náboru, doporučujeme používat [správu nabídek](offer-setup.md), která je k dispozici jako součást doplňku komplexního náboru.</span><span class="sxs-lookup"><span data-stu-id="20268-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="20268-138">Zkuste přejít myší nad vizuální prvky pro získání dalších informací.</span><span class="sxs-lookup"><span data-stu-id="20268-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="20268-139">Například při přechodu myší na vizuální prvky **Aktivní uchazeči** se zobrazí průměrné dny ve fázi.</span><span class="sxs-lookup"><span data-stu-id="20268-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="20268-140">Analýza těchto informací může poskytovat přehledy důležité pro snížení doby do náboru a umožnit náborovým pracovníkům zaměřit se na způsoby snížení času stráveného v jednotlivých fázích.</span><span class="sxs-lookup"><span data-stu-id="20268-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="20268-141">Zabezpečení specifické pro uživatele</span><span class="sxs-lookup"><span data-stu-id="20268-141">User-specific security</span></span>

<span data-ttu-id="20268-142">Sestavy Attract jsou přístupné pro [role](security-attract.md) správce, čtení všech, náborových pracovníků a náborových manažerů.</span><span class="sxs-lookup"><span data-stu-id="20268-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="20268-143">Nepřiřazení uživatelé nemají přístup k žádné ze stránek analytických sestav (Analytika práce a Centrum analytiky).</span><span class="sxs-lookup"><span data-stu-id="20268-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="20268-144">Sestavy Analytika práce zobrazují data pro vybranou práci.</span><span class="sxs-lookup"><span data-stu-id="20268-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="20268-145">Sestavy centra analýz agregují data napříč všemi pracemi, které může zobrazit uživatel.</span><span class="sxs-lookup"><span data-stu-id="20268-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="20268-146">Uživatelé, kteří mohou zobrazit jak Moje úlohy, tak Všechny úlohy, na stránce úloh, mají k dispozici stejná zobrazení v centru analýz.</span><span class="sxs-lookup"><span data-stu-id="20268-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="20268-147">Křížové filtrování</span><span class="sxs-lookup"><span data-stu-id="20268-147">Cross-filter</span></span>

<span data-ttu-id="20268-148">Jednou z skvělých funkcí aplikace Power BI je způsob, jakým jsou vzájemně propojeny všechny vizuální prvky na stránce sestavy.</span><span class="sxs-lookup"><span data-stu-id="20268-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="20268-149">Pokud vyberete datový bod na jednom z vizuálních prvků, změní se na základě tohoto výběru všechny ostatní vizuální prvky na stránce, které obsahují tato data.</span><span class="sxs-lookup"><span data-stu-id="20268-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="20268-150">Další informace a příklady naleznete v tématu [Jak se vizuální prvky křížově filtrují navzájem v sestavě Power BI](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="20268-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="20268-151">Export do aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="20268-151">Export to Excel</span></span>

<span data-ttu-id="20268-152">Chcete-li zobrazit data sestav v aplikaci Excel, můžete kliknout na nabídku možností (tři tečky) na vizuálním prvku a zvolit **Exportovat podkladová data**.</span><span class="sxs-lookup"><span data-stu-id="20268-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="20268-153">Exportovaná data budou exportována jako filtrovaná s ohledem na uživatelská oprávnění v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="20268-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="20268-154">Další informace naleznete v tématu [Export dat z vizualizací](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="20268-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
