---
title: Funkce elektronického výkaznictví STRINGJOIN
description: Toto téma obsahuje obecné informace o použití funkce STRINGJOIN elektronického výkaznictví.
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917182"
---
# <span data-ttu-id="9f1c0-103"><a name="STRINGJOIN">Funkce elektronického výkaznictví STRINGJOIN</a></span><span class="sxs-lookup"><span data-stu-id="9f1c0-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f1c0-104">Funkce `STRINGJOIN` vrátí hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="9f1c0-105">Hodnoty mohou být odděleny určeným oddělovačem.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f1c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f1c0-106">Syntax</span></span>

```
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="9f1c0-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9f1c0-107">Arguments</span></span>

<span data-ttu-id="9f1c0-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="9f1c0-108">`list`: *Record list*</span></span>

<span data-ttu-id="9f1c0-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9f1c0-110">`field`: *pole*</span><span class="sxs-lookup"><span data-stu-id="9f1c0-110">`field`: *Field*</span></span>

<span data-ttu-id="9f1c0-111">Platná cesta k poli datového typu *řetězec* v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="9f1c0-112">`delimiter`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9f1c0-112">`delimiter`: *String*</span></span>

<span data-ttu-id="9f1c0-113">Oddělovač k oddělení dílčích řetězců.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="9f1c0-114">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9f1c0-114">Return values</span></span>

<span data-ttu-id="9f1c0-115">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="9f1c0-115">*String*</span></span>

<span data-ttu-id="9f1c0-116">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9f1c0-117">Příklad</span><span class="sxs-lookup"><span data-stu-id="9f1c0-117">Example</span></span>

<span data-ttu-id="9f1c0-118">Když zadáte `SPLIT("abc" , 1)` jako zdroj dat **DS**, výraz `STRINGJOIN (DS, DS.Value, "-")` vrátí **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="9f1c0-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f1c0-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9f1c0-119">Additional resources</span></span>

[<span data-ttu-id="9f1c0-120">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="9f1c0-120">List functions</span></span>](er-functions-category-list.md)
