---
title: Pružné skupiny
description: Toto téma popisuje, jak se používají pružné skupiny v modulu Čas a docházka.
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: aae00f3605a6598a34e58fad3e06e687476dd859
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "361192"
---
# <a name="flex-groups"></a>Pružné skupiny

[!include[banner](../includes/banner.md)]

Pružná pracovní doba umožňuje společnostem minimalizovat platby za přesčasy tak, že nabídnou zaměstnancům extra pracovní volno v době, kdy je nízké pracovní vytížení. Tato funkce má smysl například v oblastech, kde se mění pracovního vytížení podle sezóny.

Můžete použít pružné skupiny pro nastavení následujících pravidel a zásad pružné pracovní doby pracovníka:

- Pravidla pro předpisy pružné pracovní doby
- Principy pro výpočet pružného zůstatku pracovníka

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Nastavení pružné pracovní doby do pružných skupin

- Vyberte **Čas a docházka** \> **Nastavení** \> **Skupiny** \> **Pružné skupiny** pro nastavení pružných skupin pro pružné pracovní doby.

## <a name="associate-workers-with-flex-groups"></a>Přiřazení pracovníků k pružným skupinám

- Zvolte **Čas a docházka** \> **Nastavení** \> **Pracovníci registrace času**.

## <a name="rules-for-flex-regulations"></a>Pravidla pro předpisy pružné pracovní doby

Můžete používat pravidla pro regulace pružné pracovní doby, abyste definovali její limity, nebo nebo minimální a maximální počet hodin, který je povolen na účtu pružné pracovní doby pracovníka. Limity pružné pracovní doby se nastavují na pružné skupině. Když jsou limity pružné pracovní doby překročeny, lze upravit zůstatek pružné pracovní doby pracovníka a mzdu.

Pokud je překročeno minimum pružné pracovní doby pracovníka (tj. pokud je počet hodin na účtu pružné pracovní doby nižší než určené minimum), můžete pomocí těchto metod zůstatek pružné pracovní doby pracovníka regulací pružné pracovní doby:

- Účet pružné pracovní doby pracovníka může být nastaven na stanovené povolené minimum, ale bez odečtení mzdy pracovníka za počet hodin, kdy je účet pružné pracovní doby nižší než povolené minimum
- Mzdu pracovníka lze odečíst za počet hodin, kdy je účet pružné pracovní doby nižší než povolené minimum. Tento odpočet se provádí generováním mzdových položek pro konkrétní typ mzdy, které mají negativní nebo pozitivní mzdovou jednotku.

Pokud je překročeno maximum povolené pružné pracovní doby pracovníka, můžete tyto metody použít k úpravě zůstatku pružné pracovní doby pracovníka pomocí regulace pružné pracovní doby:

- Účet pružné pracovní doby pracovníka může být nastaven zpět na stanovené povolené maximum, ale bez kompenzace mzdy pracovníka za počet hodin, kdy pracovník pracoval nad povolené maximum.
- Počet hodin, kdy pracovník pracoval nad povolené maximum, může být převeden na mzdu. Tento přepočet se provádí generováním mzdových položek pro konkrétní typ mzdy.

Zůstatek pružné pracovní doby můžete upravit v následujících případech:

- Pokud je soubor plateb založený na mzdových datech exportován pomocí úlohy **Převést mzdu**. Mzdová data jsou generována při převodu registrace pracovníka ze stránky **Schválit**.
- Při zpracování úlohy **Upravit zůstatek pružné pracovní doby**.

> [!NOTE]
> K regulaci pružné pracovní doby nedochází během denního schvalování a převodu registrací pracovníka na stránce **Schválit**.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Principy pro výpočet zůstatku pružné pracovní doby pracovníka

Zásady pro výpočet hodin, o které jsou je upraven zůstatek pružné pracovní doby pracovníka, se nastavuje na pružné skupině. Vyberte **Čas a docházka** \> **Nastavení** \> **Skupiny** \> **Pružné skupiny**. 

Lze použít následující dvě zásady:

- **Čas** – Pružná pracovní doba pracovníka se vypočítá pouze z registrovaného času pracovníka pro daný den. Při výpočtu denních registrací pracovníka se vypočítá počet hodin Flex+ a Flex- ze zón Flex+ a Flex, definovaných v časovém profilu pracovníka.
- **Typy mezd** – Pružná pracovní doba pracovníka se vypočítá na základě příjmů typů mezd pro Flex+ a Flex-, které jsou definovány v platební dohodě pracovníka. Platební dohoda je přidružena k registraci pracovní doby pracovníka. Můžete chtít použít typy mezd ke správě účtu pružné pracovní doby, pokud například chcete navýšit účet pružné pracovní doby pracovníka o specifický koeficient v jedné nebo více pružných zónách.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Scénář 1: Úprava mzdy pracovníka a účtu pružné pracovní doby z důvodu překročení povoleného pružného minima

Pracovník, který může mít pružnou pracovní dobou, má záporný účet pružné pracovní doby.

- **Účet pružné pracovní doby:** -4

Pracovník je přiřazen k pružné skupině, která má následující konfiguiraci:

- **Pružné minimum:** -0,5
- **Minimální typ mzdy:** 1302
- **Koeficient typu mzdy:** -1,00

Jak rozdíl mezi účtem pružné pracovní doby pracovníka a jeho povoleným pružným minimem ukazuje, pracovník překročil své povolené pružné minimum o 3,5 hodiny.

Při správce mezd převede data mzdy pracovníka spuštěním úlohy **Převod na platbu** nebo **Pružná úprava**, provedou se následující úpravy:

- Účet pružné pracovní doby pracovníka se upraví o 3,5 hodiny. Z tohoto důvodu bude pružný zůstatek -4 hodiny upraven na povolené pružné minimum pracovníka -0,5 hodiny.
- Vytvoří se položka mzdy pro typ mzdy 1302. Tato položku mzdy má mzdovou jednotku -3,5 hodiny, která se odečte ze mzdy pracovníka. Mzdová jednotka v tomto případě je záporná, vzhledem k tomu, že kladná úprava 3,5 hodiny je vynásobena záporným koeficient typu mzdy -1,0, definovaným na pružné skupině. Tato položka mzdy bude součástí souboru mzdy, který je generován úlohou **Převod na platbu**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Scénář 2: Úprava mzdy pracovníka a účtu pružné pracovní doby z důvodu překročení povoleného pružného maxima

Pracovník, který může mít pružnou pracovní dobou, má kladný účet pružné pracovní doby.

- **Účet pružné pracovní doby:** 6

Pracovník je přiřazen k pružné skupině, která má následující konfiguiraci:

- **Pružné maximum:** 2,0
- **Minimální typ mzdy:** 1302
- **Koeficient typu mzdy:** -1,0

Jak rozdíl mezi účtem pružné pracovní doby pracovníka a jeho povoleným pružným maximem ukazuje, pracovník překročil své povolené pružné maximum o 4,0 hodiny.

Při správce mezd převede data mzdy pracovníka spuštěním úlohy **Převod na platbu** nebo **Pružná úprava**, provedou se následující úpravy:

- Účet pružné pracovní doby pracovníka se upraví o -4,0 hodiny. Z tohoto důvodu bude pružný zůstatek 6 hodin upraven na povolené pružné maximum pracovníka 2 hodiny.
- Vytvoří se položka mzdy pro typ mzdy 1302. Tato položku mzdy má mzdovou jednotku 4,0 hodiny, která se přidá ke mzdě pracovníka. Mzdová jednotka v tomto případě je kladná, vzhledem k tomu, že záporná úprava 4,0 hodiny je vynásobena záporným koeficient typu mzdy -1,0, definovaným na pružné skupině. Tato položka mzdy bude součástí souboru mzdy, který je generován úlohou **Převod na platbu**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Scénář 3: Správa pružného zůstatku pracovníka na základě typů mezd

Jak jsme vysvětlil dříve, účty pružné pracovní doby lze spravovat buď na základě času registrovaného v zónách Flex+ a Flex- definovaných časovým profilem pracovníka, nebo na základě typů mezd, které jsou definovány v platebních dohodách pracovníka. Pokud se používají typy mzdy, účet pružné pracovní doby pracovníka se upraví o položky mzdy, které jsou generovány při převodu registrace pracovníka ze stránky **Schválit**. Můžete chtít použít typy mezd ke správě účtu pružné pracovní doby, pokud například chcete navýšit účet pružné pracovní doby pracovníka o specifický koeficient v jedné nebo více pružných zónách.

Tento scénář používá následující profil pružné pracovní doby představující pracovní den.

