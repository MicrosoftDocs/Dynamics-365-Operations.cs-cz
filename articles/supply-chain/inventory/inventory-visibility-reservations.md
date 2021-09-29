---
title: Rezervace viditelnosti zásob
description: Toto téma popisuje, jak nastavit funkci rezervace tak, aby vytvářela rezervace, spotřebovávala rezervace a/nebo obnovovala zadaná množství zásob pomocí Viditelnosti zásob.
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
ms.openlocfilehash: 4a85520c0911bb7eed5842b3fd5bd706009351e5
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500348"
---
# <a name="inventory-visibility-reservations"></a>Rezervace viditelnosti zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Toto téma popisuje, jak nastavit funkci rezervace tak, aby vytvářela rezervace, spotřebovávala rezervace a/nebo obnovovala zadaná množství zásob pomocí Viditelnosti zásob.

Rezervace označují množství zásob, které budou použity v budoucnosti. Když vytvoříte rezervaci, systém zabrání ostatním objednávkám v rezervaci nebo konzumaci rezervovaného zboží, dokud rezervace nebude spotřebována nebo bez výhrad. Rezervace se vytvářejí, spotřebovávají a ruší pomocí volání API ke službě Viditelnost zásob.

Volitelně můžete nastavit Microsoft Dynamics 365 Supply Chain Management (a další systémy třetích stran) k automatickému vyrovnání množství, které bylo rezervováno pomocí Viditelnosti zásob. Množství vyrovnání je odstraněno ze záznamů rezervací ve Viditelnosti zásob.

Když zapnete funkci rezervace, Supply Chain Management se automaticky připraví na vyrovnání rezervací provedených pomocí Viditelnosti zásob.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Zapnutí a nastavení funkce rezervace

Chcete-li funkci rezervace zapnout, postupujte následujícím způsobem.

1. přihlaste se do Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Správa funkcí** zapněte funkci *OnHandReservation*.
1. Přihlaste se k aplikaci Supply Chain Management.
1. Jděte na **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** pracovního prostoru a povolte funkci *Integrace viditelnosti zásob s posunem rezervace* (vyžaduje verzi 10.0.22 nebo novější).
1. Jděte na **Řízení zásob \> Nastavení \> Parametry integrace viditelnosti zásob**, otevřete kartu **Ofset rezervace** a vytvořte následující nastavení:
    - **Povolit posun rezervace** - Nastavením na *Ano* povolíte tuto funkci.
    - **Modifikátor ofsetu rezervace** - Vyberte stav transakce zásob, který bude kompenzovat rezervace provedené ve službě Viditelnost zásob. Toto nastavení určuje fázi zpracování objednávky, která spouští offsety. Fáze je sledována podle stavu transakcí zásob objednávky. Vyberte jednu z následujících možností:
        - *Při objednávce* - Pro stav *Při transakci* objednávka odešle po vytvoření požadavek na vyrovnání. Ofsetové množství bude množství vytvořené objednávky.
        - *Rezervovat* - Pro stav *Rezervovat objednanou transakci* objednávka odešle požadavek na vyrovnání, pokud je rezervována, vyskladněna, zaúčtována dodacím listem nebo fakturována. Požadavek bude spuštěn pouze jednou, v prvním kroku, když nastane zmíněný proces. Ofsetové množství bude množství, ze kterého se změnil stav transakce zásob *V pořadí* na *Rezervováno objednáno* (nebo pozdější stav) na příslušném řádku objednávky.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Použijte funkci rezervace ve Viditelnosti zásob

Když zavoláte rezervační rozhraní API, systém označí rezervaci zadaného zboží a množství. Musíte definovat hierarchii rezervací a odesílat žádosti, které odpovídají této hierarchii rezervací. Rezervaci lze provést přímo voláním rezervačních rozhraní API.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurujte hierarchii rezervací

Hierarchie rezervací popisuje posloupnost dimenzí, které je třeba zadat při vytváření rezervace. Funguje stejným způsobem, jako funguje hierarchie indexů pro dotazy na zásoby na skladě.

