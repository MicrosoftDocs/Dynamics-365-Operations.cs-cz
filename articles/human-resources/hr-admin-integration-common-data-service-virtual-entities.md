---
title: Konfigurace virtuálních tabulek Dataverse
description: Toto téma ukazuje, jak konfigurovat virtuální tabulky pro Dynamics 365 Human Resources. Můžete generovat a aktualizovat existující virtuální tabulky a analyzovat vygenerované a dostupné tabulky.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 04997aba427ae6013c8154593b09ae1a45a580c3
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935746"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="909b3-104">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="909b3-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="909b3-105">Dynamics 365 Human Resources je virtuální zdroj dat v Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="909b3-106">Poskytuje úplné operací vytváření, čtení, aktualizace a mazání (CRUD) z Dataverse a Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="909b3-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="909b3-107">Data pro virtuální tabulky nejsou uloženy v Dataverse, ale v databázi aplikace.</span><span class="sxs-lookup"><span data-stu-id="909b3-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="909b3-108">Pro povolení operací CRUD v entitách Human Resources z Dataverse musíte entity zpřístupnit jako virtuální tabulky v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="909b3-109">To vám umožní provádět operace CRUD z Dataverse a Microsoft Power Platform na datech v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="909b3-110">Operace také podporují úplné ověření obchodní logiky Human Resources, aby byla zajištěna integrita dat při jejich zápisu do entit.</span><span class="sxs-lookup"><span data-stu-id="909b3-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="909b3-111">Entity Human Resources odpovídají Dataverse tabulkám.</span><span class="sxs-lookup"><span data-stu-id="909b3-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="909b3-112">Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="909b3-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="909b3-113">Dostupné virtuální tabulky pro Human Resources</span><span class="sxs-lookup"><span data-stu-id="909b3-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="909b3-114">Všechny entity Open Data Protocol (OData) v Human Resources jsou k dispozici jako virtuální tabulky v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="909b3-115">Jsou k dispozici i v Power Platform.</span><span class="sxs-lookup"><span data-stu-id="909b3-115">They're also available in Power Platform.</span></span> <span data-ttu-id="909b3-116">Nyní můžete vytvářet aplikace a prostředí s daty přímo z Human Resources s plnou schopností CRUD, a to bez kopírování nebo synchronizace dat do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="909b3-117">Můžete používat portály Power Apps k vytváření externích webů, které umožňují scénáře spolupráce pro obchodní procesy v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="909b3-118">Můžete zobrazit seznam virtuálních tabulek povolených v prostředí a začít pracovat s tabulkami v [Power Apps](https://make.powerapps.com), v řešení **Virtuální tabulky Dynamics 365 HR**.</span><span class="sxs-lookup"><span data-stu-id="909b3-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Virtuální tabulky Dynamics 365 HR ve Windows Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="909b3-120">Virtuální tabulky versus nativní tabulky</span><span class="sxs-lookup"><span data-stu-id="909b3-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="909b3-121">Virtuální tabulky pro Human Resources nejsou totéž jako nativni tabulky Dataverse vytvořené pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="909b3-122">Nativní tabulky pro Human Resources jsou generovány samostatně a udržovány v řešení HCM Common v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="909b3-123">U nativních tabulek jsou data uložena v Dataverse a vyžaduje synchronizaci s databází aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="909b3-124">Seznam nativních tabulek Dataverse pro Human Resources viz [Tabulky Dataverse](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="909b3-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="909b3-125">Nastavení</span><span class="sxs-lookup"><span data-stu-id="909b3-125">Setup</span></span>

