---
title: Funkce SUMIFS ER
description: Toto téma obsahuje obecné informace o použití funkce SUMIFS elektronického výkaznictví.
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
ms.openlocfilehash: a3adfe62d9fd7bdc23784cf7311f65a4d2e88960
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747076"
---
# <a name="sumifs-er-function"></a>Funkce SUMIFS ER

[!include [banner](../includes/banner.md)]

Funkce `SUMIFS` vrací hodnotu *reálné číslo*, která představuje součet hodnot, které byly vráceny vazbami prvků formátu a shromážděny, když byly formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadaným podmínkám. Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.

## <a name="syntax"></a>Syntaxe

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumenty

`key name for summing`: *řetězec*

Hodnota vrácená výrazem, který byl konfigurován ve vlastnosti **Název klíče shromážděných údajů** součásti pro elektronické výkaznictví (ER), pro kterou musí být hodnota vazby použita pro účely sčítání.

Vlastnost **Název klíče shromážděných dat** může být konfigurována pro komponentu **Číselný** nebo komponentu **Řetězec** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

`condition 1 range`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tento argument je povinný.

Vlastnost **Název klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

`condition 1 value`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tento argument je povinný.

Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

`condition N range`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tyto další argumenty jsou nepovinné.

Vlastnost **Název klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

`condition N value`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tyto další argumenty jsou nepovinné.

Vlastnost **Hodnota klíče shromážděných dat** může být konfigurována pro komponentu **Pořadí** nebo komponentu **Element XML** formátu elektronického výkaznictví, která je umístěna pod komponentou **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.

V argumentech `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

V argumentech `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

## <a name="example"></a>Příklad

Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.

## <a name="additional-resources"></a>Další zdroje

[Funkce shromažďování dat](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]