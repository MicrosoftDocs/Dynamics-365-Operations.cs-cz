---
title: Vytvoření pracovních příkazů
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy v modulu Správa majetku.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 76306fb31e7e5297e6a5d64b97b5bd09b64349ee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500567"
---
# <a name="creating-work-orders"></a><span data-ttu-id="7f606-103">Vytvoření pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="7f606-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f606-104">Po naplánování úloh preventivní údržby pro ně můžete v dalším kroku vytvořit pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="7f606-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="7f606-105">Tento krok můžete dokončit pomocí jednoho z plánů údržby.</span><span class="sxs-lookup"><span data-stu-id="7f606-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="7f606-106">Naplánované práce v rozvrhu údržby mohou mít různé typy odkazů, jak popisuje následující tabulka:</span><span class="sxs-lookup"><span data-stu-id="7f606-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="7f606-107">Typ odkazu</span><span class="sxs-lookup"><span data-stu-id="7f606-107">Reference type</span></span> | <span data-ttu-id="7f606-108">popis</span><span class="sxs-lookup"><span data-stu-id="7f606-108">Description</span></span> |
|---|---|
| <span data-ttu-id="7f606-109">Plány údržby</span><span class="sxs-lookup"><span data-stu-id="7f606-109">Maintenance plans</span></span> | <span data-ttu-id="7f606-110">Práce preventivní údržby na základě typů plánu údržby *Čas* nebo *Počítadlo*.</span><span class="sxs-lookup"><span data-stu-id="7f606-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="7f606-111">Pořadí údržby</span><span class="sxs-lookup"><span data-stu-id="7f606-111">Maintenance rounds</span></span> | <span data-ttu-id="7f606-112">Práce preventivní údržby obsahující několik majetků, které vyžadují podobný typ údržby.</span><span class="sxs-lookup"><span data-stu-id="7f606-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="7f606-113">Požadavek na údržbu</span><span class="sxs-lookup"><span data-stu-id="7f606-113">Maintenance request</span></span> | <span data-ttu-id="7f606-114">Ručně vytvořený požadavek na údržbu nebo opravu majetku.</span><span class="sxs-lookup"><span data-stu-id="7f606-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="7f606-115">Tento požadavek lze převést na pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="7f606-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="7f606-116">Vytvoření pracovních příkazů na základě plánu údržby</span><span class="sxs-lookup"><span data-stu-id="7f606-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="7f606-117">Chcete-li vytvořit pracovní příkazy, které jsou založeny na vašem plánu údržby, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7f606-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="7f606-118">Otevřete jednu z následujících stránek podle toho, jak chcete vybrat položky plánu pro své pracovní příkazy:</span><span class="sxs-lookup"><span data-stu-id="7f606-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="7f606-119">Všechen rozvrh údržby (**Správa majetku \> Rozvrh údržby \> Všechen rozvrh údržby**)</span><span class="sxs-lookup"><span data-stu-id="7f606-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="7f606-120">Otevřít řádky rozvrhu údržby (**Správa majetku \> Rozvrh údržby \> Otevřít řádky rozvrhu údržby**)</span><span class="sxs-lookup"><span data-stu-id="7f606-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="7f606-121">Otevřít fondy rozvrhu údržby (**Správa majetku \> Rozvrh údržby \> Otevřít fondy rozvrhu údržby**)</span><span class="sxs-lookup"><span data-stu-id="7f606-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="7f606-122">V mřížce zaškrtněte políčko u každé úlohy plánované údržby, pro kterou chcete vytvořit pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="7f606-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="7f606-123">Pak v podokně akcí vyberte možnost **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="7f606-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="7f606-124">Otevře se dialogové okno **Vytvořit pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="7f606-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="7f606-125">V poli **Hodiny prognózy údržby** se zobrazí celkový počet hodin prognózy pro vybrané řádky.</span><span class="sxs-lookup"><span data-stu-id="7f606-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Dialogové okno Vytvořit pracovní příkazy](media/18-preventive-maintenance.png)

