---
title: Konfigurace nákladů pro distribuovanou správu objednávek
description: Toto téma popisuje konfiguraci nákladů pro funkcionalitu distribuované správy objednávek v aplikaci Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b5e3e1997f3d3b61b7b3c7486f5531e386293537
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019432"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="e15b9-103">Konfigurace nákladů pro distribuovanou správu objednávek</span><span class="sxs-lookup"><span data-stu-id="e15b9-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e15b9-104">Organizace zvažují více komponent nákladů, aby určily optimální umístění, odkud se bude plnit objednávka.</span><span class="sxs-lookup"><span data-stu-id="e15b9-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="e15b9-105">Některými z těchto komponent nákladů jsou náklady na přepravu, náklady na zpracování a náklady balení.</span><span class="sxs-lookup"><span data-stu-id="e15b9-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="e15b9-106">Pro určení místa plnění se vypočítává kombinace těchto nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="e15b9-107">Když první iterace správy distribuovaných objednávek v aplikaci Dynamics 365 Retail optimalizovala přiřazení objednávek do míst plnění, byla tato skutečnost zohledněna pouze ve vzdálenosti.</span><span class="sxs-lookup"><span data-stu-id="e15b9-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="e15b9-108">Ačkoli vzdálenost může vzájemně souviset s náklady, není totéž jako náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="e15b9-109">Například náklady metody doručení na druhý den stojí více, než doručení na tutéž vzdálenost do tří nebo do sedmi dnů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="e15b9-110">Funkce konfigurace nákladů umožňuje maloobchodníkům definovat a konfigurovat další komponenty nákladů, které budou vypočítány a zohledněny při určování optimálního umístění, odkud se budou plnit řádky objednávky.</span><span class="sxs-lookup"><span data-stu-id="e15b9-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="e15b9-111">Když jsou komponenty nákladů nakonfigurovány, řešitel DOM používá k určení optimálního umístění pro plnění objednávky pouze tyto definice nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="e15b9-112">Nepovažuje komponentu vzdálenosti jako náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="e15b9-113">Když však nejsou nakonfigurovány žádné komponenty nákladů, řešitel DOM používá komponentu vzdálenosti jako náklad pro určení optimálního umístění pro plnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="e15b9-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="e15b9-114">Nastavení komponent nákladů</span><span class="sxs-lookup"><span data-stu-id="e15b9-114">Set up cost components</span></span>

<span data-ttu-id="e15b9-115">V systému lze definovat dva hlavní typy komponent nákladů: **Expedice** a **Jiné**.</span><span class="sxs-lookup"><span data-stu-id="e15b9-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="e15b9-116">Oba typy komponent nákladů podporují více základů výpočtu, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="e15b9-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e15b9-117">Typ komponenty nákladu</span><span class="sxs-lookup"><span data-stu-id="e15b9-117">Cost component type</span></span></th>
<th><span data-ttu-id="e15b9-118">Základ výpočtu</span><span class="sxs-lookup"><span data-stu-id="e15b9-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e15b9-119">Expedice</span><span class="sxs-lookup"><span data-stu-id="e15b9-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e15b9-120">Jednoduchý</span><span class="sxs-lookup"><span data-stu-id="e15b9-120">Simple</span></span></li>
<li><span data-ttu-id="e15b9-121">Vrstvený</span><span class="sxs-lookup"><span data-stu-id="e15b9-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e15b9-122">Jiný</span><span class="sxs-lookup"><span data-stu-id="e15b9-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e15b9-123">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="e15b9-123">Sales order</span></span></li>
<li><span data-ttu-id="e15b9-124">Řádek prodeje</span><span class="sxs-lookup"><span data-stu-id="e15b9-124">Sales line</span></span></li>
<li><span data-ttu-id="e15b9-125">Umístění</span><span class="sxs-lookup"><span data-stu-id="e15b9-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="e15b9-126">Typ komponenty nákladu Expedice</span><span class="sxs-lookup"><span data-stu-id="e15b9-126">Shipping cost component type</span></span>

