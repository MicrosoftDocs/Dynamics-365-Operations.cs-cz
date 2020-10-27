---
title: Redukční klíče prognózy
description: Toto téma obsahuje příklady nastavení redukčního klíče. Obsahuje informace týkající se různého nastavení redukčního klíče a výsledky každého z nich. Redukční klíč slouží k definování způsobu snížení požadavků prognózy.
author: roxanadiaconu
manager: tfehr
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fc2b63bfdec1c663027cb4e551589a705c2164e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981419"
---
# <a name="forecast-reduction-keys"></a>Redukční klíče prognózy

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o různých metodách používaných ke snížení požadavků prognózy. Obsahuje příklady výsledků každé metody. Také vysvětluje, jak vytvořit, nastavit a použít redukční klíč prognózy. Některé metody používají redukční klíč prognózy ke snížení požadavků prognózy.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Způsoby používané ke snížení požadavků prognózy

Pokud do hlavního plánu zahrnete prognózu, můžete zvolit, jak budou požadavky na prognózu sníženy, pokud bude zahrnuta skutečná poptávka. Všimněte si, že hlavní plánování vyloučí požadavky prognózy z minulosti, což znamená všechny požadavky prognózy před dnešním datem.

Chcete-li zahrnout prognózu do hlavního plánu a vybrat metodu, která se používá ke snížení požadavků na prognózu, přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány** . Zvolte model prognózy v poli **Model prognózy** . V poli **Způsob používaný ke snížení požadavků na prognózy** vyberte metodu. Existují tyto možnosti:

- Žádný
- Procento – redukční klíč
- Transakce – redukční klíč
- Transakce – dynamické období

Další části poskytují více informací o každé možnosti.

### <a name="none"></a>Žádný

Pokud zvolíte možnost **Žádná** , požadavky na prognózu nebudou během hlavního plánování sníženy. V tomto případě hlavní plánování vytvoří plánované objednávky, které budou dodávat předpokládanou poptávku (požadavky prognózy). Tyto plánované objednávky udržují navržené množství, bez ohledu na jiné typy poptávky. Pokud jsou například zadány prodejní objednávky, hlavní plánování vytvoří dodatečné plánované objednávky pro dodání prodejních objednávek. Množství požadavků prognózy se nesníží.

### <a name="percent--reduction-key"></a>Procento – redukční klíč

Pokud zvolíte **Procento – redukční klíč** , požadavky na prognózu jsou sníženy podle procenta a časového období, které jsou definovány podle redukčního klíče. V tomto případě hlavní plánování vytvoří plánované objednávky, kde se množství vypočítá jako předpokládané množství × redukční klíč v každém období. Pokud existují jiné typy poptávky, hlavní plánování také vytváří plánované objednávky pro dodání této poptávky.

#### <a name="example-percent--reduction-key"></a>Příklad: Procento – redukční klíč

Tento příklad ukazuje, jak redukční klíč snižuje požadavky na prognózu podle procent a období, které jsou definovány podle redukčního klíče.

V tomto příkladu zahrnete následující prognózu poptávky do hlavního plánu.

| Měsíc    | Prognóza poptávky |
|----------|-----------------|
| Leden  | 1 000           |
| Únor | 1 000           |
| Březen    | 1 000           |
| Duben    | 1 000           |

Na stránce **Redukční klíče** nastavte následující řádky.

| Vrácená hotovost | Jednotka  | Procento |
|--------|-------|---------|
| 1      | Měsíc | 100     |
| 2      | Měsíc | 75      |
| 3      | Měsíc | 50      |
| 4      | Měsíc | 25      |

Přiřaďte redukční klíč ke skupině disponibility položky. Poté na stránce **Hlavní plány** v poli **Způsob používaný ke snížení požadavků na prognózy** vyberete **Procento – redukční klíč** .

V tomto případě, pokud spustíte plánování prognózy 1. ledna, požadavky prognózy poptávky se spotřebují podle procentuálních hodnot, které se nastavují na stránce **Redukční klíče** . Do hlavního plánu se přenesou následující požadované objemy.

| Měsíc                | Množství plánované objednávky | Výpočet    |
|----------------------|------------------------|----------------|
| Leden              | 0                      | = 0 % × 1 000   |
| Únor             | 250                    | = 25 % × 1 000  |
| Březen                | 500                    | = 50 % × 1 000  |
| Duben                | 750                    | = 75 % × 1 000  |
| Květen až prosinec | 1 000                  | = 100 % × 1 000 |

