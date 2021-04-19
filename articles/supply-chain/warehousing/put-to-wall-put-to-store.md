---
title: Umístění na zeď - umístění do obchodu
description: Toto téma obsahuje informace o funkci Umístění na zeď - umístění do obchodu. Tato funkce umožňuje zpracovat scénáře, ve kterých musíte produkt konsolidovat do pracovní oblasti předbalení na základě konfigurovatelných kritérií. Pomáhá zkrátit dobu výdeje, protože umožňuje výběry na jednu cílovou registrační značku a může používat více pozic umístění než cluster.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cf34a61d0b3f784b5a424473588d05bf8703635c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823280"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="a33ed-105">Umístění na zeď - umístění do obchodu</span><span class="sxs-lookup"><span data-stu-id="a33ed-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a33ed-106">Funkce *Umístění na zeď - umístění do obchodu* umožňuje zpracovat scénáře, ve kterých musíte produkt konsolidovat do pracovní oblasti předbalení na základě konfigurovatelných kritérií.</span><span class="sxs-lookup"><span data-stu-id="a33ed-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="a33ed-107">Protože tato funkce umožňuje výběr na jednu cílovou registrační značku a může použít více umístěných pozic než výběr z clusteru, budou společnosti, které dodávají do obchodů nebo zpracovávají malé předměty, těžit ze zkrácené doby výběru.</span><span class="sxs-lookup"><span data-stu-id="a33ed-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="a33ed-108">Pracovní postup této funkce směruje vybraný produkt do třídicího místa pro distribuci do různých typů kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="a33ed-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="a33ed-109">Obecně platí, že každé třídicí místo zahrnuje více pozic řazení.</span><span class="sxs-lookup"><span data-stu-id="a33ed-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="a33ed-110">Každá pozice řazení je přiřazena podle kritérií stanovených obchodním procesem.</span><span class="sxs-lookup"><span data-stu-id="a33ed-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="a33ed-111">Typickými kritérii jsou konečný cíl, dodávka nebo vytížení.</span><span class="sxs-lookup"><span data-stu-id="a33ed-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="a33ed-112">Poté, co produkt dorazí, je distribuován do každé pozice řazení podle množství, které je spojeno s objednávkou, místem určení, dodávkou nebo vytížením.</span><span class="sxs-lookup"><span data-stu-id="a33ed-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="a33ed-113">Když je kontejner plný nebo kompletní, je přesunut do přechodného skladového místa nebo místa dodání pro další zpracování, v závislosti na obchodním procesu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="a33ed-114">Tato skladovací funkce je také označována jinými jmény, jako je umístění na světlo a otevření přestávky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="a33ed-115">Zapnutí funkce Odchozí třídění</span><span class="sxs-lookup"><span data-stu-id="a33ed-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="a33ed-116">Než budete moci použít funkci *Umístění na zeď - umístění do obchodu*, musí být v systému zapnutá funkce *Odchozí třídění*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="a33ed-117">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="a33ed-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a33ed-118">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="a33ed-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a33ed-119">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="a33ed-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a33ed-120">**Název funkce:** *Odchozí třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="a33ed-121">Funkci *Odchozí třídění* lze použít ve spojení s funkcí *Krokový kód široké vlny organizace*, pokud je zapnutá.</span><span class="sxs-lookup"><span data-stu-id="a33ed-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="a33ed-122">Tuto funkci musíte zapnout také v případě, že budete používat předdefinované kódy, které jsou nastaveny v kódech kroků vlny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="a33ed-123">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="a33ed-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="a33ed-124">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="a33ed-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a33ed-125">**Název funkce:** *Kód kroků vlny napříč organizací*</span><span class="sxs-lookup"><span data-stu-id="a33ed-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="a33ed-126">Nastavení</span><span class="sxs-lookup"><span data-stu-id="a33ed-126">Setup</span></span>

<span data-ttu-id="a33ed-127">Pro tuto ukázku jsou použita standardní data a sklad Contoso *62*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="a33ed-128">Používají se také některé dodatky, které jsou uvedeny později.</span><span class="sxs-lookup"><span data-stu-id="a33ed-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="a33ed-129">Typ umístění</span><span class="sxs-lookup"><span data-stu-id="a33ed-129">Location type</span></span>

1. <span data-ttu-id="a33ed-130">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Typy umístění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="a33ed-131">V podokně Akce vyberte možnost **Nová**, vytvoří se typ místa k třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="a33ed-132">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-132">Set the following values:</span></span>

    - <span data-ttu-id="a33ed-133">**Typ umístění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="a33ed-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="a33ed-134">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="a33ed-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="a33ed-135">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="a33ed-136">Parametry řízení skladu</span><span class="sxs-lookup"><span data-stu-id="a33ed-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="a33ed-137">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="a33ed-138">Ka kartě **Obecné** na pevné záložce **Typy umístění** v poli **Typ místa třídění** zadejte *SORT*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="a33ed-139">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="a33ed-140">Profil umístění</span><span class="sxs-lookup"><span data-stu-id="a33ed-140">Location profile</span></span>

1. <span data-ttu-id="a33ed-141">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="a33ed-142">V podokně Akce vyberte možnost **Nová**, vytvoří se typ profilu umístění pro umístění třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="a33ed-143">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="a33ed-144">**ID profilu umístění:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-145">**Název:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="a33ed-146">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a33ed-147">**Formát skladového místa:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="a33ed-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="a33ed-148">**Typ umístění:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="a33ed-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="a33ed-149">**Použít sledování registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="a33ed-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="a33ed-150">**Povolit smíšené položky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="a33ed-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="a33ed-151">**Povolit smíšené stavy zásob:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="a33ed-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="a33ed-152">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="a33ed-153">Umístění</span><span class="sxs-lookup"><span data-stu-id="a33ed-153">Locations</span></span>

