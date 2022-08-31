---
title: Hlavní plánování pro produkty s omezenou trvanlivostí
description: Tento článek popisuje, jak nastavit a používat funkce plánování, které berou v úvahu životnost produktů podléhajících zkáze.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 95c905cbcc3c057dbccf2b7d6e894b1e99ddfba5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337131"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Hlavní plánování pro produkty s omezenou trvanlivostí

[!include [banner](../../includes/banner.md)]

Trvanlivost je doba, po kterou může být produkt skladován, dokud jej nelze dále používat nebo prodávat. U produktů, které mají omezenou trvanlivost, pravděpodobně použijete strategii skladu first-expire, first-out (FEFO), která upřednostňuje spotřebu a prodej položek na základě jejich zbývající trvanlivosti. Tato skladová strategie je relevantní pro potraviny, léky a další zboží, které se vyznačuje krátkou dobou skladování. Podle FEFO jsou položky ve skladu uloženy jako zboží v regálech supermarketu: produkty, které mají dlouhou trvanlivost, jsou umístěny hluboko do regálů, takže produkty, které mají kratší zbývající trvanlivost, jsou odeslány jako první.

## <a name="using-shelf-life-in-master-planning"></a>Používání trvanlivosti v hlavním plánování

Tato část vysvětluje, jak hlavní plánování navrhuje zásoby pro položky s dobou trvanlivosti.

Když spustíte hlavní plánování, generuje navrhované plánované objednávky (dodávky), které splní vaši poptávku a také minimalizují zpoždění. Pokud váš plán zahrnuje položky, které mají omezenou dobu trvanlivosti, kalkulace plánování se stanou složitějšími, protože plán musí nejen minimalizovat zpoždění, ale také využít stávající zásoby před vypršením trvanlivosti. Plán se musí pokusit použít zásoby, které jsou nejblíže datu vypršení trvanlivosti, před zásobami, které vyprší později. Proto se hlavní plánování snaží dosáhnout následujících cílů v tomto pořadí:

1. Minimalizovat součet zpoždění.
1. Maximalizovat součet nabídky FEFO.
1. Minimalizovat doplňování zásob.

V některých případech může dojít ke konfliktu mezi prvními dvěma cíli a je třeba si vybrat: chcete odložit zásilku nebo chcete použít dodávku, jejíž trvanlivost vyprší později, místo dodávky, která vyprší dříve? Aby se tento konflikt vyřešil během hlavního plánování, systém upřednostňuje minimalizaci zpoždění před spotřebováním zásob, které brzy vyprší. Obecně k tomuto typu konfliktu dochází, když může dojít ke zpoždění a pokrytí podle období. Proto doporučujeme použít dobu krytí, která je kratší než doba použitelnosti položky. Jiné typy krytí (jako je požadavek) se s tímto typem konfliktu pravděpodobně nesetkají.

## <a name="set-up-shelf-life"></a>Nastavte trvanlivost

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Nakonfigurujte každý hlavní plán s ohledem na dobu trvanlivosti

Ve výchozím nastavení hlavní plány nezohledňují trvanlivost. Pomocí následujícího postupu povolíte výpočty trvanlivosti pro každý hlavní plán, který je vyžaduje.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte v podokně seznamu existující hlavní plán nebo vytvořte nový.
1. Na pevné záložce **Obecné** nastavte možnost **Použít data trvanlivosti** na *Ano*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Konfigurovat sledovací dimenze do dimenze sledování dávky

Trvanlivost položky lze sledovat pouze v případě, že je tato položka sledována v rozměru dávky. Jinými slovy, odkaz na dávku a požadovaná data musí být zaznamenána při příjmu nebo výrobě a během každé inventarizační transakce položky. Chcete-li tuto možnost spravovat, nastavte jednu nebo více skupin sledovacích dimenzí, aby prováděly požadované sledování, a poté k těmto skupinám podle potřeby přiřaďte příslušné položky.

