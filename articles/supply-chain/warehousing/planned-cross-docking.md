---
title: Plánovaný cross docking
description: Toto téma popisuje cross docking s rozšířeným plánováním, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti. Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017752"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="93c96-104">Cross docking s plánováním</span><span class="sxs-lookup"><span data-stu-id="93c96-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93c96-105">Toto téma popisuje cross docking s rozšířeným plánováním.</span><span class="sxs-lookup"><span data-stu-id="93c96-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="93c96-106">Cross docking s rozšířeným plánováním je skladový proces, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti.</span><span class="sxs-lookup"><span data-stu-id="93c96-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="93c96-107">Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="93c96-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="93c96-108">Cross docking umožňuje pracovníkům přeskočit zaskladnění zásob na vstupu a jejich výdej na výstupu, když jsou již zásoby označeny pro výstupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="93c96-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="93c96-109">Tím se všude tam, kde je to možné, minimalizuje počet operací se zásobami.</span><span class="sxs-lookup"><span data-stu-id="93c96-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="93c96-110">Protože se redukuje množství interakce se systémem, lze též dosáhnout dalších časových i prostorových úspor ve skladu.</span><span class="sxs-lookup"><span data-stu-id="93c96-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="93c96-111">Před spuštěním cross dockingu musí uživatel nakonfigurovat novou šablonu pro cross docking, jež bude splňovat požadavky na zdroj dodávky a další.</span><span class="sxs-lookup"><span data-stu-id="93c96-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="93c96-112">Po vytvoření odchozí objednávky musí být řádek označen proti příchozí objednávce obsahující stejnou položku.</span><span class="sxs-lookup"><span data-stu-id="93c96-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="93c96-113">V době přijetí příchozí objednávky nastavení cross dockingu automaticky identifikuje potřebu cross dockingu a na základě nastavení směrnice skladového místa vytvoří příslušný pohyb pro požadované množství.</span><span class="sxs-lookup"><span data-stu-id="93c96-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="93c96-114">U transakcí se zásobami se **neprovede** zrušení registrace, je-li zrušena crossdockingová úloha, a to ani v případě, že je nastavení této funkcionality v parametrech správy skladu zapnuto.</span><span class="sxs-lookup"><span data-stu-id="93c96-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="93c96-115">Zapnutí funkce Cross docking s plánováním</span><span class="sxs-lookup"><span data-stu-id="93c96-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="93c96-116">Funkci Cross docking s rozšířeným plánováním můžete používat až poté, co ji ve svém systému zapnete.</span><span class="sxs-lookup"><span data-stu-id="93c96-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="93c96-117">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="93c96-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="93c96-118">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="93c96-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="93c96-119">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="93c96-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="93c96-120">**Název funkce:** *Cross docking s plánováním*</span><span class="sxs-lookup"><span data-stu-id="93c96-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="93c96-121">Nastavení</span><span class="sxs-lookup"><span data-stu-id="93c96-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="93c96-122">Obnovte metody účtování nákladu</span><span class="sxs-lookup"><span data-stu-id="93c96-122">Regenerate load posting methods</span></span>

