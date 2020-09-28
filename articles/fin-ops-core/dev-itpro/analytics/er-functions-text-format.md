---
title: Funkce el. výkaznictví FORMAT
description: Toto téma obsahuje obecné informace o použití funkce FORMAT elektronického výkaznictví.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f3e8e5f6676c26b8d604ed950470463f04c0473
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743872"
---
# <a name="format-er-function"></a><span data-ttu-id="02219-103">Funkce el. výkaznictví FORMAT</span><span class="sxs-lookup"><span data-stu-id="02219-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02219-104">Funkce `FORMAT` vrátí zadaný řetězec jako hodnotu typu *řetězec* po jeho zformátování nahrazením všech výskytů **%N** *n*-tým argumentem.</span><span class="sxs-lookup"><span data-stu-id="02219-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="02219-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02219-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="02219-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="02219-106">Arguments</span></span>

<span data-ttu-id="02219-107">`string`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="02219-107">`string`: *String*</span></span>

<span data-ttu-id="02219-108">Odkaz na zdroj dat typu *řetězec*, který má být formátován.</span><span class="sxs-lookup"><span data-stu-id="02219-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="02219-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="02219-109">This argument is required.</span></span>

<span data-ttu-id="02219-110">`argument 1`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="02219-110">`argument 1`: *String*</span></span>

<span data-ttu-id="02219-111">První argument, který se použije k nahrazení výskytů **%1**.</span><span class="sxs-lookup"><span data-stu-id="02219-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="02219-112">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="02219-112">This argument is required.</span></span>

<span data-ttu-id="02219-113">`argument N`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="02219-113">`argument N`: *String*</span></span>

<span data-ttu-id="02219-114">*N*-tý argument, který se použije k nahrazení výskytů **%2**, **%3** atd.</span><span class="sxs-lookup"><span data-stu-id="02219-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="02219-115">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="02219-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="02219-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="02219-116">Return values</span></span>

<span data-ttu-id="02219-117">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="02219-117">*String*</span></span>

<span data-ttu-id="02219-118">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="02219-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="02219-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="02219-119">Usage notes</span></span>

<span data-ttu-id="02219-120">Pokud pro parametr není zadán argument, parametr je vrácen jako **"%N"** v řetězci.</span><span class="sxs-lookup"><span data-stu-id="02219-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="02219-121">Co se týká hodnot typu *reálné číslo*, výchozí převod řetězce je omezen na dvě desetinná místa.</span><span class="sxs-lookup"><span data-stu-id="02219-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="02219-122">Příklad</span><span class="sxs-lookup"><span data-stu-id="02219-122">Example</span></span>

<span data-ttu-id="02219-123">Na následujícím obrázku vrátí zdroj dat **PaymentModel** (platební model) seznam záznamů zákazníků pomocí součásti **Customer** (odběratel).</span><span class="sxs-lookup"><span data-stu-id="02219-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="02219-124">Vrátí hodnotu data zpracování pomocí pole **ProcessingDate** (datum zpracování).</span><span class="sxs-lookup"><span data-stu-id="02219-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="02219-125">Ve formátu elektronického výkaznictví, který je určený ke generování elektronického souboru pro vybrané odběratele, je vybrán řetězec **PaymentModel** jako zdroj dat, který řídí tok procesu.</span><span class="sxs-lookup"><span data-stu-id="02219-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="02219-126">Jestliže je vybraný odběratel zastaven k datu zpracování sestavy, je vyvolána výjimka pro informování uživatele.</span><span class="sxs-lookup"><span data-stu-id="02219-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="02219-127">Vzorec, který je určen pro tento typ ovládacího prvku pro zpracování, může využít následující zdroje:</span><span class="sxs-lookup"><span data-stu-id="02219-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="02219-128">Popisek SYS70894, který má následující text:</span><span class="sxs-lookup"><span data-stu-id="02219-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="02219-129">**U jazyka EN-US:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="02219-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="02219-130">**U jazyka DE:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="02219-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="02219-131">Popisek SYS18389, který má následující text:</span><span class="sxs-lookup"><span data-stu-id="02219-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="02219-132">**U jazyka EN-US**: "Customer %1 is stopped for %2."</span><span class="sxs-lookup"><span data-stu-id="02219-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="02219-133">**U jazyka DE**: "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="02219-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="02219-134">Zde je výraz, který lze vytvořit.</span><span class="sxs-lookup"><span data-stu-id="02219-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="02219-135">Pokud je sestava zpracovávána pro odběratele **Litware Retail** 17. prosince 2015, v národním prostředí **EN-US** a jazyce **EN-US**, tento vzorec vrátí následující text, který může být uživateli nabídnut ve formě zprávy výjimky:</span><span class="sxs-lookup"><span data-stu-id="02219-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="02219-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span><span class="sxs-lookup"><span data-stu-id="02219-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="02219-137">Jestliže je stejná sestava zpracována pro odběratele **Litware Retail** 17. prosince 2015 v jazykové verzi **DE** a jazyce **DE**, vzorec vrátí následující text, který používá jiný formát data:</span><span class="sxs-lookup"><span data-stu-id="02219-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="02219-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="02219-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="02219-139">Následující syntaxe je použita ve vzorcích elektronického výkaznictví pro popisky:</span><span class="sxs-lookup"><span data-stu-id="02219-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="02219-140">**Popisky ze zdrojů aplikace Microsoft Dynamics 365 Finance:** **\@X**, kde **X** je ID popisku ve stromu aplikačních objektů (AOT)</span><span class="sxs-lookup"><span data-stu-id="02219-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="02219-141">**Popisky, které se nachází v konfiguracích elektronického výkaznictví:** **@"GER_LABEL:X"**, kde **X** je ID popisku v konfiguraci elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="02219-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02219-142">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="02219-142">Additional resources</span></span>

[<span data-ttu-id="02219-143">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="02219-143">Text functions</span></span>](er-functions-category-text.md)
