---
title: Přehled správy zaměstnaneckých výhod
description: Přehled předběžné verze funkce správy zaměstnaneckých výhod v Dynamics 365 Human Resources. Nabídněte svým zaměstnancům rozšířené možnosti zaměstnaneckých výhod pomocí snadno použitelného online prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029456"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="6ed0e-104">Přehled správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="6ed0e-105">Chcete-li si zachovat konkurenceschopnost, musíte nabídnout bohatý soubor zaměstnaneckých výhod, abyste přilákali a udrželi své nejlepší zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="6ed0e-106">Kromě standardních výhod, jako je pojištění zdravotní a zubní péče, můžete také nabízet rozšířené služby, např. pomoc s adopcí, rekreační programy a příspěvky na ošacení.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="6ed0e-107">Předběžná verze funkce správy zaměstnaneckých výhod ve službě Microsoft Dynamics 365 Human Resources poskytuje flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="6ed0e-108">Aplikace Human Resources také zahrnuje snadno použitelné zaměstnanecké prostředí, které prezentuje vaše nabídky.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="6ed0e-109">Vylepšené plány zaměstnaneckých výhod vám umožňují vytvářet a spravovat jedinečné plány zaměstnaneckých výhod a podporovat složité tabulky sazeb zaměstnaneckých výhod a vnořené úrovně.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="6ed0e-110">Můžete snadno vytvářet programy, balíky a pravidla automatického zařazení pro zaměstnanecké výhody k usnadnění použití zaměstnancem.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="6ed0e-111">Programy flexibilních kreditů umožňují rozdělit podporu mezi důchod a další životní události.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="6ed0e-112">Rozsáhlá pravidla způsobilosti zajišťují poskytnutí správných zaměstnaneckých výhod odpovídajícím zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="6ed0e-113">Online zařazení do zaměstnaneckých výhod poskytuje vašim zaměstnancům snadno použitelné prostředí.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="6ed0e-114">Kvalifikované zpracování životních událostí je integrováno se samoobslužnými funkcemi pro zaměstnance a také podporuje budoucí životní události.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="6ed0e-115">Chcete-li získat přístup k ukázkovým datům, musíte znovu nasadit izolované testovací prostředí (sandbox).</span><span class="sxs-lookup"><span data-stu-id="6ed0e-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="6ed0e-116">Můžete poskytnout přímou zpětnou vazbu nebo ohlásit problémy na adresu: D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="6ed0e-117">Známé problémy se správou zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="6ed0e-118">Zpracování posouzení nároku</span><span class="sxs-lookup"><span data-stu-id="6ed0e-118">Eligibility processing</span></span>

<span data-ttu-id="6ed0e-119">Při spuštění posouzení nároku na zaměstnanecké výhody, které využívají 1–5násobek platu, % platu a paušální částku krytí, musíte nastavit datum **Podrobnosti zaměstnaneckých výhod** na **Počáteční datum zaměstnance** v položce **Historie zaměstnání**.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="6ed0e-120">Musíte také zahrnout **Odpracované hodiny**, **Frekvence plateb** a **Roční výše zaměstnaneckých výhod dle platu**.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="6ed0e-121">Pokud pracovník dostává pevnou odměnu, zadejte možnost **Odpracované hodiny** a **Frekvence plateb**.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="6ed0e-122">Vypočítá se výše ročního platu.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="6ed0e-123">Dostává-li zaměstnanec plat, nemusíte zadávat údaj do pole **Odpracované hodiny**.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="6ed0e-124">Doporučujeme, abyste při vytváření nových pracovníků nejprve zadali fixní kompenzaci.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="6ed0e-125">Chcete-li aktualizovat záznam o podrobnostech zaměstnaneckých výhod, přejděte na stránku **Pracovník > Historie pracovníka > Podrobnosti o zaměstnání**.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="6ed0e-126">Upravte datum na počáteční datum pracovníka.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="6ed0e-127">Samoobsluha pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="6ed0e-127">Employee self-service</span></span>

<span data-ttu-id="6ed0e-128">Částka zaměstnance se při aktualizaci částky krytí pro životní pojištění nepočítá.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="6ed0e-129">Pokud je například zaměstnanci nabídnut plán životního pojištění, může vybrat až 50,000 USD v pokrytí při nákladech 0,36 USD na pokrytí 1 000 USD.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="6ed0e-130">Když zaměstnanec aktualizuje částku pokrytí, přiřazené náklady daného zaměstnance budou nulové.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="6ed0e-131">V případě plánu zaměstnaneckých výhod, který umožňuje pouze jeden výběr tohoto typu plánu, obdrží uživatel při pokusu o odpuštění plánu po výběru plánu chybu.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="6ed0e-132">Uživatel například vybere lékařský plán a umístí jej do svého nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="6ed0e-133">Uživatel poté vybere **Vzdát se** pro jiný lékařský plán.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="6ed0e-134">Uživateli se zobrazí chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="6ed0e-135">Povolení správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-135">Enable Benefits management</span></span>

