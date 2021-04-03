---
title: Doplněk Viditelnost zásob
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574215"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="0a86b-103">Doplněk Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="0a86b-104">Doplněk Viditelnost zásob je nezávislá a vysoce škálovatelná mikroslužba, která umožňuje sledování zásob na skladě v reálném čase, a tím poskytuje globální pohled na viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="0a86b-105">Všechny informace, které se vztahují k zásobám na skladě, se do služby exportují téměř v reálném čase prostřednictvím nízkoúrovňové integrace SQL.</span><span class="sxs-lookup"><span data-stu-id="0a86b-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="0a86b-106">Externí systémy přistupují ke službě prostřednictvím rozhraní API RESTful a dotazují se na praktické informace o daných sadách dimenzí, čímž získávají seznam dostupných pozic.</span><span class="sxs-lookup"><span data-stu-id="0a86b-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="0a86b-107">Viditelnost zásob je mikroslužba postavená na Microsoft Dataverse, což znamená, že ji můžete rozšířit pomocí vytváření Power Apps a použitím Power BI, a poskytovat přizpůsobené funkce pro splnění vašich obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="0a86b-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="0a86b-108">Je také možné upgradovat index za účelem provádění dotazů na zásoby.</span><span class="sxs-lookup"><span data-stu-id="0a86b-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="0a86b-109">Viditelnost zásob poskytuje možnosti konfigurace, které umožňují její integraci s více systémy třetích stran.</span><span class="sxs-lookup"><span data-stu-id="0a86b-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="0a86b-110">Podporuje standardizovanou dimenzi zásob, přizpůsobitelnou rozšiřitelnost a standardizované, konfigurovatelné vypočítané množství.</span><span class="sxs-lookup"><span data-stu-id="0a86b-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="0a86b-111">Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management a jak používat jeho aplikační programovací rozhraní (API).</span><span class="sxs-lookup"><span data-stu-id="0a86b-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="0a86b-112">Instalace doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="0a86b-113">Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0a86b-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0a86b-114">LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich aplikací Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a86b-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="0a86b-115">Další informace naleznete v tématu [Zdroje Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="0a86b-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0a86b-116">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="0a86b-116">Prerequisites</span></span>

