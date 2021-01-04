---
title: Konfigurace finančních přehledů (Preview)
description: Toto téma vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664083"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="e7ab4-103">Konfigurace finančních přehledů (Preview)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e7ab4-104">Finanční přehledy kombinují funkčnost Microsoft Dynamics 365 Finance s Common Data Service, Azure a AI Builder, které vaší organizaci poskytnou výkonné nástroje pro prognózy.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Common Data Service, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="e7ab4-105">Toto téma vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="e7ab4-106">Nasazení Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="e7ab4-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="e7ab4-107">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="e7ab4-108">V Microsoft Dynamics Lifecycle Services (LCS) vytvořte nebo aktualizujte prostředí Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="e7ab4-109">Prostředí vyžaduje verzi aplikace 10.0.11 / Platform update 35 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="e7ab4-110">Prostředí musí mít vysokou dostupnost (HA) v prostředí Sandbox.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="e7ab4-111">(Tento typ prostředí se také nazývá prostředí 2. úrovně.) Další informace najdete v tématu [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="e7ab4-112">Pokud používáte ukázková data společnosti Contoso, budete potřebovat další ukázková data, abyste mohli používat funkce predikcí plateb zákazníka, prognózy cashflow a prognózy rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-common-data-service"></a><span data-ttu-id="e7ab4-113">Konfigurace služby Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e7ab4-113">Configure Common Data Service</span></span>

