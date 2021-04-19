---
title: Seskupení vyskladnění
description: Seskupení vyskladnění nabízejí způsob, jak vybrat více registračních značek najednou a poté je vyskladnit do různých umístění. Mohou být velmi užitečné pro maloobchod, kde registrační značky obvykle nejsou plnými paletami zásob.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b3a7d1b7109b83b26c8187a7f0d271f1c82f6d63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840358"
---
# <a name="putaway-clusters"></a><span data-ttu-id="114ce-104">Seskupení vyskladnění</span><span class="sxs-lookup"><span data-stu-id="114ce-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="114ce-105">Seskupení vyskladnění nabízejí způsob, jak vybrat více registračních značek najednou a poté je vyskladnit do různých umístění.</span><span class="sxs-lookup"><span data-stu-id="114ce-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="114ce-106">Tento proces se často označuje jako *milk run*.</span><span class="sxs-lookup"><span data-stu-id="114ce-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="114ce-107">Seskupení vyskladnění mohou být velmi užitečná pro maloobchod, kde registrační značky obvykle nejsou plnými paletami zásob.</span><span class="sxs-lookup"><span data-stu-id="114ce-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="114ce-108">Zapnutí funkce seskupení vyskladnění</span><span class="sxs-lookup"><span data-stu-id="114ce-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="114ce-109">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="114ce-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="114ce-110">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="114ce-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="114ce-111">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="114ce-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="114ce-112">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="114ce-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="114ce-113">**Název funkce:** *Funkce seskupení vyskladnění*</span><span class="sxs-lookup"><span data-stu-id="114ce-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="114ce-114">Nastavení pro příkladový scénář</span><span class="sxs-lookup"><span data-stu-id="114ce-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="114ce-115">Profily seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-115">Cluster profiles</span></span>

