---
title: Rozložení směrování popisku dokumentů
description: V tomto článku je popsán způsob použití metod formátování k tisku hodnot na štítcích.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708637"
---
# <a name="document-routing-label-layout"></a>Rozložení směrování popisku dokumentů

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvořit rozložení pro popisky registračních značek, kontejneru a vlny. Poskytuje také pokyny pro používání programovacího jazyka Zebra (ZPL), který se používá k vytváření rozložení.

Rozložení popisku směrování dokumentu definují způsob rozvržení popisků a data, která jsou na nich vytištěna. Body aktivace tisku se nastavují při nastavení položek nabídky mobilního zařízení a pracovních šablon.

Informace v tomto článku platí pro všechna rozložení štítků směrování dokumentu, včetně rozložení pro [popisky registračních značek](tasks/license-plate-label-printing.md), [popisky kontejneru](print-container-labels.md) a [popisky vlny](configure-wave-label-printing.md).

Můžete tisknout velmi složité štítky za předpokladu, že tiskové zařízení může interpretovat text, který mu byl odeslán. Například rozložení ZPL, které obsahuje čárový kód, může vypadat podobně jako v následujícím příkladu.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

V rámci procesu tisku štítků bude text `$LicensePlateId$` v tomto příkladu nahrazen datovou hodnotou. Několik široce dostupných nástrojů pro generování štítků vám může pomoci formátovat text pro rozvržení štítků. Mnohé z těchto nástrojů podporují `$FieldName$` formát. Kromě toho Microsoft Dynamics 365 Supply Chain Management používá speciální logiku formátování jako součást mapování polí pro rozložení směrování dokumentu.

Chcete-li zobrazit hodnoty, které budou vytištěny, přejděte na **Řízení skladu \> Dotazy a sestavy \> Štítky registračních značek**.

## <a name="turn-on-this-feature-for-your-system"></a>Zapnutí této funkce ve vašem systému

Pokud váš systém ještě neobsahuje funkce popsané v tomto článku, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Vylepšené rozvržení popisků poznávacích značek*. (Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout.)

## <a name="custom-number-formats"></a>Vlastní formáty čísel

Formátování hodnot číselných polí, které jsou vytištěny pomocí kódů s následujícím formátem, lze přizpůsobit.

```dos
$FieldName:FormatString$
```

Zde je vysvětlení tohoto formátu:

- `FieldName` je název datového pole (například **množství**).
- `FormatString` definuje způsob tisku dat.

Následující příklady ukazují, jak lze upravit pole pracovní množství (**množství**):

- Chcete-li vždy zobrazit čtyři číslice (pomocí nul jako zástupné symboly), použijte `$Qty:0000$`. Pokud je například množství 10, štítek zobrazí "0010".
- Chcete-li vždy zobrazit dvě desetinná místa, použijte možnost `$Qty:0.00$`. Pokud je například množství 10, štítek zobrazí "10.00".

Úplný seznam dostupných formátovacích řetězců čísel naleznete v tématu [Vlastní číselné formátovací řetězce](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Formáty vlastních řetězců

První znaky řetězce můžete odebrat pomocí následujícího pole a kódu formátu.

```dos
$FieldName:#..$
```

Zde určuje `#` počet znaků, které mají být přeskočeny. Chcete-li například vytisknout sériové číslo kontejneru (SSCC), který neobsahuje první dva znaky, použijte možnost `$LicensePlateId:2..$`. V takovém případě bude číslo registrační značky 0011111111111222221 vytisknuto jako 11111111111222221.

## <a name="custom-datetime-formats"></a>Vlastní formáty data a času

V následujícím příkladu je ukázáno, jak lze ovládat formát používaný k tisku dat.

```dos
$PrintedDate:dd-MM-yyyy$
```

V tomto příkladu bude datum 30. dubna 2020 vytisknuto jako "30-04-2020".

Úplný seznam dostupných formátů data/času naleznete v tématu [Vlastní formátovací řetězce data/času](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Tisk jednotlivých řádků z víceřádkových dat

Obsahuje-li datové pole více řádků (tj. řádků oddělených zalomením řádků), můžete vytisknout jednotlivé řádky s použitím následujícího formátu.

```dos
$FieldName[#]$
```

Zde `#` je číslo řádku, který chcete vytisknout. (Pro první řádek použijte 1.)

Váš systém má například pole `AdditionalAddress`, ve kterém je uložena následující víceřádková adresa:

Společnost Contoso-Inc.  
Název ulice 123  
Některé město, některý stát

Tuto adresu lze po jednotlivých řádcích vytisknout pomocí následujících kódů.

| Kód | Text vytištěný |
|---|---|
| `$AdditionalAddress[1]$` | Společnost Contoso-Inc. |
| `$AdditionalAddress[2]$` | Název ulice 123 |
| `$AdditionalAddress[3]$` | Některé město, některý stát |

## <a name="print-and-format-from-a-display-method"></a>Tisk a formátování z metody zobrazení

Můžete tisknout z metody zobrazení v následujícím formátu.

```dos
$DisplayMethod()$
```

Tento formát lze kombinovat s jinými typy, které byly popsány dříve v tomto článku. Například máte pojmenovanou metodu zobrazení `DisplayListOfItemsNumbers()` a chcete vytisknout číslo první položky této metody. V takovém případě můžete použít následující kód.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Další informace o tisku štítků

Další informace o nastavení a tisku štítků naleznete v následujících článcích:

- [Tisk popisku registrační značky](tasks/license-plate-label-printing.md)
- [Tisk popisku kontejneru](print-container-labels.md)
- [Tisk štítků vlny](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
