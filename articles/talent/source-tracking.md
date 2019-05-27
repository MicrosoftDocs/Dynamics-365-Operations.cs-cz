---
title: Sledování zdrojů pro profily a žádosti kandidátů
description: Toto téma obsahuje informace o sledování zdroje pro profily kandidáta a žádosti.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517552"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a><span data-ttu-id="e4db6-103">Sledování zdrojů pro profily a žádosti kandidátů</span><span class="sxs-lookup"><span data-stu-id="e4db6-103">Track sources for candidate profiles and applications</span></span> 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="e4db6-104">Funkce pojednávaná v tomto tématu je k dispozici jako součást verze Preview.</span><span class="sxs-lookup"><span data-stu-id="e4db6-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="e4db6-105">Obsah a funkce se mohou změnit.</span><span class="sxs-lookup"><span data-stu-id="e4db6-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="e4db6-106">Chcete-li použít tuto funkci, požádejte správce o její povolení pomocí **Nastavení pro správu** v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="e4db6-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="e4db6-107">Budoucí verze nabídne sestavy sledování zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e4db6-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="e4db6-108">Další informace naleznete v tématu [Přístup k funkcím Preview v aplikaci Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="e4db6-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="e4db6-109">Když kandidáti požádají o práci, Attract automaticky sleduje zdroj jejich žádostí a poskytne vám cenné informace, které vám pomohou zaměřit náborové úsilí.</span><span class="sxs-lookup"><span data-stu-id="e4db6-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="e4db6-110">Náboroví pracovníci a manažeři mohou také vybrat zdroj žádosti při ručním přidávání kandidáta k práci nebo skupině talentů.</span><span class="sxs-lookup"><span data-stu-id="e4db6-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="e4db6-111">Zdroj žádosti můžete zobrazit v podrobnostech aktivity žádosti na kartě **Aktivita**, stejně jako v historii žádosti dostupné pod možností **Profil** ve skupině talentů.</span><span class="sxs-lookup"><span data-stu-id="e4db6-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="e4db6-112">Zdroj profilu kandidáta naleznete v podrobnostech kandidáta pod kartou **Profil** v žádostech i skupinách talentů.</span><span class="sxs-lookup"><span data-stu-id="e4db6-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="e4db6-113">Šablony procesu naleznete v [doplňku komplexního náboru](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="e4db6-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="e4db6-114">Předkonfigurované zdroje</span><span class="sxs-lookup"><span data-stu-id="e4db6-114">Pre-configured sources</span></span>

<span data-ttu-id="e4db6-115">Výchozí seznam zdrojů obsahuje běžné zdroje žádostí.</span><span class="sxs-lookup"><span data-stu-id="e4db6-115">The default source list contains common application sources.</span></span> <span data-ttu-id="e4db6-116">Některé typy zdrojů, například **Pracovní vývěska** a **Sociální sítě** mají další podrobnosti zdroje.</span><span class="sxs-lookup"><span data-stu-id="e4db6-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="e4db6-117">Například **sociální sítě** zahrnují Facebook a Twitter.</span><span class="sxs-lookup"><span data-stu-id="e4db6-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="e4db6-118">Typ zdroje **Reference** vám umožní určit interního zaměstnance jako poskytovatele reference.</span><span class="sxs-lookup"><span data-stu-id="e4db6-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="e4db6-119">Výchozí seznam zdrojů obsahuje následující předem nakonfigurované zdroje:</span><span class="sxs-lookup"><span data-stu-id="e4db6-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="e4db6-120">Kariérní web Attract</span><span class="sxs-lookup"><span data-stu-id="e4db6-120">Attract career site</span></span>

-   <span data-ttu-id="e4db6-121">Agentura</span><span class="sxs-lookup"><span data-stu-id="e4db6-121">Agency</span></span>

-   <span data-ttu-id="e4db6-122">Kariérní veletrh</span><span class="sxs-lookup"><span data-stu-id="e4db6-122">Career Fair</span></span>

-   <span data-ttu-id="e4db6-123">Marketing společnosti</span><span class="sxs-lookup"><span data-stu-id="e4db6-123">Company Marketing</span></span>

-   <span data-ttu-id="e4db6-124">Konference a obchodní veletrhy</span><span class="sxs-lookup"><span data-stu-id="e4db6-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="e4db6-125">Profesní asociace</span><span class="sxs-lookup"><span data-stu-id="e4db6-125">Professional Association</span></span>

-   <span data-ttu-id="e4db6-126">Pracovní vývěska</span><span class="sxs-lookup"><span data-stu-id="e4db6-126">Job board</span></span>

    -   <span data-ttu-id="e4db6-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="e4db6-127">Indeed</span></span>

    -   <span data-ttu-id="e4db6-128">Seek</span><span class="sxs-lookup"><span data-stu-id="e4db6-128">Seek</span></span>

    -   <span data-ttu-id="e4db6-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="e4db6-129">CareerBuilder</span></span>

    -   <span data-ttu-id="e4db6-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="e4db6-130">Google Jobs</span></span>

    -   <span data-ttu-id="e4db6-131">Xing</span><span class="sxs-lookup"><span data-stu-id="e4db6-131">Xing</span></span>

    -   <span data-ttu-id="e4db6-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="e4db6-132">Glassdoor</span></span>

    -   <span data-ttu-id="e4db6-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="e4db6-133">Monster Jobs</span></span>

-   <span data-ttu-id="e4db6-134">Časopisy a publikace</span><span class="sxs-lookup"><span data-stu-id="e4db6-134">Magazines & Publications</span></span>

-   <span data-ttu-id="e4db6-135">Sociální sítě</span><span class="sxs-lookup"><span data-stu-id="e4db6-135">Social Network</span></span>

    -   <span data-ttu-id="e4db6-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="e4db6-136">Facebook</span></span>

    -   <span data-ttu-id="e4db6-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="e4db6-137">Twitter</span></span>

-   <span data-ttu-id="e4db6-138">Univerzitní nábor</span><span class="sxs-lookup"><span data-stu-id="e4db6-138">University Recruiting</span></span>

-   <span data-ttu-id="e4db6-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="e4db6-139">LinkedIn</span></span>

-   <span data-ttu-id="e4db6-140">Classifieds</span><span class="sxs-lookup"><span data-stu-id="e4db6-140">Classifieds</span></span>

-   <span data-ttu-id="e4db6-141">Reference</span><span class="sxs-lookup"><span data-stu-id="e4db6-141">Referral</span></span>

-   <span data-ttu-id="e4db6-142">Přidáno náborářem</span><span class="sxs-lookup"><span data-stu-id="e4db6-142">Added by Recruiter</span></span>

-   <span data-ttu-id="e4db6-143">Jiný</span><span class="sxs-lookup"><span data-stu-id="e4db6-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="e4db6-144">Přizpůsobení seznamu zdroje</span><span class="sxs-lookup"><span data-stu-id="e4db6-144">Customize the source list</span></span> 

<span data-ttu-id="e4db6-145">Můžete rozšířit seznam zdrojů a zahrnout další zdroje žádostí.</span><span class="sxs-lookup"><span data-stu-id="e4db6-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="e4db6-146">Chcete-li přizpůsobit tento seznam, postupujte podle pokynů v části [Rozšíření sad možností v aplikaci Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="e4db6-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="e4db6-147">Upravte entitu **TalentSource** pro zahrnutí dalších zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e4db6-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="e4db6-148">Chcete-li se vyhnout negativním dopadům na uživatelské rozhraní, neupravujte nebo neodstraňujte hodnoty výčtů **TalentCategory** (nikoli názvy) pro následující položky:</span><span class="sxs-lookup"><span data-stu-id="e4db6-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="e4db6-149">**Reference**</span><span class="sxs-lookup"><span data-stu-id="e4db6-149">**Referral**</span></span>
- <span data-ttu-id="e4db6-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="e4db6-150">**LinkedIn**</span></span>
- <span data-ttu-id="e4db6-151">**Jiný**</span><span class="sxs-lookup"><span data-stu-id="e4db6-151">**Other**</span></span>

<span data-ttu-id="e4db6-152">Místo toho můžete rozšířit výčet **TalentSource** pro přidání dalších typů zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e4db6-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