1. <span data-ttu-id="a33ed-154">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="a33ed-155">Zrušte zaškrtnutí políčka **Generovat kontrolní číslice pro místo**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="a33ed-156">V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="a33ed-157">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="a33ed-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="a33ed-158">**Místo:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-159">**ID profilu umístění:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="a33ed-160">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="a33ed-161">Profily balení</span><span class="sxs-lookup"><span data-stu-id="a33ed-161">Packing profiles</span></span>

1. <span data-ttu-id="a33ed-162">Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="a33ed-163">V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="a33ed-164">**ID profilu balení:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-165">**Popis:** *Seřadit*</span><span class="sxs-lookup"><span data-stu-id="a33ed-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-166">**Zásady balení kontejnerů:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="a33ed-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="a33ed-167">**Režim ID kontejneru:** *Automatický*</span><span class="sxs-lookup"><span data-stu-id="a33ed-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="a33ed-168">**Typ kontejneru:** *PALLET 48X48*</span><span class="sxs-lookup"><span data-stu-id="a33ed-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="a33ed-169">**Automaticky vytvořit kontejner při uzavření kontejneru:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="a33ed-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="a33ed-170">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="a33ed-171">Kódy kroku vlny</span><span class="sxs-lookup"><span data-stu-id="a33ed-171">Wave step codes</span></span>

<span data-ttu-id="a33ed-172">Pokud jste zapnuli funkci *Kód širokého kroku vln organizace*, nastavte následující kód.</span><span class="sxs-lookup"><span data-stu-id="a33ed-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="a33ed-173">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="a33ed-174">V podokně Akce klikněte na **Nový** a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="a33ed-175">**Kód kroku vlny:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-176">**Popis kroku vlny:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-177">**Typ kroku vlny:** *Šablona třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="a33ed-178">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="a33ed-179">Šablona odchozího třídění</span><span class="sxs-lookup"><span data-stu-id="a33ed-179">Outbound sorting template</span></span>

