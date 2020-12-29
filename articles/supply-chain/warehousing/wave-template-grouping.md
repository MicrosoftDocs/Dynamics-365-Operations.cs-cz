---
title: Seskupení šablon vlny
description: Seskupení šablon vlny umožňuje systému použít nastavení šablon vlny k určení postupu dělení uvolněných řádků a jejich přiřazování k novým nebo existujícím vlnám na základě definovaných kritérií. Tato funkce může být užitečná ve skladech, kde se tvoří vlny na základě konkrétních kritérií, ale kde manažeři dávají přednost automatické tvorbě vln místo ručního postupu.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9cbc0b6655de740628bcf3709d250ac02238038b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424223"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="eeaad-104">Seskupení šablon vlny</span><span class="sxs-lookup"><span data-stu-id="eeaad-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eeaad-105">Seskupení šablon vlny umožňuje systému použít nastavení [šablon vlny](tasks/configure-wave-processing.md) k určení postupu dělení uvolněných řádků a jejich přiřazování k novým nebo existujícím vlnám na základě definovaných kritérií.</span><span class="sxs-lookup"><span data-stu-id="eeaad-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="eeaad-106">Tato funkce může být užitečná ve skladech, kde se tvoří vlny na základě konkrétních kritérií, ale kde manažeři dávají přednost automatické tvorbě vln místo ručního postupu.</span><span class="sxs-lookup"><span data-stu-id="eeaad-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="eeaad-107">Umožňuje, aby byly v systému přidávány nově uvolněné dodávky do první vlny, u níž se určí shoda s příslušnou hodnotou v poli seskupení.</span><span class="sxs-lookup"><span data-stu-id="eeaad-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="eeaad-108">Pokud shoda není zjištěna, vytvoří systém pro novou dodávku novou vlnu.</span><span class="sxs-lookup"><span data-stu-id="eeaad-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eeaad-109">Seskupení šablon vlny není podporováno u prací typu *výdej surovin pro výrobu* nebo *kanban – výdej*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="eeaad-110">Je to proto, že seskupování podle vln je založeno na dodávkách, ale tyto typy prací nepoužívají dodávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="eeaad-111">Zapnutí funkce seskupení šablon vlny</span><span class="sxs-lookup"><span data-stu-id="eeaad-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="eeaad-112">Než můžete použít funkci *Seskupení šablon vlny*, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="eeaad-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="eeaad-113">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="eeaad-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="eeaad-114">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="eeaad-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eeaad-115">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="eeaad-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="eeaad-116">**Název funkce** *Seskupení šablon vlny*</span><span class="sxs-lookup"><span data-stu-id="eeaad-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="eeaad-117">Nastavení šablony vlny k použití pro seskupení šablon vlny</span><span class="sxs-lookup"><span data-stu-id="eeaad-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="eeaad-118">Chcete-li zpřístupnit seskupení šablon vlny, nastavte [šablonu vlny](tasks/configure-wave-processing.md) v souladu s pokyny níže.</span><span class="sxs-lookup"><span data-stu-id="eeaad-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="eeaad-119">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="eeaad-120">V levém podokně vyberte šablonu vlny, kterou chcete nastavovat.</span><span class="sxs-lookup"><span data-stu-id="eeaad-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="eeaad-121">Pokud se chystáte využít scénář uvedený dále v tomto tématu s využitím ukázkových dat, vyberte šablonu **Výchozí dodávka 62**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="eeaad-122">Vyberte možnost **Upravit**, tím přepnete stránku do režimu úprav.</span><span class="sxs-lookup"><span data-stu-id="eeaad-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="eeaad-123">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eeaad-124">**Automatizovat tvorbu vln:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="eeaad-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="eeaad-125">**Přiřadit k otevřeným vlnám:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="eeaad-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="eeaad-126">**Zpracovat vlnu při uvolnění do skladu:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="eeaad-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="eeaad-127">V podokně akcí zvolte **Upravit dotaz** a otevřete dialogové okno dotazů.</span><span class="sxs-lookup"><span data-stu-id="eeaad-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="eeaad-128">V dialogovém okně dotazů zkontrolujte na kartě **Třídění** kritéria třídění a ujistěte se, že existuje pravidlo zahrnující pole, jež chcete použít k seskupení vln.</span><span class="sxs-lookup"><span data-stu-id="eeaad-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="eeaad-129">Pokud se chystáte použít scénář s ukázkovými daty, přidejte řádek s následujícími hodnotami:</span><span class="sxs-lookup"><span data-stu-id="eeaad-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="eeaad-130">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="eeaad-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="eeaad-131">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="eeaad-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="eeaad-132">**Pole:** *Služba dopravce*</span><span class="sxs-lookup"><span data-stu-id="eeaad-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="eeaad-133">Po výběru této hodnoty se vám může zobrazit následující zpráva: „Služba dopravce není indexové pole.</span><span class="sxs-lookup"><span data-stu-id="eeaad-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="eeaad-134">Chcete k němu přidat třídění?“</span><span class="sxs-lookup"><span data-stu-id="eeaad-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="eeaad-135">Třídění přidáte kliknutím na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="eeaad-136">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="eeaad-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="eeaad-137">Vyberte **OK**, uložte změny a zavřete okno dotazů.</span><span class="sxs-lookup"><span data-stu-id="eeaad-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="eeaad-138">V podokně Akce vyberte možnost **Seskupení šablon vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="eeaad-139">Na stránce **Seskupení šablon vlny** zaškrtněte políčko **Seskupit podle** u každého řádku, který chcete použít k seskupení řádků objednávky do vln, jak je třeba.</span><span class="sxs-lookup"><span data-stu-id="eeaad-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="eeaad-140">Pokud se chystáte použít scénář s ukázkovými daty, zaškrtněte políčko **Seskupit podle** u řádku *Služba dopravce*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="eeaad-141">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-141">Select **Save**.</span></span>
1. <span data-ttu-id="eeaad-142">Zavřete stránku **Seskupení šablon vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="eeaad-143">Klepnutím na tlačítko **Uložit** uložte šablonu.</span><span class="sxs-lookup"><span data-stu-id="eeaad-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="eeaad-144">Scénář</span><span class="sxs-lookup"><span data-stu-id="eeaad-144">Scenario</span></span>

