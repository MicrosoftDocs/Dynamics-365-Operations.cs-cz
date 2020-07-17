---
title: Řazení práce řízené systémem
description: Toto téma uvádí informace o řazení práce řízeném systémem. Tato funkce umožňuje třídit a filtrovat pracovní příkazy, které systém předává uživatelům k provádění. Hodí se v situacích, kdy se k řízení procesu vydávání ze skladu využívají další kritéria.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 2884c480d20090266f7cffb5e7d0aca58c1174f0
ms.sourcegitcommit: edb46dce498df42b09e8f5ad6de00f86c8022dfa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534843"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="72fcc-105">Řazení práce řízené systémem</span><span class="sxs-lookup"><span data-stu-id="72fcc-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72fcc-106">Řazení práce řízené systémem umožňuje třídit a filtrovat pracovní příkazy, které systém předává uživatelům k provádění.</span><span class="sxs-lookup"><span data-stu-id="72fcc-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="72fcc-107">Funkce je užitečná v situacích kdy se k řízení procesu výdeje ze skladu vyžadují další kritéria (např. čas dodávky, zóna výdeje, profil skladového místa nebo kombinace různých kritérií).</span><span class="sxs-lookup"><span data-stu-id="72fcc-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="72fcc-108">Tato funkce rozšiřuje současnou funkci výdeje řízeného systémem přidáním systémem řízeného pořadí dotazů, kde mohou uživatelé nastavovat pořadí a jeden nebo více dotazů, jež všechny vytvořené pracovní příkazy vyhodnocují.</span><span class="sxs-lookup"><span data-stu-id="72fcc-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="72fcc-109">Pouze pracovní příkazy, jež splňují kritéria stanovená v nastavení položky nabídky mobilního zařízení, budou zachyceny a prezentovány.</span><span class="sxs-lookup"><span data-stu-id="72fcc-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="72fcc-110">Tato funkce proto umožňuje další optimalizaci procesů výdeje ze skladu. Identifikuje pracovní příkazy, které odpovídají zadaným kritériím, přiřadí je ke správné položce nabídky mobilního zařízení a poté je předloží pracovníkovi na základě konkrétní sady dovedností, zařízení pro výdej nebo jiného požadavku.</span><span class="sxs-lookup"><span data-stu-id="72fcc-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="72fcc-111">Pokud jsou nutná jiná kritéria, je třeba použít více položek nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="72fcc-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="72fcc-112">Zapnutí funkce Řazení práce řízené systémem v rámci celé organizace</span><span class="sxs-lookup"><span data-stu-id="72fcc-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="72fcc-113">Než můžete použít funkci Řazení práce řízené systémem, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="72fcc-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="72fcc-114">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="72fcc-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="72fcc-115">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="72fcc-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="72fcc-116">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="72fcc-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="72fcc-117">**Název funkce:** *Řazení práce řízené systémem v rámci celé organizace*</span><span class="sxs-lookup"><span data-stu-id="72fcc-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="72fcc-118">Nastavení</span><span class="sxs-lookup"><span data-stu-id="72fcc-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="72fcc-119">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="72fcc-119">Make demo data available</span></span>

<span data-ttu-id="72fcc-120">Chcete-li s tímto scénářem pracovat pomocí hodnot prezentovaných v tomto tématu, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data.</span><span class="sxs-lookup"><span data-stu-id="72fcc-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="72fcc-121">Dále musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="72fcc-122">Scénář používá sklad *51* z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="72fcc-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72fcc-123">Před vydáním objednávek do skladu zajistěte, aby skladová místa pro vyskladnění měla dostatečné množství zásob pro všechny položky objednávek.</span><span class="sxs-lookup"><span data-stu-id="72fcc-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="72fcc-124">Výchozí data USMF by měla tento scénář podporovat.</span><span class="sxs-lookup"><span data-stu-id="72fcc-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="72fcc-125">Pokud nepoužíváte ukázková data, zkontrolujte nastavení **Směrnice skladového místa** a zjistěte tak, která výdejní skladová místa se použijí pro výdej prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="72fcc-126">Pokud musíte upravit zásoby, můžete vytvořit ruční pohyby, použít doplnění nebo využít jakýkoli jiný tok.</span><span class="sxs-lookup"><span data-stu-id="72fcc-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="72fcc-127">Vytvoření nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="72fcc-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="72fcc-128">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="72fcc-129">V seznamu položek nabídky mobilních zařízení vyberte **Prodejní výdej – systém**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="72fcc-130">Požadovaná položka nabídky by již měla existovat.</span><span class="sxs-lookup"><span data-stu-id="72fcc-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="72fcc-131">Potvrďte následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="72fcc-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="72fcc-132">Na záložce s náhledem **Obecné** by měla být v poli **Řídí:** hodnota *Řízeno systémem*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="72fcc-133">Na záložce s náhledem **Třídy práce** by se mělo zobrazit následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="72fcc-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="72fcc-134">ID pracovní třídy</span><span class="sxs-lookup"><span data-stu-id="72fcc-134">Work class ID</span></span> | <span data-ttu-id="72fcc-135">Typ pořadí pracovních činností</span><span class="sxs-lookup"><span data-stu-id="72fcc-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="72fcc-136">Prodej.</span><span class="sxs-lookup"><span data-stu-id="72fcc-136">Sales</span></span> | <span data-ttu-id="72fcc-137">Prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="72fcc-137">Sales orders</span></span> |
        | <span data-ttu-id="72fcc-138">Výdej PO</span><span class="sxs-lookup"><span data-stu-id="72fcc-138">SO Pick</span></span> | <span data-ttu-id="72fcc-139">Prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="72fcc-139">Sales orders</span></span> |

