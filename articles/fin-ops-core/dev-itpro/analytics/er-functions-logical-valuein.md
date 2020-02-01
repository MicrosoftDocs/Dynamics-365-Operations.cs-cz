---
title: Funkce el. výkaznictví VALUEIN
description: Toto téma obsahuje obecné informace o použití funkce VALUEIN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915963"
---
# <span data-ttu-id="b9fed-103"><a name="VALUEIN">Funkce el. výkaznictví VALUEIN</a></span><span class="sxs-lookup"><span data-stu-id="b9fed-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9fed-104">Funkce `VALUEIN` určuje, zda zadaný vstup odpovídá některé hodnotě zadané položky v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="b9fed-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="b9fed-105">Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="b9fed-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="b9fed-106">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9fed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9fed-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="b9fed-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b9fed-108">Arguments</span></span>

<span data-ttu-id="b9fed-109">`input`: *pole*</span><span class="sxs-lookup"><span data-stu-id="b9fed-109">`input`: *Field*</span></span>

<span data-ttu-id="b9fed-110">Platná cesta k položce zdroje dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="b9fed-111">Hodnota této položky bude spárována.</span><span class="sxs-lookup"><span data-stu-id="b9fed-111">The value of this item will be matched.</span></span>

<span data-ttu-id="b9fed-112">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="b9fed-112">`list`: *Record list*</span></span>

<span data-ttu-id="b9fed-113">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b9fed-114">`list item expression`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="b9fed-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="b9fed-115">Platný podmíněný výraz, který buď odkazuje na nebo obsahuje jedno pole určeného seznamu, který by měl být použit pro párování.</span><span class="sxs-lookup"><span data-stu-id="b9fed-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="b9fed-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b9fed-116">Return values</span></span>

<span data-ttu-id="b9fed-117">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="b9fed-117">*Boolean*</span></span>

<span data-ttu-id="b9fed-118">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b9fed-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="b9fed-119">Usage notes</span></span>

<span data-ttu-id="b9fed-120">Obecně platí, že funkce `VALUEIN` je převedena do sady podmínek **OR**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="b9fed-121">V některých případech ji lze převést do databázového příkazu SQL pomocí operátoru `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="b9fed-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="b9fed-122">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="b9fed-122">Example 1</span></span>

<span data-ttu-id="b9fed-123">V mapování modelu definujete zdroj dat datové typu **seznam** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b9fed-124">Tento zdroj dat obsahuje výraz `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="b9fed-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="b9fed-125">Když je zdroj dat volán, pokud byl nakonfigurován jako výraz `VALUEIN ("B", List, List.Value)`, vrátí hodnotu **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="b9fed-126">V tomto případě je funkce `VALUEIN` převedena do následující sady podmínek: `(("B" = "a") or ("B" = "b") or ("B" = "c"))` kde `("B" = "b")` rovná se **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="b9fed-127">Když je zdroj dat volán, pokud byl nakonfigurován jako výraz `VALUEIN ("B", List, LEFT(List.Value, 0))`, vrátí hodnotu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="b9fed-128">V tomto případě je funkce `VALUEIN` převedena na následující podmínku: `("B" = "")`, které se nerovná **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="b9fed-129">Maximální počet znaků v textu takové podmínky je 32 768 znaků.</span><span class="sxs-lookup"><span data-stu-id="b9fed-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="b9fed-130">Proto byste neměli vytvářet zdroje dat, které mohou překročit tento limit za běhu.</span><span class="sxs-lookup"><span data-stu-id="b9fed-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="b9fed-131">Při přesažení limitu se aplikace zastaví a je vyvolána výjimka.</span><span class="sxs-lookup"><span data-stu-id="b9fed-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="b9fed-132">Například k této situaci může dojít, pokud je datový zdroj nakonfigurován jako `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, a seznamy **List1** a **List2** obsahují velké množství záznamů.</span><span class="sxs-lookup"><span data-stu-id="b9fed-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="b9fed-133">V některých případech je funkce `VALUEIN` přeložena do výkazu databázi pomocí operátoru `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="b9fed-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="b9fed-134">K tomuto chování dochází, když se používá funkce [FILTER](er-functions-list-filter.md) a jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b9fed-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="b9fed-135">Možnost **ASK FOR QUERY** je vypnuta pro datový zdroj funkce `VALUEIN`, která se odkazuje na seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="b9fed-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="b9fed-136">Žádné další podmínky nebudou použity na tento zdroj dat za běhu.</span><span class="sxs-lookup"><span data-stu-id="b9fed-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="b9fed-137">Žádné vnořené výrazy nejsou nakonfigurovány pro datový zdroj funkce `VALUEIN`, která se odkazuje na seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="b9fed-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="b9fed-138">Položka seznamu funkce `VALUEIN` odkazuje na pole zadaného zdroje dat, nikoliv na výraz nebo metodu tohoto zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="b9fed-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="b9fed-139">Zvažte použití této možnosti místo funkce [WHERE](er-functions-list-where.md), jak je popsáno výše v tomto příkladu.</span><span class="sxs-lookup"><span data-stu-id="b9fed-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="b9fed-140">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="b9fed-140">Example 2</span></span>

<span data-ttu-id="b9fed-141">Definujte v mapování modelu následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="b9fed-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="b9fed-142">Zdroj dat **In** typu *záznamy tabulky*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="b9fed-143">Tento zdroj dat odkazuje na tabulku Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b9fed-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="b9fed-144">Zdroj dat **Port** typu *záznamy tabulky*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="b9fed-145">Tento zdroj dat odkazuje na tabulku IntrastatPort.</span><span class="sxs-lookup"><span data-stu-id="b9fed-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="b9fed-146">Pokud je volán zdroj dat nakonfigurovaný jako výraz `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, je vygenerován následující příkaz SQL pro navrácení vyfiltrovaných záznamů tabulky Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b9fed-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="b9fed-147">Pro pole **dataAreaId** je konečný příkaz SQL vygenerován pomocí operátoru `IN`.</span><span class="sxs-lookup"><span data-stu-id="b9fed-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="b9fed-148">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="b9fed-148">Example 3</span></span>

<span data-ttu-id="b9fed-149">Definujte v mapování modelu následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="b9fed-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="b9fed-150">Zdroj dat **Le** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b9fed-151">Tento zdroj dat obsahuje výraz `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="b9fed-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="b9fed-152">Zdroj dat **In** typu *záznamy tabulky*.</span><span class="sxs-lookup"><span data-stu-id="b9fed-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="b9fed-153">Tento zdroj dat odkazuje na tabulku Intrastat a je pro ni zapnuta možnost **Cross-company**.</span><span class="sxs-lookup"><span data-stu-id="b9fed-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="b9fed-154">Pokud je volán zdroj dat nakonfigurovaný jako výraz `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, obsahuje konečný příkaz SQL následující podmínku.</span><span class="sxs-lookup"><span data-stu-id="b9fed-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="b9fed-155">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b9fed-155">Additional resources</span></span>

[<span data-ttu-id="b9fed-156">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="b9fed-156">Logical functions</span></span>](er-functions-category-logical.md)