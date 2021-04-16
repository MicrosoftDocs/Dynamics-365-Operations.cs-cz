---
title: Seznam funkcí ER v kategorii seznamu
description: Toto téma obsahuje informace o funkcích seznamu, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
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
ms.openlocfilehash: 9adc8c40926864ab86421a38c3a135d837391b40
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749458"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Seznam funkcí ER v kategorii seznamu

[!include [banner](../includes/banner.md)]

Funkce seznamu elektronického výkaznictví (ER) lze používat k extrahování informací ze zdrojů dat a provádění operací se zdroji dat datových typů *Seznam záznamů* a *Kontejner (záznam)*. Toto téma obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Tato funkce je spuštěná jako výběr v paměti. Vrátí novou sloučenou hodnotu typu *seznam záznamů*, která sestává ze seznamu záznamů představujících všechny položky, které odpovídají zadané cestě. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Tato funkce je spuštěna jako připojený dotaz SQL. Vrátí novou sloučenou hodnotu typu *seznam záznamů*, která sestává ze seznamu záznamů představujících všechny položky, které odpovídají zadané cestě. |
| [Počet](er-functions-list-count.md)                       | Tato funkce vrací hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný. Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula). |
| [EmptyList](er-functions-list-emptylist.md)               | Tato funkce vrací prázdnou hodnotu typu *seznam záznamů* s použitím zadaného seznamu jako zdroje pro strukturu seznamu.|
| [Výčet](er-functions-list-enumerate.md)               | Tato funkce vrací novou hodnotu typu *seznam záznamů*, která obsahuje výčtové záznamy zadaného seznamu. |
| [Filtr](er-functions-list-filter.md)                     | Tato funkce vrací zadaný seznam jako hodnotu typu *seznam záznamů* po změně dotazu, který jej filtruje podle zadané podmínky. |
| [První](er-functions-list-first.md)                       | Tato funkce vrací první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný. Pokud je seznam prázdný, vyvolá tato funkce výjimku. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Tato funkce vrací první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento záznam není prázdný. Je-li záznam prázdný, vrátí tato funkce hodnotu typu *kontejner (záznam)* s hodnotou null. |
| [Index](er-functions-list-index.md)                       | Tato funkce vrací hodnotu typu *kontejner (záznam)*, která je vybrána pomocí zadaného číselného indexu v zadaném seznamu. Pokud je index mimo rozsah záznamů v zadaném seznamu, vyvolá tato funkce výjimku. |
| [IsEmpty](er-functions-list-isempty.md)                   | Tato funkce vrací *logickou hodnotu* **TRUE**, pokud zadaný seznam neobsahuje žádné záznamy. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**. |
| [Seznam](er-functions-list-list.md)                         | Tato funkce vrací hodnotu typu *seznam záznamů*, která se skládá z nového seznamu záznamů vytvořeného ze zadaných argumentů.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Tato funkce vypočítá zadaný výraz jako selektor pro každý záznam zadaného seznamu. Vrací novou hodnotu *Seznam záznamů*, která obsahuje jeden záznam pro každou jedinečnou hodnotu selektoru.|
| [ListJoin](er-functions-list-listjoin.md)                 | Tato funkce vrací hodnotu typu *seznam záznamů*, která představuje nový spojený seznam záznamů vytvořený ze zadaných argumentů.|
| [ListOfFields](er-functions-list-listoffields.md)         | Tato funkce vrací hodnotu typu *seznam záznamů*, která je vytvořena na základě struktury zadaného argumentu typu *výčet* nebo *kontejner (záznam)*. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Tato funkce vrací hodnotu typu *seznam záznamů*, která obsahuje pouze první záznam zadaného seznamu.|
| [OrderBy](er-functions-list-orderby.md)                   | Tato funkce vrací vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl seřazen podle zadaných argumentů. Tyto argumenty lze definovat jako výrazy. |
| [Stornovat](er-functions-list-reverse.md)                   | Tato funkce vrací zadaný seznam jako hodnotu typu *seznam záznamů* v obráceném pořadí. |
| [Rozdělit](er-functions-list-split.md)                       | Tato funkce rozdělí zadaný vstupní řetězec do podřetězců a vrátí výsledek jako novou hodnotu typu *seznam záznamů*. |
| [SplitList](er-functions-list-splitlist.md)               | Tato funkce rozdělí zadaný seznam na podseznamy (neboli dávky), přičemž každá z nich obsahuje zadaný počet záznamů. Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Tato funkce rozdělí zadaný seznam na nový seznam dílčích seznamů (dávek). Počet záznamů v každé dávce se dynamicky vypočítává. Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek. |
| [StringJoin](er-functions-list-stringjoin.md)             | Tato funkce vrací hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadaného seznamu. Hodnoty mohou být odděleny určeným oddělovačem. |
| [Kde](er-functions-list-where.md)                       | Tato funkce vrací zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl filtrován podle zadané podmínky. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]