<span data-ttu-id="a33ed-180">Šablona třídění řídí, zda se vytvářejí pozice třídění, jaká kritéria se používají a další atributy procesu třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="a33ed-181">Přejděte na **Řízení skladu \> Nastavení \> Balení \> Odchozí šablona třídění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="a33ed-182">V podokně Akce vyberte možnost **Nový** a vytvořte šablonu třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="a33ed-183">V záhlaví nové šablony nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="a33ed-184">**ID odchozí šablony třídění:** *Třídění vlny*</span><span class="sxs-lookup"><span data-stu-id="a33ed-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="a33ed-185">**Popis:** *Třídění vlny*</span><span class="sxs-lookup"><span data-stu-id="a33ed-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="a33ed-186">**Typ šablony třídění:** *Vlnová poptávka*</span><span class="sxs-lookup"><span data-stu-id="a33ed-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="a33ed-187">Toto pole definuje proces, pro který se používá šablona třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="a33ed-188">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-188">The following values are available:</span></span>

        - <span data-ttu-id="a33ed-189">**Vlnová poptávka** -Šablona třídění se používá pro proces *Umístění na zeď*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="a33ed-190">Tento typ šablony slouží k obejití balicí stanice a zpracování zásob přímo mimo vlnu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="a33ed-191">Tento typ můžete použít pouze v případě, že je do šablony vlny zahrnuta metoda **třídění** vlny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="a33ed-192">**Kontejner** - Šablona třídění se používá pro proces *Budova palety po zabalení*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="a33ed-193">Tento typ šablony slouží ke zpracování kontejnerů, které jsou uzavřené v balicí stanici, a je třeba je setřídit na palety.</span><span class="sxs-lookup"><span data-stu-id="a33ed-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="a33ed-194">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="a33ed-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="a33ed-195">**Místo:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="a33ed-196">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a33ed-197">**Ověření řazení:** *Kontrola pozice*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="a33ed-198">Toto pole definuje ověření, které je vyžadováno během třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="a33ed-199">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-199">The following values are available:</span></span>

        - <span data-ttu-id="a33ed-200">Žádní</span><span class="sxs-lookup"><span data-stu-id="a33ed-200">None</span></span>
        - <span data-ttu-id="a33ed-201">Skenování registrační značky</span><span class="sxs-lookup"><span data-stu-id="a33ed-201">License plate scan</span></span>
        - <span data-ttu-id="a33ed-202">Skenování pozice</span><span class="sxs-lookup"><span data-stu-id="a33ed-202">Position scan</span></span>

    - <span data-ttu-id="a33ed-203">**Vytvořit práci při uzavření pozice:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="a33ed-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="a33ed-204">Když je tato možnost nastavená na *Ano* a pozice uzavřená, práce bude vytvořena, aby se přesunuly zásoby do konečného místa doručení.</span><span class="sxs-lookup"><span data-stu-id="a33ed-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="a33ed-205">Když je nastavená na *Ne*, zásoby budou ihned přiděleny do objednávky při zavření pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="a33ed-206">**Přiřazení pozice:** *Ruční*</span><span class="sxs-lookup"><span data-stu-id="a33ed-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="a33ed-207">Toto pole definuje typ přiřazení pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="a33ed-208">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-208">The following values are available:</span></span>

        - <span data-ttu-id="a33ed-209">**Ruční** - uživatel musí vždy označit, do jaké pozice mají být zásoby setříděny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="a33ed-210">**Automatický** -systém automaticky navede zásoby do pozice, kdykoli je to možné, na základě přestávek šablony třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="a33ed-211">**Přiřadit kritéria pozice třídění:** *Použít pouze prázdnou pozici*</span><span class="sxs-lookup"><span data-stu-id="a33ed-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="a33ed-212">Toto pole určuje, zda se při přiřazování zásob, které jsou už přítomny na pozici řazení, vezmou v úvahu zásoby, které již byly k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a33ed-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="a33ed-213">K dispozici jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-213">The following values are available:</span></span>

        - <span data-ttu-id="a33ed-214">**Použít pouze prázdné místo** - Budou brány v úvahu pozice, které již mají přidružené zásoby</span><span class="sxs-lookup"><span data-stu-id="a33ed-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="a33ed-215">**Předpokládejme, že je pozice prázdná** - Veškerý inventář, který je již v pozici, bude při přiřazování ignorován.</span><span class="sxs-lookup"><span data-stu-id="a33ed-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="a33ed-216">Budou použity všechny dostupné pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-216">All available positions will be used.</span></span>

    - <span data-ttu-id="a33ed-217">**Kód kroku vlny:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="a33ed-218">Pokud je zapnutá funkce *Kód kroku vlny pro celou organizaci*, musí být nastaven také kód vlnového kroku *Seřadit* v kódech vlnových kroků.</span><span class="sxs-lookup"><span data-stu-id="a33ed-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="a33ed-219">**Automaticky zavřít pozici třídění:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="a33ed-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="a33ed-220">Pokud je tato možnost nastavená na *Ano*, bude pozice při řazení automaticky zavřena po dokončení veškeré práce přicházející do pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="a33ed-221">**Počet pozic třídění:** *3*</span><span class="sxs-lookup"><span data-stu-id="a33ed-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="a33ed-222">Toto pole definuje maximální počet pozic třídění, které systém vytvoří.</span><span class="sxs-lookup"><span data-stu-id="a33ed-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="a33ed-223">**Předpona pozice třídění:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="a33ed-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="a33ed-224">Toto pole definuje předponu, kterou systém přiřadí před číslo pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="a33ed-225">**Automaticky zabalit pozici třídění:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="a33ed-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="a33ed-226">Je-li tato možnost nastavená na *Ano*, budou zásoby na pozici třídění po uzavření pozice zabaleny do kontejneru.</span><span class="sxs-lookup"><span data-stu-id="a33ed-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="a33ed-227">**ID profilu balení:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="a33ed-228">Toto pole definuje profil balení, který se použije při zabalení pozice řazení do kontejneru.</span><span class="sxs-lookup"><span data-stu-id="a33ed-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="a33ed-229">V podokně akcí vyberte **Upravit dotaz** k určení kritérií, která se používají pro tuto šablonu třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="a33ed-230">V dialogovém okně dotazu na kartě **Třídění** přidejte tlačítkem **Nový** řádek a pak nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a33ed-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="a33ed-231">**Tabulka:** *Podrobnosti nákladu*</span><span class="sxs-lookup"><span data-stu-id="a33ed-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="a33ed-232">**Odvozená tabulka:** *Podrobnosti nákladu*</span><span class="sxs-lookup"><span data-stu-id="a33ed-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="a33ed-233">**Pole:** *ID dodávky*</span><span class="sxs-lookup"><span data-stu-id="a33ed-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="a33ed-234">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="a33ed-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a33ed-235">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-235">Select **OK**.</span></span>
1. <span data-ttu-id="a33ed-236">Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“</span><span class="sxs-lookup"><span data-stu-id="a33ed-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="a33ed-237">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-237">Select **Yes**.</span></span>

    <span data-ttu-id="a33ed-238">Aktivuje se tlačítko **Zalomení odchozích šablon třídění** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="a33ed-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="a33ed-239">V podokně akcí vyberte možnost **Zalomení odchozích šablon třídění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="a33ed-240">Zaškrtněte políčko **Seskupit podle pole** pro seskupení podle ID zásilky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="a33ed-241">Toto nastavení vytvoří jednu pozici třídění pro každou zásilku, která je kontejnerem ve vlně.</span><span class="sxs-lookup"><span data-stu-id="a33ed-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="a33ed-242">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="a33ed-243">Metody zpracování vlny</span><span class="sxs-lookup"><span data-stu-id="a33ed-243">Wave process methods</span></span>

1. <span data-ttu-id="a33ed-244">Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="a33ed-245">V podokně Akce vyberte možnost **Obnovit metody**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="a33ed-246">Metoda **třídění** je přidána do seznamu dostupných metod a je pro ni vybrán typ vlnové šablony *Expedice*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="a33ed-247">Šablony vlny</span><span class="sxs-lookup"><span data-stu-id="a33ed-247">Wave templates</span></span>

