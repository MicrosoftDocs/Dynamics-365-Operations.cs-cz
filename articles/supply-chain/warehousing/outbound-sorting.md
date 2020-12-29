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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424233"
---
# <a name="outbound-sorting"></a><span data-ttu-id="d0e23-104">Odchozí třídění</span><span class="sxs-lookup"><span data-stu-id="d0e23-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0e23-105">Tato funkce usnadňuje manipulaci s malými kontejnery a pomáhá pracovníkům skladu lépe plánovat a organizovat kapacitu palet v kamionu.</span><span class="sxs-lookup"><span data-stu-id="d0e23-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="d0e23-106">Pokud používáte odchozí třídění, můžete třídit zabalené kontejnery na správnou paletu poté, co byly v balicí stanici.</span><span class="sxs-lookup"><span data-stu-id="d0e23-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="d0e23-107">Můžete také vytvořit hierarchii balení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="d0e23-108">Tato funkce umožňuje vytvářet palety z kontejnerů, které jsou zabaleny pomocí funkce balení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="d0e23-109">Kontejner není odeslán na místo konečného dodání, protože je v původním balicím toku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="d0e23-110">Místo toho mohou pracovníci uzavřít kontejner a přesunout jej do umístění typu řazení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="d0e23-111">Poté mohou třídit kontejnery do pozic, z nichž každá má registrační značku (RZ).</span><span class="sxs-lookup"><span data-stu-id="d0e23-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="d0e23-112">Po třídění kontejnerů lze vytvořit práci, která odešle celou registrační značku do konečného přepravního doku nebo do skladových míst fáze, podle pokynů pro určování polohy nebo podle vašich vlastních požadavků.</span><span class="sxs-lookup"><span data-stu-id="d0e23-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="d0e23-113">Akce uzavření pozice řazení může navíc okamžitě přesunout zásoby na místo konečného dodání a vybrat je do objednávky.</span><span class="sxs-lookup"><span data-stu-id="d0e23-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="d0e23-114">Zapnutí funkce Odchozí třídění</span><span class="sxs-lookup"><span data-stu-id="d0e23-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="d0e23-115">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="d0e23-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="d0e23-116">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="d0e23-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d0e23-117">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="d0e23-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d0e23-118">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="d0e23-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d0e23-119">**Název funkce:** *Odchozí třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="d0e23-120">Nastavení</span><span class="sxs-lookup"><span data-stu-id="d0e23-120">Setup</span></span>

<span data-ttu-id="d0e23-121">Pro tento scénář musíte použít standardní ukázková data **USMF** demo data a sklad *62*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="d0e23-122">Musíte také dokončit nastavení, které je popsáno v následujících podkapitolách.</span><span class="sxs-lookup"><span data-stu-id="d0e23-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="d0e23-123">Nastavení šablony vlny</span><span class="sxs-lookup"><span data-stu-id="d0e23-123">Set up a wave template</span></span>

<span data-ttu-id="d0e23-124">Toto nastavení automaticky zpracuje vlnu a vytvoří práci při uvolnění řádku do skladu.</span><span class="sxs-lookup"><span data-stu-id="d0e23-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="d0e23-125">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="d0e23-126">V seznamu šablon vyberte **Sklad 62**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="d0e23-127">Na pevné záložce **Obecné** se ujistěte, že je možnost **Zpracovat vlnu při uvolnění do skladu** nastavená na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="d0e23-128">Nastavení pracovníka</span><span class="sxs-lookup"><span data-stu-id="d0e23-128">Set up a worker</span></span>

<span data-ttu-id="d0e23-129">Balicí stanice se považuje za místo.</span><span class="sxs-lookup"><span data-stu-id="d0e23-129">The packing station is considered a location.</span></span> <span data-ttu-id="d0e23-130">Pracovníci skladu, kteří se přihlásí na balicí stanici, vidí a pracují pouze na zásilkách a kontejnerech, které jsou plánovány v tomto konkrétním místě balení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="d0e23-131">Uživatel, který se přihlásí do Microsoft Dynamics 365, musí být nastaven jako pracovník řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="d0e23-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="d0e23-132">Pokud se jméno uživatele neobjeví v seznamu pracovních uživatelů, přidejte je pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="d0e23-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="d0e23-133">Tyto kroky předpokládají, že uživatel již v systému existuje a byl v systému přidružen jako zaměstnanec nebo pracovník modulu **Lidské zdroje**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="d0e23-134">Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="d0e23-135">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-135">Select **New**.</span></span>
1. <span data-ttu-id="d0e23-136">V poli **Pracovník** vyberte cílového uživatele v seznamu zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="d0e23-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="d0e23-137">Zvolte **Zvolit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-137">Select **Select**.</span></span>
1. <span data-ttu-id="d0e23-138">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d0e23-139">Na pevné záložce **Uživatelé** FastTab vyberte **Nový** k vytvoření účtu mobilního zařízení a nastavení následujících hodnot pro tento účet:</span><span class="sxs-lookup"><span data-stu-id="d0e23-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-140">**ID uživatele:** Zadejte jedinečný identifikátor.</span><span class="sxs-lookup"><span data-stu-id="d0e23-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="d0e23-141">**Uživatelské jméno:** Zadejte název pro ID.</span><span class="sxs-lookup"><span data-stu-id="d0e23-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="d0e23-142">**Výchozí sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-143">**Název nabídky:** *Hlavní*</span><span class="sxs-lookup"><span data-stu-id="d0e23-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="d0e23-144">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d0e23-145">Zobrazí se dialogové okno **Nastavit heslo**, ve kterém můžete vytvořit jednoduché heslo, pomocí něhož se uživatel může přihlásit k mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="d0e23-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="d0e23-146">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-146">Set the following values:</span></span>

    - <span data-ttu-id="d0e23-147">**Heslo:** Zadejte jednoduché heslo.</span><span class="sxs-lookup"><span data-stu-id="d0e23-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="d0e23-148">**Potvrdit heslo:** Znovu zadejte stejné heslo.</span><span class="sxs-lookup"><span data-stu-id="d0e23-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="d0e23-149">Zvolte **Nastavit heslo**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-149">Select **Set password**.</span></span>

    <span data-ttu-id="d0e23-150">Oznámení v Centru akcí vás informuje, že pro uživatele, kterého jste vytvořili, bylo nastaveno heslo.</span><span class="sxs-lookup"><span data-stu-id="d0e23-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="d0e23-151">Vytvoření typu umístění</span><span class="sxs-lookup"><span data-stu-id="d0e23-151">Create a location type</span></span>