<span data-ttu-id="e15b9-127">Tato část vysvětluje, jak nastavit každou kombinaci typu komponenty nákladu **Expedice** a základ výpočtu pro přepravní náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="e15b9-128">Také vysvětluje, jak jsou řešitel DOM používá každou kombinaci.</span><span class="sxs-lookup"><span data-stu-id="e15b9-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="e15b9-129">Typ komponenty nákladů = Expedice a základ výpočtu = Jednoduchý</span><span class="sxs-lookup"><span data-stu-id="e15b9-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="e15b9-130">Pokud se použije kombinace typu komponenty nákladů **Expedice** a základ výpočtu **Jednoduchý**, přepravní náklady pro režim doručení jsou založeny buď na paušálních nákladech nebo na vzdálenosti.</span><span class="sxs-lookup"><span data-stu-id="e15b9-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="e15b9-131">Pro tuto kombinaci musíte nastavit následující pole:</span><span class="sxs-lookup"><span data-stu-id="e15b9-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="e15b9-132">**Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="e15b9-133">**Popis** – Zadejte název a popis koeficientu nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="e15b9-134">**Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</span><span class="sxs-lookup"><span data-stu-id="e15b9-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="e15b9-135">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</span><span class="sxs-lookup"><span data-stu-id="e15b9-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="e15b9-136">**Aktivní** - Označuje, zda je koeficient nákladů aktivní.</span><span class="sxs-lookup"><span data-stu-id="e15b9-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="e15b9-137">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="e15b9-138">**Společnost** - Určuje právnickou osobu, pro kterou je koeficient nákladů nakonfigurován.</span><span class="sxs-lookup"><span data-stu-id="e15b9-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="e15b9-139">Všechny řádky kritérií výpočtu musí být pro stejnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="e15b9-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="e15b9-140">**Způsoby dodání** - Určují způsoby dodání, pro které jsou nakonfigurovány náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="e15b9-141">**Typ výpočtu** – Určuje, jak mají být vypočítány náklady pro konkrétní způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="e15b9-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="e15b9-142">Jsou podporovány dva typy výpočtu:</span><span class="sxs-lookup"><span data-stu-id="e15b9-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="e15b9-143">**Pevný** – Pro způsob dodání se používá jednotný paušální náklad.</span><span class="sxs-lookup"><span data-stu-id="e15b9-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="e15b9-144">Pokud vyberete tento typ výpočtu, pole **Náklady** definuje jednotný paušální náklad.</span><span class="sxs-lookup"><span data-stu-id="e15b9-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="e15b9-145">**Podle jednotky vzdálenosti** – Náklad pro způsob dodání se vypočítá jako hodnota nákladů specifikovaná v poli **Náklady** krát vzdálenost mezi adresou doručení a místy.</span><span class="sxs-lookup"><span data-stu-id="e15b9-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="e15b9-146">**Náklady** – Určuje hodnotu nákladů používanou ve spojení s polem **Typ výpočtu** pro výpočet nákladů pro způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="e15b9-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="e15b9-147">Typ komponenty nákladů = Expedice a základ výpočtu = Vrstvený</span><span class="sxs-lookup"><span data-stu-id="e15b9-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="e15b9-148">Pokud se použije kombinace typu komponenty nákladů **Expedice** a základ výpočtu **Vrstvený**, přepravní náklady pro režim doručení jsou založeny buď na paušálních nákladech nebo na vzdálenosti.</span><span class="sxs-lookup"><span data-stu-id="e15b9-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="e15b9-149">V této kombinaci je však vzdálenost založena na vrstveném rozsahu vzdáleností.</span><span class="sxs-lookup"><span data-stu-id="e15b9-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="e15b9-150">Pro tuto kombinaci musíte nastavit následující pole:</span><span class="sxs-lookup"><span data-stu-id="e15b9-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="e15b9-151">**Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="e15b9-152">**Popis** – Zadejte název a popis koeficientu nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="e15b9-153">**Výchozí náklady** – Určují náklady, které by měly být použity pro způsob dodání, pokud vzdálenost mezi adresou doručení a místem nespadá do žádné z vrstvených vzdáleností pro způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="e15b9-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="e15b9-154">**Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</span><span class="sxs-lookup"><span data-stu-id="e15b9-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="e15b9-155">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</span><span class="sxs-lookup"><span data-stu-id="e15b9-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="e15b9-156">**Aktivní** - Označuje, zda je koeficient nákladů aktivní.</span><span class="sxs-lookup"><span data-stu-id="e15b9-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="e15b9-157">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="e15b9-158">**Společnost** - Určuje právnickou osobu, pro kterou je koeficient nákladů nakonfigurován.</span><span class="sxs-lookup"><span data-stu-id="e15b9-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="e15b9-159">Všechny řádky kritérií výpočtu musí být pro stejnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="e15b9-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="e15b9-160">**Způsoby dodání** - Určují způsoby dodání, pro které jsou nakonfigurovány náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="e15b9-161">**Typ vzdálenosti** – Určuje, zda definice vrstvené vzdálenosti je vzdušná vzdálenost nebo vzdálenost po silnici.</span><span class="sxs-lookup"><span data-stu-id="e15b9-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="e15b9-162">**Jednotky vzdálenosti** – Určuje jednotku, ve které se měří vrstvená vzdálenost.</span><span class="sxs-lookup"><span data-stu-id="e15b9-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="e15b9-163">**Vzdálenost od** – Určuje počátek rozsahu pro vrstvenou vzdálenost.</span><span class="sxs-lookup"><span data-stu-id="e15b9-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="e15b9-164">**Vzdálenost do** – Určuje konec rozsahu pro vrstvenou vzdálenost.</span><span class="sxs-lookup"><span data-stu-id="e15b9-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="e15b9-165">**Typ výpočtu** – Určuje, jak mají být vypočítány náklady pro konkrétní způsob dodání a vrstvenou vzdálenost.</span><span class="sxs-lookup"><span data-stu-id="e15b9-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="e15b9-166">Jsou podporovány dva typy výpočtu:</span><span class="sxs-lookup"><span data-stu-id="e15b9-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="e15b9-167">**Pevný** – Pro způsob dodání se používá jednotný paušální náklad.</span><span class="sxs-lookup"><span data-stu-id="e15b9-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="e15b9-168">Pokud vyberete tento typ výpočtu, pole **Náklady** definuje jednotný paušální náklad.</span><span class="sxs-lookup"><span data-stu-id="e15b9-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="e15b9-169">**Podle jednotky vzdálenosti** – Náklad pro způsob dodání a vrstvenou vzdálenost se vypočítá jako hodnota nákladů specifikovaná v poli **Náklady** krát vzdálenost mezi adresou doručení a místy.</span><span class="sxs-lookup"><span data-stu-id="e15b9-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="e15b9-170">**Náklady** – Určuje hodnotu nákladů používanou ve spojení s polem **Typ výpočtu** pro výpočet nákladů pro způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="e15b9-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="e15b9-171">Když definujete vrstvené vzdálenosti, systém ověří, zda se vzdálenosti nepřekrývají nebo nechybí.</span><span class="sxs-lookup"><span data-stu-id="e15b9-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="e15b9-172">Typ vzdálenosti používaný pro způsob dodání musí být shodný napříč všemi vrstvenými vzdálenostmi.</span><span class="sxs-lookup"><span data-stu-id="e15b9-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="e15b9-173">Jiný typ komponenty nákladu</span><span class="sxs-lookup"><span data-stu-id="e15b9-173">Other cost component type</span></span>

