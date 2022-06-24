---
title: Funkce el. výkaznictví JSONVALUE
description: Tento článek obsahuje obecné informace o použití funkce JSONVALUE elektronického výkaznictví.
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: 7deaed83959f033d11333efb5a2b398cbe57076d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909493"
---
# <a name="jsonvalue-er-function"></a>Funkce el. výkaznictví JSONVALUE

[!include [banner](../includes/banner.md)]

Funkce `JSONVALUE` analyzuje data ve formátu notace objektu JavaScript (JSON), který je dostupný v zadané cestě, a extrahuje skalární hodnotu se zadaným ID. Poté vrátí extrahovanou skalární hodnotu jako *řetězcovou* hodnotu.

## <a name="syntax"></a>Syntaxe

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec* obsahujícímu data JSON.

`path`: *řetězec*

Identifikátor skalární hodnoty dat JSON. K oddělení názvů souvisejících uzlů JSON použijte lomítko (/). Použijte zápis hranatých uvozovek (\[\]) k určení indexu konkrétní hodnoty v poli JSON. Všimněte si, že pro tento index se používá číslování založené na nule.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example-1"></a>Příklad 1

Zdroj dat **JsonField** obsahuje následující data ve formátu JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. V tomto případě výraz `JSONVALUE (JsonField, "BuildNumber")` vrátí následující hodnotu datového typu *řetězec*: **"7.3.1234.1"**.

## <a name="example-2"></a>Příklad 2

Zdroj dat **JsonField** typu *vypočítané pole* obsahuje následující výraz: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Tento výraz je nakonfigurován tak, aby vrátil hodnotu [*Řetězec*](er-formula-supported-data-types-primitive.md#string), která představuje následující data ve formátu JSON.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

V tomto případě výraz `JSONVALUE(json, "workers/[1]/emails/[0]")` vrátí následující hodnotu datového typu *řetězec*: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Další prostředky

[Textové funkce](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
