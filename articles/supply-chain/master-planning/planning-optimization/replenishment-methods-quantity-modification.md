---
title: Metody doplnění a modifikace množství
description: Toto téma obsahuje informace o metodách doplnění v Optimalizaci plánování Vysvětluje také, jak vícenásobné množství objednávky pro produkt ovlivňuje výsledek.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261689"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="cd19a-104">Metody doplnění a modifikace množství</span><span class="sxs-lookup"><span data-stu-id="cd19a-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd19a-105">Toto téma obsahuje informace o metodách doplnění v Optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="cd19a-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="cd19a-106">Vysvětluje také, jak vícenásobné množství objednávky pro produkt ovlivňuje výsledek.</span><span class="sxs-lookup"><span data-stu-id="cd19a-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="cd19a-107">Metody doplňování jsou také známé jako metody pokrytí a metody stanovení velikosti šarže.</span><span class="sxs-lookup"><span data-stu-id="cd19a-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="cd19a-108">Kódy pokrytí</span><span class="sxs-lookup"><span data-stu-id="cd19a-108">Coverage codes</span></span>

<span data-ttu-id="cd19a-109">Optimalizaci plánování lze nakonfigurovat tak, aby používalo různé metody doplnění.</span><span class="sxs-lookup"><span data-stu-id="cd19a-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="cd19a-110">Metody doplňování jsou techniky, které systém používá k výpočtu požadavků na produkt.</span><span class="sxs-lookup"><span data-stu-id="cd19a-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="cd19a-111">Metody doplňování jsou definovány kódy pokrytí, které můžete nastavit buď pro skupinu pokrytí, nebo pro produkt.</span><span class="sxs-lookup"><span data-stu-id="cd19a-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="cd19a-112">V optimalizaci plánování lze použít následující kódy pokrytí:</span><span class="sxs-lookup"><span data-stu-id="cd19a-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="cd19a-113">**Období** - metoda doplnění kombinuje všechny požadavky na období do jedné objednávky pro daný produkt.</span><span class="sxs-lookup"><span data-stu-id="cd19a-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="cd19a-114">Zakázka bude naplánována pro první den období a její množství bude plnit čisté požadavky během stanoveného období.</span><span class="sxs-lookup"><span data-stu-id="cd19a-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="cd19a-115">Toto období začíná první poptávkou produktu a pokrývá určenou délku v čase.</span><span class="sxs-lookup"><span data-stu-id="cd19a-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="cd19a-116">Další období bude začínat následujícími požadavky produktu.</span><span class="sxs-lookup"><span data-stu-id="cd19a-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="cd19a-117">Kód pokrytí *Období* se často používá pro nepředvídatelné čerpání zásob, produkty ovlivněné sezónou nebo produkty s vysokou cenou.</span><span class="sxs-lookup"><span data-stu-id="cd19a-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="cd19a-118">Následující obrázek znázorňuje příklad.</span><span class="sxs-lookup"><span data-stu-id="cd19a-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="cd19a-119">![Příklad použití kódu pokrytí období](./media/coverage-code-period.png "Příklad použití kódu pokrytí období")</span><span class="sxs-lookup"><span data-stu-id="cd19a-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="cd19a-120">**Požadavek** – v metodě doplňování systém vytváří plánovaný nákup, převod nebo výrobní zakázku podle požadavků na produkt.</span><span class="sxs-lookup"><span data-stu-id="cd19a-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="cd19a-121">Tato metoda se používá pro drahé výrobky, které mají nestálou poptávku.</span><span class="sxs-lookup"><span data-stu-id="cd19a-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="cd19a-122">Kód pokrytí *Požadavek* se často používá pro konfigurovatelné produkty nebo scénáře na objednávku.</span><span class="sxs-lookup"><span data-stu-id="cd19a-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="cd19a-123">Následující obrázek znázorňuje příklad.</span><span class="sxs-lookup"><span data-stu-id="cd19a-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="cd19a-124">![Příklad použití kódu pokrytí požadavku](./media/coverage-code-requirement.png "Příklad použití kódu pokrytí požadavku")</span><span class="sxs-lookup"><span data-stu-id="cd19a-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="cd19a-125">**Min./Max.**</span><span class="sxs-lookup"><span data-stu-id="cd19a-125">**Min./Max.**</span></span> <span data-ttu-id="cd19a-126">- Metoda doplňování je založena na úrovni zásob.</span><span class="sxs-lookup"><span data-stu-id="cd19a-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="cd19a-127">Definuje doplnění zásob až na určitou úroveň, když je předpokládaná úroveň po ruce pod určitou prahovou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="cd19a-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="cd19a-128">Množství doplnění bude rozdíl mezi maximální úrovní a předpokládanou úrovní zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="cd19a-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="cd19a-129">*Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-129">The *Min./Max.*</span></span> <span data-ttu-id="cd19a-130">kód pokrytí se často používá k předvídatelnému čerpání zásob, nejprodávanějším produktům nebo levnějším výrobkům.</span><span class="sxs-lookup"><span data-stu-id="cd19a-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="cd19a-131">Následující obrázek znázorňuje příklad.</span><span class="sxs-lookup"><span data-stu-id="cd19a-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="cd19a-132">![Příklad použití kódu pokrytí Min./Max.](./media/coverage-code-min-max.png "Příklad použití kódu pokrytí Min./Max.")</span><span class="sxs-lookup"><span data-stu-id="cd19a-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="cd19a-133">**Ruční** - v metodě doplňování systém nenavrhuje nákup, převod nebo výrobní objednávky pro daný produkt.</span><span class="sxs-lookup"><span data-stu-id="cd19a-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="cd19a-134">Místo toho je plánovač produktu zodpovědný za vytvoření požadovaných objednávek pro doplnění produktu.</span><span class="sxs-lookup"><span data-stu-id="cd19a-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="cd19a-135">*Ruční* kód pokrytí se často používá u produktů, pro které nejsou plánované objednávky generované systémem požadovány.</span><span class="sxs-lookup"><span data-stu-id="cd19a-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="cd19a-136">Dopad množství objednávky na výchozí nastavení objednávky</span><span class="sxs-lookup"><span data-stu-id="cd19a-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="cd19a-137">Na stránce **Výchozí nastavení objednávky** s vydaným produktem můžete na stránce zadat každé z následujících nastavení množstv na pevných záložkách **Nákupní objednávka**, **Zásoby** a **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="cd19a-138">(Pevná záložka **Zásoby** se používá pro převodní příkazy a výrobní zakázky.)</span><span class="sxs-lookup"><span data-stu-id="cd19a-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="cd19a-139">**Násobek** - Plánované objednávky budou násobkem tohoto množství.</span><span class="sxs-lookup"><span data-stu-id="cd19a-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="cd19a-140">Například pokud je pole **Násobek** nastaveno na *5*, objednávka může být na množství 5, 10, 15, 20 atd.</span><span class="sxs-lookup"><span data-stu-id="cd19a-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="cd19a-141">**Min. objednané množství** - Plánované objednávky nebudou menší než zadaná hodnota.</span><span class="sxs-lookup"><span data-stu-id="cd19a-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="cd19a-142">Například pokud je pole **Min. objednané množství** nastaveno na *10*, bude vytvořena plánovaná objednávka na množství 10, i když k uspokojení poptávky jsou zapotřebí pouze čtyři.</span><span class="sxs-lookup"><span data-stu-id="cd19a-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="cd19a-143">**Max. objednané množství** - Plánované objednávky nebudou překračovat zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cd19a-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="cd19a-144">Pokud je poptávka větší než hodnota **Max. objednané množství**, bude vytvořeno několik plánovaných objednávek, které ji pokryjí.</span><span class="sxs-lookup"><span data-stu-id="cd19a-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="cd19a-145">Například pokud je pole **Max. objednané množství** nastaveno na *100* a poptávka je 450, budou vytvořeny čtyři plánované objednávky pro množství 100 a jedna plánovaná objednávka pro množství 50.</span><span class="sxs-lookup"><span data-stu-id="cd19a-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="cd19a-146">Příklady doplňování, které používají min./max.</span><span class="sxs-lookup"><span data-stu-id="cd19a-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="cd19a-147">kód pokrytí</span><span class="sxs-lookup"><span data-stu-id="cd19a-147">coverage code</span></span>

