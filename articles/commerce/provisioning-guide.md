---
title: Zřízení prostředí vyhodnocení Dynamics 365 Commerce
description: Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 11/05/2020
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
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4410938"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="9af1f-103">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9af1f-104">Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9af1f-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="9af1f-105">Než začnete, doporučujeme vám toto téma rychle prohledat, abyste získali představu o tom, co proces vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="9af1f-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="9af1f-106">Prostředí vyhodnocení Commerce nejsou obecně dostupná a jsou poskytována partnerům a zákazníkům na základě žádosti.</span><span class="sxs-lookup"><span data-stu-id="9af1f-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="9af1f-107">Podrobnější informace získáte od kontaktu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9af1f-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="9af1f-108">Přehled</span><span class="sxs-lookup"><span data-stu-id="9af1f-108">Overview</span></span>

<span data-ttu-id="9af1f-109">Chcete-li úspěšně zřídit prostředí pro hodnocení Commerce, musíte vytvořit projekt, který má specifický název a typ produktu.</span><span class="sxs-lookup"><span data-stu-id="9af1f-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="9af1f-110">Prostředí a Commerce Scale Unit (CSU) také mají některé specifické parametry, které musíte použít, když se chystáte ke zřizování e-Commerce později.</span><span class="sxs-lookup"><span data-stu-id="9af1f-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="9af1f-111">Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.</span><span class="sxs-lookup"><span data-stu-id="9af1f-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="9af1f-112">Po úspěšném zřízení prostředí vyhodnocení Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků.</span><span class="sxs-lookup"><span data-stu-id="9af1f-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="9af1f-113">Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="9af1f-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="9af1f-114">Volitelné kroky můžete vždy dokončit později.</span><span class="sxs-lookup"><span data-stu-id="9af1f-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="9af1f-115">Informace o konfiguraci prostředí vyhodnocení Commerce po jeho vytvoření najdete v části [konfigurace prostředí vyhodnocení Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="9af1f-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="9af1f-116">Informace o konfiguraci volitelných funkcí prostředí vyhodnocení Commerce najdete v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="9af1f-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9af1f-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="9af1f-117">Prerequisites</span></span>

<span data-ttu-id="9af1f-118">Aby bylo možné zřídit prostředí vyhodnocení Commerce, musí být zavedeny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="9af1f-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="9af1f-119">Byli jste přijati do programu hodnocení a byla vám udělena kapacita pro prostředí hodnocení.</span><span class="sxs-lookup"><span data-stu-id="9af1f-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="9af1f-120">Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9af1f-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="9af1f-121">Jste stávajícím partnerem Microsoft Dynamics 365 nebo odběratelem a máte možnost vytvořit projekt Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9af1f-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="9af1f-122">Máte přístup správce k vašemu předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který vám může v případě potřeby pomoci.</span><span class="sxs-lookup"><span data-stu-id="9af1f-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="9af1f-123">Máte k dispozici ID klienta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="9af1f-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="9af1f-124">Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="9af1f-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="9af1f-125">Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="9af1f-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="9af1f-126">(Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)</span><span class="sxs-lookup"><span data-stu-id="9af1f-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="9af1f-127">Tento seznam není vyčerpávající.</span><span class="sxs-lookup"><span data-stu-id="9af1f-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="9af1f-128">Pokud se objeví nějaké problémy, měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.</span><span class="sxs-lookup"><span data-stu-id="9af1f-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="9af1f-129">Zřizování prostředí vyhodnocení služby Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="9af1f-130">Tyto postupy vysvětlují, jak zřídit prostředí vyhodnocení Commerce.</span><span class="sxs-lookup"><span data-stu-id="9af1f-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="9af1f-131">Po úspěšném dokončení těchto nastavení bude prostředí vyhodnocení Commerce připraveno na konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="9af1f-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="9af1f-132">Všechny popsané aktivity se objeví na portálu LCS.</span><span class="sxs-lookup"><span data-stu-id="9af1f-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="9af1f-133">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="9af1f-133">Create a new project</span></span>

<span data-ttu-id="9af1f-134">Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="9af1f-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="9af1f-135">Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="9af1f-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="9af1f-136">V pravém podokně proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="9af1f-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="9af1f-137">Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="9af1f-138">Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="9af1f-139">Zadat název a popis šablony a odvětví.</span><span class="sxs-lookup"><span data-stu-id="9af1f-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="9af1f-140">V poli **Název produktu** vyberte **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="9af1f-141">V poli **Verze produktu** vyberte **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="9af1f-142">V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="9af1f-143">Volitelné: Můžete importovat role a uživatele z existujícího projektu.</span><span class="sxs-lookup"><span data-stu-id="9af1f-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="9af1f-144">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-144">Select **Create**.</span></span> <span data-ttu-id="9af1f-145">Zobrazí se projekt.</span><span class="sxs-lookup"><span data-stu-id="9af1f-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="9af1f-146">Přidejte konektor Azure</span><span class="sxs-lookup"><span data-stu-id="9af1f-146">Add the Azure Connector</span></span>

<span data-ttu-id="9af1f-147">Chcete-li přidat Azure Connector do svého projektu LCS, postupujte podle kroků v části [Dokončení procesu integrace Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="9af1f-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="9af1f-148">Nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="9af1f-148">Deploy the environment</span></span>

<span data-ttu-id="9af1f-149">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9af1f-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="9af1f-150">Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny.</span><span class="sxs-lookup"><span data-stu-id="9af1f-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="9af1f-151">V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce - ukázka (10.0.* x* s aktualizací Platform *xx*)\*\* zobrazuje přímo nad polem **Název prostředí**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="9af1f-152">Podrobnosti viz obrázek, který se zobrazí po kroku 8.</span><span class="sxs-lookup"><span data-stu-id="9af1f-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="9af1f-153">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="9af1f-154">Prostředí přidáte výběrem tlačítka **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="9af1f-155">V poli **verze aplikace** vyberte nejaktuálnější verzi.</span><span class="sxs-lookup"><span data-stu-id="9af1f-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="9af1f-156">Pokud máte specifickou potřebu vybrat jinou než nejaktuálnější verzi aplikace, nevybírejte verzi před **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="9af1f-157">V poli **verze platformy** použijte verzi platformy, která je automaticky vybrána pro vybranou verzi aplikace.</span><span class="sxs-lookup"><span data-stu-id="9af1f-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. <span data-ttu-id="9af1f-159">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-159">Select **Next**.</span></span>
1. <span data-ttu-id="9af1f-160">Výberte **Demo** jako topologii prostředí.</span><span class="sxs-lookup"><span data-stu-id="9af1f-160">Select **Demo** as the environment topology.</span></span>

    ![Výběr topologie prostředí 1](./media/project2.png)

1. <span data-ttu-id="9af1f-162">Na stránce **Nasadit prostředí** zadejte název prostředí.</span><span class="sxs-lookup"><span data-stu-id="9af1f-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="9af1f-163">Ponechte Upřesňující nastavení, jak je.</span><span class="sxs-lookup"><span data-stu-id="9af1f-163">Leave the advanced settings as they are.</span></span>

    ![Stránka Nasazení prostředí](./media/project4.png)

1. <span data-ttu-id="9af1f-165">Upravte velikost VM podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="9af1f-165">Adjust the VM size as required.</span></span> <span data-ttu-id="9af1f-166">(Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="9af1f-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="9af1f-167">Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.</span><span class="sxs-lookup"><span data-stu-id="9af1f-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="9af1f-168">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-168">Select **Next**.</span></span>
1. <span data-ttu-id="9af1f-169">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="9af1f-170">Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="9af1f-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="9af1f-171">Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno.</span><span class="sxs-lookup"><span data-stu-id="9af1f-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="9af1f-172">Dokončení pracovních postupů prostředí bude trvat určitou dobu.</span><span class="sxs-lookup"><span data-stu-id="9af1f-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="9af1f-173">Proto se vraťte přibližně za 6 až 9 hodin.</span><span class="sxs-lookup"><span data-stu-id="9af1f-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="9af1f-174">Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="9af1f-175">Inicializace Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="9af1f-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="9af1f-176">Pokud chcete inicializovat CSU, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9af1f-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="9af1f-177">V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="9af1f-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="9af1f-178">V zobrazení prostředí napraco vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="9af1f-179">Zobrazí se podrobnosti o prostředí.</span><span class="sxs-lookup"><span data-stu-id="9af1f-179">The environment details view appears.</span></span>
1. <span data-ttu-id="9af1f-180">V části **Funkce prostředí** vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="9af1f-181">Na kartě **Velkoobchod** vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="9af1f-182">Zobrazí se zobrazení inicializačních parametrů CSU.</span><span class="sxs-lookup"><span data-stu-id="9af1f-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="9af1f-183">V poli **Oblast** vyberte oblast, která je stejná nebo blízká oblasti, do které jste prostředí nasadili.</span><span class="sxs-lookup"><span data-stu-id="9af1f-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="9af1f-184">Nechte pole **Verze** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="9af1f-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="9af1f-185">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="9af1f-186">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="9af1f-187">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="9af1f-188">Vaše CSU byla zařazena do fronty pro zřizování.</span><span class="sxs-lookup"><span data-stu-id="9af1f-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="9af1f-189">Než budete pokračovat, ujistěte se, že je stav CSU **Úspěch**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="9af1f-190">Inicializace trvá přibližně dvě až pět hodin.</span><span class="sxs-lookup"><span data-stu-id="9af1f-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="9af1f-191">Pokud nemůžete najít odkaz **Správa** odkaz v zobrazení podrobností o prostředí, požádejte o pomoc kontaktní osobu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9af1f-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="9af1f-192">Inicializace e-Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-192">Initialize e-Commerce</span></span>

<span data-ttu-id="9af1f-193">Pokud chcete inicializovat e-Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9af1f-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9af1f-194">Na kartě **e-Commerce** zkontrolujte souhlas s vyhodnocením a pak vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="9af1f-195">V poli **Název prostředí e-Commerce** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="9af1f-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="9af1f-196">Uvědomte, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="9af1f-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="9af1f-197">V poli **Název Commerce Scale Unit** vyberte položku CSU v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9af1f-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="9af1f-198">(Seznam by měl mít pouze jednu možnost.)</span><span class="sxs-lookup"><span data-stu-id="9af1f-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="9af1f-199">Pole **Geografie elektronického obchodování** je nastaveno automaticky.</span><span class="sxs-lookup"><span data-stu-id="9af1f-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="9af1f-200">Pokračujte výběrem tlačítka **Další**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="9af1f-201">Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="9af1f-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="9af1f-202">V poli **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy.</span><span class="sxs-lookup"><span data-stu-id="9af1f-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="9af1f-203">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="9af1f-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="9af1f-204">V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzování** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy.</span><span class="sxs-lookup"><span data-stu-id="9af1f-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="9af1f-205">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="9af1f-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="9af1f-206">Možnost **Povolit službu hodnocení a recenzování** nechte nastavenou na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="9af1f-207">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-207">Select **Initialize**.</span></span> <span data-ttu-id="9af1f-208">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="9af1f-209">Vaše inicializace e-Commerce byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="9af1f-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="9af1f-210">Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.</span><span class="sxs-lookup"><span data-stu-id="9af1f-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="9af1f-211">V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:</span><span class="sxs-lookup"><span data-stu-id="9af1f-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="9af1f-212">**Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="9af1f-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="9af1f-213">**Nástroj pro správu webu Commerce** – odkaz na nástroj pro správu webu.</span><span class="sxs-lookup"><span data-stu-id="9af1f-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9af1f-214">Další kroky</span><span class="sxs-lookup"><span data-stu-id="9af1f-214">Next steps</span></span>

<span data-ttu-id="9af1f-215">Chcete-li pokračovat v procesu zřizování a konfigurace prostředí vyhodnocení Commerce, přečtěte si část [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="9af1f-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9af1f-216">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9af1f-216">Additional resources</span></span>

[<span data-ttu-id="9af1f-217">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="9af1f-218">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="9af1f-219">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="9af1f-220">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9af1f-221">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="9af1f-222">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9af1f-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="9af1f-223">Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="9af1f-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="9af1f-224">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9af1f-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="9af1f-225">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9af1f-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
