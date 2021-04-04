---
title: Funkce ER ENDSWITH
description: Toto téma obsahuje obecné informace o použití funkce ENDSWITH elektronického výkaznictví (ER).
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
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557502"
---
# <a name="endswith-er-function"></a><span data-ttu-id="fadee-103">Funkce ER ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="fadee-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fadee-104">Funkce `ENDSWITH` určuje, zda zadaný vstup končí zadaným textem.</span><span class="sxs-lookup"><span data-stu-id="fadee-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="fadee-105">Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup končí zadaným textem.</span><span class="sxs-lookup"><span data-stu-id="fadee-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="fadee-106">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fadee-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fadee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fadee-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="fadee-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="fadee-108">Arguments</span></span>

<span data-ttu-id="fadee-109">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fadee-109">`input`: *String*</span></span>

<span data-ttu-id="fadee-110">Platná cesta k položce zdroje dat z typu *Řetězec* nebo řetězcová konstanta, jejíž hodnota může končit druhým argumentem.</span><span class="sxs-lookup"><span data-stu-id="fadee-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="fadee-111">`start text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fadee-111">`start text`: *String*</span></span>

<span data-ttu-id="fadee-112">Platná cesta k zdroje dat z typu dat *Řetězec* nebo řetězcová konstanta, jejíž hodnota může být na konci prvního argumentu.</span><span class="sxs-lookup"><span data-stu-id="fadee-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="fadee-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="fadee-113">Return values</span></span>

<span data-ttu-id="fadee-114">*Logická*</span><span class="sxs-lookup"><span data-stu-id="fadee-114">*Boolean*</span></span>

<span data-ttu-id="fadee-115">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="fadee-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fadee-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="fadee-116">Usage notes</span></span>

<span data-ttu-id="fadee-117">Tuto funkci lze použít k určení podmínkového výrazu funkce [FILTER](er-functions-list-filter.md) pouze v případě, že je příslušné mapování nakonfigurováno v [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) pro přístup k [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="fadee-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="fadee-118">Jinak je v době návrhu vyvolána výjimka.</span><span class="sxs-lookup"><span data-stu-id="fadee-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="fadee-119">Zpráva, kterou obdržíte, doporučuje použít funkci [WHERE](er-functions-list-where.md) namísto funkce `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="fadee-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="fadee-120">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="fadee-120">Example 1</span></span>

<span data-ttu-id="fadee-121">Výraz `ENDSWITH ("abc", "d")` vrací **FALSE**, zatímco výraz `ENDSWITH ("abc", "C")` vrací **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="fadee-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fadee-122">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="fadee-122">Example 2</span></span>

<span data-ttu-id="fadee-123">Výraz `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` vrací **TRUE** pokud hodnota pole **Address** zdroje **modelových** dat končí řetězcem **USA**.</span><span class="sxs-lookup"><span data-stu-id="fadee-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="fadee-124">V opačném případě vrátí hodnotu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fadee-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fadee-125">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="fadee-125">Additional resources</span></span>

[<span data-ttu-id="fadee-126">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="fadee-126">Logical functions</span></span>](er-functions-category-logical.md)