<span data-ttu-id="e7ab4-114">Můžete provést následující kroky ruční konfigurace nebo můžete zrychlit proces konfigurace pomocí skriptu Windows PowerShell, který je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="e7ab4-115">Po provedení skriptu PowerShell získáte hodnoty, které se mají použít ke konfiguraci finančních přehledů.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="e7ab4-116">V počítači otevřete PowerShell a spusťte skript.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="e7ab4-117">Možná budete potřebovat PowerShell verze 5.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="e7ab4-118">Možnost „Try it“ (vyzkoušet) Microsoft Azure CLI nemusí fungovat.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="e7ab4-119">Ruční kroky konfigurace</span><span class="sxs-lookup"><span data-stu-id="e7ab4-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="e7ab4-120">Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com/) a podle těchto kroků vytvořte nové prostředí Common Data Service ve stejném klientovi Active Directory:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Common Data Service environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="e7ab4-121">Otevřete stránku **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="e7ab4-122">[![Stránka Prostředí](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="e7ab4-123">Vyberte **Nové prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="e7ab4-124">V poli **Typ** vyberte **Sandbox**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="e7ab4-125">Nastavte možnost **Vytvořit databázi** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="e7ab4-126">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-126">Select **Next**.</span></span>
    6. <span data-ttu-id="e7ab4-127">Vyberte jazyk a měnu vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="e7ab4-128">Potvrďte výchozí hodnoty v ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="e7ab4-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-129">Select **Save**.</span></span>
    9. <span data-ttu-id="e7ab4-130">Aktualizujte stránku **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="e7ab4-131">Počkejte, až se hodnota pole **Stav** aktualizuje na **Připraveno**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="e7ab4-132">Poznamenejte si ID organizace Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-132">Make a note of the Common Data Service organization ID.</span></span>
    12. <span data-ttu-id="e7ab4-133">Vyberte prostředí , ke zkopírování a pak vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="e7ab4-134">Vyberte **Prostředky \> Všechna starší nastavení**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="e7ab4-135">Na horním navigačním panelu vyberte **Nastavení** a potom vyberte **Vlastní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="e7ab4-136">Vyberte **Vývojářské prostředky**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="e7ab4-137">Nastavte pole **ID referenčních informací o instanci** na hodnotu ID organizace Common Data Service, kterou jste si dříve poznamenali.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-137">Set the **Instance Reference Information ID** field to the Common Data Service organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="e7ab4-138">V adresním řádku prohlížeče si poznamenejte URL pro organizaci Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-138">In the browser's address bar, make a note of the URL for the Common Data Service organization.</span></span> <span data-ttu-id="e7ab4-139">Adresa URL může být například `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="e7ab4-140">Pokud plánujete použít funkci prognóz cashflow nebo rozpočtu, postupujte podle těchto kroků a aktualizujte limit anotací pro vaši organizaci na nejméně 50 megabajtů (MB):</span><span class="sxs-lookup"><span data-stu-id="e7ab4-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="e7ab4-141">Otevřete [Power Apps Portal](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="e7ab4-142">Vyberte prostředí, které jste právě vytvořili, a poté vyberte **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="e7ab4-143">Vyberte **Nastavení \> Konfigurace e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="e7ab4-144">Změňte hodnotu pole **Maximální velikost souboru** na **51200**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="e7ab4-145">(Hodnota je vyjádřena v kilobytech \[kB\].)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="e7ab4-146">Vyberte **OK** a uložte změny.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="e7ab4-147">Konfigurační skript prostředí Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7ab4-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="e7ab4-148">Konfigurace nastavení Azure</span><span class="sxs-lookup"><span data-stu-id="e7ab4-148">Configure the Azure setup</span></span>

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="e7ab4-149">Zadejte ID adresáře Common Data Service a ID objektu Azure AD uživatele</span><span class="sxs-lookup"><span data-stu-id="e7ab4-149">Enter the Common Data Service directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="e7ab4-150">Zadejte ID adresáře Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-150">Enter the Common Data Service directory ID:</span></span>

    1. <span data-ttu-id="e7ab4-151">Otevřete [portál Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="e7ab4-152">Přihlaste se pomocí ID uživatele, které bylo použito k vytvoření prostředí Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-152">Sign in by using the user ID that was used to create the Common Data Service environment.</span></span>
    3. <span data-ttu-id="e7ab4-153">Přejděte na **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="e7ab4-154">Zkopírujte hodnotu **ID klienta**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="e7ab4-155">Zadejte ID objektu uživatele Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="e7ab4-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="e7ab4-156">V [portálu Azure](https://portal.azure.com) přejděte na **Uživatelé** a vyhledejte uživatele podle e-mailové adresy.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="e7ab4-157">Vyberte jméno uživatele.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-157">Select the user's name.</span></span>
    3. <span data-ttu-id="e7ab4-158">Zkopírujte hodnotu **ID objektu**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="e7ab4-159">Použití Azure Cloud Shell k nastavení prostředků Data Lake finančních přehledů</span><span class="sxs-lookup"><span data-stu-id="e7ab4-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="e7ab4-160">Použití skriptu prostředí Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7ab4-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="e7ab4-161">Byl poskytnut skript prostředí Windows PowerShell, takže můžete snadno nastavit prostředky Azure, které jsou popsány v části [Konfigurace exportu do Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="e7ab4-162">Pokud dáváte přednost ručnímu nastavení, tento postup přeskočte a pokračujte postupem v sekci [Ruční nastavení](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="e7ab4-163">Podle následujících pokynů spusťte skript prostředí PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="e7ab4-164">Možnost „Try it“ (vyzkoušet) Azure CLI nebo spuštění skriptu na vašem počítači nemusí fungovat.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="e7ab4-165">Podle těchto pokynů nakonfigurujte Azure pomocí skriptu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="e7ab4-166">Musíte mít práva k vytvoření skupiny prostředků Azure, prostředků Azure a aplikace Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="e7ab4-167">Informace o požadovaných oprávněních najdete v části [Kontrola oprávnění Azure AD](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="e7ab4-168">V [portálu Azure](https://portal.azure.com) přejděte na své cílové předplatné Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="e7ab4-169">Vyberte tlačítko **Cloud Shell** napravo od pole **Vyhledávání**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="e7ab4-170">Vyberte **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="e7ab4-171">Pokud se zobrazí výzva, vytvořte úložiště.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="e7ab4-172">Potom nahrajte skript prostředí Windows PowerShell do relace.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="e7ab4-173">Spusťte skript.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-173">Run the script.</span></span>
5. <span data-ttu-id="e7ab4-174">Podle pokynů spusťte skript.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="e7ab4-175">Použijte informace z výstupu skriptu k instalaci doplňku **Export do Data Lake** v LCS.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="e7ab4-176">Pomocí informací z výstupu skriptu povolte úložiště entit na stránce **Datová připojení** ve Finance (**Správa systému \> Parametry systému \> Datová připojení**).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="e7ab4-177">Ruční nastavení</span><span class="sxs-lookup"><span data-stu-id="e7ab4-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="e7ab4-178">Přidání aplikací do klienta Azure AD</span><span class="sxs-lookup"><span data-stu-id="e7ab4-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="e7ab4-179">V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="e7ab4-180">Vyberte **Správa \> Podnikové aplikace**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="e7ab4-181">Vyhledejte následující aplikace podle ID aplikace.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="e7ab4-182">Přihláška</span><span class="sxs-lookup"><span data-stu-id="e7ab4-182">Application</span></span>                              | <span data-ttu-id="e7ab4-183">ID aplikace</span><span class="sxs-lookup"><span data-stu-id="e7ab4-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="e7ab4-184">Mikroslužby Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="e7ab4-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="e7ab4-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="e7ab4-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="e7ab4-186">Mikroslužby CDS Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="e7ab4-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="e7ab4-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="e7ab4-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="e7ab4-188">Autorizační služba AI Builder</span><span class="sxs-lookup"><span data-stu-id="e7ab4-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="e7ab4-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="e7ab4-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="e7ab4-190">Pokud nemůžete najít žádnou z předchozích aplikací, vyzkoušejte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="e7ab4-191">Na místním počítači vyberte nabídku **Start** a hledejte **powershell**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="e7ab4-192">Vyberte a podržte (nebo klikněte pravým tlačítkem na) **Windows PowerShell** a potom vyberte **Spustit jako správce**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="e7ab4-193">Spusťte následující příkaz k instalaci modulu **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="e7ab4-194">Pokud je pro pokračování potřeba poskytovatel NuGet, k jeho instalaci vyberte **A**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="e7ab4-195">Pokud se zobrazí zpráva „Nedůvěryhodné úložiště“, pro pokračování vyberte **A**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="e7ab4-196">Pro každou aplikaci, kterou je třeba přidat, spusťte následující příkazy, abyste ji přidali do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="e7ab4-197">Po zobrazení výzvy se přihlaste jako správce Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="e7ab4-198">Vytvoření zdrojů Azure</span><span class="sxs-lookup"><span data-stu-id="e7ab4-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="e7ab4-199">Nezapomeňte vytvořit následující prostředky ve stejné instanci Azure AD jako prostředí Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-199">Make sure that you create the following resources in the same Azure AD instance as the Common Data Service environment.</span></span> <span data-ttu-id="e7ab4-200">Nelze použít prostředky z jiné instance Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="e7ab4-201">Vytvoření nového účtu úložiště:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="e7ab4-202">V [portálu Azure](https://portal.azure.com) vytvořte účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="e7ab4-203">V dialogovém okně **Vytvoření účtu úložiště** nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="e7ab4-204">**Umístění** – Vyberte datové centrum, kde se nachází vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="e7ab4-205">**Výkon** – Doporučujeme, abyste vybrali **Standard**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="e7ab4-206">**Druh účtu** – Musíte vybrat **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="e7ab4-207">V dialogovém okně **Rozšířené možnosti** pro **Data Lake Storage Gen2** vyberte možnost **Povolit** pro funkci **Hierarchický obor názvů**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="e7ab4-208">Pokud tuto funkci deaktivujete, nebudete moci spotřebovat data, která aplikace Finance and Operations zapíše při použití služeb, jako jsou toky dat Power BI.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="e7ab4-209">Vyberte **Zkontrolovat a vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-209">Select **Review and create**.</span></span> <span data-ttu-id="e7ab4-210">Po dokončení nasazení se nový prostředek zobrazí v portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="e7ab4-211">Přejděte na účet úložiště, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="e7ab4-212">V levé nabídce vyberte možnost **Přístupové klíče**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="e7ab4-213">Zkopírujte a uložte připojovací řetězec buď **Klíč1** nebo **Klíč2**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="e7ab4-214">Zkopírujte a uložte název účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="e7ab4-215">Vytvoření nového trezoru klíčů:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="e7ab4-216">V [portálu Azure](https://portal.azure.com) vytvořte trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="e7ab4-217">V dialogovém okně **Vytvoření trezoru klíčů** v poli **Umístění** vyberte datové centrum, kde se nachází vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="e7ab4-218">Po vytvoření trezoru klíčů jej vyberte v seznamu a poté vyberte **Tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="e7ab4-219">Vyberte **Generovat/import**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="e7ab4-220">V dialogovém okně **Vytvoření tajného klíče** v poli **Možnosti odesílání** vyberte **Ručně**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="e7ab4-221">Zadejte název tajného klíče.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-221">Enter a name for the secret.</span></span> <span data-ttu-id="e7ab4-222">Poznamenejte si tento název, protože jej budete muset zadat později.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="e7ab4-223">V poli **Hodnota** zadejte připojovací řetězec, který jste získali z účtu úložiště v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="e7ab4-224">Vyberte **Povolit** a potom vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="e7ab4-225">Tajný klíč je vytvořen a přidán do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="e7ab4-226">Přejděte na **Přehled Key Vault** a poznamenejte si název DNS.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="e7ab4-227">Vytvoření a zaregistrování aplikace Azure AD:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="e7ab4-228">V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory** a poté vyberte možnost **Registrace aplikací**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="e7ab4-229">Vyberte **Registrace nové aplikace** a nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="e7ab4-230">**Název** – Zadejte název aplikace.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="e7ab4-231">**Typ aplikace** – Vyberte **Webové rozhraní API**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="e7ab4-232">**Nastavení URI přesměrování** – Zadejte adresu URL instance Dynamics 365, například `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="e7ab4-233">Přejděte do aplikace, kterou jste právě vytvořili, a zkopírujte ji a uložte její hodnotu **ID aplikace (klienta)**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="e7ab4-234">Tuto hodnotu budete muset zadat později, až nastavíte trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="e7ab4-235">Přejděte na **Oprávnění API** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="e7ab4-236">Vyberte **Přidat oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="e7ab4-237">Vyberte **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="e7ab4-238">Po výběru delegovaných oprávnění vyberte **uživatel\_zosobnění**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="e7ab4-239">Vyberte **Přidat oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="e7ab4-240">V nabídce aplikace vyberte **Certifikáty \& tajné klíče** a poté podle těchto kroků vytvořte tajné klíče Key Vault:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="e7ab4-241">Vyberte **Nový tajný klíč klienta**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="e7ab4-242">V poli **Popis klíče** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="e7ab4-243">Vyberte dobu trvání a potom vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="e7ab4-244">V poli **Hodnota** se vygeneruje tajný klíč.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="e7ab4-245">Zkopírujte a uložte hodnotu tajného klíče.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="e7ab4-246">Vytvoření tajných klíčů Key Vault:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="e7ab4-247">Přejděte do trezoru klíčů, který jste vytvořili dříve, a vyberte **Tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="e7ab4-248">Pro každý název tajného klíče v následující tabulce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="e7ab4-249">Vyberte **Generovat/import**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="e7ab4-250">V dialogovém okně **Vytvoření tajného klíče** v poli **Možnosti odesílání** vyberte **Ručně**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="e7ab4-251">Vytvořte název tajného klíče a hodnotu z následující tabulky.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="e7ab4-252">Vyberte **Povolit** a potom vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="e7ab4-253">Tajný klíč je vytvořen a přidán do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="e7ab4-254">Název tajného klíče</span><span class="sxs-lookup"><span data-stu-id="e7ab4-254">Secret name</span></span>                       | <span data-ttu-id="e7ab4-255">Hodnota tajného klíče</span><span class="sxs-lookup"><span data-stu-id="e7ab4-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="e7ab4-256">app-id</span><span class="sxs-lookup"><span data-stu-id="e7ab4-256">app-id</span></span>                            | <span data-ttu-id="e7ab4-257">ID aplikace, kterou jste vytvořili dříve</span><span class="sxs-lookup"><span data-stu-id="e7ab4-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="e7ab4-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="e7ab4-258">app-secret</span></span>                        | <span data-ttu-id="e7ab4-259">Tajný klíč klienta, které jste uložili dříve</span><span class="sxs-lookup"><span data-stu-id="e7ab4-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="e7ab4-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="e7ab4-260">storage-account-name</span></span>              | <span data-ttu-id="e7ab4-261">Název účtu úložiště, který jste vytvořili dříve, například **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="e7ab4-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="e7ab4-262">storage-account-connection-string</span></span> | <span data-ttu-id="e7ab4-263">Připojovací řetězec, který jste zkopírovali ze stránky **Přístupové klíče** pro účet úložiště</span><span class="sxs-lookup"><span data-stu-id="e7ab4-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="e7ab4-264">Autorizujte aplikaci pro přístup do trezoru klíčů:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="e7ab4-265">V [portálu Azure](https://portal.azure.com) otevřete trezor klíčů, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="e7ab4-266">Vyberte zásady přístupu.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-266">Select the access policies.</span></span>
    3. <span data-ttu-id="e7ab4-267">Pro každou aplikaci v následující tabulce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="e7ab4-268">Volbou **Přidat zásady přístupu** vytvořte zásady přístupu.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="e7ab4-269">V poli **Oprávnění na základě tajných klíčů** vyberte oprávnění z následující tabulky.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="e7ab4-270">V poli **Výběr objektu zabezpečení** vyhledejte zobrazovaný název aplikace v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="e7ab4-271">Zvolte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-271">Select **Select**.</span></span>
        5. <span data-ttu-id="e7ab4-272">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-272">Select **Add**.</span></span>
        6. <span data-ttu-id="e7ab4-273">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-273">Select **Save**.</span></span>

        | <span data-ttu-id="e7ab4-274">Přihláška</span><span class="sxs-lookup"><span data-stu-id="e7ab4-274">Application</span></span>                                              | <span data-ttu-id="e7ab4-275">Oprávnění</span><span class="sxs-lookup"><span data-stu-id="e7ab4-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="e7ab4-276">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="e7ab4-276">The display name of the new application that you created</span></span> | <span data-ttu-id="e7ab4-277">Get, List</span><span class="sxs-lookup"><span data-stu-id="e7ab4-277">Get, List</span></span>   |
        | <span data-ttu-id="e7ab4-278">**Mikroslužby Microsoft Dynamics ERP**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="e7ab4-279">Get, List</span><span class="sxs-lookup"><span data-stu-id="e7ab4-279">Get, List</span></span>   |

6. <span data-ttu-id="e7ab4-280">Přiřazení rolí pro přístup k účtu úložiště:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="e7ab4-281">V [portálu Azure](https://portal.azure.com) otevřete účet úložiště, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="e7ab4-282">Vyberte **Řízení přístupu (IAM)** a potom vyberte **Přiřazení rolí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="e7ab4-283">Vybere **Přidat, Přidat přiřazení rolí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="e7ab4-284">Pro každou aplikaci v následující tabulce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="e7ab4-285">Vyberte roli z následující tabulky.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="e7ab4-286">Ponechte pole **Přiřadit přístup k** nastaveno na **Uživatel, skupina nebo objekt zabezpečení Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="e7ab4-287">V poli **Vybrat** zadejte aplikaci z následující tabulky.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="e7ab4-288">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-288">Select **Save**.</span></span>

        | <span data-ttu-id="e7ab4-289">Přihláška</span><span class="sxs-lookup"><span data-stu-id="e7ab4-289">Application</span></span>                                              | <span data-ttu-id="e7ab4-290">Role</span><span class="sxs-lookup"><span data-stu-id="e7ab4-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="e7ab4-291">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="e7ab4-291">The display name of the new application that you created</span></span> | <span data-ttu-id="e7ab4-292">Vlastník</span><span class="sxs-lookup"><span data-stu-id="e7ab4-292">Owner</span></span>                       |
        | <span data-ttu-id="e7ab4-293">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="e7ab4-293">The display name of the new application that you created</span></span> | <span data-ttu-id="e7ab4-294">Přispěvatel</span><span class="sxs-lookup"><span data-stu-id="e7ab4-294">Contributor</span></span>                 |
        | <span data-ttu-id="e7ab4-295">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="e7ab4-295">The display name of the new application that you created</span></span> | <span data-ttu-id="e7ab4-296">Přispěvatel účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="e7ab4-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="e7ab4-297">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="e7ab4-297">The display name of the new application that you created</span></span> | <span data-ttu-id="e7ab4-298">Vlastník dat objektu blob úložiště</span><span class="sxs-lookup"><span data-stu-id="e7ab4-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="e7ab4-299">**Autorizační služba AI Builder**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="e7ab4-300">Čtenář dat objektu blob úložiště</span><span class="sxs-lookup"><span data-stu-id="e7ab4-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="e7ab4-301">Server Azure CLI</span><span class="sxs-lookup"><span data-stu-id="e7ab4-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message
  Write-Warning $_.Exception.StackTrace
  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}

```
---

## <a name="configure-the-entity-store"></a><span data-ttu-id="e7ab4-302">Konfigurace úložiště entit</span><span class="sxs-lookup"><span data-stu-id="e7ab4-302">Configure the entity store</span></span>

<span data-ttu-id="e7ab4-303">Pomocí těchto kroků nastavíte úložiště entit ve vašem prostředí Finance.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="e7ab4-304">Přejděte do nabídky **Správa systému \> Nastavení \> Systémové parametry \> Datová připojení**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="e7ab4-305">Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="e7ab4-306">Nastavte následující pole Key Vault:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="e7ab4-307">**ID aplikace (klienta)** – Zadejte ID klienta aplikace, které jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="e7ab4-308">**Tajný klíč aplikace** – Zadejte tajný klíč, které jste uložili pro aplikaci, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="e7ab4-309">**Název DNS** – Název systému DNS (Domain Name System) najdete na stránce s podrobnostmi o aplikaci, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="e7ab4-310">**Název tajného klíče** – Zadejte **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="e7ab4-311">Konfigurace datového jezera</span><span class="sxs-lookup"><span data-stu-id="e7ab4-311">Configure the data lake</span></span>

<span data-ttu-id="e7ab4-312">Podle těchto pokynů použijte LCS k přidání doplňku Azure Data Lake do prostředí.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="e7ab4-313">Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="e7ab4-314">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="e7ab4-315">Vyberte doplněk **Export do Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="e7ab4-316">Zadejte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-316">Enter the following values.</span></span>

    | <span data-ttu-id="e7ab4-317">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e7ab4-317">Value</span></span>                                                              | <span data-ttu-id="e7ab4-318">popis</span><span class="sxs-lookup"><span data-stu-id="e7ab4-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="e7ab4-319">ID klienta předplatného Azure, kde se nachází Key Vault</span><span class="sxs-lookup"><span data-stu-id="e7ab4-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="e7ab4-320">ID klienta, kde se nachází účet úložiště, aplikace a trezory klíčů.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="e7ab4-321">Tuto hodnotu najdete otevřením [portálu Azure](https://portal.azure.com), přejděte na **Azure Active Directory** a zkopírujte hodnotu **ID klienta**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="e7ab4-322">Zadejte název DNS vašeho řešení Key Vault</span><span class="sxs-lookup"><span data-stu-id="e7ab4-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="e7ab4-323">Název DNS trezoru klíčů, například `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="e7ab4-324">(Tato hodnota odpovídá názvu DNS, který se používá v úložišti entit.)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="e7ab4-325">Zadejte tajný klíč, který obsahuje název účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="e7ab4-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="e7ab4-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="e7ab4-327">Název tajného klíče pro ID aplikace, který se má použít pro přístup k Data Lake</span><span class="sxs-lookup"><span data-stu-id="e7ab4-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="e7ab4-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-328">**app-id**</span></span> |
    | <span data-ttu-id="e7ab4-329">Název tajného klíče, který se má použít s ID aplikace</span><span class="sxs-lookup"><span data-stu-id="e7ab4-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="e7ab4-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-330">**app-secret**</span></span> |

5. <span data-ttu-id="e7ab4-331">Odsouhlaste podmínky a vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="e7ab4-332">Doplněk bude nainstalován během několika minut.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="e7ab4-333">Konfigurace nástroje AI Builder</span><span class="sxs-lookup"><span data-stu-id="e7ab4-333">Configure AI Builder</span></span>

1. <span data-ttu-id="e7ab4-334">Přihlaste se k LCS a otevřete stránku **Podrobnosti prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="e7ab4-335">Přejděte do části **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="e7ab4-336">Měli byste vidět doplňky, které jsou již v tomto prostředí nainstalovány.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="e7ab4-337">Pokud doplněk **Export do Data Lake** mezi nimi není, nakonfigurujte tento doplněk.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="e7ab4-338">Vyberte doplněk **Získání přehledů**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="e7ab4-339">Na stránce podrobností doplňku **Získání přehledů** zadejte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="e7ab4-340">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e7ab4-340">Value</span></span>                                                    | <span data-ttu-id="e7ab4-341">popis</span><span class="sxs-lookup"><span data-stu-id="e7ab4-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="e7ab4-342">Adresa URL organizace CDS</span><span class="sxs-lookup"><span data-stu-id="e7ab4-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="e7ab4-343">Adrsa URL organizace Common Data Service instance Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-343">The Common Data Service organization URL of the Common Data Service instance.</span></span> <span data-ttu-id="e7ab4-344">Tuto hodnotu najdete otevřením [portálu Power Apps](https://make.powerapps.com), výběrem tlačítka **Nastavení** (symbol ozubeného kola) v pravém horním rohu, výběrem možnosti **Pokročilá nastavení** a zkopírováním adresy URL.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="e7ab4-345">(Adresa URL končí řetězcem „dynamics.com“.)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="e7ab4-346">ID org. CDS</span><span class="sxs-lookup"><span data-stu-id="e7ab4-346">CDS Org ID</span></span>                                               | <span data-ttu-id="e7ab4-347">ID prostředí instance Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-347">The environment ID of the Common Data Service instance.</span></span> <span data-ttu-id="e7ab4-348">Tuto hodnotu najdete otevřením [portálu Power Apps](https://make.powerapps.com), výběrem tlačítka **Nastavení** (symbol ozubeného kola) v pravém horním rohu, výběrem možnosti **Vlastní nastavení \> Vývojářské prostředky \> Referenční informace o instanci** a zkopírováním hodnoty **ID**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="e7ab4-349">ID klienta CDS (ID adresáře z AAD)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="e7ab4-350">ID klienta instance Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-350">The tenant ID of the Common Data Service instance.</span></span> <span data-ttu-id="e7ab4-351">Tuto hodnotu najdete otevřením [portálu Azure](https://portal.azure.com), přejděte na **Azure Active Directory** a zkopírujte hodnotu **ID klienta**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="e7ab4-352">Zadejte ID objektu uživatele, který má roli správce systému</span><span class="sxs-lookup"><span data-stu-id="e7ab4-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="e7ab4-353">ID objektu uživatele Azure AD v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-353">The Azure AD user object ID of the user in Common Data Service.</span></span> <span data-ttu-id="e7ab4-354">Tento uživatel musí být správcem systému instance Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-354">This user must be a system administrator of the Common Data Service instance.</span></span> <span data-ttu-id="e7ab4-355">Tuto hodnotu najdete otevřením [portálu Azure](https://portal.azure.com), otevřením nabídky **Azure Active Directory \> Uživatelé**, výběrem uživatele a poté v sekci **Identita** zkopírováním hodnoty **ID objektu**.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="e7ab4-356">Je toto výchozí prostředí CDS pro klienta?</span><span class="sxs-lookup"><span data-stu-id="e7ab4-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="e7ab4-357">Pokud instance Common Data Service byla první produkční instance, která byla vytvořena, zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-357">If the Common Data Service instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="e7ab4-358">Pokud instance Common Data Service byla vytvořena ručně, zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-358">If the Common Data Service instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="e7ab4-359">Názory a podpora</span><span class="sxs-lookup"><span data-stu-id="e7ab4-359">Feedback and support</span></span>

<span data-ttu-id="e7ab4-360">Zašlete prosím e-mail na [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com), pokud máte zájem o poskytnutí názoru nebo potřebujete podporu.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e7ab4-361">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="e7ab4-361">Privacy notice</span></span>

<span data-ttu-id="e7ab4-362">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
