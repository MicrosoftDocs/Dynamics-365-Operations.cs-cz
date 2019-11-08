---
title: Rozvrhnout plány údržby
description: Toto téma popisuje rozvrhování plánů údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b9efd5bccdccf6ea19b105f3518bb2ef35ec857e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571270"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="f93d2-103">Rozvrhnout plány údržby</span><span class="sxs-lookup"><span data-stu-id="f93d2-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f93d2-104">Preventivní plánování údržby vygeneruje položky kalendáře na majetku na základě plánů údržby nastavených na majetku.</span><span class="sxs-lookup"><span data-stu-id="f93d2-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="f93d2-105">Můžete plánovat položky v kalendáři na základě vybraných plánů údržby, typů majetku a majetku.</span><span class="sxs-lookup"><span data-stu-id="f93d2-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="f93d2-106">Klikněte na **Správa majetku** > **Periodické** > **Preventivní údržba** > **Rozvrhnout plány údržby**.</span><span class="sxs-lookup"><span data-stu-id="f93d2-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="f93d2-107">V polích **Období** a **Frekvence** můžete vybrat časový interval.</span><span class="sxs-lookup"><span data-stu-id="f93d2-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="f93d2-108">Pole **Období** a **Frekvence období** určují, jak moc předem má být vytvořen řádek plánu údržby na základě plánů údržby, které jste vytvořili (založené na čase nebo na základě čítače).</span><span class="sxs-lookup"><span data-stu-id="f93d2-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="f93d2-109">Na následujícím obrázku jsou řádky plánu údržby (= návrhy pracovních příkazů) vytvořeny od aktuálního data po dobu tří měsíců.</span><span class="sxs-lookup"><span data-stu-id="f93d2-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="f93d2-110">V případě, že se mají automaticky vytvářet pracovní příkazy podle řádku plánu údržby, vyberte možnost Ano na kartě **Automaticky vytvořit, pokud je to uvedeno v řádku**.</span><span class="sxs-lookup"><span data-stu-id="f93d2-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="f93d2-111">Je-li toto přepínací tlačítko nastaveno na hodnotu „Ano“ *a* políčko **Automaticky vytvořit** je také zaškrtnuto na řádcích plánu údržby v **Plánech údržby**, budou vytvořeny pracovní příkazy na základě řádků plánu údržby a budou vytvořeny také řádky plánu údržby se stavem „Pracovní příkaz vytvořen“.</span><span class="sxs-lookup"><span data-stu-id="f93d2-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="f93d2-112">Je-li vybrána pouze jedna možnost (přepínač **Automaticky vytvořit, pokud je to uvedeno v řádku** v tomto dialogovém okně nebo zaškrtávací políčko **Automaticky vytvořit** ve formuláři **Plány údržby**), budou vytvořeny pouze řádky plánu údržby se stavem „Vytvořeno".</span><span class="sxs-lookup"><span data-stu-id="f93d2-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="f93d2-113">V takovém případě se žádné pracovní příkazy nevytvoří.</span><span class="sxs-lookup"><span data-stu-id="f93d2-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="f93d2-114">Je možné generovat položky kalendáře na základě plánů údržby (čas nebo čítač), majetku, typů majetku, funkčních míst a typů funkčních umístění.</span><span class="sxs-lookup"><span data-stu-id="f93d2-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="f93d2-115">Klepněte na tlačítko **Filtr** a proveďte výběr, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="f93d2-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="f93d2-116">V souvislosti s rozvrhováním plánů údržby ve funkčních místech: Pokud aktualizujete nastavení typů majetku, výrobců a modelů v plánech údržby na pevné záložce **Všechna funkční umístění** > **Plány údržby** po provedení plánovaných plánů údržby, existující položky plánu údržby vztahující se k tomuto funkčnímu umístění jsou automaticky odstraněny.</span><span class="sxs-lookup"><span data-stu-id="f93d2-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="f93d2-117">Chcete-li vytvořit nové položky kalendáře, které odpovídají nastavení aktualizovaného plánu údržby na funkčním místě, musíte pro toto funkční místo spustit nový plán plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="f93d2-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="f93d2-118">Další informace o nastavení typů majetku, výrobců a modelů ve funkčních umístěních naleznete v části [Vytváření funkčních míst](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="f93d2-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="f93d2-119">*Příklad:* chcete vytvořit plán údržby pro konkrétní funkční místo, což znamená, že všechny majetky nastavené v tomto funkčním místě budou při plánování plánu údržby zahrnuty v daném čase.</span><span class="sxs-lookup"><span data-stu-id="f93d2-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="f93d2-120">V takovém případě vytvořte plán údržby a vyberte konkrétní funkční místo, ale NEPŘIDÁVEJTE do plánu údržby žádná aktiva.</span><span class="sxs-lookup"><span data-stu-id="f93d2-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="f93d2-121">Výsledkem je, že při rozvrhování plánu údržby budou pro všechny majetky související se funkčním místem v daném okamžiku vytvořeny řádky plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="f93d2-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="f93d2-122">Pokud provedete změny typů majetku, výrobců a modelů v **Typech majetku**, budou tyto změny mít vliv pouze na nový majetek, který používá aktualizovaný typ majetku.</span><span class="sxs-lookup"><span data-stu-id="f93d2-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="f93d2-123">Další informace o nastavení typu majetku v [Typech majetku](../setup-for-objects/object-types.md)</span><span class="sxs-lookup"><span data-stu-id="f93d2-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="f93d2-124">Kliknutím na tlačítko **OK** zahájíte generování položek plánu údržby na majetku.</span><span class="sxs-lookup"><span data-stu-id="f93d2-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="f93d2-125">Vygenerované položky budou zobrazeny na stránce se seznamem **Všechny plány údržby**.</span><span class="sxs-lookup"><span data-stu-id="f93d2-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="f93d2-126">Následující ilustrace znázorňuje příklad sestavy **Plány rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="f93d2-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![Obrázek č. 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="f93d2-128">V dialogovém okně **Rozvrhnout plány údržby** můžete nastavit dávkové úlohy na pevné záložce **Spustit na pozadí** pro automatické generování položek kalendáře v pravidelných intervalech.</span><span class="sxs-lookup"><span data-stu-id="f93d2-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="f93d2-129">Při plánování preventivní údržby nebudou vytvořeny řádky plánu údržby s očekávaným počátečním datem a časem, které předchází systémovému datu a času.</span><span class="sxs-lookup"><span data-stu-id="f93d2-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="f93d2-130">Následující obrázek poskytuje grafické znázornění výpočtu plánu údržby založené na čase.</span><span class="sxs-lookup"><span data-stu-id="f93d2-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Obrázek č. 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="f93d2-132">V souvislosti s plány údržby založenými na čítačích: v následujících obrázcích jsou zobrazeny dva různé cykly registrace čítačů.</span><span class="sxs-lookup"><span data-stu-id="f93d2-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="f93d2-133">Jsou založeny na plánu údržby nastaveném pro majetek "V0001", což předpokládá, že majetek (auto) najede přibližně 2 000 km každý měsíc.</span><span class="sxs-lookup"><span data-stu-id="f93d2-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="f93d2-134">V prvním příkladu očekávaných 2 000 km není dosaženo každý měsíc.</span><span class="sxs-lookup"><span data-stu-id="f93d2-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="f93d2-135">Podle plánu údržby založeném na čítači je prahová hodnota 2 000 km, což znamená, že při spuštění plánování plánu údržby by měl být při každém dosažení prahové hodnoty 2 000 km vytvořen řádek plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="f93d2-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="f93d2-136">V příkladu 1 existují 4 řádky registrace, ale prahové hodnoty 2 000 km bylo dosaženo pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="f93d2-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="f93d2-137">To znamená, že když spustíte rozvržení plánu údržby, bude pro tento majetek, například v období 3 měsíců, vytvořen pouze jeden řádek plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="f93d2-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="f93d2-138">Na dalším obrázku je každý měsíc registrováno 2 000 km nebo více.</span><span class="sxs-lookup"><span data-stu-id="f93d2-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="f93d2-139">Pokud tedy naplánujete plány údržby pro tento majetek v období 3 měsíců, vytvoří se tři řádky údržby.</span><span class="sxs-lookup"><span data-stu-id="f93d2-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="f93d2-140">Zde popsané příklady znázorňují, že všechny registrace čítačů provedené na majetku ukazují trend popisující opotřebení majetku.</span><span class="sxs-lookup"><span data-stu-id="f93d2-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="f93d2-141">Tato funkce se používá jako základ výpočtu v době plánování plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="f93d2-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Obrázek č. 3](media/11-preventive-maintenance.png)

![Obrázek č. 4](media/12-preventive-maintenance.png)

