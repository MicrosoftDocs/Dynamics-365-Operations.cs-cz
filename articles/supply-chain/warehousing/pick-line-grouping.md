---
title: Seskupování řádků vyskladnění
description: Toto téma poskytuje přehled seskupení řádků výdeje.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017729"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="b7412-103">Seskupování řádků vyskladnění</span><span class="sxs-lookup"><span data-stu-id="b7412-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7412-104">V seskupování řádků výdeje lze kombinovat více řádků práce, které mají stejné zboží a umístění, do jednoho výeje, které se uživateli zobrazí v mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="b7412-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="b7412-105">Pracovníci skladu tedy mohou získat nejúčinnější pokyny, které jsou možné, ale je zachováno i povinné oddělení pracovních řádků v systému (například pro různé kontejnery a objednávky).</span><span class="sxs-lookup"><span data-stu-id="b7412-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="b7412-106">Nastavit seskupování řádků výdeje</span><span class="sxs-lookup"><span data-stu-id="b7412-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b7412-107">Vytvoření položky nabídky mobilních zařízení</span><span class="sxs-lookup"><span data-stu-id="b7412-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b7412-108">Přejděte do **Řízení skladu \> Nastavení \> Mobilní řařízení \> Položky nabídky mobilního zařízení** a vytvořte novou položku nabídky nazvanou **Výdej řádku prodejní skupiny – Řízeno uživatelem**.</span><span class="sxs-lookup"><span data-stu-id="b7412-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items** , and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="b7412-109">V nabídce **Položky nabídky mobilního zařízení** nastavtenásledující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b7412-109">Under **Mobile device menu items** , set the following values:</span></span>

    - <span data-ttu-id="b7412-110">V poli **Název položky nabídky** zadejte **Vyskladňování prodeje - řádek skupiny**.</span><span class="sxs-lookup"><span data-stu-id="b7412-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="b7412-111">V poli **Nadpis** zadejte **Vyskladňování prodeje - řádek skupiny**.</span><span class="sxs-lookup"><span data-stu-id="b7412-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="b7412-112">V poli **Režim** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="b7412-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="b7412-113">Nastavte hodnotu možnosti **Použít stávající práci** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b7412-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="b7412-114">Na pevné záložce **Obecné** můžete nastavit následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b7412-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="b7412-115">V poli **Řídí** nastavte **Řízeno uživatelem**.</span><span class="sxs-lookup"><span data-stu-id="b7412-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="b7412-116">Nastavte volbu **Generovat registrační značku vozidla** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b7412-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="b7412-117">Nastavte možnost **Výdej skupiny** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b7412-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="b7412-118">Na pevné záložce **Pracovní třídy** nakonfigurujte pomocí následujícího postupu platné třídy práce pro položku nabídky mobilního zařízení:</span><span class="sxs-lookup"><span data-stu-id="b7412-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="b7412-119">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="b7412-119">Select **New**.</span></span>
    2. <span data-ttu-id="b7412-120">V poli **ID pracovní třídy** vyberte **Prodej** nebo **Výdej PO** v závislosti na skladu, který budete používat.</span><span class="sxs-lookup"><span data-stu-id="b7412-120">In the **Work class ID** field, select **Sales** or **SO Pick** , depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="b7412-121">V poli **Typ pracovního příkazu** vyberte možnost **Prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="b7412-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="b7412-122">Vytvořit nabídku mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="b7412-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="b7412-123">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="b7412-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="b7412-124">Přidejte položku nabídky, kterou jste právě vytvořili, do požadované nabídky.</span><span class="sxs-lookup"><span data-stu-id="b7412-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="b7412-125">Nastavit šablonu práce</span><span class="sxs-lookup"><span data-stu-id="b7412-125">Set up a work template</span></span>

