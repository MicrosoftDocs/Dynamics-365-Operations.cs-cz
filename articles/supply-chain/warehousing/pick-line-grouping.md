---
title: Seskupování řádků vyskladnění
description: Toto téma poskytuje přehled seskupení řádků výdeje.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828266"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="57696-103">Seskupování řádků vyskladnění</span><span class="sxs-lookup"><span data-stu-id="57696-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57696-104">V seskupování řádků výdeje lze kombinovat více řádků práce, které mají stejné zboží a umístění, do jednoho výdeje, které se uživateli zobrazí v mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="57696-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="57696-105">Pracovníci skladu tedy mohou získat nejúčinnější pokyny, které jsou možné, ale je zachováno i povinné oddělení pracovních řádků v systému (například pro různé kontejnery a objednávky).</span><span class="sxs-lookup"><span data-stu-id="57696-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="57696-106">Zapnutí funkce seskupení řádků práce výdeje</span><span class="sxs-lookup"><span data-stu-id="57696-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="57696-107">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="57696-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="57696-108">Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zkontrolovat stav této funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="57696-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="57696-109">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="57696-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="57696-110">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="57696-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="57696-111">**Název funkce:** *Seskupení řádků vyskladnění*</span><span class="sxs-lookup"><span data-stu-id="57696-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="57696-112">Nastavit seskupování řádků výdeje</span><span class="sxs-lookup"><span data-stu-id="57696-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="57696-113">Vytvoření položky nabídky mobilních zařízení</span><span class="sxs-lookup"><span data-stu-id="57696-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="57696-114">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="57696-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="57696-115">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="57696-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="57696-116">V poli **Název položky nabídky** zadejte *Vyskladnění řádků skupiny prodejů*.</span><span class="sxs-lookup"><span data-stu-id="57696-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="57696-117">V poli **Nadpis** zadejte *Vyskladnění řádků skupiny prodejů*.</span><span class="sxs-lookup"><span data-stu-id="57696-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="57696-118">Tento název se zobrazí v nabídce mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="57696-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="57696-119">V poli **Režim** vyberte *Práce*.</span><span class="sxs-lookup"><span data-stu-id="57696-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="57696-120">Nastavte hodnotu možnosti **Použít stávající práci** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="57696-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="57696-121">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="57696-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="57696-122">V poli **Řídí** nastavte *Řízeno uživatelem*.</span><span class="sxs-lookup"><span data-stu-id="57696-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="57696-123">Nastavte volbu **Generovat registrační značku vozidla** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="57696-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="57696-124">Nastavte možnost **Výdej skupiny** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="57696-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="57696-125">Potvrďte výchozí hodnoty ve všech zbývajících možnostech.</span><span class="sxs-lookup"><span data-stu-id="57696-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="57696-126">Nakonfigurujte pomocí následujícího postupu platné třídy práce pro položku nabídky mobilního zařízení:</span><span class="sxs-lookup"><span data-stu-id="57696-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="57696-127">Na kartě s náhledem **Pracovní třídy** vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="57696-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="57696-128">V poli **ID pracovní třídy** můžete vybrat *Prodej* nebo *Výdej PO* v závislosti na skladu, který budete používat.</span><span class="sxs-lookup"><span data-stu-id="57696-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="57696-129">V tomto scénáři vyberte *Výdej PO*.</span><span class="sxs-lookup"><span data-stu-id="57696-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="57696-130">Pole **Typ pracovního příkazu** je automaticky nastaveno na *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="57696-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="57696-131">Vytvořit nabídku mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="57696-131">Set up a mobile device menu</span></span>

