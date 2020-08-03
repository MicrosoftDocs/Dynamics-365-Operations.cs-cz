---
title: Skladový slotting
description: Toto téma uvádí informace o skladovém slottingu. Skladový slotting umožňuje konsolidovat poptávku podle položek a měrných jednotek z objednávek, jež jsou ve stavu Objednáno, Rezervováno nebo Uvolněno. Pomáhá skladovým manažerům inteligentně plánovat výdejová skladová místa, než uvolní objednávky do skladu a vytvoří výdejní práce.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f6764f8bc082962af37d4775b6fe53d8704658eb
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597451"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="04475-105">Skladový slotting</span><span class="sxs-lookup"><span data-stu-id="04475-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04475-106">Skladový slotting umožňuje konsolidovat poptávku podle položek a měrných jednotek z objednávek, jež jsou ve stavu *Objednáno*, *Rezervováno* nebo *Uvolněno*.</span><span class="sxs-lookup"><span data-stu-id="04475-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="04475-107">Vygenerovanou poptávku je pak možné aplikovat na skladová místa, jež budou použita k výdeji, na základě množství, měrných jednotek, fyzických rozměrů, pevných skladových míst a dalších parametrů.</span><span class="sxs-lookup"><span data-stu-id="04475-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="04475-108">Poté, co byl vytvořen slottingový plán, je možné vytvořit práce doplňování, aby bylo do každého skladového místa dodáno vhodné množství zásob.</span><span class="sxs-lookup"><span data-stu-id="04475-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="04475-109">Tato funkce pomáhá skladovým manažerům inteligentně plánovat výdejová skladová místa, než uvolní objednávky do skladu a vytvoří výdejní práce.</span><span class="sxs-lookup"><span data-stu-id="04475-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="04475-110">Zapnutí funkce skladového slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="04475-111">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="04475-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="04475-112">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="04475-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="04475-113">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="04475-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="04475-114">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="04475-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="04475-115">**Název funkce:** *Funkce skladového slottingu*</span><span class="sxs-lookup"><span data-stu-id="04475-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="04475-116">Nastavení skladového slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-116">Set up warehouse slotting</span></span>

<span data-ttu-id="04475-117">Chcete-li používat skladový slottingu, musíte v systému nastavit následující prvky.</span><span class="sxs-lookup"><span data-stu-id="04475-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="04475-118">Vytvoření úrovní měrných jednotek pro slotting</span><span class="sxs-lookup"><span data-stu-id="04475-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="04475-119">Úrovně měrných jednotek umožňují pro účely slottingu seskupovat více měrných jednotek.</span><span class="sxs-lookup"><span data-stu-id="04475-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="04475-120">Pokud se například ve stejné výdejové oblasti vydávají různé velikosti krabic, lze vytvořit jednu úroveň pro všechny velikosti.</span><span class="sxs-lookup"><span data-stu-id="04475-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="04475-121">**Pro každou měrnou jednotku, která by měla být součástí úrovně, je třeba vytvořit řádek.**</span><span class="sxs-lookup"><span data-stu-id="04475-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="04475-122">Přejděte do **Řízení skladu \> Nastavení \> Doplnění \> Úrovně měrných jednotek pro slotting**.</span><span class="sxs-lookup"><span data-stu-id="04475-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="04475-123">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04475-123">Select **New**.</span></span>
1. <span data-ttu-id="04475-124">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="04475-125">**Úroveň měrné jednotky:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="04475-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="04475-126">**Popis:** *Každá krabice na paletě*</span><span class="sxs-lookup"><span data-stu-id="04475-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="04475-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04475-127">Select **Save**.</span></span>
1. <span data-ttu-id="04475-128">Na záložce s náhledem **Měrné jednotky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="04475-129">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-130">**Jednotka:** *Krabice*</span><span class="sxs-lookup"><span data-stu-id="04475-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="04475-131">**Popis:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="04475-132">Vyplní se automaticky při uložení změn.</span><span class="sxs-lookup"><span data-stu-id="04475-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="04475-133">**Třída jednotek:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="04475-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="04475-134">Chcete-li přidat druhý řádek do mřížky, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="04475-135">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-136">**Jednotka:** *EA*</span><span class="sxs-lookup"><span data-stu-id="04475-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="04475-137">**Popis:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="04475-138">Vyplní se automaticky při uložení změn.</span><span class="sxs-lookup"><span data-stu-id="04475-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="04475-139">**Třída jednotek:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="04475-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="04475-140">Chcete-li přidat třetí řádek do mřížky, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="04475-141">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-142">**Jednotka:** *PL*</span><span class="sxs-lookup"><span data-stu-id="04475-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="04475-143">**Popis:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="04475-144">Vyplní se automaticky při uložení změn.</span><span class="sxs-lookup"><span data-stu-id="04475-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="04475-145">**Třída jednotek:** *Množství*</span><span class="sxs-lookup"><span data-stu-id="04475-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="04475-146">Kliknutím na tlačítko **Uložit** uložte úroveň.</span><span class="sxs-lookup"><span data-stu-id="04475-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="04475-147">Vytvoření kódu kód předpisu pro slotting</span><span class="sxs-lookup"><span data-stu-id="04475-147">Create a directive code for slotting</span></span>

