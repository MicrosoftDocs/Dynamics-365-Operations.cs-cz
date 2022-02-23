---
title: Funkce ER Base64StringToContainer
description: Toto téma obsahuje obecné informace o použití funkce Base64StringToContainer elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739062"
---
# <a name="base64stringtocontainer-er-function"></a>Funkce ER Base64StringToContainer

[!include [banner](../includes/banner.md)]

[Funkce](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` převede zadaný vstup datového typu *String* na položku datového typu *[Kontejner](er-functions-category-container.md)*.

## <a name="syntax"></a>Syntaxe

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner*

Výsledná binární hodnota ve formátu binárního velkého objektu (BLOB).

## <a name="usage-notes"></a>Poznámky k použití

Výjimka „Parametr není platný“ je vyvolána, pokud vstupní řetězec neposkytuje správnou skupinu schémat kódování binárního textu na Base64.

## <a name="example"></a>Příklad

Definujte v mapování modelu následující zdroje dat:

- Kořenový zdroj dat **DocuTypeGroupEnum** typu *Dynamics 365 for Operations / Výčet*, který odkazuje na výčet aplikace **DocuTypeGroup**
- Kořenový zdroj dat **Zákazník** typu *Dynamics 365 for Operations / Záznamy tabulky*, který odkazuje na aplikační tabulku **CustTable**
- Zdroj dat **\#Media** typu *Vypočítané pole*, který je nakonfigurován následujícím způsobem:

    - Je přidán jako podřízený zdroj dat **Zákazník**.
    - Obsahuje výraz `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Zdroj dat **\#MediaAsBase64String** typu *Vypočítané pole*, který je nakonfigurován následujícím způsobem:

    - Je přidán jako podřízený zdroj dat **Customer.'\#Media'**.
    - Obsahuje výraz `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Zdroj dat **\#BlobFomBase64** typu *Vypočítané pole*, který je nakonfigurován následujícím způsobem:

    - Je přidán jako podřízený zdroj dat **Customer.'\#Media'**.
    - Obsahuje výraz `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

V tomto příkladu zdroj dat **\#MediaAsBase64String** kóduje binární obsah aktuální přílohy média jako text, který představuje skupinu schémat kódování binárního textu na Base64. Zdroj dat **\#BlobFomBase64** dekóduje řetězec Base64 a vrátí binární hodnotu ve formátu BLOB.

![Ukázka zdrojů dat na stránce návrháře mapování modelu ER](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Další prostředky

[Funkce kontejneru](er-functions-category-container.md)