<span data-ttu-id="57696-132">Pomocí těchto kroků přidejte do nabídky položku, kterou jste právě vytvořili, do nabídky **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="57696-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="57696-133">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="57696-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="57696-134">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="57696-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="57696-135">V podokně seznamu jsou zobrazeny všechny nabídky mobilních zařízení.</span><span class="sxs-lookup"><span data-stu-id="57696-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="57696-136">V seznamu vyberte *Odchozí*.</span><span class="sxs-lookup"><span data-stu-id="57696-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="57696-137">V mřížce **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky *Vyzvednutí řádku prodejní položky*, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="57696-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="57696-138">Stisknutím tlačítka se šipkou doprava přesuňte položku nabídky *Výběr řádku skupiny prodeje* do seznamu **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="57696-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="57696-139">Pomocí šipky nahoru nebo tlačítek šipky dolů přesuňte položku nabídky na požadované místo ve struktuře nabídky.</span><span class="sxs-lookup"><span data-stu-id="57696-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="57696-140">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="57696-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="57696-141">Nastavit šablonu práce</span><span class="sxs-lookup"><span data-stu-id="57696-141">Set up a work template</span></span>

1. <span data-ttu-id="57696-142">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="57696-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="57696-143">V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="57696-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="57696-144">V mřížce **Přehled** vyhledejte a vyberte pracovní šablonu, která by měla být použita s touto funkcí.</span><span class="sxs-lookup"><span data-stu-id="57696-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="57696-145">V tomto scénáři vyberte šablonu *51 vybrat pro fázi*.</span><span class="sxs-lookup"><span data-stu-id="57696-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="57696-146">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="57696-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="57696-147">V dialogovém okně editoru dotazu na kartě **Třídění** přidejte tlačítkem **Přidat** řádek a pak nastavte následující hodnoty pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="57696-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="57696-148">Ve sloupci **Tabulka** vyberte *Dočasné pracovní transakce*.</span><span class="sxs-lookup"><span data-stu-id="57696-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="57696-149">Ve sloupci **Odvozená tabulka** vyberte *Dočasné pracovní transakce*.</span><span class="sxs-lookup"><span data-stu-id="57696-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="57696-150">Ve sloupci **Pole** zvolte *Číslo položky*.</span><span class="sxs-lookup"><span data-stu-id="57696-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="57696-151">Ve sloupci **Směr vyhledávání** vyberte *Vzestupně*.</span><span class="sxs-lookup"><span data-stu-id="57696-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="57696-152">Volbou **OK** uložte svá nastavení a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="57696-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="57696-153">Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“</span><span class="sxs-lookup"><span data-stu-id="57696-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="57696-154">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="57696-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57696-155">Aby funkce seskupování řádků vyskladnění fungovala, musí být pracovní řádky seřazeny podle ID položky.</span><span class="sxs-lookup"><span data-stu-id="57696-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="57696-156">Pokud řádky se stejnými položkami nejsou seřazeny jeden po druhém, nebudou seskupeny.</span><span class="sxs-lookup"><span data-stu-id="57696-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="57696-157">Příklad</span><span class="sxs-lookup"><span data-stu-id="57696-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="57696-158">Vytvořit práci výdeje</span><span class="sxs-lookup"><span data-stu-id="57696-158">Create picking work</span></span>

