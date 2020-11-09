---
title: Umístění registrační značky místa
description: Určení pozice registrační značky na skladovém místě umožňuje zjistit, kde se registrační značka nachází na skladovém místě pro více palet, například na skladovém místě využívajícím regály o hloubce na dvě palety.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017109"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="67c23-103">Umístění registrační značky místa</span><span class="sxs-lookup"><span data-stu-id="67c23-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67c23-104">Určení pozice registrační značky na skladovém místě umožňuje zjistit, kde se registrační značka nachází na skladovém místě pro více palet, například na skladovém místě využívajícím regály o hloubce na dvě palety.</span><span class="sxs-lookup"><span data-stu-id="67c23-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="67c23-105">Tato funkce přidá pořadové číslo ke každé registrační značce vložené na skladové místo.</span><span class="sxs-lookup"><span data-stu-id="67c23-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="67c23-106">Toto pořadové číslo se používá k řazení registračních značek na skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="67c23-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="67c23-107">Tato funkce proto inteligentně podporuje scénáře, kdy odběratelé používají gravitační regálový systém, a proto musí pro účely výdeje vědět, která registrační značka směřuje vpřed.</span><span class="sxs-lookup"><span data-stu-id="67c23-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="67c23-108">Toto téma představuje scénář, který ukazuje, jak tuto funkci nastavit a používat.</span><span class="sxs-lookup"><span data-stu-id="67c23-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="67c23-109">Zapnutí funkce Určení pozice registrační značky na skladovém místě</span><span class="sxs-lookup"><span data-stu-id="67c23-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="67c23-110">Než můžete použít funkci Určení pozice registrační značky na skladovém místě, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="67c23-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="67c23-111">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="67c23-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="67c23-112">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="67c23-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="67c23-113">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="67c23-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="67c23-114">**Název funkce:** *Určení pozice registrační značky na skladovém místě*</span><span class="sxs-lookup"><span data-stu-id="67c23-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="67c23-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="67c23-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="67c23-116">Příprava ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="67c23-116">Make sample data available</span></span>

<span data-ttu-id="67c23-117">Chcete-li s tímto scénářem pracovat pomocí hodnot navržených v tomto tématu, musíte používat systém, ve kterém jsou nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="67c23-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="67c23-118">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="67c23-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="67c23-119">Nastavení funkce pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="67c23-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="67c23-120">Chcete-li nastavit funkci *Určení pozice registrační značky na skladovém místě* pro scénář, který je uveden v tomto tématu, proveďte následující procedury.</span><span class="sxs-lookup"><span data-stu-id="67c23-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="67c23-121">Profily umístění</span><span class="sxs-lookup"><span data-stu-id="67c23-121">Location profiles</span></span>

<span data-ttu-id="67c23-122">Funkci je nutné zapnout v profilu skladového místa pro každé skladové místo, kde má být použita.</span><span class="sxs-lookup"><span data-stu-id="67c23-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="67c23-123">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="67c23-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="67c23-124">V seznamu profilů skladových míst v levém podokně vyberte možnost **HROMADNÝ-06**.</span><span class="sxs-lookup"><span data-stu-id="67c23-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="67c23-125">Na záložce s náhledem **Všeobecné** byly k funkci přidány dvě nové možnosti.</span><span class="sxs-lookup"><span data-stu-id="67c23-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="67c23-126">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-126">Set the following values:</span></span>

    - <span data-ttu-id="67c23-127">**Povolit určení polohy registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="67c23-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="67c23-128">Když je u této možnosti vybrána hodnota *Ano* , pozice registrační značky bude zachována pro registrační značky na daném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="67c23-128">When this option is set to *Yes* , the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="67c23-129">**Zobrazit pozici LP mobilního zařízení:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="67c23-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="67c23-130">Pokud je u této možnost vybrána hodnota *Ano* , bude se uživatelům mobilních zařízení během úprav a inventur pozice registrační značky zobrazovat.</span><span class="sxs-lookup"><span data-stu-id="67c23-130">When this option is set to *Yes* , the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="67c23-131">Nastavení této možnosti můžete změnit, pouze když je funkce zapnutá.</span><span class="sxs-lookup"><span data-stu-id="67c23-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="67c23-132">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="67c23-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="67c23-133">Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="67c23-133">Location directives</span></span>

