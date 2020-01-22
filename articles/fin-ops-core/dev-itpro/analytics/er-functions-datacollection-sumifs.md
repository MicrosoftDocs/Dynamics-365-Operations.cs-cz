---
title: Funkce SUMIFS ER
description: Toto téma obsahuje obecné informace o použití funkce SUMIFS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917596"
---
# <span data-ttu-id="174c0-103"><a name="SUMIFS">Funkce SUMIFS ER</a></span><span class="sxs-lookup"><span data-stu-id="174c0-103"><a name="SUMIFS">SUMIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="174c0-104">Funkce `SUMIFS` vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="174c0-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="174c0-105">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="174c0-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="174c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="174c0-106">Syntax</span></span>

```
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="174c0-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="174c0-107">Arguments</span></span>

<span data-ttu-id="174c0-108">`key name for summing`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="174c0-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="174c0-109">Hodnota vrácená výrazem, který byl konfigurován ve vlastnosti **Název klíče shromážděných údajů** součásti pro elektronické výkaznictví (ER), pro kterou musí být hodnota vazby použita pro účely sčítání.</span><span class="sxs-lookup"><span data-stu-id="174c0-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="174c0-110">Vlastnost **Název klíče shromážděných dat** může být konfigurována pro komponentu **Číselný** nebo komponentu **Řetězec** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="174c0-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="174c0-111">`condition 1 range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="174c0-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="174c0-112">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="174c0-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="174c0-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="174c0-113">This argument is mandatory.</span></span>

<span data-ttu-id="174c0-114">Vlastnost **Název klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="174c0-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="174c0-115">`condition 1 value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="174c0-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="174c0-116">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="174c0-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="174c0-117">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="174c0-117">This argument is mandatory.</span></span>

<span data-ttu-id="174c0-118">Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="174c0-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="174c0-119">`condition N range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="174c0-119">`condition N range`: *String*</span></span>

<span data-ttu-id="174c0-120">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="174c0-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="174c0-121">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="174c0-121">These additional arguments are optional.</span></span>

<span data-ttu-id="174c0-122">Vlastnost **Název klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="174c0-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="174c0-123">`condition N value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="174c0-123">`condition N value`: *String*</span></span>

<span data-ttu-id="174c0-124">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="174c0-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="174c0-125">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="174c0-125">These additional arguments are optional.</span></span>

<span data-ttu-id="174c0-126">Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="174c0-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="174c0-127">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="174c0-127">Return values</span></span>

<span data-ttu-id="174c0-128">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="174c0-128">*Real*</span></span>

<span data-ttu-id="174c0-129">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="174c0-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="174c0-130">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="174c0-130">Usage notes</span></span>

<span data-ttu-id="174c0-131">Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="174c0-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="174c0-132">V argumentech `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="174c0-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="174c0-133">V argumentech `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="174c0-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="174c0-134">Příklad</span><span class="sxs-lookup"><span data-stu-id="174c0-134">Example</span></span>

<span data-ttu-id="174c0-135">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="174c0-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="174c0-136">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="174c0-136">Additional resources</span></span>

[<span data-ttu-id="174c0-137">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="174c0-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
