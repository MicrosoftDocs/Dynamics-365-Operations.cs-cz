---
title: Plná pozice seskupení
description: Tohle téma obsahuje informace o funkci Plná pozice seskupení. Tato funkce nabízí alternativu k přísnějšímu vynucování pravidel pracovní přestávky při použití výdejů v seskupení, protože umožňuje větší toleranci chyb ve volumetrických omezeních kontejnerů nebo břemen.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6a7cad070377de58d21a8eb91ee3e1ffaf1c660
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233000"
---
# <a name="cluster-position-full"></a><span data-ttu-id="59adf-104">Plná pozice seskupení</span><span class="sxs-lookup"><span data-stu-id="59adf-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59adf-105">Funkce *Plná pozice seskupení* nabízí alternativu k přísnějšímu vynucování pravidel pracovní přestávky při použití výdejů v seskupení, protože umožňuje větší toleranci chyb ve volumetrických omezeních kontejnerů nebo břemen.</span><span class="sxs-lookup"><span data-stu-id="59adf-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="59adf-106">V běžném scénáři se ne všechny položky pracovního příkazu vejdou do vybraného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="59adf-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="59adf-107">Pracovníci skladu, kteří provádějí výdej v seskupení, mají v tomto scénáři několik možností: musí buď změnit velikost kontejneru na větší nebo ve spolupráci se svým nadřízeným přijít s jiným řešením.</span><span class="sxs-lookup"><span data-stu-id="59adf-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="59adf-108">Tato funkce zavádí možnost spustit tlačítko **Plná** pro jednu z pracovních jednotek v seskupení.</span><span class="sxs-lookup"><span data-stu-id="59adf-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="59adf-109">Ve starších verzích byla tato možnost k dispozici pouze pro běžný výdej objednávek, nikoli pro výdej v seskupení.</span><span class="sxs-lookup"><span data-stu-id="59adf-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="59adf-110">Tato funkce se však liší od standardního tlačítka **Plná** v tom, že zruší zbývající práci.</span><span class="sxs-lookup"><span data-stu-id="59adf-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="59adf-111">Funkce nenavrhne, aby uživatel přidal do stejného seskupení další přihrádku a automaticky nevytváří novou práci.</span><span class="sxs-lookup"><span data-stu-id="59adf-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="59adf-112">Zapnutí funkce Plná pozice seskupení</span><span class="sxs-lookup"><span data-stu-id="59adf-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="59adf-113">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="59adf-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="59adf-114">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="59adf-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="59adf-115">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="59adf-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="59adf-116">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="59adf-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="59adf-117">**Název funkce:** *Plná pozice seskupení*</span><span class="sxs-lookup"><span data-stu-id="59adf-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="59adf-118">Nastavení</span><span class="sxs-lookup"><span data-stu-id="59adf-118">Setup</span></span>

<span data-ttu-id="59adf-119">Tato část poskytuje pokyny a příklad, který ukazuje, jak nastavit a používat funkci *Plná pozice seskupení*.</span><span class="sxs-lookup"><span data-stu-id="59adf-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="59adf-120">Příprava ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="59adf-120">Make sample data available</span></span>

