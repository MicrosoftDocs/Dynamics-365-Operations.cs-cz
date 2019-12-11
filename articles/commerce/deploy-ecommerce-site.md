---
title: Nasazení nového klienta elektronického obchodu
description: V tomto tématu je popsán způsob nasazení nového klienta elektronického obchodu pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697444"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="77ef6-103">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="77ef6-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="77ef6-104">V tomto tématu je popsán způsob nasazení nového webu elektronického obchodu pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="77ef6-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="77ef6-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="77ef6-105">Overview</span></span>
    
<span data-ttu-id="77ef6-106">Microsoft Dynamics Lifecycle Services (LCS) je cloudový pracovní prostor vhodný pro spolupráci, který mohou partneři a zákazníci používat ke správě projektů a prostředí, zobrazování nejnovějších informací o produktech a funkcích Microsoft Dynamics a vytváření, sledování a procházení incidentů podpory.</span><span class="sxs-lookup"><span data-stu-id="77ef6-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="77ef6-107">Funkce správy elektronického obchodu jsou integrovány do LCS.</span><span class="sxs-lookup"><span data-stu-id="77ef6-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="77ef6-108">Další informace o LCS naleznete v části [Uživatelská příručka Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="77ef6-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="77ef6-109">Začínáme</span><span class="sxs-lookup"><span data-stu-id="77ef6-109">Get started</span></span>

<span data-ttu-id="77ef6-110">Před inicializací elektronického obchodu je nutné inicializovat projekt, prostředí a Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="77ef6-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="77ef6-111">Chcete-li provést inicializaci v LCS, musíte mít oprávnění role vlastníka projektu nebo správce prostředí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="77ef6-112">Jsou podporovány topologie provozních a sandboxovýchprostředí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="77ef6-113">Další informace o prostředích naleznete v části [Plánování prostředí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="77ef6-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="77ef6-114">Další informace o RCSU naleznete v tématu [Inicializace Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="77ef6-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="77ef6-115">Inicializace elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="77ef6-115">Initialize e-Commerce</span></span>

<span data-ttu-id="77ef6-116">Pomocí tohoto postupu můžete inicializovat funkci elektronického obchodu v existujícím prostředí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="77ef6-117">Než začnete, ujistěte se, zda jsou k dispozici následující požadované informace:</span><span class="sxs-lookup"><span data-stu-id="77ef6-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="77ef6-118">Použije se RCSU.</span><span class="sxs-lookup"><span data-stu-id="77ef6-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="77ef6-119">Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro systém správce systému elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="77ef6-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="77ef6-120">Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro moderátory hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="77ef6-121">Domény, které budou přidruženy k prostředí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="77ef6-122">Kromě toho můžete shromažďovat následující volitelné informace:</span><span class="sxs-lookup"><span data-stu-id="77ef6-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="77ef6-123">Informace o Azure AD B2C (business-to-consumer):</span><span class="sxs-lookup"><span data-stu-id="77ef6-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="77ef6-124">Název klienta.</span><span class="sxs-lookup"><span data-stu-id="77ef6-124">Tenant Name.</span></span>
    - <span data-ttu-id="77ef6-125">ID klienta.</span><span class="sxs-lookup"><span data-stu-id="77ef6-125">Client ID.</span></span>
    - <span data-ttu-id="77ef6-126">Vlastní doména přihlašování.</span><span class="sxs-lookup"><span data-stu-id="77ef6-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="77ef6-127">Adresa URL odpovědi.</span><span class="sxs-lookup"><span data-stu-id="77ef6-127">Reply URL.</span></span>
    - <span data-ttu-id="77ef6-128">ID zásady registrace a přihlášení.</span><span class="sxs-lookup"><span data-stu-id="77ef6-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="77ef6-129">ID zásady resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="77ef6-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="77ef6-130">ID zásady úpravy profilu.</span><span class="sxs-lookup"><span data-stu-id="77ef6-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="77ef6-131">Tyto informace lze přidat později prostřednictvím požadavku na službu.</span><span class="sxs-lookup"><span data-stu-id="77ef6-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="77ef6-132">Po shromáždění požadovaných informací proveďte následující kroky pro inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="77ef6-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="77ef6-133">Přihlaste se do [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="77ef6-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="77ef6-134">Otevřete projekt obsahující prostředí, ve kterém chcete provést inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="77ef6-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="77ef6-135">V části **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="77ef6-136">V části **Funkce prostředí** vyberte odkaz **Řízení maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="77ef6-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="77ef6-137">Na kartě **Elektronické obchodování** vyberte možnost **Nastavení.**</span><span class="sxs-lookup"><span data-stu-id="77ef6-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="77ef6-138">Zobrazí se dialogové okno, v němž je nutné zadat informace, které jsou požadovány pro zřízení.</span><span class="sxs-lookup"><span data-stu-id="77ef6-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="77ef6-139">Vyplňte požadované informace a přejděte na další stránku.</span><span class="sxs-lookup"><span data-stu-id="77ef6-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="77ef6-140">Na další stránce vyplňte požadované informace a odešlete daný formulář.</span><span class="sxs-lookup"><span data-stu-id="77ef6-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="77ef6-141">Vrátíte se na kartu **Elektronické obchodování**, kde by se mělo zobrazit zahájení inicializace.</span><span class="sxs-lookup"><span data-stu-id="77ef6-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="77ef6-142">Chcete-li zobrazit stav inicializace, vyberte možnost **Aktualizovat** nebo se za chvíli vraťte na kartu **Elektronické obchodování**.</span><span class="sxs-lookup"><span data-stu-id="77ef6-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="77ef6-143">Při inicializaci elektronického obchodu z LCS systém zřizuje několik součástí, které jsou potřebné pro elektronický obchod a přidruží je k prostředí.</span><span class="sxs-lookup"><span data-stu-id="77ef6-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="77ef6-144">Po zřízení je karta **Elektronické obchodování** na stránce **Řízení maloobchodu** aktualizována tak, aby reagovala na zřízení.</span><span class="sxs-lookup"><span data-stu-id="77ef6-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="77ef6-145">Na stránce jsou zobrazena nejnovější nasazení vlastních nastavení a stav všech dalších probíhajících nasazení.</span><span class="sxs-lookup"><span data-stu-id="77ef6-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="77ef6-146">Obsahuje také odkazy na web elektronického obchodu a nástroj pro správu webu elektronického obchodu (nástroj pro vytváření obsahu).</span><span class="sxs-lookup"><span data-stu-id="77ef6-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="77ef6-147">Přístup do vývojového prostředí</span><span class="sxs-lookup"><span data-stu-id="77ef6-147">Access the authoring environment</span></span>

<span data-ttu-id="77ef6-148">Chcete-li získat přístup do vývojového prostředí , přejděte na kartu **Elektronické obchodování** na stránce **Řízení maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="77ef6-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="77ef6-149">Naleznete zde odkazy na web elektronického obchodu a nástroj pro správu webu.</span><span class="sxs-lookup"><span data-stu-id="77ef6-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77ef6-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="77ef6-150">Additional resources</span></span>

[<span data-ttu-id="77ef6-151">Přehled online obchodu</span><span class="sxs-lookup"><span data-stu-id="77ef6-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="77ef6-152">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="77ef6-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="77ef6-153">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="77ef6-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="77ef6-154">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="77ef6-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="77ef6-155">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="77ef6-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="77ef6-156">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="77ef6-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="77ef6-157">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="77ef6-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
