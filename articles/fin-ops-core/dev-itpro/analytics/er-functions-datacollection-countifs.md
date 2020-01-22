---
title: Funkce COUNTIFS ER
description: Toto téma obsahuje obecné informace o použití funkce COUNTIFS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 02e401254cdfebd4b549f63dbd6a5f925e7bf544
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916469"
---
# <span data-ttu-id="7c27a-103"><a name="COUNTIFS">Funkce COUNTIFS ER</a></span><span class="sxs-lookup"><span data-stu-id="7c27a-103"><a name="COUNTIFS">COUNTIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c27a-104">Funkce `COUNTIFS` vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="7c27a-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="7c27a-105">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="7c27a-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c27a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c27a-106">Syntax</span></span>

```
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="7c27a-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="7c27a-107">Arguments</span></span>

<span data-ttu-id="7c27a-108">`condition 1 range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="7c27a-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="7c27a-109">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7c27a-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="7c27a-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="7c27a-110">This argument is mandatory.</span></span>

<span data-ttu-id="7c27a-111">`condition 1 value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="7c27a-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="7c27a-112">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7c27a-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="7c27a-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="7c27a-113">This argument is mandatory.</span></span>

<span data-ttu-id="7c27a-114">`condition N range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="7c27a-114">`condition N range`: *String*</span></span>

<span data-ttu-id="7c27a-115">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7c27a-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="7c27a-116">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="7c27a-116">These additional arguments are optional.</span></span>

<span data-ttu-id="7c27a-117">`condition N value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="7c27a-117">`condition N value`: *String*</span></span>

<span data-ttu-id="7c27a-118">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7c27a-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="7c27a-119">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="7c27a-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c27a-120">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7c27a-120">Return values</span></span>

<span data-ttu-id="7c27a-121">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="7c27a-121">*Integer*</span></span>

<span data-ttu-id="7c27a-122">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="7c27a-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7c27a-123">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="7c27a-123">Usage notes</span></span>

<span data-ttu-id="7c27a-124">Vlastnosti **Název klíče shromážděných dat** a **Hodnota klíče shromážděných dat** lze konfigurovat pro komponentu **Pořadí** nebo **Element XML** formátu elektronického výkaznictví umístěnou v komponentě **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="7c27a-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="7c27a-125">Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="7c27a-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="7c27a-126">V argumentech `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="7c27a-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="7c27a-127">V argumentech `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="7c27a-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="7c27a-128">Příklad</span><span class="sxs-lookup"><span data-stu-id="7c27a-128">Example</span></span>

<span data-ttu-id="7c27a-129">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="7c27a-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c27a-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7c27a-130">Additional resources</span></span>

[<span data-ttu-id="7c27a-131">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="7c27a-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
