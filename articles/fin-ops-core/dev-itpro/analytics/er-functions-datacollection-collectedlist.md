---
title: Funkce COLLECTEDLIST ER
description: Toto téma obsahuje obecné informace o použití funkce COLLECTEDLIST elektronického výkaznictví (ER).
author: NickSelin
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
ms.openlocfilehash: 494fb0fa1000abe8d0234d512e41926103c56f05
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755317"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="14faf-103">Funkce COLLECTEDLIST ER</span><span class="sxs-lookup"><span data-stu-id="14faf-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14faf-104">Funkce `COLLECTEDLIST` obsahuje hodnotu *Seznam záznamů*, která obsahuje seznam hodnot vrácených vlastností **Klíč shromážděných dat** elementů formátu a shromážděných, když byly elementy formátu použity ke generování odchozích dokumentů během spuštění formátu a která splňuje zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="14faf-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="14faf-105">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="14faf-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="14faf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14faf-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="14faf-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="14faf-107">Arguments</span></span>

<span data-ttu-id="14faf-108">`condition 1 range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="14faf-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="14faf-109">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="14faf-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="14faf-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="14faf-110">This argument is mandatory.</span></span>

<span data-ttu-id="14faf-111">`condition 1 value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="14faf-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="14faf-112">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="14faf-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="14faf-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="14faf-113">This argument is mandatory.</span></span>

<span data-ttu-id="14faf-114">`condition N range`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="14faf-114">`condition N range`: *String*</span></span>

<span data-ttu-id="14faf-115">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="14faf-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="14faf-116">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="14faf-116">These additional arguments are optional.</span></span>

<span data-ttu-id="14faf-117">`condition N value`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="14faf-117">`condition N value`: *String*</span></span>

<span data-ttu-id="14faf-118">Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="14faf-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="14faf-119">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="14faf-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="14faf-120">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="14faf-120">Return values</span></span>

<span data-ttu-id="14faf-121">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="14faf-121">*Record list*</span></span>

<span data-ttu-id="14faf-122">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="14faf-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14faf-123">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="14faf-123">Usage notes</span></span>

<span data-ttu-id="14faf-124">Vlastnosti **Název klíče shromážděných dat** a **Hodnota klíče shromážděných dat** lze konfigurovat pro komponentu **Pořadí** nebo **Element XML** formátu elektronického výkaznictví umístěnou v komponentě **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.</span><span class="sxs-lookup"><span data-stu-id="14faf-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="14faf-125">Tato funkce vrací prázdný seznam, když je příznak **Podrobnosti výstupu shromažďování** aktuální komponenty **Common\\File** vypnutý.</span><span class="sxs-lookup"><span data-stu-id="14faf-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="14faf-126">V argumentech `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="14faf-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="14faf-127">V argumentech `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.</span><span class="sxs-lookup"><span data-stu-id="14faf-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="14faf-128">Příklad</span><span class="sxs-lookup"><span data-stu-id="14faf-128">Example</span></span>

<span data-ttu-id="14faf-129">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="14faf-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14faf-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="14faf-130">Additional resources</span></span>

[<span data-ttu-id="14faf-131">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="14faf-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]