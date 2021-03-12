---
title: Odchozí třídění
description: Toto téma popisuje informace o odchozím třídění. Tato funkce usnadňuje manipulaci s malými kontejnery a pomáhá pracovníkům skladu lépe plánovat a organizovat kapacitu palet v kamionu.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963403"
---
# <a name="outbound-sorting"></a><span data-ttu-id="e0cf1-104">Odchozí třídění</span><span class="sxs-lookup"><span data-stu-id="e0cf1-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0cf1-105">Tato funkce usnadňuje manipulaci s malými kontejnery a pomáhá pracovníkům skladu lépe plánovat a organizovat kapacitu palet v kamionu.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="e0cf1-106">Pokud používáte odchozí třídění, můžete třídit zabalené kontejnery na správnou paletu poté, co byly v balicí stanici.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="e0cf1-107">Můžete také vytvořit hierarchii balení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="e0cf1-108">Tato funkce umožňuje vytvářet palety z kontejnerů, které jsou zabaleny pomocí funkce balení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="e0cf1-109">Kontejner není odeslán na místo konečného dodání, protože je v původním balicím toku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="e0cf1-110">Místo toho mohou pracovníci uzavřít kontejner a přesunout jej do umístění typu řazení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="e0cf1-111">Poté mohou třídit kontejnery do pozic, z nichž každá má registrační značku (RZ).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="e0cf1-112">Po třídění kontejnerů lze vytvořit práci, která odešle celou registrační značku do konečného přepravního doku nebo do skladových míst fáze, podle pokynů pro určování polohy nebo podle vašich vlastních požadavků.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="e0cf1-113">Akce uzavření pozice řazení může navíc okamžitě přesunout zásoby na místo konečného dodání a vybrat je do objednávky.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="e0cf1-114">Zapnutí funkce Odchozí třídění</span><span class="sxs-lookup"><span data-stu-id="e0cf1-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="e0cf1-115">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="e0cf1-116">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e0cf1-117">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e0cf1-118">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e0cf1-119">**Název funkce:** *Odchozí třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="e0cf1-120">Nastavení</span><span class="sxs-lookup"><span data-stu-id="e0cf1-120">Setup</span></span>

<span data-ttu-id="e0cf1-121">Pro tento scénář musíte použít standardní ukázková data **USMF** demo data a sklad *62*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="e0cf1-122">Musíte také dokončit nastavení, které je popsáno v následujících podkapitolách.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="e0cf1-123">Nastavení šablony vlny</span><span class="sxs-lookup"><span data-stu-id="e0cf1-123">Set up a wave template</span></span>

<span data-ttu-id="e0cf1-124">Toto nastavení automaticky zpracuje vlnu a vytvoří práci při uvolnění řádku do skladu.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="e0cf1-125">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e0cf1-126">V seznamu šablon vyberte **Sklad 62**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="e0cf1-127">Na pevné záložce **Obecné** se ujistěte, že je možnost **Zpracovat vlnu při uvolnění do skladu** nastavená na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="e0cf1-128">Nastavení pracovníka</span><span class="sxs-lookup"><span data-stu-id="e0cf1-128">Set up a worker</span></span>

<span data-ttu-id="e0cf1-129">Balicí stanice se považuje za místo.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-129">The packing station is considered a location.</span></span> <span data-ttu-id="e0cf1-130">Pracovníci skladu, kteří se přihlásí na balicí stanici, vidí a pracují pouze na zásilkách a kontejnerech, které jsou plánovány v tomto konkrétním místě balení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="e0cf1-131">Uživatel, který se přihlásí do Microsoft Dynamics 365, musí být nastaven jako pracovník řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="e0cf1-132">Pokud se jméno uživatele neobjeví v seznamu pracovních uživatelů, přidejte je pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="e0cf1-133">Tyto kroky předpokládají, že uživatel již v systému existuje a byl v systému přidružen jako zaměstnanec nebo pracovník modulu **Lidské zdroje**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="e0cf1-134">Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="e0cf1-135">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-135">Select **New**.</span></span>
1. <span data-ttu-id="e0cf1-136">V poli **Pracovník** vyberte cílového uživatele v seznamu zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="e0cf1-137">Zvolte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-137">Select **Select**.</span></span>
1. <span data-ttu-id="e0cf1-138">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e0cf1-139">Na pevné záložce **Uživatelé** FastTab vyberte **Nový** k vytvoření účtu mobilního zařízení a nastavení následujících hodnot pro tento účet:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-140">**ID uživatele:** Zadejte jedinečný identifikátor.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="e0cf1-141">**Uživatelské jméno:** Zadejte název pro ID.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="e0cf1-142">**Výchozí sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-143">**Název nabídky:** *Hlavní*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="e0cf1-144">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e0cf1-145">Zobrazí se dialogové okno **Nastavit heslo**, ve kterém můžete vytvořit jednoduché heslo, pomocí něhož se uživatel může přihlásit k mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="e0cf1-146">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-146">Set the following values:</span></span>

    - <span data-ttu-id="e0cf1-147">**Heslo:** Zadejte jednoduché heslo.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="e0cf1-148">**Potvrdit heslo:** Znovu zadejte stejné heslo.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="e0cf1-149">Zvolte **Nastavit heslo**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-149">Select **Set password**.</span></span>

    <span data-ttu-id="e0cf1-150">Oznámení v Centru akcí vás informuje, že pro uživatele, kterého jste vytvořili, bylo nastaveno heslo.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="e0cf1-151">Vytvoření typu umístění</span><span class="sxs-lookup"><span data-stu-id="e0cf1-151">Create a location type</span></span>

