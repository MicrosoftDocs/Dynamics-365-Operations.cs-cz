---
title: Skladový slotting
description: Toto téma uvádí informace o skladovém slottingu. Skladový slotting umožňuje konsolidovat poptávku podle položek a měrných jednotek z objednávek, jež jsou ve stavu Objednáno, Rezervováno nebo Uvolněno. Pomáhá skladovým manažerům inteligentně plánovat výdejová skladová místa, než uvolní objednávky do skladu a vytvoří výdejní práce.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 31b86837735ca16610a1d304eab611b12a6aceeb
ms.sourcegitcommit: be4b9d557511bbb43e71a93f2c3b23b5f1a4669d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/24/2020
ms.locfileid: "4627742"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="bdafe-105">Skladový slotting</span><span class="sxs-lookup"><span data-stu-id="bdafe-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdafe-106">Několik funkcí skladového slottingu pomáhá skladovým manažerům inteligentně plánovat výdejová skladová místa, než uvolní objednávky do skladu a vytvoří výdejní práce.</span><span class="sxs-lookup"><span data-stu-id="bdafe-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="bdafe-107">*Funkce Skladový slotting* umožňuje konsolidovat poptávku podle položek a měrných jednotek z objednávek, jež jsou ve stavu *Objednáno*, *Rezervováno* nebo *Uvolněno*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="bdafe-108">Vygenerovanou poptávku je pak možné aplikovat na skladová místa, jež budou použita k výdeji, na základě množství, měrných jednotek, fyzických rozměrů, pevných skladových míst a dalších parametrů.</span><span class="sxs-lookup"><span data-stu-id="bdafe-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="bdafe-109">Poté, co byl vytvořen slottingový plán, je možné vytvořit práce doplňování, aby bylo do každého skladového místa dodáno vhodné množství zásob.</span><span class="sxs-lookup"><span data-stu-id="bdafe-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="bdafe-110">Funkce *Skladový slotting pro převodní příkazy* správcům skladu umožní doplnit místa pro výdej na základě poptávky z převodních příkazů, které ještě nejsou do skladu uvolněny.</span><span class="sxs-lookup"><span data-stu-id="bdafe-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="bdafe-111">Zajišťuje, že místa výdeje budou zahrnovat všechny položky, které jsou vyžadovány pro převodní příkazy po jejich uvolnění do skladu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="bdafe-112">Tato funkce vyžaduje, abyste také zapnuli funkci *Funkce skladového slottingu*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="bdafe-113">Funkce *Vylepšení přidělování slotů pro sklad* přidává možnost pro řádky šablony, které používá vlastnost *Funkce skladového slottingu*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="bdafe-114">Tato možnost umožňuje systému zvážit existující zásoby na skladě v cílovém místě.</span><span class="sxs-lookup"><span data-stu-id="bdafe-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="bdafe-115">Proto by mohlo být generováno méně doplňování pro slotting.</span><span class="sxs-lookup"><span data-stu-id="bdafe-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="bdafe-116">Funkce *Vylepšení přidělování slotů pro sklad* vyžaduje, abyste také zapnuli funkci *Funkce skladového slottingu*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="bdafe-117">Volitelně lze použít společně s funkcí *Skladový slotting pro převodní příkazy*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="bdafe-118">Zapnutí funkcí skladového slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="bdafe-119">Než můžete použít tyto funkce, musíte je zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="bdafe-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="bdafe-120">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav těchto funkcí a dle potřeby je zapnout.</span><span class="sxs-lookup"><span data-stu-id="bdafe-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="bdafe-121">Podle potřeby zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="bdafe-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="bdafe-122">Funkce rozdělení skladu na úseky</span><span class="sxs-lookup"><span data-stu-id="bdafe-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="bdafe-123">Slotting skladu pro převodní příkazy</span><span class="sxs-lookup"><span data-stu-id="bdafe-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="bdafe-124">*Funkce slottingu skladu* musí být před touto funkcí zapnutá.</span><span class="sxs-lookup"><span data-stu-id="bdafe-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="bdafe-125">Rozšíření přidělování slottingu skladu</span><span class="sxs-lookup"><span data-stu-id="bdafe-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="bdafe-126">*Funkce slottingu skladu* musí být před touto funkcí zapnutá.</span><span class="sxs-lookup"><span data-stu-id="bdafe-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="bdafe-127">Nastavení skladového slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-127">Set up warehouse slotting</span></span>