### <a name="transactions--reduction-key"></a>Transakce – redukční klíč

Pokud zvolíte **Transakce – redukční klíč** , požadavky na prognózu jsou sníženy podle transakcí probíhajících během časového období, které jsou definovány podle redukčního klíče.

#### <a name="example-transactions--reduction-key"></a>Příklad: Transakce – redukční klíč

Tento příklad ukazuje, jak jsou skutečné objednávky prováděné v období definovány podle redukčního klíče pro snížení požadavků prognózy poptávky.

V tomto příkladu zvolte **Transakce - redukční klíč** v poli **Způsob používaný ke snížení požadavků na prognózy** na stránce **Hlavní plány** .

Následující prodejní objednávky existují k 1. lednu.

| Měsíc    | Počet objednaných kusů |
|----------|--------------------------|
| Leden  | 956                      |
| Únor | 1 176                    |
| Březen    | 451                      |
| Duben    | 119                      |

Pokud použijete stejnou prognózu poptávky pro 1000 kusů za měsíc, která byla použita v předchozím příkladu, následující požadované objemy se přenesou do hlavního plánu.

| Měsíc                | Počet požadovaných kusů |
|----------------------|---------------------------|
| Leden              | 44                        |
| Únor             | 0                         |
| Březen                | 549                       |
| Duben                | 881                       |
| Květen až prosinec | 1 000                     |

### <a name="transactions--dynamic-period"></a>Transakce – dynamické období

Vyberete-li **Transakce – dynamické období** , požadavky prognózy jsou sníženy podle skutečných transakcí objednávky, ke kterým došlo během dynamického období. Dynamické období pokrývá aktuální data prognózy a končí na začátku další prognózy. V tomto případě hlavní plánování vytvoří plánované objednávky, které budou dodávat předpokládanou poptávku (požadavky prognózy). Pokud jsou však zadány skutečné transakce objednávky, požadavky na prognózu se sníží. Skutečné transakce spotřebují část požadavků prognózy.

Použití této možnosti způsobí následující jevy:

- Redukční klíče nejsou požadovány nebo použity. 
- Pokud je prognóza snížena úplně, požadavky prognózy pro aktuální prognózu budou 0 (nula).
- Pokud neexistuje žádná budoucí prognóza, požadavky prognózy z poslední zadané prognózy budou sníženy.
- Ochranná doba je zahrnuta do výpočtu snížení prognózy.
- Kladné dny jsou zahrnuty do výpočtu snížení prognózy.
- Překračuje-li skutečná transakce objednávky požadavky prognózy, zbývající transakce nejsou předávány do dalšího období prognózy.

#### <a name="example-1-transactions--dynamic-period"></a>Příklad 1: Transakce – dynamické období

Zde je jednoduchý příklad zobrazující způsob fungování metody **Transakce – dynamické období** .

V tomto příkladu zahrnete následující prognózu poptávky do hlavního plánu.

| Datum       | Prognóza poptávky |
|------------|-----------------|
| 1. leden  | 1 000           |
| 1. únor | 1 000             |

Můžete také vytvořit následující prodejní objednávky.

| Datum        | Množství prodejní objednávky |
|-------------|----------------------|
| 15. leden  | 200                  |
| 15. únor | 400                  |

V takovém případě jsou vytvořeny následující plánované objednávky.

| Datum prognózy poptávky | Množství | Vysvětlení                           |
|--------------------- |----------|---------------------------------------|
| 1. leden            | 800      | Požadavky na prognózu (= 1 000-200) |
| 15. leden           | 200      | Požadavky na prodejní objednávky             |
| 1. únor           | 600      | Požadavky na prognózu (= 1 000 - 400) |
| 15. únor          | 400      | Požadavky na prodejní objednávky             |

#### <a name="example-2-transactions--dynamic-period"></a>Příklad 2: Transakce – dynamické období

Ve většině případů jsou systémy nastaveny tak, aby transakce snižovaly prognózu poptávky v rámci konkrétních obdobích prognózy: týdny, měsíce a tak dále. Tato období jsou definována v redukčním klíči. Čas mezi dvěma řádky však prognózy poptávky může také *vyjadřovat* období.

V tomto příkladu vytvořte prognózu poptávky pro následující data a množství.

| Datum       | Prognóza poptávky |
|------------|-----------------|
| 1. leden  | 1 000           |
| 5. leden  | 500             |
| 12. leden | 1 000           |

