---
title: Upgrade na model strany a globálního adresáře
description: Toto téma popisuje, jak upgradovat data duálního zápisu na model strany a globálního adresáře.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112666"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="9831a-103">Upgrade na model strany a globálního adresáře</span><span class="sxs-lookup"><span data-stu-id="9831a-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9831a-104">[Šablona Microsoft Azure Data Factory](https://aka.ms/dual-write-gab-adf) vám pomůže upgradovat stávající data tabulek **Účet**, **Kontakt** a **Prodejce** v duálním zápisu na model strany a globálního adresáře.</span><span class="sxs-lookup"><span data-stu-id="9831a-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="9831a-105">Šablona odsouhlasí data z aplikací Finance and Operations i aplikací Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="9831a-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="9831a-106">Na konci procesu budou pole **Strana** a **Kontakt** záznamy **Strana** vytvořeny a přidruženy k záznamům **Účet**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="9831a-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="9831a-107">Soubor CSV (`FONewParty.csv`) je generován k vytvoření nových záznamů **Strana** uvnitř aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9831a-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="9831a-108">Toto téma obsahuje pokyny k použití šablony Data Factory a upgradu dat.</span><span class="sxs-lookup"><span data-stu-id="9831a-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="9831a-109">Pokud nemáte žádná přizpůsobení, můžete použít šablonu tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="9831a-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="9831a-110">Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit pomocí následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="9831a-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="9831a-111">Šablona upgraduje pouze data **Strana**.</span><span class="sxs-lookup"><span data-stu-id="9831a-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="9831a-112">V budoucím vydání budou zahrnuty poštovní a elektronické adresy.</span><span class="sxs-lookup"><span data-stu-id="9831a-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9831a-113">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="9831a-113">Prerequisites</span></span>

<span data-ttu-id="9831a-114">K upgradu na model Strana a Globální adresář jsou vyžadovány následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="9831a-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="9831a-115">Předplatné Azure</span><span class="sxs-lookup"><span data-stu-id="9831a-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="9831a-116">Přístup k šabloně</span><span class="sxs-lookup"><span data-stu-id="9831a-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="9831a-117">Musíte být stávajícím zákazníkem se dvěma zápisy.</span><span class="sxs-lookup"><span data-stu-id="9831a-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="9831a-118">Příprava na upgrade</span><span class="sxs-lookup"><span data-stu-id="9831a-118">Prepare for the upgrade</span></span>
<span data-ttu-id="9831a-119">K přípravě na upgrade jsou potřeba následující aktivity:</span><span class="sxs-lookup"><span data-stu-id="9831a-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="9831a-120">**Plně synchronizované**: Obě prostředí jsou v plně synchronizovaném stavu pro **Účet (zákazník)**, **Kontakt** a **Prodejce**.</span><span class="sxs-lookup"><span data-stu-id="9831a-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="9831a-121">**Integrační klíče**: Tabulky **Účet (zákazník)**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků používají integrační klíče, které byly dodány ihned po vybalení.</span><span class="sxs-lookup"><span data-stu-id="9831a-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="9831a-122">Pokud jste přizpůsobili integrační klíče, musíte přizpůsobit šablonu.</span><span class="sxs-lookup"><span data-stu-id="9831a-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="9831a-123">**Číslo strany**: Všechny záznamy **Účet (zákazník)**, **Kontakt** a **Prodejce**, které budou upgradovány, mají číslo **Strana**.</span><span class="sxs-lookup"><span data-stu-id="9831a-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="9831a-124">Záznamy bez čísla **Strana** budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="9831a-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="9831a-125">Chcete-li tyto záznamy upgradovat, přidejte k nim číslo **Strana**, než zahájíte proces upgradu.</span><span class="sxs-lookup"><span data-stu-id="9831a-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="9831a-126">**Výpadek systému**: Během procesu upgradu budete muset přepnout prostředí Finance and Operations Customer Engagement offline.</span><span class="sxs-lookup"><span data-stu-id="9831a-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="9831a-127">**Snímek**: Pořiďte snímky aplikací Finance and Operations i Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="9831a-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="9831a-128">Pokud potřebujete, použijte snímky k obnovení předchozího stavu.</span><span class="sxs-lookup"><span data-stu-id="9831a-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="9831a-129">Nasazení</span><span class="sxs-lookup"><span data-stu-id="9831a-129">Deployment</span></span>

