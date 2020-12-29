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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52f9cdb78efa6fe0dbebd2ffd78cd6e9185d6b2e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685344"
---
# <a name="sumif-er-function"></a><span data-ttu-id="29816-103">Funkce SUMIF</span><span class="sxs-lookup"><span data-stu-id="29816-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29816-104">Funkce `SUMIF` vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce.</span><span class="sxs-lookup"><span data-stu-id="29816-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="29816-105">Podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="29816-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="29816-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29816-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="29816-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="29816-107">Arguments</span></span>

<span data-ttu-id="29816-108">`key name for summing`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="29816-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="29816-109">Hodnota vrácená výrazem, který byl konfigurován ve vlastnosti **Název klíče shromážděných údajů** součásti pro elektronické výkaznictví (ER), pro kterou musí být hodnota vazby použita pro účely sčítání.</span><span class="sxs-lookup"><span data-stu-id="29816-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="29816-110">Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="29816-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="29816-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="29816-111">Return values</span></span>

<span data-ttu-id="29816-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="29816-112">*Real*</span></span>

<span data-ttu-id="29816-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="29816-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="29816-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="29816-114">Usage notes</span></span>

<span data-ttu-id="29816-115">Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="29816-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="29816-116">V argumentu `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="29816-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="29816-117">V argumentu `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="29816-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="29816-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="29816-118">Example</span></span>

<span data-ttu-id="29816-119">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="29816-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="29816-120">Další informace a příklady použití této funkce naleznete v části [Odložení provádění sekvenčních prvků ve formátech elektronického výkaznictví](er-defer-sequence-element.md#Example) a [Odložení provádění prvků XML ve formátech elektronického výkaznictví](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="29816-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29816-121">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="29816-121">Additional resources</span></span>

[<span data-ttu-id="29816-122">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="29816-122">Data collection functions</span></span>](er-functions-category-data-collection.md)
