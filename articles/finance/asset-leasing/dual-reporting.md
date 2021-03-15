---
title: Duální vykazování
description: Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003174"
---
# <a name="dual-reporting"></a>Duální vykazování

[!include [banner](../includes/banner.md)]

Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku. Znalost účtovacích vrstev v Microsoft Dynamics 365 Finance je nutná a příklad bude lépe srozumitelný.

## <a name="example"></a>Příklad

Následující příklad provádí účtování pro leasing podle italského statutárního výkaznictví pomocí metody hotovostního základu i metod vykazování podle IFRS. Společnost musí založit tři účetní knihy, které zohlední jak italské zákonné požadavky, tak požadavky IFRS 16. Jedna kniha je vyžadována pro IFRS 16, jedna kniha je vyžadována pro zákonné požadavky a jedna kniha je vyžadována k automatickému stornování statutárních účtování. Knihy jsou vytvořeny tak, jak je uvedeno v následujících tabulkách.

**Kniha IFRS 16**

Kniha IFRS 16 je vytvořena v souladu s účetním standardem IFRS 16. Všechny položky, které jsou zaúčtovány v této knize, budou zaúčtovány do vlastní vrstvy.

| Jméno                                    | popis    |
|-----------------------------------------|----------------|
| Typ knihy                               | IFRS 16        |
| Popis knihy                        | IFRS 16        |
| Účtovací vrstva                           | Vlastní vrstva 1 |
| Typ leasingu                              | Finance        |
| Rámec účetnictví                    | IFRS 16        |
| Nastavení doby trvání leasingu / očekávané doby použitelnosti         | 0,00           |
| Nastavení současné hodnoty / reálné hodnoty majetku | 0,00           |
| Krátkodobá prahová hodnota                    | 12             |
| Nízká prahová hodnota                     | 5,000.00       |
| Platba dodavateli                           | Žádný             |

**Statutární kniha**

Statutární kniha je hotovostní kniha, kde společnost bude účtovat výdaje na leasing jako částku hotovosti, která se každý měsíc platí za nájem. Tato kniha nevytvoří používaný majetek ani leasingový závazek.

| Jméno                                    | popis |
|-----------------------------------------|-------------|
| Typ knihy                               | Statutární   |
| Popis knihy                        | Místní GAAP  |
| Účtovací vrstva                           | Aktuální     |
| Typ leasingu                              | Automatické   |
| Rámec účetnictví                    | Hotovostní základ  |
| Nastavení doby trvání leasingu / očekávané doby použitelnosti         | 0,00        |
| Nastavení současné hodnoty / reálné hodnoty majetku | 0,00        |
| Krátkodobá prahová hodnota                    | 0           |
| Nízká prahová hodnota                     | 0           |
| Platba dodavateli                           | Žádný          |

**Statutární stornovací kniha**

Statutární stornovací kniha je sestavena stejným způsobem jako statutární kniha.

| Jméno                                    | popis                    |
|-----------------------------------------|--------------------------------|
| Typ knihy                               | Statutární – storno           |
| Popis knihy                        | Kniha pro stornování statutární knihy |
| Účtovací vrstva                           | Vlastní vrstva 1                 |
| Typ leasingu                              | Automatické                      |
| Rámec účetnictví                    | Hotovostní základ                     |
| Nastavení doby trvání leasingu / očekávané doby použitelnosti         | 0,00                           |
| Nastavení současné hodnoty / reálné hodnoty majetku | 0,00                           |
| Krátkodobá prahová hodnota                    | 0                              |
| Nízká prahová hodnota                     | 0                              |
| Platba dodavateli                           | Žádný                             |

V tomto příkladu byl vytvořen leasing, který má následující nastavení na kartách **Obecné** a **Řádky platebního kalendáře**.

**Karta Obecné**

