---
title: Hlavní plánování s prognózami poptávky
description: Toto téma vysvětluje, jak zahrnout prognózy poptávky během hlavního plánování pomocí Optimalizace plánování.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 71e651afc83e0c2ea147a4657c0f2ce1865ec50efcd932127b4918266d3d7cd8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778669"
---
# <a name="master-planning-with-demand-forecasts"></a>Hlavní plánování s prognózami poptávky

[!include [banner](../../includes/banner.md)]

Můžete použít prognózu poptávky společně s optimalizací plánování, abyste zohlednili očekávanou poptávku ve svém hlavním plánování. Prognózu poptávky můžete ručně vytvořit, importovat nebo vygenerovat pomocí funkce prognózy poptávky v Microsoft Dynamics 365 Supply Chain Management. Další informace o prognóze poptávky najdete v části [Přehled prognózy poptávky](../introduction-demand-forecasting.md).

> [!NOTE]
> Samostatné plánování prognóz není optimalizací plánování podporováno. Proto nastavení **Aktuální plán prognózy** na stránce **Hlavní parametry plánování** nemá žádný účinek, když používáte optimalizaci plánování.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Nastavení hlavního plánu tak, aby zahrnoval prognózu poptávky

Chcete-li nakonfigurovat hlavní plán tak, aby obsahoval prognózu poptávky, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte stávající plán nebo vytvořte nový plán.
1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Model prognózy** - vyberte model prognózy, který se použije. Tento model se zohlední, když se vygeneruje návrh dodávky pro aktuální hlavní plán.
    - **Zahrnout prognózu poptávky** - Tuto možnost nastavte na *Ano*, aby byla prognóza poptávky zahrnuta do aktuálního hlavního plánu. Pokud ji nastavíte na *Ne*, transakce prognózy poptávky nebudou zahrnuty do hlavního plánu.
    - **Metoda použitá ke snížení požadavků na prognózu** - Vyberte metodu, která by měla být použita ke snížení požadavků na prognózu. Další informace naleznete v části [Redukční klíče prognózy](#reduction-keys) dále v tomto tématu.

1. Na pevné záložce **Ochranná doba ve dnech** můžete nastavit následující pole a určit období, během kterého je prognóza poptávky zahrnuta během:

    - **Plán prognózy** - Nastavte tuto možnost na *Ano* pro přepis ochranné doby plánu prognózy, která pochází z jednotlivých skupin pokrytí. Pokud chcete použít hodnoty z jednotlivých skupin pokrytí pro aktuální hlavní plán, nastavte *Ne*.
    - **Časové období prognózy** - Pokud nastavíte možnost **Plán prognózy** na *Ano*, zadejte počet dní (od dnešního data), kdy má být použita prognóza poptávky.

    > [!IMPORTANT]
    > Nastavení **Plán prognózy** ještě není v rámci optimalizace plánování podporováno.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Nastavení skupiny pokrytí tak, aby zahrnovala prognózu poptávky

Chcete-li nakonfigurovat skupinu disponibility tak, aby obsahovala prognózu poptávky, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Skupiny disponibility**.
1. Vyberte existující skupinu disponibility nebo vytvořte novou skupinu.
1. Na pevné záložce **Jiné** nastavte následující pole:

    - **Ochranná doba plánu prognózy** - Zadejte počet dní (od dnešního data), na které by se měla použít prognóza poptávky. Tuto hodnotu lze přepsat pomocí možnosti **Plán prognózy** v hlavním plánu, jak je popsáno v předchozí části.
    - **Redukční klíč** - Vyberte redukční klíč, který chcete použít. Další informace viz [Vytvoření a nastavení redukčního klíče prognózy](#create-reduction-key) a [Použití redukčního klíče](#use-reduction-key) dále v tomto tématu.
    - **Snížit prognózu o** – Pro hlavní plány, kde je pole **Metoda použitá ke snížení požadavků předpovědi** nastaveno na *Transakce- redukční klíč* nebo *Transakce - dynamické období*, určete, které transakce by měly prognózu snížit. Vyberte jednu z následujících hodnot:

        - **Všechny transakce** - Všechny transakce by měly snížit prognózu.
        - **Objednávky** - Pouze prodejní objednávky by měly snížit prognózu.

        > [!NOTE]
        > Pokud vyberete *Všechny transakce*, transakce, které mají jak poptávku, tak nabídku ve stejných dimenzích zásob, jsou považovány za neutrální a jsou během prognózy redukce ignorovány. Například pokud je dimenze plánování nastavena pouze na pracoviště, nikoli na sklad, bude příkaz k převodu mezi pracovištěm 1, skladem 11 a pracovištěm 1 sklad 13 ignorován a nezredukuje zbývající prognózu poptávky.

    - **Zahrnout mezipodnikové objednávky** - Nastavte tuto možnost na *Ano*, pokud by měly být zahrnuty mezipodnikové objednávky, když je prognóza snížena. Jinak nastavte *Ne*.
    - **Zahrnout prognózu zákazníků do prognózy poptávky** - Určete, zda má být prognóza zákazníka zahrnuta do celkové prognózy. Tato možnost určuje, jak skutečná poptávka sníží předpokládanou poptávku. Můžete ji použít k zajištění, že hlavní plánování se vztahuje na dodávku položek, které jsou zakoupeny specifickými odběrateli.

        - Tuto možnost nastavte na *Ano* k zahrnutí prognózy zákazníka do celkové prognózy. V tomto případě skutečná poptávka zákazníků snižuje jak prognózu zákazníků, tak celkovou prognózu. Hlavní plánování generuje plánované objednávky za účelem pokrytí pouze celkové prognózy množství.
        - Tuto možnost nastavte na *Ne*, pokud nechcete zahrnout prognózu zákazníka do celkové prognózy. V tomto případě skutečná poptávka zákazníka snižuje pouze prognózu zákazníka. Hlavní plánování generuje plánované objednávky za účelem pokrytí celkového množství prognózy a prognózy pro množství pro jednotlivé odběratele.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Redukční klíče prognózy

Tato část obsahuje informace o různých metodách používaných ke snížení požadavků prognózy. Obsahuje příklady výsledků každé metody. Také vysvětluje, jak vytvořit, nastavit a použít redukční klíč prognózy. Některé metody používají redukční klíč prognózy ke snížení požadavků prognózy.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Způsoby používané ke snížení požadavků prognózy

Pokud do hlavního plánu zahrnete prognózu, můžete zvolit, jak budou požadavky na prognózu sníženy, pokud bude zahrnuta skutečná poptávka. Všimněte si, že hlavní plánování vyloučí požadavky prognózy z minulosti, což znamená všechny požadavky prognózy před dnešním datem.

Chcete-li zahrnout prognózu do hlavního plánu a vybrat metodu, která se používá ke snížení požadavků na prognózu, přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**. Zvolte model prognózy v poli **Model prognózy**. V poli **Způsob používaný ke snížení požadavků na prognózy** vyberte metodu. Existují tyto možnosti:

- Není
- Procento – redukční klíč
- Transakce - redukční klíč (optimalizace plánování ho zatím nepodporuje)
- Transakce – dynamické období

Další části poskytují více informací o každé možnosti.

#### <a name="none"></a>Žádný

Pokud zvolíte možnost **Žádná**, požadavky na prognózu nebudou během hlavního plánování sníženy. V tomto případě hlavní plánování vytvoří plánované objednávky, které budou dodávat předpokládanou poptávku (požadavky prognózy). Tyto plánované objednávky udržují navržené množství, bez ohledu na jiné typy poptávky. Pokud jsou například zadány prodejní objednávky, hlavní plánování vytvoří dodatečné plánované objednávky pro dodání prodejních objednávek. Množství požadavků prognózy se nesníží.

#### <a name="percent--reduction-key"></a>Procento – redukční klíč

Pokud zvolíte **Procento – redukční klíč**, požadavky na prognózu jsou sníženy podle procenta a časového období, které jsou definovány podle redukčního klíče. V tomto případě hlavní plánování vytvoří plánované objednávky, kde se množství vypočítá jako předpokládané množství × redukční klíč v každém období. Pokud existují jiné typy poptávky, hlavní plánování také vytváří plánované objednávky pro dodání této poptávky.

##### <a name="example-percent--reduction-key"></a>Příklad: Procento – redukční klíč

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

Přiřaďte redukční klíč ke skupině disponibility položky. Poté na stránce **Hlavní plány** v poli **Způsob používaný ke snížení požadavků na prognózy** vyberete **Procento – redukční klíč**.

V tomto případě, pokud spustíte plánování prognózy 1. ledna, požadavky prognózy poptávky se spotřebují podle procentuálních hodnot, které se nastavují na stránce **Redukční klíče**. Do hlavního plánu se přenesou následující požadované objemy.

| Měsíc                | Množství plánované objednávky | Výpočet    |
|----------------------|------------------------|----------------|
| Leden              | 0                      | = 0 % × 1 000   |
| Únor             | 250                    | = 25 % × 1 000  |
| Březen                | 500                    | = 50 % × 1 000  |
| Duben                | 750                    | = 75 % × 1 000  |
| Květen až prosinec | 1 000                  | = 100 % × 1 000 |

#### <a name="transactions--reduction-key"></a>Transakce – redukční klíč

Pokud zvolíte **Transakce – redukční klíč**, požadavky na prognózu jsou sníženy podle transakcí probíhajících během časového období, které jsou definovány podle redukčního klíče.

##### <a name="example-transactions--reduction-key"></a>Příklad: Transakce – redukční klíč

Tento příklad ukazuje, jak jsou skutečné objednávky prováděné v období definovány podle redukčního klíče pro snížení požadavků prognózy poptávky.

V tomto příkladu zvolte **Transakce - redukční klíč** v poli **Způsob používaný ke snížení požadavků na prognózy** na stránce **Hlavní plány**.

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

#### <a name="transactions--dynamic-period"></a>Transakce – dynamické období

Vyberete-li **Transakce – dynamické období**, požadavky prognózy jsou sníženy podle skutečných transakcí objednávky, ke kterým došlo během dynamického období. Dynamické období pokrývá aktuální data prognózy a končí na začátku další prognózy. V tomto případě hlavní plánování vytvoří plánované objednávky, které budou dodávat předpokládanou poptávku (požadavky prognózy). Pokud jsou však zadány skutečné transakce objednávky, požadavky na prognózu se sníží. Skutečné transakce spotřebují část požadavků prognózy.

Použití této možnosti způsobí následující jevy:

- Redukční klíče nejsou požadovány nebo použity. 
- Pokud je prognóza snížena úplně, požadavky prognózy pro aktuální prognózu budou 0 (nula).
- Pokud neexistuje žádná budoucí prognóza, požadavky prognózy z poslední zadané prognózy budou sníženy.
- Ochranná doba je zahrnuta do výpočtu snížení prognózy.
- Kladné dny jsou zahrnuty do výpočtu snížení prognózy.
- Překračuje-li skutečná transakce objednávky požadavky prognózy, zbývající transakce nejsou předávány do dalšího období prognózy.

##### <a name="example-1-transactions--dynamic-period"></a>Příklad 1: Transakce – dynamické období

Zde je jednoduchý příklad zobrazující způsob fungování metody **Transakce – dynamické období**.

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

##### <a name="example-2-transactions--dynamic-period"></a>Příklad 2: Transakce – dynamické období

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Vytvoření a nastavení redukčního klíče prognózy

Redukční klíč prognózy se používá v metodách **Transakce – redukční klíč** a **Procento – redukční klíč** pro snížení požadavků prognózy. Chcete-li vytvořit a nastavit redukční klíč, postupujte podle těchto kroků.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Redukční klíče**.
2. Zvolte **Nový** pro vytvoření redukčního klíče.
3. V poli **Redukční klíč** zadejte jednoznačný identifikátor pro redukční klíč prognózy. Do pole **Název** zadejte název. 
4. V každém období definujte období a procento redukčního klíče:

    - Pole **Datum platnosti** určuje datum, kdy začíná vytvoření období. Když je možnost **Použít datum účinnosti** nastavena na **Ano**, období začíná v den účinnosti. Když je nastavena na **ne**, období začínají k datu při spuštění hlavního plánování.
    - Definujte období, během kterého má dojít ke snížení prognózy.
    - Pro konkrétní období uveďte procenta, o která by měly být požadavky prognózy sníženy. Můžete zadat kladné hodnoty a požadavky tak snížit nebo záporné hodnoty a požadavky zvýšit.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Použití redukčního klíče

Redukční klíče prognózy musí být přiřazen ke skupině disponibility položky. Postupujte podle následujícího postupu pro přiřazení redukčního klíče ke skupině disponibility položky.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility**.
2. Na záložce s náhledem **Jiné** v poli **Redukční klíč** vyberte redukční klíč, který chcete přiřadit ke skupině disponibility. Redukční klíč se pak použije na všechny položky, které patří do skupiny disponibility.
3. Chcete-li použít redukční klíč pro výpočet snížení prognózy během hlavního plánování, musíte toto nastavení definovat v nastavení plánu prognózy nebo hlavního plánu. Přejděte na jedno z následujících míst:

    - **Hlavní plánování \> Nastavení \> Plány \> Plány prognózy**
    - **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**

4. Na stránce **Plány prognózy** nebo **Hlavní plány** na záložce s náhledem **Obecné** v poli **Způsob používaný ke snížení požadavků na prognózy** vyberte buď **Procento – redukční klíč** nebo **Transakce – redukční klíč**.

### <a name="reduce-a-forecast-by-transactions"></a>Snížení prognózy podle transakcí

Když vyberete **Transakce – redukční klíč** nebo **Transakce – dynamické období** jako metodu pro snížení požadavků prognózy, můžete určit, které transakce sníží prognózu. Na stránce **Skupiny krytí** na záložce s náhledem **Jiné** v poli **Snížit prognózu podle** vyberte **Všechny transakce**, pokud mají všechny transakce snížit prognózu, nebo **Objednávky** , pokud mají prognózu snížit pouze prodejní objednávky.

## <a name="forecast-models-and-submodels"></a>Modely prognóz a dílčí modely

Tato část popisuje, jak vytvořit modely prognóz a jak kombinovat více modelů prognóz nastavením dílčích modelů.

*Model prognózy* jmenuje a identifikuje určitou prognózu. Poté, co vytvoříte model prognózy, můžete k němu přidat řádky prognózy. Chcete-li přidat řádky prognózy pro více položek, použijte stránku **Řádky prognózy poptávky**. Chcete-li přidat řádky prognózy pro konkrétní vybranou položku, použijte stránku **Vydané produkty**.

Model prognózy může zahrnovat prognózy z jiných modelů prognóz. K dosažení tohoto výsledku přidáte další modely prognóz jako *dílčí modely* rodičovského modelu prognózy. Než budete moci přidat každý relevantní model jako dílčí model nadřízeného modelu prognózy, musíte jej vytvořit.

Výsledná struktura vám poskytuje účinný způsob ovládání prognóz, protože umožňuje kombinovat (agregovat) vstup z více jednotlivých prognóz. Z hlediska plánování je proto snadné kombinovat prognózy pro simulace. Můžete například nastavit simulaci založenou na kombinaci běžné prognózy s prognózou jarní propagace.

### <a name="submodel-levels"></a>Úrovně dílčích modelů

Počet dílčích modelů, které lze přidat do nadřízeného modelu prognózy, není nijak omezen. Struktura však může mít hloubku pouze jedné úrovně. Jinými slovy, model prognózy, který je dílčím modelem jiného modelu prognózy, nemůže mít své vlastní dílčí modely. Když přidáte do modelu prognózy dílčí modely, systém zkontroluje, zda je tento model prognózy již dílčím modelem jiného modelu prognózy.

Pokud hlavní plánování narazí na dílčí model, který má své vlastní dílčí modely, zobrazí se chybová zpráva.

#### <a name="submodel-levels-example"></a>Příklad úrovní dílčích modelů

Model prognózy A obsahuje model prognózy B jako dílčí model. Proto model prognózy B nemůže mít své vlastní dílčí modely. Pokud se pokusíte přidat dílčí model do modelu prognózy B, zobrazí se následující chybová zpráva: „Model prognózy B je dílčím modelem pro model A.“

### <a name="aggregating-forecasts-across-forecast-models"></a>Agregace prognóz napříč modely prognóz

Řádky prognózy, které se vyskytnou ve stejný den, budou agregovány napříč jejich modelem prognózy a jeho dílčími modely.

#### <a name="aggregation-example"></a>Příklad agregace

Model prognózy A obsahuje modely prognózy B a C jako dílčí modely.

- Model prognózy A zahrnuje prognózu poptávky po 2 kusech (ks) na 15. června.
- Model prognózy B zahrnuje prognózu poptávky po 3 kusech (ks) na 15. června.
- Model prognózy C zahrnuje prognózu poptávky po 4 kusech (ks) na 15. června.

Výsledná prognóza poptávky na 15. června bude jedinou poptávkou po 9 ks (2 + 3 + 4).

> [!NOTE]
> Každý dílčí model prognózy používá vlastní parametry, nikoliv parametry nadřízeného modelu prognózy.

### <a name="create-a-forecast-model"></a>Vytvoření modelu prognózy

Při vytváření modelu prognózy postupujte takto:

1. Přejděte do uzlu **Hlavní plánování \> Nastavení \> Prognóza poptávky \> Modely prognózy**.
1. V podokně akcí zvolte **Nový**.
1. Nastavte následující pole pro nový model prognózy:

    - **Model** – Zadejte jedinečný identifikátor modelu.
    - **Název** – Zadejte popisný název modelu.
    - **Zastaven** – Obvykle byste měli nastavit tuto možnost na *Ne*. Nastavte ji na *Ano* pouze v případě, kdy chcete zabránit úpravám všech řádků prognózy, které jsou přiřazeny k modelu.

    > [!NOTE]
    > Pole **Zahrnout do prognóz peněžních toků** a pole na záložce **Projekt** nesouvisejí s hlavním plánováním. Proto je můžete v tomto kontextu ignorovat. Musíte je brát do úvahy, pouze když pracujete s prognózou pro modul **Řízení projektů a účetnictví**.

### <a name="assign-submodels-to-a-forecast-model"></a>Přiřazení dílčích modelů k modelu prognózy

Pokud chcete k modelu prognózy přiřadit dílčí modely, postupujte takto.

1. Přejděte do uzlu **Řízení zásob \> Nastavení \> Prognóza \> Modely prognózy**.
1. V podokně seznamu vyberte model prognózy, pro který chcete konfigurovat dílčí model.
1. Na záložce **Dílčí model** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující pole:

    - **Dílčí model** – Vyberte model prognózy, který chcete přidat jako dílčí model. Tento model prognózy již musí existovat a nesmí mít žádné vlastní dílčí modely.
    - **Název** – Zadejte popisný název dílčího modelu. Například tento název může označovat vztah dílčího modelu k nadřízenému modelu prognózy.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