1. <span data-ttu-id="67c23-134">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="67c23-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="67c23-135">V levém podokně zkontrolujte, zda je v poli **Typ pracovního příkazu** nastavena hodnota *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="67c23-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="67c23-136">V seznamu směrnic skladového místa vyberte možnost **61 SO výdejová objednávka**.</span><span class="sxs-lookup"><span data-stu-id="67c23-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="67c23-137">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="67c23-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="67c23-138">Na záložce s náhledem **Řádky** vyberte řádek, který má v poli **Pořadové číslo** hodnotu *2*.</span><span class="sxs-lookup"><span data-stu-id="67c23-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="67c23-139">Na záložce s náhledem **Akce směrnice skladového místa** vyberte řádek, který má hodnotu **Název** u možnosti *Výdej méně než palety* (mělo by se jednat o jediný takový řádek) a změnit u něj hodnotu v poli **Pořadové číslo** na *2*.</span><span class="sxs-lookup"><span data-stu-id="67c23-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="67c23-140">Klikněte nad mřížkou na **Nový** , přidá se řádek pro novou akci směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="67c23-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="67c23-141">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="67c23-142">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="67c23-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="67c23-143">**Název:** *Výdejová pozice 1*</span><span class="sxs-lookup"><span data-stu-id="67c23-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="67c23-144">Dokud je ještě nový řádek vybrán, klikněte na **Upravit dotaz** nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="67c23-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="67c23-145">V editoru dotazů klikněte na kartu **Spojení**.</span><span class="sxs-lookup"><span data-stu-id="67c23-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="67c23-146">Rozbalte spojení tabulky **Skladová místa** , zobrazí se spojení tabulky **Dimenze zásob**.</span><span class="sxs-lookup"><span data-stu-id="67c23-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="67c23-147">Rozbalte spojení tabulky **Dimenze zásob** , zobrazí se spojení tabulky **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="67c23-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="67c23-148">Vyberte **Dimenze zásob** a poté možnost **Přidat spojení tabulek**.</span><span class="sxs-lookup"><span data-stu-id="67c23-148">Select **Inventory dimensions** , and then select **Add table join**.</span></span>
1. <span data-ttu-id="67c23-149">V zobrazeném seznamu tabulek vyberte ve sloupci **Vztah** hodnotu **Registrační značka (registrační značka)**.</span><span class="sxs-lookup"><span data-stu-id="67c23-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="67c23-150">Poté vyberte možnost **Vybrat** a přidejte **Registrační značku** do spojení tabulek **Dimenze zásob**.</span><span class="sxs-lookup"><span data-stu-id="67c23-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="67c23-151">Dokud ještě máte vybranou **Registrační značku** , vyberte možnost **Přidat spojení tabulek**.</span><span class="sxs-lookup"><span data-stu-id="67c23-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="67c23-152">V zobrazeném seznamu tabulek vyberte ve sloupci **Vztah** hodnotu **Určení pozice registrační značky (registrační značka)**.</span><span class="sxs-lookup"><span data-stu-id="67c23-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="67c23-153">Poté vyberte možnost **Vybrat** a přidejte **Určení pozice registrační značky** do spojení tabulek **Dimenze zásob**.</span><span class="sxs-lookup"><span data-stu-id="67c23-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="67c23-154">![Spojení tabulek](media/LpTableJoin.png "Spojení tabulek")</span><span class="sxs-lookup"><span data-stu-id="67c23-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="67c23-155">Potvrďte aktualizované spojené tabulky kliknutím na **OK** a zavřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="67c23-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="67c23-156">Na pevné záložce **Akce směrnice skladového místa** znovu vyberte **Upravit dotaz** a znovu otevřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="67c23-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="67c23-157">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="67c23-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="67c23-158">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="67c23-159">**Tabulka:** *Určení pozice registrační značky na skladovém místě*</span><span class="sxs-lookup"><span data-stu-id="67c23-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="67c23-160">**Odvozená tabulka:** *Určení pozice registrační značky na skladovém místě*</span><span class="sxs-lookup"><span data-stu-id="67c23-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="67c23-161">**Pole:** *Pozice LP*</span><span class="sxs-lookup"><span data-stu-id="67c23-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="67c23-162">**Kritéria:** *1*</span><span class="sxs-lookup"><span data-stu-id="67c23-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="67c23-163">![Nová oblast](media/LpPositionCriteria.png "Nová oblast")</span><span class="sxs-lookup"><span data-stu-id="67c23-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="67c23-164">Výběrem **OK** potvrďte změny a zavřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="67c23-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="67c23-165">Nastavení ukázkových dat pro tento scénář</span><span class="sxs-lookup"><span data-stu-id="67c23-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="67c23-166">Pro tento scénář se musí uživatel přihlásit ke skladové mobilní aplikaci jako pracovník, který je oprávněn podle nastavení provádět práci ve skladu *61*.</span><span class="sxs-lookup"><span data-stu-id="67c23-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="67c23-167">Uživatel musí také dokončit transakce.</span><span class="sxs-lookup"><span data-stu-id="67c23-167">The user must also complete transactions.</span></span>

