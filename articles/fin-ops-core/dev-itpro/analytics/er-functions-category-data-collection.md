---
title: Seznam funkcí ER v kategorii sběru dat
description: Toto téma obsahuje informace o funkcích sběru dat, které jsou podporovány v elektronickém výkaznictví (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686286"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Seznam funkcí ER v kategorii sběru dat

[!include [banner](../includes/banner.md)]

Funkce sběru dat elektronického výkaznictví se používají k počítání a sčítání ve formátu ER, který je spuštěný na základě dat výstupu, který byl již generován ve formátu **Text** nebo **Xml**. Tento přístup se používá k vylepšení výkonu spuštěného formátu ER, k zadávání hodnot běžících součtů v generovaných dokumentech a k jiným účelům. Toto téma obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Tato funkce vrací hodnotu *Seznam záznamů*, která obsahuje seznam hodnot vrácených vlastností **Klíč shromážděných dat** elementů formátu a shromážděných, když byly elementy formátu použity ke generování odchozího dokumentu během spuštění formátu a která splňuje zadané podmínky. Každá podmínka se skládá z rozsahu klíče a hodnoty klíče. |
| [CountIF](er-functions-datacollection-countif.md) | Tato funkce vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce. Podmínka se skládá z rozsahu klíče a hodnoty klíče. |
| [CountIFs](er-functions-datacollection-countifs.md) | Tato funkce vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám. Každá podmínka se skládá z rozsahu klíče a hodnoty klíče. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Tato funkce vrací hodnotu *řetězec*, která představuje název aktuálního prvku formátu elektronického výkaznictví. |
| [SumIF](er-functions-datacollection-sumif.md) | Tato funkce vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce. Podmínka se skládá z rozsahu klíče a hodnoty klíče. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Tato funkce vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám. Každá podmínka se skládá z rozsahu klíče a hodnoty klíče. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)
