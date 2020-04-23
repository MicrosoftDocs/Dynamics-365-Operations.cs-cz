---
title: Zřízení prostředí Preview aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak zřídit ukázkové prostředí v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/10/2020
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
ms.openlocfilehash: d54db89372a0f9ef5b267d25e14067e3243a803c
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254741"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="bb9e9-103">Zřízení prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bb9e9-104">Toto téma vysvětluje, jak zřídit ukázkové prostředí v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="bb9e9-105">Než začnete, doporučujeme vám toto téma rychle prohledat, abyste získali představu o tom, co proces vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="bb9e9-106">Pokud ještě nemáte přístup k Dynamics 365 Commerce Preview, můžete si vyžádat přístup k náhledu z webu [Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="bb9e9-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="bb9e9-107">Overview</span></span>

<span data-ttu-id="bb9e9-108">Chcete-li úspěšně zřídit prostředí pro náhled Commerce, musíte vytvořit projekt, který má specifický název a typ produktu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="bb9e9-109">Prostředí a commerce scale unit (CSU) také mají některé specifické parametry, které musíte použít ke zřizování e-Commerce později.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="bb9e9-110">Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="bb9e9-111">Po úspěšném zřízení ukázkového prostředí Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="bb9e9-112">Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="bb9e9-113">Volitelné kroky můžete vždy dokončit později.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="bb9e9-114">Informace o konfiguraci prostředí pro náhled Commerce po jeho vytvoření najdete v části [konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="bb9e9-115">Informace o konfiguraci volitelných funkcí prostředí pro náhled Commerce najdete v části [konfigurace volitelných funkcí prostředí pro náhled Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="bb9e9-116">Pokud máte dotazy týkající se kroků zřizování nebo pokud se vyskytnou nějaké problémy, sdělte je společnosti Microsoft na [Microsoft Dynamics 365 Commerce, skupina náhledu Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb9e9-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="bb9e9-117">Prerequisites</span></span>

<span data-ttu-id="bb9e9-118">Aby bylo možné zřídit prostředí pro náhled Commerce, musí být zavedeny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="bb9e9-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="bb9e9-119">Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="bb9e9-120">Jste stávajícím partnerem Microsoft Dynamics 365 nebo odběratelem a máte možnost vytvořit projekt Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="bb9e9-121">Byli jste přijati do programu náhledu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="bb9e9-122">Máte požadovaná oprávnění k vytvoření projektu pro **migraci, vytvoření řešení a další informace**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="bb9e9-123">Máte roli **Správce prostředí** nebo **Vlastník projektu** v projektu, kde se chystáte zřídit prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="bb9e9-124">Máte přístup pro správu ke svému předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který může provést dva kroky, které pro vás vyžadují oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="bb9e9-125">Máte k dispozici ID klienta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="bb9e9-126">Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="bb9e9-127">Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="bb9e9-128">(Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="bb9e9-129">Zřizování ukázkového prostředí služby Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="bb9e9-130">Tyto postupy vysvětlují, jak zřídit prostředí pro náhled Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="bb9e9-131">Po úspěšném dokončení těchto nastavení bude prostředí pro náhled Commerce připraveno na konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="bb9e9-132">Všechny popsané aktivity se objeví na portálu LCS.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb9e9-133">Přístup k náhledu je svázán s účtem LCS a organizací, kterou jste určili v aplikaci Commerce pro náhled.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="bb9e9-134">K zajištění prostředí náhledu Commerce je nutné použít stejný účet.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="bb9e9-135">Pokud potřebujete použít jiný účet LCS nebo nájemce pro prostředí náhledu Commerce, musíte tyto podrobnosti poskytnout společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="bb9e9-136">Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="bb9e9-137">Zkontrolujte, zda jsou k dispozici funkce náhledu a zda jsou zapnuty v LCS.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="bb9e9-138">Chcete-li zkontrolovat, zda jsou k dispozici funkce náhledu a zda jsou zapnuty v LCS, postupujte náledovně.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="bb9e9-139">Přihlaste se k [portálu LCS](https://lcs.dynamics.com) pomocí stejného účtu LCS, který jste použili k vyžádání přístupu k náhledu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="bb9e9-140">Na domovské stránce LCS posuňte se úplně doprava a vyberte dlaždici **Správa funkcí náhledu**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Dlaždice správy verze Preview](./media/preview1.png)

1. <span data-ttu-id="bb9e9-142">Posuňte se dolů k **Funkcím soukromého náhledu** a zkontrolujte, zda jsou dostupné a zapnuté následující funkce:</span><span class="sxs-lookup"><span data-stu-id="bb9e9-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="bb9e9-143">Hodnocení e-Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="bb9e9-144">Prostředí služby Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="bb9e9-144">Commerce Preview Program Environments</span></span>

    ![Funkce soukromé verze Preview](./media/preview2.png)

1. <span data-ttu-id="bb9e9-146">Pokud se tyto funkce v seznamu neobjeví, obraťte se na společnost Microsoft a poskytněte své pracovní e-mailové adresy, účet LCS a podrobnosti o klientovi.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="bb9e9-147">Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="bb9e9-148">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="bb9e9-148">Create a new project</span></span>

<span data-ttu-id="bb9e9-149">Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="bb9e9-150">Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="bb9e9-151">V pravém podokně proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="bb9e9-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="bb9e9-152">Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="bb9e9-153">Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="bb9e9-154">Zadat název a popis šablony a odvětví.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="bb9e9-155">V poli **Název produktu** vyberte **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="bb9e9-156">V poli **Verze produktu** vyberte **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="bb9e9-157">V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="bb9e9-158">Volitelné: Můžete importovat role a uživatele z existujícího projektu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="bb9e9-159">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-159">Select **Create**.</span></span> <span data-ttu-id="bb9e9-160">Zobrazí se projekt.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="bb9e9-161">Přidejte konektor Azure</span><span class="sxs-lookup"><span data-stu-id="bb9e9-161">Add the Azure Connector</span></span>

<span data-ttu-id="bb9e9-162">Chcete-li přidat Azure konektor do projektu LCS, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="bb9e9-163">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="bb9e9-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="bb9e9-164">Pokud jste partnerem, vyberte dlaždici **Nastavení projektu** zcela vpravo.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="bb9e9-165">Pokud jste odběratel, zvolte **Nastavení projektu** z horní nabídky.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="bb9e9-166">Vyberte **Konektory Azure**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="bb9e9-167">Chcete-li přidat konektor Azure, klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="bb9e9-168">Zadejte název.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-168">Enter a name.</span></span>
1. <span data-ttu-id="bb9e9-169">Vložte své ID předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="bb9e9-170">Zapněte možnost **Konfigurovat pro použití technologie ARM (Azure Resource Manager)**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="bb9e9-171">Ověřte správnost hodnoty **Domény klienta předplatného služby Azure AAD ( nebo ID)**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="bb9e9-172">V případě potřeby se obraťte na správce předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="bb9e9-173">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-173">Select **Next**.</span></span>
1. <span data-ttu-id="bb9e9-174">Podle pokynů na stránce udělte požadovaným aplikacím přístup k vašemu předplatnému.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="bb9e9-175">V případě potřeby se obraťte na správce předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="bb9e9-176">Přihlaste se do [portálu Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="bb9e9-177">Přesvědčte se, zda je vybrán správný adresář, a v levé nabídce vyberte položku **odběry**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="bb9e9-178">Vyhledejte správné předplatné ze seznamu a vyberte je.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="bb9e9-179">Podle potřeby použijte funkci vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="bb9e9-180">V nabídce vyberte příkaz **Řízení přístupu (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="bb9e9-181">Napravo v sekci **Přidat přiřazení rolí** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="bb9e9-182">Objeví se podokno **Přidat přiřazení role**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="bb9e9-183">V poli **Role** vyberte **Přispěvatel**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="bb9e9-184">V poli **Přiřadit přístup k** ponechejte výchozí hodnotu, uživatele **Azure AD, skupinu nebo hlavní název služby**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="bb9e9-185">V možnosti **Vybrat** vložte **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="bb9e9-186">Vyberte **Služba pro nasazení aplikace Dynamics \[wsfed-enabled\]** ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="bb9e9-187">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-187">Select **Save**.</span></span>

1. <span data-ttu-id="bb9e9-188">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-188">Select **Next**.</span></span>
1. <span data-ttu-id="bb9e9-189">Podle pokynů na stránce udělte požadovaným aplikacím přístup k vašemu předplatnému.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="bb9e9-190">V případě potřeby se obraťte na správce předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="bb9e9-191">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-191">Select **Next**.</span></span>
1. <span data-ttu-id="bb9e9-192">V poli **Oblast Azure** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="bb9e9-193">Vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-193">Select **Connect**.</span></span> <span data-ttu-id="bb9e9-194">V seznamu by se měl zobrazit konektor Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="bb9e9-195">Importovat Náhled rozšíření ukázky Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="bb9e9-196">Chcete-li importovat Náhled rozšíření ukázky Commerce do projektu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="bb9e9-197">Otevřete domovskou stránku projektu výběrem názvu projektu v horní části.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="bb9e9-198">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="bb9e9-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="bb9e9-199">Pokud jste partnerem, vyberte dlaždici **Knihovna prostředků** zcela vpravo.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="bb9e9-200">Pokud jste odběratel, zvolte **Knihovna prostředků** z horní nabídky.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="bb9e9-201">Ze seznamu vlevo vyberte **Balíček nasazení softwaru**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="bb9e9-202">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-202">Select **Import**.</span></span>
1. <span data-ttu-id="bb9e9-203">V **Knihovně sdílených prostředků** vyberte **Náhled rozšíření ukázky Commerce** v knihovně prostřeků.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="bb9e9-204">Vyberte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-204">Select **Pick**.</span></span> <span data-ttu-id="bb9e9-205">Vrátíte se do knihovny majetku a toto rozšíření se zobrazí v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="bb9e9-206">Následující ilustrace znázorňuje akce, které je třeba provést na stránce **Knhovna prostředků** LCS.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Import Náhled rozšíření ukázky Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="bb9e9-208">Nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="bb9e9-208">Deploy the environment</span></span>

<span data-ttu-id="bb9e9-209">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="bb9e9-210">Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="bb9e9-211">V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce - ukázka (10.0.* x* s aktualizací Platform *xx*)\*\* zobrazuje přímo nad polem **Název prostředí**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="bb9e9-212">Podrobnosti viz obrázek, který se zobrazí po kroku 8.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="bb9e9-213">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="bb9e9-214">Prostředí přidáte výběrem tlačítka **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="bb9e9-215">V poli **verze aplikace** vyberte nejaktuálnější verzi.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="bb9e9-216">Pokud máte specifickou potřebu vybrat jinou než nejaktuálnější verzi aplikace, nevybírejte verzi před **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="bb9e9-217">V poli **verze platformy** použijte verzi platformy, která je automaticky vybrána pro vybranou verzi aplikace.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. <span data-ttu-id="bb9e9-219">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-219">Select **Next**.</span></span>
1. <span data-ttu-id="bb9e9-220">Výberte **Demo** jako topologii prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-220">Select **Demo** as the environment topology.</span></span>

    ![Výběr topologie prostředí 1](./media/project2.png)

1. <span data-ttu-id="bb9e9-222">Jako topologii prostředí vyberte **Dynamics 365 Commerce - ukázka**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="bb9e9-223">Pokud jste dříve nakonfigurovali jeden konektor Azure Connector, bude se používat pro toto prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="bb9e9-224">Pokud jste nakonfigurovali více konektorů Azure, můžete vybrat, kterou spojnici chcete použít: **:Východ USA**, **Východ USA 2**, **Západ USA** nebo **Západ USA 2**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="bb9e9-225">(Pro dosažení nejlepšího výkonu doporučujeme vybrat **Západ USA 2**.)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Výběr topologie prostředí 2](./media/project3.png)

1. <span data-ttu-id="bb9e9-227">Na stránce **Nasadit prostředí** zadejte název prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="bb9e9-228">Ponechte Upřesňující nastavení, jak je.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-228">Leave the advanced settings as they are.</span></span>

    ![Stránka Nasazení prostředí](./media/project4.png)

1. <span data-ttu-id="bb9e9-230">Upravte velikost VM podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-230">Adjust the VM size as required.</span></span> <span data-ttu-id="bb9e9-231">(Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="bb9e9-232">Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="bb9e9-233">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-233">Select **Next**.</span></span>
1. <span data-ttu-id="bb9e9-234">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="bb9e9-235">Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="bb9e9-236">Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="bb9e9-237">Dokončení pracovních postupů prostředí bude trvat určitou dobu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="bb9e9-238">Proto se vraťte přibližně za 6 až 9 hodin.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="bb9e9-239">Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="bb9e9-240">Inicializace commerce scale unit (CSU)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="bb9e9-241">Pokud chcete inicializovat CSU, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="bb9e9-242">V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="bb9e9-243">V zobrazení prostředí napraco vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="bb9e9-244">Zobrazí se podrobnosti o prostředí.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-244">The environment details view appears.</span></span>
1. <span data-ttu-id="bb9e9-245">V části **Funkce prostředí** vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="bb9e9-246">Na kartě **Velkoobchod** vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="bb9e9-247">Zobrazí se zobrazení inicializačních parametrů CSU.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="bb9e9-248">V poli **Oblast** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="bb9e9-249">V poli **Verze** vyberte možnost **Určit verzi** v seznamu a pak zadejte **9.18.20014.4** do zobrazeného pole.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="bb9e9-250">Je třeba zadat přesnou verzi, která je zde uvedena.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="bb9e9-251">V opačném případě bude nutné RCSU aktualizovat na správnou verzi později.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="bb9e9-252">Zapněte možnost **použít rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="bb9e9-253">V seznamu přípon vyberte možnost **Náhled rozšíření ukázky Commerce**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="bb9e9-254">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="bb9e9-255">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="bb9e9-256">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="bb9e9-257">Vaše CSU byla zařazena do fronty pro zřizování.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="bb9e9-258">Než budete pokračovat, ujistěte se, že je stav CSU **Úspěch**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="bb9e9-259">Inicializace trvá přibližně dvě až pět hodin.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="bb9e9-260">Inicializace e-Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-260">Initialize e-Commerce</span></span>

<span data-ttu-id="bb9e9-261">Pokud chcete inicializovat e-Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bb9e9-262">Na kartě **e-Commerce** zkontrolujte souhlas s náhledem a pak vyberte **nastavení.**</span><span class="sxs-lookup"><span data-stu-id="bb9e9-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="bb9e9-263">Zadejte název pro **Název klienta e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="bb9e9-264">Uvědomte si však, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="bb9e9-265">V poli **Název Commerce scale unit** vyberte položku CSU v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="bb9e9-266">(Seznam by měl mít pouze jednu možnost.)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="bb9e9-267">Pole **Geografie e-Commerce** je nastaveno automaticky a hodnota nemůže být změněna.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="bb9e9-268">Pokračujte výběrem tlačítka **Další**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="bb9e9-269">Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="bb9e9-270">Ve skupině **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="bb9e9-271">Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="bb9e9-272">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="bb9e9-273">Ve skupině **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="bb9e9-274">Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="bb9e9-275">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="bb9e9-276">Ponechte možnost **Povolit službu hodnocení a recenzí** povolenou.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="bb9e9-277">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-277">Select **Initialize**.</span></span> <span data-ttu-id="bb9e9-278">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="bb9e9-279">Vaše inicializace e-Commerce byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="bb9e9-280">Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="bb9e9-281">V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:</span><span class="sxs-lookup"><span data-stu-id="bb9e9-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="bb9e9-282">**Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="bb9e9-283">**Nástroj pro správu webu e-Commerce** – odkaz na nástroj pro správu webu.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="bb9e9-284">Podora ukázkového prostředí služby Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-284">Commerce preview environment support</span></span>

<span data-ttu-id="bb9e9-285">Pokud při provádění kroků zajišťování dojde k problémům, o pomoc se obraťte na [skupinu náhledu Microsoft Dynamics 365 Commerce v aplikaci Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb9e9-286">Další kroky</span><span class="sxs-lookup"><span data-stu-id="bb9e9-286">Next steps</span></span>

<span data-ttu-id="bb9e9-287">Chcete-li pokračovat v procesu zřizování a konfigurace prostředí náhledu Commerce, viz [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="bb9e9-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb9e9-288">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="bb9e9-288">Additional resources</span></span>

[<span data-ttu-id="bb9e9-289">Přehled prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="bb9e9-290">Konfigurace prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="bb9e9-291">Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="bb9e9-292">Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="bb9e9-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="bb9e9-294">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="bb9e9-294">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="bb9e9-295">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="bb9e9-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="bb9e9-296">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb9e9-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