<span data-ttu-id="cd19a-148">Pokud nezadáte hodnotu v poli **Násobek** pro produkt na stránce **Výchozí nastavení objednávky**  a pokud používáte *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="cd19a-149">metodu doplnění, Optimalizace plánování doplní zásoby až na určitou úroveň, když je předpokládaná úroveň po ruce pod určitou prahovou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="cd19a-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="cd19a-150">Pokud pro produkt definujete více množství, zobrazí se *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="cd19a-151">metoda doplňování mění své chování a bere v úvahu hodnotu **Násobek**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="cd19a-152">Jinými slovy, Optimalizace plánování bude i nadále doplňovat inventář až na definovanou maximální úroveň, pokud je předpokládaná úroveň po ruce menší než definovaná minimální úroveň.</span><span class="sxs-lookup"><span data-stu-id="cd19a-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="cd19a-153">Množství doplňování však musí být násobkem hodnoty **Násobek**.</span><span class="sxs-lookup"><span data-stu-id="cd19a-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="cd19a-154">Pokud množství doplňování (rozdíl mezi maximální úrovní a předpokládanou úrovní po ruce) není násobkem definovaného vícenásobného množství, Optimalizace plánování použije první možnou hodnotu, která spolu s předpokládanou úrovní na straně bude pod maximální úroveň.</span><span class="sxs-lookup"><span data-stu-id="cd19a-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="cd19a-155">Pokud je součet nižší než minimální úroveň, použije optimalizace plánování první hodnotu, která bude spolu s předpovězenou hodnotou vyšší než maximální úroveň.</span><span class="sxs-lookup"><span data-stu-id="cd19a-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="cd19a-156">Následující podkapitoly poskytují několik příkladů, které ukazují, jak množství vícenásobné objednávky produktu ovlivňuje výsledek *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="cd19a-157">metodu doplnění.</span><span class="sxs-lookup"><span data-stu-id="cd19a-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="cd19a-158">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="cd19a-158">Example 1</span></span>