1. <span data-ttu-id="72fcc-140">V podokně Akce vyberte možnost **Dotazy na řazení práce řízené systémem**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="72fcc-141">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-141">Select **Edit**.</span></span>
1. <span data-ttu-id="72fcc-142">Smaže stávající řádek a akci potvrďte výběrem možnosti **Ano**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="72fcc-143">V podokně Akce vyberte možnost **Nový** a vytvořte řádek.</span><span class="sxs-lookup"><span data-stu-id="72fcc-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="72fcc-144">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="72fcc-145">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="72fcc-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="72fcc-146">**Pole Popis:** *Množství práce menší než 20, sestupně*</span><span class="sxs-lookup"><span data-stu-id="72fcc-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="72fcc-147">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-147">Select **Save**.</span></span>
1. <span data-ttu-id="72fcc-148">V podokně Akce vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="72fcc-149">Na kartě **Spojení** rozbalte hierarchii spojení a zobrazte tabulku **Řádky práce**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="72fcc-150">Vyberte spojení tabulky **Řádky práce**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="72fcc-151">Zvolte **Přidat propojení tabulek**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="72fcc-152">Zobrazí se seznam, v něm vyhledejte a vyberte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="72fcc-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="72fcc-153">**Režim spojení:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="72fcc-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="72fcc-154">**Vztah:** *Skladová místa (skladové místo)*</span><span class="sxs-lookup"><span data-stu-id="72fcc-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="72fcc-155">Zvolte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-155">Select **Select**.</span></span>

    <span data-ttu-id="72fcc-156">Skladová místa se přidávají do spojení tabulky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="72fcc-157">Na kartě **Třídění** vyberte možnost **Přidat** a přidejte řádek.</span><span class="sxs-lookup"><span data-stu-id="72fcc-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="72fcc-158">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="72fcc-159">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="72fcc-160">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="72fcc-161">**Pole:** *Množství práce* (V poli zprávy, které e zobrazí, klikněte na **Ano** a třídění se přidá do tohoto pole.)</span><span class="sxs-lookup"><span data-stu-id="72fcc-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="72fcc-162">**Směr hledání:** *Sestupně*</span><span class="sxs-lookup"><span data-stu-id="72fcc-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="72fcc-163">Vyberte kartu **Oblast**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="72fcc-164">Pokud by do řazení měla být zahrnuta pouze určitá pracovní kritéria, můžete je zadat na kartě **Oblast**. V tomto příkladu chcete zahrnout pouze práci, kde je množství menší než 20 ks (nejnižší měrná jednotka).</span><span class="sxs-lookup"><span data-stu-id="72fcc-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="72fcc-165">Všimněte si, že některé řádky jsou již zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="72fcc-165">Notice that some lines are already included.</span></span> <span data-ttu-id="72fcc-166">Tyto řádky neodstraňujte.</span><span class="sxs-lookup"><span data-stu-id="72fcc-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="72fcc-167">Chcete-li přidat řádek, vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="72fcc-168">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="72fcc-169">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="72fcc-170">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="72fcc-171">**Pole:** *Zásoby – množství práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="72fcc-172">**Kritéria:** *\<20* (méně než 20)</span><span class="sxs-lookup"><span data-stu-id="72fcc-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="72fcc-173">Chcete-li přidat další řádek, vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="72fcc-174">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="72fcc-175">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="72fcc-176">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="72fcc-177">**Pole:** *Typ práce*</span><span class="sxs-lookup"><span data-stu-id="72fcc-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="72fcc-178">**Kritéria:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="72fcc-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="72fcc-179">Chcete-li přidat další řádek, vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="72fcc-180">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="72fcc-181">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="72fcc-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="72fcc-182">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="72fcc-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="72fcc-183">**Pole:** *ID profilu skladového místa*</span><span class="sxs-lookup"><span data-stu-id="72fcc-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="72fcc-184">**Kritéria:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="72fcc-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="72fcc-185">Nezapomeňte zahrnout na vykřičník (*!*) před *STAGE*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="72fcc-186">Klikněte **OK**. Dotaz se uloží a zavře.</span><span class="sxs-lookup"><span data-stu-id="72fcc-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="72fcc-187">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-187">Select **Save**.</span></span>
