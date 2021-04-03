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
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556259"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="118d5-104">Cross docking s plánováním</span><span class="sxs-lookup"><span data-stu-id="118d5-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="118d5-105">Toto téma popisuje cross docking s rozšířeným plánováním.</span><span class="sxs-lookup"><span data-stu-id="118d5-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="118d5-106">Cross docking s rozšířeným plánováním je skladový proces, kde je množství zásob potřebných pro objednávku, směrováno přímo z příjmu nebo tvorby do správného výstupního překladiště nebo přípravné oblasti.</span><span class="sxs-lookup"><span data-stu-id="118d5-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="118d5-107">Veškeré zbývající zásoby z příchozího zdroje jsou směrovány na správné přípravné místo pomocí běžného procesu zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="118d5-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="118d5-108">Cross docking umožňuje pracovníkům přeskočit zaskladnění zásob na vstupu a jejich výdej na výstupu, když jsou již zásoby označeny pro výstupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="118d5-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="118d5-109">Tím se všude tam, kde je to možné, minimalizuje počet operací se zásobami.</span><span class="sxs-lookup"><span data-stu-id="118d5-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="118d5-110">Protože se redukuje množství interakce se systémem, lze též dosáhnout dalších časových i prostorových úspor ve skladu.</span><span class="sxs-lookup"><span data-stu-id="118d5-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="118d5-111">Před spuštěním cross dockingu musí uživatel nakonfigurovat novou šablonu pro cross docking, jež bude splňovat požadavky na zdroj dodávky a další.</span><span class="sxs-lookup"><span data-stu-id="118d5-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="118d5-112">Po vytvoření odchozí objednávky musí být řádek označen proti příchozí objednávce obsahující stejnou položku.</span><span class="sxs-lookup"><span data-stu-id="118d5-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="118d5-113">V době přijetí příchozí objednávky nastavení cross dockingu automaticky identifikuje potřebu cross dockingu a na základě nastavení směrnice skladového místa vytvoří příslušný pohyb pro požadované množství.</span><span class="sxs-lookup"><span data-stu-id="118d5-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="118d5-114">U transakcí se zásobami se **neprovede** zrušení registrace, je-li zrušena crossdockingová úloha, a to ani v případě, že je nastavení této funkcionality v parametrech správy skladu zapnuto.</span><span class="sxs-lookup"><span data-stu-id="118d5-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="118d5-115">Zapnutí funkcí Cross docking s plánováním</span><span class="sxs-lookup"><span data-stu-id="118d5-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="118d5-116">Pokud váš systém ještě neobsahuje funkce popsané v tomto tématu, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapínejte následující funkce v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="118d5-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="118d5-117">*Plánovaný cross docking*</span><span class="sxs-lookup"><span data-stu-id="118d5-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="118d5-118">*Šablony cross dockingu se směrnicemi skladového místa*</span><span class="sxs-lookup"><span data-stu-id="118d5-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="118d5-119">Nastavení</span><span class="sxs-lookup"><span data-stu-id="118d5-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="118d5-120">Obnovte metody účtování nákladu</span><span class="sxs-lookup"><span data-stu-id="118d5-120">Regenerate load posting methods</span></span>