<span data-ttu-id="67c23-168">Protože funkce *Určení pozice registrační značky na skladovém místě* přidá nový identifikátor pro pozice registrační značky na skladovém místě, musíte nejprve vytvořit některá data, jež tento scénář podporují.</span><span class="sxs-lookup"><span data-stu-id="67c23-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="67c23-169">Inventura prvního skladového místa</span><span class="sxs-lookup"><span data-stu-id="67c23-169">Spot-count the first location</span></span>

1. <span data-ttu-id="67c23-170">Otevřete skladovou mobilní aplikaci a přihlaste se do skladu *61*.</span><span class="sxs-lookup"><span data-stu-id="67c23-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="67c23-171">Přejděte na **Zásoby \> Inventura**.</span><span class="sxs-lookup"><span data-stu-id="67c23-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="67c23-172">Na stránce **Inventura** nastavte v poli **Skladové místo** hodnotu *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="67c23-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="67c23-173">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-173">Select **OK**.</span></span>

    <span data-ttu-id="67c23-174">Na stránce se zobrazuje zadané skladové místo.</span><span class="sxs-lookup"><span data-stu-id="67c23-174">The page shows the location that you entered.</span></span> <span data-ttu-id="67c23-175">Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“</span><span class="sxs-lookup"><span data-stu-id="67c23-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="67c23-176">Vyberte **Obnovit** , chcete-li přidat pro dané skladové místo množství.</span><span class="sxs-lookup"><span data-stu-id="67c23-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="67c23-177">Na stránce **Cyklická inventura: přidání nové LP nebo položky** vyberte pole **Položka** a zadejte hodnotu *A0001*.</span><span class="sxs-lookup"><span data-stu-id="67c23-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="67c23-178">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-178">Select **OK**.</span></span>
