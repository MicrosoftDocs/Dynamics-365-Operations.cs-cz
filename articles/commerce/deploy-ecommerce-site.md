---
title: Nasazení nového klienta elektronického obchodu
description: V tomto tématu je popsán způsob nasazení nového webu elektronického obchodu Dynamics 365 Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0fff5d47d6eb3e08288d17853fcd94f9eab843c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801942"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="f082c-103">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="f082c-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f082c-104">V tomto tématu je popsán způsob nasazení nového webu elektronického obchodu Dynamics 365 Commerce pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f082c-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="f082c-105">Microsoft Dynamics Lifecycle Services (LCS) je cloudový pracovní prostor vhodný pro spolupráci, který mohou partneři a zákazníci používat ke správě projektů a prostředí, zobrazování nejnovějších informací o produktech a funkcích Microsoft Dynamics a vytváření, sledování a procházení incidentů podpory.</span><span class="sxs-lookup"><span data-stu-id="f082c-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="f082c-106">Funkce správy elektronického obchodu jsou integrovány do LCS.</span><span class="sxs-lookup"><span data-stu-id="f082c-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="f082c-107">Další informace o LCS naleznete v části [Uživatelská příručka Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="f082c-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="f082c-108">Začínáme</span><span class="sxs-lookup"><span data-stu-id="f082c-108">Get started</span></span>