Všimněte si, že v této prognóze není jasné období mezi daty prognózy. Mezi prvními a druhými daty je interval čtyři dny a mezi druhými a třetími daty je sedmidenní interval. Tyto intervaly jsou dynamická období.

Můžete také vytvořit následující řádky prodejní objednávky.

| Datum                             | Množství prodejní objednávky |
|----------------------------------|----------------------|
| 15. prosince v minulém roce | 500                  |
| 3. leden                        | 100                  |
| 10. leden                       | 200                  |

V takovém případě se prognóza sníží následujícím způsobem:

- Protože první prodejní objednávka není v žádném období, nesníží se žádná prognóza.
- Protože druhá prodejní objednávka je mezi 1. lednem a 5. lednem, sníží se prognóza pro 1. leden o hodnotu 100.
- Protože třetí prodejní objednávka je mezi 5. lednem a 12. lednem, sníží se prognóza pro 5. leden o hodnotu 200.

Proto jsou v takovém případě vytvořeny následující plánované objednávky.

| Datum prognózy poptávky             | Množství | Vysvětlení                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15. prosince v minulém roce | 500      | Požadavky na prodejní objednávku                                            |
| 1. leden                        | 900      | Období požadavků na prognózu 1. ledna až 5. ledna (= 1 000-100) |
| 3. leden                        | 100      | Požadavky na prodejní objednávku                                            |
| 5. leden                        | 300      | Období požadavků na prognózu 5. ledna až 10. ledna (= 500 - 200)  |
| 12. leden                       | 1 000    | Období požadavků na prognózu 12. ledna až do konce                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Vytvoření a nastavení redukčního klíče prognózy

Redukční klíč prognózy se používá v metodách **Transakce – redukční klíč** a **Procento – redukční klíč** pro snížení požadavků prognózy. Chcete-li vytvořit a nastavit redukční klíč, postupujte podle těchto kroků.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Redukční klíče** .
2. Vyberte **Nový** nebo stiskněte klávesy **Ctrl + N** k vytvoření redukčního klíče.
3. V poli **Redukční klíč** zadejte jednoznačný identifikátor pro redukční klíč prognózy. Do pole **Název** zadejte název. 
4. V každém období definujte období a procento redukčního klíče:

    - Pole **Datum platnosti** určuje datum, kdy začíná vytvoření období. Když je možnost **Použít datum účinnosti** nastavena na **Ano** , období začíná v den účinnosti. Když je nastavena na **ne** , období začínají k datu při spuštění hlavního plánování.
    - Definujte období, během kterého má dojít ke snížení prognózy.
    - Pro konkrétní období uveďte procenta, o která by měly být požadavky prognózy sníženy. Můžete zadat kladné hodnoty a požadavky tak snížit nebo záporné hodnoty a požadavky zvýšit.

## <a name="use-a-reduction-key"></a>Použití redukčního klíče

Redukční klíče prognózy musí být přiřazen ke skupině disponibility položky. Postupujte podle následujícího postupu pro přiřazení redukčního klíče ke skupině disponibility položky.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility** .
2. Na záložce s náhledem **Jiné** v poli **Redukční klíč** vyberte redukční klíč, který chcete přiřadit ke skupině disponibility. Redukční klíč se pak použije na všechny položky, které patří do skupiny disponibility.
3. Chcete-li použít redukční klíč pro výpočet snížení prognózy během hlavního plánování, musíte toto nastavení definovat v nastavení plánu prognózy nebo hlavního plánu. Přejděte na jedno z následujících míst:

    - Hlavní plánování \> Nastavení \> Plány \> Plány prognózy
    - Hlavní plánování \> Nastavení \> Plány \> Hlavní plány

4. Na stránce **Plány prognózy** nebo **Hlavní plány** na záložce s náhledem **Obecné** v poli **Způsob používaný ke snížení požadavků na prognózy** vyberte buď **Procento – redukční klíč** nebo **Transakce – redukční klíč** .

## <a name="reduce-a-forecast-by-transactions"></a>Snížení prognózy podle transakcí

Když vyberete **Transakce – redukční klíč** nebo **Transakce – dynamické období** jako metodu pro snížení požadavků prognózy, můžete určit, které transakce sníží prognózu. Na stránce **Skupiny krytí** na záložce s náhledem **Jiné** v poli **Snížit prognózu podle** vyberte **Všechny transakce** , pokud mají všechny transakce snížit prognózu, nebo **Objednávky** , pokud mají prognózu snížit pouze prodejní objednávky.

## <a name="additional-resources"></a>Další zdroje

[Přehled hlavních plánů](master-plans.md)
