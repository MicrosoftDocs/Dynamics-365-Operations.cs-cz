---
title: Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.
description: Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "329843"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="d9273-103">Synchronizujte pracovní příkazy s projektem ze služby Field Service do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d9273-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d9273-104">Toto téma popisuje šablony a základní úlohu, které se používají k synchronizaci pracovních příkazů v s číslem projektu z Microsoft Dynamics 365 for Field Service do prodejních objednávek v Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d9273-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d9273-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="d9273-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="d9273-106">Používaná šablona **Produkty Field Service (z aplikace Finance and Operations do služby Field Service)** je založena na šabloně **Produkty (z aplikace Finance and Operations do Sales) – Direct** z modulu Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="d9273-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="d9273-107">Další informace naleznete v tématu [Produkty (Finance and Operations do Sales) – přímé](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="d9273-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="d9273-108">Toto téma pouze popisuje rozdíl mezi šablonami **Produkty Field Service (Finance and Operations do Field Service)** a je založeno na šabloně **Field Service (Finance and Operations do Sales) – přímé**.</span><span class="sxs-lookup"><span data-stu-id="d9273-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="d9273-109">Hlavní rozdíl je, že tato šablona obsahuje mapování čísla projektu přirazeného pracovnímu příkazu ve službě Field Service, přičemž je zajištěno, že prodejní objednávky vytvořené v aplikaci Finance and Operations zahrnují číslo projektu a že u souvisejícího projektu může být provedena fakturace.</span><span class="sxs-lookup"><span data-stu-id="d9273-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="d9273-110">Kromě toho šablona používá pokročilé dotazování a filtrování.</span><span class="sxs-lookup"><span data-stu-id="d9273-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d9273-111">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="d9273-111">Templates and tasks</span></span>

<span data-ttu-id="d9273-112">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="d9273-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="d9273-113">Pracovní příkazy s projektem (Field Service do Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d9273-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="d9273-114">**Název úkolu v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="d9273-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="d9273-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="d9273-115">WorkOrderHeader</span></span>
- <span data-ttu-id="d9273-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="d9273-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="d9273-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="d9273-117">WorkOrderProduct</span></span>
- <span data-ttu-id="d9273-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="d9273-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d9273-119">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="d9273-119">Field Service CRM solution</span></span>
<span data-ttu-id="d9273-120">Pole **Externí projekt** bylo přidáno do entity pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="d9273-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="d9273-121">Toto pole je určeno k vyhledávání a nakupování tak, že označíte pracovní příkaz projektem a prodejní objednávka pak bude v rámci aplikace Finance and Operations propojena s projektem.</span><span class="sxs-lookup"><span data-stu-id="d9273-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="d9273-122">Jakmile se **stav systému** změní ze stavu Otevřený – probíhající (690,970,000) na vyšší stav, pole **externích projektů** se zamkne a nebudete moci přidávat, odebírat ani měnit jeho hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d9273-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d9273-123">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="d9273-123">Template mapping in Data integration</span></span>

<span data-ttu-id="d9273-124">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="d9273-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="d9273-125">Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="d9273-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="d9273-126">[![Mapování šablony v integraci dat](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="d9273-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="d9273-127">Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="d9273-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="d9273-128">[![Mapování šablony v integraci dat](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="d9273-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="d9273-129">Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="d9273-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="d9273-130">[![Mapování šablony v integraci dat](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="d9273-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="d9273-131">Pracovní příkazy s projektem (Field Service do Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="d9273-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="d9273-132">[![Mapování šablony v integraci dat](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="d9273-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
