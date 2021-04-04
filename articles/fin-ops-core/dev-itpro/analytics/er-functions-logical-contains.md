---
title: Funkce ER CONTAINS
description: Toto téma obsahuje obecné informace o použití funkce CONTAINS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557503"
---
# <a name="contains-er-function"></a><span data-ttu-id="3074c-103">Funkce ER CONTAINS</span><span class="sxs-lookup"><span data-stu-id="3074c-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3074c-104">Funkce `CONTAINS` určuje, zda zadaný vstup obsahuje zadaný text.</span><span class="sxs-lookup"><span data-stu-id="3074c-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="3074c-105">Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup obsahuje zadaný text.</span><span class="sxs-lookup"><span data-stu-id="3074c-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="3074c-106">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3074c-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3074c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3074c-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="3074c-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="3074c-108">Arguments</span></span>

<span data-ttu-id="3074c-109">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3074c-109">`input`: *String*</span></span>

<span data-ttu-id="3074c-110">Platná cesta k položce zdroje dat z typu *Řetězec* nebo řetězcová konstanta, jejíž hodnota může obsahovat druhý argument.</span><span class="sxs-lookup"><span data-stu-id="3074c-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="3074c-111">`search text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3074c-111">`search text`: *String*</span></span>

<span data-ttu-id="3074c-112">Platná cesta k zdroje dat z typu dat *Řetězec* nebo řetězcová konstanta, jejíž hodnota může být obsažena v prvním argumentu.</span><span class="sxs-lookup"><span data-stu-id="3074c-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="3074c-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="3074c-113">Return values</span></span>

<span data-ttu-id="3074c-114">*Logická*</span><span class="sxs-lookup"><span data-stu-id="3074c-114">*Boolean*</span></span>

<span data-ttu-id="3074c-115">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="3074c-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3074c-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="3074c-116">Usage notes</span></span>

<span data-ttu-id="3074c-117">Tuto funkci lze použít k určení podmínkového výrazu funkce [FILTER](er-functions-list-filter.md) pouze v případě, že je příslušné mapování nakonfigurováno v [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) pro přístup k [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="3074c-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="3074c-118">Jinak je v době návrhu vyvolána výjimka.</span><span class="sxs-lookup"><span data-stu-id="3074c-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="3074c-119">Zpráva, kterou obdržíte, doporučuje použít funkci [WHERE](er-functions-list-where.md) namísto funkce `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="3074c-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="3074c-120">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="3074c-120">Example 1</span></span>

<span data-ttu-id="3074c-121">Výraz `CONTAINS ("abc", "d")` vrací **FALSE**, zatímco výraz `CONTAINS ("abc", "C")` vrací **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="3074c-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3074c-122">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="3074c-122">Example 2</span></span>

<span data-ttu-id="3074c-123">Výraz `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` vrací **TRUE** pokud hodnota pole **Address** zdroje **modelových** dat obsahuje řetězec **DEU**.</span><span class="sxs-lookup"><span data-stu-id="3074c-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="3074c-124">V opačném případě vrátí hodnotu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3074c-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3074c-125">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3074c-125">Additional resources</span></span>

[<span data-ttu-id="3074c-126">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="3074c-126">Logical functions</span></span>](er-functions-category-logical.md)
