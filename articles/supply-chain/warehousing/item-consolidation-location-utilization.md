---
title: Konsolidace zboží - Využití skladového místa
description: Toto téma poskytuje informace o funkcích, které usnadňují vedoucím skladu prohlížet a filtrovat objemové využití umístění v celém skladu. Manažeři mohou vybírat místa a vytvářet pohyby inventáře přímo ze stránky Konsolidace položek, aby konsolidovali položky, a proto lépe využívali skladové prostory.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004645"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="53d4e-104">Konsolidace zboží - Využití skladového místa</span><span class="sxs-lookup"><span data-stu-id="53d4e-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53d4e-105">Toto téma poskytuje informace o funkcích, které usnadňují vedoucím skladu prohlížet a filtrovat objemové využití umístění v celém skladu.</span><span class="sxs-lookup"><span data-stu-id="53d4e-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="53d4e-106">Manažeři mohou vybírat místa a vytvářet pohyby inventáře přímo ze stránky **Konsolidace položek**, aby konsolidovali položky, a proto lépe využívali skladové prostory.</span><span class="sxs-lookup"><span data-stu-id="53d4e-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="53d4e-107">Zapnutí funkcí</span><span class="sxs-lookup"><span data-stu-id="53d4e-107">Turn on the features</span></span>

<span data-ttu-id="53d4e-108">Než budete moci používat funkce popsané v tomto tématu, musíte je v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="53d4e-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="53d4e-109">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav těchto funkcí a dle potřeby je zapnout.</span><span class="sxs-lookup"><span data-stu-id="53d4e-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="53d4e-110">Zapněte obě následující funkce v pořadí, v jakém jsou uvedeny v seznamu.</span><span class="sxs-lookup"><span data-stu-id="53d4e-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="53d4e-111">(Obě funkce jsou pro modul **Správa skladu**.)</span><span class="sxs-lookup"><span data-stu-id="53d4e-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="53d4e-112">Stav umístění ve skladu</span><span class="sxs-lookup"><span data-stu-id="53d4e-112">Warehouse location status</span></span>
2. <span data-ttu-id="53d4e-113">Využití skladového místa pro konsolidaci zboží</span><span class="sxs-lookup"><span data-stu-id="53d4e-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="53d4e-114">Stav umístění ve skladu</span><span class="sxs-lookup"><span data-stu-id="53d4e-114">Warehouse location status</span></span>

