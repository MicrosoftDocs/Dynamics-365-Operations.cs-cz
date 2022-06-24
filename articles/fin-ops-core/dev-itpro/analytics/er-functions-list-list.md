---
title: Funkce el. výkaznictví LIST
description: Tento článek obsahuje obecné informace o použití funkce LIST elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 758462e577c89379fd9b3d68337048488821eb25
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881181"
---
# <a name="list-er-function"></a>Funkce el. výkaznictví LIST

[!include [banner](../includes/banner.md)]

Funkce `LIST` vrátí hodnotu typu *seznam záznamů*, která se skládá z nového seznamu záznamů vytvořeného ze zadaných argumentů.

## <a name="syntax"></a>Syntaxe

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumenty

`record 1`: *kontejner (záznam)*

Odkaz na zdroj dat datového typu *záznam*. Tento argument je povinný.

`record N`: *kontejner (záznam)*

Odkaz na zdroj dat datového typu *záznam*. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Struktura vytvořeného seznamu obsahuje pouze pole, která jsou přítomna ve struktuře každého záznamu, který je uveden v argumentech.

## <a name="example"></a>Příklad

Zadáte zdroj dat **Záznam 1** typu *kontejner*. Tento zdroj dat obsahuje následující vnořená pole typu *vypočítané pole*:

- **Kód:** Toto pole obsahuje výraz, který vrací hodnotu typu *řetězec*.
- **Množství:** Toto pole obsahuje výraz, který vrací hodnotu typu *reálné číslo*.

Poté zadáte zdroj dat **Záznam 2** typu *kontejner*. Tento zdroj dat obsahuje následující vnořená pole typu *vypočítané pole*:

- **Množství:** Toto pole obsahuje výraz, který vrací hodnotu typu *reálné číslo*.
- **JePlatný:** Toto pole obsahuje výraz, který vrací hodnotu typu *logická hodnota*.

V tomto případě výraz `LIST('Record 1', 'Record 2')` vrátí nový seznam, který obsahuje dva záznamy. Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu *reálné číslo*, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]