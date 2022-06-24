---
title: Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit
description: Tento článek popisuje, jak naplánovat budoucí změny ve skladu a vypočítat množství, které lze slíbit (ATP).
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 4a0edeedfe42b43ef36c8ca091b01eef815f3632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856186"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nastavit funkci *Plán změn ve skladu* pro plánování budoucích změn ve skladu a výpočet dostupných množství, které lze slíbit (ATP). ATP (Lze slíbit) je množství položky, které je k dispozici a může být odběrateli přislíbena v příštím období. Použití tohoto výpočtu může výrazně zvýšit vaši schopnost plnění objednávky.

Mnoha výrobcům, maloobchodníkům či prodejcům nestačí jen vědět, co mají aktuálně skladem. Musejí mít úplný přehled o budoucí dostupnosti. Tato budoucí dostupnost by měla zohledňovat budoucí nabídku, budoucí poptávku a ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Povolení a nastavení funkcí

Předtím, než začnete používat ATP, musíte nastavit jedno nebo více vypočítaných měr pro výpočet množství ATP. Musíte také funkci zapnout a nakonfigurovat její nastavení v Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Nastavení vypočítaných měr pro množství ATP

*Vypočítaná míra ATP* je předem definovaná vypočítaná míra, která se obvykle používá k nalezení aktuálně dostupného množství. *Dodávané množství* je součet množství těch fyzikálních měr, které mají typ modifikátoru *sčítání* a *poptávkové množství* je součet množství těch fyzikálních měr, které mají typ modifikátoru *odčítání*.

Pro výpočet více množství ATP můžete přidat více vypočtených měr. Celkový počet jedinečných fyzických měr ve všech vypočtených mírách ATP by však měl být menší než devět.

> [!IMPORTANT]
> Vypočítaná míra je složením fyzických měr. Její vzorec může zahrnovat pouze fyzické míry bez duplicit, nikoli vypočítané míry.

Můžete vytvářet například následující vypočítanou míru:

**Dostupné na skladě** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

Součet (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) představuje nabídku a součet (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) představuje poptávku. Proto lze vypočítanou míru chápat takto:

**Dostupné na skladě** = *Nabídka* – *Poptávka*

Pro výpočet množství ATP **Fyzicky na skladě** můžete přidat další vypočítanou míru.

**Fyzicky na skladě** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

K těmto dvěma vypočteným měrám ATP existuje osm různých fyzických měr: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* a *Outbound*.

