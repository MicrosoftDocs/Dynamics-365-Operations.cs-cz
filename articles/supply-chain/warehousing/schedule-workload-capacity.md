---
title: Plánování pracovního vytížení
description: Toto téma vysvětluje postup při nastavení a plánování kapacity pracovního vytížení pro zaměstnance v určitém skladu nebo pro celý sklad.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4225d9e7ad65939c57cb770ba521377c87dea3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217257"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="29d03-103">Plánování pracovního vytížení</span><span class="sxs-lookup"><span data-stu-id="29d03-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29d03-104">Můžete naplánovat kapacitu pracovního vytížení pro sklady a také projektovat současné i budoucí pracovní vytížení pro pracovníky v jednotlivých skladech.</span><span class="sxs-lookup"><span data-stu-id="29d03-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="29d03-105">Můžete projektovat pracovní vytížení pro celý sklad, nebo můžete pracovní vytížení projektovat odděleně pro příchozí a odchozí pracovní vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="29d03-106">Aby bylo možné projektování výstupu pracovního vytížení pro vybrané sklady, data hlavního plánování musí být k dispozici pro tyto sklady.</span><span class="sxs-lookup"><span data-stu-id="29d03-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="29d03-107">Další informace o hlavních plánech naleznete v tématu [Přehled hlavních plánů](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="29d03-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="29d03-108">Plánování a zobrazení pracovního vytížení skladu</span><span class="sxs-lookup"><span data-stu-id="29d03-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="29d03-109">Pokud chcete naplánovat kapacitu pracovního vytížení pro sklad, vytvořte nastavení pracovního vytížení pro jeden nebo více skladů a poté nastavení pracovního vytížení přidružte k hlavnímu plánu.</span><span class="sxs-lookup"><span data-stu-id="29d03-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="29d03-110">V nastavení kapacity pracovního vytížení lze definovat limity na základě hmotnosti nebo objemu pro příchozí a odchozí transakce.</span><span class="sxs-lookup"><span data-stu-id="29d03-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="29d03-111">Můžete také vytvořit více než jedno nastavení pro každý sklad a potom nastavení přidružit k jednotlivým hlavním plánům.</span><span class="sxs-lookup"><span data-stu-id="29d03-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="29d03-112">Tento přístup můžete například využít v souladu se sezónními změnami stavu zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="29d03-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="29d03-113">Pokud zaměstnanci skladu pracují s transakcemi pro příchozí i odchozí pracovní vytížení, můžete nastavení kapacity skladu nakonfigurovat pro plánování pracovního vytížení v kombinovaném zobrazení.</span><span class="sxs-lookup"><span data-stu-id="29d03-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="29d03-114">Abyste mohli plánovat a zobrazovat pracovní vytížení pro sklady, musíte provést následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="29d03-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="29d03-115">Vytvořte nastavení kapacity pracovního vytížení a definujte limity kapacity pracovního vytížení pro jeden nebo více skladů.</span><span class="sxs-lookup"><span data-stu-id="29d03-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="29d03-116">Přidružte nastavení kapacity pracovního vytížení k hlavnímu plánu, abyste mohli vytvářet projekce pracovního vytížení a určit, jak dlouho budou tyto projekce platit.</span><span class="sxs-lookup"><span data-stu-id="29d03-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="29d03-117">Vytvoření nastavení kapacity pracovního vytížení pro sklad</span><span class="sxs-lookup"><span data-stu-id="29d03-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="29d03-118">Vyberte **řízení zásob** \> **nastavení** \> **sledování skladu** \> **Kapacita pracovního vytížení**.</span><span class="sxs-lookup"><span data-stu-id="29d03-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="29d03-119">V podokně akcí vyberte **nový** k vytvoření nastavení kapacity pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="29d03-120">Na pevné záložce **Sklady** vyberte **Nový**, a potom zadejte hodnoty do řádku, čímž přidružíte sklad k nastavení kapacity pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="29d03-121">Zaškrtněte políčko **kombinované vstupní a výstupní pracovní vytížení**, pokud by sestava **Kapacita pracovního vytížení** měla zobrazit celkové vytížení pro příchozí a odchozí transakce.</span><span class="sxs-lookup"><span data-stu-id="29d03-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="29d03-122">Na pevné záložce **Typy transakce** vyberte typy příchozích a odchozích transakcí, na které se budou limity pracovního vytížení vztahovat.</span><span class="sxs-lookup"><span data-stu-id="29d03-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29d03-123">Je nutné vybrat alespoň jeden typ transakce pro příchozí i odchozí pracovní vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="29d03-124">Definování limitů objemu nebo hmotnosti</span><span class="sxs-lookup"><span data-stu-id="29d03-124">Define limits for volume or weight</span></span>

