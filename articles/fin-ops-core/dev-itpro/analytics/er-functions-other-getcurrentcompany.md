---
title: Funkce el. výkaznictví GETCURRENTCOMPANY
description: Toto téma obsahuje obecné informace o použití funkce GETCURRENTCOMPANY elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744112"
---
# <a name="getcurrentcompany-er-function"></a>Funkce el. výkaznictví GETCURRENTCOMPANY

[!include [banner](../includes/banner.md)]

Funkce `GETCURRENTCOMPANY` vrátí hodnotu typu *řetězec*, která představuje kód právnické osoby (společnosti), ke které je uživatel momentálně přihlášen.

## <a name="syntax"></a>Syntaxe

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`GETCURRENTCOMPANY ()` vrátí hodnotu **USMF** u uživatele přihlášeného ke společnosti **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)
