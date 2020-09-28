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
ms.openlocfilehash: 174ac28ee2b726ec7fb2ff6d3dda45906c56af65
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745602"
---
# <a name="sumif-er-function"></a>Funkce SUMIF

[!include [banner](../includes/banner.md)]

Funkce `SUMIF` vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce. Podmínka se skládá z rozsahu klíče a hodnoty klíče.

## <a name="syntax"></a>Syntaxe

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Argumenty

`key name for summing`: *řetězec*

Hodnota vrácená výrazem, který byl konfigurován ve vlastnosti **Název klíče shromážděných údajů** součásti pro elektronické výkaznictví (ER), pro kterou musí být hodnota vazby použita pro účely sčítání.

Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.

V argumentu `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

V argumentu `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

## <a name="example"></a>Příklad

Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.

Další informace a příklady použití této funkce naleznete v části [Odložení provádění sekvenčních prvků ve formátech elektronického výkaznictví](er-defer-sequence-element.md#Example) a [Odložení provádění prvků XML ve formátech elektronického výkaznictví](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Další prostředky

[Funkce shromažďování dat](er-functions-category-data-collection.md)