<span data-ttu-id="a33ed-248">Upravte vlnovou šablonu, která se používá pro třídění požadavků na vlnu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="a33ed-249">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a33ed-250">V poli **Typ šablony vlny** vyberte *Expedice*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="a33ed-251">Vyberte existující šablonu **Výchozí dodání 62**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="a33ed-252">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a33ed-253">Na pevné záložce **Obecné** proveďte následující změny:</span><span class="sxs-lookup"><span data-stu-id="a33ed-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="a33ed-254">Nastavte možnost **Zpracovat vlnu při uvolnění do skladu** na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="a33ed-255">Nastavte možnost **Přiřadit k otevřeným vlnám** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="a33ed-256">Na pevné záložce **Metody** nastavte metodu **třídění**:</span><span class="sxs-lookup"><span data-stu-id="a33ed-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="a33ed-257">V mřížce **Zbývající metody** vyberte **třídění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="a33ed-258">Tlačítkem s šipkou doprava přesuňte metodu **třídění** do mřížky **Vybrané metody**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="a33ed-259">V mřížce **Vybrané metody** vyberte **třídění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="a33ed-260">Nastavte hodnotu pole **Kód kroku vlny** na *Třídění*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="a33ed-261">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a33ed-262">Položky nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="a33ed-262">Mobile device menu items</span></span>

1. <span data-ttu-id="a33ed-263">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a33ed-264">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a33ed-265">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="a33ed-266">**Název položky nabídky:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-267">**Titul:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="a33ed-268">**Režim:** *Nepřímý*</span><span class="sxs-lookup"><span data-stu-id="a33ed-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="a33ed-269">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="a33ed-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="a33ed-270">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a33ed-271">**Kód aktivity:** *Odchozí třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="a33ed-272">**Použít průvodce procesem:** *Ano* (výchozí hodnota)</span><span class="sxs-lookup"><span data-stu-id="a33ed-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="a33ed-273">**ID odchozí šablony třídění:** *Třídění vlny*</span><span class="sxs-lookup"><span data-stu-id="a33ed-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="a33ed-274">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="a33ed-275">Nabídka mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="a33ed-275">Mobile device menu</span></span>

1. <span data-ttu-id="a33ed-276">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="a33ed-277">V seznamu nabídek vyberte možnost **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="a33ed-278">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a33ed-279">V mřížce **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky **Třídění**, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="a33ed-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="a33ed-280">Stisknutím tlačítka se šipkou doprava přesuňte **Třídění** do mřížky **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="a33ed-281">Tímto způsobem se přidá nová položka nabídky do nabídky **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="a33ed-282">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="a33ed-283">Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="a33ed-283">Location directives</span></span>

<span data-ttu-id="a33ed-284">Musíte vytvořit směrnice o umístění, které budou řídit práci vytvořenou po dokončení třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="a33ed-285">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a33ed-286">V poli **Typ pořadí pracovních činností** vyberte možnost *Výběr seřazených zásob*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="a33ed-287">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a33ed-288">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="a33ed-289">**Posloupnost:** *1*</span><span class="sxs-lookup"><span data-stu-id="a33ed-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="a33ed-290">**Název:** *Umístění k nákladním dveřím*</span><span class="sxs-lookup"><span data-stu-id="a33ed-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="a33ed-291">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a33ed-292">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="a33ed-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a33ed-293">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="a33ed-293">**Site:** *6*</span></span>
    - <span data-ttu-id="a33ed-294">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="a33ed-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="a33ed-295">**Kód směrnice:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="a33ed-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="a33ed-296">**Více skladových jednotek:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="a33ed-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="a33ed-297">Chcete-li, aby byla dostupná záložka s náhledem **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="a33ed-298">Na pevné záložce **Řádky** vyberte **Nový** a pak nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a33ed-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="a33ed-299">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="a33ed-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="a33ed-300">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="a33ed-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a33ed-301">**Od množství:** *0*</span><span class="sxs-lookup"><span data-stu-id="a33ed-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="a33ed-302">**Do množství:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="a33ed-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="a33ed-303">Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="a33ed-304">Na pevné záložce **Akce směrnice místa** vyberte **Nový** a pak nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a33ed-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="a33ed-305">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="a33ed-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="a33ed-306">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="a33ed-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a33ed-307">**Název:** *Portál*</span><span class="sxs-lookup"><span data-stu-id="a33ed-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="a33ed-308">Vyberte možnost **Uložit**, chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na pevné záložce **Akce směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="a33ed-309">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="a33ed-310">V dialogovém okně dotazu na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Umístění*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="a33ed-311">Nastavte pole **Kritéria** pro tento řádek na *nákladová brána*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="a33ed-312">Úpravu potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="a33ed-313">Pracovní třídy</span><span class="sxs-lookup"><span data-stu-id="a33ed-313">Work classes</span></span>

1. <span data-ttu-id="a33ed-314">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="a33ed-315">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a33ed-316">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="a33ed-317">**ID pracovní třídy:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="a33ed-318">**Popis:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="a33ed-319">**Typ pracovního příkazu:** *Výběr tříděných zásob*</span><span class="sxs-lookup"><span data-stu-id="a33ed-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="a33ed-320">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="a33ed-321">Šablony práce</span><span class="sxs-lookup"><span data-stu-id="a33ed-321">Work templates</span></span>