Pomocí následujícího postupu nastavte skupinu sledovacích dimenzí pro sledování dimenze dávky.

1. Přejděte na **Správa informací o produktu \> Nastavení \> Dimenze a skupiny variant \> Skupiny sledovacích dimenzí**.
1. Proveďte jeden z následujících kroků:

    - V podokně Akce vyberte možnost **Nová**, vytvoří se nová skupina sledovacích dimenzí. Zdejte název a popis a pak vyberte **Uložit** v podokně akcí.
    - V podokně seznamu vyberte existující skupinu sledovacích dimenzí, kterou chcete nastavit pro sledování dimenze dávky.

1. Na pevné záložce **Sledovací dimenze** v řádku **Číslo dávky** zaškrtněte políčka ve sloupcích **Aktivní** a **Fyzické zásoby**.

### <a name="set-up-shelf-life-for-a-product"></a>Nastavte trvanlivost produktu

K nastavení doby trvanlivosti produktu použijte následující postup.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vytvořte nebo otevřete produkt, který chcete nastavit.
1. Chcete-li použít nastavení trvanlivosti, na pevné záložce **Obecné** nastavte pole **Skupina sledovacích dimenzí** na skupinu sledovacích dimenzí, která je nastavena pro sledování dimenze dávky. Toto pole můžete nastavit pouze při prvním vytváření produktu. U stávajících produktů nelze změnit hodnotu.
1. Na pevné záložce **Spravovat zásoby** zadejte následující pole:

    - **Období doporučeného skladování ve dnech** – Zadejte období (ve dnech), do kterého se má šarže tohoto produktu zkontrolovat, zda je vhodná ke spotřebě nebo k dalšímu prodeji. Hodnota tohoto pole se přičte k *datu výroby* dávky, aby se určilo její *datum doporučené doby skladování*. Systém můžete nakonfigurovat tak, aby generoval objednávky kvality, když se dávka přiblíží datu doporučené doby skladování.
    - **Období trvanlivosti ve dnech** – Určete počet dní před vypršením platnosti šarže tohoto produktu. Tato hodnota se přičte k *datu výroby* a určí tak *Datum vypršení platnosti*. Po tomto datu je dávka považována za nepoužitelnou.
    - **Období doporučené spotřeby ve dnech** – Uveďte období (ve dnech), po kterém je dávka tohoto produktu považována za stále prodejnou, ale již si nemůže zachovat některé ze svých původních vlastností. Tato hodnota se přičte k *datu výroby* a určí tak *Datum doporučené spotřeby*. Můžete spustit sestavy a identifikovat zásoby, které jsou po datu doporučené spotřeby. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Nastavte pro každého zákazníka pravidlo prodejních dnů

Funkce *Dny prodejnosti* zajišťuje, že produkty z dávky, která brzy vyprší, nebudou odeslány zákazníkům. Navíc zajišťuje, že když jsou produkty odeslány zákazníkovi, zbývá po dodání stále dostatečný počet dní prodejnosti.

Chcete-li používat funkci dnů prodejnosti, musíte definovat počet dní prodejnosti, který platí pro každý produkt (nebo skupinu produktů) pro každého zákazníka. Tento proces musíte dokončit ručně, protože pro něj neexistuje žádná datová entita.

Pomocí následujícího postupu nastavte dny prodejnosti pro každý produkt pro každého zákazníka.

1. Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.
1. Najděte a vyberte zákazníka, kterého chcete nastavit.
1. V podokně Akce na kartě **Prodej** ve skupině **Nastavení** zvolte **Prodej \> Dny prodejnosti**.
1. Na stránce **Dny prodejnosti pro zákazníka** mřížka uvádí existující pravidla dnů prodejnosti pro každý produkt nebo skupinu produktů. Pomocí tlačítek na panelu akcí můžete podle potřeby přidávat nebo upravovat řádky z mřížky. **Filtr** je k dispozici, aby vám pomohl najít existující řádky.
1. Pro každý řádek je třeba nastavit tato pole:

    - **Kód položky** - vyberte jednu z následujících hodnot a určete rozsah položek, které budou ovlivněny:

        - *Tabulka* - Řádek se vztahuje na konkrétní položku.
        - *Skupina* – řádek se uplatňuje pouze na určitou skupinu položek.
        - *Vše* – Řádek platí pro všechny položky.

    - **Vztah položky** - pokud nastavíte pole **Kód položek** na *Tabulka*, vyberte konkrétní položku. Pokud nastavili pole **Kód položky** na *Skupina*, vyberte skupinu položek. Pokud bylo pole **kód položky** vybrána možnost *Vše*, nebude toto pole k dispozici.
    - **Dny prodejnosti** – Zadejte minimální počet dní, které musí mít zákazník na prodej odpovídajících produktů, než vyprší platnost dávky. Hodnota dnů prodejnosti je založena na požadovaném datu příjmu (nebo potvrzeném datu příjmu, pokud je definováno) pro odpovídající produkty v prodejní objednávce.
    - *(jiné rozměry produktu)* – Chcete-li dále omezit rozsah řádku, zadejte jiné hodnoty dimenzí (např **Velikost** a **Barva**) podle potřeby. Chcete-li určit, které dimenze se zobrazí v mřížce, vyberte **Zobrazit dimenze** v podokně akcí.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Nastavte všechny relevantní produkty tak, aby byly řízeny datem FEFO

Aby dny prodejnosti fungovaly, musí každá relevantní položka patřit do skupiny modelů položek, kde je zaškrtnuto políčko **FEFO řízeno datem**.

Pomocí následujícího postupu nastavte skupinu modelů položek tak, aby podporovala funkci dnů prodejnosti.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Zásoby \> Skupiny modelu položky**.
1. Vyberte existující skupinu v podokně seznamu nebo vytvořte novou výběrem **Nová** v podokně akcí.
1. Na záložce s náhledem **Zásady zásob** zaškrtněte políčko **Řízení FEFO podle data**.
1. V případě potřeby nastavte další pole pro skupinu.

Pomocí následujícího postupu můžete zobrazit nebo nastavit skupinu modelů položek, do které produkt patří.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Otevřete produkt, který chcete zkontrolovat nebo upravit.
1. Na pevné záložce **Obecné** nastavte pole **Skupina modelů položek** na skupinu, kde je zaškrtnuto políčko **Řízení FEFO podle data**.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Příklad 1: Jednoduché FEFO, 10denní období, nula dní dodací lhůty

Tento příklad ukazuje základní příklad doby skladovatelnosti, kde se fixace mezi objednávkami dodávek a poptávkou provádí za účelem uspokojení následujících cílů systému:

- Minimalizovat součet zpoždění.
- Maximalizovat součet nabídky FEFO.
- Minimalizovat doplňování zásob.

Systém má následující nastavení položek a hlavního plánu:

- **Kód pokrytí (strategie doplňování):** Doba 
- **Doba pokrytí:** 10 dní (rovná se trvanlivosti)
- **Trvanlivost**: 10 dní
- **Dny prodejnosti** 0 dní
- **Doba realizace:** 0 dní
- **Záporné dny:** 0 dní
- **Typ plánované objednávky (výchozí nastavení objednávky položky):** Nákupní objednávka

V systému existují následující prodejní objednávky pro položku:

- **SO1:** Množství = 2, požadovaný termín dodání = dnes + 1 den
- **SO2:** Množství = 1, požadovaný termín dodání = dnes + 4 dny
- **SO3:** Množství = 1, požadovaný termín dodání = dnes + 5 dnů

Všechny tyto prodejní objednávky vytvářejí poptávku po položce.

Pro položku existuje následující dodávka:

- **Zásoby na skladě:** Množství = 1, datum expirace = dnes + 5 dní
- **Nákupní objednávka 1 (PO1):** Datum přijetí = dnes + 2 dny, množství = 1, datum vypršení platnosti = dnes + 4 dny

Systém vytvoří seznam dodávek, které mohou pokrýt tuto poptávku, a seřadí seznam podle data expirace (pomocí FEFO).

Hlavní plánování vytváří požadovanou vazbu mezi nabídkou a poptávkou. Rovněž vytváří jakoukoli požadovanou poptávku na základě seznamu dodávek (pomocí FEFO) a zohledňuje datum dostupnosti.

- SO1 může být splněno množstvím na skladě, ale nemůže být splněno PO1, protože datum dostupnosti pro PO1 je o jeden den později, než požaduje SO1. SO1 tedy generuje poptávku po jedné jednotce zboží.
- SO2 může být pokryto PO1, protože PO1 dorazí v požadovaném čase a datum expirace bude stále platné. Proto je požadavek na SO2 plně pokryt PO1.
- SO3 není pokryta, protože zdroje nejsou k dispozici. SO3 tedy generuje poptávku po jedné jednotce zboží.

Pro pokrytí všech zbývajících požadavků musí systém vytvořit následující plánovanou nákupní objednávku:

- **PPO1:** Datum přijetí = dnes, množství = 2, datum vypršení platnosti = dnes + 10 dní

Výsledek je shrnut v následující tabulce.

| Poptávka | Doložení |
|---|---|
| **SO1:** Datum dodání = dnes + 1 den, množství = 2 | <p>**Na skladě:** Množství = 1, datum expirace = dnes + 5 dní</p><p>**PPO1:** Datum přijetí = dnes, množství = 1, datum vypršení platnosti = dnes + 10 dní</p> |
| **SO2:** Datum dodání = dnes + 4 dny, množství = 1 | **PO1:** Datum přijetí = dnes + 2 dny, množství = 1, datum vypršení platnosti = dnes + 4 dny |
| **SO3:** Datum dodání = dnes + 5 dny, množství = 1 | **PPO1:** Datum přijetí = dnes, množství = 2, datum vypršení platnosti = dnes + 10 dní |

Následující obrázek znázorňuje časovou osu v tomto příkladu.

![Příklad 1: Jednoduché FEFO, 10denní období, nula dní dodací lhůty.](media/fefo-example-1.png "Příklad 1: Jednoduché FEFO, 10denní období, nula dní dodací lhůty")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Příklad 2: Jednoduché FEFO, požadavek, tři dny doby realizace

Tento příklad ukazuje, jak může pokus systému minimalizovat zpoždění někdy způsobit přeřazení.

Systém má následující nastavení položek a hlavního plánu:

- **Kód pokrytí (strategie doplňování):** Požadavek
- **Trvanlivost**: 10 dní
- **Dny prodejnosti** 0 dní
- **Doba realizace:** Založeno následujícími obchodními dohodami prodejců:

    - **Obchodní smlouva 1:** pokud množství = 1, doba realizace = 4
    - **Obchodní smlouva 2:** pokud množství = 2, doba realizace = 3

- **Záporné dny:** 0 dní
- **Typ plánované objednávky (výchozí nastavení objednávky položky):** Nákupní objednávka

V systému existuje následující prodejní objednávka:

- **SO1:** Množství = 2, požadovaný termín dodání = dnes + 3 dnů

Tato poptávka je pokryta stávající nabídkou a potvrzenou nákupní objednávkou:

- **Zásoby na skladě:** Dostupné = dnes, množství = 1, datum expirace = dnes + 2 dny
- **PO1:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 4 dny

SO1 nelze naplnit zásobami na skladě, protože datum expirace zásob je před datem expedice. PO1 může pokrýt požadavek SO1 množstvím pouze 1. SO1 tedy generuje poptávku po jedné jednotce zboží. Pro pokrytí tohoto požadavku systém vytvoří plánovanou nákupní objednávku (PPO1).