<span data-ttu-id="909b3-126">Povolte virtuální tabulky ve vašem prostředí provedením těchto kroků nastavení.</span><span class="sxs-lookup"><span data-stu-id="909b3-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="909b3-127">Povolení virtuálních tabulek v Human Resources</span><span class="sxs-lookup"><span data-stu-id="909b3-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="909b3-128">Nejprve musíte povolit virtuální tabulky v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="909b3-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="909b3-129">V modulu Human Resources vyberte **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="909b3-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="909b3-130">Vyberte dlaždici **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="909b3-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="909b3-131">Vyberte **Podpora virtuálních tabulek v HR v Dataverse** a potom vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="909b3-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="909b3-132">Další informace o povolení a zákazu funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="909b3-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="909b3-133">Registrace aplikace v Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="909b3-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="909b3-134">Musíte registrovat instanci Human Resources v portálu Azure, aby platforma identit od Microsoftu mohla poskytovat ověřovací a autorizační služby pro tuto aplikaci a uživatele.</span><span class="sxs-lookup"><span data-stu-id="909b3-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="909b3-135">Další informace o registraci aplikací v Azure najdete v tématu [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="909b3-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="909b3-136">Otevřete [Microsoft Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="909b3-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="909b3-137">V seznamu služeb Azure zvolte **Registrace aplikací**.</span><span class="sxs-lookup"><span data-stu-id="909b3-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="909b3-138">Vyberte **Nová registrace**.</span><span class="sxs-lookup"><span data-stu-id="909b3-138">Select **New registration**.</span></span>

4. <span data-ttu-id="909b3-139">V poli **Název** zadejte popisný název aplikace.</span><span class="sxs-lookup"><span data-stu-id="909b3-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="909b3-140">Například **Virtuální tabulky Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="909b3-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="909b3-141">V poli **URI přesměrování** zadejte adresu URL oboru názvů vaší instance Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="909b3-142">Vyberte **Registrovat**.</span><span class="sxs-lookup"><span data-stu-id="909b3-142">Select **Register**.</span></span>

7. <span data-ttu-id="909b3-143">Po dokončení registrace se na webu Azure Portal zobrazí podokno **Přehled** pro registraci aplikace, které obsahuje jeho **ID aplikace (klienta)**.</span><span class="sxs-lookup"><span data-stu-id="909b3-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="909b3-144">V tuto chvíli si **ID aplikace (klienta)** poznamenejte.</span><span class="sxs-lookup"><span data-stu-id="909b3-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="909b3-145">Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních tabulek](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="909b3-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="909b3-146">V levém navigačním podokně vyberte **Certifikáty a tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="909b3-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="909b3-147">V části **Tajné klíče klienta** stránky vyberte **Nový tajný klíč klienta**.</span><span class="sxs-lookup"><span data-stu-id="909b3-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="909b3-148">Zadejte popis, vyberte dobu trvání a vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="909b3-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="909b3-149">Zaznamenejte hodnotu tajného klíče z vlastnosti **Hodnota** tabulky.</span><span class="sxs-lookup"><span data-stu-id="909b3-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="909b3-150">Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních tabulek](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="909b3-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="909b3-151">V tuto chvíli si nezapomeňte hodnotu tajného klíče poznamenat.</span><span class="sxs-lookup"><span data-stu-id="909b3-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="909b3-152">Po opuštění této stránky se tajný klíč už nikdy nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="909b3-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="909b3-153">Instalace aplikaci Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="909b3-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="909b3-154">Nainstalujte si aplikaci Dynamics 365 HR Virtual Table do svého prostředí Power Apps, abyste si nasadili balíček řešení virtuální tabulky do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="909b3-155">V Human Resources otevřete stránku **Integrace Microsoft Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="909b3-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="909b3-156">Vyberte kartu **Virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="909b3-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="909b3-157">Vyberte **Nainstalovat aplikaci virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="909b3-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="909b3-158">Konfigurace zdroje dat virtuálních tabulek</span><span class="sxs-lookup"><span data-stu-id="909b3-158">Configure the virtual table data source</span></span>

<span data-ttu-id="909b3-159">Dalším krokem je konfigurace zdroje dat virtuálních tabulek v prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="909b3-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="909b3-160">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="909b3-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="909b3-161">V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="909b3-162">Vyberte **URL prostředí** v části **Podrobnosti** této stránky.</span><span class="sxs-lookup"><span data-stu-id="909b3-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="909b3-163">V **Centru stavu řešení** vyberte ikonu **Rozšířené hledání** v pravém horním rohu stránky aplikace.</span><span class="sxs-lookup"><span data-stu-id="909b3-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="909b3-164">Na stránce **Rozšířené hledání** vyberte v rozevíracím seznamu **Hledat** položku **Konfigurace zdrojů virtuálních dat ve Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="909b3-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="909b3-165">Instalace aplikace virtuální tabulky z předchozího kroku instalace může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="909b3-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="909b3-166">Pokud **Konfigurace virtuálního datového zdroje Finance and Operations** nejsou k dispozici v seznamu, počkejte minutu a obnovte seznam.</span><span class="sxs-lookup"><span data-stu-id="909b3-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="909b3-167">Vyberte **Výsledky**</span><span class="sxs-lookup"><span data-stu-id="909b3-167">Select **Results**.</span></span>

7. <span data-ttu-id="909b3-168">Vyberte záznam **Zdroj dat Microsoft HR**.</span><span class="sxs-lookup"><span data-stu-id="909b3-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="909b3-169">Zadejte požadované informace pro konfiguraci zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="909b3-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="909b3-170">**Cílová adresa URL**: URL vašeho oboru názvů pro Human Resources.</span><span class="sxs-lookup"><span data-stu-id="909b3-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="909b3-171">Formát cílové adresy URL je:</span><span class="sxs-lookup"><span data-stu-id="909b3-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="909b3-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="909b3-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="909b3-173">Například:</span><span class="sxs-lookup"><span data-stu-id="909b3-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="909b3-174">Nezapomeňte uvést znak „**/**“ na konci adresy URL, aby nedošlo k chybě.</span><span class="sxs-lookup"><span data-stu-id="909b3-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="909b3-175">**ID tenanta**: ID tenanta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="909b3-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="909b3-176">**ID aplikace AAD**: ID aplikace (klienta) vytvořené pro aplikaci registrovanou přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="909b3-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="909b3-177">Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="909b3-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="909b3-178">**Tajný klíč aplikace AAD**: Tajný klíč klienta vytvořený pro aplikaci registrovanou přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="909b3-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="909b3-179">Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="909b3-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Zdroj dat Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="909b3-181">Zvolte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="909b3-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="909b3-182">Udělení oprávnění aplikací v Human Resources</span><span class="sxs-lookup"><span data-stu-id="909b3-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="909b3-183">Udělte oprávnění těmto dvěma aplikacím Azure AD v oblasti Human Resources:</span><span class="sxs-lookup"><span data-stu-id="909b3-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="909b3-184">Aplikace vytvořená pro vašeho tenanta přes Microsoft Azure Portal</span><span class="sxs-lookup"><span data-stu-id="909b3-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="909b3-185">Aplikace Dynamics 365 HR Virtual Table nainstalovaná v prostředí Power Apps</span><span class="sxs-lookup"><span data-stu-id="909b3-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="909b3-186">V Human Resources otevřete stránku **Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="909b3-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="909b3-187">Zvolte **Nový** pro vytvoření nového záznamu aplikace:</span><span class="sxs-lookup"><span data-stu-id="909b3-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="909b3-188">V poli **ID klienta** zadejte ID klienta aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="909b3-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="909b3-189">V poli **Název** zadejte název aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="909b3-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="909b3-190">V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="909b3-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="909b3-191">Zvolte **Nový** pro vytvoření druhého záznamu aplikace:</span><span class="sxs-lookup"><span data-stu-id="909b3-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="909b3-192">**ID klienta**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="909b3-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="909b3-193">**Název**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="909b3-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="909b3-194">V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.</span><span class="sxs-lookup"><span data-stu-id="909b3-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="909b3-195">Generování virtuálních tabulek</span><span class="sxs-lookup"><span data-stu-id="909b3-195">Generate virtual tables</span></span>

<span data-ttu-id="909b3-196">Po dokončení instalace můžete vybrat virtuální tabulku, které chcete vygenerovat a povolit ve vaší instanci Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="909b3-197">V Human Resources otevřete stránku **Integrace Microsoft Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="909b3-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="909b3-198">Vyberte kartu **Virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="909b3-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="909b3-199">Přepínač **Povolte virtuální tabulku** bude nastaven na **Ano** automaticky po dokončení všech požadovaných nastavení.</span><span class="sxs-lookup"><span data-stu-id="909b3-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="909b3-200">Pokud je přepínač nastaven na **Ne**, zkontrolujte kroky v předchozích částech tohoto dokumentu a ujistěte se, že jsou dokončeny všechny nezbytné předpoklady.</span><span class="sxs-lookup"><span data-stu-id="909b3-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="909b3-201">Vyberte tabulku nebo tabulku, kterou chcete generovat v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="909b3-202">Vyberte **Generovat/aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="909b3-202">Select **Generate/refresh**.</span></span>

![Integrace Dataverse](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="909b3-204">Zkontrolujte stav generování tabulky</span><span class="sxs-lookup"><span data-stu-id="909b3-204">Check table generation status</span></span>

<span data-ttu-id="909b3-205">Virtuální tabulky jsou generovány v Dataverse prostřednictvím asynchronního procesu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="909b3-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="909b3-206">Aktualizace na displeji procesu v centru akcí.</span><span class="sxs-lookup"><span data-stu-id="909b3-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="909b3-207">Podrobnosti o procesu, včetně protokolů chyb, se objeví na stránce **Procesní automatizace**.</span><span class="sxs-lookup"><span data-stu-id="909b3-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="909b3-208">V Human Resources otevřete stránku **Procesní automatizace**.</span><span class="sxs-lookup"><span data-stu-id="909b3-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="909b3-209">Vyberte kartu **Procesy na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="909b3-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="909b3-210">Vyberte **Proces na pozadí asynchronní operace s dotazováním virtuální tabulky**.</span><span class="sxs-lookup"><span data-stu-id="909b3-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="909b3-211">Vyberte **Zobrazit nejnovější výsledky**.</span><span class="sxs-lookup"><span data-stu-id="909b3-211">Select **View most recent results**.</span></span>

<span data-ttu-id="909b3-212">V posuvném podokně se zobrazují nejnovější výsledky provádění procesu.</span><span class="sxs-lookup"><span data-stu-id="909b3-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="909b3-213">Můžete zobrazit protokol procesu, včetně všech chyb vrácených z Dataverse.</span><span class="sxs-lookup"><span data-stu-id="909b3-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="909b3-214">Viz také</span><span class="sxs-lookup"><span data-stu-id="909b3-214">See also</span></span>

[<span data-ttu-id="909b3-215">Co je Dataverse?</span><span class="sxs-lookup"><span data-stu-id="909b3-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="909b3-216">Tabulky v Dataverse</span><span class="sxs-lookup"><span data-stu-id="909b3-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="909b3-217">Přehled vztahů mezi tabulkami</span><span class="sxs-lookup"><span data-stu-id="909b3-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="909b3-218">Vytváření a úpravy virtuálních tabulek, které obsahují data z externího zdroje dat</span><span class="sxs-lookup"><span data-stu-id="909b3-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="909b3-219">Co jsou portály Power Apps?</span><span class="sxs-lookup"><span data-stu-id="909b3-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="909b3-220">Přehled vytváření aplikací v Power Apps</span><span class="sxs-lookup"><span data-stu-id="909b3-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
