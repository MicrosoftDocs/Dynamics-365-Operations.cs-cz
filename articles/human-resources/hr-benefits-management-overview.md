---
title: Přehled správy zaměstnaneckých výhod
description: Přehled funkce správy zaměstnaneckých výhod v Dynamics 365 Human Resources. Nabídněte svým zaměstnancům rozšířené možnosti zaměstnaneckých výhod pomocí snadno použitelného online prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 1043fb18c33e5ec0cde13008b168fd317c7c7be6
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599373"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="d7c35-104">Přehled správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-104">Benefits management overview</span></span>

<span data-ttu-id="d7c35-105">Chcete-li si zachovat konkurenceschopnost, musíte nabídnout bohatý soubor zaměstnaneckých výhod, abyste přilákali a udrželi své nejlepší zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d7c35-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="d7c35-106">Kromě standardních výhod, jako je pojištění zdravotní a zubní péče, můžete také nabízet rozšířené služby, např. pomoc s adopcí, rekreační programy a příspěvky na ošacení.</span><span class="sxs-lookup"><span data-stu-id="d7c35-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="d7c35-107">Funkce správy zaměstnaneckých výhod ve službě Microsoft Dynamics 365 Human Resources poskytuje flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="d7c35-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="d7c35-108">Aplikace Human Resources také zahrnuje snadno použitelné zaměstnanecké prostředí, které prezentuje vaše nabídky.</span><span class="sxs-lookup"><span data-stu-id="d7c35-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="d7c35-109">Vylepšené plány zaměstnaneckých výhod vám umožňují vytvářet a spravovat jedinečné plány zaměstnaneckých výhod a podporovat složité tabulky sazeb zaměstnaneckých výhod a vnořené úrovně.</span><span class="sxs-lookup"><span data-stu-id="d7c35-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="d7c35-110">Můžete snadno vytvářet programy, balíky a pravidla automatického zařazení pro zaměstnanecké výhody k usnadnění použití zaměstnancem.</span><span class="sxs-lookup"><span data-stu-id="d7c35-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="d7c35-111">Programy flexibilních kreditů umožňují rozdělit podporu mezi důchod a další životní události.</span><span class="sxs-lookup"><span data-stu-id="d7c35-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="d7c35-112">Rozsáhlá pravidla způsobilosti zajišťují poskytnutí správných zaměstnaneckých výhod odpovídajícím zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="d7c35-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="d7c35-113">Online zařazení do zaměstnaneckých výhod poskytuje vašim zaměstnancům snadno použitelné prostředí.</span><span class="sxs-lookup"><span data-stu-id="d7c35-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="d7c35-114">Kvalifikované zpracování životních událostí podporuje budoucí žívotní události.</span><span class="sxs-lookup"><span data-stu-id="d7c35-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="d7c35-115">Chcete-li získat přístup k ukázkovým datům, musíte znovu nasadit izolované testovací prostředí (sandbox).</span><span class="sxs-lookup"><span data-stu-id="d7c35-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="d7c35-116">Známé problémy se správou zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="d7c35-117">Programy flexibilních kreditů</span><span class="sxs-lookup"><span data-stu-id="d7c35-117">Flex credit programs</span></span>

<span data-ttu-id="d7c35-118">Celková hodnota kreditu definovaná pro program pružného kreditu není zobrazena ve formuláři **Plány zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="d7c35-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="d7c35-119">Pokud nastavíte program pružného kreditu na možnost **žádný**, zobrazí se při výběru a potvrzení plánů chyba ve formuláři **Plán zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="d7c35-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="d7c35-120">Povolení správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-120">Enable Benefits management</span></span>

<span data-ttu-id="d7c35-121">Tento článek popisuje způsob, jakým lze zapnout funkce v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d7c35-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="d7c35-122">Také sděluje, které existující funkce v aplikaci Human Resources správa zaměstnaneckých výhod nahradí nebo jsou zakázány po zapnutí správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="d7c35-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7c35-123">Po povolení Správy zaměstnaneckých výhod v **Produkčním** prostředí ji již nelze zakázat.</span><span class="sxs-lookup"><span data-stu-id="d7c35-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="d7c35-124">Doporučujeme povolit a otestovat Správu zaměstnaneckých výhod v prostředí **Sandbox** před jejím povolením v **Produkčním** prostředí.</span><span class="sxs-lookup"><span data-stu-id="d7c35-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="d7c35-125">Existují významné rozdíly mezi staršími funkcemi výhod a novými funkcemi pro správu výhod, které vyžadují další nastavení a měly by být testovány před uvedením do produkce.</span><span class="sxs-lookup"><span data-stu-id="d7c35-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="d7c35-126">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="d7c35-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="d7c35-127">Konfigurace informací o zaměstnancích</span><span class="sxs-lookup"><span data-stu-id="d7c35-127">Configure employee information</span></span>

