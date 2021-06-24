---
title: Regulatory Configuration Service
description: Toto téma poskytuje přehled schopností Regulatory Configuration Service (RCS) a vysvětluje, jak ke službě přistupovat.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216555"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="2f2fb-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="2f2fb-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f2fb-104">Regulatory Configuration Service (RCS) je samostatná služba návrhu a správy životního cyklu pro funkce globalizace bez kódování / s malým množstvím kódování.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="2f2fb-105">RCS umožňuje zúčastněným stranám globalizace rozšířit a přizpůsobit klíčové oblasti globalizace v oblasti daní, elektronické fakturace, regulačních zpráv, bankovnictví a obchodních dokumentů, aniž by bylo nutné zapojovat vývojáře.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="2f2fb-106">Tento globalizační přístup bez kódování / s malým množstvím kódování umožňuje globalizaci snazší, rychlejší a nákladově efektivnější při vytváření nebo rozšiřování.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="2f2fb-107">RCS poskytuje následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="2f2fb-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="2f2fb-108">Podpora všech funkcí, které poskytuje elektronické výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="2f2fb-109">Předpoklad ke konfiguraci nových globálních mikroslužeb.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="2f2fb-110">Podpora elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="2f2fb-111">Další informace získáte v tématu [Elektronická fakturace](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="2f2fb-112">Podporuje výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="2f2fb-113">Další informace naleznete v tématu [Daňová služba](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="2f2fb-114">Podpora nových funkcí globalizačních funkcí, která zjednodušuje správu životního cyklu vícekomponentních funkcí a poskytuje další možnosti konfigurace akcí a nastavení parametrů funkcí.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="2f2fb-115">Další informace viz [Regulatory Configuration Service – zjednodušená správa funkcí globalizace pro globalizační služby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="2f2fb-116">Podpora centralizovaného publikování, ukládání a sdílení vlastních konfigurací v globálním úložišti pro zjednodušení správy konfigurace bez nutnosti použití Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="2f2fb-117">Přístup k RCS</span><span class="sxs-lookup"><span data-stu-id="2f2fb-117">Access RCS</span></span>

<span data-ttu-id="2f2fb-118">Můžete se zaregistrovat nebo přihlásit do RCS ze [stránky Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Registrace/přihlášení k RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="2f2fb-120">Na stránce **Regulatory Configuration Service** zkontrolujte a přijměte doplňkové podmínky pro používání služby a poté vyberte jedno z následujících tlačítek:</span><span class="sxs-lookup"><span data-stu-id="2f2fb-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="2f2fb-121">**Zaregistrovat se**, pokud službu používáte poprvé a používáte pracovní e-mailovou adresu k zajištění prostředí služby vaší organizaci</span><span class="sxs-lookup"><span data-stu-id="2f2fb-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="2f2fb-122">**Přihlásit se**, pokud jste se již do služby zaregistrovali a chcete přistupovat k prostředí vaší organizace</span><span class="sxs-lookup"><span data-stu-id="2f2fb-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="2f2fb-123">Regionální dostupnost</span><span class="sxs-lookup"><span data-stu-id="2f2fb-123">Regional availability</span></span>

<span data-ttu-id="2f2fb-124">RCS je obecně k dispozici v následujících oblastech:</span><span class="sxs-lookup"><span data-stu-id="2f2fb-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="2f2fb-125">Spojené státy americké</span><span class="sxs-lookup"><span data-stu-id="2f2fb-125">United States</span></span>
- <span data-ttu-id="2f2fb-126">Indie</span><span class="sxs-lookup"><span data-stu-id="2f2fb-126">India</span></span>
- <span data-ttu-id="2f2fb-127">Francie</span><span class="sxs-lookup"><span data-stu-id="2f2fb-127">France</span></span>
- <span data-ttu-id="2f2fb-128">Evropa</span><span class="sxs-lookup"><span data-stu-id="2f2fb-128">Europe</span></span>

<span data-ttu-id="2f2fb-129">Úplný seznam oblastí najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="2f2fb-130">Výchozí společnost RCS</span><span class="sxs-lookup"><span data-stu-id="2f2fb-130">RCS default company</span></span>

<span data-ttu-id="2f2fb-131">Funkce doby návrhu, která se používá v RCS, je sdílena všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="2f2fb-132">Neexistuje žádná funkce specifická pro jednu společnost.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-132">There is no company-specific functionality.</span></span> <span data-ttu-id="2f2fb-133">Proto doporučujeme ve vašem prostředí RCS použít jednu společnost **DAT**.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="2f2fb-134">V některých scénářích však možná budete chtít, aby formáty ER používaly parametry, které souvisejí s konkrétním právním subjektem.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="2f2fb-135">Pouze v těchto scénářích byste měli použít výchozí přepínač společnosti.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="2f2fb-136">Ukázku najdete v tématu [Konfigurace formátů elektronického výkaznictví pro použití parametrů zadaných pro právnickou osobu](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="2f2fb-137">Související dokumentace RCS</span><span class="sxs-lookup"><span data-stu-id="2f2fb-137">Related RCS documentation</span></span>

<span data-ttu-id="2f2fb-138">Další informace o souvisejících součástech naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="2f2fb-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="2f2fb-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="2f2fb-139">**RCS:**</span></span>

    - [<span data-ttu-id="2f2fb-140">Vytvoření konfigurací elektronického výkaznictví v RCS a jejich odeslání do globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="2f2fb-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="2f2fb-141">**Globální úložiště:**</span><span class="sxs-lookup"><span data-stu-id="2f2fb-141">**Global repository:**</span></span>

    - [<span data-ttu-id="2f2fb-142">Vytvoření konfigurace ER a nahrání do globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="2f2fb-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="2f2fb-143">Sdílení konfigurace v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="2f2fb-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="2f2fb-144">Rozšířené filtrování v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="2f2fb-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="2f2fb-145">Stažení konfigurací elektronického výkaznictví z globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="2f2fb-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="2f2fb-146">Ukončení konfigurací v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="2f2fb-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="2f2fb-147">Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2f2fb-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="2f2fb-148">**Globalizační funkce:**</span><span class="sxs-lookup"><span data-stu-id="2f2fb-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="2f2fb-149">Regulatory Configuration Service (RCS) – Globalizační funkce</span><span class="sxs-lookup"><span data-stu-id="2f2fb-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="2f2fb-150">Řešení potíží s přihlášením do RCS</span><span class="sxs-lookup"><span data-stu-id="2f2fb-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="2f2fb-151">Při registraci do RCS ze stránky služby se můžete setkat s problémem, který souvisí se službou Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="2f2fb-152">Chybová zpráva, která se zobrazí, naznačuje, že registrace do RCS je aktuálně vypnutá a je nutné ji zapnout, abyste mohli dokončit proces registrace.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![Chybová zpráva registrace RCS](media/01_RCSSignUpError.jpg)

<span data-ttu-id="2f2fb-154">K problému dochází, protože nemáte povoleno přihlášení k odběru ad hoc předplatných a ve vašem klientu musí být zapnuta vlastnost `AllowAdHocSubscriptions`.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="2f2fb-155">Pokud vaše IT oddělení spravuje klienty Azure vaší organizace, kontaktujte toto oddělení a nahlaste problém.</span><span class="sxs-lookup"><span data-stu-id="2f2fb-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="2f2fb-156">Pokud jste zodpovědní za správu svých klientů Azure, můžete problémy vyřešit podle pokynů v článku [K čemu je samoobslužná registrace Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="2f2fb-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