<span data-ttu-id="e15b9-174">Tato část vysvětluje, jak nastavit každou kombinaci typu komponenty nákladu **Jiný** a jiný typ nákladů pro jiné než přepravní náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="e15b9-175">Také vysvětluje, jak jsou řešitel DOM používá každou kombinaci.</span><span class="sxs-lookup"><span data-stu-id="e15b9-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="e15b9-176">Typ komponenty nákladů = Jiný a jiný typ nákladů = Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="e15b9-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="e15b9-177">Kombinace typu nákladů **Jiný** a jiného typu nákladů **Prodejní objednávka** se používá pro definování nepřepravních nákladů na úrovni prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e15b9-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="e15b9-178">Pro tuto kombinaci musíte nastavit následující pole:</span><span class="sxs-lookup"><span data-stu-id="e15b9-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="e15b9-179">**Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="e15b9-180">**Popis** – Zadejte název a popis koeficientu nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="e15b9-181">**Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</span><span class="sxs-lookup"><span data-stu-id="e15b9-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="e15b9-182">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</span><span class="sxs-lookup"><span data-stu-id="e15b9-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="e15b9-183">**Aktivní** - Označuje, zda je koeficient nákladů aktivní.</span><span class="sxs-lookup"><span data-stu-id="e15b9-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="e15b9-184">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="e15b9-185">**Náklady** – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e15b9-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="e15b9-186">Typ komponenty nákladů = Jiný a jiný typ nákladů = Prodejní řádek</span><span class="sxs-lookup"><span data-stu-id="e15b9-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="e15b9-187">Kombinace typu nákladů **Jiný** a jiného typu nákladů **Prodejní řádek** se používá pro definování nepřepravních nákladů na úrovni řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e15b9-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="e15b9-188">Pro tuto kombinaci musíte nastavit následující pole:</span><span class="sxs-lookup"><span data-stu-id="e15b9-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="e15b9-189">**Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="e15b9-190">**Popis** – Zadejte název a popis koeficientu nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="e15b9-191">**Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</span><span class="sxs-lookup"><span data-stu-id="e15b9-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="e15b9-192">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</span><span class="sxs-lookup"><span data-stu-id="e15b9-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="e15b9-193">**Aktivní** - Označuje, zda je koeficient nákladů aktivní.</span><span class="sxs-lookup"><span data-stu-id="e15b9-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="e15b9-194">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="e15b9-195">**Náklady** – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e15b9-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="e15b9-196">Typ komponenty nákladů = Jiný a jiný typ nákladů = Místo</span><span class="sxs-lookup"><span data-stu-id="e15b9-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="e15b9-197">Kombinace typu nákladů **Jiný** a jiného typu nákladů **Místo** se používá pro definování nepřepravních nákladů pro skupinu míst nebo jednotlivé místo.</span><span class="sxs-lookup"><span data-stu-id="e15b9-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="e15b9-198">Pro tuto kombinaci musíte nastavit následující pole:</span><span class="sxs-lookup"><span data-stu-id="e15b9-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="e15b9-199">**Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="e15b9-200">**Popis** – Zadejte název a popis koeficientu nákladů.</span><span class="sxs-lookup"><span data-stu-id="e15b9-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="e15b9-201">**Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</span><span class="sxs-lookup"><span data-stu-id="e15b9-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="e15b9-202">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</span><span class="sxs-lookup"><span data-stu-id="e15b9-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="e15b9-203">**Aktivní** - Označuje, zda je koeficient nákladů aktivní.</span><span class="sxs-lookup"><span data-stu-id="e15b9-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="e15b9-204">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="e15b9-205">**Skupina plnění** – Určuje skupinu míst, pro která jsou definovány nepřepravní náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="e15b9-206">**Místo plnění** – Určuje místo, pro které jsou definovány nepřepravní náklady.</span><span class="sxs-lookup"><span data-stu-id="e15b9-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e15b9-207">Pro kritéria výpočtu na základě místa nelze určit skupinu plnění a místo plnění na stejném řádku.</span><span class="sxs-lookup"><span data-stu-id="e15b9-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="e15b9-208">**Náklady** – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni skupiny plnění nebo na úrovni místa plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e15b9-209">Aby distribuovaná správa objednávek zvažovala při svém spuštění tyto náklady, musíte přidat koeficient nákladů do příslušného profilu plnění.</span><span class="sxs-lookup"><span data-stu-id="e15b9-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
