---
title: Seznam funkcí ER v kategorii konkrétní pro obchodní domény
description: Tento článek obsahuje informace o funkcích konkrétní pro obchodní domény, které jsou podporovány v elektronickém výkaznictví (ER).
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b1ac46cf10d57b40af1fa99021156ad97a17ba20
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272675"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Seznam funkcí ER v kategorii konkrétní pro obchodní domény

[!include [banner](../includes/banner.md)]

Funkce konkrétní pro domény elektronického výkaznictví lze používat k provádění výpočtů a požadavků na přístup k datům, které jsou specifické pro implementaci produktu Microsoft Dynamics 365 Finance. Tento článek obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce| Popis |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Tato funkce vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD10 na základě číslic zadaného čísla faktury. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje jedno ID dimenze financí, které je převzato ze zadaného řetězce. Zadaný řetězec představuje všechny dimenze jako seznam ID oddělených čárkami. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Tato funkce vrací hodnotu typu *reálné číslo*, které představuje výsledek pro převedení zadané peněžní částky ze zadané zdrojové měny na zadanou cílovou měnu za použití nastavení zadané společnosti k zadanému datu. |
| [CurCredRef](er-functions-other-curcredref.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje referenční údaj věřitele na základě číslic zadaného čísla faktury. |
| [FA_Balance](er-functions-other-fabalance.md) | Tato funkce vrací hodnotu typu *kontejner (záznam)*, která se skládá z dat pro zůstatek dlouhodobého majetku pro zadanou položku dlouhodobého majetku, vykazovaný rok a datum vykazování. |
| [FA_Sum](er-functions-other-fasum.md) | Tato funkce vrací hodnotu typu *kontejner (záznam)*, která se skládá z dat pro částky dlouhodobého majetku pro zadanou položku dlouhodobého majetku, kód oceňovacího modelu a rozsah kalendářních dat. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje kód právnické osoby (společnosti), ke které je uživatel momentálně přihlášen. |
| [ISOCredRef](er-functions-other-isocredref.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje ISO údaj věřitele na základě číslic a abecedních symbolů zadaného čísla faktury. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Tato funkce vrací *logickou hodnotu* **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN). V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [Mod_97](er-functions-other-mod97.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD97 na základě číslic zadaného čísla faktury. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje novou vygenerovanou hodnotu číselné řady založenou na zadané číselné řadě, rozsahu a ID oboru. ID oboru se rovná kódu společnosti, který je poskytnut v kontextu, ve kterém je spuštěn formát elektronického výkaznictví (ER). |
| [RoundAmount](er-functions-other-roundamount.md) | Tato funkce vrací hodnotu typu *reálné číslo*, která představuje výsledek zaokrouhlení zadaného množství na zadaný počet dedetinných míst podle zadaného pravidla zaokrouhlení. |
| [TableName2ID](er-functions-other-tablename2id.md) | Tato funkce vrací číselnou reprezentaci ID tabulky pro zadaný název tabulky jako *celočíselnou* hodnotu. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
