---
title: Zřízení prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a57cc02c6d62f288f14b65191c2f4927a019963c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478157"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="f8e91-103">Zřízení prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8e91-104">Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8e91-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="f8e91-105">Než začnete, doporučujeme vám toto téma rychle prohledat, abyste získali představu o tom, co proces vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="f8e91-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="f8e91-106">Prostředí vyhodnocení Commerce nejsou obecně dostupná a jsou poskytována partnerům a zákazníkům na základě žádosti.</span><span class="sxs-lookup"><span data-stu-id="f8e91-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="f8e91-107">Podrobnější informace získáte od kontaktu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8e91-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="f8e91-108">Chcete-li úspěšně zřídit prostředí pro hodnocení Commerce, musíte vytvořit projekt, který má specifický název a typ produktu.</span><span class="sxs-lookup"><span data-stu-id="f8e91-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="f8e91-109">Prostředí a Commerce Scale Unit (CSU) také mají některé specifické parametry, které musíte použít, když se chystáte ke zřizování e-Commerce později.</span><span class="sxs-lookup"><span data-stu-id="f8e91-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="f8e91-110">Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.</span><span class="sxs-lookup"><span data-stu-id="f8e91-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="f8e91-111">Po úspěšném zřízení prostředí vyhodnocení Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků.</span><span class="sxs-lookup"><span data-stu-id="f8e91-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="f8e91-112">Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="f8e91-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="f8e91-113">Volitelné kroky můžete vždy dokončit později.</span><span class="sxs-lookup"><span data-stu-id="f8e91-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="f8e91-114">Informace o konfiguraci prostředí vyhodnocení Commerce po jeho vytvoření najdete v části [konfigurace prostředí vyhodnocení Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="f8e91-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="f8e91-115">Informace o konfiguraci volitelných funkcí prostředí vyhodnocení Commerce najdete v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="f8e91-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f8e91-116">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="f8e91-116">Prerequisites</span></span>

<span data-ttu-id="f8e91-117">Aby bylo možné zřídit prostředí vyhodnocení Commerce, musí být zavedeny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="f8e91-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="f8e91-118">Byli jste přijati do programu hodnocení a byla vám udělena kapacita pro prostředí hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f8e91-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="f8e91-119">Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f8e91-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="f8e91-120">Jste stávajícím partnerem Microsoft Dynamics 365 nebo odběratelem a máte možnost vytvořit projekt Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8e91-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="f8e91-121">Máte přístup správce k vašemu předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který vám může v případě potřeby pomoci.</span><span class="sxs-lookup"><span data-stu-id="f8e91-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="f8e91-122">Máte k dispozici ID klienta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f8e91-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="f8e91-123">Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="f8e91-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="f8e91-124">Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="f8e91-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="f8e91-125">(Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)</span><span class="sxs-lookup"><span data-stu-id="f8e91-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="f8e91-126">Tento seznam není vyčerpávající.</span><span class="sxs-lookup"><span data-stu-id="f8e91-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="f8e91-127">Pokud se objeví nějaké problémy, měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.</span><span class="sxs-lookup"><span data-stu-id="f8e91-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="f8e91-128">Zřizování prostředí vyhodnocení služby Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="f8e91-129">Tyto postupy vysvětlují, jak zřídit prostředí vyhodnocení Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8e91-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="f8e91-130">Po úspěšném dokončení těchto nastavení bude prostředí vyhodnocení Commerce připraveno na konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="f8e91-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="f8e91-131">Všechny popsané aktivity se objeví na portálu LCS.</span><span class="sxs-lookup"><span data-stu-id="f8e91-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="f8e91-132">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="f8e91-132">Create a new project</span></span>

<span data-ttu-id="f8e91-133">Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="f8e91-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="f8e91-134">Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="f8e91-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="f8e91-135">V pravém podokně proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="f8e91-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="f8e91-136">Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="f8e91-137">Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="f8e91-138">Zadat název a popis šablony a odvětví.</span><span class="sxs-lookup"><span data-stu-id="f8e91-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="f8e91-139">V poli **Název produktu** vyberte **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="f8e91-140">V poli **Verze produktu** vyberte **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="f8e91-141">V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="f8e91-142">Volitelné: Můžete importovat role a uživatele z existujícího projektu.</span><span class="sxs-lookup"><span data-stu-id="f8e91-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="f8e91-143">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-143">Select **Create**.</span></span> <span data-ttu-id="f8e91-144">Zobrazí se projekt.</span><span class="sxs-lookup"><span data-stu-id="f8e91-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="f8e91-145">Přidejte konektor Azure</span><span class="sxs-lookup"><span data-stu-id="f8e91-145">Add the Azure Connector</span></span>

<span data-ttu-id="f8e91-146">Chcete-li přidat Azure Connector do svého projektu LCS, postupujte podle kroků v části [Dokončení procesu integrace Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="f8e91-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="f8e91-147">Nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="f8e91-147">Deploy the environment</span></span>

<span data-ttu-id="f8e91-148">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f8e91-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="f8e91-149">Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny.</span><span class="sxs-lookup"><span data-stu-id="f8e91-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="f8e91-150">V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce - ukázka (10.0.* x* s aktualizací Platform *xx*)\*\* zobrazuje přímo nad polem **Název prostředí**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="f8e91-151">Podrobnosti viz obrázek, který se zobrazí po kroku 8.</span><span class="sxs-lookup"><span data-stu-id="f8e91-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="f8e91-152">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="f8e91-153">Prostředí přidáte výběrem tlačítka **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="f8e91-154">V poli **verze aplikace** vyberte nejaktuálnější verzi.</span><span class="sxs-lookup"><span data-stu-id="f8e91-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="f8e91-155">Pokud máte specifickou potřebu vybrat jinou než nejaktuálnější verzi aplikace, nevybírejte verzi před **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="f8e91-156">V poli **verze platformy** použijte verzi platformy, která je automaticky vybrána pro vybranou verzi aplikace.</span><span class="sxs-lookup"><span data-stu-id="f8e91-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. <span data-ttu-id="f8e91-158">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-158">Select **Next**.</span></span>
1. <span data-ttu-id="f8e91-159">Výberte **Demo** jako topologii prostředí.</span><span class="sxs-lookup"><span data-stu-id="f8e91-159">Select **Demo** as the environment topology.</span></span>

    ![Výběr topologie prostředí 1](./media/project2.png)

1. <span data-ttu-id="f8e91-161">Na stránce **Nasadit prostředí** zadejte název prostředí.</span><span class="sxs-lookup"><span data-stu-id="f8e91-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="f8e91-162">Ponechte Upřesňující nastavení, jak je.</span><span class="sxs-lookup"><span data-stu-id="f8e91-162">Leave the advanced settings as they are.</span></span>

    ![Stránka Nasazení prostředí](./media/project4.png)

1. <span data-ttu-id="f8e91-164">Upravte velikost VM podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="f8e91-164">Adjust the VM size as required.</span></span> <span data-ttu-id="f8e91-165">(Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="f8e91-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="f8e91-166">Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.</span><span class="sxs-lookup"><span data-stu-id="f8e91-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="f8e91-167">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-167">Select **Next**.</span></span>
1. <span data-ttu-id="f8e91-168">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="f8e91-169">Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="f8e91-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="f8e91-170">Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno.</span><span class="sxs-lookup"><span data-stu-id="f8e91-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="f8e91-171">Dokončení pracovních postupů prostředí bude trvat určitou dobu.</span><span class="sxs-lookup"><span data-stu-id="f8e91-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="f8e91-172">Proto se vraťte přibližně za 6 až 9 hodin.</span><span class="sxs-lookup"><span data-stu-id="f8e91-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="f8e91-173">Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="f8e91-174">Inicializace Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="f8e91-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="f8e91-175">Pokud chcete inicializovat CSU, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f8e91-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="f8e91-176">V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="f8e91-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="f8e91-177">V zobrazení prostředí napraco vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="f8e91-178">Zobrazí se podrobnosti o prostředí.</span><span class="sxs-lookup"><span data-stu-id="f8e91-178">The environment details view appears.</span></span>
1. <span data-ttu-id="f8e91-179">V části **Funkce prostředí** vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="f8e91-180">Na kartě **Velkoobchod** vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="f8e91-181">Zobrazí se zobrazení inicializačních parametrů CSU.</span><span class="sxs-lookup"><span data-stu-id="f8e91-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="f8e91-182">V poli **Oblast** vyberte oblast, která je stejná nebo blízká oblasti, do které jste prostředí nasadili.</span><span class="sxs-lookup"><span data-stu-id="f8e91-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="f8e91-183">Nechte pole **Verze** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="f8e91-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="f8e91-184">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="f8e91-185">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="f8e91-186">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="f8e91-187">Vaše CSU byla zařazena do fronty pro zřizování.</span><span class="sxs-lookup"><span data-stu-id="f8e91-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="f8e91-188">Než budete pokračovat, ujistěte se, že je stav CSU **Úspěch**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="f8e91-189">Inicializace trvá přibližně dvě až pět hodin.</span><span class="sxs-lookup"><span data-stu-id="f8e91-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="f8e91-190">Pokud nemůžete najít odkaz **Správa** odkaz v zobrazení podrobností o prostředí, požádejte o pomoc kontaktní osobu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8e91-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="f8e91-191">Při počátečním zpracování se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="f8e91-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="f8e91-192">Vyhodnocovací (demo/testovací) prostředí musí registrovat aplikaci konektoru jednotky škálování \<application ID\> v centrále.</span><span class="sxs-lookup"><span data-stu-id="f8e91-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="f8e91-193">Pokud se inicializace CSU nezdaří a zobrazí se tato chybová zpráva, poznamenejte si ID aplikace, což je globálně jedinečný identifikátor (GUID), a poté podle pokynů v další části zaregistrujte aplikaci nasazení CSU v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8e91-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="f8e91-194">Zaregistrujte aplikaci nasazení CSU v obchodním ústředí (je-li požadováno)</span><span class="sxs-lookup"><span data-stu-id="f8e91-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="f8e91-195">Chcete-li zaregistrovat aplikaci nasazení CSU v obchodním ústředí, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f8e91-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f8e91-196">V centrále Commerce přejděte na **Správa systému \> Nastavení \> Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="f8e91-197">Ve sloupci **ID klienta** zadejte ID aplikace z chybové zprávy inicializace CSU, kterou jste obdrželi.</span><span class="sxs-lookup"><span data-stu-id="f8e91-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="f8e91-198">Ve sloupci **Název** zadejte libovolný popisný text (například **CSU Eval**).</span><span class="sxs-lookup"><span data-stu-id="f8e91-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="f8e91-199">Ve sloupci **ID uživatele** zadejte **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="f8e91-200">Opakujte inicializaci a nasazení CSU z LCS.</span><span class="sxs-lookup"><span data-stu-id="f8e91-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="f8e91-201">Inicializace e-Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-201">Initialize e-Commerce</span></span>

<span data-ttu-id="f8e91-202">Pokud chcete inicializovat e-Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f8e91-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f8e91-203">Na kartě **e-Commerce** zkontrolujte souhlas s vyhodnocením a pak vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="f8e91-204">V poli **Název prostředí e-Commerce** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="f8e91-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="f8e91-205">Uvědomte, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8e91-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="f8e91-206">V poli **Název Commerce Scale Unit** vyberte položku CSU v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f8e91-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="f8e91-207">(Seznam by měl mít pouze jednu možnost.)</span><span class="sxs-lookup"><span data-stu-id="f8e91-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="f8e91-208">Pole **Geografie elektronického obchodování** je nastaveno automaticky.</span><span class="sxs-lookup"><span data-stu-id="f8e91-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="f8e91-209">Pokračujte výběrem tlačítka **Další**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="f8e91-210">Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="f8e91-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="f8e91-211">V poli **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy.</span><span class="sxs-lookup"><span data-stu-id="f8e91-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="f8e91-212">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="f8e91-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="f8e91-213">V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzování** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy.</span><span class="sxs-lookup"><span data-stu-id="f8e91-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="f8e91-214">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="f8e91-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="f8e91-215">Možnost **Povolit službu hodnocení a recenzování** nechte nastavenou na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="f8e91-216">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-216">Select **Initialize**.</span></span> <span data-ttu-id="f8e91-217">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="f8e91-218">Vaše inicializace e-Commerce byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="f8e91-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="f8e91-219">Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.</span><span class="sxs-lookup"><span data-stu-id="f8e91-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="f8e91-220">V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:</span><span class="sxs-lookup"><span data-stu-id="f8e91-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="f8e91-221">**Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8e91-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="f8e91-222">**Nástroj pro správu webu Commerce** – odkaz na nástroj pro správu webu.</span><span class="sxs-lookup"><span data-stu-id="f8e91-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f8e91-223">Další kroky</span><span class="sxs-lookup"><span data-stu-id="f8e91-223">Next steps</span></span>

<span data-ttu-id="f8e91-224">Chcete-li pokračovat v procesu zřizování a konfigurace prostředí vyhodnocení Commerce, přečtěte si část [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="f8e91-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8e91-225">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f8e91-225">Additional resources</span></span>

[<span data-ttu-id="f8e91-226">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="f8e91-227">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="f8e91-228">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="f8e91-229">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="f8e91-230">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="f8e91-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="f8e91-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="f8e91-232">Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="f8e91-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="f8e91-233">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="f8e91-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="f8e91-234">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8e91-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