<span data-ttu-id="04475-148">Musíte vybrat kód předpisu, který má být přiřazen k šabloně.</span><span class="sxs-lookup"><span data-stu-id="04475-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="04475-149">Přejděte na **Řízení skladu \> Nastavení \> Kódy předpisů**.</span><span class="sxs-lookup"><span data-stu-id="04475-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="04475-150">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="04475-151">V poli **Kód předpisu** zadejte hodnotu *Slotting*.</span><span class="sxs-lookup"><span data-stu-id="04475-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="04475-152">V poli **Popis předpisu** zadejte hodnotu *Slotting*.</span><span class="sxs-lookup"><span data-stu-id="04475-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="04475-153">Nastavení šablon slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-153">Set up slotting templates</span></span>

<span data-ttu-id="04475-154">Každá šablona slottingu určuje, jak se přiřazují zásoby do skladových míst v konkrétním skladu.</span><span class="sxs-lookup"><span data-stu-id="04475-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="04475-155">Každá šablona musí obsahovat řádek pro každou specifikaci slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="04475-156">Postupy v této části využijte k nastavení šablon slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="04475-157">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony slottingu**.</span><span class="sxs-lookup"><span data-stu-id="04475-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="04475-158">Chcete-li vytvořit šablonu, klikněte na **Nová**.</span><span class="sxs-lookup"><span data-stu-id="04475-158">Select **New** to create a template.</span></span>

