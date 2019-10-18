---
title: Synchronizace seznamu projektů z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b74a7f0445b3bdad671da4c61e561bc0d9d80cd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251585"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="99f81-103">Synchronizace seznamu projektů z aplikace Supply Chain Management do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="99f81-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="99f81-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="99f81-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="99f81-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="99f81-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="99f81-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="99f81-106">Templates and tasks</span></span>
<span data-ttu-id="99f81-107">Následující šablona a základní úlohy se používají ke spuštění synchronizace projektů ze Supply Chain Management do Field Service.</span><span class="sxs-lookup"><span data-stu-id="99f81-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="99f81-108">**Šablona v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="99f81-108">**Template in Data integration**</span></span>
- <span data-ttu-id="99f81-109">Projekty (z aplikace Supply Chain Management do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="99f81-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="99f81-110">**Úkol v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="99f81-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="99f81-111">Projekty</span><span class="sxs-lookup"><span data-stu-id="99f81-111">Projects</span></span>

<span data-ttu-id="99f81-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace seznamu projektů:</span><span class="sxs-lookup"><span data-stu-id="99f81-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="99f81-113">Obchodní vztahy (Sales do Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="99f81-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="99f81-114">Sada entit</span><span class="sxs-lookup"><span data-stu-id="99f81-114">Entity set</span></span>
| <span data-ttu-id="99f81-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="99f81-115">Field Service</span></span>           | <span data-ttu-id="99f81-116">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="99f81-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="99f81-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="99f81-117">msdynce_externalprojects</span></span> | <span data-ttu-id="99f81-118">Projekty</span><span class="sxs-lookup"><span data-stu-id="99f81-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="99f81-119">Tok entity</span><span class="sxs-lookup"><span data-stu-id="99f81-119">Entity flow</span></span>
<span data-ttu-id="99f81-120">Projekty se vytvářejí v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="99f81-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="99f81-121">Projekty s **typem projektu** nastaveným na **Čas a materiál** a **fází projektu** nastavenou na **probíhá** bude synchronizován s entitou **Externí projekt** entity ve službě Field Service, včetně čísla projektu, názvu projektu fáze projektu a informací o účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="99f81-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="99f81-122">Seznam **Externí projekt** se používá ke spárování pracovních příkazů služby Field Service s projekty aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="99f81-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="99f81-123">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="99f81-123">Field Service CRM solution</span></span>
<span data-ttu-id="99f81-124">Entita **Externí projekt** získá všechny projekty z aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="99f81-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="99f81-125">Pole **Externí projekt** bylo přidáno do entity **pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="99f81-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="99f81-126">Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Supply Chain Management propojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="99f81-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="99f81-127">Po změně pole **Stav systému** na **Otevřít – Probíhá (690,970,000)** na vyšší status se pole **Externí projekt** uzamkne a nebude dále možné přidávat, odebírat ani měnit jeho hodnotu.</span><span class="sxs-lookup"><span data-stu-id="99f81-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="99f81-128">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="99f81-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="99f81-129">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="99f81-129">Supply Chain Management</span></span>
<span data-ttu-id="99f81-130">Povolte sledování změn pro projekty datové entity.</span><span class="sxs-lookup"><span data-stu-id="99f81-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="99f81-131">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="99f81-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="99f81-132">Projekty (z aplikace Supply Chain Management do služby Field Service): Projekty</span><span class="sxs-lookup"><span data-stu-id="99f81-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="99f81-133">[![Mapování šablony v integraci dat](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="99f81-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
