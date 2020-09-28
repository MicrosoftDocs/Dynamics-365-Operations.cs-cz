---
title: Funkce el. výkaznictví GETENUMVALUEBYNAME
description: Toto téma obsahuje obecné informace o použití funkce GETENUMVALUEBYNAME elektronického výkaznictví.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743848"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="da196-103">Funkce el. výkaznictví GETENUMVALUEBYNAME</span><span class="sxs-lookup"><span data-stu-id="da196-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da196-104">Funkce `GETENUMVALUEBYNAME` vyhledá určitou hodnotu typu *výčet* v zadaném zdroji dat výčtu pomocí názvu výčtu, který je zadán jako hodnota typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="da196-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="da196-105">Pokud je nalezena hodnota *výčet*, funkce ji vrátí.</span><span class="sxs-lookup"><span data-stu-id="da196-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="da196-106">V opačném případě funkce vrátí hodnotu výčtu **null**.</span><span class="sxs-lookup"><span data-stu-id="da196-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="da196-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da196-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="da196-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="da196-108">Arguments</span></span>

<span data-ttu-id="da196-109">`enumeration data source path`: *výčet*</span><span class="sxs-lookup"><span data-stu-id="da196-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="da196-110">Platná cesta zdroje dat jednoho z následujících typů výčtu:</span><span class="sxs-lookup"><span data-stu-id="da196-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="da196-111">Výčet modelů elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="da196-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="da196-112">Výčet formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="da196-112">ER format enumeration</span></span>
- <span data-ttu-id="da196-113">Výčet Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="da196-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="da196-114">`enumeration value text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="da196-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="da196-115">Hodnota typu řetězec, která představuje název jedné hodnoty výčtu.</span><span class="sxs-lookup"><span data-stu-id="da196-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="da196-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="da196-116">Return values</span></span>

<span data-ttu-id="da196-117">Hodnota typu *výčet* s možností nabytí hodnoty Null</span><span class="sxs-lookup"><span data-stu-id="da196-117">Nullable *Enum*</span></span>

<span data-ttu-id="da196-118">Výsledná výčtová hodnota.</span><span class="sxs-lookup"><span data-stu-id="da196-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="da196-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="da196-119">Usage notes</span></span>

<span data-ttu-id="da196-120">Není vyvolána žádná výjimka, pokud není nalezena hodnota typu *výčet* za použití názvu výčtové hodnoty, která je zadána jako hodnota typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="da196-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="da196-121">Příklad</span><span class="sxs-lookup"><span data-stu-id="da196-121">Example</span></span>

<span data-ttu-id="da196-122">Na následujícím obrázku je výčet **ReportDirection** uveden v datovém modelu.</span><span class="sxs-lookup"><span data-stu-id="da196-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="da196-123">Všimněte si, že pro výčtové hodnoty jsou definovány popisky.</span><span class="sxs-lookup"><span data-stu-id="da196-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="da196-124">Následující obrázek znázorňuje tyto podrobnosti:</span><span class="sxs-lookup"><span data-stu-id="da196-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="da196-125">Zdroj dat **$Direction** je konfigurován v sestavě elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="da196-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="da196-126">Tento zdroj dat je konfigurován na základě výčtu modelu **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="da196-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="da196-127">Výraz `$IsArrivals` je určený k použití zdroje dat **$Direction** výčtu modelů jako parametr této funkce.</span><span class="sxs-lookup"><span data-stu-id="da196-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="da196-128">Hodnota tohoto porovnávacího výrazu je **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="da196-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="da196-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="da196-129">Additional resources</span></span>

[<span data-ttu-id="da196-130">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="da196-130">Text functions</span></span>](er-functions-category-text.md)
