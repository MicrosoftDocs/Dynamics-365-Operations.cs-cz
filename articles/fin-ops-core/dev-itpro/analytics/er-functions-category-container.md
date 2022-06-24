---
title: Seznam funkcí ER v kategorii kontejneru
description: Tento článek obsahuje informace o funkcích kontejneru, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5c86b0ae6cbf4ac6515491b55390d42c371eae4b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883810"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Seznam funkcí ER v kategorii kontejneru

[!include [banner](../includes/banner.md)]

[Kontejner elektronického výkaznictví (ER)](general-electronic-reporting.md) má [funkce](er-formula-language.md#Functions), které lze použít k provádění operací zahrnujících zdroje dat datového typu *Kontejner*. K těmto operacím dochází, když data zpracování představují kolekci binárních dat ve formátu binárního velkého objektu (BLOB). Tento článek obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | popis |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Tato funkce vrací hodnotu *Kontejner*, která se skládá z binárního obsahu, který je dekódován ze zadaného řetězce ASCII, který představuje skupinu Base64 schémat kódování binárního textu. |

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
