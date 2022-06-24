---
title: Funkce el. výkaznictví GETCURRENTCOMPANY
description: Tento článek obsahuje obecné informace o použití funkce GETCURRENTCOMPANY elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 06d552a0e8241d416fc49c4377b02f90fdf63d29
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872735"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]