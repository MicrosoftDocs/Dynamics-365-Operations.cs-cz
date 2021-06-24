---
title: Konfigurace Finance Insights pro public review (náhled) - verze 10.0.20 a novější
description: Toto téma vysvětluje, jak nakonfigurovat svůj systém, aby používal funkce, které jsou k dispozici ve Finance Insights pro public preview pro verze do 10.0.20.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222605"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="2ca7f-103">Konfigurace Finance Insights pro public review (náhled) - verze 10.0.20 a novější</span><span class="sxs-lookup"><span data-stu-id="2ca7f-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2ca7f-104">Finanční přehledy kombinují funkčnost Microsoft Dynamics 365 Finance s Dataverse, Azure a AI Builder, které vaší organizaci poskytnou výkonné nástroje pro prognózy.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="2ca7f-105">Toto téma vysvětluje, jak nakonfigurovat Dynamics 365 Finance verze 10.0.20, aby váš systém dokázal používat funkce, které jsou k dispozici ve Finance Insights pro public preview.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="2ca7f-106">Kroky konfigurace, které jsou popsány v tomto tématu, se vztahují pouze na verzi Finance 10.0.20 a novější.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="2ca7f-107">Informace o nastavení Finance Insights ve verzi 10.0.19 a starší najdete v tématu [Konfigurace Finance Insights - do verze 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="2ca7f-108">Nasazení Finance</span><span class="sxs-lookup"><span data-stu-id="2ca7f-108">Deploy Finance</span></span>

