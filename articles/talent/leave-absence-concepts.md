---
title: Koncepty pracovního volna a absence
description: Toto téma popisuje koncepty pracovního volna a absence a způsob určení zůstatků volna.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898635"
---
# <a name="leave-and-absence-concepts"></a>Koncepty pracovního volna a absence

Pojmy a termíny popisované v tomto tématu vám mohou pomoci určit, jak je zaměstnanci udělováno volno a jak se vypočítávají časové zůstatky tohoto zaměstnance. Další informace o řízení pracovního volna a absence získáte v části [Řízení odchodů a absence](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Podrobnosti plánu pracovního volna

### <a name="start-date"></a>Datum zahájení

Počáteční datum je datum, kdy začíná zpracování časového rozlišení. Počáteční datum rovněž slouží jako datum výročí používané k výpočtu částek převedených do dalšího období.

## <a name="accruals"></a>Časově rozlišené položky

Časové rozlišení určují, kdy a jak často je zaměstnanci uděleno volno. Zásady týkající se udělování časového rozlišení a poměrného rozložení jsou definovány v části **časové rozlišení** při vytváření plánu dovolených a absencí.

### <a name="accrual-frequency"></a>Frekvence časového rozlišení

Frekvence časového rozlišení definuje, jak často je časově rozlišeno nebo udělováno pracovní volno. Existují tyto možnosti:

- Denně
- Týdně
- Každé 2 týdny
- Každých 14 dní
- Měsíčně
- Kvartálně
- Pololetně
- Ročně
- Neomezeno

### <a name="accrual-period-basis"></a>Základ období časového rozlišení

Základ období časového rozlišení určuje datum, které slouží k výpočtu období časového rozlišení. Existují tyto možnosti:

- **Počáteční datum plánu**
- **Datum specifické pro zaměstnance** – Když je vybrána tato možnost, hodnota určuje zdroj hodnoty počátečního data, která se používá k výpočtu období časového rozlišení. Existují tyto možnosti:

    - Vlastní
    - Datum výročí
    - Datum původního přijetí
    - Datum služebního věku
    - Upravené počáteční datum pracovníka
    - Počáteční datum pracovníka

### <a name="accrual-award-date"></a>Datum odměny časového rozlišení

Datum udělení časového určuje, kdy a jak často je zaměstnanci uděleno volno. Existují tyto možnosti:

- **Datum ukončení období časového rozlišení** – zaměstnanec bude mít přidělen volno k poslednímu dni období odměny.

    Chcete-li časově rozlišovat správnou částku, musí proces časového rozlišení zahrnovat celé období. Období časového rozlišení je například 1. ledna 2018 až 31. ledna 2018. Aby byl v tomto případě zahrnut leden, musí být časové rozlišení spuštěno pro 1. únor 2018.

- **Datum zahájení období časového rozlišení** – zaměstnanec bude mít přidělen volno k prvnímu dni období odměny.

### <a name="accrual-policy-on-enrollment"></a>Zásady časového rozlišení při přihlášení

Zásady časového rozlišení při přihlášení definují způsob výpočtu časového rozlišení, když se zaměstnanec zaregistruje uprostřed období časového rozlišení. Existují tyto možnosti:

- **Poměrné rozložení** – Rozsah dat mezi datem registrace a datem zahájení slouží k určení rozdílu ve dnech. Tento rozdíl se použije při zpracování časového rozlišení.
- **Úplné časové rozlišení** – úplná částka založená na vrstvě je udělena během zpracování prvního časového rozlišení.
- **Žádné časové rozlišení** – není uděleno žádné časové rozlišení až do dalšího období časového rozlišení.

### <a name="accrual-policy-on-unenrollment"></a>Zásady časového rozlišení při odhlášení

Zásady časového rozlišení při odhlášení definují způsob výpočtu časového rozlišení, když se zaměstnanec odregistruje uprostřed období časového rozlišení. Existují tyto možnosti:

- **Poměrné rozložení** – Rozsah dat mezi datem registrace a datem zahájení slouží k určení rozdílu ve dnech. Tento rozdíl se použije při zpracování časového rozlišení.
- **Úplné časové rozlišení** – úplná částka založená na vrstvě je udělena během zpracování prvního časového rozlišení.
- **Žádné časové rozlišení** – není uděleno žádné časové rozlišení až do dalšího období časového rozlišení.

## <a name="accrual-schedule"></a>Plán časového rozlišení

Plán časového rozlišení určuje, jak si zaměstnanec rozdělí čas volna a jaké částky bude zaměstnanec rozlišovat v čase a převádět do dalšího období. Vrstvy lze vytvořit tak, aby bylo volno udělováno podle různých úrovní.

### <a name="months-of-service"></a>Počet odpracovaných měsíců

Hodnota **Odpracovaných měsíců** definuje minimální počet měsíců, které musí zaměstnanec odpracovat, aby měl nárok na časové rozlišení. Pokud se pro zaměstnance nepožaduje žádné minimum, nastavte hodnotu na **0**.

### <a name="hours-worked"></a>Odpracované hodiny

Hodnota **Odpracované hodiny** definuje minimální počet hodin, které musí zaměstnanec odpracovat v období časového rozlišení, aby měl nárok na časové rozlišení. Pokud se pro zaměstnance nepožaduje žádné minimum, nastavte hodnotu na **0**.

### <a name="accrual-amount"></a>Částka časového rozlišení

Časově rozlišená částka je počet hodin nebo dnů, které budou zaměstnanci časově rozlišovat za dané období. Období vychází z četnosti časového rozlišení.

### <a name="minimum-balance"></a>Minimální zůstatek

Zápornou hodnotu lze použít pro minimální zůstatek, pokud mohou zaměstnanci požadovat více dovolené, než mají k dispozici.

### <a name="maximum-carry-forward"></a>Maximální převedení do dalšího období

Proces časového rozlišení bude upravovat zůstatky dovolené, které překročí maximální zůstatek převedený do dalšího období k výročí počátečního data.

### <a name="grant-amount"></a>Udělené množství

Udělené množství je počáteční počet hodin nebo dní, udělených zaměstnancům při jejich prvním přihlášení do plánu dovolených. Částka není časové rozlišení pro každé období časového rozlišení.

## <a name="enrollments-and-balances"></a>Přihlášení a zůstatky

### <a name="enrollment-date"></a>Datum registrace

Datum přihlášení určuje, kdy zaměstnanec může začít s časovým rozlišením volna. Pokud má například zaměstnanec naplánovanou dovolenou od 15. června 2018, nemůže si časově rozdělit volno před 15. červnem 2018.

### <a name="current-balance"></a>Aktuální zůstatek

Aktuální zůstatek je množství dovolené, které je k dispozici pro požadavky na volno. Tato částka zahrnuje časová rozlišení, schválené požadavky a úpravy do aktuálního data.

### <a name="current-balance-examples"></a>Příklady aktuálního zůstatku

#### <a name="annual-plan"></a>Roční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 1. 2018        | Roční            | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 1. lednu 2019 (1. 1. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Požadovaná délka | Aktuální zůstatek (k 1. 1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Aktuální zůstatek (160) = časově rozlišená částka (200) – požadovaná délka (40)

#### <a name="semimonthly-plan"></a>Čtrnáctidenní plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 1. květnu 2018 (5. 1. 2018), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Požadovaná délka | Aktuální zůstatek (k 1. 1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Aktuální zůstatek (22) = časově rozlišená částka (5 × 6) – požadovaná délka (8)

#### <a name="monthly-plan"></a>Měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 1. květnu 2018 (5. 1. 2018), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Požadovaná délka | Aktuální zůstatek (k 1. 1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Aktuální zůstatek (7) = časově rozlišená částka (5 × 3) – požadovaná délka (8)

### <a name="forecasted-balance"></a>Předpovídaný zůstatek

*Předpovídaný zůstatek* je délka dovolené dostupná k budoucímu datu. Časové rozlišení a úpravy pro převedení do dalšího období jsou předpovídány do tohoto data.

Použije se následující vzorec:

Předpovídaný zůstatek pro pondělí = aktuální zůstatek – Požadavky + časově rozlišené množství – Úprava pro převod do dalšího období

### <a name="forecasted-balance-examples"></a>Příklady předpokládané zůstatku

#### <a name="annual-plan"></a>Roční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 1. 2018        | Roční            | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 15. únoru 2019 (2. 15. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Aktuální zůstatek | Předpokládaný zůstatek (k. 15. 2. 2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Předpokládaný zůstatek (40) = časově rozlišené množství (20) + aktuální zůstatek (40) – Úprava pro převod do dalšího období (20)

#### <a name="semimonthly-plan"></a>Čtrnáctidenní plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 15. únoru 2019 (2. 15. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Aktuální zůstatek | Předpokládaný zůstatek (k. 15. 2. 2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Předpokládaný zůstatek (35) = časově rozlišené množství (5 × 3) + aktuální zůstatek (40) – Úprava pro převod do dalšího období (20)

#### <a name="monthly-plan"></a>Měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 15. únoru 2019 (2. 15. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Aktuální zůstatek | Předpokládaný zůstatek (k. 15. 2. 2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Předpokládaný zůstatek (30) = časově rozlišené množství (10 × 1) + aktuální zůstatek (40) – Úprava pro převod do dalšího období (20)

### <a name="proration-balance-examples"></a>Příklady poměrně rozděleného zůstatku

#### <a name="prorated-monthly-plan"></a>Poměrně rozdělený měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Frekvence časového rozlišení | Základ období časového rozlišení |
|-----------------|-------------------|----------------------|
| 1. 1. 2018        | Měsíčně           | Počáteční datum plánu      |

**Výsledky**

| Zaměstnanec            | Počet odpracovaných měsíců | Datum registrace | Datum zahájení | Částka časového rozlišení | Zpracovat časové rozlišení | Rozvaha |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1. 6. 2018        | 1. 6. 2018   | 1.00           | 1. 9. 2018        | 3,00    |
| Jan Norman          | 0,00              | 15. 6. 2018       | 15. 6. 2018  | 1.00           | 1. 9. 2018        | 2.53    |

#### <a name="full-accrual-monthly-plan"></a>Plně časově rozlišený měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Frekvence časového rozlišení | Základ období časového rozlišení |
|-----------------|-------------------|----------------------|
| 1. 1. 2018        | Měsíčně           | Počáteční datum plánu      |

**Výsledky**

| Zaměstnanec            | Počet odpracovaných měsíců | Datum registrace | Datum zahájení | Částka časového rozlišení | Zpracovat časové rozlišení | Rozvaha |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1. 6. 2018        | 1. 6. 2018   | 1.00           | 1. 9. 2018        | 3,00    |
| Jan Norman          | 0,00              | 15. 6. 2018       | 15. 6. 2018  | 1.00           | 1. 9. 2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Žádný časově rozlišený měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Frekvence časového rozlišení | Základ období časového rozlišení |
|-----------------|-------------------|----------------------|
| 1. 1. 2018        | Měsíčně           | Počáteční datum plánu      |

**Výsledky**

| Zaměstnanec            | Počet odpracovaných měsíců | Datum registrace | Datum zahájení | Částka časového rozlišení | Zpracovat časové rozlišení | Rozvaha |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1. 6. 2018        | 1. 6. 2018   | 1.00           | 1. 9. 2018        | 3,00    |
| Jan Norman          | 0,00              | 15. 6. 2018       | 15. 6. 2018  | 1.00           | 1. 9. 2018        | 2,00    |
