---
title: Seznam funkcí ER v logické kategorii
description: Toto téma obsahuje informace o logických funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686173"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Seznam funkcí ER v logické kategorii

[!include [banner](../includes/banner.md)]

Logické funkce elektronického výkaznictví (ER) lze použít pro práci s logickými hodnotami k provádění více než jednoho porovnání v jednom výrazu nebo při testování více podmínek. Toto téma obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [A](er-functions-logical-and.md)                       | Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud jsou splněny všechny zadané podmínky. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [Pevný obal](er-functions-logical-case.md)                     | Tato funkce vyhodnotí hodnotu zadaného výrazu podle zadaných alternativních možností a vrátí výsledek první možnosti, která se rovná hodnotě zadaného výrazu. V opačném případě vrátí volitelný výchozí výsledek, pokud je výchozí výsledek zadán jako poslední argument volané funkce, jemuž nepředchází nějaká možnost. Vrácená hodnota může být libovolného podporovaného datového typu. |
| [Jestliže](er-functions-logical-if.md)                         | Při splnění dané podmínky vrátí tato funkce první zadanou hodnotu. V opačném případě vrátí druhou zadanou hodnotu. Vrácená hodnota může být libovolného podporovaného datového typu. |
| [Ne](er-functions-logical-not.md)                       | Tato funkce vrací stornovanou logickou hodnotu zadané podmínky jako *logickou* hodnotu. |
| [Or](er-functions-logical-or.md)                         | Tato funkce vrátí *logickou* hodnotu **NEPRAVDA**, pokud nejsou splněny všechny zadané podmínky. Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka. |
| [ValueIn](er-functions-logical-valuein.md)               | Tato funkce určuje, zda uvedený vstup odpovídá jakékoli hodnotě zadané položky v zadaném seznamu. Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Tato funkce určuje, zda uvedený vstup typu *Int64* nebo *Integer* odpovídá jakékoli hodnotě zadané položky v zadaném seznamu. Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |


## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]