| Typ profilu  | Spuštění    | Konec      |
|---------------|----------|----------|
| Flexibilita+         | 12:00 dop. | 08:00 dop. |
| Registrace příchodu      | 08:00 dop. | 08:00 dop. |
| Flexibilita-         | 08:00 dop. | 09:00 dop. |
| Standardní čas | 09:00 dop. | 11:30 dop. |
| Placená přestávka    | 11:30 dop. | 12:00 odp. |
| Flexibilita-         | 12:00 odp. | 04:00 odp. |
| Registrace odchodu     | 04:00 odp. | 04:00 odp. |
| Flexibilita+         | 04:00 odp. | 12:00 dop. |

V takovém případě chcete být schopni spravovat zůstatek pružného pracovní doby pracovníka na základě typů mezd. Proto je nutné nastavit možnost **Na základě typů mezd** na **Ano** na pružné skupině pracovníka.

Chcete-li zaznamenat pružnou pracovní dobu, je nutné definovat také nový typ mzdy. V tomto scénáři je typ mzdy nazván **FlexCnt**.

| Typ mzdy | popis  |
|----------|--------------|
| FlexCnt  | Počítání pružné pracovní doby |

Dále postupujte podle těchto kroků pro nastavení typu mzdy a přidání řádků nového typu mzdy do mzdového profilu.

1. Zvolte **Čas a docházka** \> **Setup** \> **Skupiny** \> **Pružné skupiny** a pak zvolte **Nový**.
2. V obou polích **Flexi+** **Flex-** zadejte nový typ mzdy **FlexCnt**.
3. Vyberte **Čas a docházka** \> **Nastavení** \> **Mzdové smlouvy** a poté vyberte **Řádky smlouvy**.
4. Pro **Pondělí**, pro typ profilu **Flex+** přidejte následující tři řádky.

    | Typ mzdy | popis  | Od | Do  | Minimum | Maximum | Koeficient |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Počítání pružné pracovní doby | 12:00 dop.  | 06:00 odp. | 00.00   | 00.00   | 1.00   |
    | FlexCnt  | Počítání pružné pracovní doby | 06:00 odp.  | 12:00 dop. | 00.00   | 02.00   | 1.50   |
    | FlexCnt  | Počítání pružné pracovní doby | 06:00 odp.  | 12:00 dop. | 02.00   | 06.00   | 2,00   |

    > [!NOTE]
    > Každý řádek se používá pro jiný časový interval a má jiný koeficient. Hodiny pružné pracovní doby, které pracovník odpracoval v časovém intervalu, se vynásobí koeficientem tohoto řádku. Například odpracované hodin od 18:00 do 20:00 se násobí 1,50. Tento koeficient se určuje v poli **Koeficient** na kartě **Obecné** stránky **Řádky mzdové smlouvy**.

Pracovník zadá následující registrace za daný den.

| Typ registrace deníku | Spuštění    | Konec      |
|---------------------------|----------|----------|
| Registrace příchodu                  | 07:00 dop. | 07:00 dop. |
| Výrobní úloha            | 07:00 dop. | 09:00 odp. |
| Registrace odchodu                 | 09:00 odp. | 09:00 odp. |

Částka, kterou je nutné zaplatit, se vypočítává na stránce **Schválit** stránky, na základě registrace pracovníka. Po výpočtu registrace můžete zobrazit výsledek na kartě **Časy**. V tomto scénáři vás zajímají následující pole.

| Flex + | Flex - | Čas  | Placený čas |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13.50 | 08.00    |

Množství času Flex+ je šest hodin a výpočet je založen na pružných zónách v časovém profilu. Tato částka se skládá z jedné hodiny času Flex+ od 07:00 do 08:00 a pěti hodin času Flex+ od 16:00 do 21:00.

Při převodu registrací zjistíte, že částka času Flex+ se změnila z 6,0 na 8,0 hodin.

| Flex + | Flex - | Čas  | Placený čas |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13.50 | 08.00    |

Tato změna proběhne po převodu, protože hodiny pružné pracovní doby byly vypočteny na základě typů mezd namísto času. Způsob výpočtu osmi hodin je vysvětlený v následující tabulce:

| Z verze     | Komu       | Čas | Koeficient    | Účet pružné pracovní doby |
|----------|----------|------|-----------|--------------|
| 07:00 dop. | 08:00 dop. | 1    | 1         | 1            |
| 04:00 odp. | 06:00 odp. | 2    | 1         | 2            |
| 06:00 odp. | 08:00 odp. | 2    | 1.5       | 3            |
| 08:00 odp. | 09:00 odp. | 1    | 2         | 2            |
|          |          |      | **Celkem** | **8**        |