<span data-ttu-id="bdafe-128">Chcete-li používat skladový slottingu, musíte v systému nastavit následující prvky:</span><span class="sxs-lookup"><span data-stu-id="bdafe-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="bdafe-129">Úrovně měrných jednotek slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="bdafe-130">Kódy předpisů</span><span class="sxs-lookup"><span data-stu-id="bdafe-130">Directive codes</span></span>
- <span data-ttu-id="bdafe-131">Šablony slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-131">Slotting templates</span></span>
- <span data-ttu-id="bdafe-132">Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="bdafe-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="bdafe-133">Vytvoření úrovní měrných jednotek pro slotting</span><span class="sxs-lookup"><span data-stu-id="bdafe-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="bdafe-134">Úrovně měrných jednotek umožňují pro účely slottingu seskupovat více měrných jednotek.</span><span class="sxs-lookup"><span data-stu-id="bdafe-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="bdafe-135">Pokud se například ve stejné výdejové oblasti vydávají různé velikosti krabic, lze vytvořit jednu úroveň pro všechny velikosti.</span><span class="sxs-lookup"><span data-stu-id="bdafe-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="bdafe-136">**Pro každou měrnou jednotku, která by měla být součástí úrovně, je třeba vytvořit řádek.**</span><span class="sxs-lookup"><span data-stu-id="bdafe-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="bdafe-137">Přejděte do **Řízení skladu \> Nastavení \> Doplnění \> Úrovně měrných jednotek pro slotting**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="bdafe-138">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-138">Select **New**.</span></span>
1. <span data-ttu-id="bdafe-139">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="bdafe-140">**Úroveň měrné jednotky:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="bdafe-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="bdafe-141">**Popis:** *Každá krabice na paletě*</span><span class="sxs-lookup"><span data-stu-id="bdafe-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="bdafe-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-142">Select **Save**.</span></span>
1. <span data-ttu-id="bdafe-143">Na záložce s náhledem **Měrné jednotky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bdafe-144">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-145">**Jednotka:** *Krabice*</span><span class="sxs-lookup"><span data-stu-id="bdafe-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="bdafe-146">**Popis:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="bdafe-147">Vyplní se automaticky při uložení změn.</span><span class="sxs-lookup"><span data-stu-id="bdafe-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="bdafe-148">**Třída jednotek:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="bdafe-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="bdafe-149">Chcete-li přidat druhý řádek do mřížky, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="bdafe-150">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-151">**Jednotka:** *EA*</span><span class="sxs-lookup"><span data-stu-id="bdafe-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="bdafe-152">**Popis:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="bdafe-153">Vyplní se automaticky při uložení změn.</span><span class="sxs-lookup"><span data-stu-id="bdafe-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="bdafe-154">**Třída jednotek:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="bdafe-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="bdafe-155">Chcete-li přidat třetí řádek do mřížky, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="bdafe-156">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-157">**Jednotka:** *PL*</span><span class="sxs-lookup"><span data-stu-id="bdafe-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="bdafe-158">**Popis:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="bdafe-159">Vyplní se automaticky při uložení změn.</span><span class="sxs-lookup"><span data-stu-id="bdafe-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="bdafe-160">**Třída jednotek:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="bdafe-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="bdafe-161">Kliknutím na tlačítko **Uložit** uložte úroveň.</span><span class="sxs-lookup"><span data-stu-id="bdafe-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="bdafe-162">Vytvoření kódu kód předpisu pro slotting</span><span class="sxs-lookup"><span data-stu-id="bdafe-162">Create a directive code for slotting</span></span>

<span data-ttu-id="bdafe-163">Musíte vybrat kód předpisu, který má být přiřazen k šabloně.</span><span class="sxs-lookup"><span data-stu-id="bdafe-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="bdafe-164">Přejděte na **Řízení skladu \> Nastavení \> Kódy předpisů**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="bdafe-165">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bdafe-166">V poli **Kód předpisu** zadejte hodnotu *Slotting*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="bdafe-167">V poli **Popis předpisu** zadejte hodnotu *Slotting*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="bdafe-168">Nastavení šablon slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-168">Set up slotting templates</span></span>