1. <span data-ttu-id="72fcc-188">Zavřete stránku a vraťte se na stránku **Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="72fcc-189">Toto nastavení definuje kritéria, která se použijí k vložení způsobilé práce do položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="72fcc-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="72fcc-190">Pokud do dotazu přidáte další řádky kritérií, systém použije jako první ten řádek dotazu, který má nejnižší pořadové číslo.</span><span class="sxs-lookup"><span data-stu-id="72fcc-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="72fcc-191">Jinými slovy, veškerá způsobilá práce s pořadovým číslem 1 bude uživateli prezentována jako první, následovat bude veškerá práce s pořadovým číslem 2.</span><span class="sxs-lookup"><span data-stu-id="72fcc-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="72fcc-192">Pokud je tedy třeba používat společně konkrétní oblast a třídění, je třeba je zadat v témže dotazu na řazení práce řízené systémem.</span><span class="sxs-lookup"><span data-stu-id="72fcc-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="72fcc-193">Toto nastavení zachytí jakoukoli práci, která má alespoň jeden řádek, kde je množství menší než 20 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="72fcc-194">Pokud tedy práce obsahuje řádek, kde je množství přesně 20 ks nebo více než 20 ks, bude platit pokud současně obsahuje také alespoň jeden řádek, kde je množství menší než 20 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="72fcc-195">Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="72fcc-195">Location directives</span></span>

<span data-ttu-id="72fcc-196">Pokud používáte výchozí data Contoso, nebude dotaz na akci směrnice skladového místa vyžadovat žádné změny.</span><span class="sxs-lookup"><span data-stu-id="72fcc-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="72fcc-197">Chcete-li však mít jistotu, že směrnice skladového místa zachytí položky na prodejních objednávkách, když tuto funkci použijete v prostředí mimo Contoso, vytvořte novou směrnici skladového místa.</span><span class="sxs-lookup"><span data-stu-id="72fcc-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="72fcc-198">Chcete-li ověřit nastavení v ukázkovém prostředí, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="72fcc-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="72fcc-199">Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="72fcc-200">V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="72fcc-201">Vyberte směrnici skladového místa s označením *51 Výdej*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="72fcc-202">Na záložce s náhledem **Akce směrnice skladového místa** vyberte řádek pro akci **Výdej**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="72fcc-203">Vyberte možnost **Upravit dotaz** nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="72fcc-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="72fcc-204">Zkontrolujte dotaz **Oblast**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="72fcc-205">Najděte řádek, kde má pole **Pole** nastavenou hodnotu *Skladové místo*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="72fcc-206">Ujistěte se, že je pole **Kritéria** prázdné (tj. neexistují žádná omezení).</span><span class="sxs-lookup"><span data-stu-id="72fcc-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="72fcc-207">Scénář</span><span class="sxs-lookup"><span data-stu-id="72fcc-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="72fcc-208">Vytvoření práce výdeje prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="72fcc-208">Create sales order picking work</span></span>

