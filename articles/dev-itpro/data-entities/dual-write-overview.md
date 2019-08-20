---
title: Integrace dat téměř v reálném čase mezi aplikací Finance and Operations a Common Data Service
description: Toto téma poskytuje přehled integrace mezi Microsoft Dynamics 365 for Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797221"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="d0206-103">Integrace dat téměř v reálném čase mezi aplikací Finance and Operations a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d0206-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="d0206-104">V současném digitálním světě používají podnikatelské ekosystémy sadu Microsoft Dynamics 365 jako celek.</span><span class="sxs-lookup"><span data-stu-id="d0206-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="d0206-105">Protože data od osob, zákazníků, operací a zařízení s internetem věcí (IoT) proudí do jednoho zdroje, existuje příležitost pro digitální smyčky zpětné vazby.</span><span class="sxs-lookup"><span data-stu-id="d0206-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="d0206-106">Pro dosažení těchto zkušeností je nezbytná integrace mezi aplikacemi Dynamics 365 for Finance and Operations a Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d0206-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="d0206-107">Aplikace Customer Engagement jsou postaveny nad službou Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d0206-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="d0206-108">Integrace mezi daty Finance and Operations a Common Data Service umožňuje aplikacím Customer Engagement komunikovat vzájemně a plynně s aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d0206-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="d0206-109">Finance and Operations a Common Data Service poskytují synchronizaci dat téměř v reálném čase mezi aplikacemi Finance and Operations a Customer Engagement prostřednictvím rámce pro dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="d0206-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="d0206-110">Pokrytí je široké a pokrývá 28 povrchových oblastí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d0206-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="d0206-111">Cílem je poskytnout uživateli jednu zkušenost s Dynamics 365 pomocí plynulých datových toků, které spojují obchodní procesy mezi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="d0206-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Diagram přehledu architektury](media/dual-write-overview.jpg)

<span data-ttu-id="d0206-113">Pro zákazníky jsou k dispozici následující propozice hodnot:</span><span class="sxs-lookup"><span data-stu-id="d0206-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="d0206-114">Organizační hierarchie v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d0206-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="d0206-115">Koncept společnosti v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d0206-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="d0206-116">Integrovaná hlavní data odběratelů</span><span class="sxs-lookup"><span data-stu-id="d0206-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="d0206-117">Integrovaná hlavní data dodavatelů</span><span class="sxs-lookup"><span data-stu-id="d0206-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="d0206-118">Sjednocený hlavní produkt</span><span class="sxs-lookup"><span data-stu-id="d0206-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="d0206-119">Systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="d0206-119">System requirements</span></span>

<span data-ttu-id="d0206-120">Synchronní, obousměrný datový tok téměř v reálném čase vyžaduje následující verze:</span><span class="sxs-lookup"><span data-stu-id="d0206-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="d0206-121">Microsoft Dynamics 365 for Finance and Operations verze 10.0.4 (července 2019) s aktualizací Platform Update 28 nebo vyšší</span><span class="sxs-lookup"><span data-stu-id="d0206-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="d0206-122">Microsoft Dynamics 365 for Customer Engagement verze Platform 9.1 (4.2) nebo novější</span><span class="sxs-lookup"><span data-stu-id="d0206-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="d0206-123">Nastavit instrukce</span><span class="sxs-lookup"><span data-stu-id="d0206-123">Setup instructions</span></span>

<span data-ttu-id="d0206-124">Pro nastavení integrace mezi aplikací Finance and Operations a Common Data Service postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="d0206-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="d0206-125">Chcete-li nastavit systém s dvojím zápisem, přečtěte si [podrobný návod](https://aka.ms/dualwrite-docs) k oznámení verze Preview dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="d0206-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="d0206-126">Stáhněte a nainstalujte řešení ze skupiny [integrace Finance and Operations, Common Data Service a Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer</span><span class="sxs-lookup"><span data-stu-id="d0206-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="d0206-127">Balíček obsahuje pět řešení:</span><span class="sxs-lookup"><span data-stu-id="d0206-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="d0206-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="d0206-128">Dynamics365Company</span></span>
    + <span data-ttu-id="d0206-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="d0206-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="d0206-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="d0206-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="d0206-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="d0206-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="d0206-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="d0206-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="d0206-133">Postupujte podle pořadí provádění pro [synchronizaci počátečních referenčních dat](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="d0206-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="d0206-134">Setkáte-li se s problémy se synchronizací dvojího zápisu, nahlédněte do [Poradce při potížích s integrací dat](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="d0206-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0206-135">Vedle sebe nelze spustit dvojí zápis a [zpeněžení potenciálního zákazníka](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="d0206-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="d0206-136">Pokud spouštíte řešení zpeněžení potenciálního zákazníka, je nutné jej odinstalovat.</span><span class="sxs-lookup"><span data-stu-id="d0206-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="d0206-137">Musíte také zakázat šablony dvojího zápisu zákazníků a dodavatelů, které jsou součástí řešení zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="d0206-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
