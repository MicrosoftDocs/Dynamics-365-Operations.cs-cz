---
title: Zřízení prostředí vyhodnocení Dynamics 365 Commerce
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
ms.openlocfilehash: 8cda79a6be1aca7ad3826b9409e110524e6560e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969894"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="8d2dc-103">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d2dc-104">Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="8d2dc-105">Než začnete, doporučujeme vám toto téma rychle prohledat, abyste získali představu o tom, co proces vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="8d2dc-106">Prostředí vyhodnocení Commerce nejsou obecně dostupná a jsou poskytována partnerům a zákazníkům na základě žádosti.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="8d2dc-107">Podrobnější informace získáte od kontaktu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="8d2dc-108">Přehled</span><span class="sxs-lookup"><span data-stu-id="8d2dc-108">Overview</span></span>

<span data-ttu-id="8d2dc-109">Chcete-li úspěšně zřídit prostředí pro hodnocení Commerce, musíte vytvořit projekt, který má specifický název a typ produktu.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="8d2dc-110">Prostředí a Commerce Scale Unit (CSU) také mají některé specifické parametry, které musíte použít, když se chystáte ke zřizování e-Commerce později.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="8d2dc-111">Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="8d2dc-112">Po úspěšném zřízení prostředí vyhodnocení Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="8d2dc-113">Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="8d2dc-114">Volitelné kroky můžete vždy dokončit později.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="8d2dc-115">Informace o konfiguraci prostředí vyhodnocení Commerce po jeho vytvoření najdete v části [konfigurace prostředí vyhodnocení Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="8d2dc-116">Informace o konfiguraci volitelných funkcí prostředí vyhodnocení Commerce najdete v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d2dc-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="8d2dc-117">Prerequisites</span></span>

<span data-ttu-id="8d2dc-118">Aby bylo možné zřídit prostředí vyhodnocení Commerce, musí být zavedeny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="8d2dc-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="8d2dc-119">Byli jste přijati do programu hodnocení a byla vám udělena kapacita pro prostředí hodnocení.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="8d2dc-120">Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="8d2dc-121">Jste stávajícím partnerem Microsoft Dynamics 365 nebo odběratelem a máte možnost vytvořit projekt Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="8d2dc-122">Máte přístup správce k vašemu předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který vám může v případě potřeby pomoci.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="8d2dc-123">Máte k dispozici ID klienta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="8d2dc-124">Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="8d2dc-125">Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="8d2dc-126">(Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="8d2dc-127">Tento seznam není vyčerpávající.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="8d2dc-128">Pokud se objeví nějaké problémy, měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="8d2dc-129">Zřizování prostředí vyhodnocení služby Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="8d2dc-130">Tyto postupy vysvětlují, jak zřídit prostředí vyhodnocení Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="8d2dc-131">Po úspěšném dokončení těchto nastavení bude prostředí vyhodnocení Commerce připraveno na konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="8d2dc-132">Všechny popsané aktivity se objeví na portálu LCS.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="8d2dc-133">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="8d2dc-133">Create a new project</span></span>

<span data-ttu-id="8d2dc-134">Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="8d2dc-135">Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="8d2dc-136">V pravém podokně proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="8d2dc-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="8d2dc-137">Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="8d2dc-138">Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="8d2dc-139">Zadat název a popis šablony a odvětví.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="8d2dc-140">V poli **Název produktu** vyberte **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="8d2dc-141">V poli **Verze produktu** vyberte **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="8d2dc-142">V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="8d2dc-143">Volitelné: Můžete importovat role a uživatele z existujícího projektu.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="8d2dc-144">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-144">Select **Create**.</span></span> <span data-ttu-id="8d2dc-145">Zobrazí se projekt.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="8d2dc-146">Přidejte konektor Azure</span><span class="sxs-lookup"><span data-stu-id="8d2dc-146">Add the Azure Connector</span></span>

<span data-ttu-id="8d2dc-147">Chcete-li přidat Azure Connector do svého projektu LCS, postupujte podle kroků v části [Dokončení procesu integrace Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="8d2dc-148">Nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="8d2dc-148">Deploy the environment</span></span>

<span data-ttu-id="8d2dc-149">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="8d2dc-150">Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="8d2dc-151">V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce - ukázka (10.0.* x* s aktualizací Platform *xx*)\*\* zobrazuje přímo nad polem **Název prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="8d2dc-152">Podrobnosti viz obrázek, který se zobrazí po kroku 8.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="8d2dc-153">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8d2dc-154">Prostředí přidáte výběrem tlačítka **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="8d2dc-155">V poli **verze aplikace** vyberte nejaktuálnější verzi.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="8d2dc-156">Pokud máte specifickou potřebu vybrat jinou než nejaktuálnější verzi aplikace, nevybírejte verzi před **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="8d2dc-157">V poli **verze platformy** použijte verzi platformy, která je automaticky vybrána pro vybranou verzi aplikace.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. <span data-ttu-id="8d2dc-159">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-159">Select **Next**.</span></span>
1. <span data-ttu-id="8d2dc-160">Výberte **Demo** jako topologii prostředí.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-160">Select **Demo** as the environment topology.</span></span>

    ![Výběr topologie prostředí 1](./media/project2.png)

1. <span data-ttu-id="8d2dc-162">Na stránce **Nasadit prostředí** zadejte název prostředí.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="8d2dc-163">Ponechte Upřesňující nastavení, jak je.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-163">Leave the advanced settings as they are.</span></span>

    ![Stránka Nasazení prostředí](./media/project4.png)

1. <span data-ttu-id="8d2dc-165">Upravte velikost VM podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-165">Adjust the VM size as required.</span></span> <span data-ttu-id="8d2dc-166">(Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="8d2dc-167">Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="8d2dc-168">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-168">Select **Next**.</span></span>
1. <span data-ttu-id="8d2dc-169">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="8d2dc-170">Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="8d2dc-171">Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="8d2dc-172">Dokončení pracovních postupů prostředí bude trvat určitou dobu.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="8d2dc-173">Proto se vraťte přibližně za 6 až 9 hodin.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="8d2dc-174">Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="8d2dc-175">Inicializace Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="8d2dc-176">Pokud chcete inicializovat CSU, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-176">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="8d2dc-177">V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="8d2dc-178">V zobrazení prostředí napraco vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="8d2dc-179">Zobrazí se podrobnosti o prostředí.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-179">The environment details view appears.</span></span>
1. <span data-ttu-id="8d2dc-180">V části **Funkce prostředí** vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="8d2dc-181">Na kartě **Velkoobchod** vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="8d2dc-182">Zobrazí se zobrazení inicializačních parametrů CSU.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="8d2dc-183">V poli **Oblast** vyberte oblast, která je stejná nebo blízká oblasti, do které jste prostředí nasadili.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="8d2dc-184">Nechte pole **Verze** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="8d2dc-185">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="8d2dc-186">Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="8d2dc-187">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="8d2dc-188">Vaše CSU byla zařazena do fronty pro zřizování.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="8d2dc-189">Než budete pokračovat, ujistěte se, že je stav CSU **Úspěch**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="8d2dc-190">Inicializace trvá přibližně dvě až pět hodin.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="8d2dc-191">Pokud nemůžete najít odkaz **Správa** odkaz v zobrazení podrobností o prostředí, požádejte o pomoc kontaktní osobu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="8d2dc-192">Při počátečním zpracování se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="8d2dc-192">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="8d2dc-193">Vyhodnocovací (demo/testovací) prostředí musí registrovat aplikaci konektoru jednotky škálování \<application ID\> v centrále.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-193">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="8d2dc-194">Pokud se inicializace CSU nezdaří a zobrazí se tato chybová zpráva, poznamenejte si ID aplikace, což je globálně jedinečný identifikátor (GUID), a poté podle pokynů v další části zaregistrujte aplikaci nasazení CSU v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-194">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="8d2dc-195">Zaregistrujte aplikaci nasazení CSU v obchodním ústředí (je-li požadováno)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-195">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="8d2dc-196">Chcete-li zaregistrovat aplikaci nasazení CSU v obchodním ústředí, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-196">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8d2dc-197">V centrále Commerce přejděte na **Správa systému \> Nastavení \> Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-197">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="8d2dc-198">Ve sloupci **ID klienta** zadejte ID aplikace z chybové zprávy inicializace CSU, kterou jste obdrželi.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-198">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="8d2dc-199">Ve sloupci **Název** zadejte libovolný popisný text (například **CSU Eval**).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-199">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="8d2dc-200">Ve sloupci **ID uživatele** zadejte **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-200">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="8d2dc-201">Opakujte inicializaci a nasazení CSU z LCS.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-201">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="8d2dc-202">Inicializace e-Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-202">Initialize e-Commerce</span></span>

<span data-ttu-id="8d2dc-203">Pokud chcete inicializovat e-Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-203">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8d2dc-204">Na kartě **e-Commerce** zkontrolujte souhlas s vyhodnocením a pak vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-204">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="8d2dc-205">V poli **Název prostředí e-Commerce** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-205">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="8d2dc-206">Uvědomte, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-206">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="8d2dc-207">V poli **Název Commerce Scale Unit** vyberte položku CSU v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-207">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="8d2dc-208">(Seznam by měl mít pouze jednu možnost.)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-208">(The list should have only one option.)</span></span>

    <span data-ttu-id="8d2dc-209">Pole **Geografie elektronického obchodování** je nastaveno automaticky.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-209">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="8d2dc-210">Pokračujte výběrem tlačítka **Další**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-210">Select **Next** to continue.</span></span>
1. <span data-ttu-id="8d2dc-211">Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-211">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="8d2dc-212">V poli **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-212">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="8d2dc-213">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-213">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="8d2dc-214">V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzování** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-214">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="8d2dc-215">V seznamu vyberte správnou skupinu zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-215">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="8d2dc-216">Možnost **Povolit službu hodnocení a recenzování** nechte nastavenou na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-216">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="8d2dc-217">Vyberte **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-217">Select **Initialize**.</span></span> <span data-ttu-id="8d2dc-218">Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-218">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="8d2dc-219">Vaše inicializace e-Commerce byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-219">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="8d2dc-220">Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-220">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="8d2dc-221">V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:</span><span class="sxs-lookup"><span data-stu-id="8d2dc-221">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="8d2dc-222">**Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-222">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="8d2dc-223">**Nástroj pro správu webu Commerce** – odkaz na nástroj pro správu webu.</span><span class="sxs-lookup"><span data-stu-id="8d2dc-223">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8d2dc-224">Další kroky</span><span class="sxs-lookup"><span data-stu-id="8d2dc-224">Next steps</span></span>

<span data-ttu-id="8d2dc-225">Chcete-li pokračovat v procesu zřizování a konfigurace prostředí vyhodnocení Commerce, přečtěte si část [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="8d2dc-225">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d2dc-226">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="8d2dc-226">Additional resources</span></span>

[<span data-ttu-id="8d2dc-227">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-227">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8d2dc-228">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-228">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="8d2dc-229">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-229">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8d2dc-230">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-230">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="8d2dc-231">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-231">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8d2dc-232">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-232">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8d2dc-233">Commerce Scale Unit (cloud)</span><span class="sxs-lookup"><span data-stu-id="8d2dc-233">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8d2dc-234">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8d2dc-234">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8d2dc-235">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d2dc-235">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
