---
title: Funkce el. výkaznictví DATETIMEFORMAT
description: Toto téma obsahuje obecné informace o použití funkce DATETIMEFORMAT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 98919f40751a77465ae26acbd46af4396c588b13
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916400"
---
# <a name="DATETIMEFORMAT">Funkce el. výkaznictví DATETIMEFORMAT</a>

[!include [banner](../includes/banner.md)]

Funkce `DATETIMEFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadanou hodnotu data/času jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaxe 1

```
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Syntaxe 2

```
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumenty

`datetime`: *datum a čas*

Hodnota data/času, která představuje datum a čas pro zformátování.

`format`: *řetězec*

Formát výstupního řetězce.

`culture`: *řetězec*

Jazyková verze, která má být použita pro formátování.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná hodnota řetězce.

## <a name="usage-notes"></a>Poznámky k použití

Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání. Například, pokud je funkce `DATETIMEFORMAT` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze. Výchozí hodnota `culture` je **EN-US**.

Když funkce `DATETIMEFORMAT` převádí zadanou hodnotu data/času, bere v potaz nastavení časového pásma uživatele aplikace, který používá formát elektronického výkaznictví, v jehož kontextu je funkce volána.

## <a name="example-1"></a>Příklad 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` vrátí aktuální datum/čas aplikačního serveru, například 24. prosince 2015 jako **"24-12-2015"** na základě zadaného vlastního formátu.

## <a name="example-2"></a>Příklad 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` vrátí aktuální datum a čas relace aplikace, 24. prosince 2015, jako **"24.12.2015"** na základě vybrané německé jazykové verze a zadaného formátu.

## <a name="example-3"></a>Příklad 3

Funkce `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` vrátí řetězcovou hodnotu **2019-11-12T 08:00:00.0000000-08:00**, pokud je volána během procesu, který byl iniciován uživatelem aplikace, který má hodnotu časového pásma **(GMT-08:00) Tichomoří (USA a Kanada)** v sekci **Předvolby jazyka a země/oblasti**.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)
