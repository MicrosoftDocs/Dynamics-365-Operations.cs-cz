---
title: Oznámení o provedení vlny
description: Toto téma popisuje oznámení o provedení vlny a vysvětluje, jak je nastavit.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838075"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="8af4e-103">Oznámení o provedení vlny</span><span class="sxs-lookup"><span data-stu-id="8af4e-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8af4e-104">Funkce *Oznámení o provedení vlny* používá obchodní události a centrum akcí k doručování oznámení, která souvisejí s prováděním vln.</span><span class="sxs-lookup"><span data-stu-id="8af4e-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="8af4e-105">Umožňuje určit typy událostí, které generují oznámení, sklady, které je generují, a uživatele, kteří je dostávají.</span><span class="sxs-lookup"><span data-stu-id="8af4e-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="8af4e-106">Tlačítko **Zobrazit zprávy** (symbol zvonku) na pravé straně navigační lišty označuje, kdy je pro aktuálního uživatele k dispozici zpráva z centra akcí.</span><span class="sxs-lookup"><span data-stu-id="8af4e-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="8af4e-107">Uživatel může tlačítkem **Zobrazit zprávy** otevřít centrum akcí a zkontrolovat zprávy.</span><span class="sxs-lookup"><span data-stu-id="8af4e-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="8af4e-108">K podnikovým událostem dochází při spuštění obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="8af4e-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="8af4e-109">Obchodní procesy jsou tvořeny úkoly.</span><span class="sxs-lookup"><span data-stu-id="8af4e-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="8af4e-110">Během obchodního procesu provádějí uživatelé, kteří se na něm podílejí, obchodní akce, kterými plní tyto úkoly.</span><span class="sxs-lookup"><span data-stu-id="8af4e-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="8af4e-111">Obchodní události poskytují mechanismus, který umožňuje externím systémům přijímat oznámení z aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8af4e-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="8af4e-112">Tímto způsobem mohou systémy provádět obchodní akce v reakci na obchodní události.</span><span class="sxs-lookup"><span data-stu-id="8af4e-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="8af4e-113">Další informace naleznete v tématu [Přehled obchodních událostí](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="8af4e-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="8af4e-114">Zapnutí funkce Oznámení o provedení vlny</span><span class="sxs-lookup"><span data-stu-id="8af4e-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="8af4e-115">Než můžete použít funkci *Oznámení o provedení vlny*, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="8af4e-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="8af4e-116">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="8af4e-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8af4e-117">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="8af4e-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8af4e-118">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="8af4e-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8af4e-119">**Název funkce:** *Zapnutí funkce Oznámení o provedení vlny*</span><span class="sxs-lookup"><span data-stu-id="8af4e-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="8af4e-120">Scénář: Odeslání oznámení o provedení dávky vlny do centra akcí</span><span class="sxs-lookup"><span data-stu-id="8af4e-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="8af4e-121">Tento scénář ukazuje kompletní tok pro odesílání oznámení o chybách při provádění dávky vlny zadané roli prostřednictvím centra akcí.</span><span class="sxs-lookup"><span data-stu-id="8af4e-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="8af4e-122">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="8af4e-122">Make demo data available</span></span>

<span data-ttu-id="8af4e-123">Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="8af4e-124">Ujistěte se, že vlny běží v dávkovém režimu</span><span class="sxs-lookup"><span data-stu-id="8af4e-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="8af4e-125">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="8af4e-126">Na pevné záložce **Zpracování vlny** nastavte možnost **Zpracovat vlny v dávce** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="8af4e-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="8af4e-127">Pokud chcete zakázat oznámení o provádění dávkových vln, nastavte možnost **Zakázat oznámení o dávkách zpracování vlny** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="8af4e-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="8af4e-128">Konfigurace zásad oznámení o vlně</span><span class="sxs-lookup"><span data-stu-id="8af4e-128">Configure a wave notification policy</span></span>

<span data-ttu-id="8af4e-129">Zásady oznámení o vlně definují typy oznámení, která se odesílají, a uživatele, kteří jsou upozorněni.</span><span class="sxs-lookup"><span data-stu-id="8af4e-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="8af4e-130">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Zásady oznámení o vlně**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="8af4e-131">Vytvořte záznam, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="8af4e-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="8af4e-132">**Zásady oznámení o vlně** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="8af4e-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="8af4e-133">**Popis:** *Chyba dávky vlny skladu 24*</span><span class="sxs-lookup"><span data-stu-id="8af4e-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="8af4e-134">**Odeslat oznámení při:** *Pouze chyba*</span><span class="sxs-lookup"><span data-stu-id="8af4e-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="8af4e-135">**Roli:** *Správce systému*</span><span class="sxs-lookup"><span data-stu-id="8af4e-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="8af4e-136">Protože tento scénář používá ukázková data, role *Správce systému* je vybrána pro zjednodušení.</span><span class="sxs-lookup"><span data-stu-id="8af4e-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="8af4e-137">Protože jste přihlášeni jako správce systému, obdržíte oznámení.</span><span class="sxs-lookup"><span data-stu-id="8af4e-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="8af4e-138">V praxi byste však měli vybrat konkrétnější roli, které budou chodit oznámení o chybách při provádění dávek vln, například *Manažer skladu*.</span><span class="sxs-lookup"><span data-stu-id="8af4e-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="8af4e-139">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="8af4e-140">Konfigurujte šablonu vlny</span><span class="sxs-lookup"><span data-stu-id="8af4e-140">Configure a wave template</span></span>

