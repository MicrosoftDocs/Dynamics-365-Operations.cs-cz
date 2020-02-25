---
title: Přehled výstrah
description: Toto téma obsahuje obecné informace o výstrahách. Výstrahy lze používat k informování o událostech, které mají být sledovány během pracovního dne.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 12fadd8387054db3e19d4136555724c23548e05c
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031012"
---
# <a name="alerts-overview"></a><span data-ttu-id="248ec-104">Přehled výstrah</span><span class="sxs-lookup"><span data-stu-id="248ec-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="248ec-105">O výstrahách</span><span class="sxs-lookup"><span data-stu-id="248ec-105">About alerts</span></span>
<span data-ttu-id="248ec-106">Výstrahy tvoří systém oznámení pro kritické události v systému.</span><span class="sxs-lookup"><span data-stu-id="248ec-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="248ec-107">Výstrahy lze používat k informování o událostech, které mají být sledovány během pracovního dne.</span><span class="sxs-lookup"><span data-stu-id="248ec-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="248ec-108">Můžete snadno vytvořit vlastní pravidla výstrah, abyste byli upozorněni na zpožděné dodávky, smazané objednávky, změny cen nebo jiné události, na které musíte reagovat.</span><span class="sxs-lookup"><span data-stu-id="248ec-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="248ec-109">Při plánování podnikových zdrojů (ERP) existují některé typické scénáře, kde lze použít funkci výstrahy.</span><span class="sxs-lookup"><span data-stu-id="248ec-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="248ec-110">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="248ec-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="248ec-111">Scénář 1: Vytvoření pravidla výstrahy pro nové prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="248ec-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="248ec-112">Otevřete stránku **Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="248ec-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="248ec-113">V podokně akcí na kartě **Možnosti** ve skupině **Sdílení** vyberte **vytvořit vlastní oznámení**.</span><span class="sxs-lookup"><span data-stu-id="248ec-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="248ec-114">V dialogovém okně **vytvořit pravidlo výstrahy** na pevné záložce **Upozornit mě při** v poli **Událost** vyberte **Záznam byl vytvořen**.</span><span class="sxs-lookup"><span data-stu-id="248ec-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="248ec-115">Scénář 2: Vytvoření pravidla výstrahy pro odložení data doručení</span><span class="sxs-lookup"><span data-stu-id="248ec-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="248ec-116">Otevřete stránku **Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="248ec-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="248ec-117">Vyberte ID nákupní objednávky pro přístup k podrobnostem o nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="248ec-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="248ec-118">Rozbalte pevnou záložku **Záhlaví nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="248ec-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="248ec-119">V podokně akcí na kartě **Možnosti** ve skupině **Sdílení** vyberte **vytvořit vlastní oznámení**.</span><span class="sxs-lookup"><span data-stu-id="248ec-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="248ec-120">V dialogovém okně **vytvořit pravidlo výstrahy** na pevné záložce **Upozornit mě při** v poli **Událost** vyberte **Datum doručení**.</span><span class="sxs-lookup"><span data-stu-id="248ec-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="248ec-121">V poli **Událost** vyberte **Bylo odloženo**.</span><span class="sxs-lookup"><span data-stu-id="248ec-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="248ec-122">Po ukončení dialogového okna **Vytvořit pravidlo výstrahy** se zobrazí vaše pravidlo zobrazí na stránce **Správa pravidel výstrah**.</span><span class="sxs-lookup"><span data-stu-id="248ec-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="248ec-123">Můžete použít stránku **Správa pravidel výstrah** k aktualizaci existujících pravidel výstrah.</span><span class="sxs-lookup"><span data-stu-id="248ec-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="248ec-124">Můžete například upravit aktivační události, aktualizovat události oznámení a aktualizovat data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="248ec-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="248ec-125">Chcete-li otevřít stránku **Správa pravidel výstrah**, použijte tlačítko **Upozornit mě** na kartě **Možnosti** podokna akcí.</span><span class="sxs-lookup"><span data-stu-id="248ec-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="248ec-126">Co se stane, když se vytvoří pravidlo výstrahy?</span><span class="sxs-lookup"><span data-stu-id="248ec-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="248ec-127">Při vytváření pravidel výstrah můžete přidružit k určitému poli předem definované události.</span><span class="sxs-lookup"><span data-stu-id="248ec-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="248ec-128">Například nastane datum zadané v poli nebo se změní obsah pole.</span><span class="sxs-lookup"><span data-stu-id="248ec-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="248ec-129">Rovněž je možné přiřadit událost záznamům na konkrétní stránce.</span><span class="sxs-lookup"><span data-stu-id="248ec-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="248ec-130">Například je vytvořen záznam nebo odstraněn záznam.</span><span class="sxs-lookup"><span data-stu-id="248ec-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="248ec-131">Vyskytne-li se u daného pole nebo u záznamu na stránce vybraná událost, odešle se vám výstraha.</span><span class="sxs-lookup"><span data-stu-id="248ec-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="248ec-132">Například vytvoříte pravidlo, ve kterém přiřadíte **datum dodání** na řádek specifické nákupní objednávky s událostí **splatnost před určitou dobou**.</span><span class="sxs-lookup"><span data-stu-id="248ec-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="248ec-133">Časový rámec nastavíte na pět dní.</span><span class="sxs-lookup"><span data-stu-id="248ec-133">You set the time frame to five days.</span></span> <span data-ttu-id="248ec-134">V tomto případě se výstraha odešle pět dnů po datu doručení tohoto řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="248ec-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="248ec-135">Dále můžete upřesnit pravidla výstrah nastavením podmínek.</span><span class="sxs-lookup"><span data-stu-id="248ec-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="248ec-136">Například můžete být informováni o nových nákupních objednávkách vytvořených pro konkrétní dodavatele.</span><span class="sxs-lookup"><span data-stu-id="248ec-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="248ec-137">Příprava pro výstrahu</span><span class="sxs-lookup"><span data-stu-id="248ec-137">Preparing for an alert</span></span>

