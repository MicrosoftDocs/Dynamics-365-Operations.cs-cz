---
title: "Obnovení datového tržiště finančního vykazování po obnovení databáze"
description: "Toto téma popisuje, jak obnovit datový trh finančního výkaznictví po obnovení databázeMicrosoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="b4d36-103">Obnovení datového tržiště finančního vykazování po obnovení databáze</span><span class="sxs-lookup"><span data-stu-id="b4d36-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b4d36-104">Toto téma popisuje, jak obnovit datový trh finančního výkaznictví po obnovení databázeMicrosoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b4d36-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="b4d36-105">Pokud někdy obnovíte databázi Finance and Operations ze zálohy nebo zkopírujete databázi z jiného prostředí, musíte postupovat podle kroků v tomto tématu, chcete-li zajistit, aby datové tržiště finančního vykazování správně používalo obnovenou databázi aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b4d36-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="b4d36-106">Kroky v tomto procesu jsou podporovány pro vydání aplikace Dynamics 365 for Operations z května 2016 release (sestavení aplikace 7.0.1265.23014 a sestavení finančního výkaznictví 7.0.10000.4) a novější verze.</span><span class="sxs-lookup"><span data-stu-id="b4d36-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="b4d36-107">Pokud máte dřívější verzi aplikace Finance and Operations, obraťte se na náš tým podpory pro pomoc.</span><span class="sxs-lookup"><span data-stu-id="b4d36-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="b4d36-108">Export definicí sestav</span><span class="sxs-lookup"><span data-stu-id="b4d36-108">Export report definitions</span></span>
<span data-ttu-id="b4d36-109">Nejprve exportujte návrhy sestavy z Návrháře sestav pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="b4d36-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="b4d36-110">V Návrháři sestav přejděte na **Společnost** &gt; **Skupiny stavebních bloků**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="b4d36-111">Vyberte skupinu stavebních bloků k exportu a klepněte na tlačítko **Export**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="b4d36-112">V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="b4d36-113">Vyberte definice sestavy k exportu:</span><span class="sxs-lookup"><span data-stu-id="b4d36-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="b4d36-114">Pokud chcete exportovat všechny definice sestavy a přidružené stavební bloky, klikněte na tlačítko **Vybrat vše**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="b4d36-115">Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, klikněte na příslušnou kartu a vyberte položky k exportu.</span><span class="sxs-lookup"><span data-stu-id="b4d36-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="b4d36-116">Stisknutím a podržením klávesy Ctrl vyberte více položek na kartě. Při výběru sestav, které chcete exportovat, jsou vybrány přidružené řádky, sloupce, stromy a sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b4d36-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="b4d36-117">Klikněte na **Exportovat**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-117">Click **Export**.</span></span>
5.  <span data-ttu-id="b4d36-118">Zadejte název souboru a vyberte bezpečné místo, kam chcete uložit exportované definice sestavy.</span><span class="sxs-lookup"><span data-stu-id="b4d36-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="b4d36-119">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-119">Click **Save**.</span></span>

