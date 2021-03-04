---
title: Funkce el. výkaznictví VALUEIN
description: Toto téma obsahuje obecné informace o použití funkce VALUEIN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0a133067ab74c711084cc1d7f456cbe49acdf79d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686923"
---
# <a name="valuein-er-function"></a>Funkce el. výkaznictví VALUEIN

[!include [banner](../includes/banner.md)]

Funkce `VALUEIN` určuje, zda zadaný vstup odpovídá některé hodnotě zadané položky v zadaném seznamu. Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumenty

`input`: *pole*

Platná cesta k položce zdroje dat typu *seznam záznamů*. Hodnota této položky bude spárována.

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`list item expression`: *logická hodnota*

Platný podmíněný výraz, který buď odkazuje na nebo obsahuje jedno pole určeného seznamu, který by měl být použit pro párování.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="usage-notes"></a>Poznámky k použití

Obecně platí, že funkce `VALUEIN` je převedena do sady podmínek **OR**. Pokud je seznam podmínek **OR** velký a může být překročena maximální celková délka příkazu SQL, zvažte použití funkce [`VALUEINLARGE`](er-functions-logical-valueinlarge.md).

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

V některých případech ji lze převést do databázového příkazu SQL pomocí operátoru `EXISTS JOIN`.

## <a name="example-1"></a>Příklad 1

V mapování modelu definujete zdroj dat datové typu **seznam** typu *vypočítané pole*. Tento zdroj dat obsahuje výraz `SPLIT ("a,b,c", ",")`.

Když je zdroj dat volán, pokud byl nakonfigurován jako výraz `VALUEIN ("B", List, List.Value)`, vrátí hodnotu **TRUE**. V tomto případě je funkce `VALUEIN` převedena do následující sady podmínek: `(("B" = "a") or ("B" = "b") or ("B" = "c"))` kde `("B" = "b")` rovná se **TRUE**.

Když je zdroj dat volán, pokud byl nakonfigurován jako výraz `VALUEIN ("B", List, LEFT(List.Value, 0))`, vrátí hodnotu **FALSE**. V tomto případě je funkce `VALUEIN` převedena na následující podmínku: `("B" = "")`, které se nerovná **TRUE**.

Maximální počet znaků v textu takové podmínky je 32 768 znaků. Proto byste neměli vytvářet zdroje dat, které mohou překročit tento limit za běhu. Při přesažení limitu se aplikace zastaví a je vyvolána výjimka. Například k této situaci může dojít, pokud je datový zdroj nakonfigurován jako `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, a seznamy **List1** a **List2** obsahují velké množství záznamů.

V některých případech je funkce `VALUEIN` přeložena do výkazu databázi pomocí operátoru `EXISTS JOIN`. K tomuto chování dochází, když se používá funkce [`FILTER`](er-functions-list-filter.md) a jsou splněny následující podmínky:

- Možnost **ASK FOR QUERY** je vypnuta pro datový zdroj funkce `VALUEIN`, která se odkazuje na seznam záznamů. Žádné další podmínky nebudou použity na tento zdroj dat za běhu.
- Žádné vnořené výrazy nejsou nakonfigurovány pro datový zdroj funkce `VALUEIN`, která se odkazuje na seznam záznamů.
- Položka seznamu funkce `VALUEIN` odkazuje na pole zadaného zdroje dat, nikoliv na výraz nebo metodu tohoto zdroje dat.

Zvažte použití této možnosti místo funkce [`WHERE`](er-functions-list-where.md), jak je popsáno výše v tomto příkladu.

## <a name="example-2"></a>Příklad 2

Definujte v mapování modelu následující zdroje dat:

- Zdroj dat **In** typu *záznamy tabulky*. Tento zdroj dat odkazuje na tabulku Intrastat.
- Zdroj dat **Port** typu *záznamy tabulky*. Tento zdroj dat odkazuje na tabulku IntrastatPort.

Pokud je volán zdroj dat nakonfigurovaný jako výraz `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, je vygenerován následující příkaz SQL pro navrácení vyfiltrovaných záznamů tabulky Intrastat.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Pro pole **dataAreaId** je konečný příkaz SQL vygenerován pomocí operátoru `IN`.

## <a name="example-3"></a>Příklad 3

Definujte v mapování modelu následující zdroje dat:

- Zdroj dat **Le** typu *vypočítané pole*. Tento zdroj dat obsahuje výraz `SPLIT ("DEMF,GBSI,USMF", ",")`.
- Zdroj dat **In** typu *záznamy tabulky*. Tento zdroj dat odkazuje na tabulku Intrastat a je pro ni zapnuta možnost **Cross-company**.

Pokud je volán zdroj dat nakonfigurovaný jako výraz `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, obsahuje konečný příkaz SQL následující podmínku.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Další prostředky

[Logické funkce](er-functions-category-logical.md)

[Funkce VALUEINLARGE](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]