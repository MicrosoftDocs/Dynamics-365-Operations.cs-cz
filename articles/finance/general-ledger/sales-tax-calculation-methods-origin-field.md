---
title: Metody výpočtu DPH v poli Zdroj
description: Tento článek vysvětluje možnosti v poli Zdroj na stránce Kódy DPH, a postup výpočtu DPH na základě vybrané možnosti pro kód DPH.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d326480cc03d80d1ce27f8762e300dca3b0d325e
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770636"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Metody výpočtu DPH v poli Zdroj

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje možnosti v poli Zdroj na stránce Kódy DPH, a postup výpočtu DPH na základě vybrané možnosti pro kód DPH.

Pro každý vytvořený kód DPH na stránce Kódy DPH je nutné vybrat metodu výpočtu, která je použita pro částku základu daně v poli Zdroj.

## <a name="percentage-of-net-amount"></a>Procento z čisté částky
Metoda výpočtu Procento z čisté částky je výchozí hodnotou v poli Zdroj. DPH se počítá jako procento z částky nákupu nebo prodeje bez všech jiných DPH.
### <a name="example"></a>Příklad

Sazba daně je 25%. Řádek faktury zobrazuje množství 10 položek po $1,00 za kus a odběrateli je poskytnuta desetiprocentní řádková sleva. Čistá částka: (10 × 1,00) -10 % = 9,00 DPH: 9,00 x 25 % = 2,25 Celková částka: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Procento z hrubé částky
Pokud vyberete metodu Procento z hrubé částky, DPH bude vypočteno jako procento z hrubé částky prodeje. Hrubá částka je čistá částka na řádku plus všechny daně a poplatky pro řádek kromě jedné daně, kde Zdroj = procento z hrubé částky.
### <a name="example"></a>Příklad

Daňový úřad na položku uložil zvláštní cla. Částky cla se před výpočtem DPH přičtou k čisté částce. Použijme následující kódy DPH:
-   CLO 1 = 10% s pomocí metody výpočtu procenta z čisté částky
-   CLO 2 = 20% s pomocí metody výpočtu procenta z čisté částky
-   DPH = 25% s pomocí metody výpočtu procenta z hrubé částky

Pokud je čistá částka 10,00, pak CLO 1 = 1,00 (10,00 x 10 %) a CLO 2 = 2,00 (10,00 x 20 %). Částky budou vypadat následovně: Hrubá částka: Čistá částka + Částka cla 1 + částka cla 2 (10,00 + 1,00 + 2,00) = 13,00 DPH = 13,00 x 25 % = 3,25 Celkové clo a DPH: 1,00 + 2,00 + 3,25 = 6,25 Celková částka: 10,00 + 6,25 = 16,25

| **Poznámka**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pro transakci lze použít pouze jeden daňový kód, kde Zdroj = procento z hrubé částky. Je-li více než jeden takový kód daně určen pro transakci, zobrazí se chyba a DPH nemůže být vypočítána. |


<a name="percentage-of-sales-tax"></a>Procento DPH
-----------------------

Vyberete-li v poli Zdroj hodnotu Procento DPH, DPH se vypočítá jako procento z DPH vybrané v části Prodejní daň v poli DPH. DPH, která je vybrána v části Prodejní daň v poli DPH se vypočítá jako první. Druhá DPH bude vypočítána následovně na základě první částky DPH.
### <a name="example"></a>Příklad

Použijme následující kódy DPH:
-   CLO 1 = 10% s pomocí metody Procento z čisté částky
-   CLO 2 = 20 % pomocí metody Procento z DPH s vybranou možností Clo 1 v části Prodejní daň v poli DPH
-   DPH = 25% s pomocí metody Procento z hrubé částky

Čistá částka: 10,00 Clo 1: 10,00 x 10 % = 1,00 Clo 2: 1,00 x 20 % = 0,20 Hrubá částka: 10,00 + 1,00 + 0,20 = 11,20 DPH: 11,20 x 25 % = 2,80 Celkové clo a DPH: 1,00 + 0,20 + 2,80 = 4,00 Celková částka: 10,00 + 4,00 = 14,00

| **Poznámka**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Při výpočtu daně není možné použít více úrovní daně. Daň nelze vypočítat na základě DPH, které je již vypočteno na základě jiné daně. U transakce lze vypočítat více jednotlivých úrovní daně u kódů daně. |

## <a name="amount-per-unit"></a> Částka za jednotku
Vyberete-li částky za jednotku v poli Zdroj, DPH se vypočítá jako pevná částka za jednotku vynásobená množstvím zadaným na řádku dokladu. Jednotka musí být zvolena v poli Jednotka. Částka na jednotku je uvedena na stránce Hodnoty kódu DPH.
### <a name="example"></a>Příklad

