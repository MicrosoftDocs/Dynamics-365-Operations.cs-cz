---
title: Přehled správy zaměstnaneckých výhod
description: Přehled funkce správy zaměstnaneckých výhod v Dynamics 365 Human Resources. Nabídněte svým zaměstnancům rozšířené možnosti zaměstnaneckých výhod pomocí snadno použitelného online prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2020
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
ms.openlocfilehash: e2e8fcdd0b6124b459c4dc073e2929418d18bcc5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417596"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="fb77b-104">Přehled správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-104">Benefits management overview</span></span>

<span data-ttu-id="fb77b-105">Chcete-li si zachovat konkurenceschopnost, musíte nabídnout bohatý soubor zaměstnaneckých výhod, abyste přilákali a udrželi své nejlepší zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="fb77b-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="fb77b-106">Kromě standardních výhod, jako je pojištění zdravotní a zubní péče, můžete také nabízet rozšířené služby, např. pomoc s adopcí, rekreační programy a příspěvky na ošacení.</span><span class="sxs-lookup"><span data-stu-id="fb77b-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="fb77b-107">Funkce správy zaměstnaneckých výhod ve službě Microsoft Dynamics 365 Human Resources poskytuje flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="fb77b-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="fb77b-108">Aplikace Human Resources také zahrnuje snadno použitelné zaměstnanecké prostředí, které prezentuje vaše nabídky.</span><span class="sxs-lookup"><span data-stu-id="fb77b-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="fb77b-109">Vylepšené plány zaměstnaneckých výhod vám umožňují vytvářet a spravovat jedinečné plány zaměstnaneckých výhod a podporovat složité tabulky sazeb zaměstnaneckých výhod a vnořené úrovně.</span><span class="sxs-lookup"><span data-stu-id="fb77b-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="fb77b-110">Můžete snadno vytvářet programy, balíky a pravidla automatického zařazení pro zaměstnanecké výhody k usnadnění použití zaměstnancem.</span><span class="sxs-lookup"><span data-stu-id="fb77b-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="fb77b-111">Programy flexibilních kreditů umožňují rozdělit podporu mezi důchod a další životní události.</span><span class="sxs-lookup"><span data-stu-id="fb77b-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="fb77b-112">Rozsáhlá pravidla způsobilosti zajišťují poskytnutí správných zaměstnaneckých výhod odpovídajícím zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="fb77b-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="fb77b-113">Online zařazení do zaměstnaneckých výhod poskytuje vašim zaměstnancům snadno použitelné prostředí.</span><span class="sxs-lookup"><span data-stu-id="fb77b-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="fb77b-114">Kvalifikované zpracování životních událostí podporuje budoucí žívotní události.</span><span class="sxs-lookup"><span data-stu-id="fb77b-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="fb77b-115">Chcete-li získat přístup k ukázkovým datům, musíte znovu nasadit izolované testovací prostředí (sandbox).</span><span class="sxs-lookup"><span data-stu-id="fb77b-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="fb77b-116">Povolení správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-116">Enable Benefits management</span></span>

<span data-ttu-id="fb77b-117">Toto téma popisuje způsob, jakým lze zapnout funkce v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fb77b-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="fb77b-118">Také sděluje, které existující funkce v aplikaci Human Resources správa zaměstnaneckých výhod nahradí nebo jsou zakázány po zapnutí správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="fb77b-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb77b-119">Po povolení Správy zaměstnaneckých výhod v **Produkčním** prostředí ji již nelze zakázat.</span><span class="sxs-lookup"><span data-stu-id="fb77b-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="fb77b-120">Doporučujeme povolit a otestovat Správu zaměstnaneckých výhod v prostředí **Sandbox** před jejím povolením v **Produkčním** prostředí.</span><span class="sxs-lookup"><span data-stu-id="fb77b-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="fb77b-121">Existují významné rozdíly mezi staršími funkcemi výhod a novými funkcemi pro správu výhod, které vyžadují další nastavení a měly by být testovány před uvedením do produkce.</span><span class="sxs-lookup"><span data-stu-id="fb77b-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="fb77b-122">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="fb77b-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="fb77b-123">Konfigurace informací o zaměstnancích</span><span class="sxs-lookup"><span data-stu-id="fb77b-123">Configure employee information</span></span>

