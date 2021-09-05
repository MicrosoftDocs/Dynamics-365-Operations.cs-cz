---
title: Veřejná rozhraní API Viditelnosti zásob
description: Toto téma popisuje veřejná API, která jsou poskytována doplňkem Viditelnost zásob.
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
ms.openlocfilehash: 0aca5838ff6d7c9c4d881698be1e2da2e0e1c02e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343625"
---
# <a name="inventory-visibility-public-apis"></a>Veřejná rozhraní API Viditelnosti zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

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
| /api/environment/{environmentId}/onhand/indexquery | Získat | [Dotaz pomocí metody POST](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Zaúčtovat | [Dotaz pomocí metody GET](#query-with-get-method) |

Společnost Microsoft poskytla integrovanou kolekci požadavků *Postman*. Tuto kolekci můžete importovat do svého softwaru *Postman* pomocí následujícího sdíleného odkazu: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Najděte koncový bod podle svého prostředí Lifecycle Services

Mikroslužba Viditelnost zásob je nasazena v prostředí Microsoft Azure Service Fabric, ve více geografických oblastech a více regionech. V současné době neexistuje centrální koncový bod, který by mohl automaticky přesměrovat váš požadavek na odpovídající geografickou oblast a region. Proto musíte tyto informace sestavit do adresy URL pomocí následujícího vzorce:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Krátký název regionu najdete v prostředí Microsoft Dynamics Lifecycle Services (LCS). V následující tabulce jsou uvedeny regiony, které jsou aktuálně k dispozici.

| Oblast Azure | Krátký název oblasti |
|---|---|
| Austrálie – východ | eau |
| Austrálie – jihovýchod | seau |
| Střední Kanada | cca |
| Kanada – východ | eca |
| Evropa – sever | neu |
| Evropa – západ | weu |
| Východní USA | eus |
| USA – západ | wus |
| Velká Británie – jih | suk |
| Velká Británie – západ | wuk |

Číslo ostrova je místo, kde je vaše prostředí LCS nasazeno v prostředí Service Fabric. V současné době neexistuje žádný způsob, jak tyto informace získat na straně uživatele.

Společnost Microsoft vytvořila uživatelské rozhraní (UI) v Power Apps, abyste mohli získat úplný koncový bod mikroslužby. Více informací najdete v části [Vyhledání koncového bodu služby](inventory-visibility-power-platform.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Ověřování

Token zabezpečení platformy se používá k volání veřejného API Viditelnosti zásob. Proto musíte _token Azure Active Directory (Azure AD)_ vygenerovat pomocí vaší aplikace Azure AD. Poté musíte token Azure AD použít k získání _přístupového tokenu_ od služby zabezpečení.

Chcete-li získat token služby zabezpečení, postupujte takto:

1. Přihlaste se na portál Azure a použijte jej k vyhledání hodnot `clientId` a `clientSecret` pro vaši aplikaci Dynamics 365 Supply Chain Management.
1. Načtěte token Azure AD (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Metoda:** `GET`
    - **Obsah těla (údaje formuláře):**

        | Klíč | Hodnota |
        |---|---|
        | id klienta | ${aadAppId} |
        | tajný klíč klienta | ${aadAppSecret} |
        | typ grantu | client_credentials |
        | prostředek | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

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
    - Hodnota `context` musí být ID prostředí, do kterého chcete doplněk nasadit.
    - Nastavte všechny ostatní hodnoty, jak je znázorněno v příkladu.

1. Odešlete požadavek HTTP s následujícími vlastnostmi:

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

V dalších částech použijete `$access_token` jako token, který byl načten v posledním kroku.

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
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Následující příklad ukazuje ukázkový obsah těla bez `dimensionDataSource`.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Vytvoření více změnových událostí

Toto API může vytvářet více záznamů současně. Jediné rozdíly mezi tímto API a [API pro jednu událost](#create-one-onhand-change-event) jsou hodnoty `Path` a `Body`. U tohoto API obsahuje `Body` pole záznamů.

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
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "@PRODUCT1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
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

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Chcete-li použít API *Reserve*, musíte otevřít funkci rezervace a dokončit konfiguraci rezervace. Další informace viz [Konfigurace rezervace (volitelná)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Vytvoření jedné rezervační události

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

API _Query on-hand_ (dotaz na zásoby na skladě) se používá k načítání aktuálních skladových dat vašich produktů.

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
        organizationId: string,
        filters: {
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Následující příklad ukazuje ukázkový obsah těla.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Dotaz pomocí metody GET

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
