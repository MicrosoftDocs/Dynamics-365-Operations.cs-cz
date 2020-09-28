---
title: Funkce elektronického výkaznictví QRCODE
description: Toto téma obsahuje obecné informace o použití funkce QRCODE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: f634976d83fb4066a953b7ab09c963214415e29b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743751"
---
# <a name="qrcode-er-function"></a>Funkce elektronického výkaznictví QRCODE

[!include [banner](../includes/banner.md)]

Funkce `QRCODE` vrátí hodnotu typu *kontejner*, která představuje kód rychlé odezvy (QR kód) pro zadaný řetězec v binárním formátu.

## <a name="syntax"></a>Syntaxe

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje původní text.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner*

Výsledný binární datový proud.

## <a name="example"></a>Příklad

Můžete nakonfigurovat formát elektronického výkaznictví (ER) pro vygenerování odchozího dokumentu ve formátu Microsoft Office (sešity aplikace Excel nebo dokumenty aplikace Word) pomocí předdefinované šablony. Tato šablona může obsahovat objekt **obrázku** (sešit aplikace Excel) nebo **ovládací prvek obsahu obrázku** (dokument aplikace Word) jako zástupný symbol pro obrázek kódu QR. Do nakonfigurovaného formátu ER je třeba přidat prvek **buňky**, který se použije k vyplnění tohoto zástupného symbolu. Chcete-li určit, jaké informace budou uloženy v kódu QR, musíte definovat vazbu pro tento prvek **buňky**. Můžete například nakonfigurovat vazbu obsahující následující výraz:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Když spustíte konfigurovaný formát ER, textová hodnota pole **LabelText** ve zdroji dat **model.ListOfShelfLabels** bude použita ke generování obrázku kódu QR. Tento obrázek nahradí zástupný symbol obrázku kódu QR v šabloně dokumentu použité ke generování odchozího dokumentu. Když je obrázek vygenerovaného dokumentu naskenován, vrátí text, který byl převzat z pole **LabelText** ve zdroji dat **model.ListOfShelfLabels**. Další informace viz [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