<span data-ttu-id="93c96-123">Cross docking s plánováním se implementuje jako metoda účtování nákladu.</span><span class="sxs-lookup"><span data-stu-id="93c96-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="93c96-124">Po zapnutí funkce je nutné obnovit metody.</span><span class="sxs-lookup"><span data-stu-id="93c96-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="93c96-125">Přejděte do **Řízení skladu \> Nastavení \> Metody účtování nákladů**.</span><span class="sxs-lookup"><span data-stu-id="93c96-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="93c96-126">V podokně Akce vyberte možnost **Obnovit metody**.</span><span class="sxs-lookup"><span data-stu-id="93c96-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="93c96-127">Po dokončení obnovy byste měli vidět metodu, jež má v poli **Název metody** hodnotu *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="93c96-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="93c96-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="93c96-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="93c96-129">Vytvoření šablony cross dockingu</span><span class="sxs-lookup"><span data-stu-id="93c96-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="93c96-130">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Šablony cross dockingu**.</span><span class="sxs-lookup"><span data-stu-id="93c96-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="93c96-131">V podokně Akce vyberte možnost **Nový** a vytvořte šablonu.</span><span class="sxs-lookup"><span data-stu-id="93c96-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="93c96-132">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="93c96-133">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="93c96-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="93c96-134">Toto pole definuje pořadí, ve kterém budou šablony vyhodnocovány.</span><span class="sxs-lookup"><span data-stu-id="93c96-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="93c96-135">**ID šablony cross dockingu:** *51*</span><span class="sxs-lookup"><span data-stu-id="93c96-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="93c96-136">**Popis:** *Sklad 51*</span><span class="sxs-lookup"><span data-stu-id="93c96-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="93c96-137">**Zásady uvolnění poptávky:** *Před přijetím dodávky*</span><span class="sxs-lookup"><span data-stu-id="93c96-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="93c96-138">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="93c96-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="93c96-139">Fungování šablony určuje nastavení na záložce s náhledem **Plánování**.</span><span class="sxs-lookup"><span data-stu-id="93c96-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="93c96-140">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-140">Set the following values:</span></span>

    - <span data-ttu-id="93c96-141">**Požadavky poptávky:** *Žádné*</span><span class="sxs-lookup"><span data-stu-id="93c96-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="93c96-142">Toto pole určuje požadavky poptávky na zásoby.</span><span class="sxs-lookup"><span data-stu-id="93c96-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="93c96-143">Pokud musí být poptávka před uvolněním spojena s dodávkou, vyberte možnost *Označení*.</span><span class="sxs-lookup"><span data-stu-id="93c96-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="93c96-144">Pokud musí být poptávka před uvolněním rezervována na základě objednávky, vyberte možnost *Rezervace objednávky*.</span><span class="sxs-lookup"><span data-stu-id="93c96-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="93c96-145">**Typ vyhledávání:** *Umístění dodávky*</span><span class="sxs-lookup"><span data-stu-id="93c96-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="93c96-146">Toto pole definuje, zda by měla práce cross dockingu používat přípravná/nákladová skladová místa z dodávky, případně zda by měla používat směrnice skladového místa a na jejich základě vyhledat vlastní přípravná/nákladová skladová místa.</span><span class="sxs-lookup"><span data-stu-id="93c96-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="93c96-147">**Šablona práce:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="93c96-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="93c96-148">Toto pole definuje šablonu práce, která by měla být použita při vytváření práce cross dockingu.</span><span class="sxs-lookup"><span data-stu-id="93c96-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="93c96-149">**Znovu ověřit při přijetí dodávky:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="93c96-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="93c96-150">Tato volba určuje, zda má být dodávka během příjmu znovu ověřena.</span><span class="sxs-lookup"><span data-stu-id="93c96-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="93c96-151">Pokud je u této možnosti nastavena hodnota *Ano* , proběhne kontrola maximálního časového úseku i počtu dní vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="93c96-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="93c96-152">**Ověření časového úseku:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="93c96-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="93c96-153">Tato možnost určuje, zda se má vyhodnocovat maximální časový úsek, když dojde k výběru zdroje dodávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="93c96-154">Pokud je u této možnosti zadána hodnota *Ano* , budou k dispozici pole týkající se maximálního a minimálního časového úseku.</span><span class="sxs-lookup"><span data-stu-id="93c96-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="93c96-155">**Maximální časový úsek:** *5*</span><span class="sxs-lookup"><span data-stu-id="93c96-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="93c96-156">Toto pole určuje maximální období, jež smí uplynout mezi doručením dodávky a odesláním poptávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="93c96-157">**Jednotka maximálního časového úseku:** *Dny*</span><span class="sxs-lookup"><span data-stu-id="93c96-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="93c96-158">**Minimální časový úsek:** *0*</span><span class="sxs-lookup"><span data-stu-id="93c96-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="93c96-159">Toto pole určuje minimální období, jež smí uplynout mezi doručením dodávky a odesláním poptávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="93c96-160">**Jednotka minimálního časového úseku:** *Dny*</span><span class="sxs-lookup"><span data-stu-id="93c96-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="93c96-161">**Rozsah dnů vypršení platnosti:** *0*</span><span class="sxs-lookup"><span data-stu-id="93c96-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="93c96-162">*Kritéria FEFO (First expiry first out):* Toto pole určuje maximální počet dní mezi datem expirace šarže, která vyprší jako první, jež je aktuálně ve skladu, a šarží, která je přijímána.</span><span class="sxs-lookup"><span data-stu-id="93c96-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="93c96-163">Na záložce s náhledem **Zdroje dodávek** se určují typy dodávek, které jsou pro tuto šablonu platné.</span><span class="sxs-lookup"><span data-stu-id="93c96-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="93c96-164">Klikněte na **Nový** a poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="93c96-165">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="93c96-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="93c96-166">**Zdroj dodávky:** *Nákupní objednávka*</span><span class="sxs-lookup"><span data-stu-id="93c96-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="93c96-167">Vytvoření pracovní třídy</span><span class="sxs-lookup"><span data-stu-id="93c96-167">Create a work class</span></span>

