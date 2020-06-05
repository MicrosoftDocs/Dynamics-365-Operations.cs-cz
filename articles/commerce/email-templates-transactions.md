---
title: Vytvoření e-mailových šablon pro transakční události
description: Toto téma popisuje, jak vytvářet, odesílat a konfigurovat e-mailové šablony pro transakční události v aplikaci Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5cd928e90654cca639ed1e163be9192c0dffd9ad
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367168"
---
# <a name="create-email-templates-for-transactional-events"></a>Vytvoření e-mailových šablon pro transakční události

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvářet, odesílat a konfigurovat e-mailové šablony pro transakční události v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Dynamics 365 Commerce poskytuje vestavěné řešení pro odesílání e-mailů, které upozorňují zákazníky na transakční události (například při zadávání objednávky, když je objednávka připravená k vyzvednutí nebo když byla expedována). Toto téma popisuje kroky pro vytváření, odesílání a konfiguraci e-mailových šablon, které se používají k odesílání transakčních e-mailů.

## <a name="create-an-email-template"></a>Vytvoření šablonu e-mailu

Než budete moci mapovat konkrétní transakční událost na e-mailovou šablonu, musíte ji vytvořit.

Šablonu e-mailu vytvoříte takto:

1. V Commerce Headquarters přejděte na **Retail and Commerce \> Nastavení Headquarters \> Šablony e-mailu organizace**.
1. Zvolte **Nové**.
1. Pod možností **Obecné** nastavte následující pole:

    - **ID e-mailu** - ID e-mailu je jedinečný identifikátor pro šablonu a je to hodnota, která se zobrazí, když vyberete šablonu pro mapování na událost.
    - **Popis e-mailu** - Pomocí tohoto volitelného pole můžete zadat popis šablony. Zadaná hodnota se zobrazí pouze v Commerce Headquarters.
    - **Jméno odesílatele** - Jméno, které zadáte, se objeví v poli „Odesílatel“ většiny e-mailových klientů.
    - **E-mail odesílatele** - Zadejte e-mailovou adresu, která má být použita pro e-maily odeslané pomocí této šablony.
    - **Výchozí kód jazyka** - Toto pole určuje lokalizovanou verzi e-mailu, který je odeslán ve výchozím nastavení, pokud kanál, který vyvolává tuto šablonu, neposkytuje žádný jazyk.

1. V části **Obsah e-mailové zprávy** vyberte **Nový**.
1. V poli **Jazyk** zadejte jazyk šablony e-mailu. Později můžete přidat další jazyky a lokalizované šablony.
1. V poli **Předmět** zadejte předmět e-mailu, který by se měl objevit v poli předmětu e-mailu.
1. Vyberte **Upravit** a odešlete svou e-mailovou šablonu.

## <a name="create-an-email-message-body-by-using-html"></a>Vytvoření těla e-mailové zprávy pomocí HTML

Tělo zprávy vašeho e-mailu je vytvořeno v HTML. Můžete použít libovolné rozvržení, styl a značky, které HTML a vložené šablony stylů CSS umožňují. Můžete také použít obrázky, pokud je hostujete na veřejně dostupném webovém koncovém bodu. Chcete-li přidat obrázek, zadejte adresu URL obrázku do atributu **src** značky HTML **&lt;img&gt;**.

> [!NOTE]
> E-mailoví klienti mají omezení rozložení a stylu, která mohou vyžadovat úpravy HTML a CSS stylů, které používáte pro tělo zprávy. Doporučujeme vám seznámit se s osvědčenými postupy vytváření HTML, které budou podporovat nejoblíbenější e-mailoví klienti.

## <a name="add-placeholders-to-the-email-message-body"></a>Přidání zástupného textu do těla e-mailové zprávy

Váš e-mail může obsahovat zástupné texty, které jsou při vygenerování e-mailu nahrazeny hodnotami specifickými pro zákazníka a pro transakce. Zástupné texty jsou vždy obklopeny znakem procenta (%) a jsou vloženy přímo do dokumentu HTML.

Následuje příklad.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Zástupné texty objednávek (úroveň prodejní objednávky)