| Pole                      | Hodnota            |
|----------------------------|------------------|
| Přírůstková výpůjční úroková sazba | 5 %               |
| Datum zahájení          | 1. 1. 2020         |
| Skupina leasingu                | Budovy        |
| Dodavatel                     | 1001             |
| Reálná hodnota majetku    | 245,000          |
| Očekávaná doba použitelnosti majetku          | 120              |
| Typ anuity               | Běžná anuita |
| Interval úročení       | Měsíčně          |

**Karta Řádky platebního kalendáře**

| Pole             | Hodnota      |
|-------------------|------------|
| Počáteční datum        | 1. 1. 2020   |
| Interval období   | Měsíce     |
| Období           | 24         |
| Koncové datum          | 31. 12. 2020 |
| Četnost plateb | Měsíčně    |
| Částka platby    | 1 000      |

Chcete-li tento leasing započítat do dvou rámců, použijete aktuální účtovací vrstvu a vlastní účtovací vrstvu. Následující tabulka ukazuje příklad každé položky deníku, která je potřeba pro věrné zobrazení financí podle každého standardu výkaznictví. Podrobný popis každé položky deníku pro první měsíc leasingu je poskytnut později.

<table>
<thead>
<tr>
<th rowspan='3'>Číslo účtu</th>
<th rowspan='3'>popis</th>
<th colspan='3'>Statutární kniha (aktuální vrstva)</th>
<th rowspan='3'>Celková aktuální vrstva</th>
<th>Stornovací kniha (vlastní vrstva)</th>
<th colspan='4'>Kniha IFRS 16 (vlastní vrstva)</th>
<th rowspan='3'>Aktuální vrstva + vlastní vrstva celkem</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Výdaje leasingu</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>−1 000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankovní poplatek</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>Výdaje DPH</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Clearingový účet</td>
<td>−1 000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>−1 000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Závazky</td>
<td></td>
<td>-1008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Používaný majetek</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Povinnost finančního leasingu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22 794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21 888,87</td>
</tr>
<tr>
<td>8</td>
<td>Výdaje na úroky</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Hotovost</td>
<td></td>
<td></td>
<td>-1008,00</td>
<td>-1008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1008,00</td>
</tr>
<tr>
<td>10</td>
<td>Odpisové výdaje</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Akumulovaný odpis</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Jak ukazuje předchozí tabulka, jsou potřeba tři knihy pro vykazování v rámci statutárního výkaznictví i výkaznictví podle IFRS.

- Statutární kniha zaznamenává leasingové splátky podle pravidel pro hotovostní účetnictví v aktuální vrstvě.
- Statutární stornovací kniha stornuje položky statutárního deníku.
- Kniha IFRS 16 vytváří položky deníku, které jsou vyžadovány podle IFRS 16.

Leasing musíte zadat pouze jednou. Poté můžete otevřít stránku **Knihy**, kde jsou všechny knihy, které jsou přidruženy k leasingu.

> [!NOTE]
> Když vytvoříte knihy, všechny tři musí být přidruženy ke stejnému záznamu leasingu.

První položka deníku zaznamenává výdaje na leasing podle statutární knihy. Platby můžete vytvářet v dávce nebo výběrem platebního kalendáře ve statutární knize.

V tomto příkladu se pro statutární knihu z platebního kalendáře vytvoří následující položka deníku.

### <a name="lease-payment--1312020--je-100"></a>Leasingová splátka – 31. 1. 2020 – JE 100

| Typ účtu | Číslo účtu | Vrstva   | Popis účtu | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Aktuální | Výdaje leasingu       | 1,000.00 |          |
| Ledger       | 4              | Aktuální | Clearingový účet    |          | 1,000.00 |

Úředník pro závazky používá standardní funkce Dynamics 365 k vytvoření fakturu pro zaplacení leasingu mimo leasing majetku. Nicméně místo výběru **Výdaje na leasing** jako debetního účtu vybere clearingový účet pro vygenerování následující položky.