<span data-ttu-id="04475-159">Dále musíte nastavit záhlaví šablony, specifikaci slottingu a směrnice skladového místa, jak se vysvětluje v následujících částech.</span><span class="sxs-lookup"><span data-stu-id="04475-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="04475-160">Nastavení záhlaví šablony slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="04475-161">V záhlaví šablony nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="04475-162">**Šablona slottingu:** _61_</span><span class="sxs-lookup"><span data-stu-id="04475-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="04475-163">**Popis:** _61_</span><span class="sxs-lookup"><span data-stu-id="04475-163">**Description:** _61_</span></span>
    - <span data-ttu-id="04475-164">**Typ poptávky:** *Prodejní objednávka*</span><span class="sxs-lookup"><span data-stu-id="04475-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="04475-165">V současné době je jediný podporovaný typ poptávky *Prodejní objednávka*.</span><span class="sxs-lookup"><span data-stu-id="04475-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="04475-166">**Strategie poptávky:** _Objednáno_</span><span class="sxs-lookup"><span data-stu-id="04475-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="04475-167">K dispozici pro toto pole jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="04475-168">**Objednáno** – za poptávku je třeba považovat kompletní objednané množství na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="04475-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="04475-169">**Rezervováno** – pouze rezervovaná (fyzická a objednávaná) množství z řádků objednávek lze považovat za poptávku.</span><span class="sxs-lookup"><span data-stu-id="04475-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="04475-170">**Sklad:** _61_</span><span class="sxs-lookup"><span data-stu-id="04475-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="04475-171">**Povolit použití nerezervovaných množství ve vlnové poptávce:** _Ano_</span><span class="sxs-lookup"><span data-stu-id="04475-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="04475-172">Můžete také určit dotaz ke zúžení oboru vyhodnocené poptávky.</span><span class="sxs-lookup"><span data-stu-id="04475-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="04475-173">Nastavení specifikací slottingu pro jednotlivé šablony</span><span class="sxs-lookup"><span data-stu-id="04475-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="04475-174">Pro každou vytvořenou šablonu přidejte pro každou specifikaci slottingu řádek. Postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="04475-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="04475-175">Na záložce s náhledem **Podrobnosti šablony slottingu** vytvoříte řádek šablony kliknutím na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="04475-176">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-177">**Posloupnost:** _1_</span><span class="sxs-lookup"><span data-stu-id="04475-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="04475-178">**Popis:** _Pevné skladové místo_</span><span class="sxs-lookup"><span data-stu-id="04475-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="04475-179">**Minimální množství:** _1_</span><span class="sxs-lookup"><span data-stu-id="04475-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="04475-180">Toto pole definuje minimální množství z poptávky, jež řádek vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="04475-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="04475-181">**Maximální množství:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="04475-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="04475-182">Toto pole definuje maximální množství z poptávky, jež je pro daný řádek platné.</span><span class="sxs-lookup"><span data-stu-id="04475-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="04475-183">**Jednotka:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="04475-184">Toto pole definuje měrnou jednotku, jež se využívá v definici minimálního a maximálního množství.</span><span class="sxs-lookup"><span data-stu-id="04475-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="04475-185">**Úroveň měrné jednotky:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="04475-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="04475-186">Toto pole definuje měrné jednotky poptávky, jež jsou pro daný řádek platné.</span><span class="sxs-lookup"><span data-stu-id="04475-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="04475-187">(Další informace naleznete v části [Nastavení úrovní měrných jednotek pro slotting](#unit-tiers) výše v tomto tématu.)</span><span class="sxs-lookup"><span data-stu-id="04475-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="04475-188">**Kritéria přiřazení slotu:** _Zvážit množství_</span><span class="sxs-lookup"><span data-stu-id="04475-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="04475-189">K dispozici pro toto pole jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="04475-190">**Předpokládat prázdné** – tento systém by měl předpokládat, že všechna skladová místa ve výdejové oblasti jsou prázdná a nemělo by se kontrolovat, zda v nich nejsou zásoby.</span><span class="sxs-lookup"><span data-stu-id="04475-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="04475-191">**Zvážit množství** – tento systém by měl kontrolovat skladová míst ve výdejové oblasti, aby v nich nebyly zásoby; pokud narazí na skladová místa, jež nejsou prázdná, měl by je přeskočit.</span><span class="sxs-lookup"><span data-stu-id="04475-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="04475-192">**Kód předpisu:** _Slotting_</span><span class="sxs-lookup"><span data-stu-id="04475-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="04475-193">Toto pole definuje směrnici skladového místa, jež se používá k vyhledání skladového místa práce doplňování.</span><span class="sxs-lookup"><span data-stu-id="04475-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="04475-194">**Skladové místo pro přeplnění:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="04475-195">Toto pole definuje skladové místo, do něhož se naskladňují zásoby, pokud se při zpracování řádku nedaří najít skladové místo pro dané množství.</span><span class="sxs-lookup"><span data-stu-id="04475-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="04475-196">**Povolit přerušení:** _Ano_</span><span class="sxs-lookup"><span data-stu-id="04475-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="04475-197">Je-li u této možnosti nastavena hodnota *Ano*, v případě, že u určité poptávky nelze provést slotting, se vytvoří pohyb, kterým budou zásoby odebrány ze skladových míst, kde se nacházejí zásoby, ale kde nic nebylo zpracováno pomocí slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="04475-198">Šablona se poté spustí znovu.</span><span class="sxs-lookup"><span data-stu-id="04475-198">The template is then run again.</span></span> <span data-ttu-id="04475-199">Tentokrát bude ignorovat zásoby v daných skladových místech.</span><span class="sxs-lookup"><span data-stu-id="04475-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="04475-200">Tato funkce funguje nejlépe, když je v poli **Kritéria přiřazení slotu** zadána hodnota _Zvážit množství_.</span><span class="sxs-lookup"><span data-stu-id="04475-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="04475-201">**Použití pevného skladového místa:** _Pouze pevná skladová místa pro produkt_</span><span class="sxs-lookup"><span data-stu-id="04475-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="04475-202">K dispozici pro toto pole jsou následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="04475-203">**Pevná a nepevná skladová místa** – systém by se neměl omezovat na použití pouze pevných skladových míst.</span><span class="sxs-lookup"><span data-stu-id="04475-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="04475-204">**Pouze pevná skladová místa pro produkt** – systém by měl provádět slotting pouze na skladová místa, jež jsou pro produkt pevnými skladovými místy.</span><span class="sxs-lookup"><span data-stu-id="04475-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="04475-205">**Pouze pevná skladová místa pro variantu produktu** – systém by měl provádět slotting pouze na skladová místa, jež jsou pro variantu produktu pevnými skladovými místy.</span><span class="sxs-lookup"><span data-stu-id="04475-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="04475-206">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04475-206">Select **Save**.</span></span>
1. <span data-ttu-id="04475-207">Chcete-li vytvořit druhý řádek šablony, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="04475-208">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-209">**Posloupnost:** _2_</span><span class="sxs-lookup"><span data-stu-id="04475-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="04475-210">**Popis:** _Jiný_</span><span class="sxs-lookup"><span data-stu-id="04475-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="04475-211">**Minimální množství:** _1_</span><span class="sxs-lookup"><span data-stu-id="04475-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="04475-212">**Maximální množství:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="04475-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="04475-213">**Jednotka:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="04475-214">**Úroveň měrné jednotky:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="04475-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="04475-215">**Kritéria přiřazení slotu:** _Zvážit množství_</span><span class="sxs-lookup"><span data-stu-id="04475-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="04475-216">**Kód předpisu:** _Slotting_</span><span class="sxs-lookup"><span data-stu-id="04475-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="04475-217">**Skladové místo pro přeplnění:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="04475-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="04475-218">**Povolit přerušení:** _Ano_</span><span class="sxs-lookup"><span data-stu-id="04475-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="04475-219">**Použít pevná skladová místa:** _Pevná a nepevná skladová místa_</span><span class="sxs-lookup"><span data-stu-id="04475-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="04475-220">V dotazu pro druhý řádek nyní určíte kritéria, jež se použijí k určení skladových míst, na něž může proběhnout slotting poptávky z příslušného řádku.</span><span class="sxs-lookup"><span data-stu-id="04475-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="04475-221">Vyberte řádek, kde má pole **Pořadí** nastavenou hodnotu *2*.</span><span class="sxs-lookup"><span data-stu-id="04475-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="04475-222">Vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="04475-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="04475-223">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="04475-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="04475-224">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-225">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="04475-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="04475-226">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="04475-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="04475-227">**Pole:** *ID profilu skladového místa*</span><span class="sxs-lookup"><span data-stu-id="04475-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="04475-228">**Kritéria:** *Výdej-06* (Klikněte v poli na dvojité plus \[**++**\], rozbalí se seznam, poté vyberte *Výdej-06* - *Výdejová lokalita 6*.)</span><span class="sxs-lookup"><span data-stu-id="04475-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="04475-229">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04475-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="04475-230">Nastavit směrnice skladových míst</span><span class="sxs-lookup"><span data-stu-id="04475-230">Set up location directives</span></span>

<span data-ttu-id="04475-231">Musí se nastavit alespoň jedna směrnice skladového místa, jež bude podporovat výběr slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="04475-232">Chcete-li nastavit novou *směrnici skladového místa doplnění* pro skladová místa podporující výběr slottingu, využijte procedury popsané v této části.</span><span class="sxs-lookup"><span data-stu-id="04475-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="04475-233">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="04475-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="04475-234">V levém podokně vyberte v poli **Typ pracovního příkazu** hodnotu *Doplnění*.</span><span class="sxs-lookup"><span data-stu-id="04475-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="04475-235">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="04475-236">V záhlaví nové směrnice skladového místa zadejte v poli **Název** hodnotu *61 Výběr slotu*.</span><span class="sxs-lookup"><span data-stu-id="04475-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="04475-237">Konfigurace záložky s náhledem pro Směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="04475-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="04475-238">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="04475-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="04475-239">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="04475-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="04475-240">**Typ práce:** _Výdej_</span><span class="sxs-lookup"><span data-stu-id="04475-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="04475-241">**Lokalita:** _6_</span><span class="sxs-lookup"><span data-stu-id="04475-241">**Site:** _6_</span></span>
    - <span data-ttu-id="04475-242">**Sklad:** _61_</span><span class="sxs-lookup"><span data-stu-id="04475-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="04475-243">**Kód předpisu:** _Slotting_</span><span class="sxs-lookup"><span data-stu-id="04475-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="04475-244">Chcete-li, aby byla dostupná záložka s náhledem **Řádky**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04475-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="04475-245">Konfigurace záložky s náhledem Řádky</span><span class="sxs-lookup"><span data-stu-id="04475-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="04475-246">Na záložce s náhledem **Řádky** vytvořte řádek výběrem tlačítka **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="04475-247">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="04475-247">On the new line, set the following values.</span></span> <span data-ttu-id="04475-248">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="04475-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="04475-249">**Od množství:** _0_</span><span class="sxs-lookup"><span data-stu-id="04475-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="04475-250">**Do množství:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="04475-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="04475-251">Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04475-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="04475-252">Konfigurace záložky s náhledem pro Akce směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="04475-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="04475-253">Na záložce s náhledem **Akce směrnice skladového místa** vytvořte řádek výběrem tlačítka **Nový**.</span><span class="sxs-lookup"><span data-stu-id="04475-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="04475-254">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="04475-254">On the new line, set the following values.</span></span> <span data-ttu-id="04475-255">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="04475-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="04475-256">**Název:** _Hromadný_</span><span class="sxs-lookup"><span data-stu-id="04475-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="04475-257">**Strategie:** _Žádná_</span><span class="sxs-lookup"><span data-stu-id="04475-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="04475-258">Kliknutím na **Uložit** zpřístupníte tlačítko **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="04475-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="04475-259">Upravit dotaz</span><span class="sxs-lookup"><span data-stu-id="04475-259">Edit the query</span></span>

1. <span data-ttu-id="04475-260">Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="04475-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="04475-261">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="04475-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="04475-262">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04475-263">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="04475-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="04475-264">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="04475-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="04475-265">**Pole:** *ID zóny*</span><span class="sxs-lookup"><span data-stu-id="04475-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="04475-266">**Kritéria:** *Hromadné* (Klikněte v poli na dvojité plus \[**++**\], rozbalí se seznam, poté vyberte *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="04475-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="04475-267">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04475-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="04475-268">Scénář</span><span class="sxs-lookup"><span data-stu-id="04475-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="04475-269">Nastavení scénáře</span><span class="sxs-lookup"><span data-stu-id="04475-269">Set up the scenario</span></span>

<span data-ttu-id="04475-270">Pro tento scénář použijte předdefinovaná ukázková data a vytvořte záznamy, jak se popisuje v této části.</span><span class="sxs-lookup"><span data-stu-id="04475-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="04475-271">Použití ukázkových dat USMF</span><span class="sxs-lookup"><span data-stu-id="04475-271">Use the USMF sample data</span></span>

<span data-ttu-id="04475-272">Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="04475-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="04475-273">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="04475-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="04475-274">Vytvoření poptávky</span><span class="sxs-lookup"><span data-stu-id="04475-274">Create demand</span></span>

<span data-ttu-id="04475-275">Postupujte podle těchto kroků a vytvořte poptávku, na kterou použijete slotting.</span><span class="sxs-lookup"><span data-stu-id="04475-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="04475-276">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="04475-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="04475-277">Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="04475-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="04475-278">V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu _US-007_.</span><span class="sxs-lookup"><span data-stu-id="04475-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="04475-279">V poli **Sklad** zvolte _61_.</span><span class="sxs-lookup"><span data-stu-id="04475-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="04475-280">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="04475-280">Select **OK**.</span></span>
1. <span data-ttu-id="04475-281">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="04475-281">The new sales order is opened.</span></span> <span data-ttu-id="04475-282">Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="04475-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="04475-283">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="04475-284">**Položka:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="04475-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="04475-285">**Množství:** _20_</span><span class="sxs-lookup"><span data-stu-id="04475-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="04475-286">Chcete-li přidat nový řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="04475-287">**Položka:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="04475-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="04475-288">**Množství:** _8_</span><span class="sxs-lookup"><span data-stu-id="04475-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="04475-289">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04475-289">Select **Save**.</span></span>
1. <span data-ttu-id="04475-290">Klepnutím na možnost **Nová** vytvořte druhou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="04475-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="04475-291">V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu _US-008_.</span><span class="sxs-lookup"><span data-stu-id="04475-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="04475-292">V poli **Sklad** zvolte _61_.</span><span class="sxs-lookup"><span data-stu-id="04475-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="04475-293">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="04475-293">The new sales order is opened.</span></span> <span data-ttu-id="04475-294">Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="04475-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="04475-295">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="04475-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="04475-296">**Položka:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="04475-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="04475-297">**Množství:** _1_</span><span class="sxs-lookup"><span data-stu-id="04475-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="04475-298">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="04475-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="04475-299">Vyzkoušení obvyklého scénáře slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="04475-300">Když jsou splněny všechny nezbytné předpoklady, jak se popisuje v předchozí části, můžete vyzkoušet tuto funkci pomocí cvičení v této části.</span><span class="sxs-lookup"><span data-stu-id="04475-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="04475-301">Generovat poptávku</span><span class="sxs-lookup"><span data-stu-id="04475-301">Generate demand</span></span>

1. <span data-ttu-id="04475-302">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony slottingu** a vyberte šablonu slottingu, kterou jste předtím vytvořili.</span><span class="sxs-lookup"><span data-stu-id="04475-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="04475-303">V podokně Akce klikněte na možnost **Generovat poptávku**.</span><span class="sxs-lookup"><span data-stu-id="04475-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="04475-304">Tento příkaz vyhodnocuje veškerou poptávku, jež se nachází v systému a shoduje se s dotazem dle šablony slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="04475-305">Celková poptávka napříč všemi objednávkami je pak konsolidována do jednoho řádku na množství / měrnou jednotku.</span><span class="sxs-lookup"><span data-stu-id="04475-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="04475-306">Po dokončení procesu se zobrazí informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="04475-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="04475-307">Poptávka na slotting</span><span class="sxs-lookup"><span data-stu-id="04475-307">Slotting demand</span></span>

<span data-ttu-id="04475-308">*Poptávka na slotting* ukazuje výsledky generování poptávky na základě nastavení šablony slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="04475-309">V podokně Akce vyberte **poptávka na slotting**, zobrazí se výsledky příkazu **Generovat poptávku**.</span><span class="sxs-lookup"><span data-stu-id="04475-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="04475-310">Řádky poptávky na slotting lze upravovat.</span><span class="sxs-lookup"><span data-stu-id="04475-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="04475-311">Můžete smazat řádek, přidat nový řádek nebo upravit podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="04475-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="04475-312">Poptávku lze upravit ručně nebo ji můžete importovat z externího systému pomocí správy dat.</span><span class="sxs-lookup"><span data-stu-id="04475-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="04475-313">Ať už je v poptávce na slotting cokoli, bude to použito v dalším kroku, bez ohledu na to, odkud to bylo získáno.</span><span class="sxs-lookup"><span data-stu-id="04475-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="04475-314">Vyhledat poptávku</span><span class="sxs-lookup"><span data-stu-id="04475-314">Locate demand</span></span>

<span data-ttu-id="04475-315">Po vygenerování poptávky musíte použít příkaz **Vyhledat poptávku** k vygenerování *plánu slottingu*.</span><span class="sxs-lookup"><span data-stu-id="04475-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="04475-316">V podokně Akce klikněte na možnost **Vyhledat poptávku**.</span><span class="sxs-lookup"><span data-stu-id="04475-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="04475-317">Spustí se proces slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-317">The slotting process runs.</span></span> <span data-ttu-id="04475-318">Po dokončení procesu se zobrazí informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="04475-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="04475-319">Plán slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-319">Slotting plan</span></span>

<span data-ttu-id="04475-320">Plán slottingu ukazuje skladová místa, k nimž byly přiřazeny jednotlivé položky a jednotlivá množství, zda bylo použito přeplnění, zda byla vytvořena práce s přerušením a jaká šablona bylo pro daný řádek použita.</span><span class="sxs-lookup"><span data-stu-id="04475-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="04475-321">**Jakákoli poptávka, která nemohla být zpracována formou slottingu, se zvýrazní červeně.**</span><span class="sxs-lookup"><span data-stu-id="04475-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="04475-322">V podokně Akce vyberte **Plán slottingu**, zobrazí se výsledky.</span><span class="sxs-lookup"><span data-stu-id="04475-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="04475-323">Vytvoření doplnění</span><span class="sxs-lookup"><span data-stu-id="04475-323">Create replenishment</span></span>

<span data-ttu-id="04475-324">Po vytvoření plánu slottingu musíte na základě tohoto plánu vytvořit *práce doplnění*.</span><span class="sxs-lookup"><span data-stu-id="04475-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="04475-325">V podokně Akce zvolte **Spustit doplnění**.</span><span class="sxs-lookup"><span data-stu-id="04475-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="04475-326">Po dokončení procesu se zobrazí informační zpráva.</span><span class="sxs-lookup"><span data-stu-id="04475-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="04475-327">Tato zpráva označuje počet záhlaví, jež byla vytvořena pro ID sestavení práce.</span><span class="sxs-lookup"><span data-stu-id="04475-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="04475-328">Směrnice skladového místa, jež budou použity, se identifikují na základě kódu předpisu, který je specifikován na každém řádku šablony.</span><span class="sxs-lookup"><span data-stu-id="04475-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="04475-329">Tipy</span><span class="sxs-lookup"><span data-stu-id="04475-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="04475-330">Nastavení automatického slottingu</span><span class="sxs-lookup"><span data-stu-id="04475-330">Set up automatic slotting</span></span>

<span data-ttu-id="04475-331">Po přípravě všech povinných prvků můžete nastavit automatizaci slottingu tak, aby se slotting prováděl automaticky. Postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="04475-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="04475-332">Přejděte na **Řízení skladu \> Doplnění \> Provádění slottingu**.</span><span class="sxs-lookup"><span data-stu-id="04475-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="04475-333">Určete kroky slottingu, jež se mají provést.</span><span class="sxs-lookup"><span data-stu-id="04475-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="04475-334">Vyberte jeden nebo více z následujících kroků slottingu:</span><span class="sxs-lookup"><span data-stu-id="04475-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="04475-335">Generovat poptávku</span><span class="sxs-lookup"><span data-stu-id="04475-335">Generate demand</span></span>
    - <span data-ttu-id="04475-336">Vyhledat poptávku</span><span class="sxs-lookup"><span data-stu-id="04475-336">Locate demand</span></span>
    - <span data-ttu-id="04475-337">Vytvořit práci doplnění</span><span class="sxs-lookup"><span data-stu-id="04475-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="04475-338">Kroky slottingu jsou progresivní.</span><span class="sxs-lookup"><span data-stu-id="04475-338">The slotting steps are progressive.</span></span> <span data-ttu-id="04475-339">Pokud chcete vybrat krok *Vyhledat poptávku*, musíte nejprve vybrat *Generovat poptávku*.</span><span class="sxs-lookup"><span data-stu-id="04475-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="04475-340">Určete šablonu slottingu, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="04475-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="04475-341">Pokud chcete spouštět běh automaticky, nastavte opakování.</span><span class="sxs-lookup"><span data-stu-id="04475-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="04475-342">Pro cvičení ve scénáři **nenastavujte** automatické spouštění slottingu.</span><span class="sxs-lookup"><span data-stu-id="04475-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
