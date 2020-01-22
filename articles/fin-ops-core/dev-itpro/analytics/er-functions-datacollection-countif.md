---
title: Funkce COUNTIF ER
description: Toto téma obsahuje obecné informace o použití funkce COUNTIF elektronického výkaznictví.
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
ms.openlocfilehash: ca7c0f449aff75527e5052ba01e6fc0e29bb0fd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917688"
---
# <span data-ttu-id="68625-103"><a name="COUNTIF">Funkce COUNTIF ER</a></span><span class="sxs-lookup"><span data-stu-id="68625-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68625-104">Funkce `COUNTIF` vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce.</span><span class="sxs-lookup"><span data-stu-id="68625-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="68625-105">Podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="68625-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="68625-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68625-106">Syntax</span></span>

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="68625-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="68625-107">Arguments</span></span>

<span data-ttu-id="68625-108">`condition range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="68625-108">`condition range`: *String*</span></span>

<span data-ttu-id="68625-109">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="68625-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="68625-110">`condition value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="68625-110">`condition value`: *String*</span></span>

<span data-ttu-id="68625-111">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="68625-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="68625-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="68625-112">Return values</span></span>

<span data-ttu-id="68625-113">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="68625-113">*Integer*</span></span>

<span data-ttu-id="68625-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="68625-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="68625-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="68625-115">Usage notes</span></span>

<span data-ttu-id="68625-116">Vlastnosti **Název klíče shromážděných dat** a **Hodnota klíče shromážděných dat** lze konfigurovat pro komponentu **Pořadí** nebo **Element XML** formátu elektronického výkaznictví umístěnou v komponentě **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="68625-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="68625-117">Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.</span><span class="sxs-lookup"><span data-stu-id="68625-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="68625-118">V argumentu `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="68625-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="68625-119">V argumentu `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="68625-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="68625-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="68625-120">Example</span></span>

<span data-ttu-id="68625-121">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="68625-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68625-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="68625-122">Additional resources</span></span>

[<span data-ttu-id="68625-123">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="68625-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
