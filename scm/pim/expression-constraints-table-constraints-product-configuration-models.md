---
title: "Omezení výrazu a omezení tabulky v modelech konfigurace produktu"
description: "Toto téma popisuje použití omezení výrazu a omezení tabulky. Omezení řídí hodnoty atributů, které jsou k dispozici při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku. Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 66d5ec61c1d69ebc8a8fc10d0b9b2a4b174729ee
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="2e173-105">Omezení výrazu a omezení tabulky v modelech konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="2e173-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e173-106">Toto téma popisuje použití omezení výrazu a omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="2e173-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="2e173-107">Omezení řídí hodnoty atributů, které jsou k dispozici při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="2e173-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="2e173-108">Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.</span><span class="sxs-lookup"><span data-stu-id="2e173-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="2e173-109">Omezení slouží k řízení hodnot atributů, které můžete vybrat při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="2e173-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="2e173-110">Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.</span><span class="sxs-lookup"><span data-stu-id="2e173-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="2e173-111">Co jsou omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="2e173-111">What are expression constraints?</span></span>
<span data-ttu-id="2e173-112">Omezení výrazu se vyznačují výrazem, který používá aritmetické a logické operátory a funkce.</span><span class="sxs-lookup"><span data-stu-id="2e173-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="2e173-113">Omezení výrazu zapisuje pro určitou komponentu v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="2e173-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="2e173-114">Nelze ji znovu použít nebo sdílet s jinou součástí.</span><span class="sxs-lookup"><span data-stu-id="2e173-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="2e173-115">Omezení výrazů pro komponentu se však může odkazovat na atributy dílčích komponent dané komponenty.</span><span class="sxs-lookup"><span data-stu-id="2e173-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="2e173-116">Co jsou omezení tabulky?</span><span class="sxs-lookup"><span data-stu-id="2e173-116">What are table constraints?</span></span>
<span data-ttu-id="2e173-117">Omezení tabulky jsou seznam kombinací hodnoty, které jsou povoleny pro atributy při konfiguraci produktu.</span><span class="sxs-lookup"><span data-stu-id="2e173-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="2e173-118">Definice omezení tabulky lze používat genericky.</span><span class="sxs-lookup"><span data-stu-id="2e173-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="2e173-119">Při vytváření omezení tabulky pro komponentu v modelu konfigurace produktu je třeba vybrat definici omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="2e173-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="2e173-120">Chcete-li vytvořit kombinace, které jsou povoleny, přidáváte atributy specifických typů ke komponentám.</span><span class="sxs-lookup"><span data-stu-id="2e173-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="2e173-121">Každý typ atributu má konkrétní hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2e173-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="2e173-122">Příklad omezení tabulky</span><span class="sxs-lookup"><span data-stu-id="2e173-122">Example of a table constraint</span></span>

<span data-ttu-id="2e173-123">Tento příklad ukazuje, jak můžete omezit konfiguraci reproduktoru na konkrétní povrchové úpravy skříně a přední kryty.</span><span class="sxs-lookup"><span data-stu-id="2e173-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="2e173-124">První tabulka obsahuje povrchové úpravy skříně a přední kryty, které jsou obecně dostupné pro konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="2e173-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="2e173-125">Hodnoty jsou definovány pro typy atributů **Povrch skříňky** a **Přední mřížka**.</span><span class="sxs-lookup"><span data-stu-id="2e173-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="2e173-126">Typ atributu</span><span class="sxs-lookup"><span data-stu-id="2e173-126">Attribute type</span></span> | <span data-ttu-id="2e173-127">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="2e173-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="2e173-128">Povrch skříňky</span><span class="sxs-lookup"><span data-stu-id="2e173-128">Cabinet finish</span></span> | <span data-ttu-id="2e173-129">Černá, dub, palisandr, bílá</span><span class="sxs-lookup"><span data-stu-id="2e173-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="2e173-130">Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="2e173-130">Front grill</span></span>    | <span data-ttu-id="2e173-131">Černá, kov, bílá</span><span class="sxs-lookup"><span data-stu-id="2e173-131">Black, Metal, White</span></span>         |