<span data-ttu-id="f082c-109">Před inicializací elektronického obchodu je nutné inicializovat projekt, prostředí a Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="f082c-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="f082c-110">Chcete-li provést inicializaci v LCS, musíte mít oprávnění role vlastníka projektu nebo správce prostředí.</span><span class="sxs-lookup"><span data-stu-id="f082c-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="f082c-111">Jsou podporovány topologie provozních a sandboxovýchprostředí.</span><span class="sxs-lookup"><span data-stu-id="f082c-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="f082c-112">Další informace o prostředích naleznete v části [Plánování prostředí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="f082c-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="f082c-113">Další informace o RCSU naleznete v tématu [Inicializace Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="f082c-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="f082c-114">Inicializace elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="f082c-114">Initialize e-commerce</span></span>

<span data-ttu-id="f082c-115">Pomocí tohoto postupu můžete inicializovat funkci elektronického obchodu v existujícím prostředí.</span><span class="sxs-lookup"><span data-stu-id="f082c-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="f082c-116">Než začnete, ujistěte se, zda jsou k dispozici následující požadované informace:</span><span class="sxs-lookup"><span data-stu-id="f082c-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="f082c-117">Použije se RCSU.</span><span class="sxs-lookup"><span data-stu-id="f082c-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="f082c-118">Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro systém správce systému elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="f082c-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="f082c-119">Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro moderátory hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="f082c-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="f082c-120">Domény, které budou přidruženy k prostředí.</span><span class="sxs-lookup"><span data-stu-id="f082c-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="f082c-121">Kromě toho můžete shromažďovat následující volitelné informace:</span><span class="sxs-lookup"><span data-stu-id="f082c-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="f082c-122">Informace o Azure AD B2C (business-to-consumer):</span><span class="sxs-lookup"><span data-stu-id="f082c-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="f082c-123">Název klienta.</span><span class="sxs-lookup"><span data-stu-id="f082c-123">Tenant Name.</span></span>
    - <span data-ttu-id="f082c-124">ID klienta.</span><span class="sxs-lookup"><span data-stu-id="f082c-124">Client ID.</span></span>
    - <span data-ttu-id="f082c-125">Vlastní doména přihlašování.</span><span class="sxs-lookup"><span data-stu-id="f082c-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="f082c-126">Adresa URL odpovědi.</span><span class="sxs-lookup"><span data-stu-id="f082c-126">Reply URL.</span></span>
    - <span data-ttu-id="f082c-127">ID zásady registrace a přihlášení.</span><span class="sxs-lookup"><span data-stu-id="f082c-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="f082c-128">ID zásady resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="f082c-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="f082c-129">ID zásady úpravy profilu.</span><span class="sxs-lookup"><span data-stu-id="f082c-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="f082c-130">Tyto informace lze přidat později prostřednictvím požadavku na službu.</span><span class="sxs-lookup"><span data-stu-id="f082c-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="f082c-131">Po shromáždění požadovaných informací proveďte následující kroky pro inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="f082c-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="f082c-132">Přihlaste se do [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="f082c-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="f082c-133">Otevřete projekt obsahující prostředí, ve kterém chcete provést inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="f082c-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="f082c-134">V části **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="f082c-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="f082c-135">V části **Funkce prostředí** vyberte odkaz **Řízení maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="f082c-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="f082c-136">Na kartě **Elektronické obchodování** vyberte možnost **Nastavení.**</span><span class="sxs-lookup"><span data-stu-id="f082c-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="f082c-137">Zobrazí se dialogové okno, v němž je nutné zadat informace, které jsou požadovány pro zřízení.</span><span class="sxs-lookup"><span data-stu-id="f082c-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="f082c-138">Vyplňte požadované informace a přejděte na další stránku.</span><span class="sxs-lookup"><span data-stu-id="f082c-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="f082c-139">Na další stránce vyplňte požadované informace a odešlete daný formulář.</span><span class="sxs-lookup"><span data-stu-id="f082c-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="f082c-140">Vrátíte se na kartu **Elektronické obchodování**, kde by se mělo zobrazit zahájení inicializace.</span><span class="sxs-lookup"><span data-stu-id="f082c-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="f082c-141">Chcete-li zobrazit stav inicializace, vyberte možnost **Aktualizovat** nebo se za chvíli vraťte na kartu **Elektronické obchodování**.</span><span class="sxs-lookup"><span data-stu-id="f082c-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="f082c-142">Při inicializaci elektronického obchodu z LCS systém zřizuje několik součástí, které jsou potřebné pro elektronický obchod a přidruží je k prostředí.</span><span class="sxs-lookup"><span data-stu-id="f082c-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="f082c-143">Po zřízení je karta **Elektronické obchodování** na stránce **Řízení maloobchodu** aktualizována tak, aby reagovala na zřízení.</span><span class="sxs-lookup"><span data-stu-id="f082c-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="f082c-144">Na stránce jsou zobrazena nejnovější nasazení vlastních nastavení a stav všech dalších probíhajících nasazení.</span><span class="sxs-lookup"><span data-stu-id="f082c-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="f082c-145">Obsahuje také odkazy na web elektronického obchodu a nástroj pro konfigurátor webu elektronického obchodu, kde se weby vytváří.</span><span class="sxs-lookup"><span data-stu-id="f082c-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="f082c-146">Přístup ke konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="f082c-146">Access Commerce site builder</span></span>

<span data-ttu-id="f082c-147">Chcete-li získat přístup k konfigurátoru webů Commerce, přejděte na kartu **Elektronické obchodování** na stránce **Řízení maloobchodu** v LCS a zvolte odkaz **Nástroj pro správu webu e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f082c-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="f082c-148">Cílová stránka konfigurátoru webu ukazuje zobrazení na úrovni klienta.</span><span class="sxs-lookup"><span data-stu-id="f082c-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="f082c-149">Z této stránky můžete:</span><span class="sxs-lookup"><span data-stu-id="f082c-149">From this page, you can:</span></span>

- <span data-ttu-id="f082c-150">Upravit nastavení na úrovni klienta.</span><span class="sxs-lookup"><span data-stu-id="f082c-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="f082c-151">Přejít na libovolný web, který jste vytvořili a k němuž máte oprávnění k zobrazení.</span><span class="sxs-lookup"><span data-stu-id="f082c-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="f082c-152">Získat přístup k funkcím,recenzí, jako je moderování a vykazování.</span><span class="sxs-lookup"><span data-stu-id="f082c-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="f082c-153">Vytvořit nový web.</span><span class="sxs-lookup"><span data-stu-id="f082c-153">Create a new site.</span></span> <span data-ttu-id="f082c-154">Další informace o tom, jak vytvářet nový web, naleznete v tématu [Vytvoření webu elektronického obchodování](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="f082c-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f082c-155">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f082c-155">Additional resources</span></span>

[<span data-ttu-id="f082c-156">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="f082c-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f082c-157">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="f082c-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f082c-158">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="f082c-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f082c-159">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="f082c-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f082c-160">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="f082c-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f082c-161">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="f082c-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f082c-162">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="f082c-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f082c-163">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="f082c-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f082c-164">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="f082c-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f082c-165">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="f082c-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
