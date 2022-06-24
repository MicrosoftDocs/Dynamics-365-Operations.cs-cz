---
title: Funkce VALUEINLARGE elektronického výkaznictví
description: Tento článek obsahuje obecné informace o použití funkce VALUEINLARGE elektronického výkaznictví.
author: NickSelin
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 977c1cd7dac75781677461b288bc8e5e79d13e6f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888138"
---
# <a name="valueinlarge-er-function"></a>Funkce VALUEINLARGE elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Funkce `VALUEINLARGE` určuje, zda uvedený vstup typu *Int64* nebo *Integer* odpovídá jakékoli hodnotě zadané položky v zadaném seznamu. Tato funkce vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. Abyste pochopili rozdíl oproti funkci `VALUEIN`, viz sekce [Poznámka k použití](#usage_note) dále v tomto článku.

## <a name="syntax"></a>Syntaxe

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumenty

`input`: *pole*

Platná cesta k položce zdroje dat typu *Seznam záznamů*. Hodnota této položky bude spárována.

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`list item expression`: *výraz*

Platný podmíněný výraz, který buď odkazuje na nebo obsahuje jedno pole určeného seznamu, který by měl být použit pro párování.

## <a name="return-values"></a>Vrácené hodnoty

*Boolean*

Výsledná *logická hodnota*.

## <a name=""></a><a name="usage_note">Poznámky k použití</a>

Když zadaný vstup představuje typ *Int64* nebo *Integer* položky zdroje dat, jejíž volání lze přeložit na přímý příkaz SQL, zadaný seznam se převede na dočasnou tabulku SQL a párování se provede v databázi provedením jediného dotazu `EXISTS JOIN`. Jinak tato funkce funguje jako funkce [`VALUEIN`](er-functions-logical-valuein.md).

Když zadaný vstup představuje položku zdroje dat, která je navržena jako položka jiného typu než *Int64* a *Integer*, dojde v době návrhu k chybě informující o tom, že funkce `VALUEINLARGE` není použitelná pro nakonfigurovaný výraz elektronického výkaznictví.

Když je spušten výraz funkce `VALUEINLARGE` a v rámci tohoto spuštění je použita více než jedna dočasná tabulka, dojde k chybě běhu.

## <a name="example"></a>Příklad

Definujte v mapování modelu následující zdroje dat:

- Zdroj dat **In** typu *záznamy tabulky*.
    - Tento zdroj dat odkazuje na tabulku **Intrastat**.
    - Možnost **Mezi společnostmi** je nastavena na **Ne**.
- Zdroj dat **InMemory** typu *vypočítané pole*.
    - Tento zdroj dat obsahuje výraz `WHERE (In, In.Port <> "")`.
- Zdroj dat **InFiltered** typu *vypočítané pole*.
    - Tento zdroj dat obsahuje výraz `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Když se zdroj dat **InFiltered** nazývá v kontextu společnosti **DEMF**, v databázi aplikace se vytvoří nová dočasná tabulka, do této tabulky se vloží seznam identifikačních kódů záznamů shromážděných v paměti a vygeneruje se následující příkaz SQL, který vrátí filtrované záznamy v tabulce **Intrastat**.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Další prostředky

[Logické funkce](er-functions-category-logical.md)

[Funkce VALUEIN](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]