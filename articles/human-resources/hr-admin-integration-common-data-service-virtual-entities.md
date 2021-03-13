---
title: Konfigurace virtuálních tabulek Dataverse
description: Toto téma ukazuje, jak konfigurovat virtuální tabulky pro Dynamics 365 Human Resources. Můžete generovat a aktualizovat existující virtuální tabulky a analyzovat vygenerované a dostupné tabulky.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: cd299b51e38cc30c3e18f3ef9de1f43fa817b840
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111827"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="5574d-104">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="5574d-104">Configure Dataverse virtual tables</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5574d-105">Dynamics 365 Human Resources je virtuální zdroj dat v Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="5574d-106">Poskytuje úplné operací vytváření, čtení, aktualizace a mazání (CRUD) z Dataverse a Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="5574d-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="5574d-107">Data pro virtuální tabulky nejsou uloženy v Dataverse, ale v databázi aplikace.</span><span class="sxs-lookup"><span data-stu-id="5574d-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="5574d-108">Pro povolení operací CRUD v entitách Human Resources z Dataverse musíte entity zpřístupnit jako virtuální tabulky v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="5574d-109">To vám umožní provádět operace CRUD z Dataverse a Microsoft Power Platform na datech v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="5574d-110">Operace také podporují úplné ověření obchodní logiky Human Resources, aby byla zajištěna integrita dat při jejich zápisu do entit.</span><span class="sxs-lookup"><span data-stu-id="5574d-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="5574d-111">Entity Human Resources odpovídají Dataverse tabulkám.</span><span class="sxs-lookup"><span data-stu-id="5574d-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="5574d-112">Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="5574d-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="5574d-113">Dostupné virtuální tabulky pro Human Resources</span><span class="sxs-lookup"><span data-stu-id="5574d-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="5574d-114">Všechny entity Open Data Protocol (OData) v Human Resources jsou k dispozici jako virtuální tabulky v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="5574d-115">Jsou k dispozici i v Power Platform.</span><span class="sxs-lookup"><span data-stu-id="5574d-115">They're also available in Power Platform.</span></span> <span data-ttu-id="5574d-116">Nyní můžete vytvářet aplikace a prostředí s daty přímo z Human Resources s plnou schopností CRUD, a to bez kopírování nebo synchronizace dat do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="5574d-117">Můžete používat portály Power Apps k vytváření externích webů, které umožňují scénáře spolupráce pro obchodní procesy v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="5574d-118">Můžete zobrazit seznam virtuálních tabulek povolených v prostředí a začít pracovat s tabulkami v [Power Apps](https://make.powerapps.com), v řešení **Virtuální tabulky Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="5574d-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Virtuální tabulky Dynamics 365 HR ve Windows Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="5574d-120">Virtuální tabulky versus nativní tabulky</span><span class="sxs-lookup"><span data-stu-id="5574d-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="5574d-121">Virtuální tabulky pro Human Resources nejsou totéž jako nativni tabulky Dataverse vytvořené pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="5574d-122">Nativní tabulky pro Human Resources jsou generovány samostatně a udržovány v řešení HCM Common v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="5574d-123">U nativních tabulek jsou data uložena v Dataverse a vyžaduje synchronizaci s databází aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="5574d-124">Seznam nativních tabulek Dataverse pro Human Resources viz [Tabulky Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="5574d-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="5574d-125">Nastavení</span><span class="sxs-lookup"><span data-stu-id="5574d-125">Setup</span></span>

