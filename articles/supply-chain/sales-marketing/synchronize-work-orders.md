---
title: Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536726"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="eec10-103">Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eec10-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="eec10-104">Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eec10-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="eec10-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="eec10-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="eec10-106">Používaná šablona **Pracovní příkazy s projektem (Field Service do Fin and Ops)** je založena na šabloně **Pracovní příkazy (Field Service to Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="eec10-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="eec10-107">Více informací naleznete v části [Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="eec10-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="eec10-108">V tomto tématu jsou popsány pouze rozdíly mezi dvěma šablonami:</span><span class="sxs-lookup"><span data-stu-id="eec10-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="eec10-109">**Pracovní příkazy s projektem (Field Service do Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="eec10-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="eec10-110">**Pracovní příkazy (Field Service do Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="eec10-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="eec10-111">Hlavní rozdíl je, že tato šablona obsahuje mapování čísla projektu přirazeného pracovnímu příkazu ve službě Field Service, přičemž je zajištěno, že prodejní objednávky vytvořené v aplikaci Finance and Operations zahrnují číslo projektu a že u souvisejícího projektu může být provedena fakturace.</span><span class="sxs-lookup"><span data-stu-id="eec10-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="eec10-112">Kromě toho šablona používá pokročilé dotazování a filtrování.</span><span class="sxs-lookup"><span data-stu-id="eec10-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="eec10-113">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="eec10-113">Templates and tasks</span></span>

<span data-ttu-id="eec10-114">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="eec10-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="eec10-115">Pracovní příkazy s projektem (Field Service do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="eec10-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="eec10-116">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="eec10-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="eec10-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="eec10-117">WorkOrderHeader</span></span>
- <span data-ttu-id="eec10-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="eec10-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="eec10-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="eec10-119">WorkOrderProduct</span></span>
- <span data-ttu-id="eec10-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="eec10-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="eec10-121">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="eec10-121">Field Service CRM solution</span></span>
<span data-ttu-id="eec10-122">Pole **Externí projekt** bylo přidáno do entity pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="eec10-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="eec10-123">Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Finance and Operations propojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="eec10-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="eec10-124">Jakmile se **stav systému** změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole **externích projektů** se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.</span><span class="sxs-lookup"><span data-stu-id="eec10-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="eec10-125">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="eec10-125">Template mapping in Data integration</span></span>

<span data-ttu-id="eec10-126">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="eec10-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="eec10-127">Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="eec10-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="eec10-128">[![Mapování šablony v integraci dat](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="eec10-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="eec10-129">Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="eec10-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="eec10-130">[![Mapování šablony v integraci dat](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="eec10-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="eec10-131">Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="eec10-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="eec10-132">[![Mapování šablony v integraci dat](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="eec10-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="eec10-133">Pracovní příkazy s projektem (Field Service do Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="eec10-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="eec10-134">[![Mapování šablony v integraci dat](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="eec10-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