1. <span data-ttu-id="9831a-130">Stáhněte si šablonu z [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="9831a-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="9831a-131">Přihlásit se k aplikaci [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="9831a-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="9831a-132">Vytvořte [skupinu prostředků](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="9831a-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="9831a-133">Vytvořte [účet úložiště](/azure/storage/common/storage-account-create?tabs=azure-portal) ve skupině prostředků, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="9831a-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="9831a-134">Vytvořte [datovou továrnu](/azure/data-factory/quickstart-create-data-factory-portal) ve výše uvedené skupině prostředků, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="9831a-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="9831a-135">Otevřete datovou továrnu a vyberte dlaždici **Autor a monitor**.</span><span class="sxs-lookup"><span data-stu-id="9831a-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="9831a-136">Na kartě **Spravovat** vyberte **Šablona ARM**.</span><span class="sxs-lookup"><span data-stu-id="9831a-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="9831a-137">Vyberte **Importovat šablonu ARM** k importování šablony **Strana**.</span><span class="sxs-lookup"><span data-stu-id="9831a-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="9831a-138">Importujte šablonu do datové továrny.</span><span class="sxs-lookup"><span data-stu-id="9831a-138">Import the template into the data factory.</span></span> <span data-ttu-id="9831a-139">Zadejte následující hodnoty pro **Detaily projektu** a **Podrobnosti instance**.</span><span class="sxs-lookup"><span data-stu-id="9831a-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="9831a-140">Pole</span><span class="sxs-lookup"><span data-stu-id="9831a-140">Field</span></span> | <span data-ttu-id="9831a-141">Hodnota</span><span class="sxs-lookup"><span data-stu-id="9831a-141">Value</span></span>
    ---|---
    <span data-ttu-id="9831a-142">Předplatné</span><span class="sxs-lookup"><span data-stu-id="9831a-142">Subscription</span></span> | <span data-ttu-id="9831a-143">Předplatné Azure</span><span class="sxs-lookup"><span data-stu-id="9831a-143">Azure subscription</span></span>
    <span data-ttu-id="9831a-144">Skupina prostředků</span><span class="sxs-lookup"><span data-stu-id="9831a-144">Resource group</span></span> | <span data-ttu-id="9831a-145">Poskytněte stejný prostředek, pod kterým je vytvořen účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="9831a-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="9831a-146">Oblast</span><span class="sxs-lookup"><span data-stu-id="9831a-146">Region</span></span> | <span data-ttu-id="9831a-147">Zadejte region.</span><span class="sxs-lookup"><span data-stu-id="9831a-147">Specify region.</span></span>
    <span data-ttu-id="9831a-148">Název továrny</span><span class="sxs-lookup"><span data-stu-id="9831a-148">Factory Name</span></span> | <span data-ttu-id="9831a-149">Zadejte název továrny.</span><span class="sxs-lookup"><span data-stu-id="9831a-149">Specify factory name.</span></span>
    <span data-ttu-id="9831a-150">Klíč objektu zabezpečení Service_service spojený s FO</span><span class="sxs-lookup"><span data-stu-id="9831a-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="9831a-151">Zadejte klíč aplikace.</span><span class="sxs-lookup"><span data-stu-id="9831a-151">Specify the application's key.</span></span>
    <span data-ttu-id="9831a-152">Řetězec Storage_connection Azure Blob</span><span class="sxs-lookup"><span data-stu-id="9831a-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="9831a-153">Řetězec připojení Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="9831a-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="9831a-154">Dynamics Crm propojené Service_password</span><span class="sxs-lookup"><span data-stu-id="9831a-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="9831a-155">Heslo uživatelského účtu, který jste zadali jako uživatelské jméno.</span><span class="sxs-lookup"><span data-stu-id="9831a-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="9831a-156">Service_properties_type Properties_url propojené s FO</span><span class="sxs-lookup"><span data-stu-id="9831a-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="9831a-157">Service_properties_type Properties_tenant propojené s FO</span><span class="sxs-lookup"><span data-stu-id="9831a-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="9831a-158">Zadejte údaje o klientovi (název domény nebo ID tenanta), pod kterými se vaše aplikace nachází.</span><span class="sxs-lookup"><span data-stu-id="9831a-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="9831a-159">Id prostředku Service_properties_type Properties_aad propojené s FO</span><span class="sxs-lookup"><span data-stu-id="9831a-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="9831a-160">Id objektu zabezpečení Service_properties_type Properties_service propojené s FO</span><span class="sxs-lookup"><span data-stu-id="9831a-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="9831a-161">Zadejte ID klienta aplikace.</span><span class="sxs-lookup"><span data-stu-id="9831a-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="9831a-162">Dynamics Crm spojené Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="9831a-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="9831a-163">Uživatelské jméno pro připojení k Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9831a-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="9831a-164">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="9831a-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="9831a-165">Ručně propagujte šablonu Resource Manageru pro každé prostředí</span><span class="sxs-lookup"><span data-stu-id="9831a-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="9831a-166">Vlastnosti propojené služby</span><span class="sxs-lookup"><span data-stu-id="9831a-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="9831a-167">Zkopírujte data pomocí Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="9831a-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="9831a-168">Po nasazení ověřte datové sady, tok dat a propojenou službu datové továrny.</span><span class="sxs-lookup"><span data-stu-id="9831a-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datové sady, tok dat a propojená služba](media/data-factory-validate.png)

11. <span data-ttu-id="9831a-170">Přejděte na **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="9831a-170">Navigate to **Manage**.</span></span> <span data-ttu-id="9831a-171">V části **Připojení** vyberte **Propojená služba**.</span><span class="sxs-lookup"><span data-stu-id="9831a-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="9831a-172">Vyberte **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="9831a-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="9831a-173">Ve formuláři **Upravit propojenou službu (Dynamics CRM)** zadejte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="9831a-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="9831a-174">Pole</span><span class="sxs-lookup"><span data-stu-id="9831a-174">Field</span></span> | <span data-ttu-id="9831a-175">Hodnota</span><span class="sxs-lookup"><span data-stu-id="9831a-175">Value</span></span>
    ---|---
    <span data-ttu-id="9831a-176">Jméno</span><span class="sxs-lookup"><span data-stu-id="9831a-176">Name</span></span> | <span data-ttu-id="9831a-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="9831a-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="9831a-178">popis</span><span class="sxs-lookup"><span data-stu-id="9831a-178">Description</span></span> | <span data-ttu-id="9831a-179">Propojené služby pro připojení k instanci CRM k načtení dat entit</span><span class="sxs-lookup"><span data-stu-id="9831a-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="9831a-180">Připojte se pomocí modulu runtime integrace</span><span class="sxs-lookup"><span data-stu-id="9831a-180">Connect via integration runtime</span></span> | <span data-ttu-id="9831a-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9831a-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="9831a-182">Typ nasazení</span><span class="sxs-lookup"><span data-stu-id="9831a-182">Deployment type</span></span> | <span data-ttu-id="9831a-183">Online</span><span class="sxs-lookup"><span data-stu-id="9831a-183">Online</span></span>
    <span data-ttu-id="9831a-184">Uri služby</span><span class="sxs-lookup"><span data-stu-id="9831a-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="9831a-185">Typ ověření</span><span class="sxs-lookup"><span data-stu-id="9831a-185">Authentication type</span></span> | <span data-ttu-id="9831a-186">Office365</span><span class="sxs-lookup"><span data-stu-id="9831a-186">Office365</span></span>
    <span data-ttu-id="9831a-187">Uživatelské jméno</span><span class="sxs-lookup"><span data-stu-id="9831a-187">User name</span></span> |
    <span data-ttu-id="9831a-188">Heslo nebo Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="9831a-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="9831a-189">Heslo</span><span class="sxs-lookup"><span data-stu-id="9831a-189">Password</span></span>
    <span data-ttu-id="9831a-190">Heslo</span><span class="sxs-lookup"><span data-stu-id="9831a-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="9831a-191">Spusťte šablonu</span><span class="sxs-lookup"><span data-stu-id="9831a-191">Run the template</span></span>

1. <span data-ttu-id="9831a-192">Zastavte následující mapy dvojitého zápisu **Účet**, **Kontakt** a **Prodejce** pomocí aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9831a-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="9831a-193">Zákazníci V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="9831a-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="9831a-194">Zákazníci V3(kontakty)</span><span class="sxs-lookup"><span data-stu-id="9831a-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="9831a-195">Kontakty CDS V2(kontakty)</span><span class="sxs-lookup"><span data-stu-id="9831a-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="9831a-196">Kontakty CDS V2(kontakty)</span><span class="sxs-lookup"><span data-stu-id="9831a-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="9831a-197">Dodavatel V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="9831a-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="9831a-198">Ujistěte se, že jsou mapy odstraněny z tabulky `msdy_dualwriteruntimeconfig` v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9831a-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="9831a-199">Nainstalujte [řešení strany a globálního adresáře s duálním zápisem](https://aka.ms/dual-write-gab) z AppSource.</span><span class="sxs-lookup"><span data-stu-id="9831a-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="9831a-200">V aplikaci Finance and Operations, pokud následující tabulky obsahují data, pak pro ně spusťte **Počáteční synchronizaci**.</span><span class="sxs-lookup"><span data-stu-id="9831a-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="9831a-201">Oslovení</span><span class="sxs-lookup"><span data-stu-id="9831a-201">Salutations</span></span>
    + <span data-ttu-id="9831a-202">Typy osobní charakteristiky</span><span class="sxs-lookup"><span data-stu-id="9831a-202">Personal character types</span></span>
    + <span data-ttu-id="9831a-203">Zdvořilostní zakončení</span><span class="sxs-lookup"><span data-stu-id="9831a-203">Complimentary closing</span></span>
    + <span data-ttu-id="9831a-204">Tituly kontaktní osoby</span><span class="sxs-lookup"><span data-stu-id="9831a-204">Contact person titles</span></span>
    + <span data-ttu-id="9831a-205">Role v rozhodovacím procesu</span><span class="sxs-lookup"><span data-stu-id="9831a-205">Decision making roles</span></span>
    + <span data-ttu-id="9831a-206">Úrovně věrnosti</span><span class="sxs-lookup"><span data-stu-id="9831a-206">Loyalty levels</span></span>

5. <span data-ttu-id="9831a-207">V aplikaci pro zapojení zákazníků deaktivujte následující kroky pluginu.</span><span class="sxs-lookup"><span data-stu-id="9831a-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="9831a-208">Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="9831a-208">Account Update</span></span>
         + <span data-ttu-id="9831a-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="9831a-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="9831a-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="9831a-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="9831a-211">Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="9831a-211">Contact Update</span></span>
         + <span data-ttu-id="9831a-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="9831a-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="9831a-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="9831a-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="9831a-214">Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="9831a-214">msdyn_party Update</span></span>
         + <span data-ttu-id="9831a-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="9831a-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="9831a-216">Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="9831a-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="9831a-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="9831a-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="9831a-218">V aplikaci pro zapojení zákazníků deaktivujte následující pracovní postupy:</span><span class="sxs-lookup"><span data-stu-id="9831a-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="9831a-219">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="9831a-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9831a-220">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="9831a-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9831a-221">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="9831a-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="9831a-222">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="9831a-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="9831a-223">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="9831a-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9831a-224">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="9831a-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="9831a-225">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="9831a-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="9831a-226">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="9831a-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="9831a-227">V datové továrně spusťte šablonu výběrem **Spustit hned**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="9831a-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="9831a-228">V závislosti na objemu dat může tento proces trvat několik hodin.</span><span class="sxs-lookup"><span data-stu-id="9831a-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Spustit běh](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="9831a-230">Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit.</span><span class="sxs-lookup"><span data-stu-id="9831a-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="9831a-231">Importujte nové záznamy **Strana** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9831a-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="9831a-232">Stáhněte si soubor `FONewParty.csv` z úložiště Azure blob.</span><span class="sxs-lookup"><span data-stu-id="9831a-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="9831a-233">Cesta je `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="9831a-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="9831a-234">Převeďte soubor `FONewParty.csv` do souboru Excel a importujte soubor Excel do souboru aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9831a-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="9831a-235">Pokud vám csv import vyhovuje, můžete soubor csv importovat přímo.</span><span class="sxs-lookup"><span data-stu-id="9831a-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="9831a-236">Import může trvat několik hodin, v závislosti na objemu dat.</span><span class="sxs-lookup"><span data-stu-id="9831a-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="9831a-237">Další informace naleznete v tématu [Přehled úloh importu a exportu dat](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="9831a-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importování záznamů strany Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="9831a-239">V aplikaci pro zapojení zákazníků aktivujte následující kroky pluginu:</span><span class="sxs-lookup"><span data-stu-id="9831a-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="9831a-240">Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="9831a-240">Account Update</span></span>
         + <span data-ttu-id="9831a-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="9831a-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="9831a-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="9831a-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="9831a-243">Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="9831a-243">Contact Update</span></span>
         + <span data-ttu-id="9831a-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="9831a-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="9831a-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="9831a-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="9831a-246">Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="9831a-246">msdyn_party Update</span></span>
         + <span data-ttu-id="9831a-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="9831a-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="9831a-248">Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="9831a-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="9831a-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="9831a-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="9831a-250">V aplikacích pro zapojení zákazníků aktivujte následující pracovní postupy, pokud jste je deaktivovali v předchozích krocích:</span><span class="sxs-lookup"><span data-stu-id="9831a-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="9831a-251">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="9831a-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9831a-252">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="9831a-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9831a-253">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="9831a-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="9831a-254">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="9831a-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="9831a-255">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="9831a-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9831a-256">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="9831a-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="9831a-257">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="9831a-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="9831a-258">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="9831a-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="9831a-259">Spusťte mapy související se **stranou** podle pokynů v části [Strana a globální adresář](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="9831a-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9831a-260">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="9831a-260">Troubleshooting</span></span>

1. <span data-ttu-id="9831a-261">Pokud proces selže, spusťte znovu továrnu dat počínaje neúspěšnou aktivitou.</span><span class="sxs-lookup"><span data-stu-id="9831a-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="9831a-262">Některé soubory generuje datová továrna, kterou můžete použít pro účely ověření dat.</span><span class="sxs-lookup"><span data-stu-id="9831a-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="9831a-263">Datová továrna běží na základě souborů CSV, které jsou odděleny čárkami.</span><span class="sxs-lookup"><span data-stu-id="9831a-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="9831a-264">Pokud existuje hodnota pole s čárkou, může to ovlivnit výsledky.</span><span class="sxs-lookup"><span data-stu-id="9831a-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="9831a-265">Musíte odstranit čárky.</span><span class="sxs-lookup"><span data-stu-id="9831a-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="9831a-266">Karta **Monitorování** poskytuje informace o všech krocích a zpracovaných datech.</span><span class="sxs-lookup"><span data-stu-id="9831a-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="9831a-267">Vyberte konkrétní krok k ladění.</span><span class="sxs-lookup"><span data-stu-id="9831a-267">Select a specific step to debug it.</span></span>

    ![Záložka Monitorování](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="9831a-269">Další informace o šabloně</span><span class="sxs-lookup"><span data-stu-id="9831a-269">Learn more about the template</span></span>

<span data-ttu-id="9831a-270">Další informace o šabloně najdete v [Komentářích k readme šablony Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="9831a-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