<span data-ttu-id="114ce-116">Profil seskupení vyskladnění určuje, kam se položka dostane, na základě umístění, které je položce přiřazeno v době přijetí.</span><span class="sxs-lookup"><span data-stu-id="114ce-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="114ce-117">Pokud jsou vyžadována různá seskupení, měly by být pro každou položku nabídky mobilního zařízení vytvořena seskupení vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="114ce-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="114ce-118">Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Profily seskupení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="114ce-119">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="114ce-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="114ce-120">V zobrazení **Záhlaví** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="114ce-121">**ID profilu seskupení vyskladnění:** *Seskupení vyskladnění*</span><span class="sxs-lookup"><span data-stu-id="114ce-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="114ce-122">**Název ID profilu seskupení vyskladnění:** *Seskupení vyskladnění*</span><span class="sxs-lookup"><span data-stu-id="114ce-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="114ce-123">**Typ seskupení:** *Vyskladnění*</span><span class="sxs-lookup"><span data-stu-id="114ce-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="114ce-124">**Pořadové číslo:** Přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="114ce-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="114ce-125">Chcete-li, aby byla dostupná požadovaná pole, na záložce s náhledem **Obecné** vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="114ce-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="114ce-126">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="114ce-127">**Načasování přiřazení seskupení:** *Při přijetí*</span><span class="sxs-lookup"><span data-stu-id="114ce-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="114ce-128">Toto pole definuje, zda by mělo být seskupení vyskladnění přiřazeno okamžitě po přijetí zásob, nebo zda by mělo být tříděno později.</span><span class="sxs-lookup"><span data-stu-id="114ce-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="114ce-129">**Pravidlo přiřazení seskupení:** *Manuální*</span><span class="sxs-lookup"><span data-stu-id="114ce-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="114ce-130">Toto pole definuje, zda má být přiřazení seskupení určeno automaticky systémem nebo ručně uživatelem.</span><span class="sxs-lookup"><span data-stu-id="114ce-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="114ce-131">**Kód směrnice:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="114ce-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="114ce-132">**Vyhledání seskupení vyskladnění:** *Příjemka*</span><span class="sxs-lookup"><span data-stu-id="114ce-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="114ce-133">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-133">The following values are available:</span></span>

        - <span data-ttu-id="114ce-134">**Příjemka** - Umístění je nalezeno ihned během příjmu.</span><span class="sxs-lookup"><span data-stu-id="114ce-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="114ce-135">**Uzavření seskupení**- Umístění nalezené, když je seskupení uzavřené.</span><span class="sxs-lookup"><span data-stu-id="114ce-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="114ce-136">**Nasměrované uživatelem** - Místo je nalezeno, když je registrační značka vybrána ze seskupení vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="114ce-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="114ce-137">V tomto případě není zadáno žádné umístění, když je vytvořena práce vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="114ce-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="114ce-138">Během samotného vyskladnění musí uživatel naskenovat registrační značku nebo ID práce, aby zahájil krok vložení.</span><span class="sxs-lookup"><span data-stu-id="114ce-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="114ce-139">Systém poté znovu vyhledá místo vložení a řekne uživateli, kam má vybrané množství uložit.</span><span class="sxs-lookup"><span data-stu-id="114ce-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="114ce-140">**Seskupení vyskladnění podle uživatele:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="114ce-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="114ce-141">Toto pole definuje, zda by každé seskupení mělo být pro každého uživatele jedinečné, když jsou seskupení přiřazována automaticky.</span><span class="sxs-lookup"><span data-stu-id="114ce-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="114ce-142">Je k dispozici pouze v případě, kdy je pole **Pravidlo seskupení vyskladnění** nastaveno na *Automatické*.</span><span class="sxs-lookup"><span data-stu-id="114ce-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="114ce-143">**Omezení jednotky:** Ponechejte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="114ce-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="114ce-144">Toto pole definuje jednotku, která musí být přijata, aby byl profil platný.</span><span class="sxs-lookup"><span data-stu-id="114ce-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="114ce-145">Ponecháte-li ho prázdné, jsou platné všechny jednotky.</span><span class="sxs-lookup"><span data-stu-id="114ce-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="114ce-146">**Přerušení jednotky práce:** *Individuální*</span><span class="sxs-lookup"><span data-stu-id="114ce-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="114ce-147">Toto pole definuje, zda by měly být všechny zásoby sloučeny (pomocí ID sestavení a registrační značky) na jednu registrační značku, když je sestavení uzavřeno, a zda by měly být vyskladněny jako jedna registrační značka nebo samostatně na přijatých registračních značkách.</span><span class="sxs-lookup"><span data-stu-id="114ce-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="114ce-148">Toto pole není k dispozici, když je pole **Vyhledání sestavení vyskladnění** nastaveno na *Příjemka*.</span><span class="sxs-lookup"><span data-stu-id="114ce-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="114ce-149">**Seskupení přetrvává jako nadřazená registrační značka:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="114ce-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="114ce-150">Pokud je tato možnost nastavena na *Ano* po dokončení kroku vložení, ID sestavení se stane nadřazenou registrační značkou a všechny položky v ID seskupení budou propojeny s touto nadřazenou registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="114ce-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="114ce-151">Na záložce s náhledem **Řazení seskupení** můžete definovat kritéria třídění vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="114ce-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="114ce-152">Vyberte **Nový** na panelu nástrojů pro přidání řádku a pak nastavte tyto hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="114ce-153">**Pořadové číslo:** Přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="114ce-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="114ce-154">**Název pole:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="114ce-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="114ce-155">Toto pole definuje pole, které by tento řádek měl použít jako kritérium řazení.</span><span class="sxs-lookup"><span data-stu-id="114ce-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="114ce-156">**Řazení:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="114ce-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="114ce-157">Toto pole určuje, zda se třídění provede vzestupně nebo sestupně.</span><span class="sxs-lookup"><span data-stu-id="114ce-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="114ce-158">Na záložce s náhledem **Pracovní šablona sestavení** vyberte v panelu nástrojů **Nový**, chcete-li přidat řádek a poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="114ce-159">**Typ pracovního příkazu:** *Nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="114ce-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="114ce-160">**Pracovní šablona:** *61 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="114ce-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="114ce-161">V podokně akcí vyberte **Uložit** a potom vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="114ce-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="114ce-162">V dialogovém okně **Seskupení vyskladnění** na kartě **Oblast** vyberte **Přidat** a přidejte druhý řádek do dotazu.</span><span class="sxs-lookup"><span data-stu-id="114ce-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="114ce-163">Poté aktualizujte řádky dotazu, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="114ce-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="114ce-164">Tabulka</span><span class="sxs-lookup"><span data-stu-id="114ce-164">Table</span></span> | <span data-ttu-id="114ce-165">Odvozená tabulka</span><span class="sxs-lookup"><span data-stu-id="114ce-165">Derived table</span></span> | <span data-ttu-id="114ce-166">Pole</span><span class="sxs-lookup"><span data-stu-id="114ce-166">Field</span></span> | <span data-ttu-id="114ce-167">Kritéria</span><span class="sxs-lookup"><span data-stu-id="114ce-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="114ce-168">Práce</span><span class="sxs-lookup"><span data-stu-id="114ce-168">Work</span></span> | <span data-ttu-id="114ce-169">Práce</span><span class="sxs-lookup"><span data-stu-id="114ce-169">Work</span></span> | <span data-ttu-id="114ce-170">Sklad</span><span class="sxs-lookup"><span data-stu-id="114ce-170">Warehouse</span></span> | <span data-ttu-id="114ce-171">*61*</span><span class="sxs-lookup"><span data-stu-id="114ce-171">*61*</span></span> |
    | <span data-ttu-id="114ce-172">Práce</span><span class="sxs-lookup"><span data-stu-id="114ce-172">Work</span></span> | <span data-ttu-id="114ce-173">Práce</span><span class="sxs-lookup"><span data-stu-id="114ce-173">Work</span></span> | <span data-ttu-id="114ce-174">ID práce</span><span class="sxs-lookup"><span data-stu-id="114ce-174">Work ID</span></span> | <span data-ttu-id="114ce-175">Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="114ce-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="114ce-176">Vyberte **OK**, uložte dotaz a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="114ce-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="114ce-177">V podokně akcí zvolte **Uložit** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="114ce-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="114ce-178">Pole v profilu seskupení, která se při zobrazování zobrazují šedě, když je možnost **Vygenerovat ID seskupení** nastavena na *Ano*, nejsou k dispozici a při použití této funkce nebudou brány v úvahu.</span><span class="sxs-lookup"><span data-stu-id="114ce-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="114ce-179">Položky nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="114ce-179">Mobile device menu items</span></span>

