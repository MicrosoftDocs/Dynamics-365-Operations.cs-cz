---
title: Obecné řešení potíží
description: Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d5d9dbce0c74d32107db6bbae033b921e4201693
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275643"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="b5be3-103">Obecné řešení potíží</span><span class="sxs-lookup"><span data-stu-id="b5be3-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b5be3-104">Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b5be3-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5be3-105">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="b5be3-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b5be3-106">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="b5be3-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="b5be3-107">Při pokusu o instalaci balíčku dvojího zapisování pomocí nástroje package deployer se nezobrazí žádná dostupná řešení</span><span class="sxs-lookup"><span data-stu-id="b5be3-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="b5be3-108">Některé verze nástroje package deployer nejsou kompatibilní s balíčkem řešení dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="b5be3-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="b5be3-109">Chcete-li úspěšně nainstalovat balíček, je nutné použít [verzi 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) nebo novější z nástroje package deployer.</span><span class="sxs-lookup"><span data-stu-id="b5be3-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="b5be3-110">Po instalaci nástroje package deployer nainstalujte balíček řešení pomocí následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b5be3-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="b5be3-111">Stáhněte si nejnovější soubor balíčku řešení z Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="b5be3-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="b5be3-112">Po stažení souboru ZIP balíčku klepněte na něj pravým tlačítkem myši a vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="b5be3-113">Zaškrtněte políčko **odblokovat** a vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="b5be3-114">Není-li zaškrtávací políčko **Odblokovat** zobrazeno, je již zrušeno blokování souboru zip a tento krok můžete přeskočit.</span><span class="sxs-lookup"><span data-stu-id="b5be3-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogové okno Vlastnosti](media/unblock_option.png)

