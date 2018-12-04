---
title: "Redukční klíče"
description: "Tento článek obsahuje příklady nastavení redukčního klíče. Obsahuje informace týkající se různého nastavení redukčního klíče a výsledky každého z nich. Redukční klíč slouží k definování způsobu snížení požadavků prognózy."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4b7f4ebd635e02f3cfc6d0f620dad30e6b1a98a2
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="reduction-keys"></a>Redukční klíče

[!include [banner](../includes/banner.md)]

Tento článek obsahuje příklady nastavení redukčního klíče. Obsahuje informace týkající se různého nastavení redukčního klíče a výsledky každého z nich. Redukční klíč slouží k definování způsobu snížení požadavků prognózy.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Příklad 1: Procento – princip redukce prognózy redukčního klíče
---------------------------------------------------------------

Tento příklad ukazuje, jak redukční klíč snižuje požadavky na prognózu podle procent a období, které jsou definovány podle redukčního klíče.

1. Na stránce **Redukční klíče** nastavte následující řádky.

   | Vrácená hotovost | Jednotka  | Procento |
   |--------|-------|---------|
   |   1    | Měsíc |   100   |
   |   2    | Měsíc |   75    |
   |   3    | Měsíc |   50    |
   |   4    | Měsíc |   25    |


2. Propojte redukční klíč se skupinou disponibility položky.
3. Na stránce **Hlavní plány**v poli **Metoda redukce** vyberte **Procento – redukční klíč**.
4. Vytvořte prognózu poptávky pro 1000 kusů za měsíc.

Pokud spustíte plánování prognózy 1. ledna, požadavky prognózy poptávky se spotřebují podle procentuálních hodnot, které se nastavují na stránce **Redukční klíče**. Do hlavního plánu se přenesou následující požadované objemy.

| Měsíc                | Počet požadovaných kusů |
|----------------------|---------------------------|
| Leden              | 0                         |
| Únor             | 250                       |
| Březen                | 500                       |
| Duben                | 750                       |
| Květen až prosinec | 1 000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Příklad 2: Transakce – princip redukce prognózy redukčního klíče
Tento příklad ukazuje, jak jsou skutečné objednávky prováděné v období definovány podle redukčního klíče pro snížení požadavků prognózy poptávky.

-   Na stránce **Hlavní plány**v poli **Metoda redukce** vyberte **Transakce – redukční klíč**.

Následující prodejní objednávky existují k 1. lednu.

| Měsíc    | Počet objednaných kusů |
|----------|--------------------------|
| Leden  | 956                      |
| Únor | 1 176                    |
| Březen    | 451                      |
| Duben    | 119                      |

Pokud použijete stejnou prognózu poptávky pro 1000 kusů za měsíc, následující požadované objemy se přenesou do hlavního plánu.

| Měsíc                | Počet požadovaných kusů |
|----------------------|---------------------------|
| Leden              | 44                        |
| Únor             | 0                         |
| Březen                | 549                       |
| Duben                | 881                       |
| Květen až prosinec | 1 000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Příklad 3: Transakce – princip redukce prognózy dynamického období
Ve většině případů jsou systémy nastaveny tak, aby transakce snižovaly prognózu poptávky v rámci konkrétních obdobích prognózy: týdny, měsíce a tak dále. Tato období jsou definována v redukčním klíči. Čas mezi dvěma řádky však prognózy poptávky může také *vyjadřovat* období.

1. Vytvořte prognózu poptávky pro následující data a množství.

   | Datum       | Prognóza poptávky |
   |------------|-----------------|
   | 1. leden  | 1 000           |
   | 5. leden  | 500             |
   | 12. leden | 1 000           |

   V této prognóze není jasné období mezi daty prognózy: mezi 1. a 2. daty existuje 4denní rozpětí a mezi 2. a 3. daty je 7denní rozpětí. Tato různá rozpětí jsou dynamická období.
2. Vytvořte řádky prodejní objednávky následovně.
   | Datum                             | Množství prodejní objednávky |
   |----------------------------------|----------------------|
   | 15. prosince v minulém roce | 500                  |
   | 3. leden                        | 100                  |
   | 10. leden                       | 200                  |

Prognóza bude snížena následujícím způsobem:

-   První prodejní objednávka není v rámci žádného období, takže nesníží žádnou prognózu.
-   Druhá prodejní objednávka je mezi 1. lednem a 5. lednem, takže sníží prognózu pro 1. leden o hodnotu 100.
-   Třetí prodejní objednávka je mezi 5. lednem a 12. lednem, takže sníží prognózu pro 5. leden o hodnotu 200.

Následující plánovaná objednávka bude vytvořena ke splnění prognózy.

| Datum prognózy poptávky | Snížené množství |
|----------------------|------------------|
| 1. leden            | 900              |
| 5. leden            | 300              |
| 12. leden           | 1 000            |

Zde je souhrn snížení **Transakce – dynamické období**:

-   Požadavky prognózy jsou sníženy podle skutečných transakcích objednávky, ke kterým došlo během dynamické doby. Dynamické období pokrývá aktuální data prognózy a končí na začátku další prognózy.
-   Tato metoda nepoužívá ani nevyžaduje redukční klíč.
-   Použití této možnosti způsobí následující jevy:
    -   Pokud je prognóza snížena úplně, požadavky prognózy pro aktuální prognózu budou 0 (nula).
    -   Pokud neexistuje žádná budoucí prognóza, požadavky prognózy z poslední zadané prognózy budou sníženy.
    -   Ochranná doba je zahrnuta do výpočtu snížení prognózy.
    -   Kladné dny jsou zahrnuty do výpočtu snížení prognózy.
    -   Překračuje-li skutečná transakce objednávky požadavky prognózy, zbývající transakce nejsou předávány do dalšího období prognózy.


<a name="additional-resources"></a>Další zdroje
--------

[Hlavní plány](master-plans.md)




