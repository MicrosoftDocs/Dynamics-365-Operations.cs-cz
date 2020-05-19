---
title: Funkce SUMIF
description: Toto téma obsahuje obecné informace o použití funkce SUMIF elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 9df7be0825203f91434d348385c1ee358ae555ea
ms.sourcegitcommit: ef6fd78c817f93610771cfb2477f52f16b882164
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290193"
---
# <a name=""></a><span data-ttu-id="0a11e-103"><a name="SUMIF">Funkce SUMIF</a></span><span class="sxs-lookup"><span data-stu-id="0a11e-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a11e-104">Funkce `SUMIF` vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce.</span><span class="sxs-lookup"><span data-stu-id="0a11e-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="0a11e-105">Podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="0a11e-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a11e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a11e-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="0a11e-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0a11e-107">Arguments</span></span>

<span data-ttu-id="0a11e-108">`key name for summing`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="0a11e-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="0a11e-109">Hodnota vrácená výrazem, který byl konfigurován ve vlastnosti **Název klíče shromážděných údajů** součásti pro elektronické výkaznictví (ER), pro kterou musí být hodnota vazby použita pro účely sčítání.</span><span class="sxs-lookup"><span data-stu-id="0a11e-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="0a11e-110">Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="0a11e-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a11e-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0a11e-111">Return values</span></span>

<span data-ttu-id="0a11e-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="0a11e-112">*Real*</span></span>

<span data-ttu-id="0a11e-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="0a11e-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0a11e-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="0a11e-114">Usage notes</span></span>

<span data-ttu-id="0a11e-115">Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="0a11e-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="0a11e-116">V argumentu `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="0a11e-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="0a11e-117">V argumentu `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="0a11e-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="0a11e-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="0a11e-118">Example</span></span>

<span data-ttu-id="0a11e-119">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="0a11e-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="0a11e-120">Další informace a příklady použití této funkce naleznete v části [Odložení provádění sekvenčních prvků ve formátech elektronického výkaznictví](er-defer-sequence-element.md#Example) a [Odložení provádění prvků XML ve formátech elektronického výkaznictví](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="0a11e-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a11e-121">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0a11e-121">Additional resources</span></span>

[<span data-ttu-id="0a11e-122">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="0a11e-122">Data collection functions</span></span>](er-functions-category-data-collection.md)
