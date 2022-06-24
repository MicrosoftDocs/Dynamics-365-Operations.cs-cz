---
title: Scénáře data vyrovnání
description: Tento článek obsahuje příklady, které ukazují, jak fungují data vyrovnání ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 102e3a104be5be287f914172160e95aff65d0b18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872608"
---
# <a name="alignment-date-scenarios"></a>Scénáře data vyrovnání

Tento článek obsahuje příklady, které ukazují, jak fungují data vyrovnání ve fakturaci předplatného.

V těchto příkladech má fakturační údaj pro plán fakturace datum vyrovnání 31. října 2019. První fakturační údaj pro řádek končí 31. října 2019 a podle toho je poměrný. Řádek se automaticky obnoví podle počátečního data obnovy 11. listopadu.

> [!NOTE]
> Rok je relevantní, protože může způsobit, že datum vyrovnání bude delší nebo kratší než rok. Například způsob poměrného rozdělení je nastaven jako **Měsíčně** na stránce **Parametry opakované fakturace smlouvy**. Pokud je nastaven na **Denně**, některé dílčí částky se budou lišit.

## <a name="scenario-1-no-alignment"></a>Scénář 1: Žádné vyrovnání

Plán fakturace je nastaven s následujícími údaji:

- **Počáteční datum:** 1. května 2019
- **Koncové datum:** 31. prosince 2024
- **Částka:** 1000 USD

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 1. 5. 2019 | 30. 4. 2020 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 5. 2020 | 30. 4. 2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 5. 2021 | 30. 4. 2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 5. 2022 | 30. 4. 2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 5. 2023 | 30. 4. 2024 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 5. 2024 | 31. 12. 2024 | | | 1,00 | | 1,00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Scénář 2: Zkrácené vyrovnání

Plán fakturace je nastaven s následujícími údaji:

- **Počáteční datum:** 1. května 2019
- **Koncové datum:** 31. prosince 2024
- **Částka:** 1000 USD
- **Datum vyrovnání:** 31. prosince 2019

První částka obnovení je kratší než jeden rok.

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 1. 5. 2019 | 31. 12. 2019 | | | 1,00 | | 1,00 | 666.67 |
| 1. 1. 2020 | 31. 12. 2020 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2021 | 31. 12. 2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2022 | 31. 12. 2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2023 | 31. 12. 2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2024 | 31. 12. 2024 | | | 1,00 | | 1,00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Scénář 3: Rozšířené vyrovnání

Plán fakturace je nastaven s následujícími údaji:

- **Počáteční datum:** 1. května 2019
- **Koncové datum:** 31. prosince 2024
- **Částka:** 1000 USD
- **Datum vyrovnání:** 31. prosince 2020

První částka obnovení je delší než jeden rok.

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 1. 5. 2019 | 31. 12. 2020 | | | 1,00 | | 1,00 | 1,666.67 |
| 1. 1. 2021 | 31. 12. 2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2022 | 31. 12. 2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2023 | 31. 12. 2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2024 | 31. 12. 2024 | | | 1,00 | | 1,00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Scénář 4: Vyrovnání s jiným koncovým měsícem

Plán fakturace je nastaven s následujícími údaji:

- **Počáteční datum:** 1. května 2019
- **Koncové datum:** 31. října 2024
- **Částka:** 1000 USD
- **Datum vyrovnání:** 31. prosince 2019

> [!NOTE]
> Tento scénář není běžný.

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 1. 5. 2019 | 31. 12. 2019 | | | 1,00 | | 1,00 | 666.67 |
| 1. 1. 2020 | 31. 12. 2020 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2021 | 31. 12. 2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2022 | 31. 12. 2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2023 | 31. 12. 2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1. 1. 2024 | 31. 10. 2024 | | | 1,00 | | 1,00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Scénář 5: Jeden částečný rok

Plán fakturace je nastaven s následujícími údaji:

- **Počáteční datum:** 1. května 2019
- **Koncové datum:** 31. prosince 2019
- **Částka:** 1000 USD
- **Datum vyrovnání**: 31. prosince 2019