<span data-ttu-id="72fcc-209">Před spuštěním výdeje řízeného systémem je třeba vytvořit výstupní práci.</span><span class="sxs-lookup"><span data-stu-id="72fcc-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="72fcc-210">Pro tento scénář vytvořte čtyři prodejní objednávky, které vycházejí ze zadaných dotazů na řazení práce řízené systémem.</span><span class="sxs-lookup"><span data-stu-id="72fcc-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="72fcc-211">Rezervujte si množství zásob pro každou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="72fcc-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="72fcc-212">Rezervované zásoby nemohou tedy být ze skladu odebrány na jiné objednávky, dokud se nezruší rezervace zásob nebo její část.</span><span class="sxs-lookup"><span data-stu-id="72fcc-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="72fcc-213">Poté uvolníte každou prodejní objednávku do skladu a vytvoříte výstupní práci.</span><span class="sxs-lookup"><span data-stu-id="72fcc-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="72fcc-214">Prodejní objednávka 1</span><span class="sxs-lookup"><span data-stu-id="72fcc-214">Sales order 1</span></span>

1. <span data-ttu-id="72fcc-215">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="72fcc-216">V podokně Akce vyberte možnost **Nová** a vytvořte prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="72fcc-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="72fcc-217">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="72fcc-218">V sekci **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-004*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="72fcc-219">V sekci **Všeobecné** zadejte do pole **Sklad** hodnotu *51*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="72fcc-220">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="72fcc-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="72fcc-221">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="72fcc-222">Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-223">**Číslo položky:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="72fcc-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="72fcc-224">**Množství:** *20*</span><span class="sxs-lookup"><span data-stu-id="72fcc-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="72fcc-225">V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="72fcc-226">Na stránce **Rezervace** vyberte **Rezervovat šarži** k rezervování zásob.</span><span class="sxs-lookup"><span data-stu-id="72fcc-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="72fcc-227">Zavřete stránku **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="72fcc-228">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**. Vytvoří se práce pro sklad.</span><span class="sxs-lookup"><span data-stu-id="72fcc-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="72fcc-229">Zobrazí se informační zprávy určující ID vlny a ID dodávky, jež byly vytvořeny pro tuto prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="72fcc-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="72fcc-230">Prodejní objednávka 2</span><span class="sxs-lookup"><span data-stu-id="72fcc-230">Sales order 2</span></span>

1. <span data-ttu-id="72fcc-231">V podokně Akce vyberte možnost **Nová** a vytvořte prodení objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="72fcc-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="72fcc-232">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="72fcc-233">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="72fcc-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="72fcc-234">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="72fcc-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="72fcc-235">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="72fcc-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="72fcc-236">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="72fcc-237">Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-238">**Číslo položky:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="72fcc-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="72fcc-239">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="72fcc-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="72fcc-240">Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-241">**Číslo položky:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="72fcc-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="72fcc-242">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="72fcc-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="72fcc-243">Proveďte rezervaci zásob pro oba řádky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="72fcc-244">Uvolněte objednávku do skladu.</span><span class="sxs-lookup"><span data-stu-id="72fcc-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="72fcc-245">Prodejní objednávka 3</span><span class="sxs-lookup"><span data-stu-id="72fcc-245">Sales order 3</span></span>

1. <span data-ttu-id="72fcc-246">V podokně Akce vyberte možnost **Nová** a vytvořte prodení objednávku 3.</span><span class="sxs-lookup"><span data-stu-id="72fcc-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="72fcc-247">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="72fcc-248">**Účet zákazníka:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="72fcc-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="72fcc-249">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="72fcc-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="72fcc-250">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="72fcc-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="72fcc-251">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="72fcc-252">Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-253">**Číslo položky:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="72fcc-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="72fcc-254">**Množství:** *7*</span><span class="sxs-lookup"><span data-stu-id="72fcc-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="72fcc-255">Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-256">**Číslo položky:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="72fcc-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="72fcc-257">**Množství:** *8*</span><span class="sxs-lookup"><span data-stu-id="72fcc-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="72fcc-258">Proveďte rezervaci zásob pro oba řádky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="72fcc-259">Uvolněte objednávku do skladu.</span><span class="sxs-lookup"><span data-stu-id="72fcc-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="72fcc-260">Prodejní objednávka 4</span><span class="sxs-lookup"><span data-stu-id="72fcc-260">Sales order 4</span></span>

