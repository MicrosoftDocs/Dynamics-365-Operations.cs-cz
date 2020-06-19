---
title: Systémové požadavky
description: Tento článek popisuje požadavky pro Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f68b8f642ada1345e7097b5e7220e222b132b1dd
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431146"
---
# <a name="system-requirements"></a><span data-ttu-id="d8164-103">Systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="d8164-103">System requirements</span></span>

<span data-ttu-id="d8164-104">Tento článek popisuje požadavky pro Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d8164-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d8164-105">Dále jsou zde uvedeny země a oblasti, ve kterých je aplikace Human Resources k dispozici, a informace o jazycích a lokalizaci dat aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d8164-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="d8164-106">Podporované webové prohlížeče</span><span class="sxs-lookup"><span data-stu-id="d8164-106">Supported web browsers</span></span>

<span data-ttu-id="d8164-107">Aplikace Human Resources může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:</span><span class="sxs-lookup"><span data-stu-id="d8164-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="d8164-108">Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10</span><span class="sxs-lookup"><span data-stu-id="d8164-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="d8164-109">Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8164-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="d8164-110">Google Chrome (nejnovější veřejně dostupná verze)</span><span class="sxs-lookup"><span data-stu-id="d8164-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="d8164-111">Apple Safari (nejnovější veřejně dostupná verze)</span><span class="sxs-lookup"><span data-stu-id="d8164-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="d8164-112">Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru.</span><span class="sxs-lookup"><span data-stu-id="d8164-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="d8164-113">K zachycení bitových kopií, které jsou generovány ze Záznamníku úkolů a jejich zahrnutí do dokumentů aplikace Microsoft Word, musíte mít nainstalováno rozšíření Chrome.</span><span class="sxs-lookup"><span data-stu-id="d8164-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="d8164-114">Editor pracovního postupu je spuštěn jako aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="d8164-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="d8164-115">Pouze Microsoft Edge a Internet Explorer (podporované verze Microsoft Windows) podporují aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="d8164-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="d8164-116">Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.</span><span class="sxs-lookup"><span data-stu-id="d8164-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="d8164-117">K zobrazení náhledu souborů PDF doporučujeme používat moderní prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="d8164-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="d8164-118">Požadavky na síť</span><span class="sxs-lookup"><span data-stu-id="d8164-118">Network requirements</span></span>
> * <span data-ttu-id="d8164-119">Human Resources je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně.</span><span class="sxs-lookup"><span data-stu-id="d8164-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="d8164-120">Tato latence představuje latenci z prohlížeče do datového centra Microsoft Azure, které hostuje aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d8164-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="d8164-121">Doporučujeme otestovat čekací dobu v síti na stránkách [www.azurespeed.com](https://www.azurespeed.com "Test latence Azure").</span><span class="sxs-lookup"><span data-stu-id="d8164-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="d8164-122">Požadavky na šířku pásma pro Human Resources závisí na daném scénáři.</span><span class="sxs-lookup"><span data-stu-id="d8164-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="d8164-123">Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).</span><span class="sxs-lookup"><span data-stu-id="d8164-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="d8164-124">Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma.</span><span class="sxs-lookup"><span data-stu-id="d8164-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="d8164-125">Souběžné využití daného umístění je velmi obtížné vypočítat.</span><span class="sxs-lookup"><span data-stu-id="d8164-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="d8164-126">Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d8164-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="d8164-127">Podporované aplikace Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="d8164-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="d8164-128">Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac.</span><span class="sxs-lookup"><span data-stu-id="d8164-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="d8164-129">Další informace o požadavcích na verzi naleznete v tématu [řešení problémů s integrací se sadou Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací s Office").</span><span class="sxs-lookup"><span data-stu-id="d8164-129">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="d8164-130">Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="d8164-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="d8164-131">Regionální dostupnost, jazyky a lokalizace</span><span class="sxs-lookup"><span data-stu-id="d8164-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="d8164-132">Můžete si stáhnout PDF soubor se zeměmi, oblastmi a jazyky, které Human Resources podporuje, na [Mezinárodní dostupnosti Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="d8164-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="d8164-133">Zatímco je uživatelské rozhraní lokalizováno do jiných jazyků, budou všechna uživatelská data uložena v jazyce, ve kterém byla zadána.</span><span class="sxs-lookup"><span data-stu-id="d8164-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="d8164-134">E-maily a šablony můžete vytvářet v jiných jazycích, ale data jako informace o plánování budou v tomto okamžiku k dispozici pouze v angličtině.</span><span class="sxs-lookup"><span data-stu-id="d8164-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="d8164-135">Pokud jste vývojáři a máte zájem o vytváření vlastních nastavení specifických pro zemi nebo oblast, nebo o vytváření řešení pro zemi nebo oblast, která není aktuálně podporována společností Microsoft, prohlédněte si část [Globalizace](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="d8164-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>