<span data-ttu-id="53d4e-115">Funkce *Stav umístění skladu* přidá čtyři nová pole na stránku **Místa** pro sledování dalších informace o aktuálním stavu místa:</span><span class="sxs-lookup"><span data-stu-id="53d4e-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="53d4e-116">**Číslo položky** – položka, která je aktuálně na skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="53d4e-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="53d4e-117">Pokud skladové místo obsahuje více položek, bude toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="53d4e-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="53d4e-118">**Datum a čas poslední aktivity** – časové razítko poslední skladové transakce provedené v daném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="53d4e-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="53d4e-119">**Datum pro sledování stárnutí** – datum, kdy byly zásoby ve skladovém místě přivezeny do skladu.</span><span class="sxs-lookup"><span data-stu-id="53d4e-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="53d4e-120">Toto datuj se vypočítává na základě data stárnutí registrační značky.</span><span class="sxs-lookup"><span data-stu-id="53d4e-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="53d4e-121">Přestože je toto datum přesné pro skladová místa, pro něž se využívá měření podle registračních značek, nemusí být přesné v případě skladových míst, jež takto sledována nejsou.</span><span class="sxs-lookup"><span data-stu-id="53d4e-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="53d4e-122">**Stav skladového místa** – stav skladového místa.</span><span class="sxs-lookup"><span data-stu-id="53d4e-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="53d4e-123">K dispozici jsou čtyři hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-123">Four values are available:</span></span>

    - <span data-ttu-id="53d4e-124">**Neurčeno** – profil skladového místa stav nesleduje.</span><span class="sxs-lookup"><span data-stu-id="53d4e-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="53d4e-125">Aktuální stav proto není známý.</span><span class="sxs-lookup"><span data-stu-id="53d4e-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="53d4e-126">**Prázdné** – ve skladovém místě nejsou v současné době žádné zásoby.</span><span class="sxs-lookup"><span data-stu-id="53d4e-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="53d4e-127">**Výdej** – ve skladovém místě byly od doby, kdy bylo naposledy prázdné, provedeny odchozí transakce.</span><span class="sxs-lookup"><span data-stu-id="53d4e-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="53d4e-128">**Skladování** – od doby, kdy bylo skladové místo naposledy prázdné, byly prováděny pouze příchozí transakce.</span><span class="sxs-lookup"><span data-stu-id="53d4e-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="53d4e-129">Tato pole umožňují manažerům skladu mít lepší přehled o stavu skladových míst ve skladu.</span><span class="sxs-lookup"><span data-stu-id="53d4e-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="53d4e-130">Umožňují také pokročilejší vykazování a filtrování.</span><span class="sxs-lookup"><span data-stu-id="53d4e-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="53d4e-131">Nastavení konsolidace zboží a využití skladového místa</span><span class="sxs-lookup"><span data-stu-id="53d4e-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="53d4e-132">Tato část popisuje, jak připravit systém k použití konsolidace položek a využití umístění.</span><span class="sxs-lookup"><span data-stu-id="53d4e-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="53d4e-133">Postupy používají ukázkové hodnoty ze standardních demonstračních dat.</span><span class="sxs-lookup"><span data-stu-id="53d4e-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="53d4e-134">Pokud se chystáte projít cvičná scénář, který je uveden dále v tomto tématu, vyberte právnickou osobu **USMF** (která obsahuje standardní demo data) a vytvořte každý záznam popsaný v této části.</span><span class="sxs-lookup"><span data-stu-id="53d4e-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="53d4e-135">Pokud neplánujete pracovat s ukázkovým scénářem, mohou být hodnoty, které jsou zde uvedeny, považovány za příklady typů nastavení, které musíte pro použití funkcí dokončit.</span><span class="sxs-lookup"><span data-stu-id="53d4e-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="53d4e-136">Uvolněný produkt</span><span class="sxs-lookup"><span data-stu-id="53d4e-136">Released product</span></span>

1. <span data-ttu-id="53d4e-137">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="53d4e-138">V poli **Číslo položky** vyberte *M9201* a otevřete stránku podrobností.</span><span class="sxs-lookup"><span data-stu-id="53d4e-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="53d4e-139">V podokně Akce na kartě **Správa zásob** ve skupině **Sklad** vyberte **Fyzické rozměry**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="53d4e-140">Na stránce **Fyzické rozměry** v podokně Akce vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="53d4e-141">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="53d4e-141">A new line is added to the grid.</span></span> <span data-ttu-id="53d4e-142">Pole **Číslo položky** je přednastaveno.</span><span class="sxs-lookup"><span data-stu-id="53d4e-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="53d4e-143">V poli **Jednotka** pak vyberte možnost *ea*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="53d4e-144">Zbývající pole na řádku se nastaví automaticky.</span><span class="sxs-lookup"><span data-stu-id="53d4e-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="53d4e-145">Zvolte **Uložit** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="53d4e-146">Profil umístění</span><span class="sxs-lookup"><span data-stu-id="53d4e-146">Location profile</span></span>

1. <span data-ttu-id="53d4e-147">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="53d4e-148">V seznamu profilů polohy vyberte možnost **FLOOR-05**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="53d4e-149">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="53d4e-150">Na pevné záložce **Všeobecné** se ujistěte, že jsou obě následující možnosti nastaveny na *Ano*:</span><span class="sxs-lookup"><span data-stu-id="53d4e-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="53d4e-151">Povolit položku v umístění</span><span class="sxs-lookup"><span data-stu-id="53d4e-151">Enable item in location</span></span>
    - <span data-ttu-id="53d4e-152">Povolit stav umístění</span><span class="sxs-lookup"><span data-stu-id="53d4e-152">Enable location status</span></span>