1. <span data-ttu-id="67c23-179">Na stránce **Cyklická inventura: Přidání nové LP nebo položky** zadejte do pole **LP** hodnotu *LP1001* (nebo jakékoli jiné číslo registrační značky podle vaší volby).</span><span class="sxs-lookup"><span data-stu-id="67c23-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="67c23-180">Na stránce **Cyklická inventura: Přidání nové LP nebo položky** se zobrazí **Pozice registrační značky 1**.</span><span class="sxs-lookup"><span data-stu-id="67c23-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="67c23-181">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-181">Select **OK**.</span></span>

    <span data-ttu-id="67c23-182">Nyní musíte určit množství položek, jež se pro registrační značku počítá.</span><span class="sxs-lookup"><span data-stu-id="67c23-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="67c23-183">Nastavte v poli **Množ.** hodnotu *10*.</span><span class="sxs-lookup"><span data-stu-id="67c23-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="67c23-184">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-184">Select **OK**.</span></span>

    <span data-ttu-id="67c23-185">Na stránce se zobrazuje zadané skladové místo.</span><span class="sxs-lookup"><span data-stu-id="67c23-185">The page shows the location that you entered.</span></span> <span data-ttu-id="67c23-186">Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“</span><span class="sxs-lookup"><span data-stu-id="67c23-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="67c23-187">Vyberte **Obnovit** , chcete-li přidat pro dané skladové další místo množství.</span><span class="sxs-lookup"><span data-stu-id="67c23-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="67c23-188">Na stránce **Cyklická inventura: přidání nové LP nebo položky** vyberte pole **Položka** a zadejte hodnotu *A0002*.</span><span class="sxs-lookup"><span data-stu-id="67c23-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="67c23-189">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-189">Select **OK**.</span></span>
1. <span data-ttu-id="67c23-190">Na stránce **Cyklická inventura: Přidání nové LP nebo položky** vyberte pole **LP** a zadejte hodnotu *LP1002* (nebo jakékoli jiné číslo registrační značky dle vašeho výběru. Podmínkou je, že se číslo musí lišit od čísla registrační značky, které jste zadali dříve).</span><span class="sxs-lookup"><span data-stu-id="67c23-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="67c23-191">Změňte pozici registrační značky zadáním hodnoty **2** do pole *Pozice LP*.</span><span class="sxs-lookup"><span data-stu-id="67c23-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="67c23-192">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-192">Select **OK**.</span></span>
1. <span data-ttu-id="67c23-193">Určete množství položky k počítání na registrační značce nastavením hodnoty **10** v poli *Množ.*</span><span class="sxs-lookup"><span data-stu-id="67c23-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="67c23-194">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-194">Select **OK**.</span></span>

    <span data-ttu-id="67c23-195">Na stránce se zobrazuje zadané skladové místo.</span><span class="sxs-lookup"><span data-stu-id="67c23-195">The page shows the location that you entered.</span></span> <span data-ttu-id="67c23-196">Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“</span><span class="sxs-lookup"><span data-stu-id="67c23-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="67c23-197">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-197">Select **OK**.</span></span>

<span data-ttu-id="67c23-198">Práce je nyní dokončena.</span><span class="sxs-lookup"><span data-stu-id="67c23-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="67c23-199">Inventura druhého skladového místa</span><span class="sxs-lookup"><span data-stu-id="67c23-199">Spot-count the second location</span></span>

1. <span data-ttu-id="67c23-200">Na stránce **Inventura** nastavte v poli **Skladové místo** hodnotu *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="67c23-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="67c23-201">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-201">Select **OK**.</span></span>

    <span data-ttu-id="67c23-202">Na stránce se zobrazuje zadané skladové místo.</span><span class="sxs-lookup"><span data-stu-id="67c23-202">The page shows the location that you entered.</span></span> <span data-ttu-id="67c23-203">Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“</span><span class="sxs-lookup"><span data-stu-id="67c23-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="67c23-204">Vyberte **Obnovit** , chcete-li přidat pro dané skladové místo množství.</span><span class="sxs-lookup"><span data-stu-id="67c23-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="67c23-205">Na stránce **Cyklická inventura: přidání nové LP nebo položky** vyberte pole **Položka** a zadejte hodnotu *A0002*.</span><span class="sxs-lookup"><span data-stu-id="67c23-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="67c23-206">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-206">Select **OK**.</span></span>