<span data-ttu-id="118d5-121">Cross docking s plánováním se implementuje jako metoda účtování nákladu.</span><span class="sxs-lookup"><span data-stu-id="118d5-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="118d5-122">Po zapnutí funkce je nutné obnovit metody.</span><span class="sxs-lookup"><span data-stu-id="118d5-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="118d5-123">Přejděte do **Řízení skladu \> Nastavení \> Metody účtování nákladů**.</span><span class="sxs-lookup"><span data-stu-id="118d5-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="118d5-124">V podokně Akce vyberte možnost **Obnovit metody**.</span><span class="sxs-lookup"><span data-stu-id="118d5-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="118d5-125">Po dokončení obnovy byste měli vidět metodu, jež má v poli **Název metody** hodnotu *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="118d5-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="118d5-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="118d5-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="118d5-127">Vytvoření šablony cross dockingu</span><span class="sxs-lookup"><span data-stu-id="118d5-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="118d5-128">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Šablony cross dockingu**.</span><span class="sxs-lookup"><span data-stu-id="118d5-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="118d5-129">V podokně Akce vyberte možnost **Nový** a vytvořte šablonu.</span><span class="sxs-lookup"><span data-stu-id="118d5-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="118d5-130">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="118d5-131">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="118d5-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="118d5-132">Toto pole definuje pořadí, ve kterém budou šablony vyhodnocovány.</span><span class="sxs-lookup"><span data-stu-id="118d5-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="118d5-133">**ID šablony cross dockingu:** *51*</span><span class="sxs-lookup"><span data-stu-id="118d5-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="118d5-134">**Popis:** *Sklad 51*</span><span class="sxs-lookup"><span data-stu-id="118d5-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="118d5-135">**Zásady uvolnění poptávky:** *Před přijetím dodávky*</span><span class="sxs-lookup"><span data-stu-id="118d5-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="118d5-136">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="118d5-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="118d5-137">Fungování šablony určuje nastavení na záložce s náhledem **Plánování**.</span><span class="sxs-lookup"><span data-stu-id="118d5-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="118d5-138">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-138">Set the following values:</span></span>

    - <span data-ttu-id="118d5-139">**Požadavky poptávky:** *Žádné*</span><span class="sxs-lookup"><span data-stu-id="118d5-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="118d5-140">Toto pole určuje požadavky poptávky na zásoby.</span><span class="sxs-lookup"><span data-stu-id="118d5-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="118d5-141">Pokud musí být poptávka před uvolněním spojena s dodávkou, vyberte možnost *Označení*.</span><span class="sxs-lookup"><span data-stu-id="118d5-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="118d5-142">Pokud musí být poptávka před uvolněním rezervována na základě objednávky, vyberte možnost *Rezervace objednávky*.</span><span class="sxs-lookup"><span data-stu-id="118d5-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="118d5-143">**Typ vyhledávání:** *Umístění dodávky*</span><span class="sxs-lookup"><span data-stu-id="118d5-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="118d5-144">Toto pole definuje, zda by měla práce cross dockingu používat přípravná/nákladová skladová místa z dodávky, případně zda by měla používat směrnice skladového místa a na jejich základě vyhledat vlastní přípravná/nákladová skladová místa.</span><span class="sxs-lookup"><span data-stu-id="118d5-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="118d5-145">**Šablona práce:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="118d5-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="118d5-146">Toto pole definuje šablonu práce, která by měla být použita při vytváření práce cross dockingu.</span><span class="sxs-lookup"><span data-stu-id="118d5-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="118d5-147">**Znovu ověřit při přijetí dodávky:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="118d5-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="118d5-148">Tato volba určuje, zda má být dodávka během příjmu znovu ověřena.</span><span class="sxs-lookup"><span data-stu-id="118d5-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="118d5-149">Pokud je u této možnosti nastavena hodnota *Ano*, proběhne kontrola maximálního časového úseku i počtu dní vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="118d5-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="118d5-150">**Kód směrnice** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="118d5-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="118d5-151">Tato možnost umožňuje systému používat direktivy umístění, aby pomohla určit nejlepší umístění pro přesun zásob cross-docking.</span><span class="sxs-lookup"><span data-stu-id="118d5-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="118d5-152">Můžete jej nastavit přiřazením kódu direktivy ke každé příslušné šabloně cross-dockingu.</span><span class="sxs-lookup"><span data-stu-id="118d5-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="118d5-153">Každý kód direktivy označuje jedinečnou direktivu umístění.</span><span class="sxs-lookup"><span data-stu-id="118d5-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="118d5-154">**Ověření časového úseku:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="118d5-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="118d5-155">Tato možnost určuje, zda se má vyhodnocovat maximální časový úsek, když dojde k výběru zdroje dodávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="118d5-156">Pokud je u této možnosti zadána hodnota *Ano*, budou k dispozici pole týkající se maximálního a minimálního časového úseku.</span><span class="sxs-lookup"><span data-stu-id="118d5-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="118d5-157">**Maximální časový úsek:** *5*</span><span class="sxs-lookup"><span data-stu-id="118d5-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="118d5-158">Toto pole určuje maximální období, jež smí uplynout mezi doručením dodávky a odesláním poptávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="118d5-159">**Jednotka maximálního časového úseku:** *Dny*</span><span class="sxs-lookup"><span data-stu-id="118d5-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="118d5-160">**Minimální časový úsek:** *0*</span><span class="sxs-lookup"><span data-stu-id="118d5-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="118d5-161">Toto pole určuje minimální období, jež smí uplynout mezi doručením dodávky a odesláním poptávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="118d5-162">**Jednotka minimálního časového úseku:** *Dny*</span><span class="sxs-lookup"><span data-stu-id="118d5-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="118d5-163">**Rozsah dnů vypršení platnosti:** *0*</span><span class="sxs-lookup"><span data-stu-id="118d5-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="118d5-164">*Kritéria FEFO (First expiry first out):* Toto pole určuje maximální počet dní mezi datem expirace šarže, která vyprší jako první, jež je aktuálně ve skladu, a šarží, která je přijímána.</span><span class="sxs-lookup"><span data-stu-id="118d5-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="118d5-165">Na záložce s náhledem **Zdroje dodávek** se určují typy dodávek, které jsou pro tuto šablonu platné.</span><span class="sxs-lookup"><span data-stu-id="118d5-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="118d5-166">Klikněte na **Nový** a poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="118d5-167">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="118d5-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="118d5-168">**Zdroj dodávky:** *Nákupní objednávka*</span><span class="sxs-lookup"><span data-stu-id="118d5-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="118d5-169">Vytvoření pracovní třídy</span><span class="sxs-lookup"><span data-stu-id="118d5-169">Create a work class</span></span>