<span data-ttu-id="2ca7f-109">Pro nasazení prostředí postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="2ca7f-110">V Microsoft Dynamics Lifecycle Services (LCS) vytvořte nebo aktualizujte prostředí Finance.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="2ca7f-111">Prostředí vyžaduje verzi aplikace 10.0.20 nebo novější aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="2ca7f-112">Prostředí musí mít vysokou dostupnost (HA) v prostředí Sandbox.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="2ca7f-113">(Tento typ prostředí se také nazývá prostředí 2. úrovně.) Další informace najdete v tématu [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="2ca7f-114">Pokud konfigurujete Finance Insights v prostředí Sandbox, možná budete muset zkopírovat produkční data do tohoto prostředí, aby předpovědi fungovaly.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="2ca7f-115">Predikční model využívá k sestavování předpovědí několik let dat.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="2ca7f-116">Contoso demo data neobsahují dostatek historických dat pro adekvátní trénink predikčního modelu.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="2ca7f-117">Konfigurace služby Dataverse</span><span class="sxs-lookup"><span data-stu-id="2ca7f-117">Configure Dataverse</span></span>

<span data-ttu-id="2ca7f-118">Ke konfiguraci Dataverse pro Finance Insights proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="2ca7f-119">Otevřete stránku prostředí v LCS a ověřte, že část **Integrace Power Platform** je již nastavena.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="2ca7f-120">Pokud je již nastavena, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="2ca7f-121">Pokud ještě není nastavena, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="2ca7f-122">V části **Integrace Power Platform** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="2ca7f-123">Nastavení prostředí může trvat až hodinu.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="2ca7f-124">Pokud je prostředí Dataverse úspěšně nastaveno, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="2ca7f-125">Po dokončení nastavení prostředí **nevybírejte** **Odkaz na CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="2ca7f-126">Toto tlačítko není nutné pro Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="2ca7f-127">Pokud jej vyberete, nebudete moci nakonfigurovat požadované doplňky prostředí v LCS.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="2ca7f-128">Nakonfigurujte Azure</span><span class="sxs-lookup"><span data-stu-id="2ca7f-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="2ca7f-129">Použití Azure Cloud Shell k nastavení prostředků Data Lake finančních přehledů</span><span class="sxs-lookup"><span data-stu-id="2ca7f-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="2ca7f-130">Použití skriptu prostředí Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2ca7f-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="2ca7f-131">Byl poskytnut skript prostředí Windows PowerShell, takže můžete snadno nastavit prostředky Azure, které jsou popsány v části [Konfigurace exportu do Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="2ca7f-132">Pokud dáváte přednost ručnímu nastavení, tento postup přeskočte a dokončete postup v sekci [Ruční nastavení](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="2ca7f-133">Pomocí následujícího postupu spustíte skript prostředí Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="2ca7f-134">Nastavení nemusí fungovat, pokud používáte možnost **Vyzkoušet** v Azure CLI nebo pokud spustíte skript v počítači.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="2ca7f-135">Podle těchto pokynů nakonfigurujte Azure pomocí skriptu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="2ca7f-136">Musíte mít práva k vytvoření skupiny prostředků Azure, prostředků Azure a aplikace Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="2ca7f-137">Informace o požadovaných oprávněních najdete v části [Kontrola oprávnění Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="2ca7f-138">V [portálu Azure](https://portal.azure.com) přejděte na své cílové předplatné Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="2ca7f-139">Vyberte **Cloud Shell** napravo od pole **Vyhledávání**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="2ca7f-140">Vyberte **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="2ca7f-141">Pokud se zobrazí výzva, vytvořte úložiště.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="2ca7f-142">Na kartě **Azure CLI** vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="2ca7f-143">V poznámkovém bloku otevřete nový soubor a vložte jej do skriptu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="2ca7f-144">Uložte soubor jako **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="2ca7f-145">Nahrajte skript Windows PowerShell do relace pomocí možnosti nabídky pro nahrání v Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="2ca7f-146">Spusťte skript **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="2ca7f-147">Podle pokynů spusťte skript.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="2ca7f-148">Použijte informace z výstupu skriptu k instalaci doplňku Export do Data Lake v LCS.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="2ca7f-149">Ruční nastavení</span><span class="sxs-lookup"><span data-stu-id="2ca7f-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="2ca7f-150">Přidání aplikací do klienta Azure AD</span><span class="sxs-lookup"><span data-stu-id="2ca7f-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="2ca7f-151">V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="2ca7f-152">Vyberte **Správa \> Podnikové aplikace**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="2ca7f-153">Vyhledejte následující aplikace podle ID aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="2ca7f-154">Přihláška</span><span class="sxs-lookup"><span data-stu-id="2ca7f-154">Application</span></span>                              | <span data-ttu-id="2ca7f-155">ID aplikace</span><span class="sxs-lookup"><span data-stu-id="2ca7f-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="2ca7f-156">Mikroslužby Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="2ca7f-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="2ca7f-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="2ca7f-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="2ca7f-158">Mikroslužby CDS Microsoft Dynamics ERP</span><span class="sxs-lookup"><span data-stu-id="2ca7f-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="2ca7f-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="2ca7f-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="2ca7f-160">Autorizační služba AI Builder</span><span class="sxs-lookup"><span data-stu-id="2ca7f-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="2ca7f-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="2ca7f-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="2ca7f-162">Pokud nemůžete najít žádnou z předchozích aplikací, vyzkoušejte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="2ca7f-163">Na místním počítači vyberte nabídku **Start** a hledejte **powershell**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="2ca7f-164">Vyberte a podržte (nebo klikněte pravým tlačítkem na) **Windows PowerShell** a potom vyberte **Spustit jako správce**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="2ca7f-165">Spusťte následující příkaz k instalaci modulu **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="2ca7f-166">Pokud je pro pokračování potřeba poskytovatel NuGet, k jeho instalaci vyberte **Y**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="2ca7f-167">Pokud obdržíte zprávu „Nedůvěryhodné úložiště“, pro pokračování vyberte **Y**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="2ca7f-168">Pro každou aplikaci, kterou je třeba přidat, spusťte následující příkazy, abyste ji přidali do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="2ca7f-169">Po zobrazení výzvy se přihlaste jako správce Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="2ca7f-170">Vytvoření zdrojů Azure</span><span class="sxs-lookup"><span data-stu-id="2ca7f-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="2ca7f-171">Nezapomeňte vytvořit následující prostředky ve stejné instanci Azure AD, ve kterém je prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="2ca7f-172">Nelze použít prostředky z jiné instance Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="2ca7f-173">Vytvoření účtu úložiště:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-173">Create a storage account:</span></span>

    1. <span data-ttu-id="2ca7f-174">V [portálu Azure](https://portal.azure.com) vytvořte účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="2ca7f-175">V dialogovém okně **Vytvoření účtu úložiště** nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="2ca7f-176">**Umístění** – Vyberte datové centrum, kde se nachází vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="2ca7f-177">**Výkon** – Doporučujeme, abyste vybrali **Standard**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="2ca7f-178">**Druh účtu** – Musíte vybrat **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="2ca7f-179">V dialogovém okně **Rozšířené možnosti** pro **Data Lake Storage Gen2** vyberte možnost **Povolit** pro funkci **Hierarchický obor názvů**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="2ca7f-180">Pokud tuto funkci nepovolíte, nebudete moci spotřebovat data, která aplikace Finance and Operations zapíše při použití služeb, jako jsou toky dat Power BI.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="2ca7f-181">Vyberte **Zkontrolovat a vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-181">Select **Review and create**.</span></span> <span data-ttu-id="2ca7f-182">Po dokončení nasazení se nový prostředek zobrazí v portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="2ca7f-183">Přejděte na účet úložiště, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="2ca7f-184">V levé nabídce vyberte možnost **Přístupové klíče**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="2ca7f-185">Zkopírujte a uložte název účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="2ca7f-186">Tuto hodnotu budete muset zadat později, až nastavíte tajné kódy trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="2ca7f-187">Vytvoření trezoru klíčů:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-187">Create a key vault:</span></span>

    1. <span data-ttu-id="2ca7f-188">V [portálu Azure](https://portal.azure.com) vytvořte trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="2ca7f-189">V dialogovém okně **Vytvoření trezoru klíčů** v poli **Umístění** vyberte datové centrum, kde se nachází vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="2ca7f-190">Po vytvoření trezoru klíčů přejděte na **Přehled trezoru klíčů** a zkopírujte a uložte název DNS.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="2ca7f-191">Tuto hodnotu budete muset zadat později, až nastavíte doplněk Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="2ca7f-192">Vytvoření a zaregistrování aplikace Azure AD:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="2ca7f-193">V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory** a poté vyberte možnost **Registrace aplikací**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="2ca7f-194">Vyberte **Registrace nové aplikace** a nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="2ca7f-195">**Název** – Zadejte název aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="2ca7f-196">**Typ aplikace** – Vyberte **Webové rozhraní API**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="2ca7f-197">**Nastavení URI přesměrování** – Zadejte adresu URL instance Dynamics 365, například `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="2ca7f-198">Přejděte do aplikace, kterou jste právě vytvořili, a zkopírujte ji a uložte její hodnotu **ID aplikace (klienta)**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="2ca7f-199">Tuto hodnotu budete muset zadat později, až nastavíte tajné kódy trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="2ca7f-200">Přejděte na **Oprávnění API** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="2ca7f-201">Vyberte **Přidat oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="2ca7f-202">Vyberte **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="2ca7f-203">Po výběru delegovaných oprávnění vyberte **uživatel\_zosobnění**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="2ca7f-204">Vyberte **Přidat oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="2ca7f-205">V nabídce aplikace vyberte **Certifikáty \& tajné klíče** a poté podle těchto kroků vytvořte tajné klíče Key Vault:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="2ca7f-206">Vyberte **Nový tajný klíč klienta**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="2ca7f-207">V poli **Popis klíče** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="2ca7f-208">Vyberte dobu trvání a potom vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="2ca7f-209">V poli **Hodnota** se vygeneruje tajný klíč.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="2ca7f-210">Zkopírujte a uložte hodnotu tajného klíče klienta.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-210">Copy and save the client secret value.</span></span> <span data-ttu-id="2ca7f-211">Tuto hodnotu budete muset zadat později, až nastavíte tajné kódy trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="2ca7f-212">Vytvoření tajných klíčů Key Vault:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="2ca7f-213">Přejděte do trezoru klíčů, který jste vytvořili dříve, a vyberte **Tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="2ca7f-214">Pro každý název tajného klíče v následující tabulce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="2ca7f-215">Vyberte **Generovat/import**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="2ca7f-216">V dialogovém okně **Vytvoření tajného klíče** v poli **Možnosti odesílání** vyberte **Ručně**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="2ca7f-217">Vytvořte název tajného klíče a hodnotu z tabulky.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="2ca7f-218">Vyberte **Povolit** a potom vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="2ca7f-219">Tajný klíč je vytvořen a přidán do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="2ca7f-220">Název tajného klíče</span><span class="sxs-lookup"><span data-stu-id="2ca7f-220">Secret name</span></span>                       | <span data-ttu-id="2ca7f-221">Hodnota tajného klíče</span><span class="sxs-lookup"><span data-stu-id="2ca7f-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="2ca7f-222">app-id</span><span class="sxs-lookup"><span data-stu-id="2ca7f-222">app-id</span></span>                            | <span data-ttu-id="2ca7f-223">ID aplikace, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="2ca7f-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="2ca7f-224">app-secret</span></span>                        | <span data-ttu-id="2ca7f-225">Tajný klíč klienta, které jste uložili dříve.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="2ca7f-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="2ca7f-226">storage-account-name</span></span>              | <span data-ttu-id="2ca7f-227">Název účtu úložiště, který jste vytvořili dříve, například **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="2ca7f-228">Autorizujte aplikaci pro přístup do trezoru klíčů:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="2ca7f-229">V [portálu Azure](https://portal.azure.com) otevřete trezor klíčů, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="2ca7f-230">Vyberte zásady přístupu.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-230">Select the access policies.</span></span>
    3. <span data-ttu-id="2ca7f-231">Pro každou aplikaci v následující tabulce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="2ca7f-232">Volbou **Přidat zásady přístupu** vytvořte zásady přístupu.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="2ca7f-233">V poli **Oprávnění na základě tajných klíčů** vyberte oprávnění z tabulky.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="2ca7f-234">V poli **Výběr objektu zabezpečení** vyhledejte zobrazovaný název aplikace v tabulce.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="2ca7f-235">Zvolte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-235">Select **Select**.</span></span>
        5. <span data-ttu-id="2ca7f-236">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-236">Select **Add**.</span></span>
        6. <span data-ttu-id="2ca7f-237">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-237">Select **Save**.</span></span>

        | <span data-ttu-id="2ca7f-238">Přihláška</span><span class="sxs-lookup"><span data-stu-id="2ca7f-238">Application</span></span>                                              | <span data-ttu-id="2ca7f-239">Oprávnění</span><span class="sxs-lookup"><span data-stu-id="2ca7f-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="2ca7f-240">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="2ca7f-240">The display name of the new application that you created</span></span> | <span data-ttu-id="2ca7f-241">Get, List</span><span class="sxs-lookup"><span data-stu-id="2ca7f-241">Get, List</span></span>   |
        | <span data-ttu-id="2ca7f-242">**Mikroslužby Microsoft Dynamics ERP**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="2ca7f-243">Get, List</span><span class="sxs-lookup"><span data-stu-id="2ca7f-243">Get, List</span></span>   |

6. <span data-ttu-id="2ca7f-244">Přiřazení rolí pro přístup k účtu úložiště:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="2ca7f-245">V [portálu Azure](https://portal.azure.com) otevřete účet úložiště, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="2ca7f-246">Vyberte **Řízení přístupu (IAM)** a potom vyberte **Přiřazení rolí**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="2ca7f-247">Vybere **Přidat, Přidat přiřazení rolí**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="2ca7f-248">Pro každou aplikaci v následující tabulce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2ca7f-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="2ca7f-249">Vyberte roli z tabulky.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="2ca7f-250">Ponechte pole **Přiřadit přístup k** nastaveno na **Uživatel, skupina nebo objekt zabezpečení Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="2ca7f-251">V poli **Vybrat** zadejte aplikaci z tabulky.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="2ca7f-252">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-252">Select **Save**.</span></span>

        | <span data-ttu-id="2ca7f-253">Přihláška</span><span class="sxs-lookup"><span data-stu-id="2ca7f-253">Application</span></span>                                              | <span data-ttu-id="2ca7f-254">Role</span><span class="sxs-lookup"><span data-stu-id="2ca7f-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="2ca7f-255">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="2ca7f-255">The display name of the new application that you created</span></span> | <span data-ttu-id="2ca7f-256">Vlastník</span><span class="sxs-lookup"><span data-stu-id="2ca7f-256">Owner</span></span>                       |
        | <span data-ttu-id="2ca7f-257">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="2ca7f-257">The display name of the new application that you created</span></span> | <span data-ttu-id="2ca7f-258">Přispěvatel</span><span class="sxs-lookup"><span data-stu-id="2ca7f-258">Contributor</span></span>                 |
        | <span data-ttu-id="2ca7f-259">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="2ca7f-259">The display name of the new application that you created</span></span> | <span data-ttu-id="2ca7f-260">Přispěvatel účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="2ca7f-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="2ca7f-261">Zobrazovaný název nové aplikace, kterou jste vytvořili</span><span class="sxs-lookup"><span data-stu-id="2ca7f-261">The display name of the new application that you created</span></span> | <span data-ttu-id="2ca7f-262">Vlastník dat objektu blob úložiště</span><span class="sxs-lookup"><span data-stu-id="2ca7f-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="2ca7f-263">**Autorizační služba AI Builder**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="2ca7f-264">Čtenář dat objektu blob úložiště</span><span class="sxs-lookup"><span data-stu-id="2ca7f-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="2ca7f-265">Server Azure CLI</span><span class="sxs-lookup"><span data-stu-id="2ca7f-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="2ca7f-266">Konfigurace doplňku Export do Data Lake</span><span class="sxs-lookup"><span data-stu-id="2ca7f-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="2ca7f-267">Podle těchto pokynů použijte LCS k přidání doplňku Export do Data Lake do prostředí.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="2ca7f-268">Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="2ca7f-269">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="2ca7f-270">Vyberte doplněk **Export do Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="2ca7f-271">Zadejte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-271">Enter the following values.</span></span>

    | <span data-ttu-id="2ca7f-272">Hodnota</span><span class="sxs-lookup"><span data-stu-id="2ca7f-272">Value</span></span>                                                              | <span data-ttu-id="2ca7f-273">popis</span><span class="sxs-lookup"><span data-stu-id="2ca7f-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="2ca7f-274">ID klienta předplatného Azure, kde se nachází Key Vault</span><span class="sxs-lookup"><span data-stu-id="2ca7f-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="2ca7f-275">ID klienta, kde se nachází účet úložiště, aplikace a trezory klíčů.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="2ca7f-276">Tuto hodnotu získáte otevřením [portálu Azure](https://portal.azure.com), přejděte na **Azure Active Directory** a zkopírujte hodnotu **ID klienta**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="2ca7f-277">Zadejte název DNS vašeho řešení Key Vault</span><span class="sxs-lookup"><span data-stu-id="2ca7f-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="2ca7f-278">Název DNS trezoru klíčů, například `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="2ca7f-279">Zadejte tajný klíč, který obsahuje název účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="2ca7f-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="2ca7f-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="2ca7f-281">Název tajného klíče pro ID aplikace, který se má použít pro přístup k Data Lake</span><span class="sxs-lookup"><span data-stu-id="2ca7f-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="2ca7f-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-282">**app-id**</span></span> |
    | <span data-ttu-id="2ca7f-283">Název tajného klíče pro tajný kód klienta aplikace</span><span class="sxs-lookup"><span data-stu-id="2ca7f-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="2ca7f-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-284">**app-secret**</span></span> |

5. <span data-ttu-id="2ca7f-285">Odsouhlaste podmínky a pak vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="2ca7f-286">Doplněk bude nainstalován během několika minut.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="2ca7f-287">Konfigurace doplňku Finance Insights</span><span class="sxs-lookup"><span data-stu-id="2ca7f-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="2ca7f-288">Pokud jste si dříve nainstalovali doplněk Získání přehledů, odinstalujte jej před dokončením následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="2ca7f-289">Podle těchto pokynů nainstalujte doplněk Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="2ca7f-290">Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="2ca7f-291">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="2ca7f-292">Vyberte doplněk **Finance Insights**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="2ca7f-293">Odsouhlaste podmínky a pak vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="2ca7f-294">Zpětná vazba a podpora</span><span class="sxs-lookup"><span data-stu-id="2ca7f-294">Feedback and support</span></span>

<span data-ttu-id="2ca7f-295">Pokud máte zájem o poskytnutí zpětné vazby nebo pokud vyžadujete technickou podporu, zašlete prosím e-mail na [Finance Insights (Preview)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