### <a name="ap-process--1312020--je-110"></a>Proces AP – 31. 1. 2020 – JE 110

| Typ účtu | Číslo účtu | Vrstva   | Popis účtu | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Aktuální | Clearingový účet    | 1,000.00 |          |
| Ledger       | 2              | Aktuální | Bankovní poplatek            | 3.00     |          |
| Ledger       | 3              | Aktuální | Výdaje DPH         | 5.00     |          |
| Dodavatel       | 5              | Aktuální | Závazky    |          | 1,008.00 |

Když je prodejci vystaven výpis, postupujete podle pravidelného platebního procesu. Během tohoto procesu je vygenerována následující položka deníku.

### <a name="cash-payment--1312020--je-120"></a>Platba v hotovosti – 31. 1. 2020 – 120

| Typ účtu | Číslo účtu | Vrstva   | Popis účtu | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Dodavatel       | 5              | Aktuální | Závazky    | 1,008.00 |          |
| Banka         | 9              | Aktuální | Hotovost                |          | 1,008.00 |

V tomto okamžiku jste plně zaúčtovali tento leasing podle zákonných požadavků na výkaznictví a můžete vygenerovat předvahu pomocí aktuální vrstvy. Systém vrátí předvahu s následujícími čísly.

<table>
<thead>
<tr>
<th rowspan='3'>Číslo účtu</th>
<th rowspan='3'>popis</th>
<th colspan='3'>Statutární kniha (aktuální vrstva)</th>
<th rowspan='3'>Celková aktuální vrstva</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Výdaje leasingu</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankovní poplatek</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>Výdaje DPH</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Clearingový účet</td>
<td>−1 000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Závazky</td>
<td></td>
<td>-1008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Používaný majetek</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Povinnost finančního leasingu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Výdaje na úroky</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Hotovost</td>
<td></td>
<td></td>
<td>-1008,00</td>
<td>-1008,00</td>
</tr>
<tr>
<td>10</td>
<td>Odpisové výdaje</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Akumulovaný odpis</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Pokud chcete použít čísla IFRS 16 ke spuštění stejné předvahy, musí být položky deníku statutárního účtování stornovány a položky deníku IFRS 16 musí být zaúčtovány. Chcete-li stornovat položky statutárního deníku, tento příklad obsahuje statutární stornovací knihu, která má stejné nastavení jako statutární kniha, ale má opačný profil účtování. Například statutární kniha *debetovala* účet výdaje na leasing, ale stornovací kniha bude tento účet *kreditovat*. Tyto vztahy lze snadno definovat v účtech pro zaúčtování leasingu majetku na stránce **Parametry leasingu majetku** (**Leasing majetku \> Nastavení \> Parametry leasingu majetku**).

Když se pro stornovací knihu použije stejný proces, který byl použit pro statutární knihu, vytvoří se následující položka deníku. Rozdíl je v tom, že stornovací kniha rezervuje stornované položky ze statutární knihy. Stornování položek se provede také ve vlastní vrstvě. Když je na aktuální vrstvě spuštěna předvaha, stornované položky deníku nejsou zahrnuty.

### <a name="lease-payment--1312020--je-130"></a>Leasingová splátka – 31. 1. 2020 – JE 130

| Typ účtu | Číslo účtu | Vrstva  | Popis účtu | Debet    | Kredit   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Vlastní | Clearingový účet    | 1,000.00 |          |
| Ledger       | 1              | Vlastní | Výdaje leasingu       |          | 1,000.00 |

Nyní, když jste vyloučili položky statutárního deníku, zarezervujete všechny položky deníku, které vyžadují IFRS 16 v knize IFRS 16. Mezi tyto položky patří počáteční uznání používaného majetku a záznam úroků a odpisů.

### <a name="initial-recognition--112020--je-140"></a>Počáteční uznání – 1. 1. 2020 – JE 140

