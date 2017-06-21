---
title: "Nastavení úrokových sazeb pro kód úroku"
description: "Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b9595cf287f59ddb7543f36b2b541200f70a9c96
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Nastavení úrokových sazeb pro kód úroku

[!include[banner](../includes/banner.md)]


Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti.

Můžete nastavit jediný kód úroku a použít ho pro více účetních profilů zákazníků, účtovacích kódů nebo určité řady faktur. Při změně podrobností kódu úroku, všechny funkce, které používají kód automaticky implementují změny pro nové transakce. Pro každý kód úroku můžete nastavit dva typy sazeb:
-   Sazby pro úrokové příjmy – představují výnosy, které jsou vytvořené účtováním úroků na fakturách nebo oznámeních úroků.
-   Sazby pro úrokové platby − představují náklady zaplacené za úrok u dobropisů.

Oba tyto typy sazeb mohou existovat ve stejnou dobu a ve stejném kódu úroku. Úrokové sazby mohou být založeny na třech typech výpočtů:
-   Úrok podle procent.
-   Úrok podle částky.
-   Úrok podle rozsahu, jehož výsledkem je jednotná procentní sazba nebo částka.

Při použití kódu úroku, který se používá k výpočtu úroku, je pro každou úrokovou sazbu platnou v době, kdy platba překročila datum splatnosti transakce, vytvořeno samostatné oznámení úroků. K nastavení úrokových sazeb pro úroky, které můžete získat účtováním úroků, slouží karta **Zisky** na stránce **Kód úroku**. Na kartě **Platby** můžete nastavit úrokové sazby pro úroky, které platíte.

## <a name="interest-rates-based-on-a-percentage"></a>Úrokové sazby podle procent
Můžete nastavit úrokové sazby pro výpočet zadané procentní hodnoty.

-   Částka úroku platí pro všechny měny.
-   Volitelně lze zadat omezení částky úroku.
-   Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Procento**.

Pokud chcete například nastavit kód úroku, který stanoví 5% úrok po uplynutí každých dvou měsíců, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 2 a vyberte možnost **Měsíc**.

## <a name="interest-rates-based-on-amounts"></a>Úrokové sazby podle částek
Můžete nastavit úrokové sazby pro výpočet určité částky podle měny.
-   Částka úroku se zadává pro každou měnu v kódu úroku.
-   Volitelně lze zadat omezení částky úroku.
-   Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Částka **.

Pokud chcete například nastavit kód úroku, který stanoví úrok 25,00 po uplynutí každých 20 dnů, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 20 a vyberte možnost **Den**.

## <a name="interest-rates-based-on-ranges"></a>Úrokové sazby podle rozsahů
Můžete nastavit úrokové sazby, které jsou závislé na částce po splatnosti, počtu dní, po které je částka po splatnosti nebo počtu měsíců, po které je částka po splatnosti.
-   Na kartě **Zisky podle měny** můžete určit specifické nastavení úroků pro každou měnu. Na stejném místě se určuje také rozsah.
-   K přidání řádků, které představují rozsahy, které chcete nastavit, použijte tlačítko **Rozsahy**. Hodnota **Od** představuje začátek rozsahu a číslo **Hodnota úroků** představuje procento nebo částku (podle výběru provedeného v poli **Vypočítat úrok podle** na stránce **Nastavení kódů úroku**).

## <a name="example-1-interest-by-range--amount"></a>Příklad 1: Úroky podle rozsahu = částka
Nastavíte kód úroku, který přiřadí úrok jednou za každé tři měsíce, po které platba faktury překročí její splatnost. Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů částky. Hodnota úroku bude 1 % pro fakturační částky do 1 000,00, 2 procenta pro částky od 1 001,00 do 5 000,00 a 3 % pro částky větší než 5 000,00. Hodnoty polí pro kód úroku nastavíte následovně.

| **Název pole**                  | **Hodnota pole** |
|---------------------------------|-----------------|
| **Kód úroku**               | 3M%ByAmt        |
| **Vypočítat úroky jednou za**    | 3/měsíc         |
| **Úrok podle rozsahu**           | Částka          |
| **Vypočítat úrok podle** | Procento      |

Takto nastavíte rozsah informací.

| **Od hodnoty** | **Hodnota úroků** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Příklad 2: Úrok podle rozsahu = dny
--------------------------------------------------

Nastavíte kód úroku, který přiřadí úrok jednou za každých 15 dnů, po které platba faktury překročí její splatnost. Chcete založit výpočet na hodnotě částky úroku podle stupňovitých intervalů dnů. Hodnota úroku bude 10,00 za každých 15 dní během prvních 60 dnů, 15,00 za každých 15 dní od 61. do 90. dne a 20,00 za každých 15 dní od 91. dne. Hodnoty polí pro kód úroku nastavíte následovně.

| **Název pole**                  | **Hodnota pole** |
|---------------------------------|-----------------|
| **Kód úroku**               | 15DAmtXDay      |
| **Vypočítat úroky jednou za**    | 15/den          |
| **Úrok podle rozsahu**           | Dny            |
| **Vypočítat úrok podle** | Částka          |

Takto nastavíte rozsah informací.

| **Od hodnoty** | **Hodnota úroků** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Příklad 3: Úrok podle rozsahu = měsíce
----------------------------------------------------

Nastavíte kód úroku, který přiřadí úrok jednou za každý měsíc, po které platba faktury překročí její splatnost. Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů měsíců. Hodnota úroků bude 1,5 % měsíčně za první tři měsíce po splatnosti, 2,0 % měsíčně za druhé tři měsíce a 2,5 % měsíčně za každý měsíc po prvních šesti měsících. Hodnoty polí pro kód úroku nastavíte následovně.

| **Název pole**                  | **Hodnota pole** |
|---------------------------------|-----------------|
| **Kód úroku**               | 1M%ByMth        |
| **Vypočítat úroky jednou za**    | 1/měsíc         |
| **Úrok podle rozsahu**           | Měsíce          |
| **Vypočítat úrok podle** | Procento      |

Takto nastavíte rozsah informací.

| **Od hodnoty** | **Hodnota úroků** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Nové verze
Kódy úroků mají časovou platnost. Pokud chcete upravit úrokové sazby, můžete vytvořit **novou verzi**, která bude účinná k budoucímu datu.

K zobrazení různých verzí můžete použít volbu nabídky **K datu** a vybrat koncové datum. Také můžete výběrem možnosti **Zobrazit všechny záznamy** zobrazit na stránce všechny kódy úroků.




