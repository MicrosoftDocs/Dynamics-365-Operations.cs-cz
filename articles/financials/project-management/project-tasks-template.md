---
title: "Synchronizace úloh projektu z Project Service Automation"
description: "Toto téma popisuje šablonu a základní úlohu, které se používají k synchronizaci projektových úkolů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="f9559-103">Synchronizace projektových úloh z Project Service Automation přímo do projektových aktivit v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9559-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="f9559-104">Toto téma popisuje šablonu a základní úlohu, které se používají k synchronizaci projektových úkolů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9559-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f9559-105">Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Dynamics 365 for Finance and Operations verze 8.0.</span><span class="sxs-lookup"><span data-stu-id="f9559-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f9559-106">Tok dat pro Project Service Automation a aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f9559-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="f9559-107">Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9559-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="f9559-108">Šablona integrace, která je k dispozici s funkcí integrace dat, umožňuje tok dat o úlohách projektu z aplikace Project Service Automation do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9559-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f9559-109">Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9559-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="f9559-110">[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f9559-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="f9559-111">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="f9559-111">Template and task</span></span>

<span data-ttu-id="f9559-112">Chcete-li získat přístup k šabloně, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.</span><span class="sxs-lookup"><span data-stu-id="f9559-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f9559-113">K synchronizaci projektových úkolů z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkol:</span><span class="sxs-lookup"><span data-stu-id="f9559-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="f9559-114">-**Název šablony v integraci dat:** Projektové úkoly (PSA do Fin and Ops) -**Název úkolu v projektu:** Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="f9559-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="f9559-115">Než dojde k synchronizaci úkolů projektu, je nutné synchronizovat projekty a projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f9559-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f9559-116">Sada entit</span><span class="sxs-lookup"><span data-stu-id="f9559-116">Entity set</span></span>

|<span data-ttu-id="f9559-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f9559-117">Project Service Automation</span></span>               | <span data-ttu-id="f9559-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f9559-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="f9559-119">Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="f9559-119">Project Tasks</span></span>                           | <span data-ttu-id="f9559-120">Entita integrace pro úlohu projektu.</span><span class="sxs-lookup"><span data-stu-id="f9559-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="f9559-121">Tok entity</span><span class="sxs-lookup"><span data-stu-id="f9559-121">Entity flow</span></span>

<span data-ttu-id="f9559-122">Projektové úkoly jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako projektové aktivity.</span><span class="sxs-lookup"><span data-stu-id="f9559-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f9559-123">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="f9559-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="f9559-124">Než dojde k synchronizaci úkolů projektu, je nutné synchronizovat projekty a projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="f9559-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="f9559-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="f9559-125">Power Query</span></span>

<span data-ttu-id="f9559-126">K filtrování dat musíte použít Microsoft Power Query , pokud jsou splněny tytopodmínky:</span><span class="sxs-lookup"><span data-stu-id="f9559-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="f9559-127">Máte záznamy specifické pro zdroj v rámci úlohy projektu.</span><span class="sxs-lookup"><span data-stu-id="f9559-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="f9559-128">Pokud musíte použít Power Query, postupujte podle následujících pokynů:</span><span class="sxs-lookup"><span data-stu-id="f9559-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="f9559-129">Šablona projektového úkolu (PSA do Fin and Ops) má výchozí filtr, který vyloučí záznamy specifické pro zdroje z projektového úkolu projektu nastavením filtru **IsLineTask** na **False**</span><span class="sxs-lookup"><span data-stu-id="f9559-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="f9559-130">Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="f9559-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f9559-131">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="f9559-131">Template mapping in Data integration</span></span>

<span data-ttu-id="f9559-132">Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="f9559-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="f9559-133">Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9559-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f9559-134">[![Mapování šablony](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="f9559-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