<span data-ttu-id="59adf-121">Chcete-li s [příkladovým scénářem](#example-scenario) pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="59adf-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="59adf-122">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="59adf-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="59adf-123">Tento příklad můžete také použít jako průvodce pro použití této funkce ve výrobě.</span><span class="sxs-lookup"><span data-stu-id="59adf-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="59adf-124">V takovém případě však musíte každé nastavení, které je zde popsáno, nahradit vlastními hodnotami.</span><span class="sxs-lookup"><span data-stu-id="59adf-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="59adf-125">Profily seskupení</span><span class="sxs-lookup"><span data-stu-id="59adf-125">Cluster profiles</span></span>

<span data-ttu-id="59adf-126">Musíte určit, zda se ID seskupení generují automaticky, kolik pozic se používá, kdy jsou seskupení rozdělena a jak je práce výdeje řazena a ověřována.</span><span class="sxs-lookup"><span data-stu-id="59adf-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="59adf-127">Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Profily seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="59adf-128">V podokně seznamu vyberte záznam **Vytvořit seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="59adf-129">Na záložce s náhledem **Obecné** ověřte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="59adf-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="59adf-130">**Generovat ID seskupení:** – Vyberte *Ano*.</span><span class="sxs-lookup"><span data-stu-id="59adf-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="59adf-131">**Aktivovat pozice:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="59adf-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="59adf-132">**Počet pozic:** *2*</span><span class="sxs-lookup"><span data-stu-id="59adf-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="59adf-133">**Název pozice:** *Číselná*</span><span class="sxs-lookup"><span data-stu-id="59adf-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="59adf-134">**Rozdělit seskupení u:** *Vložení*</span><span class="sxs-lookup"><span data-stu-id="59adf-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="59adf-135">**Typ ověření řazení:** *Skenování pozice*</span><span class="sxs-lookup"><span data-stu-id="59adf-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="59adf-136">Na záložce s náhledem **Řazení seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="59adf-137">Mřížka by měla být prázdná (to znamená, že by neměla obsahovat žádné řádky).</span><span class="sxs-lookup"><span data-stu-id="59adf-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="59adf-138">Šablony práce</span><span class="sxs-lookup"><span data-stu-id="59adf-138">Work templates</span></span>

<span data-ttu-id="59adf-139">Musíte definovat, jak je vytvořena práce výdeje pro výdej v seskupení.</span><span class="sxs-lookup"><span data-stu-id="59adf-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="59adf-140">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="59adf-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="59adf-141">V horní části stránky nastavte pole **Typ pracovního příkjazu** na *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="59adf-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="59adf-142">Ujistěte se, že jsou uvedeny následující pracovní šablony z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="59adf-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="59adf-143">Pokud nejsou k dispozici, nebudete moci scénář dokončit.</span><span class="sxs-lookup"><span data-stu-id="59adf-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="59adf-144">Fáze 61 PO</span><span class="sxs-lookup"><span data-stu-id="59adf-144">61 SO Stage</span></span>
    - <span data-ttu-id="59adf-145">Výdej v seskupení 61 PO</span><span class="sxs-lookup"><span data-stu-id="59adf-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="59adf-146">Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="59adf-146">Location directives</span></span>

<span data-ttu-id="59adf-147">Musíte určit, odkud jsou položky vyskladněny a kam jsou vydány.</span><span class="sxs-lookup"><span data-stu-id="59adf-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="59adf-148">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="59adf-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="59adf-149">V záhlaví seznamu nastavte pole **Typ pracovního příkazu** na *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="59adf-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="59adf-150">Ujistěte se, že jsou uvedeny následující směrnice prodejní objednávky z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="59adf-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="59adf-151">Pokud nejsou k dispozici, nebudete moci scénář dokončit.</span><span class="sxs-lookup"><span data-stu-id="59adf-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="59adf-152">Výdej v seskupení 61</span><span class="sxs-lookup"><span data-stu-id="59adf-152">61 Cluster pick</span></span>
    - <span data-ttu-id="59adf-153">Výdej v seskupení 61</span><span class="sxs-lookup"><span data-stu-id="59adf-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="59adf-154">Položky nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="59adf-154">Mobile device menu items</span></span>

<span data-ttu-id="59adf-155">Musíte nakonfigurovat položku nabídky mobilního zařízení pro použití stávající práce, která se řídí výdejem v seskupení.</span><span class="sxs-lookup"><span data-stu-id="59adf-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="59adf-156">V položce nabídky mobilního zařízení pro výdej v seskupení musí být zapnutý parametr **Umožnit rozdělení práce** a musí být přidána třída práce *Výdej PO*.</span><span class="sxs-lookup"><span data-stu-id="59adf-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="59adf-157">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="59adf-158">V podokně seznamu vyberte záznam **Vytvoření výdeje v seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="59adf-159">V podokně Akce vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="59adf-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="59adf-160">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="59adf-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="59adf-161">**Řídí:** *Výdej v seskupení*</span><span class="sxs-lookup"><span data-stu-id="59adf-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="59adf-162">**Generovat registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="59adf-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="59adf-163">**Umožnit rozdělení práce** *Ano*</span><span class="sxs-lookup"><span data-stu-id="59adf-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="59adf-164">**ID profilu seskupení:** *Vytvořit seskupení*</span><span class="sxs-lookup"><span data-stu-id="59adf-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="59adf-165">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="59adf-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="59adf-166">Na záložce s náhledem **Pracovní třídy** podle potřeby přidejte následující dva řádky:</span><span class="sxs-lookup"><span data-stu-id="59adf-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="59adf-167">Řádek 1 (obvykle v ukázkových datech):</span><span class="sxs-lookup"><span data-stu-id="59adf-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="59adf-168">**ID pracovní třídy:** *Prodej*</span><span class="sxs-lookup"><span data-stu-id="59adf-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="59adf-169">**Typ pracovního příkazu:** *Prodejní objednávky*</span><span class="sxs-lookup"><span data-stu-id="59adf-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="59adf-170">Řádek 2 (pravděpodobně není v ukázkových datech):</span><span class="sxs-lookup"><span data-stu-id="59adf-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="59adf-171">**ID pracovní třídy:** *Výdej PO*</span><span class="sxs-lookup"><span data-stu-id="59adf-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="59adf-172">**Typ pracovního příkazu:** *Prodejní objednávky*</span><span class="sxs-lookup"><span data-stu-id="59adf-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="59adf-173">Jděte na **Nastavení potvrzení práce** v podokně Akce.</span><span class="sxs-lookup"><span data-stu-id="59adf-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="59adf-174">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="59adf-174">Select **Edit**.</span></span>
1. <span data-ttu-id="59adf-175">Na řádek v mřížce zadejte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="59adf-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="59adf-176">**Typ práce:** - *Výdej*</span><span class="sxs-lookup"><span data-stu-id="59adf-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="59adf-177">**Potvrzení produktu** - *Zaškrtněte políčko*</span><span class="sxs-lookup"><span data-stu-id="59adf-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="59adf-178">Vyberte **Uložit** v podokně Akce a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59adf-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="59adf-179">Vytvořit práci výdeje</span><span class="sxs-lookup"><span data-stu-id="59adf-179">Create picking work</span></span>

<span data-ttu-id="59adf-180">Než budete moci začít s výdejem seskupení, musíte vytvořit nějakou výstupní práci.</span><span class="sxs-lookup"><span data-stu-id="59adf-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="59adf-181">Dříve vytvořený profil seskupení určuje dvě pozice clusteru.</span><span class="sxs-lookup"><span data-stu-id="59adf-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="59adf-182">Proto musí být pro výdej prodejní objednávky vytvořena alespoň dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="59adf-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="59adf-183">V tomto scénáři dojde k transakcím ve skladu *61* a budou používat položky *L0101* a *T0100*.</span><span class="sxs-lookup"><span data-stu-id="59adf-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="59adf-184">Ukázková data by měla mít dostatek těchto položek na skladě.</span><span class="sxs-lookup"><span data-stu-id="59adf-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="59adf-185">Ujistěte se, že máte dostatek zásob k dokončení transakcí.</span><span class="sxs-lookup"><span data-stu-id="59adf-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="59adf-186">Vytvoření prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="59adf-186">Create sales order 1</span></span>

1. <span data-ttu-id="59adf-187">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="59adf-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="59adf-188">Volbou **Nová** vytvořte prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="59adf-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="59adf-189">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="59adf-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="59adf-190">**Účet zákazníka:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="59adf-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="59adf-191">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="59adf-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="59adf-192">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="59adf-192">Select **OK**.</span></span>
1. <span data-ttu-id="59adf-193">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="59adf-193">The new sales order is opened.</span></span> <span data-ttu-id="59adf-194">Na pevné záložce **Řádky prodejní objednávky** přidejte řádek s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="59adf-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="59adf-195">**Číslo položky:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="59adf-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="59adf-196">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="59adf-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="59adf-197">Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="59adf-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="59adf-198">Na záložce s náhledem **Řádky prodejní objednávky** přidejte druhý řádek s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="59adf-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="59adf-199">**Číslo položky:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="59adf-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="59adf-200">**Množství:** *20*</span><span class="sxs-lookup"><span data-stu-id="59adf-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="59adf-201">Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="59adf-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="59adf-202">Pro každý řádek, který jste právě přidali, rezervujte zásoby podle následujících pokynů:</span><span class="sxs-lookup"><span data-stu-id="59adf-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="59adf-203">Vyberte řádek, pro který chcete provést rezervaci.</span><span class="sxs-lookup"><span data-stu-id="59adf-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="59adf-204">Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="59adf-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="59adf-205">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.</span><span class="sxs-lookup"><span data-stu-id="59adf-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="59adf-206">Zavřete stránku **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="59adf-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="59adf-207">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="59adf-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="59adf-208">Když je dokončeno uvolnění, obdržíte informační zprávy znázorňující ID vlny a ID nákladu, jež byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="59adf-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="59adf-209">Vytvoření prodejní objednávky 2</span><span class="sxs-lookup"><span data-stu-id="59adf-209">Create sales order 2</span></span>

1. <span data-ttu-id="59adf-210">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="59adf-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="59adf-211">Volbou **Nová** vytvořte prodejní objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="59adf-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="59adf-212">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="59adf-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="59adf-213">**Účet zákazníka:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="59adf-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="59adf-214">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="59adf-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="59adf-215">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="59adf-215">Select **OK**.</span></span>
1. <span data-ttu-id="59adf-216">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="59adf-216">The new sales order is opened.</span></span> <span data-ttu-id="59adf-217">Na pevné záložce **Řádky prodejní objednávky** přidejte řádek s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="59adf-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="59adf-218">**Číslo položky:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="59adf-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="59adf-219">**Množství:** *20*</span><span class="sxs-lookup"><span data-stu-id="59adf-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="59adf-220">Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="59adf-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="59adf-221">Na záložce s náhledem **Řádky prodejní objednávky** přidejte druhý řádek s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="59adf-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="59adf-222">**Číslo položky:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="59adf-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="59adf-223">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="59adf-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="59adf-224">Na záložce s náhledem **Podrobnosti řádku** na kartě **Doručení** nastavte pole **Potvrzené datum expedice** na dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="59adf-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="59adf-225">Pro každý řádek, který jste právě přidali, rezervujte zásoby podle následujících pokynů:</span><span class="sxs-lookup"><span data-stu-id="59adf-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="59adf-226">Vyberte řádek, pro který chcete provést rezervaci.</span><span class="sxs-lookup"><span data-stu-id="59adf-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="59adf-227">Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="59adf-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="59adf-228">Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.</span><span class="sxs-lookup"><span data-stu-id="59adf-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="59adf-229">Zavřete stránku **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="59adf-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="59adf-230">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="59adf-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="59adf-231">Když je dokončeno uvolnění, obdržíte informační zprávy znázorňující ID vlny a ID nákladu, jež byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="59adf-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="59adf-232">Získání ID práce a registračních značek vozidel</span><span class="sxs-lookup"><span data-stu-id="59adf-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="59adf-233">Měla by být vytvořena dvě ID práce, z nichž každé má dva řádky výdeje.</span><span class="sxs-lookup"><span data-stu-id="59adf-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="59adf-234">Podle těchto pokynů vyhledejte ID práce a registrační značky vozidel.</span><span class="sxs-lookup"><span data-stu-id="59adf-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="59adf-235">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="59adf-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="59adf-236">V mřížce **Přehled** prohledejte sloupec **Číslo objednávky** pro dvě prodejní objednávky, které jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="59adf-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="59adf-237">Pro každou prodejní objednávku si poznamenejte odpovídající ID práce.</span><span class="sxs-lookup"><span data-stu-id="59adf-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="59adf-238">Výběrem řádku pro každou prodejní objednávku v něm zobrazíte související informace v mřížce **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="59adf-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="59adf-239">Poznamenejte si skladové místo, ze kterého bude každá položka vydána.</span><span class="sxs-lookup"><span data-stu-id="59adf-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="59adf-240">Přejděte na **Řízení zásob \> Dotazy a sestavy \> Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="59adf-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="59adf-241">V podokně Akce volbou **Dimenze** otevřete dialogové okno **Zobrazení dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="59adf-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="59adf-242">Ujistěte se, že jsou zaškrtnuta políčka **Registrační značka**, **Sklad** a **Číslo položky** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="59adf-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="59adf-243">V podokně **Filtr** nastavte následující filtry:</span><span class="sxs-lookup"><span data-stu-id="59adf-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="59adf-244">**Číslo položky** – **je jedním z** – *L0101* a *T100*</span><span class="sxs-lookup"><span data-stu-id="59adf-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="59adf-245">**Sklad** – **začíná na** – *61*</span><span class="sxs-lookup"><span data-stu-id="59adf-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="59adf-246">Poznamenejte si zobrazené hodnoty pro **registrační značku**.</span><span class="sxs-lookup"><span data-stu-id="59adf-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="59adf-247">Příklad</span><span class="sxs-lookup"><span data-stu-id="59adf-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="59adf-248">Spuštění toku mobilního zařízení – nastavení potvrzení práce pro produkt</span><span class="sxs-lookup"><span data-stu-id="59adf-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="59adf-249">Přihlaste se do skladové aplikace jako uživatel skladu *61*.</span><span class="sxs-lookup"><span data-stu-id="59adf-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="59adf-250">Jděte na **Odchozí \> Vytvoření výdeje v seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="59adf-251">Zobrazí se stránka **ÚKOL: Přiřadit práci seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="59adf-252">Zadejte ID práce pro prodejní objednávku 1 a přiřaďte jej k pozici seskupení 1.</span><span class="sxs-lookup"><span data-stu-id="59adf-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="59adf-253">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-254">Zadejte ID práce pro prodejní objednávku 2 a přiřaďte jej k pozici seskupení 2.</span><span class="sxs-lookup"><span data-stu-id="59adf-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="59adf-255">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="59adf-256">Zobrazí se stránka **ÚKOL: Vytvoření výdeje v seskupení: výdej**, která obsahuje *Položka L0101 2 PL* .</span><span class="sxs-lookup"><span data-stu-id="59adf-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="59adf-257">Protože profil seskupení nastavil počet pozic na 2, systém vás automaticky přesměruje na první konsolidovaný výdej: dvě palety (PL) položky *L0101*.</span><span class="sxs-lookup"><span data-stu-id="59adf-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="59adf-258">Během následujících kroků můžete kdykoli vybrat kartu **Podrobnosti** pro zobrazení dalších informací o úkolu, například výdejního skladovacího místa.</span><span class="sxs-lookup"><span data-stu-id="59adf-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="59adf-259">Nastavte pole **POLOŽKA** na *L0101*.</span><span class="sxs-lookup"><span data-stu-id="59adf-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="59adf-260">Tím se potvrdí číslo položky, které je pro tuto položku nabídky požadováno (to jste nakonfigurovali dříve výběrem **Nastavení potvrzení práce** na stránce **Položka nabídky mobilního zařízení**, když jste vytvořili tuto položku nabídky).</span><span class="sxs-lookup"><span data-stu-id="59adf-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="59adf-261">Zadejte registrační značku vozidla, která je přidružena k položce ve skladovém místě, ze kterého probíhá výdej.</span><span class="sxs-lookup"><span data-stu-id="59adf-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="59adf-262">Vyberete si dvě palety.</span><span class="sxs-lookup"><span data-stu-id="59adf-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="59adf-263">Nastavte pole **REGISTRAČNÍ ZNAČKA** na *REGISTRAČNÍ ZNAČKA\_VÝDEJ\_01*.</span><span class="sxs-lookup"><span data-stu-id="59adf-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="59adf-264">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="59adf-265">Zobrazí se stránka **ÚKOL: Seřadit: Vytvoření výdeje v seskupení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="59adf-266">Zde seřadíte dvě vyskladněné palety do pozice pro výdej.</span><span class="sxs-lookup"><span data-stu-id="59adf-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="59adf-267">Tato pozice může být břemeno nebo kontejner, který se používá k oddělení vyskladněných zásob podle prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="59adf-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="59adf-268">Zobrazte podrobnosti pro položku (*L0101*) a množství (*20* ks), které jsou seřazeny na pozici 1 (pro prodejní objednávku 1).</span><span class="sxs-lookup"><span data-stu-id="59adf-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="59adf-269">Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *1*.</span><span class="sxs-lookup"><span data-stu-id="59adf-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="59adf-270">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-271">Zobrazte podrobnosti pro položku (*L0101*) a množství (*20* ks), které jsou seřazeny na pozici 2 (pro prodejní objednávku 2).</span><span class="sxs-lookup"><span data-stu-id="59adf-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="59adf-272">Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *2*.</span><span class="sxs-lookup"><span data-stu-id="59adf-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="59adf-273">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="59adf-274">Zobrazí se stránka **ÚKOL: Vytvoření výdeje v seskupení: výdej**, která obsahuje *Položka T0100 7 ks* .</span><span class="sxs-lookup"><span data-stu-id="59adf-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="59adf-275">V tomto scénáři pozice 1 nemůže přijmout celé množství položek, které je třeba vyskladnit, aby byla splněna prodejní objednávka 1.</span><span class="sxs-lookup"><span data-stu-id="59adf-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="59adf-276">Pozice musí být označena jako plná.</span><span class="sxs-lookup"><span data-stu-id="59adf-276">A position must be marked as full.</span></span> <span data-ttu-id="59adf-277">V tomto scénáři provedete částečné vyskladnění druhé položky.</span><span class="sxs-lookup"><span data-stu-id="59adf-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="59adf-278">Druhá položka bude částečně vyskladněna pro pozici 1 a bude vytvořena nová práce pro vyskladnění zbývajícího množství pro splnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="59adf-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="59adf-279">Stiskněte tlačítko nabídky (tzv. „hamburgerové tlačítko“ nebo „hamburger“) a vyberte **Plná pozice**.</span><span class="sxs-lookup"><span data-stu-id="59adf-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="59adf-280">Určete pozici, která je plná, a vyberte *1*.</span><span class="sxs-lookup"><span data-stu-id="59adf-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="59adf-281">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-282">Zadejte množství k vyskladnění, které lze ještě vyskladnit do pozice 1.</span><span class="sxs-lookup"><span data-stu-id="59adf-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="59adf-283">Systém může určit, které číslo položky je vyskladňováno.</span><span class="sxs-lookup"><span data-stu-id="59adf-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="59adf-284">Zadejte *2*.</span><span class="sxs-lookup"><span data-stu-id="59adf-284">Enter *2*.</span></span>
1. <span data-ttu-id="59adf-285">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-286">Potvrďte číslo položky a dokončete vyskladnění zbývající položky do pozice 2.</span><span class="sxs-lookup"><span data-stu-id="59adf-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="59adf-287">Nastavte pole **POLOŽKA** na *T0100*.</span><span class="sxs-lookup"><span data-stu-id="59adf-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="59adf-288">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-289">Zadejte registrační značku vozidla, ze které je položka vyskladňována, nastavením pole **REGISTRAČNÍ ZNAČKA** na *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="59adf-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="59adf-290">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-291">Zobrazte podrobnosti pro položku (*T0100*) a množství (*2* ks), které jsou seřazeny na pozici 2 (pro prodejní objednávku 2).</span><span class="sxs-lookup"><span data-stu-id="59adf-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="59adf-292">Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *2*.</span><span class="sxs-lookup"><span data-stu-id="59adf-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="59adf-293">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="59adf-294">Zobrazte podrobnosti pro položku (*T0100*) a množství (*2* ks), které jsou seřazeny na pozici 1 (pro prodejní objednávku 1).</span><span class="sxs-lookup"><span data-stu-id="59adf-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="59adf-295">Nastavte pole **POZICE NENÍ K DISPOZICI** na hodnotu *1*.</span><span class="sxs-lookup"><span data-stu-id="59adf-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="59adf-296">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="59adf-297">Zobrazí se stránka **ÚKOL: Vytvoření výdeje v seskupení: vložení**.</span><span class="sxs-lookup"><span data-stu-id="59adf-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="59adf-298">V tomto scénáři byl proveden výdej v seskupení a uživatel je nasměrován k zaskladnění vyskladněních položek z pozice 1 a pozice 2 do přechodného skladového místa *FÁZE01*.</span><span class="sxs-lookup"><span data-stu-id="59adf-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="59adf-299">Zkontrolujte informace na stránce.</span><span class="sxs-lookup"><span data-stu-id="59adf-299">Review the information on the page.</span></span> <span data-ttu-id="59adf-300">Ukazuje, že celkové množství *44* bude zaskladněno do přechodného skladového místa.</span><span class="sxs-lookup"><span data-stu-id="59adf-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="59adf-301">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="59adf-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="59adf-302">Zobrazí se zpráva „Seskupení dokončeno“.</span><span class="sxs-lookup"><span data-stu-id="59adf-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="59adf-303">Nyní můžete pomocí položky nabídky **Prodejní výdej** vyskladnit zbývající množství.</span><span class="sxs-lookup"><span data-stu-id="59adf-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="59adf-304">Poté můžete pomocí položky nabídky **Nakládání prodeje** přesunout položky z přechodného skladového místa do překladišť.</span><span class="sxs-lookup"><span data-stu-id="59adf-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]