1. <span data-ttu-id="118d5-170">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="118d5-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="118d5-171">V podokně Akce vyberte možnost **Nový** a vytvořte třídu práce.</span><span class="sxs-lookup"><span data-stu-id="118d5-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="118d5-172">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-172">Set the following values:</span></span>

    - <span data-ttu-id="118d5-173">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="118d5-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="118d5-174">**Popis:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="118d5-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="118d5-175">**Typ pracovního příkazu:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="118d5-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="118d5-176">Vytvoření šablony práce</span><span class="sxs-lookup"><span data-stu-id="118d5-176">Create a work template</span></span>

1. <span data-ttu-id="118d5-177">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="118d5-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="118d5-178">V poli **Typ pracovního příkazu** nastavte možnost *Cross docking*.</span><span class="sxs-lookup"><span data-stu-id="118d5-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="118d5-179">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do tabulky **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="118d5-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="118d5-180">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="118d5-181">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="118d5-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="118d5-182">**Šablona práce:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="118d5-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="118d5-183">**Popis šablony práce:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="118d5-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="118d5-184">Chcete-li, aby byla dostupná záložka s náhledem **Podrobnosti šablony práce**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="118d5-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="118d5-185">Na záložce s náhledem **Podrobnosti šablony práce** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="118d5-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="118d5-186">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="118d5-187">**Typ práce:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="118d5-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="118d5-188">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="118d5-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="118d5-189">Chcete-li přidat další řádek, klikněte znovu na **Nový** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="118d5-190">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="118d5-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="118d5-191">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="118d5-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="118d5-192">Vyberte **Uložit** a ujistěte se, že máte zaškrtnuté políčko **Platné** pro šablonu *51 Cross Dock*.</span><span class="sxs-lookup"><span data-stu-id="118d5-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="118d5-193">ID třídy práce pro typy práce *Výdej* a *Zaskladnění* se musí shodovat.</span><span class="sxs-lookup"><span data-stu-id="118d5-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="118d5-194">Vytvoření směrnic skladového místa</span><span class="sxs-lookup"><span data-stu-id="118d5-194">Create location directives</span></span>

