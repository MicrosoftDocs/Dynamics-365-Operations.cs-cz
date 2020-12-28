---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (7. února 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 002dcd8253a0ab753ac9002e7027441db6d0b858
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460587"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a><span data-ttu-id="178a3-103">Co je nového nebo změněného v aplikaci Dynamics 365 Talent (7. února 2019)</span><span class="sxs-lookup"><span data-stu-id="178a3-103">What's new or changed in Dynamics 365 Talent (February 7, 2019)</span></span>

<span data-ttu-id="178a3-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="178a3-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="178a3-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="178a3-105">Changes in Attract</span></span>

### <a name="interview-scheduling-enhancements"></a><span data-ttu-id="178a3-106">Vylepšení plánování pohovoru</span><span class="sxs-lookup"><span data-stu-id="178a3-106">Interview scheduling enhancements</span></span>
<span data-ttu-id="178a3-107">Byla provedena vylepšení rozhraní pro plánování celého procesu pohovoru.</span><span class="sxs-lookup"><span data-stu-id="178a3-107">Improvements have been made to the end-to-end interview scheduling experience.</span></span> <span data-ttu-id="178a3-108">Nyní můžete vidět dostupnost kalendáře interního kandidáta a použít kalendář interního kandidáta pro doporučení plánu.</span><span class="sxs-lookup"><span data-stu-id="178a3-108">You can now see the calendar availability of an internal candidate and use the internal candidate’s calendar for schedule recommendations.</span></span> <span data-ttu-id="178a3-109">Další informace naleznete v tématu [Plánování pohovoru a zpětná vazba](interview-scheduling-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="178a3-109">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a><span data-ttu-id="178a3-110">Publikování pracovní nabídky na LinkedIn – problémy s neshodou společností byly opraveny</span><span class="sxs-lookup"><span data-stu-id="178a3-110">Job posting to LinkedIn – company mismatch issue fixed</span></span>
<span data-ttu-id="178a3-111">Byl opraven problém, kdy se nabídky práce publikované na LinkedIn z aplikace Attract zobrazovaly pod chybným názvem společnosti.</span><span class="sxs-lookup"><span data-stu-id="178a3-111">An issue has been fixed where jobs posted to LinkedIn from Attract were appearing under the wrong company name.</span></span> <span data-ttu-id="178a3-112">Další informace naleznete v tématu [Vytvoření, schválení a publikování pracovních míst v aplikaci Attract](creating-jobs-attract.md).</span><span class="sxs-lookup"><span data-stu-id="178a3-112">For more information, see [Create, approve, and post jobs in Attract](creating-jobs-attract.md).</span></span>

### <a name="career-site-url-displayed-in-admin-settings"></a><span data-ttu-id="178a3-113">Adresa URL kariérního webu zobrazená v nastavení pro správu</span><span class="sxs-lookup"><span data-stu-id="178a3-113">Career site URL displayed in Admin settings</span></span>
<span data-ttu-id="178a3-114">URL adresa domovské stránky kariérního webu se nyní zobrazuje v **Nastavení pro správu** pod položkou **Správa kariérního webu**.</span><span class="sxs-lookup"><span data-stu-id="178a3-114">The career site home page URL is now displayed in **Admin Settings** under **Career Site management**.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="178a3-115">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="178a3-115">Changes in Core HR</span></span>

<span data-ttu-id="178a3-116">**Sestavení 8.1.2134**</span><span class="sxs-lookup"><span data-stu-id="178a3-116">**Build 8.1.2134**</span></span>

### <a name="multiple-compensation-levels-supported-on-jobs"></a><span data-ttu-id="178a3-117">Více úrovní kompenzací podporováno u prací</span><span class="sxs-lookup"><span data-stu-id="178a3-117">Multiple compensation levels supported on jobs</span></span>
<span data-ttu-id="178a3-118">Tato změna umožňuje definovat více než jednu úroveň kompenzace pro práci, což umožňuje rozsahy fixní kompenzace zaměstnance, které se mohou lišit mezi plány při použití stejné práce.</span><span class="sxs-lookup"><span data-stu-id="178a3-118">This change allows for more than one compensation level to be defined on a job, enabling employee fixed compensation ranges which may differ between plans when using the same job.</span></span> 

<span data-ttu-id="178a3-119">Například:</span><span class="sxs-lookup"><span data-stu-id="178a3-119">For example:</span></span>    
<span data-ttu-id="178a3-120">*Práce* -Account manažer *Přidružené úrovně kompenzace:* B1 a B2 – Každá úroveň má definovaný rozsah hodnot.</span><span class="sxs-lookup"><span data-stu-id="178a3-120">*Job* - Account Manager *Associated compensation levels:* B1 and B2 - Each level has a defined range of values.</span></span> <span data-ttu-id="178a3-121">B1 = Min 50,000, Stř 60,000, Max 75,000 a B2 = Min 65,000, Stř 74,000, Max 85,000.</span><span class="sxs-lookup"><span data-stu-id="178a3-121">B1 = Min 50,000, Mid 60,000, Max 75,000 and B2 = Min 65,000, Mid 74,000, Max 85,000.</span></span> <span data-ttu-id="178a3-122">Při vytváření fixní kompenzace pro zaměstnance, na základě definovaných pravidel nároku, může každý fixní plán nyní poukazovat na stejné pracovní místo a na různé úrovně pracovního místa.</span><span class="sxs-lookup"><span data-stu-id="178a3-122">When creating fixed compensation for employees, based on the eligibility rules defined, each fixed plan can now point to the same job and to different levels on the job.</span></span> <span data-ttu-id="178a3-123">To umožňuje definovat plány v různých regionech/společnostech a poukazovat na stejnou práci, ale na rozdílné rozsahy, aniž by se zohledňovala duplicitní pracovní místa.</span><span class="sxs-lookup"><span data-stu-id="178a3-123">This allows for plans to be defined in different regions/companies and point to the same job but different ranges without duplicating jobs to account for these differences.</span></span>

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a><span data-ttu-id="178a3-124">Bylo přidáno pole úrovně kompenzace pro entitu fixní kompenzace zaměstnance</span><span class="sxs-lookup"><span data-stu-id="178a3-124">Compensation level field has been added to the Employee fixed compensation entity</span></span> 
<span data-ttu-id="178a3-125">Díky této aktualizaci byla entita fixní kompenzace zaměstnance aktualizována, aby zahrnovala pole **Úroveň kompenzace**.</span><span class="sxs-lookup"><span data-stu-id="178a3-125">With this update, the employee fixed compensation entity has been updated to include the **Compensation level** field.</span></span> <span data-ttu-id="178a3-126">Toto přidání usnadňuje aktualizaci plánů fixní kompenzace zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="178a3-126">This addition makes it easier to update employee fixed compensation plans.</span></span> 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a><span data-ttu-id="178a3-127">Aktualizace skupiny prací při aktualizaci a vytváření nových pozic</span><span class="sxs-lookup"><span data-stu-id="178a3-127">Update Job family when updating and creating new positions</span></span>
<span data-ttu-id="178a3-128">Při změně práce na pozici bude nyní ve výchozím nastavení **Skupina prací** na základě zvolené práce.</span><span class="sxs-lookup"><span data-stu-id="178a3-128">When changing the job on a position, **Job family** will now default based on the job selected.</span></span>

### <a name="performance-improvements-when-rendering-workspaces"></a><span data-ttu-id="178a3-129">Zlepšení výkonu při vykreslování pracovního prostoru</span><span class="sxs-lookup"><span data-stu-id="178a3-129">Performance improvements when rendering workspaces</span></span>
<span data-ttu-id="178a3-130">Karta analýzy na pracovních prostorech se nyní načte pouze pří přístupu na tyto stránky.</span><span class="sxs-lookup"><span data-stu-id="178a3-130">Analytics tabs on workspaces will now load only when accessing those pages.</span></span> <span data-ttu-id="178a3-131">Během úvodního vykreslování stránky v levém horním rohu stránky se zobrazí indikátor.</span><span class="sxs-lookup"><span data-stu-id="178a3-131">An indicator will display during the initial rendering of the page in the upper-left corner of the page.</span></span>