1. <span data-ttu-id="a33ed-322">Přejděte do nabídky Řízení skladu **Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a33ed-323">V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="a33ed-324">V mřížce vyberte pracovní šablonu **62 výdejů do balení**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="a33ed-325">V podokně akcí vyberte **Zalomení pracovních hlaviček**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="a33ed-326">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a33ed-327">Na řádku, kde je pole **Název pole** nastaveno na *ID dodávky* zrušte zaškrtnutí políčka **Seskupit podle tohoto pole**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="a33ed-328">Vyberte **Uložit** a zavřete dialogové okno **Zalomení pracovních hlaviček**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="a33ed-329">V poli **Typ pořadí pracovních činností** vyberte možnost *Výběr seřazených zásob*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="a33ed-330">Zvolte **Nová** pro vytvoření šablony práce.</span><span class="sxs-lookup"><span data-stu-id="a33ed-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="a33ed-331">V části **Přehled** nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a33ed-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="a33ed-332">Potvrďte výchozí hodnoty ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="a33ed-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="a33ed-333">**Šablona práce:** *Seřazený výběr*</span><span class="sxs-lookup"><span data-stu-id="a33ed-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="a33ed-334">**Popis šablony práce:** *Seřazený výběr*</span><span class="sxs-lookup"><span data-stu-id="a33ed-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="a33ed-335">Chcete-li, aby byla dostupná část **Podrobnosti šablony práce**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="a33ed-336">V části **Podrobnosti pracovní šablony** vytvoříte dva řádky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="a33ed-337">Klikněte na **Nový** a poté nastavte následující hodnoty pro řádek 1:</span><span class="sxs-lookup"><span data-stu-id="a33ed-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="a33ed-338">**Typ práce:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="a33ed-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="a33ed-339">**Povinné:** Vybráno (= *Ano*)</span><span class="sxs-lookup"><span data-stu-id="a33ed-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="a33ed-340">**ID pracovní třídy:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="a33ed-341">Znovu klikněte na **Nový** a poté nastavte následující hodnoty pro řádek 2:</span><span class="sxs-lookup"><span data-stu-id="a33ed-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="a33ed-342">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="a33ed-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a33ed-343">**Povinné:** Vybráno (= *Ano*)</span><span class="sxs-lookup"><span data-stu-id="a33ed-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="a33ed-344">**ID pracovní třídy:** *Třídění*</span><span class="sxs-lookup"><span data-stu-id="a33ed-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="a33ed-345">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a33ed-346">Příklad</span><span class="sxs-lookup"><span data-stu-id="a33ed-346">Example scenario</span></span>

<span data-ttu-id="a33ed-347">Tento scénář simuluje situaci, kdy sklad ukládá malé položky na jednotlivých místech a musí je zabalit do krabic před odesláním a kde funkce balicí stanice není opravdu vhodná.</span><span class="sxs-lookup"><span data-stu-id="a33ed-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="a33ed-348">Pracovníci vybírají objednávky pro více zákazníků a různé adresy současně, aby se zvýšila rychlost výběru.</span><span class="sxs-lookup"><span data-stu-id="a33ed-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="a33ed-349">Po dokončení výdejů dorazí pracovníci na místo třídění, kde lze vybrané položky podle požadovaných kritérií třídit do správného pole.</span><span class="sxs-lookup"><span data-stu-id="a33ed-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="a33ed-350">V tomto příkladu bude k určení správného pole použito ID zásilky, protože každá zásilka má jinou adresu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="a33ed-351">Poté, co jsou všechny položky z nákladu zabaleny a tříděny podle dodávky, budou krabice přesunuty do pracovní oblasti a nakonec naloženy na nákladní automobil.</span><span class="sxs-lookup"><span data-stu-id="a33ed-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="a33ed-352">Před zahájením scénáře se ujistěte, že všechny standardní funkce skladu jsou správně nastaveny pro váš sklad.</span><span class="sxs-lookup"><span data-stu-id="a33ed-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="a33ed-353">Pro tento účel se používá standardní sklad Contoso *62*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="a33ed-354">Standardní konfigurace se nezměnily, kromě toho, co je popsáno v nastavení.</span><span class="sxs-lookup"><span data-stu-id="a33ed-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="a33ed-355">Vytvoření poptávky</span><span class="sxs-lookup"><span data-stu-id="a33ed-355">Create demand</span></span>

<span data-ttu-id="a33ed-356">Předtím, než bude možné tuto funkčnost prokázat, musíte vytvořit určitou poptávku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="a33ed-357">V tomto scénáři vytvoříte tři prodejní objednávky pro tři různé zákazníky pro simulaci různých dodacích adres.</span><span class="sxs-lookup"><span data-stu-id="a33ed-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="a33ed-358">Tímto způsobem vytvoříte tři samostatné zásilky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="a33ed-359">Než začnete vytvářet prodejní objednávky a zásilky, zajistěte, aby skladová místa pro výdej měla dostatečné množství zásob pro všechny položky v objednávce.</span><span class="sxs-lookup"><span data-stu-id="a33ed-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="a33ed-360">Zkontrolujte nastavení směrnice skladového místa pro určení, která výdejní skladová místa se použijí pro výdej prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="a33ed-361">Pokud musíte upravit zásoby, můžete vytvořit ruční pohyby, použít doplnění nebo využít jakýkoli jiný tok.</span><span class="sxs-lookup"><span data-stu-id="a33ed-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="a33ed-362">Pak rezervujte zásoby.</span><span class="sxs-lookup"><span data-stu-id="a33ed-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="a33ed-363">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a33ed-364">Výběrem možnosti **Nová** vytvořte prodejní objednávku pro objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="a33ed-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="a33ed-365">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a33ed-366">**Zákazník:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a33ed-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="a33ed-367">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="a33ed-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a33ed-368">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-368">Select **OK**.</span></span>
1. <span data-ttu-id="a33ed-369">Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="a33ed-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a33ed-370">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-370">Set the following values:</span></span>

    - <span data-ttu-id="a33ed-371">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a33ed-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a33ed-372">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="a33ed-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="a33ed-373">Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="a33ed-374">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a33ed-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a33ed-375">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="a33ed-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="a33ed-376">Opakujte následující kroky pro každý řádek prodeje v objednávce, abyste pro ně vyhradili zásoby:</span><span class="sxs-lookup"><span data-stu-id="a33ed-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="a33ed-377">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="a33ed-378">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="a33ed-379">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-379">Select **Save**.</span></span>

