---
title: Funkce ER STARTSWITH
description: Toto téma obsahuje obecné informace o použití funkce STARTSWITH elektronického výkaznictví (ER).
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048835"
---
# <a name="startswith-er-function"></a><span data-ttu-id="fef72-103">Funkce ER STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="fef72-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fef72-104">Funkce `STARTSWITH` určuje, zda zadaný vstup začíná zadaným textem.</span><span class="sxs-lookup"><span data-stu-id="fef72-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="fef72-105">Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup začíná zadaným textem.</span><span class="sxs-lookup"><span data-stu-id="fef72-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="fef72-106">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fef72-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef72-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fef72-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="fef72-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="fef72-108">Arguments</span></span>

<span data-ttu-id="fef72-109">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fef72-109">`input`: *String*</span></span>

<span data-ttu-id="fef72-110">Platná cesta k položce zdroje dat z typu *Řetězec* nebo řetězcová konstanta, jejíž hodnota může začínat druhým argumentem.</span><span class="sxs-lookup"><span data-stu-id="fef72-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="fef72-111">`start text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fef72-111">`start text`: *String*</span></span>

<span data-ttu-id="fef72-112">Platná cesta k zdroje dat z typu dat *Řetězec* nebo řetězcová konstanta, jejíž hodnota může být na začátku prvního argumentu.</span><span class="sxs-lookup"><span data-stu-id="fef72-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="fef72-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="fef72-113">Return values</span></span>

<span data-ttu-id="fef72-114">*Logická*</span><span class="sxs-lookup"><span data-stu-id="fef72-114">*Boolean*</span></span>

<span data-ttu-id="fef72-115">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="fef72-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fef72-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="fef72-116">Usage notes</span></span>

<span data-ttu-id="fef72-117">Tuto funkci lze použít k určení podmínkového výrazu funkce [FILTER](er-functions-list-filter.md) pouze v případě, že je příslušné mapování nakonfigurováno v [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) pro přístup k [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="fef72-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="fef72-118">Jinak je v době návrhu vyvolána výjimka.</span><span class="sxs-lookup"><span data-stu-id="fef72-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="fef72-119">Zpráva, kterou obdržíte, doporučuje použít funkci [WHERE](er-functions-list-where.md) namísto funkce `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="fef72-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="fef72-120">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="fef72-120">Example 1</span></span>

<span data-ttu-id="fef72-121">Výraz `STARTSWITH ("abc", "d")` vrací **FALSE**, zatímco výraz `STARTSWITH ("abc", "A")` vrací **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="fef72-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fef72-122">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="fef72-122">Example 2</span></span>

<span data-ttu-id="fef72-123">Výraz `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` vrací **TRUE** pokud hodnota pole **Address** zdroje **modelových** dat začíná řetězcem **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="fef72-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="fef72-124">V opačném případě vrátí hodnotu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fef72-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fef72-125">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="fef72-125">Additional resources</span></span>

[<span data-ttu-id="fef72-126">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="fef72-126">Logical functions</span></span>](er-functions-category-logical.md)