1. <span data-ttu-id="53d4e-153">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="53d4e-154">Pokud již možnosti **Povolit položku na místě** a **Povolit stav místa** byly nastaveny na *Ano*, přeskočte na pokyny pro nastavení pevné záložky **Rozměry** v kroku 10.</span><span class="sxs-lookup"><span data-stu-id="53d4e-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="53d4e-155">Pokud možnosti ještě nebyly nastaveny na *Ano*, musíte provést kontrolu konzistence modulu **Správa skladu** poté, co je nastavíte ručně.</span><span class="sxs-lookup"><span data-stu-id="53d4e-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="53d4e-156">V takovém případě pokračujte dalším krokem.</span><span class="sxs-lookup"><span data-stu-id="53d4e-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="53d4e-157">Chcete-li spustit kontrolu konzistence, přejděte na **Správa systému \> Periodické úkoly \> Databáze \> Kontrola konzistence**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="53d4e-158">V dialogovém okně **Kontrola konzistence** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="53d4e-159">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="53d4e-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="53d4e-160">**Kontrola / oprava:** *Kontrola*</span><span class="sxs-lookup"><span data-stu-id="53d4e-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="53d4e-161">**Od data:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="53d4e-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="53d4e-162">**Kontrola konzistence stavu umístění skladu:** Zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="53d4e-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="53d4e-163">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="53d4e-164">Po dokončení kontroly konzistence se zobrazí oznámení.</span><span class="sxs-lookup"><span data-stu-id="53d4e-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="53d4e-165">Otevřete [Centrum akcí](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) pro zobrazení zprávy.</span><span class="sxs-lookup"><span data-stu-id="53d4e-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="53d4e-166">Vyberte **Podrobnosti zprávy** k zobrazení podrobností.</span><span class="sxs-lookup"><span data-stu-id="53d4e-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="53d4e-167">Pokud se ve zprávě pro kontrolu konzistence uvádí: „Byly nalezeny nesprávné informace o stavu umístění pro umístění XXXX ve skladu XX“, musíte znovu spustit kontrolu konzistence.</span><span class="sxs-lookup"><span data-stu-id="53d4e-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="53d4e-168">Tentokrát nastavte **Kontrola / oprava** na *Opravit chybu*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="53d4e-169">Zobrazte zprávy a ujistěte se, že nebyly nalezeny žádné chyby.</span><span class="sxs-lookup"><span data-stu-id="53d4e-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="53d4e-170">Nyní musíte dokončit nastavení profilu místa.</span><span class="sxs-lookup"><span data-stu-id="53d4e-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="53d4e-171">Přejděte zpět na **Správa skladu \> Nastavení \> Sklad \> Profily umístění**, vyberte profil místa **FLOOR-05** a poté V podokně Akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="53d4e-172">Na záložce s náhledem **Rozměry** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="53d4e-173">**Procento využití objemu:** *100*</span><span class="sxs-lookup"><span data-stu-id="53d4e-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="53d4e-174">**Objemová metoda použitá pro umístění zásob:** *Použijte objem místa*</span><span class="sxs-lookup"><span data-stu-id="53d4e-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="53d4e-175">**Skutečná výška skladového místa:** *10*</span><span class="sxs-lookup"><span data-stu-id="53d4e-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="53d4e-176">**Skutečná šířka skladového místa:** *10*</span><span class="sxs-lookup"><span data-stu-id="53d4e-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="53d4e-177">**Skutečná hloubka skladového místa:** *10*</span><span class="sxs-lookup"><span data-stu-id="53d4e-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="53d4e-178">**Maximální hmotnost:** *100*</span><span class="sxs-lookup"><span data-stu-id="53d4e-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="53d4e-179">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="53d4e-180">Položky nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="53d4e-180">Mobile device menu items</span></span>

1. <span data-ttu-id="53d4e-181">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="53d4e-182">V podokně Akce vyberte možnost **Nová**, vytvoří se položka nabídky k třídění.</span><span class="sxs-lookup"><span data-stu-id="53d4e-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="53d4e-183">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="53d4e-184">**Název položky nabídky:** *Nastavit*</span><span class="sxs-lookup"><span data-stu-id="53d4e-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="53d4e-185">**Titul:** *Nastavit*</span><span class="sxs-lookup"><span data-stu-id="53d4e-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="53d4e-186">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="53d4e-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="53d4e-187">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="53d4e-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="53d4e-188">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="53d4e-189">**Proces tvorby práce:** *Nastavit*</span><span class="sxs-lookup"><span data-stu-id="53d4e-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="53d4e-190">**Typy úprav zásob:** *Nastavit*</span><span class="sxs-lookup"><span data-stu-id="53d4e-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="53d4e-191">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="53d4e-192">Nabídka mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="53d4e-192">Mobile device menu</span></span>