Následující zástupné texty se načtou a zobrazí data, která jsou definována na úrovni prodejní objednávky (na rozdíl od úrovně řádku prodeje).

| Název zástupného textu    | Hodnota zástupného textu                                                |
|---------------------|------------------------------------------------------------------|
| customername        | Jméno zákazníka, který vystavil objednávku.                   |
| salesid             | ID prodejní objednávky.                                       |
| deliveryaddress     | Dodací adresa pro expedované objednávky.                         |
| customeraddress     | Adresa zákazníka.                                     |
| deliverydate        | Datum dodání.                                               |
| shipdate            | Datum expedice.                                                   |
| modeofdelivery      | Způsob doručení objednávky.                                  |
| náklady pro záhlaví             | Celkové poplatky za objednávku.                                 |
| daň                 | Celková daň objednávky.                                     |
| celkem               | Celková částka objednávky.                                  |
| ordernetamount      | Celková částka objednávky snížená o celkovou daň.             |
| sleva            | Celková sleva objednávky.                                |
| storename           | Název obchodu, kde byla vystavena objednávka.                |
| storeaddress        | Adresa obchodu, který vystavil objednávku.                  |
| storeopenfrom       | Otevírací čas obchodu, který vystavil objednávku.             |
| storeopento         | Zavírací čas obchodu, který vystavil objednávku.             |
| pickupstorename     | Název obchodu, kde bude objednávka vyzvednuta.         |
| pickupstoreaddress  | Adresa obchodu, kde bude objednávka vyzvednuta.      |
| pickupopenstorefrom | Otevírací čas obchodu, kde bude objednávka vyzvednuta. |
| pickupopenstoreto   | Zavírací čas obchodu, kde bude objednávka vyzvednuta. |

### <a name="order-line-placeholders-sales-line-level"></a>Zástupné texty řádku objednávky (úroveň řádku prodeje)

Následující zástupné texty získávají a zobrazují data pro jednotlivé produkty (řádky) v prodejní objednávce.

| Název zástupného textu               | Hodnota zástupného textu |
|--------------------------------|-------------------|
| productid                      | ID produktu pro řádek. |
| lineproductname                | Název produktu. |
| lineproductdescription         | Popis produktu. |
| linequantity                   | Počet jednotek, které byly objednány pro řádek, plus měrná jednotka (například **ks**, nebo **pár**). |
| lineunit                       | Měrná jednotka řádku. |
| linequantity_withoutunit       | Počet jednotek, které byly objednány pro řádek, bez měrné jednotky. |
| linequantitypicked             | Když je použita událost **PickOrder**, počet jednotek, které byly vydány. V opačném případě **0** (nula). |
| linequantitypicked_withoutunit | Když je použita událost **PickOrder**, počet jednotek, které byly vydány, bez měrné jednotky. V opačném případě **0** (nula). |
| linequantitypacked             | Když jsou použity události **PackOrder** a **Objednávka připravena k vyzvednutí**, počet jednotek, které byly zabaleny. V opačném případě **0** (nula). |
| linequantitypacked_withoutuom  | Když jsou použity události **PackOrder** a **Objednávka připravena k vyzvednutí**, počet jednotek, které byly zabaleny, bez měrné jednotky. V opačném případě **0** (nula). |
| linequantityshipped            | Vždy **0**, s výjimkou případů, kdy jsou použity konkrétní události, jak je popsáno v dalším řádku. |
| linequantityshipped_withoutuom | Když je použita událost **ShipOrder**, počet jednotek, které byly vydány, bez měrné jednotky. V opačném případě **0** (nula). |
| lineprice                      | Cena za jednotku. |
| linenetamount                  | Cena řádku po použití počtu jednotek a slevy. |
| linediscount                   | Sleva na jednotlivou jednotku. |
| lineshipdate                   | Datum expedice pro řádek. |
| linedeliverydate               | Datum dodání pro řádek. |
| linedeliverymode               | Způsob dodání pro řádek. |
| linedeliveryaddress            | Adresa dodání pro řádek. |
| giftcardnumber                 | Číslo dárkového poukazu pro výrobky typu dárkového poukazu. |
| giftcardbalance                | Zůstatek dárkového poukazu pro výrobky typu dárkového poukazu. |
| giftcardmessage                | Zpráva dárkového poukazu pro výrobky typu dárkového poukazu. |
| giftcardpin                    | PIN kód dárkového poukazu pro výrobky typu dárkového poukazu. (Tento zástupný text je specifický pro externí dárkové poukazy.) |
| giftcardexpiration             | Datum vypršení dárkového poukazu pro výrobky typu dárkového poukazu. (Tento zástupný text je specifický pro externí dárkové poukazy.) |
| giftcardrecipientname          | Jméno příjemce dárkového poukazu pro výrobky typu dárkového poukazu. |
| giftcardbuyername              | Jméno kupce dárkového poukazu pro výrobky typu dárkového poukazu. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Formát zástupných textů řádků objednávky v těle e-mailové zprávy

