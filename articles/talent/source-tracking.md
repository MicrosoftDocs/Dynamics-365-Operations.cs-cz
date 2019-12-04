---
title: Sledování zdrojů kandidátů v aplikaci Attract
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
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832637"
---
# <a name="track-candidate-sources-in-attract"></a><span data-ttu-id="7c15a-103">Sledování zdrojů kandidátů v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="7c15a-103">Track candidate sources in Attract</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="7c15a-104">Funkce pojednávaná v tomto tématu je k dispozici jako součást verze Preview.</span><span class="sxs-lookup"><span data-stu-id="7c15a-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="7c15a-105">Obsah a funkce se mohou změnit.</span><span class="sxs-lookup"><span data-stu-id="7c15a-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="7c15a-106">Chcete-li použít tuto funkci, požádejte správce o její povolení pomocí **Nastavení pro správu** v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="7c15a-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="7c15a-107">Budoucí verze nabídne sestavy sledování zdrojů.</span><span class="sxs-lookup"><span data-stu-id="7c15a-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="7c15a-108">Další informace naleznete v tématu [Přístup k funkcím Preview v aplikaci Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="7c15a-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="7c15a-109">Když kandidáti požádají o práci, Attract automaticky sleduje zdroj jejich žádostí a poskytne vám cenné informace, které vám pomohou zaměřit náborové úsilí.</span><span class="sxs-lookup"><span data-stu-id="7c15a-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="7c15a-110">Náboroví pracovníci a manažeři mohou také vybrat zdroj žádosti při ručním přidávání kandidáta k práci nebo skupině talentů.</span><span class="sxs-lookup"><span data-stu-id="7c15a-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="7c15a-111">Zdroj žádosti můžete zobrazit v podrobnostech aktivity žádosti na kartě **Aktivita**, stejně jako v historii žádosti dostupné pod možností **Profil** ve skupině talentů.</span><span class="sxs-lookup"><span data-stu-id="7c15a-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="7c15a-112">Zdroj profilu kandidáta naleznete v podrobnostech kandidáta pod kartou **Profil** v žádostech i skupinách talentů.</span><span class="sxs-lookup"><span data-stu-id="7c15a-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="7c15a-113">Šablony procesu naleznete v [doplňku komplexního náboru](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="7c15a-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="7c15a-114">Předkonfigurované zdroje</span><span class="sxs-lookup"><span data-stu-id="7c15a-114">Pre-configured sources</span></span>

<span data-ttu-id="7c15a-115">Výchozí seznam zdrojů obsahuje běžné zdroje žádostí.</span><span class="sxs-lookup"><span data-stu-id="7c15a-115">The default source list contains common application sources.</span></span> <span data-ttu-id="7c15a-116">Některé typy zdrojů, například **Pracovní vývěska** a **Sociální sítě** mají další podrobnosti zdroje.</span><span class="sxs-lookup"><span data-stu-id="7c15a-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="7c15a-117">Například **sociální sítě** zahrnují Facebook a Twitter.</span><span class="sxs-lookup"><span data-stu-id="7c15a-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="7c15a-118">Typ zdroje **Reference** vám umožní určit interního zaměstnance jako poskytovatele reference.</span><span class="sxs-lookup"><span data-stu-id="7c15a-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="7c15a-119">Výchozí seznam zdrojů obsahuje následující předem nakonfigurované zdroje:</span><span class="sxs-lookup"><span data-stu-id="7c15a-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="7c15a-120">Kariérní web Attract</span><span class="sxs-lookup"><span data-stu-id="7c15a-120">Attract career site</span></span>

-   <span data-ttu-id="7c15a-121">Agentura</span><span class="sxs-lookup"><span data-stu-id="7c15a-121">Agency</span></span>

-   <span data-ttu-id="7c15a-122">Kariérní veletrh</span><span class="sxs-lookup"><span data-stu-id="7c15a-122">Career Fair</span></span>

-   <span data-ttu-id="7c15a-123">Marketing společnosti</span><span class="sxs-lookup"><span data-stu-id="7c15a-123">Company Marketing</span></span>

