---
title: Synchronizace projektových úloh přímo z Project Service Automation do aplikace Finance and Operations.
description: Toto téma popisuje šablonu a základní úkol, které se používají k synchronizaci úkolů projektů přímo z aplikace Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770259"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="57673-103">Synchronizace projektových úloh přímo z Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="57673-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="57673-104">Toto téma popisuje šablonu a základní úkol, které se používají k synchronizaci úkolů projektů přímo z aplikace Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="57673-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="57673-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici ve verzi 8.0.</span><span class="sxs-lookup"><span data-stu-id="57673-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="57673-106">Pokud používáte Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení.</span><span class="sxs-lookup"><span data-stu-id="57673-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="57673-107">Pokud musíte resetovat rozúčtování, doporučili jsme nainstalovat též KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="57673-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="57673-108">Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo pozdější.</span><span class="sxs-lookup"><span data-stu-id="57673-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="57673-109">Tok dat pro Project Service Automation a aplikaci Finance</span><span class="sxs-lookup"><span data-stu-id="57673-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="57673-110">Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="57673-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="57673-111">Šablona integrace, která je k dispozici s funkcí integrace dat, umožňuje tok dat o úlohách projektu z aplikace Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="57673-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="57673-112">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="57673-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="57673-113">[![Tok dat pro integraci Project Service Automation s aplikací Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="57673-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="57673-114">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="57673-114">Template and task</span></span>

<span data-ttu-id="57673-115">Chcete-li získat přístup k šabloně, zvolte v centru správy Microsoft Power Apps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="57673-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="57673-116">K synchronizaci projektových úkolů z aplikace Project Service Automation do aplikace Finance slouží následující šablona a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="57673-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="57673-117">**Název šablony v integraci dat:** Úlohy projektu (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="57673-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="57673-118">**Název úkolu v projektu:** Úlohy projektu</span><span class="sxs-lookup"><span data-stu-id="57673-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="57673-119">Než dojde k synchronizaci úkolů projektu, je nutné synchronizovat projekty a projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="57673-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="57673-120">Sada entit</span><span class="sxs-lookup"><span data-stu-id="57673-120">Entity set</span></span>

| <span data-ttu-id="57673-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="57673-121">Project Service Automation</span></span> | <span data-ttu-id="57673-122">Finance</span><span class="sxs-lookup"><span data-stu-id="57673-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="57673-123">Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="57673-123">Project Tasks</span></span>              | <span data-ttu-id="57673-124">Entita integrace pro úlohu projektu</span><span class="sxs-lookup"><span data-stu-id="57673-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="57673-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="57673-125">Entity flow</span></span>

<span data-ttu-id="57673-126">Projektové úkoly jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako projektové aktivity.</span><span class="sxs-lookup"><span data-stu-id="57673-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="57673-127">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="57673-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="57673-128">Než dojde k synchronizaci úkolů projektu, je nutné synchronizovat projekty a projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="57673-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="57673-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="57673-129">Power Query</span></span>

<span data-ttu-id="57673-130">K filtrování dat musíte použít Microsoft Power Query pro Excel, pokud je splněna tato podmínka:</span><span class="sxs-lookup"><span data-stu-id="57673-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="57673-131">Máte záznamy specifické pro zdroj v úloze projektu.</span><span class="sxs-lookup"><span data-stu-id="57673-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="57673-132">Pokud musíte použít Power Query, postupujte podle těchto pokynů:</span><span class="sxs-lookup"><span data-stu-id="57673-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="57673-133">Šablona projektového úkolu (PSA do Fin and Ops) má výchozí filtr, který vyloučí záznamy specifické pro zdroje z úkolu projektu nastavením filtru **IsLineTask** na **False**</span><span class="sxs-lookup"><span data-stu-id="57673-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="57673-134">Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="57673-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="57673-135">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="57673-135">Template mapping in Data integration</span></span>

<span data-ttu-id="57673-136">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="57673-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="57673-137">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="57673-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="57673-138">[![Mapování šablony](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="57673-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
