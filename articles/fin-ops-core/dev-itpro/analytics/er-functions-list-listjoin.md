---
title: Funkce elektronického výkaznictví LISTJOIN
description: Toto téma obsahuje obecné informace o použití funkce LISTJOIN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745098"
---
# <a name="listjoin-er-function"></a>Funkce elektronického výkaznictví LISTJOIN

[!include [banner](../includes/banner.md)]

Funkce `LISTJOIN` vrací hodnotu typu *seznam záznamů*, která představuje nový spojený seznam záznamů vytvořený ze zadaných argumentů.

## <a name="syntax"></a>Syntaxe

```vb
LIST (list 1 [, list 2, …, list N])
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

![Stránka Návrhář mapování modelu ER](./media/er-functions-list-listjoin-image1.gif)

V tomto případě výraz `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` vrátí nový seznam, který obsahuje dva záznamy.

![Stránka návrháře mapování modelu elektronického výkaznictví se dvěma záznamy](./media/er-functions-list-listjoin-image2.gif)

Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu `Real`, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.

![Pole částky na stránce návrháře mapování modelu elektronického výkaznictví](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)

[Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace](er-debug-data-sources.md)
