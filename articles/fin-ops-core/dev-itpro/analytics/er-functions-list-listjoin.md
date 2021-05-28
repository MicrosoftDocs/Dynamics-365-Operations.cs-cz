---
title: Funkce elektronického výkaznictví LISTJOIN
description: Toto téma obsahuje obecné informace o použití funkce LISTJOIN elektronického výkaznictví.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b300cef0a508f7cc37397480738091158efdead
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027908"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="afcab-103">Funkce elektronického výkaznictví LISTJOIN</span><span class="sxs-lookup"><span data-stu-id="afcab-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afcab-104">Funkce `LISTJOIN` vrací hodnotu typu *seznam záznamů*, která představuje nový spojený seznam záznamů vytvořený ze zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="afcab-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="afcab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afcab-105">Syntax</span></span>

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="afcab-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="afcab-106">Arguments</span></span>

<span data-ttu-id="afcab-107">`list 1`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="afcab-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="afcab-108">Odkaz na zdroj dat datového typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="afcab-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="afcab-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="afcab-109">This argument is mandatory.</span></span>

<span data-ttu-id="afcab-110">`list N`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="afcab-110">`list N`: *Record list*</span></span>

<span data-ttu-id="afcab-111">Odkaz na zdroj dat datového typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="afcab-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="afcab-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="afcab-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="afcab-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="afcab-113">Return values</span></span>

<span data-ttu-id="afcab-114">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="afcab-114">*Record list*</span></span>

<span data-ttu-id="afcab-115">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="afcab-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="afcab-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="afcab-116">Usage notes</span></span>

<span data-ttu-id="afcab-117">Struktura vytvořeného seznamu obsahuje pouze pole, která jsou přítomna ve struktuře každého seznamu záznamů, který na který je odkazováno v argumentech.</span><span class="sxs-lookup"><span data-stu-id="afcab-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="afcab-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="afcab-118">Example</span></span>

<span data-ttu-id="afcab-119">Zadáte zdroj dat **Záznam 1** typu `Container`.</span><span class="sxs-lookup"><span data-stu-id="afcab-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="afcab-120">Tento zdroj dat obsahuje následující vnořená pole typu `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="afcab-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="afcab-121">**Kód**: Toto pole obsahuje výraz, který vrací hodnotu typu `String`.</span><span class="sxs-lookup"><span data-stu-id="afcab-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="afcab-122">**Množství**: Toto pole obsahuje výraz, který vrací hodnotu typu `Real`.</span><span class="sxs-lookup"><span data-stu-id="afcab-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="afcab-123">Zadáte pak zdroj dat **Záznam 2** typu `Container`.</span><span class="sxs-lookup"><span data-stu-id="afcab-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="afcab-124">Tento zdroj dat obsahuje následující vnořená pole typu `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="afcab-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="afcab-125">**Množství**: Toto pole obsahuje výraz, který vrací hodnotu typu `Real`.</span><span class="sxs-lookup"><span data-stu-id="afcab-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="afcab-126">**IsValid**: Toto pole obsahuje výraz, který vrací hodnotu typu `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="afcab-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![Stránka Návrhář mapování modelu ER](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="afcab-128">V tomto případě výraz `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` vrátí nový seznam, který obsahuje dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="afcab-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![Stránka návrháře mapování modelu elektronického výkaznictví se dvěma záznamy](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="afcab-130">Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu `Real`, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.</span><span class="sxs-lookup"><span data-stu-id="afcab-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![Pole částky na stránce návrháře mapování modelu elektronického výkaznictví](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="afcab-132">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="afcab-132">Additional resources</span></span>

[<span data-ttu-id="afcab-133">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="afcab-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="afcab-134">Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace</span><span class="sxs-lookup"><span data-stu-id="afcab-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
