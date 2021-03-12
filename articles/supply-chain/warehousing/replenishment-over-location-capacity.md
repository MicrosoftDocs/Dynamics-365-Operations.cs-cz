---
title: Doplnění nad kapacitu místa
description: Toto téma obsahuje informace o funkci Doplňování přes kapacitu místa. Tato funkce umožňuje veškerou doplňovací práci, která bude vyžadována na den, který má být vytvořen, a řídí dostupnost této doplňovací práce, aby bylo zajištěno, že místu vyskladnění nedojdou zásoby, ani nepřekročí kapacitu.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3f94053920b475ef9190b5ac65a5f9ca01dcd4a1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996116"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="2a902-104">Doplnění nad kapacitu místa</span><span class="sxs-lookup"><span data-stu-id="2a902-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a902-105">Některé velkoobjemové sklady nebo sklady s omezeným prostorem musí přepravit více kusů zboží za den, než kolik se vejde na místo vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="2a902-106">Funkce *Doplnění nad kapacitu místa* umožňuje veškerou doplňovací práci, která bude vyžadována na den, který má být vytvořen, a řídí dostupnost této doplňovací práce, aby bylo zajištěno, že místu vyskladnění nedojdou zásoby, ani nepřekročí kapacitu.</span><span class="sxs-lookup"><span data-stu-id="2a902-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="2a902-107">Tato funkce umožňuje vytvořit více prací doplnění, než kolik se vejde na místo, a blokuje dokončení doplňovacích prací, když je místo plné.</span><span class="sxs-lookup"><span data-stu-id="2a902-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="2a902-108">Jak zásoby ve vychystávacím místě klesnou pod nastavitelný práh, je k dispozici více doplňovacích prací.</span><span class="sxs-lookup"><span data-stu-id="2a902-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="2a902-109">Zapnutí funkce Doplnění nad kapacitu místa</span><span class="sxs-lookup"><span data-stu-id="2a902-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="2a902-110">Chcete-li tuto funkci zpřístupnit, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí):</span><span class="sxs-lookup"><span data-stu-id="2a902-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="2a902-111">Blokování práce pro celou organizaci</span><span class="sxs-lookup"><span data-stu-id="2a902-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="2a902-112">Doplnění nad kapacitu místa</span><span class="sxs-lookup"><span data-stu-id="2a902-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="2a902-113">Nastavení funkce pro tento vzorový scénář</span><span class="sxs-lookup"><span data-stu-id="2a902-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="2a902-114">Tato část obsahuje pokyny a příklad, který ukazuje, jak nastavit tuto funkci a připravit ukázková data pro příkladový scénář, který je uveden dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2a902-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="2a902-115">Povolit ukázková data</span><span class="sxs-lookup"><span data-stu-id="2a902-115">Enable sample data</span></span>