1. <span data-ttu-id="67c23-207">Na stránce **Cyklická inventura: Přidání nové LP nebo položky** vyberte pole **LP** a zadejte hodnotu *LP1003* (nebo jakékoli jiné číslo registrační značky dle vašeho výběru. Podmínkou je, že se číslo musí lišit od obou čísel registračních značek z předchozí procedury).</span><span class="sxs-lookup"><span data-stu-id="67c23-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="67c23-208">Na stránce **Cyklická inventura: Přidání nové LP nebo položky** se zobrazí **Pozice registrační značky 1**.</span><span class="sxs-lookup"><span data-stu-id="67c23-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="67c23-209">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-209">Select **OK**.</span></span>
1. <span data-ttu-id="67c23-210">Určete množství položky k počítání na registrační značce nastavením hodnoty **10** v poli *Množ.*</span><span class="sxs-lookup"><span data-stu-id="67c23-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="67c23-211">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-211">Select **OK**.</span></span>

    <span data-ttu-id="67c23-212">Na stránce se zobrazuje zadané skladové místo.</span><span class="sxs-lookup"><span data-stu-id="67c23-212">The page shows the location that you entered.</span></span> <span data-ttu-id="67c23-213">Zobrazuje se zde také následující zpráva: „Skladové místo je dokončeno, přidat novou LP nebo položku?“</span><span class="sxs-lookup"><span data-stu-id="67c23-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="67c23-214">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-214">Select **OK**.</span></span>