<span data-ttu-id="bdafe-169">Každá šablona slottingu určuje, jak se přiřazují zásoby do skladových míst v konkrétním skladu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="bdafe-170">Každá šablona musí obsahovat řádek pro každou specifikaci slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="bdafe-171">Postupy v této části využijte k nastavení šablon slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="bdafe-172">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony slottingu**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="bdafe-173">Chcete-li vytvořit šablonu, klikněte na **Nová**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-173">Select **New** to create a template.</span></span>

<span data-ttu-id="bdafe-174">Dále musíte nastavit záhlaví šablony, specifikaci slottingu a směrnice skladového místa, jak se vysvětluje v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="bdafe-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="bdafe-175">Nastavení pro slotting pro převodní příkazy se podobá nastavení pro slotting pro prodejní objednávky, ale pole **Typ poptávky** je nastaveno na *Převodní příkazy* namísto *Prodejní objednávka*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="bdafe-176">Nastavte záhlaví pro šablonu slottingu prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="bdafe-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="bdafe-177">V záhlaví šablony nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="bdafe-178">**Šablona slottingu:** _61_</span><span class="sxs-lookup"><span data-stu-id="bdafe-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="bdafe-179">**Popis:** _61_</span><span class="sxs-lookup"><span data-stu-id="bdafe-179">**Description:** _61_</span></span>
    - <span data-ttu-id="bdafe-180">**Typ poptávky:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="bdafe-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="bdafe-181">V současné době jsou *Prodejní objednávky* a *Převodní příkazy* jediné podporované typy poptávky.</span><span class="sxs-lookup"><span data-stu-id="bdafe-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="bdafe-182">Můžete vybrat *Převodní příkazy* pouze pokud je zapnutá funkce *Skladový slotting pro převodní příkazy*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="bdafe-183">**Strategie poptávky:** _Objednáno_</span><span class="sxs-lookup"><span data-stu-id="bdafe-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="bdafe-184">K dispozici pro toto pole jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="bdafe-185">**Objednáno** – za poptávku je třeba považovat kompletní objednané množství na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="bdafe-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="bdafe-186">**Rezervováno** – pouze rezervovaná (fyzická a objednávaná) množství z řádků objednávek lze považovat za poptávku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="bdafe-187">**Uvolněno** - Uvolněné množství by mělo být považováno za poptávku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="bdafe-188">**Sklad:** _61_</span><span class="sxs-lookup"><span data-stu-id="bdafe-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="bdafe-189">**Povolit použití nerezervovaných množství ve vlnové poptávce:** _Ano_</span><span class="sxs-lookup"><span data-stu-id="bdafe-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="bdafe-190">Můžete také určit dotaz ke zúžení oboru vyhodnocené poptávky.</span><span class="sxs-lookup"><span data-stu-id="bdafe-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="bdafe-191">Nastavení specifikací slottingu pro jednotlivé šablony</span><span class="sxs-lookup"><span data-stu-id="bdafe-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="bdafe-192">Pro každou vytvořenou šablonu prodejní objednávky dle následujících instrukcí přidejte řádek pro každou specifikaci slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="bdafe-193">Na záložce s náhledem **Podrobnosti šablony slottingu** vytvoříte řádek šablony kliknutím na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="bdafe-194">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-195">**Posloupnost:** _1_</span><span class="sxs-lookup"><span data-stu-id="bdafe-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="bdafe-196">**Popis:** _Pevné skladové místo_</span><span class="sxs-lookup"><span data-stu-id="bdafe-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="bdafe-197">**Minimální množství:** _1_</span><span class="sxs-lookup"><span data-stu-id="bdafe-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="bdafe-198">Toto pole definuje minimální množství z poptávky, jež řádek vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="bdafe-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="bdafe-199">**Maximální množství:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="bdafe-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="bdafe-200">Toto pole definuje maximální množství z poptávky, jež je pro daný řádek platné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="bdafe-201">**Jednotka:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="bdafe-202">Toto pole definuje měrnou jednotku, jež se využívá v definici minimálního a maximálního množství.</span><span class="sxs-lookup"><span data-stu-id="bdafe-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="bdafe-203">**Úroveň měrné jednotky:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="bdafe-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="bdafe-204">Toto pole definuje měrné jednotky poptávky, jež jsou pro daný řádek platné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="bdafe-205">(Další informace naleznete v části [Nastavení úrovní měrných jednotek pro slotting](#unit-tiers) výše v tomto tématu.)</span><span class="sxs-lookup"><span data-stu-id="bdafe-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="bdafe-206">**Kritéria přiřazení slotu:** _Zvážit množství_</span><span class="sxs-lookup"><span data-stu-id="bdafe-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="bdafe-207">K dispozici pro toto pole jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="bdafe-208">**Předpokládat prázdné** – tento systém by měl předpokládat, že všechna skladová místa ve výdejové oblasti jsou prázdná a nemělo by se kontrolovat, zda v nich nejsou zásoby.</span><span class="sxs-lookup"><span data-stu-id="bdafe-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="bdafe-209">**Zvážit množství** – tento systém by měl kontrolovat skladová míst ve výdejové oblasti, aby v nich nebyly zásoby; pokud narazí na skladová místa, jež nejsou prázdná, měl by je přeskočit.</span><span class="sxs-lookup"><span data-stu-id="bdafe-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="bdafe-210">**Zohlednění stavu na skladě** - Systém by měl zkontrolovat, zda nějaké cílové umístění obsahuje nerezervovaná množství pro položku na řádku poptávky.</span><span class="sxs-lookup"><span data-stu-id="bdafe-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="bdafe-211">Pokud je množství dostatečně velké, aby uspokojilo alespoň jednu jednotku řádku poptávky, vygenerovaný záznam plánu slottingu se sníží o dostupné množství.</span><span class="sxs-lookup"><span data-stu-id="bdafe-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="bdafe-212">Například, pokud je poptávka 10 beden a je k dispozici jedna bedna, bude lokalizovaná poptávka devět beden.</span><span class="sxs-lookup"><span data-stu-id="bdafe-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="bdafe-213">Pokud je poptávka 10 beden a je k dispozici je každá, bude lokalizovaná poptávka 10 beden.</span><span class="sxs-lookup"><span data-stu-id="bdafe-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="bdafe-214">Tato hodnota je k dispozici pouze v případě, že je zapnuta funkce *Rozšíření přidělování slottingu skladu*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="bdafe-215">**Kód předpisu:** _Slotting_</span><span class="sxs-lookup"><span data-stu-id="bdafe-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="bdafe-216">Toto pole definuje směrnici skladového místa, jež se používá k vyhledání skladového místa práce doplňování.</span><span class="sxs-lookup"><span data-stu-id="bdafe-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="bdafe-217">**Skladové místo pro přeplnění:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="bdafe-218">Toto pole definuje skladové místo, do něhož se naskladňují zásoby, pokud se při zpracování řádku nedaří najít skladové místo pro dané množství.</span><span class="sxs-lookup"><span data-stu-id="bdafe-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="bdafe-219">**Povolit přerušení:** _Ano_</span><span class="sxs-lookup"><span data-stu-id="bdafe-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="bdafe-220">Je-li u této možnosti nastavena hodnota *Ano*, v případě, že u určité poptávky nelze provést slotting, se vytvoří pohyb, kterým budou zásoby odebrány ze skladových míst, kde se nacházejí zásoby, ale kde nic nebylo zpracováno pomocí slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="bdafe-221">Šablona se poté spustí znovu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-221">The template is then run again.</span></span> <span data-ttu-id="bdafe-222">Tentokrát bude ignorovat zásoby v daných skladových místech.</span><span class="sxs-lookup"><span data-stu-id="bdafe-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="bdafe-223">Tato funkce funguje nejlépe, když je v poli **Kritéria přiřazení slotu** zadána hodnota _Zvážit množství_.</span><span class="sxs-lookup"><span data-stu-id="bdafe-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="bdafe-224">**Použití pevného skladového místa:** _Pouze pevná skladová místa pro produkt_</span><span class="sxs-lookup"><span data-stu-id="bdafe-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="bdafe-225">K dispozici pro toto pole jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="bdafe-226">**Pevná a nepevná skladová místa** – systém by se neměl omezovat na použití pouze pevných skladových míst.</span><span class="sxs-lookup"><span data-stu-id="bdafe-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="bdafe-227">**Pouze pevná skladová místa pro produkt** – systém by měl provádět slotting pouze na skladová místa, jež jsou pro produkt pevnými skladovými místy.</span><span class="sxs-lookup"><span data-stu-id="bdafe-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="bdafe-228">**Pouze pevná skladová místa pro variantu produktu** – systém by měl provádět slotting pouze na skladová místa, jež jsou pro variantu produktu pevnými skladovými místy.</span><span class="sxs-lookup"><span data-stu-id="bdafe-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="bdafe-229">Pokud šablona slottingu obsahuje alespoň jeden řádek, kde je pole **Přiřaďte kritéria slotu** nastaveno na *Zohlednění stavu na skladě*, pro jakýkoli řádek v šabloně již nejsou povolena přerušení.</span><span class="sxs-lookup"><span data-stu-id="bdafe-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="bdafe-230">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-230">Select **Save**.</span></span>
1. <span data-ttu-id="bdafe-231">Chcete-li vytvořit druhý řádek šablony, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="bdafe-232">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-233">**Posloupnost:** _2_</span><span class="sxs-lookup"><span data-stu-id="bdafe-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="bdafe-234">**Popis:** _Jiný_</span><span class="sxs-lookup"><span data-stu-id="bdafe-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="bdafe-235">**Minimální množství:** _1_</span><span class="sxs-lookup"><span data-stu-id="bdafe-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="bdafe-236">**Maximální množství:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="bdafe-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="bdafe-237">**Jednotka:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="bdafe-238">**Úroveň měrné jednotky:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="bdafe-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="bdafe-239">**Kritéria přiřazení slotu:** _Zvážit množství_</span><span class="sxs-lookup"><span data-stu-id="bdafe-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="bdafe-240">**Kód předpisu:** _Slotting_</span><span class="sxs-lookup"><span data-stu-id="bdafe-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="bdafe-241">**Skladové místo pro přeplnění:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="bdafe-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="bdafe-242">**Povolit přerušení:** _Ano_</span><span class="sxs-lookup"><span data-stu-id="bdafe-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="bdafe-243">**Použít pevná skladová místa:** _Pevná a nepevná skladová místa_</span><span class="sxs-lookup"><span data-stu-id="bdafe-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="bdafe-244">V dotazu pro druhý řádek nyní určíte kritéria, jež se použijí k určení skladových míst, na něž může proběhnout slotting poptávky z příslušného řádku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="bdafe-245">Vyberte řádek, kde má pole **Pořadí** nastavenou hodnotu *2*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="bdafe-246">Vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="bdafe-247">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="bdafe-248">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-249">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="bdafe-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="bdafe-250">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="bdafe-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="bdafe-251">**Pole:** *ID profilu skladového místa*</span><span class="sxs-lookup"><span data-stu-id="bdafe-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="bdafe-252">**Kritéria:** *Výdej-06* (Klikněte v poli na dvojité plus \[**++**\], rozbalí se seznam, poté vyberte *Výdej-06* - *Výdejová lokalita 6*.)</span><span class="sxs-lookup"><span data-stu-id="bdafe-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="bdafe-253">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="bdafe-254">Nastavit směrnice skladových míst</span><span class="sxs-lookup"><span data-stu-id="bdafe-254">Set up location directives</span></span>

<span data-ttu-id="bdafe-255">Musí se nastavit alespoň jedna směrnice skladového místa, jež bude podporovat výběr slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="bdafe-256">Chcete-li nastavit novou *směrnici skladového místa doplnění* pro skladová místa podporující výběr slottingu, využijte procedury popsané v této části.</span><span class="sxs-lookup"><span data-stu-id="bdafe-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="bdafe-257">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="bdafe-258">V levém podokně vyberte v poli **Typ pracovního příkazu** hodnotu *Doplnění*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="bdafe-259">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bdafe-260">V záhlaví nové směrnice skladového místa zadejte v poli **Název** hodnotu *61 Výběr slotu*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="bdafe-261">V poli **Pořadové číslo** přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="bdafe-262">Konfigurace záložky s náhledem pro Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="bdafe-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="bdafe-263">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="bdafe-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="bdafe-264">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="bdafe-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="bdafe-265">**Typ práce:** _Výdej_</span><span class="sxs-lookup"><span data-stu-id="bdafe-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="bdafe-266">**Lokalita:** _6_</span><span class="sxs-lookup"><span data-stu-id="bdafe-266">**Site:** _6_</span></span>
    - <span data-ttu-id="bdafe-267">**Sklad:** _61_</span><span class="sxs-lookup"><span data-stu-id="bdafe-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="bdafe-268">**Kód předpisu:** _Slotting_</span><span class="sxs-lookup"><span data-stu-id="bdafe-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="bdafe-269">Chcete-li, aby byla dostupná záložka s náhledem **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="bdafe-270">Konfigurace záložky s náhledem Řádky</span><span class="sxs-lookup"><span data-stu-id="bdafe-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="bdafe-271">Na záložce s náhledem **Řádky** vytvořte řádek výběrem tlačítka **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="bdafe-272">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="bdafe-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="bdafe-273">**Od množství:** _0_</span><span class="sxs-lookup"><span data-stu-id="bdafe-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="bdafe-274">**Do množství:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="bdafe-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="bdafe-275">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="bdafe-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="bdafe-276">Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="bdafe-277">Konfigurace záložky s náhledem pro Akce směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="bdafe-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="bdafe-278">Na záložce s náhledem **Akce směrnice skladového místa** vytvořte řádek výběrem tlačítka **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="bdafe-279">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="bdafe-279">On the new line, set the following values.</span></span> <span data-ttu-id="bdafe-280">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="bdafe-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="bdafe-281">**Pořadové číslo:** Přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="bdafe-282">**Název:** _Hromadný_</span><span class="sxs-lookup"><span data-stu-id="bdafe-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="bdafe-283">**Strategie:** _Žádná_</span><span class="sxs-lookup"><span data-stu-id="bdafe-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="bdafe-284">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="bdafe-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="bdafe-285">Kliknutím na **Uložit** zpřístupníte tlačítko **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="bdafe-286">Upravit dotaz</span><span class="sxs-lookup"><span data-stu-id="bdafe-286">Edit the query</span></span>

1. <span data-ttu-id="bdafe-287">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="bdafe-288">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="bdafe-289">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-290">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="bdafe-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="bdafe-291">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="bdafe-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="bdafe-292">**Pole:** *ID zóny*</span><span class="sxs-lookup"><span data-stu-id="bdafe-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="bdafe-293">**Kritéria:** *Hromadné* (Klikněte v poli na dvojité plus \[**++**\], rozbalí se seznam, poté vyberte *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="bdafe-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="bdafe-294">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="bdafe-295">Scénář</span><span class="sxs-lookup"><span data-stu-id="bdafe-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="bdafe-296">Nastavení scénáře</span><span class="sxs-lookup"><span data-stu-id="bdafe-296">Set up the scenario</span></span>

<span data-ttu-id="bdafe-297">Pro tento scénář použijte předdefinovaná ukázková data a vytvořte záznamy, jak se popisuje v této části.</span><span class="sxs-lookup"><span data-stu-id="bdafe-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="bdafe-298">Použití ukázkových dat USMF</span><span class="sxs-lookup"><span data-stu-id="bdafe-298">Use the USMF sample data</span></span>

<span data-ttu-id="bdafe-299">Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="bdafe-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bdafe-300">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="bdafe-301">Vytvoření poptávky</span><span class="sxs-lookup"><span data-stu-id="bdafe-301">Create demand</span></span>

<span data-ttu-id="bdafe-302">Postupujte podle těchto kroků a vytvořte poptávku, na kterou použijete slotting.</span><span class="sxs-lookup"><span data-stu-id="bdafe-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="bdafe-303">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="bdafe-304">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="bdafe-305">V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu _US-007_.</span><span class="sxs-lookup"><span data-stu-id="bdafe-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="bdafe-306">V poli **Sklad** zvolte _61_.</span><span class="sxs-lookup"><span data-stu-id="bdafe-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="bdafe-307">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-307">Select **OK**.</span></span>
1. <span data-ttu-id="bdafe-308">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="bdafe-308">The new sales order is opened.</span></span> <span data-ttu-id="bdafe-309">Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bdafe-310">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-311">**Položka:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="bdafe-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="bdafe-312">**Množství:** _20_</span><span class="sxs-lookup"><span data-stu-id="bdafe-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="bdafe-313">Chcete-li přidat nový řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="bdafe-314">**Položka:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="bdafe-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="bdafe-315">**Množství:** _8_</span><span class="sxs-lookup"><span data-stu-id="bdafe-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="bdafe-316">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-316">Select **Save**.</span></span>
1. <span data-ttu-id="bdafe-317">Klepnutím na možnost **Nová** vytvořte druhou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="bdafe-318">V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu _US-008_.</span><span class="sxs-lookup"><span data-stu-id="bdafe-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="bdafe-319">V poli **Sklad** zvolte _61_.</span><span class="sxs-lookup"><span data-stu-id="bdafe-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="bdafe-320">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="bdafe-320">The new sales order is opened.</span></span> <span data-ttu-id="bdafe-321">Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bdafe-322">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="bdafe-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="bdafe-323">**Položka:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="bdafe-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="bdafe-324">**Množství:** _1_</span><span class="sxs-lookup"><span data-stu-id="bdafe-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="bdafe-325">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="bdafe-326">Vyzkoušení obvyklého scénáře slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="bdafe-327">Když jsou splněny všechny nezbytné předpoklady, jak se popisuje v předchozí části, můžete vyzkoušet tuto funkci pomocí cvičení v této části.</span><span class="sxs-lookup"><span data-stu-id="bdafe-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="bdafe-328">Generovat poptávku</span><span class="sxs-lookup"><span data-stu-id="bdafe-328">Generate demand</span></span>

1. <span data-ttu-id="bdafe-329">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony slottingu** a vyberte šablonu slottingu, kterou jste předtím vytvořili.</span><span class="sxs-lookup"><span data-stu-id="bdafe-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="bdafe-330">V podokně Akce klikněte na možnost **Generovat poptávku**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="bdafe-331">Tento příkaz vyhodnocuje veškerou poptávku, jež se nachází v systému a shoduje se s dotazem dle šablony slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="bdafe-332">Celková poptávka napříč všemi objednávkami je pak konsolidována do jednoho řádku na množství / měrnou jednotku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="bdafe-333">Po dokončení procesu se zobrazí informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="bdafe-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="bdafe-334">Poptávka na slotting</span><span class="sxs-lookup"><span data-stu-id="bdafe-334">Slotting demand</span></span>

<span data-ttu-id="bdafe-335">*Poptávka na slotting* ukazuje výsledky generování poptávky na základě nastavení šablony slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="bdafe-336">V podokně Akce vyberte **poptávka na slotting**, zobrazí se výsledky příkazu **Generovat poptávku**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="bdafe-337">Řádky poptávky na slotting lze upravovat.</span><span class="sxs-lookup"><span data-stu-id="bdafe-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="bdafe-338">Můžete smazat řádek, přidat nový řádek nebo upravit podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="bdafe-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="bdafe-339">Poptávku lze upravit ručně nebo ji můžete importovat z externího systému pomocí správy dat.</span><span class="sxs-lookup"><span data-stu-id="bdafe-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="bdafe-340">Ať už je v poptávce na slotting cokoli, bude to použito v dalším kroku, bez ohledu na to, odkud to bylo získáno.</span><span class="sxs-lookup"><span data-stu-id="bdafe-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="bdafe-341">Vyhledat poptávku</span><span class="sxs-lookup"><span data-stu-id="bdafe-341">Locate demand</span></span>

<span data-ttu-id="bdafe-342">Po vygenerování poptávky musíte použít příkaz **Vyhledat poptávku** k vygenerování *plánu slottingu*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="bdafe-343">V podokně Akce klikněte na možnost **Vyhledat poptávku**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="bdafe-344">Spustí se proces slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-344">The slotting process runs.</span></span> <span data-ttu-id="bdafe-345">Po dokončení procesu se zobrazí informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="bdafe-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="bdafe-346">Plán slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-346">Slotting plan</span></span>

<span data-ttu-id="bdafe-347">Plán slottingu ukazuje skladová místa, k nimž byly přiřazeny jednotlivé položky a jednotlivá množství, zda bylo použito přeplnění, zda byla vytvořena práce s přerušením a jaká šablona bylo pro daný řádek použita.</span><span class="sxs-lookup"><span data-stu-id="bdafe-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="bdafe-348">*Jakákoli poptávka, která nemohla být zpracována formou slottingu, se zvýrazní červeně.*</span><span class="sxs-lookup"><span data-stu-id="bdafe-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="bdafe-349">V podokně Akce vyberte **Plán slottingu**, zobrazí se výsledky.</span><span class="sxs-lookup"><span data-stu-id="bdafe-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="bdafe-350">Procesy **Generovat poptávku**, **Vyhledat poptávku** a **Spustit doplňování** nyní běží v sandboxu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="bdafe-351">(Tyto procesy jsou k dispozici v podokně akcí na stránce **Šablony slottingu**.)</span><span class="sxs-lookup"><span data-stu-id="bdafe-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="bdafe-352">Procesy **Generovat poptávku**, **Vyhledat poptávku** a **Spustit doplňování** mají zámek, který zajišťuje, že nemohou být spuštěny současně.</span><span class="sxs-lookup"><span data-stu-id="bdafe-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="bdafe-353">V opačném případě mohou být použitá data odstraněna.</span><span class="sxs-lookup"><span data-stu-id="bdafe-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="bdafe-354">Procesy **Generovat poptávku** a **Vyhledat poptávku** zobrazují varování, pokud běh negeneroval záznamy nebo pokud záznamům chybí informace.</span><span class="sxs-lookup"><span data-stu-id="bdafe-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="bdafe-355">Když vyberete **Plán slottingu**, stránka neobsahuje tlačítka **Nový**, **Upravit** nebo **Odstranit** v podokně akcí, protože zdroj dat nelze upravovat.</span><span class="sxs-lookup"><span data-stu-id="bdafe-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="bdafe-356">Když vyberete **Spustit doplňování**, systém ověří vybranou šablonu slotu a procesy.</span><span class="sxs-lookup"><span data-stu-id="bdafe-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="bdafe-357">Vytvoření doplnění</span><span class="sxs-lookup"><span data-stu-id="bdafe-357">Create replenishment</span></span>

<span data-ttu-id="bdafe-358">Po vytvoření plánu slottingu musíte na základě tohoto plánu vytvořit *práce doplnění*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="bdafe-359">V podokně Akce zvolte **Spustit doplnění**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="bdafe-360">Po dokončení procesu se zobrazí informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="bdafe-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="bdafe-361">Tato zpráva označuje počet záhlaví, jež byla vytvořena pro ID sestavení práce.</span><span class="sxs-lookup"><span data-stu-id="bdafe-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="bdafe-362">Směrnice skladového místa, jež budou použity, se identifikují na základě kódu předpisu, který je specifikován na každém řádku šablony.</span><span class="sxs-lookup"><span data-stu-id="bdafe-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="bdafe-363">Tipy</span><span class="sxs-lookup"><span data-stu-id="bdafe-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="bdafe-364">Nastavení automatického slottingu</span><span class="sxs-lookup"><span data-stu-id="bdafe-364">Set up automatic slotting</span></span>

<span data-ttu-id="bdafe-365">Po přípravě všech povinných prvků můžete nastavit automatizaci slottingu tak, aby se slotting prováděl automaticky. Postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="bdafe-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="bdafe-366">Přejděte na **Řízení skladu \> Doplnění \> Provádění slottingu**.</span><span class="sxs-lookup"><span data-stu-id="bdafe-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="bdafe-367">Určete kroky slottingu, jež se mají provést.</span><span class="sxs-lookup"><span data-stu-id="bdafe-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="bdafe-368">Vyberte jeden nebo více z následujících kroků slottingu:</span><span class="sxs-lookup"><span data-stu-id="bdafe-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="bdafe-369">Generovat poptávku</span><span class="sxs-lookup"><span data-stu-id="bdafe-369">Generate demand</span></span>
    - <span data-ttu-id="bdafe-370">Vyhledat poptávku</span><span class="sxs-lookup"><span data-stu-id="bdafe-370">Locate demand</span></span>
    - <span data-ttu-id="bdafe-371">Vytvořit práci doplnění</span><span class="sxs-lookup"><span data-stu-id="bdafe-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="bdafe-372">Kroky slottingu jsou progresivní.</span><span class="sxs-lookup"><span data-stu-id="bdafe-372">The slotting steps are progressive.</span></span> <span data-ttu-id="bdafe-373">Pokud chcete vybrat krok *Vyhledat poptávku*, musíte nejprve vybrat *Generovat poptávku*.</span><span class="sxs-lookup"><span data-stu-id="bdafe-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="bdafe-374">Určete šablonu slottingu, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="bdafe-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="bdafe-375">Pokud chcete spouštět běh automaticky, nastavte opakování.</span><span class="sxs-lookup"><span data-stu-id="bdafe-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="bdafe-376">Pro cvičení ve scénáři **nenastavujte** automatické spouštění slottingu.</span><span class="sxs-lookup"><span data-stu-id="bdafe-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
