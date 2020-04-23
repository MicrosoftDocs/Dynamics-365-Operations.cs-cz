---
title: Synchronizace informací o úrovni zásob z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
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
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215900"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="72b33-103">Synchronizace informací o úrovni zásob z aplikace Supply Chain Management do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="72b33-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="72b33-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="72b33-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="72b33-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="72b33-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="72b33-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="72b33-106">Templates and tasks</span></span>
<span data-ttu-id="72b33-107">Následující šablona a základní úlohy se používají k synchronizaci praktických úrovní skladů ze Supply Chain Management do Field Service.</span><span class="sxs-lookup"><span data-stu-id="72b33-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="72b33-108">**Šablona v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="72b33-108">**Template in Data integration**</span></span>
- <span data-ttu-id="72b33-109">Zásoby produktu (z aplikace Supply Chain Management do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="72b33-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="72b33-110">**Úkol v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="72b33-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="72b33-111">Zásoby produktu</span><span class="sxs-lookup"><span data-stu-id="72b33-111">Product inventory</span></span>

<span data-ttu-id="72b33-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace množství zásob:</span><span class="sxs-lookup"><span data-stu-id="72b33-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="72b33-113">Sklady (z aplikace Supply Chain Management do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="72b33-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="72b33-114">Produkty Field Service se skladovou jednotkou (Supply Chain Management do Sales)</span><span class="sxs-lookup"><span data-stu-id="72b33-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="72b33-115">Sada entit</span><span class="sxs-lookup"><span data-stu-id="72b33-115">Entity set</span></span>

| <span data-ttu-id="72b33-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="72b33-116">Field Service</span></span>                      | <span data-ttu-id="72b33-117">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="72b33-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="72b33-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="72b33-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="72b33-119">CDS zásoby na skladě podle skladu</span><span class="sxs-lookup"><span data-stu-id="72b33-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="72b33-120">Tok entity</span><span class="sxs-lookup"><span data-stu-id="72b33-120">Entity flow</span></span>
<span data-ttu-id="72b33-121">Informace o množství zásob z aplikace Finance and Operations jsou pro vybrané produkty odeslány do služby Field Service.</span><span class="sxs-lookup"><span data-stu-id="72b33-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="72b33-122">Informace na úrovni zásob zahrnují:</span><span class="sxs-lookup"><span data-stu-id="72b33-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="72b33-123">Množství na skladě (aktuální evidované fyzické množství, které se nachází ve skladu)</span><span class="sxs-lookup"><span data-stu-id="72b33-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="72b33-124">Množství objednávky (celkové zaznamenané množství na objednávce, jako jsou prodejní objednávky)</span><span class="sxs-lookup"><span data-stu-id="72b33-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="72b33-125">Objednané množství (celkové zaznamenané objednané množství, jako jsou prodejní objednávky)</span><span class="sxs-lookup"><span data-stu-id="72b33-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="72b33-126">Tyto informace jsou zaznamenány pro uvolněný produkt pro každý sklad a synchronizovány podle sledování změn, když se změní úroveň zásob.</span><span class="sxs-lookup"><span data-stu-id="72b33-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="72b33-127">Ve službě Field Service, řešení integrace vytváří deníky zásob pro deltu, takže úrovně ve službě Field Service odpovídají množstvím v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72b33-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="72b33-128">Aplikace Supply Chain Management bude sloužit jako hlavní zdroj pro úroveň zásob.</span><span class="sxs-lookup"><span data-stu-id="72b33-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="72b33-129">Proto je důležité nastavit integraci pro pracovní příkazy, převody a opravy ze služby Field Service do aplikace Supply Chain Management, pokud se tato funkce používá ve službě Field Service, dohromady se synchronizací množství zásob z aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72b33-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="72b33-130">Produkty a sklady, kde jsou zásoby řízení z aplikace Supply Chain Management lze ovládat pomocí Rozšířeného dotazu a filtrování (Power Query).</span><span class="sxs-lookup"><span data-stu-id="72b33-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="72b33-131">Poznámka: Je možné vytvořit více skladů ve službě Field Services (pomocí **Je externě spravován = Ne**) a poté je namapovat do jediného skladu v aplikaci Supply Chain Management pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="72b33-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="72b33-132">Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72b33-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="72b33-133">V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72b33-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="72b33-134">Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt v Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="72b33-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="72b33-135">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="72b33-135">Field Service CRM solution</span></span>
<span data-ttu-id="72b33-136">Entita **zásoby externího produktu** je nová entita, která se používá pouze pro jištění při integraci.</span><span class="sxs-lookup"><span data-stu-id="72b33-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="72b33-137">Tato entita přijme integrované hodnoty úrovně zásob z aplikace Supply Chain Management a potom tyto hodnoty transformuje do deníků ručních zásob, které poté změní produkty zásob skladu.</span><span class="sxs-lookup"><span data-stu-id="72b33-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="72b33-138">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="72b33-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="72b33-139">Integrace dat</span><span class="sxs-lookup"><span data-stu-id="72b33-139">Data integration</span></span>
<span data-ttu-id="72b33-140">Aby projekt fungoval, je nutné zajistit, aby byl klíč integrace aktualizován pro msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="72b33-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="72b33-141">Přejděte na **Integrace dat > Sady připojení**.</span><span class="sxs-lookup"><span data-stu-id="72b33-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="72b33-142">Vyberte použitou sadu připojení.</span><span class="sxs-lookup"><span data-stu-id="72b33-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="72b33-143">Na kartě **Klíč integrace** se ujistěte, že jsou do msdynce_externalproductinventories přidány následující klíče:</span><span class="sxs-lookup"><span data-stu-id="72b33-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="72b33-144">msdynce_productnumber (číslo produktu)</span><span class="sxs-lookup"><span data-stu-id="72b33-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="72b33-145">msdynce_warehouseid (ID skladu)</span><span class="sxs-lookup"><span data-stu-id="72b33-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="72b33-146">Projekt integrace dat</span><span class="sxs-lookup"><span data-stu-id="72b33-146">Data integration project</span></span>
<span data-ttu-id="72b33-147">Můžete použít filtry s pokročilým dotazováním a filtrování, pomocí kterých lze řídit, že informace o zásobách budou z aplikace Supply Chain Management do služby Field Service odesílat pouze požadované produkty a sklady.</span><span class="sxs-lookup"><span data-stu-id="72b33-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="72b33-148">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="72b33-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="72b33-149">Zásoby produktu (Supply Chain Management do Field Service): Zásoby produktu</span><span class="sxs-lookup"><span data-stu-id="72b33-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="72b33-150">[![Mapování šablony v integraci dat](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="72b33-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
