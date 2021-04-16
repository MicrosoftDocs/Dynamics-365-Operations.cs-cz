---
title: Seznam funkcí ER v kategorii sběru dat
description: Toto téma obsahuje informace o funkcích sběru dat, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 31b5e7b08a3de77d461fff5e42164975e53dfe1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748056"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="43f6d-103">Seznam funkcí ER v kategorii sběru dat</span><span class="sxs-lookup"><span data-stu-id="43f6d-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43f6d-104">Funkce sběru dat elektronického výkaznictví se používají k počítání a sčítání ve formátu ER, který je spuštěný na základě dat výstupu, který byl již generován ve formátu **Text** nebo **Xml**.</span><span class="sxs-lookup"><span data-stu-id="43f6d-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="43f6d-105">Tento přístup se používá k vylepšení výkonu spuštěného formátu ER, k zadávání hodnot běžících součtů v generovaných dokumentech a k jiným účelům.</span><span class="sxs-lookup"><span data-stu-id="43f6d-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="43f6d-106">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="43f6d-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="43f6d-107">Seznam podporovaných funkcí</span><span class="sxs-lookup"><span data-stu-id="43f6d-107">List of supported functions</span></span>

| <span data-ttu-id="43f6d-108">Funkce</span><span class="sxs-lookup"><span data-stu-id="43f6d-108">Function</span></span> | <span data-ttu-id="43f6d-109">Popis</span><span class="sxs-lookup"><span data-stu-id="43f6d-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="43f6d-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="43f6d-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="43f6d-111">Tato funkce vrací hodnotu *Seznam záznamů*, která obsahuje seznam hodnot vrácených vlastností **Klíč shromážděných dat** elementů formátu a shromážděných, když byly elementy formátu použity ke generování odchozího dokumentu během spuštění formátu a která splňuje zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="43f6d-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="43f6d-112">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="43f6d-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="43f6d-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="43f6d-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="43f6d-114">Tato funkce vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce.</span><span class="sxs-lookup"><span data-stu-id="43f6d-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="43f6d-115">Podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="43f6d-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="43f6d-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="43f6d-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="43f6d-117">Tato funkce vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="43f6d-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="43f6d-118">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="43f6d-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="43f6d-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="43f6d-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="43f6d-120">Tato funkce vrací hodnotu *řetězec*, která představuje název aktuálního prvku formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="43f6d-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="43f6d-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="43f6d-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="43f6d-122">Tato funkce vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce.</span><span class="sxs-lookup"><span data-stu-id="43f6d-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="43f6d-123">Podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="43f6d-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="43f6d-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="43f6d-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="43f6d-125">Tato funkce vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="43f6d-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="43f6d-126">Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.</span><span class="sxs-lookup"><span data-stu-id="43f6d-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="43f6d-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="43f6d-127">Additional resources</span></span>

[<span data-ttu-id="43f6d-128">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="43f6d-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="43f6d-129">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="43f6d-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="43f6d-130">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="43f6d-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]