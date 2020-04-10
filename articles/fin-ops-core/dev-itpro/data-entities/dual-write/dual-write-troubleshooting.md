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
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172684"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="a2d12-103">Obecné řešení potíží</span><span class="sxs-lookup"><span data-stu-id="a2d12-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a2d12-104">Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a2d12-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2d12-105">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a2d12-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a2d12-106">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="a2d12-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="a2d12-107">Při pokusu o instalaci balíčku dvojího zapisování pomocí nástroje package deployer se nezobrazí žádná dostupná řešení</span><span class="sxs-lookup"><span data-stu-id="a2d12-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="a2d12-108">Některé verze nástroje package deployer nejsou kompatibilní s balíčkem řešení dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="a2d12-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="a2d12-109">Chcete-li úspěšně nainstalovat balíček, je nutné použít [verzi 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) nebo novější z nástroje package deployer.</span><span class="sxs-lookup"><span data-stu-id="a2d12-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="a2d12-110">Po instalaci nástroje package deployer nainstalujte balíček řešení pomocí následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a2d12-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="a2d12-111">Stáhněte si nejnovější soubor balíčku řešení z Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="a2d12-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="a2d12-112">Po stažení souboru ZIP balíčku klepněte na něj pravým tlačítkem myši a vyberte **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="a2d12-113">Zaškrtněte políčko **odblokovat** a vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="a2d12-114">Není-li zaškrtávací políčko **Odblokovat** zobrazeno, je již zrušeno blokování souboru zip a tento krok můžete přeskočit.</span><span class="sxs-lookup"><span data-stu-id="a2d12-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogové okno Vlastnosti](media/unblock_option.png)