1. <span data-ttu-id="b7412-126">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="b7412-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b7412-127">Najděte šablonu práce, která má být použita s touto funkcí.</span><span class="sxs-lookup"><span data-stu-id="b7412-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="b7412-128">V tomto příkladu vyberte šablonu pro práci Contoso **51 výdej ddo fáze**.</span><span class="sxs-lookup"><span data-stu-id="b7412-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="b7412-129">V nabídce vyberte příkaz **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="b7412-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="b7412-130">Na kartě **Řazení** vyberte možnost **Přidat** a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b7412-130">On the **Sorting** tab, select **Add** , and then set the following values:</span></span>

    - <span data-ttu-id="b7412-131">V poli **Tabulka** vyberte **Dočasné pracovní transakce**.</span><span class="sxs-lookup"><span data-stu-id="b7412-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="b7412-132">V poli **Odvozená tabulka** vyberte **Dočasné pracovní transakce**.</span><span class="sxs-lookup"><span data-stu-id="b7412-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="b7412-133">V poli **Pole** zvolte **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="b7412-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="b7412-134">V poli **Směr vyhledávání** vyberte **Vzestupně**.</span><span class="sxs-lookup"><span data-stu-id="b7412-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="b7412-135">Aby funkce seskupování řádků vyskladnění fungovala, musí být pracovní řádky seřazeny podle ID položky.</span><span class="sxs-lookup"><span data-stu-id="b7412-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="b7412-136">Pokud řádky se stejnými položkami nejsou seřazeny jeden po druhém, nebudou seskupeny.</span><span class="sxs-lookup"><span data-stu-id="b7412-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="b7412-137">Příklad</span><span class="sxs-lookup"><span data-stu-id="b7412-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="b7412-138">Vytvořit práci výdeje</span><span class="sxs-lookup"><span data-stu-id="b7412-138">Create picking work</span></span>

