---
title: Funkce COLLECTEDLIST ER
description: Tento článek obsahuje obecné informace o použití funkce COLLECTEDLIST elektronického výkaznictví (ER).
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5102035cf2a8667222beb7bc42ae9aec1b311790
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280887"
---
# <a name="collectedlist-er-function"></a>Funkce COLLECTEDLIST ER

[!include [banner](../includes/banner.md)]

Funkce `COLLECTEDLIST` obsahuje hodnotu *Seznam záznamů*, která obsahuje seznam hodnot vrácených vlastností **Klíč shromážděných dat** elementů formátu a shromážděných, když byly elementy formátu použity ke generování odchozích dokumentů během spuštění formátu a která splňuje zadané podmínky. Každá podmínka se skládá z rozsahu klíče a hodnoty klíče.

## <a name="syntax"></a>Syntaxe

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumenty

`condition 1 range`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tento argument je povinný.

`condition 1 value`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tento argument je povinný.

`condition N range`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Název klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tyto další argumenty jsou nepovinné.

`condition N value`: *řetězec*

Hodnota, která je vrácena výrazem nakonfigurovaným ve vlastnosti **Hodnota klíče shromážděných dat** v komponentě formátu elektronického výkaznictví. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Vlastnosti **Název klíče shromážděných dat** a **Hodnota klíče shromážděných dat** lze konfigurovat pro komponentu **Pořadí** nebo **Element XML** formátu elektronického výkaznictví umístěnou v komponentě **Common\\File**, kde je zapnutá možnost **Podrobnosti výstupu shromažďování**.

Tato funkce vrací prázdný seznam, když je příznak **Podrobnosti výstupu shromažďování** aktuální komponenty **Common\\File** vypnutý.

V argumentech `condition range` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

V argumentech `condition value` může zástupný znak **"\*"** sloužit k vyjádření libovolných více znaků.

## <a name="example"></a>Příklad

Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.

## <a name="additional-resources"></a>Další zdroje

[Funkce shromažďování dat](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