-   <span data-ttu-id="7c15a-124">Konference a obchodní veletrhy</span><span class="sxs-lookup"><span data-stu-id="7c15a-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="7c15a-125">Profesní asociace</span><span class="sxs-lookup"><span data-stu-id="7c15a-125">Professional Association</span></span>

-   <span data-ttu-id="7c15a-126">Pracovní vývěska</span><span class="sxs-lookup"><span data-stu-id="7c15a-126">Job board</span></span>

    -   <span data-ttu-id="7c15a-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="7c15a-127">Indeed</span></span>

    -   <span data-ttu-id="7c15a-128">Seek</span><span class="sxs-lookup"><span data-stu-id="7c15a-128">Seek</span></span>

    -   <span data-ttu-id="7c15a-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="7c15a-129">CareerBuilder</span></span>

    -   <span data-ttu-id="7c15a-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="7c15a-130">Google Jobs</span></span>

    -   <span data-ttu-id="7c15a-131">Xing</span><span class="sxs-lookup"><span data-stu-id="7c15a-131">Xing</span></span>

    -   <span data-ttu-id="7c15a-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="7c15a-132">Glassdoor</span></span>

    -   <span data-ttu-id="7c15a-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="7c15a-133">Monster Jobs</span></span>

-   <span data-ttu-id="7c15a-134">Časopisy a publikace</span><span class="sxs-lookup"><span data-stu-id="7c15a-134">Magazines & Publications</span></span>

-   <span data-ttu-id="7c15a-135">Sociální sítě</span><span class="sxs-lookup"><span data-stu-id="7c15a-135">Social Network</span></span>

    -   <span data-ttu-id="7c15a-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="7c15a-136">Facebook</span></span>

    -   <span data-ttu-id="7c15a-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="7c15a-137">Twitter</span></span>

-   <span data-ttu-id="7c15a-138">Univerzitní nábor</span><span class="sxs-lookup"><span data-stu-id="7c15a-138">University Recruiting</span></span>

-   <span data-ttu-id="7c15a-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7c15a-139">LinkedIn</span></span>

-   <span data-ttu-id="7c15a-140">Classifieds</span><span class="sxs-lookup"><span data-stu-id="7c15a-140">Classifieds</span></span>

-   <span data-ttu-id="7c15a-141">Reference</span><span class="sxs-lookup"><span data-stu-id="7c15a-141">Referral</span></span>

-   <span data-ttu-id="7c15a-142">Přidáno náborářem</span><span class="sxs-lookup"><span data-stu-id="7c15a-142">Added by Recruiter</span></span>

-   <span data-ttu-id="7c15a-143">Jiný</span><span class="sxs-lookup"><span data-stu-id="7c15a-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="7c15a-144">Přizpůsobení seznamu zdroje</span><span class="sxs-lookup"><span data-stu-id="7c15a-144">Customize the source list</span></span> 

<span data-ttu-id="7c15a-145">Můžete rozšířit seznam zdrojů a zahrnout další zdroje žádostí.</span><span class="sxs-lookup"><span data-stu-id="7c15a-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="7c15a-146">Chcete-li přizpůsobit tento seznam, postupujte podle pokynů v části [Rozšíření sad možností v aplikaci Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="7c15a-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="7c15a-147">Upravte entitu **TalentSource** pro zahrnutí dalších zdrojů.</span><span class="sxs-lookup"><span data-stu-id="7c15a-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="7c15a-148">Chcete-li se vyhnout negativním dopadům na uživatelské rozhraní, neupravujte nebo neodstraňujte hodnoty výčtů **TalentCategory** (nikoli názvy) pro následující položky:</span><span class="sxs-lookup"><span data-stu-id="7c15a-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="7c15a-149">**Reference**</span><span class="sxs-lookup"><span data-stu-id="7c15a-149">**Referral**</span></span>
- <span data-ttu-id="7c15a-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="7c15a-150">**LinkedIn**</span></span>
- <span data-ttu-id="7c15a-151">**Jiný**</span><span class="sxs-lookup"><span data-stu-id="7c15a-151">**Other**</span></span>

<span data-ttu-id="7c15a-152">Místo toho můžete rozšířit výčet **TalentSource** pro přidání dalších typů zdrojů.</span><span class="sxs-lookup"><span data-stu-id="7c15a-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