Systém má dvě obchodní smlouvy (jedna pro množství = 1, dodací lhůta = 4 dny a jedna pro množství = 2, dodací lhůta = 3 dny). Systém se proto snaží minimalizovat zpoždění vytvořením plánované nákupní objednávky (PPO1), která splňuje druhou obchodní smlouvu. Výsledkem je navýšení dodávky (množství = 2, datum vypršení platnosti = dnes + 10 dní).

Výsledek je shrnut v následující tabulce.

| Poptávka | Doložení |
|---|---|
| **SO1:** Datum dodání = dnes + 3 dny, množství = 2 | <p>**PO1:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 4 dny</p><p>**PPO1:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 10 dny</p> |

Následující obrázek znázorňuje časovou osu v tomto příkladu.

![Příklad 2: Jednoduché FEFO, požadavek, tři dny doby realizace.](media/fefo-example-2.png "Příklad 2: Jednoduché FEFO, požadavek, tři dny doby realizace")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Příklad 3: Jednoduché FEFO, požadavek, tři dny doby realizace, pětr dnů prodejnosti

Tento příklad ukazuje, jak funguje skladovatelnost, když jsou pro položku přidány dny prodeje.

Systém má následující nastavení položek a hlavního plánu:

- **Kód pokrytí (strategie doplňování):** Požadavek
- **Trvanlivost**: 10 dní
- **Dny prodejnosti** 5 dní
- **Doba realizace:** 5 dní
- **Záporné dny:** 0 dní
- **Typ plánované objednávky (výchozí nastavení objednávky položky):** Nákupní objednávka

V systému existují následující prodejní objednávky:

- **SO1:** Množství = 2, požadovaný termín dodání = dnes + 2 dnů
- **SO2:** Množství = 1, požadovaný termín dodání = dnes + 3 dnů
- **SO3:** Množství = 1, požadovaný termín dodání = dnes + 5 dnů

Tuto poptávku lze pokrýt stávající nabídkou a potvrzenou nákupní objednávkou:

- **Zásoby na skladě:** Dostupné = dnes, množství = 1, datum expirace = dnes + 6 dny
- **PO1:** Datum přijetí = dnes + 2 dny, množství = 3, datum vypršení platnosti = dnes + 10 dny

Systém vytvoří seznam kandidátů na doložení na základě seznamu dodávek (FEFO) a dat dostupnosti. Proto SO1 nemůže být plněna zásobami na skladě, protože tyto zásoby vyprší před koncem dnů prodejnosti, které zákazník požaduje (požadované datum přijetí + 5 dní). PO1 může pokrýt potřebu SO1 dvěma jednotkami a potřebu SO2 jednou jednotkou. Pouze SO3 má tedy stále nepokrytou poptávku po jedné jednotce zboží. Pro pokrytí tohoto požadavku systém vytvoří následující plánovanou nákupní objednávku:

- **PP01:** Datum přijetí = dnes + 5 dny, množství = 1, datum vypršení platnosti = dnes + 10 dny

Výsledek je shrnut v následující tabulce.

| Poptávka | Doložení |
|---|---|
| **SO1:** Datum dodání = dnes + 2 dny, množství = 2 | **PO1:** Datum přijetí = dnes + 2 dny, množství = 2, datum vypršení platnosti = dnes + 10 dny |
| **SO2:** Datum dodání = dnes + 3 dny, množství = 1 | **PO1:** Datum přijetí = dnes + 2 dny, množství = 1, datum vypršení platnosti = dnes + 10 dny |
| **SO3:** Datum dodání = dnes + 5 dny, množství = 1 | **PPO1:** Datum přijetí = dnes + 5 dny, množství = 1, datum vypršení platnosti = dnes + 10 dny |

