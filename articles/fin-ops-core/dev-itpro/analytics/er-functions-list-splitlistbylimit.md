---
title: Funkce elektronického výkaznictví SPLITLISTBYLIMIT
description: Toto téma obsahuje obecné informace o použití funkce SPLITLISTBYLIMIT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1e6a4638cd32cb253261cc7fbaacb45b47f52c62
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683692"
---
# <a name="splitlistbylimit-er-function"></a>Funkce elektronického výkaznictví SPLITLISTBYLIMIT

[!include [banner](../includes/banner.md)]

Funkce `SPLITLISTBYLIMIT` rozdělí zadaný seznam na nový seznam dílčích seznamů (dávek). Počet záznamů v každé dávce se dynamicky vypočítává. Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.

## <a name="syntax"></a>Syntaxe

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`limit value`: *celé číslo* nebo *reálné číslo*

Maximální hodnota limitu použitého k rozdělení původního seznamu na dávky.

`limit source`: *pole*

Platná cesta k poli datového typu *celé číslo* nebo *reálné číslo* v zadaném seznamu. Hodnota v tomto poli definuje krok, o který je celková částka zvýšena.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Vrácený seznam dávek obsahuje následující prvky:

- **Value**: *seznam*

    Seznam záznamů, které patří do aktuální dávky.

- **BatchNumber**: *celé číslo*

    Číslo aktuální dávky ve vráceném seznamu.

Limit nebude použito na jednu položku z původního seznamu, když zdrojový limit překročí definovaný limit.

## <a name="example"></a>Příklad

Následující ilustrace znázorňuje formát elektronického vykazování (ER).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Následující obrázek zobrazuje formát a zdroje dat, které se pro něj používají.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Následující obrázek znázorňuje výsledek při spuštění formátu. V takovém případě je výstup prostý seznam položek komodit.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Následující obrázek uvádí stejný formát, který byl upraven tak, aby obsahoval seznam položek komodit v dávkách, kdy musí jedna dávka zahrnovat komodity a celková hmotnost (weight) nesmí překračovat limit 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Následující obrázek znázorňuje výsledek při spuštění upraveného formátu.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Limit není použit na poslední položku v původním seznamu, protože hodnota (**11**) zdroje limitu (**weight**) překračuje definovaný limit (**9**). Chcete-li ignorovat podseznamy při generování sestavy, dle potřeby použijte buď funkci `WHERE`, nebo výraz **Enabled** odpovídajícího prvku formátu.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]