1. <span data-ttu-id="d0e23-152">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Typy umístění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="d0e23-153">V podokně akcí vyberte **Nový** k vytvoření typu umístění a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-154">**Typ umístění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="d0e23-155">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="d0e23-156">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="d0e23-157">Nastavení parametrů pro řízení skladu</span><span class="sxs-lookup"><span data-stu-id="d0e23-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="d0e23-158">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="d0e23-159">Ka kartě **Obecné** na pevné záložce **Typy umístění** nastavte hodnotu pole **Typ místa třídění** na *SORT*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="d0e23-160">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="d0e23-161">Nastavení profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="d0e23-161">Set up a location profile</span></span>

1. <span data-ttu-id="d0e23-162">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="d0e23-163">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-164">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="d0e23-165">**ID profilu umístění:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="d0e23-166">**Název:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="d0e23-167">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-168">**Formát umístění:** *ASRB* (ulička, stojan, police a přihrádka)</span><span class="sxs-lookup"><span data-stu-id="d0e23-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="d0e23-169">**Typ umístění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="d0e23-170">**Použít sledování registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="d0e23-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="d0e23-171">**Povolit smíšené položky:** *Ano* (Když tuto možnost nastavíte na *Ano*, možnost **Povolit smíšené dávky zásob** se automaticky nastaví na *Ano* a nelze ji změnit samostatně.)</span><span class="sxs-lookup"><span data-stu-id="d0e23-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="d0e23-172">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="d0e23-173">Nastavení skladového místa</span><span class="sxs-lookup"><span data-stu-id="d0e23-173">Set up a location</span></span>

1. <span data-ttu-id="d0e23-174">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="d0e23-175">V záhlaví zrušte zaškrtnutí políčka **Generovat kontrolní číslice pro místo**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="d0e23-176">V podokně akcí vyberte **Nový** k vytvoření skladového místa a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-177">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-178">**Skladové místo:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="d0e23-179">**ID profilu umístění:** *TŘÍDĚNǏ*</span><span class="sxs-lookup"><span data-stu-id="d0e23-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="d0e23-180">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="d0e23-181">Nastavte odchozí šablonu třídění</span><span class="sxs-lookup"><span data-stu-id="d0e23-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="d0e23-182">Odchozí šablona třídění určuje, zda se práce vytváří mimo místo třídění a zda se třídění provádí ručně nebo automaticky.</span><span class="sxs-lookup"><span data-stu-id="d0e23-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="d0e23-183">Pro tento scénář vytvoříte odchozí šablonu třídění pro sestavení palet za balicí stanicí.</span><span class="sxs-lookup"><span data-stu-id="d0e23-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="d0e23-184">Přejděte na **Řízení skladu \> Nastavení \> Balení \> Odchozí šablona třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="d0e23-185">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-186">V záhlaví nové šablony nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="d0e23-187">**ID odchozí šablony třídění:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="d0e23-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="d0e23-188">**Popis:** *Automatické vytvoření práce*</span><span class="sxs-lookup"><span data-stu-id="d0e23-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="d0e23-189">**Typ odchozí šablony třídění:** *Kontejner*</span><span class="sxs-lookup"><span data-stu-id="d0e23-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="d0e23-190">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-191">**Skladové místo:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="d0e23-192">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-193">**Ověření řazení:** *Kontrola pozice*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="d0e23-194">**Vytvořit práci při uzavření pozice:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="d0e23-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="d0e23-195">Když je tato možnost nastavená na *Ano* a pozice uzavřená, práce bude vytvořena, aby se přesunuly zásoby do konečného místa doručení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="d0e23-196">Když je nastavená na *Ne*, zásoby budou ihned přiděleny do objednávky při zavření pozice.</span><span class="sxs-lookup"><span data-stu-id="d0e23-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="d0e23-197">**Přiřazení pozice:** *Automaticky*</span><span class="sxs-lookup"><span data-stu-id="d0e23-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="d0e23-198">Pokud je pole nastaveno na *Ruční*, uživatel musí vždy označit, do jaké pozice mají být zásoby setříděny.</span><span class="sxs-lookup"><span data-stu-id="d0e23-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="d0e23-199">Pokud je nastavená na *Automaticky*, systém automaticky navede zásoby do pozice, kdykoli je to možné, na základě přestávek šablony třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="d0e23-200">V podokně akcí zvolte možnost **Uložit**. Tím se zpřístupní možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="d0e23-201">V podokně Akce vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="d0e23-202">V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="d0e23-203">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="d0e23-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="d0e23-204">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="d0e23-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="d0e23-205">**Pole:** *Služba dopravce*</span><span class="sxs-lookup"><span data-stu-id="d0e23-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="d0e23-206">Po výběru této hodnoty se vám může zobrazit následující zpráva: „Služba dopravce není indexové pole.</span><span class="sxs-lookup"><span data-stu-id="d0e23-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="d0e23-207">Chcete k němu přidat třídění?“</span><span class="sxs-lookup"><span data-stu-id="d0e23-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="d0e23-208">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-208">Select **Yes**.</span></span>

    - <span data-ttu-id="d0e23-209">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="d0e23-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="d0e23-210">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-210">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-211">Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“</span><span class="sxs-lookup"><span data-stu-id="d0e23-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="d0e23-212">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-212">Select **Yes**.</span></span>

    <span data-ttu-id="d0e23-213">Aktivuje se tlačítko **Zalomení odchozích šablon třídění** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="d0e23-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="d0e23-214">V podokně akcí vyberte možnost **Zalomení odchozích šablon třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="d0e23-215">V dialogovém okně **Odchozí kritéria třídění** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d0e23-216">**Název referenční tabulky:** *Zásilky*</span><span class="sxs-lookup"><span data-stu-id="d0e23-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="d0e23-217">**Název referenčního pole:** *Přepravní služba*</span><span class="sxs-lookup"><span data-stu-id="d0e23-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="d0e23-218">**Seskupit podle pole:** Zaškrtněte toto políčko pro seskupení dodávek podle přepravní služby.</span><span class="sxs-lookup"><span data-stu-id="d0e23-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="d0e23-219">Volbou **OK** uložte svá nastavení a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d0e23-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="d0e23-220">Nastavení zásad balení kontejneru</span><span class="sxs-lookup"><span data-stu-id="d0e23-220">Set up container packing policies</span></span>

