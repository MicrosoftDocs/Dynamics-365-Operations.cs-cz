---
title: Funkce el. výkaznictví NUMSEQVALUE
description: Toto téma obsahuje obecné informace o použití funkce NUMSEQVALUE elektronického výkaznictví.
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
ms.openlocfilehash: 53040d1f4b3c8089fab264a524309df909a90ed5e617bd86658704b286fabb34
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758233"
---
# <a name="numseqvalue-er-function"></a>Funkce el. výkaznictví NUMSEQVALUE

[!include [banner](../includes/banner.md)]

Funkce `NUMSEQVALUE` vrátí *řetězcovou* hodnotu, která představuje novou vygenerovanou hodnotu číselné řady založenou na zadané číselné řadě, rozsahu a ID oboru. ID oboru se rovná kódu společnosti, který je poskytnut v kontextu, ve kterém je spuštěn formát elektronického vykazování (ER).

## <a name="syntax-1"></a>Syntaxe 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Syntaxe 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumenty

`number sequence code`: *řetězec*

Textová hodnota, která představuje kód číselné řady, ve které je požadována nová hodnota.

`number sequence record ID`: *Int64*

Hodnota *Int64*, která představuje ID záznamu v tabulce NumberSequenceTable, která obsahuje definici číselné řady, ve které je požadována nová hodnota.

`scope type`: *hodnota výčtu*

Hodnota výčtu **ERExpressionNumberSequenceScopeType**, která definuje obor číselné řady, ve které je požadována nová hodnota. Dostupné typy oborů jsou **Sdílený**, **Právnická osoba** a **Společnosti**

`scope ID`: *řetězec*

Hodnota typu *řetězec* identifikující obor na základě zadaného typu oboru.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Pro typ oboru **Sdílený** zadejte prázdný řetězec jako ID oboru.

Pro typy oborů **Společnost** a **Právnická osoba** zadejte kód společnosti jako ID oboru. Pokud pro tyto typy oborů zadáte prázdný řetězec, použije se aktuální kód společnosti.

Při použití syntaxe 1 je požadována číselná řada pro typ oboru **Společnost** a kód společnosti je poskytnut v kontextu, ve kterém je spuštěn formát elektronického výkaznictví.

## <a name="example-1"></a>Příklad 1

Ve vašem formátu elektronického výkaznictví definujete zdroj dat **AskNumSeq** pro typ *parametru vstupu uživatele*. Tento zdroj dat odkazuje na rozšířený datový typ (EDT) **popis**. Dále definujete zdroj dat **NumSeq** typu *vypočítané pole*. Tento zdroj dat obsahuje výraz `NUMSEQVALUE (AskNumSeq)`. Když je zavolán zdroj dat **NumSeq**, vrátí novou vygenerovanou hodnotu číselné řady, která byla zadána v době běhu zadáním jeho kódu do dialogového okna. Číselná řada je požadována pro typ oboru **Společnost**. Kód společnosti je poskytnut v kontextu, ve kterém je spuštěn formát elektronického výkaznictví.

## <a name="example-2"></a>Příklad 2

V mapování modelu jsou definovány následující zdroje dat:

- Zdroj dat **LedgerParms** typu *tabulka*. Tento zdroj dat odkazuje na tabulku LedgerParameters.
- Zdroj dat **NumSeq** typu *vypočítané pole*. Tento zdroj dat obsahuje výraz `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Když je volán datový zdroj **NumSeq**, vrátí novou vygenerovanou hodnotu číselné řady, která byla nakonfigurována v parametrech hlavní knihy pro společnost poskytující kontext, pod kterým běží formát elektronického výkaznictví. Tato číselná řada jedinečně identifikuje deníky a chová se jako číslo dávky propojující transakce dohromady.

## <a name="example-3"></a>Příklad 3

V mapování modelu jsou definovány následující zdroje dat:

- Zdroj dat **enumScope** pro typ *výčet* aplikace Microsoft Dynamics 365 Finance. Tento zdroj dat odkazuje na výčet **ERExpressionNumberSequenceScopeType**.
- Zdroj dat **NumSeq** typu *vypočítané pole*. Tento zdroj dat obsahuje výraz `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Když je volán datový zdroj **NumSeq**, vrátí novou vygenerovanou hodnotu číselné řady **Gene\_1**, která byla nakonfigurována pro společnost poskytující kontext, pod kterým běží formát elektronického výkaznictví.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]