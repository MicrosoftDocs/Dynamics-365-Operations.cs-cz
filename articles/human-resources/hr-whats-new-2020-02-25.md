---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (25. února 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092745"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="cef9c-103">Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (25. února 2020)</span><span class="sxs-lookup"><span data-stu-id="cef9c-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="cef9c-104">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cef9c-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cef9c-105">Změny se vztahují na sestavení číslo 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="cef9c-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="cef9c-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="cef9c-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="cef9c-107">Povolení entity platformy správy dat (DMF) a navigace správy případů (414754)</span><span class="sxs-lookup"><span data-stu-id="cef9c-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="cef9c-108">Tato ukázková funkce umožňuje další navigaci k případům správy případů.</span><span class="sxs-lookup"><span data-stu-id="cef9c-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="cef9c-109">Tuto ukázkovou funkci lze povolit v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="cef9c-110">Tyto položky nabídky se zobrazí v pracovním prostoru **Dodržování předpisů** v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cef9c-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cef9c-111">Díky této změně má Human Resources přístup k následujícím prostředkům:</span><span class="sxs-lookup"><span data-stu-id="cef9c-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="cef9c-112">Všechny případy</span><span class="sxs-lookup"><span data-stu-id="cef9c-112">All cases</span></span>
- <span data-ttu-id="cef9c-113">Moje případy</span><span class="sxs-lookup"><span data-stu-id="cef9c-113">My cases</span></span>
- <span data-ttu-id="cef9c-114">Moje otevřené případy</span><span class="sxs-lookup"><span data-stu-id="cef9c-114">My open cases</span></span>
- <span data-ttu-id="cef9c-115">Moje zpožděné případy</span><span class="sxs-lookup"><span data-stu-id="cef9c-115">My overdue cases</span></span>
- <span data-ttu-id="cef9c-116">Případy přiřazené mně prostřednictvím workflow</span><span class="sxs-lookup"><span data-stu-id="cef9c-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="cef9c-117">Spolu s těmito novými přehledy případů je k dispozici také entita DMF **Podrobnosti případu**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="cef9c-118">Povolení definic vztahů v globálním adresáři (414762)</span><span class="sxs-lookup"><span data-stu-id="cef9c-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="cef9c-119">V globálním adresáři jsou nyní povoleny vztahy.</span><span class="sxs-lookup"><span data-stu-id="cef9c-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="cef9c-120">Před vydáním verze tento týden se v okně s fakty **Vztahy** zobrazí všechny systémem definované vztahy.</span><span class="sxs-lookup"><span data-stu-id="cef9c-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="cef9c-121">Nyní můžete definovat vztahy v rámci stránky globálního adresáře.</span><span class="sxs-lookup"><span data-stu-id="cef9c-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="cef9c-122">Lze odebrat pozici, pokud existují aktivní záznamy kompenzace pro danou pozici (414568)</span><span class="sxs-lookup"><span data-stu-id="cef9c-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="cef9c-123">S touto změnou se zobrazí upozornění, pokud se pokusíte odstranit pozici a pracovník má aktivní záznam kompenzace pro stejnou pozici.</span><span class="sxs-lookup"><span data-stu-id="cef9c-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="cef9c-124">Pokud k tomu dojde, je nutné před odebráním pozice aktualizovat záznam fixní kompenzace zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="cef9c-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="cef9c-125">Workflow hodnocení výkonu občas přidává odhlášené osoby, které nejsou součástí procesu (414171)</span><span class="sxs-lookup"><span data-stu-id="cef9c-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="cef9c-126">Tato změna opravuje problém, kdy se do hodnocení výkonu přidávali další odhlášení účastníci.</span><span class="sxs-lookup"><span data-stu-id="cef9c-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="cef9c-127">Přiřazení pozice pracovníka není vytvořeno v Common Data Service, když je tato možnost vybrána v dialogovém okně Nový pracovník (413479)</span><span class="sxs-lookup"><span data-stu-id="cef9c-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="cef9c-128">Tato změna opravuje problém při zařazení nového pracovníka a jeho přiřazení k pozici prostřednictvím dialogového okna **Nový pracovník**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="cef9c-129">Nyní se přiřazení pozice projeví v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cef9c-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="cef9c-130">Již brzy</span><span class="sxs-lookup"><span data-stu-id="cef9c-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="cef9c-131">Aktualizované řešení služby Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cef9c-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="cef9c-132">Nové řešení Common Data Service bude brzy k dispozici po provedení následujících změn:</span><span class="sxs-lookup"><span data-stu-id="cef9c-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="cef9c-133">Popis</span><span class="sxs-lookup"><span data-stu-id="cef9c-133">Description</span></span> | <span data-ttu-id="cef9c-134">Změna</span><span class="sxs-lookup"><span data-stu-id="cef9c-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="cef9c-135">Změny entity **práce/pozice**</span><span class="sxs-lookup"><span data-stu-id="cef9c-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="cef9c-136">Přidána **Oblast kompenzace**</span><span class="sxs-lookup"><span data-stu-id="cef9c-136">**Compensation region** added</span></span></br><span data-ttu-id="cef9c-137">Přidání **finančních dimenzí**</span><span class="sxs-lookup"><span data-stu-id="cef9c-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="cef9c-138">Změny entity **pracovníka**</span><span class="sxs-lookup"><span data-stu-id="cef9c-138">**Worker** entity changes</span></span> | <span data-ttu-id="cef9c-139">Přidání **sekvence jmen**</span><span class="sxs-lookup"><span data-stu-id="cef9c-139">**Name sequence** added</span></span></br><span data-ttu-id="cef9c-140">Přidaná možnost **Práce z domova**</span><span class="sxs-lookup"><span data-stu-id="cef9c-140">**Works from home** added</span></span></br><span data-ttu-id="cef9c-141">Přidán **jazyk**</span><span class="sxs-lookup"><span data-stu-id="cef9c-141">**Language** added</span></span></br><span data-ttu-id="cef9c-142">Přidáno **Datum služebního věku**</span><span class="sxs-lookup"><span data-stu-id="cef9c-142">**Seniority date** added</span></span></br><span data-ttu-id="cef9c-143">Přidáno **Datum výročí**</span><span class="sxs-lookup"><span data-stu-id="cef9c-143">**Anniversary date** added</span></span></br><span data-ttu-id="cef9c-144">Přidáno **Datum původního přijetí**</span><span class="sxs-lookup"><span data-stu-id="cef9c-144">**Original hire date** added</span></span> |
| <span data-ttu-id="cef9c-145">Změny **entity zaměstnání**</span><span class="sxs-lookup"><span data-stu-id="cef9c-145">**Employment** entity changes</span></span> | <span data-ttu-id="cef9c-146">Přidání **finančních dimenzí**</span><span class="sxs-lookup"><span data-stu-id="cef9c-146">**Financial dimensions** added</span></span></br><span data-ttu-id="cef9c-147">Přidán **Důvod pro výpověď**</span><span class="sxs-lookup"><span data-stu-id="cef9c-147">**Termination reason** added</span></span></br><span data-ttu-id="cef9c-148">**Datum ukončení** přejmenováno z **data přechodu**</span><span class="sxs-lookup"><span data-stu-id="cef9c-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="cef9c-149">Přidáno **datum zkušební doby**</span><span class="sxs-lookup"><span data-stu-id="cef9c-149">**Probation date** added</span></span> |
| <span data-ttu-id="cef9c-150">Změny entity **adresy pracovníka**</span><span class="sxs-lookup"><span data-stu-id="cef9c-150">**Worker address** entity changes</span></span> | <span data-ttu-id="cef9c-151">Přidána **Adresa ulice**</span><span class="sxs-lookup"><span data-stu-id="cef9c-151">**Street address** added</span></span></br><span data-ttu-id="cef9c-152">**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis</span><span class="sxs-lookup"><span data-stu-id="cef9c-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="cef9c-153">Nové entity nastavení s nastavením variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="cef9c-153">New variable compensation setup entities</span></span> | <span data-ttu-id="cef9c-154">**Typ plánu variabilní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="cef9c-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="cef9c-155">**Plán variabilní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="cef9c-155">**Compensation variable plan**</span></span></br><span data-ttu-id="cef9c-156">**Pravidla připsání**</span><span class="sxs-lookup"><span data-stu-id="cef9c-156">**Vesting rules**</span></span></br><span data-ttu-id="cef9c-157">**Úroveň plánu variabilní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="cef9c-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="cef9c-158">Nová entita **Zaměstnání dle kalendáře pracovníka**</span><span class="sxs-lookup"><span data-stu-id="cef9c-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="cef9c-159">Byla přidána **entita pracovního kalendáře**</span><span class="sxs-lookup"><span data-stu-id="cef9c-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="cef9c-160">Nová entita **Mzdové podrobnosti o pozici**</span><span class="sxs-lookup"><span data-stu-id="cef9c-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="cef9c-161">Byla přidána položka **Mzdové podrobnosti o pozici**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="cef9c-162">Nová entita **Pozice**</span><span class="sxs-lookup"><span data-stu-id="cef9c-162">New **Title** entity</span></span> | <span data-ttu-id="cef9c-163">Byla přidána položka **Pozice**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-163">**Title** added.</span></span> <span data-ttu-id="cef9c-164">Nová entita **Nadpis** bude zahrnuta do procesu synchronizace mezi lidskými zdroji a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cef9c-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="cef9c-165">Na počátku nebude odkazovat z entit **Pracovní pozice** nebo **Úloha**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="cef9c-166">Během příštích několika týdnů budou tyto změny entit k dispozici ve všech prostředích.</span><span class="sxs-lookup"><span data-stu-id="cef9c-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="cef9c-167">Postup při ruční instalaci nejnovějšího řešení Common Data Service pro Human Resources:</span><span class="sxs-lookup"><span data-stu-id="cef9c-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="cef9c-168">Přejděte do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cef9c-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="cef9c-169">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="cef9c-170">Vyhledjete prostředí, která chcete upgradovat.</span><span class="sxs-lookup"><span data-stu-id="cef9c-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="cef9c-171">To by mělo odpovídat poli **Název prostředí** v sekci **Informace o Common Data Service** ve formuláři **O aplikaci** v modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cef9c-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="cef9c-172">Vyberte prostředí pro zobrazení podrobností o prostředí.</span><span class="sxs-lookup"><span data-stu-id="cef9c-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="cef9c-173">Vyberte možnost **Správa řešení** na panelu akcí nahoře.</span><span class="sxs-lookup"><span data-stu-id="cef9c-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="cef9c-174">Otevře se nové okno prohlížeče a přejde do **Centra pro správu Dynamics 365** v kontextu vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="cef9c-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="cef9c-175">Na seznamu **Řešení** vyberte možnost **Kotva Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="cef9c-176">Chcete-li použít poslední řešení, vyberte možnost **Upgrade**.</span><span class="sxs-lookup"><span data-stu-id="cef9c-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="cef9c-177">Náhled</span><span class="sxs-lookup"><span data-stu-id="cef9c-177">In preview</span></span>

<span data-ttu-id="cef9c-178">Od 3. února 2020 budou k dispozici následující ukázkové funkce:</span><span class="sxs-lookup"><span data-stu-id="cef9c-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="cef9c-179">**Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="cef9c-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="cef9c-180">**Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cef9c-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>
