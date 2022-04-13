---
title: Veřejná rozhraní API Viditelnosti zásob
description: Toto téma popisuje veřejná API, která jsou poskytována doplňkem Viditelnost zásob.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: cbd33b16a4b21e8e1931bc61cb55e376e7d73179
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524458"
---
# <a name="inventory-visibility-public-apis"></a>Veřejná rozhraní API Viditelnosti zásob

[!include [banner](../includes/banner.md)]


Toto téma popisuje veřejná API, která jsou poskytována doplňkem Viditelnost zásob.

Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů pro integraci. Podporuje čtyři hlavní typy interakce:

- Odesílání změn zásob na skladě do doplňku z externího systému
- Nastavení nebo přepsání množství zásob na skladě v doplňku z externího systému
- Odesílání událostí rezervace do doplňku z externího systému
- Dotazování na aktuální množství zásob na skladě z externího systému

V následující tabulce jsou uvedeny rozhraní API, které jsou aktuálně k dispozici:

| Cesta | Metoda | popis |
|---|---|---|
| /api/environment/{environmentId}/onhand | Zaúčtovat | [Vytvoří jednu událost změny ve skladu](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Zaúčtovat | [Vytvoří více změnových událostí](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Zaúčtovat | [Nastaví/přepíše množství na skladě](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Zaúčtovat | [Vytvoří jednu rezervační událost](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Zaúčtovat | [Vytvoří více rezervačních událostí](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/on-hand/changeschedule | Zaúčtovat | [Vytvoří jednu plánovanou změnu ve skladu](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/on-hand/changeschedule/bulk | Zaúčtovat | [Vytvoří více plánovaných změn ve skladu](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Zaúčtovat | [Dotaz pomocí metody POST](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Získat | [Dotaz pomocí metody GET](#query-with-get-method) |

> [!NOTE]
> Součástí cesty {environmentId} je ID prostředí v Microsoft Dynamics Lifecycle Services (LCS).
> 
> Hromadné API může vrátit maximálně 512 záznamů pro každý požadavek.

Společnost Microsoft poskytla integrovanou kolekci požadavků *Postman*. Tuto kolekci můžete importovat do svého softwaru *Postman* pomocí následujícího sdíleného odkazu: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Najděte koncový bod podle svého prostředí Lifecycle Services

Mikroslužba Viditelnost zásob je nasazena v prostředí Microsoft Azure Service Fabric, ve více geografických oblastech a více regionech. V současné době neexistuje centrální koncový bod, který by mohl automaticky přesměrovat váš požadavek na odpovídající geografickou oblast a region. Proto musíte tyto informace sestavit do adresy URL pomocí následujícího vzorce:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Krátký název regionu najdete v prostředí Microsoft Dynamics Lifecycle Services (LCS). V následující tabulce jsou uvedeny regiony, které jsou aktuálně k dispozici.

| Oblast Azure        | Krátký název oblasti |
| ------------------- | ----------------- |
| Austrálie – východ      | eau               |
| Austrálie – jihovýchod | seau              |
| Střední Kanada      | cca               |
| Kanada – východ         | eca               |
| Evropa – sever        | neu               |
| Evropa – západ         | weu               |
| Východní USA             | eus               |
| USA – západ             | wus               |
| Velká Británie – jih            | suk               |
| Velká Británie – západ             | wuk               |
| Východní Japonsko          | ejp               |
| Západní Japonsko          | wjp               |
| Jižní Brazílie        | sbr               |
| Střed USA – jih    | scus              |

Číslo ostrova je místo, kde je vaše prostředí LCS nasazeno v prostředí Service Fabric. V současné době neexistuje žádný způsob, jak tyto informace získat na straně uživatele.

Společnost Microsoft vytvořila uživatelské rozhraní (UI) v Power Apps, abyste mohli získat úplný koncový bod mikroslužby. Více informací najdete v části [Vyhledání koncového bodu služby](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Ověřování

Token zabezpečení platformy se používá k volání veřejného API Viditelnosti zásob. Proto musíte _token Azure Active Directory (Azure AD)_ vygenerovat pomocí vaší aplikace Azure AD. Poté musíte token Azure AD použít k získání _přístupového tokenu_ od služby zabezpečení.

Společnost Microsoft poskytuje integrovanou kolekci pro získání tokenů *Postman*. Tuto kolekci můžete importovat do svého softwaru *Postman* pomocí následujícího sdíleného odkazu: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Chcete-li získat token služby zabezpečení, postupujte takto:

1. Přihlaste se na portál Azure a použijte jej k vyhledání hodnot `clientId` a `clientSecret` pro vaši aplikaci Dynamics 365 Supply Chain Management.
1. Načtěte token Azure AD (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Metoda:** `GET`
   - **Obsah těla (údaje formuláře):**

     | Klíč           | Hodnota                                |
     | ------------- | ------------------------------------ |
     | id klienta     | ${aadAppId}                          |
     | tajný klíč klienta | ${aadAppSecret}                      |
     | typ grantu    | client_credentials                   |
     | prostředek      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   V odpovědi byste měli obdržet token Azure AD (`aadToken`). Výsledek by měl vypadat podobně jako v následujícím příkladu.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
       "access_token": "eyJ0eX...8WQ"
   }
   ```

1. Formulujte požadavek JSON (JavaScript Object Notation), který se podobá následujícímu příkladu.

   ```json
   {
       "grant_type": "client_credentials",
       "client_assertion_type": "aad_app",
       "client_assertion": "{Your_AADToken}",
       "scope": "https://inventoryservice.operations365.dynamics.com/.default",
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   Mějte na paměti následující body:

   - Hodnotou `client_assertion` musí být token Azure AD (`aadToken`), který jste obdrželi v předchozím kroku.
   - Hodnota `context` musí být ID prostředí LCS, do kterého chcete doplněk nasadit.
   - Nastavte všechny ostatní hodnoty, jak je znázorněno v příkladu.

1. Načtěte přístupový token (`access_token`) odesláním požadavku HTTP s následujícími vlastnostmi:

   - **URL:** `https://securityservice.operations365.dynamics.com/token`
   - **Metoda:** `POST`
   - **Záhlaví HTTP:** Včetně verze API. (Klíč je`Api-Version` a hodnota je`1.0` .)
   - **Obsah těla:** Zahrňte požadavek JSON, který jste vytvořili v předchozím kroku.

   V odpovědi byste měli obdržet přístupový token (`access_token`). Tento token musíte použít jako nosný token pro volání rozhraní API doplňku Viditelnost zásob. Následuje příklad.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> Když použijete kolekci požadavků *Postman* k volání veřejných rozhraní API viditelnosti zásob, musíte pro každý požadavek přidat token nositele. Token nositele najdete takto: vyberte kartu **Autorizace** pod adresou URL požadavku, vyberte typ **Token nositele** a zkopírujte přístupový token, který byl načten v posledním kroku. V dalších částech tohoto tématu použijete `$access_token` jako token, který byl načten v posledním kroku.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Vytvoření událostí změn ve skladu

Existují dvě rozhraní API pro vytváření událostí skladových změn:

- Vytvoření jednoho záznamu: `/api/environment/{environmentId}/onhand`
- Vytvoření více záznamů: `/api/environment/{environmentId}/onhand/bulk`

Následující tabulka sumarizuje význam každého pole v těle JSON.

| ID pole | popis |
|---|---|
| `id` | Jedinečné ID pro konkrétní událost změny. Toto ID se používá k zajištění toho, že pokud komunikace se službou během publikování selže, stejná událost nebude v systému započítána dvakrát, pokud bude odeslána znovu. |
| `organizationId` | Identifikátor organizace spojené s událostí. Tato hodnota se mapuje na organizaci nebo ID datové oblasti v Supply Chain Management. |
| `productId` | Identifikátor produktu. |
| `quantities` | Množství, o které se musí změnit skladové množství. Pokud je například do police přidáno 10 nových knih, bude tato hodnota `quantities:{ shelf:{ received: 10 }}`. Pokud budou tři knihy odstraněny z police nebo prodány, bude tato hodnota `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Zdroj dat dimenzí použitých v události změny publikování změny a dotazu. Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat. Viditelnost zásob může konfiguraci dimenze použít k mapování vlastních dimenzí na obecné výchozí dimenze. Pokud není zadána hodnota `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné [základní dimenze](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dynamický pár klíč/hodnota. Hodnoty jsou namapovány na některé dimenze v Supply Chain Management. Můžete však také přidat vlastní dimenze (např ._Zdroj_) k označení, zda událost pochází ze Supply Chain Management nebo z externího systému. |

> [!NOTE]
> Parametry `SiteId` a `LocationId` tvoří [ konfiguraci oddílu](inventory-visibility-configuration.md#partition-configuration). Proto je musíte zadat v dimenzích, když vytváříte události změny zásob na skladě, nastavujete nebo přepisujete množství v ruce nebo vytváříte události rezervace.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Vytvoření jedné události změny ve skladu

Toto API vytvoří jednu událost změny ve skladu.

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Následující příklad ukazuje ukázkový obsah těla. V této ukázce odešlete událost změny pro produkt *T-shirt* (tričko). Tato událost je ze systému pokladního místa (POS) a zákazník vrátil červené tričko zpět do vašeho obchodu. Tato událost zvýší množství produktu *T-shirt* o 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Následující příklad ukazuje ukázkový obsah těla bez `dimensionDataSource`. V tomto případě bude `dimensions` [základní dimenze](inventory-visibility-configuration.md#data-source-configuration-dimension). Pokud je nastavena hodnota `dimensionDataSource`, `dimensions` může být buď dimenze zdroje dat, nebo základní dimenze.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Vytvoření více změnových událostí

Toto API může vytvářet více záznamů současně. Jediné rozdíly mezi tímto API a [API pro jednu událost](#create-one-onhand-change-event) jsou hodnoty `Path` a `Body`. U tohoto API obsahuje `Body` pole záznamů. Maximální počet záznamů je 512, což znamená, že rozhraní API pro hromadné změny může podporovat až 512 událostí změn najednou.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Nastavení/přepis množství na skladě

API _Set on-hand_ přepíše aktuální data pro zadaný produkt.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Následující příklad ukazuje ukázkový obsah těla. Chování tohoto rozhraní API se liší od chování těch API, která jsou popsána v části [Vytvoření událostí změn ve skladu](#create-onhand-change-event) dříve v tomto tématu. V této ukázce bude množství produktu *T-shirt* nastaveno na 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Vytvoření rezervačních událostí

Chcete-li použít API *Reserve*, musíte otevřít funkci rezervace a dokončit konfiguraci rezervace. Další informace viz [Konfigurace rezervace (volitelná)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Vytvoření jedné rezervační události

Je možné provést rezervaci proti různým nastavením zdroje dat. Chcete -li konfigurovat tento typ rezervace, nejprve zadejte zdroj dat v parametru `dimensionDataSource`. Poté v parametru `dimensions` zadejte kóty podle nastavení dimenzí v cílovém zdroji dat.

Když zavoláte rezervační rozhraní API, můžete řídit ověření rezervace zadáním logické hodnoty parametru `ifCheckAvailForReserv` v těle požadavku. Hodnota `True` znamená, že je vyžadováno ověření, zatímco hodnota `False` znamená, že ověření není vyžadováno. Výchozí hodnota je typu `True`.

Pokud chcete zrušit rezervaci nebo zrušit rezervaci zadaného množství zásob, nastavte množství na zápornou hodnotu a nastavte parametr `ifCheckAvailForReserv` na `False` pro přeskočení ověření.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Následující příklad ukazuje ukázkový obsah těla.

```json
{
    "id": "reserve-0",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Vytvoření více rezervačních událostí

Toto API je hromadná verze [API pro jednu událost](#create-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="query-on-hand"></a>Dotaz na zásoby na skladě

Rozhraní API _Query on-hand_ (dotaz na zásoby na skladě) se používá k načítání aktuálních skladových dat vašich produktů. Toto rozhraní API aktuálně podporuje dotazování až 100 jednotlivých položek podle hodnoty `ProductID`. V každém dotazu také může být zadáno více hodnot `SiteID` a `LocationID`. Maximální limit je definován jako `NumOf(SiteID) * NumOf(LocationID) <= 100`.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Dotaz pomocí metody POST

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

V těle této žádosti, `dimensionDataSource` je stále volitelný parametr. Pokud není nastaven, s parametrem `filters` bude zacházeno jako se *základními dimenzemi*. K dispozici jsou čtyři povinná pole pro `filters`: `organizationId`, `productId`, `siteId`, a `locationId`.

- `organizationId` by měl obsahovat pouze jednu hodnotu, ale stále je to pole.
- `productId` může obsahovat jednu nebo více hodnot. Pokud je prázdné pole, budou vráceny všechny produkty.
- `siteId` a `locationId` se ve viditelnosti skladu používají k dělení. V požadavku *Dotaz na zásoby na skladě* můžete zadat více než jednu hodnotu `siteId` a `locationId`. V aktuálním vydání musíte zadat obě hodnoty `siteId` i `locationId`.

Parametr `groupByValues` by se měl řídit vaší konfigurací pro indexování. Další informace najdete v tématu [Konfigurace hierarchie indexu produktů](./inventory-visibility-configuration.md#index-configuration).

Parametr `returnNegative` určuje, zda výsledky obsahují záporné položky.

> [!NOTE]
> Pokud jste povolili časový plán změn ve skladu a funkce Lze slíbit, váš dotaz může také zahrnovat logický parametr `QueryATP`, který řídí, zda výsledky dotazu obsahují informace funkce Lze slíbit. Další informace a příklady najdete v tématu [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md).

Následující příklad ukazuje ukázkový obsah těla.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Následující příklady ukazují, jak dotazovat všechny produkty na konkrétním pracovišti a umístění.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Dotaz pomocí metody GET

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

Zde je ukázka adresy URL pro metodu GET. Tento GET požadavek je přesně stejný jako ukázka POST, která byla uvedena dříve.

```txt
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Lze slíbit (ATP)

Viditelnost zásob vám umožní naplánovat budoucí změny ve skladu a vypočítat množství, které lze slíbit. ATP (Lze slíbit) je množství položky, které je k dispozici a může být odběrateli přislíbena v příštím období. Použití výpočtu ATP může výrazně zvýšit vaši schopnost plnění objednávky. Informace o tom, jak povolit tuto funkci a jak interagovat s Viditelností zásob prostřednictvím jejího rozhraní API po aktivaci funkce, naleznete v tématu [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
