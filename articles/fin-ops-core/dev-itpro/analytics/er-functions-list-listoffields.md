---
title: Funkce elektronického výkaznictví LISTOFFIELDS
description: Toto téma obsahuje obecné informace o použití funkce LISTOFFIELDS elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1d15649aed4343f2ed9192834047a17e273e29f190aa83c386bebe7857b47908
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761481"
---
# <a name="listoffields-er-function"></a>Funkce elektronického výkaznictví LISTOFFIELDS

[!include [banner](../includes/banner.md)]

Funkce `LISTOFFIELDS` vrátí hodnotu typu *seznam záznamů*, která je vytvořena na základě struktury zadaného argumentu typu *výčet* nebo *kontejner (záznam)*.

## <a name="syntax-1"></a>Syntaxe 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumenty

`path`: odkaz na zdroj dat

Platná cesta odkazu na zdroj dat jednoho z následujících datových typů:

- Výčet modelu
- Výčet formátu
- Výčet aplikací
- Kontejner (záznam)

`language`: *řetězec*

Text, který představuje kód jazyka.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Vytvořený seznam obsahuje záznamy, které mají následující pole:

- **Name** (datový typ *řetezec*)
- **Label** (datový typ *řetezec*)
- **Description** (datový typ *řetezec*)
- **IsTranslated** (*logický* datový typ)

Pokud argument `path` odkazuje na zdroj dat typu *kontejner (záznam)*, pro každé pole odkazovaného záznamu kontejneru je do vytvořeného seznamu přidán nový záznam. Pro každý vytvořený záznam vrátí pole **Name** název pole odkazovaného záznamu kontejneru, pro který byl aktuální záznam vytvořen.

Pokud argument `path` odkazuje na zdroj dat jednoho z typů *výčet*, pro každou hodnotu výčtu odkazovaného výčtu je do vytvořeného seznamu přidán nový záznam. Pro každý vytvořený záznam vrátí pole **Name** hodnotu odkazovaného výčtu, pro který byl vytvořen aktuální záznam, pole **Description** vrátí popis tohoto výčtu a pole **Label** vrátí popisek tohoto výčtu.

V době běhu je při použití syntaxe 1 nutné, aby pole **Label** a **Description** vrátila hodnoty, které jsou založeny na jazykovém nastavení formátu spuštěného elektronického vykazování (ER):

- Jsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na daném jazyku, a pole **IsTranslated** vrátí hodnotu **True**.
- Nejsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na výchozím jazyku **EN-US**, a pole **IsTranslated** vrátí hodnotu **False**.

V době běhu je při použití syntaxe 2 nutné, aby pole **Label** a **Description** vrátila hodnoty, které jsou založeny na jazyku, který je definován jako druhý argument volané funkce:

- Jsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na daném jazyku, a pole **IsTranslated** vrátí hodnotu **True**.
- Nejsou-li k dispozici popisky a popisy požadovaného jazyka, vrátí pole **Label** a **Description** hodnoty, které jsou založeny na jazyku **EN-US**, a pole **IsTranslated** vrátí hodnotu **False**.

## <a name="example-1"></a>Příklad 1

Na následujícím obrázku je výčet uveden v datovém modelu elektronického vykazování.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Následující obrázek znázorňuje tyto podrobnosti:

- Výčet modelů je vložen do sestavy jako zdroj dat.
- Výraz elektronického výkaznictví používá výčet modelů jako parametr funkce `LISTOFFIELDS`.
- Zdroj dat typu *seznamu záznamů* je vložen do sestavy pomocí vytvořeného výrazu elektronického výkaznictví.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Následující příklad uvádí prvky formátu ER, které jsou vázané na zdroj dat typu *seznamu záznamů*, který byl vytvořen pomocí funkce `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Přeložený text popisků a popisů je zadáván do výstupu formátu elektronického výkaznictví na základě nastavení jazyka nadřazených prvků formátu **FILE** a **FOLDER**.

## <a name="example-2"></a>Příklad 2

Typ datového zdroje *Vypočítané pole* použijete ke konfiguraci zdrojů dat **enumType\_de** a **enumType\_deCH** pro výčet datových modelů **enumType**:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

V takovém případě můžete použít následující výraz k získání popisku hodnoty výčtu ve švýcarské němčině, pokud je tento překlad k dispozici. Není-li k dispozici překlad do švýcarské němčiny, je popisek v němčině.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]