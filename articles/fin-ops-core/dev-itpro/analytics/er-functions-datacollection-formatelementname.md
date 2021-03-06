---
title: Funkce FORMATELEMENTNAME ER
description: Toto téma obsahuje obecné informace o použití funkce FORMATELEMENTNAME elektronického výkaznictví.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: f716fe779903b4e9142b7959d868256f2d84c624
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755221"
---
# <a name="formatelementname-er-function"></a>Funkce FORMATELEMENTNAME ER

[!include [banner](../includes/banner.md)]

Funkce `FORMATELEMENTNAME` vrací hodnotu *řetězec*, která představuje název aktuálního prvku formátu elektronického výkaznictví.

## <a name="syntax"></a>Syntaxe

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Tuto funkci lze volat ve výrazech ER, které byly nakonfigurovány pro vlastnosti **název získaného datového klíče** a **hodnota získaného datového klíče** komponenty formátu ER ze skupiny **Text**, která se nachází v rámci komponenty **Společné\\Soubor**, kde je zapnutá možnost **Shromáždit podrobnosti výstupu**.

## <a name="example"></a>Příklad

Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.

## <a name="additional-resources"></a>Další zdroje

[Funkce shromažďování dat](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]