1. <span data-ttu-id="e0cf1-152">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Typy umístění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="e0cf1-153">V podokně akcí vyberte **Nový** k vytvoření typu umístění a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-154">**Typ umístění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="e0cf1-155">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="e0cf1-156">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="e0cf1-157">Nastavení parametrů pro řízení skladu</span><span class="sxs-lookup"><span data-stu-id="e0cf1-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="e0cf1-158">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="e0cf1-159">Ka kartě **Obecné** na pevné záložce **Typy umístění** nastavte hodnotu pole **Typ místa třídění** na *SORT*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="e0cf1-160">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="e0cf1-161">Nastavení profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="e0cf1-161">Set up a location profile</span></span>

1. <span data-ttu-id="e0cf1-162">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="e0cf1-163">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-164">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-165">**ID profilu umístění:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="e0cf1-166">**Název:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="e0cf1-167">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-168">**Formát umístění:** *ASRB* (ulička, stojan, police a přihrádka)</span><span class="sxs-lookup"><span data-stu-id="e0cf1-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="e0cf1-169">**Typ umístění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="e0cf1-170">**Použít sledování registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="e0cf1-171">**Povolit smíšené položky:** *Ano* (Když tuto možnost nastavíte na *Ano*, možnost **Povolit smíšené dávky zásob** se automaticky nastaví na *Ano* a nelze ji změnit samostatně.)</span><span class="sxs-lookup"><span data-stu-id="e0cf1-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="e0cf1-172">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="e0cf1-173">Nastavení skladového místa</span><span class="sxs-lookup"><span data-stu-id="e0cf1-173">Set up a location</span></span>

1. <span data-ttu-id="e0cf1-174">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="e0cf1-175">V záhlaví zrušte zaškrtnutí políčka **Generovat kontrolní číslice pro místo**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="e0cf1-176">V podokně akcí vyberte **Nový** k vytvoření skladového místa a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-177">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-178">**Skladové místo:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="e0cf1-179">**ID profilu umístění:** *TŘÍDĚNǏ*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="e0cf1-180">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="e0cf1-181">Nastavte odchozí šablonu třídění</span><span class="sxs-lookup"><span data-stu-id="e0cf1-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="e0cf1-182">Odchozí šablona třídění určuje, zda se práce vytváří mimo místo třídění a zda se třídění provádí ručně nebo automaticky.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="e0cf1-183">Pro tento scénář vytvoříte odchozí šablonu třídění pro sestavení palet za balicí stanicí.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="e0cf1-184">Přejděte na **Řízení skladu \> Nastavení \> Balení \> Odchozí šablona třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="e0cf1-185">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-186">V záhlaví nové šablony nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-187">**ID odchozí šablony třídění:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="e0cf1-188">**Popis:** *Automatické vytvoření práce*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="e0cf1-189">**Typ odchozí šablony třídění:** *Kontejner*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="e0cf1-190">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-191">**Skladové místo:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="e0cf1-192">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-193">**Ověření řazení:** *Kontrola pozice*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="e0cf1-194">**Vytvořit práci při uzavření pozice:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="e0cf1-195">Když je tato možnost nastavená na *Ano* a pozice uzavřená, práce bude vytvořena, aby se přesunuly zásoby do konečného místa doručení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="e0cf1-196">Když je nastavená na *Ne*, zásoby budou ihned přiděleny do objednávky při zavření pozice.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="e0cf1-197">**Přiřazení pozice:** *Automaticky*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="e0cf1-198">Pokud je pole nastaveno na *Ruční*, uživatel musí vždy označit, do jaké pozice mají být zásoby setříděny.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="e0cf1-199">Pokud je nastavená na *Automaticky*, systém automaticky navede zásoby do pozice, kdykoli je to možné, na základě přestávek šablony třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="e0cf1-200">V podokně akcí zvolte možnost **Uložit**. Tím se zpřístupní možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="e0cf1-201">V podokně Akce vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="e0cf1-202">V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="e0cf1-203">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e0cf1-204">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e0cf1-205">**Pole:** *Služba dopravce*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="e0cf1-206">Po výběru této hodnoty se vám může zobrazit následující zpráva: „Služba dopravce není indexové pole.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="e0cf1-207">Chcete k němu přidat třídění?“</span><span class="sxs-lookup"><span data-stu-id="e0cf1-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="e0cf1-208">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-208">Select **Yes**.</span></span>

    - <span data-ttu-id="e0cf1-209">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e0cf1-210">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-210">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-211">Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“</span><span class="sxs-lookup"><span data-stu-id="e0cf1-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="e0cf1-212">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-212">Select **Yes**.</span></span>

    <span data-ttu-id="e0cf1-213">Aktivuje se tlačítko **Zalomení odchozích šablon třídění** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="e0cf1-214">V podokně akcí vyberte možnost **Zalomení odchozích šablon třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="e0cf1-215">V dialogovém okně **Odchozí kritéria třídění** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-216">**Název referenční tabulky:** *Zásilky*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="e0cf1-217">**Název referenčního pole:** *Přepravní služba*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="e0cf1-218">**Seskupit podle pole:** Zaškrtněte toto políčko pro seskupení dodávek podle přepravní služby.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="e0cf1-219">Volbou **OK** uložte svá nastavení a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="e0cf1-220">Nastavení zásad balení kontejneru</span><span class="sxs-lookup"><span data-stu-id="e0cf1-220">Set up container packing policies</span></span>

