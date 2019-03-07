---
title: Project Service Automation
description: Toto téma poskytuje informace o řešení integrace Project Service Automation do Finance and Operations. Toto integrační řešení používá funkci integrace dat a synchronizaci dat mezi instancemi Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation prostřednictvím Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "335685"
---
# <a name="project-service-automation"></a><span data-ttu-id="6ad0b-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6ad0b-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6ad0b-105">Integrační řešení Project Service Automation to Finance and Operations používá funkci Integrace dat k synchronizaci dat napříč instancemi Microsoft Dynamics 365 for Finance and Operations a Microsoft Dynamics 365 for Project Service Automation prostřednictvím Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="6ad0b-106">Šablony integrace, které jsou k dispozici s funkcí integrace dat povolují tok projektů, projektové smlouvy, řádky smlouvy projektu, milníky řádků smlouvy projektu, úlohy projektu, kategorie transakcí výdajů, odhady hodin, a odhady výdajů z aplikace Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="6ad0b-107">Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="6ad0b-108">Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="6ad0b-109">Pokud používáte Finance and Operations 7.3.0, je nutné nainstalovat KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="6ad0b-110">Poté budete schopni integrovat projekty s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="6ad0b-111">Pokud používáte Finance and Operations 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, aby byly tyto poplatky zahrnuty ve faktuře projektu.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="6ad0b-112">Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0, budete moci používat integraci úkolů projektu, kategorie výdajových transakcí, odhady času, odhady výdajů a uzamknutí funkčnosti.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="6ad0b-113">Pokud používáte Microsoft Dynamics 365 for Finance and Operations verze 8.0.1, nebo novější, budete moci synchronizovat skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="6ad0b-114">Než budete moci integrovat Project Service Automation s Finance and Operations, musíte nakonfigurovat parametry Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="6ad0b-115">Další informace naleznete v tématu [Parametry integrace Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ad0b-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="6ad0b-116">Toto řešení integrace umožňuje přímou synchronizaci v následujících scénářích:</span><span class="sxs-lookup"><span data-stu-id="6ad0b-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="6ad0b-117">Při správě projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-118">Při vytváření projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-119">Při správě řádků projektových smluv v Project Service Automation a jeijch přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-120">Při správě milníků řádků projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-121">Při správě projektových úloh v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-122">Při správě kategorií transakcí výdajů v Finance and Operations a jejich přímé synchronizaci z Finance and Operations do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="6ad0b-123">Při vytváření odhadu projektových hodin v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-124">Při vytváření odhadu projektových výdajů v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6ad0b-125">Při vytváření času projektu, výdajů a skutečných hodnot poplatků v Project Service Automation a při vytváření transakcí projektu v deníku integrace Project Service Automation, aby mohly být zaúčtovány v Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="6ad0b-126">Synchronizace dat</span><span class="sxs-lookup"><span data-stu-id="6ad0b-126">Data synchronization</span></span>

<span data-ttu-id="6ad0b-127">Následující obrázek znázorňuje, jak jsou synchronizována data jako součást Integrace mezi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="6ad0b-128">Ne všechny šablony jsou momentálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-128">Not all templates are currently available.</span></span> <span data-ttu-id="6ad0b-129">Šablony budou uvolňovány při jejich dokončení.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="6ad0b-130">[![Integrace Project Service Automation s aplikací Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="6ad0b-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="6ad0b-131">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6ad0b-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="6ad0b-132">Pokud chcete používat integrační řešení Project Service Automation to Finance and Operations, musíte si nainstalovat Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 s aktualizací platformy 12 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="6ad0b-133">Požadavky na systém pro Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6ad0b-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="6ad0b-134">Chcete-li použít řešení integrace Project Service Automation do Finance and Operations, musíte si nainstalovat následující součásti:</span><span class="sxs-lookup"><span data-stu-id="6ad0b-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="6ad0b-135">Microsoft Dynamics 365 for Project Service Automation verze 9.0.0.0 nebo novější</span><span class="sxs-lookup"><span data-stu-id="6ad0b-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="6ad0b-136">Řešení zpeněžení potenciálního zákazníka pro Microsoft Dynamics 365 for Sales, verze 1.14.0.0 (v14) nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="6ad0b-137">Integrační řešení Project Service Automation to Finance and Operations pro Microsoft Dynamics 365 for Project Service Automation verze 1.0.0.0 nebo pozdější</span><span class="sxs-lookup"><span data-stu-id="6ad0b-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="6ad0b-138">Nainstalujte řešení integrace Project Service Automation do Finance and Operations do své instance Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6ad0b-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="6ad0b-139">Stáhněte si řešení integrace Project Service Automation do Finance and Operations z [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016) a postupujte podle pokynů, které jsou součástí řešení.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
