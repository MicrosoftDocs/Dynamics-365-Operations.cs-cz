---
title: Synchronizace skladů z aplikace Supply Chain Management do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skladů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0c0c1bafb5b36bb9ddc00061e0040a199c8c033d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010840"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="322d7-103">Synchronizace skladů z aplikace Supply Chain Management do služby Field Service</span><span class="sxs-lookup"><span data-stu-id="322d7-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="322d7-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skladů z Dynamics 365 Supply Chain Management do Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="322d7-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="322d7-105">[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="322d7-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="322d7-106">Šablony a úkoly</span><span class="sxs-lookup"><span data-stu-id="322d7-106">Templates and tasks</span></span>
<span data-ttu-id="322d7-107">Následující šablona a základní úlohy se používají k synchronizaci skladů ze Supply Chain Management do Field Service.</span><span class="sxs-lookup"><span data-stu-id="322d7-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="322d7-108">**Šablona v integraci dat**</span><span class="sxs-lookup"><span data-stu-id="322d7-108">**Template in Data integration**</span></span>
- <span data-ttu-id="322d7-109">Sklady (z aplikace Supply Chain Management do služby Field Service)</span><span class="sxs-lookup"><span data-stu-id="322d7-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="322d7-110">**Úkol v projektu integrace dat**</span><span class="sxs-lookup"><span data-stu-id="322d7-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="322d7-111">Sklad</span><span class="sxs-lookup"><span data-stu-id="322d7-111">Warehouse</span></span>

## <a name="table-set"></a><span data-ttu-id="322d7-112">Nastavení tabulky</span><span class="sxs-lookup"><span data-stu-id="322d7-112">Table set</span></span>
| <span data-ttu-id="322d7-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="322d7-113">Field Service</span></span>    | <span data-ttu-id="322d7-114">Správa dodavatelsko-odběratelského řetězce</span><span class="sxs-lookup"><span data-stu-id="322d7-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="322d7-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="322d7-115">msdyn_warehouses</span></span> | <span data-ttu-id="322d7-116">Sklady</span><span class="sxs-lookup"><span data-stu-id="322d7-116">Warehouses</span></span>                             |

## <a name="table-flow"></a><span data-ttu-id="322d7-117">Tok tabulky</span><span class="sxs-lookup"><span data-stu-id="322d7-117">Table flow</span></span>
<span data-ttu-id="322d7-118">Sklady vytvořené a spravované v aplikaci Supply Chain Management lze synchronizovat se službu Field Service prostřednictvím projektu integrace dat Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="322d7-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="322d7-119">Požadované sklady, které chcete synchronizovat do služby Field Service, je možné v projektu řídit pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="322d7-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="322d7-120">Sklady, které se synchronizují z aplikace Supply Chain Management, jsou vytvořeny ve sloupci **Field Service, kde je pole Je spravováno externě** nastaveno na **Ano** a záznam je určen pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="322d7-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** column set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="322d7-121">Řešení Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="322d7-121">Field Service CRM solution</span></span>
<span data-ttu-id="322d7-122">K podpoře integrace mezi Field Service a Supply Chain Management jsou požadovány další funkce z řešení služby CRM Field Service.</span><span class="sxs-lookup"><span data-stu-id="322d7-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="322d7-123">V řešení byl sloupec **Je externě udržováno** přidáno do sloupce **Sklad (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="322d7-123">In the solution, the **Is Maintained Externally** column has been added to the **Warehouse (msdyn_warehouses)** table.</span></span> <span data-ttu-id="322d7-124">Tento sloupec napomáhá identifikovat, zda je sklad řízen z aplikace Supply Chain Management nebo zda existuje pouze ve službě Field Service.</span><span class="sxs-lookup"><span data-stu-id="322d7-124">This column helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="322d7-125">Nastavení tohoto sloupce zahrnuje:</span><span class="sxs-lookup"><span data-stu-id="322d7-125">The settings for this column include:</span></span>
- <span data-ttu-id="322d7-126">**Ano** – Sklad pochází z aplikace Supply Chain Management a nebude ho možné upravovat v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="322d7-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="322d7-127">**Ne** – Sklad byl zadán přímo do služby Field Service a je zde udržován.</span><span class="sxs-lookup"><span data-stu-id="322d7-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="322d7-128">Sloupec **Je externě spravován** pomáhá řídit synchronizaci úrovní zásob, úprav, převody a použití u pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="322d7-128">The **Is Externally Maintained** column helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="322d7-129">Pouze sklady se stavem **Je externě spravován** je nastaveno na **Ano** lze použít k synchronizaci přímo ke stejnému skladu v jiném systému.</span><span class="sxs-lookup"><span data-stu-id="322d7-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="322d7-130">Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí **Je externě spravován** = Ne) a poté je namapovat do jediného skladu pomocí funkce filtrování a pokročilých dotazů.</span><span class="sxs-lookup"><span data-stu-id="322d7-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="322d7-131">Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="322d7-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="322d7-132">V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="322d7-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="322d7-133">Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) a [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt ve Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="322d7-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="322d7-134">Nastavení mapování a předpokladů</span><span class="sxs-lookup"><span data-stu-id="322d7-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="322d7-135">Projekt integrace dat</span><span class="sxs-lookup"><span data-stu-id="322d7-135">Data Integration project</span></span>
<span data-ttu-id="322d7-136">Před synchronizací skladů je nutné aktualizovat rozšířený dotaz a filtrování projektu, aby byly zahrnuty pouze sklady, které chcete převést z aplikace Supply Chain Management do služby Field Service.</span><span class="sxs-lookup"><span data-stu-id="322d7-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="322d7-137">Upozorňujeme, že budete potřebovat sklad ve službě Field Service, abyste jej mohli použít na pracovní příkazy, úpravy a převody.</span><span class="sxs-lookup"><span data-stu-id="322d7-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="322d7-138">Ujistěte se, že **klíč integrace** existuje pro **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="322d7-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="322d7-139">Přjděte na integraci dat.</span><span class="sxs-lookup"><span data-stu-id="322d7-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="322d7-140">Vyberte kartu **Nastavení připojení**.</span><span class="sxs-lookup"><span data-stu-id="322d7-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="322d7-141">Vyberte sadu připojení použitou při synchronizaci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="322d7-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="322d7-142">Vyberte kartu **klíč integrace**.</span><span class="sxs-lookup"><span data-stu-id="322d7-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="322d7-143">Vyhledejte msdyn_warehouses a potvrďte, že je přidán klíč **msdyn_name (name)**.</span><span class="sxs-lookup"><span data-stu-id="322d7-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="322d7-144">Pokud se nezobrazuje, přidejte ho kliknutím na tlačítko **Přidat klíč** a klikněte na tlačítko **Uložit** v horní části stránky</span><span class="sxs-lookup"><span data-stu-id="322d7-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="322d7-145">Mapování šablony v integraci dat</span><span class="sxs-lookup"><span data-stu-id="322d7-145">Template mapping in Data integration</span></span>

<span data-ttu-id="322d7-146">Na následujícím obrázku je příklad mapování šablony v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="322d7-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="322d7-147">Sklady (z aplikace Supply Chain Management do služby Field Service): Sklad</span><span class="sxs-lookup"><span data-stu-id="322d7-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="322d7-148">[![Mapování šablony v integraci dat](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="322d7-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
