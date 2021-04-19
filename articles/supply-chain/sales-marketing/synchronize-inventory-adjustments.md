---
title: Synchronizace převodů a úprav zásob ze služby Field Service do Supply Chain Management
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci úprav zásob a převodů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 9f3bfe950446a6e87e34c32d2593cba0af84d8e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838974"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="7e5c5-103">Synchronizace převodů a úprav zásob ze služby Field Service do Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7e5c5-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7e5c5-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci úprav zásob a převodů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="7e5c5-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="7e5c5-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7e5c5-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="7e5c5-106">Templates and tasks</span></span>
<span data-ttu-id="7e5c5-107">Následující šablona a základní úlohy se používají k synchronizaci úprav skladů a převodů z Field Service do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="7e5c5-108">**šablony v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="7e5c5-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="7e5c5-109">Úprava produktu (z aplikace Field Service do Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7e5c5-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="7e5c5-110">Převody zásob (z aplikace Field Service do Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7e5c5-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="7e5c5-111">**úkoly v projektech integrace dat**</span><span class="sxs-lookup"><span data-stu-id="7e5c5-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="7e5c5-112">Množstevní úpravy zásob</span><span class="sxs-lookup"><span data-stu-id="7e5c5-112">Inventory Adjustments</span></span>
- <span data-ttu-id="7e5c5-113">Převody zásob</span><span class="sxs-lookup"><span data-stu-id="7e5c5-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="7e5c5-114">Nastavení tabulky</span><span class="sxs-lookup"><span data-stu-id="7e5c5-114">Table set</span></span>
| <span data-ttu-id="7e5c5-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="7e5c5-115">Field Service</span></span>                     | <span data-ttu-id="7e5c5-116">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="7e5c5-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="7e5c5-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="7e5c5-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="7e5c5-118">Dataverse záhlaví a řádky deníku úprav zásob</span><span class="sxs-lookup"><span data-stu-id="7e5c5-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="7e5c5-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="7e5c5-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="7e5c5-120">Dataverse záhlaví a řádky deníku převodu zásob</span><span class="sxs-lookup"><span data-stu-id="7e5c5-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="7e5c5-121">Tok tabulky</span><span class="sxs-lookup"><span data-stu-id="7e5c5-121">Table flow</span></span>
<span data-ttu-id="7e5c5-122">Úpravy zásob a převodů provedené ve službě Field Service se synchronizují s aplikací Supply Chain Management, poté, co se změní **stav zaúčtování** z hodnoty **vytvořeno** na **zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="7e5c5-123">V tomto případě se úprava nebo převodní příkaz uzamknou a budou jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="7e5c5-124">To znamená, že úpravy převodů lze v aplikaci Supply Chain Management zaúčtovat, ale ne změnit.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="7e5c5-125">V aplikaci Supply Chain Management můžete nastavit dávkovou úlohu, aby automaticky zaúčtovala a úpravy a převedla deníky zásob generované při integraci.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="7e5c5-126">Další informace o tom, jak povolit dávkovou úlohu, naleznete v předpokladech níže.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="7e5c5-127">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="7e5c5-127">Field Service CRM solution</span></span> 
<span data-ttu-id="7e5c5-128">Sloupec **Jednotka zásob** byl přidán do tabulky **produkt**.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="7e5c5-129">Tento sloupec je třeba, jelikož jednotka prodeje a zásob není v aplikaci Supply Chain Management vždy stejná a skladová jednotka je potřeba pro skladové zásoby v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="7e5c5-130">Při nastavování produktu v poli úprava zásob produktu pro úpravy zásob a převody zásob bude jednotka získána z hodnoty produktových zásob produktu.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="7e5c5-131">Pokud je hodnota nalezena, sloupec **Jednotka** bude v rámci úpravy zásob produktu zamčené.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="7e5c5-132">Sloupec **Stav zaúčtování** byl přidán jak k tabulce **Úprava zásob**, tak k tabulce **Převod zásob**.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="7e5c5-133">Tento sloupec slouží jako filtr, když je úprava nebo převod odeslán do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="7e5c5-134">Výchozí hodnota v tomto sloupci je Vytvořeno (1), není však odeslána do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="7e5c5-135">Jakmile hodnotu aktualizujete na Zaúčtováno (2), je odeslána do aplikace Supply Chain Management, ale pak už nebude možné provádět úpravy, převod ani přidávat nové řádky.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="7e5c5-136">Sloupec **Číselná řada** byl přidán do tabulky **Produkt úpravy zásob**.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="7e5c5-137">Tento sloupec zajišťuje, aby integrace měla jedinečné číslo, takže může vytvořit a aktualizovat úpravu.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="7e5c5-138">Při vytvoření prvního produktu úprav zásob dojde k vytvoření nového záznamu v tabulce **P2C AutoNumber** za účelem zachování číselné řady a předpony, která se používá.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7e5c5-139">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="7e5c5-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="7e5c5-140">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="7e5c5-140">Supply Chain Management</span></span>
<span data-ttu-id="7e5c5-141">Deníky zásob integrace generované integrací lze zaúčtovat automaticky pomocí dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="7e5c5-142">To můžete povolit zde: **Řízení zásob > Periodické úlohy > integrace Dataverse > Zaúčtovat skladové deníky integrace**.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7e5c5-143">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="7e5c5-143">Template mapping in Data integration</span></span>

<span data-ttu-id="7e5c5-144">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="7e5c5-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="7e5c5-145">Úprava zásob (Field Service do Supply Chain Management): Úprava zásob</span><span class="sxs-lookup"><span data-stu-id="7e5c5-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="7e5c5-146">[![Mapování šablony v integraci dat](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="7e5c5-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="7e5c5-147">Převod zásob (Field Service do Supply Chain Management): Převod zásob</span><span class="sxs-lookup"><span data-stu-id="7e5c5-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="7e5c5-148">[![Mapování šablony v integraci dat](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="7e5c5-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]