---
title: Strategie doplňování
description: Toto téma poskytuje informace o strategiích doplňování a vysvětluje, jak můžete pomocí pole Strategie doplňování na řádcích šablon doplňování poptávky vlny vybrat, jak se doplnění provádí.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a66d48c6636f9f2012c92945868728d8430c1cbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256032"
---
# <a name="replenishment-strategies"></a><span data-ttu-id="25aa0-103">Strategie doplňování</span><span class="sxs-lookup"><span data-stu-id="25aa0-103">Replenishment strategies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25aa0-104">Šablony, které jsou definovány na stránce **Šablony doplňování**, obsahují řádky šablony doplňování poptávky vlny, které vám umožňují vybrat, jak se doplnění provádí.</span><span class="sxs-lookup"><span data-stu-id="25aa0-104">The templates that are defined on the **Replenishment templates** page include wave demand replenishment template lines that let you select how replenishment is done.</span></span> <span data-ttu-id="25aa0-105">Každý řádek nyní obsahuje a pole **Strategie doplňování**.</span><span class="sxs-lookup"><span data-stu-id="25aa0-105">Each line now includes a **Replenishment strategy** field.</span></span>

<span data-ttu-id="25aa0-106">Strategie *Množství poptávky vlny* je výchozí strategie.</span><span class="sxs-lookup"><span data-stu-id="25aa0-106">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="25aa0-107">Jedná se o strategii doplňování, která byla použita před zavedením pole **Strategie doplňování**.</span><span class="sxs-lookup"><span data-stu-id="25aa0-107">It's the replenishment strategy that was used before the introduction of the **Replenishment strategy** field.</span></span> <span data-ttu-id="25aa0-108">Směrnice skladového místa se používá k vyhledání míst, která lze doplnit.</span><span class="sxs-lookup"><span data-stu-id="25aa0-108">It uses the replenishment location directives to find locations that can be replenished.</span></span> <span data-ttu-id="25aa0-109">Poté tato místa doplňuje, dokud není pokryta poptávka.</span><span class="sxs-lookup"><span data-stu-id="25aa0-109">It then replenishes those locations until the demand is covered.</span></span>

<span data-ttu-id="25aa0-110">Strategie *Maximální kapacita skladového místa* zavádí některé nové funkce.</span><span class="sxs-lookup"><span data-stu-id="25aa0-110">The *Maximum location capacity* strategy introduces some new functionality.</span></span> <span data-ttu-id="25aa0-111">Stejně jako strategie *Množství poptávky vlny* tato strategie používá směrnice skladového místa doplňování k vyhledání míst, která lze doplnit, a poté tato místa doplňuje, dokud není pokryta poptávka.</span><span class="sxs-lookup"><span data-stu-id="25aa0-111">Like the *Wave demand quantity* strategy, this strategy uses the replenishment location directives to find locations that can be replenished, and then it replenishes those locations until the demand is covered.</span></span> <span data-ttu-id="25aa0-112">Liší se od strategie *Množství poptávky vlny* v tom, že všechna doplňovaná místa jsou doplněna na svou maximální kapacitu, jak je definována skladovacími limity místa.</span><span class="sxs-lookup"><span data-stu-id="25aa0-112">It differs from the *Wave demand quantity* strategy in that all the replenished locations are replenished to their maximum capacity, as defined by the location stocking limits.</span></span> <span data-ttu-id="25aa0-113">Strategie *Maximální kapacita skladového místa* se snaží vytvořit práci, která přinese požadované množství plus nějaké další množství, aby vyplnila místa, která se doplňují.</span><span class="sxs-lookup"><span data-stu-id="25aa0-113">The *Maximum location capacity* strategy tries to create work to bring in the requested quantity, plus some extra quantity, to fill the locations that are being replenished.</span></span> <span data-ttu-id="25aa0-114">V některých případech však tento pokus může selhat.</span><span class="sxs-lookup"><span data-stu-id="25aa0-114">However, in some cases, that attempt might fail.</span></span> <span data-ttu-id="25aa0-115">Například hromadná umístění nemusí mít dostatek zásob k pokrytí extra množství.</span><span class="sxs-lookup"><span data-stu-id="25aa0-115">For example, the bulk locations might not have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="25aa0-116">V těchto případech systém detekuje poruchu a pokusí se o obnovení.</span><span class="sxs-lookup"><span data-stu-id="25aa0-116">In these cases, the system detects the failure and tries to recover.</span></span>