<span data-ttu-id="8af4e-141">Šablony vln vám umožní propojit konkrétní příklady vlnových metod s odpovídajícími šablonami popisků vln.</span><span class="sxs-lookup"><span data-stu-id="8af4e-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="8af4e-142">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="8af4e-143">V podokně seznamu nastavte pole **Typ šablony vlny** na *Expedice* a potom vyberte šablonu vlny *Výchozí expedice 24* pro sklad 24.</span><span class="sxs-lookup"><span data-stu-id="8af4e-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="8af4e-144">Na pevné záložce **Obecné** nastavte pole **Zásady oznámení o vlně** na *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="8af4e-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="8af4e-145">Konfigurace šablony práce</span><span class="sxs-lookup"><span data-stu-id="8af4e-145">Configure a work template</span></span>

<span data-ttu-id="8af4e-146">Šablony práce se používají při provádění vln pro generování práce.</span><span class="sxs-lookup"><span data-stu-id="8af4e-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="8af4e-147">V tomto scénáři by provedení vlny mělo vyvolat chybu.</span><span class="sxs-lookup"><span data-stu-id="8af4e-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="8af4e-148">Nastavením dotazu šablony práce na použití neexistujícího skladu zajistíte, že se provedení vlny nezdaří, a proto dojde k odeslání oznámení.</span><span class="sxs-lookup"><span data-stu-id="8af4e-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="8af4e-149">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8af4e-150">V podokně seznamu nastavte pole **Typ šablony práce** na *Prodejní objednávky* a potom vyberte šablonu práce *24 SO Stage* pro sklad 24.</span><span class="sxs-lookup"><span data-stu-id="8af4e-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="8af4e-151">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8af4e-152">V dialogovém okně editoru dotazů na kartě **Rozsah** upravte následující řádek (nebo jej přidejte, pokud neexistuje):</span><span class="sxs-lookup"><span data-stu-id="8af4e-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="8af4e-153">**Tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="8af4e-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="8af4e-154">**Odvozená tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="8af4e-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="8af4e-155">**Pole:** *Sklad*</span><span class="sxs-lookup"><span data-stu-id="8af4e-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="8af4e-156">**Kritéria:** Změňte hodnotu z *24* na *Chyba*.</span><span class="sxs-lookup"><span data-stu-id="8af4e-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="8af4e-157">Vyberte **OK** a potvrďte změnu.</span><span class="sxs-lookup"><span data-stu-id="8af4e-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="8af4e-158">Vytvořte prodejní objednávku a uvolněte ji do skladu</span><span class="sxs-lookup"><span data-stu-id="8af4e-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="8af4e-159">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="8af4e-160">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="8af4e-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8af4e-161">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8af4e-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8af4e-162">**Sklad:** *24*</span><span class="sxs-lookup"><span data-stu-id="8af4e-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="8af4e-163">Na záložce s náhledem **Řádky prodejní objednávky** přidejte prodejní objednávku s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="8af4e-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="8af4e-164">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8af4e-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="8af4e-165">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="8af4e-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="8af4e-166">Tyto položky a množství jsou pouze příklady.</span><span class="sxs-lookup"><span data-stu-id="8af4e-166">These items and quantities are only examples.</span></span> <span data-ttu-id="8af4e-167">Zadaný sklad musí obsahovat dostatečný sklad.</span><span class="sxs-lookup"><span data-stu-id="8af4e-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="8af4e-168">V době, kdy je vybrán nový řádek na záložce s náhledem **Řádky prodejní objednávky**, vyberte na panelu nástrojů **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="8af4e-169">Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="8af4e-170">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="8af4e-170">Then close the page.</span></span>
1. <span data-ttu-id="8af4e-171">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="8af4e-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="8af4e-172">Oznámení o provedení dávkové úlohy vlny</span><span class="sxs-lookup"><span data-stu-id="8af4e-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="8af4e-173">V závislosti na nastavení vašich obchodních událostí nakonec obdržíte oznámení o selhání provedení vlny.</span><span class="sxs-lookup"><span data-stu-id="8af4e-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="8af4e-174">Zpráva centra akcí bude vypadat jako v následujícím příkladu a bude obsahovat odkaz na vlnu, která selhala.</span><span class="sxs-lookup"><span data-stu-id="8af4e-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="8af4e-175">**Chyba během provedení vlny**</span><span class="sxs-lookup"><span data-stu-id="8af4e-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="8af4e-176">Při provádění vlny USMF-000000001 došlo k chybě.</span><span class="sxs-lookup"><span data-stu-id="8af4e-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="8af4e-177">Poslední zprávy: Pro vlnu USMF-000000001 nebyla vytvořena žádná práce.</span><span class="sxs-lookup"><span data-stu-id="8af4e-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="8af4e-178">**STAV**</span><span class="sxs-lookup"><span data-stu-id="8af4e-178">**STATUS**</span></span>  
> <span data-ttu-id="8af4e-179">Aktivní</span><span class="sxs-lookup"><span data-stu-id="8af4e-179">Active</span></span>
>
> <span data-ttu-id="8af4e-180">Otevřít podrobnosti vlny</span><span class="sxs-lookup"><span data-stu-id="8af4e-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