<span data-ttu-id="248ec-138">Před nastavením pravidla výstrahy rozhodněte, kdy nebo za jakých situací chcete přijímat výstrahy.</span><span class="sxs-lookup"><span data-stu-id="248ec-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="248ec-139">Pokud víte, o kterých událostech chcete být vyrozuměni, vyhledejte v aplikaci stránku, kde se zobrazují data, která událost způsobila.</span><span class="sxs-lookup"><span data-stu-id="248ec-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="248ec-140">Událost může být nadcházející datum nebo nastalá specifická změna.</span><span class="sxs-lookup"><span data-stu-id="248ec-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="248ec-141">Musíte tedy vyhledat stránku, kde je zadáno datum, nebo kde se objevuje pole, které se změní, nebo nový záznam, který je vytvořen.</span><span class="sxs-lookup"><span data-stu-id="248ec-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="248ec-142">Jakmile máte tyto informace k dispozici, můžete vytvořit pravidlo výstrahy.</span><span class="sxs-lookup"><span data-stu-id="248ec-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="248ec-143">Komponenty pravidla výstrahy</span><span class="sxs-lookup"><span data-stu-id="248ec-143">Components of an alert rule</span></span>

<span data-ttu-id="248ec-144">Pravidlo výstrahy obsahuje pět komponent:</span><span class="sxs-lookup"><span data-stu-id="248ec-144">An alert rule has five components:</span></span>

- <span data-ttu-id="248ec-145">**Událost** – událost, která spouští pravidlo výstrahy, může být datum nebo nastalá specifická změna, ke které dochází.</span><span class="sxs-lookup"><span data-stu-id="248ec-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="248ec-146">Události definujete na pevné záložce **Odeslat e-mailové výstrahy pro změny stavu úlohy** dialogového okna **vytvořit pravidlo výstrahy**.</span><span class="sxs-lookup"><span data-stu-id="248ec-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="248ec-147">**Podmínka** – na pevné záložce **Upozornit mě na** v dialogovém okně **Vytvořit pravidlo výstrahy** můžete vybrat rozsah podmínky, chcete-li řídit, kdy budete upozorňováni na události.</span><span class="sxs-lookup"><span data-stu-id="248ec-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="248ec-148">Můžete použít pravidlo buď pouze pro aktuální záznam nebo na všechny viditelné záznamy na stránce.</span><span class="sxs-lookup"><span data-stu-id="248ec-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="248ec-149">Pokud se pravidlo platí mezi právnickými osobami, můžete nastavit **celoorganizační** možnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="248ec-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="248ec-150">**Uplynutí platnosti pravidla** – na pevné záložce **Upozornit mě do** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, jak dlouho má být pravidlo výstrahy aktivní.</span><span class="sxs-lookup"><span data-stu-id="248ec-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="248ec-151">**Obsah** – na pevné záložce **Upozornit mě pomocí** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit text předmětu a text zprávy, kterou by zprávy s výstrahou měly používat.</span><span class="sxs-lookup"><span data-stu-id="248ec-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="248ec-152">**Uživatel** – na pevné záložce **Příjemce výstrahy** dialogového okna **Vytvořit pravidlo výstrahy** můžete určit, který uživatel by měl přijímat zprávy s výstrahou.</span><span class="sxs-lookup"><span data-stu-id="248ec-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="248ec-153">ID uživatele je ve výchozím nastavení vybráno.</span><span class="sxs-lookup"><span data-stu-id="248ec-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="248ec-154">Tato možnost je omezen na správce organizace.</span><span class="sxs-lookup"><span data-stu-id="248ec-154">This option is restricted to organization administrators.</span></span>

## <a name="email-notifications-from-alerts"></a><span data-ttu-id="248ec-155">E-mailová oznámení z výstrah</span><span class="sxs-lookup"><span data-stu-id="248ec-155">Email notifications from alerts</span></span>

<span data-ttu-id="248ec-156">E-mailová oznámení z výstrah dosud nejsou povolena.</span><span class="sxs-lookup"><span data-stu-id="248ec-156">Email notifications from alerts are not yet enabled.</span></span> <span data-ttu-id="248ec-157">To bude k dispozici v budoucí aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="248ec-157">This will be enabled in a future update.</span></span>

## <a name="videos"></a><span data-ttu-id="248ec-158">Videa</span><span class="sxs-lookup"><span data-stu-id="248ec-158">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="248ec-159">Jak používat výstrahy ke sledování filtrovaných dat</span><span class="sxs-lookup"><span data-stu-id="248ec-159">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="248ec-160">Video [Jak používat výstrahy ke sledování filtrovaných dat](https://youtu.be/ZYKMcv6kl9s) (zobrazeno výše) je zahrnuto v [Playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupné na YouTube.</span><span class="sxs-lookup"><span data-stu-id="248ec-160">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="248ec-161">Možnosti pravidla výstrahy</span><span class="sxs-lookup"><span data-stu-id="248ec-161">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="248ec-162">Video [Možnosti pravidel výstrah](https://youtu.be/cpzimwOjicM)  (zobrazené výše) je zahrnuto do [Playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.</span><span class="sxs-lookup"><span data-stu-id="248ec-162">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


