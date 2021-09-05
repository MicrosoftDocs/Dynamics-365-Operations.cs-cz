---
title: Konfigurace doplňku Viditelnost zásob
description: Toto téma popisuje, jak konfigurovat doplněk Viditelnost zásob.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345026"
---
# <a name="inventory-visibility-configuration"></a>Konfigurace doplňku Viditelnost zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Toto téma popisuje, jak konfigurovat doplněk Viditelnost zásob.

## <a name="introduction"></a><a name="introduction"></a>Úvod

Než začnete pracovat s Viditelností zásob, musíte dokončit následující konfiguraci, jak je popsáno v tomto tématu:

- [Konfigurace zdroje dat](#data-source-configuration)
- [Konfigurace oddílu](#partition-configuration)
- [Konfigurace hierarchie indexu produktů](#index-configuration)
- [Konfigurace rezervace (volitelná)](#reservation-configuration)
- [Ukázka výchozí konfigurace](#default-configuration-sample)

> [!NOTE]
> Konfigurace doplňku Viditelnost zásob můžete prohlížet a upravovat v prostředí [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). Po dokončení konfigurace vyberte v aplikaci příkaz **Aktualizovat konfiguraci**.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Konfigurace zdroje dat

Zdroj dat představuje systém, ze kterého vaše data pocházejí. Mezi příklady patří `fno` (což znamená „aplikace Dynamics 365 Finance and Operations“) a `pos` (což znamená „prodejní místo“).

Konfigurace zdroje dat obsahuje následující části:

- Dimenze (mapování dimenzí)
- Fyzická míra
- Vypočtená míra

> [!NOTE]
> Zdroj dat `fno` je vyhrazen pro Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimenze (mapování dimenzí)

Účelem konfigurace dimenze je standardizovat integraci více systémů pro odesílání událostí a dotazů na základě kombinací dimenzí.

Viditelnost zásob podporuje následující obecné základní dimenze.

| Typ dimenze | Základní dimenze |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Sledování | `BatchId` |
| Sledování | `SerialId` |
| Skladové místo | `LocationId` |
| Skladové místo | `SiteId` |
| Stav skladu | `StatusId` |
| Specifické pro sklad | `WMSLocationId` |
| Specifické pro sklad | `WMSPalletId` |
| Specifické pro sklad | `LicensePlateId` |
| Další | `VersionId` |
| Zásoby (vlastní) | `InventDimension1` až `InventDimension12` |
| Linka | `ExtendedDimension1` až `ExtendedDimension8` |

> [!NOTE]
> Typy dimenzí uvedené v předchozí tabulce slouží pouze pro informaci. Ve Viditelnosti zásob je nemusíte definovat.
>
> Dimenze inventáře (vlastní) mohou být vyhrazeny pro Supply Chain Management. V takovém případě můžete místo toho použít rozšířené dimenze.

Externí systémy mají přístup k Viditelnosti zásob prostřednictvím svých RESTful rozhraní API. Pro integraci vám Viditelnost zásob umožňuje konfigurovat _externí zdroj dat_ a mapování z _externích dimenzí_ do _základních dimenzí_. Následuje příklad tabulky mapování dimenzí.

| Externí dimenze | Základní dimenze |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Po konfiguraci mapování dimenzí můžete odeslat externí dimenze přímo do Viditelnosti zásob. Viditelnost zásob pak automaticky převede externí dimenze na základní.

### <a name="physical-measures"></a>Fyzické míry

Fyzické míry mění množství a odrážejí stav zásob. Na základě vašich požadavků můžete definovat své vlastní fyzické míry.

Viditelnost zásob poskytuje seznam výchozích fyzických měr, které jsou propojeny s aplikací Supply Chain Management (zdroj dat `fno`). Následující tabulka uvádí příklad fyzických měr.

| Název fyzické míry | popis |
|---|---|
| `NotSpecified` | Neurčeno |
| `Arrived` | Doručeno |
| `AvailOrdered` | Dostupné seřazené |
| `AvailPhysical` | Fyzicky k dispozici |
| `Deducted` | Odečteno |
| `OnOrder` | OnOrder |
| `Ordered` | Objednáno |
| `PhysicalInvent` | Fyzické zásoby |
| `Picked` | Vyzvednuto |
| `PostedQty` | Zaúčtované mn. |
| `QuotationIssue` | Vystavení nabídky |
| `QuotationReceipt` | Nabídky při příjmu |
| `Received` | Přijato |
| `Registered` | Registrováno |
| `ReservOrdered` | Rezervováno k objednání |
| `ReservPhysical` | Fyzicky rezervováno |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Vypočtené míry

Vypočítané míry poskytují přizpůsobený výpočetní vzorec, který se skládá z kombinace fyzických měr. Tato funkce vám umožňuje definovat sadu fyzických měrných systémů, které budou přidány, anebo sadu fyzických měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.

Například máte následující výsledek dotazu:

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Poté nakonfigurujete vypočítanou míru, která je pojmenována `MyCustomAvailableforReservation`, jak ukazuje následující tabulka. Tato vypočítaná míra bude spotřebována systémem spotřeby.

| Systém spotřeby | Vypočtená míra | Zdroj dat | Fyzická míra | Typ výpočtu |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Když se použije tento výpočetní vzorec, výsledek nového dotazu bude zahrnovat přizpůsobenou míru.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Výstup `MyCustomAvailableforReservation`, založený na nastavení výpočtu ve vlastních měrných systémech, je 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Konfigurace oddílu

Konfigurace oddílu se skládá z kombinace základních dimenzí. Definuje vzor distribuce dat. Datové operace ve stejném oddílu podporují vysoký výkon a nestojí příliš mnoho. Dobré vzory oddílů proto mohou přinést značné výhody.

Viditelnost zásob poskytuje následující výchozí konfiguraci oddílu.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Výchozí konfigurace oddílu je pouze orientační. Ve Viditelnosti zásob ji nemusíte definovat. Aktualizace konfigurace oddílu není aktuálně podporována.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Konfigurace hierarchie indexu produktů

Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni. Místo toho můžete také chtít zobrazit výsledky, které jsou agregovány na základě dimenzí skladu.

Viditelnost zásob je dostatečně pružná, protože vám umožňuje nastavit _indexy_. Tyto indexy jsou založeny na dimenzi nebo kombinaci dimenzí. Index se skládá z *čísla sady*, *dimenze* a *hierarchie*, jak je definováno v následující tabulce.

| Jméno | popis |
|---|---|
| Číslo sady | Dimenze, které patří do stejné sady (indexu), budou seskupeny a bude jim přiděleno stejné číslo sady. |
| Dimenze | Základní dimenze, na kterých je výsledek dotazu agregován. |
| Hierarchie | Hierarchie se používá k definování podporovaných kombinací dimenzí, které lze dotazovat. Například nastavíte sadu dimenzí, která má hierarchickou posloupnost `(ColorId, SizeId, StyleId)`. V tomto případě systém podporuje dotazy na čtyři kombinace dimenzí. První kombinace je prázdná, druhá je `(ColorId)`, třetí je `(ColorId, SizeId)` a čtvrtá je `(ColorId, SizeId, StyleId)`. Ostatní kombinace nejsou podporovány. Další informace naleznete v následujícím příkladu. |

### <a name="example"></a>Příklad

Tato část poskytuje příklad, který ukazuje, jak hierarchie funguje.

Ve svém skladu máte následující položky.

| Zboží | ColorId | SizeId | StyleId | Množství |
|---|---|---|---|---|
| Tričko | Černé | Malé | Široké | 1 |
| Tričko | Černé | Malé | Normální | 2 |
| Tričko | Černé | Velké | Široké | 3 |
| Tričko | Černé | Velké | Normální | 4 |
| Tričko | Červené | Malé | Široké | 5 |
| Tričko | Červené | Malé | Normální | 6 |
| Tričko | Červené | Velké | Normální | 7 |

Zde je index.

| Číslo sady | Dimenze | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Index vám umožňuje dotazovat se na množství na skladě následujícími způsoby:

- `()` – Seskupeni podle všech

    - Tričko, 28

- `(ColorId)` – Seskupeni podle `ColorId`

    - Tričko, Černé, 10
    - Tričko, Červené, 18

- `(ColorId, SizeId)` – Seskupeno podle kombinace `ColorId` a `SizeId`

    - Tričko, Černé, Malé, 3
    - Tričko, Černé, Velké, 7
    - Tričko, Červené, Malé, 11
    - Tričko, Červené, Velké, 7

- `(ColorId, SizeId, StyleId)` – Seskupeno podle kombinace `ColorId`, `SizeId` a `StyleId`

    - Tričko, Černé, Malé, Široké, 1
    - Tričko, Černé, Malé, Normální, 2
    - Tričko, Černé, Velké, Široké, 3
    - Tričko, Černé, Velké, Normální, 4
    - Tričko, Červené, Malé, Široké, 5
    - Tričko, Červené, Malé, Normální, 6
    - Tričko, Červené, Velké, Normální, 7

> [!NOTE]
> Základní dimenze, které jsou definovány v konfiguraci oddílu, by neměly být definovány v konfiguracích indexu.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Konfigurace rezervace (volitelná)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Konfigurace rezervace je vyžadována, pokud chcete používat funkci předběžné rezervace. Konfigurace se skládá ze dvou základních částí:

- Mapování předběžných rezervací
- Hierarchie předběžných rezervací

### <a name="soft-reservation-mapping"></a>Mapování předběžných rezervací

Když provádíte rezervaci, asi budete chtít vědět, zda je požadované množství na skladě aktuálně k dispozici pro rezervaci. Ověření je spojeno s vypočítanou mírou, která představuje výpočetní vzorec kombinace fyzických měr.

Rezervační míra je například založena na fyzické míře `SoftReservOrdered` ze zdroje dat `iv` (Viditelnost zásob). V takovém případě můžete nastavit vypočítanou míru `AvailableToReserve` zdroje dat `iv`, jak je uvedeno zde.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `AvailPhysical` |
| Dodatek | `pos` | `Inbound` |
| Odčítání | `pos` | `Outbound` |
| Odčítání | `iv` | `SoftReservOrdered` |

Poté nastavte mapování předběžných rezervací, které poskytne mapování z rezervační míry `SoftReservOrdered` na vypočítanou míru `AvailableToReserve`.

| Zdroj dat fyzické míry | Fyzická míra | K dispozici pro zdroj dat rezervace | K dispozici pro vypočítanou míru rezervace |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Nyní, když provedete rezervaci zdroje `SoftReservOrdered`, Viditelnost zásob automaticky najde `AvailableToReserve` a s ním související výpočetní vzorec k provedení ověření rezervace.

Například máte v doplňku Viditelnost zásob k dispozici následující množství na skladě.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

V takovém případě se použije následující výpočet:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Pokud se tedy pokusíte vytvořit rezervaci ze zdroje `iv.SoftReservOrdered` a množství je menší nebo rovno `AvailableToReserve` (10), můžete rezervaci provést.

### <a name="soft-reservation-hierarchy"></a>Hierarchie předběžných rezervací

Hierarchie rezervací popisuje posloupnost dimenzí, které je třeba zadat při vytváření rezervace. Funguje stejným způsobem, jako funguje hierarchie indexu produktů pro dotazy na zásoby na skladě.

Hierarchie rezervací je nezávislá na hierarchii indexu produktů. Tato nezávislost vám umožňuje implementovat správu kategorií, kde mohou uživatelé rozdělit dimenze na detaily a specifikovat požadavky, aby vytvářeli přesnější rezervace.

Následuje příklad hierarchie předběžné rezervace.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

V tomto příkladu můžete provést rezervaci v následujících posloupnostech dimenzí:

- `()` – Není zadána žádná dimenze.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Platná posloupnost dimenzí by měla striktně dodržovat hierarchii rezervací, dimenzi po dimenzi. Například hierarchická posloupnost`(SiteId, LocationId, SizeId)` není platná, protože chybí `ColorId`.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Ukázka výchozí konfigurace

Během své fáze inicializace nastaví Viditelnost zásob výchozí konfiguraci. Konfiguraci můžete upravit podle potřeby.

### <a name="data-source-configuration"></a>Konfigurace zdroje dat

#### <a name="configuration-of-the-iv-data-source"></a>Konfigurace zdroje dat iv

Tato část popisuje, jak je konfigurován zdroj dat `iv`.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fyzické míry konfigurované pro zdroj dat iv

Pro zdroj dat `iv` jsou konfigurovány následující fyzické míry:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Vypočítaná míra OrderedTotal

Vypočítaná míra `OrderedTotal` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `Ordered` |
| Dodatek | `fno` | `Arrived` |
| Dodatek | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Vypočtená míra OnHand

Vypočítaná míra `OnHand` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `PhysicalInvent` |
| Dodatek | `iom` | `OnHand` |
| Dodatek | `erp` | `Unrestricted` |
| Dodatek | `erp` | `QualityInspection` |
| Dodatek | `pos` | `PosInbound` |
| Odčítání | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Vypočítaná míra ReservedTotal

Vypočítaná míra `ReservedTotal` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `ReservPhysical` |
| Dodatek | `fno` | `ReservOrdered` |
| Dodatek | `iv` | `SoftReservPhysical` |
| Dodatek | `iv` | `SoftReservOrdered` |
| Dodatek | `iv` | `ReservPhysical` |
| Dodatek | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Vypočítaná míra SoftReserved

Vypočítaná míra `SoftReserved` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `iv` | `SoftReservPhysical` |
| Dodatek | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Vypočítaná míra HardReserved

Vypočítaná míra `HardReserved` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `ReservPhysical` |
| Dodatek | `fno` | `ReservOrdered` |
| Dodatek | `iv` | `ReservPhysical` |
| Dodatek | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Vypočítaná míra OpenOrder

Vypočítaná míra `OpenOrder` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `OnOrder` |
| Dodatek | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Vypočítaná míra OnHandAvailable

Vypočítaná míra `OnHandAvailable` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `PhysicalInvent` |
| Dodatek | `iom` | `OnHand` |
| Dodatek | `erp` | `Unrestricted` |
| Dodatek | `erp` | `QualityInspection` |
| Dodatek | `pos` | `PosInbound` |
| Odčítání | `fno` | `ReservPhysical` |
| Odčítání | `iv` | `SoftReservPhysical` |
| Odčítání | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Vypočítaná míra AvailableToReserve

Vypočítaná míra `AvailableToReserve` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `PhysicalInvent` |
| Dodatek | `iom` | `OnHand` |
| Dodatek | `erp` | `Unrestricted` |
| Dodatek | `erp` | `QualityInspection` |
| Dodatek | `pos` | `PosInbound` |
| Dodatek | `fno` | `Ordered` |
| Dodatek | `fno` | `Arrived` |
| Dodatek | `iv` | `Ordered` |
| Odčítání | `fno` | `ReservPhysical` |
| Odčítání | `fno` | `ReservOrdered` |
| Odčítání | `iv` | `SoftReservPhysical` |
| Odčítání | `iv` | `SoftReservOrdered` |
| Odčítání | `iv` | `ReservPhysical` |
| Odčítání | `iv` | `ReservOrdered` |
| Odčítání | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Vypočítaná míra InventorySupply

Vypočítaná míra `InventorySupply` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `Ordered` |
| Dodatek | `fno` | `Arrived` |
| Dodatek | `iv` | `Ordered` |
| Dodatek | `fno` | `PhysicalInvent` |
| Dodatek | `iom` | `OnHand` |
| Dodatek | `erp` | `Unrestricted` |
| Dodatek | `erp` | `QualityInspection` |
| Dodatek | `pos` | `PosInbound` |
| Odčítání | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Vypočítaná míra InventoryDemand

Vypočítaná míra `InventoryDemand` se konfiguruje pro zdroj dat `iv`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `OnOrder` |
| Dodatek | `iom` | `OnOrder` |
| Dodatek | `iv` | `SoftReservPhysical` |
| Dodatek | `iv` | `SoftReservOrdered` |
| Dodatek | `fno` | `ReservPhysical` |
| Dodatek | `fno` | `ReservOrdered` |
| Dodatek | `iv` | `ReservPhysical` |
| Dodatek | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Konfigurace zdroje dat fno

Tato část popisuje, jak je konfigurován zdroj dat `fno`.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Mapování dimenzí pro zdroj dat fno

Mapování dimenzí, která jsou uvedena v následující tabulce, jsou konfigurována pro zdroj dat `fno`.

| Externí dimenze | Základní dimenze |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fyzické míry konfigurované pro zdroj dat fno

Pro zdroj dat `fno` jsou konfigurovány následující fyzické míry:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Konfigurace zdroje dat pos

Tato část popisuje, jak je konfigurován zdroj dat `pos`.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fyzické míry konfigurované pro zdroj dat pos

Pro zdroj dat `pos` jsou konfigurovány následující fyzické míry:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Vypočítaná míra AvailQuantity

Vypočítaná míra `AvailQuantity` se konfiguruje pro zdroj dat `pos`, jak ukazuje následující tabulka.

| Typ výpočtu | Zdroj dat | Fyzická míra |
|---|---|---|
| Dodatek | `fno` | `AvailPhysical` |
| Dodatek | `pos` | `PosInbound` |
| Odčítání | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Konfigurace zdroje dat iom

Pro zdroj dat `iom` (inteligentní správa objednávek) jsou konfigurovány následující fyzické míry:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfigurace zdroje dat erp

Pro zdroj dat `erp` (plánování podnikových zdrojů) jsou konfigurovány následující fyzické míry:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Konfigurace oddílu

Následující tabulka ukazuje výchozí konfiguraci oddílu.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Konfigurace indexu

Následující tabulka ukazuje výchozí konfiguraci indexu.

| Číslo sady | Dimenze | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Konfigurace rezervace

Tato část popisuje výchozí konfiguraci rezervace.

#### <a name="reservation-mapping"></a>Mapování rezervace

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Následující tabulka ukazuje výchozí mapování rezervace.

| Zdroj dat fyzické míry | Fyzická míra | K dispozici pro zdroj dat rezervace | K dispozici pro vypočítanou míru rezervace |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Hierarchie rezervací

Následující tabulka ukazuje výchozí hierarchii rezervace.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
