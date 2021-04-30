---
title: Upgrade na model strany a globálního adresáře
description: Toto téma popisuje, jak upgradovat data duálního zápisu na model strany a globálního adresáře.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857363"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="3f795-103">Upgrade na model strany a globálního adresáře</span><span class="sxs-lookup"><span data-stu-id="3f795-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3f795-104">[Šablona Azure Data Factory](https://aka.ms/dual-write-gab-adf) vám pomůže upgradovat stávající data tabulek **Účet**, **Kontakt** a **Prodejce** v duálním zápisu na model strany a globálního adresáře.</span><span class="sxs-lookup"><span data-stu-id="3f795-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="3f795-105">Šablona odsouhlasí data z aplikací Finance and Operations i aplikací pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="3f795-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="3f795-106">Na konci procesu budou pole **Strana** a **Kontakt** záznamy **Strana** vytvořeny a přidruženy k záznamům **Účet**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="3f795-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="3f795-107">Soubor CSV (`FONewParty.csv`) je generován k vytvoření nových záznamů **Strana** uvnitř aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f795-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="3f795-108">Toto téma obsahuje pokyny k použití šablony Data Factory a upgradu dat.</span><span class="sxs-lookup"><span data-stu-id="3f795-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="3f795-109">Pokud nemáte žádná přizpůsobení, můžete použít šablonu tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="3f795-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="3f795-110">Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit pomocí následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="3f795-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="3f795-111">Šablona pomáhá upgradovat pouze data **Strana**.</span><span class="sxs-lookup"><span data-stu-id="3f795-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="3f795-112">V budoucím vydání budou zahrnuty poštovní a elektronické adresy.</span><span class="sxs-lookup"><span data-stu-id="3f795-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3f795-113">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="3f795-113">Prerequisites</span></span>

<span data-ttu-id="3f795-114">Jsou zapotřebí následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="3f795-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="3f795-115">Předplatné Azure</span><span class="sxs-lookup"><span data-stu-id="3f795-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="3f795-116">Přístup k šabloně</span><span class="sxs-lookup"><span data-stu-id="3f795-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="3f795-117">Jste stávajícím zákazníkem se dvěma zápisy.</span><span class="sxs-lookup"><span data-stu-id="3f795-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="3f795-118">Příprava na upgrade</span><span class="sxs-lookup"><span data-stu-id="3f795-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="3f795-119">**Plně synchronizované**: Obě prostředí jsou plně synchronizovaná pro **Účet (zákazník)**, **Kontakt** a **Prodejce**.</span><span class="sxs-lookup"><span data-stu-id="3f795-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="3f795-120">**Integrační klíče**: Tabulky **Účet (zákazník)**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků používají integrační klíče, které byly dodány ihned po vybalení.</span><span class="sxs-lookup"><span data-stu-id="3f795-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="3f795-121">Pokud jste přizpůsobili integrační klíče, musíte přizpůsobit šablonu.</span><span class="sxs-lookup"><span data-stu-id="3f795-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="3f795-122">**Číslo strany**: Všechny záznamy **Účet (zákazník)**, **Kontakt** a **Prodejce**, které budou upgradovány, mají číslo **Strana**.</span><span class="sxs-lookup"><span data-stu-id="3f795-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="3f795-123">Záznamy bez čísla **Strana** budou ignorovány.</span><span class="sxs-lookup"><span data-stu-id="3f795-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="3f795-124">Chcete-li tyto záznamy upgradovat, přidejte k nim číslo **Strana**, než zahájíte proces upgradu.</span><span class="sxs-lookup"><span data-stu-id="3f795-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="3f795-125">**Výpadek systému**: Během procesu upgradu budete muset přepnout prostředí Finance and Operations i prostředí zapojení zákazníků offline.</span><span class="sxs-lookup"><span data-stu-id="3f795-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="3f795-126">**Snímek** : Pořiďte snímky aplikací Finance and Operations i zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="3f795-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="3f795-127">Pokud potřebujete, použijte snímky k obnovení předchozího stavu.</span><span class="sxs-lookup"><span data-stu-id="3f795-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="3f795-128">Nasazení</span><span class="sxs-lookup"><span data-stu-id="3f795-128">Deployment</span></span>

