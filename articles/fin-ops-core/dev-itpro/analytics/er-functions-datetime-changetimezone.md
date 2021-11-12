---
title: Funkce ER CHANGETIMEZONE
description: Toto téma obsahuje obecné informace o použití funkce CHANGETIMEZONE elektronického výkaznictví.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647923"
---
# <a name="changetimezone-er-function"></a>Funkce ER CHANGETIMEZONE

[!include [banner](../includes/banner.md)]

Funkce `CHANGETIMEZONE` vrátí hodnotu typu *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]), která je převedena na danou hodnotu datum/čas v jednom časovém pásmu na hodnotu datum/čas v jiném časovém pásmu.

## <a name="syntax"></a>Syntaxe

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumenty

`datetime`: *datum a čas*

Hodnota data a času v časovém pásmu koordinovaný univerzální čas, která představuje hodnotu data a času, která se má převést.

`base time zone`: *[Řetězec](er-formula-supported-data-types-primitive.md#string)*

Název časového pásma, do kterého je daná hodnota data/času posunuta před převodem.

`target time zone`: *řetězec*

Název časového pásma, do kterého je převedená hodnota data/času posunuta během převodu.

## <a name="return-values"></a>Vrácené hodnoty

*Datum/čas*

Výsledná hodnota data a času v koordinovaném univerzálním časovém pásmu.

## <a name="usage-notes"></a>Poznámky k použití

Chcete-li zadat zdrojová a cílová časová pásma, můžete použít názvy časových pásem, které jsou [poskytnuty](https://data.iana.org/time-zones/releases/) úřadem [Internet Assigned Numbers Authority (IANA)](https://www.iana.org/) nebo které jsou [podporovány](/windows-hardware/manufacture/desktop/default-time-zones) systémem Microsoft Windows.

Běhová výjimka „Časové pásmo '\<time zone name\>' neexistuje“ je vyvolána, pokud zadaný název není nalezen v seznamu IANA nebo v registru Windows.

U časových pásem, kde je dodržován letní čas, převod bere v úvahu posun letního času koordinovaného univerzálního času. Při převodu jsou použity nejnovější dostupné informace o tomto posunu.

## <a name="example-1"></a>Příklad 1

V tomto příkladu jsou použity názvy časových pásem pro Windows.

Nakonfigurujete zdroj dat **DSX** typu **Vypočítané pole**. Obsahuje následující výraz.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Pokud nakonfigurujete výraz zdroje dat **DSY** typu **Vypočítané pole** jako `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, zdroj dat **DSX** vrátí text **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Tento text ukazuje, že časový rozdíl mezi dvěma poskytnutými časovými pásmy 1. června je více než 24 hodin. Převedená hodnota data a času je tedy o jeden den dřívější než daná hodnota data a času, protože základní časové pásmo je před cílovým časovým pásmem.

Pokud nakonfigurujete výraz zdroje dat **DSY** typu **Vypočítané pole** jako `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, zdroj dat **DSX** vrátí text **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Tento text ukazuje, že časový rozdíl mezi dvěma poskytnutými časovými pásmy 1. prosince je méně než 24 hodin. Převedená hodnota data a času se tedy rovná dané hodnotě data a času.

> [!NOTE]
> Stejný výraz vrátí různou odchylku mezi poskytnutými a převedenými hodnotami data a času pro stejnou dvojici časových pásem, protože pro zadaná časová pásma je v dané datum a čas pozorován jiný posun koordinovaného univerzálního času na letní čas.

## <a name="example-2"></a>Příklad 2

V tomto příkladu jsou použity názvy časových pásem IANA.

Nakonfigurujete zdroj dat **DSX** typu **Vypočítané pole**. Obsahuje následující výraz.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Pokud nakonfigurujete výraz zdroje dat **DSY** typu **Vypočítané pole** jako `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, zdroj dat **DSX** vrátí text **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Tento text ukazuje, že časový rozdíl mezi dvěma poskytnutými časovými pásmy 1. června je více než 24 hodin. Převedená hodnota data a času je tedy o jeden den dřívější než daná hodnota data a času, protože základní časové pásmo je před cílovým časovým pásmem.

Pokud nakonfigurujete výraz zdroje dat **DSY** typu **Vypočítané pole** jako `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, zdroj dat **DSX** vrátí text **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Tento text ukazuje, že časový rozdíl mezi dvěma poskytnutými časovými pásmy 1. prosince je méně než 24 hodin. Převedená hodnota data a času se tedy rovná dané hodnotě data a času.

## <a name="example-3"></a>Příklad 3

Nakonfigurujete zdroj dat **DSX** typu **Vypočítané pole**. Obsahuje následující výraz.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Pokud nakonfigurujete výraz zdroje dat **DSY** typu **Vypočítané pole** jako `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, zdroj dat **DSX** vrátí text **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00**. Tento text ukazuje, že časový rozdíl mezi dvěma poskytnutými časovými pásmy 1. června je více než 24 hodin. Převedená hodnota data a času je tedy o jeden den pozdější než daná hodnota data a času, protože cílové časové pásmo je před základním časovým pásmem.

## <a name="example-4"></a>Příklad 4

Datum/časové razítko můžete obdržet z externího zdroje jako text, který neobsahuje žádné informace o časovém pásmu. Možná však znáte časové pásmo, ve kterém je zdroj provozován. Obdržíte například datum a čas **01/12/2021 12:55:00** ze služby, která je provozována ve Španělsku. Chcete-li správně uložit tuto hodnotu data/času do databáze, proveďte následující převod:

- Nakonfigurujte zdroj dat **DSY** typu **Vypočítané pole**, chcete-li převést razítko data a času z textu na hodnotu data a času koordinovaného univerzálního času.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Nakonfigurujte zdroj dat **DSX** typu **Vypočítané pole**, chcete-li změnit převedenou hodnotu data/času na koordinovaný univerzální čas jako hodnotu data/času časového pásma externího zdroje.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Když použijete funkci `CHANGETIMEZONE` pro převod data/času, mějte na paměti, že jakákoli hodnota data/času je uložena v databázi jako hodnota v koordinovaném univerzálním časovém pásmu. Než může být tato hodnota prezentována na stránkách aplikace, je transformována. Transformace bere v úvahu časové pásmo, které je [nastaveno](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) jako preferované pásmo pro aktuálně přihlášeného uživatele aplikace.

## <a name="additional-resources"></a>Další prostředky

[Funkce data a času](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