<span data-ttu-id="d7c35-128">Před zapojením zaměstnanců do zaměstnaneckých výhod je nutné zadat požadované informace.</span><span class="sxs-lookup"><span data-stu-id="d7c35-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="d7c35-129">Je nutné, aby byl zaměstnanec zapsán do **Plánu fixní kompenzace** první den a musíte vybrat **Frekvence plateb zaměstnaneckých výhod** v **Podrobnostech o zaměstnání** ve formuláři **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="d7c35-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="d7c35-130">Pokud máte zaměstnance, který dostává dodatečné odměny, jako jsou provize, můžete přidat částku **Roční výplata benefitů** ze záznamu zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d7c35-130">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="d7c35-131">Human Resources budou využívat částku **Roční výplata benefitů** při určování částek krytí, namísto pevné roční náhrady.</span><span class="sxs-lookup"><span data-stu-id="d7c35-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="d7c35-132">**Roční výplata benefitů** musí platit od počátečního data zaměstnance nebo od začátku období zaměstnaneckých výhod, podle toho, co nastane dříve.</span><span class="sxs-lookup"><span data-stu-id="d7c35-132">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="d7c35-133">Pokud je pro zaměstnance zaznamenána jak pevná odměna, tak roční částka zamšstnaneckých výhod, použije se při stanovení výše krytí roční plat zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="d7c35-133">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="d7c35-134">Při vytvoření plánu zaměstnaneckých výhod, který používá sazby založené na pohlaví nebo věku, je nutné zadat datum narození a pohlaví zaměstnance pro výpočet nákladů na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="d7c35-134">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="d7c35-135">Konfigurace správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-135">Configure Benefits management</span></span>

<span data-ttu-id="d7c35-136">Před vytvořením plánů zaměstnaneckých výhod pro vaše zaměstnance musíte nakonfigurovat možnosti pro plány.</span><span class="sxs-lookup"><span data-stu-id="d7c35-136">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="d7c35-137">Nastavení parametrů správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-137">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="d7c35-138">Konfigurace možností a pravidel způsobilosti</span><span class="sxs-lookup"><span data-stu-id="d7c35-138">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="d7c35-139">Konfigurace možností způsobilosti osobních kontaktů</span><span class="sxs-lookup"><span data-stu-id="d7c35-139">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="d7c35-140">Vytvoření možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="d7c35-140">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="d7c35-141">Nastavení frekvencí platby</span><span class="sxs-lookup"><span data-stu-id="d7c35-141">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="d7c35-142">Konfigurace typů životních událostí</span><span class="sxs-lookup"><span data-stu-id="d7c35-142">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="d7c35-143">Vytvoření typů plánu</span><span class="sxs-lookup"><span data-stu-id="d7c35-143">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="d7c35-144">Nastavení kódů důvodů</span><span class="sxs-lookup"><span data-stu-id="d7c35-144">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="d7c35-145">Nastavení kódů úrovně</span><span class="sxs-lookup"><span data-stu-id="d7c35-145">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="d7c35-146">Konfigurace sazeb</span><span class="sxs-lookup"><span data-stu-id="d7c35-146">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="d7c35-147">Konfigurace srážek</span><span class="sxs-lookup"><span data-stu-id="d7c35-147">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="d7c35-148">Konfigurace dnů čekání</span><span class="sxs-lookup"><span data-stu-id="d7c35-148">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="d7c35-149">Konfigurace období čekání</span><span class="sxs-lookup"><span data-stu-id="d7c35-149">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="d7c35-150">Nastavení pravidel zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="d7c35-150">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="d7c35-151">Vytvoření kategorií zaměstnání</span><span class="sxs-lookup"><span data-stu-id="d7c35-151">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="d7c35-152">Nastavení typů zaměstnání</span><span class="sxs-lookup"><span data-stu-id="d7c35-152">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="d7c35-153">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="d7c35-153">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="d7c35-154">Vytvoření plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-154">Create benefit plans</span></span>

<span data-ttu-id="d7c35-155">Tyto články ukazují, jak vytvářet plány zaměstnaneckých výhod, včetně balíků a programů pro pružné kredity.</span><span class="sxs-lookup"><span data-stu-id="d7c35-155">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="d7c35-156">Nastavení plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-156">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="d7c35-157">Nastavení programů flexibilních kreditů</span><span class="sxs-lookup"><span data-stu-id="d7c35-157">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="d7c35-158">Zpracování plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="d7c35-158">Process benefit plans</span></span>

<span data-ttu-id="d7c35-159">Některé změny je nutné zpracovat, aby byly aktivní.</span><span class="sxs-lookup"><span data-stu-id="d7c35-159">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="d7c35-160">Zpracování způsobilosti k registraci</span><span class="sxs-lookup"><span data-stu-id="d7c35-160">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="d7c35-161">Zpracování životních událostí</span><span class="sxs-lookup"><span data-stu-id="d7c35-161">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="d7c35-162">Zpracování změn životních událostí</span><span class="sxs-lookup"><span data-stu-id="d7c35-162">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="d7c35-163">Zpracování způsobilosti k životním událostem</span><span class="sxs-lookup"><span data-stu-id="d7c35-163">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="d7c35-164">Zpracování změn sazby</span><span class="sxs-lookup"><span data-stu-id="d7c35-164">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

