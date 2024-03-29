---
title: Funkce el. výkaznictví FORMAT
description: Tento článek obsahuje obecné informace o použití funkce FORMAT elektronického výkaznictví.
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
ms.openlocfilehash: a7eb3d4a4c72e8faf40d28a724cda5ba7d7e8a47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285992"
---
# <a name="format-er-function"></a>Funkce el. výkaznictví FORMAT

[!include [banner](../includes/banner.md)]

Funkce `FORMAT` vrátí zadaný řetězec jako hodnotu typu *řetězec* po jeho zformátování nahrazením všech výskytů **%N** *n*-tým argumentem.

## <a name="syntax"></a>Syntaxe

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumenty

`string`: *řetězec*

Odkaz na zdroj dat typu *řetězec*, který má být formátován. Tento argument je povinný.

`argument 1`: *řetězec*

První argument, který se použije k nahrazení výskytů **%1**. Tento argument je povinný.

`argument N`: *řetězec*

*N*-tý argument, který se použije k nahrazení výskytů **%2**, **%3** atd. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Pokud pro parametr není zadán argument, parametr je vrácen jako **"%N"** v řetězci. Co se týká hodnot typu *reálné číslo*, výchozí převod řetězce je omezen na dvě desetinná místa.

## <a name="example"></a>Příklad

Na následujícím obrázku vrátí zdroj dat **PaymentModel** (platební model) seznam záznamů zákazníků pomocí součásti **Customer** (odběratel). Vrátí hodnotu data zpracování pomocí pole **ProcessingDate** (datum zpracování).

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Ve formátu elektronického výkaznictví, který je určený ke generování elektronického souboru pro vybrané odběratele, je vybrán řetězec **PaymentModel** jako zdroj dat, který řídí tok procesu. Jestliže je vybraný odběratel zastaven k datu zpracování sestavy, je vyvolána výjimka pro informování uživatele. Vzorec, který je určen pro tento typ ovládacího prvku pro zpracování, může využít následující zdroje:

- Popisek SYS70894, který má následující text:

    - **U jazyka EN-US:** "Nothing to print"
    - **U jazyka DE:** "Nichts zu drucken"

- Popisek SYS18389, který má následující text:

    - **U jazyka EN-US**: "Customer %1 is stopped for %2."
    - **U jazyka DE**: "Debitor '%1' wird für %2 gesperrt."

Zde je výraz, který lze vytvořit.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Pokud je sestava zpracovávána pro odběratele **Litware Retail** 17. prosince 2015, v národním prostředí **EN-US** a jazyce **EN-US**, tento vzorec vrátí následující text, který může být uživateli nabídnut ve formě zprávy výjimky:

*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*

Jestliže je stejná sestava zpracována pro odběratele **Litware Retail** 17. prosince 2015 v jazykové verzi **DE** a jazyce **DE**, vzorec vrátí následující text, který používá jiný formát data:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Následující syntaxe je použita ve vzorcích elektronického výkaznictví pro popisky:
>
> - **Popisky ze zdrojů aplikace Microsoft Dynamics 365 Finance:** **\@X**, kde **X** je ID popisku ve stromu aplikačních objektů (AOT)
> - **Popisky, které se nachází v konfiguracích elektronického výkaznictví:** **@"GER_LABEL:X"**, kde **X** je ID popisku v konfiguraci elektronického výkaznictví.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
