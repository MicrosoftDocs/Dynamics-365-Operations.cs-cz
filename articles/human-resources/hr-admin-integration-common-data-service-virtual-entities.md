---
title: Konfigurace virtuálních entit Common Data Service
description: Toto téma ukazuje, jak konfigurovat virtuální entity pro Dynamics 365 Human Resources. Můžete generovat a aktualizovat existující virtuální entity a analyzovat vygenerované a dostupné entity.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645594"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="13954-104">Konfigurace virtuálních entit Common Data Service</span><span class="sxs-lookup"><span data-stu-id="13954-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="13954-105">Dynamics 365 Human Resources je virtuální zdroj dat v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="13954-106">Poskytuje úplné operací vytváření, čtení, aktualizace a mazání (CRUD) z Common Data Service a Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="13954-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="13954-107">Data pro virtuální entity nejsou uloženy v Common Data Service, ale v databázi aplikace.</span><span class="sxs-lookup"><span data-stu-id="13954-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="13954-108">Pro povolení operací CRUD v entitách Human Resources z Common Data Service musíte entity zpřístupnit jako virtuální entity v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="13954-109">To vám umožní provádět operace CRUD z Common Data Service a Microsoft Power Platform na datech v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="13954-110">Operace také podporují úplné ověření obchodní logiky Human Resources, aby byla zajištěna integrita dat při jejich zápisu do entit.</span><span class="sxs-lookup"><span data-stu-id="13954-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="13954-111">Dostupné virtuální entity pro Human Resources</span><span class="sxs-lookup"><span data-stu-id="13954-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="13954-112">Všechny entity Open Data Protocol (OData) v Human Resources jsou k dispozici jako virtuální entity v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="13954-113">Jsou k dispozici i v Power Platform.</span><span class="sxs-lookup"><span data-stu-id="13954-113">They're also available in Power Platform.</span></span> <span data-ttu-id="13954-114">Nyní můžete vytvářet aplikace a prostředí s daty přímo z Human Resources s plnou schopností CRUD, a to bez kopírování nebo synchronizace dat do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="13954-115">Můžete používat portály Power Apps k vytváření externích webů, které umožňují scénáře spolupráce pro obchodní procesy v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="13954-116">Můžete zobrazit seznam virtuálních entit povolených v prostředí a začít pracovat s entitami v [Power Apps](https://make.powerapps.com), v řešení **Virtuální entity Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="13954-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Virtuální entity Dynamics 365 HR ve Windows Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="13954-118">Virtuální entity versus přirozené entity</span><span class="sxs-lookup"><span data-stu-id="13954-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="13954-119">Virtuální entity pro Human Resources nejsou totéž jako přirozené entity Common Data Service vytvořené pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="13954-120">Přirozené entity pro Human Resources jsou generovány samostatně a udržovány v řešení HCM Common v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="13954-121">U přirozených entit jsou data uložena v Common Data Service a vyžaduje synchronizaci s databází aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="13954-122">Seznam přirozených entit Common Data Service pro Human Resources viz [Entity Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="13954-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="13954-123">Nastavení</span><span class="sxs-lookup"><span data-stu-id="13954-123">Setup</span></span>

