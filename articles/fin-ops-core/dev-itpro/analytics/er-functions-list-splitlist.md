---
title: Funkce elektronického výkaznictví SPLITLIST
description: Toto téma obsahuje obecné informace o použití funkce SPLITLIST elektronického výkaznictví.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: ef0b548173a01cc5a15fcfb743dfb29397c1349b3c2926fa6401399459d07026
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776115"
---
# <a name="splitlist-er-function"></a>Funkce elektronického výkaznictví SPLITLIST

[!include [banner](../includes/banner.md)]

Funkce `SPLITLIST` rozdělí zadaný seznam na podseznamy (neboli dávky), přičemž každá z nich obsahuje zadaný počet záznamů. Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.

## <a name="syntax-1"></a>Syntaxe 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`number`: *celé číslo*

Maximální počet zobrazených záznamů na dávku.

`on-demand reading flag`: *logická hodnota*

*Booleovská* hodnota určující, zda mají být prvky dílčích seznamů generovány na vyžádání.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Vrácený seznam dávek obsahuje následující prvky:

 - **Value:** *seznam*

    Seznam záznamů, které patří do aktuální dávky.

- **BatchNumber:** *celé číslo*

    Číslo aktuální dávky ve vráceném seznamu.

Když je příznak čtení na vyžádání nastaven na **Pravda**, dílčí seznamy jsou generovány na vyžádání, což umožňuje snížit spotřebu paměti, ale může dojít k pomalejšímu zpracování, pokud se prvky nepoužívají postupně.

## <a name="example"></a>Příklad

V následujícím příkladu je datový zdroj **Řádky** vytvořen jako seznam záznamů se třemi záznamy. Tento seznam je rozdělen do dávek, z nichž každá obsahuje až dva záznamy.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Následující obrázek znázorňuje navržené rozvržení formátu. V tomto rozvržení formátu jsou vytvořeny vazby na datový zdroj **Řádky** za účelem vygenerování výstupu ve formátu XML. Tento výstup představuje jednotlivé uzly pro každou dávku a záznamy v ní.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
