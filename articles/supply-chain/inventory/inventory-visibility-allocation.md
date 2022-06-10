---
title: Doplněk Viditelnost skladu - Přidělení zásob
description: Toto téma vysvětluje, jak nastavit a používat funkci přidělení zásob, která vám umožní odložit vyhrazené zásoby, abyste zajistili, že budete moci plnit své nejziskovější kanály nebo zákazníky.
author: yufeihuang
ms.date: 05/20/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 4293ead4ccfc9ba04e8b9da437134b4e97569026
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786943"
---
# <a name="inventory-visibility-inventory-allocation"></a>Doplněk Viditelnost skladu - Přidělení zásob

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Obchodní zázemí a účel

V mnoha případech musejí výrobci, maloobchodníci a další články v dodavatelském řetězci předem alokovat zásoby pro důležité prodejní kanály, umístění nebo zákazníky, nebo pro konkrétní prodejní akce. Přidělení zásob je typickou praxí v procesu operativního plánování prodeje a provádí se před skutečnými prodejními aktivitami a vytvořením prodejní objednávky.

Například společnost vyrábějící jízdní kola má k dispozici omezené zásoby dílů pro velmi oblíbené kolo. Tato společnost provádí prodej online i v kamenných obchodech. V každém prodejním kanálu má společnost několik důležitých firemních partnerů (tržišť a velkých maloobchodníků), kteří požadují, aby pro ně byla uložena určitá část dostupných zásob kol. Proto musí být společnost vyrábějící kola schopna vyvážit distribuci zásob napříč kanály a také řídit očekávání svých VIP partnerů. Nejlepším způsobem, jak dosáhnout obou cílů, je použít přidělení zásob, takže každý kanál a maloobchodník mohou získat konkrétní přidělená množství, která mohou být později prodána spotřebitelům.

Přidělení zásob má dva základní obchodní účely:

- **Ochrana zásob (ringfencing)** – Organizace chtějí předem přidělit omezené zásoby prioritním kanálům, regionům, VIP zákazníkům a dceřiným společnostem. Funkce přidělení doplňku Viditelnost zásob má za cíl chránit přidělené zásoby, aby ostatní přidělení, rezervace nebo jiné požadavky na prodej neovlivnily dříve přidělené zásoby.
- **Kontrola přeprodeje** – Funkce přidělení doplňku Viditelnost zásob má za cíl omezit dříve přidělená množství, aby je přijímající strana (například kanál nebo skupina zákazníků) nespotřebovala nadměrně, když skutečná prodejní transakce založená na předběžné rezervaci vstoupí v platnost.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Definice přidělení ve službě viditelnosti zásob

Přestože funkce přidělení ve službě Viditelnost zásob nevyčleňuje množství fyzické zásoby, odkazuje na dostupné množství fyzické zásoby, aby bylo možné definovat její počáteční množství *k dispozici pro přidělení* virtuálního fondu. Přidělení zásob ve Viditelnosti zásob je předběžné přidělení. Provádí se před skutečnými prodejními transakcemi a nezávisí na prodejních objednávkách. Můžete například přidělit zásoby svým nejdůležitějším prodejním kanálům nebo velkým maloobchodníkům dříve, než koncoví zákazníci navštíví prodejní kanál nebo maloobchod, aby si je koupili.

