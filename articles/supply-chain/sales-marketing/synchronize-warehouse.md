---
title: Synchronizujte sklady z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skladů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "340308"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="3a8fd-103">Synchronizace skladů z aplikace Finance and Operations do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="3a8fd-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3a8fd-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skladů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="3a8fd-105">[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="3a8fd-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3a8fd-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="3a8fd-106">Templates and tasks</span></span>
<span data-ttu-id="3a8fd-107">Následující šablona a základní úlohy slouží ke spuštění synchronizace skladů z Microsoft Dynamics 365 for Finance and Operations k Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="3a8fd-108">**Šablona v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="3a8fd-108">**Template in Data integration**</span></span>
- <span data-ttu-id="3a8fd-109">Sklady (z aplikace Finance and Operations do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="3a8fd-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="3a8fd-110">**Úkol v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="3a8fd-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="3a8fd-111">Sklad</span><span class="sxs-lookup"><span data-stu-id="3a8fd-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="3a8fd-112">Sada entit</span><span class="sxs-lookup"><span data-stu-id="3a8fd-112">Entity set</span></span>
| <span data-ttu-id="3a8fd-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="3a8fd-113">Field Service</span></span>    | <span data-ttu-id="3a8fd-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3a8fd-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="3a8fd-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="3a8fd-115">msdyn_warehouses</span></span> | <span data-ttu-id="3a8fd-116">Sklady</span><span class="sxs-lookup"><span data-stu-id="3a8fd-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="3a8fd-117">Tok entity</span><span class="sxs-lookup"><span data-stu-id="3a8fd-117">Entity flow</span></span>
<span data-ttu-id="3a8fd-118">Sklady vytvořené a spravované v aplikaci Finance and Operations lze synchronizovat se službu Field Service prostřednictvím projektu integrace dat Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="3a8fd-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="3a8fd-119">Požadované sklady, které chcete synchronizovat do služby Field Service, je možné v projektu řídit pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="3a8fd-120">Sklady, které se synchronizují z aplikace Finance and Operations, jsou vytvořeny ve službě **Field Service, kde je pole Je spravováno externě** nastaveno na **Ano** a záznam je určen pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="3a8fd-121">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="3a8fd-121">Field Service CRM solution</span></span>
<span data-ttu-id="3a8fd-122">K podpoře integrace mezi moduly Field Service a Finance and Operations jsou požadovány další funkce z řešení služby CRM Field Service.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="3a8fd-123">V řešení bylo pole **Je externě udržováno** přidáno do entity **Sklad (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="3a8fd-124">Toto pole napomáhá identifikovat, zda je sklad řízen z modulu Finance and Operations nebo zda existuje pouze ve službě Field Service.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="3a8fd-125">Nastavení tohoto pole zahrnuje:</span><span class="sxs-lookup"><span data-stu-id="3a8fd-125">The settings for this field include:</span></span>
- <span data-ttu-id="3a8fd-126">**Ano** – Sklad pochází z aplikace Finance and Operations a nebude ho možné upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="3a8fd-127">**Ne** – Sklad byl zadán přímo do služby Field Service a je zde udržován.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="3a8fd-128">Pole **Je externě spravován** pomáhá řídit synchronizaci úrovní zásob, úprav, převody a použití u pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="3a8fd-129">Pouze sklady se stavem **Je externě spravován** je nastaveno na **Ano** lze použít k synchronizaci přímo ke stejnému skladu v jiném systému.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="3a8fd-130">Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí **Je externě spravován** = Ne) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="3a8fd-131">Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="3a8fd-132">V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="3a8fd-133">Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt ve Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="3a8fd-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3a8fd-134">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="3a8fd-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="3a8fd-135">Projekt integrace dat</span><span class="sxs-lookup"><span data-stu-id="3a8fd-135">Data Integration project</span></span>
<span data-ttu-id="3a8fd-136">Před synchronizací skladů je nutné aktualizovat rozšířený dotaz a filtrování projektu, aby byly zahrnuty pouze sklady, které chcete převést z aplikace Finance and Operations do služby Field Service.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="3a8fd-137">Upozorňujeme, že budete potřebovat sklad ve službě Field Service, abyste jej mohli použít na pracovní příkazy, úpravy a převody.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="3a8fd-138">Ujistěte se, že **klíč integrace** existuje pro **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="3a8fd-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="3a8fd-139">Přjděte na integraci dat.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="3a8fd-140">Vyberte kartu **Nastavení připojení**.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="3a8fd-141">Vyberte sadu připojení použitou při synchronizaci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="3a8fd-142">Vyberte kartu **klíč integrace**.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="3a8fd-143">Vyhledejte msdyn_warehouses a potvrďte, že je přidán klíč **msdyn_name (name)**.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="3a8fd-144">Pokud se nezobrazuje, přidejte ho kliknutím na tlačítko **Přidat klíč** a klikněte na tlačítko **Uložit** v horní části stránky</span><span class="sxs-lookup"><span data-stu-id="3a8fd-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3a8fd-145">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="3a8fd-145">Template mapping in Data integration</span></span>

<span data-ttu-id="3a8fd-146">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="3a8fd-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="3a8fd-147">Sklady (z aplikace Finance and Operations do služby Field Service): sklad</span><span class="sxs-lookup"><span data-stu-id="3a8fd-147">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="3a8fd-148">[![Mapování šablony v integraci dat](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="3a8fd-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
