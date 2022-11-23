---
title: Rezervace v Inventory Visibility
description: Tento článek popisuje, jak nastavit funkci rezervace tak, aby vytvářela rezervace, spotřebovávala rezervace a/nebo obnovovala zadaná množství zásob pomocí Viditelnosti zásob.
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
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762715"
---
# <a name="inventory-visibility-reservations"></a>Rezervace v Inventory Visibility

[!include [banner](../includes/banner.md)]

Tento článek popisuje typický případ použití pro předběžné rezervace a vysvětluje, jak je nastavit ve viditelnosti inventáře. Obsahuje informace o tom, jak vytvořit předběžné rezervace, kompenzovat je při fyzické spotřebě a upravit nebo zrušit rezervaci specifikovaných zásob.

## <a name="sample-use-case-for-soft-reservation"></a>Ukázkový případ použití pro předběžnou rezervaci

Předběžné rezervace pomáhají organizacím získat jediný zdroj pravdy pro dostupné zásoby, zejména během procesu plnění objednávek. Tato funkce je užitečná pro organizace, kde existují následující podmínky:

- Organizace má alespoň dva různé systémy, které přímo přijímají odchozí objednávky.
- Organizace je velmi přísná a chce zabránit dvojímu zaúčtování zásob produktů, ke kterému může dojít, pokud je více systémů schopno nadměrně rezervovat poslední kus na skladě. Této situaci lze předejít, když všechny objednávkové systémy mohou provádět okamžitá volání rozhraní API pro předběžné rezervace do viditelnosti zásob, což poskytuje jediný zdroj pravdy o dostupnosti zásob.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Předběžná rezervace ve Viditelnosti zásob" width="720" />](media/inventory-visibility-soft-reservation.png)

Předchozí obrázek ukazuje, jak funguje předběžná rezervace, a zdůrazňuje následující operace:

- Vaše počáteční úroveň zásob se synchronizuje s viditelností zásob z Microsoft Dynamics 365 Supply Chain Management.
- Předběžné rezervace jsou odesílány z každého z vašich objednávkových kanálů nebo systémů do viditelnosti zásob. Viditelnost zásob ověřuje dostupnost zásob a pokouší se provést předběžnou rezervaci. Pokud je předběžná rezervace úspěšná, Viditelnost zásob přidá k omezenému rezervovanému množství, odečte od množství dostupného pro rezervaci (AFR) a odpoví ID předběžné rezervace.
- V tuto chvíli zůstává množství vaší fyzické zásoby stejné.
- Poté můžete synchronizovat buď jednotlivé, nebo agregované objednávky (řádky objednávek) s předběžnými rezervacemi do Supply Chain Management, abyste mohli provádět pevné rezervace a uvolnit je do skladu nebo aktualizovat konečné množství zásob.
- Systém můžete nastavit na [kompenzaci předběžných rezervací](#offset-scm) při aktualizaci fyzických zásob v Supply Chain Management.

Předběžné rezervace se obvykle vytvářejí, spotřebovávají a ruší pomocí volání API ke službě Viditelnost zásob.

> [!NOTE]
> Volitelně můžete nastavit Supply Chain Management (a další systémy třetích stran) k automatickému vyrovnání množství, které bylo rezervováno pomocí Viditelnosti zásob. Množství vyrovnání je odstraněno ze záznamů rezervací ve Viditelnosti zásob.
>
> Ve výchozím nastavení se funkce kompenzace automaticky zapne, když zapnete funkci předběžné rezervace.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Zapnutí a nastavení funkce rezervace

Chcete-li funkci rezervace zapnout, postupujte následujícím způsobem.

1. Přihlaste se do Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Správa funkcí** zapněte funkci *OnHandReservation*.
1. Přihlaste se do prostředí Supply Chain Management.
1. Jděte na **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** pracovního prostoru a povolte funkci *Integrace viditelnosti zásob s posunem rezervace* (vyžaduje verzi 10.0.22 nebo novější).
1. Jděte na **Řízení zásob \> Nastavení \> Parametry integrace viditelnosti zásob**, otevřete kartu **Ofset rezervace** a vytvořte následující nastavení:

    - **Povolit posun rezervace** - Nastavením na *Ano* povolíte tuto funkci.
    - **Modifikátor kompenzace rezervace** - Vyberte stav transakce zásob, který bude kompenzovat rezervace provedené ve službě Viditelnost zásob. Toto nastavení určuje fázi zpracování objednávky, která spouští offsety. Fáze je sledována podle stavu transakcí zásob objednávky. Vyberte jednu z následujících hodnot:

        - *Při objednávce* - Objednávky, které mají stav *Na objednávce*, odešlou po vytvoření požadavek na kompenzaci. Kompenzované množství bude množství vytvořené objednávky (řádek).
        - *Rezervovat* – Objednávky, které mají stav *Rezervovat*, odešlou požadavek na kompenzaci, když je objednávka rezervována nebo fyzicky rezervována. Když kompenzujete na stavu *Rezervovat*, objednávka odešle požadavek na kompenzaci při jakémkoli novém stavu zásob, který je nejblíže rezervovanému vyskladnění (např. vyskladnění, zaslání dodacího listu nebo fakturace). K tomuto chování dochází, i když přeskočíte rezervaci v Supply Chain Management a budete pokračovat do jiného stavu zásob (například pokud přeskočíte z vydání do skladu k vyskladnění a balení). Požadavek bude spuštěn pouze jednou. Pokud byla spuštěna při vychystání, nezduplikuje kompenzaci při vystavení dodacího listu. Kompenzované množství bude stejné jako množství, ze kterého se změnil stav transakce zásob, když byla spuštěna kompenzace (jinými slovy *Rezervované objednané*/*Rezervované fyzické* nebo pozdější stav na příslušném řádku objednávky).

1. Přihlaste se zpět do aplikace Viditelnost inventáře, přejděte na stránku **Konfigurace** a poté na kartě **Předběžná rezervace** zkontrolujte výchozí hierarchii předběžných rezervací. Podle potřeby přidejte do hierarchie nové dimenze.
1. V části **Nastavení mapování předběžných rezervací** zobrazte výchozí nastavení. Ve výchozím nastavení budou množství rezervovaných zásob zaúčtována proti fyzické míře `softreservephysical` zdroje dat `iv`. Vypočítaná míra *K dispozici pro rezervaci* je mapována na `availabletoreserve`. Pokud chcete aktualizovat vypočítanou míru `availabletoreserve`, přejděte na stránku **Konfigurace** a poté na kartu **Vypočítaná míra** a rozbalte a upravte vypočítanou míru.

Další informace viz [Konfigurace viditelnosti zásob](inventory-visibility-configuration.md).

> [!NOTE]
> Hierarchie rezervací popisuje posloupnost dimenzí, které je třeba zadat při vytváření rezervace. Funguje to stejným způsobem, jako hierarchie indexu funguje pro dotazy na zásoby na skladě, ale používá se nezávisle, takže uživatelé mohou specifikovat podrobnosti dimenze a provádět přesnější rezervace.
>
> Vaše hierarchie předběžných rezervací by měla obsahovat `SiteId` a `LocationId` jako součásti, protože vytvářejí konfiguraci oddílu Viditelnosti zásob.

Další informace o způsobu konfigurace rezervací naleznete v tématu [Konfigurace rezervací](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Použijte funkci rezervace ve Viditelnosti zásob

Když zavoláte rezervační rozhraní API, systém označí rezervaci zadaného zboží a množství.

Zde je příklad scénáře a ukázkové tělo dotazu API. Společnost Contoso prodává produkt D0002 (skříň) ze svého e-shopu. Zákazník prostřednictvím webové stránky zadá prodejní objednávku na malou červenou skříňku. Společnost Contoso se rozhodla splnit tuto objednávku pomocí následujících rozměrů:

- ID organizace = usmf
- Lokalita = 1
- Sklad = 11
- Produkt = D0002
- Barva = červená
- Velikost = malá

Společnost Contoso již nastavila rozhraní API připojení k Viditelnosti zásob ze svého vlastního systému elektronického obchodování. Když je objednávka přijata, systém okamžitě spustí volání API pro provedení předběžné rezervace pro skříň ve viditelnosti zásob.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Vytváření předběžných rezervací pomocí rezervačního rozhraní API

Rezervace se provádějí ve službě Viditelnost zásob odesláním požadavku POST na adresu URL služby, jako je například `/api/environment/{environmentId}/onhand/reserve`.

U rezervace musí orgán žádosti obsahovat ID organizace, ID produktu, rezervovaná množství a rozměry.

Když zavoláte rezervační rozhraní API, můžete řídit ověření rezervace zadáním logické hodnoty parametru `ifCheckAvailForReserv` v těle požadavku. Hodnota `True` znamená, že je vyžadováno ověření, zatímco hodnota `False` znamená, že ověření není vyžadováno. Výchozí hodnota je typu `True`.

Pokud chcete zrušit rezervaci nebo zrušit rezervaci zadaného množství zásob, nastavte množství na zápornou hodnotu a nastavte parametr `ifCheckAvailForReserv` na `False` pro přeskočení ověření.

Zde je příklad těla požadavku, který odkazuje na prodejní objednávku v předchozím kontextu.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Úspěšný požadavek na předběžnou rezervaci vrátí *ID předběžné rezervace* pro každý záznam o rezervaci. ID předběžné rezervace není jedinečný identifikátor pro jednotlivý záznam předběžné rezervace, ale kombinace ID produktu a hodnot dimenze, které jsou spojeny s požadavkem na předběžnou rezervaci. ID předběžné rezervace můžete zaznamenat na řádek objednávky, když synchronizujete úspěšně rezervované objednávky do Supply Chain Management nebo jiného systému ERP pro kompenzaci.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Kompenzace předběžných rezervací v Supply Chain Management

Můžete kompenzovat rezervované množství poté, co je množství na objednávce fyzicky odečteno v Supply Chain Management nebo jiném ERP systému. Viditelnost zásob nabízí připravenou integraci kompenzace předběžných rezervací se Supply Chain Management.

Ke kompenzaci předběžné rezervace postupujte následovně.

1. Přihlaste se k aplikaci Supply Chain Management.
1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. Znovu vytvořte externí prodejní objednávku a přidejte prodejní řádek, který používá přesně stejné ID produktu, organizaci, lokalitu, sklad a hodnoty dimenzí.
1. Na záložce s náhledem **Řádky prodejní objednávky** vyberte prodejní řádek, který jste právě zadali, a poté na panelu nástrojů vyberte **Zásoby \> ID rezervace**.
1. Proveďte jeden z následujících kroků:

    - Zkopírujte ID předběžné rezervace do odpovědi na žádost o nezávaznou rezervaci a vložte ji do pole **ID rezervace**.
    - Ponechte pole **ID rezervace** prázdné, ale zaškrtněte tlačítko **Automatická kompenzace služby zásob**. Systém automaticky určí, který produkt a dimenze produktu se mají kompenzovat, na základě ID položky a hodnot dimenze, které jsou zadány na vybraném řádku.

1. Vyberte **OK**.
1. V době, kdy je vybrán řádek prodeje, fyzicky rezervujte objednané množství výběrem **Zásoby \> Rezervace** na panelu nástrojů na pevné záložce **Řádky prodejní objednávky**.
1. Pokud jste dříve nastavili pole **Modifikátor kompenzace rezervace** na *Rezervováno*, kompenzace se spustí, když má řádek objednávky stav *Fyzická rezervace* nebo *Rezervace objednána*. Dávková úloha se spouští jednou za minutu, aby se synchronizovaly požadavky na kompenzaci ze Supply Chain Management do viditelnosti zásob.

> [!NOTE]
> U stavů transakcí, které obsahují zadaný modifikátor vyrovnání rezervace, aktualizace transakce vyrovná odpovídající záznam rezervace, pokud jsou splněny všechny následující podmínky:
>
> - ID rezervace u transakce zásob odpovídá ID rezervace záznamu rezervace ve Viditelnosti zásob.
> - Dimenze transakce zásob je identická s dimenzemi záznamu rezervace ve Viditelnosti zásob.
> - Změny stavu transakcí zásob aktivují vyrovnání rezervací, když stav transakcí zásob odráží skutečnost, že zpracování objednávky bylo dokončeno nebo přeskočeno.

Množství kompenzace následují množství zásob, které je uvedeno v příslušných transakcích zásob. Kompenzace se neprojeví, pokud ve Viditelnosti zásob nezůstane žádné rezervované množství.

### <a name="cancel-or-revert-a-soft-reservation"></a>Zrušení nebo vrácení předběžné rezervace

Pokud je původní řádek objednávky zrušen nebo odstraněn a vy musíte vrátit zpět odpovídající předběžnou rezervaci, odešlete záporné množství, které má přesně stejné informace v těle vašeho dotazu API.