1. <span data-ttu-id="93c96-168">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="93c96-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="93c96-169">V podokně Akce vyberte možnost **Nový** a vytvořte třídu práce.</span><span class="sxs-lookup"><span data-stu-id="93c96-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="93c96-170">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-170">Set the following values:</span></span>

    - <span data-ttu-id="93c96-171">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="93c96-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="93c96-172">**Popis:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="93c96-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="93c96-173">**Typ pracovního příkazu:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="93c96-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="93c96-174">Vytvoření šablony práce</span><span class="sxs-lookup"><span data-stu-id="93c96-174">Create a work template</span></span>

1. <span data-ttu-id="93c96-175">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="93c96-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="93c96-176">V poli **Typ pracovního příkazu** nastavte možnost *Cross docking*.</span><span class="sxs-lookup"><span data-stu-id="93c96-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="93c96-177">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do tabulky **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="93c96-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="93c96-178">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93c96-179">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="93c96-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="93c96-180">**Šablona práce:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="93c96-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="93c96-181">**Popis šablony práce:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="93c96-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="93c96-182">Chcete-li, aby byla dostupná záložka s náhledem **Podrobnosti šablony práce** , klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93c96-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="93c96-183">Na záložce s náhledem **Podrobnosti šablony práce** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="93c96-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="93c96-184">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93c96-185">**Typ práce:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="93c96-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="93c96-186">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="93c96-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="93c96-187">Chcete-li přidat další řádek, klikněte znovu na **Nový** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="93c96-188">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="93c96-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="93c96-189">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="93c96-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="93c96-190">Vyberte **Uložit** a ujistěte se, že máte zaškrtnuté políčko **Platné** pro šablonu *51 Cross Dock*.</span><span class="sxs-lookup"><span data-stu-id="93c96-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="93c96-191">ID třídy práce pro typy práce *Výdej* a *Zaskladnění* se musí shodovat.</span><span class="sxs-lookup"><span data-stu-id="93c96-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="93c96-192">Vytvoření směrnic skladového místa</span><span class="sxs-lookup"><span data-stu-id="93c96-192">Create location directives</span></span>

