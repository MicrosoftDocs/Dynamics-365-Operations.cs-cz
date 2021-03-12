---
title: Příklady a logika sestavy stárnutí zásob
description: Toto téma uvádí několik příkladů, které ukazují, jak interpretovat výsledky sestavy stárnutí zásob.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983918"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Příklady a logika sestavy stárnutí zásob

[!include [banner](../includes/banner.md)]

Toto téma uvádí několik příkladů, které ukazují, jak interpretovat výsledky sestavy **stárnutí zásob**. Tato sestava kategorizuje hodnoty množství na skladě a zásob pro vybranou položku nebo skupinu položek do několika intervalů období. Toto téma také ukazuje vnitřní logiku sestavy.

Příklady v tomto tématu ukazují výsledky, které jsou prezentovány ve standardní sestavě **Stárnutí zásob**. Obecně však doporučujeme použít verzi [úložiště sestavy stárnutí zásob](inventory-aging-report-storage.md) této sestavy, zejména pokud máte mnoho položek a skladů, které je třeba zpracovat. Úložiště sestavy stárnutí zásob ukládá každý vygenerovaný přehled, zobrazuje výsledky jako interaktivní stránku a graf a umožňuje exportovat všechny uložené sestavy.

## <a name="sample-data-that-is-used-in-these-examples"></a>Ukázková data použitá v těchto příkladech

Příklady v tomto tématu jsou založeny na ukázkových datech skladových transakcí, které jsou popsány v této části.

### <a name="storage-dimension-setup"></a>Nastavení dimenze úložiště

Příklad systému obsahuje následující nastavení dimenzí úložiště.

| Jméno      | Aktivní | Fyzické zásoby | Finanční zásoby |
|-----------|--------|--------------------|---------------------|
| Lokalita      | Ano    | Ano                | Ano                 |
| Sklad | Ano    | Ano                | Žádný                  |

### <a name="inventory-model"></a>Model zásob

Skladový model vydaných produktů je v příkladu systému *FIFO* a nastavení **nákladové ceny** pro skladový model je *Zahrnout fyzickou hodnotu*.

### <a name="inventory-transactions"></a>Transakce zásob

Příklad systému obsahuje následující transakce zásob vydaného produktu, který má číslo položky *1000*.

| Odkaz      | Lokalita | Sklad | Příjem   | Výdej | Fyzické datum | Finanční datum | Množství | Částka nákladů | Fyzická částka nákladů |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Nákupní objednávka | 1    | 11        | Koupeno |       | 15. březen      | 15. březen       | 10       | 1 000       | 1 000                |
| Nákupní objednávka | 2    | 21        | Koupeno |       | 15. březen      | 15. březen       | 10       | 2,000       | 2,000                |
| Nákupní objednávka | 1    | 11        | Přijato  |       | 15. duben      |                | 5        |             | 375                  |
| Objednávka převozu | 1    | 11        |           | Prodáno  | 2. květen         | 2. květen          | -5       | -458,33     | -458,33              |
| Objednávka převozu | 1    | 12        | Koupeno |       | 2. květen         | 2. květen          | 5        | 458.33      | 458.33               |
| Prodejní objednávka    | 1    | 12        |           | Prodáno  | 3. květen         | 3. květen          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Jak se vypočítává množství a částky v jednotlivých intervalech období

Pomocí ukázkových dat, která jsou popsána v předchozích částech, můžete spustit sestavu **Stárnutí zásob**, která má následující nastavení:

- **K datu:** *9. května 2020*
- **Pracoviště:** *Zobrazit*
- **Sklad:** *Ne*
- **Číslo položky:** *Součet*
- **Doba stárnutí:** Toto pole nastavte tak, aby generovalo měsíční intervaly.

V takovém případě bude obsah vygenerované sestavy vypadat jako v následujícím příkladu.

<table>
<thead>
<tr>
    <th rowspan="2">Č. položky</th>
    <th rowspan="2">Lokalita</th>
    <th rowspan="2">Množství na skladě</th>
    <th rowspan="2">Hodnota položek na skladě</th>
    <th rowspan="2">Hodnota/množství skladových zásob</th>
    <th rowspan="2">Hodnota zásob</th>
    <th rowspan="2">Průměrné náklady na jednotku</th>
    <th colspan="2">5/8/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1:Množství</th>
    <th>P1:Částka</th>
    <th>P2:Množství</th>
    <th>P2:Částka</th>
    <th>P3:Množství</th>
    <th>P3:Částka</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1 000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1 000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>Celkem 1000</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

