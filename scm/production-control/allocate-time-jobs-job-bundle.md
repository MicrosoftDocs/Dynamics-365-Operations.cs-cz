---
title: "Přidělení času k úlohám ve skupině prací"
description: "V modulu Provádění výroby můžete úlohy ukládat do svazků. Potom můžete spustit více úloh současně na stránce se seznamem úloh."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 26f6d0868ac195d21becec35898e2ac1bcb41e0f
ms.lasthandoff: 03/31/2017


---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Přidělení času k úlohám ve skupině prací

[!include[banner](../includes/banner.md)]


V modulu Provádění výroby můžete úlohy ukládat do svazků. Potom můžete spustit více úloh současně na stránce se seznamem úloh.

Pokud svážete více úloh, je nutné definovat, jak má být přidělen celkový registrovaný čas pro všechny úlohy k jednotlivým pracím. Definování přidělení provádíte výběrem některé z následujících možností v poli **Typ sady** na stránce **Alokační klíče**:

-   **Odhad** - čas je rozdělen mezi úlohy na základě odhadovaného času, který je pro úlohy potřebný.
-   **Práce** - čas je rozdělen podle celkového počtu úloh ve skupině a času stráveného dokončením všech úloh.
-   **Čistý čas** - čas je vždy rozdělen stejnoměrně mezi úlohy, které jsou spolu svázány.
-   **Reálný čas** – skutečný čas úlohy je přidělen. Náklady lze vypočítat na základě skutečných mzdových nákladů. **Poznámka:** Alokační klíč **Reálný čas** je k dispozici pouze v případě, že vaše společnost používá v modulu Čas a docházka funkci mzdy.

V následujících příkladech jsou uvedeny výsledky různých alokačních klíčů.

## <a name="example-scenario"></a>Příklad
Musí být dokončeny tři úlohy ve frontě prací. Začnete s první úlohou a zatímco probíhá, začnete s druhou úlohou a pak se třetí. Proto vznikne vytvoří svazek tří úloh. V následující tabulce jsou uvedeny odhadované výrobní doby pro každou úlohu.

| Úloha   | Doba výroby |
|-------|-----------------|
| Úloha 1 | 1 hodina          |
| Úloha 2 | 3 hodiny         |
| Úloha 3 | 4 hodiny         |
| Celkem | 8 hodin         |

V následující tabulce jsou uvedeny skutečné pracovní hodiny využité pro jednotlivé úlohy.

| Úloha    | Počáteční čas | Koncový čas | Čas svazku |
|--------|------------|----------|-------------|
| Úloha 1  | 09:00      | 11:00    | 2 hodiny     |
| Úloha 2  | 10:00      | 13:00    | 3 hodiny     |
| Úloha 3  | 10:00      | 15:00    | 5 hodin     |
| Sada | 09:00      | 15:00    | 6 hodin     |

Následující části popisují výsledky vypočítaného času pro každý alokační klíč.

## <a name="estimation-allocation-key"></a>Alokační klíč odhadu
V následující tabulce je znázorněn vzorec pro výpočet přiděleného času. Zde je vzorec: Čas na úlohu = celkový čas svazku * (odhadovaný čas úlohy/celkový odhadovaný čas)

| Úloha   | Receptura           | Přidělený čas |
|-------|-------------------|----------------|
| Úloha 1 | 6 × (1 ÷ 8) hodin | 0,75 hodiny      |
| Úloha 2 | 6 × (3 ÷ 8) hodin | 2,25 hodin     |
| Úloha 3 | 6 × (4 ÷ 8) hodin | 3,00 hodiny     |

## <a name="jobs-allocation-key"></a>Alokační klíč úloh
V následující tabulce je znázorněn vzorec pro výpočet přiděleného času. Zde je vzorec: čas na úlohu = celkový čas sady ÷ počet úloh

