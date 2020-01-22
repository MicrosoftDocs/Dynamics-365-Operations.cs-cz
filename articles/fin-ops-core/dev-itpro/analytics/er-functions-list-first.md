---
title: Funkce elektronického výkaznictví FIRST
description: Toto téma obsahuje obecné informace o použití funkce FIRST elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917343"
---
# <a name="FIRST">Funkce elektronického výkaznictví FIRST</a>

[!include [banner](../includes/banner.md)]

Funkce `FIRST` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný. Pokud je seznam prázdný, vyvolá tato funkce výjimku.

## <a name="syntax"></a>Syntaxe

```
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
