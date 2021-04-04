---
title: Funkce COUNTIFS ER
description: Toto téma obsahuje obecné informace o použití funkce COUNTIFS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5bc0beb20f600afdea2d58187dd2a9c26a775ec1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561319"
---
# <a name="countifs-er-function"></a><span data-ttu-id="6011f-103">Funkce COUNTIFS ER</span><span class="sxs-lookup"><span data-stu-id="6011f-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6011f-104">Funkce `COUNTIFS` vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="6011f-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="6011f-105">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="6011f-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6011f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6011f-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="6011f-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="6011f-107">Arguments</span></span>

<span data-ttu-id="6011f-108">`condition 1 range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="6011f-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="6011f-109">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6011f-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="6011f-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="6011f-110">This argument is mandatory.</span></span>

<span data-ttu-id="6011f-111">`condition 1 value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="6011f-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="6011f-112">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6011f-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="6011f-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="6011f-113">This argument is mandatory.</span></span>

<span data-ttu-id="6011f-114">`condition N range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="6011f-114">`condition N range`: *String*</span></span>

<span data-ttu-id="6011f-115">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6011f-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="6011f-116">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="6011f-116">These additional arguments are optional.</span></span>

<span data-ttu-id="6011f-117">`condition N value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="6011f-117">`condition N value`: *String*</span></span>

<span data-ttu-id="6011f-118">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6011f-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="6011f-119">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="6011f-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6011f-120">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="6011f-120">Return values</span></span>

<span data-ttu-id="6011f-121">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="6011f-121">*Integer*</span></span>

<span data-ttu-id="6011f-122">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="6011f-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6011f-123">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="6011f-123">Usage notes</span></span>

<span data-ttu-id="6011f-124">Vlastnosti **Název klíče shromážděných dat** a **Hodnota klíče shromážděných dat** lze konfigurovat pro komponentu **Pořadí** nebo **Element XML** formátu elektronického výkaznictví umístěnou v komponentě **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="6011f-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6011f-125">Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="6011f-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="6011f-126">V argumentech `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="6011f-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="6011f-127">V argumentech `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="6011f-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="6011f-128">Příklad</span><span class="sxs-lookup"><span data-stu-id="6011f-128">Example</span></span>

<span data-ttu-id="6011f-129">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="6011f-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6011f-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="6011f-130">Additional resources</span></span>

[<span data-ttu-id="6011f-131">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="6011f-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]