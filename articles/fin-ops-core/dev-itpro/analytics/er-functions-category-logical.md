---
title: Seznam funkcí ER v logické kategorii
description: Tento článek obsahuje informace o logických funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291287"
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
