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
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249028"
---
# <a name=""></a><a name="LISTJOIN">Funkce elektronického výkaznictví LISTJOIN</a>

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

V tomto případě výraz `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` vrátí nový seznam, který obsahuje dva záznamy. Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu `Real`, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)