1. <span data-ttu-id="72fcc-261">V podokně Akce vyberte možnost **Nová** a vytvořte prodení objednávku 4.</span><span class="sxs-lookup"><span data-stu-id="72fcc-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="72fcc-262">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="72fcc-263">**Účet zákazníka:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="72fcc-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="72fcc-264">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="72fcc-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="72fcc-265">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="72fcc-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="72fcc-266">Poznamenejte si číslo prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="72fcc-267">Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-268">**Číslo položky:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="72fcc-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="72fcc-269">**Množství:** *25*</span><span class="sxs-lookup"><span data-stu-id="72fcc-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="72fcc-270">Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="72fcc-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="72fcc-271">**Číslo položky:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="72fcc-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="72fcc-272">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="72fcc-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="72fcc-273">Proveďte rezervaci zásob pro oba řádky.</span><span class="sxs-lookup"><span data-stu-id="72fcc-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="72fcc-274">Uvolněte objednávku do skladu.</span><span class="sxs-lookup"><span data-stu-id="72fcc-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="72fcc-275">Získání ID práce pro vytvořenou práci</span><span class="sxs-lookup"><span data-stu-id="72fcc-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="72fcc-276">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="72fcc-277">Filtrujte pole **Sklad** tak, aby se zobrazila pouze práce pro sklad *51*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="72fcc-278">Měla by se vytvořit čtyři ID práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-278">Four work IDs should have been created.</span></span> <span data-ttu-id="72fcc-279">Pro každou prodejní objednávku si poznamenejte ID práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="72fcc-280">ID prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="72fcc-280">Sales order ID</span></span> | <span data-ttu-id="72fcc-281">ID práce</span><span class="sxs-lookup"><span data-stu-id="72fcc-281">Work ID</span></span> | <span data-ttu-id="72fcc-282">Množství práce</span><span class="sxs-lookup"><span data-stu-id="72fcc-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="72fcc-283">Prodejní objednávka 1</span><span class="sxs-lookup"><span data-stu-id="72fcc-283">Sales Order 1</span></span> | <span data-ttu-id="72fcc-284">ID práce 1</span><span class="sxs-lookup"><span data-stu-id="72fcc-284">Work ID 1</span></span> | <span data-ttu-id="72fcc-285">20 ks</span><span class="sxs-lookup"><span data-stu-id="72fcc-285">20 ea</span></span> |
    | <span data-ttu-id="72fcc-286">Prodejní objednávka 2</span><span class="sxs-lookup"><span data-stu-id="72fcc-286">Sales Order 2</span></span> | <span data-ttu-id="72fcc-287">ID práce 2</span><span class="sxs-lookup"><span data-stu-id="72fcc-287">Work ID 2</span></span> | <span data-ttu-id="72fcc-288">6 ks (součet obou řádků)</span><span class="sxs-lookup"><span data-stu-id="72fcc-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="72fcc-289">Prodejní objednávka 3</span><span class="sxs-lookup"><span data-stu-id="72fcc-289">Sales Order 3</span></span> | <span data-ttu-id="72fcc-290">ID práce 3</span><span class="sxs-lookup"><span data-stu-id="72fcc-290">Work ID 3</span></span> | <span data-ttu-id="72fcc-291">15 ks (součet obou řádků)</span><span class="sxs-lookup"><span data-stu-id="72fcc-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="72fcc-292">Prodejní objednávka 4</span><span class="sxs-lookup"><span data-stu-id="72fcc-292">Sales Order 4</span></span> | <span data-ttu-id="72fcc-293">ID práce 4</span><span class="sxs-lookup"><span data-stu-id="72fcc-293">Work ID 4</span></span> | <span data-ttu-id="72fcc-294">35 ks (součet obou řádků)</span><span class="sxs-lookup"><span data-stu-id="72fcc-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="72fcc-295">Před spuštěním toku na mobilním zařízení se ujistěte, že pro sklad *51* je pouze práce, kterou jste právě vytvořili, ve stavu *Otevřená* a že typ pracovního příkazu je *Prodejní objednávka*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="72fcc-296">V opačném případě se výsledky testu mohou lišit, protože výdej řízený systémem bude zahrnovat veškerou způsobilou práci.</span><span class="sxs-lookup"><span data-stu-id="72fcc-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="72fcc-297">Přejděte do **Řízení skladu \> Práce \> Výstupní \> Otevřená prodejní práce**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="72fcc-298">V mřížce **Otevřená prodejní práce** filtrujte pole **Sklad** tak, aby se zobrazila pouze práce pro sklad *51*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="72fcc-299">Ověřte, že jsou zobrazeny pouze čtyři ID práce, jež jste předtím vytvořili.</span><span class="sxs-lookup"><span data-stu-id="72fcc-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="72fcc-300">Zavřete stránku **Práce**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="72fcc-301">Realizace toku na mobilním zařízení</span><span class="sxs-lookup"><span data-stu-id="72fcc-301">Mobile device flow execution</span></span>