<span data-ttu-id="114ce-180">Pro tuto funkci jsou k dispozici dvě nové položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="114ce-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="114ce-181">Položka nabídky **Přijmout a setřídit seskupení** se používá k třídění přijatých zásob do seskupení vyskladnění při příjmu.</span><span class="sxs-lookup"><span data-stu-id="114ce-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="114ce-182">Položka nabídky **Seskupení vyskladnění** slouží k vyskladnění sestavení po jeho přiřazení.</span><span class="sxs-lookup"><span data-stu-id="114ce-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="114ce-183">Přijmout a setřídit seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-183">Receive and sort cluster</span></span>

<span data-ttu-id="114ce-184">Vytvořte novou položku nabídky mobilního zařízení pro příjem zásob a řazení do seskupení.</span><span class="sxs-lookup"><span data-stu-id="114ce-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="114ce-185">Tato položka nabídky vytvoří příchozí práci po přijetí zásob, což znamená, že se položka nabídky příjmu použije pro seskupení vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="114ce-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="114ce-186">Položku nabídky **Přijmout a setřídit seskupení** lze použít s následujícími položkami nabídky příjmu:</span><span class="sxs-lookup"><span data-stu-id="114ce-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="114ce-187">Přijetí řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="114ce-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="114ce-188">Přijetí položky nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="114ce-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="114ce-189">Přijetí položky nákladu</span><span class="sxs-lookup"><span data-stu-id="114ce-189">Load item receiving</span></span>

1. <span data-ttu-id="114ce-190">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="114ce-191">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="114ce-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="114ce-192">V zobrazení **Záhlaví** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="114ce-193">**Název položky nabídky:** *Přijmout a setřídit seskupení*</span><span class="sxs-lookup"><span data-stu-id="114ce-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="114ce-194">**Název:** *Přijmout a setřídit seskupení*</span><span class="sxs-lookup"><span data-stu-id="114ce-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="114ce-195">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="114ce-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="114ce-196">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="114ce-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="114ce-197">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="114ce-198">**Proces tvorby práce:** *Příjem položky nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="114ce-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="114ce-199">**Generovat registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="114ce-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="114ce-200">**Přiřadit seskupení vyskladnění:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="114ce-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="114ce-201">Možnost **Přiřadit seskupení vyskladnění** je k dispozici pouze pro jednokrokovou aktivitu *Proces tvorby práce* pro příjem.</span><span class="sxs-lookup"><span data-stu-id="114ce-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="114ce-202">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="114ce-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="114ce-203">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="114ce-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="114ce-204">Odložení seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-204">Cluster putaway</span></span>