2. <span data-ttu-id="a2d12-116">Extrahujte soubor zip balíčku a zkopírujte všechny soubory ve složce **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.**</span><span class="sxs-lookup"><span data-stu-id="a2d12-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Obsah složky Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="a2d12-118">Vložte všechny zkopírované soubory do složky **Nástroje** v nástroji Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="a2d12-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="a2d12-119">Spuštěním **PackageDeployer.exe** vyberte prostředí Common Data Service a nainstalujte řešení.</span><span class="sxs-lookup"><span data-stu-id="a2d12-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Obsah složky Nástroje](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="a2d12-121">Chcete-li zobrazit podrobnosti chyby, povolte a zobrazte protokol sledování modulů plug-in v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a2d12-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="a2d12-122">**Požadovaná role pro zapnutí protokolu sledování a zobrazení chyb:** správce systému</span><span class="sxs-lookup"><span data-stu-id="a2d12-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="a2d12-123">Chcete-li zapnout protokol sledování, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="a2d12-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="a2d12-124">Přihlaste se k aplikaci Finance and Operations, otevřete stránku **Nastavení** a v části **Systém** vyberte možnost **Správa**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="a2d12-125">Na stránce **Správa** zvolte **Nastavení systému**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="a2d12-126">Na kartě **Vlastní nastavení** v poli **Modul plug-in a vlastní sledování aktivity workflowu** vyberte možnost **Vše**, chcete-li povolit trasovací protokol modulu plug-in.</span><span class="sxs-lookup"><span data-stu-id="a2d12-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="a2d12-127">Chcete-li protokolovat protokoly trasování pouze při výskytu výjimek, můžete namísto toho vybrat **Výjika**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="a2d12-128">Chcete-li zobrazit protokol sledování, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="a2d12-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="a2d12-129">Přihlaste se k aplikaci Finance and Operations, otevřete stránku **Nastavení** a v části **vlastní nastavení** vyberte možnost **Protokol sledování modulu plug-in**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="a2d12-130">Najděte protokoly sledování, kde pole **Název typu** je nastaveno na **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="a2d12-131">Chcete-li zobrazit úplný protokol, klikněte dvakrát na položku, a potom na pevné záložce **Spuštění** zkontrolujte text **Message Block**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="a2d12-132">Povolit režim ladění pro řešení potíží se živými synchronizacemi v aplikacích Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a2d12-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="a2d12-133">**Požadovaná role pro zobrazení chyb:** správce systému</span><span class="sxs-lookup"><span data-stu-id="a2d12-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="a2d12-134">Chyby dvojího zapisování, které pocházejí z aplikace Common Data Service, se mohou objevit v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a2d12-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="a2d12-135">V některých případech není úplný text chybové zprávy k dispozici, protože zpráva je příliš dlouhá nebo obsahuje osobní identifikační údaje (PII).</span><span class="sxs-lookup"><span data-stu-id="a2d12-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="a2d12-136">Pomocí následujících kroků můžete zapnout podrobné protokolování chyb.</span><span class="sxs-lookup"><span data-stu-id="a2d12-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="a2d12-137">Všechny konfigurace projektu v aplikacích Finance and Operations mají vlastnost **IsDebugMode** v entitě **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="a2d12-138">Otevřete entitu **DualWriteProjectConfiguration** pomocí doplňku aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a2d12-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="a2d12-139">Snadným způsobem, jak tuto entitu otevřít, je zapnout režim **Návrh** v doplňku aplikace Excel a poté přidat **DualWriteProjectConfigurationEntity** do listu.</span><span class="sxs-lookup"><span data-stu-id="a2d12-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="a2d12-140">další informace získáte v tématu [Otevření dat entity v aplikaci Excel a jejich aktualizace pomocí doplňku aplikace Excel](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="a2d12-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="a2d12-141">Nastavte vlastnost **IsDebugMode** na **Ano** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="a2d12-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="a2d12-142">Spuštění scénáře generujících chyby.</span><span class="sxs-lookup"><span data-stu-id="a2d12-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="a2d12-143">Podrobné protokoly jsou k dispozici v tabulce DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="a2d12-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="a2d12-144">Chcete-li vyhledat data v prohlížeči tabulky, použijte následující adresu URL (nahraďte **XXX**):</span><span class="sxs-lookup"><span data-stu-id="a2d12-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="a2d12-145">Zkontrolujte chyby synchronizace ve virtuálním počítači pro aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a2d12-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="a2d12-146">**Požadovaná role pro zobrazení chyb:** správce systému</span><span class="sxs-lookup"><span data-stu-id="a2d12-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="a2d12-147">Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a2d12-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="a2d12-148">Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="a2d12-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="a2d12-149">Zvolte dlaždici **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="a2d12-150">Pomocí vzdálené plochy se přihlaste k virtuálnímu počítači (VM) pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a2d12-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="a2d12-151">Použijte místní účet, který je zobrazen v poli LCS.</span><span class="sxs-lookup"><span data-stu-id="a2d12-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="a2d12-152">Otevřete prohlížeč událostí.</span><span class="sxs-lookup"><span data-stu-id="a2d12-152">Open Event viewer.</span></span>
6. <span data-ttu-id="a2d12-153">Vyberte **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="a2d12-154">Prohlédněte si seznam posledních chyb.</span><span class="sxs-lookup"><span data-stu-id="a2d12-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="a2d12-155">Zrušte propojení a propjte jiné prostředí Common Data Service z aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a2d12-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="a2d12-156">**Požadovaná pověření pro zrušení propojení prostředí:** Správa tenanta Azure AD</span><span class="sxs-lookup"><span data-stu-id="a2d12-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="a2d12-157">Přihlášení do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a2d12-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="a2d12-158">Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="a2d12-159">Vyberte všechna spuštěná mapování a pak vyberte **Zastavit**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="a2d12-160">Zvolte **Odpojit prostředí**.</span><span class="sxs-lookup"><span data-stu-id="a2d12-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="a2d12-161">Vyberte **Ano**, chcete-li potvrdit operaci.</span><span class="sxs-lookup"><span data-stu-id="a2d12-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="a2d12-162">Nyní můžete propojit nové prostředí.</span><span class="sxs-lookup"><span data-stu-id="a2d12-162">You can now link a new environment.</span></span>
