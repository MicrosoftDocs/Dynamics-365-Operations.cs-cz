---
title: Funkce VALUEINLARGE elektronického výkaznictví
description: Toto téma obsahuje obecné informace o použití funkce VALUEINLARGE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705136"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="e2199-103">Funkce VALUEINLARGE elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="e2199-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2199-104">Funkce `VALUEINLARGE` určuje, zda uvedený vstup typu *Int64* nebo *Integer* odpovídá jakékoli hodnotě zadané položky v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="e2199-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="e2199-105">Tato funkce vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="e2199-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="e2199-106">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e2199-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="e2199-107">Abyste pochopili rozdíl oproti funkci `VALUEIN`, viz sekce [Poznámka k použití](#usage_note) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="e2199-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2199-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2199-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="e2199-109">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e2199-109">Arguments</span></span>

<span data-ttu-id="e2199-110">`input`: *pole*</span><span class="sxs-lookup"><span data-stu-id="e2199-110">`input`: *Field*</span></span>

<span data-ttu-id="e2199-111">Platná cesta k položce zdroje dat typu *Seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="e2199-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="e2199-112">Hodnota této položky bude spárována.</span><span class="sxs-lookup"><span data-stu-id="e2199-112">The value of this item will be matched.</span></span>

<span data-ttu-id="e2199-113">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="e2199-113">`list`: *Record list*</span></span>

<span data-ttu-id="e2199-114">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="e2199-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e2199-115">`list item expression`: *výraz*</span><span class="sxs-lookup"><span data-stu-id="e2199-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="e2199-116">Platný podmíněný výraz, který buď odkazuje na nebo obsahuje jedno pole určeného seznamu, který by měl být použit pro párování.</span><span class="sxs-lookup"><span data-stu-id="e2199-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2199-117">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e2199-117">Return values</span></span>

<span data-ttu-id="e2199-118">*Boolean*</span><span class="sxs-lookup"><span data-stu-id="e2199-118">*Boolean*</span></span>

<span data-ttu-id="e2199-119">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="e2199-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="e2199-120"><a name="usage_note">Poznámky k použití</a></span><span class="sxs-lookup"><span data-stu-id="e2199-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="e2199-121">Když zadaný vstup představuje typ *Int64* nebo *Integer* položky zdroje dat, jejíž volání lze přeložit na přímý příkaz SQL, zadaný seznam se převede na dočasnou tabulku SQL a párování se provede v databázi provedením jediného dotazu `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="e2199-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="e2199-122">Jinak tato funkce funguje jako funkce [`VALUEIN`](er-functions-logical-valuein.md).</span><span class="sxs-lookup"><span data-stu-id="e2199-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="e2199-123">Když zadaný vstup představuje položku zdroje dat, která je navržena jako položka jiného typu než *Int64* a *Integer*, dojde v době návrhu k chybě informující o tom, že funkce `VALUEINLARGE` není použitelná pro nakonfigurovaný výraz elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="e2199-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="e2199-124">Když je spušten výraz funkce `VALUEINLARGE` a v rámci tohoto spuštění je použita více než jedna dočasná tabulka, dojde k chybě běhu.</span><span class="sxs-lookup"><span data-stu-id="e2199-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="e2199-125">Příklad</span><span class="sxs-lookup"><span data-stu-id="e2199-125">Example</span></span>

<span data-ttu-id="e2199-126">Definujte v mapování modelu následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="e2199-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="e2199-127">Zdroj dat **In** typu *záznamy tabulky*.</span><span class="sxs-lookup"><span data-stu-id="e2199-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="e2199-128">Tento zdroj dat odkazuje na tabulku **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e2199-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="e2199-129">Možnost **Mezi společnostmi** je nastavena na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="e2199-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="e2199-130">Zdroj dat **InMemory** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="e2199-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="e2199-131">Tento zdroj dat obsahuje výraz `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="e2199-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="e2199-132">Zdroj dat **InFiltered** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="e2199-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="e2199-133">Tento zdroj dat obsahuje výraz `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="e2199-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="e2199-134">Když se zdroj dat **InFiltered** nazývá v kontextu společnosti **DEMF**, v databázi aplikace se vytvoří nová dočasná tabulka, do této tabulky se vloží seznam identifikačních kódů záznamů shromážděných v paměti a vygeneruje se následující příkaz SQL, který vrátí filtrované záznamy v tabulce **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e2199-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="e2199-135">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="e2199-135">Additional resources</span></span>

[<span data-ttu-id="e2199-136">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="e2199-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="e2199-137">Funkce VALUEIN</span><span class="sxs-lookup"><span data-stu-id="e2199-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