1. <span data-ttu-id="e0cf1-221">Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Zásady balení kontejneru**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="e0cf1-222">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-223">V záhlaví nové zásady nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-224">**Zásady balení kontejnerů:** *Třídit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-225">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="e0cf1-226">Na pevné záložce **Přehled** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-227">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-228">**Výchozí místo pro třídění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="e0cf1-229">**Hmotnost/jedn.:** *kg*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="e0cf1-230">**Zásady uzavírání kontejnerů:** *Automatické vydání*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="e0cf1-231">**Zásady uvolňování kontejnerů:** *Přiřadit kontejner k odchozí poloze třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="e0cf1-232">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="e0cf1-233">Nastavení profilů balení</span><span class="sxs-lookup"><span data-stu-id="e0cf1-233">Set up packing profiles</span></span>

<span data-ttu-id="e0cf1-234">Vytvořte nový profil balení, který bude použit spolu s funkcí třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="e0cf1-235">Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="e0cf1-236">V podokně akcí vyberte **Nový** k vytvoření řádky a nastavte pro ni následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-237">**ID profilu balení:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-238">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-239">**Zásady balení kontejnerů:** *Třídit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-240">**Režim ID kontejneru:** *Automatický*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="e0cf1-241">**Typ kontejneru:** *Velká krabice*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="e0cf1-242">**Automatické vytvoření kontejneru při uzavření kontejneru:** Vymazáno (= *Ne*)</span><span class="sxs-lookup"><span data-stu-id="e0cf1-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="e0cf1-243">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="e0cf1-244">Nastavení tříd práce</span><span class="sxs-lookup"><span data-stu-id="e0cf1-244">Set up work classes</span></span>

<span data-ttu-id="e0cf1-245">Nastavte pracovní třídu, která bude použita společně s tříděním.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="e0cf1-246">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="e0cf1-247">V podokně akcí vyberte **Nový** k vytvoření pracovní třídy k třídění a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-248">**ID pracovní třídy:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-249">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-250">**Typ pracovního příkazu:** *Výběr tříděných zásob*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="e0cf1-251">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="e0cf1-252">Vytvoření položek nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="e0cf1-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="e0cf1-253">Nastavení položky nabídky nové palety</span><span class="sxs-lookup"><span data-stu-id="e0cf1-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="e0cf1-254">Vytvořte položku nabídky mobilního zařízení pro vtvoření palet během třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="e0cf1-255">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e0cf1-256">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-257">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-258">**Název položky nabídky:** *Sestavení palety*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="e0cf1-259">**Název:** *Sestavení palety*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="e0cf1-260">**Režim:** *Nepřímý*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="e0cf1-261">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="e0cf1-262">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-263">**Kód aktivity:** *Odchozí třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="e0cf1-264">Když je toto pole nastaveno na *Odchozí třídění*, zobrazí se pole **ID šablony odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="e0cf1-265">**Použít průvodce procesem:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="e0cf1-266">Když je hodnota v poli **Kód aktivity** nastavená na *Odchozí třídění*, je tato možnost automaticky nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="e0cf1-267">**ID odchozí šablony třídění:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="e0cf1-268">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="e0cf1-269">Nastavení nové položky nabídky načtení</span><span class="sxs-lookup"><span data-stu-id="e0cf1-269">Set up a new loading menu item</span></span>

