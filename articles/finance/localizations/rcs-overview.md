---
title: Regulatory Configuration Service
description: Toto téma poskytuje přehled schopností Regulatory Configuration Service (RCS) a vysvětluje, jak ke službě přistupovat.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
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
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890793"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="b5784-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="b5784-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5784-104">Regulatory Configuration Service (RCS) je samostatná služba návrhu a správy životního cyklu pro funkce globalizace bez kódování / s malým množstvím kódování.</span><span class="sxs-lookup"><span data-stu-id="b5784-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="b5784-105">RCS umožňuje zúčastněným stranám globalizace rozšířit a přizpůsobit klíčové oblasti globalizace v oblasti daní, elektronické fakturace, regulačních zpráv, bankovnictví a obchodních dokumentů, aniž by bylo nutné zapojovat vývojáře.</span><span class="sxs-lookup"><span data-stu-id="b5784-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="b5784-106">Tento globalizační přístup bez kódování / s malým množstvím kódování umožňuje globalizaci snazší, rychlejší a nákladově efektivnější při vytváření nebo rozšiřování.</span><span class="sxs-lookup"><span data-stu-id="b5784-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="b5784-107">RCS poskytuje následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="b5784-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="b5784-108">Podpora všech funkcí, které poskytuje elektronické výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="b5784-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="b5784-109">Předpoklad ke konfiguraci nových globálních mikroslužeb.</span><span class="sxs-lookup"><span data-stu-id="b5784-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="b5784-110">Podpora elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="b5784-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="b5784-111">Další informace získáte v tématu [Elektronická fakturace](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="b5784-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="b5784-112">Podporuje výpočet daně.</span><span class="sxs-lookup"><span data-stu-id="b5784-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="b5784-113">Další informace naleznete v tématu [Daňová služba](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="b5784-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="b5784-114">Podpora nových funkcí globalizačních funkcí, která zjednodušuje správu životního cyklu vícekomponentních funkcí a poskytuje další možnosti konfigurace akcí a nastavení parametrů funkcí.</span><span class="sxs-lookup"><span data-stu-id="b5784-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="b5784-115">Další informace viz [Regulatory Configuration Service – zjednodušená správa funkcí globalizace pro globalizační služby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="b5784-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="b5784-116">Podpora centralizovaného publikování, ukládání a sdílení vlastních konfigurací v globálním úložišti pro zjednodušení správy konfigurace bez nutnosti použití Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b5784-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="b5784-117">Přístup k RCS</span><span class="sxs-lookup"><span data-stu-id="b5784-117">Access RCS</span></span>

<span data-ttu-id="b5784-118">Můžete se zaregistrovat nebo přihlásit do RCS ze [stránky Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="b5784-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Registrace/přihlášení k RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="b5784-120">Na stránce **Regulatory Configuration Service** zkontrolujte a přijměte doplňkové podmínky pro používání služby a poté vyberte jedno z následujících tlačítek:</span><span class="sxs-lookup"><span data-stu-id="b5784-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="b5784-121">**Zaregistrovat se**, pokud službu používáte poprvé a používáte pracovní e-mailovou adresu k zajištění prostředí služby vaší organizaci</span><span class="sxs-lookup"><span data-stu-id="b5784-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="b5784-122">**Přihlásit se**, pokud jste se již do služby zaregistrovali a chcete přistupovat k prostředí vaší organizace</span><span class="sxs-lookup"><span data-stu-id="b5784-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="b5784-123">Regionální dostupnost</span><span class="sxs-lookup"><span data-stu-id="b5784-123">Regional availability</span></span>

<span data-ttu-id="b5784-124">RCS je obecně k dispozici v následujících oblastech:</span><span class="sxs-lookup"><span data-stu-id="b5784-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="b5784-125">Spojené státy americké</span><span class="sxs-lookup"><span data-stu-id="b5784-125">United States</span></span>
- <span data-ttu-id="b5784-126">Indie</span><span class="sxs-lookup"><span data-stu-id="b5784-126">India</span></span>
- <span data-ttu-id="b5784-127">Francie</span><span class="sxs-lookup"><span data-stu-id="b5784-127">France</span></span>
- <span data-ttu-id="b5784-128">Evropa</span><span class="sxs-lookup"><span data-stu-id="b5784-128">Europe</span></span>

<span data-ttu-id="b5784-129">Úplný seznam oblastí najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="b5784-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="b5784-130">Související dokumentace RCS</span><span class="sxs-lookup"><span data-stu-id="b5784-130">Related RCS documentation</span></span>

<span data-ttu-id="b5784-131">Další informace o souvisejících komponentech naleznete v následující dokumentaci:</span><span class="sxs-lookup"><span data-stu-id="b5784-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="b5784-132">**Globální úložiště:**</span><span class="sxs-lookup"><span data-stu-id="b5784-132">**Global repository:**</span></span>

    - [<span data-ttu-id="b5784-133">Vytvoření konfigurace ER a nahrání do globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="b5784-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="b5784-134">Sdílení konfigurace v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="b5784-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="b5784-135">Rozšířené filtrování v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="b5784-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="b5784-136">Stažení konfigurací elektronického výkaznictví z globálního úložiště</span><span class="sxs-lookup"><span data-stu-id="b5784-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="b5784-137">Ukončení konfigurací v globálním úložišti</span><span class="sxs-lookup"><span data-stu-id="b5784-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="b5784-138">**Globalizační funkce:**</span><span class="sxs-lookup"><span data-stu-id="b5784-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="b5784-139">Regulatory Configuration Service (RCS) – Globalizační funkce</span><span class="sxs-lookup"><span data-stu-id="b5784-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)