Rozdíl mezi přidělením zásob a [předběžnou rezervací zásob](inventory-visibility-reservations.md) je v tom, že předběžná rezervace je obvykle spojena se skutečnými prodejními transakcemi (řádky prodejních objednávek). Pokud tedy chcete používat funkce přidělení a předběžné rezervace společně, doporučujeme provést nejprve přidělení zásob a poté předběžnou rezervaci proti přiděleným množstvím. Více informací viz část [Spotřeba jako předběžná rezervace](#consume-to-soft-reserved).

Funkce přidělení zásob umožňuje plánovačům prodeje nebo manažerům klíčových zákazníků spravovat a předem přidělovat důležité zásoby napříč skupinami přidělení (jako jsou kanály, regiony a skupiny zákazníků). Podporuje také sledování v reálném čase, úpravu a analýzu spotřeby oproti přiděleným množstvím, takže doplnění nebo přerozdělení může být provedeno včas. Tato schopnost mít přehled o přidělení, spotřebě a bilanci přidělení je zvláště důležitá při akcích rychlého prodeje nebo propagačních akcích.

## <a name="terminology"></a>Terminologie

Při výkladu přidělování zásob budeme používat následující pojmy a koncepty:

- **Skupina přidělení** – Skupina, která vlastní přidělení, jako je prodejní kanál, skupina zákazníků nebo typ objednávky.
- **Hodnota skupiny přidělení** – Hodnota každé skupiny přidělení. Například *web* nebo *prodejna* může být hodnotou skupiny přidělení prodejních kanálů, zatímco *VIP* nebo *normální* může být hodnota skupiny přidělení zákazníků.
- **Hierarchie přidělení** – Prostředek ke kombinování skupin přidělení hierarchickým způsobem. Můžete například definovat *kanál* jako úroveň hierarchie 1, *oblast* jako úroveň 2 a *skupinu zákazníků* jako úroveň 3. Během přidělování zásob musíte při zadávání hodnoty skupiny přidělení postupovat podle pořadí hierarchie přidělování. Můžete například přidělit 200 červených kol kanálu *Web*, oblasti *Londýn* a skupině zákazníků *VIP*.
- **K dispozici pro přidělení** – *Virtuální společný fond*, který udává množství, které je k dispozici pro další přidělení. Je to vypočítaná míra, kterou můžete volně definovat pomocí vlastního vzorce. Pokud také používáte funkci předběžných rezervací, doporučujeme použít stejný vzorec pro výpočet dostupných přidělení a dostupných rezervací.
- **Přiděleno** – Fyzická míra, která ukazuje přidělenou kvótu, kterou mohou spotřebovat skupiny přidělení.
- **Spotřebováno** – Fyzická míra, která označuje množství, která byla spotřebována oproti původně přidělenému množství. Jak se k této fyzické míře přičítají další čísla, automaticky se snižuje přidělovaná fyzická míra.

Následující obrázek znázorňuje příklad pracovního postupu pro přidělování zásob.

![Pracovní postup přidělení Viditelnosti zásob.](media/inventory-visibility-allocation-flow.png "Pracovní postup přidělení Viditelnosti zásob.")

## <a name="set-up-inventory-allocation"></a>Příprava přidělování zásob

Funkce přidělování zásob se skládá z následujících součástí:

- Předdefinovaný zdroj dat související s přidělením, fyzické míry a vypočítané míry.
- Přizpůsobitelné skupiny přidělení, které mají maximálně osm úrovní.
- Sada aplikačních programovacích rozhraní (API) pro přidělování:

    - allocate
    - reallocate
    - unallocate
    - consume
    - query

Proces konfigurace funkce přidělení je složen ze dvou kroků:

- Nastavte [zdroj dat](inventory-visibility-configuration.md#data-source-configuration) a jeho [míry](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Nastavte název a hierarchii skupiny přidělení.

### <a name="predefined-data-source"></a>Předdefinovaný zdroj dat

Když povolíte funkci přidělení a zavoláte rozhraní API pro aktualizaci konfigurace, Viditelnost zásob vytvoří jeden předdefinovaný zdroj dat a několik počátečních opatření.

Zdroj dat se jmenuje `@iv`.

Zde jsou počáteční fyzické míry:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Zde jsou počáteční vypočítané míry:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Přidejte další fyzické míry do vypočítané míry K dispozici pro přidělení

Chcete-li použít přidělení, musíte nastavit vypočítanou míru K dispozici pro přidělení (`@iv` .`@available_to_allocate`). Například máte zdroj dat `fno` a míru `onordered`, zdroj dat `pos` a míru `inbound` a chcete provést přidělení zásob na skladě ve výši součtu `fno.onordered` a `pos.inbound`. V tomto případě by `@iv.@available_to_allocate` měla ve vzorci obsahovat `pos.inbound` a `fno.onordered`. Následuje příklad:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

### <a name="change-the-allocation-group-name"></a>Změňte název skupiny přidělení

Nastavit se dá maximálně osm názvů skupin přidělení. Skupiny mají hierarchii.

Názvy skupin se zadávají na stránce **Konfigurace aplikace Viditelnost zásob**. Chcete-li otevřít tuto stránku, otevřete v prostředí Microsoft Dataverse aplikaci Viditelnost zásob a vyberte položku **Konfigurace \> Přidělení**.

Pokud například použijete čtyři názvy skupin a nastavíte je na \[`channel`, `customerGroup`, `region`, `orderType`\], budou tato jména platná pro požadavky související s přidělením, když zavoláte rozhraní API pro aktualizaci konfigurace.

### <a name="allcoation-using-tips"></a>Přidělení pomocí tipů

- U každého produktu by funkce přidělení měla používat stejnou úroveň dimenze podle hierarchie indexu produktu, kterou nastavíte v [konfiguraci hierarchie indexu produktů](inventory-visibility-configuration.md#index-configuration). Hierarchie indexu je například lokalita, umístění, barva, velikost. Pokud přidělíte nějaké množství pro jeden produkt na úrovni lokality, umístění, barvy. Při příštím přidělení byste měli také použít úrovně lokality, umístění, barvy, pokud použijete lokalitu, umístění, barvu a velikost nebo lokalitu a umístění, nebudou data konzistentní.
- Změna názvu skupiny přidělení neovlivní data uložená ve službě.
- K přidělení by mělo dojít poté, co má produkt kladné množství na skladě.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a>Použití rozhraní API pro přidělování

V současné době je otevřeno pět rozhraní API pro přidělování:

- POST /api/environment/{environmentId}/allocation/allocate
- POST /api/environment/{environmentId}/allocation/unallocate
- POST /api/environment/{environmentId}/allocation/reallocate
- POST /api/environment/{environmentId}/allocation/consume
- POST /api/environment/{environmentId}/allocation/query

#### <a name="allocate"></a>Allocate

Volání `Allocate` API použijte, když chcete přidělit produkt, který má konkrétní dimenze. Zde je schéma pro tělo požadavku.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Například chcete přidělit množství 10 produktu *Kolo* pro lokalitu *1*, umístění je *11*, barva *červená*, kanál *Online*, skupina zákazníků *VIP* a oblast *US*. Chcete-li provést toto přidělení, odešlete volání API s následujícím obsahem těla.

```json
{
    "id": "???",
    "productId": "Bike",
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Množství musí být vždy větší než 0 (nula).

#### <a name="unallocate"></a>Unallocate

Volání `Unallocate` API použijte ke zrušení operace `Allocate`. Záporné množství není v operaci `Allocate` povoleno. Tělo volání `Unallocate` je shodné s tělem volání `Allocate`.

#### <a name="reallocate"></a>Reallocate

Volání `Reallocate` API použijte k přesunutí určitého přiděleného množství do jiné kombinace skupin. Zde je schéma pro tělo požadavku.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "targetGroups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Můžete například přesunout dvě kola, která mají dimenze \[lokalita=1, umístění=11, barva=červená\] ze skupiny přidělení \[Online, VIP, USA\] do skupiny přidělení \[Online, VIP, EU\] voláním `Reallocate` API s následujícím textem těla.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

#### <a name="consume"></a>Consume

Volání `Consume` API použijte k zaúčtování množství spotřeby proti přidělení. Toto rozhraní API můžete například použít k přesunutí přiděleného množství na některé reálné míry. Zde je schéma pro tělo požadavku.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Například existuje osm přidělených kol, která mají dimenze \[lokalita=1, umístění=11, barva=červená\] pro skupinu přidělení \[Online, VIP, USA\]. Použije se následující vzorec pro přidělení:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

Osm kol je přiděleno z míry `pos.inbound`.

Následně jsou tři kola prodána a jsou odebrána z fondu přidělení. Chcete-li registrovat tento přesun, odešlete volání API s následujícím tělem požadavku.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Po tomto volání bude přidělené množství produktu sníženo o 3. Viditelnost zásob navíc vygeneruje událost změny na skladě, kde `pos.inbound` = *-3*. Případně můžete hodnotu `pos.inbound` ponechat tak, jak je, a pouze spotřebujte přidělené množství. V tomto případě však musíte buď vytvořit další fyzickou míru, abyste zachovali spotřebovaná množství, nebo použít předdefinovanou míru `@iv.@consumed`.

V tomto požadavku si všimněte, že fyzická míra, kterou používáte v těle požadavku consume, by měla používat opačný typ modifikátoru (sčítání nebo odčítání) ve srovnání s typem modifikátoru použitým ve vypočítané míře. Takže v těle požadavku consume má `iv.inbound` hodnotu `Subtraction`, ne `Addition`.

Zdroj dat `fno`nelze použít v těle consume, protože Viditelnost zásob nemůže změnit žádná data ve zdroji dat `fno`. Tok dat je jednosměrný, což znamená, že veškeré změny množství pro zdroj dat `fno` musejí pocházet z vašeho prostředí Supply Chain Management.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Spotřeba jako předběžná rezervace

Volání `Consume` API může také spotřebovat přidělené množství jako předběžnou rezervaci. V tomto případě volání `Consume` sníží přidělené množství a poté pro toto množství provede předběžnou rezervaci. Chcete-li použít tento přístup, musíte také používat funkci [předběžné rezervace](inventory-visibility-reservations.md) Viditelnosti zásob.

Například jste nastavili modifikátor předběžné rezervace (míru) na `iv.softreserved`. Pro vypočítanou míru K dispozici pro rezervaci se používá následující vzorec:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Chcete-li použít toto nastavení s funkcí přidělení, přidejte `@iv.@allocated` do vzorce `iv.available_to_reserve` a vytvořte následující vzorec:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Poté aktualizujte `@iv.@available_to_allocate` na stejnou hodnotu.

Pokud chcete spotřebovat množství 3 a přímo rezervovat toto množství, můžete odeslat volání s následujícím tělem požadavku.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

V požadavku si všimněte, že `iv.softreserved` má hodnotu `Addition`, ne `Subtraction`.

#### <a name="query"></a>Query

Volání `Query` API použijte k načtení informací souvisejících s přidělením u některých produktů. K zúžení výsledků můžete použít filtry dimenzí a filtry skupin přidělení. Dimenze se musejí přesně shodovat s těmi, které chcete načíst, např. \[lokalita=1, umístění=11\] bude mít nesouvisející výsledky ve srovnání s kombinací \[lokalita=1, umístění=11, barva=červená\].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Použijte například \[lokalita=1, umístění=11, barva=červená\] a prázdné pole skupin, abyste získali všechny záznamy o přidělení:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

K získání záznamů o přidělení pro tuto skupinu použijte zápis \[lokalita=1, umístění=11, barva=červená\] a skupiny \[channel=Online, customerGroup=VIP, region=US\]:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId&quot;: &quot;red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region&quot;: &quot;US"
    },
}
```
