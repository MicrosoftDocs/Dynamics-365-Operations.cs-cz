---
title: Podporované typy složených dat pro vzorce elektronického výkaznictví
description: Toto téma obsahuje informace o typech složených dat, které jsou podporovány ve vzorcích elektronického výkaznictví (ER).
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf7178888e39a5f26ae92e77df9c996374b76bf3
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323658"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Podporované typy složených dat pro vzorce elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o typech složených dat, které jsou podporovány ve výrazech [elektronického výkaznictví (ER)](general-electronic-reporting.md). Složené datové typy jsou [třída](#class), [kontejner](#container), [záznam](#record), [seznam záznamů](#record-list) a [objekt](#object).

## <a name="class"></a><a name="class"></a>Třída

Datový typ *třída* odkazuje na veřejnou třídu aplikace. V ER je to reprezentováno jako [*záznam*](#record), který obsahuje samostatné pole pro každou veřejnou metodu odkazované třídy. Když je volání metody parametrizováno, musíte také určit požadované argumenty příslušných typů ve výrazu ER, který je nakonfigurován pro volání metody.

V komponentách mapování a formát ER můžete přidat zdroj dat **Třída**, který je uveden jako zdroj dat a který vrací hodnotu typu *třída*. Tento zdroj dat zpřístupňuje veřejné metody třídy, které lze volat za běhu.

> [!NOTE]
> Z výrazů ER lze volat pouze metody, které vracejí hodnotu.
>
> Z výrazů ER lze volat pouze metody, které mají rozsah od nuly do osmi argumentů.

Výchozí hodnota a *třídy* je **null**.

Následující obrázek ukazuje, jak zdroj dat **Systémové informace(xInfo)** typu **Třída** je přidán, aby se vytvořila instance třídy aplikací **xInfo** volala svoji metodu **productName()** pro získání názvu aktuální aplikace. Název aktuální aplikace se načte za běhu spuštěním vazby `xInfo.productName`, která byla nakonfigurována pro pole **Název softwaru(SoftwareName)** datového modelu ER. Tato vazba volá metodu `productName()` třídy aplikací **xInfo**, která je v aktuálním mapování modelu reprezentována jako zdroj dat **Systémové informace(xInfo)**.

[![Konfigurace zdroje dat třídy v návrháři mapování modelů ER.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Následující obrázek ukazuje, jak je formát ER nakonfigurován tak, aby poskytoval zadaný název aplikace do generovaných dokumentů. Pole **Název softwaru(SoftwareName)** použitého datového modelu bylo vázáno na komponentu **Řetězec**, která je vnořená pod prvek XML **softwareUsed** formátu ER. Takže název aktuální aplikace je umístěn za běhu do prvku XML **softwareUsed** vygenerovaného dokumentu ve formátu XML.

[![Konfigurace struktury elektronického odchozího dokumentu v návrháři formátů ER.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Kontejner

Datový typ *kontejner* obsahuje binární obsah. Hodnotu *kontejner* lze použít k předání konkrétních informací z úložiště do generovaného dokumentu. V rámci ER se tento datový typ často používá k vložení mediálního obsahu, jako je logo společnosti, do generovaných dokumentů.

> [!NOTE]
> Ačkoli každou položku média lze reprezentovat jako hodnotu *kontejner*, ne každá hodnota *kontejner* představuje mediální položku. Proto, pokud nakonfigurujete formát ER tak, aby používal *kontejner* pro vložení obrázku do vygenerovaných dokumentů, ale odkazovaný *kontejner* nevrátí mediální obsah, může být vyvolána výjimka podobná následujícímu příkladu: „Chyba při provádění kódu: Binární (objekt), metoda constructFromContainer volaná s neplatnými parametry.“

Výchozí hodnota a *kontejneru* je **null**.

Následující obrázek ukazuje, jak je pole **Bitmap(Image)** typu *Kontejner* vázáno na pole **Logo** datového modelu typu **Kontejner** v mapování modelu **Prodejní faktura**. Tato vazba zpřístupňuje logo společnosti pro jakýkoli formát ER, který je určen pro kořenovou definici **SalesInvoice** a která používá toto mapování modelu za běhu.

[![Vazba pole typu kontejner v návrháři mapování modelu ER.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Záznam

*Záznam* je kolekce pojmenovaných polí, z nichž každé je spojeno s hodnotou buď [jednoduchého](er-formula-supported-data-types-primitive.md) datového typu nebo složeného datového typu. Obvykle se *záznam* používá k reprezentaci jednoho záznamu seznamu záznamů. V tomto případě každá položka představuje jednotlivá pole, metody a vztahy.

Výchozí hodnota *záznamu* je **null**.

> [!NOTE]
> Když získáte hodnotu pole prázdného *záznamu*, je vrácena výchozí hodnota příslušného datového typu.

*Záznam* lze získat pomocí následujících funkcí:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Další informace o transformaci hodnot *záznam* viz [Seznam funkcí ER v kategorii seznamu](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Seznam záznamů

*Seznam záznamů* je seznam položek typu *záznam*. Obvykle se *seznam záznamů* používá k reprezentaci seznamu záznamů, které byly načteny z databázové tabulky.

Ve výchozím nastavení jsou záznamy *seznamu záznamů* přístupné postupně. Pro přístup ke konkrétnímu záznamu můžete použít funkci [INDEX](er-functions-list-index.md) a zadat index *integer*.

Výchozí hodnota *seznamu záznamů* je **null**. Můžete použít funkci [ISEMPTY](/er-functions-list-isempty.md) k vyhodnocení, zda je *seznam záznamů* prázdný.

> [!NOTE]
> Pokud je *seznam záznamů* prázdný, jakýkoli pokus o získání hodnoty pole pro *záznam*, který se v něm nachází, způsobí, že výjimka bude vyvolána za běhu. Informace o tom, jak můžete zabránit výjimkám za běhu tohoto typu, najdete v tématu [Zvažování případů prázdného seznamu](er-components-inspections.md#i9).

*Seznam záznamů* lze spustit pomocí následujících funkcí:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Další informace o transformaci hodnot *seznamu záznamů* viz [Seznam funkcí ER v kategorii seznamu](er-functions-category-list.md). Chcete-li se naučit, jak představit položky *seznamu záznamů*, naplňte je daty aplikace a poté použijte data ke generování obchodních dokumentů, viz [Navrhněte nové řešení ER pro tisk vlastní sestavy](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekt

*Objekt* odkazuje na stavovou instanci *třídy*. Obvykle je *objekt* zahájen ve zdrojovém kódu. Poté se předá mapování modelu ER a poskytne podrobnosti kontextu spuštění.

Výchozí hodnota *objektu* je **null**.

Následující obrázek ukazuje, jak je zdroj dat **ReportDataContract** typu *Objekt* přidán pro předání informací o generované faktuře ze zdrojového kódu do mapování modelu **Faktura projektu**. Například text instance faktury se předává jako součást kontextu provádění. Tento text je převzat ze zdrojového kódu za běhu spuštěním vazby `ReportDataContract.parmInvoiceInstanceText`, která byla nakonfigurována pro pole **Poznámka** datového modelu ER. Tato vazba volá metodu `parmInvoiceInstanceText()` třídy aplikací **PSAProjInvoiceContract**, která je v aktuálním mapování modelu reprezentována jako zdroj dat **ReportDataContract**.

[![Konfigurace zdroje dat objektu v návrháři mapování modelů ER.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Pokud se chcete dozvědět, jak předat podrobnosti kontextu spuštění ze zdrojového kódu do spuštěného řešení ER, přečtěte si téma [Vyvíjejte artefakty aplikací pro volání navržené zprávy](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)
- [Podporované typy jednoduchých dat](er-formula-supported-data-types-primitive.md)