<span data-ttu-id="e0cf1-270">Dále vytvořte položku nabídky, která uživatelům umožní přesunout setříděné skladové položky do místa expedice.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="e0cf1-271">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e0cf1-272">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-273">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-274">**Název položky nabídky:** *Načíst z třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="e0cf1-275">**Název:** *Načíst z třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="e0cf1-276">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e0cf1-277">**Použít existující práci:** - *Ano*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="e0cf1-278">Na pevné záložce **Obecné** nastavte hodnotu v poli **Řídí:** na *Řízeno systémem*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="e0cf1-279">Na pevné záložce **Pracovní třídy** vyberte **Nový** a pak nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="e0cf1-280">**ID pracovní třídy:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="e0cf1-281">**Typ pracovního příkazu:** *Výběr tříděných zásob*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="e0cf1-282">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="e0cf1-283">Nastavení nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="e0cf1-283">Set up the mobile device menu</span></span>

<span data-ttu-id="e0cf1-284">Nyní musíte nové položky nabídky přidat do nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="e0cf1-285">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="e0cf1-286">Vyberte nabídku **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="e0cf1-287">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e0cf1-288">Ve sloupci **Dostupné nabídky a položky nabídky** najděte a vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="e0cf1-289">Stisknutím tlačítka se šipkou doprava přesuňte **Sestavení palety** do sloupce **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="e0cf1-290">Použijte tlačítka se šipkou nahoru a dolů pro přesunutí položky nabídky **Sestavení palety** na požadovanou pozici v nabídce mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="e0cf1-291">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-291">Select **Save**.</span></span>
1. <span data-ttu-id="e0cf1-292">Opakujte tento postup pro přidání položky nabídky **Načíst z třídění** do nabídky **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="e0cf1-293">Nastavit směrnice skladových míst</span><span class="sxs-lookup"><span data-stu-id="e0cf1-293">Set up location directives</span></span>

<span data-ttu-id="e0cf1-294">*Směrnice skladového místa* jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="e0cf1-295">Nyní musíte vytvořit pravidlo pro správu třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="e0cf1-296">Nastavení směrnice jedné skladové jednotky</span><span class="sxs-lookup"><span data-stu-id="e0cf1-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="e0cf1-297">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="e0cf1-298">V levém podokně změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="e0cf1-299">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-300">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-301">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="e0cf1-302">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="e0cf1-303">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-304">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="e0cf1-305">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-305">**Site:** *6*</span></span>
    - <span data-ttu-id="e0cf1-306">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-307">**Více skladových jednotek:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="e0cf1-308">Chcete-li, aby byl dostupný panel nástrojů na pevné záožce **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="e0cf1-309">Na pevné záložce **Řádky** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="e0cf1-310">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="e0cf1-311">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="e0cf1-312">**Od:** *0*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-312">**From:** *0*</span></span>
    - <span data-ttu-id="e0cf1-313">**Do:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="e0cf1-314">Chcete-li, aby byl dostupný panel nástrojů na pevné záložce **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="e0cf1-315">Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="e0cf1-316">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="e0cf1-317">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="e0cf1-318">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="e0cf1-319">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-319">Select **Save**.</span></span>
1. <span data-ttu-id="e0cf1-320">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="e0cf1-321">V editoru dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="e0cf1-322">Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="e0cf1-323">Výběrem **OK** uložte nastavení a zavřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="e0cf1-324">Nastavení směrnice více skladových jednotek</span><span class="sxs-lookup"><span data-stu-id="e0cf1-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="e0cf1-325">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="e0cf1-326">V levém podokně změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="e0cf1-327">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-328">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-329">**Posloupnost:** *2*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="e0cf1-330">**Název:** *Více nákladových bran*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="e0cf1-331">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-332">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="e0cf1-333">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-333">**Site:** *6*</span></span>
    - <span data-ttu-id="e0cf1-334">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-335">**Více SKU:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="e0cf1-336">Chcete-li, aby byl dostupný panel nástrojů na pevné záožce **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="e0cf1-337">Na pevné záložce **Řádky** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="e0cf1-338">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="e0cf1-339">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="e0cf1-340">**Od:** *0*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-340">**From:** *0*</span></span>
    - <span data-ttu-id="e0cf1-341">**Do:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="e0cf1-342">Chcete-li, aby byl dostupný panel nástrojů na pevné záložce **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="e0cf1-343">Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="e0cf1-344">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="e0cf1-345">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="e0cf1-346">**Název:** *Více nákladových bran*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="e0cf1-347">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-347">Select **Save**.</span></span>
1. <span data-ttu-id="e0cf1-348">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="e0cf1-349">V editoru dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="e0cf1-350">Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="e0cf1-351">Výběrem **OK** uložte nastavení a zavřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="e0cf1-352">Nastavit šablony práce</span><span class="sxs-lookup"><span data-stu-id="e0cf1-352">Set up work templates</span></span>

