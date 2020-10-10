---
title: Funkce el. výkaznictví GETENUMVALUEBYNAME
description: Toto téma obsahuje obecné informace o použití funkce GETENUMVALUEBYNAME elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885220"
---
# <a name="getenumvaluebyname-er-function"></a>Funkce el. výkaznictví GETENUMVALUEBYNAME

[!include [banner](../includes/banner.md)]

Funkce `GETENUMVALUEBYNAME` vyhledá určitou hodnotu typu *výčet* v zadaném zdroji dat výčtu pomocí názvu výčtu, který je zadán jako hodnota typu *řetězec*. Pokud je nalezena hodnota *výčet*, funkce ji vrátí. V opačném případě funkce vrátí hodnotu výčtu **null**.

## <a name="syntax"></a>Syntaxe

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenty

`enumeration data source path`: *výčet*

Platná cesta zdroje dat jednoho z následujících typů výčtu:

- Výčet modelů elektronického výkaznictví
- Výčet formátu elektronického výkaznictví
- Výčet Microsoft Dynamics 365 Finance

`enumeration value text`: *řetězec*

Hodnota typu řetězec, která představuje název jedné hodnoty výčtu.

## <a name="return-values"></a>Vrácené hodnoty

Hodnota typu *výčet* s možností nabytí hodnoty Null

Výsledná výčtová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Není vyvolána žádná výjimka, pokud není nalezena hodnota typu *výčet* za použití názvu výčtové hodnoty, která je zadána jako hodnota typu *řetězec*.

## <a name="example-1"></a>Příklad 1

Na následujícím obrázku je výčet **ReportDirection** uveden v datovém modelu. Všimněte si, že pro výčtové hodnoty jsou definovány popisky.

![Dostupné hodnoty pro výčet datového modelu](./media/ER-data-model-enumeration-values.PNG)

Následující obrázek znázorňuje tyto podrobnosti:

- Zdroj dat **$Direction** je konfigurován v sestavě elektronického výkaznictví. Tento zdroj dat je konfigurován na základě výčtu modelu **ReportDirection**.
- Výraz `$IsArrivals` je určený k použití zdroje dat **$Direction** výčtu modelů jako parametr této funkce.
- Hodnota tohoto porovnávacího výrazu je **TRUE**.

![Příklad výčtu mapování modelu dat](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Příklad 2

Funkce `GETENUMVALUEBYNAME` a [`LISTOFFIELDS`](er-functions-list-listoffields.md) vám umožňují načíst hodnoty a štítky podporovaných výčtů jako textové hodnoty. (Podporované výčty jsou výčty aplikací, výčty datových modelů a výčty formátů.)

Na následujícím obrázku je datový zdroj **TransType** uveden v mapování modelu. Tento zdroj dat odkazuje na výčet aplikace **LedgerTransType**.

![Zdroj dat mapování modelu, který odkazuje na výčet aplikace](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Následující obrázek je datový zdroj **TransTypeList**, který je konfigurován v mapování modelu. Tento zdroj dat je konfigurován na základě výčtu aplikace **TransType**. Funkce `LISTOFFIELDS` se používá k vrácení všech hodnot výčtu jako seznam záznamů, které obsahují pole. Tímto způsobem jsou vystaveny podrobnosti každé hodnoty výčtu.

> [!NOTE]
> Pole **EnumValue** je nakonfigurováno pro zdroj dat **TransTypeList** pomocí výrazu `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. Toto pole vrací hodnotu výčtu pro každý záznam v tomto seznamu.

![Zdroj dat mapování modelu, který vrací všechny hodnoty výčtu vybraného výčtu jako seznam záznamů](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Následující obrázek je datový zdroj **VendTrans**, který je konfigurován v mapování modelu. Tento zdroj dat vrací záznamy transakcí dodavatele z aplikační tabulky **VendTrans**. Typ typ registru každé transakce je definován hodnotou pole **TransType**.

> [!NOTE]
> Pole **TransTypeTitle** je nakonfigurováno pro zdroj dat **VendTrans** pomocí výrazu `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. Toto pole vrací štítek hodnoty výčtu aktuální transakce jako text, pokud je tato hodnota výčtu k dispozici. Jinak bude vrácena hodnota prázdného řetězce.
>
> Pole **TransTypeTitle** je vázáno na pole **LedgerType** datového modelu, které umožňuje použití těchto informací v každém formátu ER, který používá datový model jako zdroj dat.

![Zdroj dat mapování modelu, který vrací transakce dodavatele](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Následující ilustrace ukazuje, jak můžete použít [ladicí program zdroje dat](er-debug-data-sources.md) a otestovat nakonfigurované mapování modelu.

![Pomocí ladicího programu zdroje dat otestujte nakonfigurované mapování modelu](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Pole **LedgerType** datového modelu vystavuje popisky typů transakcí podle očekávání.

Pokud plánujete použít tento přístup pro velké množství transakčních dat, musíte zvážit výkon provádění. Více informací viz [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Další prostředky

[Textové funkce](er-functions-category-text.md)

[Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md)

[Funkce elektronického výkaznictví LISTOFFIELDS](er-functions-list-listoffields.md)

[Funkce elektronického výkaznictví FIRSTORNULL](er-functions-list-firstornull.md)

[Funkce elektronického výkaznictví WHERE](er-functions-list-where.md)