<span data-ttu-id="fb77b-124">Před zapojením zaměstnanců do zaměstnaneckých výhod je nutné zadat požadované informace.</span><span class="sxs-lookup"><span data-stu-id="fb77b-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="fb77b-125">Je nutné, aby byl zaměstnanec zapsán do **Plánu fixní kompenzace** první den a musíte vybrat **Frekvence plateb zaměstnaneckých výhod** v **Podrobnostech o zaměstnání** ve formuláři **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="fb77b-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="fb77b-126">Pokud máte zaměstnance, který dostává dodatečné odměny, jako jsou provize, můžete přidat částku **Roční výplata benefitů** ze záznamu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="fb77b-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="fb77b-127">Human Resources budou využívat částku **Roční výplata benefitů** při určování částek krytí, namísto pevné roční náhrady.</span><span class="sxs-lookup"><span data-stu-id="fb77b-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="fb77b-128">**Roční výplata benefitů** musí platit od počátečního data zaměstnance nebo od začátku období zaměstnaneckých výhod, podle toho, co nastane dříve.</span><span class="sxs-lookup"><span data-stu-id="fb77b-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="fb77b-129">Pokud je pro zaměstnance zaznamenána jak pevná odměna, tak roční částka zamšstnaneckých výhod, použije se při stanovení výše krytí roční plat zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="fb77b-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="fb77b-130">Při vytvoření plánu zaměstnaneckých výhod, který používá sazby založené na pohlaví nebo věku, je nutné zadat datum narození a pohlaví zaměstnance pro výpočet nákladů na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="fb77b-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="fb77b-131">Konfigurace správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-131">Configure Benefits management</span></span>

<span data-ttu-id="fb77b-132">Před vytvořením plánů zaměstnaneckých výhod pro vaše zaměstnance musíte nakonfigurovat možnosti pro plány.</span><span class="sxs-lookup"><span data-stu-id="fb77b-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="fb77b-133">Nastavení parametrů správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="fb77b-134">Konfigurace možností a pravidel způsobilosti</span><span class="sxs-lookup"><span data-stu-id="fb77b-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="fb77b-135">Konfigurace možností způsobilosti osobních kontaktů</span><span class="sxs-lookup"><span data-stu-id="fb77b-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="fb77b-136">Vytvoření možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="fb77b-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="fb77b-137">Nastavení frekvencí platby</span><span class="sxs-lookup"><span data-stu-id="fb77b-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="fb77b-138">Konfigurace typů životních událostí</span><span class="sxs-lookup"><span data-stu-id="fb77b-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="fb77b-139">Vytvoření typů plánu</span><span class="sxs-lookup"><span data-stu-id="fb77b-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="fb77b-140">Nastavení kódů důvodů</span><span class="sxs-lookup"><span data-stu-id="fb77b-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="fb77b-141">Nastavení kódů úrovně</span><span class="sxs-lookup"><span data-stu-id="fb77b-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="fb77b-142">Konfigurace sazeb</span><span class="sxs-lookup"><span data-stu-id="fb77b-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="fb77b-143">Konfigurace srážek</span><span class="sxs-lookup"><span data-stu-id="fb77b-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="fb77b-144">Konfigurace dnů čekání</span><span class="sxs-lookup"><span data-stu-id="fb77b-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="fb77b-145">Konfigurace období čekání</span><span class="sxs-lookup"><span data-stu-id="fb77b-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="fb77b-146">Nastavení pravidel zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="fb77b-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="fb77b-147">Vytvoření kategorií zaměstnání</span><span class="sxs-lookup"><span data-stu-id="fb77b-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="fb77b-148">Nastavení typů zaměstnání</span><span class="sxs-lookup"><span data-stu-id="fb77b-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="fb77b-149">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="fb77b-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="fb77b-150">Vytvoření plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-150">Create benefit plans</span></span>

<span data-ttu-id="fb77b-151">Tyto články ukazují, jak vytvářet plány zaměstnaneckých výhod, včetně balíků a programů pro pružné kredity.</span><span class="sxs-lookup"><span data-stu-id="fb77b-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="fb77b-152">Nastavení plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="fb77b-153">Nastavení programů flexibilních kreditů</span><span class="sxs-lookup"><span data-stu-id="fb77b-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="fb77b-154">Zpracování plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="fb77b-154">Process benefit plans</span></span>

<span data-ttu-id="fb77b-155">Některé změny je nutné zpracovat, aby byly aktivní.</span><span class="sxs-lookup"><span data-stu-id="fb77b-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="fb77b-156">Zpracování způsobilosti k registraci</span><span class="sxs-lookup"><span data-stu-id="fb77b-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="fb77b-157">Zpracování životních událostí</span><span class="sxs-lookup"><span data-stu-id="fb77b-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="fb77b-158">Zpracování změn životních událostí</span><span class="sxs-lookup"><span data-stu-id="fb77b-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="fb77b-159">Zpracování způsobilosti k životním událostem</span><span class="sxs-lookup"><span data-stu-id="fb77b-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="fb77b-160">Zpracování změn sazby</span><span class="sxs-lookup"><span data-stu-id="fb77b-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