<span data-ttu-id="114ce-205">Vytvořte novou položku nabídky mobilního zařízení pro vyskladnění sestavení po jeho přiřazení.</span><span class="sxs-lookup"><span data-stu-id="114ce-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="114ce-206">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="114ce-207">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="114ce-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="114ce-208">V zobrazení **Záhlaví** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="114ce-209">**Název položky nabídky:** *Vyskladnění seskupení*</span><span class="sxs-lookup"><span data-stu-id="114ce-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="114ce-210">**Název:** *Vyskladnění seskupení*</span><span class="sxs-lookup"><span data-stu-id="114ce-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="114ce-211">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="114ce-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="114ce-212">**Použít existující práci:** - *Ano*</span><span class="sxs-lookup"><span data-stu-id="114ce-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="114ce-213">Na pevné záložce **Obecné** nastavte hodnotu v poli **Řídí:** na *Vyskladnění seskupení*.</span><span class="sxs-lookup"><span data-stu-id="114ce-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="114ce-214">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="114ce-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="114ce-215">Na záložce s náhledem **Pracovní třídy** nastavte platnou pracovní třídu pro tuto položku nabídky mobilního zařízení:</span><span class="sxs-lookup"><span data-stu-id="114ce-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="114ce-216">**ID pracovní třídy:** *Nákup*</span><span class="sxs-lookup"><span data-stu-id="114ce-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="114ce-217">**Typ pracovního příkazu:** *Nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="114ce-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="114ce-218">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="114ce-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="114ce-219">Nabídka mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="114ce-219">Mobile device menu</span></span>

<span data-ttu-id="114ce-220">Přidejte položky nabídky, které jste právě vytvořili, do příchozí nabídky mobilní aplikace.</span><span class="sxs-lookup"><span data-stu-id="114ce-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="114ce-221">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="114ce-222">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="114ce-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="114ce-223">V seznamu nabídek vyberte možnost **Vstupní**.</span><span class="sxs-lookup"><span data-stu-id="114ce-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="114ce-224">V seznamu **Dostupné nabídky a položky nabídky** najděte a vyberte **Přijmout a setřídit seskupení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="114ce-225">Stisknutím tlačítka se šipkou doprava přesuňte vybranou položku nabídky do seznamu **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="114ce-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="114ce-226">Pomocí šipky nahoru nebo šipky dolů přesuňte položku nabídky na požadované místo v nabídce.</span><span class="sxs-lookup"><span data-stu-id="114ce-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="114ce-227">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="114ce-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="114ce-228">Chcete-li přidat zbývající položky nabídky, zopakujte kroky 4 až 7.</span><span class="sxs-lookup"><span data-stu-id="114ce-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="114ce-229">Přiřadit seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-229">Assign cluster</span></span>
    - <span data-ttu-id="114ce-230">Odložení seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="114ce-231">Příklad</span><span class="sxs-lookup"><span data-stu-id="114ce-231">Example scenario</span></span>

<span data-ttu-id="114ce-232">Tento scénář simuluje zpracování seskupení vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="114ce-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="114ce-233">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="114ce-233">Create a purchase order</span></span>

