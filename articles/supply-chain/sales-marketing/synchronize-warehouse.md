---
title: "Synchronizujte sklady z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci skladů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="799dc-103">Synchronizujte sklady z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="799dc-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="799dc-104">Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci skladů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="799dc-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="799dc-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="799dc-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="799dc-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="799dc-106">Templates and tasks</span></span>
<span data-ttu-id="799dc-107">Následující šablona a základní úlohy, které se používají k synchronizaci skladů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 or Field Service.</span><span class="sxs-lookup"><span data-stu-id="799dc-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="799dc-108">**Název šablony v integraci dat:**</span><span class="sxs-lookup"><span data-stu-id="799dc-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="799dc-109">Sklady (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="799dc-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="799dc-110">**Názvy úkolů v projektu integrace dat:**</span><span class="sxs-lookup"><span data-stu-id="799dc-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="799dc-111">Sklad</span><span class="sxs-lookup"><span data-stu-id="799dc-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="799dc-112">Sada entit</span><span class="sxs-lookup"><span data-stu-id="799dc-112">Entity set</span></span>
| <span data-ttu-id="799dc-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="799dc-113">Field Service</span></span>    | <span data-ttu-id="799dc-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="799dc-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="799dc-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="799dc-115">msdyn_warehouses</span></span> | <span data-ttu-id="799dc-116">Sklady</span><span class="sxs-lookup"><span data-stu-id="799dc-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="799dc-117">Tok entity</span><span class="sxs-lookup"><span data-stu-id="799dc-117">Entity flow</span></span>
<span data-ttu-id="799dc-118">Sklady vytvořené a spravované v aplikaci Finance and Operations lze synchronizovat se službu Field Service prostřednictvím projektu integrace dat Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="799dc-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="799dc-119">Požadované sklady, které jsou synchronizovány do služby Field Service, je možné v projektu řídit pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="799dc-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="799dc-120">Sklady, které se synchronizují z aplikace Finance and Operations, jsou vytvořeny ve službě Field Service, kde je pole externě nastaveno na Ano a záznam je určen pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="799dc-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="799dc-121">Řešení služby CRM Field Service K podpoře integrace mezi moduly Field Service a Finance and Operations jsou požadovány další funkce z řešení služby CRM Field Service.</span><span class="sxs-lookup"><span data-stu-id="799dc-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="799dc-122">Řešení obsahuje následující změny.</span><span class="sxs-lookup"><span data-stu-id="799dc-122">The solution includes the following changes.</span></span>
<span data-ttu-id="799dc-123">Pole **udržovány externě je** bylo přidáno do entity **skladu (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="799dc-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="799dc-124">Toto pole napomáhá identifikovat, zda je sklad řízen operacemi nebo zda existuje pouze ve službě Field Service.</span><span class="sxs-lookup"><span data-stu-id="799dc-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="799dc-125">Ano – Sklad pochází z aplikace Finance and Operations a nebude ho možné upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="799dc-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="799dc-126">Ne – Sklad byl zadán přímo do služby Field Service a je zde udržován.</span><span class="sxs-lookup"><span data-stu-id="799dc-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="799dc-127">Pole **Externě spravován** pomáhá řídit synchronizaci úrovní zásob, úprav, převody a použití u pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="799dc-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="799dc-128">Pouze sklady se stavem **externě spravován** = Ano lze použít k synchronizaci přímo ke stejnému skladu v jiném systému.</span><span class="sxs-lookup"><span data-stu-id="799dc-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="799dc-129">Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí **Je externě spravován** = Ne) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="799dc-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="799dc-130">Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="799dc-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="799dc-131">V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="799dc-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="799dc-132">Zobrazit další informace v Synchronizovat úpravy zásob ze služby Field Service do aplikace Finance and Operations a v Synchronizovat pracovní příkazy ve službě Field Service do prodejních objednávce propojených s projektem v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="799dc-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="799dc-133">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="799dc-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="799dc-134">V projektu Integrace dat</span><span class="sxs-lookup"><span data-stu-id="799dc-134">In the Data Integration project</span></span>
<span data-ttu-id="799dc-135">Před synchronizací skladů je nutné aktualizovat rozšířený dotaz a filtrování projektu, aby byly zahrnuty pouze sklady, které chcete převést z aplikace Finance and Operations do služby Field Service.</span><span class="sxs-lookup"><span data-stu-id="799dc-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="799dc-136">Upozorňujeme, že budete potřebovat sklad ve službě Field Service, abyste jej mohli použít na pracovní příkazy, úpravy a převody.</span><span class="sxs-lookup"><span data-stu-id="799dc-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="799dc-137">Ujistěte se, že **klíč integrace** existuje pro **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="799dc-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="799dc-138">Přejít na integraci dat</span><span class="sxs-lookup"><span data-stu-id="799dc-138">Go to Data Integration</span></span>
2. <span data-ttu-id="799dc-139">Vyberte kartu **nastavit připojení**.</span><span class="sxs-lookup"><span data-stu-id="799dc-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="799dc-140">Vyberte sadu připojení použitou při synchronizaci pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="799dc-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="799dc-141">Vyberte kartu **klíč integrace**</span><span class="sxs-lookup"><span data-stu-id="799dc-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="799dc-142">Vyhledejte msdyn_warehouses a zkontrolujte, že je přidán klíč **msdyn_name (name)**.</span><span class="sxs-lookup"><span data-stu-id="799dc-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="799dc-143">Pokud se nezobrazuje, přidejte ho klepnutím na tlačítko **Přidat klíč** a klepněte na tlačítko **Uložit** v horní části stránky</span><span class="sxs-lookup"><span data-stu-id="799dc-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="799dc-144">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="799dc-144">Template mapping in Data integration</span></span>

<span data-ttu-id="799dc-145">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="799dc-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="799dc-146">Sklady (z aplikace Finance and Operations do služby Field Service): sklad</span><span class="sxs-lookup"><span data-stu-id="799dc-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="799dc-147">[![Mapování šablony v integraci dat](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="799dc-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