1. <span data-ttu-id="e0cf1-353">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="e0cf1-354">Změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="e0cf1-355">V podokně Akce vyberte možnost **Nový** a vytvořte šablonu práce.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="e0cf1-356">Na kartě **Přehled** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-357">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="e0cf1-358">**Šablona práce:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="e0cf1-359">**Popis šablony práce:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="e0cf1-360">Chcete-li, aby byla dostupná záložka s náhledem **Podrobnosti šablony práce**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="e0cf1-361">Na pevné záložce **Podrobnosti pracovní šablony** vyberte **Nový**, chcete-li přidat řádek a poté pro něj nastavit následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-362">**Typ práce:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="e0cf1-363">**ID pracovní třídy:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="e0cf1-364">Vyberte **Nový** pro přidání druhého řádku a pak pro něho nastavte tyto hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="e0cf1-365">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="e0cf1-366">**ID pracovní třídy:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="e0cf1-367">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="e0cf1-368">Scénář</span><span class="sxs-lookup"><span data-stu-id="e0cf1-368">Scenario</span></span>

<span data-ttu-id="e0cf1-369">Tento scénář simuluje situaci, kdy by se balené kontejnery měly automaticky třídit do různých pozic (palet) po balicí stanici, v závislosti na službě přepravce.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="e0cf1-370">Poté, co jsou všechny položky z nákladu zabaleny a roztříděny podle adresy, budou palety přemístěny k nákladové bráně.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="e0cf1-371">Vytvoření prodejních objednávek a výběr práce</span><span class="sxs-lookup"><span data-stu-id="e0cf1-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="e0cf1-372">Vytvoření prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="e0cf1-372">Create sales order 1</span></span>

1. <span data-ttu-id="e0cf1-373">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e0cf1-374">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-375">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-376">**Účet zákazníka:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="e0cf1-377">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e0cf1-378">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="e0cf1-379">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="e0cf1-380">Přepněte na zobrazení **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e0cf1-381">Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-382">**Dopravce dodávky:** *Letecká přeprava*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="e0cf1-383">**Služba dopravce:** *Air*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="e0cf1-384">Přepněte do zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="e0cf1-385">Pokud se do mřížky na pevné záložce **Řádky prodejní objednávky** automaticky nepřidá prázdný řádek, vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="e0cf1-386">Na novém řádku objednávky nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-387">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="e0cf1-388">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e0cf1-389">V době, kdy je vybrán nový řádek na pevné záložce **Řádky prodejní objednávky**, vyberte v nabídce **Zásoby** nad mřížkou možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e0cf1-390">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="e0cf1-391">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e0cf1-392">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="e0cf1-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e0cf1-393">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="e0cf1-394">Poznamenejte si čísla ID vlny a ID dodávky.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="e0cf1-395">Prodejní objednávka 2</span><span class="sxs-lookup"><span data-stu-id="e0cf1-395">Sales order 2</span></span>

1. <span data-ttu-id="e0cf1-396">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e0cf1-397">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e0cf1-398">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-399">**Účet zákazníka:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="e0cf1-400">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e0cf1-401">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="e0cf1-402">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-402">The new sales order is opened.</span></span> <span data-ttu-id="e0cf1-403">Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="e0cf1-404">Na tomto řádku objednávky nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="e0cf1-405">**Položka:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="e0cf1-406">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e0cf1-407">Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** nastavte pole **Způsob dodání** na *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="e0cf1-408">Na pevné záložce **Řádky prodejní objednávky** vyberte **Přidat řádek** a pak na druhém řádku objednávky nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="e0cf1-409">**Položka:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="e0cf1-410">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e0cf1-411">Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** změňte hodnotu pole **Způsob dodání** na *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="e0cf1-412">Na pevné záložce **Řádky prodejní objednávky** vyberte první řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="e0cf1-413">Pak v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e0cf1-414">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="e0cf1-415">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e0cf1-416">Na pevné záložce **Řádky prodejní objednávky** vyberte druhý řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="e0cf1-417">Pak v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e0cf1-418">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="e0cf1-419">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e0cf1-420">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="e0cf1-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e0cf1-421">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="e0cf1-422">Všimněte si, že byla vytvořena dvě identifikační čísla vln a dvě identifikační čísla zásilek, jedno pro každý režim doručení pro řádky prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="e0cf1-423">Získání ID práce z podrobností o práci</span><span class="sxs-lookup"><span data-stu-id="e0cf1-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="e0cf1-424">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="e0cf1-425">Na této stránce jsou uvedena ID práce, která byla vytvořena z prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="e0cf1-426">Pomocí ID vlny a ID zásilky z prodejních objednávek, které jste vytvořili, vyhledejte pracovní ID pro každou vlnu a zásilku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="e0cf1-427">Poznamenejte si tato ID práce, protože je budete potřebovat v dalších krocích.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="e0cf1-428">Všimněte si, že pro druhou prodejní objednávku byla vytvořena dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="e0cf1-429">Pokud jsou různé položky vybrány z různých umístění, vygenerují se samostatná ID slov.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="e0cf1-430">Vyberte položky pro prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="e0cf1-430">Pick items for the sales orders</span></span>

