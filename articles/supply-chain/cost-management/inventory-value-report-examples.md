---
title: Příklady a logika sestavy hodnoty zásob
description: Tento článek poskytuje některé příklady výsledků, které jsou uvedeny v každém typu sestavy hodnoty zásob. Sestavy hodnoty zásob poskytují podrobnosti o fyzických a finančních množstvích a částkách vašich zásob.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877646"
---
# <a name="inventory-value-report-examples-and-logic"></a>Příklady a logika sestavy hodnoty zásob

[!include [banner](../includes/banner.md)]

Sestavy hodnoty zásob poskytují podrobnosti o fyzických a finančních množstvích a částkách vašich zásob. Tento článek poskytuje některé příklady výsledků, které jsou uvedeny v každém typu sestavy hodnoty zásob.

Další informace o tom, jak generovat a používat jednotlivé typy sestav hodnoty zásob, viz [Sestavy hodnoty zásob](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Ukázková data použitá v těchto příkladech

Příklady v tomto článku jsou založeny na ukázkových datech skladových transakcí, které jsou popsány v této části.

### <a name="storage-dimension-setup"></a>Nastavení dimenze úložiště

Příklad systému obsahuje následující nastavení dimenzí úložiště.

| Jméno | Aktivní | Fyzické zásoby | Finanční zásoby |
|---|---|---|---|
| Lokalita | Ano | Ano | Ano |
| Sklad | Ano | Ano | Ne |

### <a name="inventory-model"></a>Model zásob

Skladový model vydaných produktů je v příkladu systému *FIFO* a pole **Nákladové ceny** pro skladový model je nastaveno na *Zahrnout fyzickou hodnotu*.

### <a name="inventory-transactions"></a>Skladové transakce

Příklad systému obsahuje následující transakce zásob vydaného produktu, který má číslo položky *B0001*.

| Odkaz | Lokalita | Sklad | Příjemka | Problém | Fyzické datum | Finanční datum | Množství | Částka nákladů | Fyzická částka nákladů |
|---|---|---|---|---|---|---|---|---|---|
| Nákupní objednávka | 1 | 11 | Koupeno | | 15. březen | 15. březen | 10 | 1 000 | 1 000 |
| Nákupní objednávka | 2 | 21 | Koupeno | | 15. březen | 15. březen | 10 | 2,000 | 2,000 |
| Nákupní objednávka | 1 | 11 | Přijato | | 15. duben | | 5 | | 375 |
| Objednávka převozu | 1 | 11 | | Prodáno | 2. květen | 2. květen | -5 | -458,33 | -458,33 |
| Objednávka převozu | 1 | 12 | Koupeno | | 2. květen | 2. květen | 5 | 458.33 | 458.33 |
| Prodejní objednávka | 1 | 12 | | Prodáno | 3. květen | 3. květen | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Konfigurace sestavy hodnot zásob

Ukázkový systém zahrnuje konfiguraci sestavy hodnot zásob, která má následující nastavení:

- **Rozsah:**  *Datum zaúčtování*
- **Zásoby:** *Ano*
- **Vypočítejte průměrné jednotkové náklady:** *Ano*
- **Celkové množství a hodnota:** *Ano*
- **Web, zobrazení:** *Vybraný*
- **ID zdroje, zobrazení:** *Ano*
- **Úroveň:** *Součty*

## <a name="inventory-value-report-example-1"></a>Příklad 1 sestavy hodnot zásob

Následující tabulka a ilustrace ukazují výsledky, když použijete ukázková data a konfiguraci sestavy, které jsou popsány dříve v tomto článku.

| Typ zdroje | Prostředek | Web | Reference | Zásoby: Finanční množství | Zásoby: Finanční částka | Zásoby: Zaúčtované fyzické množství | Zásoby: Zaúčtovaná fyzická částka | Zásoby: Množství | Zásoby: Částka | Průměrné náklady na jednotku |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiál | B0001 | 1 | Konečný zůstatek | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Materiál | B0001 | 2 | Konečný zůstatek | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standardní sestava hodnot zásob pro příklad 1

Následující obrázek ukazuje standardní sestavu **Hodnota zásob** pro například 1. (Výběrem obrázku otevřete větší verzi.)

[![Sestava hodnot zásob pro příklad 1.](media/inventory-value-report-ex1-small.png "Sestava hodnot zásob pro příklad 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Sestava Úložiště sestavy hodnot zásob pro příklad 1

Následující obrázek ukazuje sestavu **Úložiště sestav Hodnota zásob** pro například 1. (Výběrem obrázku otevřete větší verzi.)

[![Sestava Úložiště sestavy hodnot zásob pro příklad 1.](media/inventory-value-report-storage-ex1-small.png "Sestava Úložiště sestavy hodnot zásob pro příklad 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Příklad 2 sestavy hodnot zásob

Následující tabulka a ilustrace ukazují výsledky, když použijete ukázková data, která jsou popsána dříve v tomto článku, ale změníte hodnotu pole **Úroveň** na *Transakce* v konfiguraci sestavy a nastavíte pole **Od data** na *15. března* při spuštění sestavy.

| Typ zdroje | Prostředek | Lokalita | Datum | Číslo | Odkaz | Zásoby: Finanční množství | Zásoby: Finanční částka | Zásoby: Zaúčtované fyzické množství | Zásoby: Zaúčtovaná fyzická částka | Zásoby: Množství | Zásoby: Částka |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiál | B0001 | 1 | 3/15/2021 | 00000126 | Nákupní objednávka | 0,00 | 0,00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| Materiál | B0001 | 1 | 3/15/2021 | 00000126 | Nákupní objednávka | 10.00 | 1,000.00 | -10,00 | -1 000,00 | **0.00** | **0.00** |
| Materiál | B0001 | 1 | 4/15/2021 | 00000128 | Nákupní objednávka | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materiál | B0001 | 1 | 5/2/2021 | 000003 | Dodávka převodního příkazu | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Materiál | B0001 | 1 | 5/2/2021 | 000003 | Příjem převodního příkazu | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiál | B0001 | 1 | 5/3/2021 | 000835 | Prodejní objednávka | 0,00 | 0,00 | -1,00 | -91,67 | **-1.00** | **-91.67** |
| Materiál | B0001 | 1 | 5/3/2021 | 000835 | Prodejní objednávka | -1,00 | -91,67 | 1,00 | 91.67 | **0.00** | **0.00** |
| Materiál | B0001 | 2 | 3/15/2021 | 00000127 | Nákupní objednávka | 0,00 | 0,00 | 10.00 | 2,000.00 | **10.00** | **2,000.00** |
| Materiál | B0001 | 2 | 3/15/2021 | 00000127 | Nákupní objednávka | 10.00 | 2,000.00 | -10,00 | -2 000,00 | **0.00** | **0.00** |
| Materiál | B0001 | 2 | 5/2/2021 | 000003 | Dodávka převodního příkazu | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiál | B0001 | 2 | 5/2/2021 | 000003 | Příjem převodního příkazu | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standardní sestava hodnot zásob pro příklad 2

Následující obrázek ukazuje standardní sestavu **Hodnota zásob** pro například 2. (Výběrem obrázku otevřete větší verzi.)

[![Sestava hodnot zásob pro příklad 2.](media/inventory-value-report-ex2-small.png "Sestava hodnot zásob pro příklad 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Sestava Úložiště sestavy hodnot zásob pro příklad 2

Následující obrázek ukazuje sestavu **Úložiště sestav Hodnota zásob** pro například 2. (Výběrem obrázku otevřete větší verzi.)

[![Sestava Úložiště sestavy hodnot zásob pro příklad 2.](media/inventory-value-report-storage-ex2-small.png "Sestava Úložiště sestavy hodnot zásob pro příklad 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Příklad 3 sestavy hodnot zásob

Doporučujeme spouštět sestavy hodnot zásob po přepočtu nebo uzávěrce zásob, abyste měli k dispozici transakce a částky, kterých se přepočet nebo uzávěrka zásob týká.

V následujících podsekcích jsou uvedeny přehledy hodnoty zásob, které se generují po uzavření inventáře do 30. května.

### <a name="example-3-when-the-totals-level-is-used"></a>Příklad 3 při použití úrovně Součty

Následující tabulka ukazuje výsledky, když použijete ukázková data a konfiguraci sestavy, které jsou popsány dříve v tomto článku. (V této konfiguraci sestavy je pole **Úroveň** nastaveno na *Součty*.)

| Typ zdroje | Prostředek | Lokalita | Odkaz | Zásoby: Finanční množství | Zásoby: Finanční částka | Zásoby: Zaúčtované fyzické množství | Zásoby: Zaúčtovaná fyzická částka | Zásoby: Množství | Zásoby: Částka | Průměrné náklady na jednotku |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiál | B0001 | 1 | Konečný zůstatek | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Materiál | B0001 | 2 | Konečný zůstatek | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Příklad 3 při použití úrovně Transakce

Následující tabulka ukazuje výsledky, když použijete ukázková data popsaná dříve v tomto článku, ale změníte hodnotu pole **Úroveň** na *Transakce* v konfiguraci sestavy.

| Typ zdroje | Prostředek | Lokalita | Datum | Číslo | Odkaz | Zásoby: Finanční množství | Zásoby: Finanční částka | Zásoby: Zaúčtované fyzické množství | Zásoby: Zaúčtovaná fyzická částka | Zásoby: Množství | Zásoby: Částka |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiál | B0001 | 1 | 3/15/2021 | 00000126 | Nákupní objednávka | 0,00 | 0,00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| Materiál | B0001 | 1 | 3/15/2021 | 00000126 | Nákupní objednávka | 10.00 | 1,000.00 | -10,00 | -1 000,00 | 0,00 | 0,00 |
| Materiál | B0001 | 1 | 4/15/2021 | 00000128 | Nákupní objednávka | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materiál | B0001 | 1 | 5/2/2021 | 000003 | Dodávka převodního příkazu | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiál | B0001 | 1 | 5/2/2021 | 000003 | Příjem převodního příkazu | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiál | B0001 | 1 | 5/3/2021 | 000835 | Prodejní objednávka | 0,00 | 0,00 | -1,00 | -91,67 | -1,00 | -91,67 |
| Materiál | B0001 | 1 | 5/3/2021 | 000835 | Prodejní objednávka | -1,00 | -91,67 | 1,00 | 91.67 | 0,00 | 0,00 |
| Materiál | B0001 | 1 | 5/31/2021 | 000835 | Prodejní objednávka | 0,00 | -8,33 | 0,00 | 0,00 | 0,00 | -8,33 |
| Materiál | B0001 | 1 | 5/31/2021 | 000003 | Dodávka převodního příkazu | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Materiál | B0001 | 1 | 5/31/2021 | 000003 | Příjem převodního příkazu | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiál | B0001 | 2 | 3/15/2021 | 00000127 | Nákupní objednávka | 0,00 | 0,00 | 10.00 | 2,000.00 | 10.00 | 2,000.00 |
| Materiál | B0001 | 2 | 3/15/2021 | 00000127 | Nákupní objednávka | 10.00 | 2,000.00 | -10,00 | -2 000,00 | 0,00 | 0,00 |
| Materiál | B0001 | 2 | 5/2/2021 | 000003 | Dodávka převodního příkazu | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiál | B0001 | 2 | 5/2/2021 | 000003 | Příjem převodního příkazu | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiál | B0001 | 2 | 5/31/2021 | 000003 | Dodávka převodního příkazu | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiál | B0001 | 2 | 5/31/2021 | 000003 | Příjem převodního příkazu | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