<span data-ttu-id="2e173-132">Následující tabulka zobrazuje kombinace, které jsou definovány omezením tabulky **Barva a povrch**.</span><span class="sxs-lookup"><span data-stu-id="2e173-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="2e173-133">Pomocí tohoto omezení tabulky lze konfigurovat reproduktor, který má dubový povrch a černou mřížku, palisandrový povrch a bílou mřížku a tak dále.</span><span class="sxs-lookup"><span data-stu-id="2e173-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="2e173-134">Dokončit</span><span class="sxs-lookup"><span data-stu-id="2e173-134">Finish</span></span>         | <span data-ttu-id="2e173-135">Mřížka</span><span class="sxs-lookup"><span data-stu-id="2e173-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="2e173-136">Dub</span><span class="sxs-lookup"><span data-stu-id="2e173-136">Oak</span></span>            | <span data-ttu-id="2e173-137">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-137">Black</span></span>                       |
| <span data-ttu-id="2e173-138">Palisandr</span><span class="sxs-lookup"><span data-stu-id="2e173-138">Rosewood</span></span>       | <span data-ttu-id="2e173-139">Bílá</span><span class="sxs-lookup"><span data-stu-id="2e173-139">White</span></span>                       |
| <span data-ttu-id="2e173-140">Bílá</span><span class="sxs-lookup"><span data-stu-id="2e173-140">White</span></span>          | <span data-ttu-id="2e173-141">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-141">Black</span></span>                       |
| <span data-ttu-id="2e173-142">Bílá</span><span class="sxs-lookup"><span data-stu-id="2e173-142">White</span></span>          | <span data-ttu-id="2e173-143">Bílá</span><span class="sxs-lookup"><span data-stu-id="2e173-143">White</span></span>                       |
| <span data-ttu-id="2e173-144">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-144">Black</span></span>          | <span data-ttu-id="2e173-145">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-145">Black</span></span>                       |
| <span data-ttu-id="2e173-146">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-146">Black</span></span>          | <span data-ttu-id="2e173-147">Kov</span><span class="sxs-lookup"><span data-stu-id="2e173-147">Metal</span></span>                       | 

<span data-ttu-id="2e173-148">Můžete vytvořit omezení tabulek definovaná uživatelem nebo systémem.</span><span class="sxs-lookup"><span data-stu-id="2e173-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="2e173-149">Další informace naleznete v tématu [Omezení tabulek definovaná uživatelem nebo systémem](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="2e173-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="2e173-150">Jaká syntax se používá pro řešení omezení psaní?</span><span class="sxs-lookup"><span data-stu-id="2e173-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="2e173-151">Když píšete omezení, musíte použít syntaxi jazyka OML (Optimization Modeling Language).</span><span class="sxs-lookup"><span data-stu-id="2e173-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="2e173-152">Systém používá k řešení omezení produkt Microsoft Solver Foundation.</span><span class="sxs-lookup"><span data-stu-id="2e173-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="2e173-153">Mám použít omezení tabulky nebo omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="2e173-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="2e173-154">Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.</span><span class="sxs-lookup"><span data-stu-id="2e173-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="2e173-155">Omezení tabulky vytváříte jako matici, zatímco omezení výrazu je jednotlivý výraz.</span><span class="sxs-lookup"><span data-stu-id="2e173-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="2e173-156">Při konfiguraci produktu nezáleží na omezení, jaký druh omezení se použije.</span><span class="sxs-lookup"><span data-stu-id="2e173-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="2e173-157">V následujícím příkladu je znázorněn rozdíl v těchto dvou metodách.</span><span class="sxs-lookup"><span data-stu-id="2e173-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="2e173-158">Při konfiguraci produktu pomocí následujícího nastavení omezení jsou povoleny tyto kombinace:</span><span class="sxs-lookup"><span data-stu-id="2e173-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="2e173-159">Černá barva produktu a velikost 30 nebo 50</span><span class="sxs-lookup"><span data-stu-id="2e173-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="2e173-160">Červená barva produktu a velikost 20</span><span class="sxs-lookup"><span data-stu-id="2e173-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="2e173-161">Nastavení omezení tabulky</span><span class="sxs-lookup"><span data-stu-id="2e173-161">Table constraint setup</span></span>