<span data-ttu-id="0a86b-117">Před instalací doplňku Viditelnost zásob musíte provést následující:</span><span class="sxs-lookup"><span data-stu-id="0a86b-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="0a86b-118">Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.</span><span class="sxs-lookup"><span data-stu-id="0a86b-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="0a86b-119">Ujistěte se, že předpoklady pro nastavení doplňků uvedené v [Přehledu doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) byly dokončeny.</span><span class="sxs-lookup"><span data-stu-id="0a86b-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="0a86b-120">Viditelnost zásob nevyžaduje propojení duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="0a86b-121">Kontaktujte tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyžádejte si následující tři požadované soubory:</span><span class="sxs-lookup"><span data-stu-id="0a86b-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="0a86b-122">`Inventory Visibility Integration.zip` (pokud je spuštěná verze Supply Chain Management starší než verze 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="0a86b-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="0a86b-123">Mezi aktuálně podporované země a oblasti patří Kanada, Spojené státy a Evropská unie (EU).</span><span class="sxs-lookup"><span data-stu-id="0a86b-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="0a86b-124">Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="0a86b-125">Nastavení Dataverse</span><span class="sxs-lookup"><span data-stu-id="0a86b-125">Set up Dataverse</span></span>

<span data-ttu-id="0a86b-126">Při nastavení Dataverse postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="0a86b-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="0a86b-127">Přidejte svému klientu princip služby:</span><span class="sxs-lookup"><span data-stu-id="0a86b-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="0a86b-128">Nainstalujte Azure AD PowerShell Module v2 dle popisu v tématu [Instalace Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="0a86b-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="0a86b-129">Spusťte následující příkaz PowerShellu:</span><span class="sxs-lookup"><span data-stu-id="0a86b-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="0a86b-130">Vytvořte uživatele aplikace pro Viditelnost zásob v Dataverse:</span><span class="sxs-lookup"><span data-stu-id="0a86b-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="0a86b-131">Otevřete adresu URL svého prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0a86b-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="0a86b-132">Přejděte do uzlu **Pokročilá nastavení \> Systém \> Zabezpečení \> Uživatelé** a vytvořte uživatele aplikace.</span><span class="sxs-lookup"><span data-stu-id="0a86b-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="0a86b-133">Pomocí nabídky zobrazení změňte zobrazení stránky na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="0a86b-134">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-134">Select **New**.</span></span> <span data-ttu-id="0a86b-135">Nastavte ID aplikace na *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="0a86b-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="0a86b-136">(ID objektu se automaticky načte, když uložíte změny.) Název můžete upravit.</span><span class="sxs-lookup"><span data-stu-id="0a86b-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="0a86b-137">Můžete jej například změnit na *Viditelnost zásob*.</span><span class="sxs-lookup"><span data-stu-id="0a86b-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="0a86b-138">Po dokončení zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="0a86b-139">Vyberte příkaz **Přiřadit roli** a potom vyberte **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="0a86b-140">Pokud existuje role, která je pojmenována **Uživatel Common Data Service**, vyberte ji také.</span><span class="sxs-lookup"><span data-stu-id="0a86b-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="0a86b-141">Další informace naleznete v tématu [Vytvoření uživatele aplikace](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="0a86b-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="0a86b-142">Importujte soubor `Inventory Visibility Dataverse Solution.zip`, který obsahuje entity související s konfigurací Dataverse a Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0a86b-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="0a86b-143">Přejděte na stránku **Řešení**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="0a86b-144">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-144">Select **Import**.</span></span>

1. <span data-ttu-id="0a86b-145">Importujte tok triggeru upgradu konfigurace:</span><span class="sxs-lookup"><span data-stu-id="0a86b-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="0a86b-146">Přejděte na stránku Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="0a86b-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="0a86b-147">Ujistěte se, že existuje připojení s názvem *Dataverse (zastaralé)*.</span><span class="sxs-lookup"><span data-stu-id="0a86b-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="0a86b-148">(Pokud neexistuje, vytvořte jej.)</span><span class="sxs-lookup"><span data-stu-id="0a86b-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="0a86b-149">Importujte soubor `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="0a86b-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="0a86b-150">Po importu se trigger zobrazí v části **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="0a86b-151">Inicializujte následující čtyři proměnné na základě informací o prostředí:</span><span class="sxs-lookup"><span data-stu-id="0a86b-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="0a86b-152">ID klienta Azure</span><span class="sxs-lookup"><span data-stu-id="0a86b-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="0a86b-153">ID klienta aplikace Azure</span><span class="sxs-lookup"><span data-stu-id="0a86b-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="0a86b-154">Tajný klíč klienta aplikace Azure</span><span class="sxs-lookup"><span data-stu-id="0a86b-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="0a86b-155">Koncový bod Viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="0a86b-156">Další informace o této proměnné najdete v části [ Nastavení integrace Viditelnosti zásob](#setup-inventory-visibility-integration) v další části tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="0a86b-157">![Trigger konfigurace](media/configuration-trigger.png "Trigger konfigurace")</span><span class="sxs-lookup"><span data-stu-id="0a86b-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="0a86b-158">Vyberte příkaz **Zapnout**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="0a86b-159">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="0a86b-159">Install the add-in</span></span>

<span data-ttu-id="0a86b-160">Pro instalaci doplňku Viditelnost zásob proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="0a86b-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="0a86b-161">Přihlaste se k portálu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="0a86b-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="0a86b-162">Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="0a86b-163">Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.</span><span class="sxs-lookup"><span data-stu-id="0a86b-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="0a86b-164">Na stránce prostředí přejděte dolů, dokud neuvidíte část **Doplňky prostředí** v části **Integrace Power Platform** , kde najdete název prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0a86b-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="0a86b-165">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="0a86b-166">![Stránka prostředí v LCS](media/inventory-visibility-environment.png "Stránka prostředí v LCS")</span><span class="sxs-lookup"><span data-stu-id="0a86b-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="0a86b-167">Vyberte odkaz **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="0a86b-168">Otevře se seznam dostupných doplňků.</span><span class="sxs-lookup"><span data-stu-id="0a86b-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="0a86b-169">V seznamu vyberte možnost **Viditelnost zásob**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="0a86b-170">Zadejte hodnoty pro následující pole pro vaše prostředí:</span><span class="sxs-lookup"><span data-stu-id="0a86b-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="0a86b-171">**ID aplikace AAD (klienta)**</span><span class="sxs-lookup"><span data-stu-id="0a86b-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="0a86b-172">**ID klienta AAD**</span><span class="sxs-lookup"><span data-stu-id="0a86b-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="0a86b-173">![Stránka nastavení doplňku](media/inventory-visibility-setup.png "Stránka nastavení doplňku")</span><span class="sxs-lookup"><span data-stu-id="0a86b-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="0a86b-174">Odsouhlaste smluvní podmínky výběrem zaškrtávacího políčka **Smluvní podmínky**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="0a86b-175">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-175">Select **Install**.</span></span> <span data-ttu-id="0a86b-176">Stav doplňku se zobrazí jako **Probíhá instalace**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="0a86b-177">Po dokončení obnovte stránku, aby se zobrazila změna stavu **Nainstalováno**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="0a86b-178">Odinstalace doplňku</span><span class="sxs-lookup"><span data-stu-id="0a86b-178">Uninstall the add-in</span></span>

<span data-ttu-id="0a86b-179">Chcete-li doplněk odinstalovat, vyberte **Odinstalovat**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="0a86b-180">Po obnovení LCS bude doplněk Viditelnost zásob odebrán.</span><span class="sxs-lookup"><span data-stu-id="0a86b-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="0a86b-181">Proces odinstalace odebere registraci doplňku a také spustí úlohu k vyčištění všech obchodních dat, která jsou uložena ve službě.</span><span class="sxs-lookup"><span data-stu-id="0a86b-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="0a86b-182">Data o spotřebě množství na skladě z aplikace Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0a86b-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="0a86b-183">Nasaďte integrační balíček Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="0a86b-184">Pokud používáte Supply Chain Management verze 10.0.17 nebo starší, kontaktujte tým podpory doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyžádejte si soubor balíčku.</span><span class="sxs-lookup"><span data-stu-id="0a86b-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="0a86b-185">Pak nasaďte balíček do LCS.</span><span class="sxs-lookup"><span data-stu-id="0a86b-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="0a86b-186">Pokud během nasazení dojde k chybě neshody verzí, musíte ručně importovat projekt X++ do vývojového prostředí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="0a86b-187">Pak vytvořte nasaditelný balíček ve vývojovém prostředí a nasaďte jej ve svém produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="0a86b-188">Kód je součástí Supply Chain Management verze 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="0a86b-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="0a86b-189">Pokud používáte tuto verzi nebo novější, nasazení se nevyžaduje.</span><span class="sxs-lookup"><span data-stu-id="0a86b-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="0a86b-190">Zkontrolujte, zda jsou ve vašem prostředí Supply Chain Management zapnuty následující funkce.</span><span class="sxs-lookup"><span data-stu-id="0a86b-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="0a86b-191">(Implicitně jsou zapnuté.)</span><span class="sxs-lookup"><span data-stu-id="0a86b-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="0a86b-192">Popis funkce</span><span class="sxs-lookup"><span data-stu-id="0a86b-192">Feature description</span></span> | <span data-ttu-id="0a86b-193">Verze kódu</span><span class="sxs-lookup"><span data-stu-id="0a86b-193">Code version</span></span> | <span data-ttu-id="0a86b-194">Třída přepnutí</span><span class="sxs-lookup"><span data-stu-id="0a86b-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="0a86b-195">Povolení nebo zákaz používání dimenzí zásob v tabulce InventSum</span><span class="sxs-lookup"><span data-stu-id="0a86b-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="0a86b-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="0a86b-196">10.0.11</span></span> | <span data-ttu-id="0a86b-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="0a86b-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="0a86b-198">Povolení nebo zákaz používání dimenzí zásob v tabulce InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="0a86b-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="0a86b-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="0a86b-199">10.0.12</span></span> | <span data-ttu-id="0a86b-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="0a86b-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="0a86b-201">Nastavení integrace viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="0a86b-202">V aplikaci Supply Chain Management otevřete pracovní prostor **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** a zapněte funkci **Integrace viditelnosti zásob**.</span><span class="sxs-lookup"><span data-stu-id="0a86b-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="0a86b-203">Přejděte do uzlu **Řízení zásob \> Nastavení \> Parametry integrace viditelnosti zásob** a zadejte adresu URL prostředí, ve kterém je spuštěn doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="0a86b-204">Najděte oblast Azure prostředí LCS a zadejte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="0a86b-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="0a86b-205">Adresa URL má následující tvar:</span><span class="sxs-lookup"><span data-stu-id="0a86b-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="0a86b-206">Pokud jste například v Evropě, vaše prostředí bude mít jednu z následujících adres URL:</span><span class="sxs-lookup"><span data-stu-id="0a86b-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="0a86b-207">Nyní jsou k dispozici následující oblasti:</span><span class="sxs-lookup"><span data-stu-id="0a86b-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="0a86b-208">Oblast Azure</span><span class="sxs-lookup"><span data-stu-id="0a86b-208">Azure region</span></span> | <span data-ttu-id="0a86b-209">Krátký název oblasti</span><span class="sxs-lookup"><span data-stu-id="0a86b-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="0a86b-210">Austrálie – východ</span><span class="sxs-lookup"><span data-stu-id="0a86b-210">Australia east</span></span> | <span data-ttu-id="0a86b-211">eau</span><span class="sxs-lookup"><span data-stu-id="0a86b-211">eau</span></span> |
    | <span data-ttu-id="0a86b-212">Austrálie – jihovýchod</span><span class="sxs-lookup"><span data-stu-id="0a86b-212">Australia southeast</span></span> | <span data-ttu-id="0a86b-213">seau</span><span class="sxs-lookup"><span data-stu-id="0a86b-213">seau</span></span> |
    | <span data-ttu-id="0a86b-214">Střední Kanada</span><span class="sxs-lookup"><span data-stu-id="0a86b-214">Canada central</span></span> | <span data-ttu-id="0a86b-215">cca</span><span class="sxs-lookup"><span data-stu-id="0a86b-215">cca</span></span> |
    | <span data-ttu-id="0a86b-216">Kanada – východ</span><span class="sxs-lookup"><span data-stu-id="0a86b-216">Canada east</span></span> | <span data-ttu-id="0a86b-217">eca</span><span class="sxs-lookup"><span data-stu-id="0a86b-217">eca</span></span> |
    | <span data-ttu-id="0a86b-218">Evropa – sever</span><span class="sxs-lookup"><span data-stu-id="0a86b-218">North Europe</span></span> | <span data-ttu-id="0a86b-219">neu</span><span class="sxs-lookup"><span data-stu-id="0a86b-219">neu</span></span> |
    | <span data-ttu-id="0a86b-220">Evropa – západ</span><span class="sxs-lookup"><span data-stu-id="0a86b-220">West Europe</span></span> | <span data-ttu-id="0a86b-221">weu</span><span class="sxs-lookup"><span data-stu-id="0a86b-221">weu</span></span> |
    | <span data-ttu-id="0a86b-222">Východní USA</span><span class="sxs-lookup"><span data-stu-id="0a86b-222">East US</span></span> | <span data-ttu-id="0a86b-223">eus</span><span class="sxs-lookup"><span data-stu-id="0a86b-223">eus</span></span> |
    | <span data-ttu-id="0a86b-224">USA – západ</span><span class="sxs-lookup"><span data-stu-id="0a86b-224">West US</span></span> | <span data-ttu-id="0a86b-225">wus</span><span class="sxs-lookup"><span data-stu-id="0a86b-225">wus</span></span> |

1. <span data-ttu-id="0a86b-226">Přejděte do uzlu **Řízení zásob \> Periodické \> Integrace viditelnosti zásob** a povolte úlohu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="0a86b-227">Všechny události změny zásob z aplikace Supply Chain Management budou nyní odeslány do Viditelnosti zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="0a86b-228">Veřejné rozhraní API doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="0a86b-229">Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů pro integraci.</span><span class="sxs-lookup"><span data-stu-id="0a86b-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="0a86b-230">Podporuje tři hlavní typy interakce:</span><span class="sxs-lookup"><span data-stu-id="0a86b-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="0a86b-231">Odesílání změn zásob na skladě do doplňku z externího systému</span><span class="sxs-lookup"><span data-stu-id="0a86b-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="0a86b-232">Dotazování na aktuální množství zásob na skladě z externího systému</span><span class="sxs-lookup"><span data-stu-id="0a86b-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="0a86b-233">Automatická synchronizace se zásobami na skladě v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0a86b-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="0a86b-234">Automatická synchronizace není součástí veřejného API.</span><span class="sxs-lookup"><span data-stu-id="0a86b-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="0a86b-235">Místo toho se zpracovává na pozadí pro ta prostředí, kde je povolen doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="0a86b-236">Ověřování</span><span class="sxs-lookup"><span data-stu-id="0a86b-236">Authentication</span></span>

<span data-ttu-id="0a86b-237">Token zabezpečení platformy se používá k volání doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="0a86b-238">Proto musíte *token Azure Active Directory (Azure AD)* vygenerovat pomocí vaší aplikace Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0a86b-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="0a86b-239">Poté musíte token Azure AD použít k získání *přístupového tokenu* od služby zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="0a86b-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="0a86b-240">Token služby zabezpečení získáte takto:</span><span class="sxs-lookup"><span data-stu-id="0a86b-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="0a86b-241">Přihlaste se na portál Azure a použijte jej k vyhledání údajů `clientId` a `clientSecret` pro vaši aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0a86b-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="0a86b-242">Načtěte token Azure Active Directory (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:</span><span class="sxs-lookup"><span data-stu-id="0a86b-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0a86b-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="0a86b-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="0a86b-244">**Metoda** - `GET`</span><span class="sxs-lookup"><span data-stu-id="0a86b-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="0a86b-245">**Obsah těla (údaje formuláře)**:</span><span class="sxs-lookup"><span data-stu-id="0a86b-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="0a86b-246">klíč</span><span class="sxs-lookup"><span data-stu-id="0a86b-246">key</span></span> | <span data-ttu-id="0a86b-247">hodnota</span><span class="sxs-lookup"><span data-stu-id="0a86b-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="0a86b-248">id klienta</span><span class="sxs-lookup"><span data-stu-id="0a86b-248">client_id</span></span> | <span data-ttu-id="0a86b-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="0a86b-249">${aadAppId}</span></span> |
        | <span data-ttu-id="0a86b-250">tajný klíč klienta</span><span class="sxs-lookup"><span data-stu-id="0a86b-250">client_secret</span></span> | <span data-ttu-id="0a86b-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="0a86b-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="0a86b-252">typ grantu</span><span class="sxs-lookup"><span data-stu-id="0a86b-252">grant_type</span></span> | <span data-ttu-id="0a86b-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="0a86b-253">client_credentials</span></span> |
        | <span data-ttu-id="0a86b-254">prostředek</span><span class="sxs-lookup"><span data-stu-id="0a86b-254">resource</span></span> | <span data-ttu-id="0a86b-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="0a86b-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="0a86b-256">Měli byste obdržet `aadToken` v odpovědi, která se podobá následujícímu příkladu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="0a86b-257">Formulujte požadavek JSON, který se podobá následujícímu:</span><span class="sxs-lookup"><span data-stu-id="0a86b-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="0a86b-258">Kde:</span><span class="sxs-lookup"><span data-stu-id="0a86b-258">Where:</span></span>
    - <span data-ttu-id="0a86b-259">Hodnota `client_assertion` musí být `aadToken`, který jste obdrželi v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="0a86b-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="0a86b-260">Hodnota `context` musí být ID prostředí, do kterého chcete doplněk nasadit.</span><span class="sxs-lookup"><span data-stu-id="0a86b-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="0a86b-261">Nastavte všechny ostatní hodnoty, jak je znázorněno v příkladu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="0a86b-262">Odešlete požadavek HTTP s následujícími vlastnostmi:</span><span class="sxs-lookup"><span data-stu-id="0a86b-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0a86b-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="0a86b-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="0a86b-264">**Metoda** - `POST`</span><span class="sxs-lookup"><span data-stu-id="0a86b-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="0a86b-265">**Záhlaví HTTP** - Zahrňte verzi API (klíč je `Api-Version` a hodnota je `1.0`)</span><span class="sxs-lookup"><span data-stu-id="0a86b-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="0a86b-266">**Obsah těla** - Zahrňte požadavek JSON, který jste vytvořili v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="0a86b-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="0a86b-267">V odpovědi získáte `access_token`.</span><span class="sxs-lookup"><span data-stu-id="0a86b-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="0a86b-268">To je to, co potřebujete jako nosný token pro volání rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="0a86b-269">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="0a86b-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="0a86b-270">Konfigurace rozhraní API doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="0a86b-271">Před použitím služby musíte dokončit konfigurace popsané v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="0a86b-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="0a86b-272">Konfigurace se může lišit v závislosti na podrobnostech vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="0a86b-273">Obsahuje primárně čtyři části:</span><span class="sxs-lookup"><span data-stu-id="0a86b-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="0a86b-274">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="0a86b-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="0a86b-275">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="0a86b-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="0a86b-276">Indexace</span><span class="sxs-lookup"><span data-stu-id="0a86b-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="0a86b-277">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="0a86b-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="0a86b-278">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="0a86b-278">Partitioning</span></span>

<span data-ttu-id="0a86b-279">Rozdělení může významně ovlivnit výkonnost rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="0a86b-280">Je vhodné definovat schéma, které umožňuje malá seskupení dat a přitom umožňuje smysluplné dotazy na data.</span><span class="sxs-lookup"><span data-stu-id="0a86b-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="0a86b-281">`organizationId` (`dataAreaId` v Supply Chain Management) bude vždy součástí rozdělení a ve výchozím nastavení je Viditelnost zásob nastavena na rozdělení podle dimenzí jako *Pracoviště + skladové místo*.</span><span class="sxs-lookup"><span data-stu-id="0a86b-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="0a86b-282">To znamená, že služba musí být vždy dotazována s těmito dimenzemi definovanými na filtrech.</span><span class="sxs-lookup"><span data-stu-id="0a86b-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="0a86b-283">*Pracoviště* a *Skladové místo* jsou dvě obecné výchozí dimenze ve Viditelnosti zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="0a86b-284">V aplikaci Supply Chain Management se tyto dimenze nazývají *Pracoviště* (`InventSiteId`) a *Sklad* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="0a86b-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="0a86b-285">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="0a86b-285">Dimension configurations</span></span>

<span data-ttu-id="0a86b-286">Viditelnost zásob poskytne seznam obecných výchozích dimenzí umožňujících integraci více zdrojových systémů.</span><span class="sxs-lookup"><span data-stu-id="0a86b-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="0a86b-287">V následující tabulce jsou uvedeny dimenze zásob, které budou výchozími názvy dimenzí v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="0a86b-288">Typ dimenze</span><span class="sxs-lookup"><span data-stu-id="0a86b-288">Dimension type</span></span> | <span data-ttu-id="0a86b-289">Název dimenze</span><span class="sxs-lookup"><span data-stu-id="0a86b-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="0a86b-290">Produkt</span><span class="sxs-lookup"><span data-stu-id="0a86b-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="0a86b-291">Produkt</span><span class="sxs-lookup"><span data-stu-id="0a86b-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="0a86b-292">Produkt</span><span class="sxs-lookup"><span data-stu-id="0a86b-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="0a86b-293">Produkt</span><span class="sxs-lookup"><span data-stu-id="0a86b-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="0a86b-294">Sledování</span><span class="sxs-lookup"><span data-stu-id="0a86b-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="0a86b-295">Sledování</span><span class="sxs-lookup"><span data-stu-id="0a86b-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="0a86b-296">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="0a86b-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="0a86b-297">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="0a86b-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="0a86b-298">Stav zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="0a86b-299">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="0a86b-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="0a86b-300">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="0a86b-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="0a86b-301">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="0a86b-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="0a86b-302">Typ dimenze uvedený v předchozí tabulce slouží pouze pro informaci.</span><span class="sxs-lookup"><span data-stu-id="0a86b-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="0a86b-303">V doplňku Viditelnost zásob není nutné definovat typ dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="0a86b-304">Pokud vlastní dimenze existuje a je třeba ji přepnout na výchozí hodnotu, když je spotřebována doplňkem Viditelnost zásob, můžete nakonfigurovat název **Vlastní dimenze** v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="0a86b-305">Externí systémy přistupují k doplňku Viditelnost zásob prostřednictvím rozhraní RESTful API, která umožňují dotazování na informace o dostupnosti na skladě u daných sad dimenzí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="0a86b-306">Pro integraci vám doplněk Viditelnost zásob umožňuje konfigurovat *externí zdroj dat kanálu* a zdrojovou dimenzi do *cílových dimenzí* v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="0a86b-307">Cílové dimenze by měly být jednou z následujících:</span><span class="sxs-lookup"><span data-stu-id="0a86b-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="0a86b-308">Výchozí dimenze v doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="0a86b-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="0a86b-309">Vlastní dimenze</span><span class="sxs-lookup"><span data-stu-id="0a86b-309">Custom dimensions</span></span>

<span data-ttu-id="0a86b-310">Účelem konfigurace dimenze je standardizovat integraci více systémů pro dotazování na dimenzích a publikování události s dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="0a86b-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="0a86b-311">Indexace</span><span class="sxs-lookup"><span data-stu-id="0a86b-311">Indexing</span></span>

<span data-ttu-id="0a86b-312">Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni, ale možná budete chtít vidět výsledky agregované na základě dimenzí zásob.</span><span class="sxs-lookup"><span data-stu-id="0a86b-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="0a86b-313">Viditelnost zásob poskytuje flexibilitu tím, že umožňuje nastavit indexy, které jsou založeny na dimenzi nebo kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="0a86b-314">V současné době můžete indexy nakonfigurovat pouze na maximálně pět.</span><span class="sxs-lookup"><span data-stu-id="0a86b-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="0a86b-315">Před implementací musíte pečlivě zvážit, kterou dimenzi nebo kombinaci dimenzí použijete, abyste zajistili, že bude vyhovovat vašim obchodním potřebám.</span><span class="sxs-lookup"><span data-stu-id="0a86b-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="0a86b-316">Chcete-li se například dotazovat na produkty následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="0a86b-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="0a86b-317">Dotazujte se na agregované zásoby na skladě produktu podle dimenzí *Barva* a *Velikost*.</span><span class="sxs-lookup"><span data-stu-id="0a86b-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="0a86b-318">V některých případech se chcete pouze dotazovat na produkt celkem.</span><span class="sxs-lookup"><span data-stu-id="0a86b-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="0a86b-319">Měli byste dva indexy definované následovně:</span><span class="sxs-lookup"><span data-stu-id="0a86b-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="0a86b-320">Prázdná závorka se agreguje na základě ID produktu v oddílu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="0a86b-321">Indexování definuje, jak můžete seskupit výsledky na základě nastavení dotazu `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="0a86b-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="0a86b-322">V tomto případě, pokud nedefinujete žádné hodnoty `groupBy`, získáte součty `productid`.</span><span class="sxs-lookup"><span data-stu-id="0a86b-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="0a86b-323">Pokud definujete `groupBy` jako `groupBy=ColorId&groupBy=SizeId`, vrátí se vám více řádků na základě různých kombinací barev a velikostí v systému.</span><span class="sxs-lookup"><span data-stu-id="0a86b-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="0a86b-324">Kritéria dotazu můžete zadat do textu požadavku.</span><span class="sxs-lookup"><span data-stu-id="0a86b-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="0a86b-325">Zde je ukázkový dotaz na produkt s kombinací barev a velikostí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-325">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="0a86b-326">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="0a86b-326">Custom measurement</span></span>

<span data-ttu-id="0a86b-327">Výchozí množství měření jsou spojena se Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0a86b-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="0a86b-328">Možná však budete chtít množství, které je tvořeno kombinací výchozích měření.</span><span class="sxs-lookup"><span data-stu-id="0a86b-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="0a86b-329">Chcete-li to provést, můžete mít konfiguraci vlastních množství, která budou přidána k výstupu dotazů na zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="0a86b-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="0a86b-330">Funkce jednoduše umožňuje definovat sadu měrných systémů, které budou přidány, anebo sadu měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.</span><span class="sxs-lookup"><span data-stu-id="0a86b-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="0a86b-331">Například s následující podmínkou dotazu nakonfigurujete vlastní množství měrné jednotky jako `MyCustomAvailableforReservation`, která má být spotřebována systémem spotřeby.</span><span class="sxs-lookup"><span data-stu-id="0a86b-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="0a86b-332">Systém spotřeby</span><span class="sxs-lookup"><span data-stu-id="0a86b-332">Consumption system</span></span> | <span data-ttu-id="0a86b-333">Vypočtené měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="0a86b-333">Calculated measurers</span></span> | <span data-ttu-id="0a86b-334">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="0a86b-334">Data source</span></span> | <span data-ttu-id="0a86b-335">Modifikátor</span><span class="sxs-lookup"><span data-stu-id="0a86b-335">Modifier</span></span> | <span data-ttu-id="0a86b-336">Typ výpočtu modifikátoru</span><span class="sxs-lookup"><span data-stu-id="0a86b-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="0a86b-337">Sčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="0a86b-338">Sčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="0a86b-339">Odčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="0a86b-340">Sčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="0a86b-341">Odčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="0a86b-342">Sčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="0a86b-343">Sčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="0a86b-344">Odčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="0a86b-345">Odčítání</span><span class="sxs-lookup"><span data-stu-id="0a86b-345">Subtraction</span></span> |

<span data-ttu-id="0a86b-346">Takto dotaz na vlastní množství měrnou jednotku vrátí následující výstup.</span><span class="sxs-lookup"><span data-stu-id="0a86b-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="0a86b-347">Výstup `MyCustomAvailableforReservation` je založen na nastavení výpočtu ve vlastních měrných systémech jako:</span><span class="sxs-lookup"><span data-stu-id="0a86b-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="0a86b-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="0a86b-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="0a86b-349">Publikování změn množství na skladě</span><span class="sxs-lookup"><span data-stu-id="0a86b-349">Posting on-hand changes</span></span>

<span data-ttu-id="0a86b-350">Přesná adresa URL, na kterou bude událost publikována, bude záviset na vaší zeměpisné oblasti.</span><span class="sxs-lookup"><span data-stu-id="0a86b-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="0a86b-351">Bude mít formu:</span><span class="sxs-lookup"><span data-stu-id="0a86b-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="0a86b-352">Po ověření lze tuto adresu URL použít společně s metodou HTTP `POST` pro odesílání událostí změny zásob na skladě do služby.</span><span class="sxs-lookup"><span data-stu-id="0a86b-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="0a86b-353">Pro komunikaci se službami Dynamics 365 prostřednictvím požadavků HTTP se používá speciální záhlaví, které označuje ID prostředí instance Supply Chain Management, ke které jsou data propojena.</span><span class="sxs-lookup"><span data-stu-id="0a86b-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="0a86b-354">Například:</span><span class="sxs-lookup"><span data-stu-id="0a86b-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="0a86b-355">Zveřejnění dotazu na změny zásob na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="0a86b-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="0a86b-356">Tento příklad ukazuje scénář, ve kterém nastavíte konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0a86b-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0a86b-357">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0a86b-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0a86b-358">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0a86b-359">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="0a86b-360">Zveřejnění dotazu na změny zásob na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="0a86b-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="0a86b-361">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0a86b-362">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` hodnotu null, je prázdné nebo má mezeru.</span><span class="sxs-lookup"><span data-stu-id="0a86b-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="0a86b-363">Vlastnosti pole dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="0a86b-363">JSON document field properties</span></span>

<span data-ttu-id="0a86b-364">Pole z dříve poskytnutých příkladů dotazů JSON mají vlastnosti uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="0a86b-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="0a86b-365">ID pole</span><span class="sxs-lookup"><span data-stu-id="0a86b-365">Field ID</span></span> | <span data-ttu-id="0a86b-366">popis</span><span class="sxs-lookup"><span data-stu-id="0a86b-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="0a86b-367">Jedinečné ID pro konkrétní událost změny.</span><span class="sxs-lookup"><span data-stu-id="0a86b-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="0a86b-368">Toto ID se používá k zajištění toho, že pokud komunikace se službou během publikování selže, opětovné odeslání události nebude mít za následek, že se v systému dvakrát započítá stejná událost.</span><span class="sxs-lookup"><span data-stu-id="0a86b-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="0a86b-369">Identifikátor organizace spojené s událostí.</span><span class="sxs-lookup"><span data-stu-id="0a86b-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="0a86b-370">To se mapuje na organizace Supply Chain Management nebo ID datové oblasti.</span><span class="sxs-lookup"><span data-stu-id="0a86b-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="0a86b-371">Identifikátor daného produktu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="0a86b-372">Množství, o které je třeba změnit zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="0a86b-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="0a86b-373">Pokud by bylo například na polici přidáno 10 nových housek, byla by tato hodnota 10.</span><span class="sxs-lookup"><span data-stu-id="0a86b-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="0a86b-374">Pokud by pak byly 3 housky odebrány z police nebo prodány, byla by tato hodnota -3.</span><span class="sxs-lookup"><span data-stu-id="0a86b-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="0a86b-375">Zdroj dat dimenzí použitých v události změny publikování změny a dotazu.</span><span class="sxs-lookup"><span data-stu-id="0a86b-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="0a86b-376">Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="0a86b-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="0a86b-377">S konfigurací dimenzí může Viditelnost dat mapovat vlastní dimenze na obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="0a86b-378">Pokud není zadán `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="0a86b-379">Dynamická sada párů klíč/hodnota.</span><span class="sxs-lookup"><span data-stu-id="0a86b-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="0a86b-380">Budou mapovány na některé dimenze v Supply Chain Management, ale můžete také přidat vlastní dimenze (jako *Zdroj*), což může naznačovat, že událost pocházela ze Supply Chain Managementu nebo externího systému.</span><span class="sxs-lookup"><span data-stu-id="0a86b-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="0a86b-381">Dotaz na aktuální zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="0a86b-381">Querying current on-hand</span></span>

<span data-ttu-id="0a86b-382">Koncový bod pro dotazování na aktuální zásoby na skladě bude mít podobnou adresu URL:</span><span class="sxs-lookup"><span data-stu-id="0a86b-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="0a86b-383">Bude dotazován pomocí metody HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="0a86b-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="0a86b-384">Dotaz na aktuální zásoby na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="0a86b-384">Current on-hand query example 1</span></span>

<span data-ttu-id="0a86b-385">Tento příklad ukazuje scénář, ve kterém jste dokončili konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0a86b-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0a86b-386">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0a86b-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0a86b-387">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0a86b-388">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="0a86b-389">Můžete určit `DimensionDataSource` v `filters` a zadat vlastní dimenze v `filters` i `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="0a86b-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="0a86b-390">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="0a86b-391">Dotaz na aktuální zásoby na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="0a86b-391">Current on-hand query example 2</span></span>

<span data-ttu-id="0a86b-392">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="0a86b-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0a86b-393">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` pod `filters` hodnotu null nebo mezeru.</span><span class="sxs-lookup"><span data-stu-id="0a86b-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="0a86b-394">Příklad výsledku vrácení</span><span class="sxs-lookup"><span data-stu-id="0a86b-394">Example return result</span></span>

<span data-ttu-id="0a86b-395">Dotazy zobrazené v předchozích příkladech by mohly vrátit takový výsledek.</span><span class="sxs-lookup"><span data-stu-id="0a86b-395">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="0a86b-396">Všimněte si, že pole množství jsou strukturována jako slovník měrných jednotek a jejich přidružených hodnot.</span><span class="sxs-lookup"><span data-stu-id="0a86b-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
