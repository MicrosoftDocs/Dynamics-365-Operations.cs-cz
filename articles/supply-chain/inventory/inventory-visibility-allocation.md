---
title: Přidělení zásob v Inventory Visibility
description: Tento článek vysvětluje, jak nastavit a používat funkci přidělení zásob, která vám umožní odložit vyhrazené zásoby, abyste zajistili, že budete moci plnit své nejziskovější kanály nebo zákazníky.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762665"
---
# <a name="inventory-visibility-inventory-allocation"></a>Přidělení zásob v Inventory Visibility

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Obchodní zázemí a účel

Organizace často musí předem přidělit své skladové zásoby svým nejdůležitějším prodejním kanálům, skupinám zákazníků, regionům a propagačním akcím, aby zajistily, že předem přidělené zásoby budou chráněny proti jakémukoli jinému použití a že je lze spotřebovat pouze prostřednictvím prodejních transakcí, které jsou relevantní pro dané přidělení. Přidělení zásob ve Viditelnosti zásob je komponentou v procesu operativního plánování prodeje a provádí se před skutečnými prodejními aktivitami a vytvořením prodejní objednávky.

Například společnost, která se jmenuje Contoso, vyrábí populární kolo. Bohužel, protože nedávné narušení dodavatelského řetězce ovlivnilo všechny zásoby tohoto kola v tranzitu, Contoso má pouze omezené zásoby na skladě a musí je co nejlépe využít. Contoso provádí prodej online i v kamenných obchodech. V každém prodejním kanálu má společnost několik důležitých firemních partnerů (tržišť a velkých maloobchodníků), kteří požadují, aby pro ně byla uložena určitá část dostupných zásob kol. Proto musí být společnost vyrábějící kola schopna vyvážit distribuci zásob napříč kanály a také řídit očekávání svých VIP partnerů. Nejlepším způsobem, jak dosáhnout obou cílů, je použít přidělení zásob, takže každý kanál a maloobchodník mohou získat konkrétní přidělená množství, která mohou být později prodána spotřebitelům.

Přidělení zásob má dva základní obchodní účely:

- **Ochrana zásob (ringfencing)** – Organizace chtějí předem přidělit omezené zásoby prioritním kanálům, regionům, VIP zákazníkům a dceřiným společnostem. Funkce přidělení doplňku Viditelnost zásob má za cíl chránit přidělené zásoby, aby ostatní přidělení, rezervace nebo jiné požadavky na prodej neovlivnily dříve přidělené zásoby.
- **Kontrola přeprodeje** – Funkce přidělení doplňku Viditelnost zásob má za cíl omezit dříve přidělená množství, aby je přijímající strana (například kanál nebo skupina zákazníků) nespotřebovala nadměrně, když skutečná prodejní transakce založená na předběžné rezervaci vstoupí v platnost.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Definice přidělení ve službě viditelnosti zásob

### <a name="allocation-virtual-pool"></a>Alokační virtuální fond

Přestože funkce přidělení ve službě Viditelnost zásob nevyčleňuje množství fyzické zásoby, odkazuje na dostupné množství fyzické zásoby, aby bylo možné definovat její počáteční množství *k dispozici pro přidělení* virtuálního fondu. Přidělení zásob ve Viditelnosti zásob je předběžné přidělení. Provádí se před skutečnými prodejními transakcemi a nezávisí na prodejních objednávkách. Můžete například přidělit zásoby svým nejdůležitějším prodejním kanálům nebo velkým maloobchodníkům dříve, než koncoví zákazníci navštíví prodejní kanál nebo maloobchod, aby si je koupili.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Rozdíl mezi přidělením zásob a předběžnou rezervací

