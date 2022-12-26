---
title: Konfigurace Inventory Visibility
description: Tento článek popisuje, jak konfigurovat doplněk Viditelnost zásob.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2a368535c9644e174d1a2460ac0891c9dc1b1b3f
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850016"
---
# <a name="configure-inventory-visibility"></a>Konfigurace Inventory Visibility

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Úvod

Než začnete pracovat s Viditelností zásob, musíte dokončit následující konfiguraci, jak je popsáno v tomto článku:

- [Konfigurace zdroje dat](#data-source-configuration)
- [Konfigurace oddílu](#partition-configuration)
- [Konfigurace hierarchie indexu produktů](#index-configuration)
- [Konfigurace rezervace (volitelná)](#reservation-configuration)
- [Konfigurace předběžného načtení dotazu (volitelné)](#query-preload-configuration)
- [Ukázka výchozí konfigurace](#default-configuration-sample)

## <a name="prerequisites"></a>Předpoklady

Než začnete, nainstalujte a nastavte doplněk Viditelnost inventáře podle popisu v tématu [Instalace a nastavení doplňku Viditelnost zásob](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Stránka Konfigurace aplikace Viditelnost zásob

V Power Apps stránka **Konfigurace** [aplikace Viditelnost zásob](inventory-visibility-power-platform.md) vám pomůže nastavit konfiguraci množství na skladě a konfiguraci předběžných rezervací. Po instalaci doplňku obsahuje výchozí konfigurace hodnotu ze softwaru Microsoft Dynamics 365 Supply Chain Management (zdroj dat `fno`). Výchozí nastavení můžete zkontrolovat. Navíc na základě vašich obchodních požadavků a požadavků na účtování zásob vašeho externího systému můžete upravit konfiguraci a standardizovat tak způsob, jakým mohou být změny v inventáři zaúčtovány, organizovány a dotazovány z různých systémů. Zbývající části tohoto článku vysvětlují, jak používat každou část stránky **Konfigurace**.

Po dokončení konfigurace vyberte v aplikaci příkaz **Aktualizovat konfiguraci**.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Povolení funkcí Viditelnost zásob ve správě funkcí Power Apps

Doplněk Viditelnost zásob přidává do vašeho systému několik nových funkcí instalace Power Apps. Ve výchozím nastavení jsou tyto funkce vypnuté. Chcete-li je použít, otevřete stránku **Konfigurace** a potom na kartě **Správa funkcí** zapněte podle potřeby následující funkce.

| Název ve Správě funkcí | Popis |
|---|---|
| *OnHandReservation* | Tato funkce vám umožní vytvářet rezervace, spotřebovat rezervace a/nebo obnovit zadaná množství zásob pomocí Viditelnosti zásob. Další informace viz [Rezervace ve Viditelnosti zásob](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Tato funkce poskytuje souhrn zásob produktů společně se všemi dimenzemi. Souhrnná data zásob budou pravidelně synchronizována z aplikace Viditelnost zásob. Výchozí frekvence synchronizace je jednou za 15 minut a lze ji nastavit až na každých 5 minut. Další informace naleznete v tématu [Souhrn zásob](inventory-visibility-power-platform.md#inventory-summary). |
| *OnHandIndexQueryPreloadBackgroundService* | Tato funkce pravidelně načítá a ukládá sadu souhrnných údajů o zásobách na základě předem nakonfigurovaných dimenzí. Poskytuje souhrn zásob, který obsahuje pouze dimenze, které jsou relevantní pro vaše každodenní podnikání a které jsou kompatibilní s položkami povolenými pro procesy řízení skladu (WMS). Další informace naleznete v části [Zapnutí a konfigurace předem načtených dotazů na zásoby na skladě](#query-preload-configuration) a [Přednačtení přehlednějšího dotazu na zásoby na skladě](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Tato volitelná funkce umožňuje plán změn na skladě a funkci Lze slíbit (ATP). Další informace najdete v tématu [Plán změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md). |
| *Přidělení* | Tato volitelná funkce umožňuje Viditelnosti zásob mít možnost ochrany zásob (ringfencing) a kontroly nadměrného prodeje. Další informace viz [Alokace zásob doplňku Viditelnost zásob](inventory-visibility-allocation.md). |
| *Povolte skladové položky ve viditelnosti zásob* | Tato volitelná funkce umožňuje viditelnosti zásob podporovat položky, které jsou povoleny pro procesy správy skladu (WMS). Další informace viz [Podpora Viditelnost zásob pro položky WMS](inventory-visibility-whs-support.md). |

> [!IMPORTANT]
> Doporučujeme použít buď funkci *OnHandIndexQueryPreloadBackgroundService* nebo *OnHandMostSpecificBackgroundService*, nikoli obě. Povolení obou funkcí ovlivní výkon.

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Vyhledání koncového bodu služby

Pokud neznáte správný koncový bod služby Viditelnost zásob, otevřete stránku **Konfigurace** v Power Apps a poté vyberte v pravém horním rohu příkaz **Zobrazit detaily služby**. Na stránce se zobrazí správný koncový bod služby. Koncový bod můžete také najít v Microsoft Dynamics Lifecycle Services, jak je popsáno v části [Nalezení koncového bodu podle prostředí Lifecycle Services](inventory-visibility-api.md#endpoint-lcs).

> [!NOTE]
> Použití nesprávného koncového bodu může způsobit selhání instalace Viditelnosti zásob a chyby, když je Supply Chain Management synchronizována s Viditelností zásob. Pokud si nejste jisti, jaký je váš koncový bod, obraťte se na správce systému. Adresy URL koncového bodu mají následující formát:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Konfigurace zdroje dat

Každý zdroj dat představuje systém, ze kterého vaše data pocházejí. Mezi příklady názvů zdroje dat patří `fno` (což odpovídá Supply Chain Management) a `pos` (což znamená „pokladní místo“). Ve výchozím nastavení je Supply Chain Management nastaven ve Viditelnosti zásob jako výchozí zdroj dat (`fno`).

> [!NOTE]
> Zdroj dat `fno` je vyhrazen pro Supply Chain Management. Pokud je váš doplněk Viditelnost zásob integrován s prostředím Supply Chain Management, doporučujeme neodstraňovat konfigurace související s `fno` ve zdroji dat.

Chcete-li přidat zdroj dat, postupujte takto:

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Zdroj dat** vyberte **Nový zdroj dat** pro přidání zdroje dat (např `ecommerce` nebo jiné smysluplné ID zdroje dat).

> [!NOTE]
> Když přidáte zdroj dat, ověřte si před aktualizací konfigurace služby Viditelnost zásob název zdroje dat, fyzické míry a mapování dimenzí. Po výběru příkazu **Aktualizovat konfiguraci** nebudete moci tato nastavení upravovat.

Konfigurace zdroje dat obsahuje následující části:

- Dimenze (mapování dimenzí)
- Fyzické míry
- Vypočtené míry

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimenze (mapování dimenzí)

Účelem konfigurace dimenze je standardizovat integraci více systémů pro odesílání událostí a dotazů na základě kombinací dimenzí. Viditelnost inventáře poskytuje seznam základních dimenzí, které lze mapovat z dimenzí vašeho zdroje dat. Pro mapování je k dispozici celkem třicet tři dimenzí.

- Ve výchozím nastavení, pokud jako jeden ze zdrojů dat používáte Supply Chain Management, je 13 dimenzí již mapováno na standardní dimenze Supply Chain Management. Dvanáct dalších dimenzí (`inventDimension1` až `inventDimension12`) je mapováno také na vlastní dimenze v Supply Chain Management. Zbývajících osm dimenzí (`ExtendedDimension1` až `ExtendedDimension8`) jsou rozšířené dimenze, které můžete namapovat na externí zdroje dat.
- Pokud jako jeden ze zdrojů dat nepoužíváte Supply Chain Management, můžete dimenze mapovat libovolně. Následující tabulka ukazuje úplný seznam dostupných dimenzí.

> [!NOTE]
> Pokud použijete Supply Chain Management a změníte výchozí mapování dimenzí mezi Supply Chain Management a Viditelností zásob, změněná dimenze nebude synchronizovat data. Proto pokud vaše dimenze není v seznamu výchozích dimenzí a používáte externí zdroj dat, doporučujeme v mapování použít dimenze `ExtendedDimension1` až `ExtendedDimension8`.

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
| Rozšíření | `ExtendedDimension1` až `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Typy dimenzí uvedené v předchozí tabulce slouží pouze pro informaci. Ve Viditelnosti zásob je nemusíte definovat.
>
> Dimenze inventáře (vlastní) mohou být vyhrazeny pro Supply Chain Management. V takovém případě místo toho použijte rozšířené dimenze.

Externí systémy mají přístup k Viditelnosti zásob prostřednictvím svých RESTful rozhraní API. Pro integraci vám Viditelnost zásob umožňuje konfigurovat *externí zdroj dat* a mapování z *externích dimenzí* do *základních dimenzí*. Následuje příklad tabulky mapování dimenzí.

| Externí dimenze | Základní dimenze |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Po konfiguraci mapování dimenzí můžete odeslat externí dimenze přímo do Viditelnosti zásob. Viditelnost zásob pak automaticky převede externí dimenze na základní.

Chcete-li přidat mapování dimenzí, postupujte následujícím způsobem.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Zdroj dat** vyberte zdroj dat, kde chcete provést mapování dimenzí. Potom v části **Mapování dimenzí** vyberte příkaz **Přidat**.

    ![Přidání mapování dimenzí](media/inventory-visibility-dimension-mapping.png "Přidání mapování dimenzí")

1. V poli **Název dimenze** zadejte zdrojovou dimenzi.
1. V poli **Na základní dimenzi** vyberte dimenzi v aplikaci Viditelnost zásob, kterou chcete namapovat.
1. Zvolte možnost **Uložit**.

Například jste již vytvořili zdroj dat s názvem `ecommerce` a zahrnuje dimenzi barvy produktu. V tomto případě k provedení mapování můžete nejprve přidat `ProductColor` k poli **Název dimenze** ve zdroji dat `ecommerce` a poté vybrat `ColorId` v poli **K základní dimenzi**.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fyzické míry

Když zdroj dat odešle změnu zásob do Viditelnosti zásob, odešle tuto změnu pomocí *fyzických měr*. Fyzické míry mění množství a odrážejí stav zásob. Na základě vašich požadavků můžete definovat své vlastní fyzické míry. Dotazy mohou být založeny na fyzických mírách.

Viditelnost zásob poskytuje seznam výchozích fyzických měr, které jsou mapovány s aplikací Supply Chain Management (zdroj dat `fno`). Tyto výchozí fyzická míry jsou převzaty ze stavů transakcí zásob na stránce **Seznam skladu** v Supply Chain Management (**Řízení zásob \> Dotazy a hlášení \> Seznam skladu**). Následující tabulka uvádí příklad fyzických měr.

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

Pokud je zdrojem dat Supply Chain Management, nemusíte znovu vytvářet výchozí fyzické míry. U externích zdrojů dat však můžete vytvořit nové fyzické míry podle následujících kroků.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Zdroj dat** vyberte zdroj dat, do kterého chcete přidat fyzické míry (například zdroj dat `ecommerce`). Poté v části **Fyzikální míry** vyberte **Přidat** a zadejte název míry (např. `Returned`, pokud chcete zaznamenat vrácená množství v tomto zdroji dat do viditelnosti zásob). Uložte změny.

### <a name="extended-dimensions"></a>Rozšířené dimenze

Zákazníci, kteří chtějí ve zdroji dat používat externí zdroje dat, mohou využít výhody rozšiřitelnosti, kterou nabízí Dynamics 365, vytvořením [rozšíření třídy](../../fin-ops-core/dev-itpro/extensibility/class-extensions.md) pro třády `InventOnHandChangeEventDimensionSet` a `InventInventoryDataServiceBatchJobTask`.

Po vytvoření rozšíření nezapomeňte provést synchronizaci s databází, aby se vlastní pole přidala do tabulky `InventSum`. Poté se můžete podívat do sekce Dimenze dříve v tomto článku a namapovat vlastní dimenze na kteroukoli z osmi rozšířených dimenzí v `BaseDimensions` v zásobách.

> [!NOTE] 
> Další podrobnosti o vytváření rozšíření naleznete v části [Domovská stránka pro rozšiřitelnost](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

### <a name="calculated-measures"></a>Vypočtené míry

Viditelnost zásob můžete použít k dotazování na fyzické míry zásob i na *vlastní vypočítané míry*. Vypočítané míry poskytují přizpůsobený výpočetní vzorec, který se skládá z kombinace fyzických měr. Tato funkce vám umožňuje definovat sadu fyzických měrných systémů, které budou přidány, anebo sadu fyzických měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.

> [!IMPORTANT]
> Vypočítaná míra je složením fyzických měr. Její vzorec může zahrnovat pouze fyzické míry bez duplicit, nikoli vypočítané míry.

Konfigurace umožňuje definovat sadu vzorců vypočítaných měr, které obsahují modifikátory sčítání a odčítání, aby se získalo celkové agregované výstupní množství.

Chcete-li nastavit vlastí vypočítanou míru, postupujte následovně.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Vypočítaná míra** vyberte příkaz **Nová výpočetní míra** a přidejte vypočítanou míru.
1. Nastavte následující pole pro novou vypočítanou míru:

    - **Název nové vypočítané míry** – Zadejte název vypočítané míry.
    - **Zdroj dat** – Vyberte zdroj dat, které se má zahrnout do nové vypočítané míry. Dotazovací systém je zdrojem dat.

1. Vyberte **Přidat** a přidejte modifikátor k nové vypočítané míře.
1. Nastavte následující pole pro nový modifikátor:

    - **Modifikátor** – Vyberte typ modifikátoru (*Sčítání* nebo *Odčítání*).
    - **Zdroj dat** – Vyberte zdroj dat, kde by se měla nacházet míra, která poskytuje hodnotu modifikátoru.
    - **Míra** – Vyberte název míry (z vybraného zdroje dat), která poskytuje hodnotu pro modifikátor.

1. Opakujte kroky 5 až 6, dokud nepřidáte všechny požadované modifikátory a nedokončíte vzorek vypočítané míry.
1. Zvolte možnost **Uložit**.

Například módní společnost působí ve třech zdrojích dat:

- `pos` – Odpovídá kanálu prodejny.
- `fno` – Odpovídá Supply Chain Management.
- `ecommerce` – Odpovídá webovému kanálu.

Bez vypočítaných měr, když se dotazujete na produkt D0002 (skříň) pod místem 1, skladem 11 a hodnotou dimenze `ColorID` `Red`, můžete získat následující výsledek dotazu, který zobrazuje množství zásob v rámci každé předem nakonfigurované fyzické míry. Nemáte však přehled o celkovém dostupném množství rezervací napříč vašimi zdroji dat.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Když se použije tento výpočetní vzorec, výsledek nového dotazu bude zahrnovat přizpůsobenou míru.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Výstup `MyCustomAvailableforReservation`, založený na nastavení výpočtu ve vlastních měrných systémech, je 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Konfigurace oddílu

V současné době se konfigurace oddílu skládá ze dvou základních dimenzí (`SiteId` a `LocationId`), které ukazují, jak jsou data distribuována. Operace ve stejném oddílu mohou poskytovat vyšší výkon za nižší náklady. Následující tabulka ukazuje výchozí konfiguraci oddílu, kterou poskytuje doplněk Viditelnost zásob.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Ve výchozím nastavení obsahuje řešení tuto konfiguraci oddílu. Z tohoto důvodu ji *nemusíte sami definovat*.

> [!IMPORTANT]
> Nepřizpůsobujte výchozí konfiguraci oddílu. Pokud ji odstraníte nebo změníte, pravděpodobně způsobíte neočekávanou chybu.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Konfigurace hierarchie indexu produktů

Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni. Místo toho můžete také chtít zobrazit výsledky, které jsou agregovány na základě dimenzí skladu.

Viditelnost zásob poskytuje flexibilitu tím, že vám umožňuje nastavení *indexů* ke zlepšení výkonu vašich dotazů. Tyto indexy jsou založeny na dimenzi nebo kombinaci dimenzí. Index se skládá z *čísla sady*, *dimenze* a *hierarchie*, jak je definováno v následující tabulce.

| Jméno | popis |
|---|---|
| Číslo sady | Dimenze, které patří do stejné sady (indexu), budou seskupeny a bude jim přiděleno stejné číslo sady. |
| Dimenze | Základní dimenze, na kterých je výsledek dotazu agregován. |
| Hierarchie | Hierarchie vám umožňuje zvýšit výkon konkrétních kombinací dimenzí při použití v parametrech filtru a seskupení podle dotazů. Pokud například nastavíte sadu dimenzí s posloupností hierarchie `(ColorId, SizeId, StyleId)`, pak může systém rychleji zpracovávat dotazy týkající se čtyřrozměrných kombinací. První kombinace je prázdná, druhá je `(ColorId)`, třetí je `(ColorId, SizeId)` a čtvrtá je `(ColorId, SizeId, StyleId)`. Ostatní kombinace nebudou urychleny. Filtry nejsou omezeny objednávkou, ale pokud chcete zlepšit jejich výkon, musí být uvnitř těchto dimenzí. Další informace naleznete v následujícím příkladu. |

Chcete-li nastavit index hierarchie produktů, postupujte následujícím způsobem.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Index hierarchie produktů** v části **Mapování dimenzí** vyberte příkaz **Přidat**.
1. Ve výchozím nastavení je k dispozici seznam indexů. Chcete-li upravit stávající index, vyberte **Upravit** nebo **Přidat** v části příslušného rejstříku. Chcete-li vytvořit novou sadu indexů, vyberte příkaz **Nová sada indexů**. Pro každý řádek v každé sadě indexů vyberte v poli **Dimenze** hodnotu ze seznamu základních dimenzí. Automaticky se generují hodnoty pro následující pole:

    - **Číslo sady** – Dimenze, které patří do stejné skupiny (indexu), budou seskupeny a bude jim přiděleno stejné číslo sady.
    - **Hierarchie** – Umožňuje zvýšit výkon konkrétních kombinací dimenzí při použití v parametrech filtru a seskupení podle dotazů.

> [!TIP]
> Zde je několik tipů, které je třeba mít na paměti při nastavování hierarchie indexu:
>
> - Základní dimenze, které jsou definovány v konfiguraci oddílu, by neměly být definovány v konfiguracích indexu. Pokud je základní dimenze znovu definována v konfiguraci indexu, nebudete moci pomocí tohoto indexu dotazovat.
> - Pokud se potřebujete dotazovat pouze na inventář, který je agregován všemi kombinacemi dimenzí, můžete nastavit jeden index, který obsahuje základní dimenzi `Empty`.

### <a name="example"></a>Příklad

Tato část poskytuje příklad, který ukazuje, jak hierarchie funguje.

Následující tabulka obsahuje seznam dostupných zásob pro tento příklad.

| Položka | ColorId | SizeId | StyleId | Množství |
|---|---|---|---|---|
| D0002 | Černá | Malá | Široká | 1 |
| D0002 | Černá | Malá | Pravidelný | 2 |
| D0002 | Černá | Velká | Široká | 3 |
| D0002 | Černá | Velká | Pravidelný | 4 |
| D0002 | Červená | Malá | Široká | 5 |
| D0002 | Červená | Malá | Pravidelný | 6 |
| D0002 | Červená | Velká | Pravidelný | 7 |

V následující tabulce jsou uvedena nastavení hierarchie indexů.

| Číslo sady | Dimenze | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Index vám umožňuje dotazovat se na množství na skladě následujícími způsoby:

- `()` – Seskupeni podle všech

    - D0002, 28

- `(ColorId)` – Seskupeni podle `ColorId`

    - D0002, Černá, 10
    - D0002, Červená, 18

- `(ColorId, SizeId)` – Seskupeno podle kombinace `ColorId` a `SizeId`

    - D0002, Černá, Malá, 3
    - D0002, Černá, Velká, 7
    - D0002, Červená, Malá, 11
    - D0002, Červená, Velká, 7

- `(ColorId, SizeId, StyleId)` – Seskupeno podle kombinace `ColorId`, `SizeId` a `StyleId`

    - D0002, Černá, Malá, Široká, 1
    - D0002, Černá, Malá, Běžná, 2
    - D0002, Černá, Velká, Široká, 3
    - D0002, Černá, Velká, Běžná, 4
    - D0002, Červená, Malá, Široká, 5
    - D0002, Červená, Malá, Běžná, 6
    - D0002, Červená, Velká, Běžná, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Konfigurace rezervace (volitelná)

Konfigurace rezervace je vyžadována, pokud chcete používat funkci předběžné rezervace. Konfigurace se skládá ze dvou základních částí:

- Mapování předběžných rezervací
- Hierarchie předběžných rezervací

### <a name="soft-reservation-mapping"></a>Mapování předběžných rezervací

Když provádíte rezervaci, asi budete chtít vědět, zda je požadované množství na skladě aktuálně k dispozici pro rezervaci. Ověření je spojeno s vypočítanou mírou, která představuje výpočetní vzorec kombinace fyzických měr.

Nastavením mapování z fyzické míry na vypočítanou míru povolíte službě Viditelnost zásob automaticky ověřovat dostupnost rezervace na základě fyzické míry.

Než nastavíte toto mapování, musí být na kartách **Zdroj dat** a **Vypočítaná míra** ve stránce **Konfigurace** v Power Apps definovány fyzické míry, vypočítané míry a jejich zdroje dat (jak je popsáno dříve v tomto článku).

Chcete-li definovat mapování předběžných rezervací, postupujte takto.

1. Definujte fyzickou míru, která slouží jako míra pro předběžnou rezervaci (např.`SoftReservPhysical`).
1. Na kartě **Vypočítaná míra** ve stránce **Konfigurace** definujte vypočítanou míru *k dispozici pro rezervaci* (AFR), která obsahuje výpočetní vzorec AFR, který chcete namapovat na fyzickou míru. Můžete například nastavit `AvailableToReserve` (k dispozici pro rezervaci), takže je mapováno na dříve definovanou fyzickou míru `SoftReservPhysical`. Tímto způsobem můžete zjistit, která množství se stavem zásob `SoftReservPhysical` budou k dispozici pro rezervaci. Následující tabulka ukazuje výpočetní vzorec AFR.

    | Typ výpočtu | Zdroj dat | Fyzická míra |
    |---|---|---|
    | Dodatek | `fno` | `AvailPhysical` |
    | Dodatek | `pos` | `Inbound` |
    | Odčítání | `pos` | `Outbound` |
    | Odčítání | `iv` | `SoftReservPhysical` |

    Doporučujeme nastavit vypočítanou míru tak, aby obsahovala fyzickou míru, ze které vychází rezervační míra. Tímto způsobem bude vypočtené množství opatření ovlivněno množstvím rezervovaného opatření. Proto by v tomto příkladu vypočítaná míra `AvailableToReserve` `iv` zdroje dat měla obsahovat fyzickou míru `SoftReservPhysical` u `iv` jako součást.

1. Otevřete stránku **Konfigurace**.
1. Na kartě **Mapování předběžné rezervace** nastavte mapování z fyzické míry na vypočítanou míru. V předchozím příkladu můžete následující nastavení použít k mapování `AvailableToReserve` na dříve definovanou fyzickou míru `SoftReservPhysical`.

    | Zdroj dat fyzické míry | Fyzická míra | K dispozici pro zdroj dat rezervace | K dispozici pro vypočítanou míru rezervace |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Pokud se vám nepodaří upravit kartu **Mapování předběžné rezervace**, může být nutné zapnout funkci *OnHandReservation* na kartě **Správa funkcí**.

Nyní, když provedete rezervaci zdroje `SoftReservPhysical`, Viditelnost zásob automaticky najde `AvailableToReserve` a s ním související výpočetní vzorec k provedení ověření rezervace.

Například máte v doplňku Viditelnost zásob k dispozici následující množství na skladě.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Pokud se tedy pokusíte vytvořit rezervaci ze zdroje `iv.SoftReservPhysical` a množství je menší nebo rovno `AvailableToReserve` (10), požadavek na předběžnou rezervaci uspěje.

> [!NOTE]
> Když zavoláte rezervační rozhraní API, můžete řídit ověření rezervace zadáním logické hodnoty parametru `ifCheckAvailForReserv` v těle požadavku. Hodnota `True` znamená, že je vyžadováno ověření, zatímco hodnota `False` znamená, že ověření není vyžadováno (ačkoli můžete skončit s negativním množstvím `AvailableToReserve`, systém vám stále umožní předběžnou rezervaci). Výchozí hodnota je typu `True`.

### <a name="soft-reservation-hierarchy"></a>Hierarchie předběžných rezervací

Hierarchie rezervací popisuje posloupnost dimenzí, které je třeba zadat při vytváření rezervace. Funguje stejným způsobem, jako funguje hierarchie indexu produktů pro dotazy na zásoby na skladě.

Hierarchie rezervací je nezávislá na hierarchii indexu produktů. Tato nezávislost vám umožňuje implementovat správu kategorií, kde mohou uživatelé rozdělit dimenze na detaily a specifikovat požadavky, aby vytvářeli přesnější rezervace. Vaše hierarchie měkkých rezervací by měla obsahovat `SiteId` a `LocationId` jako součásti, protože vytvářejí konfiguraci oddílu. Při rezervaci musíte určit oddíl pro produkt.

Následuje příklad hierarchie předběžné rezervace.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

V tomto příkladu můžete provést rezervaci v následujících posloupnostech dimenzí. Při rezervaci musíte určit oddíl pro produkt. Základní hierarchie, kterou můžete použít, je tedy `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Platná posloupnost dimenzí by měla striktně dodržovat hierarchii rezervací, dimenzi po dimenzi. Například hierarchická posloupnost`(SiteId, LocationId, SizeId)` není platná, protože chybí `ColorId`.

## <a name="available-to-promise-configuration-optional"></a>Konfigurace funkce Lze slíbit (volitelné)

Viditelnost zásob vám umožní naplánovat budoucí změny ve skladu a vypočítat množství, které lze slíbit (ATP). ATP (Lze slíbit) je množství položky, které je k dispozici a může být odběrateli přislíbena v příštím období. Použití tohoto výpočtu může výrazně zvýšit vaši schopnost plnění objednávky. Chcete-li tuto funkci používat, musíte ji povolit na kartě **Správa funkcí** a poté ji nastavit na kartě **Nastavení ATP**. Další informace najdete v tématu [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md).

## <a name="turn-on-and-configure-preloaded-on-hand-queries-optional"></a><a name="query-preload-configuration"></a>Zapnutí a konfigurace předem načtených dotazů na zásoby na skladě (volitelné)

Viditelnost zásob může pravidelně načíst a uložit sadu souhrnných údajů o zásobách na základě předem nakonfigurovaných dimenzí. Přináší to následující výhody:

- Přehlednější zobrazení, které ukazuje souhrn zásob pouze s dimenzemi, které jsou relevantní pro vaši každodenní činnost.
- Souhrn zásob, který je kompatibilní s položkami povolenými pro procesy řízení skladu (WMS).

Další informace, jak s touto funkcí pracovat po jejím nastavení, najdete v části [Přednačtení přehlednějšího dotazu na zásoby na skladě](inventory-visibility-power-platform.md#preload-streamlined-onhand-query).

> [!IMPORTANT]
> Doporučujeme použít buď funkci *OnHandIndexQueryPreloadBackgroundService* nebo *OnHandMostSpecificBackgroundService*, nikoli obě. Povolení obou funkcí ovlivní výkon.

Pro nastavení funkce postupujte následujícím způsobem:

1. Přihlaste se do Power aplikace Viditelnost zásob.
1. Přejděte do nabídky **Konfigurace \> Správa funkcí a nastavení**.
1. Pokud je již funkce *OnHandIndexQueryPreloadBackgroundService* povolena, doporučujeme ji prozatím vypnout, protože dokončení procesu čištění může trvat velmi dlouho. Zapnete ji znovu později v tomto postupu.
1. Otevřete kartu **Nastavení přednačtení**.
1. V části **Krok 1: Vyčištění úložiště pro přednačtení** vyberte **Vyčistit**, čímž databázi vyčistíte a připravíte pro přijetí nových nastavení skupiny.
1. V části **Krok 2: Nastavení seskupení podle hodnot** zadejte do pole **Seskupit výsledky podle** seznam názvů polí oddělených čárkami, podle kterých se mají seskupit výsledky dotazu. Jakmile budete mít data v databázi úložiště pro přednačtení, nebudete moci toto nastavení změnit, dokud databázi nevyčistíte, jak je popsáno v předchozím kroku.
1. Přejděte do nabídky **Konfigurace \> Správa funkcí a nastavení**.
1. Zapněte funkci *OnHandIndexQueryPreloadBackgroundService*.
1. Vyberte příkaz **Aktualizovat konfiguraci** v pravém horním rohu stránky **Konfigurace**, abyste změny potvrdili

## <a name="complete-and-update-the-configuration"></a>Dokončení a aktualizace konfigurace

Po dokončení konfigurace musíte potvrdit všechny změny v doplňku Viditelnosti zásob. K potvrzení změn postupujte následovně.

1. V Power Apps na stránce **Konfigurace** vyberte **Aktualizovat konfiguraci** v pravém horním rohu. 
1. Systém vyžaduje přihlašovací údaje. Zadejte následující hodnoty:

    - **ID klienta** – ID aplikace Azure, které jste vytvořili pro Viditelnost zásob.
    - **ID tenanta** – ID vašeho tenanta Azure.
    - **Tajný klíč klienta** – Tajný klíč aplikace Azure, který jste vytvořili pro Viditelnost zásob.

    Další informace o těchto přihlašovacích údajích a jak je najít, najdete v části [Instalace a nastavení doplňku Viditelnost zásob](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Ověřte si před aktualizací konfigurace název zdroje dat, fyzické míry a mapování dimenzí. Po aktualizaci nebudete moci tato nastavení upravovat.

1. Po přihlášení vyberte **Aktualizovat konfiguraci** znovu. Systém použije vaše nastavení a ukáže, co se změnilo.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Ukázka výchozí konfigurace

Během své fáze inicializace nastaví Viditelnost zásob výchozí konfiguraci, což je podrobně popsáno zde. Konfiguraci můžete upravit podle potřeby.

### <a name="data-source-configuration"></a>Konfigurace zdroje dat

#### <a name="configuration-of-the-iv-data-source"></a>Konfigurace zdroje dat iv

Tato část popisuje, jak je konfigurován zdroj dat `iv`.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fyzické míry konfigurované pro zdroj dat „iv“

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

#### <a name="configuration-of-the-fno-data-source"></a>Konfigurace zdroje dat „fno“

Tato část popisuje, jak je konfigurován zdroj dat `fno`.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Mapování dimenzí pro zdroj dat „fno“

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fyzické míry konfigurované pro zdroj dat „fno“

Pro zdroj dat `fno` jsou konfigurovány následující fyzické míry:

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>Konfigurace zdroje dat „pos“

Tato část popisuje, jak je konfigurován zdroj dat `pos`.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fyzické míry konfigurované pro zdroj dat „pos“

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

#### <a name="configuration-of-the-iom-data-source"></a>Konfigurace zdroje dat „iom“

Pro zdroj dat `iom` (inteligentní správa objednávek) jsou konfigurovány následující fyzické míry:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfigurace zdroje dat „erp“

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

Následující tabulka ukazuje výchozí mapování rezervace.

| Zdroj dat fyzické míry | Fyzická míra | K dispozici pro zdroj dat rezervace | K dispozici pro vypočítanou míru rezervace |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Hierarchie rezervací

Následující tabulka ukazuje výchozí hierarchii rezervace.

| Základní dimenze | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