V této ukázkové sestavě si všimněte následujících podrobností:

- Hodnoty **Množství hodnoty zásob**, **Hodnota zásob** a **Průměrná jednotková cena** uvedené v sestavě jsou hodnoty dimenze finančních zásob (v tomto případě **Pracoviště**).

    Například pro pracoviště 1 obsahuje sestava následující informace:

    - Hodnota **Množství hodnoty zásob** je *14* (= 10 + 5 - 5 + 5 - 1).
    - Hodnota **Hodnota zásob** je *1,283.33* (= 1,000 + 375 - 458.33 + 458.33 - 91.67).
    - Hodnota **Průměrné náklady na jednotku** je *91,67*.
    - Hodnota **Hodnota na skladě** a hodnota **Částka** v jednotlivých intervalech období se vypočítává pomocí hodnoty **Průměrná jednotková cena**.

- Sestava určuje množství na skladě pro každý interval období sečtením celkového přijatého skladového množství pro každý interval období. Následně použije princip FIFO (první dovnitř, první ven) k odečtení celkového vydaného množství bez ohledu na model zásob, který položky používají.

Pokud stejnou sestavu spustíte znovu, ale tentokrát nastavíte pole **Pracoviště** i **Sklad** na *Zobrazení*, bude nová sestava vypadat jako v následujícím příkladu.

<table>
<thead>
<tr>
    <th rowspan="2">Č. položky</th>
    <th rowspan="2">Lokalita</th>
    <th rowspan="2">Sklad</th>
    <th rowspan="2">Množství na skladě</th>
    <th rowspan="2">Hodnota položek na skladě</th>
    <th rowspan="2">Hodnota/množství skladových zásob</th>
    <th rowspan="2">Hodnota zásob</th>
    <th rowspan="2">Průměrné náklady na jednotku</th>
    <th colspan="2">5/8/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1:Množství</th>
    <th>P1:Částka</th>
    <th>P2:Množství</th>
    <th>P2:Částka</th>
    <th>P3:Množství</th>
    <th>P3:Částka</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1 000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1 000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1 000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>Celkem 1000</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Tentokrát je pracoviště 1 rozděleno na dva řádky, jeden pro sklad 11 a jeden pro sklad 12. Hodnoty **Množství hodnoty zásob**, **Hodnota zásob** a **Průměrná jednotková cena** uvedené v sestavě jsou však stejné, protože **Sklad** není dimenze finančních zásob.

Dále si všimněte, že distribuce množství na pracovišti 1 je odlišná. V první sestavě, kterou jste spustili, systém ignoroval příkaz k převodu, ke kterému došlo na stejném pracovišti, a odečetl množství prodejní faktury z intervalu období **31. 3. 2020 - 3. 1. 2020** na pracovišti 1. V nové sestavě však systém odečte z prodejní faktury množství z intervalu období **5. 5. 2012 - 5. 1. 2012** ve skladu 12.

## <a name="effects-of-inventory-closing"></a>Dopady uzávěrky skladu

Pokud spustíte uzávěrku zásob na květen a poté znovu spustíte předchozí sestavu, ale nastavíte hodnotu v poli **K datu** na *31. května 2020*, všimnete si následujících výsledků:

- Hodnoty **Hodnota zásob** a **Průměrné jednotkové náklady** se aktualizují.
- Hodnota **Hodnota na skladě** a všechny hodnoty **Částka** v každém intervalu období se aktualizují odpovídajícím způsobem.

Nová sestava bude vypadat podobně jako v následujícím příkladu.

<table>
<thead>
<tr>
    <th rowspan="2">Č. položky</th>
    <th rowspan="2">Lokalita</th>
    <th rowspan="2">Sklad</th>
    <th rowspan="2">Množství na skladě</th>
    <th rowspan="2">Hodnota položek na skladě</th>
    <th rowspan="2">Hodnota/množství skladových zásob</th>
    <th rowspan="2">Hodnota zásob</th>
    <th rowspan="2">Průměrné náklady na jednotku</th>
    <th colspan="2">5/31/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1:Množství</th>
    <th>P1:Částka</th>
    <th>P2:Množství</th>
    <th>P2:Částka</th>
    <th>P3:Množství</th>
    <th>P3:Částka</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1 000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1 000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1 000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>Celkem 1000</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>
