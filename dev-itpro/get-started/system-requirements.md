---
title: "Systémové požadavky pro nasazení cloudu"
description: "Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 for Finance and Operations, edici Enterprise pro nasazení cloudu."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: cs-cz
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="e9409-103">Systémové požadavky pro nasazení cloudu</span><span class="sxs-lookup"><span data-stu-id="e9409-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9409-104">Toto téma obsahuje seznam požadavků na aktuální verzi Microsoft Dynamics 365 for Finance and Operations, edici Enterprise pro nasazení cloudu.</span><span class="sxs-lookup"><span data-stu-id="e9409-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="e9409-105">Před tím, než nainstalujete Finance and Operations, je-li tento krok vhodný, ověřte, že systém se kterým pracujete, splňuje nebo přesahuje minimální požadavky na síť, hardware a software.</span><span class="sxs-lookup"><span data-stu-id="e9409-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="e9409-106">Podporované webové prohlížeče</span><span class="sxs-lookup"><span data-stu-id="e9409-106">Supported web browsers</span></span>
<span data-ttu-id="e9409-107">Webová aplikace může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:</span><span class="sxs-lookup"><span data-stu-id="e9409-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="e9409-108">Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9409-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="e9409-109">Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9409-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="e9409-110">Google Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1, Windows 8, Windows 7 nebo tabletu Google Nexus 10</span><span class="sxs-lookup"><span data-stu-id="e9409-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="e9409-111">Apple Safari (nejnovější veřejně dostupná verze) v systému Mac OS X 10.10 (Yosemite), 10.11 El Capitan) nebo 10.12 (Sierra), nebo Apple iPad</span><span class="sxs-lookup"><span data-stu-id="e9409-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="e9409-112">Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru.</span><span class="sxs-lookup"><span data-stu-id="e9409-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="e9409-113">Musíte nainstalovat předběžnou verzi doplňku Chrome, abyste umožnili záznamníku úloh pořídit snímky obrazovky a zahrnout je do generovaných dokumentů aplikace Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="e9409-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="e9409-114">Editor pracovního postupu je spuštěn jako aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="e9409-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="e9409-115">Aplikace ClickOnce podporují pouze Microsoft Edge and Internet Explorer (v podporované verzi systému Microsoft Windows).</span><span class="sxs-lookup"><span data-stu-id="e9409-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="e9409-116">Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.</span><span class="sxs-lookup"><span data-stu-id="e9409-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="e9409-117">Návrhář sestav pro finanční vykazování je uveden jako aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="e9409-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="e9409-118">Vyžaduje 64bitový kompatibilní operační systém.</span><span class="sxs-lookup"><span data-stu-id="e9409-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="e9409-119">Pokud používáte Chrome, je nutné nainstalovat doplněk ClickOnce, abyste mohli stáhnout klienta Návrháře sestav.</span><span class="sxs-lookup"><span data-stu-id="e9409-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="e9409-120">Pokud používáte Chrome s anonymním režimem, zkontrolujte, zda je povoleno rozšíření ClickOnce pro anonymní režim.</span><span class="sxs-lookup"><span data-stu-id="e9409-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="e9409-121">K zobrazení náhledu souborů PDF doporučujeme používat prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="e9409-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="e9409-122">Podporované webové prohlížeče pro Retail Cloud POS</span><span class="sxs-lookup"><span data-stu-id="e9409-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="e9409-123">Retail Cloud POS může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:</span><span class="sxs-lookup"><span data-stu-id="e9409-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="e9409-124">Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9409-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="e9409-125">Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9409-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="e9409-126">Chrome (nejnovější veřejně dostupná verze) v systému Windows 10, Windows 8.1 nebo Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9409-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="e9409-127">Požadavky na síť</span><span class="sxs-lookup"><span data-stu-id="e9409-127">Network requirements</span></span>
-   <span data-ttu-id="e9409-128">Finance and Operations je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně.</span><span class="sxs-lookup"><span data-stu-id="e9409-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="e9409-129">Tato latence je latence z prohlížeče klienta datového centra Microsoft Azure, který je hostitelem aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9409-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="e9409-130">Doporučujeme otestovat čekací dobu v síti na stránkách <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="e9409-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="e9409-131">Požadavky na šířku pásma pro Finance and Operations závisí na vašem scénáři.</span><span class="sxs-lookup"><span data-stu-id="e9409-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="e9409-132">Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).</span><span class="sxs-lookup"><span data-stu-id="e9409-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="e9409-133">Pro scénáře, které mají vysoké požadavky na zatížení, jako jsou pracovní prostory, nebo scénáře, které obsahují rozsáhlé přizpůsobení, se však doporučuje větší šířka pásma.</span><span class="sxs-lookup"><span data-stu-id="e9409-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="e9409-134">Obecně je aplikace Finance and Operations optimalizována pro Internet.</span><span class="sxs-lookup"><span data-stu-id="e9409-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="e9409-135">Počet opakovaných cest z klienta prohlížeče do datového centra Azure je velmi nízký a celé pracovní zatížení se komprimuje.</span><span class="sxs-lookup"><span data-stu-id="e9409-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="e9409-136">Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma.</span><span class="sxs-lookup"><span data-stu-id="e9409-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="e9409-137">Souběžné využití daného umístění je velmi obtížné vypočítat.</span><span class="sxs-lookup"><span data-stu-id="e9409-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="e9409-138">Zákazníci, kteří mají pochybnosti ohledně požadavků na šířku pásma by měli použít verzi preview aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9409-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="e9409-139">Požadavky systému .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e9409-139">.NET Framework requirements</span></span>
<span data-ttu-id="e9409-140">Finance and Operations vyžaduje rozhraní Microsoft .NET Framework verze 4.6.2 pro všechny aplikace ClickOnce, jako je agent směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="e9409-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="e9409-141">Pokyny k instalaci naleznete v tématu [Instalace rozhraní.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="e9409-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="e9409-142">Podporované aplikace Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="e9409-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="e9409-143">V cloudovém a místním nasazení Finance and Operations jsou podporovány následující aplikace Microsoft Office:</span><span class="sxs-lookup"><span data-stu-id="e9409-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="e9409-144">Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac.</span><span class="sxs-lookup"><span data-stu-id="e9409-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="e9409-145">Další informace o požadavcích na verzi naleznete v tématu [Řešení problémů s integrací se sadou Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="e9409-145">For more information about version requirements, see [Office integration troubleshooting](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span></span>
-   <span data-ttu-id="e9409-146">Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="e9409-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="e9409-147">Požadavky na Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="e9409-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="e9409-148">Pokud Retail Modern POS bude používat offline databázi, počítač musí splňovat všechny požadavky na systém pro aplikaci Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9409-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="e9409-149">Offline databáze Retail Modern POS bude pracovat na serveru Microsoft SQL Server 2012 s aktualizací Service Pack 3 nebo vyšší, Microsoft SQL Server 2014 s aktualizací Service Pack 2 nebo vyšší a Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e9409-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="e9409-150">Doporučujeme vždy použít nejnovější verzi, která je k dispozici, a nainstalovat všechny poslední aktualizace.</span><span class="sxs-lookup"><span data-stu-id="e9409-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="e9409-151">Podporované operační systémy</span><span class="sxs-lookup"><span data-stu-id="e9409-151">Supported operating systems</span></span>