1. <span data-ttu-id="7f606-127">V části **Parametry** zadejte počet pracovních příkazů, které mají být vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="7f606-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="7f606-128">Vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="7f606-128">Select one of the following options:</span></span>

    - <span data-ttu-id="7f606-129">**Jeden pracovní příkaz na řádek** - Vytvořte jeden pracovní příkaz na řádek plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="7f606-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="7f606-130">**Jeden pracovní příkaz na** - Vytvářejte pracovní příkazy, které jsou seskupeny podle nastavení ostatních možností, které budou k dispozici, když vyberete tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="7f606-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="7f606-131">V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu, který se má použít pro všechny pracovní příkazy, které vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="7f606-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="7f606-132">Vyberte **OK** k vytvoření pracovních příkazů podle vašeho nastavení.</span><span class="sxs-lookup"><span data-stu-id="7f606-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="7f606-133">Seskupte řádky pracovních příkazů, které se automaticky vytvářejí, když běží plán údržby</span><span class="sxs-lookup"><span data-stu-id="7f606-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="7f606-134">Tato funkce umožňuje definovat pravidla pro seskupování řádků pracovních příkazů do jednoho pracovního příkazu, když je systém nastaven na automatické generování pracovních příkazů na základě plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="7f606-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="7f606-135">Dříve mohly automaticky generované pracovní příkazy obsahovat pouze jeden řádek.</span><span class="sxs-lookup"><span data-stu-id="7f606-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="7f606-136">Nyní však můžete pracovní příkazy seskupovat například podle majetku, typu majetku nebo funkčního umístění.</span><span class="sxs-lookup"><span data-stu-id="7f606-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="7f606-137">(Ručně generované pracovní příkazy již lze tímto způsobem seskupit, jak je popsáno v předchozí části tohoto tématu.)</span><span class="sxs-lookup"><span data-stu-id="7f606-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="7f606-138">Povolení seskupování pro automaticky generované pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="7f606-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="7f606-139">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="7f606-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="7f606-140">Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="7f606-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="7f606-141">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="7f606-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7f606-142">**Modul:** *Správa majetku*</span><span class="sxs-lookup"><span data-stu-id="7f606-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="7f606-143">**Název funkce:** *(Náhled) Použít pravidla pro seskupování pracovních příkazů při provádění plánu údržby*</span><span class="sxs-lookup"><span data-stu-id="7f606-143">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="7f606-144">Nastavení seskupování pro automaticky generované pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="7f606-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="7f606-145">Při nastavení seskupování pro automaticky generované pracovní příkazy postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="7f606-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="7f606-146">Klikněte na **Správa majetku \> Nastavení \> Preventivní údržba \> Plány údržby**.</span><span class="sxs-lookup"><span data-stu-id="7f606-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="7f606-147">U každého plánu, kde chcete generovat seskupené pracovní příkazy, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="7f606-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="7f606-148">V podokně seznamu vyberte plán.</span><span class="sxs-lookup"><span data-stu-id="7f606-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="7f606-149">Na záložce s náhledem **Řádky** se ujistěte, že je na každém řádku zaškrtnuto políčko **Automaticky vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="7f606-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="7f606-150">Přejděte na **Správa majetku \> Periodické \> Preventivní údržba \> Rozvrhnout plány údržby**.</span><span class="sxs-lookup"><span data-stu-id="7f606-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="7f606-151">V dialogovém okně **Naplánovat rozvrhy údržby** v části **Období** určete časový horizont plánu (jak daleko se dívat dopředu při hledání úloh plánované údržby, pro které se má generovat práce).</span><span class="sxs-lookup"><span data-stu-id="7f606-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="7f606-152">Nastavte možnost **Automaticky vytvořit pracovní příkaz podle plánu** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="7f606-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="7f606-153">V oddílu **pracovní příkaz** vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="7f606-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="7f606-154">**Jeden pracovní příkaz na řádek** - Vytvořte jeden pracovní příkaz na řádek plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="7f606-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="7f606-155">(Tato možnost poskytuje stejnou funkcionalitu, která je k dispozici, když je vypnutá funkce *Použít pravidla pro seskupování pracovních příkazů při provádění plánu údržby*.)</span><span class="sxs-lookup"><span data-stu-id="7f606-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="7f606-156">**Jeden pracovní příkaz na** - Vytvářejte pracovní příkazy, které jsou seskupeny podle nastavení ostatních možností, které budou k dispozici, když vyberete tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="7f606-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="7f606-157">Pokud chcete, aby se možnosti uplatnily při spuštění pouze některých vašich plánů údržby, na kartě s náhledem **Záznamy, které mají být zahrnuty**, přidejte filtry podle potřeby, stejně jako to můžete udělat pro jiné dávkové úlohy v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7f606-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="7f606-158">Na kartě s náhledem **Spustit na pozadí** nastavte dávkové a plánovací možnosti, jak požadujete, stejně jako u jiných dávkových úloh v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7f606-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="7f606-159">Výběrem **OK** spusťte a/nebo naplánujte vybrané plány údržby.</span><span class="sxs-lookup"><span data-stu-id="7f606-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]