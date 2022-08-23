---
title: Seznam funkcí ER v kategorii kontejneru
description: Tento článek obsahuje informace o funkcích kontejneru, které jsou podporovány v elektronickém výkaznictví (ER).
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282644"
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