<span data-ttu-id="25aa0-117">Hlavní sezóna je jedním z příkladů situace, kdy strategie *Maximální kapacita skladového místa* je lepší než strategie *Množství poptávky vlny*.</span><span class="sxs-lookup"><span data-stu-id="25aa0-117">Peak season is one example of a situation where the *Maximum location capacity* strategy is preferable to the *Wave demand quantity* strategy.</span></span> <span data-ttu-id="25aa0-118">Během hlavní sezóny se některé položky mohou prodávat ve velkém objemu.</span><span class="sxs-lookup"><span data-stu-id="25aa0-118">During peak season, some items might be selling at high volume.</span></span> <span data-ttu-id="25aa0-119">Proto možná budete chtít proaktivně co nejvíce doplňovat relevantní umístění pro vychystávání, abyste snížili počet ID práce, které jsou vytvořeny pro doplnění.</span><span class="sxs-lookup"><span data-stu-id="25aa0-119">Therefore, you might want to proactively replenish the relevant picking locations as much as possible, to reduce the number of work IDs that are created for replenishment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25aa0-120">Chcete-li plně využít výhod strategie *Maximální kapacita skladového místa*, musíte předefinovat limity skladování pro příslušná místa.</span><span class="sxs-lookup"><span data-stu-id="25aa0-120">To take full advantage of the *Maximum location capacity* strategy, you must redefine the stocking limits for the relevant locations.</span></span> <span data-ttu-id="25aa0-121">Jinak tato strategie funguje stejně jako strategie *Množství poptávky vlny*.</span><span class="sxs-lookup"><span data-stu-id="25aa0-121">Otherwise, this strategy works just like the *Wave demand quantity* strategy.</span></span>

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a><span data-ttu-id="25aa0-122">Zapněte funkci Doplnění na maximum na základě limitů skladování</span><span class="sxs-lookup"><span data-stu-id="25aa0-122">Turn on the Replenish to max based on stocking limits feature</span></span>

<span data-ttu-id="25aa0-123">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="25aa0-123">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="25aa0-124">Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zkontrolovat stav této funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="25aa0-124">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of this feature and turn it on if it's required.</span></span> <span data-ttu-id="25aa0-125">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="25aa0-125">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="25aa0-126">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="25aa0-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="25aa0-127">**Název funkce:** *Doplnění na maximum na základě limitů skladování*</span><span class="sxs-lookup"><span data-stu-id="25aa0-127">**Feature name:** *Replenish to max based on stocking limits*</span></span>

## <a name="set-up-replenishment-strategies"></a><span data-ttu-id="25aa0-128">Nastavení strategie doplňování</span><span class="sxs-lookup"><span data-stu-id="25aa0-128">Set up replenishment strategies</span></span>

<span data-ttu-id="25aa0-129">Pro přístup k šablonám přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="25aa0-129">To access the templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span> <span data-ttu-id="25aa0-130">V části **Přehled** vyberte nebo vytvořte šablonu doplňování poptávky vlny, kde pole **Typ doplňování** je nastaveno na *Poptávka vlny*.</span><span class="sxs-lookup"><span data-stu-id="25aa0-130">In the **Overview** section, select or create a wave demand replenishment template where the **Replenishment type** field is set to *Wave demand*.</span></span> <span data-ttu-id="25aa0-131">Poté nastavte řádky šablony doplňování v části **Podrobnosti šablony doplňování**.</span><span class="sxs-lookup"><span data-stu-id="25aa0-131">Then set up the replenishment template lines in the **Replenishment template details** section.</span></span> <span data-ttu-id="25aa0-132">Pro každý řádek v poli **Strategie doplňování** vyberte strategii doplňování, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="25aa0-132">For each line, in the **Replenishment strategy** field, select the replenishment strategy that you want to use.</span></span>

<span data-ttu-id="25aa0-133">![Stránka Šablony doplnění](media/ReplenTempWaveDmdMaxLocCap.png "Stránka Šablony doplnění")</span><span class="sxs-lookup"><span data-stu-id="25aa0-133">![Replenishment templates page](media/ReplenTempWaveDmdMaxLocCap.png "Replenishment templates page")</span></span>