Kód DPH je nastaven jako: 1,20 USD za jednotku = balení Na řádku prodejní faktury je prodáno 25 balení položky DPH bude vypočtena jako hodnota 25 x 1,20 = 30,00

| **Poznámka**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Je-li transakce zadána u jiné jednotky než jednotky zadané v kódu prodejní daně, převede se automaticky podle pravidel převodů jednotek, které jsou nastaveny na stránce Převody jednotek. |

###  <a name="amount-per-unit-additional-option"></a> Částka za jednotku, doplňková možnost

Na kartě Výpočet můžete určit, zda je daň vypočítaná jako částka na jednotku před dalšími kódy DPH, a přidána k čisté částce před vypočítáním ostatních kódů DPH, kde Zdroj = procento z čisté částky.

### <a name="examples"></a>Příklad

Předpokládejme, že vypočítáme 2 kódy daně u transakce:

-   CLO: Původ = částka za jednotku a prodejní daň, hodnota je nastavena na 5,00 za jednotku = kusy
-   DPH: Původ = jak je uvedeno v následujících příkladech, hodnota je nastavena na hodnotu 25 %

Prodáme 1 kus položky za jednotkovou cenu ve výši 10,00
#### <a name="example-1"></a>Příklad 1

DPH: Původ = metoda Procento z hrubé částky Možnost Výpočet před DPH nemá žádný vliv, protože DPH se počítá jako procento z hrubé částky. CLO: 1 x 5,00 = 5,00 Hrubá částka: 10,00 + 5,00 = 15,00 DPH: 15,00 x 25 % = 3,75 Celková částka DPH: 5,00 + 3,75 = 8,75 Celková částka: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Příklad 2

DPH: Původ = procento z čisté částky Možnost Výpočet před DPH není vybrána pro výpočet cla. Čistá částka: 10,00 Clo: 1 x 5,00 = 5,00 DPH: 10,00 x 25 % = 2,50 Celková částka DPH: 5,00 + 2,50 = 7,50 Celková částka: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Příklad 3

DPH: Původ = procento z čisté částky Možnost Výpočet před DPH je vybrána pro výpočet cla. Čistá částka: 10,00 Clo: 1 x 5,00 = 5,00 DPH: (10,00 + 5,00) x 25 % = 3,75 Celková částka DPH: 5,00 + 3,75 = 8,75 Celková částka: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Příklad 4

Výsledek příkladu 3 a příkladu 1 je stejný, protože se počítá pouze s jedním clem. Předpokládejme, že máte dvě cla, a pouze jedno z nich je součástí čisté částky pro výpočet DPH: Clo 1: 5,00, pomocí metody Částka za jednotku a možnost Výpočet před DPH je vybrána Clo 2: 2,50, pomocí metody Částka za jednotku a možnost Výpočet před DPH není vybrána DPH: 25 %, pomocí metody Procento čisté částky Čistá částka: 10,00 Clo 1: 1 x 5,00 = 5,00 Clo 2: 1 x 2,50 = 2,50 Čistá částka podléhá DPH: 10,00 + 5,00 = 15,00 DPH: 15,00 x 25 % = 3,75 Celková DPH včetně cel: 5,00 + 2,50 + 3,75 = 11,25 Celková částka: 10,00 + 11,25 = 21,25 DPH 25 % je vypočítáno pro součet čisté částky (10,00) + cla 1 (5,00) = 15,00. Clo 2 je k částce daně přičteno po výpočtu DPH.

## <a name="calculated-percentage-of-net-amount"></a> Vypočtené procento čisté částky
Vypočtené procento čisté částky řídí výpočet daně jiným způsobem v závislosti na nastavení parametru Částky včetně DPH pro deník nebo doklad.
### <a name="example-1"></a>Příklad 1

Dokument / deník je nastaven na Částky včetně DPH = Ano Částka řádku transakce: 10,00 Sazba daně: 25 % DPH: Částka řádku transakce x sazba daně (10,00 x 25 %) = 2,50 Částka základu daně (původ částky): Částka řádku transakce - prodejní daň (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Příklad 2

Dokument / deník je nastaven na Částky včetně DPH = Ne Částka řádku transakce: 10,00 Sazba daně: 25 % DPH: (Částka řádku transakce x sazba daně) / (100 - sazba daně) (10,00 x 25 %) / (100 % - 25 %) = 3,33 Částka základu daně (původ částky): Částka řádku transakce = 10,00



<a name="additional-resources"></a>Další zdroje
--------

[Sazby DPH na základě polí Základ marže a Metody výpočtu](marginal-base-field.md)

[Možnosti výpočtu celé částky a intervalu pro kódy daně z prodeje](whole-amount-interval-options-sales-tax-codes.md)



