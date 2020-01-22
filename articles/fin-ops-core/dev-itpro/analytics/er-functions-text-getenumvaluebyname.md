---
title: Funkce el. výkaznictví GETENUMVALUEBYNAME
description: Toto téma obsahuje obecné informace o použití funkce GETENUMVALUEBYNAME elektronického výkaznictví.
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916837"
---
# <a name="GETENUMVALUEBYNAME">Funkce el. výkaznictví GETENUMVALUEBYNAME</a>

[!include [banner](../includes/banner.md)]

Funkce `GETENUMVALUEBYNAME` vyhledá určitou hodnotu typu *výčet* v zadaném zdroji dat výčtu pomocí názvu výčtu, který je zadán jako hodnota typu *řetězec*. Pokud je nalezena hodnota *výčet*, funkce ji vrátí. V opačném případě funkce vrátí hodnotu výčtu **null**.

## <a name="syntax"></a>Syntaxe

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenty

`enumeration data source path`: *výčet*

Platná cesta zdroje dat jednoho z následujících typů výčtu:

- Výčet modelů elektronického výkaznictví
- Výčet formátu elektronického výkaznictví
- Výčet Microsoft Dynamics 365 Finance

`enumeration value text`: *řetězec*

Hodnota typu řetězec, která představuje název jedné hodnoty výčtu.

## <a name="return-values"></a>Vrácené hodnoty

Hodnota typu *výčet* s možností nabytí hodnoty Null

Výsledná výčtová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Není vyvolána žádná výjimka, pokud není nalezena hodnota typu *výčet* za použití názvu výčtové hodnoty, která je zadána jako hodnota typu *řetězec*.

## <a name="example"></a>Příklad

Na následujícím obrázku je výčet **ReportDirection** uveden v datovém modelu. Všimněte si, že pro výčtové hodnoty jsou definovány popisky.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Následující obrázek znázorňuje tyto podrobnosti:

- Zdroj dat **$Direction** je konfigurován v sestavě elektronického výkaznictví. Tento zdroj dat je konfigurován na základě výčtu modelu **ReportDirection**.
- Výraz `$IsArrivals` je určený k použití zdroje dat **$Direction** výčtu modelů jako parametr této funkce.
- Hodnota tohoto porovnávacího výrazu je **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