<span data-ttu-id="25aa0-134">Pokud se sloupec **Strategie doplňování** nezobrazí v mřížce v sekci **Podrobnosti šablony doplňování**, ujistěte se, že byla funkce zapnuta a že vybraná šablona doplňování má typ doplňování *Poptávka vlny*.</span><span class="sxs-lookup"><span data-stu-id="25aa0-134">If the **Replenishment strategy** column doesn't appear in the grid in the **Replenishment template details** section, make sure that the feature has been turned on, and that the selected replenishment template has a replenishment type of *Wave demand*.</span></span>

> [!NOTE]
> <span data-ttu-id="25aa0-135">Strategie *Množství poptávky vlny* je výchozí strategie.</span><span class="sxs-lookup"><span data-stu-id="25aa0-135">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="25aa0-136">Proto stačí aktualizovat řádky šablony doplňování tam, kde chcete použít místo toho strategii *Maximální kapacita skladového místa*.</span><span class="sxs-lookup"><span data-stu-id="25aa0-136">Therefore, you just have to update the replenishment template lines where you want to use the *Maximum location capacity* strategy instead.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="25aa0-137">Ukázkové scénáře</span><span class="sxs-lookup"><span data-stu-id="25aa0-137">Example scenarios</span></span>

### <a name="example-1"></a><span data-ttu-id="25aa0-138">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="25aa0-138">Example 1</span></span>

<span data-ttu-id="25aa0-139">V tomto příkladu existuje pouze jedna šablona doplňování, která má pouze jeden řádek šablony doplňování.</span><span class="sxs-lookup"><span data-stu-id="25aa0-139">For this example, there is only one replenishment template that has only one replenishment template line.</span></span>

<span data-ttu-id="25aa0-140">Vytvoříte prodejní objednávku na 130 kusů (ks) položky A0001.</span><span class="sxs-lookup"><span data-stu-id="25aa0-140">You create a sales order for 130 pieces (pcs) of item A0001.</span></span> <span data-ttu-id="25aa0-141">Před uvolněním objednávky do skladu je sklad nastaven následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="25aa0-141">Before you release the order to the warehouse, the warehouse is set up in the following way:</span></span>

- <span data-ttu-id="25aa0-142">Existuje pouze jedno hromadné umístění a má 500 ks dostupných zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="25aa0-142">There is only one bulk location, and it has 500 pcs of available on-hand inventory.</span></span>
- <span data-ttu-id="25aa0-143">Existují tři výdejová místa, z nichž každé má limit skladování 100 ks.</span><span class="sxs-lookup"><span data-stu-id="25aa0-143">There are three pick locations, each of which has a stocking limit of 100 pcs.</span></span> <span data-ttu-id="25aa0-144">(Pamatujte, že pro strategii *Maximální kapacita skladového místa* jsou povinné skladovací limity.)</span><span class="sxs-lookup"><span data-stu-id="25aa0-144">(Remember that stocking limits are required for the *Maximum location capacity* strategy.)</span></span>
- <span data-ttu-id="25aa0-145">Místa vložení doplnění jsou stejná jako místa prodejního výdeje.</span><span class="sxs-lookup"><span data-stu-id="25aa0-145">The replenishment put locations are the same as the sales pick locations.</span></span>
- <span data-ttu-id="25aa0-146">Jednotka doplnění je krabice (1 krabice = 20 ks).</span><span class="sxs-lookup"><span data-stu-id="25aa0-146">The replenishment unit is a box (1 box = 20 pcs).</span></span>

<span data-ttu-id="25aa0-147">V době objednávky jsou v prodejních výdejových místech k dispozici následující zásoby:</span><span class="sxs-lookup"><span data-stu-id="25aa0-147">At the time of the order, the following inventory is on hand at the sales pick locations:</span></span>

