---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (5. března 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 561b6fad0facad86e9a7bc8f36218ab98fcec73c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773258"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a><span data-ttu-id="44dcf-103">Co je nového nebo změněného v aplikaci Dynamics 365 Talent (5. března 2019)</span><span class="sxs-lookup"><span data-stu-id="44dcf-103">What's new or changed in Dynamics 365 Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="44dcf-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="44dcf-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="44dcf-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="44dcf-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="44dcf-106">Rozšíření sad možností v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="44dcf-106">Extending option sets in Attract</span></span>

<span data-ttu-id="44dcf-107">V aplikaci Attract existuje několik polí, která jsou sadami možností v rámci služby Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="44dcf-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="44dcf-108">Byly zavedeny nové možnosti pro rozšíření sad možností, počínaje polem důvodu **Zamítnutí**, polem **Typ zaměstnání** a polem **Typ služebního věku**.</span><span class="sxs-lookup"><span data-stu-id="44dcf-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44dcf-109">Funkce publikování pracovní nabídky na LinkedIn vyžaduje použití polí **Typ zaměstnání** a **Typ služebního věku** na stránce **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="44dcf-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="44dcf-110">Výchozí hodnoty v těchto polích jsou podporovány službou LinkedIn a jsou zobrazeny při publikování nabídky práce.</span><span class="sxs-lookup"><span data-stu-id="44dcf-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="44dcf-111">Pokud publikujete nabídku práce na LinkedIn a upravujete existující hodnoty sady možností pro tato pole, práce bude nadále publikována, ale LinkedIn nezobrazí vlastní hodnoty **Typ zaměstnání** a **Typ služebního věku**.</span><span class="sxs-lookup"><span data-stu-id="44dcf-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="44dcf-112">Změny v aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="44dcf-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="44dcf-113">Soukromá verze Preview pro týmy aplikace Onboard</span><span class="sxs-lookup"><span data-stu-id="44dcf-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="44dcf-114">Nyní můžete snadno sdílet a spolupracovat na šablonách napříč celou organizací.</span><span class="sxs-lookup"><span data-stu-id="44dcf-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="44dcf-115">Další informace naleznete v tématu [Sdílení doporučených postupů napříč vaší organizací pomocí zaškolovacích týmů](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="44dcf-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="44dcf-116">Soukromá verze Preview pro zástupné texty zmocněnce</span><span class="sxs-lookup"><span data-stu-id="44dcf-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="44dcf-117">Šablony můžete obohatit přiřazením aktivit rolím namísto jednotlivců.</span><span class="sxs-lookup"><span data-stu-id="44dcf-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="44dcf-118">Role jsou pak přiřazeny jednotlivcům v době vytvoření průvodce.</span><span class="sxs-lookup"><span data-stu-id="44dcf-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="44dcf-119">Další informace naleznete v tématu [Zefektivnění správy průvodců přiřazením aktivit rolím](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="44dcf-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="44dcf-120">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="44dcf-120">Changes in Core HR</span></span>
<span data-ttu-id="44dcf-121">**Sestavení 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="44dcf-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="44dcf-122">Konfigurace workflow pro automatické schvalování nebo následování workflow, když manažer lidských zdrojů nebo úsekový manažer odešle nebo aktualizuje žádosti o volno</span><span class="sxs-lookup"><span data-stu-id="44dcf-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="44dcf-123">Byly přidány nové podmínky workflow, aby mohly být žádosti o volno automaticky schváleny, pokud je předloží manažer zaměstnance nebo oddělení lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="44dcf-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="44dcf-124">Jedním ze způsobů, jak dosáhnout tohoto automatického schválení na workflow, je povolení automatické akce na schválení workflow.</span><span class="sxs-lookup"><span data-stu-id="44dcf-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="44dcf-125">Podmínky, které byly přidány, zahrnují:</span><span class="sxs-lookup"><span data-stu-id="44dcf-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="44dcf-126">Odesláno kým – Použitá se k vyhodnocení ID systémového uživatele, který odeslal požadavek do workflow.</span><span class="sxs-lookup"><span data-stu-id="44dcf-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="44dcf-127">Odesláno jménem - Používá se k vyhodnocení toho, zda byl požadavek odeslán jménem pracovníka přiřazeného k požadavku.</span><span class="sxs-lookup"><span data-stu-id="44dcf-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="44dcf-128">Odesláno oddělením lidských zdrojů - Používá se k vyhodnocení, zda je systémový uživatel, který odeslal požadavek do workflow, v roli lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="44dcf-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="44dcf-129">Odesláno nadřízeným - Používá se k vyhodnocení, zda je uživatel, který odeslal žádost o volno do workflow, hierarchicky přímý nadřízený pracovníka přidruženého k požadavku.</span><span class="sxs-lookup"><span data-stu-id="44dcf-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="44dcf-130">Povolení fixní kompenzace zaměstnance pro budoucí přiřazení pozice</span><span class="sxs-lookup"><span data-stu-id="44dcf-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="44dcf-131">Je obvyklé, že zaměstnanec je přijat do organizace s budoucím počátečním datem.</span><span class="sxs-lookup"><span data-stu-id="44dcf-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="44dcf-132">Tato změna umožňuje definování fixní kompenzace pro zaměstnance s budoucími přiřazeními pozice.</span><span class="sxs-lookup"><span data-stu-id="44dcf-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="44dcf-133">Při úpravě pozice jsou pole mzdy pozice prázdná</span><span class="sxs-lookup"><span data-stu-id="44dcf-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="44dcf-134">Při této změně se při požadavku na změny stávajících pozic pole mzdy nastaví na ve výchozím nastavení na aktuální hodnoty.</span><span class="sxs-lookup"><span data-stu-id="44dcf-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="44dcf-135">Ostatní různé opravy chyb</span><span class="sxs-lookup"><span data-stu-id="44dcf-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="44dcf-136">V této verzi existují jiné menší opravy chyb.</span><span class="sxs-lookup"><span data-stu-id="44dcf-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="44dcf-137">Upgrade na Common Data Service</span><span class="sxs-lookup"><span data-stu-id="44dcf-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="44dcf-138">Konečné termíny pro upgrade na Common Data Service se rychle blíží.</span><span class="sxs-lookup"><span data-stu-id="44dcf-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="44dcf-139">Přihlaste se do centra pro správu Power Apps k určení, zda je třeba provést upgrade databáze.</span><span class="sxs-lookup"><span data-stu-id="44dcf-139">Sign in to the Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="44dcf-140">Další informace o konečných termínech a nutných krocích k upgradu naleznete v tématu [Upgrade na Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="44dcf-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="44dcf-141">Již brzy</span><span class="sxs-lookup"><span data-stu-id="44dcf-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="44dcf-142">Rozšířené zabezpečení kompenzace (fixní a variabilní)</span><span class="sxs-lookup"><span data-stu-id="44dcf-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="44dcf-143">V mnoha organizacích mohou manažeři kompenzací a zaměstnaneckých výhod získat přístup pouze k určitým záznamům o kompenzacích, jako jsou záznamy pro vedoucí pracovníky nebo regionální zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="44dcf-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="44dcf-144">Díky této změně můžete spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci.</span><span class="sxs-lookup"><span data-stu-id="44dcf-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="44dcf-145">Fixním a variabilním plánům lze přiřadit role zabezpečení, které určí přístup k plánům a údajům zaměstnance souvisejících s plány, jako jsou například záznamy o mzdě nebo bonusech.</span><span class="sxs-lookup"><span data-stu-id="44dcf-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="44dcf-146">Kompenzace pro tyto zaměstnance budou moci zpracovávat pouze role s daným přístupem.</span><span class="sxs-lookup"><span data-stu-id="44dcf-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24-for-finance-and-operations"></a><span data-ttu-id="44dcf-147">Ajtzakuzace Platform Update 24 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="44dcf-147">Platform update 24 for Finance and Operations</span></span>
<span data-ttu-id="44dcf-148">Další podrobnosti o aktualizaci Platform Update 24 for Finance and Operations naleznete v tématu [Co je nového a co se změnilo v aplikaci Finance and Operations, Platform Update 24 (březen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="44dcf-148">For additional details about Platform update 24 for Finance and Operations, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