<span data-ttu-id="67c23-215">Práce je nyní dokončena.</span><span class="sxs-lookup"><span data-stu-id="67c23-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="67c23-216">Podrobnosti o práci</span><span class="sxs-lookup"><span data-stu-id="67c23-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="67c23-217">Inventury z mobilní aplikace vytvářejí v systému Microsoft Dynamics 365 práci inventury.</span><span class="sxs-lookup"><span data-stu-id="67c23-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="67c23-218">Práce vyžaduje, aby byly počty přijaty před zaúčtováním do zásob.</span><span class="sxs-lookup"><span data-stu-id="67c23-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="67c23-219">Přihlaste se do Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="67c23-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="67c23-220">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="67c23-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="67c23-221">Na kartě **Přehled** vyhledejte řádky, které mají následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="67c23-222">**Typ pracovního příkazu:** *Cyklická inventura*</span><span class="sxs-lookup"><span data-stu-id="67c23-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="67c23-223">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="67c23-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="67c23-224">**Stav práce:** *Čeká na kontrolu*</span><span class="sxs-lookup"><span data-stu-id="67c23-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="67c23-225">Pro tyto řádky by měla být vytvořena dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="67c23-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="67c23-226">Počty k oběma těmto ID práce je nutné přijmout.</span><span class="sxs-lookup"><span data-stu-id="67c23-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="67c23-227">V mřížce vyberte první ID práce pro typ pracovního příkazu *Cyklická inventura*.</span><span class="sxs-lookup"><span data-stu-id="67c23-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="67c23-228">V podokně Akce na kartě **Práce** ve skupině **Práce** vyberte **Cyklická inventura**.</span><span class="sxs-lookup"><span data-stu-id="67c23-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="67c23-229">Zobrazí se dva řádky, jeden pro každou položku a registrační značku.</span><span class="sxs-lookup"><span data-stu-id="67c23-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="67c23-230">Hodnoty v polích **Napočítané množství** , **Skladové místo** , **Registrační značka** a **Položka** by měly odpovídat položkám množství vytvořeným na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="67c23-230">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="67c23-231">Pokud kterékoli z těchto polí nevidíte, vyberte možnost **Zobrazit dimenze** v podokně Akce a přidejte je do mřížky.</span><span class="sxs-lookup"><span data-stu-id="67c23-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="67c23-232">Vyberte oba řádky.</span><span class="sxs-lookup"><span data-stu-id="67c23-232">Select both lines.</span></span>
1. <span data-ttu-id="67c23-233">V podokně Akce klikněte na možnost **Přijmout množství**.</span><span class="sxs-lookup"><span data-stu-id="67c23-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="67c23-234">Zobrazí se zpráva „Zaúčtování – deník“.</span><span class="sxs-lookup"><span data-stu-id="67c23-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="67c23-235">Vybrat **Podrobnosti zprávy** , zobrazí se číslo, pod kterým proběhlo zaúčtování do deníku.</span><span class="sxs-lookup"><span data-stu-id="67c23-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="67c23-236">Zavřete podrobnosti zprávy.</span><span class="sxs-lookup"><span data-stu-id="67c23-236">Close the message details.</span></span>
1. <span data-ttu-id="67c23-237">Obnovte stránku **Práce**.</span><span class="sxs-lookup"><span data-stu-id="67c23-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="67c23-238">První ID práce bylo uzavřeno a již se nezobrazuje.</span><span class="sxs-lookup"><span data-stu-id="67c23-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="67c23-239">Chcete-li zobrazit uzavřenou práci, zaškrtněte políčko **Zobrazovat uzavřené** nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="67c23-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="67c23-240">Nyní přijmete práci pro registrační značku ve skladovém místě *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="67c23-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="67c23-241">Na kartě **Přehled** vyberte druhé ID práce pro typ pracovního příkazu *Cyklická inventura*.</span><span class="sxs-lookup"><span data-stu-id="67c23-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="67c23-242">V podokně Akce na kartě **Práce** ve skupině **Práce** vyberte **Cyklická inventura**.</span><span class="sxs-lookup"><span data-stu-id="67c23-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="67c23-243">Je zobrazen jeden řádek pro položku a registrační značku.</span><span class="sxs-lookup"><span data-stu-id="67c23-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="67c23-244">Hodnoty v polích **Napočítané množství** , **Skladové místo** , **Registrační značka** a **Položka** by měly odpovídat položkám množství vytvořeným na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="67c23-244">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="67c23-245">Vyberte řádek.</span><span class="sxs-lookup"><span data-stu-id="67c23-245">Select the line.</span></span>
1. <span data-ttu-id="67c23-246">V podokně Akce klikněte na možnost **Přijmout množství**.</span><span class="sxs-lookup"><span data-stu-id="67c23-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="67c23-247">Zobrazí se zpráva „Zaúčtování – deník“.</span><span class="sxs-lookup"><span data-stu-id="67c23-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="67c23-248">Vybrat **Podrobnosti zprávy** , zobrazí se číslo, pod kterým proběhlo zaúčtování do deníku.</span><span class="sxs-lookup"><span data-stu-id="67c23-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="67c23-249">Zavřete podrobnosti zprávy.</span><span class="sxs-lookup"><span data-stu-id="67c23-249">Close the message details.</span></span>
1. <span data-ttu-id="67c23-250">Obnovte stránku **Práce**.</span><span class="sxs-lookup"><span data-stu-id="67c23-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="67c23-251">Druhé ID práce bylo uzavřeno a již se nezobrazuje.</span><span class="sxs-lookup"><span data-stu-id="67c23-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="67c23-252">Chcete-li zobrazit uzavřenou práci, zaškrtněte políčko **Zobrazovat uzavřené** nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="67c23-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="67c23-253">Množství na skladě podle místa</span><span class="sxs-lookup"><span data-stu-id="67c23-253">On-hand by location</span></span>

