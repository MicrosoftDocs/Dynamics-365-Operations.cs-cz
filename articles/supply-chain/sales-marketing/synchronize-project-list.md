---
title: Synchronizujte seznamy projektů z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525870"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="df29b-103">Synchronizace seznamu projektů z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="df29b-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="df29b-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci projektů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="df29b-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="df29b-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="df29b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="df29b-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="df29b-106">Templates and tasks</span></span>
<span data-ttu-id="df29b-107">Následující šablona a základní úlohy slouží ke spuštění synchronizace projektů z Microsoft Dynamics 365 for Finance and Operations k Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="df29b-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="df29b-108">**Šablona v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="df29b-108">**Template in Data integration**</span></span>
- <span data-ttu-id="df29b-109">Projekty (Fin and Ops do Field Service)</span><span class="sxs-lookup"><span data-stu-id="df29b-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="df29b-110">**Úkol v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="df29b-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="df29b-111">Projekty</span><span class="sxs-lookup"><span data-stu-id="df29b-111">Projects</span></span>

<span data-ttu-id="df29b-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace seznamu projektů:</span><span class="sxs-lookup"><span data-stu-id="df29b-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="df29b-113">Účty (Sales do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="df29b-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="df29b-114">Sada entit</span><span class="sxs-lookup"><span data-stu-id="df29b-114">Entity set</span></span>
| <span data-ttu-id="df29b-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="df29b-115">Field Service</span></span>           | <span data-ttu-id="df29b-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="df29b-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="df29b-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="df29b-117">msdynce_externalprojects</span></span> | <span data-ttu-id="df29b-118">Projekty</span><span class="sxs-lookup"><span data-stu-id="df29b-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="df29b-119">Tok entity</span><span class="sxs-lookup"><span data-stu-id="df29b-119">Entity flow</span></span>
<span data-ttu-id="df29b-120">Projekty jsou vytvářeny v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="df29b-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="df29b-121">Projekty s **typem projektu** nastaveným na **Čas a materiál** a **fází projektu** nastavenou na **probíhá** bude synchronizován s entitou **Externí projekt** entity ve službě Field Service, včetně čísla projektu, názvu projektu fáze projektu a informací o účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="df29b-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="df29b-122">Seznam **Externí projekt** se používá ke spárování pracovních příkazů služby Field Service s projekty aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="df29b-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="df29b-123">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="df29b-123">Field Service CRM solution</span></span>
<span data-ttu-id="df29b-124">Entita **Externí projekt** získá všechny projekty z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="df29b-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="df29b-125">Pole **Externí projekt** bylo přidáno do entity **pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="df29b-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="df29b-126">Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Finance and Operations propojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="df29b-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="df29b-127">Po změně pole **Stav systému** na **Otevřít – Probíhá (690,970,000)** na vyšší status se pole **Externí projekt** uzamkne a nebude dále možné přidávat, odebírat ani měnit jeho hodnotu.</span><span class="sxs-lookup"><span data-stu-id="df29b-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="df29b-128">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="df29b-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="df29b-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="df29b-129">Finance and Operations</span></span>
<span data-ttu-id="df29b-130">Povolte sledování změn pro projekty datové entity.</span><span class="sxs-lookup"><span data-stu-id="df29b-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="df29b-131">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="df29b-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="df29b-132">Projekty (Fin and Ops do Field Service): Projekty</span><span class="sxs-lookup"><span data-stu-id="df29b-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="df29b-133">[![Mapování šablony v integraci dat](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="df29b-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