1. <span data-ttu-id="d0e23-221">Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Zásady balení kontejneru**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="d0e23-222">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-223">V záhlaví nové zásady nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="d0e23-224">**Zásady balení kontejnerů:** *Třídit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-225">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="d0e23-226">Na pevné záložce **Přehled** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-227">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-228">**Výchozí místo pro třídění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="d0e23-229">**Hmotnost/jedn.:** *kg*</span><span class="sxs-lookup"><span data-stu-id="d0e23-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="d0e23-230">**Zásady uzavírání kontejnerů:** *Automatické vydání*</span><span class="sxs-lookup"><span data-stu-id="d0e23-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="d0e23-231">**Zásady uvolňování kontejnerů:** *Přiřadit kontejner k odchozí poloze třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="d0e23-232">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="d0e23-233">Nastavení profilů balení</span><span class="sxs-lookup"><span data-stu-id="d0e23-233">Set up packing profiles</span></span>

<span data-ttu-id="d0e23-234">Vytvořte nový profil balení, který bude použit spolu s funkcí třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="d0e23-235">Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="d0e23-236">V podokně akcí vyberte **Nový** k vytvoření řádky a nastavte pro ni následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-237">**ID profilu balení:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-238">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-239">**Zásady balení kontejnerů:** *Třídit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-240">**Režim ID kontejneru:** *Automatický*</span><span class="sxs-lookup"><span data-stu-id="d0e23-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="d0e23-241">**Typ kontejneru:** *Velká krabice*</span><span class="sxs-lookup"><span data-stu-id="d0e23-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="d0e23-242">**Automatické vytvoření kontejneru při uzavření kontejneru:** Vymazáno (= *Ne*)</span><span class="sxs-lookup"><span data-stu-id="d0e23-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="d0e23-243">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="d0e23-244">Nastavení tříd práce</span><span class="sxs-lookup"><span data-stu-id="d0e23-244">Set up work classes</span></span>

<span data-ttu-id="d0e23-245">Nastavte pracovní třídu, která bude použita společně s tříděním.</span><span class="sxs-lookup"><span data-stu-id="d0e23-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="d0e23-246">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d0e23-247">V podokně akcí vyberte **Nový** k vytvoření pracovní třídy k třídění a nastavte pro něj následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-248">**ID pracovní třídy:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-249">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-250">**Typ pracovního příkazu:** *Výběr tříděných zásob*</span><span class="sxs-lookup"><span data-stu-id="d0e23-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="d0e23-251">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="d0e23-252">Vytvoření položek nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="d0e23-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="d0e23-253">Nastavení položky nabídky nové palety</span><span class="sxs-lookup"><span data-stu-id="d0e23-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="d0e23-254">Vytvořte položku nabídky mobilního zařízení pro vtvoření palet během třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="d0e23-255">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d0e23-256">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-257">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="d0e23-258">**Název položky nabídky:** *Sestavení palety*</span><span class="sxs-lookup"><span data-stu-id="d0e23-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="d0e23-259">**Název:** *Sestavení palety*</span><span class="sxs-lookup"><span data-stu-id="d0e23-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="d0e23-260">**Režim:** *Nepřímý*</span><span class="sxs-lookup"><span data-stu-id="d0e23-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="d0e23-261">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="d0e23-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="d0e23-262">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-263">**Kód aktivity:** *Odchozí třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="d0e23-264">Když je toto pole nastaveno na *Odchozí třídění*, zobrazí se pole **ID šablony odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="d0e23-265">**Použít průvodce procesem:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="d0e23-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="d0e23-266">Když je hodnota v poli **Kód aktivity** nastavená na *Odchozí třídění*, je tato možnost automaticky nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="d0e23-267">**ID odchozí šablony třídění:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="d0e23-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="d0e23-268">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="d0e23-269">Nastavení nové položky nabídky načtení</span><span class="sxs-lookup"><span data-stu-id="d0e23-269">Set up a new loading menu item</span></span>

