---
title: Veřejné rozhraní API Inventory Visibility
description: Tento článek popisuje veřejná API, která jsou poskytována doplňkem Viditelnost zásob.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762827"
---
# <a name="inventory-visibility-public-apis"></a>Veřejné rozhraní API Inventory Visibility

[!include [banner](../includes/banner.md)]

Tento článek popisuje veřejná API, která jsou poskytována doplňkem Viditelnost zásob.

Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů pro integraci. Podporuje čtyři hlavní typy interakce:

- Odesílání změn zásob na skladě do doplňku z externího systému
- Nastavení nebo přepsání množství zásob na skladě v doplňku z externího systému
- Odesílání událostí rezervace do doplňku z externího systému
- Dotazování na aktuální množství zásob na skladě z externího systému

V následující tabulce jsou uvedeny rozhraní API, které jsou aktuálně k dispozici:

| Cesta | Metoda | popis |
|---|---|---|
| /api/environment/{environmentId}/onhand | Zaúčtovat | [Vytvoří jednu událost změny ve skladu](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Zaúčtovat | [Vytvoří více změnových událostí](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Zaúčtovat | [Nastaví/přepíše množství na skladě](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Zaúčtovat | [Vytvoření jedné události předběžné rezervace](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Zaúčtovat | [Vytvoří více událostí předběžné rezervace](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | Zaúčtovat | [Vrátí jednu událost předběžné rezervace](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Zaúčtovat | [Vrátí více událostí předběžné rezervace](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Zaúčtovat | [Vytvoří jednu plánovanou změnu ve skladu](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Zaúčtovat | [Vytvoří více změn ve skladu s daty](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Zaúčtovat | [Dotaz pomocí metody POST](#query-with-post-method) (doporučeno) |
| /api/environment/{environmentId}/onhand | Získat | [Dotaz pomocí metody GET](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | Zaúčtovat | [Přesný dotaz pomocí metody POST](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | Zaúčtovat | [Vytvoří jednu událost přidělení](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | Zaúčtovat | [Vytvoří jednu událost zrušení přidělení](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | Zaúčtovat | [Vytvoří jednu událost změny přidělení](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | Zaúčtovat | [Vytvoří jednu událost spotřeby](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | Zaúčtovat | [Dotaz na výsledek přidělení](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Součástí cesty {environmentId} je ID prostředí v Microsoft Dynamics Lifecycle Services.
> 
> Hromadné API může vrátit maximálně 512 záznamů pro každý požadavek.

Společnost Microsoft poskytla integrovanou kolekci požadavků *Postman*. Tuto kolekci můžete importovat do svého softwaru *Postman* pomocí následujícího sdíleného odkazu: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Najděte koncový bod podle svého prostředí Lifecycle Services

Mikroslužba Viditelnost zásob je nasazena v prostředí Microsoft Azure Service Fabric, ve více geografických oblastech a více regionech. V současné době neexistuje centrální koncový bod, který by mohl automaticky přesměrovat váš požadavek na odpovídající geografickou oblast a region. Proto musíte tyto informace sestavit do adresy URL pomocí následujícího vzorce:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Krátký název regionu najdete v prostředí Lifecycle Services. V následující tabulce jsou uvedeny regiony, které jsou aktuálně k dispozici.

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
| Centrální Indie       | cin               |
| Indie – jih         | sin               |
| Švýcarsko - sever   | nch               |
| Švýcarsko – západ    | wch               |
| Francie – jih        | sfr               |
| Východní Asie           | eas               |
| Jihovýchodní Asie     | seas              |
| Spojené arabské emiráty – sever           | nae               |
| Norsko – východ         | eno               |
| Norsko – západ         | wno               |
| Jižní Afrika – západ   | wza               |
| Jižní Afrika – sever  | nza               |

Číslo ostrova je místo, kde je vaše prostředí Lifecycle Services nasazeno v prostředí Service Fabric. V současné době neexistuje žádný způsob, jak tyto informace získat na straně uživatele.

Společnost Microsoft vytvořila uživatelské rozhraní (UI) v Power Apps, abyste mohli získat úplný koncový bod mikroslužby. Více informací najdete v části [Vyhledání koncového bodu služby](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Ověřování

Token zabezpečení platformy se používá k volání veřejného API Viditelnosti zásob. Proto musíte *token Azure Active Directory (Azure AD)* vygenerovat pomocí vaší aplikace Azure AD. Poté musíte token Azure AD použít k získání *přístupového tokenu* od služby zabezpečení.

Společnost Microsoft poskytuje integrovanou kolekci pro získání tokenů *Postman*. Tuto kolekci můžete importovat do svého softwaru *Postman* pomocí následujícího sdíleného odkazu: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Chcete-li získat token služby zabezpečení, postupujte takto:

1. Přihlaste se na portál Azure a použijte jej k vyhledání hodnot `clientId` a `clientSecret` pro vaši aplikaci Dynamics 365 Supply Chain Management.
1. Načtěte token Azure AD (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Metoda:** `GET`
    - **Obsah těla (údaje formuláře):**

        | Klíč           | Hodnota                                            |
        | ------------- | -------------------------------------------------|
        | id klienta     | ${aadAppId}                                      |
        | tajný klíč klienta | ${aadAppSecret}                                  |
        | typ grantu    | client_credentials                               |
        | rozsah         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    V odpovědi byste měli obdržet token Azure AD (`aadToken`). Výsledek by měl vypadat podobně jako v následujícím příkladu.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
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
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Mějte na paměti následující body:

    - Hodnotou `client_assertion` musí být token Azure AD (`aadToken`), který jste obdrželi v předchozím kroku.
    - Hodnota `context` musí být ID prostředí Lifecycle Services, do kterého chcete doplněk nasadit.
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
> Když použijete kolekci požadavků *Postman* k volání veřejných rozhraní API viditelnosti zásob, musíte pro každý požadavek přidat token nositele. Token nositele najdete takto: vyberte kartu **Autorizace** pod adresou URL požadavku, vyberte typ **Token nositele** a zkopírujte přístupový token, který byl načten v posledním kroku. V dalších částech tohoto článku použijete `$access_token` jako token, který byl načten v posledním kroku.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Vytvoření událostí změn ve skladu

Existují dvě rozhraní API pro vytváření událostí skladových změn:

- Vytvoření jednoho záznamu: `/api/environment/{environmentId}/onhand`
- Vytvoření více záznamů: `/api/environment/{environmentId}/onhand/bulk`

Následující tabulka sumarizuje význam každého pole v těle JSON.

| ID pole | Popis |
|---|---|
| `id` | Jedinečné ID pro konkrétní událost změny. Pokud se opakované odeslání provádí kvůli selhání služby, toto ID se používá k zajištění toho, že stejná událost nebude v systému započítána dvakrát. |
| `organizationId` | Identifikátor organizace spojené s událostí. Tato hodnota se mapuje na organizaci nebo ID datové oblasti v Supply Chain Management. |
| `productId` | Identifikátor produktu. |
| `quantities` | Množství, o které se musí změnit skladové množství. Pokud je například do police přidáno 10 nových knih, bude tato hodnota `quantities:{ shelf:{ received: 10 }}`. Pokud budou tři knihy odstraněny z police nebo prodány, bude tato hodnota `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Zdroj dat dimenzí použitých v události změny publikování změny a dotazu. Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat. Viditelnost zásob může konfiguraci dimenze použít k mapování vlastních dimenzí na obecné výchozí dimenze. Pokud není zadána hodnota `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné [základní dimenze](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dynamický pár klíč/hodnota. Hodnoty jsou namapovány na některé dimenze v Supply Chain Management. Můžete však také přidat vlastní dimenze (např .*Zdroj*) k označení, zda událost pochází ze Supply Chain Management nebo z externího systému. |

> [!NOTE]
> Parametry `siteId` a `locationId` tvoří [ konfiguraci oddílu](inventory-visibility-configuration.md#partition-configuration). Proto je musíte zadat v dimenzích, když vytváříte události změny zásob na skladě, nastavujete nebo přepisujete množství v ruce nebo vytváříte události rezervace.

Následující podčásti poskytují příklady, které ukazují, jak tato rozhraní API používat.

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

Následující příklad ukazuje ukázkový obsah těla. V tomto příkladu má společnost systém POS (pokladní místo), který zpracovává transakce v obchodě, a tedy změny zásob. Zákazník vrátil do vašeho obchodu červené tričko. Pro tuto změnu zaúčtujete jednu událost změny pro produkt *Tričko*. Tato událost zvýší množství produktu *T-shirt* o 1.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
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
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Vytvoření více změnových událostí

Toto rozhraní API může vytvářet události změn, stejně jako [rozhraní API pro jednu událost](#create-one-onhand-change-event). Jediný rozdíl je, že toto rozhraní API může vytvářet více záznamů současně. Proto se hodnoty `Path` a `Body` liší. U tohoto API obsahuje `Body` pole záznamů. Maximální počet záznamů je 512. Rozhraní API pro hromadné změny množství na skladě proto může podporovat až 512 událostí změn najednou. 

Například POS v maloobchodě zpracoval následující dvě transakce:

- Jedna vratka jednoho červeného trička
- Jedna prodejní transakce tří černých triček

V tomto případě můžete zahrnout obě aktualizace zásob do jednoho volání API.

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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Nastavení/přepis množství na skladě

API *Set on-hand* přepíše aktuální data pro zadaný produkt. Tato funkce se obvykle používá k aktualizaci počítání zásob. Například během denního počítání zásob může obchod zjistit, že skutečné zásoby červených triček na skladě jsou 100. Proto musí být příchozí množství POS aktualizováno na 100 bez ohledu na to, jaké bylo předchozí množství. Toto rozhraní API můžete použít k přepsání stávající hodnoty.

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

Následující příklad ukazuje ukázkový obsah těla. Chování tohoto rozhraní API se liší od chování těch API, která jsou popsána v části [Vytvoření událostí změn ve skladu](#create-onhand-change-event) dříve v tomto článku. V této ukázce bude množství produktu *T-shirt* nastaveno na 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Vytvoření rezervačních událostí

Chcete-li použít API *Reserve*, musíte zapnout funkci rezervace a dokončit konfiguraci rezervace. Další informace (včetně datového toku a ukázkového scénáře) viz [Konfigurace rezervace (volitelné)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Vytvoření jedné rezervační události

Je možné provést rezervaci proti různým nastavením zdroje dat. Chcete -li konfigurovat tento typ rezervace, nejprve zadejte zdroj dat v parametru `dimensionDataSource`. Poté v parametru `dimensions` zadejte kóty podle nastavení dimenzí v cílovém zdroji dat.

Když zavoláte rezervační rozhraní API, můžete řídit ověření rezervace zadáním logické hodnoty parametru `ifCheckAvailForReserv` v těle požadavku. Hodnota `True` znamená, že je vyžadováno ověření, zatímco hodnota `False` znamená, že ověření není vyžadováno. Výchozí hodnota je typu `True`.

Pokud chcete vrátit rezervaci nebo zrušit rezervaci zadaného množství zásob, nastavte množství na zápornou hodnotu a nastavte parametr `ifCheckAvailForReserv` na `False` pro přeskočení ověření. K dispozici je také vyhrazené nerezervované API, které dělá totéž. Rozdíl je pouze ve způsobu volání těchto dvou API. Je snazší zvrátit konkrétní událost rezervace pomocí `reservationId` s API *unreserve*. Další informace naleznete v části [Zrušit jednu událost rezervace](#reverse-reservation-events).

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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Následující příklad ukazuje úspěšnou odpověď.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Vytvoření více rezervačních událostí

Toto API je hromadná verze [API pro jednu událost](#create-reservation-events).

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

## <a name="reverse-reservation-events"></a>Vrácení událostí rezervace

Rozhraní API *Unreserve* slouží jako operace vrácení pro události [*Rezervace*](#create-reservation-events). Poskytuje způsob, jak vrátit událost rezervace specifikovanou pomocí `reservationId` nebo snížení rezervovaného množství.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Vrátí jednu rezervační událost

Když je vytvořena rezervace, `reservationId` budou zahrnuty v těle odpovědi. Musíte poskytnout stejné `reservationId` ke zrušení rezervaci a zahrnout stejné `organizationId` a `dimensions` použité se pro volání rezervačního API. Nakonec zadejte hodnotu `OffsetQty`, která představuje počet položek, které mají být uvolněny z předchozí rezervace. Rezervace může být buď zcela, nebo částečně stornována v závislosti na specifikaci `OffsetQty`. Například pokud bylo rezervováno *100* jednotek položek, můžete určit `OffsetQty: 10` ke zrušení rezervace *10* z původní rezervované částky.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Následující kód ukazuje příklad obsahu těla.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Následující kód ukazuje příklad těla úspěšné odpovědi.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> V těle odpovědi, kdy `OffsetQty` je menší nebo rovno rezervovanému množství, `processingStatus` bude „*success*“ a `totalInvalidOffsetQtyByReservId` bude *0*.
>
> Pokud je `OffsetQty` větší než rezervovaná částka, `processingStatus` bude „*partialSuccess*“ a `totalInvalidOffsetQtyByReservId` bude rozdíl mezi `OffsetQty` a rezervovaným množstvím.
>
>Například, pokud má rezervace množství *10* a `OffsetQty` má hodnotu *12*, `totalInvalidOffsetQtyByReservId` by bylo *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Vrátí více rezervačních událostí

Toto API je hromadná verze [API pro jednu událost](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Dotaz na zásoby na skladě

Rozhraní API *Query on-hand* (dotaz na zásoby na skladě) se používá k načítání aktuálních skladových dat vašich produktů. Toto rozhraní API můžete použít, kdykoli potřebujete znát skladové zásoby, například když chcete zkontrolovat stav zásob produktů na webu elektronického obchodu nebo když chcete zkontrolovat dostupnost produktu v různých regionech nebo v okolních obchodech a skladech. Toto rozhraní API aktuálně podporuje dotazování až 5000 jednotlivých položek podle hodnoty `productID`. V každém dotazu také může být zadáno více hodnot `siteID` a `locationID`. Maximální limit je definován následující rovnicí:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

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

Doporučujeme použít parametr `groupByValues` k řízení konfigurace pro indexování. Další informace najdete v tématu [Konfigurace hierarchie indexu produktů](./inventory-visibility-configuration.md#index-configuration).

Parametr `returnNegative` určuje, zda výsledky obsahují záporné položky.

> [!NOTE]
> Pokud jste povolili časový plán změn ve skladu a funkce Lze slíbit, váš dotaz může také zahrnovat logický parametr `QueryATP`, který řídí, zda výsledky dotazu obsahují informace funkce Lze slíbit. Další informace a příklady najdete v tématu [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md).

Následující příklad ukazuje ukázkový obsah těla. Ukazuje, že můžete dotazovat na zásoby na skladě z více míst (skladů).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Následující příklad ukazuje, jak dotazovat všechny produkty na konkrétním pracovišti a umístění.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
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

Zde je ukázka adresy URL. Tento GET požadavek je přesně stejný jako ukázka POST, která byla uvedena dříve.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>Přesný dotaz na zásoby na skladě

Přesné dotazy na zásoby na skladě se podobají běžným dotazům na zásoby na skladě, ale umožňují vám určit hierarchii mapování mezi webem a umístěním. Například máte následující dvě lokality:

- Lokalita 1, která je mapována na umístění A
- Lokalita 2, která je mapována na umístění B

Pro běžný dotaz na zásoby na skladě, pokud zadáte `"siteId": ["1","2"]` a `"locationId": ["A","B"]`, Viditelnost inventáře se automaticky dotáže na výsledek pro následující lokality a umístění:

- Lokalita 1, umístění A
- Lokalita 1, umístění B
- Lokalita 2, umístění A
- Lokalita 2, umístění B

Jak vidíte, běžný dotaz na zásoby na skladě nerozpozná, že umístění A existuje pouze na lokalitě 1 a umístění B existuje pouze na lokalitě 2. Proto vytváří nadbytečné dotazy. Chcete-li se přizpůsobit tomuto hierarchickému mapování, můžete použít přesný dotaz a určit mapování umístění v těle dotazu. V tomto případě zadáte dotaz a obdržíte výsledky pouze pro web 1, umístění A a web 2, umístění B.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>Přesný dotaz pomocí metody POST

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

V těle této žádosti, `dimensionDataSource` je volitelný parametr. Pokud není nastaven, s `dimensions` ve `filters` bude zacházeno jako se *základními dimenzemi*. K dispozici jsou čtyři povinná pole pro `filters`: `organizationId`, `productId`, `dimensions`, a `values`.

- `organizationId` by měl obsahovat pouze jednu hodnotu, ale stále je to pole.
- `productId` může obsahovat jednu nebo více hodnot. Pokud je prázdné pole, budou vráceny všechny produkty.
- V poli `dimensions` jsou `siteId` a `locationId` povinné, ale mohou se objevit s dalšími prvky v libovolném pořadí.
- `values` může obsahovat jednu nebo více různých n-tic hodnot odpovídajících `dimensions`.

`dimensions` ve `filters` bude automaticky přidáno do `groupByValues`.

Parametr `returnNegative` určuje, zda výsledky obsahují záporné položky.

Následující příklad ukazuje ukázkový obsah těla.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Následující příklad ukazuje, jak dotazovat všechny produkty na konkrétním pracovišti a umístění.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Lze slíbit (ATP)

Viditelnost zásob vám umožní naplánovat budoucí změny ve skladu a vypočítat množství, které lze slíbit. ATP (Lze slíbit) je množství položky, které je k dispozici a může být odběrateli přislíbena v příštím období. Použití výpočtu ATP může výrazně zvýšit vaši schopnost plnění objednávky. Informace o tom, jak povolit tuto funkci a jak interagovat s Viditelností zásob prostřednictvím jejího rozhraní API po aktivaci funkce, naleznete v tématu [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Přidělení

API související s přidělením se nacházejí v [přidělování Viditelnosti zásob](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
