---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (18. února 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 18. únoru 2020.
author: andreabichsel
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66ffd9d0ffcf0e8466be785274ef5fb0fceda7a9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463783"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="7dc53-103">Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (18. února 2020)</span><span class="sxs-lookup"><span data-stu-id="7dc53-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7dc53-104">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7dc53-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7dc53-105">Změny se vztahují na sestavení číslo 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="7dc53-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="7dc53-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="7dc53-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="7dc53-107">Aktualizace platformy 32</span><span class="sxs-lookup"><span data-stu-id="7dc53-107">Platform update 32</span></span> 

<span data-ttu-id="7dc53-108">Nyní je k dispozici aktualizace platformy 32.</span><span class="sxs-lookup"><span data-stu-id="7dc53-108">Platform update 32 is now available.</span></span> <span data-ttu-id="7dc53-109">Další informace naleznete v tématu [Co je nového nebo změněné v aktualizaci Platform update 32 pro Finance and Operations (únor 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="7dc53-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="7dc53-110">Vyhledávací hodnoty se pamatují při změně možností zobrazení ve zjednodušeném formuláři zaměstnanců (383833)</span><span class="sxs-lookup"><span data-stu-id="7dc53-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="7dc53-111">Nový formulář **Pracovníka** nyní pamatuje hodnoty vyhledávání, když změníte možnosti zobrazení a použijete změny.</span><span class="sxs-lookup"><span data-stu-id="7dc53-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="7dc53-112">Souhrnné dlaždice správy kompenzací v náhledu funkce přesměrovat na nesprávný formulář (401861)</span><span class="sxs-lookup"><span data-stu-id="7dc53-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="7dc53-113">Dlaždice správy pevné a variabilní kompenzace nyní zobrazují správné záznamy ve formuláři nový **pracovník**.</span><span class="sxs-lookup"><span data-stu-id="7dc53-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="7dc53-114">Týká se pouze zjednodušené funkce náhledu formuláře zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="7dc53-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="7dc53-115">Tuto funkci náhledu lze povolit ve **Správě funkcí**.</span><span class="sxs-lookup"><span data-stu-id="7dc53-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="7dc53-116">Další informace naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="7dc53-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a><span data-ttu-id="7dc53-117">Prázdné pole stavu pro některé záznamy požadavků na dovolenou v Dataverse (414915)</span><span class="sxs-lookup"><span data-stu-id="7dc53-117">Empty Status field for some leave request records in Dataverse (414915)</span></span>

<span data-ttu-id="7dc53-118">Tato změna opravuje problém v Dataverse v případě, že je pole **Stav** v požadavku na dovolenou nastaveno na **Zkontrolovat**.</span><span class="sxs-lookup"><span data-stu-id="7dc53-118">This change corrects an issue in Dataverse when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="7dc53-119">Dataverse nyní odráží stav.</span><span class="sxs-lookup"><span data-stu-id="7dc53-119">Dataverse now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="7dc53-120">Analýza mezer v dovednostech je možná pouze pro přiřazenou úlohu (411390)</span><span class="sxs-lookup"><span data-stu-id="7dc53-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="7dc53-121">Nyní můžete provést analýzu mezer v dovednostech u kterékoli úlohy definované v modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7dc53-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="7dc53-122">Systémovou měnu nelze synchronizovat z Dataverse do modulu Human Resources v nových prostředích (418011)</span><span class="sxs-lookup"><span data-stu-id="7dc53-122">System currency doesn't sync from Dataverse to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="7dc53-123">Systémovou měnu v Dataverse lze nyní synchronizovat s Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7dc53-123">The system currency in Dataverse can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7dc53-124">Náhled</span><span class="sxs-lookup"><span data-stu-id="7dc53-124">In preview</span></span>

- [<span data-ttu-id="7dc53-125">Funkce náhledu pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="7dc53-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="7dc53-126">Funkce náhledu správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="7dc53-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="7dc53-127">Již brzy</span><span class="sxs-lookup"><span data-stu-id="7dc53-127">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="7dc53-128">Aktualizované řešení služby Dataverse</span><span class="sxs-lookup"><span data-stu-id="7dc53-128">Updated Dataverse solution</span></span>

<span data-ttu-id="7dc53-129">Nové řešení Dataverse bude brzy k dispozici po provedení následujících změn:</span><span class="sxs-lookup"><span data-stu-id="7dc53-129">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="7dc53-130">Popis</span><span class="sxs-lookup"><span data-stu-id="7dc53-130">Description</span></span> | <span data-ttu-id="7dc53-131">Změna</span><span class="sxs-lookup"><span data-stu-id="7dc53-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="7dc53-132">Změny entity **práce/pozice**</span><span class="sxs-lookup"><span data-stu-id="7dc53-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="7dc53-133">Přidána **Oblast kompenzace**</span><span class="sxs-lookup"><span data-stu-id="7dc53-133">**Compensation region** added</span></span></br><span data-ttu-id="7dc53-134">Přidání **finančních dimenzí**</span><span class="sxs-lookup"><span data-stu-id="7dc53-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="7dc53-135">Změny entity **pracovníka**</span><span class="sxs-lookup"><span data-stu-id="7dc53-135">**Worker** entity changes</span></span> | <span data-ttu-id="7dc53-136">Přidání **sekvence jmen**</span><span class="sxs-lookup"><span data-stu-id="7dc53-136">**Name sequence** added</span></span></br><span data-ttu-id="7dc53-137">Přidaná možnost **Práce z domova**</span><span class="sxs-lookup"><span data-stu-id="7dc53-137">**Works from home** added</span></span></br><span data-ttu-id="7dc53-138">Přidán **jazyk**</span><span class="sxs-lookup"><span data-stu-id="7dc53-138">**Language** added</span></span></br><span data-ttu-id="7dc53-139">Přidáno **Datum služebního věku**</span><span class="sxs-lookup"><span data-stu-id="7dc53-139">**Seniority date** added</span></span></br><span data-ttu-id="7dc53-140">Přidáno **Datum výročí**</span><span class="sxs-lookup"><span data-stu-id="7dc53-140">**Anniversary date** added</span></span></br><span data-ttu-id="7dc53-141">Přidáno **Datum původního přijetí**</span><span class="sxs-lookup"><span data-stu-id="7dc53-141">**Original hire date** added</span></span> |
| <span data-ttu-id="7dc53-142">Změny **entity zaměstnání**</span><span class="sxs-lookup"><span data-stu-id="7dc53-142">**Employment** entity changes</span></span> | <span data-ttu-id="7dc53-143">Přidání **finančních dimenzí**</span><span class="sxs-lookup"><span data-stu-id="7dc53-143">**Financial dimensions** added</span></span></br><span data-ttu-id="7dc53-144">Přidán **Důvod pro výpověď**</span><span class="sxs-lookup"><span data-stu-id="7dc53-144">**Termination reason** added</span></span></br><span data-ttu-id="7dc53-145">**Datum ukončení** přejmenováno z **data přechodu**</span><span class="sxs-lookup"><span data-stu-id="7dc53-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="7dc53-146">Přidáno **datum zkušební doby**</span><span class="sxs-lookup"><span data-stu-id="7dc53-146">**Probation date** added</span></span> |
| <span data-ttu-id="7dc53-147">Změny entity **adresy pracovníka**</span><span class="sxs-lookup"><span data-stu-id="7dc53-147">**Worker address** entity changes</span></span> | <span data-ttu-id="7dc53-148">Přidána **Adresa ulice**</span><span class="sxs-lookup"><span data-stu-id="7dc53-148">**Street address** added</span></span></br><span data-ttu-id="7dc53-149">**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis</span><span class="sxs-lookup"><span data-stu-id="7dc53-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="7dc53-150">Nové entity nastavení s nastavením variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="7dc53-150">New variable compensation setup entities</span></span> | <span data-ttu-id="7dc53-151">**Typ plánu variabilní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="7dc53-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="7dc53-152">**Plán variabilní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="7dc53-152">**Compensation variable plan**</span></span></br><span data-ttu-id="7dc53-153">**Pravidla připsání**</span><span class="sxs-lookup"><span data-stu-id="7dc53-153">**Vesting rules**</span></span></br><span data-ttu-id="7dc53-154">**Úroveň plánu variabilní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="7dc53-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="7dc53-155">Nová entita **Zaměstnání dle kalendáře pracovníka**</span><span class="sxs-lookup"><span data-stu-id="7dc53-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="7dc53-156">Byla přidána **entita pracovního kalendáře**</span><span class="sxs-lookup"><span data-stu-id="7dc53-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="7dc53-157">Nová entita **Mzdové podrobnosti o pozici**</span><span class="sxs-lookup"><span data-stu-id="7dc53-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="7dc53-158">Byla přidána položka **Mzdové podrobnosti o pozici**.</span><span class="sxs-lookup"><span data-stu-id="7dc53-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="7dc53-159">Nová entita **Pozice**</span><span class="sxs-lookup"><span data-stu-id="7dc53-159">New **Title** entity</span></span> | <span data-ttu-id="7dc53-160">Byla přidána položka **Pozice**.</span><span class="sxs-lookup"><span data-stu-id="7dc53-160">**Title** added.</span></span> <span data-ttu-id="7dc53-161">Nová entita **Nadpis** bude zahrnuta do procesu synchronizace mezi lidskými zdroji a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7dc53-161">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="7dc53-162">Na počátku nebude odkazovat z entit **Pracovní pozice** nebo **Úloha**.</span><span class="sxs-lookup"><span data-stu-id="7dc53-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7dc53-163">Viz také</span><span class="sxs-lookup"><span data-stu-id="7dc53-163">See also</span></span>

[<span data-ttu-id="7dc53-164">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="7dc53-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7dc53-165">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="7dc53-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7dc53-166">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="7dc53-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7dc53-167">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="7dc53-167">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]