<span data-ttu-id="d0e23-270">Dále vytvořte položku nabídky, která uživatelům umožní přesunout setříděné skladové položky do místa expedice.</span><span class="sxs-lookup"><span data-stu-id="d0e23-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="d0e23-271">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d0e23-272">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-273">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="d0e23-274">**Název položky nabídky:** *Načíst z třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="d0e23-275">**Název:** *Načíst z třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="d0e23-276">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="d0e23-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="d0e23-277">**Použít existující práci:** - *Ano*</span><span class="sxs-lookup"><span data-stu-id="d0e23-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="d0e23-278">Na pevné záložce **Obecné** nastavte hodnotu v poli **Řídí:** na *Řízeno systémem*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="d0e23-279">Na pevné záložce **Pracovní třídy** vyberte **Nový** a pak nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0e23-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d0e23-280">**ID pracovní třídy:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="d0e23-281">**Typ pracovního příkazu:** *Výběr tříděných zásob*</span><span class="sxs-lookup"><span data-stu-id="d0e23-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="d0e23-282">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="d0e23-283">Nastavení nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="d0e23-283">Set up the mobile device menu</span></span>

<span data-ttu-id="d0e23-284">Nyní musíte nové položky nabídky přidat do nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="d0e23-285">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="d0e23-286">Vyberte nabídku **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="d0e23-287">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d0e23-288">Ve sloupci **Dostupné nabídky a položky nabídky** najděte a vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="d0e23-289">Stisknutím tlačítka se šipkou doprava přesuňte **Sestavení palety** do sloupce **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="d0e23-290">Použijte tlačítka se šipkou nahoru a dolů pro přesunutí položky nabídky **Sestavení palety** na požadovanou pozici v nabídce mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="d0e23-291">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-291">Select **Save**.</span></span>
1. <span data-ttu-id="d0e23-292">Opakujte tento postup pro přidání položky nabídky **Načíst z třídění** do nabídky **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="d0e23-293">Nastavit směrnice skladových míst</span><span class="sxs-lookup"><span data-stu-id="d0e23-293">Set up location directives</span></span>

<span data-ttu-id="d0e23-294">*Směrnice skladového místa* jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob.</span><span class="sxs-lookup"><span data-stu-id="d0e23-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="d0e23-295">Nyní musíte vytvořit pravidlo pro správu třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="d0e23-296">Nastavení směrnice jedné skladové jednotky</span><span class="sxs-lookup"><span data-stu-id="d0e23-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="d0e23-297">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d0e23-298">V levém podokně změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d0e23-299">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-300">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="d0e23-301">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d0e23-302">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="d0e23-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="d0e23-303">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-304">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d0e23-305">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="d0e23-305">**Site:** *6*</span></span>
    - <span data-ttu-id="d0e23-306">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-307">**Více skladových jednotek:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="d0e23-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="d0e23-308">Chcete-li, aby byl dostupný panel nástrojů na pevné záožce **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d0e23-309">Na pevné záložce **Řádky** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0e23-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="d0e23-310">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="d0e23-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d0e23-311">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d0e23-312">**Od:** *0*</span><span class="sxs-lookup"><span data-stu-id="d0e23-312">**From:** *0*</span></span>
    - <span data-ttu-id="d0e23-313">**Do:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="d0e23-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="d0e23-314">Chcete-li, aby byl dostupný panel nástrojů na pevné záložce **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d0e23-315">Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0e23-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="d0e23-316">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="d0e23-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d0e23-317">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d0e23-318">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="d0e23-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="d0e23-319">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-319">Select **Save**.</span></span>
1. <span data-ttu-id="d0e23-320">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d0e23-321">V editoru dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="d0e23-322">Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="d0e23-323">Výběrem **OK** uložte nastavení a zavřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="d0e23-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="d0e23-324">Nastavení směrnice více skladových jednotek</span><span class="sxs-lookup"><span data-stu-id="d0e23-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="d0e23-325">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d0e23-326">V levém podokně změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d0e23-327">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-328">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="d0e23-329">**Posloupnost:** *2*</span><span class="sxs-lookup"><span data-stu-id="d0e23-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="d0e23-330">**Název:** *Více nákladových bran*</span><span class="sxs-lookup"><span data-stu-id="d0e23-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="d0e23-331">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-332">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d0e23-333">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="d0e23-333">**Site:** *6*</span></span>
    - <span data-ttu-id="d0e23-334">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-335">**Více SKU:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="d0e23-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="d0e23-336">Chcete-li, aby byl dostupný panel nástrojů na pevné záožce **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d0e23-337">Na pevné záložce **Řádky** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0e23-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="d0e23-338">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="d0e23-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d0e23-339">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d0e23-340">**Od:** *0*</span><span class="sxs-lookup"><span data-stu-id="d0e23-340">**From:** *0*</span></span>
    - <span data-ttu-id="d0e23-341">**Do:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="d0e23-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="d0e23-342">Chcete-li, aby byl dostupný panel nástrojů na pevné záložce **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d0e23-343">Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0e23-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="d0e23-344">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="d0e23-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d0e23-345">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d0e23-346">**Název:** *Více nákladových bran*</span><span class="sxs-lookup"><span data-stu-id="d0e23-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="d0e23-347">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-347">Select **Save**.</span></span>
1. <span data-ttu-id="d0e23-348">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d0e23-349">V editoru dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="d0e23-350">Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="d0e23-351">Výběrem **OK** uložte nastavení a zavřete editor dotazů.</span><span class="sxs-lookup"><span data-stu-id="d0e23-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="d0e23-352">Nastavit šablony práce</span><span class="sxs-lookup"><span data-stu-id="d0e23-352">Set up work templates</span></span>