| Úloha   | Receptura | Přidělený čas |
|-------|---------|----------------|
| Úloha 1 | 6 ÷ 3   | 2 hodiny        |
| Úloha 2 | 6 ÷ 3   | 2 hodiny        |
| Úloha 3 | 6 ÷ 3   | 2 hodiny        |

## <a name="net-time-allocation-key"></a>Alokační klíč čistého času
V následující tabulce je znázorněn vzorec pro výpočet přiděleného času. Zde je vzorec: vypočítaný čas na sestavu = čas sady ÷ počet úloh

|                              | 09:00–10:00 (1 hodina) | 10:00–11:00 (1 hodina) | 11:00–13:00 (2 hodiny) | 13:00–15:00 (2 hodiny) | Přidělený čas |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Počet úloh v sadě | 1                    | 3                    | 2                     | 1                     | Nelze použít |
| Úloha 1                        | 1 ÷ 1 = 1 hodina       | 1 ÷ 3 = 0,33 hodiny    | Nelze použít        | Nelze použít        | 1,33 hodiny     |
| Úloha 2                        | Nelze použít       | 1 ÷ 3 = 0,33 hodiny    | 2 ÷ 2 = 1 hodina        | Nelze použít        | 1,33 hodiny     |
| Úloha 3                        | Nelze použít       | 1 ÷ 3 = 0,33 hodiny    | 2 ÷ 2 = 1 hodina        | 2 ÷ 1 = 2 hodiny       | 3,33 hodin     |

## <a name="real-time-allocation-key"></a>Alokační klíč reálného času
Pokud mají být výrobní náklady vypočítány na základě skutečných nákladů, je nutné vymazat možnost **Nákladové kategorie** na stránce **Výchozí hodnoty pro výrobní objednávku**. V následující tabulce je znázorněn vzorec pro výpočet přiděleného času. Zde je vzorec: Skutečný čas na úlohu = skutečný čas na svazek

| Úloha   | Skutečný čas |
|-------|-------------|
| Úloha 1 | 2 hodiny     |
| Úloha 2 | 3 hodiny     |
| Úloha 3 | 5 hodin     |

Zvažte 3 úlohy, které provádí pracovník, který má hodinovou mzdou 12,00 USD. Během času stráveného na úlohu nebyly získány žádné bonusy ani prémie. pracovník na těchto 3 úlohách ve svazku pracoval celkem 6 hodin. Náklady na mzdu tedy 6 × 12,00 USD = 72,00 USD. Pokud použijete přidělení mezd, náklady na hodinu jsou přepočteny se součinitelem na základě vzorce Čistý čas. Skutečný čas vynaložený na každou úlohu je přenesen společně s korigovanou cenou za hodinové náklady. Na příkladu jej vynaloženo 6 hodin, i když přiděleno bylo hodin 10. V následující tabulce je znázorněn vzorec pro výpočet nákladů. Zde je vzorec: Náklady na hodinu = celkový čas pro svazek úloh (čistý čas) / skutečný čas na úlohu) * standardní náklady na hodinu

| Úloha   | Výpočet korigovaných nákladů za hodinu | Korigované náklady na hodinu | Přidělený čas | Celkové náklady na úlohu |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Úloha 1 | (1,33 ÷ 2) × 12,00 USD                 | 8.00 USD                | 2 hodiny        | 16.00 USD         |
| Úloha 2 | (1,33 ÷ 3) × 12,00 USD                 | 5.33 USD                | 3 hodiny        | 16.00 USD         |
| Úloha 3 | (3,33 ÷ 5) × 12,00 USD                 | 8.00 USD                | 5 hodin        | 40.00 USD         |

Korigované náklady na hodinu a na čas úlohy jsou zaúčtovány do výrobního deníku. **Poznámka:** vyberete-li možnost **Nákladová kategorie** na kartě **Hlavní** na stránce **Výchozí hodnoty pro výrobní objednávku**, skutečný čas pro každou úlohu je přenesen do výrobního deníku, kde jsou náklady aplikovány na nákladovou kategorii příslušné úlohy.




