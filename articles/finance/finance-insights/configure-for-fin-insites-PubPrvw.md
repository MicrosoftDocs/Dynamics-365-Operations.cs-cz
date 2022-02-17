---
title: Konfigurace Finance Insights – verze 10.0.20 a pozdější
description: Toto téma vysvětluje, jak nakonfigurovat svůj systém, aby používal funkce, které jsou k dispozici ve Finance Insights pro verze 10.0.20 a pozdější.
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: cea6258d3a99ba33e73acd2508ec7b6c11d15859
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061747"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>Konfigurace Finance Insights – verze 10.0.20 a pozdější

[!include [banner](../includes/banner.md)]



Finance Insights kombinují funkčnost Microsoft Dynamics 365 Finance s Dataverse, Azure a AI Builder, které vaší organizaci poskytnou výkonné nástroje pro prognózy. Toto téma vysvětluje, jak nakonfigurovat Dynamics 365 Finance verze 10.0.20, aby váš systém dokázal používat funkce, které jsou k dispozici ve Finance Insights.

> [!NOTE]
> Kroky konfigurace, které jsou popsány v tomto tématu, se vztahují pouze na verzi Finance 10.0.20 a novější. Informace o nastavení Finance Insights ve verzi 10.0.19 a starší najdete v tématu [Konfigurace Finance Insights - do verze 10.0.19](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Nasazení Finance

Pro nasazení prostředí postupujte takto.

1. V Microsoft Dynamics Lifecycle Services (LCS) vytvořte nebo aktualizujte prostředí Finance. Prostředí vyžaduje finanční a provozní aplikaci verze 10.0.20 nebo novější.
2. Prostředí musí mít vysokou dostupnost (HA) v prostředí Sandbox. (Tento typ prostředí se také nazývá prostředí 2. úrovně.) Další informace najdete v tématu [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Pokud konfigurujete Finance Insights v prostředí Sandbox, možná budete muset zkopírovat produkční data do tohoto prostředí, aby předpovědi fungovaly. Predikční model využívá k sestavování předpovědí několik let dat. Ukázková data Contoso neobsahují dostatek historických dat pro adekvátní trénink modelu predikce. 

## <a name="configure-dataverse"></a>Konfigurace služby Dataverse

Ke konfiguraci Dataverse pro Finance Insights proveďte následující kroky.

1. Otevřete stránku prostředí v LCS a ověřte, že část **Integrace Power Platform** je již nastavena.

    - Pokud je již nastavena, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.
    - Pokud ještě není nastavena, postupujte takto:

        1. V části **Integrace Power Platform** vyberte **Nastavení**. Nastavení prostředí může trvat až hodinu.
        2. Pokud je prostředí Dataverse úspěšně nastaveno, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.

        > [!NOTE]
        > Po dokončení nastavení prostředí **nevybírejte** **Odkaz na CDS for Apps**. Toto tlačítko není nutné pro Finance Insights. Pokud jej vyberete, nebudete moci nakonfigurovat požadované doplňky prostředí v LCS.

## <a name="configure-azure"></a>Nakonfigurujte Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Použití Azure Cloud Shell k nastavení prostředků Data Lake finančních přehledů

# <a name="use-a-windows-powershell-script"></a>[Použití skriptu prostředí Windows PowerShell](#tab/use-a-powershell-script)

Byl poskytnut skript prostředí Windows PowerShell, takže můžete snadno nastavit prostředky Azure, které jsou popsány v části [Konfigurace exportu do Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Pokud dáváte přednost ručnímu nastavení, tento postup přeskočte a dokončete postup v sekci [Ruční nastavení](#manual-setup).

> [!NOTE]
> Pomocí následujícího postupu spustíte skript prostředí Windows PowerShell. Nastavení nemusí fungovat, pokud používáte možnost **Vyzkoušet** v Azure CLI nebo pokud spustíte skript v počítači.

Podle těchto pokynů nakonfigurujte Azure pomocí skriptu Windows PowerShell. Musíte mít práva k vytvoření skupiny prostředků Azure, prostředků Azure a aplikace Azure AD. Informace o požadovaných oprávněních najdete v části [Kontrola oprávnění Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. V [portálu Azure](https://portal.azure.com) přejděte na své cílové předplatné Azure.
2. Vyberte **Cloud Shell** napravo od pole **Vyhledávání**.
3. Vyberte **PowerShell**.
4. Pokud se zobrazí výzva, vytvořte úložiště.
5. Na kartě **Azure CLI** vyberte **Kopírovat**.
6. V poznámkovém bloku otevřete nový soubor a vložte jej do skriptu Windows PowerShell.
7. Uložte soubor jako **ConfigureDataLake.ps1**.
8. Nahrajte skript Windows PowerShell do relace pomocí možnosti nabídky pro nahrání v Cloud Shell.
9. Spusťte skript **.\ConfigureDataLake.ps1**.
10. Podle pokynů spusťte skript.
11. Použijte informace z výstupu skriptu k instalaci doplňku Export do Data Lake v LCS.

### <a name="manual-setup"></a>Ruční nastavení

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Přidání aplikací do klienta Azure AD

1. V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory**.
2. Vyberte **Správa \> Podnikové aplikace**.
3. Vyhledejte následující aplikace podle ID aplikace.

    | Přihláška                              | ID aplikace                               |
    |------------------------------------------|--------------------------------------|
    | Mikroslužby Microsoft Dynamics ERP     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Mikroslužby CDS Microsoft Dynamics ERP | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | Autorizační služba AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Pokud nemůžete najít žádnou z předchozích aplikací, vyzkoušejte následující kroky.

1. Na místním počítači vyberte nabídku **Start** a hledejte **powershell**.
2. Vyberte a podržte (nebo klikněte pravým tlačítkem na) **Windows PowerShell** a potom vyberte **Spustit jako správce**.
3. Spusťte následující příkaz k instalaci modulu **AzureAD**.

    `Install-Module -Name AzureAD`

4. Pokud je pro pokračování potřeba poskytovatel NuGet, k jeho instalaci vyberte **Y**.
5. Pokud obdržíte zprávu „Nedůvěryhodné úložiště“, pro pokračování vyberte **Y**.
6. Pro každou aplikaci, kterou je třeba přidat, spusťte následující příkazy, abyste ji přidali do Azure AD. Po zobrazení výzvy se přihlaste jako správce Azure AD.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Vytvoření zdrojů Azure

> [!NOTE]
> Nezapomeňte vytvořit následující prostředky ve stejné instanci Azure AD, ve kterém je prostředí Dataverse. Nelze použít prostředky z jiné instance Azure AD.

1. Vytvoření účtu úložiště:

    1. V [portálu Azure](https://portal.azure.com) vytvořte účet úložiště.
    2. V dialogovém okně **Vytvoření účtu úložiště** nastavte následující pole:

        - **Umístění** – Vyberte datové centrum, kde se nachází vaše prostředí.
        - **Výkon** – Doporučujeme, abyste vybrali **Standard**.
        - **Druh účtu** – Musíte vybrat **StorageV2**.

    3. V dialogovém okně **Rozšířené možnosti** pro **Data Lake Storage Gen2** vyberte možnost **Povolit** pro funkci **Hierarchický obor názvů**. Pokud tuto funkci nepovolíte, nebudete moci spotřebovat data, která finanční a provozní aplikace zapíše při použití služeb, jako jsou toky dat Power BI.
    4. Vyberte **Zkontrolovat a vytvořit**. Po dokončení nasazení se nový prostředek zobrazí v portálu Azure.
    5. Přejděte na účet úložiště, který jste vytvořili.
    6. V levé nabídce vyberte možnost **Přístupové klíče**.
    7. Zkopírujte a uložte název účtu úložiště. Tuto hodnotu budete muset zadat později, až nastavíte tajné kódy trezoru klíčů.

2. Vytvoření trezoru klíčů:

    1. V [portálu Azure](https://portal.azure.com) vytvořte trezor klíčů.
    2. V dialogovém okně **Vytvoření trezoru klíčů** v poli **Umístění** vyberte datové centrum, kde se nachází vaše prostředí.
    3. Po vytvoření trezoru klíčů přejděte na **Přehled trezoru klíčů** a zkopírujte a uložte název DNS. Tuto hodnotu budete muset zadat později, až nastavíte doplněk Data Lake.

3. Vytvoření a zaregistrování aplikace Azure AD:

    1. V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory** a poté vyberte možnost **Registrace aplikací**.
    2. Vyberte **Registrace nové aplikace** a nastavte následující pole:

        - **Název** – Zadejte název aplikace.
        - **Typ aplikace** – Vyberte **Webové rozhraní API**.
        - **Nastavení URI přesměrování** – Zadejte adresu URL instance Dynamics 365, například `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Přejděte do aplikace, kterou jste právě vytvořili, a zkopírujte ji a uložte její hodnotu **ID aplikace (klienta)**. Tuto hodnotu budete muset zadat později, až nastavíte tajné kódy trezoru klíčů.
    4. Přejděte na **Oprávnění API** a postupujte takto:

        1. Vyberte **Přidat oprávnění**.
        2. Vyberte **Azure Key Vault**.
        3. Po výběru delegovaných oprávnění vyberte **uživatel\_zosobnění**.
        4. Vyberte **Přidat oprávnění**.

    5. V nabídce aplikace vyberte **Certifikáty \& tajné klíče** a poté podle těchto kroků vytvořte tajné klíče Key Vault:

        1. Vyberte **Nový tajný klíč klienta**.
        2. V poli **Popis klíče** zadejte název.
        3. Vyberte dobu trvání a potom vyberte **Přidat**. V poli **Hodnota** se vygeneruje tajný klíč.
        4. Zkopírujte a uložte hodnotu tajného klíče klienta. Tuto hodnotu budete muset zadat později, až nastavíte tajné kódy trezoru klíčů.

4. Vytvoření tajných klíčů Key Vault:

    1. Přejděte do trezoru klíčů, který jste vytvořili dříve, a vyberte **Tajné klíče**.
    2. Pro každý název tajného klíče v následující tabulce postupujte takto:

        1. Vyberte **Generovat/import**.
        2. V dialogovém okně **Vytvoření tajného klíče** v poli **Možnosti odesílání** vyberte **Ručně**.
        3. Vytvořte název tajného klíče a hodnotu z tabulky.
        4. Vyberte **Povolit** a potom vyberte **Vytvořit**. Tajný klíč je vytvořen a přidán do Key Vault.

        | Název tajného klíče                       | Hodnota tajného klíče                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | ID aplikace, kterou jste vytvořili dříve.                                      |
        | app-secret                        | Tajný klíč klienta, které jste uložili dříve.                                                    |
        | storage-account-name              | Název účtu úložiště, který jste vytvořili dříve, například **storageaccount1**.       |

5. Autorizujte aplikaci pro přístup do trezoru klíčů:

    1. V [portálu Azure](https://portal.azure.com) otevřete trezor klíčů, který jste vytvořili dříve.
    2. Vyberte zásady přístupu.
    3. Pro každou aplikaci v následující tabulce postupujte takto:

        1. Volbou **Přidat zásady přístupu** vytvořte zásady přístupu.
        2. V poli **Oprávnění na základě tajných klíčů** vyberte oprávnění z tabulky.
        3. V poli **Výběr objektu zabezpečení** vyhledejte zobrazovaný název aplikace v tabulce.
        4. Zvolte **Zvolit**.
        5. Vyberte **přidat**.
        6. Zvolte možnost **Uložit**.

        | Přihláška                                              | Oprávnění |
        |----------------------------------------------------------|-------------|
        | Zobrazovaný název nové aplikace, kterou jste vytvořili | Get, List   |
        | **Mikroslužby Microsoft Dynamics ERP**                 | Get, List   |

6. Přiřazení rolí pro přístup k účtu úložiště:

    1. V [portálu Azure](https://portal.azure.com) otevřete účet úložiště, který jste vytvořili dříve.
    2. Vyberte **Řízení přístupu (IAM)** a potom vyberte **Přiřazení rolí**.
    3. Vybere **Přidat, Přidat přiřazení rolí**.
    4. Pro každou aplikaci v následující tabulce postupujte takto:

        1. Vyberte roli z tabulky.
        2. Ponechte pole **Přiřadit přístup k** nastaveno na **Uživatel, skupina nebo objekt zabezpečení Azure AD**.
        3. V poli **Vybrat** zadejte aplikaci z tabulky.
        4. Zvolte možnost **Uložit**.

        | Přihláška                                              | Role                        |
        |----------------------------------------------------------|-----------------------------|
        | Zobrazovaný název nové aplikace, kterou jste vytvořili | Vlastník                       |
        | Zobrazovaný název nové aplikace, kterou jste vytvořili | Přispěvatel                 |
        | Zobrazovaný název nové aplikace, kterou jste vytvořili | Přispěvatel účtu úložiště |
        | Zobrazovaný název nové aplikace, kterou jste vytvořili | Vlastník dat objektu blob úložiště     |
        | **Autorizační služba AI Builder**                     | Čtenář dat objektu blob úložiště    |

# <a name="azure-cli"></a>[Server Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
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

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
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
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a>Konfigurace doplňku Export do Data Lake

Podle těchto pokynů použijte LCS k přidání doplňku Export do Data Lake do prostředí.

1. Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.
2. V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.
3. Vyberte doplněk **Export do Data Lake**.
4. Zadejte následující hodnoty.

    | Hodnota                                                              | popis |
    |--------------------------------------------------------------------|-------------|
    | ID klienta předplatného Azure, kde se nachází Key Vault | ID klienta, kde se nachází účet úložiště, aplikace a trezory klíčů. Tuto hodnotu získáte otevřením [portálu Azure](https://portal.azure.com), přejděte na **Azure Active Directory** a zkopírujte hodnotu **ID klienta**. |
    | Zadejte název DNS vašeho řešení Key Vault                             | Název DNS trezoru klíčů, například `https://customkeyvault.vault.azure.net/`. |
    | Zadejte tajný klíč, který obsahuje název účtu úložiště   | **storage-account-name** |
    | Název tajného klíče pro ID aplikace, který se má použít pro přístup k Data Lake          | **app-id** |
    | Název tajného klíče pro tajný kód klienta aplikace                                  | **app-secret** |

5. Odsouhlaste podmínky a pak vyberte **Instalovat**.

Doplněk bude nainstalován během několika minut.

## <a name="configure-the-finance-insights-add-in"></a>Konfigurace doplňku Finance Insights

> [!NOTE]
> Pokud jste si dříve nainstalovali doplněk Získání přehledů, odinstalujte jej před dokončením následujícího postupu.

Podle těchto pokynů nainstalujte doplněk Finance Insights.

1. Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.
2. V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.
3. Vyberte doplněk **Finance Insights**.
4. Odsouhlaste podmínky a pak vyberte **Instalovat**.

Instalace doplňku může trvat několik minut.

## <a name="feedback-and-support"></a>Zpětná vazba a podpora

Pokud máte zájem o poskytnutí zpětné vazby nebo pokud vyžadujete technickou podporu, zašlete prosím e-mail na [Finance Insights](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
