---
title: Aplikace Viditelnost zásob
description: Toto téma popisuje, jak používat aplikaci Viditelnost zásob.
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
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344995"
---
# <a name="inventory-visibility-app"></a>Aplikace Viditelnost zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Toto téma popisuje, jak používat aplikaci Viditelnost zásob.

Viditelnost zásob poskytuje modelem řízenou aplikaci pro vizualizaci. Aplikace obsahuje tři stránky: **Konfigurace**, **Provozní viditelnost** a **Souhrn zásob**. Má následující funkce:

- Poskytuje uživatelské rozhraní (UI) pro konfiguraci množství na skladě a konfiguraci předběžných rezervací.
- Podporuje dotazy na zásoby v reálném čase,. zahrnující různé kombinace dimenzí.
- Poskytuje uživatelské rozhraní pro odesílání požadavků na rezervaci.
- Poskytuje přizpůsobený pohled na skladové zásoby produktů společně se všemi dimenzemi

## <a name="prerequisites"></a>Předpoklady

Než začnete, nainstalujte a nastavte doplněk Viditelnost inventáře podle popisu v tématu [Nastavení doplňku Viditelnost zásob](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Konfigurace

Stránka **Konfigurace** vám pomůže nastavit konfiguraci množství na skladě a konfiguraci předběžných rezervací. Po instalaci doplňku obsahuje výchozí konfigurace hodnotu ze softwaru Microsoft Dynamics 365 Supply Chain Management (zdroj dat `fno`). Výchozí nastavení můžete zkontrolovat. Navíc na základě vašich obchodních požadavků a požadavků na účtování zásob vašeho externího systému můžete upravit konfiguraci v [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) a standardizovat tak způsob, jakým mohou být změny v inventáři zaúčtovány, organizovány a dotazovány z různých systémů.

### <a name="define-data-sources"></a>Definování zdrojů dat

Každý *zdroj dat*, který chcete integrovat s Viditelností zásob, musíte definovat. Viditelnost zásob podporuje integraci s různými zdroji dat, jako je systém prodejního místa (POS), Supply Chain Management a další externí systémy. Ve výchozím nastavení je Supply Chain Management nastaven ve Viditelnosti zásob jako výchozí zdroj dat (`fno`).

Chcete-li přidat zdroj dat, postupujte takto:

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Zdroj dat** vyberte příkaz **Nový zdroj dat** a přidejte zdroj dat.

> [!NOTE]
> Když přidáte zdroj dat, ověřte si před aktualizací konfigurace služby Viditelnost zásob název zdroje dat, fyzické míry a mapování dimenzí. Po výběru příkazu **Aktualizovat konfiguraci** nebudete moci tato nastavení upravovat.

### <a name="set-up-dimension-mappings"></a>Nastavení mapování dimenzí

Viditelnost inventáře poskytuje seznam základních dimenzí, které lze mapovat z dimenzí vašeho zdroje dat. Pro mapování je k dispozici celkem třicet tři dimenzí.

- Ve výchozím nastavení, pokud jako jeden ze zdrojů dat používáte Supply Chain Management, je 13 dimenzí mapováno na standardní dimenze Supply Chain Management. Dvanáct dalších dimenzí (`inventDimension1` až `inventDimension12`) je mapováno na vlastní dimenze v Supply Chain Management. Zbývajících osm dimenzí jsou rozšířené dimenze, které můžete namapovat na externí zdroje dat.
- Pokud jako jeden ze zdrojů dat nepoužíváte Supply Chain Management, můžete dimenze mapovat libovolně. Následující tabulka ukazuje úplný seznam dostupných dimenzí.

> [!NOTE]
> Pokud vaše dimenze není v seznamu výchozích dimenzí a používáte externí zdroj dat, doporučujeme v mapování použít dimenze `ExtendedDimension1` až `ExtendedDimension8`.

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
| Ostatní | `VersionId` |
| Zásoby (vlastní) | `InventDimension1` až `InventDimension12` |
| Ostatní | `ExtendedDimension1` až `ExtendedDimension8` |

Chcete-li přidat mapování dimenzí, postupujte následujícím způsobem.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Zdroj dat** v části **Mapování dimenzí** vyberte příkaz **Přidat**.
1. V poli **Název dimenze** zadejte zdrojovou dimenzi.
1. V poli **Na základní dimenzi** vyberte dimenzi v aplikaci Viditelnost zásob, kterou chcete namapovat.
1. Zvolte možnost **Uložit**.

![Přidání mapování dimenzí](media/inventory-visibility-dimension-mapping.png "Přidání mapování dimenzí")

Pokud váš zdroj dat obsahuje například dimenzi barvy produktu, můžete ji namapovat na základní dimenzi `ColorId` a přidat tak vlastní dimenzi `ProductColor` ve zdroji dat `exterchannel`. Poté je dimenze mapována na základní dimenzi `ColorId`.

## <a name="create-a-physical-measure"></a>Vytvoření fyzické míry

Když zdroj dat odešle změnu zásob do Viditelnosti zásob, odešle tuto změnu pomocí *fyzických měr*. Fyzické míry jsou modifikátory, které odrážejí stavy souhrnných transakcí zásob. Dotazy mohou být založeny na fyzických mírách.

Viditelnost zásob má seznam výchozích fyzických měr. Tyto výchozí fyzická míry jsou převzaty ze stavů transakcí zásob na stránce **Seznam skladu** v Supply Chain Management (**Řízení zásob \> Dotazy a hlášení \> Seznam skladu**).

| Modifikátor | Jméno |
|---|---|
| `PhysicalInvent` | Fyzické zásoby |
| `ReservPhysical` | Rezervované fyzicky |
| `AvailPhysical` | Fyzicky k dispozici |
| `ReservOrdered` | Rezervované objednané |
| `PostedQty` | Zaúčtované množství |
| `Deducted` | Odečteno |
| `Picked` | Vyzvednuto |
| `Received` | Přijato |
| `Registered` | Registrováno |
| `Arrived` | Doručeno |
| `Ordered` | Objednáno |
| `OnOrder` | Na objednávce |
| `QuotationReceipt` | Příjem nabídky |
| `QuotationIssue` | Vystavení nabídky |

Pokud je zdrojem dat Supply Chain Management, nemusíte znovu vytvářet výchozí fyzické míry. U externích zdrojů dat však můžete vytvořit nové fyzické míry podle následujících kroků.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Zdroj dat** v části **Fyzické míry** vyberte **Přidat**, zadejte název zdrojové míry a uložte změny.

## <a name="define-the-product-hierarchy-index"></a>Definování indexu hierarchie produktů

Po nastavení agregovaných skupin dimenzí můžete pomocí Viditelnosti inventáře odesílat dotazy na stav zásob na skladě. Ve Viditelnosti zásob je každá skupina dimenzí známá jako *index*. Každý index odpovídá číslu sady. Můžete si vybrat, které dimenze budou použity k nastavení indexování, a to na základě způsobu, jakým budete dotazovat Viditelnost inventáře.

Chcete-li nastavit index hierarchie produktů, postupujte následujícím způsobem.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Index hierarchie produktů** v části **Mapování dimenzí** vyberte příkaz **Přidat**.
1. Ve výchozím nastavení je k dispozici seznam indexů. Chcete-li upravit stávající index, vyberte **Upravit** nebo **Přidat** v části příslušného rejstříku. Chcete-li vytvořit novou sadu indexů, vyberte příkaz **Nová sada indexů**. Pro každý řádek v každé sadě indexů vyberte v poli **Dimenze** hodnotu ze seznamu základních dimenzí. Automaticky se generují hodnoty pro následující pole:

    - **Číslo sady** – Dimenze, které patří do stejné skupiny (indexu), budou seskupeny a bude jim přiděleno stejné číslo sady.
    - **Hierarchie** – Hierarchie se používá k definování podporovaných kombinací dimenzí, které lze dotazovat ve skupině dimenzí (indexu). Pokud například nastavíte skupinu dimenzí, která má hierarchickou posloupnost *Styl*, *Barva* a *Velikost*, systém umí vrátit výsledek na tři skupiny dotazů. První skupina je pouze styl. Druhá skupina je kombinace stylu a barvy. A třetí skupina je kombinace stylu, barvy a velikosti. Ostatní kombinace nejsou podporovány.

Další informace najdete v tématu [Konfigurace hierarchie indexu produktů](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Příklad

Tato část poskytuje příklad, který ukazuje, jak hierarchie funguje. Následující tabulka obsahuje seznam dostupných zásob pro tento příklad.

| Zboží | Styl | Barva | Velikost | Množství |
|---|---|---|---|---|
| I0001 | Široká | Černá | Malá | 1 |
| I0001 | Široká | Černá | Velká | 2 |
| I0001 | Široká | Červená | Malá | 3 |
| I0001 | Normální | Černá | Malá | 4 |
| I0001 | Normální | Černá | Velká | 5 |
| I0001 | Normální | Červená | Malá | 6 |
| I0001 | Normální | Červená | Velká | 7 |

V následující tabulce jsou uvedena nastavení hierarchie indexů.

| Klíč | Číslo sady | Hierarchie |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Na základě předchozího nastavení vypadá kombinace dimenzí pro dotaz Viditelnost zásob takto: *Styl*, *Barva* a *Velikost*. Nastavení hierarchie umožňuje externím systémům dotazovat se na zásoby skladem následujícími způsoby:

- `()` – Seskupeni podle všech. Zde je výsledný výstup:

    - I0001, 28

- `(StyleId)` – Seskupení podle stylu. Zde je výsledný výstup:

    - I0001, Široká, 6
    - I0001, Normální, 22

- `(StyleId, ColorId)` – Seskupeno podle kombinace stylu a barvy. Zde je výsledný výstup:

    - I0001, Široká, Černá, 3
    - I0001, Široká, Červená, 3
    - I0001, Normální, Černá, 9
    - I0001, Normální, Červená, 13

- `(StyleId, ColorId, SizeId)` – Seskupeno podle kombinace stylu, barvy a velikosti. Zde je výsledný výstup:

    - I0001, Široká, Černá, Malá, 1
    - I0001, Široká, Černá, Velká, 2
    - I0001, Široká, Červená, Malá, 3
    - I0001, Normální, Černá, Malá, 4
    - I0001, Normální, Černá, Velká, 5
    - I0001, Normální, Červená, Malá, 6
    - I0001, Normální, Červená, Velká, 7

## <a name="set-up-a-custom-calculated-measure"></a>Nastavení vlastní vypočítané míry

Viditelnost zásob můžete použít k dotazování na fyzické míry zásob i na *vlastní vypočítané míry*.

Konfigurace umožňuje definovat sadu modifikátorů, které se přidávají nebo odčítají, aby se získalo celkové agregované výstupní množství.

1. Přihlaste se ke svému prostředí Power Apps a otevřete **Viditelnost zásob**.
1. Otevřete stránku **Konfigurace**.
1. Na kartě **Vypočítaná míra** vyberte příkaz **Nová výpočetní míra** a přidejte vypočítanou míru. Poté nastavte pole, jak je popsáno v následující tabulce.

    | Pole | Hodnota |
    |---|---|
    | Název nové vypočítané míry | Zadejte název vypočítané míry. |
    | Zdroj dat | Dotazovací systém je zdrojem dat. |
    | Zdroj dat modifikátoru | Zadejte zdroj dat modifikátoru. |
    | Modifikátor | Zadejte název modifikátoru. |
    | Typ modifikátoru | Vyberte typ modifikátoru (*Sčítání* nebo *Odčítání*). |

Následující tabulka zobrazuje příklad vlastního vypočítaného měření `MyCustomAvailableforReservation`. Další informace o tomto příkladu naleznete v tématu [Konfigurace zdroje dat](inventory-visibility-configuration.md#data-source-configuration).

| Zdroj dat vypočtené míry | Vypočtená míra | Zdroj dat modifikátoru | Modifikátor | Typ modifikátoru |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Nastavení mapování předběžných rezervací

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Než budete moci upravit kartu **Mapování předběžné rezervace**, musíte zapnout funkci *OnHandReservation* na kartě **Správa funkcí**.

Nastavením mapování z fyzické míry na vypočítanou míru povolíte službě Viditelnost zásob automaticky ověřovat dostupnost rezervace na základě fyzické míry.

Než nastavíte toto mapování, musí být na kartách **Zdroj dat** a **Vypočítaná míra** ve stránce **Konfigurace** v Power Apps definovány fyzické míry, vypočítané míry a jejich zdroje dat (jak je popsáno dříve v tomto tématu).

Chcete-li definovat mapování předběžných rezervací, postupujte takto.

1. Definujte fyzickou míru, která slouží jako míra pro předběžnou rezervaci (např.`softreservordered`).
1. Na kartě **Vypočítaná míra** ve stránce **Konfigurace** definujte vypočítanou míru *k dispozici pro rezervaci* (AFR), která obsahuje výpočetní vzorec AFR, který chcete namapovat na fyzickou míru. Můžete například nastavit `availforreserv` (k dispozici pro rezervaci), takže je mapováno na dříve definovanou fyzickou míru `softreservordered`. Tímto způsobem můžete zjistit, která množství se stavem zásob `softreservordered` budou k dispozici pro rezervaci. Následující tabulka ukazuje výpočetní vzorec AFR.

    | Modifikátor | Zdroj dat | Míra |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Otevřete stránku **Konfigurace**.
1. Na kartě **Mapování předběžné rezervace** nastavte mapování z fyzické míry na vypočítanou míru. V předchozím příkladu můžete následující nastavení použít k mapování `availforreserv` na dříve definovanou fyzickou míru `softreservordered`.

    | Zdroj dat fyzické míry | Fyzická míra | K dispozici pro zdroj dat rezervace | K dispozici pro vypočítanou míru rezervace |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Nastavení hierarchie předběžné rezervace

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Než budete moci upravit kartu **Hierarchie předběžné rezervace**, musíte zapnout funkci *OnHandReservation* na kartě **Správa funkcí**.

Hierarchie rezervací popisuje posloupnost dimenzí, které je třeba zadat při vytváření rezervace. Funguje stejným způsobem, jako funguje hierarchie indexu produktů pro dotazy na zásoby na skladě.

Hierarchie rezervací se může lišit od hierarchie indexu zásob na skladě. Tato nezávislost vám umožňuje implementovat správu kategorií, kde mohou uživatelé rozdělit dimenze na detaily a specifikovat požadavky, aby vytvářeli přesnější rezervace.

#### <a name="example"></a>Příklad

Ve vašem systému je nastavena následující hierarchie rezervací.

| Dimenze | Hierarchie |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Na základě této hierarchie rezervací můžete provést rezervaci v následujícím pořadí dimenzí:

- `()` – Není zadána žádná dimenze.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Pořadí dimenzí by mělo striktně dodržovat posloupnost hierarchie rezervace, dimenzi po dimenzi. Například rezervace, které mají posloupnost `(ColorId, StyleId)`, nebudou v tomto příkladu povoleny, protože tato posloupnost není v hierarchii rezervací definována.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Správa řídicích funkcí

Doplněk Viditelnost zásob nabízí různé funkce, např. *OnHandReservation* a *OnHandMostSpecificBackgroundService*. Ve výchozím nastavení jsou tyto funkce vypnuté. Chcete-li je použít, otevřete stránku **Konfigurace** v Power Apps a potom je zapněte na kartě **Správa funkcí**.

### <a name="complete-and-update-the-configuration"></a>Dokončení a aktualizace konfigurace

Po dokončení konfigurace musíte potvrdit všechny změny v doplňku Viditelnosti zásob. Chcete-li potvrdit změny, vyberte příkaz **Aktualizovat konfiguraci** v pravém horním rohu stránky **Konfigurace** v Power Apps.

Při prvním výběru příkazu **Aktualizovat konfiguraci** systém požádá o vaše přihlašovací údaje.

- **ID klienta** – ID aplikace Azure, které jste vytvořili pro Viditelnost zásob.
- **ID tenanta** – ID vašeho tenanta Azure.
- **Tajný klíč klienta** – Tajný klíč aplikace Azure, který jste vytvořili pro Viditelnost zásob.

Po přihlášení se konfigurace aktualizuje ve službě Viditelnost zásob.

> [!NOTE]
> Ověřte si před aktualizací konfigurace služby Viditelnost zásob název zdroje dat, fyzické míry a mapování dimenzí. Po výběru příkazu **Aktualizovat konfiguraci** nebudete moci tato nastavení upravovat.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Vyhledání koncového bodu služby

Pokud neznáte správný koncový bod služby Viditelnost zásob, otevřete stránku **Konfigurace** v Power Apps a poté vyberte v pravém horním rohu příkaz **Zobrazit koncový bod služby**. Na stránce se zobrazí správný koncový bod služby.

## <a name="operational-visibility"></a>Provozní viditelnost

Stránka **Provozní viditelnost** obsahuje výsledky dotazu na zásoby v reálném čase sestaveného na základě různých kombinací dimenzí. Když je zapnutá funkce *OnHandReservation*, můžete také odesílat požadavky na rezervaci ze stránky **Provozní viditelnost**.

### <a name="on-hand-query"></a>Dotaz na zásoby na skladě

Karta **Dotaz na zásoby na skladě** zobrazuje výsledky dotazu na zásoby v reálném čase.

Když vyberete kartu **Dotaz na zásoby na skladě**, systém požádá o vaše přihlašovací údaje, aby mohl získat nosný token, který je vyžadován pro dotaz do služby Viditelnost zásob. Nosný token můžete jednoduše vložit do pole **Nosný token** a pak zavřít dialogové okno. Poté můžete odeslat požadavek na zpracování dotazu.

Pokud nosný token není platný nebo pokud jeho platnost vypršela, musíte do pole **Nosný token** vložit nový token. Zadejte správné hodnoty v polích **ID klienta**, **ID tenanta**, **Tajný klíč klienta** a poté vyberte **Obnovit**. Systém automaticky získá nový, platný nosný token.

Chcete-li odeslat dotaz na skladové množství, zadejte dotaz do těla požadavku. Použijte vzor, který je popsán v části [Dotaz pomocí metody POST](inventory-visibility-api.md#query-with-post-method).

![Nastavení dotazu na zásoby na skladě](media/inventory-visibility-query-settings.png "Nastavení dotazu na zásoby na skladě")

### <a name="reservation-posting"></a>Odeslání rezervace

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

K odeslání požadavku na rezervaci použijte kartu **Odeslání rezervace**. Než budete moci odeslat požadavek na rezervaci, musíte zapnout funkci *OnHandReservation*. Další informace o této funkci naleznete v části [Rezervace Viditelnosti zásob](inventory-visibility-reservations.md).

Chcete-li odeslat požadavek na rezervaci, musíte do těla požadavku zadat hodnotu. Použijte vzor, který je popsán v části [Vytvoření jedné rezervační události](inventory-visibility-api.md#create-one-reservation-event). Pak vyberte **Odeslat**. Chcete-li zobrazit podrobnosti odpovědi na požadavek, vyberte **Zobrazit detaily**. Z podrobností odpovědi můžete také získat hodnotu **reservationId** (ID rezervace).

## <a name="inventory-summary"></a>Souhrn zásob

**Souhrn zásob** je přizpůsobené zobrazení pro *entitu součtu zásob na skladě*. Poskytuje souhrn zásob produktů společně se všemi dimenzemi. Pomocí **rozšířeného filtru**, který Dataverse nabízí, můžete vytvořit osobní zobrazení ukazující řádky, které jsou pro vás důležité. Možnosti rozšířeného filtru vám umožní vytvořit širokou škálu zobrazení, od jednoduchých po složité. Také vám umožňují přidat do filtrů seskupené a vnořené podmínky.

Chcete-li se dozvědět více o tom, jak používat **Rozšířený filtr**, přečtěte si téma [´´Uprava nebo vytvoření osobních zobrazení pomocí rozšířených filtrů mřížky](/powerapps/user/grid-filters-advanced)

V horní části přizpůsobeného zobrazení jsou tři pole: **Výchozí dimenze**, **Vlastní dimenze** a **Míra**. Pomocí těchto polí můžete řídit, které sloupce jsou viditelné.

Můžete vybrat záhlaví sloupce a filtrovat nebo seřadit aktuální výsledek.

Ve spodní části přizpůsobeného zobrazení se zobrazují informace typu „50 záznamů (29 vybraných)“ nebo „50 záznamů“. Tyto informace se týkají aktuálně načtených záznamů z výsledku **Rozšířeného filtru**. Text „29 vybraných“ odkazuje na počet záznamů, které byly vybrány pomocí filtru záhlaví sloupců z načtených záznamů.

V dolní části pohledu je tlačítko **Načíst další**, kterým načtete další záznamy z Dataverse. Výchozí počet načtených záznamů je 50. Když použijete tlačítko **Načíst další**, do zobrazení se načte dalších 1 000 dostupných záznamů. Číslo na tlačítku **Načíst další** vyjadřuje aktuálně načtené záznamy a celkový počet záznamů ve výsledku **Rozšířeného filtru**.

![Souhrn zásob](media/inventory-visibility-onhand-list.png "Souhrn zásob")
