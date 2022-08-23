---
title: Funkce REPEAT ER
description: Tento článek obsahuje obecné informace o použití funkce REPEAT elektronického výkaznictví.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220685"
---
# <a name="repeat-er-function"></a>Funkce REPEAT ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funkce `REPEAT` vytvoří záznam, který obsahuje pole, které má hodnotu odpovídající zadanému vstupu. Poté vrátí nový *Seznam záznamů* záznamu, který se zadaný počet opakování opakuje.

## <a name="syntax"></a>Syntaxe

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumenty

`item`: Všechny podporované [primitivní](er-formula-supported-data-types-primitive.md) nebo [složené](er-formula-supported-data-types-composite.md) datové typy

Hodnota, která se má opakovat.

`number`: *celé číslo*

Počet opakování.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Vrácený seznam opakovaných záznamů dávek obsahuje následující pole:

- Zadaná hodnota (pole `Item`)
- Aktuální index záznamů (pole `Number`)

> [!NOTE]
> Protože se pro tuto funkci používá číslování založené na čísle 1, má pole `Number` hodnotu **1** pro první záznam výsledného seznamu.

Tuto funkci můžete použít k násobení existujících dat, abyste mohli provádět testování výkonu a objemu řešení [Elektronického vykazování (ER)](general-electronic-reporting.md) pomocí [Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Příklad

Chcete vygenerovat dokument ve formátu XML, který musí obsahovat tolik prvků XML `Party`, kolik určíte v poli pro zadávání dat v dialogovém okně za běhu, před zahájením provádění formátu ER.

Následující obrázek znázorňuje [formát](er-overview-components.md#format-component) ER. V tomto formátu je jeden prvek XML `Party` přidán k odhalení vlastností jedné strany.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Následující obrázek ukazuje následující nakonfigurované zdroje dat:

- Zdroj dat `Party`, který představuje jednu stranu. Pole `Party.Value` se používá k zobrazení jedné textové hodnoty.
- [Zdroj dat](er-user-input-parameter-data-sources.md) `NumberOfRepeats`, který se používá k nabídnutí pole pro zadávání dat v dialogovém okně za běhu, takže můžete určit počet stran, které by měly být zapsány do generovaného dokumentu.
- Zdroj dat `Party2`, který opakuje záznam `Party` tolikrát, kolikrát jste zadali ve zdroji dat `NumberOfRepeats`.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Další obrázek ukazuje datové vazby upravitelného formátu ER, které jsou vytvořeny pro generování výstupu ve formátu XML. Tento výstup představuje jednotlivé strany jako výčtové uzly.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Následující obrázek ukazuje výsledek při spuštění navrženého formátu a hodnotě zdroje dat `NumberOfRepeats` zadané jako **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