1. <span data-ttu-id="53d4e-193">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="53d4e-194">V seznamu nabídek vyberte možnost **Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="53d4e-195">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="53d4e-196">V seznamu **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="53d4e-197">Stisknutím tlačítka se šipkou doprava přesuňte **Upravit** do seznamu **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="53d4e-198">Tímto způsobem se přidá nová položka nabídky do vybrané nabídky.</span><span class="sxs-lookup"><span data-stu-id="53d4e-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="53d4e-199">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="53d4e-200">Typy pohybů</span><span class="sxs-lookup"><span data-stu-id="53d4e-200">Movement types</span></span>

1. <span data-ttu-id="53d4e-201">Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Typy pohybů**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="53d4e-202">V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="53d4e-203">**Kód typu pohybu:** *KONSOLIDOVAT*</span><span class="sxs-lookup"><span data-stu-id="53d4e-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="53d4e-204">**Popis:** *Konsolidovat místa*</span><span class="sxs-lookup"><span data-stu-id="53d4e-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="53d4e-205">**ID pracovní třídy:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="53d4e-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="53d4e-206">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="53d4e-207">Příklad</span><span class="sxs-lookup"><span data-stu-id="53d4e-207">Example scenario</span></span>

<span data-ttu-id="53d4e-208">Následující scénář používá k vytvoření inventáře aplikaci skladu na mobilním zařízení pro *úpravu* zásob do dvou míst ve skladu.</span><span class="sxs-lookup"><span data-stu-id="53d4e-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="53d4e-209">Přidat zásoby na skladová místa</span><span class="sxs-lookup"><span data-stu-id="53d4e-209">Add inventory to locations</span></span>

1. <span data-ttu-id="53d4e-210">Přihlaste se do mobilního zařízení jako uživatel, který je nastaven pro sklad *51*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="53d4e-211">Přejděte na **Zásoby \> Upravit**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="53d4e-212">Nyní zadáte první úpravu místa.</span><span class="sxs-lookup"><span data-stu-id="53d4e-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="53d4e-213">V úloze **Úprava** vyberte místo, pro které chcete provést úpravu zásob.</span><span class="sxs-lookup"><span data-stu-id="53d4e-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="53d4e-214">V poli **LOC** vyberte *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="53d4e-215">Potvrďte umístění.</span><span class="sxs-lookup"><span data-stu-id="53d4e-215">Confirm the location.</span></span>
1. <span data-ttu-id="53d4e-216">Vytvořte ID registrační značky pro položku, která bude přidána do umístění.</span><span class="sxs-lookup"><span data-stu-id="53d4e-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="53d4e-217">Do pole **LP** zadejte hodnotu *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="53d4e-218">Potvrďte registrační značku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="53d4e-219">Zadejte položku, která bude přidána na registrační značku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="53d4e-220">Do pole **ITEM** zadejte hodnotu *M9201*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="53d4e-221">Potvrďte položku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-221">Confirm the item.</span></span>
1. <span data-ttu-id="53d4e-222">Zadejte množství položky, která bude přidána.</span><span class="sxs-lookup"><span data-stu-id="53d4e-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="53d4e-223">Do pole **QTY** zadejte *10*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="53d4e-224">Potvrďte množství.</span><span class="sxs-lookup"><span data-stu-id="53d4e-224">Confirm the quantity.</span></span>

    <span data-ttu-id="53d4e-225">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="53d4e-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="53d4e-226">Nyní zadáte druhou úpravu místa.</span><span class="sxs-lookup"><span data-stu-id="53d4e-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="53d4e-227">V úloze **Úprava** vyberte místo, pro které chcete provést úpravu zásob.</span><span class="sxs-lookup"><span data-stu-id="53d4e-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="53d4e-228">V poli **LOC** vyberte *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="53d4e-229">Potvrďte umístění.</span><span class="sxs-lookup"><span data-stu-id="53d4e-229">Confirm the location.</span></span>