Když vytvoříte HTML pro jednotlivé řádky objednávky v těle e-mailové zprávy, ohraničte opakující se blok HTML a zástupné texty pro řádky s následujícími zástupnými texty, které jsou vloženy do značek komentářů HTML.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Následuje příklad.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Vytvoření šablon pro e-mailové účtenky

Účtenky lze zaslat e-mailem zákazníkům, kteří nakupují v maloobchodním pokladním místě (POS). Obecně jsou kroky pro vytvoření šablony účtenky odeslané e-mailem stejné jako kroky pro vytvoření šablon pro jiné transakční události. Jsou však nutné následující změny:

- ID e-mailu e-mailové šablony musí být **emailRecpt**.
- Text účtenky se vloží do e-mailu pomocí zástupného textu **%message%**. Aby bylo zajištěno, že tělo účtenky je správně vykresleno, obklopte zástupný text **%message%** HTML značkami **&lt;pre&gt;** a **&lt;/pre&gt;**.
- Konce řádků v HTML pro záhlaví a zápatí e-mailu jsou převedeny na HTML značky **&lt;br /&gt;**, aby bylo tělo účtenky vykresleno správně. Chcete-li vyloučit nežádoucí vertikální prostor v e-mailech s účtenkou, odstraňte konce řádků z jakéhokoli místa v HTML, kde vertikální prostor není vyžadován.

Další informace o způsobu konfigurace e-mailových účtenek naleznete v tématu [Nastavení účtenek e-mailem](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).

## <a name="upload-the-email-html"></a>Odeslání HTML e-mailu

Poté, co jste vytvořili a otestovali HTML pro tělo své zprávy, musí být odesláno do Commerce Headquarters. V současné době nelze HTML e-mailu exportovat. Proto musíte zachovat hlavní kopii vašeho HTML mimo Commerce Headquarters.

Chcete-li nahrát novou nebo upravenou HTML e-mailovou šablonu, postupujte takto.

1. V Commerce Headquarters přejděte na **Retail and Commerce \> Nastavení Headquarters \> Šablony e-mailu organizace**.
1. Vyberte řádek pro jazyk, pro který chcete přidat nebo nahradit HTML. Případně vyberte **Nový** pro vytvoření řádku pro nový jazyk.
1. Vyberte možnost **Upravit**.
1. V zobrazeném dialogovém okně vyberte **Procházet**. Vyhledejte dokument HTML, který chcete odeslat, vyberte ho a poté vyberte **Otevřít**.
1. Vyberte **Odeslat**.
1. Poté, co se v okně náhledu zobrazí vaše HTML e-mail, vyberte **OK**.
1. Ujistěte se, že je pro řádek zaškrtnuto políčko **Má tělo**.

Pokud jste již nakonfigurovali Commerce Headquarters pro odesílání e-mailu, váš nový nebo aktualizovaný e-mail bude zaslán všem zákazníkům, kteří provedou transakci, která vyvolá událost mapovanou na šablonu.

Další informace o způsobu konfigurace e-mailů v Dynamics 365 Commerce naleznete v části [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Další prostředky 

[Nastavení profilu oznámení e-mailem](email-notification-profiles.md)

[Konfigurace a odeslání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Nastavení účtenek e-mailem](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Odesílání účtenek e-mailem z Modern POS](email-receipts.md)
