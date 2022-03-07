---
title: Funkce elektronického výkaznictví LISTJOIN
description: Toto téma obsahuje obecné informace o použití funkce LISTJOIN elektronického výkaznictví.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b300cef0a508f7cc37397480738091158efdead
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027908"
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

![Stránka Návrhář mapování modelu ER](./media/er-functions-list-listjoin-image1.gif)

V tomto případě výraz `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` vrátí nový seznam, který obsahuje dva záznamy.

![Stránka návrháře mapování modelu elektronického výkaznictví se dvěma záznamy](./media/er-functions-list-listjoin-image2.gif)

Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu `Real`, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.

![Pole částky na stránce návrháře mapování modelu elektronického výkaznictví](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)

[Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
