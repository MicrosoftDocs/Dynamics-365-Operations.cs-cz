---
title: Funkce elektronického výkaznictví LISTJOIN
description: Tento článek obsahuje obecné informace o použití funkce LISTJOIN elektronického výkaznictví.
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ec8a5985277de8036ec8ad51b947a8bab098a1c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291197"
---
# <a name="listjoin-er-function"></a>Funkce elektronického výkaznictví LISTJOIN

[!include [banner](../includes/banner.md)]

Funkce `LISTJOIN` vrací hodnotu typu *seznam záznamů*, která představuje nový spojený seznam záznamů vytvořený ze zadaných argumentů.

## <a name="syntax"></a>Syntaxe

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumenty

`list 1`: *seznam záznamů*

Odkaz na zdroj dat datového typu *seznam záznamů*. Tento argument je povinný.

`list N`: *seznam záznamů*

Odkaz na zdroj dat datového typu *seznam záznamů*. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Struktura vytvořeného seznamu obsahuje pouze pole, která jsou přítomna ve struktuře každého seznamu záznamů, který na který je odkazováno v argumentech.

## <a name="example"></a>Příklad

Zadáte zdroj dat **Záznam 1** typu `Container`. Tento zdroj dat obsahuje následující vnořená pole typu `Calculated field`:

- **Kód**: Toto pole obsahuje výraz, který vrací hodnotu typu `String`.
- **Množství**: Toto pole obsahuje výraz, který vrací hodnotu typu `Real`.

Zadáte pak zdroj dat **Záznam 2** typu `Container`. Tento zdroj dat obsahuje následující vnořená pole typu `Calculated field`:

- **Množství**: Toto pole obsahuje výraz, který vrací hodnotu typu `Real`.
- **IsValid**: Toto pole obsahuje výraz, který vrací hodnotu typu `Boolean`.

![Stránka Návrhář mapování modelu ER.](./media/er-functions-list-listjoin-image1.gif)

V tomto případě výraz `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` vrátí nový seznam, který obsahuje dva záznamy.

![Stránka návrháře mapování modelu elektronického výkaznictví se dvěma záznamy.](./media/er-functions-list-listjoin-image2.gif)

Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu `Real`, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.

![Pole částky na stránce návrháře mapování modelu elektronického výkaznictví.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)

[Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