-   <span data-ttu-id="e9409-152">Retail Modern POS je 32bitová aplikace, ale lze ji používat v architektuře x86 a x64.</span><span class="sxs-lookup"><span data-stu-id="e9409-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e9409-153">Retail Modern POS je podporován pouze v edicích Windows 10 Pro, Enterprise a Enterprise Long Term Servicing Branch (LTSB).</span><span class="sxs-lookup"><span data-stu-id="e9409-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e9409-154">Minimální systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="e9409-154">Minimum system requirements</span></span>

-   <span data-ttu-id="e9409-155">Minimální podporované rozlišení je 1280×1024.</span><span class="sxs-lookup"><span data-stu-id="e9409-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="e9409-156">Počítač s Retail Modern POS musí splňovat tyto požadavky:</span><span class="sxs-lookup"><span data-stu-id="e9409-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="e9409-157">Musí mít alespoň dvoujádrový procesor, který se běží při nejméně 2 gigahertzech (GHz).</span><span class="sxs-lookup"><span data-stu-id="e9409-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="e9409-158">Musí mít alespoň 3 gigabajty (GB) paměti RAM.</span><span class="sxs-lookup"><span data-stu-id="e9409-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="e9409-159">Musí mít přístup k Internetu.</span><span class="sxs-lookup"><span data-stu-id="e9409-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="e9409-160">Požadavky na Základní balíček Retail hardware station</span><span class="sxs-lookup"><span data-stu-id="e9409-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="e9409-161">Podporované operační systémy</span><span class="sxs-lookup"><span data-stu-id="e9409-161">Supported operating systems</span></span>

-   <span data-ttu-id="e9409-162">Retail hardware station je 32bitová aplikace, ale lze ji používat v architektuře x86 a x64.</span><span class="sxs-lookup"><span data-stu-id="e9409-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e9409-163">Retail hardware station je podporována v následujících operačních systémech:</span><span class="sxs-lookup"><span data-stu-id="e9409-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="e9409-164">Edice Windows 7 Professional, Enterprise a Ultimate</span><span class="sxs-lookup"><span data-stu-id="e9409-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="e9409-165">Windows 7 jsou podporovány pouze pokud je v systému ručně instalován Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="e9409-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="e9409-166">Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded</span><span class="sxs-lookup"><span data-stu-id="e9409-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="e9409-167">Edice Windows 10 Pro, Enterprise a Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="e9409-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e9409-168">Minimální systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="e9409-168">Minimum system requirements</span></span>

