---
title: Seznam funkcí ER v logické kategorii
description: Tento článek obsahuje informace o logických funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 02/11/2021
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
ms.openlocfilehash: 2361fa0df3fe60813e75c772134299ad948f3582
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888184"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Seznam funkcí ER v logické kategorii

[!include [banner](../includes/banner.md)]

Logické funkce elektronického výkaznictví (ER) lze použít pro práci s logickými hodnotami k provádění více než jednoho porovnání v jednom výrazu nebo při testování více podmínek. Tento článek obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [A](er-functions-logical-and.md)                       | Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud jsou splněny všechny zadané podmínky. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [Pevný obal](er-functions-logical-case.md)                     | Tato funkce vyhodnotí hodnotu zadaného výrazu podle zadaných alternativních možností a vrátí výsledek první možnosti, která se rovná hodnotě zadaného výrazu. V opačném případě vrátí volitelný výchozí výsledek, pokud je výchozí výsledek zadán jako poslední argument volané funkce, jemuž nepředchází nějaká možnost. Vrácená hodnota může být libovolného podporovaného datového typu. |
| [Obsahuje](er-functions-logical-contains.md)             | Tato funkce určuje, zda zadaný vstup obsahuje zadaný text. Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup obsahuje zadaný text. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [EndsWith](er-functions-logical-endswith.md)             | Tato funkce určuje, zda zadaný vstup končí zadaným textem. Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup končí zadaným textem. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [Jestliže](er-functions-logical-if.md)                         | Při splnění dané podmínky vrátí tato funkce první zadanou hodnotu. V opačném případě vrátí druhou zadanou hodnotu. Vrácená hodnota může být libovolného podporovaného datového typu. |
| [Ne](er-functions-logical-not.md)                       | Tato funkce vrací stornovanou logickou hodnotu zadané podmínky jako *logickou* hodnotu. |
| [Or](er-functions-logical-or.md)                         | Tato funkce vrátí *logickou* hodnotu **NEPRAVDA**, pokud nejsou splněny všechny zadané podmínky. Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka. |
| [StartsWith](er-functions-logical-startswith.md)         | Tato funkce určuje, zda zadaný vstup začíná zadaným textem. Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup začíná zadaným textem. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [ValueIn](er-functions-logical-valuein.md)               | Tato funkce určuje, zda uvedený vstup odpovídá jakékoli hodnotě zadané položky v zadaném seznamu. Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Tato funkce určuje, zda uvedený vstup typu *Int64* nebo *Integer* odpovídá jakékoli hodnotě zadané položky v zadaném seznamu. Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |


## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]