<span data-ttu-id="eeaad-145">Tato část obsahuje skript, pomocí kterého můžete zjistit, co tato funkce provádí a jak s ní lze pracovat.</span><span class="sxs-lookup"><span data-stu-id="eeaad-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="eeaad-146">Příprava ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="eeaad-146">Make sample data available</span></span>

<span data-ttu-id="eeaad-147">Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="eeaad-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="eeaad-148">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="eeaad-149">Tento scénář můžete také použít jako vodítko pro použití této funkce při práci na produkčním systému.</span><span class="sxs-lookup"><span data-stu-id="eeaad-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="eeaad-150">V takovém případě však musíte nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="eeaad-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="eeaad-151">Scénář: Seskupení šablon vlny</span><span class="sxs-lookup"><span data-stu-id="eeaad-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="eeaad-152">Tento scénář ukazuje, jak pomocí seskupení šablon vlny automaticky vytvářet více vln na základě kritérií seskupení definovaných v šabloně vlny.</span><span class="sxs-lookup"><span data-stu-id="eeaad-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="eeaad-153">V tomto scénáři je šablona vlny nastavena v systému tak, aby vytvořila jednu vlnu pro každou službu dopravce.</span><span class="sxs-lookup"><span data-stu-id="eeaad-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="eeaad-154">Než začnete, připravte si šablonu vlny postupem popsaným v tématu v části [Nastavení šablony vlny k použití pro seskupení šablon vlny](#set-up-template) výše.</span><span class="sxs-lookup"><span data-stu-id="eeaad-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="eeaad-155">Pokud budete využívat tento scénář s ukázkovými daty, je třeba použít hodnoty z ukázkových dat, jak se v proceduře navrhuje.</span><span class="sxs-lookup"><span data-stu-id="eeaad-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="eeaad-156">Toto nastavení seskupí vaše vlny podle služby dopravce, jež je nastavena pro každou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="eeaad-157">Vytvoření prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="eeaad-157">Create sales order 1</span></span>

1. <span data-ttu-id="eeaad-158">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eeaad-159">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="eeaad-160">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eeaad-161">Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-004*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="eeaad-162">Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="eeaad-163">Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="eeaad-164">Nová prodejní objednávka se otevře v zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="eeaad-165">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="eeaad-166">Přepněte na zobrazení **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="eeaad-167">Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="eeaad-168">**Dopravce dodávky:** *Letecká přeprava*</span><span class="sxs-lookup"><span data-stu-id="eeaad-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="eeaad-169">**Služba dopravce:** *Air*</span><span class="sxs-lookup"><span data-stu-id="eeaad-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="eeaad-170">Přepněte znovu do zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="eeaad-171">V oddílu **Řádky prodejní objednávky** přidejte řádek mřížky výběrem položky **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="eeaad-172">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eeaad-173">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="eeaad-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="eeaad-174">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="eeaad-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="eeaad-175">Vyberte nový řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eeaad-176">Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eeaad-177">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="eeaad-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eeaad-178">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="eeaad-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eeaad-179">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eeaad-180">Poznamenejte si čísla ID vlny a dodávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="eeaad-181">Zobrazení vlny, která byla vytvořena z prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="eeaad-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="eeaad-182">Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="eeaad-183">Vyberte ID vlny, která byla vytvořena z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="eeaad-184">Kliknutím na odkaz ID vlny otevřete stránku podrobností vlny.</span><span class="sxs-lookup"><span data-stu-id="eeaad-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="eeaad-185">Všimněte si, že dodávka byla přidána na záložku s náhledem **Řádky vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="eeaad-186">Vytvoření prodejní objednávky 2</span><span class="sxs-lookup"><span data-stu-id="eeaad-186">Create sales order 2</span></span>

1. <span data-ttu-id="eeaad-187">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eeaad-188">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="eeaad-189">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eeaad-190">Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-005*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="eeaad-191">Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="eeaad-192">Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="eeaad-193">Nová prodejní objednávka se otevře v zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="eeaad-194">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="eeaad-195">Přepněte na zobrazení **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="eeaad-196">Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="eeaad-197">**Dopravce dodávky:** *Flower moving*</span><span class="sxs-lookup"><span data-stu-id="eeaad-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="eeaad-198">**Služba dopravce:** *Std*</span><span class="sxs-lookup"><span data-stu-id="eeaad-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="eeaad-199">Přepněte znovu do zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="eeaad-200">V oddílu **Řádky prodejní objednávky** přidejte řádek mřížky výběrem položky **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="eeaad-201">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eeaad-202">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eeaad-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eeaad-203">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="eeaad-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="eeaad-204">Vyberte nový řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eeaad-205">Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eeaad-206">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="eeaad-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eeaad-207">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="eeaad-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eeaad-208">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eeaad-209">Poznamenejte si čísla ID vlny a dodávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="eeaad-210">Všimněte si, že ID vlny se liší od ID vlny první prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="eeaad-211">Zobrazení vlny, která byla vytvořena z prodejní objednávky 2</span><span class="sxs-lookup"><span data-stu-id="eeaad-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="eeaad-212">Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="eeaad-213">Vyberte ID vlny, která byla vytvořena z druhé prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="eeaad-214">Kliknutím na odkaz ID vlny otevřete stránku podrobností vlny.</span><span class="sxs-lookup"><span data-stu-id="eeaad-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="eeaad-215">Všimněte si, že dodávka byla přidána na záložku s náhledem **Řádky vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="eeaad-216">Pro tuto dodávku byla vytvořena nová vlna, protože používá jinou službu dopravce než první prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="eeaad-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="eeaad-217">Vytvoření prodejní objednávky 3</span><span class="sxs-lookup"><span data-stu-id="eeaad-217">Create sales order 3</span></span>

1. <span data-ttu-id="eeaad-218">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eeaad-219">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="eeaad-220">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eeaad-221">Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-006*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="eeaad-222">Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.</span><span class="sxs-lookup"><span data-stu-id="eeaad-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="eeaad-223">Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="eeaad-224">Nová prodejní objednávka se otevře v zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="eeaad-225">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="eeaad-226">Přepněte na zobrazení **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="eeaad-227">Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="eeaad-228">**Dopravce dodávky:** *Letecká přeprava*</span><span class="sxs-lookup"><span data-stu-id="eeaad-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="eeaad-229">**Služba dopravce:** *Air*</span><span class="sxs-lookup"><span data-stu-id="eeaad-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="eeaad-230">Přepněte znovu do zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="eeaad-231">V oddílu **Řádky prodejní objednávky** přidejte řádek mřížky výběrem položky **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="eeaad-232">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="eeaad-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eeaad-233">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eeaad-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eeaad-234">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="eeaad-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="eeaad-235">Vyberte nový řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eeaad-236">Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eeaad-237">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="eeaad-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eeaad-238">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="eeaad-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eeaad-239">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eeaad-240">Poznamenejte si čísla ID vlny a dodávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="eeaad-241">Dodávka byla přiřazena ke stávající vlně z první prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="eeaad-242">Zobrazení vlny pro prodejní objednávky 1 a 3</span><span class="sxs-lookup"><span data-stu-id="eeaad-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="eeaad-243">Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.</span><span class="sxs-lookup"><span data-stu-id="eeaad-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="eeaad-244">Vyberte ID vlny, která byla vytvořena ze třetí prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="eeaad-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="eeaad-245">Kliknutím na odkaz ID vlny otevřete stránku podrobností vlny.</span><span class="sxs-lookup"><span data-stu-id="eeaad-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="eeaad-246">Všimněte si, že dodávka byla přidána na záložku s náhledem **Řádky vlny** spolu s dodávkou za první prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="eeaad-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