<span data-ttu-id="2a902-116">Chcete-li s [příkladovým scénářem](#example-scenario) pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2a902-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="2a902-117">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="2a902-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="2a902-118">Profil umístění</span><span class="sxs-lookup"><span data-stu-id="2a902-118">Location profile</span></span>

<span data-ttu-id="2a902-119">Povolte funkci doplňování přes kapacitu v profilu místa.</span><span class="sxs-lookup"><span data-stu-id="2a902-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="2a902-120">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily míst**.</span><span class="sxs-lookup"><span data-stu-id="2a902-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="2a902-121">V levém podokně vyberte možnost **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="2a902-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="2a902-122">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2a902-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2a902-123">Na pevné záložce **Doplnění** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2a902-124">**Překročit lokální kapacitu:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="2a902-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="2a902-125">Když je tato možnost povolena, bude povoleno překročení maximální kapacity místa o práci doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="2a902-126">To také umožňuje další pole na pevné záložce **Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="2a902-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="2a902-127">**Typ prahu dostupnosti práce:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="2a902-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="2a902-128">Toto pole definuje metodu, která se používá k určení, kdy by mělo být uvolněno více práce.</span><span class="sxs-lookup"><span data-stu-id="2a902-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="2a902-129">Můžete uvolnit podle množství nebo procent.</span><span class="sxs-lookup"><span data-stu-id="2a902-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="2a902-130">*Procento* - Tuto možnost vyberte, chcete-li použít procentuální kapacitu, která je založena na limitech skladování nebo objemu.</span><span class="sxs-lookup"><span data-stu-id="2a902-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="2a902-131">Výběr této možnosti povolí pole **Procento přetečení** a zakáže dvě pole související s množstvím, **Množství přetečení** a **Jednotka přetečení**.</span><span class="sxs-lookup"><span data-stu-id="2a902-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="2a902-132">Tuto možnost můžete použít, pokud místa výběru používají objemové jednotky.</span><span class="sxs-lookup"><span data-stu-id="2a902-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="2a902-133">Pokud je vybrána tato možnost, nastavte pole **Procento přetečení** na, ve kterém bude k dispozici více prací doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="2a902-134">*Množství* - Tuto možnost vyberte, chcete-li použít konkrétní hodnotu množství.</span><span class="sxs-lookup"><span data-stu-id="2a902-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="2a902-135">Výběr této možnosti zakáže pole **Procento přetečení** a povolí pole **Množství přetečení** a **Jednotka přetečení**.</span><span class="sxs-lookup"><span data-stu-id="2a902-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="2a902-136">Tuto možnost použijte, pokud nepoužíváte objem pro místa, která se doplňují, nebo pokud máte konzistentní množství, ve kterých chcete do místa přivést další inventář.</span><span class="sxs-lookup"><span data-stu-id="2a902-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="2a902-137">Pokud je vybrána tato možnost, nastavte pole **Množství přetečení** a **Jednotka přetečení** na množství a jednotku, ve které bude k dispozici více doplňovacích prací.</span><span class="sxs-lookup"><span data-stu-id="2a902-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="2a902-138">**Množství přetečení:** *0.65*</span><span class="sxs-lookup"><span data-stu-id="2a902-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="2a902-139">Toto pole definuje množství, při kterém místo přetéká.</span><span class="sxs-lookup"><span data-stu-id="2a902-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="2a902-140">Práce bude k dispozici pokaždé, když je součet množství na skladě v místě a množství práce pod touto hodnotou.</span><span class="sxs-lookup"><span data-stu-id="2a902-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="2a902-141">Jakákoli práce doplnění nad touto hodnotou bude blokována a bude nutné ji odblokovat ručně.</span><span class="sxs-lookup"><span data-stu-id="2a902-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="2a902-142">Při výpočtu pracovního množství se berou v úvahu limity místního skladování.</span><span class="sxs-lookup"><span data-stu-id="2a902-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="2a902-143">**Jednotka přetečení:** *PL*</span><span class="sxs-lookup"><span data-stu-id="2a902-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="2a902-144">Toto pole definuje jednotku, která je spojena s množstvím přetečení.</span><span class="sxs-lookup"><span data-stu-id="2a902-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="2a902-145">V tomto případě bude k dispozici více doplňovacích prací, jakmile se umístění dostane na 0,65 palety (PL).</span><span class="sxs-lookup"><span data-stu-id="2a902-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="2a902-146">**Procento přetečení**</span><span class="sxs-lookup"><span data-stu-id="2a902-146">**Overflow percentage**</span></span>

        <span data-ttu-id="2a902-147">Toto pole definuje procento, při kterém místo přetéká.</span><span class="sxs-lookup"><span data-stu-id="2a902-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="2a902-148">Práce bude k dispozici pokaždé, když je součet množství na skladě v místě a množství práce pod tímto procentem.</span><span class="sxs-lookup"><span data-stu-id="2a902-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="2a902-149">Jakékoli procento množství práce doplnění nad touto hodnotou bude blokováno a bude nutné je odblokovat ručně.</span><span class="sxs-lookup"><span data-stu-id="2a902-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="2a902-150">Při výpočtu procenta pracovního množství se berou v úvahu limity místního skladování.</span><span class="sxs-lookup"><span data-stu-id="2a902-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="2a902-151">Pokud nejsou definovány žádné limity pro místo uskladnění, procento množství práce bude vypočteno podle objemu, pokud jsou v profilu místa definována omezení objemu.</span><span class="sxs-lookup"><span data-stu-id="2a902-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a902-152">Pokud používáte ukázková data pro právnickou osobu **USMF** právnická osoba a dříve jste zapnuli funkci *Umístění poznávací značky*, musíte vypnout nastavení **Povolit umístění poznávací značky** pro profil místa **BULK-06** k dokončení mobilních kroků v příkladu scénáře.</span><span class="sxs-lookup"><span data-stu-id="2a902-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="2a902-153">Kód kroku vlny</span><span class="sxs-lookup"><span data-stu-id="2a902-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="2a902-154">Chcete-li nastavit kód kroku vlny, jak je zde popsáno, možná budete muset nejprve použít [řízení funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k zapnutí funkce, která je pojmenována *Kód kroků vlny napříč organizací*.</span><span class="sxs-lookup"><span data-stu-id="2a902-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="2a902-155">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny**.</span><span class="sxs-lookup"><span data-stu-id="2a902-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="2a902-156">Klikněte na **Nový** a poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="2a902-157">**Kód kroku vlny:** *Replen*</span><span class="sxs-lookup"><span data-stu-id="2a902-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="2a902-158">**Popis kroku vlny:** *Doplnění*</span><span class="sxs-lookup"><span data-stu-id="2a902-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="2a902-159">**Typ kroku vlny:** *Doplnění*</span><span class="sxs-lookup"><span data-stu-id="2a902-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="2a902-160">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2a902-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="2a902-161">Šablona doplnění</span><span class="sxs-lookup"><span data-stu-id="2a902-161">Replenishment template</span></span>

<span data-ttu-id="2a902-162">Šablony doplnění jsou sada pravidel, která určují, kdy a jak je skladové místo doplňováno.</span><span class="sxs-lookup"><span data-stu-id="2a902-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="2a902-163">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="2a902-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="2a902-164">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2a902-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2a902-165">V části **Přehled** vyberte řádek, na kterém je pole **Doplňte šablonu** nastaveno na *Doplnění poptávky*.</span><span class="sxs-lookup"><span data-stu-id="2a902-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="2a902-166">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-166">Set the following values:</span></span>

    - <span data-ttu-id="2a902-167">**Kód kroku vlny:** *Replen*</span><span class="sxs-lookup"><span data-stu-id="2a902-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="2a902-168">**Povolit použití nerezervovaných množství ve vlnové poptávce:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="2a902-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="2a902-169">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2a902-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="2a902-170">Šablona vlny</span><span class="sxs-lookup"><span data-stu-id="2a902-170">Wave template</span></span>

1. <span data-ttu-id="2a902-171">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="2a902-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="2a902-172">V levém podokně nastavte v poli **Typ šablony vlny** na hodnotu *Doplnění*.</span><span class="sxs-lookup"><span data-stu-id="2a902-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="2a902-173">Vyberte šablonu **61 Shipping** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2a902-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="2a902-174">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2a902-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2a902-175">Na pevné záložce **Obecné** nastavte volbu **Uvolnění práce automatického doplnění** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="2a902-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="2a902-176">Nastavením této možnosti na *ano* můžete vytvořit doplnění podle poptávky a automaticky je vydat.</span><span class="sxs-lookup"><span data-stu-id="2a902-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="2a902-177">Musíte přidat metodu doplnění vlny do šablony vlny a vytvořit šablonu doplnění typu **Poptávka vlny**.</span><span class="sxs-lookup"><span data-stu-id="2a902-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="2a902-178">Nastavte šablonu doplnění na stránce **Šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="2a902-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="2a902-179">Chcete-li nastavit šablonu doplňování, musíte do šablony vlny přidat metodu doplňování.</span><span class="sxs-lookup"><span data-stu-id="2a902-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="2a902-180">Na pevné záložce **Metody** ve sloupci **Vybrané metody** najděte následující řádek:</span><span class="sxs-lookup"><span data-stu-id="2a902-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="2a902-181">**Název metody:** *replenish*</span><span class="sxs-lookup"><span data-stu-id="2a902-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="2a902-182">**Název:** *Doplnění*</span><span class="sxs-lookup"><span data-stu-id="2a902-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="2a902-183">Nastavte pole **Kód kroku vlny** pro tento řádek na *Replen*.</span><span class="sxs-lookup"><span data-stu-id="2a902-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="2a902-184">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2a902-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2a902-185">Příklad</span><span class="sxs-lookup"><span data-stu-id="2a902-185">Example scenario</span></span>

<span data-ttu-id="2a902-186">Po zpřístupnění a nastavení všech výše popsaných vzorových dat můžete v rámci tohoto scénáře vyzkoušet funkci *Doplnění nad kapacitu místa*.</span><span class="sxs-lookup"><span data-stu-id="2a902-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="2a902-187">Hodnoty zobrazené v tomto scénáři předpokládají, že pracujete se standardními ukázkovými daty, která jste vybrali v právnické osobě **USMF** a připravili jste vzorové záznamy, které jsou popsány dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2a902-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="2a902-188">Tento scénář také slouží jako příklad, který ukazuje, jak lze funkci použít v produkčním nastavení.</span><span class="sxs-lookup"><span data-stu-id="2a902-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="2a902-189">Vytvořit práci doplnění</span><span class="sxs-lookup"><span data-stu-id="2a902-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="2a902-190">Vytvoření prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="2a902-190">Create sales order 1</span></span>

1. <span data-ttu-id="2a902-191">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2a902-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2a902-192">V podokně Akce zvolte možnost **Nová** a otevře se dialogové okno pro vytvoření nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2a902-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="2a902-193">V dialogovém okně nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="2a902-194">**Účet zákazníka:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2a902-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="2a902-195">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="2a902-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="2a902-196">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="2a902-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="2a902-197">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="2a902-197">The new sales order is opened.</span></span> <span data-ttu-id="2a902-198">Zahrnuje nový prázdný řádek na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2a902-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2a902-199">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="2a902-200">**Číslo položky:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="2a902-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="2a902-201">**Množství:** *40*</span><span class="sxs-lookup"><span data-stu-id="2a902-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="2a902-202">Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="2a902-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="2a902-203">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.</span><span class="sxs-lookup"><span data-stu-id="2a902-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="2a902-204">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2a902-204">Close the page.</span></span>
1. <span data-ttu-id="2a902-205">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="2a902-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2a902-206">Zobrazí se informační zprávy, které uvádí ID vlny a ID dodávky, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="2a902-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="2a902-207">Vytvoří se také vlna doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="2a902-208">Obdržíte také varovnou zprávu, která uvádí: „ID práce XXXX nelze odblokovat, protože má nedokončené doplňování.“</span><span class="sxs-lookup"><span data-stu-id="2a902-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="2a902-209">Vytvoření prodejní objednávky 2</span><span class="sxs-lookup"><span data-stu-id="2a902-209">Create sales order 2</span></span>

1. <span data-ttu-id="2a902-210">Na stránce **Všechny prodejní objednávky** v podokně akcí zvolte možnost **Nová** a otevře se dialogové okno pro vytvoření nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2a902-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="2a902-211">V dialogovém okně nastavte následující hodnota:</span><span class="sxs-lookup"><span data-stu-id="2a902-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="2a902-212">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2a902-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2a902-213">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="2a902-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="2a902-214">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="2a902-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="2a902-215">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="2a902-215">The new sales order is opened.</span></span> <span data-ttu-id="2a902-216">Zahrnuje nový prázdný řádek na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2a902-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2a902-217">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="2a902-218">**Číslo položky:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="2a902-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="2a902-219">**Množství:** *60*</span><span class="sxs-lookup"><span data-stu-id="2a902-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="2a902-220">Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="2a902-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="2a902-221">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.</span><span class="sxs-lookup"><span data-stu-id="2a902-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="2a902-222">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2a902-222">Close the page.</span></span>
1. <span data-ttu-id="2a902-223">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="2a902-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2a902-224">Zobrazí se informační zprávy, které uvádí ID vlny a ID dodávky, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="2a902-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="2a902-225">Vytvoří se také vlna doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="2a902-226">Obdržíte také varovnou zprávu, která uvádí: „ID práce XXXX nelze odblokovat, protože má nedokončené doplňování.“</span><span class="sxs-lookup"><span data-stu-id="2a902-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="2a902-227">Vytvoření prodejní objednávky 3</span><span class="sxs-lookup"><span data-stu-id="2a902-227">Create sales order 3</span></span>

1. <span data-ttu-id="2a902-228">Na stránce **Všechny prodejní objednávky** v podokně akcí zvolte možnost **Nová** a otevře se dialogové okno pro vytvoření nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2a902-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="2a902-229">V dialogovém okně nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="2a902-230">**Účet zákazníka:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="2a902-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="2a902-231">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="2a902-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="2a902-232">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="2a902-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="2a902-233">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="2a902-233">The new sales order is opened.</span></span> <span data-ttu-id="2a902-234">Zahrnuje nový prázdný řádek na pevné záložce **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2a902-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2a902-235">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2a902-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="2a902-236">**Číslo položky:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="2a902-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="2a902-237">**Množství:** *30*</span><span class="sxs-lookup"><span data-stu-id="2a902-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="2a902-238">Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="2a902-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="2a902-239">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.</span><span class="sxs-lookup"><span data-stu-id="2a902-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="2a902-240">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2a902-240">Close the page.</span></span>
1. <span data-ttu-id="2a902-241">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="2a902-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2a902-242">Zobrazí se informační zprávy, které uvádí ID vlny a ID dodávky, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="2a902-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="2a902-243">Vytvoří se také vlna doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="2a902-244">Obdržíte také varovnou zprávu, která uvádí: „ID práce XXXX nelze odblokovat, protože má nedokončené doplňování.“</span><span class="sxs-lookup"><span data-stu-id="2a902-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="2a902-245">Zobrazit podrobnosti práce</span><span class="sxs-lookup"><span data-stu-id="2a902-245">View work details</span></span>

1. <span data-ttu-id="2a902-246">Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="2a902-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="2a902-247">V části **Přehled** vyfiltrujte sloupec **Sklad** pro sklad *61*.</span><span class="sxs-lookup"><span data-stu-id="2a902-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="2a902-248">Měli byste vidět, že pro tři prodejní objednávky bylo vytvořeno sedm ID práce.</span><span class="sxs-lookup"><span data-stu-id="2a902-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="2a902-249">Tři ze sedmi ID práce mají hodnotu **Typ pracovního příkazu** *Doplnění* a čtyři mají hodnotu **Typ pracovního příkazu** *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="2a902-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="2a902-250">Všechna tři ID práce, která mají hodnotu **Typ pracovního příkazu** *Doplnění*, mají stejná místa *Výběr* a *Vložení* v sekci **Řádky**:</span><span class="sxs-lookup"><span data-stu-id="2a902-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="2a902-251">**Výběr:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="2a902-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="2a902-252">**Vložení:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="2a902-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="2a902-253">Pro prodejní objednávku 1 byla vytvořena dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="2a902-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="2a902-254">Pro každou prodejní objednávku si poznamenejte ID práce.</span><span class="sxs-lookup"><span data-stu-id="2a902-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="2a902-255">V závislosti na množství, které máte k dispozici, se mohou vytvořená množství práce mírně lišit.</span><span class="sxs-lookup"><span data-stu-id="2a902-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="2a902-256">Celkově by se však vytvořená záhlaví práce měla shodovat s tímto příkladem scénáře.</span><span class="sxs-lookup"><span data-stu-id="2a902-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="2a902-257">ID registrační značky na skladě</span><span class="sxs-lookup"><span data-stu-id="2a902-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="2a902-258">Později v tomto scénáři budete používat skladovací aplikaci (nebo emulátor), kde musíte identifikovat registrační značku pro dokončení scénářů vychystávání a doplňování.</span><span class="sxs-lookup"><span data-stu-id="2a902-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="2a902-259">Chcete-li najít ID registrační značky, které budete později potřebovat, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2a902-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="2a902-260">Přejděte na **Řízení zásob \> Dotazy a sestavy \> Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="2a902-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="2a902-261">Vyberte **Zobrazit filtry** pro otevření podokna filtru.</span><span class="sxs-lookup"><span data-stu-id="2a902-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="2a902-262">Chcete-li získat poznávací značky pro scénář, zadejte následující kritéria filtrování.</span><span class="sxs-lookup"><span data-stu-id="2a902-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="2a902-263">Použijte filtr *začíná na*.</span><span class="sxs-lookup"><span data-stu-id="2a902-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="2a902-264">**Číslo položky:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="2a902-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="2a902-265">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="2a902-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="2a902-266">Zvolte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="2a902-266">Select **Apply**.</span></span>
1. <span data-ttu-id="2a902-267">V podokně akcí zvolte **Rozměry**.</span><span class="sxs-lookup"><span data-stu-id="2a902-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="2a902-268">V dialogovém okně **Zobrazení dimenzí** v části **Dimenze úložiště** vyberte všechny hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2a902-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="2a902-269">V části **Transakce** vyberte **Číslo položky** a **Množství \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="2a902-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="2a902-270">Po dokončení vyberte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2a902-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="2a902-271">Mřížka **Na skladě** zobrazuje čísla registračních značek pro položku *T0100* na každém místě.</span><span class="sxs-lookup"><span data-stu-id="2a902-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="2a902-272">Poznamenejte si poznávací značku, která je na každém místě, protože tyto informace budete potřebovat později.</span><span class="sxs-lookup"><span data-stu-id="2a902-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="2a902-273">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2a902-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="2a902-274">Kroky procesu</span><span class="sxs-lookup"><span data-stu-id="2a902-274">Process steps</span></span>

<span data-ttu-id="2a902-275">Provedete doplnění umístění skladu pro první dvě ID práce.</span><span class="sxs-lookup"><span data-stu-id="2a902-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="2a902-276">Práce na třetím doplňování budou blokovány, dokud úroveň zásob v místě vyskladnění neklesne pod prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2a902-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="2a902-277">Doplnění</span><span class="sxs-lookup"><span data-stu-id="2a902-277">Replenishment</span></span>

1. <span data-ttu-id="2a902-278">Přihlaste se do skladové aplikace jako uživatel skladu *61*.</span><span class="sxs-lookup"><span data-stu-id="2a902-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="2a902-279">(Zadejte *61* jako ID uživatele a *1* jako heslo.)</span><span class="sxs-lookup"><span data-stu-id="2a902-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="2a902-280">Přejděte na **Zásoby \> Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="2a902-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="2a902-281">Jste vyzváni, abyste dokončili první práci na doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="2a902-282">Zobrazí se číslo položky, množství a umístění pro vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="2a902-283">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="2a902-284">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="2a902-285">Systém vygeneruje cílové číslo registrační značky pro novou registrační značku pro vybranou položku.</span><span class="sxs-lookup"><span data-stu-id="2a902-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="2a902-286">Hodnotu potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="2a902-287">Je ukázána práce vyskladnění, která dává uživateli pokyn k umístění cílové registrační značky do místa doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="2a902-288">Umístění *Vložení* by mělo být **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="2a902-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="2a902-289">Potvrďte zadané údaje a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="2a902-290">Zobrazí se zpráva „Práce dokončena“ a jsou zobrazeny podrobnosti o další úloze výběru doplňku: číslo položky, množství a umístění, ze kterého lze vybrat.</span><span class="sxs-lookup"><span data-stu-id="2a902-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="2a902-291">Místo výběru bude stejné jako první místo doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="2a902-292">Proto bude registrační značka mít stejné ID registrační značky, jaké bylo použito pro první úkol doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="2a902-293">Opakováním předchozích kroků dokončete doplňování pro druhý pracovní úkol.</span><span class="sxs-lookup"><span data-stu-id="2a902-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="2a902-294">Množství a cílová registrační značka se budou lišit od množství a cílové registrační značky pro první pracovní úkol.</span><span class="sxs-lookup"><span data-stu-id="2a902-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="2a902-295">Po dokončení druhého doplňování práce se zobrazí zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="2a902-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="2a902-296">Mobilní zařízení vás také informuje, že není k dispozici žádná práce, přestože některé práce na doplňování zbývají.</span><span class="sxs-lookup"><span data-stu-id="2a902-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="2a902-297">K tomuto chování dochází, protože práce doplňování má stav dostupnosti *Zadržení* a je proto označen jako **Blokováno**.</span><span class="sxs-lookup"><span data-stu-id="2a902-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="2a902-298">Stav *Zadržení* byl spuštěn, protože profil umístění pro místo výběru, ke kterému je práce přiřazena, má hodnotu **Množství přetečení** *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="2a902-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="2a902-299">Dva předchozí pracovní úkoly doplňování naplnily umístění téměř na hranici přetečení pro položku *T0100*.</span><span class="sxs-lookup"><span data-stu-id="2a902-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="2a902-300">(Převod jednotek pro položku je *1 PL = 100 ea* .) Proto by zbývající doplňovací práce způsobily, že umístění překročí limit přetečení.</span><span class="sxs-lookup"><span data-stu-id="2a902-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="2a902-301">Dokud nebude z místa vybrán dostatek zásob, aby byl pod položkou nabídky uvolnění práce v položce nabídky mobilního zařízení, zůstane toto doplňování blokováno.</span><span class="sxs-lookup"><span data-stu-id="2a902-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="2a902-302">Výběr prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="2a902-302">Sales order pick</span></span>

<span data-ttu-id="2a902-303">Před dokončením zbývajícího úkolu doplňování musí být místo vyskladnění vyčerpáno ze zásoby na úroveň, na které lze zbývající část doplňování odblokovat.</span><span class="sxs-lookup"><span data-stu-id="2a902-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="2a902-304">Jinými slovy, součet množství zásob na skladě v místě a množství doplňování nesmí překročit hodnota **Přetečené množství**.</span><span class="sxs-lookup"><span data-stu-id="2a902-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="2a902-305">Pokud je tato částka menší než množství přetečení, zbývající doplňování bude odblokováno.</span><span class="sxs-lookup"><span data-stu-id="2a902-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="2a902-306">Přihlaste se do skladové aplikace jako uživatel skladu *61*.</span><span class="sxs-lookup"><span data-stu-id="2a902-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="2a902-307">(Zadejte *61* jako ID uživatele a *1* jako heslo.)</span><span class="sxs-lookup"><span data-stu-id="2a902-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="2a902-308">Přejděte do **Výstupní \> Prodejní výdej**.</span><span class="sxs-lookup"><span data-stu-id="2a902-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="2a902-309">Zadejte první ID práce pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="2a902-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="2a902-310">Podívejte se na ID práce u prodejních objednávek, které jste si poznamenali dříve, na stránce **Podrobnosti o práci**.</span><span class="sxs-lookup"><span data-stu-id="2a902-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="2a902-311">ID práce, které zde zadáte, vygeneruje výběrovou práci pro množství 10 ea ze dvou samostatných míst.</span><span class="sxs-lookup"><span data-stu-id="2a902-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="2a902-312">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-312">Select **OK**.</span></span>

    <span data-ttu-id="2a902-313">Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat první umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="2a902-314">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="2a902-315">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="2a902-316">Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat další umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="2a902-317">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="2a902-318">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="2a902-319">Stránka **Prodejní objednávky: Vložení** vám dá pokyn k odložení obou dokončených prací výběru na odchozí skladové místo.</span><span class="sxs-lookup"><span data-stu-id="2a902-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="2a902-320">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-320">Select **OK**.</span></span>

    <span data-ttu-id="2a902-321">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="2a902-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2a902-322">Zadejte druhé ID práce pro prodejní objednávku 1.</span><span class="sxs-lookup"><span data-stu-id="2a902-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="2a902-323">Pro toto pracovní ID existuje pouze jeden výběrový úkol.</span><span class="sxs-lookup"><span data-stu-id="2a902-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="2a902-324">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-324">Select **OK**.</span></span>

    <span data-ttu-id="2a902-325">Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat.</span><span class="sxs-lookup"><span data-stu-id="2a902-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="2a902-326">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="2a902-327">Zadaná registrační značka bude jednou z registračních značek generovaných systémem z pracovních úkolů doplňování.</span><span class="sxs-lookup"><span data-stu-id="2a902-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="2a902-328">Chcete-li se ujistit, že jste zachytili správné ID registrační značky, zkontrolujte zásoby na stránce **Seznam po ruce** pro položku, umístění a množství.</span><span class="sxs-lookup"><span data-stu-id="2a902-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="2a902-329">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="2a902-330">Potvrďte pokyny pro úlohu umístění do odchozího skladového místa.</span><span class="sxs-lookup"><span data-stu-id="2a902-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="2a902-331">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-331">Select **OK**.</span></span>

    <span data-ttu-id="2a902-332">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="2a902-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="2a902-333">Prodejní objednávka 2 je zablokována, protože úkol doplňování, ke kterému je připojen, není dokončen.</span><span class="sxs-lookup"><span data-stu-id="2a902-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="2a902-334">V současné době je v místě vychystávání stále množství 30 ks a množství doplňování pro prodejní objednávku 2 je 60 ks.</span><span class="sxs-lookup"><span data-stu-id="2a902-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="2a902-335">Součet zásob na skladě a zásob doplňování (90 ks) překračuje množství přetečení o 0,65 PL (nebo 65 ks).</span><span class="sxs-lookup"><span data-stu-id="2a902-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="2a902-336">Před dokončením doplňovacích prací musí být vybrána prodejní objednávka 3.</span><span class="sxs-lookup"><span data-stu-id="2a902-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="2a902-337">Zadejte ID práce pro prodejní objednávku 3.</span><span class="sxs-lookup"><span data-stu-id="2a902-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="2a902-338">Pro toto pracovní ID existuje pouze jeden výběrový úkol.</span><span class="sxs-lookup"><span data-stu-id="2a902-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="2a902-339">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-339">Select **OK**.</span></span>

    <span data-ttu-id="2a902-340">Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat.</span><span class="sxs-lookup"><span data-stu-id="2a902-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="2a902-341">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="2a902-342">Zadaná registrační značka bude jednou z registračních značek generovaných systémem z pracovních úkolů doplňování.</span><span class="sxs-lookup"><span data-stu-id="2a902-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="2a902-343">Chcete-li se ujistit, že jste zachytili správné ID registrační značky, zkontrolujte zásoby na stránce **Seznam po ruce** pro položku, umístění a množství.</span><span class="sxs-lookup"><span data-stu-id="2a902-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="2a902-344">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="2a902-345">Potvrďte pokyny pro úlohu umístění do odchozího skladového místa.</span><span class="sxs-lookup"><span data-stu-id="2a902-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="2a902-346">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-346">Select **OK**.</span></span>

    <span data-ttu-id="2a902-347">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="2a902-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="2a902-348">Jakmile je součet množství na skladě v místě vychystávání a množství doplňování pod prahem, budete moci zpracovat zbývající práci doplňování.</span><span class="sxs-lookup"><span data-stu-id="2a902-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="2a902-349">Vraťte se na stránku **Podrobnosti o práci** a všimněte si, že je dostupnost práce doplnění pro poslední kus doplnění (pro prodejní objednávku 2) *Otevřeno*, protože nyní je v místě dostatek prostoru na přijetí doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="2a902-350">Nyní můžete tuto práci na doplňování zpracovat prostřednictvím mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="2a902-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="2a902-351">Přejděte na **Zásoby \> Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="2a902-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="2a902-352">Jste vyzváni, abyste dokončili zbývající práci na doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="2a902-353">Zobrazí se číslo položky, množství a umístění pro vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="2a902-354">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="2a902-355">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="2a902-356">Systém vygeneruje cílové číslo registrační značky pro novou registrační značku pro vybranou položku.</span><span class="sxs-lookup"><span data-stu-id="2a902-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="2a902-357">Hodnotu potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="2a902-358">Je ukázána práce vyskladnění, která dává uživateli pokyn k umístění cílové registrační značky do místa doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="2a902-359">Umístění *Vložení* by mělo být **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="2a902-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="2a902-360">Potvrďte zadané údaje a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="2a902-361">Obdržíte zprávy „Práce dokončena“ a „Žádná práce není k dispozici“.</span><span class="sxs-lookup"><span data-stu-id="2a902-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="2a902-362">Nyní si můžete vybrat prodejní objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="2a902-362">You can now pick sales order 2.</span></span> <span data-ttu-id="2a902-363">Když bylo dokončeno doplňování, které je spojeno s prodejní objednávkou, došlo k jeho odblokování.</span><span class="sxs-lookup"><span data-stu-id="2a902-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="2a902-364">Zadejte ID práce pro prodejní objednávku 2.</span><span class="sxs-lookup"><span data-stu-id="2a902-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="2a902-365">Pro toto pracovní ID existuje pouze jeden výběrový úkol.</span><span class="sxs-lookup"><span data-stu-id="2a902-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="2a902-366">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-366">Select **OK**.</span></span>

    <span data-ttu-id="2a902-367">Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat.</span><span class="sxs-lookup"><span data-stu-id="2a902-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="2a902-368">V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.</span><span class="sxs-lookup"><span data-stu-id="2a902-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="2a902-369">Zadaná registrační značka bude jednou z registračních značek generovaných systémem z pracovního úkolu doplňování.</span><span class="sxs-lookup"><span data-stu-id="2a902-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="2a902-370">Chcete-li se ujistit, že jste zachytili správné ID registrační značky, zkontrolujte zásoby na stránce **Seznam po ruce** pro položku, umístění a množství.</span><span class="sxs-lookup"><span data-stu-id="2a902-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="2a902-371">Vyberte tlačítko **OK** (symbol zaškrtnutí).</span><span class="sxs-lookup"><span data-stu-id="2a902-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="2a902-372">Potvrďte pokyny pro úlohu umístění do odchozího skladového místa.</span><span class="sxs-lookup"><span data-stu-id="2a902-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="2a902-373">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a902-373">Select **OK**.</span></span>

    <span data-ttu-id="2a902-374">Zobrazí se zpráva „Práce dokončena“.</span><span class="sxs-lookup"><span data-stu-id="2a902-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="2a902-375">Poznámky a tipy</span><span class="sxs-lookup"><span data-stu-id="2a902-375">Notes and tips</span></span>

- <span data-ttu-id="2a902-376">Tato funkce pracuje se všemi typy doplňování: požadavek na vlnu, min / max, požadavek na zatížení a slotting.</span><span class="sxs-lookup"><span data-stu-id="2a902-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="2a902-377">Pokud chcete, můžete ručně přepsat dostupnost práce doplňování pro každou hlavičku práce ze stránky **Podrobnosti o práci**.</span><span class="sxs-lookup"><span data-stu-id="2a902-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="2a902-378">Když systém nastaví dostupnost práce při doplňování, vezme v úvahu veškerý inventář, který je již v místě před dokončením jakékoli práce</span><span class="sxs-lookup"><span data-stu-id="2a902-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="2a902-379">Každá část práce na prodejní objednávce je spojena s konkrétní prací na doplnění.</span><span class="sxs-lookup"><span data-stu-id="2a902-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="2a902-380">Neexistuje žádná odpovídající funkce dostupnosti prodejní práce.</span><span class="sxs-lookup"><span data-stu-id="2a902-380">There is no corresponding sales work availability functionality.</span></span>
