---
title: Omezení výrazu a omezení tabulky v modelech konfigurace produktu
description: Toto téma popisuje použití omezení výrazu a omezení tabulky. Omezení řídí hodnoty atributů, které jsou k dispozici při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku. Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc07d5b915e0b878cc7b2ef1d5f3253de8776608
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007690"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="da781-105">Omezení výrazu a omezení tabulky v modelech konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="da781-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da781-106">Toto téma popisuje použití omezení výrazu a omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="da781-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="da781-107">Omezení řídí hodnoty atributů, které jsou k dispozici při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="da781-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="da781-108">Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.</span><span class="sxs-lookup"><span data-stu-id="da781-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="da781-109">Omezení slouží k řízení hodnot atributů, které můžete vybrat při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="da781-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="da781-110">Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.</span><span class="sxs-lookup"><span data-stu-id="da781-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="da781-111">Co jsou omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="da781-111">What are expression constraints?</span></span>
<span data-ttu-id="da781-112">Omezení výrazu se vyznačují výrazem, který používá aritmetické a logické operátory a funkce.</span><span class="sxs-lookup"><span data-stu-id="da781-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="da781-113">Omezení výrazu zapisuje pro určitou komponentu v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="da781-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="da781-114">Nelze ji znovu použít nebo sdílet s jinou součástí.</span><span class="sxs-lookup"><span data-stu-id="da781-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="da781-115">Omezení výrazů pro komponentu se však může odkazovat na atributy dílčích komponent dané komponenty.</span><span class="sxs-lookup"><span data-stu-id="da781-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="da781-116">Co jsou omezení tabulky?</span><span class="sxs-lookup"><span data-stu-id="da781-116">What are table constraints?</span></span>
<span data-ttu-id="da781-117">Omezení tabulky jsou seznam kombinací hodnoty, které jsou povoleny pro atributy při konfiguraci produktu.</span><span class="sxs-lookup"><span data-stu-id="da781-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="da781-118">Definice omezení tabulky lze používat genericky.</span><span class="sxs-lookup"><span data-stu-id="da781-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="da781-119">Při vytváření omezení tabulky pro komponentu v modelu konfigurace produktu je třeba vybrat definici omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="da781-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="da781-120">Chcete-li vytvořit kombinace, které jsou povoleny, přidáváte atributy specifických typů ke komponentám.</span><span class="sxs-lookup"><span data-stu-id="da781-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="da781-121">Každý typ atributu má konkrétní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="da781-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="da781-122">Příklad omezení tabulky</span><span class="sxs-lookup"><span data-stu-id="da781-122">Example of a table constraint</span></span>

<span data-ttu-id="da781-123">Tento příklad ukazuje, jak můžete omezit konfiguraci reproduktoru na konkrétní povrchové úpravy skříně a přední kryty.</span><span class="sxs-lookup"><span data-stu-id="da781-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="da781-124">První tabulka obsahuje povrchové úpravy skříně a přední kryty, které jsou obecně dostupné pro konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="da781-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="da781-125">Hodnoty jsou definovány pro typy atributů **Povrch skříňky** a **Přední mřížka**.</span><span class="sxs-lookup"><span data-stu-id="da781-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="da781-126">Typ atributu</span><span class="sxs-lookup"><span data-stu-id="da781-126">Attribute type</span></span> | <span data-ttu-id="da781-127">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="da781-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="da781-128">Povrch skříňky</span><span class="sxs-lookup"><span data-stu-id="da781-128">Cabinet finish</span></span> | <span data-ttu-id="da781-129">Černá, dub, palisandr, bílá</span><span class="sxs-lookup"><span data-stu-id="da781-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="da781-130">Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="da781-130">Front grill</span></span>    | <span data-ttu-id="da781-131">Černá, kov, bílá</span><span class="sxs-lookup"><span data-stu-id="da781-131">Black, Metal, White</span></span>         |