<span data-ttu-id="b4d36-120">Soubor lze zkopírovat nebo nahrát do bezpečného umístění, odkud ho lze později importovat do jiného prostředí.</span><span class="sxs-lookup"><span data-stu-id="b4d36-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="b4d36-121">Informace o použití účtu úložiště Microsoft Azure naleznete v části [Přenos dat pomocí nástroje příkazového řádku AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="b4d36-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="b4d36-122">Microsoft neposkytuje úložiště účtu v rámci vaší smlouvy na aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b4d36-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="b4d36-123">Musíte zakoupit účet úložiště nebo použít účet úložiště ze samostatného předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d36-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="b4d36-124">Musíte znát chování jednotky D na Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="b4d36-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="b4d36-125">Nenechávejte zde exportované stavební skupiny trvale.</span><span class="sxs-lookup"><span data-stu-id="b4d36-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="b4d36-126">Další informace o dočasných jednotkách viz [Principy dočasné jednotky na Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="b4d36-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="b4d36-127">Ukončení služeb</span><span class="sxs-lookup"><span data-stu-id="b4d36-127">Stop services</span></span>
<span data-ttu-id="b4d36-128">Pomocí připojení ke vzdálené ploše se připojte ke všem počítačům v prostředí a zastavte následující služby systému Windows pomocí services.msc:</span><span class="sxs-lookup"><span data-stu-id="b4d36-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="b4d36-129">World wide web publishing service (na všech počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="b4d36-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="b4d36-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="b4d36-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="b4d36-131">Management Reporter 2012 Process Service (pouze v počítačích BI)</span><span class="sxs-lookup"><span data-stu-id="b4d36-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="b4d36-132">Tyto služby mají otevřené připojení k databázi Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b4d36-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="b4d36-133">Resetovat</span><span class="sxs-lookup"><span data-stu-id="b4d36-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="b4d36-134">Vyhledejte a stáhněte nejnovější balíček MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="b4d36-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="b4d36-135">Vyhledejte nejnovější balíček MinorVersionDataUpgrade.zip pomocí pokynů v části [Stažení nejnovějšího nasaditelného balíčku pro upgrade dat](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="b4d36-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="b4d36-136">Pokyny vysvětlují, jak najít a stáhnout správnou verzi balíčku pro upgradování dat.</span><span class="sxs-lookup"><span data-stu-id="b4d36-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="b4d36-137">Upgrade ke stažení balíčku MinorVersionDataUpgrade.zip není vyžadován.</span><span class="sxs-lookup"><span data-stu-id="b4d36-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="b4d36-138">Je zapotřebí dokončit kroky v části "Stažení nejnovějšího nasaditelného balíčku pro upgrade dat" bez provedení jakýchkoliv dalších kroků v článku pro načtení kopie balíčku MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="b4d36-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="b4d36-139">Spuštění skriptů proti databázi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b4d36-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="b4d36-140">Spusťte následující skripty proti databázi Finance and Operations (nikoli proti databázi finančního výkaznictví).</span><span class="sxs-lookup"><span data-stu-id="b4d36-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="b4d36-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="b4d36-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="b4d36-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="b4d36-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="b4d36-143">Tyto skripty zkontrolujte správnost uživatelů, rolí a nastavení sledování změn.</span><span class="sxs-lookup"><span data-stu-id="b4d36-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="b4d36-144">Chcete-li obnovit databázi, spusťte příkaz prostředí PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4d36-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="b4d36-145">V počítači AOS spusťte následující příkazy v nástroji PowerShell jako správce pro obnovení integrace mezi aplikací Finance and Operations a finančním výkaznictvím.</span><span class="sxs-lookup"><span data-stu-id="b4d36-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="b4d36-146">Po vykonání příkazu se zobrazí výzva k zadání Y pro potvrzení.</span><span class="sxs-lookup"><span data-stu-id="b4d36-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="b4d36-147">Vysvětlení parametrů:</span><span class="sxs-lookup"><span data-stu-id="b4d36-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="b4d36-148">Platné hodnoty parametru  -Reason jsou: SERVIS, CHYBNÁ DATA, JINÉ</span><span class="sxs-lookup"><span data-stu-id="b4d36-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="b4d36-149">Parametr -ReasonDetail je textový.</span><span class="sxs-lookup"><span data-stu-id="b4d36-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="b4d36-150">Parametry reason a reasonDetail budou zaznamenány ve sledování telemetrie/prostředí.</span><span class="sxs-lookup"><span data-stu-id="b4d36-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="b4d36-151">Spuštění služeb</span><span class="sxs-lookup"><span data-stu-id="b4d36-151">Start services</span></span>
<span data-ttu-id="b4d36-152">Pomocí services.msc restartujte dříve zastavené služby:</span><span class="sxs-lookup"><span data-stu-id="b4d36-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="b4d36-153">World wide web publishing service (na všech počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="b4d36-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="b4d36-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="b4d36-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="b4d36-155">Management Reporter 2012 Process Service (pouze v počítačích BI)</span><span class="sxs-lookup"><span data-stu-id="b4d36-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="b4d36-156">Import definicí sestav</span><span class="sxs-lookup"><span data-stu-id="b4d36-156">Import report definitions</span></span>
<span data-ttu-id="b4d36-157">Importujte návrhy sestavy z Návrháře sestav pomocí souboru vytvořeného během exportu:</span><span class="sxs-lookup"><span data-stu-id="b4d36-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="b4d36-158">V Návrháři sestav přejděte na **Společnost** &gt; **Skupiny stavebních bloků**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="b4d36-159">Vyberte skupinu stavebních bloků k exportu a klepněte na tlačítko **Export**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="b4d36-160">V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="b4d36-161">Vyberte stavební blok **Výchozí** a klikněte na **Import**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="b4d36-162">Vyberte soubor obsahující definice exportované sestavy a klepněte na tlačítko **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="b4d36-163">V dialogovém okně Import vyberte definice sestavy k importu:</span><span class="sxs-lookup"><span data-stu-id="b4d36-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="b4d36-164">Pokud chcete importovat všechny definice sestavy a podpůrné stavební bloky, klikněte na tlačítko **Vybrat vše**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="b4d36-165">Chcete-li importovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, vyberte sestavy, řádky, sloupce, stromy a sady dimenzí k importu.</span><span class="sxs-lookup"><span data-stu-id="b4d36-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="b4d36-166">Klepněte na tlačítko **Import**.</span><span class="sxs-lookup"><span data-stu-id="b4d36-166">Click **Import**.</span></span>