<span data-ttu-id="29d03-125">Můžete nastavit limity pro objem či hmotnost podle toho, která omezení jsou relevantní pro zaměstnance skladu.</span><span class="sxs-lookup"><span data-stu-id="29d03-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="29d03-126">Limity, které zadáte, jsou součástí projekce kapacity pracovního vytížení, kterou najdete v sestavě **Kapacita pracovního vytížení**.</span><span class="sxs-lookup"><span data-stu-id="29d03-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="29d03-127">Pro účely projekce informací o objemu a hmotnosti položek musí být pro všechny produkty určen standardní objem jedné skladové položky a hmotnost jedné skladové položky.</span><span class="sxs-lookup"><span data-stu-id="29d03-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="29d03-128">Pole, která jsou vyžadována, jsou k dispozici v následujících skupinách polí na pevné záložce **správa skladu** stránky **podrobnosti uvolnění produktu**:</span><span class="sxs-lookup"><span data-stu-id="29d03-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="29d03-129">Manipulace</span><span class="sxs-lookup"><span data-stu-id="29d03-129">Handling</span></span>
- <span data-ttu-id="29d03-130">Fyzické rozměry</span><span class="sxs-lookup"><span data-stu-id="29d03-130">Physical dimensions</span></span>
- <span data-ttu-id="29d03-131">Měření hmotnosti</span><span class="sxs-lookup"><span data-stu-id="29d03-131">Weight measurements</span></span>

<span data-ttu-id="29d03-132">Pokud tyto informace nejsou správně zadány, zobrazí se zpráva při generování sestavy **Kapacita pracovního zatížení**.</span><span class="sxs-lookup"><span data-stu-id="29d03-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="29d03-133">Ze sestavy se pak můžete dostat až k chybějícím informacím, které jsou potřeba k projekci budoucího pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="29d03-134">Přidružení nastavení kapacity pracovního vytížení k hlavnímu plánu</span><span class="sxs-lookup"><span data-stu-id="29d03-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="29d03-135">Vyberte **řízení zásob** \> **Periodicky** \> **pracovní vytížení plánu**.</span><span class="sxs-lookup"><span data-stu-id="29d03-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="29d03-136">V poli **Hlavní plán** vyberte hlavní plán k použití pro projekce pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="29d03-137">V poli **Počet dní** zadejte počet dní, které má projekce pracovního vytížení pokrývat.</span><span class="sxs-lookup"><span data-stu-id="29d03-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="29d03-138">V poli **pracovní vytížení** vyberte nastavení pracovního vytížení, které má být přidruženo k hlavnímu plánu.</span><span class="sxs-lookup"><span data-stu-id="29d03-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="29d03-139">Zobrazení kapacity pracovního vytížení</span><span class="sxs-lookup"><span data-stu-id="29d03-139">View workload capacity</span></span>

1. <span data-ttu-id="29d03-140">Vyberte **řízení zásob** \> **dotazy a sestavy** \> **sestavy fyzických zásob** \> **kapacita pracovního vytížení**.</span><span class="sxs-lookup"><span data-stu-id="29d03-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="29d03-141">V poli **Počet sloupců** určete počet sloupců, které chcete zobrazit v sestavě.</span><span class="sxs-lookup"><span data-stu-id="29d03-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="29d03-142">V poli **typ objednávky** vyberte **plánované a potvrzené**, **plánováno** nebo **potvrzeno** k označení typu objednávek pro plánování v sestavě.</span><span class="sxs-lookup"><span data-stu-id="29d03-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="29d03-143">V poli **Typ vytížení** výběrem typu vytížení určete, zda má být kapacita pracovního vytížení projektována v paletách, objemu či hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="29d03-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="29d03-144">V poli **Kapacita pracovního vytížení** vyberte nastavení kapacity pracovního vytížení.</span><span class="sxs-lookup"><span data-stu-id="29d03-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