| <span data-ttu-id="2e173-162">Barva</span><span class="sxs-lookup"><span data-stu-id="2e173-162">Color</span></span> | <span data-ttu-id="2e173-163">Velikost</span><span class="sxs-lookup"><span data-stu-id="2e173-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="2e173-164">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-164">Black</span></span> | <span data-ttu-id="2e173-165">30</span><span class="sxs-lookup"><span data-stu-id="2e173-165">30</span></span>   |
| <span data-ttu-id="2e173-166">Černá</span><span class="sxs-lookup"><span data-stu-id="2e173-166">Black</span></span> | <span data-ttu-id="2e173-167">50</span><span class="sxs-lookup"><span data-stu-id="2e173-167">50</span></span>   |
| <span data-ttu-id="2e173-168">Červená</span><span class="sxs-lookup"><span data-stu-id="2e173-168">Red</span></span>   | <span data-ttu-id="2e173-169">20</span><span class="sxs-lookup"><span data-stu-id="2e173-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="2e173-170">Nastavení omezení výrazu</span><span class="sxs-lookup"><span data-stu-id="2e173-170">Expression constraint setup</span></span>

<span data-ttu-id="2e173-171">(Barva == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="2e173-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="2e173-172">Mám používat operátory nebo infixový zápis při psaní omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="2e173-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="2e173-173">Můžete napsat omezení výrazu buď pomocí dostupných prefixových operátorů, nebo pomocí infixového zápisu.</span><span class="sxs-lookup"><span data-stu-id="2e173-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="2e173-174">U operátorů **Min**, **Max** a **Abs** nelze použít infixový zápis.</span><span class="sxs-lookup"><span data-stu-id="2e173-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="2e173-175">Tyto operátory jsou k dispozici jako standardní operátory ve většině programovacích jazyků.</span><span class="sxs-lookup"><span data-stu-id="2e173-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="2e173-176">Které operátory a infixový zápis můžu používat při psaní omezení výrazu?</span><span class="sxs-lookup"><span data-stu-id="2e173-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="2e173-177">V následujících tabulkách jsou uvedeny operátory a infixový zápis, které lze použít při zápisu omezení výrazu pro komponentu v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="2e173-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="2e173-178">V příkladech v první tabulce můžete vidět způsob zápisu výrazu pomocí infixového zápisu nebo operátorů.</span><span class="sxs-lookup"><span data-stu-id="2e173-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e173-179">Operátor</span><span class="sxs-lookup"><span data-stu-id="2e173-179">Operator</span></span></th>
<th><span data-ttu-id="2e173-180">Popis</span><span class="sxs-lookup"><span data-stu-id="2e173-180">Description</span></span></th>
<th><span data-ttu-id="2e173-181">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e173-181">Syntax</span></span></th>
<th><span data-ttu-id="2e173-182">Příklad</span><span class="sxs-lookup"><span data-stu-id="2e173-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e173-183">Implikace</span><span class="sxs-lookup"><span data-stu-id="2e173-183">Implies</span></span></td>
<td><span data-ttu-id="2e173-184">To platí v případě, že první podmínka není splněna, druhá podmínka je pravda, nebo obojí.</span><span class="sxs-lookup"><span data-stu-id="2e173-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="2e173-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="2e173-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-186"><strong>Operátor:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="2e173-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="2e173-187"><strong>Infixový zápis:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="2e173-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e173-188">A</span><span class="sxs-lookup"><span data-stu-id="2e173-188">And</span></span></td>
<td><span data-ttu-id="2e173-189">To platí pouze v případě, že jsou splněny všechny podmínky.</span><span class="sxs-lookup"><span data-stu-id="2e173-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="2e173-190">Pokud je počet podmínek 0 (nula), výsledkem je <strong>pravda</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="2e173-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="2e173-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-192"><strong>Operátor:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="2e173-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="2e173-193"><strong>Infixový zápis:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="2e173-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e173-194">Nebo</span><span class="sxs-lookup"><span data-stu-id="2e173-194">Or</span></span></td>
<td><span data-ttu-id="2e173-195">To platí při splnění libovolné podmínky.</span><span class="sxs-lookup"><span data-stu-id="2e173-195">This is true if any condition is true.</span></span> <span data-ttu-id="2e173-196">Pokud je počet podmínek 0 (nula), výsledkem je <strong>nepravda</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="2e173-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="2e173-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-198"><strong>Operátor:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="2e173-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="2e173-199"><strong>Infixový zápis:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="2e173-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e173-200">Kladný</span><span class="sxs-lookup"><span data-stu-id="2e173-200">Plus</span></span></td>
<td><span data-ttu-id="2e173-201">Sečte podmínky.</span><span class="sxs-lookup"><span data-stu-id="2e173-201">This sums its conditions.</span></span> <span data-ttu-id="2e173-202">Pokud je počet podmínek 0 (nula), výsledkem je <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="2e173-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="2e173-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-204"><strong>Operátor:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2e173-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="2e173-205"><strong>Infixový zápis:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="2e173-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e173-206">Záporný</span><span class="sxs-lookup"><span data-stu-id="2e173-206">Minus</span></span></td>
<td><span data-ttu-id="2e173-207">Argumenty se negují.</span><span class="sxs-lookup"><span data-stu-id="2e173-207">This negates its argument.</span></span> <span data-ttu-id="2e173-208">Musí mít právě jednu podmínku.</span><span class="sxs-lookup"><span data-stu-id="2e173-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="2e173-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="2e173-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-210"><strong>Operátor:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="2e173-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="2e173-211"><strong>Infixový zápis:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="2e173-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e173-212">Funkce ABS</span><span class="sxs-lookup"><span data-stu-id="2e173-212">Abs</span></span></td>
<td><span data-ttu-id="2e173-213">Vezme absolutní hodnotu podmínky.</span><span class="sxs-lookup"><span data-stu-id="2e173-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="2e173-214">Musí mít právě jednu podmínku.</span><span class="sxs-lookup"><span data-stu-id="2e173-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="2e173-215">ABS [výraz]</span><span class="sxs-lookup"><span data-stu-id="2e173-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="2e173-216"><strong>Operátor:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="2e173-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e173-217">Časy</span><span class="sxs-lookup"><span data-stu-id="2e173-217">Times</span></span></td>
<td><span data-ttu-id="2e173-218">Vezme násobek podmínek.</span><span class="sxs-lookup"><span data-stu-id="2e173-218">This takes the product of its conditions.</span></span> <span data-ttu-id="2e173-219">Pokud je počet podmínek 0 (nula), výsledkem je <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="2e173-220">Krát[args], infix: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="2e173-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-221"><strong>Operátor:</strong> Doby[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2e173-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="2e173-222"><strong>Infixový zápis:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="2e173-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e173-223">Výkon</span><span class="sxs-lookup"><span data-stu-id="2e173-223">Power</span></span></td>
<td><span data-ttu-id="2e173-224">Vezme mocninu.</span><span class="sxs-lookup"><span data-stu-id="2e173-224">This takes an exponential.</span></span> <span data-ttu-id="2e173-225">Umocňuje se zprava doleva.</span><span class="sxs-lookup"><span data-stu-id="2e173-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="2e173-226">(Jinými slovy je zprava asociativní.) Proto je <strong>Power[a, b, c]</strong> ekvivalentní <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="2e173-227"><strong>Výkon</strong> lze použít pouze s exponentem jako kladnou konstantou.</span><span class="sxs-lookup"><span data-stu-id="2e173-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="2e173-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="2e173-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-229"><strong>Operátor:</strong> Výkon[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="2e173-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="2e173-230"><strong>Infixový zápis:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="2e173-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e173-231">Maximum</span><span class="sxs-lookup"><span data-stu-id="2e173-231">Max</span></span></td>
<td><span data-ttu-id="2e173-232">Výsledkem je největší podmínka.</span><span class="sxs-lookup"><span data-stu-id="2e173-232">This produces the largest condition.</span></span> <span data-ttu-id="2e173-233">Pokud je počet podmínek 0 (nula), výsledkem je <strong>nekonečno</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="2e173-234">Max[argumenty]</span><span class="sxs-lookup"><span data-stu-id="2e173-234">Max[args]</span></span></td>
<td><span data-ttu-id="2e173-235"><strong>Operátor:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2e173-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e173-236">Minimum</span><span class="sxs-lookup"><span data-stu-id="2e173-236">Min</span></span></td>
<td><span data-ttu-id="2e173-237">Výsledkem je nejmenší podmínka.</span><span class="sxs-lookup"><span data-stu-id="2e173-237">This produces the smallest condition.</span></span> <span data-ttu-id="2e173-238">Pokud je počet podmínek 0 (nula), výsledkem je <strong>nekonečno</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e173-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="2e173-239">Min[argumenty]</span><span class="sxs-lookup"><span data-stu-id="2e173-239">Min[args]</span></span></td>
<td><span data-ttu-id="2e173-240"><strong>Operátor:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2e173-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e173-241">Ne</span><span class="sxs-lookup"><span data-stu-id="2e173-241">Not</span></span></td>
<td><span data-ttu-id="2e173-242">Výsledkem logický opak podmínky.</span><span class="sxs-lookup"><span data-stu-id="2e173-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="2e173-243">Musí mít právě jednu podmínku.</span><span class="sxs-lookup"><span data-stu-id="2e173-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="2e173-244">Ne[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="2e173-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="2e173-245"><strong>Operátor:</strong> Ne[x] &amp; Ne[y == 3]</span><span class="sxs-lookup"><span data-stu-id="2e173-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="2e173-246"><strong>Infixový zápis:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="2e173-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2e173-247">V následující tabulce jsou uvedeny příklady, jak zapsat infixový zápis.</span><span class="sxs-lookup"><span data-stu-id="2e173-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="2e173-248">Infixový zápis</span><span class="sxs-lookup"><span data-stu-id="2e173-248">Infix notation</span></span>    | <span data-ttu-id="2e173-249">popis</span><span class="sxs-lookup"><span data-stu-id="2e173-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e173-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="2e173-250">x + y + z</span></span>         | <span data-ttu-id="2e173-251">Dodatek</span><span class="sxs-lookup"><span data-stu-id="2e173-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="2e173-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="2e173-252">x \* y \* z</span></span>       | <span data-ttu-id="2e173-253">Násobení</span><span class="sxs-lookup"><span data-stu-id="2e173-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="2e173-254">x - y</span><span class="sxs-lookup"><span data-stu-id="2e173-254">x - y</span></span>             | <span data-ttu-id="2e173-255">Binární odčítání je převedeno stejně jako binární součet, kde je negovaná druhá podmínka.</span><span class="sxs-lookup"><span data-stu-id="2e173-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="2e173-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="2e173-256">x ^ y ^ z</span></span>         | <span data-ttu-id="2e173-257">Umocňování s pravou asociativitou</span><span class="sxs-lookup"><span data-stu-id="2e173-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="2e173-258">!x</span><span class="sxs-lookup"><span data-stu-id="2e173-258">!x</span></span>                | <span data-ttu-id="2e173-259">Logické ne</span><span class="sxs-lookup"><span data-stu-id="2e173-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="2e173-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="2e173-260">x -: y</span></span>            | <span data-ttu-id="2e173-261">Logická implikace</span><span class="sxs-lookup"><span data-stu-id="2e173-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="2e173-262"> linka</span><span class="sxs-lookup"><span data-stu-id="2e173-262">x</span></span> | <span data-ttu-id="2e173-263">y</span><span class="sxs-lookup"><span data-stu-id="2e173-263">y</span></span> | <span data-ttu-id="2e173-264">z</span><span class="sxs-lookup"><span data-stu-id="2e173-264">z</span></span>         | <span data-ttu-id="2e173-265">Logické nebo</span><span class="sxs-lookup"><span data-stu-id="2e173-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="2e173-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="2e173-266">x & y & z</span></span>         | <span data-ttu-id="2e173-267">Logické a</span><span class="sxs-lookup"><span data-stu-id="2e173-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="2e173-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="2e173-268">x == y == z</span></span>       | <span data-ttu-id="2e173-269">Rovnost</span><span class="sxs-lookup"><span data-stu-id="2e173-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="2e173-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="2e173-270">x != y != z</span></span>       | <span data-ttu-id="2e173-271">Různé</span><span class="sxs-lookup"><span data-stu-id="2e173-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="2e173-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="2e173-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="2e173-273">Je menší než</span><span class="sxs-lookup"><span data-stu-id="2e173-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="2e173-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="2e173-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="2e173-275">Je větší než</span><span class="sxs-lookup"><span data-stu-id="2e173-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="2e173-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="2e173-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="2e173-277">Menší než nebo rovno</span><span class="sxs-lookup"><span data-stu-id="2e173-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="2e173-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="2e173-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="2e173-279">Větší než nebo rovno</span><span class="sxs-lookup"><span data-stu-id="2e173-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="2e173-280">(x)</span><span class="sxs-lookup"><span data-stu-id="2e173-280">(x)</span></span>               | <span data-ttu-id="2e173-281">Závorky ruší výchozí priority.</span><span class="sxs-lookup"><span data-stu-id="2e173-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="2e173-282">Proč nejsou má omezení výrazu vyhodnocena správně?</span><span class="sxs-lookup"><span data-stu-id="2e173-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="2e173-283">Rezervovaná slovo nelze použít jako řešitelské názvy atributů, komponentů nebo dílčích komponentů v modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="2e173-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="2e173-284">Následující seznam obsahuje rezervovaná klíčová slova, která nelze použít:</span><span class="sxs-lookup"><span data-stu-id="2e173-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="2e173-285">Horní mez</span><span class="sxs-lookup"><span data-stu-id="2e173-285">Ceiling</span></span>
-   <span data-ttu-id="2e173-286">Prvek</span><span class="sxs-lookup"><span data-stu-id="2e173-286">Element</span></span>
-   <span data-ttu-id="2e173-287">Rovno</span><span class="sxs-lookup"><span data-stu-id="2e173-287">Equal</span></span>
-   <span data-ttu-id="2e173-288">Podlaží</span><span class="sxs-lookup"><span data-stu-id="2e173-288">Floor</span></span>
-   <span data-ttu-id="2e173-289">Jestliže</span><span class="sxs-lookup"><span data-stu-id="2e173-289">If</span></span>
-   <span data-ttu-id="2e173-290">Menší</span><span class="sxs-lookup"><span data-stu-id="2e173-290">Less</span></span>
-   <span data-ttu-id="2e173-291">Větší</span><span class="sxs-lookup"><span data-stu-id="2e173-291">Greater</span></span>
-   <span data-ttu-id="2e173-292">Implikace</span><span class="sxs-lookup"><span data-stu-id="2e173-292">Implies</span></span>
-   <span data-ttu-id="2e173-293">Protokol</span><span class="sxs-lookup"><span data-stu-id="2e173-293">Log</span></span>
-   <span data-ttu-id="2e173-294">Maximum</span><span class="sxs-lookup"><span data-stu-id="2e173-294">Max</span></span>
-   <span data-ttu-id="2e173-295">Minimum</span><span class="sxs-lookup"><span data-stu-id="2e173-295">Min</span></span>
-   <span data-ttu-id="2e173-296">Záporný</span><span class="sxs-lookup"><span data-stu-id="2e173-296">Minus</span></span>
-   <span data-ttu-id="2e173-297">Kladný</span><span class="sxs-lookup"><span data-stu-id="2e173-297">Plus</span></span>
-   <span data-ttu-id="2e173-298">Výkon</span><span class="sxs-lookup"><span data-stu-id="2e173-298">Power</span></span>
-   <span data-ttu-id="2e173-299">Časy</span><span class="sxs-lookup"><span data-stu-id="2e173-299">Times</span></span>
-   <span data-ttu-id="2e173-300">Úsek</span><span class="sxs-lookup"><span data-stu-id="2e173-300">Slot</span></span>
-   <span data-ttu-id="2e173-301">Model</span><span class="sxs-lookup"><span data-stu-id="2e173-301">Model</span></span>
-   <span data-ttu-id="2e173-302">Rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="2e173-302">Decision</span></span>
-   <span data-ttu-id="2e173-303">Cíl</span><span class="sxs-lookup"><span data-stu-id="2e173-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="2e173-304">Viz také</span><span class="sxs-lookup"><span data-stu-id="2e173-304">See also</span></span>
--------

<span data-ttu-id="2e173-305">[Vytvoření omezení výrazu (Průvodce záznamem úloh)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span><span class="sxs-lookup"><span data-stu-id="2e173-305">[Create an expression constraint (Task guide)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span></span>

[<span data-ttu-id="2e173-306">Přidání výpočtu do modelu konfigurace produktu (Průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="2e173-306">Add a calculation to a product configuration model (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/add-calculation-product-configuration-model)