<span data-ttu-id="6ed0e-136">Správa zaměstnaneckých výhod je předběžná verze služby, která je dostupná pouze v **izolovaných testovacích prostředích (sandbox)**.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="6ed0e-137">Tyto články popisují způsob, jakým lze zapnout předběžné verze funkcí v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="6ed0e-138">Také sdělují, které existující funkce v aplikaci Human Resources správa zaměstnaneckých výhod nahradí nebo jsou zakázány po zapnutí správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="6ed0e-139">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="6ed0e-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="6ed0e-140">Předběžná verze funkce: Správa zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="6ed0e-141">Konfigurace správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-141">Configure Benefits management</span></span>

<span data-ttu-id="6ed0e-142">Před vytvořením plánů zaměstnaneckých výhod pro vaše zaměstnance musíte nakonfigurovat možnosti pro plány.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="6ed0e-143">Nastavení parametrů správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="6ed0e-144">Konfigurace možností a pravidel způsobilosti</span><span class="sxs-lookup"><span data-stu-id="6ed0e-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="6ed0e-145">Konfigurace možností způsobilosti osobních kontaktů</span><span class="sxs-lookup"><span data-stu-id="6ed0e-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="6ed0e-146">Vytvoření možností krytí</span><span class="sxs-lookup"><span data-stu-id="6ed0e-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="6ed0e-147">Nastavení frekvencí platby</span><span class="sxs-lookup"><span data-stu-id="6ed0e-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="6ed0e-148">Konfigurace typů životních událostí</span><span class="sxs-lookup"><span data-stu-id="6ed0e-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="6ed0e-149">Vytvoření typů plánu</span><span class="sxs-lookup"><span data-stu-id="6ed0e-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="6ed0e-150">Nastavení kódů důvodů</span><span class="sxs-lookup"><span data-stu-id="6ed0e-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="6ed0e-151">Nastavení kódů úrovně</span><span class="sxs-lookup"><span data-stu-id="6ed0e-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="6ed0e-152">Konfigurace sazeb</span><span class="sxs-lookup"><span data-stu-id="6ed0e-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="6ed0e-153">Konfigurace srážek</span><span class="sxs-lookup"><span data-stu-id="6ed0e-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="6ed0e-154">Konfigurace dnů čekání</span><span class="sxs-lookup"><span data-stu-id="6ed0e-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="6ed0e-155">Konfigurace období čekání</span><span class="sxs-lookup"><span data-stu-id="6ed0e-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="6ed0e-156">Nastavení pravidel zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="6ed0e-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="6ed0e-157">Vytvoření kategorií zaměstnání</span><span class="sxs-lookup"><span data-stu-id="6ed0e-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="6ed0e-158">Nastavení typů zaměstnání</span><span class="sxs-lookup"><span data-stu-id="6ed0e-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="6ed0e-159">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="6ed0e-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="6ed0e-160">Vytvoření plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-160">Create benefit plans</span></span>

<span data-ttu-id="6ed0e-161">Tyto články ukazují, jak vytvářet plány zaměstnaneckých výhod, včetně balíků a programů pro pružné kredity.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="6ed0e-162">Nastavení plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="6ed0e-163">Vytvoření plánů zaměstnaneckých výhod pracovníka</span><span class="sxs-lookup"><span data-stu-id="6ed0e-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="6ed0e-164">Nastavení programů flexibilních kreditů</span><span class="sxs-lookup"><span data-stu-id="6ed0e-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="6ed0e-165">Konfigurace budoucích životních událostí</span><span class="sxs-lookup"><span data-stu-id="6ed0e-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="6ed0e-166">Zpracování plánů zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6ed0e-166">Process benefit plans</span></span>

<span data-ttu-id="6ed0e-167">Některé změny je nutné zpracovat, aby byly aktivní.</span><span class="sxs-lookup"><span data-stu-id="6ed0e-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="6ed0e-168">Zpracování způsobilosti k registraci</span><span class="sxs-lookup"><span data-stu-id="6ed0e-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="6ed0e-169">Zpracování životních událostí</span><span class="sxs-lookup"><span data-stu-id="6ed0e-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="6ed0e-170">Zpracování změn životních událostí</span><span class="sxs-lookup"><span data-stu-id="6ed0e-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="6ed0e-171">Zpracování způsobilosti k životním událostem</span><span class="sxs-lookup"><span data-stu-id="6ed0e-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="6ed0e-172">Zpracování změn sazby</span><span class="sxs-lookup"><span data-stu-id="6ed0e-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

