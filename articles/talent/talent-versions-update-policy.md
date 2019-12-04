---
title: Systémové požadavky aplikace Talent
description: Toto téma obsahuje požadavky na Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
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
ms.openlocfilehash: 0bd7d7051dd01834f306e165af55d740192b99e0
ms.sourcegitcommit: caeb24027831efccbc316ff8e7f9e62b42010d65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/19/2019
ms.locfileid: "2818472"
---
# <a name="talent-system-requirements"></a><span data-ttu-id="ba359-103">Systémové požadavky aplikace Talent</span><span class="sxs-lookup"><span data-stu-id="ba359-103">Talent system requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba359-104">V tomto tématu jsou popsány požadavky pro aplikaci Microsoft Dynamics 365 Talent, včetně aplikací Attract, Onboard a Core HR.</span><span class="sxs-lookup"><span data-stu-id="ba359-104">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="ba359-105">Dále jsou zde uvedeny země a oblasti, ve kterých je Talent k dispozici, a informace o jazycích a lokalizaci dat aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="ba359-105">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="ba359-106">Navíc toto téma obsahuje zásady aktualizace pro aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="ba359-106">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="ba359-107">Podporované webové prohlížeče</span><span class="sxs-lookup"><span data-stu-id="ba359-107">Supported web browsers</span></span>

<span data-ttu-id="ba359-108">Aplikace Microsoft Dynamics 365 Talent může běžet v kterémkoli z následujících webových prohlížečů v určeném operačním systému:</span><span class="sxs-lookup"><span data-stu-id="ba359-108">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="ba359-109">Microsoft Edge (nejnovější veřejně dostupná verze) v systému Windows 10</span><span class="sxs-lookup"><span data-stu-id="ba359-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="ba359-110">Internet Explorer 11 v systému Windows 10, Windows 8.1 nebo Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba359-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="ba359-111">Google Chrome (nejnovější veřejně dostupná verze)</span><span class="sxs-lookup"><span data-stu-id="ba359-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="ba359-112">Apple Safari (nejnovější veřejně dostupná verze)</span><span class="sxs-lookup"><span data-stu-id="ba359-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="ba359-113">Poslední verzi pro každý webový prohlížeč naleznete na webu výrobce softwaru.</span><span class="sxs-lookup"><span data-stu-id="ba359-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="ba359-114">K zachycení bitových kopií, které jsou generovány ze Záznamníku úkolů a jejich zahrnutí do dokumentů aplikace Microsoft Word, musíte mít nainstalováno rozšíření Chrome.</span><span class="sxs-lookup"><span data-stu-id="ba359-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="ba359-115">Editor pracovního postupu je spuštěn jako aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="ba359-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="ba359-116">Pouze Microsoft Edge a Internet Explorer (podporované verze Microsoft Windows) podporují aplikace ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="ba359-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="ba359-117">Editor pracovního postupu aplikace ClickOnce vyžaduje 64bitový kompatibilní operační systém.</span><span class="sxs-lookup"><span data-stu-id="ba359-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="ba359-118">K zobrazení náhledu souborů PDF doporučujeme používat moderní prohlížeče, jako je Microsoft Edge (nejnovější veřejně dostupnou verzi) na operačním systému Windows 10, nebo Google Chrome (nejnovější veřejně dostupnou verzi) na operačních systémech Windows 10, Windows 8.1, Windows 8, Windows 7 nebo na tabletu Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="ba359-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="ba359-119">Požadavky na síť</span><span class="sxs-lookup"><span data-stu-id="ba359-119">Network requirements</span></span>
> * <span data-ttu-id="ba359-120">Dynamics 365 Talent je navržena pro sítě s latencí 250 - 300 milisekund (ms) nebo méně.</span><span class="sxs-lookup"><span data-stu-id="ba359-120">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="ba359-121">Tato latence představuje latenci z prohlížeče do datového centra Microsoft Azure, které hostuje aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="ba359-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="ba359-122">Doporučujeme otestovat čekací dobu v síti na stránkách [www.azurespeed.com](https://www.azurespeed.com "Test latence Azure").</span><span class="sxs-lookup"><span data-stu-id="ba359-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="ba359-123">Požadavky na šířku pásma pro Talent závisí na danému scénáři.</span><span class="sxs-lookup"><span data-stu-id="ba359-123">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="ba359-124">Některé běžné scénáře vyžadují šířku pásma větší než 50 kilobajtů za sekundu (kb/s).</span><span class="sxs-lookup"><span data-stu-id="ba359-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="ba359-125">Nepočítejte požadavky na šířku pásma z klientského umístění tím, že vynásobíte počet uživatelů minimálními požadavky na šířku pásma.</span><span class="sxs-lookup"><span data-stu-id="ba359-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="ba359-126">Souběžné využití daného umístění je velmi obtížné vypočítat.</span><span class="sxs-lookup"><span data-stu-id="ba359-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="ba359-127">Pro zákazníky, kteří mají pochybnosti ohledně požadavků na šířku pásma, použijte zkušební verzi aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="ba359-127">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="ba359-128">Podporované aplikace Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="ba359-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="ba359-129">Chcete-li používat doplňky aplikace Microsoft Excel a Word, musíte mít nainstalovanou sadu Microsoft Office 2016 pro Windows nebo Mac.</span><span class="sxs-lookup"><span data-stu-id="ba359-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="ba359-130">Další informace o požadavcích na verzi naleznete v tématu [řešení problémů s integrací se sadou Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Řešení problémů s integrací s Office").</span><span class="sxs-lookup"><span data-stu-id="ba359-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="ba359-131">Chcete-li zobrazit dokumenty, které jsou generovány pomocí funkce exportu do aplikace Excel nebo Word funkce, musíte mít nainstalovanou sadu Microsoft Office 2007 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="ba359-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="ba359-132">Regionální dostupnost, jazyky a lokalizace</span><span class="sxs-lookup"><span data-stu-id="ba359-132">Regional availability, languages, and localization</span></span>

<span data-ttu-id="ba359-133">Můžete si stáhnout PDF soubor se zeměmi, oblastmi a jazyky, které Talent podporuje, na [Mezinárodní dostupnosti Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="ba359-133">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="ba359-134">Zatímco je uživatelské rozhraní lokalizováno do jiných jazyků, budou všechna uživatelská data uložena v jazyce, ve kterém byla zadána.</span><span class="sxs-lookup"><span data-stu-id="ba359-134">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="ba359-135">E-maily a šablony můžete vytvářet v jiných jazycích, ale data jako informace o plánování budou v tomto okamžiku k dispozici pouze v angličtině.</span><span class="sxs-lookup"><span data-stu-id="ba359-135">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="ba359-136">Pokud jste vývojáři a máte zájem o vytváření vlastních nastavení specifických pro zemi nebo oblast, nebo o vytváření řešení pro zemi nebo oblast, která není aktuálně podporována společností Microsoft, prohlédněte si část [Globalizace](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="ba359-136">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