1. <span data-ttu-id="d0e23-353">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d0e23-354">Změňte hodnotu pole **Typ pracovního příkazu** na *Výběr tříděných zásob*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d0e23-355">V podokně Akce vyberte možnost **Nový** a vytvořte šablonu práce.</span><span class="sxs-lookup"><span data-stu-id="d0e23-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="d0e23-356">Na kartě **Přehled** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-357">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d0e23-358">**Šablona práce:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="d0e23-359">**Popis šablony práce:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="d0e23-360">Chcete-li, aby byla dostupná záložka s náhledem **Podrobnosti šablony práce**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d0e23-361">Na pevné záložce **Podrobnosti pracovní šablony** vyberte **Nový**, chcete-li přidat řádek a poté pro něj nastavit následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-362">**Typ práce:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="d0e23-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d0e23-363">**ID pracovní třídy:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="d0e23-364">Vyberte **Nový** pro přidání druhého řádku a pak pro něho nastavte tyto hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="d0e23-365">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="d0e23-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d0e23-366">**ID pracovní třídy:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="d0e23-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="d0e23-367">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d0e23-368">Scénář</span><span class="sxs-lookup"><span data-stu-id="d0e23-368">Scenario</span></span>

<span data-ttu-id="d0e23-369">Tento scénář simuluje situaci, kdy by se balené kontejnery měly automaticky třídit do různých pozic (palet) po balicí stanici, v závislosti na službě přepravce.</span><span class="sxs-lookup"><span data-stu-id="d0e23-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="d0e23-370">Poté, co jsou všechny položky z nákladu zabaleny a roztříděny podle adresy, budou palety přemístěny k nákladové bráně.</span><span class="sxs-lookup"><span data-stu-id="d0e23-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="d0e23-371">Vytvoření prodejních objednávek a výběr práce</span><span class="sxs-lookup"><span data-stu-id="d0e23-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="d0e23-372">Vytvoření prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="d0e23-372">Create sales order 1</span></span>

1. <span data-ttu-id="d0e23-373">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d0e23-374">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-375">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d0e23-376">**Účet zákazníka:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="d0e23-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="d0e23-377">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d0e23-378">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d0e23-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="d0e23-379">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="d0e23-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="d0e23-380">Přepněte na zobrazení **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="d0e23-381">Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="d0e23-382">**Dopravce dodávky:** *Letecká přeprava*</span><span class="sxs-lookup"><span data-stu-id="d0e23-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="d0e23-383">**Služba dopravce:** *Air*</span><span class="sxs-lookup"><span data-stu-id="d0e23-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="d0e23-384">Přepněte do zobrazení **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="d0e23-385">Pokud se do mřížky na pevné záložce **Řádky prodejní objednávky** automaticky nepřidá prázdný řádek, vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="d0e23-386">Na novém řádku objednávky nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="d0e23-387">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d0e23-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d0e23-388">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="d0e23-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="d0e23-389">V době, kdy je vybrán nový řádek na pevné záložce **Řádky prodejní objednávky**, vyberte v nabídce **Zásoby** nad mřížkou možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d0e23-390">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="d0e23-391">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="d0e23-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="d0e23-392">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="d0e23-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="d0e23-393">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="d0e23-394">Poznamenejte si čísla ID vlny a ID dodávky.</span><span class="sxs-lookup"><span data-stu-id="d0e23-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="d0e23-395">Prodejní objednávka 2</span><span class="sxs-lookup"><span data-stu-id="d0e23-395">Sales order 2</span></span>

1. <span data-ttu-id="d0e23-396">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d0e23-397">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0e23-398">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d0e23-399">**Účet zákazníka:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="d0e23-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="d0e23-400">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d0e23-401">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d0e23-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="d0e23-402">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="d0e23-402">The new sales order is opened.</span></span> <span data-ttu-id="d0e23-403">Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d0e23-404">Na tomto řádku objednávky nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="d0e23-405">**Položka:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d0e23-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="d0e23-406">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="d0e23-407">Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** nastavte pole **Způsob dodání** na *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="d0e23-408">Na pevné záložce **Řádky prodejní objednávky** vyberte **Přidat řádek** a pak na druhém řádku objednávky nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="d0e23-409">**Položka:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="d0e23-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="d0e23-410">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="d0e23-411">Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** změňte hodnotu pole **Způsob dodání** na *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="d0e23-412">Na pevné záložce **Řádky prodejní objednávky** vyberte první řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="d0e23-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="d0e23-413">Pak v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d0e23-414">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="d0e23-415">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="d0e23-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="d0e23-416">Na pevné záložce **Řádky prodejní objednávky** vyberte druhý řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="d0e23-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="d0e23-417">Pak v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d0e23-418">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="d0e23-419">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="d0e23-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="d0e23-420">V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**</span><span class="sxs-lookup"><span data-stu-id="d0e23-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="d0e23-421">Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="d0e23-422">Všimněte si, že byla vytvořena dvě identifikační čísla vln a dvě identifikační čísla zásilek, jedno pro každý režim doručení pro řádky prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="d0e23-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="d0e23-423">Získání ID práce z podrobností o práci</span><span class="sxs-lookup"><span data-stu-id="d0e23-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="d0e23-424">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="d0e23-425">Na této stránce jsou uvedena ID práce, která byla vytvořena z prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="d0e23-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="d0e23-426">Pomocí ID vlny a ID zásilky z prodejních objednávek, které jste vytvořili, vyhledejte pracovní ID pro každou vlnu a zásilku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="d0e23-427">Poznamenejte si tato ID práce, protože je budete potřebovat v dalších krocích.</span><span class="sxs-lookup"><span data-stu-id="d0e23-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="d0e23-428">Všimněte si, že pro druhou prodejní objednávku byla vytvořena dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="d0e23-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="d0e23-429">Pokud jsou různé položky vybrány z různých umístění, vygenerují se samostatná ID slov.</span><span class="sxs-lookup"><span data-stu-id="d0e23-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="d0e23-430">Vyberte položky pro prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="d0e23-430">Pick items for the sales orders</span></span>

