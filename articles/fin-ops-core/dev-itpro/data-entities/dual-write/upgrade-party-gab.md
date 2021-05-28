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
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018305"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="48efd-103">Upgrade na model strany a globálního adresáře</span><span class="sxs-lookup"><span data-stu-id="48efd-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="48efd-104">[Šablona Azure Data Factory](https://aka.ms/dual-write-gab-adf) vám pomůže upgradovat stávající data tabulek **Účet**, **Kontakt** a **Prodejce** v duálním zápisu na model strany a globálního adresáře.</span><span class="sxs-lookup"><span data-stu-id="48efd-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="48efd-105">Šablona odsouhlasí data z aplikací Finance and Operations i aplikací pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="48efd-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="48efd-106">Na konci procesu budou pole **Strana** a **Kontakt** záznamy **Strana** vytvořeny a přidruženy k záznamům **Účet**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="48efd-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="48efd-107">Soubor CSV (`FONewParty.csv`) je generován k vytvoření nových záznamů **Strana** uvnitř aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48efd-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="48efd-108">Toto téma obsahuje pokyny k použití šablony Data Factory a upgradu dat.</span><span class="sxs-lookup"><span data-stu-id="48efd-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="48efd-109">Pokud nemáte žádná přizpůsobení, můžete použít šablonu tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="48efd-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="48efd-110">Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit pomocí následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="48efd-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="48efd-111">Šablona pomáhá upgradovat pouze data **Strana**.</span><span class="sxs-lookup"><span data-stu-id="48efd-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="48efd-112">V budoucím vydání budou zahrnuty poštovní a elektronické adresy.</span><span class="sxs-lookup"><span data-stu-id="48efd-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="48efd-113">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="48efd-113">Prerequisites</span></span>

<span data-ttu-id="48efd-114">Jsou zapotřebí následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="48efd-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="48efd-115">Předplatné Azure</span><span class="sxs-lookup"><span data-stu-id="48efd-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="48efd-116">Přístup k šabloně</span><span class="sxs-lookup"><span data-stu-id="48efd-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="48efd-117">Jste stávajícím zákazníkem se dvěma zápisy.</span><span class="sxs-lookup"><span data-stu-id="48efd-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="48efd-118">Příprava na upgrade</span><span class="sxs-lookup"><span data-stu-id="48efd-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="48efd-119">**Plně synchronizované**: Obě prostředí jsou plně synchronizovaná pro **Účet (zákazník)**, **Kontakt** a **Prodejce**.</span><span class="sxs-lookup"><span data-stu-id="48efd-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="48efd-120">**Integrační klíče**: Tabulky **Účet (zákazník)**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků používají integrační klíče, které byly dodány ihned po vybalení.</span><span class="sxs-lookup"><span data-stu-id="48efd-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="48efd-121">Pokud jste přizpůsobili integrační klíče, musíte přizpůsobit šablonu.</span><span class="sxs-lookup"><span data-stu-id="48efd-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="48efd-122">**Číslo strany**: Všechny záznamy **Účet (zákazník)**, **Kontakt** a **Prodejce**, které budou upgradovány, mají číslo **Strana**.</span><span class="sxs-lookup"><span data-stu-id="48efd-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="48efd-123">Záznamy bez čísla **Strana** budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="48efd-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="48efd-124">Chcete-li tyto záznamy upgradovat, přidejte k nim číslo **Strana**, než zahájíte proces upgradu.</span><span class="sxs-lookup"><span data-stu-id="48efd-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="48efd-125">**Výpadek systému**: Během procesu upgradu budete muset přepnout prostředí Finance and Operations i prostředí zapojení zákazníků offline.</span><span class="sxs-lookup"><span data-stu-id="48efd-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="48efd-126">**Snímek** : Pořiďte snímky aplikací Finance and Operations i zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="48efd-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="48efd-127">Pokud potřebujete, použijte snímky k obnovení předchozího stavu.</span><span class="sxs-lookup"><span data-stu-id="48efd-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="48efd-128">Nasazení</span><span class="sxs-lookup"><span data-stu-id="48efd-128">Deployment</span></span>

1. <span data-ttu-id="48efd-129">Stáhněte si šablonu z [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="48efd-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="48efd-130">Přihlásit se k aplikaci [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="48efd-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="48efd-131">Vytvořte [skupinu prostředků](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="48efd-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="48efd-132">Vytvořte [účet úložiště](/azure/storage/common/storage-account-create?tabs=azure-portal) ve skupině prostředků, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="48efd-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="48efd-133">Vytvořte [datovou továrnu](/azure/data-factory/quickstart-create-data-factory-portal) ve výše uvedené skupině prostředků, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="48efd-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="48efd-134">Otevřete datovou továrnu a vyberte dlaždici **Autor a monitor**.</span><span class="sxs-lookup"><span data-stu-id="48efd-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="48efd-135">Na kartě **Spravovat** vyberte **Šablona ARM**.</span><span class="sxs-lookup"><span data-stu-id="48efd-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="48efd-136">Vyberte **Importovat šablonu ARM** k importování šablony **Strana**.</span><span class="sxs-lookup"><span data-stu-id="48efd-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="48efd-137">Importujte šablonu do datové továrny.</span><span class="sxs-lookup"><span data-stu-id="48efd-137">Import the template into the data factory.</span></span> <span data-ttu-id="48efd-138">Zadejte následující hodnoty pro **Detaily projektu** a **Podrobnosti instance**.</span><span class="sxs-lookup"><span data-stu-id="48efd-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="48efd-139">Pole</span><span class="sxs-lookup"><span data-stu-id="48efd-139">Field</span></span> | <span data-ttu-id="48efd-140">Hodnota</span><span class="sxs-lookup"><span data-stu-id="48efd-140">Value</span></span>
    ---|---
    <span data-ttu-id="48efd-141">Předplatné</span><span class="sxs-lookup"><span data-stu-id="48efd-141">Subscription</span></span> | <span data-ttu-id="48efd-142">Předplatné Azure</span><span class="sxs-lookup"><span data-stu-id="48efd-142">Azure subscription</span></span>
    <span data-ttu-id="48efd-143">Skupina prostředků</span><span class="sxs-lookup"><span data-stu-id="48efd-143">Resource group</span></span> | <span data-ttu-id="48efd-144">Poskytněte stejný prostředek, pod kterým je vytvořen účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="48efd-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="48efd-145">Oblast</span><span class="sxs-lookup"><span data-stu-id="48efd-145">Region</span></span> | <span data-ttu-id="48efd-146">Zadejte region.</span><span class="sxs-lookup"><span data-stu-id="48efd-146">Specify region.</span></span>
    <span data-ttu-id="48efd-147">Název továrny</span><span class="sxs-lookup"><span data-stu-id="48efd-147">Factory Name</span></span> | <span data-ttu-id="48efd-148">Zadejte název továrny.</span><span class="sxs-lookup"><span data-stu-id="48efd-148">Specify factory name.</span></span>
    <span data-ttu-id="48efd-149">Klíč objektu zabezpečení Service_service spojený s FO</span><span class="sxs-lookup"><span data-stu-id="48efd-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="48efd-150">Zadejte klíč aplikace.</span><span class="sxs-lookup"><span data-stu-id="48efd-150">Specify the application's key.</span></span>
    <span data-ttu-id="48efd-151">Řetězec Storage_connection Azure Blob</span><span class="sxs-lookup"><span data-stu-id="48efd-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="48efd-152">Řetězec připojení Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="48efd-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="48efd-153">Dynamics Crm propojené Service_password</span><span class="sxs-lookup"><span data-stu-id="48efd-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="48efd-154">Heslo uživatelského účtu, který jste zadali jako uživatelské jméno.</span><span class="sxs-lookup"><span data-stu-id="48efd-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="48efd-155">Service_properties_type Properties_url propojené s FO</span><span class="sxs-lookup"><span data-stu-id="48efd-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="48efd-156">Service_properties_type Properties_tenant propojené s FO</span><span class="sxs-lookup"><span data-stu-id="48efd-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="48efd-157">Zadejte údaje o klientovi (název domény nebo ID tenanta), pod kterými se vaše aplikace nachází.</span><span class="sxs-lookup"><span data-stu-id="48efd-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="48efd-158">Id prostředku Service_properties_type Properties_aad propojené s FO</span><span class="sxs-lookup"><span data-stu-id="48efd-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="48efd-159">Id objektu zabezpečení Service_properties_type Properties_service propojené s FO</span><span class="sxs-lookup"><span data-stu-id="48efd-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="48efd-160">Zadejte ID klienta aplikace.</span><span class="sxs-lookup"><span data-stu-id="48efd-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="48efd-161">Dynamics Crm spojené Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="48efd-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="48efd-162">Uživatelské jméno pro připojení k Dynamics.</span><span class="sxs-lookup"><span data-stu-id="48efd-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="48efd-163">Další informace viz [Ruční propagace šablony Resource Manageru pro každé prostředí](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Vlastnosti propojené služby](/azure/data-factory/connector-dynamics-ax#linked-service-properties) a [Kopírování dat pomocí Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="48efd-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="48efd-164">Po nasazení ověřte datové sady, tok dat a propojenou službu datové továrny.</span><span class="sxs-lookup"><span data-stu-id="48efd-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datové sady, tok dat a propojená služba](media/data-factory-validate.png)

11. <span data-ttu-id="48efd-166">Přejděte na **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="48efd-166">Navigate to **Manage**.</span></span> <span data-ttu-id="48efd-167">V části **Připojení** vyberte **Propojená služba**.</span><span class="sxs-lookup"><span data-stu-id="48efd-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="48efd-168">Vyberte **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="48efd-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="48efd-169">Ve formuláři **Upravit propojenou službu (Dynamics CRM)** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="48efd-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="48efd-170">Pole</span><span class="sxs-lookup"><span data-stu-id="48efd-170">Field</span></span> | <span data-ttu-id="48efd-171">Hodnota</span><span class="sxs-lookup"><span data-stu-id="48efd-171">Value</span></span>
    ---|---
    <span data-ttu-id="48efd-172">Jméno</span><span class="sxs-lookup"><span data-stu-id="48efd-172">Name</span></span> | <span data-ttu-id="48efd-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="48efd-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="48efd-174">popis</span><span class="sxs-lookup"><span data-stu-id="48efd-174">Description</span></span> | <span data-ttu-id="48efd-175">Propojené služby pro připojení k instanci CRM k načtení dat entit</span><span class="sxs-lookup"><span data-stu-id="48efd-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="48efd-176">Připojte se pomocí modulu runtime integrace</span><span class="sxs-lookup"><span data-stu-id="48efd-176">Connect via integration runtime</span></span> | <span data-ttu-id="48efd-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48efd-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="48efd-178">Typ nasazení</span><span class="sxs-lookup"><span data-stu-id="48efd-178">Deployment type</span></span> | <span data-ttu-id="48efd-179">Online</span><span class="sxs-lookup"><span data-stu-id="48efd-179">Online</span></span>
    <span data-ttu-id="48efd-180">Uri služby</span><span class="sxs-lookup"><span data-stu-id="48efd-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="48efd-181">Typ ověření</span><span class="sxs-lookup"><span data-stu-id="48efd-181">Authentication type</span></span> | <span data-ttu-id="48efd-182">Office365</span><span class="sxs-lookup"><span data-stu-id="48efd-182">Office365</span></span>
    <span data-ttu-id="48efd-183">Uživatelské jméno</span><span class="sxs-lookup"><span data-stu-id="48efd-183">User name</span></span> |
    <span data-ttu-id="48efd-184">Heslo nebo Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="48efd-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="48efd-185">Heslo</span><span class="sxs-lookup"><span data-stu-id="48efd-185">Password</span></span>
    <span data-ttu-id="48efd-186">Heslo</span><span class="sxs-lookup"><span data-stu-id="48efd-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="48efd-187">Spusťte šablonu</span><span class="sxs-lookup"><span data-stu-id="48efd-187">Run the template</span></span>

1. <span data-ttu-id="48efd-188">Zastavte následující dvojitý zápis **Účet**, **Kontakt** a **Prodejce** pomocí aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48efd-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="48efd-189">Zákazníci V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="48efd-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="48efd-190">Zákazníci V3(kontakty)</span><span class="sxs-lookup"><span data-stu-id="48efd-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="48efd-191">Kontakty CDS V2(kontakty)</span><span class="sxs-lookup"><span data-stu-id="48efd-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="48efd-192">Kontakty CDS V2(kontakty)</span><span class="sxs-lookup"><span data-stu-id="48efd-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="48efd-193">Dodavatel V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="48efd-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="48efd-194">Ujistěte se, že jsou mapy odstraněny z tabulky `msdy_dualwriteruntimeconfig` v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="48efd-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="48efd-195">Nainstalujte [řešení strany a globálního adresáře s duálním zápisem](https://aka.ms/dual-write-gab) z AppSource.</span><span class="sxs-lookup"><span data-stu-id="48efd-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="48efd-196">V aplikaci Finance and Operations, pokud následující tabulky obsahují data, pak pro ně spusťte **Počáteční synchronizaci**.</span><span class="sxs-lookup"><span data-stu-id="48efd-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="48efd-197">Oslovení</span><span class="sxs-lookup"><span data-stu-id="48efd-197">Salutations</span></span>
    + <span data-ttu-id="48efd-198">Typy osobní charakteristiky</span><span class="sxs-lookup"><span data-stu-id="48efd-198">Personal character types</span></span>
    + <span data-ttu-id="48efd-199">Zdvořilostní zakončení</span><span class="sxs-lookup"><span data-stu-id="48efd-199">Complimentary closing</span></span>
    + <span data-ttu-id="48efd-200">Tituly kontaktní osoby</span><span class="sxs-lookup"><span data-stu-id="48efd-200">Contact person titles</span></span>
    + <span data-ttu-id="48efd-201">Role v rozhodovacím procesu</span><span class="sxs-lookup"><span data-stu-id="48efd-201">Decision making roles</span></span>
    + <span data-ttu-id="48efd-202">Úrovně věrnosti</span><span class="sxs-lookup"><span data-stu-id="48efd-202">Loyalty levels</span></span>

5. <span data-ttu-id="48efd-203">V aplikaci pro zapojení zákazníků deaktivujte následující kroky pluginu.</span><span class="sxs-lookup"><span data-stu-id="48efd-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="48efd-204">Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="48efd-204">Account Update</span></span>
         + <span data-ttu-id="48efd-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="48efd-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="48efd-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="48efd-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="48efd-207">Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="48efd-207">Contact Update</span></span>
         + <span data-ttu-id="48efd-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="48efd-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="48efd-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="48efd-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="48efd-210">Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="48efd-210">msdyn_party Update</span></span>
         + <span data-ttu-id="48efd-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="48efd-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="48efd-212">Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="48efd-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="48efd-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="48efd-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="48efd-214">V aplikaci pro zapojení zákazníků deaktivujte následující pracovní postupy:</span><span class="sxs-lookup"><span data-stu-id="48efd-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="48efd-215">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="48efd-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="48efd-216">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="48efd-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="48efd-217">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="48efd-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="48efd-218">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="48efd-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="48efd-219">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="48efd-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="48efd-220">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="48efd-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="48efd-221">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="48efd-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="48efd-222">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="48efd-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="48efd-223">V datové továrně spusťte šablonu výběrem **Spustit hned**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="48efd-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="48efd-224">V závislosti na objemu dat může tento proces trvat několik hodin.</span><span class="sxs-lookup"><span data-stu-id="48efd-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Spustit běh](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="48efd-226">Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit.</span><span class="sxs-lookup"><span data-stu-id="48efd-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="48efd-227">Importujte nové záznamy **Strana** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48efd-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="48efd-228">Stáhněte si soubor `FONewParty.csv` z úložiště Azure blob.</span><span class="sxs-lookup"><span data-stu-id="48efd-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="48efd-229">Cesta je `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="48efd-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="48efd-230">Převeďte soubor `FONewParty.csv` do souboru Excel a importujte soubor Excel do souboru aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48efd-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="48efd-231">Pokud vám csv import vyhovuje, můžete soubor csv importovat přímo.</span><span class="sxs-lookup"><span data-stu-id="48efd-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="48efd-232">Import může trvat několik hodin, v závislosti na objemu dat.</span><span class="sxs-lookup"><span data-stu-id="48efd-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="48efd-233">Další informace naleznete v tématu [Přehled úloh importu a exportu dat](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="48efd-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importování záznamů strany Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="48efd-235">V aplikaci pro zapojení zákazníků aktivujte následující kroky pluginu:</span><span class="sxs-lookup"><span data-stu-id="48efd-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="48efd-236">Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="48efd-236">Account Update</span></span>
         + <span data-ttu-id="48efd-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="48efd-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="48efd-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="48efd-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="48efd-239">Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="48efd-239">Contact Update</span></span>
         + <span data-ttu-id="48efd-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="48efd-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="48efd-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="48efd-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="48efd-242">Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="48efd-242">msdyn_party Update</span></span>
         + <span data-ttu-id="48efd-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="48efd-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="48efd-244">Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="48efd-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="48efd-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="48efd-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="48efd-246">V aplikacích pro zapojení zákazníků aktivujte následující pracovní postupy, pokud jste je deaktivovali v předchozích krocích:</span><span class="sxs-lookup"><span data-stu-id="48efd-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="48efd-247">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="48efd-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="48efd-248">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="48efd-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="48efd-249">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="48efd-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="48efd-250">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="48efd-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="48efd-251">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="48efd-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="48efd-252">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="48efd-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="48efd-253">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="48efd-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="48efd-254">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="48efd-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="48efd-255">Spusťte mapy související se **stranou** podle pokynů v části [Strana a globální adresář](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="48efd-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="48efd-256">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="48efd-256">Troubleshooting</span></span>

1. <span data-ttu-id="48efd-257">V procesu selže, spusťte znovu továrnu dat počínaje neúspěšnou aktivitou.</span><span class="sxs-lookup"><span data-stu-id="48efd-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="48efd-258">Některé soubory generuje datová továrna, kterou můžete použít pro účely ověření dat.</span><span class="sxs-lookup"><span data-stu-id="48efd-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="48efd-259">Datová továrna běží na základě souborů CSV, které jsou odděleny čárkami.</span><span class="sxs-lookup"><span data-stu-id="48efd-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="48efd-260">Pokud existuje hodnota pole s čárkou, může to ovlivnit výsledky.</span><span class="sxs-lookup"><span data-stu-id="48efd-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="48efd-261">Musíte odstranit čárky.</span><span class="sxs-lookup"><span data-stu-id="48efd-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="48efd-262">Karta **Monitorování** poskytuje informace o všech krocích a zpracovaných datech.</span><span class="sxs-lookup"><span data-stu-id="48efd-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="48efd-263">Vyberte konkrétní krok k ladění.</span><span class="sxs-lookup"><span data-stu-id="48efd-263">Select a specific step to debug it.</span></span>

    ![Záložka Monitorování](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="48efd-265">Další informace o šabloně</span><span class="sxs-lookup"><span data-stu-id="48efd-265">Learn more about the template</span></span>

<span data-ttu-id="48efd-266">Komentáře k šabloně najdete v souboru [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="48efd-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>