---
title: "Synchronizujte převody zásob a množstevních úprav ze služby Field Service do aplikace Finance and Operations"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci převodů zásob a množstevních úprav z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="785a8-103">Synchronizujte množstevní úpravy zásob a ze služby Field Service do aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="785a8-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="785a8-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci převodů zásob a množstevních úprav z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="785a8-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="785a8-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="785a8-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="785a8-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="785a8-106">Templates and tasks</span></span>
<span data-ttu-id="785a8-107">Následující šablona a základní úlohy, které se používají k synchronizaci převodů zásob a množstevních úprav z aplikace Microsoft Dynamics 365 for Field Service do aplikace Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="785a8-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="785a8-108">**Název šablon v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="785a8-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="785a8-109">Množstevní úpravy zásob (ze služby Field Service do aplikace Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="785a8-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="785a8-110">Převody zásob (ze služby Field Service do aplikace Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="785a8-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="785a8-111">**Názvy úkolů v projektech integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="785a8-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="785a8-112">Množstevní úpravy zásob</span><span class="sxs-lookup"><span data-stu-id="785a8-112">Inventory Adjustments</span></span>
- <span data-ttu-id="785a8-113">Převody zásob</span><span class="sxs-lookup"><span data-stu-id="785a8-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="785a8-114">Sada entit</span><span class="sxs-lookup"><span data-stu-id="785a8-114">Entity set</span></span>
| <span data-ttu-id="785a8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="785a8-115">Field Service</span></span>                     | <span data-ttu-id="785a8-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="785a8-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="785a8-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="785a8-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="785a8-118">CDS záhlaví a řádky deníku úprav zásob</span><span class="sxs-lookup"><span data-stu-id="785a8-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="785a8-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="785a8-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="785a8-120">CDS záhlaví a řádky deníku převodu zásob</span><span class="sxs-lookup"><span data-stu-id="785a8-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="785a8-121">Tok entity</span><span class="sxs-lookup"><span data-stu-id="785a8-121">Entity flow</span></span>
<span data-ttu-id="785a8-122">Úpravy zásob a převodů provedené ve službě Field Service se synchronizují s aplikací Finance and Operations, jakmile se změní **stav zaúčtování** z hodnoty vytvořeno na zaúčtováno.</span><span class="sxs-lookup"><span data-stu-id="785a8-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="785a8-123">Když k tomu dojde, úprava nebo převodní příkaz budou uzamčeny a bude jen pro čtení, jelikož úpravy a převody mohou být zaúčtovány v aplikaci Finance and Operations, a proto je nelze měnit.</span><span class="sxs-lookup"><span data-stu-id="785a8-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="785a8-124">V aplikaci Finance and Operations můžete nastavit dávkovou úlohu, aby automaticky zaúčtovala a převedla deníky zásob generované s integrací.</span><span class="sxs-lookup"><span data-stu-id="785a8-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="785a8-125">Další informace o tom, jak povolit tuto dávkovou úlohu, naleznete v předpokladu níže.</span><span class="sxs-lookup"><span data-stu-id="785a8-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="785a8-126">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="785a8-126">Field Service CRM solution</span></span> 
<span data-ttu-id="785a8-127">Pole Jednotka zásob bylo přidáno do entity produktu.</span><span class="sxs-lookup"><span data-stu-id="785a8-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="785a8-128">Toto pole je třeba, jelikož prodejní jednotka a jednotka zásob nejsou vždy v operacích totožné a pro skladové zásoby v operacích je zapotřebí jednotka zásob.</span><span class="sxs-lookup"><span data-stu-id="785a8-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="785a8-129">Při nastavování produktu v poli úprava zásob produktu pro úpravy zásob a převody zásob bude jednotka získána z hodnoty produktových zásob produktu.</span><span class="sxs-lookup"><span data-stu-id="785a8-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="785a8-130">Pokud je hodnota nalezena, pole jednotky bude v rámci úpravy zásob produktu zamčené.</span><span class="sxs-lookup"><span data-stu-id="785a8-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="785a8-131">Pole Stav zaúčtování bylo přidáno jak k entitě úprav zásob, tak k entitě převodu zásob.</span><span class="sxs-lookup"><span data-stu-id="785a8-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="785a8-132">Toto pole slouží jako filtr, když je úprava nebo převod odeslán do Operací.</span><span class="sxs-lookup"><span data-stu-id="785a8-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="785a8-133">Pole je přednastaveno jako Vytvořené (1) a poté není odesláno do Operací.</span><span class="sxs-lookup"><span data-stu-id="785a8-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="785a8-134">Jakmile pole změníte na Zaúčtováno (2), je odesláno do operací, ale už nebude možné provádět úpravy, převod ani přidávat nové řádky.</span><span class="sxs-lookup"><span data-stu-id="785a8-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="785a8-135">Pole Číselná řada bylo přidáno do entity úpravy zásob produktu.</span><span class="sxs-lookup"><span data-stu-id="785a8-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="785a8-136">Toto pole umožňuje integraci mít jedinečné číslo, takže integrace pozná, kdy se vytvářet a kdy aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="785a8-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="785a8-137">Při vytvoření prvního produktu úprav zásob dojde k vytvoření nového záznamu v entitě P2C AutoNumber za účelem zachování číselné řady a předpony, která se používá.</span><span class="sxs-lookup"><span data-stu-id="785a8-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="785a8-138">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="785a8-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="785a8-139">V aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="785a8-139">In Finance and Operations</span></span>
<span data-ttu-id="785a8-140">Deníky zásob integrace generované integrací lze zaúčtovat automaticky pomocí dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="785a8-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="785a8-141">To můžete povolit zde: Řízení zásob > Periodické úlohy > CDS integrace > Zaúčtovat skladové deníky integrace</span><span class="sxs-lookup"><span data-stu-id="785a8-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="785a8-142">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="785a8-142">Template mapping in Data integration</span></span>

<span data-ttu-id="785a8-143">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="785a8-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="785a8-144">Množstevní úpravy (služba Field Service do aplikace Finance and Operations): Množstevní úpravy</span><span class="sxs-lookup"><span data-stu-id="785a8-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="785a8-145">[![Mapování šablony v integraci dat](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="785a8-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="785a8-146">Převod zásob (služba Field Service do aplikace Finance and Operations): převod zásob</span><span class="sxs-lookup"><span data-stu-id="785a8-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="785a8-147">[![Mapování šablony v integraci dat](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="785a8-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