1. <span data-ttu-id="67c23-254">Přejděte na **Řízení skladu \> Dotazy a sestavy \> Množství na skladě podle skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="67c23-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="67c23-255">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-255">Set the following values:</span></span>

    - <span data-ttu-id="67c23-256">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="67c23-256">**Site:** *6*</span></span>
    - <span data-ttu-id="67c23-257">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="67c23-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="67c23-258">**Obnovit napříč skladovými místy:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="67c23-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="67c23-259">Všimněte si, že skladové místo *01A01R1S1B* má dvě registrační značky:</span><span class="sxs-lookup"><span data-stu-id="67c23-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="67c23-260">**A0001** , kde je v poli **Pozice LP** zadána hodnota *1*</span><span class="sxs-lookup"><span data-stu-id="67c23-260">**A0001** , where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="67c23-261">**A0002** , kde je v poli **Pozice LP** zadána hodnota *2*</span><span class="sxs-lookup"><span data-stu-id="67c23-261">**A0002** , where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="67c23-262">Všimněte si, že skladové místo *01A01R1S2B* má jednu registrační značku:</span><span class="sxs-lookup"><span data-stu-id="67c23-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="67c23-263">**A0002** , kde je v poli **Pozice LP** zadána hodnota *1*</span><span class="sxs-lookup"><span data-stu-id="67c23-263">**A0002** , where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="67c23-264">Scénář prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="67c23-264">Sales order scenario</span></span>

<span data-ttu-id="67c23-265">Po nastavení funkce *Určení pozice registrační značky na skladovém místě* a přípravě inventury musíte vytvořit prodejní objednávku, aby se vygenerovala práce výdeje, která nasměruje pracovníka skladu k výdeji položky *A0002* z místa se zásobami, kde je ID palety na pozici *1*.</span><span class="sxs-lookup"><span data-stu-id="67c23-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="67c23-266">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="67c23-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="67c23-267">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="67c23-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67c23-268">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="67c23-269">**Účet zákazníka:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="67c23-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="67c23-270">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="67c23-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="67c23-271">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="67c23-271">Select **OK**.</span></span>
1. <span data-ttu-id="67c23-272">Na záložce s náhledem **Řádky prodejní objednávky** se do mřížky přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="67c23-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="67c23-273">Na tomto novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="67c23-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="67c23-274">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="67c23-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="67c23-275">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="67c23-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="67c23-276">V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="67c23-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="67c23-277">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob pro řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="67c23-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="67c23-278">Zavřete stránku **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="67c23-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="67c23-279">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="67c23-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="67c23-280">Zobrazí se informační zpráva indikující ID vlny a ID dodávky, jež byly vytvořeny pro tuto objednávku.</span><span class="sxs-lookup"><span data-stu-id="67c23-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="67c23-281">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Sklad** vyberte nad mřížkou možnost **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="67c23-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="67c23-282">Zobrazí se stránka **Práce** , na níž je zobrazena práce, která byla vytvořena pro řádek prodeje.</span><span class="sxs-lookup"><span data-stu-id="67c23-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="67c23-283">Poznamenejte si ID zobrazené práce.</span><span class="sxs-lookup"><span data-stu-id="67c23-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="67c23-284">Scénář výdeje pro prodej</span><span class="sxs-lookup"><span data-stu-id="67c23-284">Sales picking scenario</span></span>

1. <span data-ttu-id="67c23-285">Otevřete mobilní aplikaci a přihlaste se do skladu *61*.</span><span class="sxs-lookup"><span data-stu-id="67c23-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="67c23-286">Přejděte do **Výstupní \> Prodejní výdej**.</span><span class="sxs-lookup"><span data-stu-id="67c23-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="67c23-287">Na stránce **Naskenujte ID práce / ID registrační značky** vyberte pole **ID** a zadejte ID práce z řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="67c23-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="67c23-288">Všimněte si, že výdejová práce vás nasměruje k výdeji položky *A0002* z místa *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="67c23-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="67c23-289">Tuto instrukci obdržíte, protože položka *A0002* je na registrační značce, jež je na daném skladovém místě v pozici *1*.</span><span class="sxs-lookup"><span data-stu-id="67c23-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="67c23-290">![Pozice 1 skladového místa](media/LocationLicensePlatePositioning.png "Pozice 1 skladového místa")</span><span class="sxs-lookup"><span data-stu-id="67c23-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="67c23-291">Zadejte ID registrační značky vtvořené pro dané skladové místo a poté podle pokynů proveďte výdej prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="67c23-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