<span data-ttu-id="e0cf1-431">Vytvořené dílo dokončete pomocí mobilního zařízení k přesunutí položek do balicí stanice.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="e0cf1-432">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="e0cf1-433">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="e0cf1-434">V nabídce **Odchozí** vyberte **Prodejní výdej**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="e0cf1-435">V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="e0cf1-436">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-436">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-437">Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku, která byla vytvořena pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="e0cf1-438">Všimněte si, že se zobrazí místo výběru (*hromadně-001*), položka (*A0001*) a množství (*2 ks*).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="e0cf1-439">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-439">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-440">Zkontrolujte informace na stránce **prodejní objednávky: vložení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="e0cf1-441">V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="e0cf1-442">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-442">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-443">Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva Práce dokončena, která uvádí, že bylo dokončeno ID práce z prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="e0cf1-444">Nyní si vyberete prodejní objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="e0cf1-445">V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 2, kde na řádku 1 je položka *A0001*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="e0cf1-446">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-446">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-447">Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="e0cf1-448">Všimněte si, že se zobrazí místo výběru (*hromadně-001*), položka (*A0001*) a množství (*1 ks*).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="e0cf1-449">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-449">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-450">Zkontrolujte informace na stránce **prodejní objednávky: vložení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="e0cf1-451">V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="e0cf1-452">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-452">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-453">Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="e0cf1-454">Tato zpráva označuje, že ID práce z řádku 1 prodejní objednávky 2 bylo dokončeno.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="e0cf1-455">V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 2, kde na řádku 2 je položka *A0002*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="e0cf1-456">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-456">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-457">Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="e0cf1-458">Všimněte si, že se zobrazí místo výběru (*hromadně-002*), položka (*A0001*) a množství (*1 ks*).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="e0cf1-459">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-459">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-460">Zkontrolujte informace na stránce **prodejní objednávky: vložení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="e0cf1-461">V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="e0cf1-462">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-462">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-463">Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="e0cf1-464">Tato zpráva označuje, že ID práce z řádku 2 prodejní objednávky 2 bylo dokončeno.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="e0cf1-465">Balení prodejních objednávek do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="e0cf1-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="e0cf1-466">Balení prodejní objednávky 1 do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="e0cf1-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="e0cf1-467">Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Balení**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="e0cf1-468">Otevře se dialogové okno **Vybrat balicí stanici**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="e0cf1-469">Ve výchozím nastavení by mělo být v poli **Pracovník** nastaveno jméno pracovníka, kterého jste nastavili dříve.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="e0cf1-470">Chcete-li zobrazit a pracovat na zásilkách a kontejnerech, které jsou plánovány na konkrétním místě balení, nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="e0cf1-471">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-471">**Site:** *6*</span></span>
    - <span data-ttu-id="e0cf1-472">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e0cf1-473">**Místo:** *balení*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="e0cf1-474">**ID profilu balení:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="e0cf1-475">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="e0cf1-476">Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="e0cf1-477">Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="e0cf1-478">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e0cf1-479">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="e0cf1-480">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="e0cf1-481">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-482">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e0cf1-483">**Identifikátor:** Položka *A0001*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="e0cf1-484">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e0cf1-485">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="e0cf1-486">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-486">Select **OK**.</span></span> <span data-ttu-id="e0cf1-487">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="e0cf1-488">Vytvořte druhý kontejner a přidejte druhou položku z registrační značky pro prodejní objednávku 1 do nového kontejneru.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="e0cf1-489">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e0cf1-490">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="e0cf1-491">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="e0cf1-492">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-493">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e0cf1-494">**Identifikátor:** Položka *A0001*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="e0cf1-495">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e0cf1-496">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="e0cf1-497">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-497">Select **OK**.</span></span> <span data-ttu-id="e0cf1-498">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="e0cf1-499">Balení prodejní objednávky 2 do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="e0cf1-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="e0cf1-500">Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku řádek 1 prodejní objednávky 2.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="e0cf1-501">Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="e0cf1-502">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e0cf1-503">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="e0cf1-504">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="e0cf1-505">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-506">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e0cf1-507">**Identifikátor:** Položka *A0001*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="e0cf1-508">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e0cf1-509">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="e0cf1-510">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-510">Select **OK**.</span></span> <span data-ttu-id="e0cf1-511">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="e0cf1-512">V poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku řádek 2 prodejní objednávky 2.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="e0cf1-513">Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="e0cf1-514">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e0cf1-515">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="e0cf1-516">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="e0cf1-517">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="e0cf1-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e0cf1-518">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e0cf1-519">**Pole identifikátoru:** Položka *A0002*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="e0cf1-520">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e0cf1-521">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="e0cf1-522">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-522">Select **OK**.</span></span> <span data-ttu-id="e0cf1-523">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="e0cf1-524">Chcete-li zobrazit podrobnosti o kontejneru, přejděte na **Řízení skladu \> Balení a kontejnerizace \> Kontejnery** a vyhledejte ID kontejnerů, které byly vytvořeny během balení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="e0cf1-525">Třídění kontejnerů</span><span class="sxs-lookup"><span data-stu-id="e0cf1-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0cf1-526">Jakmile přejdete na položku nabídky **Sestavení palety** v mobilní aplikaci pro odchozí třídění, uvidíte tlačítko označené jako **Plné**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="e0cf1-527">*Tlačítko **Plné** nepoužívejte pro seřazení nebo uzavření pozice.*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="e0cf1-528">Tlačítko **Plné** je ve výchozím nastavení k dispozici a nelze jej na stránce deaktivovat ani odebrat.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="e0cf1-529">Nepoužívá se pro funkci *Odchozí třídění*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="e0cf1-530">Třídění prvního kontejneru</span><span class="sxs-lookup"><span data-stu-id="e0cf1-530">Sort the first container</span></span>

