---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (10. září 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
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
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 1340f17e57f49d6adb9dc0a7c769bafa655de56e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551236"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="e054e-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (10. září 2018)</span><span class="sxs-lookup"><span data-stu-id="e054e-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e054e-104">**Sestavení 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="e054e-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="e054e-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="e054e-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="e054e-106">Povolení specifického času ze dne na požadavku o volno (půlden)</span><span class="sxs-lookup"><span data-stu-id="e054e-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="e054e-107">Pokud jsou pracovní volno a absence nastaveny tak, aby bylo volno zadáváno ve dnech, můžete teď rovněž povolit definici půldne.</span><span class="sxs-lookup"><span data-stu-id="e054e-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="e054e-108">Když uživatelé odešlou požadavky na volno, mohou určit, zda žádají volno na první nebo druhou polovinu dne.</span><span class="sxs-lookup"><span data-stu-id="e054e-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="e054e-109">Ve výchozím nastavení je tato možnost vypnuta.</span><span class="sxs-lookup"><span data-stu-id="e054e-109">By default, this option is turned off.</span></span> <span data-ttu-id="e054e-110">U zaměstnanců, kteří mohou požádat o volno pouze na první nebo druhou polovinu dne, musíte zapnout tuto možnost v oblasti **Pracovní volno a absence** parametrů lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e054e-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="e054e-111">Oprávnění zabezpečení pro tuto funkci je Udržovat parametry lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e054e-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="e054e-112">Ověření zadání pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="e054e-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="e054e-113">V závislosti na konfiguraci pracovního volna zaměstnanci, kteří se pokusí odeslat požadavek na volno, které je delší než jejich pracovní den, obdrží zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="e054e-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="e054e-114">Jinak řečeno, jsou upozorněni v případě, že se pokusí vzít více než jeden celý den volna v jakékoliv dané datum.</span><span class="sxs-lookup"><span data-stu-id="e054e-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="e054e-115">Toto ověření je vždy zapnuto.</span><span class="sxs-lookup"><span data-stu-id="e054e-115">This validation is always turned on.</span></span> <span data-ttu-id="e054e-116">Pokaždé, když zaměstnanec překročí definovanou prahovou hodnotu dnů, dostane upozornění ve svém požadavku na volno.</span><span class="sxs-lookup"><span data-stu-id="e054e-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="e054e-117">Další pole pro podmíněné příkazy ve workflow</span><span class="sxs-lookup"><span data-stu-id="e054e-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="e054e-118">Další pole byla přidána do podmíněných příkazů a zástupných textů pro některá workflow v Core HR.</span><span class="sxs-lookup"><span data-stu-id="e054e-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="e054e-119">Následující pole byla přidána do workflow kompenzací, ukončení a převodu:</span><span class="sxs-lookup"><span data-stu-id="e054e-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="e054e-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="e054e-120">EmploymentType</span></span>
- <span data-ttu-id="e054e-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="e054e-121">LegalEntity</span></span>
- <span data-ttu-id="e054e-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="e054e-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="e054e-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="e054e-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="e054e-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="e054e-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="e054e-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="e054e-125">TransitionDate</span></span>
- <span data-ttu-id="e054e-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="e054e-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="e054e-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="e054e-127">WorkerStartDate</span></span>
- <span data-ttu-id="e054e-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="e054e-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="e054e-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="e054e-129">ProbationEndDate</span></span>
- <span data-ttu-id="e054e-130">Pozice</span><span class="sxs-lookup"><span data-stu-id="e054e-130">Position</span></span>
- <span data-ttu-id="e054e-131">Sjednocení</span><span class="sxs-lookup"><span data-stu-id="e054e-131">Union</span></span>
- <span data-ttu-id="e054e-132">Oddělení</span><span class="sxs-lookup"><span data-stu-id="e054e-132">Department</span></span>
- <span data-ttu-id="e054e-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="e054e-133">PositionType</span></span>
- <span data-ttu-id="e054e-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="e054e-134">CompLocation</span></span>
- <span data-ttu-id="e054e-135">Pozice</span><span class="sxs-lookup"><span data-stu-id="e054e-135">Title</span></span>
- <span data-ttu-id="e054e-136">Práce</span><span class="sxs-lookup"><span data-stu-id="e054e-136">Job</span></span>
- <span data-ttu-id="e054e-137">JobType</span><span class="sxs-lookup"><span data-stu-id="e054e-137">JobType</span></span>
- <span data-ttu-id="e054e-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="e054e-138">JobFamily</span></span>
- <span data-ttu-id="e054e-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="e054e-139">JobFunction</span></span>

<span data-ttu-id="e054e-140">Následující pole byla přidána do workflow pozic:</span><span class="sxs-lookup"><span data-stu-id="e054e-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="e054e-141">Pozice</span><span class="sxs-lookup"><span data-stu-id="e054e-141">Position</span></span>
- <span data-ttu-id="e054e-142">Sjednocení</span><span class="sxs-lookup"><span data-stu-id="e054e-142">Union</span></span>
- <span data-ttu-id="e054e-143">Oddělení</span><span class="sxs-lookup"><span data-stu-id="e054e-143">Department</span></span>
- <span data-ttu-id="e054e-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="e054e-144">PositionType</span></span>
- <span data-ttu-id="e054e-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="e054e-145">CompLocation</span></span>
- <span data-ttu-id="e054e-146">Pozice</span><span class="sxs-lookup"><span data-stu-id="e054e-146">Title</span></span>
- <span data-ttu-id="e054e-147">Práce</span><span class="sxs-lookup"><span data-stu-id="e054e-147">Job</span></span>
- <span data-ttu-id="e054e-148">JobType</span><span class="sxs-lookup"><span data-stu-id="e054e-148">JobType</span></span>
- <span data-ttu-id="e054e-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="e054e-149">JobFamily</span></span>
- <span data-ttu-id="e054e-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="e054e-150">JobFunction</span></span>

<span data-ttu-id="e054e-151">Pole v podmíněných příkazech a zástupných textech jsou dostupná pro všechny uživatele, kteří mají přístup ke konfiguraci výše zmíněných workflow.</span><span class="sxs-lookup"><span data-stu-id="e054e-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="e054e-152">Navigace do aplikace Attract ze správy personálu</span><span class="sxs-lookup"><span data-stu-id="e054e-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="e054e-153">Pokud nebyla aplikace Attract nastavena, část **Kandidáti k přjetí** přesměruje uživatele na spuštění aplikace Attract, namísto zobrazení zprávy „Nenašli jsme tady nic k zobrazení“.</span><span class="sxs-lookup"><span data-stu-id="e054e-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="e054e-154">Další změny</span><span class="sxs-lookup"><span data-stu-id="e054e-154">Other changes</span></span>

<span data-ttu-id="e054e-155">Toto vydání obsahuje několik dalších oprav chyb:</span><span class="sxs-lookup"><span data-stu-id="e054e-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="e054e-156">Když je přijat dodavatel, karta **Kompenzace** by neměla být k dispozici na stránce požadavku/akce.</span><span class="sxs-lookup"><span data-stu-id="e054e-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="e054e-157">V průběhu procesu ukončení požadavku nelze pokračovat, dokud všechna povinná pole neobsahují data.</span><span class="sxs-lookup"><span data-stu-id="e054e-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="e054e-158">Problémy s pořadím řazení a zobrazením dat v analýze správy personálu byly vyřešeny.</span><span class="sxs-lookup"><span data-stu-id="e054e-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