Následující obrázek znázorňuje časovou osu v tomto příkladu.

![Příklad 3: Jednoduché FEFO, požadavek, tři dny doby realizace, pětr dnů prodejnosti.](media/fefo-example-3.png "Příklad 3: Jednoduché FEFO, požadavek, tři dny doby realizace, pětr dnů prodejnosti")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Příklad 4: Jednoduché FEFO, období, dodací lhůta závisí na množství

Tento příklad ukazuje, jak může pokus systému minimalizovat zpoždění někdy způsobit přeřazení.

Systém má následující nastavení položek a hlavního plánu:

- **Kód pokrytí (strategie doplňování):** Doba
- **Doba pokrytí:** 10 dní (rovná se trvanlivosti)
- **Trvanlivost**: 10 dní
- **Dny prodejnosti** 0 dní
- **Doba realizace:** Založeno následujícími obchodními dohodami prodejců:

    - **Obchodní smlouva 1:** pokud množství = 1, doba realizace = 5
    - **Obchodní smlouva 2:** pokud množství = 2, doba realizace = 0

- **Záporné dny:** 0 dní
- **Typ plánované objednávky (výchozí nastavení objednávky položky):** Nákupní objednávka

V systému existují následující prodejní objednávky:

- **SO1:** Množství = 1, požadovaný termín dodání = dnes
- **SO2:** Množství = 1, požadovaný termín dodání = dnes + 6 dnů

Tato poptávka může být částečně pokryta stávající nabídkou z následujících potvrzených nákupních objednávek:

- **PO1:** Datum přijetí = dnes + 1 dny, množství = 1, datum vypršení platnosti = dnes + 2 dny
- **PO2:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 7 dny

Systém má dvě obchodní smlouvy (jedna pro množství = 1, dodací lhůta = 5 dny a jedna pro množství = 2, dodací lhůta = 0 dny). Systém se proto snaží minimalizovat zpoždění vytvořením následující plánované nákupní objednávky, která splňuje druhou obchodní smlouvu:

- **PP01:** Datum přijetí = dnes, množství = 2, datum vypršení platnosti = dnes + 10 dní

SO1 bude pokryta jednou jednotkou z PPO1. SO2 bude pokryto PO2, protože platnost PO2 vyprší dříve než PPO1.

Výsledek je shrnut v následující tabulce.

| Poptávka | Doložení |
|---|---|
| **SO1:** Datum dodání = dnes, množství = 1 | **PPO1:** Datum přijetí = dnes, množství = 1, datum vypršení platnosti = dnes + 10 dní |
| **SO2:** Datum dodání = dnes + 6 dny, množství = 1 | **PO2:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 7 dny |

> [!NOTE]
> PO1 se nepoužívá, protože přijde příliš pozdě na S01 a vyprší před doručením S02. PPO1 přeřadil o jednu jednotku, aby byl dodací čas 0 (nula), dle obchodní dohody 2.

Následující obrázek znázorňuje časovou osu v tomto příkladu.

![Příklad 4: Jednoduché FEFO, období, dodací lhůta závisí na množství.](media/fefo-example-4.png "Příklad 4: Jednoduché FEFO, období, dodací lhůta závisí na množství")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Příklad 5: Jednoduché FEFO, požadavek, 10 záporných dnů

<!-- KFM: This is more of a negative days example than a shelf life example. We should point out more explicitly how shelf life affects this situation (or maybe otherwise remove this example). -->

Tento příklad ukazuje, jak funguje skladovatelnost, když je k položce přidáno velké množství záporných dnů. Záporné dny představují počet dní, které jste ochotni čekat před objednáním nového doplnění položky, která má záporné množství zásob. Systém nevytváří zásobu, pokud není překročen počet záporných dnů.

Systém má následující nastavení položek a hlavního plánu:

- **Kód pokrytí (strategie doplňování):** Požadavek
- **Doba realizace:** 0 dní
- **Záporné dny:** 10 dní
- **Typ plánované objednávky (výchozí nastavení objednávky položky):** Nákupní objednávka

V systému existuje následující prodejní objednávka:

- **SO1:** Množství = 1, požadovaný termín dodání = dnes

Tato poptávka může být pokryta stávající nabídkou z následující potvrzené nákupní objednávky:

- **PO1:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 5 dny

Protože je systém nakonfigurován tak, aby umožňoval 10 záporných dní, pokrývá poptávku SO1 pomocí PO1, i když výsledkem bude zpoždění tří dnů, protože SO1 vytváří záporné zásoby, dokud nedorazí PO1. Nevytvoří se žádná plánovaná nákupní objednávka, přestože dodací lhůta je 0 (nula) a vytvoření plánované nákupní objednávky by zkrátilo zpoždění.

Výsledek je shrnut v následující tabulce.

| Poptávka | Doložení |
|---|---|
| **SO1:** Datum dodání = dnes, množství = 1 | **PO1:** Datum přijetí = dnes + 3 dny, množství = 1, datum vypršení platnosti = dnes + 5 dny |

Následující obrázek znázorňuje časovou osu v tomto příkladu.

![Příklad 5: Jednoduché FEFO, požadavek, 10 záporných dnů.](media/fefo-example-5.png "Příklad 5: Jednoduché FEFO, požadavek, 10 záporných dnů")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Příklad 6: Jednoduché FEFO, požadavek, pět záporných dnů

Tento příklad ukazuje, jak funguje skladovatelnost, když je počet záporných dnů pro položku menší než doba trvanlivosti.

Systém má následující nastavení položek a hlavního plánu:

- **Kód pokrytí (strategie doplňování):** Požadavek
- **Dny prodejnosti** 0 dní
- **Doba realizace:** 0 dní
- **Záporné dny:** 5 dní
- **Typ plánované objednávky (výchozí nastavení objednávky položky):** Nákupní objednávka

V systému existuje následující prodejní objednávka:

- **SO1:** Množství = 2, požadovaný termín dodání = dnes

Tato poptávka může být pokryta stávající nabídkou z následujících potvrzených nákupních objednávek:

- **PO1:** Datum přijetí = dnes, množství = 1, datum vypršení platnosti = dnes + 1 den
- **PO2:** Datum přijetí = dnes + 2 dny, množství = 1, datum vypršení platnosti = dnes + 3 dny

Systém však musí respektovat omezení, že platnost odeslaných položek nemůže vypršet v době odeslání. Proto PO2 a PO1 nelze použít pro SO1, protože platnost PO1 vyprší před příchodem PO2. Systém vytvoří následující plánovanou nákupní objednávku, aby dokončil pokrrytí požadavku na SO1:

- **PPO1:** Datum přijetí = dnes, množství = 1, datum vypršení platnosti = dnes + 10 dní

Systém může využít pět záporných dnů a použít PO2 a PPO1 k pokrytí SO1. Tento přístup však způsobí, že doručení bude zpožděno, dokud nepřijde PO2, a platnost PO1 mezitím vyprší. Proto systém pokrývá SO1 pomocí PPO1 a PO1.

Výsledek je shrnut v následující tabulce.

| Poptávka | Doložení |
|---|---|
| **SO1:** Datum dodání = dnes, množství = 2 | <p>**PO1:** Datum přijetí = dnes, množství = 1, datum vypršení platnosti = dnes + 1 den</p><p>**PPO1:** Datum přijetí = dnes, množství = 1, datum vypršení platnosti = dnes + 10 dní</p> |

Následující obrázek znázorňuje časovou osu v tomto příkladu.

![Příklad 6: Jednoduché FEFO, požadavek, pět záporných dnů.](media/fefo-example-6.png "Příklad 6: Jednoduché FEFO, požadavek, pět záporných dnů")
