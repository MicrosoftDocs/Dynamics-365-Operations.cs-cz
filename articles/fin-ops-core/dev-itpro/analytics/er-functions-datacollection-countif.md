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
# <a name="COUNTIF">Funkce COUNTIF ER</a>

[!include [banner](../includes/banner.md)]

Funkce `COUNTIF` vrací hodnotu *Celé číslo*, která představuje počet elementů formátu, které byly shromážděny, když byly prvky formátu použity ke generování výstupního dokumentu během spuštění formátu a které vyhovují zadané podmínce. Podmínka se skládá z rozsahu klíče a hodnoty klíče.

## <a name="syntax"></a>Syntaxe

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumenty

`condition range`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.

`condition value`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Vlastnosti **Název klíče shromážděných dat** a **Hodnota klíče shromážděných dat** lze konfigurovat pro komponentu **Pořadí** nebo **Element XML** formátu elektronického výkaznictví umístěnou v komponentě **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

Tato funkce vrací hodnotu **0** (nula), když je možnost **Podrobnosti o výstupu sběru** aktuální komponenty **Common\\File** vypnutá.

V argumentu `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

V argumentu `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

## <a name="example"></a>Příklad

Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.

## <a name="additional-resources"></a>Další zdroje

[Funkce shromažďování dat](er-functions-category-data-collection.md)