<span data-ttu-id="d0e23-431">Vytvořené dílo dokončete pomocí mobilního zařízení k přesunutí položek do balicí stanice.</span><span class="sxs-lookup"><span data-stu-id="d0e23-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="d0e23-432">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="d0e23-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="d0e23-433">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d0e23-434">V nabídce **Odchozí** vyberte **Prodejní výdej**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="d0e23-435">V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="d0e23-436">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-436">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-437">Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku, která byla vytvořena pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="d0e23-438">Všimněte si, že se zobrazí místo výběru (*hromadně-001*), položka (*A0001*) a množství (*2 ks*).</span><span class="sxs-lookup"><span data-stu-id="d0e23-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="d0e23-439">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-439">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-440">Zkontrolujte informace na stránce **prodejní objednávky: vložení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="d0e23-441">V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="d0e23-442">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-442">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-443">Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva Práce dokončena, která uvádí, že bylo dokončeno ID práce z prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="d0e23-444">Nyní si vyberete prodejní objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="d0e23-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="d0e23-445">V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 2, kde na řádku 1 je položka *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="d0e23-446">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-446">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-447">Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="d0e23-448">Všimněte si, že se zobrazí místo výběru (*hromadně-001*), položka (*A0001*) a množství (*1 ks*).</span><span class="sxs-lookup"><span data-stu-id="d0e23-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="d0e23-449">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-449">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-450">Zkontrolujte informace na stránce **prodejní objednávky: vložení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="d0e23-451">V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="d0e23-452">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-452">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-453">Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="d0e23-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="d0e23-454">Tato zpráva označuje, že ID práce z řádku 1 prodejní objednávky 2 bylo dokončeno.</span><span class="sxs-lookup"><span data-stu-id="d0e23-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="d0e23-455">V poli **ID** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku 2, kde na řádku 2 je položka *A0002*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="d0e23-456">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-456">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-457">Na stránce **Prodejní objednávky - výběr** zadejte cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="d0e23-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="d0e23-458">Všimněte si, že se zobrazí místo výběru (*hromadně-002*), položka (*A0001*) a množství (*1 ks*).</span><span class="sxs-lookup"><span data-stu-id="d0e23-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="d0e23-459">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-459">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-460">Zkontrolujte informace na stránce **prodejní objednávky: vložení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="d0e23-461">V poli **Loc** by mělo být uvedeno, že vybrané položky jdou do umístění *Balíček*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="d0e23-462">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-462">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-463">Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="d0e23-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="d0e23-464">Tato zpráva označuje, že ID práce z řádku 2 prodejní objednávky 2 bylo dokončeno.</span><span class="sxs-lookup"><span data-stu-id="d0e23-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="d0e23-465">Balení prodejních objednávek do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="d0e23-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="d0e23-466">Balení prodejní objednávky 1 do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="d0e23-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="d0e23-467">Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Balení**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="d0e23-468">Otevře se dialogové okno **Vybrat balicí stanici**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="d0e23-469">Ve výchozím nastavení by mělo být v poli **Pracovník** nastaveno jméno pracovníka, kterého jste nastavili dříve.</span><span class="sxs-lookup"><span data-stu-id="d0e23-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="d0e23-470">Chcete-li zobrazit a pracovat na zásilkách a kontejnerech, které jsou plánovány na konkrétním místě balení, nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="d0e23-471">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="d0e23-471">**Site:** *6*</span></span>
    - <span data-ttu-id="d0e23-472">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="d0e23-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d0e23-473">**Místo:** *balení*</span><span class="sxs-lookup"><span data-stu-id="d0e23-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="d0e23-474">**ID profilu balení:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="d0e23-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="d0e23-475">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d0e23-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="d0e23-476">Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="d0e23-477">Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.</span><span class="sxs-lookup"><span data-stu-id="d0e23-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="d0e23-478">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="d0e23-479">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="d0e23-480">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d0e23-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="d0e23-481">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-482">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="d0e23-483">**Identifikátor:** Položka *A0001*</span><span class="sxs-lookup"><span data-stu-id="d0e23-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="d0e23-484">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="d0e23-485">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="d0e23-486">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-486">Select **OK**.</span></span> <span data-ttu-id="d0e23-487">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="d0e23-488">Vytvořte druhý kontejner a přidejte druhou položku z registrační značky pro prodejní objednávku 1 do nového kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d0e23-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="d0e23-489">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="d0e23-490">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="d0e23-491">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d0e23-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="d0e23-492">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-493">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="d0e23-494">**Identifikátor:** Položka *A0001*</span><span class="sxs-lookup"><span data-stu-id="d0e23-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="d0e23-495">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="d0e23-496">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="d0e23-497">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-497">Select **OK**.</span></span> <span data-ttu-id="d0e23-498">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="d0e23-499">Balení prodejní objednávky 2 do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="d0e23-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="d0e23-500">Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku řádek 1 prodejní objednávky 2.</span><span class="sxs-lookup"><span data-stu-id="d0e23-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="d0e23-501">Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.</span><span class="sxs-lookup"><span data-stu-id="d0e23-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="d0e23-502">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="d0e23-503">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="d0e23-504">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d0e23-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="d0e23-505">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-506">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="d0e23-507">**Identifikátor:** Položka *A0001*</span><span class="sxs-lookup"><span data-stu-id="d0e23-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="d0e23-508">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="d0e23-509">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="d0e23-510">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-510">Select **OK**.</span></span> <span data-ttu-id="d0e23-511">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="d0e23-512">V poli **Registrační značka nebo zásilka** zadejte cílovou registrační značku řádek 2 prodejní objednávky 2.</span><span class="sxs-lookup"><span data-stu-id="d0e23-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="d0e23-513">Pak na klávesnici použijte klávesu **Tab** nebo **Enter** pro přesun mimo pole.</span><span class="sxs-lookup"><span data-stu-id="d0e23-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="d0e23-514">V podokně akcí zvolte **Nový kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="d0e23-515">Přijměte všechna výchozí nastavení a vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="d0e23-516">Poznamenejte si ID kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d0e23-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="d0e23-517">Na pevné záložce **Balení položky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d0e23-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d0e23-518">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0e23-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="d0e23-519">**Pole identifikátoru:** Položka *A0002*</span><span class="sxs-lookup"><span data-stu-id="d0e23-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="d0e23-520">V podokně akcí zvolte **Zavřít kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="d0e23-521">V dialogovém okně **zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby systém aktualizoval pole **Celková hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="d0e23-522">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-522">Select **OK**.</span></span> <span data-ttu-id="d0e23-523">Kontejner se přesune do skladového místa *SORT* a je připraven k třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="d0e23-524">Chcete-li zobrazit podrobnosti o kontejneru, přejděte na **Řízení skladu \> Balení a kontejnerizace \> Kontejnery** a vyhledejte ID kontejnerů, které byly vytvořeny během balení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="d0e23-525">Třídění kontejnerů</span><span class="sxs-lookup"><span data-stu-id="d0e23-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0e23-526">Jakmile přejdete na položku nabídky **Sestavení palety** v mobilní aplikaci pro odchozí třídění, uvidíte tlačítko označené jako **Plné**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="d0e23-527">*Tlačítko **Plné** nepoužívejte pro seřazení nebo uzavření pozice.*</span><span class="sxs-lookup"><span data-stu-id="d0e23-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="d0e23-528">Tlačítko **Plné** je ve výchozím nastavení k dispozici a nelze jej na stránce deaktivovat ani odebrat.</span><span class="sxs-lookup"><span data-stu-id="d0e23-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="d0e23-529">Nepoužívá se pro funkci *Odchozí třídění*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="d0e23-530">Třídění prvního kontejneru</span><span class="sxs-lookup"><span data-stu-id="d0e23-530">Sort the first container</span></span>

