---
title: Funkce elektronického výkaznictví LISTOFFIELDS
description: Toto téma obsahuje obecné informace o použití funkce LISTOFFIELDS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8d9f41d6ee5256f560c83486c95ecd47f5b081
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686505"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="e9db7-103">Funkce elektronického výkaznictví LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="e9db7-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9db7-104">Funkce `LISTOFFIELDS` vrátí hodnotu typu *seznam záznamů*, která je vytvořena na základě struktury zadaného argumentu typu *výčet* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="e9db7-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e9db7-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="e9db7-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="e9db7-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="e9db7-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="e9db7-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e9db7-107">Arguments</span></span>

<span data-ttu-id="e9db7-108">`path`: odkaz na zdroj dat</span><span class="sxs-lookup"><span data-stu-id="e9db7-108">`path`: Data source reference</span></span>

<span data-ttu-id="e9db7-109">Platná cesta odkazu na zdroj dat jednoho z následujících datových typů:</span><span class="sxs-lookup"><span data-stu-id="e9db7-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="e9db7-110">Výčet modelu</span><span class="sxs-lookup"><span data-stu-id="e9db7-110">Model enumeration</span></span>
- <span data-ttu-id="e9db7-111">Výčet formátu</span><span class="sxs-lookup"><span data-stu-id="e9db7-111">Format enumeration</span></span>
- <span data-ttu-id="e9db7-112">Výčet aplikací</span><span class="sxs-lookup"><span data-stu-id="e9db7-112">Application enumeration</span></span>
- <span data-ttu-id="e9db7-113">Kontejner (záznam)</span><span class="sxs-lookup"><span data-stu-id="e9db7-113">Container (record)</span></span>

<span data-ttu-id="e9db7-114">`language`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e9db7-114">`language`: *String*</span></span>

<span data-ttu-id="e9db7-115">Text, který představuje kód jazyka.</span><span class="sxs-lookup"><span data-stu-id="e9db7-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9db7-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e9db7-116">Return values</span></span>

<span data-ttu-id="e9db7-117">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="e9db7-117">*Record list*</span></span>

<span data-ttu-id="e9db7-118">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="e9db7-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e9db7-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="e9db7-119">Usage notes</span></span>

<span data-ttu-id="e9db7-120">Vytvořený seznam obsahuje záznamy, které mají následující pole:</span><span class="sxs-lookup"><span data-stu-id="e9db7-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="e9db7-121">**Name** (datový typ *řetezec*)</span><span class="sxs-lookup"><span data-stu-id="e9db7-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="e9db7-122">**Label** (datový typ *řetezec*)</span><span class="sxs-lookup"><span data-stu-id="e9db7-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="e9db7-123">**Description** (datový typ *řetezec*)</span><span class="sxs-lookup"><span data-stu-id="e9db7-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="e9db7-124">**IsTranslated** (*logický* datový typ)</span><span class="sxs-lookup"><span data-stu-id="e9db7-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="e9db7-125">Pokud argument `path` odkazuje na zdroj dat typu *kontejner (záznam)*, pro každé pole odkazovaného záznamu kontejneru je do vytvořeného seznamu přidán nový záznam.</span><span class="sxs-lookup"><span data-stu-id="e9db7-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="e9db7-126">Pro každý vytvořený záznam vrátí pole **Name** název pole odkazovaného záznamu kontejneru, pro který byl aktuální záznam vytvořen.</span><span class="sxs-lookup"><span data-stu-id="e9db7-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="e9db7-127">Pokud argument `path` odkazuje na zdroj dat jednoho z typů *výčet*, pro každou hodnotu výčtu odkazovaného výčtu je do vytvořeného seznamu přidán nový záznam.</span><span class="sxs-lookup"><span data-stu-id="e9db7-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="e9db7-128">Pro každý vytvořený záznam vrátí pole **Name** hodnotu odkazovaného výčtu, pro který byl vytvořen aktuální záznam, pole **Description** vrátí popis tohoto výčtu a pole **Label** vrátí popisek tohoto výčtu.</span><span class="sxs-lookup"><span data-stu-id="e9db7-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="e9db7-129">V době běhu je při použití syntaxe 1 nutné, aby pole **Label** a **Description** vrátila hodnoty, které jsou založeny na jazykovém nastavení formátu spuštěného elektronického vykazování (ER):</span><span class="sxs-lookup"><span data-stu-id="e9db7-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="e9db7-130">Jsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na daném jazyku, a pole **IsTranslated** vrátí hodnotu **True**.</span><span class="sxs-lookup"><span data-stu-id="e9db7-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="e9db7-131">Nejsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na výchozím jazyku **EN-US**, a pole **IsTranslated** vrátí hodnotu **False**.</span><span class="sxs-lookup"><span data-stu-id="e9db7-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="e9db7-132">V době běhu je při použití syntaxe 2 nutné, aby pole **Label** a **Description** vrátila hodnoty, které jsou založeny na jazyku, který je definován jako druhý argument volané funkce:</span><span class="sxs-lookup"><span data-stu-id="e9db7-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="e9db7-133">Jsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na daném jazyku, a pole **IsTranslated** vrátí hodnotu **True**.</span><span class="sxs-lookup"><span data-stu-id="e9db7-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="e9db7-134">Nejsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na jazyku **EN-US**, a pole **IsTranslated** vrátí hodnotu **False**.</span><span class="sxs-lookup"><span data-stu-id="e9db7-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="e9db7-135">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="e9db7-135">Example 1</span></span>