[Předběžné rezervace](inventory-visibility-reservations.md) jsou obvykle spojeny se skutečnými prodejními transakcemi (řádky prodejních objednávek). Přidělení i předběžnou rezervaci lze použít nezávisle, ale pokud je chcete používat společně, je třeba provést předběžnou rezervaci až po přidělení. Doporučujeme provést nejprve přidělení zásob a poté předběžnou rezervaci proti přiděleným množstvím, abyste dosáhli spotřeby proti přidělení téměř v reálném čase. Více informací viz část [Spotřeba jako předběžná rezervace](#consume-to-soft-reserved).

Funkce přidělení zásob umožňuje plánovačům prodeje nebo manažerům klíčových zákazníků spravovat a předem přidělovat důležité zásoby napříč skupinami přidělení (jako jsou kanály, regiony a skupiny zákazníků). Podporuje také sledování v reálném čase, úpravu a analýzu spotřeby oproti přiděleným množstvím, aby bylo zajištěno, že doplnění nebo přerozdělení může být provedeno včas. Tato schopnost mít přehled o přidělení, spotřebě a bilanci přidělení je zvláště důležitá při akcích rychlého prodeje nebo propagačních akcích.

## <a name="terminology"></a>Terminologie

Při výkladu přidělování zásob budeme používat následující pojmy a koncepty:

- **Skupina přidělení** – Skupina, která vlastní přidělení, jako je prodejní kanál, skupina zákazníků nebo typ objednávky.
- **Hodnota skupiny přidělení** – Hodnota každé skupiny přidělení. Například *web* nebo *prodejna* může být hodnotou skupiny přidělení prodejních kanálů, zatímco *VIP* nebo *normální* může být hodnota skupiny přidělení zákazníků.
- **Hierarchie přidělení** – Prostředek ke kombinování skupin přidělení hierarchickým způsobem. Můžete například definovat *kanál* jako úroveň hierarchie 1, *oblast* jako úroveň 2 a *skupinu zákazníků* jako úroveň 3. Během přidělování zásob musíte při zadávání hodnoty skupiny přidělení postupovat podle pořadí hierarchie přidělování. Můžete například přidělit 200 červených kol kanálu *Web*, oblasti *Londýn* a skupině zákazníků *VIP*.
- **K dispozici pro přidělení** – *Virtuální společný fond*, který udává množství, které je k dispozici pro další přidělení. Je to vypočítaná míra, kterou můžete volně definovat pomocí vlastního vzorce. Pokud také používáte funkci předběžných rezervací, doporučujeme použít stejný vzorec pro výpočet dostupných přidělení a dostupných rezervací.
- **Přiděleno** – Fyzická míra, která ukazuje přidělenou kvótu, kterou mohou spotřebovat skupiny přidělení. Odečítá se zároveň s připočtením spotřebovaného množství.
- **Spotřebováno** – Fyzická míra, která označuje množství, která byla spotřebována oproti původně přidělenému množství. Jak se k této fyzické míře přičítají další čísla, automaticky se snižuje přidělovaná fyzická míra.

Následující obrázek znázorňuje příklad pracovního postupu pro přidělování zásob.

![Pracovní postup přidělení Viditelnosti zásob.](media/inventory-visibility-allocation-flow.png "Pracovní postup přidělení Viditelnosti zásob.")

Následující obrázek ukazuje hierarchii přidělení a skupiny přidělení. Zde zobrazený *virtuální společný fond* je množství dostupné k přidělení.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Hierarchie přidělení ve Viditelnosti zásob" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

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

Proces konfigurace funkce přidělení je složen ze tří kroků:

- Aktivujte funkci v aplikaci Viditelnost zásob tím, že přejdete na **Konfigurace \> Správa a nastavení funkcí \> Přidělení**.
- Nastavte [zdroj dat](inventory-visibility-configuration.md#data-source-configuration) a jeho [míry](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Nastavte název a hierarchii skupiny přidělení.

### <a name="predefined-data-source"></a>Předdefinovaný zdroj dat

Když povolíte funkci přidělení a zavoláte rozhraní API pro aktualizaci konfigurace, Viditelnost zásob vytvoří jeden předdefinovaný zdroj dat a několik počátečních opatření.

Zdroj dat se jmenuje `@iv`. Zahrnuje sadu výchozích fyzických měr. Můžete je zobrazit v aplikaci Viditelnost zásob na **Konfigurace \> Zdroj dat**. Měli byste vidět **Datasource - @IV**. Rozbalte zdroj dat `@iv` pro zobrazení seznamu počátečních fyzických měr:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Vyberte kartu **Vypočítané míry** a zobrazíte počáteční vypočítanou míru, která je pojmenována `@iv.@available_to_allocate`:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Přidejte další fyzické míry do vypočítané míry K dispozici pro přidělení

Chcete-li použít přidělení, musíte správně nastavit vzorec pro vypočítanou míru K dispozici pro přidělení (`@iv.@available_to_allocate`). Například máte zdroj dat `fno` a míru `onordered`, zdroj dat `pos` a míru `inbound` a chcete provést přidělení zásob na skladě ve výši součtu `fno.onordered` a `pos.inbound`. V tomto případě by `@iv.@available_to_allocate` měla ve vzorci obsahovat `pos.inbound` a `fno.onordered`. Následuje příklad:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Zdroj dat `@iv` je předdefinovaný zdroj dat a fyzické míry definované v `@iv` s předponou `@` jsou předem definovaná opatření. Tyto míry jsou předdefinovanou konfigurací pro funkci alokace, takže je neměňte ani neodstraňujte, protože při používání funkce alokace pravděpodobně narazíte na neočekávané chyby.
>
> K předdefinované vypočítané míře `@iv.@available_to_allocate` můžete přidat nové fyzické míry, ale nesmíte změnit její název.

### <a name="manage-allocation-groups"></a>Správa skupin přidělení

Nastavit se dá maximálně osm názvů skupin přidělení. Skupiny mají hierarchii. K zobrazení a aktualizaci skupin přidělení postupujte následovně.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace** a poté na kartě **Přidělení** vyberte **Upravit konfiguraci**. Ve výchozím nastavení existuje hierarchie přidělení, která má čtyři vrstvy: `Channel` (vrchní vrstva), `customerGroup` (druhá vrstva), `Region` (třetí vrstva) a `OrderType` (čtvrtá vrstva).
1. Existující skupinu přidělení můžete odstranit výběrem **X** vedle ní. Můžete také přidat nové skupiny přidělení do hierarchie zadáním názvu každé nové skupiny přímo do pole.

    > [!IMPORTANT]
    > Buďte opatrní, když odstraňujete nebo měníte mapování hierarchie přidělení. Návod viz [Tipy pro použití přidělení](#allocation-tips).

1. Po dokončení konfigurace skupiny přidělení a nastavení hierarchie uložte změny a poté vyberte **Aktualizovat konfiguraci** v pravém horním rohu. Hodnoty nakonfigurovaných skupin přidělení budou aktualizovány, když vytvoříte přidělení pomocí uživatelského rozhraní nebo API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate). Podrobnosti o obou přístupech jsou uvedeny dále v tomto článku.

Pokud použijete čtyři názvy skupin a nastavíte je na \[`channel`, `customerGroup`, `region`, `orderType`\], budou tato jména platná pro požadavky související s přidělením, když zavoláte rozhraní API pro aktualizaci konfigurace.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>Tipy pro používání přidělení

- U každého produktu by funkce přidělení měla používat stejnou *úroveň dimenze* podle hierarchie indexu produktu, kterou nastavíte v [konfiguraci hierarchie indexu produktů](inventory-visibility-configuration.md#index-configuration). Předpokládejme například, že vaše hierarchie indexu je \[`Site`, `Location`, `Color`, `Size`\]. Pokud přidělíte nějaké množství pro jeden produkt na úrovni dimenze \[`Site`, `Location`, `Color`\], až budete příště chtít přidělit tento produkt, měli byste také přidělit na stejné úrovni, \[`Site`, `Location`, `Color`\]. Pokud použijete úroveň \[`Site`, `Location`, `Color`, `Size`\] nebo \[`Site`, `Location`\], data budou nekonzistentní.
- **Úprava skupin přidělení a hierarchie:** Pokud již v systému existují data přidělení, odstranění existujících skupin přidělení nebo posun v hierarchii skupin přidělení poškodí existující mapování mezi skupinami přidělení. Před aktualizací nové konfigurace proto nezapomeňte ručně vyčistit všechna stará data. Protože však přidání nových skupin přidělení do nejnižší hierarchie neovlivní existující mapování, nebudete muset data čistit.
- Přidělení bude úspěšné pouze v případě, že produkt má kladné množství `available_to_allocate`.
- Chcete-li přidělit produkty ze skupiny vysoké *úrovně přidělení* do podskupiny, použijte rozhraní API `Reallocate`. Máte například hierarchii skupiny alokace \[`channel`, `customerGroup`, `region`, `orderType`\] a chcete alokovat nějaký produkt ze skupiny alokace \[Online, VIP\] do podskupiny alokace \[Online, VIP, EU\], použijte rozhraní API `Reallocate` pro přesun množství. Pokud použijete rozhraní API `Allocate`, přidělí množství z virtuálního společného fondu.
- Chcete-li zobrazit celkovou dostupnost produktu (společný fond), použijte rozhraní API [dotazu na zásoby na skladě](inventory-visibility-api.md#query-on-hand) pro vyžádání množství zásob, které je *k dispozici k přidělení*. Na základě těchto informací pak můžete činit rozhodnutí o přidělení.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>Použití rozhraní API pro přidělování

V současné době je otevřeno pět rozhraní API pro přidělování:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – Toto rozhraní API se používá k vytvoření počátečního přidělení.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – Toto rozhraní API se používá k vrácení nebo odebrání přidělených množství.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – Toto rozhraní API se používá k přesunutí přiděleného množství z existujícího přidělení do jiných skupin přidělení.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – Toto rozhraní API se používá odečtení (použití) přiděleného množství.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – Toto rozhraní API se používá ke kontrole existujících záznamů přidělení proti skupinám přidělení a hierarchii.

### <a name="allocate"></a>Allocate

Volání `Allocate` API použijte, když chcete přidělit produkt, který má konkrétní dimenze. Zde je schéma pro tělo požadavku.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
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

### <a name="unallocate"></a>Unallocate

Volání `Unallocate` API použijte ke zrušení operace `Allocate`. Záporné množství není v operaci `Allocate` povoleno. Tělo volání `Unallocate` je shodné s tělem volání `Allocate`.

### <a name="reallocate"></a>Reallocate

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
    "groups": {
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
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume"></a>Consume

Volání `Consume` API použijte k zaúčtování množství spotřeby proti přidělení. Toto rozhraní API můžete například použít k přesunutí přiděleného množství na některé reálné míry. Zde je schéma pro tělo požadavku.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Spotřeba jako předběžná rezervace

Volání `Consume` API může také spotřebovat přidělené množství jako předběžnou rezervaci. V tomto případě volání `Consume` sníží přidělené množství a poté pro toto množství provede předběžnou rezervaci. Chcete-li použít tento přístup, musíte také používat funkci [předběžné rezervace](inventory-visibility-reservations.md) Viditelnosti zásob.

Například jste nastavili fyzickou míru předběžné rezervace na `iv.softreserved`. Pro vypočítanou míru K dispozici pro rezervaci se používá následující vzorec:

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
    "groups": {
        "channel": "Web",
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

### <a name="query"></a>Query

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
        "channel": "Web",
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
        "channel": "Web",
        "customerGroup": "VIP",
        "region&quot;: &quot;US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Použití uživatelského rozhraní přidělení

Přidělení můžete ručně spravovat prostřednictvím uživatelského rozhraní otevřením aplikace Viditelnost zásob a přechodem na **Provozní viditelnost \> Přidělení**. Odtud můžete provádět libovolnou z akcí, které jsou popsány v následujících podsekcích.

### <a name="create-an-allocation"></a>Vytvoření přidělení

Chcete-li vytvořit přidělení ze stránky **Přidělení** v aplikaci Viditelnost inventáře, postupujte následovně.

1. Vyberte **Přidělit**.
1. Nastavte hodnoty základních polí, dimenzí a cílových skupin přidělení. (Když vyberete zdroj shromažďování dat v části **Dimenze**, nejprve pomocí rozevíracího seznamu zadejte dimenze (např. `siteId`). Poté do zobrazených polí zadejte hodnoty dimenzí.)
1. Vyberte **odeslat**.

### <a name="consume-an-allocation"></a>Spotřeba přidělení

Vyberte **Spotřebovat** pro spotřebování přidělení. Chcete-li zajistit, že spotřebováváte v rámci správné skupiny přidělení a hierarchie, zadejte stejné sady podrobností o organizaci a dimenzích, které jste zadali při vytváření přidělení.

### <a name="reallocate-an-allocation"></a>Změna přidělení

Vyberte **Změnit přidělení** pro přesun existujícího přidělené množství z jedné sady skupin přidělení do jiné.

### <a name="query-existing-allocations"></a>Dotaz na existující přidělení

Vyberte **Dotaz** a poté zadejte hodnoty produktu, organizace, dimenze a skupiny přidělení, abyste získali výsledky dotazu existujících přidělení.