1. <span data-ttu-id="114ce-234">Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="114ce-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="114ce-235">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="114ce-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="114ce-236">V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="114ce-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="114ce-237">**Účet dodavatele:** *1001*</span><span class="sxs-lookup"><span data-stu-id="114ce-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="114ce-238">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="114ce-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="114ce-239">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="114ce-239">Select **OK**.</span></span>

    <span data-ttu-id="114ce-240">Zobrazí se stránka **Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="114ce-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="114ce-241">Na stránce **Všechny nákupní objednávky** na záložce s náhledem **Řádky nákupní objednávky** použijte tlačítko **Přidat řádek** pro přidání následujících řádků:</span><span class="sxs-lookup"><span data-stu-id="114ce-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="114ce-242">Řádek nákupní objednávky 1:</span><span class="sxs-lookup"><span data-stu-id="114ce-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="114ce-243">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="114ce-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="114ce-244">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="114ce-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="114ce-245">Řádek nákupní objednávky 2:</span><span class="sxs-lookup"><span data-stu-id="114ce-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="114ce-246">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="114ce-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="114ce-247">**Množství:** *20*</span><span class="sxs-lookup"><span data-stu-id="114ce-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="114ce-248">Řádek nákupní objednávky 3:</span><span class="sxs-lookup"><span data-stu-id="114ce-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="114ce-249">**Číslo položky:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="114ce-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="114ce-250">**Množství:** *30*</span><span class="sxs-lookup"><span data-stu-id="114ce-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="114ce-251">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="114ce-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="114ce-252">Poznamenejte si číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="114ce-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="114ce-253">Přijetí zásob a jejich vyskladnění z mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="114ce-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="114ce-254">Příjem a třídění zásob do seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="114ce-255">Přihlaste se do mobilní aplikace Řízení skladu jako uživatel, který je nastaven pro sklad *61*.</span><span class="sxs-lookup"><span data-stu-id="114ce-255">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="114ce-256">V hlavní nabídce vyberte **Příchozí**.</span><span class="sxs-lookup"><span data-stu-id="114ce-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="114ce-257">V nabídce **Příchozí** vyberte **Přijímat a setřídit seskupení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="114ce-258">V poli **Ponum** zadejte číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="114ce-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="114ce-259">Vyberte tlačítko **OK** (tlačítko zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="114ce-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="114ce-260">Vyberte pole **Položka**, zadejte číslo položky *A0001* a poté zvolte **OK**..</span><span class="sxs-lookup"><span data-stu-id="114ce-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="114ce-261">Vyberte pole **Množství**, zadejte *10* pomocí číselné klávesnice a poté vyberte tlačítko zaškrtnutí.</span><span class="sxs-lookup"><span data-stu-id="114ce-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="114ce-262">Na stránce s úkolem **Množství** vyberte **OK** (tlačítko zaškrtnutí) k potvrzení zadaného množství.</span><span class="sxs-lookup"><span data-stu-id="114ce-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="114ce-263">Na stránce s úkolem **Položka** vyberte **OK** a potvrďte, že položka *A0001* byla zadána.</span><span class="sxs-lookup"><span data-stu-id="114ce-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="114ce-264">Vyberte pole **ID seskupení** a zadejte hodnotu pro přiřazení ID pro seskupení, který vytváříte.</span><span class="sxs-lookup"><span data-stu-id="114ce-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="114ce-265">ID, které zde zadáte, bude použito při přijetí dvou zbývajících položek v nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="114ce-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="114ce-266">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="114ce-266">Select **OK**.</span></span>

    <span data-ttu-id="114ce-267">Zobrazí se stránka s úkolem **Ponum** a pak se zobrazí zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="114ce-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="114ce-268">Položka *A0001* nyní byla přijat do umístění *RECV* a přiřazena k ID seskupení, které jste zadali v kroku 10.</span><span class="sxs-lookup"><span data-stu-id="114ce-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="114ce-269">Opakováním kroků 4 až 11 přijměte zbývající dvě položky z nákupní objednávky a přiřaďte je k ID seskupení:</span><span class="sxs-lookup"><span data-stu-id="114ce-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="114ce-270">Množství *20* pro položku *A0002*</span><span class="sxs-lookup"><span data-stu-id="114ce-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="114ce-271">Množství *30* pro položku *M9215*</span><span class="sxs-lookup"><span data-stu-id="114ce-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="114ce-272">Zavřete seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-272">Close the cluster</span></span>

<span data-ttu-id="114ce-273">Než bude možné položky v seskupení vyskladnit, musí být seskupení uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="114ce-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="114ce-274">V části Supply Chain Management přejděte na **Řízení skladu \> Práce \> Odchozí \> Pracovní seskupení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="114ce-275">Na stránce **Pracovní seskupení** v sekci **Pracovní seskupení** vyhledejte pole **ID seskupení** pro ID seskupení, které jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="114ce-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="114ce-276">Pokud se seskupení nezobrazí, mohl být již uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="114ce-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="114ce-277">Chcete-li zjistit, zda bylo seskupení uzavřeno, vyberte zaškrtávací políčko **Zobrazit uzavřenou práci** a vyhledejte ID seskupení, které jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="114ce-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="114ce-278">Potom proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="114ce-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="114ce-279">Pokud by bylo seskupení uzavřeno, přeskočte zbývající kroky tohoto postupu a přejděte k dalšímu postupu, [Vyskladnění seskupení](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="114ce-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="114ce-280">Pokud seskupení nebylo uzavřeno, postupujte podle zbývajících kroků tohoto postupu a ručně jej zavřete.</span><span class="sxs-lookup"><span data-stu-id="114ce-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="114ce-281">Poté se přesuňte na následující postup.</span><span class="sxs-lookup"><span data-stu-id="114ce-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="114ce-282">V sekci **Pracovní seskupení** vyberte ID seskupení, které jste zadali dříve.</span><span class="sxs-lookup"><span data-stu-id="114ce-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="114ce-283">V podokně akcí zvolte **Zavřít seskupení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="114ce-284">Poté, co bylo seskupení uzavřeno, již se dále nezobrazuje v sekci **Pracovní seskupení** (pokud není zvoleno zaškrtávací políčko **Zobrazit uzavřenou práci**).</span><span class="sxs-lookup"><span data-stu-id="114ce-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="114ce-285">Vyskladnění seskupení</span><span class="sxs-lookup"><span data-stu-id="114ce-285">Put the cluster away</span></span>

1. <span data-ttu-id="114ce-286">Přihlaste se do mobilní aplikace Řízení skladu jako uživatel, který je nastaven pro sklad *61*.</span><span class="sxs-lookup"><span data-stu-id="114ce-286">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="114ce-287">V hlavní nabídce vyberte **Příchozí**.</span><span class="sxs-lookup"><span data-stu-id="114ce-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="114ce-288">V nabídce **Příchozí** zvolte **Vyskladnění seskupení**.</span><span class="sxs-lookup"><span data-stu-id="114ce-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="114ce-289">Vyberte **ID seskupení** a zadejte ID seskupení, které jste dříve zadali pro uzavřené seskupení.</span><span class="sxs-lookup"><span data-stu-id="114ce-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="114ce-290">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="114ce-290">Select **OK**.</span></span>

    <span data-ttu-id="114ce-291">Zobrazí se stránka **Vyskladnění seskupení: Výdej**</span><span class="sxs-lookup"><span data-stu-id="114ce-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="114ce-292">Zobrazuje ID seskupení, místo výdeje, položky (zobrazí se hodnota *Násobek*) a celkové množství v seskupení, které je třeba vydat.</span><span class="sxs-lookup"><span data-stu-id="114ce-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="114ce-293">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="114ce-293">Select **OK**.</span></span>

    <span data-ttu-id="114ce-294">Zobrazí se stránka **Vyskladnění seskupení: Vložení**</span><span class="sxs-lookup"><span data-stu-id="114ce-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="114ce-295">Pokyny **Vložení** identifikují ID seskupení, místo vložení, položky, celkové množství a ID registrační značky pro položky, které byly přijaty v seskupení.</span><span class="sxs-lookup"><span data-stu-id="114ce-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="114ce-296">Máte standardní možnosti, jak tento krok přepsat nebo předat.</span><span class="sxs-lookup"><span data-stu-id="114ce-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="114ce-297">![Vyskladnění seskupení: Stránka vložení](media/Cluster_putaway-Put.png "Vyskladnění seskupení: Stránka vložení")</span><span class="sxs-lookup"><span data-stu-id="114ce-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="114ce-298">Zvolte **OK** a potvrďte vyskladnění seskupení.</span><span class="sxs-lookup"><span data-stu-id="114ce-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="114ce-299">Zobrazí se zpráva „Seskupení dokončeno“.</span><span class="sxs-lookup"><span data-stu-id="114ce-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="114ce-300">Poznámky a tipy</span><span class="sxs-lookup"><span data-stu-id="114ce-300">Notes and tips</span></span>

<span data-ttu-id="114ce-301">V případech, kdy se ID seskupení stane nadřazenou registrační značkou pro vnořenou paletu, je při skenování ID seskupení pozice vložení automaticky dána.</span><span class="sxs-lookup"><span data-stu-id="114ce-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="114ce-302">Žádná další registrační značka nesmí být skenována, i když je generování poznávací značky nastaveno na ruční.</span><span class="sxs-lookup"><span data-stu-id="114ce-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]