Hierarchie rezervací se může lišit od hierarchie indexu. Tato nezávislost vám umožňuje implementovat správu kategorií, kde mohou uživatelé rozdělit dimenze na detaily a specifikovat požadavky, aby vytvářeli přesnější rezervace.

Konfigurace hierarchie měkkých rezervací v Power Apps otevřete stránku **Konfigurace** a poté na kartě **Měkká hierarchie rezervací** nastavte hierarchii rezervací přidáním a/nebo úpravou dimenzí a jejich úrovní hierarchie.

Vaše hierarchie měkkých rezervací by měla obsahovat `SiteId` a `LocationId` jako součásti, protože vytvářejí konfiguraci oddílu.

Další informace o způsobu konfigurace rezervací naleznete v tématu [Konfigurace rezervací](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Zavolejte rezervační rozhraní API

Rezervace se provádějí ve službě Viditelnost zásob odesláním požadavku POST na adresu URL služby, jako je například `/api/environment/{environment-ID}/onhand/reserve`.

U rezervace musí orgán žádosti obsahovat ID organizace, ID produktu, rezervovaná množství a rozměry. Požadavek generuje jedinečné ID rezervace pro každý záznam rezervace. Záznam rezervace obsahuje jedinečnou kombinaci ID produktu a dimenzí.

Když zavoláte rezervační rozhraní API, můžete řídit ověření rezervace zadáním logické hodnoty parametru `ifCheckAvailForReserv` v těle požadavku. Hodnota `True` znamená, že je vyžadováno ověření, zatímco hodnota `False` znamená, že ověření není vyžadováno. Výchozí hodnota je typu `True`.

Pokud chcete zrušit rezervaci nebo zrušit rezervaci zadaného množství zásob, nastavte množství na zápornou hodnotu a nastavte parametr `ifCheckAvailForReserv` na `False` pro přeskočení ověření.

Zde je příklad textu požadavku pro referenci.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Vyrovnání rezervacví v Supply Chain Management

U stavů transakcí zásob, které obsahují zadaný modifikátor vyrpvnání rezervace, aktualizace transakce vyrovná odpovídající záznam rezervace, pokud jsou splněny všechny následující podmínky:

- ID rezervace u transakce zásob odpovídá ID rezervace záznamu rezervace ve službě Viditelnost zásob.
- Dimenze transakce zásob je identická s dimenzemi záznamu rezervace ve službě Viditelnost zásob.
- Změny stavu transakcí zásob aktivují vyrovnání rezervací, když stav transakcí zásob odráží skutečnost, že zpracování objednávky bylo dokončeno nebo přeskočeno.

Množství vyrovnání následuje po množství zásob, které je uvedeno v transakcích zásob. Vyrovnání se neprojeví, pokud ve službě Viditelnost zásob nezůstane žádné rezervované množství.

### <a name="set-up-the-reservation-offset-modifier"></a>Nastavte modifikátor vyrovnání rezervace

Pokud jste to ještě neudělali, nastavte modifikátor rezervace podle popisu v tématu [Zapnutí a nastavení funkce rezervace](#turn-on).

### <a name="set-up-reservation-ids"></a>Nastavení ID rezervací

ID rezervace jedinečně označuje záznam rezervace ve Viditelnosti zásob. V Supply Chain Management uživatelé zadávají rezervace na řádky objednávky, aby označili vyrovnání pro odpovídající záznam rezervace.

Chcete-li nastavit ID rezervace v Supply Chain Management, postupujte takto.

1. Otevřete prodejní objednávku (například ze stránky **Všechny prodejní objednávky**).
1. Na pevné záložce **Řádky prodejní objednávky** vyberte řádek objednávky.
1. Na pevné záložce **Řádky prodejní objednávky** na panelu nástrojů vyberte **Aktualizovat řádek \> Zásoby \> Integrace viditelnosti zásob**.
1. Zadejte příslušná ID rezervace.

Změna stavu zásob odpovídá nastavení modifikátoru vyrovnání.
