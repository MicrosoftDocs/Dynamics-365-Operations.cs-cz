---
title: Nasazení nového klienta elektronického obchodu
description: V tomto tématu je popsán způsob nasazení nového webu elektronického obchodu Dynamics 365 Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b750ee89a85688dcebe673f9c3ff13693e9fcad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976731"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="d925f-103">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="d925f-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d925f-104">V tomto tématu je popsán způsob nasazení nového webu elektronického obchodu Dynamics 365 Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d925f-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="d925f-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d925f-105">Overview</span></span>

<span data-ttu-id="d925f-106">Microsoft Dynamics Lifecycle Services (LCS) je cloudový pracovní prostor vhodný pro spolupráci, který mohou partneři a zákazníci používat ke správě projektů a prostředí, zobrazování nejnovějších informací o produktech a funkcích Microsoft Dynamics a vytváření, sledování a procházení incidentů podpory.</span><span class="sxs-lookup"><span data-stu-id="d925f-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="d925f-107">Funkce správy elektronického obchodu jsou integrovány do LCS.</span><span class="sxs-lookup"><span data-stu-id="d925f-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="d925f-108">Další informace o LCS naleznete v části [Uživatelská příručka Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="d925f-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="d925f-109">Začínáme</span><span class="sxs-lookup"><span data-stu-id="d925f-109">Get started</span></span>

<span data-ttu-id="d925f-110">Před inicializací elektronického obchodu je nutné inicializovat projekt, prostředí a Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="d925f-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="d925f-111">Chcete-li provést inicializaci v LCS, musíte mít oprávnění role vlastníka projektu nebo správce prostředí.</span><span class="sxs-lookup"><span data-stu-id="d925f-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="d925f-112">Jsou podporovány topologie provozních a sandboxovýchprostředí.</span><span class="sxs-lookup"><span data-stu-id="d925f-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="d925f-113">Další informace o prostředích naleznete v části [Plánování prostředí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="d925f-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="d925f-114">Další informace o RCSU naleznete v tématu [Inicializace Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="d925f-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="d925f-115">Inicializace elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="d925f-115">Initialize e-commerce</span></span>

<span data-ttu-id="d925f-116">Pomocí tohoto postupu můžete inicializovat funkci elektronického obchodu v existujícím prostředí.</span><span class="sxs-lookup"><span data-stu-id="d925f-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="d925f-117">Než začnete, ujistěte se, zda jsou k dispozici následující požadované informace:</span><span class="sxs-lookup"><span data-stu-id="d925f-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="d925f-118">Použije se RCSU.</span><span class="sxs-lookup"><span data-stu-id="d925f-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="d925f-119">Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro systém správce systému elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="d925f-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="d925f-120">Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro moderátory hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="d925f-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="d925f-121">Domény, které budou přidruženy k prostředí.</span><span class="sxs-lookup"><span data-stu-id="d925f-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="d925f-122">Kromě toho můžete shromažďovat následující volitelné informace:</span><span class="sxs-lookup"><span data-stu-id="d925f-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="d925f-123">Informace o Azure AD B2C (business-to-consumer):</span><span class="sxs-lookup"><span data-stu-id="d925f-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="d925f-124">Název klienta.</span><span class="sxs-lookup"><span data-stu-id="d925f-124">Tenant Name.</span></span>
    - <span data-ttu-id="d925f-125">ID klienta.</span><span class="sxs-lookup"><span data-stu-id="d925f-125">Client ID.</span></span>
    - <span data-ttu-id="d925f-126">Vlastní doména přihlašování.</span><span class="sxs-lookup"><span data-stu-id="d925f-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="d925f-127">Adresa URL odpovědi.</span><span class="sxs-lookup"><span data-stu-id="d925f-127">Reply URL.</span></span>
    - <span data-ttu-id="d925f-128">ID zásady registrace a přihlášení.</span><span class="sxs-lookup"><span data-stu-id="d925f-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="d925f-129">ID zásady resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="d925f-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="d925f-130">ID zásady úpravy profilu.</span><span class="sxs-lookup"><span data-stu-id="d925f-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="d925f-131">Tyto informace lze přidat později prostřednictvím požadavku na službu.</span><span class="sxs-lookup"><span data-stu-id="d925f-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="d925f-132">Po shromáždění požadovaných informací proveďte následující kroky pro inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="d925f-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="d925f-133">Přihlaste se do [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="d925f-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="d925f-134">Otevřete projekt obsahující prostředí, ve kterém chcete provést inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="d925f-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="d925f-135">V části **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="d925f-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="d925f-136">V části **Funkce prostředí** vyberte odkaz **Řízení maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="d925f-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="d925f-137">Na kartě **Elektronické obchodování** vyberte možnost **Nastavení.**</span><span class="sxs-lookup"><span data-stu-id="d925f-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="d925f-138">Zobrazí se dialogové okno, v němž je nutné zadat informace, které jsou požadovány pro zřízení.</span><span class="sxs-lookup"><span data-stu-id="d925f-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="d925f-139">Vyplňte požadované informace a přejděte na další stránku.</span><span class="sxs-lookup"><span data-stu-id="d925f-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="d925f-140">Na další stránce vyplňte požadované informace a odešlete daný formulář.</span><span class="sxs-lookup"><span data-stu-id="d925f-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="d925f-141">Vrátíte se na kartu **Elektronické obchodování**, kde by se mělo zobrazit zahájení inicializace.</span><span class="sxs-lookup"><span data-stu-id="d925f-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="d925f-142">Chcete-li zobrazit stav inicializace, vyberte možnost **Aktualizovat** nebo se za chvíli vraťte na kartu **Elektronické obchodování**.</span><span class="sxs-lookup"><span data-stu-id="d925f-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="d925f-143">Při inicializaci elektronického obchodu z LCS systém zřizuje několik součástí, které jsou potřebné pro elektronický obchod a přidruží je k prostředí.</span><span class="sxs-lookup"><span data-stu-id="d925f-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="d925f-144">Po zřízení je karta **Elektronické obchodování** na stránce **Řízení maloobchodu** aktualizována tak, aby reagovala na zřízení.</span><span class="sxs-lookup"><span data-stu-id="d925f-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="d925f-145">Na stránce jsou zobrazena nejnovější nasazení vlastních nastavení a stav všech dalších probíhajících nasazení.</span><span class="sxs-lookup"><span data-stu-id="d925f-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="d925f-146">Obsahuje také odkazy na web elektronického obchodu a nástroj pro konfigurátor webu elektronického obchodu, kde se weby vytváří.</span><span class="sxs-lookup"><span data-stu-id="d925f-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="d925f-147">Přístup ke konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="d925f-147">Access Commerce site builder</span></span>

<span data-ttu-id="d925f-148">Chcete-li získat přístup k konfigurátoru webů Commerce, přejděte na kartu **Elektronické obchodování** na stránce **Řízení maloobchodu** v LCS a zvolte odkaz **Nástroj pro správu webu e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d925f-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="d925f-149">Cílová stránka konfigurátoru webu ukazuje zobrazení na úrovni klienta.</span><span class="sxs-lookup"><span data-stu-id="d925f-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="d925f-150">Z této stránky můžete:</span><span class="sxs-lookup"><span data-stu-id="d925f-150">From this page, you can:</span></span>

- <span data-ttu-id="d925f-151">Upravit nastavení na úrovni klienta.</span><span class="sxs-lookup"><span data-stu-id="d925f-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="d925f-152">Přejít na libovolný web, který jste vytvořili a k němuž máte oprávnění k zobrazení.</span><span class="sxs-lookup"><span data-stu-id="d925f-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="d925f-153">Získat přístup k funkcím,recenzí, jako je moderování a vykazování.</span><span class="sxs-lookup"><span data-stu-id="d925f-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="d925f-154">Vytvořit nový web.</span><span class="sxs-lookup"><span data-stu-id="d925f-154">Create a new site.</span></span> <span data-ttu-id="d925f-155">Další informace o tom, jak vytvářet nový web, naleznete v tématu [Vytvoření webu elektronického obchodování](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="d925f-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d925f-156">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d925f-156">Additional resources</span></span>

[<span data-ttu-id="d925f-157">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="d925f-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="d925f-158">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="d925f-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="d925f-159">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="d925f-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="d925f-160">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="d925f-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="d925f-161">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="d925f-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="d925f-162">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="d925f-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="d925f-163">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="d925f-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="d925f-164">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="d925f-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="d925f-165">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="d925f-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="d925f-166">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="d925f-166">Enable location-based store detection</span></span>](enable-store-detection.md)