2. <span data-ttu-id="b5be3-116">Extrahujte soubor zip balíčku a zkopírujte všechny soubory ve složce **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.**</span><span class="sxs-lookup"><span data-stu-id="b5be3-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Obsah složky Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="b5be3-118">Vložte všechny zkopírované soubory do složky **Nástroje** v nástroji Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="b5be3-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="b5be3-119">Spuštěním **PackageDeployer.exe** vyberte prostředí Common Data Service a nainstalujte řešení.</span><span class="sxs-lookup"><span data-stu-id="b5be3-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Obsah složky Nástroje](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="b5be3-121">Chcete-li zobrazit podrobnosti chyby, povolte a zobrazte protokol sledování modulů plug-in v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b5be3-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="b5be3-122">**Požadovaná role pro zapnutí protokolu sledování a zobrazení chyb:** správce systému</span><span class="sxs-lookup"><span data-stu-id="b5be3-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="b5be3-123">Chcete-li zapnout protokol sledování, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="b5be3-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="b5be3-124">Přihlaste se k aplikaci Finance and Operations, otevřete stránku **Nastavení** a v části **Systém** vyberte možnost **Správa**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="b5be3-125">Na stránce **Správa** zvolte **Nastavení systému**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="b5be3-126">Na kartě **Vlastní nastavení** v poli **Modul plug-in a vlastní sledování aktivity workflowu** vyberte možnost **Vše**, chcete-li povolit trasovací protokol modulu plug-in.</span><span class="sxs-lookup"><span data-stu-id="b5be3-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="b5be3-127">Chcete-li protokolovat protokoly trasování pouze při výskytu výjimek, můžete namísto toho vybrat **Výjika**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="b5be3-128">Chcete-li zobrazit protokol sledování, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="b5be3-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="b5be3-129">Přihlaste se k aplikaci Finance and Operations, otevřete stránku **Nastavení** a v části **vlastní nastavení** vyberte možnost **Protokol sledování modulu plug-in**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="b5be3-130">Najděte protokoly sledování, kde pole **Název typu** je nastaveno na **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="b5be3-131">Chcete-li zobrazit úplný protokol, klikněte dvakrát na položku, a potom na pevné záložce **Spuštění** zkontrolujte text **Message Block**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="b5be3-132">Povolit režim ladění pro řešení potíží se živými synchronizacemi v aplikacích Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b5be3-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="b5be3-133">**Požadovaná role pro zobrazení chyb:** Chyby duálního zápisu správce systému, které vznikly v Common Data Service, se mohou objevit v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5be3-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="b5be3-134">V některých případech není úplný text chybové zprávy k dispozici, protože zpráva je příliš dlouhá nebo obsahuje osobní identifikační údaje (PII).</span><span class="sxs-lookup"><span data-stu-id="b5be3-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="b5be3-135">Pomocí následujících kroků můžete zapnout podrobné protokolování chyb.</span><span class="sxs-lookup"><span data-stu-id="b5be3-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="b5be3-136">Všechny konfigurace projektu v aplikacích Finance and Operations mají vlastnost **IsDebugMode** v entitě **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="b5be3-137">Otevřete entitu **DualWriteProjectConfiguration** pomocí doplňku aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b5be3-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="b5be3-138">Snadným způsobem, jak tuto entitu otevřít, je zapnout režim **Návrh** v doplňku aplikace Excel a poté přidat **DualWriteProjectConfigurationEntity** do listu.</span><span class="sxs-lookup"><span data-stu-id="b5be3-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="b5be3-139">další informace získáte v tématu [Otevření dat entity v aplikaci Excel a jejich aktualizace pomocí doplňku aplikace Excel](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b5be3-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="b5be3-140">Nastavte vlastnost **IsDebugMode** na **Ano** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="b5be3-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="b5be3-141">Spuštění scénáře generujících chyby.</span><span class="sxs-lookup"><span data-stu-id="b5be3-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="b5be3-142">Podrobné protokoly jsou k dispozici v tabulce DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="b5be3-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="b5be3-143">Chcete-li vyhledat data v prohlížeči tabulky, použijte následující adresu URL (nahraďte **XXX**):</span><span class="sxs-lookup"><span data-stu-id="b5be3-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="b5be3-144">Zkontrolujte chyby synchronizace ve virtuálním počítači pro aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b5be3-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="b5be3-145">**Požadovaná role pro zobrazení chyb:** Správce systému</span><span class="sxs-lookup"><span data-stu-id="b5be3-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="b5be3-146">Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b5be3-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="b5be3-147">Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="b5be3-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="b5be3-148">Zvolte dlaždici **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="b5be3-149">Pomocí vzdálené plochy se přihlaste k virtuálnímu počítači (VM) pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5be3-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="b5be3-150">Použijte místní účet, který je zobrazen v poli LCS.</span><span class="sxs-lookup"><span data-stu-id="b5be3-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="b5be3-151">Otevřete prohlížeč událostí.</span><span class="sxs-lookup"><span data-stu-id="b5be3-151">Open Event viewer.</span></span>
6. <span data-ttu-id="b5be3-152">Vyberte **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="b5be3-153">Prohlédněte si seznam posledních chyb.</span><span class="sxs-lookup"><span data-stu-id="b5be3-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="b5be3-154">Zrušte propojení a propjte jiné prostředí Common Data Service z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b5be3-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="b5be3-155">**Požadovaná role pro zrušení propojení prostředí:** Správce systému buď pro aplikaci Finance and Operations nebo Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b5be3-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="b5be3-156">Přihlášení do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5be3-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="b5be3-157">Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="b5be3-158">Vyberte všechna spuštěná mapování a pak vyberte **Zastavit**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="b5be3-159">Zvolte **Odpojit prostředí**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="b5be3-160">Vyberte **Ano**, chcete-li potvrdit operaci.</span><span class="sxs-lookup"><span data-stu-id="b5be3-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="b5be3-161">Nyní můžete propojit nové prostředí.</span><span class="sxs-lookup"><span data-stu-id="b5be3-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="b5be3-162">Nelze zobrazit formulář informací o řádku prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="b5be3-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="b5be3-163">Po vytvoření prodejní objednávky v produktu Dynamics 365 Sales se můžete kliknutím na možnost **+ Přidat produkty** přesměrovat do formuláře řádku objednávky Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b5be3-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="b5be3-164">Neexistuje žádný způsob, jak z tohoto formuláře zobrazit formulář **Informace** pro řádek prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b5be3-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="b5be3-165">Možnost pro **informace** není zobrazena v rozevírací nabídce pod položkou **Nový řádek objednávky**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="b5be3-166">K tomu dojde, protože operace projektu byly nainstalovány ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="b5be3-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="b5be3-167">Chcete-li znovu povolit možnost formuláře **Informace**, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="b5be3-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="b5be3-168">Přejděte na entitu **Řádek** objednávky.</span><span class="sxs-lookup"><span data-stu-id="b5be3-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="b5be3-169">Vyhledejte formulář **Informace** v uzlu formulářů.</span><span class="sxs-lookup"><span data-stu-id="b5be3-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="b5be3-170">Vyberte formulář **Informace** a klikněte na možnost **Povolit role zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="b5be3-171">Změňte nastavení zabezpečení na **Zobrazit všem**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-171">Change the security setting to **Display to everyone**.</span></span>
