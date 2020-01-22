---
title: Funkce el. výkaznictví DATETODATETIME
description: Toto téma obsahuje obecné informace o použití funkce DATETODATETIME elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916377"
---
# <a name="DATETODATETIME">Funkce el. výkaznictví DATETODATETIME</a>

[!include [banner](../includes/banner.md)]

Funkce `DATETODATETIME` vrátí hodnotu typu *datum a čas*, která je převedena ze zadané hodnoty kalendářního data na hodnotu data a času ve koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxe

```
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