1. <span data-ttu-id="a33ed-380">Výběrem možnosti **Nová** vytvořte prodejní objednávku pro objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="a33ed-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="a33ed-381">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a33ed-382">**Zákazník:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="a33ed-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="a33ed-383">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="a33ed-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a33ed-384">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-384">Select **OK**.</span></span>
1. <span data-ttu-id="a33ed-385">Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="a33ed-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a33ed-386">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-386">Set the following values:</span></span>

    - <span data-ttu-id="a33ed-387">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a33ed-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a33ed-388">**Množství:** *7*</span><span class="sxs-lookup"><span data-stu-id="a33ed-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="a33ed-389">Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="a33ed-390">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a33ed-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a33ed-391">**Množství:** *3*</span><span class="sxs-lookup"><span data-stu-id="a33ed-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="a33ed-392">Opakujte následující kroky pro každý řádek prodeje v objednávce, abyste pro ně vyhradili zásoby:</span><span class="sxs-lookup"><span data-stu-id="a33ed-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="a33ed-393">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="a33ed-394">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="a33ed-395">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-395">Select **Save**.</span></span>

1. <span data-ttu-id="a33ed-396">Výběrem možnosti **Nová** vytvořte prodejní objednávku pro objednávku 3.</span><span class="sxs-lookup"><span data-stu-id="a33ed-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="a33ed-397">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a33ed-398">**Zákazník:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a33ed-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="a33ed-399">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="a33ed-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a33ed-400">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-400">Select **OK**.</span></span>
1. <span data-ttu-id="a33ed-401">Na záložce s náhledem **Řádky prodejní objednávky** se přidá nový řádek.</span><span class="sxs-lookup"><span data-stu-id="a33ed-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a33ed-402">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a33ed-402">Set the following values:</span></span>

    - <span data-ttu-id="a33ed-403">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a33ed-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a33ed-404">**Množství:** *8*</span><span class="sxs-lookup"><span data-stu-id="a33ed-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="a33ed-405">Chcete-li rezervovat zásoby pro řádek prodejní objednávky, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="a33ed-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="a33ed-406">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="a33ed-407">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="a33ed-408">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-408">Select **Save**.</span></span>

<span data-ttu-id="a33ed-409">Chcete-li uvolnit každou prodejní objednávku do skladu, proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="a33ed-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="a33ed-410">Budou vytvořeny tři různé zásilky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-410">Three different shipments will be created.</span></span> <span data-ttu-id="a33ed-411">Poté přidáte všechny tři zásilky do jedné nové vlny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="a33ed-412">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a33ed-413">V mřížce vyberte první prodejní objednávku, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="a33ed-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="a33ed-414">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a33ed-415">Zobrazí se informační zpráva, která uvádí ID vlny a ID objednávky, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="a33ed-416">Opakováním předchozích kroků uvolněte prodejní objednávky 2 a 3 do skladu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="a33ed-417">Všimněte si, že informační zpráva, kterou obdržíte, označuje, že zásilka byla přidána do vlny, která byla vytvořena při uvolnění prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="a33ed-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="a33ed-418">Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a33ed-419">Vyberte ID vlny, které bylo vytvořeno při uvolnění prodejních objednávek, k otevření stránky **Vlny**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="a33ed-420">Tato stránka zobrazuje podrobnosti o vlně.</span><span class="sxs-lookup"><span data-stu-id="a33ed-420">This page shows the wave details.</span></span> <span data-ttu-id="a33ed-421">Na pevné záložce **Vlnové linie** se zobrazí zásilky, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="a33ed-422">Nyní musíte vytvořit práci, která přinese položky z míst výběru do místa třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="a33ed-423">V podokně akcí klikněte na možnost **Zpracovat**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="a33ed-424">Během zpracování vlny použije metoda třídění šablonu řazení k přiřazení inventáře k pozicím třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="a33ed-425">Po dokončení zpracování vlny obdržíte informační zprávu, která uvádí, že vlna byla zaúčtována a práce vytvořena.</span><span class="sxs-lookup"><span data-stu-id="a33ed-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="a33ed-426">V podokně akcí na kartě **Vlna** ve skupině **Související informace** vyberte **Práce** k zobrazení práce, která byla vytvořena pro tuto vlnu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="a33ed-427">Poznamenejte si ID práce.</span><span class="sxs-lookup"><span data-stu-id="a33ed-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="a33ed-428">Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Přiřazení pozice odchozího třídění**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="a33ed-429">V levém sloupci můžete zobrazit odchozí pozici třídění, která byla vytvořena pro každou zásilku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="a33ed-430">Na pevné záložce **Seřadit kritéria pozice** můžete zobrazit ID zásilky pro tuto pozici.</span><span class="sxs-lookup"><span data-stu-id="a33ed-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="a33ed-431">Bylo vytvořeno jedno ID práce pro přenesení zásob z míst výběru do místa třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="a33ed-432">K dokončení práce budete potřebovat ID práce, které bylo vytvořeno během zpracování vlny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="a33ed-433">Výběr prodejní objednávky do místa třídění</span><span class="sxs-lookup"><span data-stu-id="a33ed-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="a33ed-434">Přihlaste se do mobilní aplikace jako pracovník ve skladu *62*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="a33ed-435">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="a33ed-436">V nabídce **Odchozí** vyberte **Prodejní výdej**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="a33ed-437">Vyberte pole **ID** a zadejte ID práce ze zpracování vlny.</span><span class="sxs-lookup"><span data-stu-id="a33ed-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="a33ed-438">Potvrďte zadání.</span><span class="sxs-lookup"><span data-stu-id="a33ed-438">Confirm your entry.</span></span>

    <span data-ttu-id="a33ed-439">Dále se zobrazí výzva k zadání cílové registrační značky (LP).</span><span class="sxs-lookup"><span data-stu-id="a33ed-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="a33ed-440">Všimněte si, že řádek 1 z prodejní objednávky 1 je to, co musí být vybráno a přidáno na cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="a33ed-441">Zobrazí se číslo položky, množství, popis položky a místo výběru.</span><span class="sxs-lookup"><span data-stu-id="a33ed-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="a33ed-442">V poli **Cílová RZ** zadejte číslo registrační značky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="a33ed-443">Vyberete všechny řádky, které byly vytvořeny ze zpracované vlny, do stejné cílové poznávací značky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="a33ed-444">Potvrďte zadání.</span><span class="sxs-lookup"><span data-stu-id="a33ed-444">Confirm your entry.</span></span>

    <span data-ttu-id="a33ed-445">Mobilní aplikace nyní představují řadu stránek **Výběr**, které vás nasměrují na místo výdeje a na položku a množství, které je třeba vybrat.</span><span class="sxs-lookup"><span data-stu-id="a33ed-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="a33ed-446">Po přidání vybrané položky do poznávací značky potvrdíte výběr.</span><span class="sxs-lookup"><span data-stu-id="a33ed-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="a33ed-447">Poslední stránkou bude práce umístění vybraných položek do místa třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="a33ed-448">Potvrďte první práci vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="a33ed-449">Zobrazí se další práce vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-449">The next pick work is shown.</span></span> <span data-ttu-id="a33ed-450">Potvrďte vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-450">Confirm the pick.</span></span>
