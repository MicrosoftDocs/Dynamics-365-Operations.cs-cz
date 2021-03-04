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
# <a name="configuration-for-finance-insights-preview"></a>Konfigurace finančních přehledů (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finanční přehledy kombinují funkčnost Microsoft Dynamics 365 Finance s Common Data Service, Azure a AI Builder, které vaší organizaci poskytnou výkonné nástroje pro prognózy. Toto téma vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech.

## <a name="deploy-dynamics-365-finance"></a>Nasazení Dynamics 365 Finance

Pro nasazení prostředí postupujte takto.

1. V Microsoft Dynamics Lifecycle Services (LCS) vytvořte nebo aktualizujte prostředí Dynamics 365 Finance. Prostředí vyžaduje verzi aplikace 10.0.11 / Platform update 35 nebo novější.
2. Prostředí musí mít vysokou dostupnost (HA) v prostředí Sandbox. (Tento typ prostředí se také nazývá prostředí 2. úrovně.) Další informace najdete v tématu [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Pokud používáte ukázková data společnosti Contoso, budete potřebovat další ukázková data, abyste mohli používat funkce predikcí plateb zákazníka, prognózy cashflow a prognózy rozpočtu. 

## <a name="configure-common-data-service"></a>Konfigurace služby Common Data Service

Můžete provést následující kroky ruční konfigurace nebo můžete zrychlit proces konfigurace pomocí skriptu Windows PowerShell, který je k dispozici. Po provedení skriptu PowerShell získáte hodnoty, které se mají použít ke konfiguraci finančních přehledů. 

> [!NOTE]
> V počítači otevřete PowerShell a spusťte skript. Možná budete potřebovat PowerShell verze 5. Možnost „Try it“ (vyzkoušet) Microsoft Azure CLI nemusí fungovat.

# <a name="manual-configuration-steps"></a>[Ruční kroky konfigurace](#tab/configuration-steps)

1. Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com/) a podle těchto kroků vytvořte nové prostředí Common Data Service ve stejném klientovi Active Directory:

    1. Otevřete stránku **Prostředí**.

        [![Stránka Prostředí](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Vyberte **Nové prostředí**.
    3. V poli **Typ** vyberte **Sandbox**.
    4. Nastavte možnost **Vytvořit databázi** na **Ano**.
    5. Zvolte **Další**.
    6. Vyberte jazyk a měnu vaší organizace.
    7. Potvrďte výchozí hodnoty v ostatních polích.
    8. Zvolte **Uložit**.
    9. Aktualizujte stránku **Prostředí**.
    10. Počkejte, až se hodnota pole **Stav** aktualizuje na **Připraveno**.
    11. Poznamenejte si ID organizace Common Data Service.
    12. Vyberte prostředí , ke zkopírování a pak vyberte **Nastavení**.
    13. Vyberte **Prostředky \> Všechna starší nastavení**.
    14. Na horním navigačním panelu vyberte **Nastavení** a potom vyberte **Vlastní nastavení**.
    15. Vyberte **Vývojářské prostředky**.
    16. Nastavte pole **ID referenčních informací o instanci** na hodnotu ID organizace Common Data Service, kterou jste si dříve poznamenali.
    17. V adresním řádku prohlížeče si poznamenejte URL pro organizaci Common Data Service. Adresa URL může být například `https://org42b2b3d3.crm.dynamics.com`.

2. Pokud plánujete použít funkci prognóz cashflow nebo rozpočtu, postupujte podle těchto kroků a aktualizujte limit anotací pro vaši organizaci na nejméně 50 megabajtů (MB):

    1. Otevřete [Power Apps Portal](https://make.powerapps.com).
    2. Vyberte prostředí, které jste právě vytvořili, a poté vyberte **Pokročilá nastavení**.
    3. Vyberte **Nastavení \> Konfigurace e-mailu**.
    4. Změňte hodnotu pole **Maximální velikost souboru** na **51200**. (Hodnota je vyjádřena v kilobytech \[kB\].)
    5. Vyberte **OK** a uložte změny.

# <a name="windows-powershell-configuration-script"></a>[Konfigurační skript prostředí Windows PowerShell](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>Konfigurace nastavení Azure

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a>Zadejte ID adresáře Common Data Service a ID objektu Azure AD uživatele

1. Zadejte ID adresáře Common Data Service:

    1. Otevřete [portál Azure](https://portal.azure.com).
    2. Přihlaste se pomocí ID uživatele, které bylo použito k vytvoření prostředí Common Data Service.
    3. Přejděte na **Azure Active Directory**.
    4. Zkopírujte hodnotu **ID klienta**.

2. Zadejte ID objektu uživatele Azure Active Directory (Azure AD):

    1. V [portálu Azure](https://portal.azure.com) přejděte na **Uživatelé** a vyhledejte uživatele podle e-mailové adresy.
    2. Vyberte jméno uživatele.
    3. Zkopírujte hodnotu **ID objektu**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Použití Azure Cloud Shell k nastavení prostředků Data Lake finančních přehledů

# <a name="use-a-windows-powershell-script"></a>[Použití skriptu prostředí Windows PowerShell](#tab/use-a-powershell-script)

Byl poskytnut skript prostředí Windows PowerShell, takže můžete snadno nastavit prostředky Azure, které jsou popsány v části [Konfigurace exportu do Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake). Pokud dáváte přednost ručnímu nastavení, tento postup přeskočte a pokračujte postupem v sekci [Ruční nastavení](#manual-setup).

> [!NOTE]
> Podle následujících pokynů spusťte skript prostředí PowerShell. Možnost „Try it“ (vyzkoušet) Azure CLI nebo spuštění skriptu na vašem počítači nemusí fungovat.

Podle těchto pokynů nakonfigurujte Azure pomocí skriptu Windows PowerShell. Musíte mít práva k vytvoření skupiny prostředků Azure, prostředků Azure a aplikace Azure AD. Informace o požadovaných oprávněních najdete v části [Kontrola oprávnění Azure AD](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. V [portálu Azure](https://portal.azure.com) přejděte na své cílové předplatné Azure. Vyberte tlačítko **Cloud Shell** napravo od pole **Vyhledávání**.
2. Vyberte **PowerShell**.
3. Pokud se zobrazí výzva, vytvořte úložiště. Potom nahrajte skript prostředí Windows PowerShell do relace.
4. Spusťte skript.
5. Podle pokynů spusťte skript.
6. Použijte informace z výstupu skriptu k instalaci doplňku **Export do Data Lake** v LCS.
7. Pomocí informací z výstupu skriptu povolte úložiště entit na stránce **Datová připojení** ve Finance (**Správa systému \> Parametry systému \> Datová připojení**).

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

4. Pokud je pro pokračování potřeba poskytovatel NuGet, k jeho instalaci vyberte **A**.
5. Pokud se zobrazí zpráva „Nedůvěryhodné úložiště“, pro pokračování vyberte **A**.
6. Pro každou aplikaci, kterou je třeba přidat, spusťte následující příkazy, abyste ji přidali do Azure AD. Po zobrazení výzvy se přihlaste jako správce Azure AD.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Vytvoření zdrojů Azure

> [!NOTE]
> Nezapomeňte vytvořit následující prostředky ve stejné instanci Azure AD jako prostředí Common Data Service. Nelze použít prostředky z jiné instance Azure AD.

1. Vytvoření nového účtu úložiště:

    1. V [portálu Azure](https://portal.azure.com) vytvořte účet úložiště.
    2. V dialogovém okně **Vytvoření účtu úložiště** nastavte následující pole:

        - **Umístění** – Vyberte datové centrum, kde se nachází vaše prostředí.
        - **Výkon** – Doporučujeme, abyste vybrali **Standard**.
        - **Druh účtu** – Musíte vybrat **StorageV2**.

    3. V dialogovém okně **Rozšířené možnosti** pro **Data Lake Storage Gen2** vyberte možnost **Povolit** pro funkci **Hierarchický obor názvů**. Pokud tuto funkci deaktivujete, nebudete moci spotřebovat data, která aplikace Finance and Operations zapíše při použití služeb, jako jsou toky dat Power BI.
    4. Vyberte **Zkontrolovat a vytvořit**. Po dokončení nasazení se nový prostředek zobrazí v portálu Azure.
    5. Přejděte na účet úložiště, který jste vytvořili.
    6. V levé nabídce vyberte možnost **Přístupové klíče**.
    7. Zkopírujte a uložte připojovací řetězec buď **Klíč1** nebo **Klíč2**.
    8. Zkopírujte a uložte název účtu úložiště.

2. Vytvoření nového trezoru klíčů:

    1. V [portálu Azure](https://portal.azure.com) vytvořte trezor klíčů.
    2. V dialogovém okně **Vytvoření trezoru klíčů** v poli **Umístění** vyberte datové centrum, kde se nachází vaše prostředí.
    3. Po vytvoření trezoru klíčů jej vyberte v seznamu a poté vyberte **Tajné klíče**.
    4. Vyberte **Generovat/import**.
    5. V dialogovém okně **Vytvoření tajného klíče** v poli **Možnosti odesílání** vyberte **Ručně**.
    6. Zadejte název tajného klíče. Poznamenejte si tento název, protože jej budete muset zadat později.
    7. V poli **Hodnota** zadejte připojovací řetězec, který jste získali z účtu úložiště v předchozím postupu.
    8. Vyberte **Povolit** a potom vyberte **Vytvořit**. Tajný klíč je vytvořen a přidán do Key Vault.
    9. Přejděte na **Přehled Key Vault** a poznamenejte si název DNS.

3. Vytvoření a zaregistrování aplikace Azure AD:

    1. V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory** a poté vyberte možnost **Registrace aplikací**.
    2. Vyberte **Registrace nové aplikace** a nastavte následující pole:

        - **Název** – Zadejte název aplikace.
        - **Typ aplikace** – Vyberte **Webové rozhraní API**.
        - **Nastavení URI přesměrování** – Zadejte adresu URL instance Dynamics 365, například `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Přejděte do aplikace, kterou jste právě vytvořili, a zkopírujte ji a uložte její hodnotu **ID aplikace (klienta)**. Tuto hodnotu budete muset zadat později, až nastavíte trezor klíčů.
    4. Přejděte na **Oprávnění API** a postupujte takto:

        1. Vyberte **Přidat oprávnění**.
        2. Vyberte **Azure Key Vault**.
        3. Po výběru delegovaných oprávnění vyberte **uživatel\_zosobnění**.
        4. Vyberte **Přidat oprávnění**.

    5. V nabídce aplikace vyberte **Certifikáty \& tajné klíče** a poté podle těchto kroků vytvořte tajné klíče Key Vault:

        1. Vyberte **Nový tajný klíč klienta**.
        2. V poli **Popis klíče** zadejte název.
        3. Vyberte dobu trvání a potom vyberte **Přidat**. V poli **Hodnota** se vygeneruje tajný klíč.
        4. Zkopírujte a uložte hodnotu tajného klíče.

4. Vytvoření tajných klíčů Key Vault:

    1. Přejděte do trezoru klíčů, který jste vytvořili dříve, a vyberte **Tajné klíče**.
    2. Pro každý název tajného klíče v následující tabulce postupujte takto:

        1. Vyberte **Generovat/import**.
        2. V dialogovém okně **Vytvoření tajného klíče** v poli **Možnosti odesílání** vyberte **Ručně**.
        3. Vytvořte název tajného klíče a hodnotu z následující tabulky.
        4. Vyberte **Povolit** a potom vyberte **Vytvořit**. Tajný klíč je vytvořen a přidán do Key Vault.

        | Název tajného klíče                       | Hodnota tajného klíče                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | ID aplikace, kterou jste vytvořili dříve                                      |
        | app-secret                        | Tajný klíč klienta, které jste uložili dříve                                                    |
        | storage-account-name              | Název účtu úložiště, který jste vytvořili dříve, například **storageaccount1**       |
        | storage-account-connection-string | Připojovací řetězec, který jste zkopírovali ze stránky **Přístupové klíče** pro účet úložiště |

5. Autorizujte aplikaci pro přístup do trezoru klíčů:

    1. V [portálu Azure](https://portal.azure.com) otevřete trezor klíčů, který jste vytvořili dříve.
    2. Vyberte zásady přístupu.
    3. Pro každou aplikaci v následující tabulce postupujte takto:

        1. Volbou **Přidat zásady přístupu** vytvořte zásady přístupu.
        2. V poli **Oprávnění na základě tajných klíčů** vyberte oprávnění z následující tabulky.
        3. V poli **Výběr objektu zabezpečení** vyhledejte zobrazovaný název aplikace v následující tabulce.
        4. Zvolte **Zvolit**.
        5. Vyberte **přidat**.
        6. Zvolte **Uložit**.

        | Přihláška                                              | Oprávnění |
        |----------------------------------------------------------|-------------|
        | Zobrazovaný název nové aplikace, kterou jste vytvořili | Get, List   |
        | **Mikroslužby Microsoft Dynamics ERP**                 | Get, List   |

6. Přiřazení rolí pro přístup k účtu úložiště:

    1. V [portálu Azure](https://portal.azure.com) otevřete účet úložiště, který jste vytvořili dříve.
    2. Vyberte **Řízení přístupu (IAM)** a potom vyberte **Přiřazení rolí**.
    3. Vybere **Přidat, Přidat přiřazení rolí**.
    4. Pro každou aplikaci v následující tabulce postupujte takto:

        1. Vyberte roli z následující tabulky.
        2. Ponechte pole **Přiřadit přístup k** nastaveno na **Uživatel, skupina nebo objekt zabezpečení Azure AD**.
        3. V poli **Vybrat** zadejte aplikaci z následující tabulky.
        4. Zvolte **Uložit**.

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

## <a name="configure-the-entity-store"></a>Konfigurace úložiště entit

Pomocí těchto kroků nastavíte úložiště entit ve vašem prostředí Finance.

1. Přejděte do nabídky **Správa systému \> Nastavení \> Systémové parametry \> Datová připojení**.
2. Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.
3. Nastavte následující pole Key Vault:

    - **ID aplikace (klienta)** – Zadejte ID klienta aplikace, které jste vytvořili dříve.
    - **Tajný klíč aplikace** – Zadejte tajný klíč, které jste uložili pro aplikaci, kterou jste vytvořili dříve.
    - **Název DNS** – Název systému DNS (Domain Name System) najdete na stránce s podrobnostmi o aplikaci, kterou jste vytvořili dříve.
    - **Název tajného klíče** – Zadejte **storage-account-connection-string**.

## <a name="configure-the-data-lake"></a>Konfigurace datového jezera

Podle těchto pokynů použijte LCS k přidání doplňku Azure Data Lake do prostředí.

1. Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.
2. V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.
3. Vyberte doplněk **Export do Data Lake**.
4. Zadejte následující hodnoty.

    | Hodnota                                                              | popis |
    |--------------------------------------------------------------------|-------------|
    | ID klienta předplatného Azure, kde se nachází Key Vault | ID klienta, kde se nachází účet úložiště, aplikace a trezory klíčů. Tuto hodnotu najdete otevřením [portálu Azure](https://portal.azure.com), přejděte na **Azure Active Directory** a zkopírujte hodnotu **ID klienta**. |
    | Zadejte název DNS vašeho řešení Key Vault                             | Název DNS trezoru klíčů, například `https://customkeyvault.vault.azure.net/`. (Tato hodnota odpovídá názvu DNS, který se používá v úložišti entit.) |
    | Zadejte tajný klíč, který obsahuje název účtu úložiště   | **storage-account-name** |
    | Název tajného klíče pro ID aplikace, který se má použít pro přístup k Data Lake          | **app-id** |
    | Název tajného klíče, který se má použít s ID aplikace                                 | **app-secret** |

5. Odsouhlaste podmínky a vyberte **Instalovat**.

Doplněk bude nainstalován během několika minut.

## <a name="configure-ai-builder"></a>Konfigurace nástroje AI Builder

1. Přihlaste se k LCS a otevřete stránku **Podrobnosti prostředí**.
2. Přejděte do části **Doplňky prostředí**. Měli byste vidět doplňky, které jsou již v tomto prostředí nainstalovány. Pokud doplněk **Export do Data Lake** mezi nimi není, nakonfigurujte tento doplněk.
3. Vyberte doplněk **Získání přehledů**.
4. Na stránce podrobností doplňku **Získání přehledů** zadejte následující hodnoty.

    | Hodnota                                                    | popis |
    |----------------------------------------------------------|-------------|
    | Adresa URL organizace CDS                                     | Adrsa URL organizace Common Data Service instance Common Data Service. Tuto hodnotu najdete otevřením [portálu Power Apps](https://make.powerapps.com), výběrem tlačítka **Nastavení** (symbol ozubeného kola) v pravém horním rohu, výběrem možnosti **Pokročilá nastavení** a zkopírováním adresy URL. (Adresa URL končí řetězcem „dynamics.com“.) |
    | ID org. CDS                                               | ID prostředí instance Common Data Service. Tuto hodnotu najdete otevřením [portálu Power Apps](https://make.powerapps.com), výběrem tlačítka **Nastavení** (symbol ozubeného kola) v pravém horním rohu, výběrem možnosti **Vlastní nastavení \> Vývojářské prostředky \> Referenční informace o instanci** a zkopírováním hodnoty **ID**. |
    | ID klienta CDS (ID adresáře z AAD)               | ID klienta instance Common Data Service. Tuto hodnotu najdete otevřením [portálu Azure](https://portal.azure.com), přejděte na **Azure Active Directory** a zkopírujte hodnotu **ID klienta**. |
    | Zadejte ID objektu uživatele, který má roli správce systému | ID objektu uživatele Azure AD v Common Data Service. Tento uživatel musí být správcem systému instance Common Data Service. Tuto hodnotu najdete otevřením [portálu Azure](https://portal.azure.com), otevřením nabídky **Azure Active Directory \> Uživatelé**, výběrem uživatele a poté v sekci **Identita** zkopírováním hodnoty **ID objektu**. |
    | Je toto výchozí prostředí CDS pro klienta?      | Pokud instance Common Data Service byla první produkční instance, která byla vytvořena, zaškrtněte toto políčko. Pokud instance Common Data Service byla vytvořena ručně, zrušte zaškrtnutí tohoto políčka. |

## <a name="feedback-and-support"></a>Názory a podpora

Zašlete prosím e-mail na [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com), pokud máte zájem o poskytnutí názoru nebo potřebujete podporu.

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]