V tomto scénáři není datum vyrovnání potřeba. Tento scénář je běžný pro automatická obnovení.

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 1. 5. 2019 | 31. 12. 2019 | | | 1,00 | | 1,00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Scénář 6: Vypočítaná data

Podpora a obnovení jsou nastaveny s následujícími údaji:

- **Počáteční datum přepsání:** Ne
- **Počáteční data podpory a obnovení:** Začátek příštího měsíce
- **Datum zaúčtování faktury:** 22. června 2019
- **Datum vyrovnání:** 31. prosince 2020

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 1. 7. 2019 | 31. 7. 2019 | | | 1,00 | | 1,00 | 297.60 |
| 1. 8. 2019 | 31. 12. 2020 | | | 1,00 | | 1,00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Scénář 7: Vypočítaná data a budoucí zaúčtování

Podpora a obnovení jsou nastaveny s následujícími údaji:

- **Počáteční datum přepsání:** Ne
- **Počáteční data podpory a obnovení:** Začátek příštího měsíce
- **Datum zaúčtování faktury:** 22. června 2019
- **Datum vyrovnání:** 31. prosince 2020

Pro tento scénář je datum vyrovnání změněno na 31. prosince 2021.

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 22. 6. 2019 | 22. 6. 2019 | | | 1,00 | | 1,00 | 0,00 |
| 1. 8. 2019 | 31. 12. 2020 | | | 1,00 | | 1,00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Scénář 8: Ruční data a více let

Podpora a obnovení jsou nastaveny s následujícími údaji:

- **Počáteční datum přepsání:** Ano
- **Počáteční datum obnovení:** 1. července 2020
- **Koncové datum obnovení:** 31. prosince 2024
- **Datum vyrovnání:** 31. prosince 2021

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 22. 6. 2019 | 22. 6. 2019 | | | 1,00 | | 1,00 | 0,00 |
| 1. 7. 2020 | 31. 12. 2021 | | | 1,00 | | 1,00 | 375.00 |
| 1/1/2022 | 31. 12. 2022 | | | 1,00 | | 1,00 | 250.00 |
| 1. 1. 2023 | 31. 12. 2023 | | | 1,00 | | 1,00 | 250.00 |
| 1. 1. 2024 | 31. 12. 2024 | | | 1,00 | | 1,00 | 250.00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Scénář 9: Ruční data, více let a jiný koncový měsíc

Podpora a obnovení jsou nastaveny s následujícími údaji:

- **Počáteční datum přepsání:** Ano
- **Počáteční datum obnovení:** 1. července 2020
- **Koncové datum obnovení:** 31. října 2024
- **Datum vyrovnání:** 31. prosince 2021

| Počáteční datum fakturace | Koncové datum fakturace | Předchozí čtení | Aktuální čtení | Zadané množství | Volné množství | Fakturovatelné množství | Jednotková cena |
|---|---|---|---|---|---|---|---|
| 22. 6. 2019 | 22. 6. 2019 | | | 1,00 | | 1,00 | 0,00 |
| 1. 7. 2020 | 31. 12. 2021 | | | 1,00 | | 1,00 | 375.00 |
| 1/1/2022 | 31. 12. 2022 | | | 1,00 | | 1,00 | 250.00 |
| 1. 1. 2023 | 31. 12. 2023 | | | 1,00 | | 1,00 | 250.00 |
| 1. 1. 2024 | 31. 10. 2024 | | | 1,00 | | 1,00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Scénář 10: Vyrovnání bez poměrného rozložení

Podpora a obnovení jsou nastaveny s následujícími údaji:

- **Počáteční datum přepsání:** Ne
- **Datum zaúčtování faktury:** 22. června 2019
- **Datum vyrovnání:** 31. prosince 2019

Počáteční datum obnovení a data vyrovnání jsou upravena tak, aby obě počáteční data byla po datu zaúčtování.

- **Počáteční datum obnovení:** 1. ledna 2020
- **Koncové datum obnovení:** 31. prosince 2020
