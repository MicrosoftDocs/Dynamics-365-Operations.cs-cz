---
title: Zjednodušené zadávání zaměstnance a navigace
description: Zadávání dat pro pracovníky v aplikaci Dynamics 365 Talent bylo rozšířeno tak, aby umožňovalo rychlé zadání pro všechny zaměstnance, minulé, aktivní nebo budoucí. Byl aktualizován zjednodušený nebo konsolidovaný navigační model s cílem rychlého vyhledání souvisejících informací a zobrazení a provedení nezbytných aktualizací.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009415"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="0a1ae-104">Zjednodušené zadávání zaměstnance a navigace</span><span class="sxs-lookup"><span data-stu-id="0a1ae-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a1ae-105">Dynamics 365 Talent umožňuje efektivní zadávání údajů o zaměstnancích a zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="0a1ae-106">Informace o historii práce můžete rychle aktualizovat pro minulé, aktivní a budoucí zaměstnance a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="0a1ae-107">Můžete také povolit zjednodušenou navigaci s rychlým vyhledáváním informací souvisejících s uživatelem a provést potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="0a1ae-108">Tato funkce je nyní k dispozici v prostředích izolovaného prostoru.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="0a1ae-109">Chcete-li tuto funkci zapnout, přejděte na **Správa systému > Odkazy > Nastavení > Systémové parametry > Funkce náhledu**.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="0a1ae-110">Vyberte **Rozšířený formulář pracovníka a navigace**.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="0a1ae-111">To povolí tyto změny pro všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-111">This will enable these changes for all users.</span></span> <span data-ttu-id="0a1ae-112">Tuto možnost můžete kdykoli vypnout.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="0a1ae-113">Možnosti zobrazení</span><span class="sxs-lookup"><span data-stu-id="0a1ae-113">View options</span></span>

<span data-ttu-id="0a1ae-114">Pomocí příkazu **Možnosti zobrazení** ve formuláři pracovníka můžete vybrat libovolnou kombinaci zaměstnanců a dodavatelů z jednoho seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="0a1ae-115">Tyto možnosti umožňují zobrazit pracovníky mezi právnickými osobami nebo pro právnickou osobu, ke které jste právě přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="0a1ae-116">Můžete také zobrazit aktivní, čekající a ukončené pracovníky a můžete omezit výsledky na základě typu pracovníka (zaměstnanec nebo dodavatel).</span><span class="sxs-lookup"><span data-stu-id="0a1ae-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="0a1ae-117">Je-li povoleno rozšířené zabezpečení, zobrazí se pouze zaměstnanci a dodavatelé v právnických osobách, ke kterým máte přístup.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="0a1ae-118">Sloupce v seznamu se změní na základě vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="0a1ae-119">Například při zobrazení ukončených zaměstnanců se kódy data ukončení a důvodu zobrazí jako další sloupce v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="0a1ae-120">[![Možnosti zobrazení](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="0a1ae-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="0a1ae-121">Navigace a banner</span><span class="sxs-lookup"><span data-stu-id="0a1ae-121">Navigation and banner</span></span>

<span data-ttu-id="0a1ae-122">V tomto banneru jsou zobrazeny klíčové informace pro každého pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="0a1ae-123">V banneru aktivních pracovníků se zobrazí následující pole:</span><span class="sxs-lookup"><span data-stu-id="0a1ae-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="0a1ae-124">**Titul**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-124">**Title**</span></span>
- <span data-ttu-id="0a1ae-125">**Oddělení**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-125">**Department**</span></span>
- <span data-ttu-id="0a1ae-126">**Typ pozice**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-126">**Position type**</span></span>
- <span data-ttu-id="0a1ae-127">**Typ pracovníka**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-127">**Worker type**</span></span>
- <span data-ttu-id="0a1ae-128">**Manažer**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-128">**Manager**</span></span>
- <span data-ttu-id="0a1ae-129">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-129">**Legal entity**</span></span>