1. <span data-ttu-id="d0e23-531">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="d0e23-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="d0e23-532">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d0e23-533">V nabídce **Odchozí** vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="d0e23-534">Do pole **Registrační značka/kontejner** zadejte ID prvního kontejneru spojeného s prodejní objednávkou 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="d0e23-535">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-535">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-536">Protože v současné době neexistují žádné pozice řazení, musíte nějakou zadat.</span><span class="sxs-lookup"><span data-stu-id="d0e23-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="d0e23-537">Do pole **ID pozice třídění** zadejte *SP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="d0e23-538">Protože k pozici řazení není aktuálně přiřazen žádná RZ *SP01*, musíte ji zadat.</span><span class="sxs-lookup"><span data-stu-id="d0e23-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="d0e23-539">Do pole **LP** zadejte hodnotu *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="d0e23-540">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-540">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-541">Protože je zapnuto ověření pozice řazení, musíte znovu zadat ID pozice řazení.</span><span class="sxs-lookup"><span data-stu-id="d0e23-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="d0e23-542">Do pole **ID pozice třídění** zadejte *SP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="d0e23-543">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-543">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-544">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="d0e23-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="d0e23-545">Pokud chcete zobrazit pozici třídění a registrační značku, kterou obsahuje, přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="d0e23-546">Na stránce **Přiřazení pozice odchozího třídění** se zobrazují všechny aktuálně aktivní pozice třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="d0e23-547">Pole **Seřadit transakce pozic** zobrazuje RP, která je přidružena jednotlivým pozicím třídění, a kontejnery, které jsou v poloze třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="d0e23-548">Momentálně existuje jedna pozice třídění a na pevné záložce **Seřadit kritéria pozice** se zobrazuje kritérium **Zásilka - Dopravní služba - Letecká doprava**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="d0e23-549">Třídění zbývajících kontejnerů</span><span class="sxs-lookup"><span data-stu-id="d0e23-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="d0e23-550">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="d0e23-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="d0e23-551">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d0e23-552">V nabídce **Odchozí** vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="d0e23-553">Do pole **Registrační značka/kontejner** zadejte ID druhého kontejneru spojeného s prodejní objednávkou 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="d0e23-554">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-554">Select **OK**.</span></span> <span data-ttu-id="d0e23-555">Protože je šablona třídění nastavena na automatické třídění a pozice třídění, která již obsahuje kritéria pro přiřazení, již existuje, jste automaticky přesměrováni na správnou pozici třídění.</span><span class="sxs-lookup"><span data-stu-id="d0e23-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="d0e23-556">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-556">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-557">Potvrďte ID pozice třídění a označte, že jsou zásoby na správném místě.</span><span class="sxs-lookup"><span data-stu-id="d0e23-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="d0e23-558">Do pole **ID pozice třídění** zadejte *SP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="d0e23-559">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-559">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-560">Práce na druhém kontejneru byla dokončena z prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="d0e23-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="d0e23-561">Nyní budete třídit zbývající kontejnery z prodejní objednávky 2.</span><span class="sxs-lookup"><span data-stu-id="d0e23-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="d0e23-562">Do pole **Registrační značka / kontejner** zadejte ID kontejneru z prodejní objednávky 2, která obsahuje zboží *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="d0e23-563">Protože se služba operátora liší, budete vyzváni k zadání nové pozice řazení a přiřazení RZ této poloze.</span><span class="sxs-lookup"><span data-stu-id="d0e23-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="d0e23-564">Použijte pozici třídění *SP02* a RZ *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="d0e23-565">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-565">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-566">Potvrďte pozici třídění zadáním *SP02* do pole **ID polohy třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="d0e23-567">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-567">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-568">Práce na kontejneru byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="d0e23-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="d0e23-569">Do pole **Registrační značka / kontejner** zadejte ID zbývajícího kontejneru z prodejní objednávky 2, která obsahuje zboží *A0002*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="d0e23-570">Protože služba operátora je stejná jako služba operátora pro prodejní objednávku 1, systém zobrazí existující pozici řazení, která má odpovídající kritéria.</span><span class="sxs-lookup"><span data-stu-id="d0e23-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="d0e23-571">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-571">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-572">Potvrďte pozici třídění zadáním *SP01* do pole **ID pozice třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="d0e23-573">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-573">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-574">Práce na kontejneru byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="d0e23-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="d0e23-575">Zavřete odchozí pozice třídění</span><span class="sxs-lookup"><span data-stu-id="d0e23-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="d0e23-576">Po roztřídění všech zásob musí být pozice před vytvořením práce uzavřena.</span><span class="sxs-lookup"><span data-stu-id="d0e23-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="d0e23-577">Vytvoří se práce výběru seřazených zásob pro převedení zásob k nákladové bráně.</span><span class="sxs-lookup"><span data-stu-id="d0e23-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="d0e23-578">Zavřete pozici z mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="d0e23-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="d0e23-579">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="d0e23-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="d0e23-580">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d0e23-581">V nabídce **Odchozí** vyberte **Sestavení palety**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="d0e23-582">Do pole **Registrační značka / kontejner** zadejte ID kontejneru tříděné do pozice *SP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="d0e23-583">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-583">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-584">Zobrazí se následující zpráva: "Kontejner je již zařazen na pozici SP01.</span><span class="sxs-lookup"><span data-stu-id="d0e23-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="d0e23-585">Uzavřít pozici?"</span><span class="sxs-lookup"><span data-stu-id="d0e23-585">Close the position?"</span></span> <span data-ttu-id="d0e23-586">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-586">Select **Close**.</span></span>

    <span data-ttu-id="d0e23-587">Práce je dokončena.</span><span class="sxs-lookup"><span data-stu-id="d0e23-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="d0e23-588">Uzavřete pozici z přiřazení odchozí pozice třídění</span><span class="sxs-lookup"><span data-stu-id="d0e23-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="d0e23-589">Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="d0e23-590">V levém sloupci vyberte možnost **SP02**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="d0e23-591">Tento řádek pro odchozí třídění je ten, který uzavřete.</span><span class="sxs-lookup"><span data-stu-id="d0e23-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="d0e23-592">V podokně akcí zvolte **Zavřít pozici**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="d0e23-593">Záznam pozice třídění je uzavřen a již se nezobrazuje.</span><span class="sxs-lookup"><span data-stu-id="d0e23-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="d0e23-594">Chcete-li zobrazit všechny záznamy uzavřené polohy, zaškrtněte políčko **Zobrazit uzavřené**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="d0e23-595">Výdej setříděných zásob</span><span class="sxs-lookup"><span data-stu-id="d0e23-595">Sorted inventory picking</span></span>

