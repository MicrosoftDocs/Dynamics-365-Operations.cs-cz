---
title: Hlavní plánování s prognózami dodávek
description: Tento článek popisuje, jak jsou prognózy dodávek zvažovány během hlavního plánování.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690074"
---
# <a name="master-planning-with-supply-forecasts"></a>Hlavní plánování s prognózami dodávek

[!include [banner](../../includes/banner.md)]

Prognózy zásob vám umožňují specifikovat zásoby, které očekáváte, že budete potřebovat v nějakém budoucím období. Odhad obvykle založíte na historii prodeje z předchozího roku a prognózu pak použijete pro účely rozpočtování. Můžete také nastavit hlavní plány tak, aby při plánování zohledňovaly prognózy.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Nastavení hlavního plánu tak, aby zvažoval prognózu dodávek

Můžete určit, zda má každý hlavní plán při spuštění zohledňovat prognózy. Pomocí následujícího postupu nastavte možnosti prognózy pro každý plán.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Buď vyberte existující hlavní plán v podokně seznamu nebo vyberte v podokně akcí možnost **Nový** a vytvořte nový.
1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Model prognózy** – Vyberte model, který obsahuje prognózy nabídky a/nebo poptávky, které by měl hlavní plán zohlednit.
    - **Zahrnout prognózu dodávek** - Tuto možnost nastavte na *Ano*, pokud má hlavní plán zvažovat prognózu dodávek.
    - **Zahrnout prognózu poptávky** - Tuto možnost nastavte na *Ano*, pokud má hlavní plán zvažovat prognózu poptávky. Ačkoli toto nastavení je nezávislé na nastavení **Zahrnout prognózu dodávek**, některá další nastavení na stránce platí pro prognózy dodávek i prognózy poptávky. Další informace o plánování, které zohledňuje prognózy poptávky, viz [Ovládněte plánování s prognózami poptávky](demand-forecast.md).
    - **Metoda použitá ke snížení požadavků na prognózu** - Vyberte metodu ke snížení požadavků na prognózu během hlavního plánování:

        - *Žádné* – Požadavky na prognózu nebudou během hlavního plánování sníženy.
        - *Procento – redukční klíč* - Požadavky na prognózu budou sníženy podle procenta a časových období, které jsou definovány v redukčním klíči.
        - *Transakce – redukční klíč* - Požadavky na prognózu budou sníženy podle transakcí probíhajících během časových období, které jsou definovány v redukčním klíči.
        - *Transakce – dynamické období* - Požadavky prognózy budou sníženy podle transakcí objednávky, ke kterým došlo během dynamického období. Dynamické období pokrývá aktuální data prognózy a končí na začátku další prognózy. Metoda *Transakce – dynamické období* nepoužívá ani nevyžaduje redukční klíč, a když ji použijete, platí následující podmínky:

            - Pokud je prognóza snížena úplně, požadavky prognózy pro aktuální prognózu budou 0 (nula).
            - Pokud neexistuje žádná budoucí prognóza, požadavky prognózy z poslední zadané prognózy budou sníženy.
            - Ochranná doba je zahrnuta do výpočtu snížení prognózy.
            - Kladné dny jsou zahrnuty do výpočtu snížení prognózy.
            - Překračuje-li skutečná transakce objednávky požadavky prognózy, zbývající transakce nejsou předávány do dalšího období prognózy.

        > [!NOTE]
        > Nastavení **Metoda používaná ke snížení požadavků na prognózu** se vztahuje také na prognózy poptávky, pokud jste je povolili pro hlavní plán, a ovlivňuje je podobným způsobem. Další informace naleznete v části [Hlavní plánování s prognózami poptávky](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Nastavte možnosti redukce pro skupiny pokrytí

Chcete-li nastavit možnosti, které určují, jak skupina pokrytí sníží své požadavky na prognózu pro hlavní plány, které používají redukci na základě transakcí, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Skupiny disponibility**.
1. Buď vyberte existující skupinu pokrytí v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte novou.
1. Na pevné záložce **Ostatní**, v poli **Snížit prognózu o** určete, jak by měly být sníženy požadavky na prognózu dodávek pro položky ve skupině pokrytí, pro hlavní plány, kde je pole **Metoda použitá ke snížení požadavků na prognózu** nastaveno na *Transakce- redukční klíč* nebo *Transakce - dynamické období*. Vyberte jednu z následujících hodnot:

    - *Všechny transakce* - Všechny transakce by měly snížit prognózu.
    - *Objednávky* - Pouze objednávky stejného typu by měly snížit prognózu.

    Například výchozí nastavení objednávky pro položku označují, že by měla být vyrobena. Existuje řádek prognózy dodávek pro množství 50 a existuje stávající nákupní objednávka pro množství 20. Pokud je pole **Snížit prognózu o** nastaveno na *Objednávky*, bude vytvořena plánovaná výrobní zakázka na množství 50. Pokud je nastaveno na *Všechny transakce*, plánovaná výrobní zakázka bude snížena na množství 30.

    Toto nastavení platí také pro snížení prognózy poptávky. Další informace naleznete v části [Hlavní plánování s prognózami poptávky](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Zadejte prognózu dodávek pro produkt

Chcete-li zadat prognózu dodávek pro produkt, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt, ke kterému chcete zadat prognózu.
1. V podokně akcí na kartě **Plánování** vyberte **Prognóza dodávek**.
1. Na stránce **Prognóza dodávek**, v podokně akcí vyberte možnost **Nový**, a přidejte prognózu do mřížky.
1. Zadejte informace do nového řádku podle potřeby pro upřesnění vaší prognózy.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Plán pro položku s řádky prognózy dodávek

Když spustíte hlavní plán, který obsahuje položku, pro kterou existuje prognóza dodávek, systém vytvoří nákupní objednávku pro zadané řádky dodávek. Výchozí nastavení objednávky pro položku jsou respektována. Pokud tato výchozí nastavení objednávky specifikují hodnotu **Výchozí typ objednávky** položky *Nákupní objednávka* a na řádku prognózy dodávek není zadán žádný účet dodavatele, systém použije pro položku výchozího dodavatele.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Zkontrolujte, zda plánovaná objednávka je objednávkou prognózy dodávek

Pomocí následujícího postupu zjistíte, zda byla na základě prognózy dodávek vytvořena plánovaná objednávka.

1. Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**.
1. Otevřete plánovanou objednávku, kterou chcete zkontrolovat.
1. Na pevné záložce **Obecné** se podívehte na pole **Prognóza dodávek**. Pokud byla objednávka vytvořena pro pokrytí prognózy dodávek, toto pole bude nastaveno na *Ano*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Příklady hlavního plánování s prognózami dodávek

Tato část obsahuje několik příkladů, které ukazují, jak prognóza dodávek ovlivňuje hlavní plánování.

### <a name="example-1-supply-forecast-for-an-item"></a>Příklad 1: Prognóza dodávek pro položku

Máte položku, kde je výchozí typ objednávky *Nákupní objednávka* a výchozím dodavatelem je *US-002*. Má následující řádek prognózy dodávek.

| Model    | Datum     | Účet dodavatele | Skupina dodavatelů | Množství | Jednotka | Web | Sklad |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | ks   | 1    | 11        |

Když spustíte hlavní plánování, vytvoří se plánovaná nákupní objednávka na *35 ea* od prodejce *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Příklad 2: Několik řádků prognózy dodávek s dodavatelem a bez něj

Máte položku, kde je výchozí typ objednávky *Nákupní objednávka* a výchozím dodavatelem je *US-002*. Má následující řádky prognózy dodávek.

| Model    | Datum     | Účet dodavatele | Skupina dodavatelů | Množství | Jednotka | Web | Sklad |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | ks   | 1    | 11        |
| CurrentF | 10/10/22 | US-101         |              | 25       | ks   | 1    | 11        |

V tomto případě systém považuje řádek, který neurčuje dodavatele, za obecnou prognózu a předpokládá, že řádek, který dodavatele uvádí, by měl být odečten od obecné prognózy. Proto hlavní plánování vytvoří pro položku následující plánované nákupní objednávky:

- Plánovaná nákupní objednávka na množství *25 ea* od prodejce *US-101* (Použije se prodejce a množství, které jsou uvedeny na řádku prognózy.)
- Plánovaná nákupní objednávka na množství *10 ea* od prodejce *US-002* (Protože na druhém řádku prognózy nebyl zadán žádný dodavatel, použije se výchozí dodavatel a množství tohoto řádku prognózy se sníží o množství řádku prognózy specifického pro dodavatele.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Příklad 3: Plány, které používají metodu Transakce – dynamické snížení období v jednom období prognózy

Pro hlavní plány, které používají *Transakce - dynamické období* jako metodu snížení prognózy, hlavní plánování sníží předpokládané množství, pokud existují transakce, které odpovídají těmto charakteristikám dodávek.

Máte například položku, kde je výchozí typ objednávky *Nákupní objednávka*. Má následující řádek prognózy dodávek.

| Model    | Datum     | Účet dodavatele | Skupina dodavatelů | Množství | Jednotka | Web | Sklad |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | ks   | 1    | 11        |

Protože existuje pouze jeden řádek prognózy dodávek, existuje pouze jedno období prognózy.

Když spustíte hlavní plán, který je nastaven k použití *Transakce – dynamické období* jako redukční metodu, může dojít k jednomu z následujících výsledků:

- Pokud pro dodavatele existuje nákupní objednávka *US-101* a množství *10 ea* a pole **Prognóza dodávek** je nastaveno na *Ano*, hlavní plánování vytvoří novou plánovanou nákupní objednávku pro zbývající množství *10 ea*. Řádek prognózy je zmenšen, protože dodavatel odpovídá existující nákupní objednávce.
- Pokud existuje nákupní objednávka pro dodavatele *US-102*, site *1*, sklad *11* a množství *10 ea* a pole **Prognóza dodávek** je nastaveno na *Ano*, hlavní plánování vytvoří novou plánovanou nákupní objednávku pro plné množství *25 ea*. Řádek prognózy nelze zmenšit, protože má jiného dodavatele než stávající nákupní objednávka.

> [!NOTE]
> Tato situace může nastat u plánovaných nákupních objednávek, protože je k nim přidružen dodavatel. U převodních zakázek a výrobních zakázek však budou předpokládané částky dodávek vždy sníženy o stávající zakázky, protože pro tyto typy zakázek není určen žádný dodavatel.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Příklad 4: Plány, které používají metodu Transakce – dynamické snížení období ve více obdobích prognózy

Máte položku, kde je výchozí typ objednávky *Nákupní objednávka*. Má následující řádky prognózy dodávek.

| Model    | Datum     | Účet dodavatele | Skupina dodavatelů | Množství | Jednotka | Web | Sklad |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | ks   | 1    | 11        |
| CurrentF | 10/15/22 | US-101         |              | 25       | ks   | 1    | 11        |

V tomto příkladu jsou dva řádky prognózy, z nichž každá má jiné datum. Data proto určují hranice období prognózy. První období je od 10. října do 14. října 2022 (10/10/22–10/14/22). Druhý je od 15. října 2022 (10/15/22) dále.

Existuje existující nákupní objednávka pro dodavatele *US-101*, množství *10 ea* a datum *10/12/22* (12. října 2022). Když spustíte hlavní plán, který je nastaven k použití *Transakce – dynamické období* jako redukční metodu, vytvoří následující objednávky:

- Plánovaná objednávka na množství *15 ea* a datum *10/10/22* (Množství je sníženo o stávající nákupní objednávku, která je datována ve stejném období prognózy.)
- Plánovaná objednávka na množství *25 ea* a datum *15.10.22* (Množství je celé množství prognózy.)

### <a name="example-5-plans-that-use-no-reduction"></a>Příklad 5: Plány, které nepoužívají žádné snížení

Když spustíte plán, kde je metoda snížení prognózy *Žádný*, hlavní plánování vždy vytvoří plánovanou dodávku pro všechny řádky prognózy dodávek. Po schválení této plánované dodávky se sníží budoucí plánované objednávky. Nákupní objednávky však nesníží řádky prognózy dodávek.

Máte například položku, kde je výchozí typ objednávky *Nákupní objednávka*. Má následující řádek prognózy dodávek.

| Model    | Datum     | Účet dodavatele | Skupina dodavatelů | Množství | Jednotka | Web | Sklad |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | ks   | 1    | 11        |

Existuje existující nákupní objednávka pro dodavatele *US-101*, site *1*, sklad *11*, množství *25 ea* a datum *10/10/22*. 

Když spustíte hlavní plán, který je nastaven k použití metody snížení *Žádný*, vytvoří plánovanou nákupní objednávku pro dodavatele *US-101*, site *1*, sklad *11*, množství *25 ea* a datum *10/10/22*. Jinými slovy, stávající nákupní objednávka nebude redukována, protože metoda snížení prognózy je *Žádný*.

Nyní upravíte plánovanou nákupní objednávku, která byla vytvořena po posledním spuštění plánování, a změníte množství na *15 ea*. Pak schválíte objednávku. Až příště spustíte hlavní plán, vytvoří plánovanou nákupní objednávku pro dodavatele *US-101*, site *1*, sklad *11*, množství *10 ea* a datum *10/10/22*. Tentokrát bude množství sníženo tak, aby odráželo množství existující schválené objednávky z předchozího běhu plánování.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Rozdíly mezi Optimalizací plánování a integrovaným plánovacím modulem

Prognózy dodávek fungují trochu odlišně na základě toho, který modul plánování používáte (nebo integrovaný plánovací modul nebo Optimalizace plánování). Tato část popisuje rozdíly.

### <a name="vendor-groups"></a>Skupiny dodavatelů

Když přidáte řádek prognózy, můžete určit dodavatele a skupinu dodavatelů. Ve vestavěném modulu plánování jsou vytvořené plánované objednávky seskupeny podle kombinace hodnot dodavatele a skupiny dodavatelů. V Optimalizaci plánování jsou plánované objednávky seskupeny podle dodavatele.

Následující tabulka uvádí některé příklady řádků prognózy dodávek pro položku.

| Model    | Datum     | Účet dodavatele | Skupina dodavatelů | Množství | Jednotka | Web | Sklad |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                | VendorGroupA | 5        | ks   | 1    | 11        |
| CurrentF | 10/10/22 |                | VendorGroupA | 6        | ks   | 1    | 11        |
| CurrentF | 10/10/22 |                |              | 7        | ks   | 1    | 11        |

Prodejce *VendorA* je výchozí dodavatel pro skupinu dodavatelů *VendorGroupA*. Jedná se také o výchozího dodavatele pro položku.

Vestavěný plánovací modul vytvoří následující objednávky:

- Plánovaná nákupní objednávka pro dodavatele *VendorA*, skupinu prodejců *VendorGroupA* a množství *11*
- Plánovaná nákupní objednávka pro dodavatele *VendorA* a množství *7*

Optimalizace plánování vytvoří pouze jednu objednávku:

- Plánovaná nákupní objednávka pro dodavatele *VendorA*, skupinu prodejců *VendorGroupA* a množství *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Redukce obecných prognóz o konkrétnější prognózy

Ve vestavěném modulu hlavního plánování je výsledek nepředvídatelný, pokud některé prognózy mají dodavatele, ale jiné ne.

V Optimalizaci plánování jsou obecné prognózy vždy redukovány o konkrétnější prognózy, jak ukazuje následující příklad.

Následující tabulka uvádí některé příklady řádků prognózy dodávek pro položku.

| Datum       | Množství | Dodavatel   | Skupina dodavatelů  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Vendor-A | VendorGroup-A |
| 02/11/2022 | 6,00     | Vendor-A | VendorGroup-A |
| 02/11/2022 | 15.00    |          |               |

Obecná prognóza (pro 15,00 kusů) je redukována o specifičtější prognózy (pro 5,00 + 6,00 = 11,00 kusů). Zbytek je přiřazen výchozímu dodavateli. Následující tabulka zobrazuje plánované objednávky.

| Datum       | Množství | Dodavatel   | Skupina dodavatelů  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11.00    | Vendor-A | VendorGroup-A |
| 02/11/2022 | 4.00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Respektování výchozího nastavení objednávky při generování plánovaných objednávek

Každá položka může mít výchozí nastavení objednávky, jako je minimální množství nákupní objednávky. Vestavěný plánovací modul ignoruje tato nastavení, a proto převádí prognózy do plánovaných objednávek, které mají stejné množství. Optimalizace plánování respektuje tato nastavení, když jsou plánované objednávky generovány z prognóz dodávek. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Agregace plánovaných objednávek v důsledku redukce o schválené zakázky

Vestavěný modul hlavního plánování předpokládá, že pouze jedna objednávka sníží stávající prognózu dodávek. Pokud tedy několik objednávek odpovídá řádku prognózy dodávek, sníží ji pouze první objednávka. V Optimalizaci plánování se všechny objednávky, které odpovídají linii prognózy dodávek, sníží.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Snížení prognóz pouze odpovídajícími dodavateli

Když vestavěný modul hlavního plánování redukuje prognózu o existující uvolněné nákupní objednávky, nezajistí, že se dodavatel na nákupní objednávce shoduje s dodavatelem z prognózy. Optimalizace plánování snižuje prognózy pouze u nákupních objednávek, které mají odpovídající hodnotu v poli dodavatele.

U převodních a výrobních objednávek je pole dodavatele vždy ignorováno, protože pro tyto typy zakázek není relevantní.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Redukce předpovědí převodními příkazy

Pokud je výchozí typ objednávky pro položku *Převod*, prognózy lze snížit pouze o existující plánované převodní příkazy. U výrobních zakázek a nákupních zakázek však prognózu dodávek snižují pouze uvolněné objednávky.

Vestavěný plánovací modul snižuje pro všechny stavy převodních příkazů, zatímco Optimalizace plánování snižuje prognózy pouze o převodní příkazy, které jsou ve stavu *Uvolněno*.