- <span data-ttu-id="25aa0-148">**Pick-001:** 20 ks (1 krabice)</span><span class="sxs-lookup"><span data-stu-id="25aa0-148">**Pick-001:** 20 pcs (1 box)</span></span>
- <span data-ttu-id="25aa0-149">**Pick-002:** 0 ks</span><span class="sxs-lookup"><span data-stu-id="25aa0-149">**Pick-002:** 0 pcs</span></span>
- <span data-ttu-id="25aa0-150">**Pick-003:** 0 ks</span><span class="sxs-lookup"><span data-stu-id="25aa0-150">**Pick-003:** 0 pcs</span></span>

<span data-ttu-id="25aa0-151">Zpočátku je strategie doplňování nastavena na *Množství poptávky vlny*.</span><span class="sxs-lookup"><span data-stu-id="25aa0-151">Initially, the replenishment strategy is set to *Wave demand quantity*.</span></span>

<span data-ttu-id="25aa0-152">Po uvolnění prodejní objednávky do skladu a spuštění zpracování vln pro vlnu získáte následující práci doplnění:</span><span class="sxs-lookup"><span data-stu-id="25aa0-152">After you release the sales order to the warehouse, and wave processing runs for the wave, you get the following replenishment work:</span></span>

- <span data-ttu-id="25aa0-153">**Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.</span><span class="sxs-lookup"><span data-stu-id="25aa0-153">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="25aa0-154">**Práce doplnění 2:** Vyberte 2 krabice z hromadného umístění a umístěte je do místa pick-002.</span><span class="sxs-lookup"><span data-stu-id="25aa0-154">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="25aa0-155">Získáte dvě ID práce doplňování, protože musíte doplnit dvě místa a vícenásobné vložení není podporováno.</span><span class="sxs-lookup"><span data-stu-id="25aa0-155">You get two replenishment work IDs because you must replenish two locations, and multi-puts aren't supported.</span></span>

<span data-ttu-id="25aa0-156">Pokud nastavíte strategii doplňování místo toho na *Maximální kapacita skladového místa*, získáte následující práci doplnění:</span><span class="sxs-lookup"><span data-stu-id="25aa0-156">If you set the replenishment strategy to *Maximum location capacity* instead, you get the following replenishment work:</span></span>

- <span data-ttu-id="25aa0-157">**Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.</span><span class="sxs-lookup"><span data-stu-id="25aa0-157">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="25aa0-158">**Práce doplnění 2:** Vyberte 5 krabice z hromadného umístění a umístěte je do místa pick-002.</span><span class="sxs-lookup"><span data-stu-id="25aa0-158">**Replenishment work 2:** Pick 5 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="25aa0-159">[![Příklad 1](media/ReplenTemp_example_1.png "Příklad 1")](media/ReplenTemp_example_1_large.png)</span><span class="sxs-lookup"><span data-stu-id="25aa0-159">[![Example 1](media/ReplenTemp_example_1.png "Example 1")](media/ReplenTemp_example_1_large.png)</span></span>

### <a name="example-2"></a><span data-ttu-id="25aa0-160">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="25aa0-160">Example 2</span></span>

<span data-ttu-id="25aa0-161">Tento příklad ukazuje, co se stane, když hromadné umístění nemá dostatek zásob k pokrytí extra množství.</span><span class="sxs-lookup"><span data-stu-id="25aa0-161">This example shows what happens when the bulk location doesn't have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="25aa0-162">Používá stejný scénář jako v příkladu 1, ale hromadné umístění má 160 ks (8 krabic).</span><span class="sxs-lookup"><span data-stu-id="25aa0-162">It uses the same scenario as example 1, but the bulk location has 160 pcs (8 boxes).</span></span>

<span data-ttu-id="25aa0-163">Strategie *Množství poptávky vlny* vytváří stejnou práci jako v příkladu 1.</span><span class="sxs-lookup"><span data-stu-id="25aa0-163">The *Wave demand quantity* strategy creates the same work that it did in example 1.</span></span>

<span data-ttu-id="25aa0-164">Protože se však strategie *Maximální kapacita skladového místa* pokusí vytvořit ID práce, jako tomu bylo v příkladu 1, může selhat.</span><span class="sxs-lookup"><span data-stu-id="25aa0-164">However, because the *Maximum location capacity* strategy tries to create the work IDs as it did in example 1, it might fail.</span></span> <span data-ttu-id="25aa0-165">V tomto okamžiku se systém pokusí o obnovení.</span><span class="sxs-lookup"><span data-stu-id="25aa0-165">At that point, the system tries to recover.</span></span>

