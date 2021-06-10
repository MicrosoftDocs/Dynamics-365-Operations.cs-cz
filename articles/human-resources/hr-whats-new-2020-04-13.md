---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (13. dubna 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 13. dubnu 2020.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a43b55c075102056ed7c752b72a85f2c9012d46
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051034"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="446de-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (13. dubna 2020)</span><span class="sxs-lookup"><span data-stu-id="446de-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="446de-104">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="446de-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="446de-105">Změny se vztahují na sestavení číslo 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="446de-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="446de-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="446de-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="446de-107">Četnost nových vydání</span><span class="sxs-lookup"><span data-stu-id="446de-107">New production release cadence</span></span>

<span data-ttu-id="446de-108">S vydáním tohoto týdne se četnost vydání produktu Human Resources mění z týdenní aktualizace na čtrnáctidenní aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="446de-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="446de-109">Abychom zajistili sbližování s postupy bezpečného nasazení a udržovat ve službě vysoké standardy stability a spolehlivosti, proces nasazení aktualizací služeb do všech regionů je nyní tvořen dvěma týdny.</span><span class="sxs-lookup"><span data-stu-id="446de-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="446de-110">Dodatečná testování a sledovaní jsou zavedena pro ověření úspěšného nasazení v každé fázi procesu.</span><span class="sxs-lookup"><span data-stu-id="446de-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="446de-111">Další informace o četnosti vydání naleznete v tématu [Aktualizace procesu](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="446de-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="446de-112">Pole přesnosti zaokrouhlení nelze upravit po zadání typu zaokrouhlení (435616)</span><span class="sxs-lookup"><span data-stu-id="446de-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="446de-113">Tato změna má nyní k dispozici pole **Přesnost zaokrouhlení** po aktualizaci pole **Typ zaokrouhlení**.</span><span class="sxs-lookup"><span data-stu-id="446de-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="446de-114">Nelze upravit datum ukončení přihlášení, pokud plán volna neobsahuje období časového rozlišení (413628)</span><span class="sxs-lookup"><span data-stu-id="446de-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="446de-115">Nyní můžete upravit koncové datum přihlášení, aniž by došlo k chybě "Je nutné vyplnit základ data časového rozlišení".</span><span class="sxs-lookup"><span data-stu-id="446de-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="446de-116">Entita zaměstnání se nesynchronizuje do Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="446de-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="446de-117">Tato změna opravuje problém, kdy se data zaměstnání nesynchronizují do Dataverse po přidání finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="446de-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="446de-118">Odebrat pro entitu časového intervalu pracovního kalendáře více nadřazenosti (431775)</span><span class="sxs-lookup"><span data-stu-id="446de-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="446de-119">Tato změna odstraňuje více nadřazenosti pro entitu **Časový interval pracovního kalenáře**.</span><span class="sxs-lookup"><span data-stu-id="446de-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="446de-120">Filtr s funkcí CAST nefunguje na volání OData entity Přiřazení pozice pracovníka (431699)</span><span class="sxs-lookup"><span data-stu-id="446de-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="446de-121">Tato aktualizace obsahuje změnu pro povolení filtru s funkcí CAST v rámci OData pro entitu **Přiřazení pozice pracovníka**.</span><span class="sxs-lookup"><span data-stu-id="446de-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="446de-122">Náhled</span><span class="sxs-lookup"><span data-stu-id="446de-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="446de-123">Pozastavit pracovní volno</span><span class="sxs-lookup"><span data-stu-id="446de-123">Leave suspension</span></span>

<span data-ttu-id="446de-124">Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="446de-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="446de-125">Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="446de-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="446de-126">Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="446de-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="446de-127">Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="446de-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="446de-128">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="446de-128">Carry forward rules</span></span>

<span data-ttu-id="446de-129">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="446de-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="446de-130">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="446de-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="446de-131">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="446de-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="446de-132">Známé problémy</span><span class="sxs-lookup"><span data-stu-id="446de-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="446de-133">Entita Podrobnosti o zaměstnání</span><span class="sxs-lookup"><span data-stu-id="446de-133">Employment Details entity</span></span>

<span data-ttu-id="446de-134">Entita **podrobností o zaměstnání** byla aktualizována pomocí následujících polí:</span><span class="sxs-lookup"><span data-stu-id="446de-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="446de-135">**PayFrequency**</span><span class="sxs-lookup"><span data-stu-id="446de-135">**PayFrequency**</span></span>
- <span data-ttu-id="446de-136">**ID Kategorie zaměstnání**</span><span class="sxs-lookup"><span data-stu-id="446de-136">**Employment Category ID**</span></span>
- <span data-ttu-id="446de-137">**Typ zaměstnání**</span><span class="sxs-lookup"><span data-stu-id="446de-137">**Employment Type**</span></span>
- <span data-ttu-id="446de-138">**EmploymentType ID**</span><span class="sxs-lookup"><span data-stu-id="446de-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="446de-139">**Stav zaměstnaneckých výhod zaměstnání**</span><span class="sxs-lookup"><span data-stu-id="446de-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="446de-140">Data nastavení pro tato pole spoléhají na správu výhod, která je povolena v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="446de-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="446de-141">Tato pole v entitě **podrobností o zaměstnání** se nezaplňují ani neaktualizují, protože během importu způsobí chyby.</span><span class="sxs-lookup"><span data-stu-id="446de-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="446de-142">V některých prostředích nefunguje náhled služby SharePoint</span><span class="sxs-lookup"><span data-stu-id="446de-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="446de-143">Pokud nefunguje náhled dokumentů uložených ve službě SharePoint, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="446de-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="446de-144">Ověřte, zda má uživatelský účet Správce přidružen e-mail k záznamu uživatele.</span><span class="sxs-lookup"><span data-stu-id="446de-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="446de-145">Tyto informace můžete zobrazit na stránce **Uživatel**.</span><span class="sxs-lookup"><span data-stu-id="446de-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="446de-146">Není-li e-mail nastaven, je nutné přidat e-mail a poskytovatele pomocí doplňku OData Excel.</span><span class="sxs-lookup"><span data-stu-id="446de-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="446de-147">Ve výchozím nastavení není v návrhu aplikace Excel e-mailová adresa k dispozici.</span><span class="sxs-lookup"><span data-stu-id="446de-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="446de-148">Je nutné upravit návrh aplikace Excel, přidat všechna pole, použít a aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="446de-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="446de-149">Po dokončení těchto kroků můžete aktualizovat účet správce.</span><span class="sxs-lookup"><span data-stu-id="446de-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="446de-150">Poté, co má účet správce přidružen e-mailový účet, přihlaste se k modulu Human Resources s pověřeními správce.</span><span class="sxs-lookup"><span data-stu-id="446de-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="446de-151">Ve službě SharePoint přistupte k příloze a zobrazte náhled dokumentu.</span><span class="sxs-lookup"><span data-stu-id="446de-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="446de-152">Přihlaste se s jiným uživatelským účtem, který má přístup k přílohám, a ověřte, že náhled funguje očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="446de-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="446de-153">Viz také</span><span class="sxs-lookup"><span data-stu-id="446de-153">See also</span></span>

[<span data-ttu-id="446de-154">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="446de-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="446de-155">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="446de-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="446de-156">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="446de-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="446de-157">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="446de-157">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]