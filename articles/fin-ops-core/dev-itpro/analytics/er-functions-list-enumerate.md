---
title: Funkce el. výkaznictví ENUMERATE
description: Toto téma obsahuje obecné informace o použití funkce ENUMERATE elektronického výkaznictví.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34ebbec94644276be4ef9beb1c77638606dd37a0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679455"
---
# <a name="enumerate-er-function"></a>Funkce el. výkaznictví ENUMERATE

[!include [banner](../includes/banner.md)]

Funkce `ENUMERATE` vrátí novou hodnotu typu *seznam záznamů*, která obsahuje výčtové záznamy zadaného seznamu.

## <a name="syntax"></a>Syntaxe

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Vrácený seznam výčtových záznamů dávek obsahuje následující dodatečné prvky:

- Záznam polí (součást **Value**)
- Aktuální index záznamů (součást **Number**)

## <a name="example"></a>Příklad

Na následujícím obrázku je zdroj dat **Enumerated** vytvořen jako výčtový seznam záznamů dodavatelů ze zdroje dat **Vendors**, který odkazuje na tabulku VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Následující ilustrace znázorňuje formát elektronického vykazování (ER). V tomto formátu jsou vytvořeny vazby za účelem vygenerování výstupu ve formátu XML. Tento výstup představuje jednotlivé dodavatel jako výčtové uzly.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]