<span data-ttu-id="25aa0-166">V závislosti na nastavení možnost **Povolit rozdělení** ve směrnicích skladového místa pro výdej doplňování jsou možné dva výsledky:</span><span class="sxs-lookup"><span data-stu-id="25aa0-166">Depending on the setting of the **Allow split** option on the location directives for replenishment picking, two outcomes are possible:</span></span>

- <span data-ttu-id="25aa0-167">Pokud je možnost **Povolit rozdělení** nastavena na *Ano*, je vytvořena následující práce doplnění:</span><span class="sxs-lookup"><span data-stu-id="25aa0-167">If the **Allow split** option is set to *Yes*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="25aa0-168">**Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.</span><span class="sxs-lookup"><span data-stu-id="25aa0-168">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="25aa0-169">**Práce doplnění 2:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-002.</span><span class="sxs-lookup"><span data-stu-id="25aa0-169">**Replenishment work 2:** Pick 4 boxes from the bulk location, and put them in location pick-002.</span></span>

- <span data-ttu-id="25aa0-170">Pokud je možnost **Povolit rozdělení** nastavena na *Ne*, je vytvořena následující práce doplnění:</span><span class="sxs-lookup"><span data-stu-id="25aa0-170">If the **Allow split** option is set to *No*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="25aa0-171">**Práce doplnění 1:** Vyberte 4 krabice z hromadného umístění a umístěte je do místa pick-001.</span><span class="sxs-lookup"><span data-stu-id="25aa0-171">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="25aa0-172">**Práce doplnění 2:** Vyberte 2 krabice z hromadného umístění a umístěte je do místa pick-002.</span><span class="sxs-lookup"><span data-stu-id="25aa0-172">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="25aa0-173">Výsledky se liší kvůli informacím, které jsou k dispozici při vytváření práce.</span><span class="sxs-lookup"><span data-stu-id="25aa0-173">The outcomes differ because of the information that is available when you create the work.</span></span> <span data-ttu-id="25aa0-174">Když je možnost **Povolit rozdělení** nastavena na *Ano* ve směrnicích skladového místa pro výdej doplňování víte, že se vám podařilo najít 160 ks.</span><span class="sxs-lookup"><span data-stu-id="25aa0-174">When the **Allow split** is set to *Yes* on the location directives for replenishment picking, you know that you managed to find 160 pcs.</span></span> <span data-ttu-id="25aa0-175">Proto pro toto množství můžete vytvořit práci.</span><span class="sxs-lookup"><span data-stu-id="25aa0-175">Therefore, you can create work for that quantity.</span></span> <span data-ttu-id="25aa0-176">Když je však možnost **Povolit rozdělení** nastavena na *Ne*, nevíte o existenci 160 ks.</span><span class="sxs-lookup"><span data-stu-id="25aa0-176">However, when the **Allow split** option is set to *No*, you don't know about the existence of the 160 pcs.</span></span> <span data-ttu-id="25aa0-177">Protože extra množství, které jste se rozhodli doplnit, byly 3 krabice, odečtete toto extra množství a zkusíte původní množství znovu.</span><span class="sxs-lookup"><span data-stu-id="25aa0-177">Because the extra quantity that you decided to replenish was 3 boxes, you drop that extra quantity and try the original quantity again.</span></span>

<span data-ttu-id="25aa0-178">[![Příklad 2](media/ReplenTemp_example_2.png "Příklad 2")](media/ReplenTemp_example_2_large.png)</span><span class="sxs-lookup"><span data-stu-id="25aa0-178">[![Example 2](media/ReplenTemp_example_2.png "Example 2")](media/ReplenTemp_example_2_large.png)</span></span>

<span data-ttu-id="25aa0-179">Chcete-li tedy získat maximální množství na doplněná místa, měli byste nastavit možnost **Povolit rozdělení** na *Ano* na směrnicích skladového místa pro výdej doplňování.</span><span class="sxs-lookup"><span data-stu-id="25aa0-179">Therefore, to get the maximum quantity to the replenished locations, you should set the **Allow split** option to *Yes* on the location directives for replenishment picking.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]