---
title: Funkce elektronického výkaznictví LISTJOIN
description: Toto téma obsahuje obecné informace o použití funkce LISTJOIN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249028"
---
# <a name=""></a><span data-ttu-id="8563a-103"><a name="LISTJOIN">Funkce elektronického výkaznictví LISTJOIN</a></span><span class="sxs-lookup"><span data-stu-id="8563a-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8563a-104">Funkce `LISTJOIN` vrací hodnotu typu *seznam záznamů*, která představuje nový spojený seznam záznamů vytvořený ze zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="8563a-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="8563a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8563a-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="8563a-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="8563a-106">Arguments</span></span>

<span data-ttu-id="8563a-107">`list 1`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="8563a-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="8563a-108">Odkaz na zdroj dat datového typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="8563a-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="8563a-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="8563a-109">This argument is mandatory.</span></span>

<span data-ttu-id="8563a-110">`list N`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="8563a-110">`list N`: *Record list*</span></span>

<span data-ttu-id="8563a-111">Odkaz na zdroj dat datového typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="8563a-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="8563a-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="8563a-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8563a-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="8563a-113">Return values</span></span>

<span data-ttu-id="8563a-114">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="8563a-114">*Record list*</span></span>

<span data-ttu-id="8563a-115">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="8563a-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8563a-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="8563a-116">Usage notes</span></span>

<span data-ttu-id="8563a-117">Struktura vytvořeného seznamu obsahuje pouze pole, která jsou přítomna ve struktuře každého seznamu záznamů, který na který je odkazováno v argumentech.</span><span class="sxs-lookup"><span data-stu-id="8563a-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="8563a-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="8563a-118">Example</span></span>

<span data-ttu-id="8563a-119">Zadáte zdroj dat **Záznam 1** typu `Container`.</span><span class="sxs-lookup"><span data-stu-id="8563a-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="8563a-120">Tento zdroj dat obsahuje následující vnořená pole typu `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="8563a-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="8563a-121">**Kód**: Toto pole obsahuje výraz, který vrací hodnotu typu `String`.</span><span class="sxs-lookup"><span data-stu-id="8563a-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="8563a-122">**Množství**: Toto pole obsahuje výraz, který vrací hodnotu typu `Real`.</span><span class="sxs-lookup"><span data-stu-id="8563a-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="8563a-123">Zadáte pak zdroj dat **Záznam 2** typu `Container`.</span><span class="sxs-lookup"><span data-stu-id="8563a-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="8563a-124">Tento zdroj dat obsahuje následující vnořená pole typu `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="8563a-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="8563a-125">**Množství**: Toto pole obsahuje výraz, který vrací hodnotu typu `Real`.</span><span class="sxs-lookup"><span data-stu-id="8563a-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="8563a-126">**IsValid**: Toto pole obsahuje výraz, který vrací hodnotu typu `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="8563a-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="8563a-127">V tomto případě výraz `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` vrátí nový seznam, který obsahuje dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="8563a-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="8563a-128">Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu `Real`, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.</span><span class="sxs-lookup"><span data-stu-id="8563a-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8563a-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8563a-129">Additional resources</span></span>

[<span data-ttu-id="8563a-130">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="8563a-130">List functions</span></span>](er-functions-category-list.md)