1. <span data-ttu-id="a33ed-451">Pokračujte v potvrzení zbývající práce vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="a33ed-452">Posledním krokem je dokončení práce vložení.</span><span class="sxs-lookup"><span data-stu-id="a33ed-452">The last step is to complete the put work.</span></span> <span data-ttu-id="a33ed-453">Potvrďte odložení do místa třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="a33ed-454">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="a33ed-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="a33ed-455">Ukončete **prodejní výběr** v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="a33ed-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="a33ed-456">Třídění / umístění na zeď</span><span class="sxs-lookup"><span data-stu-id="a33ed-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="a33ed-457">Nyní, když byly veškeré zásoby vloženy do místa třídění, musí být roztříděny do správné pozice třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="a33ed-458">Přihlaste se do mobilní aplikace.</span><span class="sxs-lookup"><span data-stu-id="a33ed-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="a33ed-459">V hlavní nabídce vyberte **Odchozí**.</span><span class="sxs-lookup"><span data-stu-id="a33ed-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="a33ed-460">V nabídce **Odchozí** vyberte **Třídit** pro zahájení třídění položek.</span><span class="sxs-lookup"><span data-stu-id="a33ed-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="a33ed-461">V poli **LP / CON** zadejte cílovou poznávací značku práce s vybranou prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="a33ed-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="a33ed-462">Potvrďte zadání.</span><span class="sxs-lookup"><span data-stu-id="a33ed-462">Confirm your entry.</span></span>
1. <span data-ttu-id="a33ed-463">Nejprve zadejte číslo položky k třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="a33ed-464">Systém určuje první polohu řazení, která by měla být zobrazena.</span><span class="sxs-lookup"><span data-stu-id="a33ed-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="a33ed-465">Potvrďte polohu třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="a33ed-466">Budete vyzváni k přiřazení registrační značky k pozici třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="a33ed-467">Vyberte pole **RZ**, zadejte číslo registrační značky a potvrďte zadání.</span><span class="sxs-lookup"><span data-stu-id="a33ed-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="a33ed-468">Protože pozice třídění souvisí s ID dodávky, roztřídíte vybrané položky seřadíte do registrační značky, která je specifická pro odchozí zásilku a prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="a33ed-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="a33ed-469">Na další stránce jsou uvedeny hodnoty ID položky, množství, ID pozice třídění a ID registrační značky "od" (výběr) a "do" (třídění).</span><span class="sxs-lookup"><span data-stu-id="a33ed-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="a33ed-470">Informace na této stránce vás vyzývají k třídění zadané položky a množství z registrační značky výběru do registrační značky třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="a33ed-471">Potvrďte polohu třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="a33ed-472">Seřaďte položky na první pozici třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="a33ed-473">Po dokončení vás systém přesměruje na další pozici třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="a33ed-474">Tento postup opakujte pro všechny vybrané řádky v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="a33ed-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="a33ed-475">Tento proces byste také měli použít, pokud existuje více řádků vyskladnění, které mají stejné číslo položky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="a33ed-476">Když tento proces opakujete pro všechny položky, systém vyhodnotí kritéria z další naskenované položky (pracovní linky) a určí, do které pozice se má třídit.</span><span class="sxs-lookup"><span data-stu-id="a33ed-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="a33ed-477">Budete automaticky nasměrováni, abyste položku umístili na správnou pozici.</span><span class="sxs-lookup"><span data-stu-id="a33ed-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="a33ed-478">V závislosti na nastavení potvrzení budete také vyzváni k potvrzení této akce zadáním čísla pozice nebo ID registrační značky.</span><span class="sxs-lookup"><span data-stu-id="a33ed-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a33ed-479">Pokud je zapnuto automatické třídění, není ruční přepsání k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a33ed-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="a33ed-480">Až skončíte, v Microsoft Dynamics 365 Supply Chain Management otevřete stránku **Přiřazení pozice odchozího třídění** a zkontrolujte stav pozic.</span><span class="sxs-lookup"><span data-stu-id="a33ed-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="a33ed-481">Pokud jsou pozice zavřené automaticky, vyberte **Zobrazit uzavřené** k zobrazení uzavřených pozic.</span><span class="sxs-lookup"><span data-stu-id="a33ed-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="a33ed-482">Všimněte si, že jsou zobrazeny transakce pozic třídění.</span><span class="sxs-lookup"><span data-stu-id="a33ed-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="a33ed-483">Zobrazí se položka a množství, které byly zpracovány prostřednictvím pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="a33ed-484">Když nastavíte šablonu pro odchozí třídění, nastavte možnost **Automaticky zavřít pozici třídění** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="a33ed-485">Pozice se proto automaticky uzavře po uložení posledních očekávaných zásob.</span><span class="sxs-lookup"><span data-stu-id="a33ed-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="a33ed-486">Pozice třídění jsou ve stavu **Zavřeno** a byla vytvořena práce na přesunutí tříděného inventáře do umístění k *nákladovým dveřím*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="a33ed-487">Dokončete práci výběru tříděných zásob a přesuňte zásoby do místa dodání.</span><span class="sxs-lookup"><span data-stu-id="a33ed-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="a33ed-488">Až budou zásoby připravené, potvrďte jejich odeslání.</span><span class="sxs-lookup"><span data-stu-id="a33ed-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="a33ed-489">Aby byly práce výběru seřazených zásob správně zpracována, měla by pro proces pohybu a naložení položka nabídky mobilního zařízení, která má ID pracovní třídy, kde je pole **Typ pracovního příkazu** nastaveno na *Seřazený výběr zásob*.</span><span class="sxs-lookup"><span data-stu-id="a33ed-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="a33ed-490">Ruční uzavření pozice (volitelné)</span><span class="sxs-lookup"><span data-stu-id="a33ed-490">Manually close a position (optional)</span></span>