<span data-ttu-id="e9409-169">Počítač musí splňovat všechny požadavky na systém pro instalaci a používání následujících položek:</span><span class="sxs-lookup"><span data-stu-id="e9409-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="e9409-170">Internetová informační služba (IIS)</span><span class="sxs-lookup"><span data-stu-id="e9409-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="e9409-171">Hardware třetí strany</span><span class="sxs-lookup"><span data-stu-id="e9409-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="e9409-172">Požadavky na základní balíček Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="e9409-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="e9409-173">Podporované operační systémy</span><span class="sxs-lookup"><span data-stu-id="e9409-173">Supported operating systems</span></span>

-   <span data-ttu-id="e9409-174">Retail Store Scale Unit je 32bitová aplikace, ale lze ji používat v architektuře x86 a x64.</span><span class="sxs-lookup"><span data-stu-id="e9409-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e9409-175">Retail Store Scale Unit je podporována v následujících operačních systémech:</span><span class="sxs-lookup"><span data-stu-id="e9409-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="e9409-176">Edice Windows 7 Professional, Enterprise a Ultimate</span><span class="sxs-lookup"><span data-stu-id="e9409-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="e9409-177">Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded</span><span class="sxs-lookup"><span data-stu-id="e9409-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="e9409-178">Edice Windows 10 Pro, Enterprise a Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="e9409-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e9409-179">Minimální systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="e9409-179">Minimum system requirements</span></span>

-   <span data-ttu-id="e9409-180">4 GB paměti RAM</span><span class="sxs-lookup"><span data-stu-id="e9409-180">4 GB of RAM</span></span>
-   <span data-ttu-id="e9409-181">1,6 GHz maximální rychlost procesoru na jádro (minimum jsou dvě jádra.)</span><span class="sxs-lookup"><span data-stu-id="e9409-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="e9409-182">Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)</span><span class="sxs-lookup"><span data-stu-id="e9409-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="e9409-183">Doporučené systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="e9409-183">Recommended system requirements</span></span>

-   <span data-ttu-id="e9409-184">6 GB paměti RAM</span><span class="sxs-lookup"><span data-stu-id="e9409-184">6 GB of RAM</span></span>
-   <span data-ttu-id="e9409-185">Procesor s nejvyšší rychlostí CPU 2,4 GHz i7 (nebo ekvivalentní) na jádro (doporučují se čtyři jádra.)</span><span class="sxs-lookup"><span data-stu-id="e9409-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="e9409-186">Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)</span><span class="sxs-lookup"><span data-stu-id="e9409-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="e9409-187">Požadavky na konektor</span><span class="sxs-lookup"><span data-stu-id="e9409-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="e9409-188">Podporované operační systémy</span><span class="sxs-lookup"><span data-stu-id="e9409-188">Supported operating systems</span></span>

-   <span data-ttu-id="e9409-189">Konektor pro aplikaci Microsoft Dynamics AX má dva samostatné instalační programy, jeden pro službu Async Server Connector a jeden pro Real-time service for Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="e9409-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="e9409-190">Obě komponenty jsou 32bitové aplikace, ale lze je používat v architektuře x86 i x64.</span><span class="sxs-lookup"><span data-stu-id="e9409-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e9409-191">Obě součásti jsou podporovány v následujících operačních systémech:</span><span class="sxs-lookup"><span data-stu-id="e9409-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="e9409-192">Edice Windows 7 Professional, Enterprise a Ultimate</span><span class="sxs-lookup"><span data-stu-id="e9409-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="e9409-193">Edice Windows 8.1 Update 1 Professional, Enterprise a Embedded</span><span class="sxs-lookup"><span data-stu-id="e9409-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="e9409-194">Edice Windows 10 Pro, Enterprise a Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="e9409-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="e9409-195">Microsoft Windows Server 2012 R2 a Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e9409-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e9409-196">Minimální systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="e9409-196">Minimum system requirements</span></span>
-   <span data-ttu-id="e9409-197">2 GB RAM paměti (4 GB doporučené paměti RAM)</span><span class="sxs-lookup"><span data-stu-id="e9409-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="e9409-198">1,6 GHz maximální rychlost procesoru na jádro (minimum jsou dvě jádra.)</span><span class="sxs-lookup"><span data-stu-id="e9409-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="e9409-199">Alespoň 10 GB volného místa (databáze kanálu může vyžadovat velké množství místa.)</span><span class="sxs-lookup"><span data-stu-id="e9409-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="e9409-200">Požadavky na vývoj na místních virtuálních počítačích</span><span class="sxs-lookup"><span data-stu-id="e9409-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="e9409-201">Informace o požadavcích na vývoj na místních virtuálních počítačích (VM) naleznete v tématu [místní spuštění virtuálního počítače](../dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="e9409-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="e9409-202">Viz také</span><span class="sxs-lookup"><span data-stu-id="e9409-202">See also</span></span>

[<span data-ttu-id="e9409-203">Získání kopie Dynamics 365 for Finance and Operations, Enterprise edition ve verzi pro hodnocení</span><span class="sxs-lookup"><span data-stu-id="e9409-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

