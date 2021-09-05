---
title: Pravidla zaokrouhlování výpočtu daně
description: Toto téma poskytuje informace o pravidlech zaokrouhlování v parametrech výpočtu daně služby pro výpočet daně.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 38760879d84d8262cc1e8395c59bcbc0429bc753
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7347678"
---
# <a name="tax-calculation-rounding-rules"></a>Pravidla zaokrouhlování výpočtu daně

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o pravidlech zaokrouhlování v parametrech výpočtu daně služby pro výpočet daně.

> [!NOTE] 
> Když je povolena služba výpočtu daně, pravidla zaokrouhlení na stránkách **Kód DPH** a **Skupina DPH** nejsou účinná.

Konfiguraci pravidel zaokrouhlování pro službu výpočtu daně můžete zobrazit v sekci **Pravidlo zaokrouhlování DPH** na pevné záložce **Výpočet** na kartě **Všeobecné** stránky **Parametry výpočtu daně** (**Daň** \> **Nastavit** \> **Konfigurace daně** \> **Parametry výpočtu daně**).

[![Konfigurace pravidla zaokrouhlení na stránce Parametry výpočtu daně](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Pole **Přesnost zaoblení** a **Metoda zaokrouhlování** určují, jak jsou zaokrouhleny vypočítané částky v datové části ze služby pro výpočet daně.

## <a name="rounding-precision"></a>Přesnost zaokrouhlování

Pole **Přesnost zaokrouhlení** podporuje hodnotu, která má až šest desetinných míst. Pokud například nastavíte pole **Přesnost zaokrouhlení** na **0,000000**, vypočtené částky jsou zaokrouhleny na šest desetinných míst a poté odeslány do Microsoft Dynamics 365 Finance. Pokud se použije například metoda zakrouhlení **Normální**, částka **987,1234567** je zaokrouhlena na **987,123457**.

> [!NOTE]
> Finance zaokrouhlují částky podle pravidel zaokrouhlování měny. Proto jsou částky daně, které jsou zobrazeny a zaznamenány v transakcích, ovlivněny jak pravidly zaokrouhlování výpočtu daně, tak pravidly zaokrouhlování měny.

## <a name="rounding-method"></a>Metoda zaokrouhlení

Metodu zaokrouhlování pro výpočet daně lze nakonfigurovat pro každou právnickou osobu. V poli **Metoda zaokrouhlování** si můžete vybrat ze tří možností: **Normální**, **Dolů** a **Nahoru**.

### <a name="rounding-example"></a>Příklad zaokrouhlení

Následující tabulka uvádí příklad, který ukazuje, jak je částka **987,345** zaokrouhlena pro různé kombinace přesností zaokrouhlení a metod zaokrouhlení.

<table>
<thead>
<tr>
<th rowspan="2">Metoda zaokrouhlení</th>
<th colspan="8">Přesnost zaokrouhlování</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10.00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normální</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Dolů</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Zaokrouhlení nahoru</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Logiku výpočtu a zaokrouhlování částek daně lze konfigurovat podle pravidel zdanění.

## <a name="rounding-by"></a>Zaokrouhlení 

V poli **Zaokrouhlení** vyberte pravidlo zaokrouhlování, které platí pro daně. Existují tyto možnosti:

- **Daňové kódy** - Zaokrouhlete částku daně uvnitř každého daňového kódu.
- **Kombinace daňových kódů** - Zaokrouhlete částku daně do kombinace kódu daně na řádku.

## <a name="calculation-method"></a>Metoda výpočtu

V poli **Způsob kalkulace** vyberte, zda mají být daně ve fakturách vypočteny pro jednotlivé nebo pro všechny řádky. Existují tyto možnosti:

- **Řádek** - Vypočítejte částku daně po řádcích. Výše daně na každém řádku není ovlivněna částkou daně na ostatních řádcích.
- **Celkový** - Vypočítejte částku daně ve všech řádcích na jednom dokladu.

### <a name="rounding-calculation-example"></a>Příklad výpočtu zaokrouhlování

Tento příklad ukazuje různé výpočty, které lze provést pro jednu fakturu pro různé kombinace hodnot **Zaokrouhlení** a **Metoda výpočtu**. V tomto případě je na místě následující nastavení:

- Faktura má čtyři řádky.
- Existují dva daňové kódy: **VAT1** (10 procent) a **VAT2** (10 procent).
- Přesnost zaokrouhlení je nastavena na **0,01**.
- Metoda zaokrouhlení je nastavena na **Zaokrouhlování nahoru**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Zaokrouhlení = daňové kódy a metoda výpočtu = řádek

| Číslo řádku | Čistá částka řádku | Stanovené daňové kódy | Částka daně před zaokrouhlením | Zaokrouhlená částka daně |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1; VAT2           | 2.222; 2.222               | 2.23; 2.23         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4           | 44.44           | VAT1; VAT2           | 4.444; 4;444               | 4.45; 4.45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Zaokrouhlení = kombinace daňových kódů a metoda výpočtu = řádek

| Číslo řádku | Čistá částka řádku | Stanovené daňové kódy | Částka daně před zaokrouhlením | Zaokrouhlená částka daně |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | VAT1; VAT2           | 2.222; 2.222               | 2.23; 2.22         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4.444; 4;444               | 4.45; 4.44         |

\* Řádek 2 = Round\[22.22 × (10 procent + 10 procent)\] = 2.23 + 2.22

\*\* Řádek 4 = Round\[44.44 × (10 procent + 10 procent)\] = 4.45 + 4.44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Zaokrouhlení = daňové kódy a metoda výpočtu = celkem

| Číslo řádku | Čistá částka řádku | Stanovené daňové kódy | Částka daně před zaokrouhlením | Zaokrouhlená částka daně |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1\*; VAT2\*\*     | 2.222; 2.222               | 2.22; 2.23         |
| 3           | 33.33           | VAT1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | VAT1\*; VAT2\*\*     | 4.444; 4;444               | 4.44; 4.44         |

\* VAT1(Řádek 1, Řádek 2, Řádek 3, Řádek 4) = Round\[(11.11 + 22.22 + 33.33 + 44.44) × 10 procent\] = 1.12 + 2.22 + 3.33 + 4.44

\*\* VAT2 (řádek 2, řádek 4) = Round\[(22,22 + 44,44) × 10 procent\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Zaokrouhlení = kombinace daňových kódů a metoda výpočtu = celkem

| Číslo řádku | Čistá částka řádku | Stanovené daňové kódy | Částka daně před zaokrouhlením | Zaokrouhlená částka daně |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | VAT1; VAT2           | 2.222; 2.222               | 2.23; 2.22         |
| 3\*         | 33.33           | VAT1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4.444; 4;444               | 4.44; 4.45         |

\* Řádek 1, Řádek 3 = Round\[(11.11 + 33.33) × 10 procent\] = 1.12 + 3.33

\*\* Řádek 2, řádek 4 = Round\[ (22,22 + 44,44) × (10 procent + 10 procent)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
