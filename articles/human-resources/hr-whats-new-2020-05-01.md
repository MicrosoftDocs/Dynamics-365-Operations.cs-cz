---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (1. května 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a0cfd1c1b0dcc9defaad7e4cce22ebe1e91fae
ms.sourcegitcommit: cc5dc0bd90277f1ba684dd310da3274886ce573c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2020
ms.locfileid: "3320912"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="d4292-103">Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (1. května 2020)</span><span class="sxs-lookup"><span data-stu-id="d4292-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

<span data-ttu-id="d4292-104">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4292-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d4292-105">Změny se vztahují na sestavení číslo 8.1.3196.</span><span class="sxs-lookup"><span data-stu-id="d4292-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="d4292-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="d4292-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="d4292-107">Nové entity správy výkonu dostupné v architektuře pro správu dat (DMF)</span><span class="sxs-lookup"><span data-stu-id="d4292-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="d4292-108">K dispozici jsou následující entity.</span><span class="sxs-lookup"><span data-stu-id="d4292-108">The following entities are now available.</span></span> <span data-ttu-id="d4292-109">Pokud tyto entity nejsou uvedeny v seznamu entity, použijte možnost **aktualizovat entity** v **Parametrech rozhraní > Nastavení entit > Aktualizovat seznam entit**.</span><span class="sxs-lookup"><span data-stu-id="d4292-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="d4292-110">**Způsobilost k diskusi**</span><span class="sxs-lookup"><span data-stu-id="d4292-110">**Discussion Competency**</span></span>
- <span data-ttu-id="d4292-111">**Cíle diskuse**</span><span class="sxs-lookup"><span data-stu-id="d4292-111">**Discussion Goals**</span></span>
- <span data-ttu-id="d4292-112">**Měření diskuse**</span><span class="sxs-lookup"><span data-stu-id="d4292-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="d4292-113">**Téma diskuse**</span><span class="sxs-lookup"><span data-stu-id="d4292-113">**Discussion Topic**</span></span>
- <span data-ttu-id="d4292-114">**Deník výkonnosti**</span><span class="sxs-lookup"><span data-stu-id="d4292-114">**Performance Journal**</span></span>
- <span data-ttu-id="d4292-115">**Měření**</span><span class="sxs-lookup"><span data-stu-id="d4292-115">**Measurement**</span></span>
- <span data-ttu-id="d4292-116">**Měření cíle**</span><span class="sxs-lookup"><span data-stu-id="d4292-116">**Goal Measurement**</span></span>

<span data-ttu-id="d4292-117">Kromě toho byly do entity **diskuse** přidány volby **Celkové skóre** a **Průměrné skóre**.</span><span class="sxs-lookup"><span data-stu-id="d4292-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="d4292-118">Zvětšit délku komentářů k žádosti o dovolenou (275641)</span><span class="sxs-lookup"><span data-stu-id="d4292-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="d4292-119">Komentáře k žádostem o dovolenou nyní umožňují více než 100 znaků.</span><span class="sxs-lookup"><span data-stu-id="d4292-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="d4292-120">Závěrečné komentáře k revizím se nezobrazí, když je manažer nebo zaměstnanec přihlášen do jiné společnosti (431688)</span><span class="sxs-lookup"><span data-stu-id="d4292-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="d4292-121">Všechny komentáře se nyní zobrazí při prohlížení recenzí.</span><span class="sxs-lookup"><span data-stu-id="d4292-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="d4292-122">U nového formuláře pracovníka nejsou uživatelem definované odkazy podporovány (390374)</span><span class="sxs-lookup"><span data-stu-id="d4292-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="d4292-123">Uživatelem definované odkazy jsou nyní povoleny na zjednodušeném formuláři **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="d4292-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="d4292-124">HcmRatingLevelEntity způsobuje selhání rozhraní API OData (439476)</span><span class="sxs-lookup"><span data-stu-id="d4292-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="d4292-125">Tato změna opravuje selhání rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="d4292-125">This change corrects the API crash.</span></span> <span data-ttu-id="d4292-126">Tuto chybu způsobil duplicitní název.</span><span class="sxs-lookup"><span data-stu-id="d4292-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d4292-127">Náhled</span><span class="sxs-lookup"><span data-stu-id="d4292-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="d4292-128">Pozastavit pracovní volno</span><span class="sxs-lookup"><span data-stu-id="d4292-128">Leave suspension</span></span>

<span data-ttu-id="d4292-129">Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d4292-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="d4292-130">Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="d4292-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="d4292-131">Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d4292-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="d4292-132">Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="d4292-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="d4292-133">Aktualizujte uživatelské prostředí, abyste naznačili, že akruální účet je pozastaven (429550)</span><span class="sxs-lookup"><span data-stu-id="d4292-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="d4292-134">Uživatelská zkušenost nyní naznačuje, že přírůstek byl pro plán pozastaven.</span><span class="sxs-lookup"><span data-stu-id="d4292-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="d4292-135">Pozastavení časového limitu pro vybrané typy dovolené (272447)</span><span class="sxs-lookup"><span data-stu-id="d4292-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="d4292-136">V této verzi může HR vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="d4292-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d4292-137">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="d4292-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d4292-138">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="d4292-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="d4292-139">Entita DMF je k dispozici pro akruální pozastavení (429549)</span><span class="sxs-lookup"><span data-stu-id="d4292-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="d4292-140">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="d4292-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="d4292-141">Přidejte kód příčiny pro akruální pozastavení (429547)</span><span class="sxs-lookup"><span data-stu-id="d4292-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="d4292-142">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="d4292-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="d4292-143">Začněte přechod z parametrů lidských zdrojů na parametry dovolené a nepřítomnosti</span><span class="sxs-lookup"><span data-stu-id="d4292-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="d4292-144">Tato verze začíná kombinovat parametry lidských zdrojů s parametry dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="d4292-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d4292-145">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="d4292-145">Carry forward rules</span></span>

<span data-ttu-id="d4292-146">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="d4292-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d4292-147">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="d4292-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d4292-148">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="d4292-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="d4292-149">Známé problémy</span><span class="sxs-lookup"><span data-stu-id="d4292-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="d4292-150">V některých prostředích nefunguje náhled služby SharePoint</span><span class="sxs-lookup"><span data-stu-id="d4292-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="d4292-151">Pokud nefunguje náhled dokumentů uložených ve službě SharePoint, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="d4292-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="d4292-152">Ověřte, zda má uživatelský účet Správce přidružen e-mail k záznamu uživatele.</span><span class="sxs-lookup"><span data-stu-id="d4292-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="d4292-153">Tyto informace můžete zobrazit na stránce **Uživatel**.</span><span class="sxs-lookup"><span data-stu-id="d4292-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="d4292-154">Není-li e-mail nastaven, je nutné přidat e-mail a poskytovatele pomocí doplňku OData Excel.</span><span class="sxs-lookup"><span data-stu-id="d4292-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="d4292-155">Ve výchozím nastavení není v návrhu aplikace Excel e-mailová adresa k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d4292-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="d4292-156">Je nutné upravit návrh aplikace Excel, přidat všechna pole, použít a aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="d4292-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="d4292-157">Po dokončení těchto kroků můžete aktualizovat účet správce.</span><span class="sxs-lookup"><span data-stu-id="d4292-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="d4292-158">Poté, co má účet správce přidružen e-mailový účet, přihlaste se k modulu Human Resources s pověřeními správce.</span><span class="sxs-lookup"><span data-stu-id="d4292-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="d4292-159">Ve službě SharePoint přistupte k příloze a zobrazte náhled dokumentu.</span><span class="sxs-lookup"><span data-stu-id="d4292-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="d4292-160">Přihlaste se s jiným uživatelským účtem, který má přístup k přílohám, a ověřte, že náhled funguje očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="d4292-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>