1. <span data-ttu-id="e0cf1-531">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="e0cf1-532">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="e0cf1-533">V nabídce **Odchozí** vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="e0cf1-534">Do pole **Registrační značka/kontejner** zadejte ID prvního kontejneru spojeného s prodejní objednávkou 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="e0cf1-535">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-535">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-536">Protože v současné době neexistují žádné pozice řazení, musíte nějakou zadat.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="e0cf1-537">Do pole **ID pozice třídění** zadejte *SP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="e0cf1-538">Protože k pozici řazení není aktuálně přiřazen žádná RZ *SP01*, musíte ji zadat.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="e0cf1-539">Do pole **LP** zadejte hodnotu *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="e0cf1-540">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-540">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-541">Protože je zapnuto ověření pozice řazení, musíte znovu zadat ID pozice řazení.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="e0cf1-542">Do pole **ID pozice třídění** zadejte *SP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="e0cf1-543">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-543">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-544">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="e0cf1-545">Pokud chcete zobrazit pozici třídění a registrační značku, kterou obsahuje, přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="e0cf1-546">Na stránce **Přiřazení pozice odchozího třídění** se zobrazují všechny aktuálně aktivní pozice třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="e0cf1-547">Pole **Seřadit transakce pozic** zobrazuje RP, která je přidružena jednotlivým pozicím třídění, a kontejnery, které jsou v poloze třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="e0cf1-548">Momentálně existuje jedna pozice třídění a na pevné záložce **Seřadit kritéria pozice** se zobrazuje kritérium **Zásilka - Dopravní služba - Letecká doprava**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="e0cf1-549">Třídění zbývajících kontejnerů</span><span class="sxs-lookup"><span data-stu-id="e0cf1-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="e0cf1-550">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="e0cf1-551">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="e0cf1-552">V nabídce **Odchozí** vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="e0cf1-553">Do pole **Registrační značka/kontejner** zadejte ID druhého kontejneru spojeného s prodejní objednávkou 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="e0cf1-554">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-554">Select **OK**.</span></span> <span data-ttu-id="e0cf1-555">Protože je šablona třídění nastavena na automatické třídění a pozice třídění, která již obsahuje kritéria pro přiřazení, již existuje, jste automaticky přesměrováni na správnou pozici třídění.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="e0cf1-556">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-556">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-557">Potvrďte ID pozice třídění a označte, že jsou zásoby na správném místě.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="e0cf1-558">Do pole **ID pozice třídění** zadejte *SP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="e0cf1-559">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-559">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-560">Práce na druhém kontejneru byla dokončena z prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="e0cf1-561">Nyní budete třídit zbývající kontejnery z prodejní objednávky 2.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="e0cf1-562">Do pole **Registrační značka / kontejner** zadejte ID kontejneru z prodejní objednávky 2, která obsahuje zboží *A0001*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="e0cf1-563">Protože se služba operátora liší, budete vyzváni k zadání nové pozice řazení a přiřazení RZ této poloze.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="e0cf1-564">Použijte pozici třídění *SP02* a RZ *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="e0cf1-565">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-565">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-566">Potvrďte pozici třídění zadáním *SP02* do pole **ID polohy třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="e0cf1-567">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-567">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-568">Práce na kontejneru byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="e0cf1-569">Do pole **Registrační značka / kontejner** zadejte ID zbývajícího kontejneru z prodejní objednávky 2, která obsahuje zboží *A0002*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="e0cf1-570">Protože služba operátora je stejná jako služba operátora pro prodejní objednávku 1, systém zobrazí existující pozici řazení, která má odpovídající kritéria.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="e0cf1-571">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-571">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-572">Potvrďte pozici třídění zadáním *SP01* do pole **ID pozice třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="e0cf1-573">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-573">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-574">Práce na kontejneru byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="e0cf1-575">Zavřete odchozí pozice třídění</span><span class="sxs-lookup"><span data-stu-id="e0cf1-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="e0cf1-576">Po roztřídění všech zásob musí být pozice před vytvořením práce uzavřena.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="e0cf1-577">Vytvoří se práce výběru seřazených zásob pro převedení zásob k nákladové bráně.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="e0cf1-578">Zavřete pozici z mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="e0cf1-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="e0cf1-579">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="e0cf1-580">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="e0cf1-581">V nabídce **Odchozí** vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="e0cf1-582">Do pole **Registrační značka / kontejner** zadejte ID kontejneru tříděné do pozice *SP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="e0cf1-583">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-583">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-584">Zobrazí se následující zpráva: "Kontejner je již zařazen na pozici SP01.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="e0cf1-585">Uzavřít pozici?"</span><span class="sxs-lookup"><span data-stu-id="e0cf1-585">Close the position?"</span></span> <span data-ttu-id="e0cf1-586">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-586">Select **Close**.</span></span>

    <span data-ttu-id="e0cf1-587">Práce je dokončena.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="e0cf1-588">Uzavřete pozici z přiřazení odchozí pozice třídění</span><span class="sxs-lookup"><span data-stu-id="e0cf1-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="e0cf1-589">Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="e0cf1-590">V levém sloupci vyberte možnost **SP02**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="e0cf1-591">Tento řádek pro odchozí třídění je ten, který uzavřete.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="e0cf1-592">V podokně akcí zvolte **Zavřít pozici**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="e0cf1-593">Záznam pozice třídění je uzavřen a již se nezobrazuje.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="e0cf1-594">Chcete-li zobrazit všechny záznamy uzavřené polohy, zaškrtněte políčko **Zobrazit uzavřené**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="e0cf1-595">Výdej setříděných zásob</span><span class="sxs-lookup"><span data-stu-id="e0cf1-595">Sorted inventory picking</span></span>

