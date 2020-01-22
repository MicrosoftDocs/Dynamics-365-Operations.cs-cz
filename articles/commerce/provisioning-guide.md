---
title: Zřizování ukázkového prostředí služby Commerce
description: Toto téma vysvětluje, jak zřídit ukázkové prostředí v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934741"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="2bcaa-103">Zřizování ukázkového prostředí služby Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2bcaa-104">Toto téma vysvětluje, jak zřídit ukázkové prostředí v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="2bcaa-105">Než začnete, doporučujeme, abyste celé téma alespoň zběžně pročetli, abyste získali představu o tom, co proces obnáší a co téma obsahuje.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="2bcaa-106">Pokud ještě nemáte přístup k náhledu Dynamics 365 Commerce, můžete požádat o přístup k náhledu z [webu Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="2bcaa-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="2bcaa-107">Overview</span></span>

<span data-ttu-id="2bcaa-108">Chcete-li úspěšně zřídit prostředí pro náhled Commerce, musíte vytvořit projekt, který má specifický název a typ produktu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="2bcaa-109">Prostředí a Retail Cloud Scale Unit (RCSU) také mají některé specifické parametry, které musíte použít ke zřizování e-Commerce později.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="2bcaa-110">Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="2bcaa-111">Po úspěšném zřízení ukázkového prostředí Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="2bcaa-112">Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="2bcaa-113">Volitelné kroky můžete vždy dokončit později.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="2bcaa-114">Informace o konfiguraci prostředí pro náhled Commerce po jeho vytvoření najdete v části [konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="2bcaa-115">Informace o konfiguraci volitelných funkcí prostředí pro náhled Commerce najdete v části [konfigurace volitelných funkcí prostředí pro náhled Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="2bcaa-116">Pokud máte dotazy týkající se kroků zřizování nebo pokud se vyskytnou nějaké problémy, sdělte je společnosti Microsoft na [Microsoft Dynamics 365 Commerce, skupina náhledu Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2bcaa-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="2bcaa-117">Prerequisites</span></span>

<span data-ttu-id="2bcaa-118">Aby bylo možné zřídit prostředí pro náhled Commerce, musí být zavedeny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="2bcaa-119">Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="2bcaa-120">Byli jste přijati do programu náhledu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="2bcaa-121">Máte požadovaná oprávnění k vytvoření projektu pro **potenciální předprodej** nebo **migraci, vytvoření řešení a další informace**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="2bcaa-122">Máte roli **Správce prostředí** nebo **Vlastník projektu** v projektu, kde se chystáte zřídit prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="2bcaa-123">Máte přístup pro správu ke svému předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který může provést dva kroky, které pro vás vyžadují oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="2bcaa-124">Máte k dispozici ID klienta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="2bcaa-125">Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="2bcaa-126">Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="2bcaa-127">(Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)</span><span class="sxs-lookup"><span data-stu-id="2bcaa-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="2bcaa-128">Najděte ID klienta Azure AD</span><span class="sxs-lookup"><span data-stu-id="2bcaa-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="2bcaa-129">ID klienta Azure AD je globálně jedinečný identifikátor (GUID), který se podobá následujícímu příkladu: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="2bcaa-130">Najděte své ID klienta Azure AD pomocí Azure portálu</span><span class="sxs-lookup"><span data-stu-id="2bcaa-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="2bcaa-131">Přihlaste se do [portálu Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="2bcaa-132">Ujistěte se, zda jste vybrali správný adreář.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="2bcaa-133">V levé nabídce vyberte **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="2bcaa-134">Ve **Spravovat** vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="2bcaa-135">ID klienta Azure AD se zobrazí v **ID adresáře**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="2bcaa-136">Vyhledání ID klienta Azure AD pomocí metadat OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="2bcaa-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="2bcaa-137">Vytvořte adresu URL OpenID nahrazením **\{VAšE\_DOMéNA\}** VAší doménou, například `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="2bcaa-138">Například `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration`  se stane `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="2bcaa-139">Přejděte na adresu URL OpenID, která obsahuje vaši doménu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="2bcaa-140">ID klienta Azure AD lze zobrazit ve více hodnotách vlastností.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="2bcaa-141">Najděte **authorization\_endpoint** a extrahujte identifikátor GUID, který se zobrazí ihned po `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="2bcaa-142">Vyhledání ID skupiny zabezpečení Azure AD</span><span class="sxs-lookup"><span data-stu-id="2bcaa-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="2bcaa-143">ID skupiny zabezpečení Azure AD je identifikátor GUID, který se podobá následujícímu příkladu: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="2bcaa-144">Tento postup předpokládá, že jste členem skupiny, pro kterou chcete najít ID.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="2bcaa-145">Otevřete [Orůzkumník grafů](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="2bcaa-146">Vyberte **Přihlásit se k Microsoft** a přihlaste se pomocí svých pověření.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="2bcaa-147">Vlevo vyberte možnost **zobrazit další ukázky**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="2bcaa-148">Povolte **Skupiny** z pravého podokna.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="2bcaa-149">Zavřít pravé podokno.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-149">Close the right pane.</span></span>
1. <span data-ttu-id="2bcaa-150">Vyberte možnost **všechny skupiny, do kterých patřím**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="2bcaa-151">V poli **náhledu odpovědi** najděte svou skupinu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="2bcaa-152">ID skupiny zabezpečení se zobrazí ve vlastnosti **ID**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="2bcaa-153">Zřizování ukázkového prostředí služby Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="2bcaa-154">Tyto postupy vysvětlují, jak zřídit prostředí pro náhled Commerce.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="2bcaa-155">Po úspěšném dokončení těchto nastavení bude prostředí pro náhled Commerce připraveno na konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="2bcaa-156">Všechny popsané aktivity se objeví na portálu LCS.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bcaa-157">Přístup k náhledu je svázán s účtem LCS a organizací, kterou jste určili v aplikaci pro náhled.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="2bcaa-158">K zajištění prostředí náhledu Commerce je nutné použít stejný účet.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="2bcaa-159">Pokud musíte použít jiný účet LCS nebo nájemce pro prostředí náhledu Commerce, musíte tyto podrobnosti poskytnout společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="2bcaa-160">Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="2bcaa-161">Udělení přístupu k aplikacím e-Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bcaa-162">Osoba, která se přihlásí, musí být správcem klienta Azure AD, který má ID klienta Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="2bcaa-163">Pokud tento krok není úspěšně dokončen, zbývající kroky zřízení se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="2bcaa-164">Chcete-li autorizovat aplikace e-Commerce a získat přístup k předplatnému vašeho Azure, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-165">Sestavte adresu URL v následujícím formátu:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="2bcaa-166">Zkopírujte a vložte adresu URL do prohlížeče nebo do textového editoru a nahraďte **\{AAD\_TENANT\_ID\}** vaším ID klienta Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="2bcaa-167">Pak otevřete adresu URL.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-167">Then open the URL.</span></span>
1. <span data-ttu-id="2bcaa-168">V dialogovém okně přihlášení Azure AD se přihlaste a potvrďte, že chcete udělit přístup k předplatnému **Dynamics 365 Commerce (náhled)**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="2bcaa-169">Budete přesměrováni na stránku ukazující, zda operace proběhla úspěšně.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="2bcaa-170">Zkontrolujte, zda jsou k dispozici funkce náhledu a zda jsou zapnuty v LCS.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="2bcaa-171">Chcete-li zkontrolovat, zda jsou k dispozici funkce náhledu a zda jsou zapnuty v LCS, postupujte náledovně.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-172">Přihlaste se k [portálu LCS](https://lcs.dynamics.com) pomocí stejného účtu LCS, který jste použili k vyžádání přístupu k náhledu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="2bcaa-173">Na domovské stránce LCS posuňte se úplně doprava a vyberte dlaždici **Správa funkcí náhledu**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Dlaždice správy verze Preview](./media/preview1.png)

1. <span data-ttu-id="2bcaa-175">Posuňte se dolů k **Funkcím soukromého náhledu** a zkontrolujte, zda jsou dostupné a zapnuté následující funkce:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="2bcaa-176">Hodnocení e-Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="2bcaa-177">Prostředí služby Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="2bcaa-177">Commerce Preview Program Environments</span></span>

    ![Funkce soukromé verze Preview](./media/preview2.png)

1. <span data-ttu-id="2bcaa-179">Pokud se tyto funkce v seznamu neobjeví, obraťte se na společnost Microsoft a poskytněte své pracovní e-mailové adresy, účet LCS a podrobnosti o klientovi.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="2bcaa-180">Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="2bcaa-181">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="2bcaa-181">Create a new project</span></span>

<span data-ttu-id="2bcaa-182">Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-183">Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="2bcaa-184">V pravém podokně proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="2bcaa-185">Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="2bcaa-186">Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="2bcaa-187">Zadat název a popis šablony a odvětví.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="2bcaa-188">V poli **Název produktu** vyberte **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="2bcaa-189">V poli **Verze produktu** vyberte **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="2bcaa-190">V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="2bcaa-191">Volitelné: Můžete importovat role a uživatele z existujícího projektu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="2bcaa-192">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-192">Select **Create**.</span></span> <span data-ttu-id="2bcaa-193">Zobrazí se projekt.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="2bcaa-194">Přidejte konektor Azure</span><span class="sxs-lookup"><span data-stu-id="2bcaa-194">Add the Azure Connector</span></span>

<span data-ttu-id="2bcaa-195">Chcete-li přidat Azure konektor do projektu LCS, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-196">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="2bcaa-197">Pokud jste partnerem, vyberte dlaždici **Nastavení projektu** zcela vpravo.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="2bcaa-198">Pokud jste odběratel, zvolte **Nastavení projektu** z horní nabídky.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="2bcaa-199">Vyberte **Konektory Azure**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="2bcaa-200">Chcete-li přidat konektor Azure, klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="2bcaa-201">Zadejte název.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-201">Enter a name.</span></span>
1. <span data-ttu-id="2bcaa-202">Vložte své ID předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="2bcaa-203">Zapněte možnost **Konfigurovat pro použití technologie ARM (Azure Resource Manager)**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="2bcaa-204">Ověřte správnost hodnoty **Domény klienta předplatného služby Azure AAD ( nebo ID)**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="2bcaa-205">V případě potřeby se obraťte na správce předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="2bcaa-206">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-206">Select **Next**.</span></span>
1. <span data-ttu-id="2bcaa-207">Podle pokynů na stránce udělte požadovaným aplikacím přístup k vašemu předplatnému.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="2bcaa-208">V případě potřeby se obraťte na správce předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="2bcaa-209">Přihlaste se do [portálu Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="2bcaa-210">Přesvědčte se, zda je vybrán správný adresář, a v levé nabídce vyberte položku **odběry**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="2bcaa-211">Vyhledejte správné předplatné ze seznamu a vyberte je.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="2bcaa-212">Podle potřeby použijte funkci vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="2bcaa-213">V nabídce vyberte příkaz **Řízení přístupu (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="2bcaa-214">Napravo v sekci **Přidat přiřazení rolí** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="2bcaa-215">Objeví se podokno **Přidat přiřazení role**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="2bcaa-216">V poli **Role** vyberte **Přispěvatel**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="2bcaa-217">V poli **Přiřadit přístup k** ponechejte výchozí hodnotu, uživatele **Azure AD, skupinu nebo hlavní název služby**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="2bcaa-218">V možnosti **Vybrat** vložte **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="2bcaa-219">Vyberte **Služba pro nasazení aplikace Dynamics \[wsfed-enabled\]** ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="2bcaa-220">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-220">Select **Save**.</span></span>

1. <span data-ttu-id="2bcaa-221">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-221">Select **Next**.</span></span>
1. <span data-ttu-id="2bcaa-222">Podle pokynů na stránce udělte požadovaným aplikacím přístup k vašemu předplatnému.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="2bcaa-223">V případě potřeby se obraťte na správce předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="2bcaa-224">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-224">Select **Next**.</span></span>
1. <span data-ttu-id="2bcaa-225">V poli **Oblast Azure** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="2bcaa-226">Vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-226">Select **Connect**.</span></span> <span data-ttu-id="2bcaa-227">V seznamu by se měl zobrazit konektor Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="2bcaa-228">Importovat Náhled rozšíření ukázky Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="2bcaa-229">Chcete-li importovat Náhled rozšíření ukázky Commerce do projektu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-230">Otevřete domovskou stránku projektu výběrem názvu projektu v horní části.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="2bcaa-231">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="2bcaa-232">Pokud jste partnerem, vyberte dlaždici **Knihovna prostředků** zcela vpravo.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="2bcaa-233">Pokud jste odběratel, zvolte **Knihovna prostředků** z horní nabídky.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="2bcaa-234">Ze seznamu vlevo vyberte **Balíček nasazení softwaru**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="2bcaa-235">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-235">Select **Import**.</span></span>
1. <span data-ttu-id="2bcaa-236">V **Knihovně sdílených prostředků** vyberte **Náhled rozšíření ukázky Commerce** v knihovně prostřeků.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="2bcaa-237">Vyberte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-237">Select **Pick**.</span></span> <span data-ttu-id="2bcaa-238">Vrátíte se do knihovny majetku a toto rozšíření se zobrazí v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="2bcaa-239">Následující ilustrace znázorňuje akce, které je třeba provést na stránce **Knhovna prostředků** LCS.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Import Náhled rozšíření ukázky Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="2bcaa-241">Nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="2bcaa-241">Deploy the environment</span></span>

<span data-ttu-id="2bcaa-242">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="2bcaa-243">Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="2bcaa-244">V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce (Náhled)-demo (10.0.6 s aktualizací platformy 30)** zobrazuje přímo nad polem **Název prostředí**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="2bcaa-245">Viz obrázek, který se zobrazí po kroku 8.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="2bcaa-246">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="2bcaa-247">Prostředí přidáte výběrem tlačítka **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="2bcaa-248">V poli **Verze aplikace** vyberte **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="2bcaa-249">V poli **Verzi platformy** vyberte **Platform Update 30**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. <span data-ttu-id="2bcaa-251">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-251">Select **Next**.</span></span>
1. <span data-ttu-id="2bcaa-252">Výberte **Demo** jako topologii prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-252">Select **Demo** as the environment topology.</span></span>

    ![Výběr topologie prostředí 1](./media/project2.png)

1. <span data-ttu-id="2bcaa-254">Vyberte **Dynamics 365 Commerce (Náhled) - Demo** jako topologii prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="2bcaa-255">Pokud jste dříve nakonfigurovali jeden konektor Azure Connector, bude se používat pro toto prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="2bcaa-256">Pokud jste nakonfigurovali více konektorů Azure, můžete vybrat, kterou spojnici chcete použít: **:Východ USA**, **Východ USA 2**, **Západ USA** nebo **Západ USA 2**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="2bcaa-257">(Pro dosažení nejlepšího výkonu doporučujeme vybrat **Západ USA 2**.)</span><span class="sxs-lookup"><span data-stu-id="2bcaa-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Výběr topologie prostředí 2](./media/project3.png)

1. <span data-ttu-id="2bcaa-259">Na stránce **Nasadit prostředí** zadejte název prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="2bcaa-260">Ponechte Upřesňující nastavení, jak je.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-260">Leave the advanced settings as they are.</span></span>

    ![Stránka Nasazení prostředí](./media/project4.png)

1. <span data-ttu-id="2bcaa-262">Upravte velikost VM podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-262">Adjust the VM size as required.</span></span> <span data-ttu-id="2bcaa-263">(Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="2bcaa-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="2bcaa-264">Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="2bcaa-265">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-265">Select **Next**.</span></span>
1. <span data-ttu-id="2bcaa-266">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="2bcaa-267">Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="2bcaa-268">Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="2bcaa-269">Dokončení pracovních postupů prostředí bude trvat určitou dobu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="2bcaa-270">Proto se vraťte přibližně za 6 až 9 hodin.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="2bcaa-271">Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="2bcaa-272">Inicializujte RCSU</span><span class="sxs-lookup"><span data-stu-id="2bcaa-272">Initialize RCSU</span></span>

<span data-ttu-id="2bcaa-273">Pokud chcete inicializovat RCSU, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-274">V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="2bcaa-275">V zobrazení prostředí napraco vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="2bcaa-276">Zobrazí se podrobnosti o prostředí.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-276">The environment details view appears.</span></span>
1. <span data-ttu-id="2bcaa-277">V části **Funkce prostředí** vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="2bcaa-278">Na kartě **Maloobchod** vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="2bcaa-279">Zobrazí se zobrazení inicializačních parametrů RCSU.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="2bcaa-280">V poli **Oblast** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="2bcaa-281">V poli **Verze** vyberte možnost **Určit verzi** v seznamu a pak zadejte **9.16.19262.5** do zobrazeného pole.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="2bcaa-282">Je třeba zadat přesnou verzi, která je zde uvedena.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="2bcaa-283">V opačném případě bude nutné RCSU aktualizovat na správnou verzi později.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="2bcaa-284">Zapněte možnost **použít rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="2bcaa-285">V seznamu přípon vyberte možnost **Náhled rozšíření ukázky Commerce**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="2bcaa-286">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="2bcaa-287">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="2bcaa-288">Vrátíte se do zobrazení **Řízení maloobchodu** s vybranou kartou **Maloobchod**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="2bcaa-289">Vaše RCSU byla zařazena do fronty pro zřizování.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="2bcaa-290">Než budete pokračovat, ujistěte se, že je stav RCSU **Úspěch**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="2bcaa-291">Inicializace trvá přibližně dvě až pět hodin.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="2bcaa-292">Inicializace e-Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-292">Initialize e-Commerce</span></span>

<span data-ttu-id="2bcaa-293">Pokud chcete inicializovat e-Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2bcaa-294">Na kartě **e-Commerce (Náhled)** zkontrolujte souhlas s náhledem a pak vyberte **nastavení.**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="2bcaa-295">Zadejte název pro **Název klienta e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="2bcaa-296">Uvědomte si však, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="2bcaa-297">V poli **Název Retail Cloud Scale Unit** vyberte položku RCSU v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="2bcaa-298">(Seznam by měl mít pouze jednu možnost.)</span><span class="sxs-lookup"><span data-stu-id="2bcaa-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="2bcaa-299">Pole **Geografie e-Commerce** je nastaveno automaticky a hodnota nemůže být změněna.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="2bcaa-300">Pokračujte výběrem tlačítka **Další**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="2bcaa-301">Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="2bcaa-302">Ve skupině **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="2bcaa-303">Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="2bcaa-304">Vyberte skupinu zabezpečení ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="2bcaa-305">Ve skupině **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="2bcaa-306">Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="2bcaa-307">Vyberte skupinu zabezpečení ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="2bcaa-308">Ponechte možnost **Povolit službu hodnocení a recenzí** povolenou.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="2bcaa-309">Pokud jste již dokončili krok souhlasu společnosti Microsoft Azure Active Directory (Azure AD) podle popisu v části "Udělení přístupu k aplikacím e-Commerce", zaškrtněte políčko a potvrďte svůj souhlas.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="2bcaa-310">Pokud jste tento krok ještě nedokončili, musíte to provést dříve, než budete pokračovat v inicializaci.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="2bcaa-311">Chcete-li otevřít dialogové okno souhlasu a dokončit krok, vyberte odkaz v textu vedle zaškrtávacího políčka.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="2bcaa-312">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-312">Select **Initialize**.</span></span> <span data-ttu-id="2bcaa-313">Vrátíte se do zobrazení **Řízení maloobchodu** s vybranou kartou **e-Commerce (Náhled)**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="2bcaa-314">Vaše inicializace e-Commerce byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="2bcaa-315">Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="2bcaa-316">V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:</span><span class="sxs-lookup"><span data-stu-id="2bcaa-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="2bcaa-317">**Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="2bcaa-318">**Nástroj pro správu webu e-Commerce** – odkaz na nástroj pro správu webu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="2bcaa-319">Podora ukázkového prostředí služby Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-319">Commerce preview environment support</span></span>

<span data-ttu-id="2bcaa-320">Pokud při provádění kroků zajišťování dojde k problémům, o pomoc se obraťte na [skupinu náhledu Microsoft Dynamics 365 Commerce v aplikaci Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="2bcaa-321">Pokud se při pokusu o přístup ke skupině Yammer vyskytnou problémy, můžete kontaktovat společnost Microsoft e-mailem na adrese <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="2bcaa-322">Tato e-mailová adresa není aktivně monitorována.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="2bcaa-323">Proto očekávejte prodlevu v odpovědi.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2bcaa-324">Další kroky</span><span class="sxs-lookup"><span data-stu-id="2bcaa-324">Next steps</span></span>

<span data-ttu-id="2bcaa-325">Chcete-li pokračovat v procesu zřizování a konfigurace prostředí náhledu Commerce, viz [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2bcaa-326">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2bcaa-326">Additional resources</span></span>

[<span data-ttu-id="2bcaa-327">Přehled prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="2bcaa-328">Konfigurovat prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="2bcaa-329">Nastavení volitelných funkcí pro prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="2bcaa-330">Často kladené dotazy k prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="2bcaa-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2bcaa-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="2bcaa-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="2bcaa-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="2bcaa-333">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="2bcaa-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="2bcaa-334">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2bcaa-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="2bcaa-335">Zdroje nápovědy pro Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="2bcaa-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