<span data-ttu-id="a33ed-491">Pokud by se měly pozice třídění uzavřít ručně, musí být možnost **Automaticky zavřít pozici třídění** pro šablonu odchozího třídění nastavena na *Ne* a uzavření musí být provedeno před přesunutím zásob do oblasti nákladové brány.</span><span class="sxs-lookup"><span data-stu-id="a33ed-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="a33ed-492">Pozice lze uzavřít různými způsoby:</span><span class="sxs-lookup"><span data-stu-id="a33ed-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="a33ed-493">Prostřednictvím mobilní aplikace Řízení skladu:</span><span class="sxs-lookup"><span data-stu-id="a33ed-493">Via the Warehouse Management mobile app:</span></span>

    - <span data-ttu-id="a33ed-494">Uživatel může naskenovat jednu z položek, které jsou již na dané pozici, a poté vybrat **Zavřít** pro uzavření pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="a33ed-495">Pokud uživatel prohledá kontejner, který již byl roztříděn, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="a33ed-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="a33ed-496">Uživatel však stále může pokračovat k zavření pozice.</span><span class="sxs-lookup"><span data-stu-id="a33ed-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="a33ed-497">Ze stránky Microsoft Dynamics 365 Supply Chain Management **Přiřazení pozice odchozího třídění**:</span><span class="sxs-lookup"><span data-stu-id="a33ed-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="a33ed-498">Uživatel si může vybrat záznam pozice odchozího třídění a poté vybrat **Zavřít pozici** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="a33ed-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="a33ed-499">Tipy</span><span class="sxs-lookup"><span data-stu-id="a33ed-499">Tips</span></span>

- <span data-ttu-id="a33ed-500">Položky nemohou být přesouvány mezi pozicemi poté, co byly přiřazeny k jedné z nich.</span><span class="sxs-lookup"><span data-stu-id="a33ed-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="a33ed-501">Systém vyhodnotí, jaké množství jednotlivého zboží by mělo jít na konkrétní pozici.</span><span class="sxs-lookup"><span data-stu-id="a33ed-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="a33ed-502">Šablonu třídění lze nakonfigurovat tak, aby automaticky vytvořila kontejnery po uzavření pozic.</span><span class="sxs-lookup"><span data-stu-id="a33ed-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="a33ed-503">Tento přístup vytvoří standardní strukturu ID kontejneru, která je založena na určeném profilu balení.</span><span class="sxs-lookup"><span data-stu-id="a33ed-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a33ed-504">Po vytvoření pohybu z místa třídění nesmíte práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="a33ed-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="a33ed-505">V opačném případě bude pozice a kontejnery v ní odstraněny ze systému a nebudou k dispozici pro další zpracování.</span><span class="sxs-lookup"><span data-stu-id="a33ed-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="a33ed-506">Budou odstraněny rovněž zásoby.</span><span class="sxs-lookup"><span data-stu-id="a33ed-506">The inventory will also be removed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]