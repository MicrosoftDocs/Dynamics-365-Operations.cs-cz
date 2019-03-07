---
title: Synchronizujte informace o množství zásob z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "356776"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c5b99-103">Synchronizace informací o úrovni zásob z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="c5b99-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c5b99-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci informací na úrovni zásob z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c5b99-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c5b99-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="c5b99-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c5b99-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="c5b99-106">Templates and tasks</span></span>
<span data-ttu-id="c5b99-107">Následující šablony a základní úkoly se používají k synchronizaci úprav zásob na skladě a převodů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c5b99-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c5b99-108">**Šablona v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="c5b99-108">**Template in Data integration**</span></span>
- <span data-ttu-id="c5b99-109">Zásob produktu (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="c5b99-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="c5b99-110">**Úkol v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="c5b99-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="c5b99-111">Zásoby produktu</span><span class="sxs-lookup"><span data-stu-id="c5b99-111">Product inventory</span></span>

<span data-ttu-id="c5b99-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace množství zásob:</span><span class="sxs-lookup"><span data-stu-id="c5b99-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="c5b99-113">Sklady (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="c5b99-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="c5b99-114">Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej)</span><span class="sxs-lookup"><span data-stu-id="c5b99-114">Field Service products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c5b99-115">Sada entit</span><span class="sxs-lookup"><span data-stu-id="c5b99-115">Entity set</span></span>

| <span data-ttu-id="c5b99-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="c5b99-116">Field Service</span></span>                      | <span data-ttu-id="c5b99-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c5b99-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="c5b99-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="c5b99-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="c5b99-119">CDS zásoby na skladě podle skladu</span><span class="sxs-lookup"><span data-stu-id="c5b99-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="c5b99-120">Tok entity</span><span class="sxs-lookup"><span data-stu-id="c5b99-120">Entity flow</span></span>
<span data-ttu-id="c5b99-121">Informace o množství zásob z aplikace Finance and Operations jsou pro vybrané produkty odeslány do služby Field Service.</span><span class="sxs-lookup"><span data-stu-id="c5b99-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="c5b99-122">Informace na úrovni zásob zahrnují:</span><span class="sxs-lookup"><span data-stu-id="c5b99-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="c5b99-123">Množství na skladě (aktuální evidované fyzické množství, které se nachází ve skladu)</span><span class="sxs-lookup"><span data-stu-id="c5b99-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="c5b99-124">Množství objednávky (celkové zaznamenané množství na objednávce, jako jsou prodejní objednávky)</span><span class="sxs-lookup"><span data-stu-id="c5b99-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="c5b99-125">Objednané množství (celkové zaznamenané objednané množství, jako jsou prodejní objednávky)</span><span class="sxs-lookup"><span data-stu-id="c5b99-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="c5b99-126">Tyto informace jsou zaznamenány pro uvolněný produkt pro každý sklad a synchronizovány podle sledování změn, když se změní úroveň zásob.</span><span class="sxs-lookup"><span data-stu-id="c5b99-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="c5b99-127">Ve službě Field Service, řešení integrace vytváří deníky zásob pro deltu, takže úrovně ve službě Field Service odpovídají množstvím v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c5b99-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="c5b99-128">Aplikace Finance and Operations bude sloužit jako hlavní zdro pro úroveň zásob.</span><span class="sxs-lookup"><span data-stu-id="c5b99-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="c5b99-129">Proto je důležité nastavit integraci pro pracovní příkazy, převody a opravy ze služby Field Service do aplikace Finance and Operations, pokud se tato funkce používá ve službě Field Service, dohromady se synchronizací množství zásob z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c5b99-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="c5b99-130">Produkty a sklady, kde jsou zásoby řízení z aplikace Finance and Operations lze ovládat pomocí Rozšířeného dotazu a filtrování (Power Query).</span><span class="sxs-lookup"><span data-stu-id="c5b99-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="c5b99-131">Poznámka: Je možné vytvořit více skladů ve službě Field Services (pomocí **Je externě spravován = Ne**) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="c5b99-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="c5b99-132">Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c5b99-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="c5b99-133">V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c5b99-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="c5b99-134">Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt ve Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="c5b99-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c5b99-135">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="c5b99-135">Field Service CRM solution</span></span>
<span data-ttu-id="c5b99-136">Entita **zásoby externího produktu** je nová entita, která se používá pouze pro jištění při integraci.</span><span class="sxs-lookup"><span data-stu-id="c5b99-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="c5b99-137">Tato entita přijme integrované hodnoty úrovně zásob z aplikace Finance and Operations a potom tyto hodnoty transformuje do deníků ručních zásob, které poté změní produkty zásob skladu.</span><span class="sxs-lookup"><span data-stu-id="c5b99-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c5b99-138">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="c5b99-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="c5b99-139">Projekt integrace dat</span><span class="sxs-lookup"><span data-stu-id="c5b99-139">Data integration project</span></span>
<span data-ttu-id="c5b99-140">Můžete použít filtry s pokročilým dotazováním a filtrování, pomocí kterých lze řídit, že informace o zásobách budou z aplikace Finance and Operations do služby Field Service odesílat pouze požadované produkty a sklady.</span><span class="sxs-lookup"><span data-stu-id="c5b99-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c5b99-141">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="c5b99-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="c5b99-142">Zásoby produktu (z aplikace Finance and Operations do služby Field Service): zásoby produktu</span><span class="sxs-lookup"><span data-stu-id="c5b99-142">Product inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="c5b99-143">[![Mapování šablony v integraci dat](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="c5b99-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
