---
title: "Synchronizujte seznamy projektů z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci projektů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="1830c-103">Synchronizujte seznamy projektů z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="1830c-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1830c-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci projektů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1830c-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1830c-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1830c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1830c-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="1830c-106">Templates and tasks</span></span>
<span data-ttu-id="1830c-107">Následující šablona a základní úlohy, které se používají k synchronizaci projektů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 or Field Service.</span><span class="sxs-lookup"><span data-stu-id="1830c-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1830c-108">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="1830c-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="1830c-109">Projekty (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="1830c-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="1830c-110">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="1830c-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="1830c-111">Projekty</span><span class="sxs-lookup"><span data-stu-id="1830c-111">Projects</span></span>

<span data-ttu-id="1830c-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace seznamu projektů:</span><span class="sxs-lookup"><span data-stu-id="1830c-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1830c-113">Účty (Sales do aplikace Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="1830c-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1830c-114">Sada entit</span><span class="sxs-lookup"><span data-stu-id="1830c-114">Entity set</span></span>
<span data-ttu-id="1830c-115">Služba Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1830c-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="1830c-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="1830c-116">Field Service</span></span>           | <span data-ttu-id="1830c-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1830c-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1830c-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1830c-118">msdynce_externalprojects</span></span> | <span data-ttu-id="1830c-119">Projekty</span><span class="sxs-lookup"><span data-stu-id="1830c-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1830c-120">Tok entity</span><span class="sxs-lookup"><span data-stu-id="1830c-120">Entity flow</span></span>
<span data-ttu-id="1830c-121">Projekty jsou vytvářeny v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1830c-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="1830c-122">Probíhající projekty s **typem projektu** časem a materiálem a **fází projektu** se synchronizují do **externích projektů** entity ve službě Field Serivce, včetně čísla projektu, názvu projektu fáze projektu a informací o účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="1830c-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="1830c-123">Seznam **externích projektů** se používá ke spárování pracovních příkazů služby Field Service s projekty aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1830c-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="1830c-124">Řešení CRM služby Field Service Externí projekt je nová entita, která získá všechny projekty z operací.</span><span class="sxs-lookup"><span data-stu-id="1830c-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="1830c-125">Pole Externí projekt bylo přidáno do entity pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="1830c-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="1830c-126">Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci operací propojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="1830c-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="1830c-127">Jakmile se stav systému změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole externích projektů se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1830c-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1830c-128">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="1830c-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="1830c-129">V aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1830c-129">In Finance and Operations</span></span>
<span data-ttu-id="1830c-130">Povolit sledování změn pro projekty datové entity.</span><span class="sxs-lookup"><span data-stu-id="1830c-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1830c-131">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="1830c-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="1830c-132">Projekty (z aplikace Finance and Operations do služby Field Service): projekty</span><span class="sxs-lookup"><span data-stu-id="1830c-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="1830c-133">[![Mapování šablony v integraci dat](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1830c-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