| Typ účtu | Číslo účtu | Vrstva  | Popis účtu      | Debet     | Kredit    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Vlastní | Používaný majetek                | 22,793.90 |           |
| Ledger       | 7              | Vlastní | Povinnost finančního leasingu |           | 22,793.90 |

Leasingová splátka je zaúčtována jako ostatní leasingové splátky. Důvodem pro použití clearingového účtu je zajistit, aby byla hotovost připsána pouze jednou.

### <a name="lease-payment--1312020--je-150"></a>Leasingová splátka – 31. 1. 2020 – JE 150

| Typ účtu | Číslo účtu | Vrstva  | Popis účtu      | Debet    | Kredit   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Vlastní | Povinnost finančního leasingu | 1,000.00 |          |
| Ledger       | 4              | Vlastní | Clearingový účet         |          | 1,000.00 |

Položka deníku úrokových nákladů je generována z plánu amortizace závazků.

### <a name="interest-expense--1312020--je-160"></a>Úrokové náklady – 31. 1. 2020 – JE 160

| Typ účtu | Číslo účtu | Vrstva  | Popis účtu      | Debet | Kredit |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Vlastní | Výdaje na úroky         | 94.97 |        |
| Ledger       | 7              | Vlastní | Povinnost finančního leasingu |       | 94.97  |

Položka deníku odpisových výdajů je generována z plánu odpisu majetku.

### <a name="depreciation-expense--1312020--je-170"></a>Odpisové výdaje – 31. 1. 2020 – JE 170

| Typ účtu | Číslo účtu | Vrstva  | Popis účtu      | Debet  | Kredit |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10             | Vlastní | Odpisové výdaje     | 949.75 |        |
| Ledger       | 11             | Vlastní | Akumulovaný odpis |        | 949.75 |

Po vytvoření a zaúčtování všech těchto položek deníku se zobrazí následující hodnoty „vlastní vrstvy 1“. Všimněte si, že poslední sloupec obsahuje bankovní poplatek, výdaj na daň z přidané hodnoty (DPH) a snížení hotovosti z předchozí vrstvy, ale nezahrnuje položky deníku pro statutární vykazování. Proto dosáhnete skutečného využití možností duálního hlášení. V tomto okamžiku musí společnost spustit předvahu a zkombinovat aktuální a vlastní vrstvu, aby vytvořila předvahu podle IFRS.

| Č. účtu | popis              | Statutární kniha\-Aktuální vrstva\-JE\-100\-Dr \(Cr\) | Statutární kniha\-Aktuální vrstva\-JE\-110\-Dr \(Cr\) | Statutární kniha\-Aktuální vrstva\-JE\-120\-Dr \(Cr\) | Aktuální vrstva \- Celkem | - | Stornovací kniha\-Vlastní vrstva\-JE\-130\-Dr \(Cr\) | Kniha IFRS 16\-Vlastní vrstva\-JE\-140\-Dr \(Cr\) | Kniha IFRS 16\-Vlastní vrstva\-JE\-150\-Dr \(Cr\) | Kniha IFRS 16\-Vlastní vrstva\-JE\-160\-Dr \(Cr\) | Kniha IFRS 16\-Vlastní vrstva\-JE\-170\-Dr \(Cr\) | Vlastní vrstva \+ Vlastní vrstva \- Celkem |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Výdaje leasingu            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankovní poplatek                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | Výdaje DPH              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Clearingový účet         | \-1000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1 000                                           |                                                | \-1000                                        |                                                |                                                | 0\.00                                   |
| 5          | Závazky         |                                                   | \-1008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | Používaný majetek                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Povinnost finančního leasingu |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22 794                                       | 1 000                                          | \-94\.97                                       |                                                | \-21 888\.87                            |
| 8          | Výdaje na úroky         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Hotovost                     |                                                   |                                                   | \-1008\.00                                       | \-1008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1008\.00                             |
| 10         | Odpisové výdaje     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Akumulovaný odpis |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]