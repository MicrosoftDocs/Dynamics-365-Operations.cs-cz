---
title: Funkce elektronického výkaznictví FIRST
description: Toto téma obsahuje obecné informace o použití funkce FIRST elektronického výkaznictví.
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
ms.openlocfilehash: f108676c2ff8801fddc0a72be3f75d212582efe6b5d96f7515354739eb446532
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740983"
---
# <a name="first-er-function"></a>Funkce elektronického výkaznictví FIRST

[!include [banner](../includes/banner.md)]

Funkce `FIRST` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný. Pokud je seznam prázdný, vyvolá tato funkce výjimku.

## <a name="syntax"></a>Syntaxe

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="example-1"></a>Příklad 1

Výraz `FIRST(SPLIT("ABC",1)).Value` vrátí textovou hodnotu **"A"**.

## <a name="example-2"></a>Příklad 2

Výraz `FIRST(SPLIT("",1)).Value` vyvolá výjimku za běhu.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]