<span data-ttu-id="e9db7-136">Na následujícím obrázku je výčet uveden v datovém modelu elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="e9db7-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="e9db7-137">Následující obrázek znázorňuje tyto podrobnosti:</span><span class="sxs-lookup"><span data-stu-id="e9db7-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="e9db7-138">Výčet modelů je vložen do sestavy jako zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="e9db7-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="e9db7-139">Výraz elektronického výkaznictví používá výčet modelů jako parametr funkce `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="e9db7-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="e9db7-140">Zdroj dat typu *seznamu záznamů* je vložen do sestavy pomocí vytvořeného výrazu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="e9db7-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="e9db7-141">Následující příklad uvádí prvky formátu ER, které jsou vázané na zdroj dat typu *seznamu záznamů*, který byl vytvořen pomocí funkce `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="e9db7-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="e9db7-142">Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</span><span class="sxs-lookup"><span data-stu-id="e9db7-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="e9db7-143">Přeložený text popisků a popisů je zadáván do výstupu formátu elektronického výkaznictví na základě nastavení jazyka nadřazených prvků formátu **FILE** a **FOLDER**.</span><span class="sxs-lookup"><span data-stu-id="e9db7-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="e9db7-144">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="e9db7-144">Example 2</span></span>

<span data-ttu-id="e9db7-145">Typ datového zdroje *Vypočítané pole* použijete ke konfiguraci zdrojů dat **enumType\_de** a **enumType\_deCH** pro výčet datových modelů **enumType**:</span><span class="sxs-lookup"><span data-stu-id="e9db7-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="e9db7-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="e9db7-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="e9db7-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="e9db7-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="e9db7-148">V takovém případě můžete použít následující výraz k získání popisku hodnoty výčtu ve švýcarské němčině, pokud je tento překlad k dispozici.</span><span class="sxs-lookup"><span data-stu-id="e9db7-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="e9db7-149">Není-li k dispozici překlad do švýcarské němčiny, je popisek v němčině.</span><span class="sxs-lookup"><span data-stu-id="e9db7-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="e9db7-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e9db7-150">Additional resources</span></span>

[<span data-ttu-id="e9db7-151">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="e9db7-151">List functions</span></span>](er-functions-category-list.md)
