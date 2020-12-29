---
title: Synchronizace pracovních příkazů s projektem z aplikace Field Service do Supply Chain Management
description: Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Dynamics 365 Field Service do prodejních objednávek v Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ebf23c5c831e9dad5d13c72f82eb3eeb30da853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423622"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="27432-103">Synchronizace pracovních příkazů s projektem z aplikace Field Service do Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="27432-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27432-104">Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Dynamics 365 Field Service do prodejních objednávek v Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="27432-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="27432-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="27432-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="27432-106">Používaná šablona **Pracovní příkazy s projektem (Field Service do Supply Chain Management)** je založena na šabloně **Pracovní příkazy (Field Service do Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="27432-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="27432-107">Více informací naleznete v části [Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="27432-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="27432-108">V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:</span><span class="sxs-lookup"><span data-stu-id="27432-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="27432-109">**Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="27432-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="27432-110">**Pracovní příkazy (Field Service do Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="27432-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="27432-111">Hlavní rozdíl je, že tato šablona obsahuje mapování čísla projektu přirazeného pracovnímu příkazu ve službě Field Service, přičemž je zajištěno, že prodejní objednávky vytvořené v aplikaci Supply Chain Management zahrnují číslo projektu a že u souvisejícího projektu může být provedena fakturace.</span><span class="sxs-lookup"><span data-stu-id="27432-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="27432-112">Kromě toho šablona používá pokročilé dotazování a filtrování.</span><span class="sxs-lookup"><span data-stu-id="27432-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="27432-113">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="27432-113">Templates and tasks</span></span>

<span data-ttu-id="27432-114">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="27432-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="27432-115">Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="27432-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="27432-116">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="27432-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="27432-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="27432-117">WorkOrderHeader</span></span>
- <span data-ttu-id="27432-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="27432-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="27432-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="27432-119">WorkOrderProduct</span></span>
- <span data-ttu-id="27432-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="27432-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="27432-121">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="27432-121">Field Service CRM solution</span></span>
<span data-ttu-id="27432-122">Pole **Externí projekt** bylo přidáno do entity pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="27432-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="27432-123">Toto pole je vyhledávací hodnota určená k označení nákupu v pracovním příkazu s projektem, a prodejní objednávka pak bude v rámci aplikace Supply Chain Management propojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="27432-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="27432-124">Jakmile se **stav systému** změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole **externích projektů** se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.</span><span class="sxs-lookup"><span data-stu-id="27432-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="27432-125">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="27432-125">Template mapping in Data integration</span></span>

<span data-ttu-id="27432-126">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="27432-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="27432-127">Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="27432-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="27432-128">[![Mapování šablony v integraci dat](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="27432-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="27432-129">Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="27432-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="27432-130">[![Mapování šablony v integraci dat](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="27432-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="27432-131">Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="27432-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="27432-132">[![Mapování šablony v integraci dat](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="27432-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="27432-133">Pracovní příkazy s aplikací Project (Field Service do Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="27432-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="27432-134">[![Mapování šablony v integraci dat](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="27432-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
