---
title: Doplněk Viditelnost zásob
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114663"
---
# <a name="inventory-visibility-add-in"></a>Doplněk Viditelnost zásob

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Doplněk Viditelnost zásob je nezávislá a vysoce škálovatelná mikroslužba, která umožňuje sledování zásob na skladě v reálném čase, a tím poskytuje globální pohled na viditelnost zásob.

Všechny informace, které se vztahují k zásobám na skladě, se do služby exportují téměř v reálném čase prostřednictvím nízkoúrovňové integrace SQL. Externí systémy přistupují ke službě prostřednictvím rozhraní API RESTful a dotazují se na praktické informace o daných sadách dimenzí, čímž získávají seznam dostupných pozic.

Viditelnost zásob je mikroslužba postavená na Microsoft Dataverse, což znamená, že ji můžete rozšířit pomocí vytváření Power Apps a použitím Power BI, a poskytovat přizpůsobené funkce pro splnění vašich obchodních požadavků. Je také možné upgradovat index za účelem provádění dotazů na zásoby.

Viditelnost zásob poskytuje možnosti konfigurace, které umožňují její integraci s více systémy třetích stran. Podporuje standardizovanou dimenzi zásob, přizpůsobitelnou rozšiřitelnost a standardizované, konfigurovatelné vypočítané množství.

Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management a jak používat jeho aplikační programovací rozhraní (API).

## <a name="install-the-inventory-visibility-add-in"></a>Instalace doplňku Viditelnost zásob

Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS). LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich aplikací Dynamics 365 Finance and Operations.