1. <span data-ttu-id="93c96-193">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="93c96-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="93c96-194">V levém podokně nastavte v poli **Typ pracovního příkazu** hodnotu *Cross docking*.</span><span class="sxs-lookup"><span data-stu-id="93c96-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="93c96-195">V podokně Akce klikněte na **Nový** a poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="93c96-196">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="93c96-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="93c96-197">**Název:** *51 Cross Dock Put*</span><span class="sxs-lookup"><span data-stu-id="93c96-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="93c96-198">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="93c96-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="93c96-199">**Lokalita:** *5*</span><span class="sxs-lookup"><span data-stu-id="93c96-199">**Site:** *5*</span></span>
    - <span data-ttu-id="93c96-200">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="93c96-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="93c96-201">Chcete-li, aby byla dostupná záložka s náhledem **Řádky** , klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93c96-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="93c96-202">Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="93c96-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="93c96-203">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93c96-204">**Od množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="93c96-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="93c96-205">**Do množství:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="93c96-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="93c96-206">Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa** , klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93c96-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="93c96-207">Na záložce s náhledem **Akce směrnice skladového místa** přidejte řádek do mřížky výběrem možnosti **Nová**.</span><span class="sxs-lookup"><span data-stu-id="93c96-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="93c96-208">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93c96-209">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="93c96-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="93c96-210">**Využití pevného skladového místa:** *Pevná a nepevná skladová místa*</span><span class="sxs-lookup"><span data-stu-id="93c96-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="93c96-211">Vyberte možnost **Uložit** , chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na nástrojové liště **Akce směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="93c96-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="93c96-212">Vyberte **Upravit dotaz** , otevře se editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="93c96-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="93c96-213">Ujistěte se, že jsou na kartě **Oblast** nakonfigurovány následující dva řádky:</span><span class="sxs-lookup"><span data-stu-id="93c96-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="93c96-214">Řádek 1:</span><span class="sxs-lookup"><span data-stu-id="93c96-214">Line 1:</span></span>

        - <span data-ttu-id="93c96-215">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="93c96-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="93c96-216">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="93c96-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="93c96-217">**Pole:** *Sklad*</span><span class="sxs-lookup"><span data-stu-id="93c96-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="93c96-218">**Kritéria:** *51*</span><span class="sxs-lookup"><span data-stu-id="93c96-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="93c96-219">Řádek 2:</span><span class="sxs-lookup"><span data-stu-id="93c96-219">Line 2:</span></span>

        - <span data-ttu-id="93c96-220">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="93c96-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="93c96-221">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="93c96-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="93c96-222">**Pole:** *Skladové místo*</span><span class="sxs-lookup"><span data-stu-id="93c96-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="93c96-223">**Kritéria:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="93c96-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="93c96-224">Vyberte **OK** a editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="93c96-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="93c96-225">Vytvoření položky nabídky mobilních zařízení</span><span class="sxs-lookup"><span data-stu-id="93c96-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="93c96-226">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="93c96-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="93c96-227">V seznamu položek nabídky v levém podokně vyberte **Nákupní vyskladnění**.</span><span class="sxs-lookup"><span data-stu-id="93c96-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="93c96-228">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="93c96-228">Select **Edit**.</span></span>
1. <span data-ttu-id="93c96-229">Na záložce s náhledem **Pracovní třídy** přidejte řádek do mřížky výběrem možnosti **Nová**.</span><span class="sxs-lookup"><span data-stu-id="93c96-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="93c96-230">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93c96-231">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="93c96-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="93c96-232">**Typ pracovního příkazu:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="93c96-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="93c96-233">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93c96-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="93c96-234">Scénář</span><span class="sxs-lookup"><span data-stu-id="93c96-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="93c96-235">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="93c96-235">Create a purchase order</span></span>

<span data-ttu-id="93c96-236">Pomocí následujících kroků vytvořte objednávku jako zdroj dodávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="93c96-237">Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="93c96-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="93c96-238">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="93c96-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="93c96-239">V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="93c96-240">**Účet dodavatele:** *104*</span><span class="sxs-lookup"><span data-stu-id="93c96-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="93c96-241">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="93c96-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="93c96-242">Vybrat **OK** a poznamenejte si číslo objednávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="93c96-243">Na záložce s náhledem **Řádky objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="93c96-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="93c96-244">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="93c96-245">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="93c96-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="93c96-246">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="93c96-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="93c96-247">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="93c96-247">Create a sales order</span></span>

<span data-ttu-id="93c96-248">Pomocí následujících kroků vytvořte prodejní objednávku jako zdroj poptávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="93c96-249">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="93c96-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="93c96-250">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="93c96-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="93c96-251">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="93c96-252">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="93c96-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="93c96-253">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="93c96-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="93c96-254">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-254">Select **OK**.</span></span>
1. <span data-ttu-id="93c96-255">Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="93c96-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="93c96-256">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="93c96-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="93c96-257">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="93c96-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="93c96-258">**Množství:** *3*</span><span class="sxs-lookup"><span data-stu-id="93c96-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="93c96-259">Vytvoření cross dockingu s plánováním</span><span class="sxs-lookup"><span data-stu-id="93c96-259">Create planned cross-docking</span></span>

