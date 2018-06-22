---
title: Project Service Automation
description: "Toto řešení používá funkci integrace dat k synchronizaci dat mezi instancemi aplikací Microsoft Dynamics 365 for Finance and Operations a Dynamics 365 for Project Service Automation prostřednictvím služby Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="f31e9-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f31e9-103">Project Service Automation</span></span>

<span data-ttu-id="f31e9-104">Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi aplikací Microsoft Dynamics 365 for Finance and Operations a Dynamics 365 for Project Service Automation prostřednictvím služby Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="f31e9-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="f31e9-105">Šablony integrace, které jsou k dispozici s funkcí integrace dat povolují tok projektů, projektové smlouvy, řádky smlouvy projektu, milníky řádků smlouvy projektu, úlohy projektu, kategorie transakcí výdajů, odhady hodin, a odhady výdajů z aplikace Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="f31e9-106">Pokud používáte aplikaci Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, musíte si nainstalovat KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="f31e9-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="f31e9-107">To vám poskytne integrovat projekty s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="f31e9-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="f31e9-108">Pokud používáte Dynamics 365 for Finance and Operations verzi 8.0, budete moci používat integraci úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí.</span><span class="sxs-lookup"><span data-stu-id="f31e9-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="f31e9-109">Pokud používáte Dynamics 365 for Finance and Operations verze 8.0.1, bude možné synchronizovat skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f31e9-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="f31e9-110">Pokud používáte Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení.</span><span class="sxs-lookup"><span data-stu-id="f31e9-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f31e9-111">Pokud musíte resetovat rozúčtování, doporučujeme nainstalovat též KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="f31e9-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="f31e9-112">Než budete moci integrovat Project Service Automation s Finance and Operations, musíte nakonfigurovat parametry Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f31e9-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="f31e9-113">Další informace naleznete v tématu parametry integrace Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f31e9-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="f31e9-114">Toto řešení integrace umožňuje přímou synchronizaci v následujících scénářích:</span><span class="sxs-lookup"><span data-stu-id="f31e9-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="f31e9-115">Při správě projektových smluv v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f31e9-116">Při vytváření projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f31e9-117">Při správě řádků projektových smluv v Project Service Automation a jeijch přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f31e9-118">Při správě milníků řádků projektových smluv v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f31e9-119">Při správě projektových úloh v Project Service Automation a jeich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f31e9-120">Při správě kategorií transakcí výdajů v Finance and Operations a jejich přímé synchronizaci z Finance and Operations do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f31e9-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="f31e9-121">Při vytváření odhadu projektových hodin v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f31e9-122">Při vytváření odhadu projektových výdajů v Project Service Automation a jejich přímé synchronizaci z Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="f31e9-123">Synchronizace dat</span><span class="sxs-lookup"><span data-stu-id="f31e9-123">Data synchronization</span></span>
<span data-ttu-id="f31e9-124">Následující obrázek znázorňuje, jak jsou synchronizována data jako součást Integrace mezi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f31e9-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f31e9-125">Ne všechny šablony jsou momentálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f31e9-125">Not all templates are currently available.</span></span> <span data-ttu-id="f31e9-126">Šablony budou uvolňovány při jejich dokončení.</span><span class="sxs-lookup"><span data-stu-id="f31e9-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="f31e9-127">[![Integrace Project Service Automation s aplikací Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="f31e9-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="f31e9-128">Systémové požadavky aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f31e9-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="f31e9-129">Chcete-li použít řešení integrace Project Service Automation do Finance and Operations, musíte si nainstalovat Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 s aktualizací platform update 12 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="f31e9-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="f31e9-130">Požadavky na systém pro Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f31e9-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="f31e9-131">Chcete-li použít řešení integrace Project Service Automation do Finance and Operations, musíte si nainstalovat následující součásti:</span><span class="sxs-lookup"><span data-stu-id="f31e9-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="f31e9-132">Microsoft Dynamics 365 for Project Service Automation , verze 9.0.0.0 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="f31e9-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="f31e9-133">Řešení zpeněžení potenciálního zákazníka pro Dynamics 365 for Sales, verze 1.14.0.0 (v14) nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="f31e9-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="f31e9-134">Řešení Project Service Automation do Operations pro Dynamics 365 for Project Service Automation verze 1.0.0.0 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="f31e9-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="f31e9-135">Nainstalujte řešení integrace Project Service Automation do Finance and Operations do své instance Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f31e9-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



