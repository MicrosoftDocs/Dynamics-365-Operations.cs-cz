---
title: Zpracování způsobilosti k registraci
description: Tento článek vysvětluje, jak spustit proces nároku na přihlášení.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25699d643b3e74fe7118884457ab17314d1f9132
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466295"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="dc263-103">Zpracování způsobilosti k registraci</span><span class="sxs-lookup"><span data-stu-id="dc263-103">Process enrollment eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dc263-104">Tento článek vysvětluje, jak spustit proces nároku na přihlášení.</span><span class="sxs-lookup"><span data-stu-id="dc263-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="dc263-105">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování nároku na registraci**.</span><span class="sxs-lookup"><span data-stu-id="dc263-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="dc263-106">V dialogovém okně **Spustit proces nároku na registraci zaměstnanecké výhody** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="dc263-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="dc263-107">Pole</span><span class="sxs-lookup"><span data-stu-id="dc263-107">Field</span></span> | <span data-ttu-id="dc263-108">Popis</span><span class="sxs-lookup"><span data-stu-id="dc263-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="dc263-109">**Období registrace**</span><span class="sxs-lookup"><span data-stu-id="dc263-109">**Enrollment period**</span></span> | <span data-ttu-id="dc263-110">Období pro přihlášení pro zpracování nároku na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="dc263-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="dc263-111">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="dc263-111">**Legal entity**</span></span> | <span data-ttu-id="dc263-112">Právnická osoba pro zpracování nároku na registraci.</span><span class="sxs-lookup"><span data-stu-id="dc263-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="dc263-113">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="dc263-113">**Worker**</span></span> | <span data-ttu-id="dc263-114">Pracovník pro zpracování nároku na registraci.</span><span class="sxs-lookup"><span data-stu-id="dc263-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="dc263-115">Pokud toto pole ponecháte prázdné, bude nárok na registraci zpracován pro všechny pracovníky.</span><span class="sxs-lookup"><span data-stu-id="dc263-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="dc263-116">**Plán zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="dc263-116">**Benefit plan**</span></span> | <span data-ttu-id="dc263-117">Plán zaměstnaneckých výhod pro zpracování nároku na registraci.</span><span class="sxs-lookup"><span data-stu-id="dc263-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="dc263-118">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="dc263-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="dc263-119">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="dc263-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="dc263-120">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc263-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="dc263-121">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc263-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="dc263-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc263-122">Select **OK**.</span></span> <span data-ttu-id="dc263-123">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="dc263-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="dc263-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc263-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="dc263-125">Zobrazit výsledky procesu</span><span class="sxs-lookup"><span data-stu-id="dc263-125">View Process Results</span></span>

<span data-ttu-id="dc263-126">Tento článek vysvětluje, jak zobrazit výsledky procesu nároku.</span><span class="sxs-lookup"><span data-stu-id="dc263-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="dc263-127">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracovat výsledky**.</span><span class="sxs-lookup"><span data-stu-id="dc263-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="dc263-128">Ve formuláři **Zpracovat výsledky** se specifikují následující pole:</span><span class="sxs-lookup"><span data-stu-id="dc263-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="dc263-129">Pole</span><span class="sxs-lookup"><span data-stu-id="dc263-129">Field</span></span> | <span data-ttu-id="dc263-130">popis</span><span class="sxs-lookup"><span data-stu-id="dc263-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="dc263-131">**ID procesu**</span><span class="sxs-lookup"><span data-stu-id="dc263-131">**Process ID**</span></span> | <span data-ttu-id="dc263-132">Jedinečné ID pro kombinaci pracovníka, právnické osoby a běhu procesu.</span><span class="sxs-lookup"><span data-stu-id="dc263-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="dc263-133">**Typ procesu**</span><span class="sxs-lookup"><span data-stu-id="dc263-133">**Process type**</span></span> | <span data-ttu-id="dc263-134">Tím se identifikuje proces, který byl spuštěn.</span><span class="sxs-lookup"><span data-stu-id="dc263-134">This identifies the process that was run.</span></span> <span data-ttu-id="dc263-135">Například: Přihlášení.</span><span class="sxs-lookup"><span data-stu-id="dc263-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="dc263-136">**Časový údaj**</span><span class="sxs-lookup"><span data-stu-id="dc263-136">**Time stamp**</span></span> | <span data-ttu-id="dc263-137">Čas, kdy byl spuštěn proces nároku.</span><span class="sxs-lookup"><span data-stu-id="dc263-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="dc263-138">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="dc263-138">**Legal entity**</span></span> | <span data-ttu-id="dc263-139">Právnická osoba určená v průběhu procesu zápisu.</span><span class="sxs-lookup"><span data-stu-id="dc263-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="dc263-140">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="dc263-140">**Worker**</span></span> | <span data-ttu-id="dc263-141">Pracovník, který byl zpracován.</span><span class="sxs-lookup"><span data-stu-id="dc263-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="dc263-142">\*\*Plán</span><span class="sxs-lookup"><span data-stu-id="dc263-142">\*\*Plan</span></span> | <span data-ttu-id="dc263-143">Plán zaměstnaneckých výhod, pro který byl proveden pokus o zápis.</span><span class="sxs-lookup"><span data-stu-id="dc263-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="dc263-144">**Pravidlo způsobilosti**</span><span class="sxs-lookup"><span data-stu-id="dc263-144">**Eligibility rule**</span></span> | <span data-ttu-id="dc263-145">Pravidlo způsobilosti, které bylo zpracováno.</span><span class="sxs-lookup"><span data-stu-id="dc263-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="dc263-146">Pokud došlo k chybě před spuštěním nároku na způsobilost, bude toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="dc263-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="dc263-147">Například: Pokud pro pracovníka nebyla definována kompenzace, proces nároku nebude spuštěn a toto pole zůstane prázdné.</span><span class="sxs-lookup"><span data-stu-id="dc263-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="dc263-148">**Výsledný stav**</span><span class="sxs-lookup"><span data-stu-id="dc263-148">**Result status**</span></span> | <span data-ttu-id="dc263-149">To bude způsobilé nebo nezpůsobilé.</span><span class="sxs-lookup"><span data-stu-id="dc263-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="dc263-150">Pokud pracovník nesplní požadované informace, jako je například četnost plateb nebo fixní kompenzace, nebo pokud v plánu zaměstnaneckých výhod chybí informace, které brání registraci zaměstnanců, nebude mít výsledný stav nárok.</span><span class="sxs-lookup"><span data-stu-id="dc263-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="dc263-151">**Výsledná zpráva**</span><span class="sxs-lookup"><span data-stu-id="dc263-151">**Result message**</span></span> | <span data-ttu-id="dc263-152">Označuje, proč pracovník nemá nárok na plán zaměstnaneckých výhod nebo který předává pravidlo způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="dc263-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |



[!INCLUDE[footer-include](../includes/footer-banner.md)]