1. <span data-ttu-id="118d5-195">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="118d5-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="118d5-196">V levém podokně nastavte v poli **Typ pracovního příkazu** hodnotu *Cross docking*.</span><span class="sxs-lookup"><span data-stu-id="118d5-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="118d5-197">V podokně Akce klikněte na **Nový** a poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="118d5-198">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="118d5-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="118d5-199">**Název:** *51 Cross Dock Put*</span><span class="sxs-lookup"><span data-stu-id="118d5-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="118d5-200">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="118d5-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="118d5-201">**Lokalita:** *5*</span><span class="sxs-lookup"><span data-stu-id="118d5-201">**Site:** *5*</span></span>
    - <span data-ttu-id="118d5-202">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="118d5-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="118d5-203">Chcete-li, aby byla dostupná záložka s náhledem **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="118d5-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="118d5-204">Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="118d5-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="118d5-205">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="118d5-206">**Od množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="118d5-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="118d5-207">**Do množství:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="118d5-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="118d5-208">Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="118d5-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="118d5-209">Na záložce s náhledem **Akce směrnice skladového místa** přidejte řádek do mřížky výběrem možnosti **Nová**.</span><span class="sxs-lookup"><span data-stu-id="118d5-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="118d5-210">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="118d5-211">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="118d5-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="118d5-212">**Využití pevného skladového místa:** *Pevná a nepevná skladová místa*</span><span class="sxs-lookup"><span data-stu-id="118d5-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="118d5-213">Vyberte možnost **Uložit**, chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na nástrojové liště **Akce směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="118d5-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="118d5-214">Vyberte **Upravit dotaz**, otevře se editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="118d5-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="118d5-215">Ujistěte se, že jsou na kartě **Oblast** nakonfigurovány následující dva řádky:</span><span class="sxs-lookup"><span data-stu-id="118d5-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="118d5-216">Řádek 1:</span><span class="sxs-lookup"><span data-stu-id="118d5-216">Line 1:</span></span>

        - <span data-ttu-id="118d5-217">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="118d5-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="118d5-218">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="118d5-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="118d5-219">**Pole:** *Sklad*</span><span class="sxs-lookup"><span data-stu-id="118d5-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="118d5-220">**Kritéria:** *51*</span><span class="sxs-lookup"><span data-stu-id="118d5-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="118d5-221">Řádek 2:</span><span class="sxs-lookup"><span data-stu-id="118d5-221">Line 2:</span></span>

        - <span data-ttu-id="118d5-222">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="118d5-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="118d5-223">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="118d5-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="118d5-224">**Pole:** *Skladové místo*</span><span class="sxs-lookup"><span data-stu-id="118d5-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="118d5-225">**Kritéria:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="118d5-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="118d5-226">Vyberte **OK** a editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="118d5-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="118d5-227">Vytvoření položky nabídky mobilních zařízení</span><span class="sxs-lookup"><span data-stu-id="118d5-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="118d5-228">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="118d5-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="118d5-229">V seznamu položek nabídky v levém podokně vyberte **Nákupní vyskladnění**.</span><span class="sxs-lookup"><span data-stu-id="118d5-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="118d5-230">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="118d5-230">Select **Edit**.</span></span>
1. <span data-ttu-id="118d5-231">Na záložce s náhledem **Pracovní třídy** přidejte řádek do mřížky výběrem možnosti **Nová**.</span><span class="sxs-lookup"><span data-stu-id="118d5-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="118d5-232">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="118d5-233">**ID pracovní třídy:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="118d5-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="118d5-234">**Typ pracovního příkazu:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="118d5-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="118d5-235">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="118d5-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="118d5-236">Scénář</span><span class="sxs-lookup"><span data-stu-id="118d5-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="118d5-237">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="118d5-237">Create a purchase order</span></span>

<span data-ttu-id="118d5-238">Pomocí následujících kroků vytvořte objednávku jako zdroj dodávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="118d5-239">Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="118d5-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="118d5-240">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="118d5-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="118d5-241">V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="118d5-242">**Účet dodavatele:** *104*</span><span class="sxs-lookup"><span data-stu-id="118d5-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="118d5-243">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="118d5-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="118d5-244">Vybrat **OK** a poznamenejte si číslo objednávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="118d5-245">Na záložce s náhledem **Řádky objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="118d5-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="118d5-246">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="118d5-247">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="118d5-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="118d5-248">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="118d5-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="118d5-249">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="118d5-249">Create a sales order</span></span>

<span data-ttu-id="118d5-250">Pomocí následujících kroků vytvořte prodejní objednávku jako zdroj poptávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="118d5-251">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="118d5-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="118d5-252">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="118d5-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="118d5-253">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="118d5-254">**Účet zákazníka:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="118d5-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="118d5-255">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="118d5-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="118d5-256">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-256">Select **OK**.</span></span>
1. <span data-ttu-id="118d5-257">Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="118d5-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="118d5-258">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="118d5-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="118d5-259">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="118d5-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="118d5-260">**Množství:** *3*</span><span class="sxs-lookup"><span data-stu-id="118d5-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="118d5-261">Vytvoření cross dockingu s plánováním</span><span class="sxs-lookup"><span data-stu-id="118d5-261">Create planned cross-docking</span></span>