<span data-ttu-id="0a1ae-130">V banneru ukončených pracovníků se zobrazí následující pole:</span><span class="sxs-lookup"><span data-stu-id="0a1ae-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="0a1ae-131">**Datum ukončení**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-131">**Exited date**</span></span>
- <span data-ttu-id="0a1ae-132">**Důvod**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-132">**Reason**</span></span>

<span data-ttu-id="0a1ae-133">V banneru čekajících zaměstnanců se zobrazí následující pole:</span><span class="sxs-lookup"><span data-stu-id="0a1ae-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="0a1ae-134">**Titul**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-134">**Title**</span></span>
- <span data-ttu-id="0a1ae-135">**Oddělení**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-135">**Department**</span></span>
- <span data-ttu-id="0a1ae-136">**Typ pozice**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-136">**Position type**</span></span>
- <span data-ttu-id="0a1ae-137">**Manažer**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-137">**Manager**</span></span>
- <span data-ttu-id="0a1ae-138">**Počáteční datum**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-138">**Starting date**</span></span>
- <span data-ttu-id="0a1ae-139">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="0a1ae-139">**Legal entity**</span></span>

<span data-ttu-id="0a1ae-140">Podokno akcí na stránce pracovníka bylo znovu uspořádáno tak, aby obsahovalo méně možností.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="0a1ae-141">Informace jsou nyní uspořádány do následujících kategorií:</span><span class="sxs-lookup"><span data-stu-id="0a1ae-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="0a1ae-142">Práce</span><span class="sxs-lookup"><span data-stu-id="0a1ae-142">Work</span></span>
- <span data-ttu-id="0a1ae-143">Osoba</span><span class="sxs-lookup"><span data-stu-id="0a1ae-143">Person</span></span>
- <span data-ttu-id="0a1ae-144">Odejít</span><span class="sxs-lookup"><span data-stu-id="0a1ae-144">Leave</span></span>
- <span data-ttu-id="0a1ae-145">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="0a1ae-145">Compensation</span></span>
- <span data-ttu-id="0a1ae-146">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="0a1ae-146">Benefits</span></span>
- <span data-ttu-id="0a1ae-147">Dodržování předpisů</span><span class="sxs-lookup"><span data-stu-id="0a1ae-147">Compliance</span></span>

<span data-ttu-id="0a1ae-148">Kromě toho nová karta **Odkazy** na hlavní stránce pracovníka poskytuje uživatelům centrální umístění pro přístup ke všem souvisejícím informacím pro daného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="0a1ae-149">Z důvodu těchto změn se mohou informace zobrazit na jiném místě, než na jaké jste zvyklí.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="0a1ae-150">Například informace o mzdách, které se dříve zobrazily ve formuláři pracovníka, se nyní zobrazí v podokně akcí pod položkou **Kompenzace > mzdy** a karta **Osobní údaje** má nyní tlačítko **Další informace** pro pole, která často nepoužíváte.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="0a1ae-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="0a1ae-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="0a1ae-152">Historie práce</span><span class="sxs-lookup"><span data-stu-id="0a1ae-152">Work history</span></span>

<span data-ttu-id="0a1ae-153">Karta **Historie práce** zobrazuje historii práce pro všechny právnické osoby a je k dispozici pro ukončené, aktivní a čekající zaměstnance a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="0a1ae-154">Nyní můžete zobrazit celou historie práce pro právnické osoby, ke kterým máte přístup.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="0a1ae-155">Kromě toho můžete upravit informace pro každou z položek historie práce, aniž byste změnili kontext dat.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="0a1ae-156">Všechny informace lze aktualizovat přímo na stránce.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="0a1ae-157">[![Historie práce](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="0a1ae-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="0a1ae-158">Historie pozic</span><span class="sxs-lookup"><span data-stu-id="0a1ae-158">Position history</span></span>

<span data-ttu-id="0a1ae-159">Karta **Pozice** na hlavní stránce pracovníka poskytuje kompletní přehled o všech pozicích zastávaných v rámci organizace, včetně předchozích, současných a budoucích přiřazení.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="0a1ae-160">V podokně akcí lze nadále přejít přímo na historii pozic pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a1ae-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="0a1ae-161">[![Pozice](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="0a1ae-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