<span data-ttu-id="d0e23-596">Musíte dokončit práci výběru tříděných zásob.</span><span class="sxs-lookup"><span data-stu-id="d0e23-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="d0e23-597">Po dokončení budou zásoby vybrány do prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d0e23-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="d0e23-598">V tomto okamžiku platí všechny ostatní skladové procesy.</span><span class="sxs-lookup"><span data-stu-id="d0e23-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="d0e23-599">Na mobilním zařízení se přihlaste do skladu *62* pomocí ID uživatele, které jste pro tento scénář vytvořili (nebo ID existujícího uživatele ukázkových dat).</span><span class="sxs-lookup"><span data-stu-id="d0e23-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="d0e23-600">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d0e23-601">V nabídce **Odchozí** vyberte **Načíst z třídění**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="d0e23-602">Zadejte cílové ID LP z první pozice třídění, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="d0e23-603">Nastavte pole **ID** na *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="d0e23-604">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-604">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-605">Na stránce **Výběr seřazených zásob: Vybrat** se zobrazuje práce výběru, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="d0e23-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="d0e23-606">Vyberte z umístění *SORT* a cílového RZ *PLP01*, který má více položek a množství *3*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="d0e23-607">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-607">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-608">Na stránce **Výběr seřazených zásob: Vložit** se zobrazuje práce vložení, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="d0e23-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="d0e23-609">Vložte do umístění *Nákladová brána* a cílového RZ *PLP01*, který má více položek a množství *3*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="d0e23-610">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-610">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-611">Práce je dokončena.</span><span class="sxs-lookup"><span data-stu-id="d0e23-611">Work is completed.</span></span>

1. <span data-ttu-id="d0e23-612">Zadejte cílové ID registrační značky ze druhé pozice třídění, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="d0e23-613">Nastavte pole **ID** na *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="d0e23-614">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-614">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-615">Na stránce **Výběr seřazených zásob: Vybrat** se zobrazuje práce výběru, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="d0e23-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="d0e23-616">Vyberte z umístění *SORT* a cílového RZ *PLP02*, který má více položek a množství *1*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="d0e23-617">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-617">Select **OK**.</span></span>
1. <span data-ttu-id="d0e23-618">Na stránce **Výběr seřazených zásob: Vložit** se zobrazuje práce vložení, kterou je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="d0e23-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="d0e23-619">Vložte do umístění *Nákladová brána* a cílového RZ *PLP02*, který má více položek a množství *1*.</span><span class="sxs-lookup"><span data-stu-id="d0e23-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="d0e23-620">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e23-620">Select **OK**.</span></span>

    <span data-ttu-id="d0e23-621">Práce je dokončena.</span><span class="sxs-lookup"><span data-stu-id="d0e23-621">Work is completed.</span></span>

<span data-ttu-id="d0e23-622">Odteď platí všechny ostatní skladové procesy.</span><span class="sxs-lookup"><span data-stu-id="d0e23-622">From this point forward, all other warehouse processes apply.</span></span>