<span data-ttu-id="5574d-126">Povolte virtuální tabulky ve vašem prostředí provedením těchto kroků nastavení.</span><span class="sxs-lookup"><span data-stu-id="5574d-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="5574d-127">Povolení virtuálních tabulek v Human Resources</span><span class="sxs-lookup"><span data-stu-id="5574d-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="5574d-128">Nejprve musíte povolit virtuální tabulky v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="5574d-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="5574d-129">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="5574d-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="5574d-130">Vyberte dlaždici **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="5574d-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="5574d-131">Vyberte **Podpora virtuálních tabulek v HR v Dataverse** a potom vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="5574d-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="5574d-132">Další informace o povolení a zákazu funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="5574d-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="5574d-133">Registrace aplikace v Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="5574d-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="5574d-134">Musíte registrovat instanci Human Resources v portálu Azure, aby platforma identit od Microsoftu mohla poskytovat ověřovací a autorizační služby pro tuto aplikaci a uživatele.</span><span class="sxs-lookup"><span data-stu-id="5574d-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="5574d-135">Další informace o registraci aplikací v Azure najdete v tématu [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="5574d-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="5574d-136">Otevřete [Microsoft Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="5574d-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="5574d-137">V seznamu služeb Azure zvolte **Registrace aplikací**.</span><span class="sxs-lookup"><span data-stu-id="5574d-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="5574d-138">Vyberte **Nová registrace**.</span><span class="sxs-lookup"><span data-stu-id="5574d-138">Select **New registration**.</span></span>

4. <span data-ttu-id="5574d-139">V poli **Název** zadejte popisný název aplikace.</span><span class="sxs-lookup"><span data-stu-id="5574d-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="5574d-140">Například **Virtuální tabulky Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="5574d-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="5574d-141">V poli **URI přesměrování** zadejte adresu URL oboru názvů vaší instance Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="5574d-142">Vyberte **Registrovat**.</span><span class="sxs-lookup"><span data-stu-id="5574d-142">Select **Register**.</span></span>

7. <span data-ttu-id="5574d-143">Po dokončení registrace se na webu Azure Portal zobrazí podokno **Přehled** pro registraci aplikace, které obsahuje jeho **ID aplikace (klienta)**.</span><span class="sxs-lookup"><span data-stu-id="5574d-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="5574d-144">V tuto chvíli si **ID aplikace (klienta)** poznamenejte.</span><span class="sxs-lookup"><span data-stu-id="5574d-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="5574d-145">Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních tabulek](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="5574d-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="5574d-146">V levém navigačním podokně vyberte **Certifikáty a tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="5574d-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="5574d-147">V části **Tajné klíče klienta** stránky vyberte **Nový tajný klíč klienta**.</span><span class="sxs-lookup"><span data-stu-id="5574d-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="5574d-148">Zadejte popis, vyberte dobu trvání a vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5574d-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="5574d-149">Zaznamenejte hodnotu tajného klíče.</span><span class="sxs-lookup"><span data-stu-id="5574d-149">Record the secret's value.</span></span> <span data-ttu-id="5574d-150">Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních tabulek](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="5574d-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5574d-151">V tuto chvíli si nezapomeňte hodnotu tajného klíče poznamenat.</span><span class="sxs-lookup"><span data-stu-id="5574d-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="5574d-152">Po opuštění této stránky se tajný klíč už nikdy nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="5574d-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="5574d-153">Instalace aplikaci Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="5574d-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="5574d-154">Nainstalujte si aplikaci Dynamics 365 HR Virtual Table do svého prostředí Power Apps, abyste si nasadili balíček řešení virtuální tabulky do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="5574d-155">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="5574d-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="5574d-156">V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="5574d-157">V části **Zdroje** této stránky vyberte **Aplikace Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5574d-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="5574d-158">Vyberte akci **Nainstalovat aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="5574d-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="5574d-159">Vyberte **Dynamics 365 HR Virtual Table** a pak **Další**.</span><span class="sxs-lookup"><span data-stu-id="5574d-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="5574d-160">Přečtěte si podmínky služby a potvrďte svůj souhlas.</span><span class="sxs-lookup"><span data-stu-id="5574d-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="5574d-161">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="5574d-161">Select **Install**.</span></span>

<span data-ttu-id="5574d-162">Instalace trvá několik minut.</span><span class="sxs-lookup"><span data-stu-id="5574d-162">The install takes a few minutes.</span></span> <span data-ttu-id="5574d-163">Po jejím dokončení pokračujte dalšími kroky.</span><span class="sxs-lookup"><span data-stu-id="5574d-163">When it completes, continue to the next steps.</span></span>

![Instalace aplikace Dynamics 365 HR Virtual Table z centra pro správu Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="5574d-165">Konfigurace zdroje dat virtuálních tabulek</span><span class="sxs-lookup"><span data-stu-id="5574d-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="5574d-166">Dalším krokem je konfigurace zdroje dat virtuálních tabulek v prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5574d-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="5574d-167">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="5574d-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="5574d-168">V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="5574d-169">Vyberte **URL prostředí** v části **Podrobnosti** této stránky.</span><span class="sxs-lookup"><span data-stu-id="5574d-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="5574d-170">V **Centru stavu řešení** vyberte ikonu **Rozšířené hledání** v pravém horním rohu stránky aplikace.</span><span class="sxs-lookup"><span data-stu-id="5574d-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="5574d-171">Na stránce **Rozšířené hledání** vyberte v rozevíracím seznamu **Hledat** položku **Konfigurace zdrojů virtuálních dat ve Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="5574d-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="5574d-172">Vyberte **Výsledky**</span><span class="sxs-lookup"><span data-stu-id="5574d-172">Select **Results**.</span></span>

7. <span data-ttu-id="5574d-173">Vyberte záznam **Zdroj dat Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="5574d-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="5574d-174">Zadejte požadované informace pro konfiguraci zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="5574d-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="5574d-175">**Cílová adresa URL**: URL vašeho oboru názvů pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5574d-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="5574d-176">Formát cílové adresy URL je:</span><span class="sxs-lookup"><span data-stu-id="5574d-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="5574d-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="5574d-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="5574d-178">Například:</span><span class="sxs-lookup"><span data-stu-id="5574d-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="5574d-179">Nezapomeňte uvést znak „**/**“ na konci adresy URL, aby nedošlo k chybě.</span><span class="sxs-lookup"><span data-stu-id="5574d-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="5574d-180">**ID tenanta**: ID tenanta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5574d-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="5574d-181">**ID aplikace AAD**: ID aplikace (klienta) vytvořené pro aplikaci registrovanou přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="5574d-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="5574d-182">Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="5574d-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="5574d-183">**Tajný klíč aplikace AAD**: Tajný klíč klienta vytvořený pro aplikaci registrovanou přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="5574d-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="5574d-184">Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="5574d-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Zdroj dat Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="5574d-186">Zvolte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="5574d-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="5574d-187">Udělení oprávnění aplikací v Human Resources</span><span class="sxs-lookup"><span data-stu-id="5574d-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="5574d-188">Udělte oprávnění těmto dvěma aplikacím Azure AD v oblasti Human Resources:</span><span class="sxs-lookup"><span data-stu-id="5574d-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="5574d-189">Aplikace vytvořená pro vašeho tenanta přes Microsoft Azure Portal</span><span class="sxs-lookup"><span data-stu-id="5574d-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="5574d-190">Aplikace Dynamics 365 HR Virtual Table nainstalovaná v prostředí Power Apps</span><span class="sxs-lookup"><span data-stu-id="5574d-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="5574d-191">V Human Resources otevřete stránku **Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="5574d-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="5574d-192">Zvolte **Nový** pro vytvoření nového záznamu aplikace:</span><span class="sxs-lookup"><span data-stu-id="5574d-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="5574d-193">V poli **ID klienta** zadejte ID klienta aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="5574d-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="5574d-194">V poli **Název** zadejte název aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="5574d-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="5574d-195">V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5574d-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="5574d-196">Zvolte **Nový** pro vytvoření druhého záznamu aplikace:</span><span class="sxs-lookup"><span data-stu-id="5574d-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="5574d-197">**ID klienta**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="5574d-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="5574d-198">**Název**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="5574d-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="5574d-199">V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5574d-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="5574d-200">Generování virtuálních tabulek</span><span class="sxs-lookup"><span data-stu-id="5574d-200">Generate virtual tables</span></span>

<span data-ttu-id="5574d-201">Po dokončení instalace můžete vybrat virtuální tabulku, které chcete vygenerovat a povolit ve vaší instanci Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="5574d-202">V Human Resources otevřete stránku **Integrace Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="5574d-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="5574d-203">Vyberte kartu **Virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="5574d-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="5574d-204">Přepínač **Povolte virtuální tabulku** bude nastaven na **Ano** automaticky po dokončení všech požadovaných nastavení.</span><span class="sxs-lookup"><span data-stu-id="5574d-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="5574d-205">Pokud je přepínač nastaven na **Ne**, zkontrolujte kroky v předchozích částech tohoto dokumentu a ujistěte se, že jsou dokončeny všechny nezbytné předpoklady.</span><span class="sxs-lookup"><span data-stu-id="5574d-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="5574d-206">Vyberte tabulku nebo tabulku, kterou chcete generovat v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="5574d-207">Vyberte **Generovat/aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="5574d-207">Select **Generate/refresh**.</span></span>

![Integrace Dataverse](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="5574d-209">Zkontrolujte stav generování tabulky</span><span class="sxs-lookup"><span data-stu-id="5574d-209">Check table generation status</span></span>

<span data-ttu-id="5574d-210">Virtuální tabulky jsou generovány v Dataverse prostřednictvím asynchronního procesu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="5574d-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="5574d-211">Aktualizace na displeji procesu v centru akcí.</span><span class="sxs-lookup"><span data-stu-id="5574d-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="5574d-212">Podrobnosti o procesu, včetně protokolů chyb, se objeví na stránce **Procesní automatizace**.</span><span class="sxs-lookup"><span data-stu-id="5574d-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="5574d-213">V Human Resources otevřete stránku **Procesní automatizace**.</span><span class="sxs-lookup"><span data-stu-id="5574d-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="5574d-214">Vyberte kartu **Procesy na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="5574d-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="5574d-215">Vyberte **Proces na pozadí asynchronní operace s dotazováním virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="5574d-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="5574d-216">Vyberte **Zobrazit nejnovější výsledky**.</span><span class="sxs-lookup"><span data-stu-id="5574d-216">Select **View most recent results**.</span></span>

<span data-ttu-id="5574d-217">V posuvném podokně se zobrazují nejnovější výsledky provádění procesu.</span><span class="sxs-lookup"><span data-stu-id="5574d-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="5574d-218">Můžete zobrazit protokol procesu, včetně všech chyb vrácených z Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5574d-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="5574d-219">Viz také</span><span class="sxs-lookup"><span data-stu-id="5574d-219">See also</span></span>

[<span data-ttu-id="5574d-220">Co je Dataverse?</span><span class="sxs-lookup"><span data-stu-id="5574d-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="5574d-221">Tabulky v Dataverse</span><span class="sxs-lookup"><span data-stu-id="5574d-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="5574d-222">Přehled vztahů mezi tabulkami</span><span class="sxs-lookup"><span data-stu-id="5574d-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="5574d-223">Vytváření a úpravy virtuálních tabulek, které obsahují data z externího zdroje dat</span><span class="sxs-lookup"><span data-stu-id="5574d-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="5574d-224">Co jsou portály Power Apps?</span><span class="sxs-lookup"><span data-stu-id="5574d-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="5574d-225">Přehled vytváření aplikací v Power Apps</span><span class="sxs-lookup"><span data-stu-id="5574d-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
