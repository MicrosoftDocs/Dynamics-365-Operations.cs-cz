---
title: Funkce el. výkaznictví GUIDVALUE
description: Toto téma obsahuje obecné informace o použití funkce GUIDVALUE elektronického výkaznictví.
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
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915687"
---
# <span data-ttu-id="f19cb-103"><a name="GUIDVALUE">Funkce el. výkaznictví GUIDVALUE</a></span><span class="sxs-lookup"><span data-stu-id="f19cb-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f19cb-104">Funkce `GUIDVALUE` převede zadaný vstup datového typu *řetězec* na datovou položku datového typu *GUID*.</span><span class="sxs-lookup"><span data-stu-id="f19cb-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f19cb-105">Syntax</span></span>

```
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="f19cb-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="f19cb-106">Arguments</span></span>

<span data-ttu-id="f19cb-107">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f19cb-107">`input`: *String*</span></span>

<span data-ttu-id="f19cb-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="f19cb-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f19cb-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="f19cb-109">Return values</span></span>

<span data-ttu-id="f19cb-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f19cb-110">*GUID*</span></span>

<span data-ttu-id="f19cb-111">Výsledná hodnota globálně jedinečného identifikátoru (GUID).</span><span class="sxs-lookup"><span data-stu-id="f19cb-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f19cb-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="f19cb-112">Usage notes</span></span>

<span data-ttu-id="f19cb-113">Pro převod opačným směrem (to znamená převod zadaného vstupu datového typu *GUID* na datovou položku datového typu *řetězec*) lze použít funkci [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="f19cb-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="f19cb-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="f19cb-114">Example</span></span>

<span data-ttu-id="f19cb-115">Definujte v mapování modelu následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="f19cb-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="f19cb-116">Zdroj dat **myID** typu *vypočítané pole*, který obsahuje výraz `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="f19cb-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="f19cb-117">Zdroj dat **Users** typu *záznamy tabulky*, který odkazuje na tabulku UserInfo</span><span class="sxs-lookup"><span data-stu-id="f19cb-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="f19cb-118">Potom můžete použít výraz jako `FILTER (Users, Users.objectId = myID)` pro filtrování tabulky UserInfo podle pole **objectId** datového typu *GUID*.</span><span class="sxs-lookup"><span data-stu-id="f19cb-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f19cb-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f19cb-119">Additional resources</span></span>

[<span data-ttu-id="f19cb-120">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="f19cb-120">Text functions</span></span>](er-functions-category-text.md)