Další informace naleznete v tématu [Zdroje Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Předpoklady

Před instalací doplňku Viditelnost zásob musíte provést následující:

- Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.
- Vygenerujte beta klíče pro vaši nabídku v LCS.
- Povolte beta klíče pro vaši nabídku pro uživatele v LCS.
- Kontaktujte produktový tým doplňku Viditelnost zásob společnosti Microsoft a sdělte jim ID prostředí, kam chcete nasadit doplněk Viditelnost zásob.

Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Instalace doplňku

Pro instalaci doplňku Viditelnost zásob proveďte následující:

1. Přihlaste se k portálu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.
1. Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.
1. Na stránce prostředí přejděte dolů, dokud neuvidíte sekci **Doplňky prostředí**. Pokud sekce není viditelná, ujistěte se, že byly plně zpracovány nezbytné beta klíče.
1. V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.
    ![Stránka prostředí v LCS](media/inventory-visibility-environment.png "Stránka prostředí v LCS")
1. Vyberte odkaz **Nainstalovat nový doplněk**. Otevře se seznam dostupných doplňků.
1. Vyberte ze seznamu **Služba zásob**. (Upozorňujeme, že toto může být nyní uvedeno jako **Doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management**.)
1. Zadejte hodnoty pro následující pole pro vaše prostředí:

    - **ID aplikace AAD**
    - **ID klienta AAD**

    ![Stránka nastavení doplňku](media/inventory-visibility-setup.png "Stránka nastavení doplňku")

1. Odsouhlaste smluvní podmínky výběrem zaškrtávacího políčka **Smluvní podmínky**.
1. Vyberte **Instalovat**. Stav doplňku se zobrazí jako **Probíhá instalace**. Po dokončení obnovte stránku, aby se zobrazila změna stavu **Nainstalováno**.

### <a name="get-a-security-service-token"></a>Získání tokenu služby zabezpečení

Token služby zabezpečení získáte takto:

1. Přihlaste se na Azure Portal a použijte jej k vyhledání `clientId` a `clientSecret` pro vaši aplikaci Supply Chain Management.
1. Načtěte token Azure Active Directory (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Metoda** - `GET`
    - **Obsah těla (údaje formuláře)**:

        | klíč | hodnota |
        | --- | --- |
        | id klienta | ${aadAppId} |
        | tajný klíč klienta | ${aadAppSecret} |
        | typ grantu | client_credentials |
        | prostředek | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Měli byste obdržet `aadToken` v odpovědi, která se podobá následujícímu příkladu.

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

1. Formulujte požadavek JSON, který se podobá následujícímu:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Kde:
    - Hodnota `client_assertion` musí být `aadToken`, který jste obdrželi v předchozím kroku.
    - Hodnota `context` musí být ID prostředí, do kterého chcete doplněk nasadit.
    - Nastavte všechny ostatní hodnoty, jak je znázorněno v příkladu.

1. Odešlete požadavek HTTP s následujícími vlastnostmi:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **Metoda** - `POST`
    - **Záhlaví HTTP** - Zahrňte verzi API (klíč je `Api-Version` a hodnota je `1.0`)
    - **Obsah těla** - Zahrňte požadavek JSON, který jste vytvořili v předchozím kroku.

1. V odpovědi získáte `access_token`. To je to, co potřebujete jako nosný token pro volání rozhraní API doplňku Viditelnost zásob. Následuje příklad.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Odinstalace doplňku

Chcete-li doplněk odinstalovat, vyberte **Odinstalovat**. Obnovte LCS a doplněk Viditelnost zásob bude odebrán. Proces odinstalace odebere registraci doplňku a také spustí úlohu k vyčištění všech obchodních dat uložených ve službě.

## <a name="inventory-visibility-add-in-public-api"></a>Veřejné rozhraní API doplňku Viditelnosti zásob

Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů integrace. Podporuje tři hlavní typy interakce:

- Odesílání změn zásob na skladě do doplňku z externího systému.
- Dotazování na aktuální množství zásob na skladě z externího systému.
- Automatická synchronizace se zásobami na skladě v Supply Chain Management.

Automatická synchronizace není součástí veřejného API, ale místo toho se zpracovává na pozadí pro prostředí, která mají povolený doplněk Viditelnost zásob.

### <a name="authentication"></a>Ověřování

Token zabezpečení platformy se používá k volání doplňku Viditelnost zásob, takže musíte vygenerovat token Azure Active Directory pomocí vaší aplikace Azure Active Directory.

Další informace o tom, jak získat token zabezpečení, najdete v části [Instalace doplňku Viditelnost zásob](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Konfigurace rozhraní API doplňku Viditelnost zásob

Před použitím služby musíte dokončit konfigurace popsané v následujících pododdílech. Konfigurace se může lišit v závislosti na podrobnostech vašeho prostředí. Obsahuje primárně čtyři části:

- [Rozdělení](#partitioning)
- [Konfigurace dimenzí](#dimension-configurations)
- [Indexace](#indexing)
- [Vlastní měrné systémy](#custom-measurement)

#### <a name="partitioning"></a>Rozdělení

Rozdělení může významně ovlivnit výkonnost rozhraní API doplňku Viditelnost zásob. Je vhodné definovat schéma, které umožňuje malá seskupení dat a přitom umožňuje smysluplné dotazy na data.

`organizationId` (`dataAreaId` v Supply Chain Management) bude vždy součástí rozdělení a ve výchozím nastavení je Viditelnost zásob nastavena na rozdělení podle dimenzí jako *Pracoviště + skladové místo*. To znamená, že služba musí být vždy dotazována s těmito dimenzemi definovanými na filtrech.

> [!NOTE]
> *Pracoviště* a *Skladové místo* jsou dvě obecné výchozí dimenze ve Viditelnosti zásob. V aplikaci Supply Chain Management se tyto dimenze nazývají *Pracoviště* (`InventSiteId`) a *Sklad* (`InventLocationId`).

### <a name="dimension-configurations"></a>Konfigurace dimenzí

Viditelnost zásob poskytne seznam obecných výchozích dimenzí umožňujících integraci více zdrojových systémů.

V následující tabulce jsou uvedeny dimenze zásob, které budou výchozími názvy dimenzí v doplňku Viditelnost zásob.

| Typ dimenze | Název dimenze |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Sledování | `BatchId` |
| Sledování | `SerialId` |
| Skladové místo | `LocationId` |
| Skladové místo | `SiteId` |
| Stav zásob | `StatusId` |
| Specifické pro sklad | `WMSLocationId` |
| Specifické pro sklad | `WMSPalletId` |
| Specifické pro sklad | `LicensePlateId` |

> [!NOTE]
> Typ dimenze uvedený v předchozí tabulce slouží pouze pro informaci. V doplňku Viditelnost zásob není nutné definovat typ dimenze.

Pokud vlastní dimenze existuje a je třeba ji přepnout na výchozí hodnotu, když je spotřebována doplňkem Viditelnost zásob, můžete nakonfigurovat název **Vlastní dimenze** v doplňku Viditelnost zásob.

Externí systémy přistupují k doplňku Viditelnost zásob prostřednictvím rozhraní RESTful API, která umožňují dotazování na informace o dostupnosti na skladě u daných sad dimenzí. Pro integraci vám doplněk Viditelnost zásob umožňuje konfigurovat *externí zdroj dat kanálu* a zdrojovou dimenzi do *cílových dimenzí* v doplňku Viditelnost zásob.

Cílové dimenze by měly být jednou z následujících:

- Výchozí dimenze v doplňku Viditelnost zásob
- Vlastní dimenze

Účelem konfigurace dimenze je standardizovat integraci více systémů pro dotazování na dimenzích a publikování události s dimenzemi.

#### <a name="indexing"></a>Indexace

Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni, ale možná budete chtít vidět výsledky agregované na základě dimenzí zásob.

Viditelnost zásob poskytuje flexibilitu tím, že umožňuje nastavit indexy, které jsou založeny na dimenzi nebo kombinaci dimenzí.

> [!NOTE]
> V současné době můžete indexy nakonfigurovat pouze na maximálně pět. Před implementací musíte pečlivě zvážit, kterou dimenzi nebo kombinaci dimenzí použijete, abyste zajistili, že bude vyhovovat vašim obchodním potřebám. Chcete-li se například dotazovat na produkty následujícím způsobem:

- Dotazujte se na agregované zásoby na skladě produktu podle dimenzí *Barva* a *Velikost*.
- V některých případech se chcete pouze dotazovat na produkt celkem.

Měli byste dva indexy definované následovně:

- `["ColorId", "SizeId"]`
- `[]`

Prázdná závorka se agreguje na základě ID produktu v oddílu.

Indexování definuje, jak můžete seskupit výsledky na základě nastavení dotazu `groupBy`. V tomto případě, pokud nedefinujete žádné hodnoty `groupBy`, získáte součty `productid`. Jinak pokud definujete `groupBy` jako `groupBy=ColorId&groupBy=SizeId`, vrátí se vám více řádků na základě různých kombinací barev a velikostí v systému.

Kritéria dotazu můžete zadat do textu požadavku.

Zde je ukázkový dotaz na produkt s kombinací barev a velikostí.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Vlastní měrné systémy

Výchozí množství měrného systému jsou propojena se Supply Chain Management, můžete však chtít mít množství, které je tvořeno kombinací výchozích měrných systémů. Chcete-li to provést, můžete mít konfiguraci vlastních množství, která budou přidána k výstupu dotazů na zásoby na skladě.

Funkce jednoduše umožňuje definovat sadu měrných systémů, které budou přidány, anebo sadu měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.

Například s následující podmínkou dotazu nakonfigurujete vlastní množství měrné jednotky jako `MyCustomAvailableforReservation`, která má být spotřebována systémem spotřeby.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Systém spotřeby | Vypočtené měrné jednotky | Zdroj dat | Modifikátor | Typ výpočtu modifikátoru |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Sčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Sčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Odčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Sčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Odčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Sčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Sčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Odčítání |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Odčítání |

Takto dotaz na vlastní množství měrnou jednotku vrátí následující výstup.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Výstup `MyCustomAvailableforReservation` je založen na nastavení výpočtu ve vlastních měrných systémech jako:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Publikování změn množství na skladě

Přesná adresa URL, na kterou bude událost publikována, bude záviset na vaší zeměpisné oblasti. Bude mít formu:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Po ověření lze tuto adresu URL použít společně s metodou HTTP `POST` pro odesílání událostí změny zásob na skladě do služby.

Pro komunikaci se službami Dynamics 365 prostřednictvím požadavků HTTP se používá speciální záhlaví, které označuje ID prostředí instance Supply Chain Management, ke které jsou data propojena. Například:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Zveřejnění dotazu na změny zásob na skladě - příklad 1

Tento příklad ukazuje scénář, ve kterém nastavíte konfiguraci dimenze v Power Apps.

Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze. Systém automaticky převede vlastní dimenze na základní dimenze.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Zveřejnění dotazu na změny zásob na skladě - příklad 2

Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze. Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` hodnotu null, je prázdné nebo má mezeru.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>Vlastnosti pole dokumentu JSON

Pole z dříve poskytnutých příkladů dotazů JSON mají vlastnosti uvedené v následující tabulce.

| ID pole | popis |
|---|---|
| `id` | Jedinečné ID pro konkrétní událost změny. Toto ID se používá k zajištění toho, že pokud komunikace se službou během publikování selže, opětovné odeslání události nebude mít za následek, že se v systému dvakrát započítá stejná událost. |
| `organizationId` | Identifikátor organizace spojené s událostí. To se mapuje na organizace Supply Chain Management nebo ID datové oblasti. |
| `productId` | Identifikátor daného produktu. |
| `quantity` | Množství, o které je třeba změnit zásoby na skladě. Pokud by bylo například na polici přidáno 10 nových housek, byla by tato hodnota 10. Pokud by pak byly 3 housky odebrány z police nebo prodány, byla by tato hodnota -3. |
| `dimensionDataSource` | Zdroj dat dimenzí použitých v události změny publikování změny a dotazu. Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat. S konfigurací dimenzí může Viditelnost dat mapovat vlastní dimenze na obecné výchozí dimenze. Pokud není zadán `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné výchozí dimenze.   |
| `dimensions` | Dynamická sada párů klíč/hodnota. Budou mapovány na některé dimenze v Supply Chain Management, ale můžete také přidat vlastní dimenze (jako *Zdroj*), což může naznačovat, že událost pocházela ze Supply Chain Managementu nebo externího systému. |

### <a name="querying-current-on-hand"></a>Dotaz na aktuální zásoby na skladě

Koncový bod pro dotazování na aktuální zásoby na skladě bude mít podobnou adresu URL:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Bude dotazován pomocí metody HTTP `POST`.

#### <a name="current-on-hand-query-example-1"></a>Dotaz na aktuální zásoby na skladě - příklad 1

Tento příklad ukazuje scénář, ve kterém jste dokončili konfiguraci dimenze v Power Apps.

Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze. Systém automaticky převede vlastní dimenze na základní dimenze. Můžete určit `DimensionDataSource` v `filters` a zadat vlastní dimenze v `filters` i `groupByValues`. Systém automaticky převede vlastní dimenze na základní dimenze.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Dotaz na aktuální zásoby na skladě - příklad 2

Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze. Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` pod `filters` hodnotu null nebo mezeru.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Příklad výsledku vrácení

Dotazy zobrazené v předchozích příkladech by mohly vrátit takový výsledek.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Všimněte si, že pole množství jsou strukturována jako slovník měrných jednotek a jejich přidružených hodnot.