<span data-ttu-id="13954-124">Povolte virtuální entity ve vašem prostředí provedením těchto kroků nastavení.</span><span class="sxs-lookup"><span data-stu-id="13954-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="13954-125">Povolení virtuálních entit v Human Resources</span><span class="sxs-lookup"><span data-stu-id="13954-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="13954-126">Nejprve musíte povolit virtuální entity v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="13954-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="13954-127">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="13954-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="13954-128">Vyberte dlaždici **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="13954-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="13954-129">Vyberte **Podpora virtuálních entit v HR/CDS** a potom vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="13954-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="13954-130">Další informace o povolení a zákazu funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="13954-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="13954-131">Registrace aplikace v Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="13954-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="13954-132">Musíte registrovat instanci Human Resources v portálu Azure, aby platforma identit od Microsoftu mohla poskytovat ověřovací a autorizační služby pro tuto aplikaci a uživatele.</span><span class="sxs-lookup"><span data-stu-id="13954-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="13954-133">Další informace o registraci aplikací v Azure najdete v tématu [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="13954-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="13954-134">Otevřete [Microsoft Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="13954-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="13954-135">V seznamu služeb Azure zvolte **Registrace aplikací**.</span><span class="sxs-lookup"><span data-stu-id="13954-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="13954-136">Vyberte **Nová registrace**.</span><span class="sxs-lookup"><span data-stu-id="13954-136">Select **New registration**.</span></span>

4. <span data-ttu-id="13954-137">V poli **Název** zadejte popisný název aplikace.</span><span class="sxs-lookup"><span data-stu-id="13954-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="13954-138">Například **Virtuální entity Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="13954-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="13954-139">V poli **URI přesměrování** zadejte adresu URL oboru názvů vaší instance Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="13954-140">Vyberte **Registrovat**.</span><span class="sxs-lookup"><span data-stu-id="13954-140">Select **Register**.</span></span>

7. <span data-ttu-id="13954-141">Po dokončení registrace se na webu Azure Portal zobrazí podokno **Přehled** pro registraci aplikace, které obsahuje jeho **ID aplikace (klienta)**.</span><span class="sxs-lookup"><span data-stu-id="13954-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="13954-142">V tuto chvíli si **ID aplikace (klienta)** poznamenejte.</span><span class="sxs-lookup"><span data-stu-id="13954-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="13954-143">Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních entit](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="13954-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="13954-144">V levém navigačním podokně vyberte **Certifikáty a tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="13954-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="13954-145">V části **Tajné klíče klienta** stránky vyberte **Nový tajný klíč klienta**.</span><span class="sxs-lookup"><span data-stu-id="13954-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="13954-146">Zadejte popis, vyberte dobu trvání a vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="13954-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="13954-147">Zaznamenejte hodnotu tajného klíče.</span><span class="sxs-lookup"><span data-stu-id="13954-147">Record the secret's value.</span></span> <span data-ttu-id="13954-148">Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních entit](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="13954-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="13954-149">V tuto chvíli si nezapomeňte hodnotu tajného klíče poznamenat.</span><span class="sxs-lookup"><span data-stu-id="13954-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="13954-150">Po opuštění této stránky se tajný klíč už nikdy nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="13954-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="13954-151">Instalace aplikaci Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="13954-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="13954-152">Nainstalujte si aplikaci Dynamics 365 HR Virtual Entity do svého prostředí Power Apps, abyste si nasadili balíček řešení virtuální entity do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="13954-153">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="13954-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="13954-154">V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="13954-155">V části **Zdroje** této stránky vyberte **Aplikace Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="13954-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="13954-156">Vyberte akci **Nainstalovat aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="13954-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="13954-157">Vyberte **Dynamics 365 HR Virtual Entity** a pak **Další**.</span><span class="sxs-lookup"><span data-stu-id="13954-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="13954-158">Přečtěte si podmínky služby a potvrďte svůj souhlas.</span><span class="sxs-lookup"><span data-stu-id="13954-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="13954-159">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="13954-159">Select **Install**.</span></span>

<span data-ttu-id="13954-160">Instalace trvá několik minut.</span><span class="sxs-lookup"><span data-stu-id="13954-160">The install takes a few minutes.</span></span> <span data-ttu-id="13954-161">Po jejím dokončení pokračujte dalšími kroky.</span><span class="sxs-lookup"><span data-stu-id="13954-161">When it completes, continue to the next steps.</span></span>

![Instalace aplikace Dynamics 365 HR Virtual Entity z centra pro správu Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="13954-163">Konfigurace zdroje dat virtuálních entit</span><span class="sxs-lookup"><span data-stu-id="13954-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="13954-164">Dalším krokem je konfigurace zdroje dat virtuálních entit v prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13954-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="13954-165">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="13954-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="13954-166">V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="13954-167">Vyberte **URL prostředí** v části **Podrobnosti** této stránky.</span><span class="sxs-lookup"><span data-stu-id="13954-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="13954-168">V **Centru stavu řešení** vyberte ikonu **Rozšířené hledání** v pravém horním rohu stránky aplikace.</span><span class="sxs-lookup"><span data-stu-id="13954-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="13954-169">Na stránce **Rozšířené hledání** vyberte v rozevíracím seznamu **Hledat** položku **Konfigurace zdrojů virtuálních dat ve Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="13954-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="13954-170">Vyberte **Výsledky**</span><span class="sxs-lookup"><span data-stu-id="13954-170">Select **Results**.</span></span>

7. <span data-ttu-id="13954-171">Vyberte záznam **Zdroj dat Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="13954-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="13954-172">Zadejte požadované informace pro konfiguraci zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="13954-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="13954-173">**Cílová adresa URL**: URL vašeho oboru názvů pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13954-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="13954-174">Formát cílové adresy URL je:</span><span class="sxs-lookup"><span data-stu-id="13954-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="13954-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="13954-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="13954-176">Například:</span><span class="sxs-lookup"><span data-stu-id="13954-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="13954-177">Nezapomeňte uvést znak „**/**“ na konci adresy URL, aby nedošlo k chybě.</span><span class="sxs-lookup"><span data-stu-id="13954-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="13954-178">**ID tenanta**: ID tenanta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="13954-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="13954-179">**ID aplikace AAD**: ID aplikace (klienta) vytvořené pro aplikaci registrovanou přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="13954-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="13954-180">Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="13954-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="13954-181">**Tajný klíč aplikace AAD**: Tajný klíč klienta vytvořený pro aplikaci registrovanou přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="13954-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="13954-182">Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="13954-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Zdroj dat Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="13954-184">Zvolte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="13954-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="13954-185">Udělení oprávnění aplikací v Human Resources</span><span class="sxs-lookup"><span data-stu-id="13954-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="13954-186">Udělte oprávnění těmto dvěma aplikacím Azure AD v oblasti Human Resources:</span><span class="sxs-lookup"><span data-stu-id="13954-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="13954-187">Aplikace vytvořená pro vašeho tenanta přes Microsoft Azure Portal</span><span class="sxs-lookup"><span data-stu-id="13954-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="13954-188">Aplikace Dynamics 365 HR Virtual Entity nainstalovaná v prostředí Power Apps</span><span class="sxs-lookup"><span data-stu-id="13954-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="13954-189">V Human Resources otevřete stránku **Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="13954-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="13954-190">Zvolte **Nový** pro vytvoření nového záznamu aplikace:</span><span class="sxs-lookup"><span data-stu-id="13954-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="13954-191">V poli **ID klienta** zadejte ID klienta aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="13954-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="13954-192">V poli **Název** zadejte název aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="13954-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="13954-193">V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13954-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="13954-194">Zvolte **Nový** pro vytvoření druhého záznamu aplikace:</span><span class="sxs-lookup"><span data-stu-id="13954-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="13954-195">**ID klienta**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="13954-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="13954-196">**Název**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="13954-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="13954-197">V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="13954-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="13954-198">Generování virtuálních entit</span><span class="sxs-lookup"><span data-stu-id="13954-198">Generate virtual entities</span></span>

<span data-ttu-id="13954-199">Po dokončení instalace můžete vybrat virtuální entity, které chcete vygenerovat a povolit ve vaší instanci Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="13954-200">V Human Resources otevřete stránku **Integrace Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="13954-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="13954-201">Vyberte kartu **Virtuální entity**.</span><span class="sxs-lookup"><span data-stu-id="13954-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="13954-202">Přepínač **Povolte virtuální entitu** bude nastaven na **Ano** automaticky po dokončení všech požadovaných nastavení.</span><span class="sxs-lookup"><span data-stu-id="13954-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="13954-203">Pokud je přepínač nastaven na **Ne**, zkontrolujte kroky v předchozích částech tohoto dokumentu a ujistěte se, že jsou dokončeny všechny nezbytné předpoklady.</span><span class="sxs-lookup"><span data-stu-id="13954-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="13954-204">Vyberte entitu nebo entity, které chcete generovat v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="13954-205">Vyberte **Generovat/aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="13954-205">Select **Generate/refresh**.</span></span>

![Integrace Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="13954-207">Zkontrolujte stav generování entity</span><span class="sxs-lookup"><span data-stu-id="13954-207">Check entity generation status</span></span>

<span data-ttu-id="13954-208">Virtuální entity jsou generovány v Common Data Service prostřednictvím asynchronního procesu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="13954-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="13954-209">Aktualizace na displeji procesu v centru akcí.</span><span class="sxs-lookup"><span data-stu-id="13954-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="13954-210">Podrobnosti o procesu, včetně protokolů chyb, se objeví na stránce **Procesní automatizace**.</span><span class="sxs-lookup"><span data-stu-id="13954-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="13954-211">V Human Resources otevřete stránku **Procesní automatizace**.</span><span class="sxs-lookup"><span data-stu-id="13954-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="13954-212">Vyberte kartu **Procesy na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="13954-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="13954-213">Vyberte **Proces na pozadí asynchronní operace s dotazováním virtuální entity**.</span><span class="sxs-lookup"><span data-stu-id="13954-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="13954-214">Vyberte **Zobrazit nejnovější výsledky**.</span><span class="sxs-lookup"><span data-stu-id="13954-214">Select **View most recent results**.</span></span>

<span data-ttu-id="13954-215">V posuvném podokně se zobrazují nejnovější výsledky provádění procesu.</span><span class="sxs-lookup"><span data-stu-id="13954-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="13954-216">Můžete zobrazit protokol procesu, včetně všech chyb vrácených z Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="13954-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="13954-217">Viz také</span><span class="sxs-lookup"><span data-stu-id="13954-217">See also</span></span>

[<span data-ttu-id="13954-218">Co je Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="13954-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="13954-219">Přehled entit</span><span class="sxs-lookup"><span data-stu-id="13954-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="13954-220">Přehled vztahů mezi entitami</span><span class="sxs-lookup"><span data-stu-id="13954-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="13954-221">Vytváření a úpravy virtuálních entit, které obsahují data z externího zdroje dat</span><span class="sxs-lookup"><span data-stu-id="13954-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="13954-222">Co jsou portály Power Apps?</span><span class="sxs-lookup"><span data-stu-id="13954-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="13954-223">Přehled vytváření aplikací v Power Apps</span><span class="sxs-lookup"><span data-stu-id="13954-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
