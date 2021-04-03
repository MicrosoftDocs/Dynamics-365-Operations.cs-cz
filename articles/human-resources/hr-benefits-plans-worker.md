---
title: Vytvoření plánů zaměstnaneckých výhod pracovníka
description: Plány zaměstnaneckých výhod pracovníka můžete v Microsoft Dynamics 365 Human Resources vytvořit pro výběr plánů zaměstnaneckých výhod pro zaměstnance a potvrzení výběrů plánu zaměstnaneckých výhod.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ac357bbef4bf84b9eaf153834bc7a609240c45e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464219"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="7a75f-103">Vytvoření plánů zaměstnaneckých výhod pracovníka</span><span class="sxs-lookup"><span data-stu-id="7a75f-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7a75f-104">Plány zaměstnaneckých výhod pracovníka můžete v Microsoft Dynamics 365 Human Resources vytvořit pro výběr plánů zaměstnaneckých výhod pro zaměstnance a potvrzení výběrů plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="7a75f-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="7a75f-105">Zaměstnanci obvykle vybírají plány zaměstnaneckých výhod sami pomocí samoobsluhy zaměstnanců a potom výběr potvrdí správce zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="7a75f-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="7a75f-106">V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **Plán zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="7a75f-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="7a75f-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="7a75f-107">Select **New**.</span></span>

3. <span data-ttu-id="7a75f-108">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="7a75f-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="7a75f-109">Pole</span><span class="sxs-lookup"><span data-stu-id="7a75f-109">Field</span></span> | <span data-ttu-id="7a75f-110">Popis</span><span class="sxs-lookup"><span data-stu-id="7a75f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7a75f-111">Období</span><span class="sxs-lookup"><span data-stu-id="7a75f-111">Period</span></span> | <span data-ttu-id="7a75f-112">Určuje období zaměstnaneckých výhod, které se použije k filtrování plánů na pevné záložce Plány. Plány filtrujte, což vám pomůže vybrat dílčí sadu všech záznamů plánu, abyste mohli dílčí sadu potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7a75f-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="7a75f-113">Vyberte například období, které jste vytvořili, s názvem 2015, a potvrďte všechny výběry pro přihlášení zaměstnaneckých výhod pro rok 2015.</span><span class="sxs-lookup"><span data-stu-id="7a75f-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="7a75f-114">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="7a75f-114">Worker</span></span> | <span data-ttu-id="7a75f-115">Určuje pracovníka, který se použije k filtrování plánů na pevné záložce Plány. Plány filtrujte, což vám pomůže vybrat dílčí sadu všech záznamů plánu, abyste mohli dílčí sadu potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7a75f-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-116">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="7a75f-116">Legal entity</span></span> | <span data-ttu-id="7a75f-117">Určuje právnickou osobu, která se použije k filtrování plánů na pevné záložce Plány. Plány filtrujte, což vám pomůže vybrat dílčí sadu všech záznamů plánu, abyste mohli dílčí sadu potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7a75f-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-118">Možnost pokrytí</span><span class="sxs-lookup"><span data-stu-id="7a75f-118">Coverage option</span></span> | <span data-ttu-id="7a75f-119">Určuje možnost krytí, která se použije k filtrování plánů na pevné záložce Plány. Plány filtrujte, což vám pomůže vybrat dílčí sadu všech záznamů plánu, abyste mohli dílčí sadu potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7a75f-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-120">Výchozí</span><span class="sxs-lookup"><span data-stu-id="7a75f-120">Default</span></span> | <span data-ttu-id="7a75f-121">Filtruje plány zaměstnaneckých výhod podle toho, zda se jedná o výchozí plán.</span><span class="sxs-lookup"><span data-stu-id="7a75f-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="7a75f-122">Filtrováním plánů usnadníte výběr dílčích záznamů plánu tak, abyste mohli potvrdit dílčí sadu.</span><span class="sxs-lookup"><span data-stu-id="7a75f-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-123">Stav</span><span class="sxs-lookup"><span data-stu-id="7a75f-123">Status</span></span> | <span data-ttu-id="7a75f-124">Filtruje plány zaměstnaneckých výhod na základě jejich stavu.</span><span class="sxs-lookup"><span data-stu-id="7a75f-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="7a75f-125">Filtrováním plánů usnadníte výběr dílčích záznamů plánu tak, abyste mohli potvrdit dílčí sadu.</span><span class="sxs-lookup"><span data-stu-id="7a75f-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-126">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="7a75f-126">Confirmation</span></span> | <span data-ttu-id="7a75f-127">Určuje stav potvrzení, který se použije k filtrování plánů na pevné záložce Plány. Plány filtrujte, což vám pomůže vybrat dílčí sadu všech záznamů plánu, abyste mohli dílčí sadu potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7a75f-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-128">Zrušení</span><span class="sxs-lookup"><span data-stu-id="7a75f-128">Cancellation</span></span> | <span data-ttu-id="7a75f-129">Určuje stav zrušení, který se použije k filtrování plánů na pevné záložce Plány. Plány filtrujte, což vám pomůže vybrat dílčí sadu všech záznamů plánu, abyste mohli dílčí sadu potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7a75f-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="7a75f-130">Filtr data platnosti</span><span class="sxs-lookup"><span data-stu-id="7a75f-130">Effective date filter</span></span> | <span data-ttu-id="7a75f-131">Filtruje plány podle toho, zda vyprší, jsou aktivní, nebo budou aktivní v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="7a75f-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="7a75f-132">Zaškrtněte políčka, která odpovídají plánům, které chcete zobrazit na pevné záložce Plány.</span><span class="sxs-lookup"><span data-stu-id="7a75f-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="7a75f-133">Plány</span><span class="sxs-lookup"><span data-stu-id="7a75f-133">Plans</span></span> | <span data-ttu-id="7a75f-134">Pevná záložka plány obsahuje plány, které vyhovují zadanému kritériu filtru.</span><span class="sxs-lookup"><span data-stu-id="7a75f-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="7a75f-135">Na každém řádku jsou zahrnuty odpovídající možnosti konfigurace, které byly nastaveny zaměstnancem HR a vybranými zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="7a75f-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="7a75f-136">Pole Oprávněný určuje, zda existuje konflikt ověření s výběrem plánu.</span><span class="sxs-lookup"><span data-stu-id="7a75f-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="7a75f-137">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7a75f-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]