<span data-ttu-id="b7412-139">Dříve než můžete nastavit seskupování řádků vyskladnění, musíte vytvořit nějakou způsobilou výstupní práci.</span><span class="sxs-lookup"><span data-stu-id="b7412-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="b7412-140">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="b7412-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="b7412-141">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="b7412-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="b7412-142">V poli **Účet odběratele** vyberte libovolného zákazníka.</span><span class="sxs-lookup"><span data-stu-id="b7412-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="b7412-143">Na pevné záložce **Obecné** v poli **Sklad** vyberte **51**.</span><span class="sxs-lookup"><span data-stu-id="b7412-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="b7412-144">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7412-144">Then select **OK**.</span></span>
5. <span data-ttu-id="b7412-145">Do volby **Řádky prodejní objednávky** přidejte následujících šest řádků:</span><span class="sxs-lookup"><span data-stu-id="b7412-145">Under **Sales order lines** , add the following six lines:</span></span>

    - <span data-ttu-id="b7412-146">**Řádek 1:** v poli **Číslo položky** vyberte **M9200**.</span><span class="sxs-lookup"><span data-stu-id="b7412-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="b7412-147">Do pole **Množství** zadejte **3**.</span><span class="sxs-lookup"><span data-stu-id="b7412-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="b7412-148">**Řádek 2:** v poli **Číslo položky** vyberte **M9201**.</span><span class="sxs-lookup"><span data-stu-id="b7412-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="b7412-149">Do pole **Množství** zadejte **3**.</span><span class="sxs-lookup"><span data-stu-id="b7412-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="b7412-150">**Řádek 3:** v poli **Číslo položky** vyberte **M9202**.</span><span class="sxs-lookup"><span data-stu-id="b7412-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="b7412-151">Do pole **Množství** zadejte **2**.</span><span class="sxs-lookup"><span data-stu-id="b7412-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="b7412-152">**Řádek 4:** v poli **Číslo položky** vyberte **M9200**.</span><span class="sxs-lookup"><span data-stu-id="b7412-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="b7412-153">Do pole **Množství** zadejte **1**.</span><span class="sxs-lookup"><span data-stu-id="b7412-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="b7412-154">**Řádek 5:** v poli **Číslo položky** vyberte **M9200**.</span><span class="sxs-lookup"><span data-stu-id="b7412-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="b7412-155">Do pole **Množství** zadejte **3**.</span><span class="sxs-lookup"><span data-stu-id="b7412-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="b7412-156">**Řádek 6:** v poli **Číslo položky** vyberte **M9202**.</span><span class="sxs-lookup"><span data-stu-id="b7412-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="b7412-157">Do pole **Množství** zadejte **7**.</span><span class="sxs-lookup"><span data-stu-id="b7412-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="b7412-158">Zde je souhrn celkových množství pro každou položku:</span><span class="sxs-lookup"><span data-stu-id="b7412-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="b7412-159">**Položka M9200:** každá 7</span><span class="sxs-lookup"><span data-stu-id="b7412-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="b7412-160">**Položka M9201:** každá 3</span><span class="sxs-lookup"><span data-stu-id="b7412-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="b7412-161">**Položka M9202:** každá 9</span><span class="sxs-lookup"><span data-stu-id="b7412-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="b7412-162">Před vydáním objednávek do skladu je třeba zajistit, aby skladová místa pro vyskladnění měla dostatečné množství zásob pro všechny položky ve všech objednávkách.</span><span class="sxs-lookup"><span data-stu-id="b7412-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="b7412-163">Zkontrolujte nastavení **Směrnice skladového místa** pro určení, která výdejní skladová místa se použijí pro výdej prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b7412-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="b7412-164">Rezervace zásob a jejich uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="b7412-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="b7412-165">Je vytvořeno ID práce, které má šest řádků.</span><span class="sxs-lookup"><span data-stu-id="b7412-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="b7412-166">Řádky jsou seřazeny podle čísla položky.</span><span class="sxs-lookup"><span data-stu-id="b7412-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="b7412-167">Spustit tok mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="b7412-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="b7412-168">V mobilním zařízení vyberte nabídku obsahující novou položku nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="b7412-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="b7412-169">Vyberte položku nabídky **Vyskladnění prodeje – řádek skupiny** a zahajte vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="b7412-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="b7412-170">Po výběru nabídky a zadání ID práce se zobrazí krok vyskladnění, ve kterém jsou seskupeny všechny řádky vyskladnění pro položku M9200.</span><span class="sxs-lookup"><span data-stu-id="b7412-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="b7412-171">Obdržíte pokyn k vyzvednutí 7 jednotlivých položek M9200.</span><span class="sxs-lookup"><span data-stu-id="b7412-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="b7412-172">Potvrďte krok vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="b7412-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="b7412-173">Přejděte na obrazovku klienta probíhající práce a všimněte si, že všechny tři řádky vyskladnění pro položku M9200 byly uzavřeny současně.</span><span class="sxs-lookup"><span data-stu-id="b7412-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="b7412-174">Uveden je řádek práce 4.</span><span class="sxs-lookup"><span data-stu-id="b7412-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="b7412-175">Potvrďte krok vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="b7412-175">Confirm the pick step.</span></span>

    <span data-ttu-id="b7412-176">Poslední krok vyskladnění na mobilním zařízení agreguje poslední dva řádky vyskladnění z pracovní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b7412-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="b7412-177">Dokončete krok vyskladnění pro 9 kusů položky M9202.</span><span class="sxs-lookup"><span data-stu-id="b7412-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="b7412-178">Pro dokončení práce potvrďte krok vložení a dalších párů vyskladnění/vložení.</span><span class="sxs-lookup"><span data-stu-id="b7412-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="b7412-179">Řádky práce lze seskupit pouze v případě, že jdou po sobě.</span><span class="sxs-lookup"><span data-stu-id="b7412-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="b7412-180">Následující funkce není podporována:</span><span class="sxs-lookup"><span data-stu-id="b7412-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="b7412-181">Položka se skutečnou hmotností.</span><span class="sxs-lookup"><span data-stu-id="b7412-181">Catch-weight items.</span></span> <span data-ttu-id="b7412-182">Pokud je v práci nějaké zboží se skutečnou hmotností, zobrazí se před začátkem vyskladnění chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="b7412-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="b7412-183">Výdej kusů.</span><span class="sxs-lookup"><span data-stu-id="b7412-183">Piece picking.</span></span>
>    - <span data-ttu-id="b7412-184">Řádky práce s nedokončenou doplňovací prací.</span><span class="sxs-lookup"><span data-stu-id="b7412-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="b7412-185">Naměrné vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="b7412-185">Over-picking.</span></span>
>    - <span data-ttu-id="b7412-186">Opakované přidělení zboží při krátkodobém vyskladnění</span><span class="sxs-lookup"><span data-stu-id="b7412-186">Short picking with item reallocation</span></span>