1. <span data-ttu-id="3f795-129">Stáhněte si šablonu z [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="3f795-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="3f795-130">Přihlásit se k aplikaci [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="3f795-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="3f795-131">Vytvořte [skupinu prostředků](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="3f795-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="3f795-132">Vytvořte [účet úložiště](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) ve skupině prostředků, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="3f795-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="3f795-133">Vytvořte [datovou továrnu](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) ve výše uvedené skupině prostředků, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="3f795-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="3f795-134">Otevřete datovou továrnu a vyberte dlaždici **Autor a monitor**.</span><span class="sxs-lookup"><span data-stu-id="3f795-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="3f795-135">Na kartě **Spravovat** vyberte **Šablona ARM**.</span><span class="sxs-lookup"><span data-stu-id="3f795-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="3f795-136">Vyberte **Importovat šablonu ARM** k importování šablony **Strana**.</span><span class="sxs-lookup"><span data-stu-id="3f795-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="3f795-137">Importujte šablonu do datové továrny.</span><span class="sxs-lookup"><span data-stu-id="3f795-137">Import the template into the data factory.</span></span> <span data-ttu-id="3f795-138">Zadejte následující hodnoty pro **Detaily projektu** a **Podrobnosti instance**.</span><span class="sxs-lookup"><span data-stu-id="3f795-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="3f795-139">Pole</span><span class="sxs-lookup"><span data-stu-id="3f795-139">Field</span></span> | <span data-ttu-id="3f795-140">Hodnota</span><span class="sxs-lookup"><span data-stu-id="3f795-140">Value</span></span>
    ---|---
    <span data-ttu-id="3f795-141">Předplatné</span><span class="sxs-lookup"><span data-stu-id="3f795-141">Subscription</span></span> | <span data-ttu-id="3f795-142">Předplatné Azure</span><span class="sxs-lookup"><span data-stu-id="3f795-142">Azure subscription</span></span>
    <span data-ttu-id="3f795-143">Skupina prostředků</span><span class="sxs-lookup"><span data-stu-id="3f795-143">Resource group</span></span> | <span data-ttu-id="3f795-144">Poskytněte stejný prostředek, pod kterým je vytvořen účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="3f795-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="3f795-145">Oblast</span><span class="sxs-lookup"><span data-stu-id="3f795-145">Region</span></span> | <span data-ttu-id="3f795-146">Zadejte region.</span><span class="sxs-lookup"><span data-stu-id="3f795-146">Specify region.</span></span>
    <span data-ttu-id="3f795-147">Název továrny</span><span class="sxs-lookup"><span data-stu-id="3f795-147">Factory Name</span></span> | <span data-ttu-id="3f795-148">Zadejte název továrny.</span><span class="sxs-lookup"><span data-stu-id="3f795-148">Specify factory name.</span></span>
    <span data-ttu-id="3f795-149">Klíč objektu zabezpečení Service_service spojený s FO</span><span class="sxs-lookup"><span data-stu-id="3f795-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="3f795-150">Zadejte klíč aplikace.</span><span class="sxs-lookup"><span data-stu-id="3f795-150">Specify the application's key.</span></span>
    <span data-ttu-id="3f795-151">Řetězec Storage_connection Azure Blob</span><span class="sxs-lookup"><span data-stu-id="3f795-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="3f795-152">Řetězec připojení Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="3f795-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="3f795-153">Dynamics Crm propojené Service_password</span><span class="sxs-lookup"><span data-stu-id="3f795-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="3f795-154">Heslo uživatelského účtu, který jste zadali jako uživatelské jméno.</span><span class="sxs-lookup"><span data-stu-id="3f795-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="3f795-155">Service_properties_type Properties_url propojené s FO</span><span class="sxs-lookup"><span data-stu-id="3f795-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="3f795-156">Service_properties_type Properties_tenant propojené s FO</span><span class="sxs-lookup"><span data-stu-id="3f795-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="3f795-157">Zadejte údaje o klientovi (název domény nebo ID tenanta), pod kterými se vaše aplikace nachází.</span><span class="sxs-lookup"><span data-stu-id="3f795-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="3f795-158">Id prostředku Service_properties_type Properties_aad propojené s FO</span><span class="sxs-lookup"><span data-stu-id="3f795-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="3f795-159">Id objektu zabezpečení Service_properties_type Properties_service propojené s FO</span><span class="sxs-lookup"><span data-stu-id="3f795-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="3f795-160">Zadejte ID klienta aplikace.</span><span class="sxs-lookup"><span data-stu-id="3f795-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="3f795-161">Dynamics Crm spojené Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="3f795-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="3f795-162">Uživatelské jméno pro připojení k Dynamics.</span><span class="sxs-lookup"><span data-stu-id="3f795-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="3f795-163">Další informace viz [Ruční propagace šablony Resource Manageru pro každé prostředí](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Vlastnosti propojené služby](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) a [Kopírování dat pomocí Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="3f795-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="3f795-164">Po nasazení ověřte datové sady, tok dat a propojenou službu datové továrny.</span><span class="sxs-lookup"><span data-stu-id="3f795-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datové sady, tok dat a propojená služba](media/data-factory-validate.png)

11. <span data-ttu-id="3f795-166">Přejděte na **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="3f795-166">Navigate to **Manage**.</span></span> <span data-ttu-id="3f795-167">V části **Připojení** vyberte **Propojená služba**.</span><span class="sxs-lookup"><span data-stu-id="3f795-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="3f795-168">Vyberte **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="3f795-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="3f795-169">Ve formuláři **Upravit propojenou službu (Dynamics CRM)** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="3f795-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="3f795-170">Pole</span><span class="sxs-lookup"><span data-stu-id="3f795-170">Field</span></span> | <span data-ttu-id="3f795-171">Hodnota</span><span class="sxs-lookup"><span data-stu-id="3f795-171">Value</span></span>
    ---|---
    <span data-ttu-id="3f795-172">Jméno</span><span class="sxs-lookup"><span data-stu-id="3f795-172">Name</span></span> | <span data-ttu-id="3f795-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="3f795-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="3f795-174">popis</span><span class="sxs-lookup"><span data-stu-id="3f795-174">Description</span></span> | <span data-ttu-id="3f795-175">Propojené služby pro připojení k instanci CRM k načtení dat entit</span><span class="sxs-lookup"><span data-stu-id="3f795-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="3f795-176">Připojte se pomocí modulu runtime integrace</span><span class="sxs-lookup"><span data-stu-id="3f795-176">Connect via integration runtime</span></span> | <span data-ttu-id="3f795-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f795-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="3f795-178">Typ nasazení</span><span class="sxs-lookup"><span data-stu-id="3f795-178">Deployment type</span></span> | <span data-ttu-id="3f795-179">Online</span><span class="sxs-lookup"><span data-stu-id="3f795-179">Online</span></span>
    <span data-ttu-id="3f795-180">Uri služby</span><span class="sxs-lookup"><span data-stu-id="3f795-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="3f795-181">Typ ověření</span><span class="sxs-lookup"><span data-stu-id="3f795-181">Authentication type</span></span> | <span data-ttu-id="3f795-182">Office365</span><span class="sxs-lookup"><span data-stu-id="3f795-182">Office365</span></span>
    <span data-ttu-id="3f795-183">Uživatelské jméno</span><span class="sxs-lookup"><span data-stu-id="3f795-183">User name</span></span> |
    <span data-ttu-id="3f795-184">Heslo nebo Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="3f795-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="3f795-185">Heslo</span><span class="sxs-lookup"><span data-stu-id="3f795-185">Password</span></span>
    <span data-ttu-id="3f795-186">Heslo</span><span class="sxs-lookup"><span data-stu-id="3f795-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="3f795-187">Spusťte šablonu</span><span class="sxs-lookup"><span data-stu-id="3f795-187">Run the template</span></span>

1. <span data-ttu-id="3f795-188">Zastavte následující dvojitý zápis **Účet**, **Kontakt** a **Prodejce** pomocí aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f795-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="3f795-189">Zákazníci V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="3f795-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="3f795-190">Zákazníci V3(kontakty)</span><span class="sxs-lookup"><span data-stu-id="3f795-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="3f795-191">Kontakty CDS V2(kontakty)</span><span class="sxs-lookup"><span data-stu-id="3f795-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="3f795-192">Kontakty CDS V2(kontakty)</span><span class="sxs-lookup"><span data-stu-id="3f795-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="3f795-193">Dodavatel V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="3f795-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="3f795-194">Ujistěte se, že jsou mapy odstraněny z tabulky `msdy_dualwriteruntimeconfig` v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3f795-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="3f795-195">Nainstalujte [řešení strany a globálního adresáře s duálním zápisem](https://aka.ms/dual-write-gab) z AppSource.</span><span class="sxs-lookup"><span data-stu-id="3f795-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="3f795-196">V aplikaci Finance and Operations, pokud následující tabulky obsahují data, pak pro ně spusťte **Počáteční synchronizaci**.</span><span class="sxs-lookup"><span data-stu-id="3f795-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="3f795-197">Oslovení</span><span class="sxs-lookup"><span data-stu-id="3f795-197">Salutations</span></span>
    + <span data-ttu-id="3f795-198">Typy osobní charakteristiky</span><span class="sxs-lookup"><span data-stu-id="3f795-198">Personal character types</span></span>
    + <span data-ttu-id="3f795-199">Zdvořilostní zakončení</span><span class="sxs-lookup"><span data-stu-id="3f795-199">Complimentary closing</span></span>
    + <span data-ttu-id="3f795-200">Tituly kontaktní osoby</span><span class="sxs-lookup"><span data-stu-id="3f795-200">Contact person titles</span></span>
    + <span data-ttu-id="3f795-201">Role v rozhodovacím procesu</span><span class="sxs-lookup"><span data-stu-id="3f795-201">Decision making roles</span></span>
    + <span data-ttu-id="3f795-202">Úrovně věrnosti</span><span class="sxs-lookup"><span data-stu-id="3f795-202">Loyalty levels</span></span>

5. <span data-ttu-id="3f795-203">V aplikaci pro zapojení zákazníků deaktivujte následující kroky pluginu.</span><span class="sxs-lookup"><span data-stu-id="3f795-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="3f795-204">Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="3f795-204">Account Update</span></span>
         + <span data-ttu-id="3f795-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="3f795-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="3f795-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="3f795-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="3f795-207">Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="3f795-207">Contact Update</span></span>
         + <span data-ttu-id="3f795-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="3f795-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="3f795-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="3f795-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="3f795-210">Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="3f795-210">msdyn_party Update</span></span>
         + <span data-ttu-id="3f795-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="3f795-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="3f795-212">Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="3f795-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="3f795-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="3f795-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="3f795-214">V aplikaci pro zapojení zákazníků deaktivujte následující pracovní postupy:</span><span class="sxs-lookup"><span data-stu-id="3f795-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="3f795-215">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="3f795-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3f795-216">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="3f795-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3f795-217">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="3f795-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="3f795-218">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="3f795-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="3f795-219">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="3f795-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3f795-220">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="3f795-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="3f795-221">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="3f795-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="3f795-222">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="3f795-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="3f795-223">V datové továrně spusťte šablonu výběrem **Spustit hned**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="3f795-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="3f795-224">V závislosti na objemu dat může tento proces trvat několik hodin.</span><span class="sxs-lookup"><span data-stu-id="3f795-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Spustit běh](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="3f795-226">Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit.</span><span class="sxs-lookup"><span data-stu-id="3f795-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="3f795-227">Importujte nové záznamy **Strana** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f795-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="3f795-228">Stáhněte si soubor `FONewParty.csv` z úložiště Azure blob.</span><span class="sxs-lookup"><span data-stu-id="3f795-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="3f795-229">Cesta je `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="3f795-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="3f795-230">Převeďte soubor `FONewParty.csv` do souboru Excel a importujte soubor Excel do souboru aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f795-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="3f795-231">Pokud vám csv import vyhovuje, můžete soubor csv importovat přímo.</span><span class="sxs-lookup"><span data-stu-id="3f795-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="3f795-232">Import může trvat několik hodin, v závislosti na objemu dat.</span><span class="sxs-lookup"><span data-stu-id="3f795-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="3f795-233">Další informace naleznete v tématu [Přehled úloh importu a exportu dat](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span><span class="sxs-lookup"><span data-stu-id="3f795-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![Importování záznamů strany Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="3f795-235">V aplikaci pro zapojení zákazníků aktivujte následující kroky pluginu:</span><span class="sxs-lookup"><span data-stu-id="3f795-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="3f795-236">Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="3f795-236">Account Update</span></span>
         + <span data-ttu-id="3f795-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="3f795-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="3f795-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu</span><span class="sxs-lookup"><span data-stu-id="3f795-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="3f795-239">Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="3f795-239">Contact Update</span></span>
         + <span data-ttu-id="3f795-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="3f795-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="3f795-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu</span><span class="sxs-lookup"><span data-stu-id="3f795-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="3f795-242">Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="3f795-242">msdyn_party Update</span></span>
         + <span data-ttu-id="3f795-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party</span><span class="sxs-lookup"><span data-stu-id="3f795-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="3f795-244">Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="3f795-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="3f795-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="3f795-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="3f795-246">V aplikacích pro zapojení zákazníků aktivujte následující pracovní postupy, pokud jste je deaktivovali v předchozích krocích:</span><span class="sxs-lookup"><span data-stu-id="3f795-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="3f795-247">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="3f795-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3f795-248">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="3f795-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3f795-249">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="3f795-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="3f795-250">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="3f795-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="3f795-251">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="3f795-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3f795-252">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="3f795-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="3f795-253">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="3f795-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="3f795-254">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="3f795-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="3f795-255">Spusťte mapy související se **stranou** podle pokynů v části [Strana a globální adresář](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="3f795-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="3f795-256">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="3f795-256">Troubleshooting</span></span>

1. <span data-ttu-id="3f795-257">V procesu selže, spusťte znovu továrnu dat počínaje neúspěšnou aktivitou.</span><span class="sxs-lookup"><span data-stu-id="3f795-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="3f795-258">Některé soubory generuje datová továrna, kterou můžete použít pro účely ověření dat.</span><span class="sxs-lookup"><span data-stu-id="3f795-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="3f795-259">Datová továrna běží na základě souborů CSV, které jsou odděleny čárkami.</span><span class="sxs-lookup"><span data-stu-id="3f795-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="3f795-260">Pokud existuje hodnota pole s čárkou, může to ovlivnit výsledky.</span><span class="sxs-lookup"><span data-stu-id="3f795-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="3f795-261">Musíte odstranit čárky.</span><span class="sxs-lookup"><span data-stu-id="3f795-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="3f795-262">Karta **Monitorování** poskytuje informace o všech krocích a zpracovaných datech.</span><span class="sxs-lookup"><span data-stu-id="3f795-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="3f795-263">Vyberte konkrétní krok k ladění.</span><span class="sxs-lookup"><span data-stu-id="3f795-263">Select a specific step to debug it.</span></span>

    ![Záložka Monitorování](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="3f795-265">Další informace o šabloně</span><span class="sxs-lookup"><span data-stu-id="3f795-265">Learn more about the template</span></span>

<span data-ttu-id="3f795-266">Komentáře k šabloně najdete v souboru [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="3f795-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>