1. <span data-ttu-id="53d4e-230">Vytvořte ID registrační značky pro položku, která bude přidána do umístění.</span><span class="sxs-lookup"><span data-stu-id="53d4e-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="53d4e-231">Do pole **LP** zadejte hodnotu *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="53d4e-232">Potvrďte registrační značku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="53d4e-233">Zadejte položku, která bude přidána na registrační značku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="53d4e-234">Do pole **ITEM** zadejte hodnotu *M9201*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="53d4e-235">Potvrďte položku.</span><span class="sxs-lookup"><span data-stu-id="53d4e-235">Confirm the item.</span></span>
1. <span data-ttu-id="53d4e-236">Zadejte množství položky, která bude přidána.</span><span class="sxs-lookup"><span data-stu-id="53d4e-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="53d4e-237">Do pole **QTY** zadejte *15*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="53d4e-238">Potvrďte množství.</span><span class="sxs-lookup"><span data-stu-id="53d4e-238">Confirm the quantity.</span></span>

    <span data-ttu-id="53d4e-239">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="53d4e-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="53d4e-240">Stiskněte tlačítko nabídky (tzv. „hamburgerové tlačítko“ nebo „hamburger“) a vyberte **Storno**, chcete-li opustit úkol **Úprava**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="53d4e-241">Konsolidovat umístění</span><span class="sxs-lookup"><span data-stu-id="53d4e-241">Consolidate locations</span></span>

1. <span data-ttu-id="53d4e-242">Přejděte na **Správa skladu \> Periodické úkoly \> Konsolidace položek**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="53d4e-243">V záhlaví vyberte sklad, pro který chcete provést konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="53d4e-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="53d4e-244">V poli **Sklad** zadejte *51*.</span><span class="sxs-lookup"><span data-stu-id="53d4e-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="53d4e-245">Záznam se zobrazuje pro každé místo, kde byla položka *M9201* upravena.</span><span class="sxs-lookup"><span data-stu-id="53d4e-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="53d4e-246">Sloupec **Procento využití** ukazuje objemové využití každého místa.</span><span class="sxs-lookup"><span data-stu-id="53d4e-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="53d4e-247">Chcete-li konsolidovat inventář, vyberte všechna umístění, která musí být konsolidována, a poté na podokně Akce vyberte **Konsolidovat zásoby**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="53d4e-248">V dialogovém okně **Konsolidovat zásoby** zadejte umístění a typ pohybu, který by měl být použit k vytvoření práce pro přesun zásob.</span><span class="sxs-lookup"><span data-stu-id="53d4e-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="53d4e-249">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="53d4e-249">Set the following values:</span></span>

    - <span data-ttu-id="53d4e-250">**Místo:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="53d4e-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="53d4e-251">**Kód typu pohybu:** *KONSOLIDOVAT*</span><span class="sxs-lookup"><span data-stu-id="53d4e-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="53d4e-252">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-252">Select **OK**.</span></span>
1. <span data-ttu-id="53d4e-253">Obdržíte informační zprávu, která ukazuje pohybovou práci, která byla vytvořena.</span><span class="sxs-lookup"><span data-stu-id="53d4e-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="53d4e-254">Poznamenejte si ID pohybu práce.</span><span class="sxs-lookup"><span data-stu-id="53d4e-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="53d4e-255">Zobrazit pohybové práce</span><span class="sxs-lookup"><span data-stu-id="53d4e-255">View movement work</span></span>

1. <span data-ttu-id="53d4e-256">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="53d4e-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="53d4e-257">Zobrazit vytvořenou práci.</span><span class="sxs-lookup"><span data-stu-id="53d4e-257">View the work that was created.</span></span> <span data-ttu-id="53d4e-258">Filtrujte nebo prohledávejte pracovní mřížku pomocí ID práce s pohybem z konsolidace zásob.</span><span class="sxs-lookup"><span data-stu-id="53d4e-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="53d4e-259">V tomto scénáři bylo jako umístění konsolidace zásob použito existující místo se zásobami.</span><span class="sxs-lookup"><span data-stu-id="53d4e-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="53d4e-260">Proto bylo vytvořeno pouze jedno ID práce.</span><span class="sxs-lookup"><span data-stu-id="53d4e-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="53d4e-261">Systém vytvoří jedno pracovní ID pro každý pohyb, který musí být dokončen.</span><span class="sxs-lookup"><span data-stu-id="53d4e-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="53d4e-262">Pokud určíte místo, které již obsahuje zásoby, vytvoří se pouze jedno ID práce.</span><span class="sxs-lookup"><span data-stu-id="53d4e-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="53d4e-263">Pokud zadáte nové místo, vytvoří se dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="53d4e-263">If you specify a new location, two work IDs are created.</span></span>
