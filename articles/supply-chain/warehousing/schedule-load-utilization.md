---
title: "Naplánovat využití vytížení"
description: "Toto téma vysvětluje postup při nastavení a plánování vytížení v určitém skladu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 15f3735f79671ac41789d39a5473722a5f35fde0
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="schedule-load-utilization"></a><span data-ttu-id="0789d-103">Naplánovat využití vytížení</span><span class="sxs-lookup"><span data-stu-id="0789d-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0789d-104">Můžete naplánovat zatížení využití typů vybraného umístění a také projektovat současné i budoucí využití zatížení.</span><span class="sxs-lookup"><span data-stu-id="0789d-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="0789d-105">Může projektovat vytížení jednoho nebo více míst, pro měrné zatížení jednotek (zóna nebo sklad) nebo kombinace zóny a skladu.</span><span class="sxs-lookup"><span data-stu-id="0789d-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="0789d-106">Plánování a zobrazení zatížení pro sklad nebo místo</span><span class="sxs-lookup"><span data-stu-id="0789d-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="0789d-107">Chcete-li naplánovat zatížení míst, skladů nebo zón, vytvořte nastavení využití prostoru a přidružte ho s hlavním plánem.</span><span class="sxs-lookup"><span data-stu-id="0789d-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="0789d-108">V nastavení využití místa, můžete použít typy skladových míst, například **Hromadná umístění** a **výdejní skladové místo** k určení, jak by mělo být využití místa naplánováno.</span><span class="sxs-lookup"><span data-stu-id="0789d-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="0789d-109">Můžete také určit režimu vytížení skladu, jako například **Pásmo**.</span><span class="sxs-lookup"><span data-stu-id="0789d-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="0789d-110">Projekte budoucího využití místa vychází z informací, které se počítají z přidruženého hlavního plánu.</span><span class="sxs-lookup"><span data-stu-id="0789d-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="0789d-111">Hlavní plány předpovídají plánování zdrojů pro příchozí a odchozí příkazy pro výrobu a operace.</span><span class="sxs-lookup"><span data-stu-id="0789d-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="0789d-112">Projekce volného místa je založena na vztahu mezi nastavením využití prostoru a vybraným hlavním plánem.</span><span class="sxs-lookup"><span data-stu-id="0789d-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="0789d-113">Pomocí režimu vytížení jednotky zvolené v nastavení využití prostoru určíte, zda vytížení by mělo být plánované pro každý sklad nebo zónu nebo zda má projektování zahrnovat informace o skladu i o zóně.</span><span class="sxs-lookup"><span data-stu-id="0789d-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="0789d-114">Můžete také určit, zda by blokovaná umístění měla být vyloučena z výpočtů pro využití zatížení.</span><span class="sxs-lookup"><span data-stu-id="0789d-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="0789d-115">Využití místa lze projektovat generováním sestavy **využití vytížení skladu**.</span><span class="sxs-lookup"><span data-stu-id="0789d-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="0789d-116">Při generování sestavy můžete určit, zda se využití vytížení má projektovat pro každé místo, pro všechny místa nebo pro vybrané jednotky vytížení, například pásmo nebo sklad.</span><span class="sxs-lookup"><span data-stu-id="0789d-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="0789d-117">Tvorba nastavení využití prostorů pro sklad</span><span class="sxs-lookup"><span data-stu-id="0789d-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="0789d-118">Vyberte **řízení zásob** \> **nastavení** \> **sledování skladu** \> **Využití místa**.</span><span class="sxs-lookup"><span data-stu-id="0789d-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="0789d-119">Chcete-li vytvořit nastavení využití místa, klikněte na položku **Nové**.</span><span class="sxs-lookup"><span data-stu-id="0789d-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="0789d-120">Zadejte ID a název pro nové nastavení.</span><span class="sxs-lookup"><span data-stu-id="0789d-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="0789d-121">V poli **Režim vytížení skladu** vyberte, zda by měl přehled využití místa určován podle skladu, zóny, nebo skladu a zóny.</span><span class="sxs-lookup"><span data-stu-id="0789d-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="0789d-122">Nastavte možnost **vyloučit blokován umístění** na **Ano** k vyloučení blokovaných skladových míst z výpočtu volného místa.</span><span class="sxs-lookup"><span data-stu-id="0789d-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="0789d-123">Skladové místo můžete blokovat pro vstup a výstup určením důvodu blokování v poli **Blokovaný vstup** nebo **Blokovaný výstup** na pevné záložce **Jiné** na stránce **Skladovací místa**.</span><span class="sxs-lookup"><span data-stu-id="0789d-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="0789d-124">Na pevné záložce **Typ místa** vyberte typy umístění, které chcete zahrnout do výpočtu využití prostoru.</span><span class="sxs-lookup"><span data-stu-id="0789d-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="0789d-125">Je nutné vybrat alespoň jeden typ umístění pro projektování.</span><span class="sxs-lookup"><span data-stu-id="0789d-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="0789d-126">Přidružte nastavení využití prostoru hlavního plánu</span><span class="sxs-lookup"><span data-stu-id="0789d-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="0789d-127">Vyberte **Řízení zásob** \> **Periodické úkoly** \> **Naplánovat využití vytížení**.</span><span class="sxs-lookup"><span data-stu-id="0789d-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="0789d-128">V poli **hlavní plán** vyberte hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="0789d-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="0789d-129">V poli **Počet dní** zadejte počet dní, které chcete zahrnout do projektování aktuálního a budoucího pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="0789d-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="0789d-130">V poli **Využití místa** vyberte nastavení využití místa pro projektování aktuálního a budoucího pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="0789d-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="0789d-131">Zadejte informace o projektování a zobrazení vytížení využití</span><span class="sxs-lookup"><span data-stu-id="0789d-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="0789d-132">Vyberte **řízení zásob** \> **dotazy a sestavy** \> **sestavy fyzických zásob** \> **využití vytížení skladu**.</span><span class="sxs-lookup"><span data-stu-id="0789d-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="0789d-133">V poli **Zobrazit podle** vyberte úroveň projektování využití prostoru:</span><span class="sxs-lookup"><span data-stu-id="0789d-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="0789d-134">**Web** – Projekt k projektování využití prostoru pro každé místo.</span><span class="sxs-lookup"><span data-stu-id="0789d-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="0789d-135">Toto projektování je užitečné, pokud například chcete zobrazit všechny sklady v místě, takže můžete vyrovnávat využití prostoru mezi sklady.</span><span class="sxs-lookup"><span data-stu-id="0789d-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="0789d-136">**Jednotka vytížení** – projekt k projektování využití prostoru zón či skladů.</span><span class="sxs-lookup"><span data-stu-id="0789d-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="0789d-137">Dostupné místo je poté projektované podle hodnoty, kterou jste vybrali v poli **režim vytížení úložiště** na stránce **využití místa** při vytváření nastavení využití místa.</span><span class="sxs-lookup"><span data-stu-id="0789d-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="0789d-138">Proveďte některý z následujících kroků v závislosti na hodnotě, kterou jste vybrali v předchozím kroku:</span><span class="sxs-lookup"><span data-stu-id="0789d-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="0789d-139">Pokud jste vybrali v poli **Zobrazit podle** možnost **Web**, bude k dispozici pole **Web**.</span><span class="sxs-lookup"><span data-stu-id="0789d-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="0789d-140">Vyberte jedno nebo více pracovišť, které chcete zahrnout do projektování.</span><span class="sxs-lookup"><span data-stu-id="0789d-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="0789d-141">Pokud jste vybrali v poli **Zobrazit podle** možnost **Jednotka vytížení**, bude k dispozici pole **Jednotka vytížení**.</span><span class="sxs-lookup"><span data-stu-id="0789d-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="0789d-142">Vyberte jednotku vytížení.</span><span class="sxs-lookup"><span data-stu-id="0789d-142">Select the load unit.</span></span>

4. <span data-ttu-id="0789d-143">V poli **Typ vytížení** vyberte **Objem** nebo **Hmotnost** pro označení provozní jednotky skladu, pro který se má projektovat prostor.</span><span class="sxs-lookup"><span data-stu-id="0789d-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="0789d-144">V poli **Nastavení využití prostoru** vyberte nastavení využití prostoru, na kterém by mělo být projektování založeno.</span><span class="sxs-lookup"><span data-stu-id="0789d-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>