<span data-ttu-id="cd19a-159">Produkt má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="cd19a-159">A product has the following configuration:</span></span>

- <span data-ttu-id="cd19a-160">**Kód pokrytí:** *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="cd19a-161">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="cd19a-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="cd19a-162">**Maximum:** *22*</span><span class="sxs-lookup"><span data-stu-id="cd19a-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="cd19a-163">**Násobek:** *0*</span><span class="sxs-lookup"><span data-stu-id="cd19a-163">**Multiple:** *0*</span></span>

<span data-ttu-id="cd19a-164">K dispozici je 10 kusů zásob na skladě a neexistuje žádná jiná poptávka nebo nabídka.</span><span class="sxs-lookup"><span data-stu-id="cd19a-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="cd19a-165">Když běží hlavní plánování, vytvoří se plánovaná objednávka na 12 kusů, aby se doplnily zásoby na maximální množství.</span><span class="sxs-lookup"><span data-stu-id="cd19a-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="cd19a-166">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="cd19a-166">Example 2</span></span>

<span data-ttu-id="cd19a-167">Produkt má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="cd19a-167">A product has the following configuration:</span></span>

- <span data-ttu-id="cd19a-168">**Kód pokrytí:** *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="cd19a-169">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="cd19a-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="cd19a-170">**Maximum:** *22*</span><span class="sxs-lookup"><span data-stu-id="cd19a-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="cd19a-171">**Násobek:** *5*</span><span class="sxs-lookup"><span data-stu-id="cd19a-171">**Multiple:** *5*</span></span>

<span data-ttu-id="cd19a-172">K dispozici je 10 kusů zásob na skladě a neexistuje žádná jiná poptávka nebo nabídka.</span><span class="sxs-lookup"><span data-stu-id="cd19a-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="cd19a-173">Když běží hlavní plánování, vytvoří se plánovaná objednávka na 10 kusů (protože 15 kusů doplňování plus 10 kusů inventáře na skladě překročí maximální množství).</span><span class="sxs-lookup"><span data-stu-id="cd19a-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="cd19a-174">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="cd19a-174">Example 3</span></span>

<span data-ttu-id="cd19a-175">Produkt má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="cd19a-175">A product has the following configuration:</span></span>

- <span data-ttu-id="cd19a-176">**Kód pokrytí:** *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="cd19a-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="cd19a-177">**Minimum:** *21*</span><span class="sxs-lookup"><span data-stu-id="cd19a-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="cd19a-178">**Maximum:** *24*</span><span class="sxs-lookup"><span data-stu-id="cd19a-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="cd19a-179">**Násobek:** *5*</span><span class="sxs-lookup"><span data-stu-id="cd19a-179">**Multiple:** *5*</span></span>

<span data-ttu-id="cd19a-180">K dispozici je 10 kusů zásob na skladě a neexistuje žádná jiná poptávka nebo nabídka.</span><span class="sxs-lookup"><span data-stu-id="cd19a-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="cd19a-181">Když běží hlavní plánování, vytvoří se plánovaná objednávka na 15 kusů (protože 10 kusů doplňování plus 10 kusů inventáře na skladě bude méně než minimální množství).</span><span class="sxs-lookup"><span data-stu-id="cd19a-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