<span data-ttu-id="57696-159">Dříve než můžete nastavit seskupování řádků vyskladnění, musíte vytvořit nějakou způsobilou výstupní práci.</span><span class="sxs-lookup"><span data-stu-id="57696-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="57696-160">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="57696-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="57696-161">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="57696-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="57696-162">V poli **Účet odběratele** vyberte *US-004*.</span><span class="sxs-lookup"><span data-stu-id="57696-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="57696-163">Na pevné záložce **Obecné** v poli **Sklad** vyberte *51*.</span><span class="sxs-lookup"><span data-stu-id="57696-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="57696-164">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="57696-164">Select **OK**.</span></span>
1. <span data-ttu-id="57696-165">Na kartě s náhledem **Řádky prodejní objednávky** přidejte následujících šest řádků:</span><span class="sxs-lookup"><span data-stu-id="57696-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="57696-166">**Řádek 1:** v poli **Číslo položky** vyberte *M9200*.</span><span class="sxs-lookup"><span data-stu-id="57696-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="57696-167">Do pole **Množství** zadejte *3*.</span><span class="sxs-lookup"><span data-stu-id="57696-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="57696-168">**Řádek 2:** v poli **Číslo položky** vyberte *M9201*.</span><span class="sxs-lookup"><span data-stu-id="57696-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="57696-169">Do pole **Množství** zadejte *3*.</span><span class="sxs-lookup"><span data-stu-id="57696-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="57696-170">**Řádek 3:** v poli **Číslo položky** vyberte *M9202*.</span><span class="sxs-lookup"><span data-stu-id="57696-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="57696-171">Do pole **Množství** zadejte *2*.</span><span class="sxs-lookup"><span data-stu-id="57696-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="57696-172">**Řádek 4:** v poli **Číslo položky** vyberte *M9200*.</span><span class="sxs-lookup"><span data-stu-id="57696-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="57696-173">Do pole **Množství** zadejte *1*.</span><span class="sxs-lookup"><span data-stu-id="57696-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="57696-174">**Řádek 5:** v poli **Číslo položky** vyberte *M9200*.</span><span class="sxs-lookup"><span data-stu-id="57696-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="57696-175">Do pole **Množství** zadejte *3*.</span><span class="sxs-lookup"><span data-stu-id="57696-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="57696-176">**Řádek 6:** v poli **Číslo položky** vyberte *M9202*.</span><span class="sxs-lookup"><span data-stu-id="57696-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="57696-177">Do pole **Množství** zadejte *7*.</span><span class="sxs-lookup"><span data-stu-id="57696-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="57696-178">Zde je souhrn celkových množství pro každou položku:</span><span class="sxs-lookup"><span data-stu-id="57696-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="57696-179">**Položka M9200:** *7* ks</span><span class="sxs-lookup"><span data-stu-id="57696-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="57696-180">**Položka M9201:** *3* ks</span><span class="sxs-lookup"><span data-stu-id="57696-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="57696-181">**Položka M9202:** *9* ks</span><span class="sxs-lookup"><span data-stu-id="57696-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="57696-182">Před vydáním objednávek do skladu je třeba zajistit, aby skladová místa pro vyskladnění měla dostatečné množství zásob pro všechny položky ve všech objednávkách.</span><span class="sxs-lookup"><span data-stu-id="57696-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="57696-183">Zkontrolujte nastavení **Směrnice skladového místa** pro určení, která výdejní skladová místa se použijí pro výdej prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="57696-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="57696-184">Pokud používáte prostředí ukázkových dat Contoso pro sklad *51*, potvrďte, že jsou k dispozici zásoby.</span><span class="sxs-lookup"><span data-stu-id="57696-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="57696-185">Nyní musíte rezervovat zásoby pro každý řádek.</span><span class="sxs-lookup"><span data-stu-id="57696-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="57696-186">Na kartě s náhledem **Řádky prodejní objednávky** vyberte jeden z řádků, které je třeba rezervovat.</span><span class="sxs-lookup"><span data-stu-id="57696-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="57696-187">V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="57696-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="57696-188">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** k použití rezervace.</span><span class="sxs-lookup"><span data-stu-id="57696-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="57696-189">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="57696-189">Then close the page.</span></span>
1. <span data-ttu-id="57696-190">Opakujte kroky 8 až 10 pro zbývající řádky, které je třeba rezervovat.</span><span class="sxs-lookup"><span data-stu-id="57696-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="57696-191">Nyní musíte vydat prodejní objednávku do skladu.</span><span class="sxs-lookup"><span data-stu-id="57696-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="57696-192">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="57696-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="57696-193">Zobrazí se zpráva s oznámením, že byla vytvořena zásilka a vlna a že vlna byla odeslána k dávkovému spuštění.</span><span class="sxs-lookup"><span data-stu-id="57696-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="57696-194">Po dokončení vlny a všech následných úloh se vytvoří ID práce pro práci, která má šest řádků.</span><span class="sxs-lookup"><span data-stu-id="57696-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="57696-195">Řádky jsou seřazeny podle čísla položky.</span><span class="sxs-lookup"><span data-stu-id="57696-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="57696-196">Přejděte na **Řízení skladu \> Práce \> Všechna práce** k zobrazení práce, která byla vytvořena.</span><span class="sxs-lookup"><span data-stu-id="57696-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="57696-197">Poznamenejte si hodnotu **ID práce**, protože ji budete potřebovat v dalším postupu.</span><span class="sxs-lookup"><span data-stu-id="57696-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="57696-198">Zahájení výběru z mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="57696-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="57696-199">Přihlaste se do mobilního zařízení jako uživatel, který je nastaven pro sklad *51*.</span><span class="sxs-lookup"><span data-stu-id="57696-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="57696-200">V mobilním zařízení vyberte nabídku obsahující novou položku nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="57696-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="57696-201">V tomto scénáři vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="57696-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="57696-202">Vyberte položku nabídky **Vyskladnění skupiny řádku prodeje** a zahajte vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="57696-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="57696-203">Zadejte hodnotu **ID práce**, kterou jste si poznamenali v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="57696-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="57696-204">Měli byste vidět krok výběru, kde jsou všechny řádky pro výběr položky *M9200* seskupeny a měli byste obdržet pokyn k výběru *7* ks položky *M9200*.</span><span class="sxs-lookup"><span data-stu-id="57696-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="57696-205">Na mobilním zařízení byla vychystávací práce pro tři vychystávací pracovní linky agregována do jednoho vychystávacího kroku pro uživatele.</span><span class="sxs-lookup"><span data-stu-id="57696-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="57696-206">Potvrďte krok vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="57696-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="57696-207">Přejděte na stránku práce pro ID práce a všimněte si, že všechny tři řádky vyskladnění pro položku *M9200* byly uzavřeny současně.</span><span class="sxs-lookup"><span data-stu-id="57696-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="57696-208">Vraťte se do mobilního zařízení a pokračujte ve výběru.</span><span class="sxs-lookup"><span data-stu-id="57696-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="57696-209">Měl být předložen pracovní řádek 4 pro položku *M9201*.</span><span class="sxs-lookup"><span data-stu-id="57696-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="57696-210">Protože na objednávce byl pouze jeden řádek práce, není co agregovat.</span><span class="sxs-lookup"><span data-stu-id="57696-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="57696-211">Potvrďte krok vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="57696-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="57696-212">Poslední krok vyskladnění na mobilním zařízení agreguje poslední dva řádky vyskladnění z pracovní objednávky.</span><span class="sxs-lookup"><span data-stu-id="57696-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="57696-213">Dokončete krok vyskladnění pro *9* kusů položky *M9202*.</span><span class="sxs-lookup"><span data-stu-id="57696-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="57696-214">Pro dokončení práce potvrďte krok vložení a dalších párů vyskladnění/vložení.</span><span class="sxs-lookup"><span data-stu-id="57696-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="57696-215">Řádky práce lze seskupit pouze v případě, že jdou po sobě.</span><span class="sxs-lookup"><span data-stu-id="57696-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="57696-216">Následující funkce není podporována:</span><span class="sxs-lookup"><span data-stu-id="57696-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="57696-217">Položky se skutečnou hmotností</span><span class="sxs-lookup"><span data-stu-id="57696-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="57696-218">Pokud je v práci nějaké zboží se skutečnou hmotností, zobrazí se před začátkem vyskladnění chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="57696-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="57696-219">Výdej kusů</span><span class="sxs-lookup"><span data-stu-id="57696-219">Piece picking</span></span>
>   - <span data-ttu-id="57696-220">Řádky práce s nedokončenou doplňovací prací</span><span class="sxs-lookup"><span data-stu-id="57696-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="57696-221">Naměrné vyskladnění</span><span class="sxs-lookup"><span data-stu-id="57696-221">Over-picking</span></span>
>   - <span data-ttu-id="57696-222">Opakované přidělení zboží při krátkodobém vyskladnění</span><span class="sxs-lookup"><span data-stu-id="57696-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]