<span data-ttu-id="da781-132">Následující tabulka zobrazuje kombinace, které jsou definovány omezením tabulky **Barva a povrch**.</span><span class="sxs-lookup"><span data-stu-id="da781-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="da781-133">Pomocí tohoto omezení tabulky lze konfigurovat reproduktor, který má dubový povrch a černou mřížku, palisandrový povrch a bílou mřížku a tak dále.</span><span class="sxs-lookup"><span data-stu-id="da781-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="da781-134">Dokončit</span><span class="sxs-lookup"><span data-stu-id="da781-134">Finish</span></span>         | <span data-ttu-id="da781-135">Mřížka</span><span class="sxs-lookup"><span data-stu-id="da781-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="da781-136">Dub</span><span class="sxs-lookup"><span data-stu-id="da781-136">Oak</span></span>            | <span data-ttu-id="da781-137">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-137">Black</span></span>                       |
| <span data-ttu-id="da781-138">Palisandr</span><span class="sxs-lookup"><span data-stu-id="da781-138">Rosewood</span></span>       | <span data-ttu-id="da781-139">Bílá</span><span class="sxs-lookup"><span data-stu-id="da781-139">White</span></span>                       |
| <span data-ttu-id="da781-140">Bílá</span><span class="sxs-lookup"><span data-stu-id="da781-140">White</span></span>          | <span data-ttu-id="da781-141">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-141">Black</span></span>                       |
| <span data-ttu-id="da781-142">Bílá</span><span class="sxs-lookup"><span data-stu-id="da781-142">White</span></span>          | <span data-ttu-id="da781-143">Bílá</span><span class="sxs-lookup"><span data-stu-id="da781-143">White</span></span>                       |
| <span data-ttu-id="da781-144">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-144">Black</span></span>          | <span data-ttu-id="da781-145">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-145">Black</span></span>                       |
| <span data-ttu-id="da781-146">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-146">Black</span></span>          | <span data-ttu-id="da781-147">Kov</span><span class="sxs-lookup"><span data-stu-id="da781-147">Metal</span></span>                       | 

<span data-ttu-id="da781-148">Můžete vytvořit omezení tabulek definovaná uživatelem nebo systémem.</span><span class="sxs-lookup"><span data-stu-id="da781-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="da781-149">Další informace naleznete v tématu [Omezení tabulek definovaná uživatelem nebo systémem](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="da781-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="da781-150">Jaká syntax se používá pro řešení omezení psaní?</span><span class="sxs-lookup"><span data-stu-id="da781-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="da781-151">Když píšete omezení, musíte použít syntaxi jazyka OML (Optimization Modeling Language).</span><span class="sxs-lookup"><span data-stu-id="da781-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="da781-152">Systém používá k řešení omezení produkt Microsoft Solver Foundation.</span><span class="sxs-lookup"><span data-stu-id="da781-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="da781-153">Mám použít omezení tabulky nebo omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="da781-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="da781-154">Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.</span><span class="sxs-lookup"><span data-stu-id="da781-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="da781-155">Omezení tabulky vytváříte jako matici, zatímco omezení výrazu je jednotlivý výraz.</span><span class="sxs-lookup"><span data-stu-id="da781-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="da781-156">Při konfiguraci produktu nezáleží na omezení, jaký druh omezení se použije.</span><span class="sxs-lookup"><span data-stu-id="da781-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="da781-157">V následujícím příkladu je znázorněn rozdíl v těchto dvou metodách.</span><span class="sxs-lookup"><span data-stu-id="da781-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="da781-158">Při konfiguraci produktu pomocí následujícího nastavení omezení jsou povoleny tyto kombinace:</span><span class="sxs-lookup"><span data-stu-id="da781-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="da781-159">Černá barva produktu a velikost 30 nebo 50</span><span class="sxs-lookup"><span data-stu-id="da781-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="da781-160">Červená barva produktu a velikost 20</span><span class="sxs-lookup"><span data-stu-id="da781-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="da781-161">Nastavení omezení tabulky</span><span class="sxs-lookup"><span data-stu-id="da781-161">Table constraint setup</span></span>

