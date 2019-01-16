---
title: "Synchronizujte informace o množství zásob z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci informací i mnoství zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="bd890-103">Synchronizujte informace o množství zásob z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="bd890-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bd890-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci informací i mnoství zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="bd890-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="bd890-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="bd890-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="bd890-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="bd890-106">Templates and tasks</span></span>
<span data-ttu-id="bd890-107">Následující šablona a základní úlohy, které se používají k synchronizaci dostupného množství zásob z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 or Field Service.</span><span class="sxs-lookup"><span data-stu-id="bd890-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="bd890-108">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="bd890-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="bd890-109">Zásob produktu (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="bd890-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="bd890-110">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="bd890-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="bd890-111">Zásoby produktu</span><span class="sxs-lookup"><span data-stu-id="bd890-111">Product inventory</span></span>

<span data-ttu-id="bd890-112">Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace množství zásob:</span><span class="sxs-lookup"><span data-stu-id="bd890-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="bd890-113">Sklady (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="bd890-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="bd890-114">Produkty služby Field Service s jednotkou zásob (z aplikace Finance and Operations do služby Prodej)</span><span class="sxs-lookup"><span data-stu-id="bd890-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="bd890-115">Sada entit</span><span class="sxs-lookup"><span data-stu-id="bd890-115">Entity set</span></span>

| <span data-ttu-id="bd890-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="bd890-116">Field Service</span></span>                      | <span data-ttu-id="bd890-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bd890-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="bd890-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="bd890-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="bd890-119">CDS zásoby na skladě podle skladu</span><span class="sxs-lookup"><span data-stu-id="bd890-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="bd890-120">Tok entity</span><span class="sxs-lookup"><span data-stu-id="bd890-120">Entity flow</span></span>
<span data-ttu-id="bd890-121">Informace o množství zásob z aplikace Finance and Operations jsou pro vybrané produkty odeslány do služby Field Service.</span><span class="sxs-lookup"><span data-stu-id="bd890-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="bd890-122">Skladové úrovně informace zahrnují:</span><span class="sxs-lookup"><span data-stu-id="bd890-122">The inventory level information include:</span></span> 
- <span data-ttu-id="bd890-123">Množství na skladě (aktuální evidované fyzické množství, které se nachází ve skladu)</span><span class="sxs-lookup"><span data-stu-id="bd890-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="bd890-124">Množství objednávky (celkové zaznamenané množství na objednávce - tj. prodejní objednávky)</span><span class="sxs-lookup"><span data-stu-id="bd890-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="bd890-125">Objednané množství (celkové zaznamenané objednané množství - tj. prodejní objednávky)</span><span class="sxs-lookup"><span data-stu-id="bd890-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="bd890-126">Tyto informace jsou zaznamenány pro uvolněný produkt pro každý sklad a synchronizovány podle sledování změn, když se změní úroveň zásob.</span><span class="sxs-lookup"><span data-stu-id="bd890-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="bd890-127">Ve službě Field Service, řešení integrace tvorby deníků zásob pro deltu, pro získání množství ve službě Field Service, aby odpovídaly množstvím v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bd890-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="bd890-128">Aplikace Finance and Operations bude sloužit jako hlavní zdro pro úroveň zásob.</span><span class="sxs-lookup"><span data-stu-id="bd890-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="bd890-129">Proto je důležité nastavit integrace pro zakázky, převody a opravy ze služby Field Service do aplikace Finance and Operations, pokud se tato funkce používá ve službě Field Service, dohromady se synchronizací množství zásob z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bd890-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="bd890-130">Produkty a sklady, kde jsou zásoby řízení z aplikace Finance and Operations lze ovládat pomocí Rozšířeného dotazu a filtrování (Power Query).</span><span class="sxs-lookup"><span data-stu-id="bd890-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="bd890-131">Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí Je externě spravován = Ne) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="bd890-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="bd890-132">Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bd890-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="bd890-133">V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bd890-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="bd890-134">Zobrazit další informace v Synchronizovat úpravy zásob ze služby Field Service do aplikace Finance and Operations a v Synchronizovat pracovní příkazy ve službě Field Service do prodejních objednávce propojených s projektem v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bd890-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="bd890-135">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="bd890-135">Field Service CRM solution</span></span>
<span data-ttu-id="bd890-136">Entita zásoby externího produktu je nová entita, která se používá pouze v integraci.</span><span class="sxs-lookup"><span data-stu-id="bd890-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="bd890-137">Přijme integrované hodnoty úrovně zásob z aplikace Finance and Operations a potom tyto hodnoty transformuje do deníků ručních zásob, které poté změní produkty zásob skladu.</span><span class="sxs-lookup"><span data-stu-id="bd890-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="bd890-138">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="bd890-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="bd890-139">V projektu Integrace dat</span><span class="sxs-lookup"><span data-stu-id="bd890-139">In the Data Integration project</span></span>
<span data-ttu-id="bd890-140">Použijte filtry s pokročilým dotazováním a filtrování, pomocí kterých lze řídit, že informace o zásobách budou z aplikace Finance and Operations do služby Field Service odesílat pouze požadované produkty a sklady.</span><span class="sxs-lookup"><span data-stu-id="bd890-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bd890-141">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="bd890-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="bd890-142">Zásoby produktu (z aplikace Finance and Operations do služby Field Service): zásoby produktu</span><span class="sxs-lookup"><span data-stu-id="bd890-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="bd890-143">[![Mapování šablony v integraci dat](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="bd890-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

