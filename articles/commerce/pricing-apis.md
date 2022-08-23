---
title: Rozhraní API pro naceňování v Commerce
description: Tento článek popisuje různá rozhraní API pro naceňování, která jsou poskytována modulem naceňování Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294108"
---
# <a name="commerce-pricing-apis"></a>Rozhraní API pro naceňování v Commerce

[!include [banner](../includes/banner.md)]

Tento článek popisuje různá rozhraní API pro naceňování, která jsou poskytována modulem naceňování Microsoft Dynamics 365 Commerce.

Modul naceňování Dynamics 365 Commerce poskytuje následující rozhraní API maloobchodního serveru, která mohou využívat externí aplikace pro podporu různých cenových scénářů:

- **GetActivePrices** – Toto API získá vypočítanou cenu produktu, včetně jednoduchých slev.
- **CalculateSalesDocument** – Toto API vypočítává ceny a slevy pro produkty v daném množství, pokud jsou nakupovány společně.
- **GetAvailablePromotions** – Toto API získává příslušné slevy na produkty v košíku. 
- **AddCoupons** – Toto rozhraní API přidává kupóny do košíku.
- **RemoveCoupons** – Toto rozhraní API odstraňuje kupóny z košíku.

Další informace o tom, jak používat maloobchodní serverová API v externích aplikacích, najdete v tématu [Používání maloobchodních serverových API v externích aplikacích](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

Rozhraní API *GetActivePrices* bylo představeno ve verzi Commerce 10.0.4. Toto API získá vypočítanou cenu produktu, včetně jednoduchých slev. Nepočítá víceřádkové slevy a předpokládá, že každý produkt v požadavku API má množství 1. Toto API může také brát jako vstup seznam produktů a hromadně se dotazovat na cenu jednotlivých produktů.

API *GetActivePrices* podporuje role v Commerce **Zaměstnanec**, **Zákazník**, **Anonymní** a **Aplikace**.

Hlavní případ použití pro API *GetActivePrices* je stránka s údaji o produktu (PDP), kde chtějí maloobchodníci prezentovat nejlepší cenu za produkt, včetně všech účinných slev.

Následující tabulka ukazuje vstupní parametry pro API *GetActivePrices*.

| Jméno                                    | Podnázev | Typ | Povinné/volitelné | Popis |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Povinný | |
|                                         | ChannelId | long | Povinný | |
|                                         | CatalogId | long | Povinný | |
| productIds                              | | IEnumerable\<long\> | Povinný | Seznam produktů, pro které se mají vypočítat ceny. |
| activeDate                              | | DateTimeOffset | Povinný | Datum, kdy se počítají ceny. |
| customerId                              | | řetězec | Volitelné | Číslo účtu zákazníka. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Volitelné | Věrnostní úrovně. |
|                                         | AffiliationId | long | Povinný | Věrnostní ID. |
|                                         | LoyaltyTierId | long | Volitelné | ID věrnostní úrovně. |
| includeSimpleDiscountsInContextualPrice | | bool | Volitelné | Nastavte tento parametr na **true**, chcete-li zahrnout jednoduché slevy do kalkulace ceny. Výchozí hodnota je **false**. |
| includeVariantPriceRange                | | bool | Volitelné | Nastavte tento parametr na **true**, chcete-li získat minimální a maximální ceny mezi všemi variantami hlavního produktu. Výchozí hodnota je **false**. |
| includeAttainablePricesAndDiscounts     | | bool | Volitelné | Nastavte tento parametr na **true**, chcete-li získat dostupné ceny a slevy. Výchozí hodnota je **false**. |

**Ukázkový text požadavku**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Ukázkový text odpovědi**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

Rozhraní API *CalculateSalesDocument* bylo představeno ve verzi Commerce 10.0.25. Toto API vypočítává ceny a slevy pro produkty v daném množství, pokud jsou nakupovány společně v objednávce. Cenová kalkulace za rozhraním API *CalculateSalesDocument* bere v úvahu jak jednořádkové slevy, tak víceřádkové slevy.

Hlavní případ použití pro API *CalculateSalesDocument* je kalkulace ceny ve scénářích, kdy celý kontext košíku netrvá (jako jsou prodejní nabídky). Scénáře v místě prodeje (POS) a elektronickém obchodování Commerce mohou také těžit z tohoto případu použití. Nižší celková cena, když se položky košíku počítají jako sada (například u samostatných balíčků, propojených nebo doporučených produktů nebo produktů, které již byly přidány do košíku), může zákazníky přesvědčit, aby přidali produkty do košíku.

Datový model pro požadavek i odpověď API *CalculateSalesDocument* je **Košík**. V kontextu tohoto API je však datový model pojmenován **SalesDocument**. Protože většina vlastností je volitelná a pouze několik z nich ovlivňuje výpočet ceny, jsou v následující tabulce zobrazena pouze pole související s cenou. Nedoporučujeme, aby byla do požadavku API zapojena jakákoli další pole.

Rozsah API *CalculateSalesDocument* je jen výpočet cen a slev. Daně a poplatky se nezapojují.

Následující tabulka ukazuje vstupní parametry uvnitř pojmenovaného objektu s názvem **salesDocument**.

| Jméno             | Podnázev | Typ | Povinné/volitelné | Popis |
|------------------|----------|------|-------------------|-------------|
| ID               | | řetězec | Povinný | Identifikátor prodejního dokumentu. |
| CartLines        | | IList\<CartLine\> | Volitelné | Seznam řádků, pro které se mají vypočítat ceny a slevy. |
|                  | ID produktu | long | Vyžadováno v oboru CartLine | ID záznamu produktu. |
|                  | ItemId | řetězec | Volitelné | Identifikátor položky. Pokud je zadána hodnota, musí odpovídat hodnotě parametru **ProductId**. |
|                  | InventoryDimensionId | řetězec | Volitelné | Identifikuje identifikátor dimenze. Pokud je zadána hodnota, kombinace hodnot **ItemId** a **InventoryDimensionId** se musí shodovat s hodnotou parametru **ProductId**. |
|                  | Množství | desetinné číslo | Vyžadováno v oboru CartLine | Množství produktu. |
|                  | UnitOfMeasureSymbol | řetězec | Volitelné | Jednotka produktu. Pokud není zadána hodnota, rozhraní API ve výchozím nastavení použije prodejní jednotku produktu. |
| CustomerId       | | řetězec | Volitelné | Číslo účtu zákazníka. |
| LoyaltyCardId    | | řetězec | Volitelné | Identifikátor věrnostní karty. Jakýkoli zákaznický účet spojený s věrnostní kartou musí odpovídat hodnotě parametru **CustomerId** (pokud je zadán). Pokud věrnostní karta nebude nalezena nebo její stav je **Blokováno**, nebude brána v úvahu. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Volitelné | Řádky věrnostní úrovně. Pokud jsou uvedeny hodnoty **CustomerId** nebo **LoyaltyCardId**, budou odpovídající řádky věrnostní úrovně sloučeny s řádky, které jsou poskytovány v hodnotě **AffiliationLines**. |
|                  | AffiliationId | long | Vyžadováno v oboru AffiliationLoyaltyTier | ID záznamu věrnostního programu. |
|                  | LoyaltyTierId | long | Vyžadováno v oboru AffiliationLoyaltyTier | ID záznamu věrnostní úrovně. |
|                  | AffiliationTypeValue | int | Vyžadováno v oboru AffiliationLoyaltyTier | Hodnota, která udává, zda je řádek věrnostního programu typu **Obecný** (**0**), nebo **Věrnostní** (**1**). Pokud je tento parametr nastaven na **0**, rozhraní API přebírá hodnotu **AffiliationId** jako identifikátor a ignoruje hodnotu **LoyaltyTierId**. Pokud je nastaven na **1**, rozhraní API přebírá hodnotu **LoyaltyTierId** jako identifikátor a ignoruje hodnotu **AffiliationId**. |
|                  | ReasonCodeLines | Kolekce\<ReasonCodeLine\> | Vyžadováno v oboru AffiliationLoyaltyTier | Řádky kódu důvodu. Tento parametr nemá žádný vliv na výpočet ceny, ale je vyžadován jako součást objektu **AffiliationLoyaltyTier**. |
|                  | CustomerId | řetězec | Vyžadováno v oboru AffiliationLoyaltyTier | Číslo účtu zákazníka. |
| Kupóny          | | IList\<Coupon\> | Volitelné | Kupony, které nelze použít (neaktivní, s vypršenou platností nebo nenalezené), nebudou při výpočtu ceny zohledněny. |
|                  | Kód | řetězec | Vyžadováno v oboru Coupon | Kód kupónu. |
|                  | CodeId | řetězec | Volitelné | Identifikátor kódu kupónu. Pokud je zadána hodnota, musí odpovídat hodnotě parametru **Code**. |
|                  | DiscountOfferId | řetězec | Volitelné | Identifikátor slevy. Pokud je zadána hodnota, musí odpovídat hodnotě parametru **Code**. |

**Ukázkový text požadavku**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Jako text odpovědi se vrátí celý objekt košíku. Chcete-li zkontrolovat ceny a slevy, měli byste se zaměřit na pole v následující tabulce.

| Jméno           | Podnázev | Typ | Popis |
|----------------|----------|------|--------------|
| NetPrice       | | desetinné číslo | Čistá cena celého prodejního dokladu před uplatněním slev. |
| DiscountAmount | | desetinné číslo | Celková částka slevy v celém prodejním dokladu. |
| TotalAmount    | | desetinné číslo | Celková částka celého prodejního dokladu. |
| CartLines      | | IList\<CartLine\> | Vypočítané řádky, které obsahují údaje o ceně a slevě. |
|                | Cena | desetinné číslo | Jednotková cena produktu. |
|                | NetPrice | desetinné číslo | Čistá cena řádku před uplatněním slev (= *cena* &times; *množství*). |
|                | DiscountAmount | desetinné číslo | Částka slevy. |
|                | TotalAmount | desetinné číslo | Konečný výsledek celkové ceny řádku. |
|                | PriceLines | IList\<PriceLine\> | Údaje o ceně včetně zdroje ceny (základní cena, úprava ceny nebo obchodní dohoda) a částky. |
|                | DiscountLines | IList\<DiscountLine\> | Údaje o slevě. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Pokud má košík několik řádků, API *GetAvailablePromotions* vrátí všechny příslušné slevy pro řádky košíku. 

Hlavní případ použití pro API *GetAvailablePromotions* je stránka košíku, kde chtějí prodejci prezentovat uplatněné slevy nebo dostupné kupóny pro aktuální košík.

Následující tabulka ukazuje vstupní parametry pro API *GetAvailablePromotions*.

| Jméno        | Typ | Povinné/volitelné | Popis |
|-------------|------|-------------------|-------------|
| klíč         | řetězec | Povinný | ID košíku. |
| cartLineIds | IEnumerable\<string\> | Volitelné | Nastavením tohoto parametru vrátíte slevy pouze na vybrané řady košíku. |

**Ukázkový text odpovědi**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

Rozhraní API *AddCoupons* podporuje přidání seznamu kupónů do košíku. Po přidání kupónů vrátí objekt košíku.

Následující tabulka ukazuje vstupní parametry pro API *AddCoupons*.

| Jméno                 | Typ | Povinné/volitelné | Popis |
|----------------------|------|-------------------|-------------|
| klíč                  | řetězec | Povinný | ID košíku. |
| couponCodes          | IEnumerable\<string\> | Povinný | Kódy kuponů pro přidání do košíku. |
| isLegacyDiscountCode | bool | Volitelné | Nastavte tento parametr na **true** k označení, že kupon je starší slevový kód. Výchozí hodnota je **false**. |

## <a name="removecoupons"></a>RemoveCoupons

Rozhraní API *RemoveCoupons* podporuje odstranění seznamu kupónů z košíku. Po odebrání kupónů vrátí objekt košíku.

Následující tabulka ukazuje vstupní parametry pro API *RemoveCoupons*.

| Jméno        | Typ | Povinné/volitelné | Popis |
|-------------|------|-------------------|-------------|
| klíč         | řetězec | Povinný | ID košíku. |
| couponCodes | IEnumerable\<string\> | Povinný | Kódy kuponů pro odebrání z košíku. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