<span data-ttu-id="118d5-262">Pomocí těchto kroků vytvořte z prodejní objednávky cross docking s plánováním.</span><span class="sxs-lookup"><span data-stu-id="118d5-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="118d5-263">Na stránce **Podrobnosti prodejní objednávky** pro prodejní objednávku, kterou jste právě vytvořili, vyberte v podokně Akce na kartě **Sklad** ve skupině **Akce** položku **Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="118d5-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="118d5-264">Akce uvolnění do skladu vytvoří řádek dodávky a nákladu pro řádek prodejní objednávky. Pokusí se také o přidělení zásob.</span><span class="sxs-lookup"><span data-stu-id="118d5-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="118d5-265">Zobrazí se informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="118d5-265">You receive an informational message.</span></span> <span data-ttu-id="118d5-266">Zobrazí se také následující varovná zpráva: „Pro vlnu XXXX nebyla vytvořena žádná práce.</span><span class="sxs-lookup"><span data-stu-id="118d5-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="118d5-267">Podrobnosti najdete v protokolu historie vytváření práce.“</span><span class="sxs-lookup"><span data-stu-id="118d5-267">See the work creation history log for details."</span></span> <span data-ttu-id="118d5-268">Toto chování je očekávané, protože ve skladu nejsou žádné zásoby.</span><span class="sxs-lookup"><span data-stu-id="118d5-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="118d5-269">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Sklad** vyberte možnost **Podrobnosti dodávky**.</span><span class="sxs-lookup"><span data-stu-id="118d5-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="118d5-270">Zobrazí se stránka **Podrobnosti dodávky**, na níž je dodávka, která byla vytvořena pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="118d5-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="118d5-271">Na záložce s náhledem **Řádky nákladu** si všimněte, že je v poli **Množství pro cross docking s plánováním** zadána hodnota *3*.</span><span class="sxs-lookup"><span data-stu-id="118d5-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="118d5-272">Protože ve skladu nebyly žádné zásoby, ale platný zdroj dodávky dorazí během časového úseku definováno v šabloně cross dockingu, bylo vytvořeno množství pro cross docking.</span><span class="sxs-lookup"><span data-stu-id="118d5-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="118d5-273">Na záložce s náhledem **Řádky nákladu** vyberte položku **Cross docking s plánováním**. Zobrazí se podrobnosti vytvořeného cross dockingu.</span><span class="sxs-lookup"><span data-stu-id="118d5-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="118d5-274">Zpracování cross dockingu</span><span class="sxs-lookup"><span data-stu-id="118d5-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="118d5-275">Přijetí nákupní objednávky ve skladové mobilní aplikaci</span><span class="sxs-lookup"><span data-stu-id="118d5-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="118d5-276">Systém obdrží množství 5 z nákupní objednávky do přijímacího skladového místa a vytvoří dvě různé práce.</span><span class="sxs-lookup"><span data-stu-id="118d5-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="118d5-277">První ID práce, jež vznikne, má v poli **Typ pracovního příkazu** hodnotu *Cross docking* a souvisí s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="118d5-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="118d5-278">Obsahuje množství 3 a je směrováno do skladového místa konečného dodání, takže lze dodávku okamžitě expedovat.</span><span class="sxs-lookup"><span data-stu-id="118d5-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="118d5-279">Druhé ID práce, jež vznikne, má v poli **Typ pracovního příkazu** hodnotu *Nákupní objednávky* a souvisí s nákupní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="118d5-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="118d5-280">Má zbývající množství 2, které neprošlo cross dockingem a je nasměrováno k zaskladnění na skladové místo.</span><span class="sxs-lookup"><span data-stu-id="118d5-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="118d5-281">Přihlaste se do mobilního zařízení pro uživatele ve skladu *51*.</span><span class="sxs-lookup"><span data-stu-id="118d5-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="118d5-282">Přejděte do **Vstupní \> Příjem nákupu**.</span><span class="sxs-lookup"><span data-stu-id="118d5-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="118d5-283">V poli **Č. nákup. obj.** zadejte číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="118d5-284">Do pole **Množ.** zadejte hodnotu *5*.</span><span class="sxs-lookup"><span data-stu-id="118d5-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="118d5-285">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-285">Select **OK**.</span></span>
1. <span data-ttu-id="118d5-286">Na další stránce nastavte u pole **Položka** hodnotu *A0001*.</span><span class="sxs-lookup"><span data-stu-id="118d5-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="118d5-287">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-287">Select **OK**.</span></span>
1. <span data-ttu-id="118d5-288">Na další stránce potvrďte hodnoty **Č. nákup. obj.**, **Položka**, a **Množ.** kliknutím na **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="118d5-289">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="118d5-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="118d5-290">Kliknutím na **Storno** okno opusťte.</span><span class="sxs-lookup"><span data-stu-id="118d5-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="118d5-291">Zaskladnění na cross docking a hromadné skladové místo</span><span class="sxs-lookup"><span data-stu-id="118d5-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="118d5-292">V současné době mají obě ID práce stejnou cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="118d5-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="118d5-293">Chcete-li provést další kroky, musíte získat ID práce a ID cílové registrační značky.</span><span class="sxs-lookup"><span data-stu-id="118d5-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="118d5-294">Tyto informace můžete získat z podrobností práce k řádku nákupní objednávky a z řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="118d5-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="118d5-295">Alternativně můžete přejít do **Řízení skladu \> Práce \> Podrobnosti práce**. Vyfiltrujte si pouze práce, kde je u položky **Sklad** hodnota *51*.</span><span class="sxs-lookup"><span data-stu-id="118d5-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="118d5-296">Na mobilním zařízení přejděte na **Vstupní \> Zaskladnění nákupu** a zadejte cílovou registrační značku podle práce.</span><span class="sxs-lookup"><span data-stu-id="118d5-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="118d5-297">Do pole **ID** zadejte ID cílové registrační značky z podrobností práce.</span><span class="sxs-lookup"><span data-stu-id="118d5-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="118d5-298">Stránka výdeje pomocí cross dockingu zobrazuje místo výdeje (*RECV*), cílovou registrační značku (*registrační značka*), položku (*A0001*) a množství (*3*).</span><span class="sxs-lookup"><span data-stu-id="118d5-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="118d5-299">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-299">Select **OK**.</span></span>
1. <span data-ttu-id="118d5-300">V poli **Cílová LP** zadejte cílovou registrační značku pro ID registrační značky, jež by měla být zaskladněna (cross docking) na skladové místo pro dodávku.</span><span class="sxs-lookup"><span data-stu-id="118d5-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="118d5-301">Můžete vybrat libovolné ID registrační značky dle svého výběru.</span><span class="sxs-lookup"><span data-stu-id="118d5-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="118d5-302">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-302">Select **OK**.</span></span>
1. <span data-ttu-id="118d5-303">Na následující stránce zadejte do pole **ID** ID cílové registrační značky.</span><span class="sxs-lookup"><span data-stu-id="118d5-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="118d5-304">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-304">Select **OK**.</span></span>
1. <span data-ttu-id="118d5-305">Potvrďte práci pro výdej zbývajícího množství 2 a poté klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="118d5-306">Na další stránce klikněte na **Hotovo**. Tím ukončíte proces výdeje a zahájíte proces zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="118d5-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="118d5-307">Mobilní aplikace vám poskytne skladové místo a registrační značku, do níž chcete položku umístit.</span><span class="sxs-lookup"><span data-stu-id="118d5-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="118d5-308">Potvrďte hromadné úložiště pro **Zaskladnění** kliknutím na **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="118d5-309">Na další stránce potvrďte cross docking **Zaskladnění** kliknutím na **OK**.</span><span class="sxs-lookup"><span data-stu-id="118d5-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="118d5-310">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="118d5-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="118d5-311">Kliknutím na **Storno** okno opusťte.</span><span class="sxs-lookup"><span data-stu-id="118d5-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="118d5-312">Následující obrázek ukazuje, jak by se dokončená práce cross dockingu mohla v systému Microsoft Dynamics 365 Supply Chain Management zobrazit.</span><span class="sxs-lookup"><span data-stu-id="118d5-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="118d5-313">![Práce cross docking dokončena](media/PlannedCrossDockingWork.png "Práce cross docking dokončena")</span><span class="sxs-lookup"><span data-stu-id="118d5-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]