---
title: "Definování a správa programu zaměstnaneckých výhod"
description: "Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Tento článek obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6de99fc6aea808fddbec047cc74e533c4e5f9ee9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="c7492-104">Definování a správa programu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="c7492-104">Define and manage a benefits program</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c7492-105">Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="c7492-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="c7492-106">Toto téma obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="c7492-106">This topic provides information about how to set up an manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="c7492-107">Nastavení výhod</span><span class="sxs-lookup"><span data-stu-id="c7492-107">Benefit setup</span></span>
-------------

<span data-ttu-id="c7492-108">Než bude možné pracovníky přihlásit k zaměstnaneckým výhodám, je nutné vytvořit prvky jednotlivých výhod.</span><span class="sxs-lookup"><span data-stu-id="c7492-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="c7492-109">Tyto prvky kombinují podobné plány zaměstnaneckých výhod a definují výchozí nastavení, jako jsou například sazby srážek a podrobnosti účetnictví.</span><span class="sxs-lookup"><span data-stu-id="c7492-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="c7492-110">Mnoho z těchto nastavení lze upravit při pozdějším přihlášení pracovníků k zaměstnanecké výhodě.</span><span class="sxs-lookup"><span data-stu-id="c7492-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="c7492-111">Pro každý plán zaměstnanecké výhody může organizace nabízet několik možností přihlášení a pracovník se také může zříct přihlášení k plánu.</span><span class="sxs-lookup"><span data-stu-id="c7492-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="c7492-112">[![Tok procesu výhod](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="c7492-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="c7492-113">Prvky zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="c7492-113">Benefit elements</span></span>
<span data-ttu-id="c7492-114">Před zahájením tvorby zaměstnaneckých výhod a přihlašování pracovníků k nim je nutné definovat prvky, které tvoří zaměstnaneckou výhodu: typ, plán a možnosti.</span><span class="sxs-lookup"><span data-stu-id="c7492-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="c7492-115">**Typ** – kolekce plánů pro určité zaměstnanecké výhody, jako jsou lékař nebo parkování.</span><span class="sxs-lookup"><span data-stu-id="c7492-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="c7492-116">**Plán** – zvláštní zaměstnanecké výhody sjednané od zprostředkovatele.</span><span class="sxs-lookup"><span data-stu-id="c7492-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="c7492-117">**Možnost** – úroveň krytí, například pouze zaměstnanec nebo zaměstnanec a manžel/ka či partner/ka.</span><span class="sxs-lookup"><span data-stu-id="c7492-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="c7492-118">Organizace může svým pracovníkům pro každý typ zaměstnanecké výhody (například očního či zubního vyšetření) nabídnout jeden nebo více plánů.</span><span class="sxs-lookup"><span data-stu-id="c7492-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="c7492-119">Pro každý plán může organizace nabídnout různé možnosti.</span><span class="sxs-lookup"><span data-stu-id="c7492-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="c7492-120">Například si mohou zaměstnanci zakoupit další období krytí pojištění na úrovni jedno-, dvoj- nebo trojnásobku jejich roční mzdy.</span><span class="sxs-lookup"><span data-stu-id="c7492-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="c7492-121">Každá kombinace plánu a možností se stane zaměstnaneckou výhodou, ke které se mohou pracovníci přihlásit.</span><span class="sxs-lookup"><span data-stu-id="c7492-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="c7492-122">[![obrázek výhod](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="c7492-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="c7492-123">Způsobilost</span><span class="sxs-lookup"><span data-stu-id="c7492-123">Eligibility</span></span>
<span data-ttu-id="c7492-124">Mnoho okolností určuje nárok pracovníka na různé typy zaměstnaneckých výhod, které nabízí zaměstnavatel.</span><span class="sxs-lookup"><span data-stu-id="c7492-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="c7492-125">Když v aplikaci Microsoft Talent vytvoříte zaměstnaneckou výhodu, můžete nastavit typ nároku, který se k ní vztahuje.</span><span class="sxs-lookup"><span data-stu-id="c7492-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="c7492-126">Výhodu můžete zpřístupnit pro všechny zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="c7492-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="c7492-127">Například některé společnosti nabízejí parkovací místa pro všechny zaměstnance jako zaměstnaneckou výhodu.</span><span class="sxs-lookup"><span data-stu-id="c7492-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="c7492-128">Při vytváření zaměstnanecké výhody nastavíte nárok na možnost **Všichni pracovníci mají nárok**.</span><span class="sxs-lookup"><span data-stu-id="c7492-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="c7492-129">Pro jiné výhody jako obstavení a daňové odvody nárok neplatí.</span><span class="sxs-lookup"><span data-stu-id="c7492-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="c7492-130">Při vytváření těchto typů výhod nastavujete nárok na **Přeskočit proces nároku**.</span><span class="sxs-lookup"><span data-stu-id="c7492-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="c7492-131">Nárok na zaměstnaneckou výhodu nakonec může být založené na pravidlech.</span><span class="sxs-lookup"><span data-stu-id="c7492-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="c7492-132">Například společnost nabízí dva druhy pojištění zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="c7492-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="c7492-133">Vedení společnosti má nárok na jeden plán životního pojištění, zatímco ostatní zaměstnanci na plný úvazek mají nárok na jiný plán životního pojištění.</span><span class="sxs-lookup"><span data-stu-id="c7492-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="c7492-134">V aplikaci Talent můžete vytvořit pravidlo způsobilosti k uplatnění výhod, pomocí kterého můžete vyhledat všechny zaměstnance ve vedoucích pozicích, a jiné pravidlo k vyhledání všech ostatních zaměstnanců na plný úvazek a pak tato pravidla použít u příslušné výhody.</span><span class="sxs-lookup"><span data-stu-id="c7492-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="c7492-135">Přihlášení</span><span class="sxs-lookup"><span data-stu-id="c7492-135">Enrollment</span></span>
<span data-ttu-id="c7492-136">Po vytvoření zaměstnaneckých výhod, které vaše organizace nabízí, a určení nároku můžete k zaměstnaneckým výhodám přihlásit pracovníky.</span><span class="sxs-lookup"><span data-stu-id="c7492-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="c7492-137">V rámci jednoho procesu můžete k zaměstnaneckým výhodám přihlašovat jednotlivé pracovníky nebo mnoho pracovníků najednou.</span><span class="sxs-lookup"><span data-stu-id="c7492-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="c7492-138">Někdy může organizace přestat nabízet určité zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="c7492-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="c7492-139">V tomto případě je nutné aktualizovat výhodu a pracovníky, kteří jsou v programu zaregistrováni.</span><span class="sxs-lookup"><span data-stu-id="c7492-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="c7492-140">Hromadné vypršení zaměstnaneckých výhod umožňuje hromadně změnit datum vypršení platnosti zaměstnaneckých výhod a registrace pracovníků registrovaných k dané výhodě.</span><span class="sxs-lookup"><span data-stu-id="c7492-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="c7492-141">Můžete také vybrat několik pracovníků, kteří jsou registrováni k zaměstnaneckým výhodám, a změnit koncové datum jejich pokrytí.</span><span class="sxs-lookup"><span data-stu-id="c7492-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="c7492-142">Nápodobně vám prodloužení platnosti hromadné registrace zaměstnanecké výhody umožní odložit datum vypršení platnosti zaměstnanecké výhody i registrací pracovníků k dané výhodě, když se rozhodnete zaměstnaneckou výhodu nabízet déle, než jste původně plánovali.</span><span class="sxs-lookup"><span data-stu-id="c7492-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="see-also"></a><span data-ttu-id="c7492-143">Viz také</span><span class="sxs-lookup"><span data-stu-id="c7492-143">See also</span></span>
--------

[<span data-ttu-id="c7492-144">Zásady způsobilosti k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="c7492-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)




