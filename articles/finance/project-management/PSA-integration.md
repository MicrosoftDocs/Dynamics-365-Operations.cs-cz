---
title: Přehled Project Service Automation
description: Toto téma obsahuje informace o řešení integrace Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250546"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="ff6cd-103">Přehled Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff6cd-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ff6cd-104">Řešení integrace Project Service Automation do Finance and Operations používá funkci Integrace dat k synchronizaci dat napříč instancemi Dynamics 365 Finance a Dynamics 365 Project Service Automation prostřednictvím Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="ff6cd-105">Šablony integrace, které jsou k dispozici s funkcí integrace dat povolují tok projektů, projektové smlouvy, řádky smlouvy projektu, milníky řádků smlouvy projektu, úlohy projektu, kategorie transakcí výdajů, odhady hodin, a odhady výdajů z aplikace Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ff6cd-106">Pokud používáte 7.3.0, je nutné nainstalovat KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="ff6cd-107">Poté budete schopni integrovat projekty s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="ff6cd-108">Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, aby byly tyto poplatky zahrnuty ve faktuře projektu.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="ff6cd-109">Pokud používáte verzi 8.0, budete moci používat integraci úkolů projektu, kategorie výdajových transakcí, odhady času, odhady výdajů a uzamknutí funkčnosti.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="ff6cd-110">Pokud používáte verzi 8.0.1 nebo novější, budete moci synchronizovat skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="ff6cd-111">Než budete moci integrovat Project Service Automation s Finance, musíte nakonfigurovat parametry Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="ff6cd-112">Další informace naleznete v tématu [Parametry integrace Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ff6cd-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="ff6cd-113">Toto řešení integrace umožňuje přímou synchronizaci v následujících scénářích:</span><span class="sxs-lookup"><span data-stu-id="ff6cd-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="ff6cd-114">Při správě projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-115">Při vytváření projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-116">Při správě řádek projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-117">Při správě milníků řádek projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-118">Při správě projektových úkolů v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-119">Při správě kategorií transakcí výdajů ve Finance a jejich přímé synchronizaci z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="ff6cd-120">Při vytváření odhadu projektových hodin v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-121">Při vytváření odhadu projektových výdajů v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ff6cd-122">Při vytváření času projektu, výdajů a skutečných hodnot poplatků v Project Service Automation a při vytváření transakcí projektu v deníku integrace Project Service Automation, aby mohly být zaúčtovány ve Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="ff6cd-123">Synchronizace dat</span><span class="sxs-lookup"><span data-stu-id="ff6cd-123">Data synchronization</span></span>

<span data-ttu-id="ff6cd-124">Následující obrázek znázorňuje, jak jsou synchronizována data jako součást Integrace mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="ff6cd-125">Ne všechny šablony jsou momentálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-125">Not all templates are currently available.</span></span> <span data-ttu-id="ff6cd-126">Šablony budou uvolňovány při jejich dokončení.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="ff6cd-127">[![Parametry integrace Project Service Automation s Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="ff6cd-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="ff6cd-128">Systémové požadavky pro aplikaci Finance</span><span class="sxs-lookup"><span data-stu-id="ff6cd-128">System requirements for Finance</span></span>

<span data-ttu-id="ff6cd-129">Pokud chcete používat integrační řešení Project Service Automation do Finance, musíte si nainstalovat Enterprise edition 7.3 s aktualizací Platform 12 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="ff6cd-130">Požadavky na systém pro Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff6cd-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="ff6cd-131">Chcete-li použít řešení integrace Project Service Automation do Finance, musíte si nainstalovat následující součásti:</span><span class="sxs-lookup"><span data-stu-id="ff6cd-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="ff6cd-132">Dynamics 365 Project Service Automation verze 9.0.0.0 nebo novější</span><span class="sxs-lookup"><span data-stu-id="ff6cd-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="ff6cd-133">Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 Sales, verze 1.14.0.0 (v14) nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="ff6cd-134">Integrační řešení Project Service Automation do Finance pro Dynamics 365 Project Service Automation verze 1.0.0.0 nebo pozdější</span><span class="sxs-lookup"><span data-stu-id="ff6cd-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="ff6cd-135">Nainstalujte řešení integrace Project Service Automation do Finance do své instance Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff6cd-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="ff6cd-136">Stáhněte si řešení integrace Project Service Automation do Finance z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podle pokynů, které jsou součástí řešení.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
