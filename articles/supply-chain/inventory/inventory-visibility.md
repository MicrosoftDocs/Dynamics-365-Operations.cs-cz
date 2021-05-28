---
title: Doplněk Viditelnost zásob
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6016999"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="2c8c2-103">Doplněk Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="2c8c2-104">Doplněk Viditelnost zásob je nezávislá a vysoce škálovatelná mikroslužba, která umožňuje sledování zásob na skladě v reálném čase, a tím poskytuje globální pohled na viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="2c8c2-105">Všechny informace, které se vztahují k zásobám na skladě, se do služby exportují téměř v reálném čase prostřednictvím nízkoúrovňové integrace SQL.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="2c8c2-106">Externí systémy přistupují ke službě prostřednictvím rozhraní API RESTful a dotazují se na praktické informace o daných sadách dimenzí, čímž získávají seznam dostupných pozic.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="2c8c2-107">Viditelnost zásob je mikroslužba postavená na Microsoft Dataverse, což znamená, že ji můžete rozšířit pomocí vytváření Power Apps a použitím Power BI, a poskytovat přizpůsobené funkce pro splnění vašich obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="2c8c2-108">Je také možné upgradovat index za účelem provádění dotazů na zásoby.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="2c8c2-109">Viditelnost zásob poskytuje možnosti konfigurace, které umožňují její integraci s více systémy třetích stran.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="2c8c2-110">Podporuje standardizovanou dimenzi zásob, přizpůsobitelnou rozšiřitelnost a standardizované, konfigurovatelné vypočítané množství.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="2c8c2-111">Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management a jak používat jeho aplikační programovací rozhraní (API).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="2c8c2-112">Instalace doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="2c8c2-113">Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2c8c2-114">LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich aplikací Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="2c8c2-115">Další informace naleznete v tématu [Zdroje Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="2c8c2-116">Předpoklady pro doplněk viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="2c8c2-117">Před instalací doplňku Viditelnost zásob musíte provést následující:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="2c8c2-118">Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="2c8c2-119">Ujistěte se, že předpoklady pro nastavení doplňků uvedené v [Přehledu doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) byly dokončeny.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="2c8c2-120">Viditelnost zásob nevyžaduje propojení duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="2c8c2-121">Kontaktujte tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyžádejte si následující tři požadované soubory:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="2c8c2-122">`Inventory Visibility Integration.zip` (pokud je spuštěná verze Supply Chain Management starší než verze 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="2c8c2-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="2c8c2-123">Případně kontaktujte tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) pro získání balíčků programu Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="2c8c2-124">Tyto balíčky může používat oficiální nástroj pro nasazení balíčků.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="2c8c2-125">`InventoryServiceApplication.PackageDeployer.zip` (tento balíček obsahuje všechny změny v balíčku `InventoryServiceBase`, plus další komponenty aplikace uživatelského rozhraní)</span><span class="sxs-lookup"><span data-stu-id="2c8c2-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="2c8c2-126">Postupujte podle pokynů v části [Rychlý start: Registrace aplikace na platformě identity Microsoft](/azure/active-directory/develop/quickstart-register-app) k registraci aplikace a přidání klientského tajného klíče do AAD v rámci vašeho předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="2c8c2-127">Registrace aplikace</span><span class="sxs-lookup"><span data-stu-id="2c8c2-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="2c8c2-128">Přidání tajného klíče klienta</span><span class="sxs-lookup"><span data-stu-id="2c8c2-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="2c8c2-129">**ID aplikace (klient)**, **Tajný klíč klienta** a **ID klienta** bude použito v následujících krocích.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="2c8c2-130">Mezi aktuálně podporované země a oblasti patří Kanada, Spojené státy a Evropská unie (EU).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="2c8c2-131">Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="2c8c2-132">Nastavení Dataverse</span><span class="sxs-lookup"><span data-stu-id="2c8c2-132">Set up Dataverse</span></span>

<span data-ttu-id="2c8c2-133">Pokud chcete nastavit Dataverse pro použití s Inventory Visibility, musíte nejprve připravit předpoklady a poté se rozhodnout, zda nastavit Dataverse buď pomocí nástroje Package Deployer, nebo ručním importem řešení (nemusíte dělat obojí).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="2c8c2-134">Pak instalujte doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="2c8c2-135">Následující pododdíly popisují, jak jednotlivé z těchto úkolů provádět.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="2c8c2-136">Předpoklady pro přípravu Dataverse</span><span class="sxs-lookup"><span data-stu-id="2c8c2-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="2c8c2-137">Než začnete nastavovat Dataverse, přidejte do svého klienta princip služby následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="2c8c2-138">Nainstalujte Azure AD PowerShell Module v2 dle popisu v tématu [Instalace Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="2c8c2-139">Spusťte následující příkaz PowerShellu:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="2c8c2-140">Nastavte Dataverse pomocí nástroje Package Deployer</span><span class="sxs-lookup"><span data-stu-id="2c8c2-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="2c8c2-141">Až budete mít předpoklady, použijte následující postup, pokud dáváte přednost nastavení Dataverse pomocí nástroje pro zavádění balíčků.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="2c8c2-142">V další části najdete podrobnosti o tom, jak místo toho importovat řešení ručně (nedělejte obojí).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="2c8c2-143">Nainstalujte vývojářské nástroje podle popisu v části [Stáhněte si nástroje z NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="2c8c2-144">Na základě vašich obchodních požadavků vyberte balíček `InventoryServiceBase` nebo `InventoryServiceApplication`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="2c8c2-145">Import řešení:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-145">Import the solutions:</span></span>
    1. <span data-ttu-id="2c8c2-146">Pro balíček `InventoryServiceBase`:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="2c8c2-147">Rozbalte `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="2c8c2-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="2c8c2-148">Najděte složku `InventoryServiceBase`, soubor `[Content_Types].xml`, soubor `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, soubor `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` a soubor `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="2c8c2-149">Zkopírujte každou z těchto složek a souborů do adresáře `.\Tools\PackageDeployment`, který byl vytvořen při instalaci vývojářských nástrojů.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="2c8c2-150">Pro balíček `InventoryServiceApplication`:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="2c8c2-151">Rozbalte `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="2c8c2-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="2c8c2-152">Najděte složku `InventoryServiceApplication`, soubor `[Content_Types].xml`, soubor `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, soubor `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` a soubor `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="2c8c2-153">Zkopírujte každou z těchto složek a souborů do adresáře `.\Tools\PackageDeployment`, který byl vytvořen při instalaci vývojářských nástrojů.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="2c8c2-154">Proveďte `.\Tools\PackageDeployment\PackageDeployer.exe`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="2c8c2-155">Podle pokynů na obrazovce importujte řešení.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="2c8c2-156">Přiřazení rolí zabezpečení uživateli aplikace.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="2c8c2-157">Otevřete adresu URL svého prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="2c8c2-158">Jděte na **Pokročilé nastavení \> Systém \> Zabezpečení \> Uživatelé** a vyhledejte uživatele **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="2c8c2-159">Vyberte příkaz **Přiřadit roli** a potom vyberte **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="2c8c2-160">Pokud existuje role nazvaná **Uživatel Common Data Service**, vyberte ji také.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="2c8c2-161">Ručně nastavte Dataverse importem řešení</span><span class="sxs-lookup"><span data-stu-id="2c8c2-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="2c8c2-162">Až budete mít nasazené předpoklady, použijte následující postup, pokud dáváte přednost nastavení Dataverse pomocí ručního importu řešení.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="2c8c2-163">V předchozí části najdete podrobnosti o tom, jak místo toho použít nástroj pro nasazení balíčku (nedělejte obojí).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="2c8c2-164">Vytvořte uživatele aplikace pro Viditelnost zásob v Dataverse:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="2c8c2-165">Otevřete adresu URL svého prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="2c8c2-166">Přejděte do uzlu **Pokročilá nastavení \> Systém \> Zabezpečení \> Uživatelé** a vytvořte uživatele aplikace.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="2c8c2-167">Pomocí nabídky zobrazení změňte zobrazení stránky na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="2c8c2-168">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-168">Select **New**.</span></span> <span data-ttu-id="2c8c2-169">Nastavte ID aplikace na *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="2c8c2-170">(ID objektu se automaticky načte, když uložíte změny.) Název můžete upravit.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="2c8c2-171">Můžete jej například změnit na *Viditelnost zásob*.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="2c8c2-172">Po dokončení zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="2c8c2-173">Vyberte příkaz **Přiřadit roli** a potom vyberte **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="2c8c2-174">Pokud existuje role, která je pojmenována **Uživatel Common Data Service**, vyberte ji také.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="2c8c2-175">Další informace naleznete v tématu [Vytvoření uživatele aplikace](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="2c8c2-176">Pokud výchozí jazyk vašeho Dataverse není **angličtina**:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="2c8c2-177">Přejděte do **Pokročilé nastavení \> Správa \> Jazyky**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="2c8c2-178">Vyberte **Angličtina (LanguageCode = 1033)** a vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="2c8c2-179">Importujte soubor `Inventory Visibility Dataverse Solution.zip`, který obsahuje entity související s konfigurací Dataverse a Power Apps:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="2c8c2-180">Přejděte na stránku **Řešení**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="2c8c2-181">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-181">Select **Import**.</span></span>

1. <span data-ttu-id="2c8c2-182">Importujte tok triggeru upgradu konfigurace:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="2c8c2-183">Přejděte na stránku Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="2c8c2-184">Ujistěte se, že existuje připojení s názvem *Dataverse (zastaralé)*.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="2c8c2-185">(Pokud neexistuje, vytvořte jej.)</span><span class="sxs-lookup"><span data-stu-id="2c8c2-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="2c8c2-186">Importujte soubor `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="2c8c2-187">Po importu se trigger zobrazí v části **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="2c8c2-188">Inicializujte následující čtyři proměnné na základě informací o prostředí:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="2c8c2-189">ID klienta Azure</span><span class="sxs-lookup"><span data-stu-id="2c8c2-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="2c8c2-190">ID klienta aplikace Azure</span><span class="sxs-lookup"><span data-stu-id="2c8c2-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="2c8c2-191">Tajný klíč klienta aplikace Azure</span><span class="sxs-lookup"><span data-stu-id="2c8c2-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="2c8c2-192">Koncový bod Viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="2c8c2-193">Další informace o této proměnné najdete v části [ Nastavení integrace Viditelnosti zásob](#setup-inventory-visibility-integration) v další části tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="2c8c2-194">![Trigger konfigurace](media/configuration-trigger.png "Trigger konfigurace")</span><span class="sxs-lookup"><span data-stu-id="2c8c2-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="2c8c2-195">Vyberte příkaz **Zapnout**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="2c8c2-196">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="2c8c2-196">Install the add-in</span></span>

<span data-ttu-id="2c8c2-197">Pro instalaci doplňku Viditelnost zásob proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="2c8c2-198">Přihlaste se k portálu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="2c8c2-199">Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="2c8c2-200">Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="2c8c2-201">Na stránce prostředí přejděte dolů, dokud neuvidíte část **Doplňky prostředí** v části **Integrace Power Platform** , kde najdete název prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="2c8c2-202">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="2c8c2-203">![Stránka prostředí v LCS](media/inventory-visibility-environment.png "Stránka prostředí v LCS")</span><span class="sxs-lookup"><span data-stu-id="2c8c2-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="2c8c2-204">Vyberte odkaz **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="2c8c2-205">Otevře se seznam dostupných doplňků.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="2c8c2-206">V seznamu vyberte možnost **Viditelnost zásob**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="2c8c2-207">Zadejte hodnoty pro následující pole pro vaše prostředí:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="2c8c2-208">**ID aplikace AAD (klienta)**</span><span class="sxs-lookup"><span data-stu-id="2c8c2-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="2c8c2-209">**ID klienta AAD**</span><span class="sxs-lookup"><span data-stu-id="2c8c2-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="2c8c2-210">![Stránka nastavení doplňku](media/inventory-visibility-setup.png "Stránka nastavení doplňku")</span><span class="sxs-lookup"><span data-stu-id="2c8c2-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="2c8c2-211">Odsouhlaste smluvní podmínky výběrem zaškrtávacího políčka **Smluvní podmínky**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="2c8c2-212">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-212">Select **Install**.</span></span> <span data-ttu-id="2c8c2-213">Stav doplňku se zobrazí jako **Probíhá instalace**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="2c8c2-214">Po dokončení obnovte stránku, aby se zobrazila změna stavu **Nainstalováno**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="2c8c2-215">Odinstalace doplňku</span><span class="sxs-lookup"><span data-stu-id="2c8c2-215">Uninstall the add-in</span></span>

<span data-ttu-id="2c8c2-216">Chcete-li doplněk odinstalovat, vyberte **Odinstalovat**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="2c8c2-217">Po obnovení LCS bude doplněk Viditelnost zásob odebrán.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="2c8c2-218">Proces odinstalace odebere registraci doplňku a také spustí úlohu k vyčištění všech obchodních dat, která jsou uložena ve službě.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="2c8c2-219">Data o spotřebě množství na skladě z aplikace Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2c8c2-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="2c8c2-220">Nasaďte integrační balíček Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="2c8c2-221">Pokud používáte Supply Chain Management verze 10.0.17 nebo starší, kontaktujte tým podpory doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyžádejte si soubor balíčku.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="2c8c2-222">Pak nasaďte balíček do LCS.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="2c8c2-223">Pokud během nasazení dojde k chybě neshody verzí, musíte ručně importovat projekt X++ do vývojového prostředí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="2c8c2-224">Pak vytvořte nasaditelný balíček ve vývojovém prostředí a nasaďte jej ve svém produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="2c8c2-225">Kód je součástí Supply Chain Management verze 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="2c8c2-226">Pokud používáte tuto verzi nebo novější, nasazení se nevyžaduje.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="2c8c2-227">Zkontrolujte, zda jsou ve vašem prostředí Supply Chain Management zapnuty následující funkce.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="2c8c2-228">(Implicitně jsou zapnuté.)</span><span class="sxs-lookup"><span data-stu-id="2c8c2-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="2c8c2-229">Popis funkce</span><span class="sxs-lookup"><span data-stu-id="2c8c2-229">Feature description</span></span> | <span data-ttu-id="2c8c2-230">Verze kódu</span><span class="sxs-lookup"><span data-stu-id="2c8c2-230">Code version</span></span> | <span data-ttu-id="2c8c2-231">Třída přepnutí</span><span class="sxs-lookup"><span data-stu-id="2c8c2-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="2c8c2-232">Povolení nebo zákaz používání dimenzí zásob v tabulce InventSum</span><span class="sxs-lookup"><span data-stu-id="2c8c2-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="2c8c2-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="2c8c2-233">10.0.11</span></span> | <span data-ttu-id="2c8c2-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="2c8c2-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="2c8c2-235">Povolení nebo zákaz používání dimenzí zásob v tabulce InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="2c8c2-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="2c8c2-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="2c8c2-236">10.0.12</span></span> | <span data-ttu-id="2c8c2-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="2c8c2-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="2c8c2-238">Nastavení integrace viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="2c8c2-239">V aplikaci Supply Chain Management otevřete pracovní prostor **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** a zapněte funkci **Integrace viditelnosti zásob**.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="2c8c2-240">Přejděte do uzlu **Řízení zásob \> Nastavení \> Parametry integrace viditelnosti zásob** a zadejte adresu URL prostředí, ve kterém je spuštěn doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="2c8c2-241">Najděte oblast Azure prostředí LCS a zadejte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="2c8c2-242">Adresa URL má následující tvar:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="2c8c2-243">Pokud jste například v Evropě, vaše prostředí bude mít jednu z následujících adres URL:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="2c8c2-244">Nyní jsou k dispozici následující oblasti:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="2c8c2-245">Oblast Azure</span><span class="sxs-lookup"><span data-stu-id="2c8c2-245">Azure region</span></span> | <span data-ttu-id="2c8c2-246">Krátký název oblasti</span><span class="sxs-lookup"><span data-stu-id="2c8c2-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="2c8c2-247">Austrálie – východ</span><span class="sxs-lookup"><span data-stu-id="2c8c2-247">Australia east</span></span> | <span data-ttu-id="2c8c2-248">eau</span><span class="sxs-lookup"><span data-stu-id="2c8c2-248">eau</span></span> |
    | <span data-ttu-id="2c8c2-249">Austrálie – jihovýchod</span><span class="sxs-lookup"><span data-stu-id="2c8c2-249">Australia southeast</span></span> | <span data-ttu-id="2c8c2-250">seau</span><span class="sxs-lookup"><span data-stu-id="2c8c2-250">seau</span></span> |
    | <span data-ttu-id="2c8c2-251">Střední Kanada</span><span class="sxs-lookup"><span data-stu-id="2c8c2-251">Canada central</span></span> | <span data-ttu-id="2c8c2-252">cca</span><span class="sxs-lookup"><span data-stu-id="2c8c2-252">cca</span></span> |
    | <span data-ttu-id="2c8c2-253">Kanada – východ</span><span class="sxs-lookup"><span data-stu-id="2c8c2-253">Canada east</span></span> | <span data-ttu-id="2c8c2-254">eca</span><span class="sxs-lookup"><span data-stu-id="2c8c2-254">eca</span></span> |
    | <span data-ttu-id="2c8c2-255">Evropa – sever</span><span class="sxs-lookup"><span data-stu-id="2c8c2-255">North Europe</span></span> | <span data-ttu-id="2c8c2-256">neu</span><span class="sxs-lookup"><span data-stu-id="2c8c2-256">neu</span></span> |
    | <span data-ttu-id="2c8c2-257">Evropa – západ</span><span class="sxs-lookup"><span data-stu-id="2c8c2-257">West Europe</span></span> | <span data-ttu-id="2c8c2-258">weu</span><span class="sxs-lookup"><span data-stu-id="2c8c2-258">weu</span></span> |
    | <span data-ttu-id="2c8c2-259">Východní USA</span><span class="sxs-lookup"><span data-stu-id="2c8c2-259">East US</span></span> | <span data-ttu-id="2c8c2-260">eus</span><span class="sxs-lookup"><span data-stu-id="2c8c2-260">eus</span></span> |
    | <span data-ttu-id="2c8c2-261">USA – západ</span><span class="sxs-lookup"><span data-stu-id="2c8c2-261">West US</span></span> | <span data-ttu-id="2c8c2-262">wus</span><span class="sxs-lookup"><span data-stu-id="2c8c2-262">wus</span></span> |

1. <span data-ttu-id="2c8c2-263">Přejděte do uzlu **Řízení zásob \> Periodické \> Integrace viditelnosti zásob** a povolte úlohu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="2c8c2-264">Všechny události změny zásob z aplikace Supply Chain Management budou nyní odeslány do Viditelnosti zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="2c8c2-265">Veřejné rozhraní API doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="2c8c2-266">Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů pro integraci.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="2c8c2-267">Podporuje tři hlavní typy interakce:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="2c8c2-268">Odesílání změn zásob na skladě do doplňku z externího systému</span><span class="sxs-lookup"><span data-stu-id="2c8c2-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="2c8c2-269">Dotazování na aktuální množství zásob na skladě z externího systému</span><span class="sxs-lookup"><span data-stu-id="2c8c2-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="2c8c2-270">Automatická synchronizace se zásobami na skladě v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2c8c2-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="2c8c2-271">Automatická synchronizace není součástí veřejného API.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="2c8c2-272">Místo toho se zpracovává na pozadí pro ta prostředí, kde je povolen doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="2c8c2-273">Ověřování</span><span class="sxs-lookup"><span data-stu-id="2c8c2-273">Authentication</span></span>

<span data-ttu-id="2c8c2-274">Token zabezpečení platformy se používá k volání doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="2c8c2-275">Proto musíte *token Azure Active Directory (Azure AD)* vygenerovat pomocí vaší aplikace Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="2c8c2-276">Poté musíte token Azure AD použít k získání *přístupového tokenu* od služby zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="2c8c2-277">Token služby zabezpečení získáte takto:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="2c8c2-278">Přihlaste se na portál Azure a použijte jej k vyhledání údajů `clientId` a `clientSecret` pro vaši aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="2c8c2-279">Načtěte token Azure Active Directory (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="2c8c2-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="2c8c2-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="2c8c2-281">**Metoda** - `GET`</span><span class="sxs-lookup"><span data-stu-id="2c8c2-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="2c8c2-282">**Obsah těla (údaje formuláře)**:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="2c8c2-283">klíč</span><span class="sxs-lookup"><span data-stu-id="2c8c2-283">key</span></span> | <span data-ttu-id="2c8c2-284">hodnota</span><span class="sxs-lookup"><span data-stu-id="2c8c2-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="2c8c2-285">id klienta</span><span class="sxs-lookup"><span data-stu-id="2c8c2-285">client_id</span></span> | <span data-ttu-id="2c8c2-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="2c8c2-286">${aadAppId}</span></span> |
        | <span data-ttu-id="2c8c2-287">tajný klíč klienta</span><span class="sxs-lookup"><span data-stu-id="2c8c2-287">client_secret</span></span> | <span data-ttu-id="2c8c2-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="2c8c2-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="2c8c2-289">typ grantu</span><span class="sxs-lookup"><span data-stu-id="2c8c2-289">grant_type</span></span> | <span data-ttu-id="2c8c2-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="2c8c2-290">client_credentials</span></span> |
        | <span data-ttu-id="2c8c2-291">prostředek</span><span class="sxs-lookup"><span data-stu-id="2c8c2-291">resource</span></span> | <span data-ttu-id="2c8c2-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="2c8c2-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="2c8c2-293">Měli byste obdržet `aadToken` v odpovědi, která se podobá následujícímu příkladu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="2c8c2-294">Formulujte požadavek JSON, který se podobá následujícímu:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-294">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="2c8c2-295">Kde:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-295">Where:</span></span>
    - <span data-ttu-id="2c8c2-296">Hodnota `client_assertion` musí být `aadToken`, který jste obdrželi v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="2c8c2-297">Hodnota `context` musí být ID prostředí, do kterého chcete doplněk nasadit.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="2c8c2-298">Nastavte všechny ostatní hodnoty, jak je znázorněno v příkladu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="2c8c2-299">Odešlete požadavek HTTP s následujícími vlastnostmi:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="2c8c2-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="2c8c2-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="2c8c2-301">**Metoda** - `POST`</span><span class="sxs-lookup"><span data-stu-id="2c8c2-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="2c8c2-302">**Záhlaví HTTP** - Zahrňte verzi API (klíč je `Api-Version` a hodnota je `1.0`)</span><span class="sxs-lookup"><span data-stu-id="2c8c2-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="2c8c2-303">**Obsah těla** - Zahrňte požadavek JSON, který jste vytvořili v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="2c8c2-304">V odpovědi získáte `access_token`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="2c8c2-305">To je to, co potřebujete jako nosný token pro volání rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="2c8c2-306">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="2c8c2-307">Ukázkový požadavek</span><span class="sxs-lookup"><span data-stu-id="2c8c2-307">Sample Request</span></span>

<span data-ttu-id="2c8c2-308">Pro vaši informaci je zde ukázka požadavku http, k odeslání tohoto požadavku můžete použít jakékoli nástroje nebo kódovací jazyk, například ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="2c8c2-309">Konfigurace rozhraní API doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="2c8c2-310">Před použitím služby musíte dokončit konfigurace popsané v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="2c8c2-311">Konfigurace se může lišit v závislosti na podrobnostech vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="2c8c2-312">Obsahuje primárně čtyři části:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="2c8c2-313">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="2c8c2-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="2c8c2-314">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="2c8c2-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="2c8c2-315">Indexace</span><span class="sxs-lookup"><span data-stu-id="2c8c2-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="2c8c2-316">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="2c8c2-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="2c8c2-317">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="2c8c2-317">Partitioning</span></span>

<span data-ttu-id="2c8c2-318">Rozdělení může významně ovlivnit výkonnost rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="2c8c2-319">Je vhodné definovat schéma, které umožňuje malá seskupení dat a přitom umožňuje smysluplné dotazy na data.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="2c8c2-320">`organizationId` (`dataAreaId` v Supply Chain Management) bude vždy součástí rozdělení a ve výchozím nastavení je Viditelnost zásob nastavena na rozdělení podle dimenzí jako *Pracoviště + skladové místo*.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="2c8c2-321">To znamená, že služba musí být vždy dotazována s těmito dimenzemi definovanými na filtrech.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="2c8c2-322">*Pracoviště* a *Skladové místo* jsou dvě obecné výchozí dimenze ve Viditelnosti zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="2c8c2-323">V aplikaci Supply Chain Management se tyto dimenze nazývají *Pracoviště* (`InventSiteId`) a *Sklad* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="2c8c2-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="2c8c2-324">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="2c8c2-324">Dimension configurations</span></span>

<span data-ttu-id="2c8c2-325">Viditelnost zásob poskytne seznam obecných výchozích dimenzí umožňujících integraci více zdrojových systémů.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="2c8c2-326">V následující tabulce jsou uvedeny dimenze zásob, které budou výchozími názvy dimenzí v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="2c8c2-327">Typ dimenze</span><span class="sxs-lookup"><span data-stu-id="2c8c2-327">Dimension type</span></span> | <span data-ttu-id="2c8c2-328">Název dimenze</span><span class="sxs-lookup"><span data-stu-id="2c8c2-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="2c8c2-329">Produkt</span><span class="sxs-lookup"><span data-stu-id="2c8c2-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="2c8c2-330">Produkt</span><span class="sxs-lookup"><span data-stu-id="2c8c2-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="2c8c2-331">Produkt</span><span class="sxs-lookup"><span data-stu-id="2c8c2-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="2c8c2-332">Produkt</span><span class="sxs-lookup"><span data-stu-id="2c8c2-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="2c8c2-333">Sledování</span><span class="sxs-lookup"><span data-stu-id="2c8c2-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="2c8c2-334">Sledování</span><span class="sxs-lookup"><span data-stu-id="2c8c2-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="2c8c2-335">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="2c8c2-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="2c8c2-336">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="2c8c2-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="2c8c2-337">Stav zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="2c8c2-338">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="2c8c2-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="2c8c2-339">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="2c8c2-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="2c8c2-340">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="2c8c2-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="2c8c2-341">Typ dimenze uvedený v předchozí tabulce slouží pouze pro informaci.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="2c8c2-342">V doplňku Viditelnost zásob není nutné definovat typ dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="2c8c2-343">Pokud vlastní dimenze existuje a je třeba ji přepnout na výchozí hodnotu, když je spotřebována doplňkem Viditelnost zásob, můžete nakonfigurovat název **Vlastní dimenze** v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="2c8c2-344">Externí systémy přistupují k doplňku Viditelnost zásob prostřednictvím rozhraní RESTful API, která umožňují dotazování na informace o dostupnosti na skladě u daných sad dimenzí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="2c8c2-345">Pro integraci vám doplněk Viditelnost zásob umožňuje konfigurovat *externí zdroj dat kanálu* a zdrojovou dimenzi do *cílových dimenzí* v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="2c8c2-346">Cílové dimenze by měly být jednou z následujících:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="2c8c2-347">Výchozí dimenze v doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="2c8c2-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="2c8c2-348">Vlastní dimenze</span><span class="sxs-lookup"><span data-stu-id="2c8c2-348">Custom dimensions</span></span>

<span data-ttu-id="2c8c2-349">Účelem konfigurace dimenze je standardizovat integraci více systémů pro dotazování na dimenzích a publikování události s dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="2c8c2-350">Indexace</span><span class="sxs-lookup"><span data-stu-id="2c8c2-350">Indexing</span></span>

<span data-ttu-id="2c8c2-351">Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni, ale možná budete chtít vidět výsledky agregované na základě dimenzí zásob.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="2c8c2-352">Viditelnost zásob poskytuje flexibilitu tím, že umožňuje nastavit indexy, které jsou založeny na dimenzi nebo kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="2c8c2-353">V současné době můžete indexy nakonfigurovat pouze na maximálně pět.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="2c8c2-354">Před implementací musíte pečlivě zvážit, kterou dimenzi nebo kombinaci dimenzí použijete, abyste zajistili, že bude vyhovovat vašim obchodním potřebám.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="2c8c2-355">Chcete-li se například dotazovat na produkty následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="2c8c2-356">Dotazujte se na agregované zásoby na skladě produktu podle dimenzí *Barva* a *Velikost*.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="2c8c2-357">V některých případech se chcete pouze dotazovat na produkt celkem.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="2c8c2-358">Měli byste dva indexy definované následovně:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="2c8c2-359">Prázdná závorka se agreguje na základě ID produktu v oddílu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="2c8c2-360">Indexování definuje, jak můžete seskupit výsledky na základě nastavení dotazu `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="2c8c2-361">V tomto případě, pokud nedefinujete žádné hodnoty `groupBy`, získáte součty `productid`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="2c8c2-362">Pokud definujete `groupBy` jako `groupBy=ColorId&groupBy=SizeId`, vrátí se vám více řádků na základě různých kombinací barev a velikostí v systému.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="2c8c2-363">Kritéria dotazu můžete zadat do textu požadavku.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="2c8c2-364">Zde je ukázkový dotaz na produkt s kombinací barev a velikostí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-364">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="2c8c2-365">Pro pole `filters` aktuálně pouze `ProductId` podporuje více hodnot.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="2c8c2-366">Pokud je `ProductId` prázdné pole, budou dotazovány všechny produkty.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="2c8c2-367">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="2c8c2-367">Custom measurement</span></span>

<span data-ttu-id="2c8c2-368">Výchozí množství měření jsou spojena se Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="2c8c2-369">Možná však budete chtít množství, které je tvořeno kombinací výchozích měření.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="2c8c2-370">Chcete-li to provést, můžete mít konfiguraci vlastních množství, která budou přidána k výstupu dotazů na zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="2c8c2-371">Funkce jednoduše umožňuje definovat sadu měrných systémů, které budou přidány, anebo sadu měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="2c8c2-372">Například s následující podmínkou dotazu nakonfigurujete vlastní množství měrné jednotky jako `MyCustomAvailableforReservation`, která má být spotřebována systémem spotřeby.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="2c8c2-373">Systém spotřeby</span><span class="sxs-lookup"><span data-stu-id="2c8c2-373">Consumption system</span></span> | <span data-ttu-id="2c8c2-374">Vypočtené měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="2c8c2-374">Calculated measurers</span></span> | <span data-ttu-id="2c8c2-375">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="2c8c2-375">Data source</span></span> | <span data-ttu-id="2c8c2-376">Modifikátor</span><span class="sxs-lookup"><span data-stu-id="2c8c2-376">Modifier</span></span> | <span data-ttu-id="2c8c2-377">Typ výpočtu modifikátoru</span><span class="sxs-lookup"><span data-stu-id="2c8c2-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="2c8c2-378">Sčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="2c8c2-379">Sčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="2c8c2-380">Odčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="2c8c2-381">Sčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="2c8c2-382">Odčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="2c8c2-383">Sčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="2c8c2-384">Sčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="2c8c2-385">Odčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="2c8c2-386">Odčítání</span><span class="sxs-lookup"><span data-stu-id="2c8c2-386">Subtraction</span></span> |

<span data-ttu-id="2c8c2-387">Takto dotaz na vlastní množství měrnou jednotku vrátí následující výstup.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="2c8c2-388">Výstup `MyCustomAvailableforReservation` je založen na nastavení výpočtu ve vlastních měrných systémech jako:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="2c8c2-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="2c8c2-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="2c8c2-390">Publikování změn množství na skladě</span><span class="sxs-lookup"><span data-stu-id="2c8c2-390">Posting on-hand changes</span></span>

<span data-ttu-id="2c8c2-391">Přesná adresa URL, na kterou bude událost publikována, bude záviset na vaší zeměpisné oblasti.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="2c8c2-392">Bude mít formu:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="2c8c2-393">Po ověření lze tuto adresu URL použít společně s metodou HTTP `POST` pro odesílání událostí změny zásob na skladě do služby.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="2c8c2-394">Pro komunikaci se službami Dynamics 365 prostřednictvím požadavků HTTP se používá speciální záhlaví, které označuje ID prostředí instance Supply Chain Management, ke které jsou data propojena.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="2c8c2-395">Například:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="2c8c2-396">Zveřejnění dotazu na změny zásob na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="2c8c2-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="2c8c2-397">Tento příklad ukazuje scénář, ve kterém nastavíte konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="2c8c2-398">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="2c8c2-399">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="2c8c2-400">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="2c8c2-401">Zveřejnění dotazu na změny zásob na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="2c8c2-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="2c8c2-402">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="2c8c2-403">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` hodnotu null, je prázdné nebo má mezeru.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="2c8c2-404">Vlastnosti pole dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="2c8c2-404">JSON document field properties</span></span>

<span data-ttu-id="2c8c2-405">Pole z dříve poskytnutých příkladů dotazů JSON mají vlastnosti uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="2c8c2-406">ID pole</span><span class="sxs-lookup"><span data-stu-id="2c8c2-406">Field ID</span></span> | <span data-ttu-id="2c8c2-407">popis</span><span class="sxs-lookup"><span data-stu-id="2c8c2-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="2c8c2-408">Jedinečné ID pro konkrétní událost změny.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="2c8c2-409">Toto ID se používá k zajištění toho, že pokud komunikace se službou během publikování selže, opětovné odeslání události nebude mít za následek, že se v systému dvakrát započítá stejná událost.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="2c8c2-410">Identifikátor organizace spojené s událostí.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="2c8c2-411">To se mapuje na organizace Supply Chain Management nebo ID datové oblasti.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="2c8c2-412">Identifikátor daného produktu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="2c8c2-413">Množství, o které je třeba změnit zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="2c8c2-414">Pokud by bylo například na polici přidáno 10 nových housek, byla by tato hodnota 10.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="2c8c2-415">Pokud by pak byly 3 housky odebrány z police nebo prodány, byla by tato hodnota -3.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="2c8c2-416">Zdroj dat dimenzí použitých v události změny publikování změny a dotazu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="2c8c2-417">Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="2c8c2-418">S konfigurací dimenzí může Viditelnost dat mapovat vlastní dimenze na obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="2c8c2-419">Pokud není zadán `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="2c8c2-420">Dynamická sada párů klíč/hodnota.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="2c8c2-421">Budou mapovány na některé dimenze v Supply Chain Management, ale můžete také přidat vlastní dimenze (jako *Zdroj*), což může naznačovat, že událost pocházela ze Supply Chain Managementu nebo externího systému.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="2c8c2-422">Dotaz na aktuální zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="2c8c2-422">Querying current on-hand</span></span>

<span data-ttu-id="2c8c2-423">Koncový bod pro dotazování na aktuální zásoby na skladě bude mít podobnou adresu URL:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="2c8c2-424">Bude dotazován pomocí metody HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="2c8c2-425">Dotaz na aktuální zásoby na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="2c8c2-425">Current on-hand query example 1</span></span>

<span data-ttu-id="2c8c2-426">Tento příklad ukazuje scénář, ve kterém jste dokončili konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="2c8c2-427">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="2c8c2-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="2c8c2-428">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="2c8c2-429">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="2c8c2-430">Můžete určit `DimensionDataSource` v `filters` a zadat vlastní dimenze v `filters` i `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="2c8c2-431">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="2c8c2-432">Dotaz na aktuální zásoby na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="2c8c2-432">Current on-hand query example 2</span></span>

<span data-ttu-id="2c8c2-433">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="2c8c2-434">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` pod `filters` hodnotu null nebo mezeru.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="2c8c2-435">Příklad výsledku vrácení</span><span class="sxs-lookup"><span data-stu-id="2c8c2-435">Example return result</span></span>

<span data-ttu-id="2c8c2-436">Dotazy zobrazené v předchozích příkladech by mohly vrátit takový výsledek.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-436">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="2c8c2-437">Všimněte si, že pole množství jsou strukturována jako slovník měrných jednotek a jejich přidružených hodnot.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
