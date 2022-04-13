---
title: Funkce ER GETLABELTEXT
description: Toto téma obsahuje obecné informace o použití funkce GETLABELTEXT elektronického výkaznictví.
author: NickSelin
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ce66c9410abeee16bbd074204262edf79bf6d68
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462404"
---
# <a name="getlabeltext-er-function"></a>Funkce ER GETLABELTEXT

[!include [banner](../includes/banner.md)]

Funkce `GETLABELTEXT` hledá konkrétní štítek, aby vrátila a hodnotu *[Řetězec](er-formula-supported-data-types-primitive.md#string)*, která představuje překlad zadaného štítku do zadaného jazyka.

## <a name="syntax"></a>Syntaxe

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumenty

### <a name="label-id"></a>ID popisku

`label id`: *Řetězec* nebo *ID štítku*

Platné ID jednoho z následujících typů štítků:

- Štítek [Elektronického výkaznictví (ER)](general-electronic-reporting.md)
- Štítek Microsoft Dynamics 365 Finance

#### <a name="usage-notes"></a>Poznámky k použití

Tento argument lze definovat pouze jako konstantu pomocí jednoho z následujících podporovaných vzorů:

- Pro štítky ER:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Pro štítky Financí:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> V době návrhu se zobrazí chybová zpráva ověření na stránce **[Návrhář vzorce](er-advanced-formula-editor.md)**, pokud pomocí poskytnutého ID štítku nelze najít žádný štítek.

### <a name="language"></a>Jazyk

`language`: *řetězec*

Řetězec, který představuje kód jazyka.

#### <a name="usage-notes"></a>Poznámky k použití

Tento argument lze definovat buď jako textovou konstantu, nebo jako cestu pole zdroje dat, které vrací hodnota *Řetězec*.

> [!NOTE]
> V době návrhu se zobrazí chybová zpráva ověření, pokud pomocí poskytnutého argumentu `language` nelze najít žádný kód, když byl definován jako textová konstanta.
>
> Za běhu je překlad pro systémový jazyk `EN-US` vrácen pro zadaný štítek, pokud nebyl pomocí zadaného argumentu `language` nalezen žádný kód jazyka.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example-1-system-label"></a><a name=example-1></a>Příklad 1: Systémový štítku

Výrazy `GETLABELTEXT (@"SYS70894", "en-us")` a `GETLABELTEXT ("SYS70894", "en-us")` vrátí anglický překlad „Nothing to print“ pro štítek aplikace `@SYS70894`.

## <a name="example-2-er-label"></a><a name=example-2></a>Příklad 2: štítek ER

Začnete upravovat [konfiguraci](general-electronic-reporting.md#Configuration) ER, která byla [odvozena](er-quick-start2-customize-report.md#DeriveProvidedFormat) od konfigurace **Převod kreditu ISO20022 (DE)**, zadáte nový zdroj dat typu *[Počítané pole](er-calculated-field-ds-performance.md)* a nakonfigurujete výraz `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` pro tento zdroj dat. V tomto případě za běhu zdroj dat vrátí německý překlad „Kreditorenname“ jako štítek ER `@GER_LABEL:VendorName`, který byl původně nakonfigurován v základní konfigurace ER **Převod kreditu ISO20022 (DE)**.

## <a name="additional-resources"></a>Další prostředky

[Textové funkce](er-functions-category-text.md)

[Navrhujte vícejazyčné zprávy v elektronickém výkaznictví](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