<span data-ttu-id="e0cf1-596">Musíte dokončit práci výběru tříděných zásob.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="e0cf1-597">Po dokončení budou zásoby vybrány do prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="e0cf1-598">V tomto okamžiku platí všechny ostatní skladové procesy.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="e0cf1-599">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="e0cf1-600">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="e0cf1-601">V nabídce **Odchozí** vyberte **Načíst z třídění**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="e0cf1-602">Zadejte cílové ID LP z první pozice třídění, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="e0cf1-603">Nastavte pole **ID** na *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="e0cf1-604">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-604">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-605">Na stránce **Výběr seřazených zásob: Vybrat** se zobrazuje práce výběru, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="e0cf1-606">Vyberte z umístění *SORT* a cílového RZ *PLP01*, který má více položek a množství *3*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="e0cf1-607">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-607">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-608">Na stránce **Výběr seřazených zásob: Vložit** se zobrazuje práce vložení, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="e0cf1-609">Vložte do umístění *Nákladová brána* a cílového RZ *PLP01*, který má více položek a množství *3*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="e0cf1-610">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-610">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-611">Práce je dokončena.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-611">Work is completed.</span></span>

1. <span data-ttu-id="e0cf1-612">Zadejte cílové ID registrační značky ze druhé pozice třídění, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="e0cf1-613">Nastavte pole **ID** na *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="e0cf1-614">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-614">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-615">Na stránce **Výběr seřazených zásob: Vybrat** se zobrazuje práce výběru, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="e0cf1-616">Vyberte z umístění *SORT* a cílového RZ *PLP02*, který má více položek a množství *1*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="e0cf1-617">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-617">Select **OK**.</span></span>
1. <span data-ttu-id="e0cf1-618">Na stránce **Výběr seřazených zásob: Vložit** se zobrazuje práce vložení, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="e0cf1-619">Vložte do umístění *Nákladová brána* a cílového RZ *PLP02*, který má více položek a množství *1*.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="e0cf1-620">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-620">Select **OK**.</span></span>

    <span data-ttu-id="e0cf1-621">Práce je dokončena.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-621">Work is completed.</span></span>

<span data-ttu-id="e0cf1-622">Odteď platí všechny ostatní skladové procesy.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-622">From this point forward, all other warehouse processes apply.</span></span>