<span data-ttu-id="93c96-260">Pomocí těchto kroků vytvořte z prodejní objednávky cross docking s plánováním.</span><span class="sxs-lookup"><span data-stu-id="93c96-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="93c96-261">Na stránce **Podrobnosti prodejní objednávky** pro prodejní objednávku, kterou jste právě vytvořili, vyberte v podokně Akce na kartě **Sklad** ve skupině **Akce** položku **Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="93c96-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="93c96-262">Akce uvolnění do skladu vytvoří řádek dodávky a nákladu pro řádek prodejní objednávky. Pokusí se také o přidělení zásob.</span><span class="sxs-lookup"><span data-stu-id="93c96-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="93c96-263">Zobrazí se informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="93c96-263">You receive an informational message.</span></span> <span data-ttu-id="93c96-264">Zobrazí se také následující varovná zpráva: „Pro vlnu XXXX nebyla vytvořena žádná práce.</span><span class="sxs-lookup"><span data-stu-id="93c96-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="93c96-265">Podrobnosti najdete v protokolu historie vytváření práce.“</span><span class="sxs-lookup"><span data-stu-id="93c96-265">See the work creation history log for details."</span></span> <span data-ttu-id="93c96-266">Toto chování je očekávané, protože ve skladu nejsou žádné zásoby.</span><span class="sxs-lookup"><span data-stu-id="93c96-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="93c96-267">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Sklad** vyberte možnost **Podrobnosti dodávky**.</span><span class="sxs-lookup"><span data-stu-id="93c96-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="93c96-268">Zobrazí se stránka **Podrobnosti dodávky** , na níž je dodávka, která byla vytvořena pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="93c96-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="93c96-269">Na záložce s náhledem **Řádky nákladu** si všimněte, že je v poli **Množství pro cross docking s plánováním** zadána hodnota *3*.</span><span class="sxs-lookup"><span data-stu-id="93c96-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="93c96-270">Protože ve skladu nebyly žádné zásoby, ale platný zdroj dodávky dorazí během časového úseku definováno v šabloně cross dockingu, bylo vytvořeno množství pro cross docking.</span><span class="sxs-lookup"><span data-stu-id="93c96-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="93c96-271">Na záložce s náhledem **Řádky nákladu** vyberte položku **Cross docking s plánováním**. Zobrazí se podrobnosti vytvořeného cross dockingu.</span><span class="sxs-lookup"><span data-stu-id="93c96-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="93c96-272">Zpracování cross dockingu</span><span class="sxs-lookup"><span data-stu-id="93c96-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="93c96-273">Přijetí nákupní objednávky ve skladové mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="93c96-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="93c96-274">Systém obdrží množství 5 z nákupní objednávky do přijímacího skladového místa a vytvoří dvě různé práce.</span><span class="sxs-lookup"><span data-stu-id="93c96-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="93c96-275">První ID práce, jež vznikne, má v poli **Typ pracovního příkazu** hodnotu *Cross docking* a souvisí s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="93c96-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="93c96-276">Obsahuje množství 3 a je směrováno do skladového místa konečného dodání, takže lze dodávku okamžitě expedovat.</span><span class="sxs-lookup"><span data-stu-id="93c96-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="93c96-277">Druhé ID práce, jež vznikne, má v poli **Typ pracovního příkazu** hodnotu *Nákupní objednávky* a souvisí s nákupní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="93c96-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="93c96-278">Má zbývající množství 2, které neprošlo cross dockingem a je nasměrováno k zaskladnění na skladové místo.</span><span class="sxs-lookup"><span data-stu-id="93c96-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="93c96-279">Přihlaste se do mobilního zařízení pro uživatele ve skladu *51*.</span><span class="sxs-lookup"><span data-stu-id="93c96-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="93c96-280">Přejděte do **Vstupní \> Příjem nákupu**.</span><span class="sxs-lookup"><span data-stu-id="93c96-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="93c96-281">V poli **Č. nákup. obj.** zadejte číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="93c96-282">Do pole **Množ.** zadejte hodnotu *5*.</span><span class="sxs-lookup"><span data-stu-id="93c96-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="93c96-283">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-283">Select **OK**.</span></span>
1. <span data-ttu-id="93c96-284">Na další stránce nastavte u pole **Položka** hodnotu *A0001*.</span><span class="sxs-lookup"><span data-stu-id="93c96-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="93c96-285">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-285">Select **OK**.</span></span>
1. <span data-ttu-id="93c96-286">Na další stránce potvrďte hodnoty **Č. nákup. obj.** , **Položka** , a **Množ.** kliknutím na **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="93c96-287">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="93c96-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="93c96-288">Kliknutím na **Storno** okno opusťte.</span><span class="sxs-lookup"><span data-stu-id="93c96-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="93c96-289">Zaskladnění na cross docking a hromadné skladové místo</span><span class="sxs-lookup"><span data-stu-id="93c96-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="93c96-290">V současné době mají obě ID práce stejnou cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="93c96-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="93c96-291">Chcete-li provést další kroky, musíte získat ID práce a ID cílové registrační značky.</span><span class="sxs-lookup"><span data-stu-id="93c96-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="93c96-292">Tyto informace můžete získat z podrobností práce k řádku nákupní objednávky a z řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="93c96-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="93c96-293">Alternativně můžete přejít do **Řízení skladu \> Práce \> Podrobnosti práce**. Vyfiltrujte si pouze práce, kde je u položky **Sklad** hodnota *51*.</span><span class="sxs-lookup"><span data-stu-id="93c96-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="93c96-294">Na mobilním zařízení přejděte na **Vstupní \> Zaskladnění nákupu** a zadejte cílovou registrační značku podle práce.</span><span class="sxs-lookup"><span data-stu-id="93c96-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="93c96-295">Do pole **ID** zadejte ID cílové registrační značky z podrobností práce.</span><span class="sxs-lookup"><span data-stu-id="93c96-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="93c96-296">Stránka výdeje pomocí cross dockingu zobrazuje místo výdeje ( *RECV* ), cílovou registrační značku ( *registrační značka* ), položku ( *A0001* ) a množství ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="93c96-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="93c96-297">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-297">Select **OK**.</span></span>
1. <span data-ttu-id="93c96-298">V poli **Cílová LP** zadejte cílovou registrační značku pro ID registrační značky, jež by měla být zaskladněna (cross docking) na skladové místo pro dodávku.</span><span class="sxs-lookup"><span data-stu-id="93c96-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="93c96-299">Můžete vybrat libovolné ID registrační značky dle svého výběru.</span><span class="sxs-lookup"><span data-stu-id="93c96-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="93c96-300">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-300">Select **OK**.</span></span>
1. <span data-ttu-id="93c96-301">Na následující stránce zadejte do pole **ID** ID cílové registrační značky.</span><span class="sxs-lookup"><span data-stu-id="93c96-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="93c96-302">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-302">Select **OK**.</span></span>
1. <span data-ttu-id="93c96-303">Potvrďte práci pro výdej zbývajícího množství 2 a poté klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="93c96-304">Na další stránce klikněte na **Hotovo**. Tím ukončíte proces výdeje a zahájíte proces zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="93c96-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="93c96-305">Mobilní aplikace vám poskytne skladové místo a registrační značku, do níž chcete položku umístit.</span><span class="sxs-lookup"><span data-stu-id="93c96-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="93c96-306">Potvrďte hromadné úložiště pro **Zaskladnění** kliknutím na **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="93c96-307">Na další stránce potvrďte cross docking **Zaskladnění** kliknutím na **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c96-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="93c96-308">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="93c96-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="93c96-309">Kliknutím na **Storno** okno opusťte.</span><span class="sxs-lookup"><span data-stu-id="93c96-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="93c96-310">Následující obrázek ukazuje, jak by se dokončená práce cross dockingu mohla v systému Microsoft Dynamics 365 Supply Chain Management zobrazit.</span><span class="sxs-lookup"><span data-stu-id="93c96-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="93c96-311">![Práce cross docking dokončena](media/PlannedCrossDockingWork.png "Práce cross docking dokončena")</span><span class="sxs-lookup"><span data-stu-id="93c96-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