Další informace o vypočítaných mírách naleznete v tématu [Vypočítané míry](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Zapnutí funkce Plán změn ve skladu a konfigurace nastavení ATP

Podle následujících kroků zapněte funkci *Plán změn ve skladu* v Power Apps a nakonfigurujte nastavení ATP.

1. Přihlaste se do Power Apps a otevřete Viditelnost zásob.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Správa funkcí** zapněte funkci *OnhandChangeSchedule*.
1. Vyberte kartu **Nastavení ATP**.
1. Když zašlete dotaz do aplikace Viditelnost zásob, vrátí tato výsledek, který zahrnuje každou vypočítanou míru ATP, kterou sem přidáte. Vyberte položku **Přidat** a přidejte novou vypočítanou míru pro ATP.
1. Nastavte následující pole:

    - **Zdroj dat** – Vyberte zdroj dat, který je spojen s vypočítanou mírou.
    - **Vypočítaná míra** – Vyberte vypočítanou míru, která je spojena s vybraným zdrojem dat a kterou chcete použít k nalezení aktuálně dostupného množství.
    - **Období plánu** – Zadejte počet dní, po které mohou uživatelé prohlížet a odesílat plánované změny ve skladu, když je použita vybraná vypočítaná míra. Uživatelé, kteří požádají o skladové informace, získají množství na skladě, plánované změny na skladě a ATP pro každý den v tomto období, počínaje aktuálním datem. Vyberte celé číslo mezi 1 a 7.

    > [!IMPORTANT]
    > Plánované období zahrnuje aktuální datum. Uživatelé tedy mohou naplánovat změny na skladu, které se mají provést kdykoli od aktuálního data (den, kdy je změna odeslána) až po (plánované období – 1) dnů v budoucnosti.

1. Zvolte možnost **Uložit**.
1. Opakujte kroky 5 až 7, dokud nepřidáte všechny vypočítané míry, které chcete vyžadovat u výpočtu ATP.
1. Po dokončení konfigurace všech požadovaných nastavení vyberte příkaz **Aktualizovat konfiguraci**.

Další informace naleznete v tématu [Dokončení a aktualizace konfigurace](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Jak funguje plán změn na skladu a výpočty ATP

*Plán změn ve skladu* stanoví očekávaná data a množství plánovaných změn ve skladu. Do Viditelnosti zásob můžete odeslat plán změn za předpokladu, že data patří do období definovaného v nastavení **Období plánu** (viz část [Povolení a nastavení funkcí](#setup)). Uživatelé, kteří požádají o skladové informace, získají množství na skladě, plánované změny na skladě a ATP pro každý den v tomto období.

Naplánované změny jsou zpočátku nepotvrzené, a proto neovlivňují vaše aktuální množství v systému. Chcete-li změny potvrdit, musíte odeslat *událost změny ve skladu*, která aktualizuje aktuální dostupné množství na skladě. Poté musíte vrátit naplánovanou změnu odesláním plánu změn ve skladu pro odpovídající záporné množství.

Například zadáte objednávku na 10 kol a očekáváte, že dorazí zítra. Proto odešlete plán změn, který má příchozí množství 10 a je datován na zítra. Když objednávka druhý den dorazí, přidáte kola do svého fyzického skladu. Poté musíte potvrdit změnu ve vašem systému, abyste aktualizovali skutečné množství na skladě. Chcete-li potvrdit změnu, odešlete událost změny ve skladu, která má příchozí množství 10. Poté musíte vrátit naplánovanou změnu odesláním plánu změn ve skladu, která má příchozí množství -10.

Když zašlete dotaz do aplikace Viditelnost zásob na množství na skladě a ATP, vrátí následující informace pro každý den v období plánu:

- **Datum** – Datum, na který se výsledek vztahuje. Časové pásmo je koordinovaný světový čas (UTC).
- **Množství na skladě** – Skutečné množství na skladě pro zadané datum. Tento výpočet se provádí podle vypočítané míry ATP, která je konfigurována pro Viditelnost zásob.
- **Plánovaná dodávka** – Součet všech plánovaných příchozích množství, která nebyla fyzicky k dispozici pro okamžitou spotřebu nebo odeslání k určenému datu.
- **Plánovaná poptávka** – Součet všech plánovaných odchozích množství, která nebyla spotřebována nebo odeslána k určenému datu.
- **Množství ATP** – Minimální předpokládané množství na skladě, které je k dispozici od zadaného data do konce období plánu. Toto množství zahrnuje všechny plánované úpravy množství. Je to maximální množství, které lze k aktuálnímu datu slíbit k dodání nebo spotřebě v daný den.

Pokud je například aktuální datum 1. února 2022 a plánovací období je 7, uživatelé mohou odesílat plánované změny ve skladu, které se očekávají v období od 1. února do 7. února 2022. V tomto případě se množství ATP například pro 3. února vypočítá na základě množství na skladě pro daný den a plánovaných množství od 3. února do 7. února.

## <a name="example"></a>Příklad

Následující příklad ukazuje, jak řada změn naplánovaného množství ovlivňuje množství na skladě a množství ATP, které hlásí Viditelnost zásob. Také ukazuje, jak potvrdit naplánovanou změnu, jak potvrzená změna plánu ovlivní výsledky a co se může stát, pokud naplánovanou změnu nepotvrdíte.

Výsledky v tomto příkladu ukazují hodnotu *očekávané množství na skladě*. Tato hodnota zahrnuje všechny naplánované aktualizace pro ilustrační účely, ale ve skutečnosti není při dotazu do aplikace Viditelnost zásob hlášena.

1. Následující nastavení jsou pro váš systém konfigurována na stránce **Nastavení ATP** v Power Apps:

    - **Vypočítaná míra ATP** – Máte vypočítanou míru, která je pojmenována *Na skladě*. Počítá se jako *Na skladě = nabídka – poptávka*. Zde vyberete míru.
    - **Období plánu** – Vyberte *7*.

1. Platí také následující podmínky:

    - Aktuální datum je 1. února 2022.
    - Aktuální množství na skladě je 20.

1. Pro aktuální datum (1. února 2022) odešlete do Viditelnosti zásob plánované množství poptávky 3. Předpokládané množství na skladě je proto 17. Následující tabulka zobrazuje výsledek.

    | Datum | Na skladě | Plánovaná dodávka | Plánovaná poptávka | Předpokládané množství na skladě | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. 2. 2022 | 20 | | 3 | 17 | 17 |
    | 2. 2. 2022 | 20 | | | 17 | 17 |
    | 3. 2. 2022 | 20 | | | 17 | 17 |
    | 4. 2. 2022 | 20 | | | 17 | 17 |
    | 5. 2. 2022 | 20 | | | 17 | 17 |
    | 6. 2. 2022 | 20 | | | 17 | 17 |
    | 7. 2. 2022 | 20 | | | 17 | 17 |

1. K aktuálnímu datu (1. února 2022) odešlete plánované množství dodávky 10 na 3. února 2022. Následující tabulka zobrazuje výsledek.

    | Datum | Na skladě | Plánovaná dodávka | Plánovaná poptávka | Předpokládané množství na skladě | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. 2. 2022 | 20 | | 3 | 17 | 17 |
    | 2. 2. 2022 | 20 | | | 17 | 17 |
    | 3. 2. 2022 | 20 | 10 | | 27 | 27 |
    | 4. 2. 2022 | 20 | | | 27 | 27 |
    | 5. 2. 2022 | 20 | | | 27 | 27 |
    | 6. 2. 2022 | 20 | | | 27 | 27 |
    | 7. 2. 2022 | 20 | | | 27 | 27 |

1. K aktuálnímu datu (1. února 2022) odešlete následující plánované změny množství:

    - Množství poptávky 15 na 4. února 2022
    - Množství dodávky 1 na 5. února 2022
    - Množství dodávky 3 na 6. února 2022

    Následující tabulka zobrazuje výsledek.

    | Datum | Na skladě | Plánovaná dodávka | Plánovaná poptávka | Předpokládané množství na skladě | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. 2. 2022 | 20 | | 3 | 17 | 12 |
    | 2. 2. 2022 | 20 | | | 17 | 12 |
    | 3. 2. 2022 | 20 | 10 | | 27 | 12 |
    | 4. 2. 2022 | 20 | | 15 | 12 | 12 |
    | 5. 2. 2022 | 20 | 1 | | 13 | 13 |
    | 6. 2. 2022 | 20 | 3 | | 16 | 16 |
    | 7. 2. 2022 | 20 | | | 16 | 16 |

1. K aktuálnímu datu (1. února 2022) expedujete plánované množství poptávky ve výši 3: Proto musíte tuto změnu potvrdit, aby se promítla do vašeho skutečného množství na skladě. Chcete-li potvrdit změnu, odešlete událost změny ve skladu, která má odchozí množství 3. Poté musíte vrátit naplánovanou změnu odesláním plánu změn ve skladu, která má odchozí množství -3. Následující tabulka zobrazuje výsledek.

    | Datum | Na skladě | Plánovaná dodávka | Plánovaná poptávka | Předpokládané množství na skladě | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. 2. 2022 | 17 | | 0 | 17 | 12 |
    | 2. 2. 2022 | 17 | | | 17 | 12 |
    | 3. 2. 2022 | 17 | 10 | | 27 | 12 |
    | 4. 2. 2022 | 17 | | 15 | 12 | 12 |
    | 5. 2. 2022 | 17 | 1 | | 13 | 13 |
    | 6. 2. 2022 | 17 | 3 | | 16 | 16 |
    | 7. 2. 2022 | 17 | | | 16 | 16 |

1. Následující den (2. února 2022) se plánovací období posune o jeden den dopředu. Následující tabulka zobrazuje výsledek.

    | Datum | Na skladě | Plánovaná dodávka | Plánovaná poptávka | Předpokládané množství na skladě | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2. 2. 2022 | 17 | | | 17 | 12 |
    | 3. 2. 2022 | 17 | 10 | | 27 | 12 |
    | 4. 2. 2022 | 17 | | 15 | 12 | 12 |
    | 5. 2. 2022 | 17 | 1 | | 13 | 13 |
    | 6. 2. 2022 | 17 | 3 | | 16 | 16 |
    | 7. 2. 2022 | 17 | | | 16 | 16 |
    | 8. 2. 2022 | 17 | | | 16 | 16 |

1. O dva dny později (4. února 2022) však množství dodávky 10 kusů, které bylo naplánováno na 3. února, stále nedorazilo. Následující tabulka zobrazuje výsledek.

    | Datum | Na skladě | Plánovaná dodávka | Plánovaná poptávka | Předpokládané množství na skladě | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 4. 2. 2022 | 17 | | 15 | 2 | 2 |
    | 5. 2. 2022 | 17 | 1 | | 3 | 3 |
    | 6. 2. 2022 | 17 | 3 | | 6 | 6 |
    | 7. 2. 2022 | 17 | | | 6 | 6 |
    | 8. 2. 2022 | 17 | | | 6 | 6 |
    | 9. 2. 2022 | 17 | | | 6 | 6 |
    | 10. 2. 2022 | 17 | | | 6 | 6 |

    Jak vidíte, plánované (ale nepotvrzené) změny na skladě neovlivňují skutečné množství na skladě.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Odeslání plánů změn, událostí změn a dotazů ATP prostřednictvím rozhraní API

Následující adresy URL aplikačního programovacího rozhraní (API) můžete použít k odeslání plánů změn, událostí změn a dotazů.

| Cesta | Metoda | Popis |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Vytvoří jednu plánovanou změnu množství na skladě. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Vytvoří více plánovaných změn množství na skladě. |
| `/api/environment/{environmentId}/onhand` | `POST` | Vytvoří jednu událost změny množství na skladě. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Vytvoří více změnových událostí. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Dotaz používající metodu `POST`. |
| `/api/environment/{environmentId}/onhand` | `GET` | Dotaz používající metodu `GET`. |

Další informace viz [Veřejná rozhraní API Viditelnosti zásob](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Vytvoření jednoho plánu změny množství na skladě

Plán změny množství na skladě se provádí odesláním požadavku `POST` na příslušnou adresu URL služby Viditelnost zásob (viz sekce [Odeslání plánů změn, událostí změn a dotazů ATP prostřednictvím rozhraní API](#api-urls)). Můžete také odesílat hromadné požadavky.

Plán změny množství na skladě musí být vytvořen jen pokud je plánované datum mezi aktuálním datem a koncem aktuálního plánovacího období. Formát data a času by měl být *rok-měsíc-den* (například **2022-02-01**). Formát času musí být přesný pouze na den.

Toto API vytvoří jeden plán změny množství na skladě.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Následující příklad ukazuje ukázkový obsah těla bez `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Vytvoření více plánů množství na skladě

Toto API může vytvářet více záznamů současně. Jediné rozdíly mezi tímto API a API pro jednu událost jsou hodnoty `Path` a `Body`. U tohoto API obsahuje `Body` pole záznamů. Maximální počet záznamů je 512. Rozhraní API pro hromadné plánování změn množství na skladě proto může podporovat až 512 naplánovaných změn najednou.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

Následující příklad ukazuje ukázkový obsah těla.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Vytvoření událostí změn ve skladu

Události změn množství na skladě se provádějí odesláním požadavku `POST` na příslušnou adresu URL služby Viditelnost zásob (viz sekce [Odeslání plánů změn, událostí změn a dotazů ATP prostřednictvím rozhraní API](#api-urls)). Můžete také odesílat hromadné požadavky.

> [!NOTE]
> Události změny na skladě nejsou jedinečnou součástí funkce ATP, ale jsou součástí standardního API aplikace Viditelnost skladu. Tento příklad byl začleněn, protože události jsou při práci s ATP relevantní. Události změny na skladě se podobají rezervacím změn na skladě, ale zprávy událostí musejí být odeslány na jinou adresu URL API a události používají v těle zprávy parametr `quantities` namísto `quantityByDate`. Další informace o událostech změny na skladě a dalších funkcích rozhraní API aplikace Viditelnost skladu naleznete v části [Veřejná rozhraní API aplikace Viditelnost skladu](inventory-visibility-api.md#create-one-onhand-change-event).

Následující příklad ukazuje tělo požadavku, který obsahuje jednu událost změny na skladě.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Dotaz na plánované změny na skladě a výsledky ATP

Dotazy na plánované změny na skladě a výsledky ATP odesílejte požadavkem `POST` nebo `GET` směrovaným na příslušnou adresu URL API (viz sekce [Odeslání plánů změn, událostí změn a dotazů ATP prostřednictvím rozhraní API](#api-urls)).

V požadavku nastavte parametr `QueryATP` na *true*, pokud se chcete dotazovat na plánované změny a výsledky ATP.

- Pokud požadavek odesíláte metodou `GET`, nastavte tento parametr v adrese URL.
- Pokud požadavek odesíláte metodou `POST`, nastavte tento parametr v těle požadavku.

> [!NOTE]
> Bez ohledu na to, zda je v těle požadavku parametr `returnNegative` nastaven na *true* nebo *false*, bude výsledek obsahovat záporné hodnoty, když se dotazujete na plánované změny na skladě a výsledky ATP. Tyto záporné hodnoty budou zahrnuty, protože pokud jsou plánovány pouze objednávky poptávky, nebo pokud jsou dodávaná množství menší než poptávaná množství, budou plánované změny na skladě záporné. Pokud by záporné hodnoty nebyly zahrnuty, výsledky by byly matoucí. Další informace o této možnosti a o tom, jak funguje u jiných typů dotazů, naleznete v části [Veřejná rozhraní API aplikace Viditelnost skladu](inventory-visibility-api.md#query-with-post-method).

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Následující příklad ukazuje, jak vytvořit tělo požadavku, které lze odeslat do aplikace Viditelnosti skladu metodou `POST`.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>Příklad metody GET

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Následující příklad ukazuje, jak vytvořit adresu URL požadavku jako požadavek `GET`.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Výsledek tohoto požadavku `GET` je přesně stejný jako výsledek požadavku `POST` v předchozím příkladu.

### <a name="query-result-example"></a>Příklad výsledku dotazu

Oba předchozí příklady dotazů mohou přinést následující odpověď. V tomto příkladu je systém konfigurován takto:

- **Vypočítaná míra ATP:** *iv.onhand = pos.inbound – pos.outbound*
- **Období plánu:** *7*

Následuje příklad těla požadavku.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
