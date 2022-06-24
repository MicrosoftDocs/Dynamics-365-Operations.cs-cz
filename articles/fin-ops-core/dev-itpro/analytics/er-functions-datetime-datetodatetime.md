---
title: Funkce el. výkaznictví DATETODATETIME
description: Tento článek obsahuje obecné informace o použití funkce DATETODATETIME elektronického výkaznictví.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: ba80c4c3eac703ba96a4f2741fcc19bceeb24ed0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898484"
---
# <a name="datetodatetime-er-function"></a>Funkce el. výkaznictví DATETODATETIME

[!include [banner](../includes/banner.md)]

Funkce `DATETODATETIME` vrátí hodnotu typu *datum a čas*, která je převedena ze zadané hodnoty kalendářního data na hodnotu data a času ve koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxe

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenty

`date`: *datum*

Hodnota data, která představuje datum pro převedení.

## <a name="return-values"></a>Vrácené hodnoty

*Datum a čas*

Výsledná hodnota data a času.

## <a name="example-1"></a>Příklad 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` vrátí datum aktuální relace Microsoft Dynamics 365 Finance, 24. prosince 2015, **12/24/2015 12:00:00 AM**. V tomto příkladu **CompInfo** představuje zdroj dat elektronického výkaznictví typu **Finance and Operations/Table** a odkazuje na tabulku CompanyInfo.

## <a name="example-2"></a>Příklad 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` vrátí hodnotu typu datum/čas **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]