<span data-ttu-id="72fcc-302">Na základě nastavení bude systém dodávat uživatelskou práci, jež bude tříděna od nejvyššího množství na řádku práce po nejnižší.</span><span class="sxs-lookup"><span data-stu-id="72fcc-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="72fcc-303">Množství na každém řádku musí být menší než 20 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="72fcc-304">Pamatujte, že toto nastavení zachytí jakoukoli práci, která má alespoň jeden řádek, kde je množství menší než 20 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="72fcc-305">Pokud tedy práce obsahuje další řádek, kde je množství přesně 20 ks nebo více než 20 ks, bude platit také.</span><span class="sxs-lookup"><span data-stu-id="72fcc-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="72fcc-306">Aplikace pro mobilní zařízení</span><span class="sxs-lookup"><span data-stu-id="72fcc-306">Mobile app</span></span>

1. <span data-ttu-id="72fcc-307">Přihlaste se do skladové aplikace jako uživatel skladu *51*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="72fcc-308">Přejděte do **Výstupní \> Prodejní výdej – systém**.</span><span class="sxs-lookup"><span data-stu-id="72fcc-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="72fcc-309">Je prezentován krok výdeje pro ID práce *4*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="72fcc-310">Toto ID práce je uvedeno jako první kvůli pořadí dotazů řízenému systémem, kde jste určili, že by pro práce mělo být určováno pořadí na základě sestupného množství na řádku práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="72fcc-311">Proveďte požadovaný výdej a zaskladnění a zavřete ID práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="72fcc-312">Dále je prezentováno ID práce *3*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="72fcc-313">Jeden z řádku práce je další v pořadí na základě množství na řádku práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="72fcc-314">Proveďte výdej a zaskladnění a zavřete ID práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="72fcc-315">Dále je prezentováno ID práce *2*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="72fcc-316">Tento řádek práce výdeje je další v pořadí.</span><span class="sxs-lookup"><span data-stu-id="72fcc-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="72fcc-317">Proveďte výdej a zaskladnění a zavřete ID práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="72fcc-318">Žádná další práce by se objevit neměla.</span><span class="sxs-lookup"><span data-stu-id="72fcc-318">No further work should be presented to you.</span></span> <span data-ttu-id="72fcc-319">ID práce *1* není způsobilé pro tuto položku nabídky mobilního zařízení, protože dotaz určuje, že záhlaví práce jsou brána v úvahu pouze v případě, že množství na řádcích práce je menší než 20 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="72fcc-320">Tipy</span><span class="sxs-lookup"><span data-stu-id="72fcc-320">Tips</span></span>

<span data-ttu-id="72fcc-321">Dotazy na řazení práce řízené systémem jsou *inkluzivní*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="72fcc-322">Na tuto skutečnost při nastavování nezapomínejte.</span><span class="sxs-lookup"><span data-stu-id="72fcc-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="72fcc-323">Například chcete, aby konkrétní položka nabídky zpracovávala pouze práci, kde je jako jednotka práce *ks* a zadáte toto omezení na kartě **Oblast** dotazu.</span><span class="sxs-lookup"><span data-stu-id="72fcc-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="72fcc-324">V tom případě všechny práce, kde má alespoň jeden řádek práce nastavenou jednotku *ks*, budou předloženy pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="72fcc-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="72fcc-325">Tato práce proto může zahrnovat také práci, kde mají řádky práce jinou jednotku než *ks* (např. *krabice* nebo *paleta*).</span><span class="sxs-lookup"><span data-stu-id="72fcc-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="72fcc-326">Dotaz vyloučí pouze práci, kde nemá žádný řádek práce nastavenou jednotku práce *ks*.</span><span class="sxs-lookup"><span data-stu-id="72fcc-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="72fcc-327">Proto bylo v příkladu v tomto scénáři ID práce *4* také zachyceno dotazem.</span><span class="sxs-lookup"><span data-stu-id="72fcc-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="72fcc-328">Při vytvoření byly přidány dva řádky: jeden pro 25 ks druhý pro 10 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="72fcc-329">Práce je prezentována uživateli, protože alespoň jeden řádek práce má množství menší než 20 ks.</span><span class="sxs-lookup"><span data-stu-id="72fcc-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="72fcc-330">V závislosti na scénáři můžete tomuto chování bránit s využitím dělení práce.</span><span class="sxs-lookup"><span data-stu-id="72fcc-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
