---
title: Systémové požadavky aplikace Talent a zásady aktualizace
description: Toto téma obsahuje požadavky na Dynamics 365 for Talent. Jsou zde také popsány zásady aktualizací.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2389f00b22ec3b5284eeffb2c015533b7a3d13e0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "856294"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="6efe3-104">Systémové požadavky aplikace Talent a zásady aktualizace</span><span class="sxs-lookup"><span data-stu-id="6efe3-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6efe3-105">Toto téma obsahuje požadavky na Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="6efe3-105">This topic lists requirements for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="6efe3-106">Jsou zde také popsány zásady aktualizací.</span><span class="sxs-lookup"><span data-stu-id="6efe3-106">The update policy is outlined, as well.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="6efe3-107">Podporované webové prohlížeče</span><span class="sxs-lookup"><span data-stu-id="6efe3-107">Supported web browsers</span></span>

<span data-ttu-id="6efe3-108">Webová aplikace Microsoft Dynamics 365 for Talent může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:</span><span class="sxs-lookup"><span data-stu-id="6efe3-108">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="6efe3-109">Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10</span><span class="sxs-lookup"><span data-stu-id="6efe3-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="6efe3-110">Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7</span><span class="sxs-lookup"><span data-stu-id="6efe3-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="6efe3-111">Google Chrome (nejnovější veřejně dostupná verze)</span><span class="sxs-lookup"><span data-stu-id="6efe3-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="6efe3-112">Apple Safari (nejnovější veřejně dostupná verze)</span><span class="sxs-lookup"><span data-stu-id="6efe3-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="6efe3-113">Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru.</span><span class="sxs-lookup"><span data-stu-id="6efe3-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="6efe3-114">K zachycení bitových kopií, které jsou generovány ze Záznamníku úkolů a jejich zahrnutí do dokumentů aplikace Microsoft Word, musíte mít nainstalováno rozšíření Chrome.</span><span class="sxs-lookup"><span data-stu-id="6efe3-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="6efe3-115">Editor pracovního postupu je spuštěn jako aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="6efe3-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="6efe3-116">Pouze Microsoft Edge a Internet Explorer (podporované verze Microsoft Windows) podporují aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="6efe3-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="6efe3-117">Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.</span><span class="sxs-lookup"><span data-stu-id="6efe3-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="6efe3-118">K zobrazení náhledu souborů PDF doporučujeme používat moderní prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="6efe3-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="6efe3-119">Požadavky na síť</span><span class="sxs-lookup"><span data-stu-id="6efe3-119">Network requirements</span></span>
> * <span data-ttu-id="6efe3-120">Dynamics 365 for Talent je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně.</span><span class="sxs-lookup"><span data-stu-id="6efe3-120">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="6efe3-121">Tato latence představuje latenci z prohlížeče do datového centra Microsoft Azure, které hostuje Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="6efe3-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="6efe3-122">Doporučujeme otestovat latenci sítě na stránkách [www.azurespeed.com](https://www.azurespeed.com "Test latence Azure").</span><span class="sxs-lookup"><span data-stu-id="6efe3-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="6efe3-123">Požadavky na šířku pásma pro Dynamics 365 for Talent závisí na danému scénáři.</span><span class="sxs-lookup"><span data-stu-id="6efe3-123">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="6efe3-124">Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).</span><span class="sxs-lookup"><span data-stu-id="6efe3-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="6efe3-125">Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma.</span><span class="sxs-lookup"><span data-stu-id="6efe3-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="6efe3-126">Souběžné využití daného umístění je velmi obtížné vypočítat.</span><span class="sxs-lookup"><span data-stu-id="6efe3-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="6efe3-127">Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="6efe3-127">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="6efe3-128">Podporované aplikace Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="6efe3-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="6efe3-129">Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac.</span><span class="sxs-lookup"><span data-stu-id="6efe3-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="6efe3-130">Další informace o požadavcích na verzi naleznete v tématu [Řešení problémů s integrací se sadou Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací se sadou Office").</span><span class="sxs-lookup"><span data-stu-id="6efe3-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="6efe3-131">Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="6efe3-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="update-policy"></a><span data-ttu-id="6efe3-132">Zásady aktualizace</span><span class="sxs-lookup"><span data-stu-id="6efe3-132">Update policy</span></span>

<span data-ttu-id="6efe3-133">Microsoft Dynamics 365 for Talent využívá služby jako cloudová nabídka.</span><span class="sxs-lookup"><span data-stu-id="6efe3-133">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="6efe3-134">Aktualizace pro aplikaci Dynamics 365 for Talent jsou nepřetržité a automaticky aplikované společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6efe3-134">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="6efe3-135">Aktualizace jsou vydávány v pravidelných intervalech a použijí se na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="6efe3-135">Updates are released on a regular cadence, updates will be made to all environments.</span></span>  <span data-ttu-id="6efe3-136">Dynamics 365 for Talent je podporována podle [zásad správy cyklu životnosti podpory Microsoft](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Cyklus životnosti podpory Microsoft"), které poskytují konzistentní a předvídatelné pokyny pro dostupnost podpory produktu.</span><span class="sxs-lookup"><span data-stu-id="6efe3-136">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