| <span data-ttu-id="da781-162">Barva</span><span class="sxs-lookup"><span data-stu-id="da781-162">Color</span></span> | <span data-ttu-id="da781-163">Velikost</span><span class="sxs-lookup"><span data-stu-id="da781-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="da781-164">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-164">Black</span></span> | <span data-ttu-id="da781-165">30</span><span class="sxs-lookup"><span data-stu-id="da781-165">30</span></span>   |
| <span data-ttu-id="da781-166">Černá</span><span class="sxs-lookup"><span data-stu-id="da781-166">Black</span></span> | <span data-ttu-id="da781-167">50</span><span class="sxs-lookup"><span data-stu-id="da781-167">50</span></span>   |
| <span data-ttu-id="da781-168">Červená</span><span class="sxs-lookup"><span data-stu-id="da781-168">Red</span></span>   | <span data-ttu-id="da781-169">20</span><span class="sxs-lookup"><span data-stu-id="da781-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="da781-170">Nastavení omezení výrazu</span><span class="sxs-lookup"><span data-stu-id="da781-170">Expression constraint setup</span></span>

<span data-ttu-id="da781-171">(Barva == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="da781-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="da781-172">Mám používat operátory nebo infixový zápis při psaní omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="da781-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="da781-173">Můžete napsat omezení výrazu buď pomocí dostupných prefixových operátorů, nebo pomocí infixového zápisu.</span><span class="sxs-lookup"><span data-stu-id="da781-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="da781-174">U operátorů **Min**, **Max** a **Abs** nelze použít infixový zápis.</span><span class="sxs-lookup"><span data-stu-id="da781-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="da781-175">Tyto operátory jsou k dispozici jako standardní operátory ve většině programovacích jazyků.</span><span class="sxs-lookup"><span data-stu-id="da781-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="da781-176">Které operátory a infixový zápis můžu používat při psaní omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="da781-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="da781-177">V následujících tabulkách jsou uvedeny operátory a infixový zápis, které lze použít při zápisu omezení výrazu pro komponentu v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="da781-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="da781-178">V příkladech v první tabulce můžete vidět způsob zápisu výrazu pomocí infixového zápisu nebo operátorů.</span><span class="sxs-lookup"><span data-stu-id="da781-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da781-179">Operátor</span><span class="sxs-lookup"><span data-stu-id="da781-179">Operator</span></span></th>
<th><span data-ttu-id="da781-180">Popis</span><span class="sxs-lookup"><span data-stu-id="da781-180">Description</span></span></th>
<th><span data-ttu-id="da781-181">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da781-181">Syntax</span></span></th>
<th><span data-ttu-id="da781-182">Příklad</span><span class="sxs-lookup"><span data-stu-id="da781-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da781-183">Implikace</span><span class="sxs-lookup"><span data-stu-id="da781-183">Implies</span></span></td>
<td><span data-ttu-id="da781-184">To platí v případě, že první podmínka není splněna, druhá podmínka je pravda, nebo obojí.</span><span class="sxs-lookup"><span data-stu-id="da781-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="da781-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="da781-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-186"><strong>Operátor:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="da781-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="da781-187"><strong>Infixový zápis:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="da781-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da781-188">A</span><span class="sxs-lookup"><span data-stu-id="da781-188">And</span></span></td>
<td><span data-ttu-id="da781-189">To platí pouze v případě, že jsou splněny všechny podmínky.</span><span class="sxs-lookup"><span data-stu-id="da781-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="da781-190">Pokud je počet podmínek 0 (nula), výsledkem je <strong>pravda</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="da781-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="da781-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-192"><strong>Operátor:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="da781-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="da781-193"><strong>Infixový zápis:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="da781-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da781-194">Nebo</span><span class="sxs-lookup"><span data-stu-id="da781-194">Or</span></span></td>
<td><span data-ttu-id="da781-195">To platí při splnění libovolné podmínky.</span><span class="sxs-lookup"><span data-stu-id="da781-195">This is true if any condition is true.</span></span> <span data-ttu-id="da781-196">Pokud je počet podmínek 0 (nula), výsledkem je <strong>nepravda</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="da781-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="da781-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-198"><strong>Operátor:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="da781-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="da781-199"><strong>Infixový zápis:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="da781-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da781-200">Kladný</span><span class="sxs-lookup"><span data-stu-id="da781-200">Plus</span></span></td>
<td><span data-ttu-id="da781-201">Sečte podmínky.</span><span class="sxs-lookup"><span data-stu-id="da781-201">This sums its conditions.</span></span> <span data-ttu-id="da781-202">Pokud je počet podmínek 0 (nula), výsledkem je <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="da781-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="da781-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-204"><strong>Operátor:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="da781-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="da781-205"><strong>Infixový zápis:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="da781-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da781-206">Záporný</span><span class="sxs-lookup"><span data-stu-id="da781-206">Minus</span></span></td>
<td><span data-ttu-id="da781-207">Argumenty se negují.</span><span class="sxs-lookup"><span data-stu-id="da781-207">This negates its argument.</span></span> <span data-ttu-id="da781-208">Musí mít právě jednu podmínku.</span><span class="sxs-lookup"><span data-stu-id="da781-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="da781-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="da781-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-210"><strong>Operátor:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="da781-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="da781-211"><strong>Infixový zápis:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="da781-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da781-212">Funkce ABS</span><span class="sxs-lookup"><span data-stu-id="da781-212">Abs</span></span></td>
<td><span data-ttu-id="da781-213">Vezme absolutní hodnotu podmínky.</span><span class="sxs-lookup"><span data-stu-id="da781-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="da781-214">Musí mít právě jednu podmínku.</span><span class="sxs-lookup"><span data-stu-id="da781-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="da781-215">ABS [výraz]</span><span class="sxs-lookup"><span data-stu-id="da781-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="da781-216"><strong>Operátor:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="da781-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da781-217">Časy</span><span class="sxs-lookup"><span data-stu-id="da781-217">Times</span></span></td>
<td><span data-ttu-id="da781-218">Vezme násobek podmínek.</span><span class="sxs-lookup"><span data-stu-id="da781-218">This takes the product of its conditions.</span></span> <span data-ttu-id="da781-219">Pokud je počet podmínek 0 (nula), výsledkem je <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="da781-220">Krát[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="da781-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-221"><strong>Operátor:</strong> Doby[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="da781-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="da781-222"><strong>Infixový zápis:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="da781-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da781-223">Výkon</span><span class="sxs-lookup"><span data-stu-id="da781-223">Power</span></span></td>
<td><span data-ttu-id="da781-224">Vezme mocninu.</span><span class="sxs-lookup"><span data-stu-id="da781-224">This takes an exponential.</span></span> <span data-ttu-id="da781-225">Umocňuje se zprava doleva.</span><span class="sxs-lookup"><span data-stu-id="da781-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="da781-226">(Jinými slovy je zprava asociativní.) Proto je <strong>Power[a, b, c]</strong> ekvivalentní <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="da781-227"><strong>Výkon</strong> lze použít pouze s exponentem jako kladnou konstantou.</span><span class="sxs-lookup"><span data-stu-id="da781-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="da781-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="da781-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-229"><strong>Operátor:</strong> Výkon[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="da781-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="da781-230"><strong>Infixový zápis:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="da781-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da781-231">Maximum</span><span class="sxs-lookup"><span data-stu-id="da781-231">Max</span></span></td>
<td><span data-ttu-id="da781-232">Výsledkem je největší podmínka.</span><span class="sxs-lookup"><span data-stu-id="da781-232">This produces the largest condition.</span></span> <span data-ttu-id="da781-233">Pokud je počet podmínek 0 (nula), výsledkem je <strong>nekonečno</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="da781-234">Max[argumenty]</span><span class="sxs-lookup"><span data-stu-id="da781-234">Max[args]</span></span></td>
<td><span data-ttu-id="da781-235"><strong>Operátor:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="da781-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da781-236">Minimum</span><span class="sxs-lookup"><span data-stu-id="da781-236">Min</span></span></td>
<td><span data-ttu-id="da781-237">Výsledkem je nejmenší podmínka.</span><span class="sxs-lookup"><span data-stu-id="da781-237">This produces the smallest condition.</span></span> <span data-ttu-id="da781-238">Pokud je počet podmínek 0 (nula), výsledkem je <strong>nekonečno</strong>.</span><span class="sxs-lookup"><span data-stu-id="da781-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="da781-239">Min[argumenty]</span><span class="sxs-lookup"><span data-stu-id="da781-239">Min[args]</span></span></td>
<td><span data-ttu-id="da781-240"><strong>Operátor:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="da781-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da781-241">Ne</span><span class="sxs-lookup"><span data-stu-id="da781-241">Not</span></span></td>
<td><span data-ttu-id="da781-242">Výsledkem logický opak podmínky.</span><span class="sxs-lookup"><span data-stu-id="da781-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="da781-243">Musí mít právě jednu podmínku.</span><span class="sxs-lookup"><span data-stu-id="da781-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="da781-244">Ne[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="da781-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="da781-245"><strong>Operátor:</strong> Ne[x] &amp; Ne[y == 3]</span><span class="sxs-lookup"><span data-stu-id="da781-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="da781-246"><strong>Infixový zápis:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="da781-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="da781-247">V následující tabulce jsou uvedeny příklady, jak zapsat infixový zápis.</span><span class="sxs-lookup"><span data-stu-id="da781-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="da781-248">Infixový zápis</span><span class="sxs-lookup"><span data-stu-id="da781-248">Infix notation</span></span>   |                                          <span data-ttu-id="da781-249">popis</span><span class="sxs-lookup"><span data-stu-id="da781-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="da781-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="da781-250">x + y + z</span></span>     |                                           <span data-ttu-id="da781-251">Dodatek</span><span class="sxs-lookup"><span data-stu-id="da781-251">Addition</span></span>                                            |
|    <span data-ttu-id="da781-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="da781-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="da781-253">Násobení</span><span class="sxs-lookup"><span data-stu-id="da781-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="da781-254">x - y</span><span class="sxs-lookup"><span data-stu-id="da781-254">x - y</span></span>       | <span data-ttu-id="da781-255">Binární odčítání je převedeno stejně jako binární součet, kde je negovaná druhá podmínka.</span><span class="sxs-lookup"><span data-stu-id="da781-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="da781-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="da781-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="da781-257">Umocňování s pravou asociativitou</span><span class="sxs-lookup"><span data-stu-id="da781-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="da781-258">!x</span><span class="sxs-lookup"><span data-stu-id="da781-258">!x</span></span>         |                                          <span data-ttu-id="da781-259">Logické ne</span><span class="sxs-lookup"><span data-stu-id="da781-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="da781-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="da781-260">x -: y</span></span>       |                                      <span data-ttu-id="da781-261">Logická implikace</span><span class="sxs-lookup"><span data-stu-id="da781-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="da781-262">x</span><span class="sxs-lookup"><span data-stu-id="da781-262">x</span></span>         |                                               <span data-ttu-id="da781-263">y</span><span class="sxs-lookup"><span data-stu-id="da781-263">y</span></span>                                               |
|     <span data-ttu-id="da781-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="da781-264">x & y & z</span></span>     |                                          <span data-ttu-id="da781-265">Logické a</span><span class="sxs-lookup"><span data-stu-id="da781-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="da781-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="da781-266">x == y == z</span></span>    |                                           <span data-ttu-id="da781-267">Rovnost</span><span class="sxs-lookup"><span data-stu-id="da781-267">Equality</span></span>                                            |
|    <span data-ttu-id="da781-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="da781-268">x != y != z</span></span>    |                                           <span data-ttu-id="da781-269">Různé</span><span class="sxs-lookup"><span data-stu-id="da781-269">Distinct</span></span>                                            |
|  <span data-ttu-id="da781-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="da781-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="da781-271">Je menší než</span><span class="sxs-lookup"><span data-stu-id="da781-271">Less than</span></span>                                           |
|  <span data-ttu-id="da781-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="da781-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="da781-273">Je větší než</span><span class="sxs-lookup"><span data-stu-id="da781-273">Greater than</span></span>                                          |
| <span data-ttu-id="da781-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="da781-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="da781-275">Menší než nebo rovno</span><span class="sxs-lookup"><span data-stu-id="da781-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="da781-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="da781-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="da781-277">Větší než nebo rovno</span><span class="sxs-lookup"><span data-stu-id="da781-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="da781-278">(x)</span><span class="sxs-lookup"><span data-stu-id="da781-278">(x)</span></span>        |                           <span data-ttu-id="da781-279">Závorky ruší výchozí priority.</span><span class="sxs-lookup"><span data-stu-id="da781-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="da781-280">Proč nejsou má omezení výrazu vyhodnocena správně?</span><span class="sxs-lookup"><span data-stu-id="da781-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="da781-281">Rezervovaná slovo nelze použít jako řešitelské názvy atributů, komponentů nebo dílčích komponentů v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="da781-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="da781-282">Tento seznam obsahuje rezervovaná klíčová slova, která nelze použít:</span><span class="sxs-lookup"><span data-stu-id="da781-282">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="da781-283">Horní mez</span><span class="sxs-lookup"><span data-stu-id="da781-283">Ceiling</span></span>
-   <span data-ttu-id="da781-284">Prvek</span><span class="sxs-lookup"><span data-stu-id="da781-284">Element</span></span>
-   <span data-ttu-id="da781-285">Rovno</span><span class="sxs-lookup"><span data-stu-id="da781-285">Equal</span></span>
-   <span data-ttu-id="da781-286">Podlaží</span><span class="sxs-lookup"><span data-stu-id="da781-286">Floor</span></span>
-   <span data-ttu-id="da781-287">Jestliže</span><span class="sxs-lookup"><span data-stu-id="da781-287">If</span></span>
-   <span data-ttu-id="da781-288">Menší</span><span class="sxs-lookup"><span data-stu-id="da781-288">Less</span></span>
-   <span data-ttu-id="da781-289">Větší</span><span class="sxs-lookup"><span data-stu-id="da781-289">Greater</span></span>
-   <span data-ttu-id="da781-290">Implikace</span><span class="sxs-lookup"><span data-stu-id="da781-290">Implies</span></span>
-   <span data-ttu-id="da781-291">Protokol</span><span class="sxs-lookup"><span data-stu-id="da781-291">Log</span></span>
-   <span data-ttu-id="da781-292">Maximum</span><span class="sxs-lookup"><span data-stu-id="da781-292">Max</span></span>
-   <span data-ttu-id="da781-293">Minimum</span><span class="sxs-lookup"><span data-stu-id="da781-293">Min</span></span>
-   <span data-ttu-id="da781-294">Záporný</span><span class="sxs-lookup"><span data-stu-id="da781-294">Minus</span></span>
-   <span data-ttu-id="da781-295">Kladný</span><span class="sxs-lookup"><span data-stu-id="da781-295">Plus</span></span>
-   <span data-ttu-id="da781-296">Výkon</span><span class="sxs-lookup"><span data-stu-id="da781-296">Power</span></span>
-   <span data-ttu-id="da781-297">Časy</span><span class="sxs-lookup"><span data-stu-id="da781-297">Times</span></span>
-   <span data-ttu-id="da781-298">Úsek</span><span class="sxs-lookup"><span data-stu-id="da781-298">Slot</span></span>
-   <span data-ttu-id="da781-299">Model</span><span class="sxs-lookup"><span data-stu-id="da781-299">Model</span></span>
-   <span data-ttu-id="da781-300">Rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="da781-300">Decision</span></span>
-   <span data-ttu-id="da781-301">Cíl</span><span class="sxs-lookup"><span data-stu-id="da781-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="da781-302">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="da781-302">Additional resources</span></span>
--------

[<span data-ttu-id="da781-303">Vytvoření omezení výrazu</span><span class="sxs-lookup"><span data-stu-id="da781-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="da781-304">Přidání výpočtu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="da781-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



