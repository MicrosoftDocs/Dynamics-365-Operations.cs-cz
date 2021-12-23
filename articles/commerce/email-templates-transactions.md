---
title: Vytvoření e-mailových šablon pro transakční události
description: Toto téma popisuje, jak vytvářet, odesílat a konfigurovat e-mailové šablony pro transakční události v aplikaci Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 25d7fcb803645f50ee4f5c608f5b6e789dfe3c31
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913745"
---
# <a name="create-email-templates-for-transactional-events"></a>Vytvoření e-mailových šablon pro transakční události

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje, jak vytvářet, odesílat a konfigurovat e-mailové šablony pro transakční události v aplikaci Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce poskytuje připravené řešení pro zasílání e-mailů, které upozorňují zákazníky na transakční události. E-maily lze například odeslat, když je objednávka zadána, je připravena k vyzvednutí nebo byla odeslána. Toto téma popisuje kroky pro vytváření, odesílání a konfiguraci e-mailových šablon, které se používají k odesílání transakčních e-mailů.

## <a name="notification-types"></a>Typy oznámení

Oznámení lze nakonfigurovat tak, aby informovala zákazníky prostřednictvím e-mailu, když nastanou určité události v rámci objednávky a životního cyklu zákazníka. Chcete-li nakonfigurovat oznámení, musíte namapovat šablonu e-mailu na typ oznámení vytvořením profilu oznámení e-mailu Commerce. Informace o tom, jak nastavit profily e-mailových upozornění, viz [Nastavení profilu e-mailových oznámení](email-notification-profiles.md).

Dynamics 365 Commerce podporuje následující typy oznámení.

### <a name="order-created"></a>Objednávka byla vytvořena

Typ oznámení *objednávka byla vytvořena* se spustí při vytvoření nové prodejní objednávky v centrále Commerce.

> [!NOTE]
> Typ oznámení o vytvoření objednávky se nespouští u transakcí typu cash-and-carry, ke kterým dochází na terminálu v místě prodeje (POS). V tomto případě se místo toho vygeneruje e-mailovou nebo vytištěnou účtenku. Více informací viz [Odesílání e-mailových potvrzení z moderního POS (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Objednávka byla potvrzena.

Typ oznámení *objednávka potvrzena* se spustí, když je vygenerován dokument potvrzení objednávky pro prodejní objednávku z centrály Commerce.

### <a name="picking-completed"></a>Výdej byl dokončen.

Typ oznámení *vychystávání dokončeno* se spustí, když je výdejka pro objednávku označena jako dokončená v centrále Commerce.

> [!NOTE]
> Typ oznámení o dokončení vychystávání se nespustí, když je položka označena jako vyskladněná na POS terminálu.

### <a name="packing-completed"></a>Balení bylo dokončeno.

Typ oznámení *balení dokončeno* se spustí, když je dodací list vygenerován pro objednávku v centrále Commerce na terminálu POS.

Typ oznámení o dokončení balení podporuje následující dodatečné e-mailové zástupné symboly pro usnadnění funkce „objednávka připravená k vyzvednutí“ a funkce vyhledávání objednávek z transakčních e-mailů.

| Název zástupného textu    | Účel |
| ------------------- | ------- |
| `pickupstorename`     | Název obchodu, kde je možné objednávku vyzvednout. |
| `pickupstoreaddress`  | Adresa obchodu, kde je možné objednávku vyzvednout. |
| `pickupstorehourfrom` | Otevírací doba výdejny. |
| `pickupstorehourto`   | Zavírací doba výdejny. |
| `pickupchannelid`     | ID kanálu obchodu výdejny. |
| `packingslipid`      | ID dodacího listu k objednávce, která bude vyzvednuta. |
| `confirmationid`      | ID potvrzení objednávky která bude vyzvednuta. (Toto ID se někdy označuje jako referenční ID kanálu.) |

Další informace o funkcích přihlášení zákazníků a vyhledávání objednávek naleznete v části [Nastavení geodetekcce a přesměrování](geo-detection-redirection.md) a [Povolení vyhledávání objednávek pro pokladny hostů](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Objednávka připravena k vyzvednutí

Typ oznámení *objednávka je připravena k vyzvednutí* se spustí, když je objednávka označena jako zabalená a je nastaven způsob doručení **Vyzvednutí zákazníka** na jedné nebo více řádcích objednávky.

> [!NOTE]
> Typ oznámení o připravenosti k vyzvednutí objednávky je zastaralý a používá se typ oznámení o dokončení balení. Tento typ oznámení je přizpůsoben podle způsobu doručení.

### <a name="order-shipped"></a>Expedované objednávky

Typ oznámení *objednávka je poslána* se spustí, když je fakturována objednávka, která má způsob dodání bez vyzvednutí na prodejně.

> [!NOTE]
> Typ oznámení o odeslání objednávky je zastaralý a používá se typ oznámení o fakturaci objednávky. Tento typ oznámení je přizpůsoben podle způsobu doručení.

### <a name="order-invoiced"></a>Vyfakturování objednávky

Typ oznámení *objednávka byla vyfakturována* se spustí při vyfakturování objednávky v POS nebo centrále Commerce.

### <a name="issue-gift-card"></a>Vydat dárkový poukaz

Typ oznámení *vydat dárkovou kartu* se spustí, když je fakturována prodejní objednávka, která obsahuje produkt typu dárkové karty.

> [!NOTE]
> Příjemci dárkové karty se odešle e-mail s oznámením o vydání dárkové karty. Příjemce dárkové karty je uveden v ústředí Commerce na samostatném řádku prodejní objednávky na kartě **Balení** pod **Podrobnosti řádku**. Lze jej zadat ručně nebo programově.

Typ oznámení o vydání dárkové karty podporuje následující další zástupné symboly.

| Název zástupného textu      | Účel |
| --------------------- | ------- |
| `giftcardnumber`        | Číslo dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardbalance`       | Zůstatek dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardmessage`       | Zpráva dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardpin`         | PIN kód dárkového poukazu pro výrobky typu dárkového poukazu. (Tento zástupný text je specifický pro externí dárkové poukazy.) |
| `giftcardexpiration`    | Datum vypršení dárkového poukazu pro výrobky typu dárkového poukazu. (Tento zástupný text je specifický pro externí dárkové poukazy.) |
| `giftcardrecipientname` | Jméno příjemce dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardbuyername`     | Jméno kupce dárkového poukazu pro výrobky typu dárkového poukazu. |

Další informace o dárkových kartách viz [Digitální dárkové karty pro elektronický obchod](digital-gift-cards.md) a [Podpora externích dárkových karet](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Zrušení objednávky

Typ oznámení *zrušení objednávky* se spustí při zrušení objednávky v centrále Commerce.

### <a name="customer-created"></a>Zákazník byl vytvořen.

Typ oznámení *zákazník byl vytvořen* se spustí při vytvoření nové entity zákazníka v centrále Commerce.

### <a name="b2b-prospect-approved"></a>Potenciální zákazník B2B schválen

Typ oznámení *Potenciální zákazníka B2B schválen* se spustí, když je žádost potenciálního zákazníka o registraci schválena v ústředí Commerce. Další informace o tom, jak schválit nebo zamítnout potenciální zákazníky B2B, viz [Nastavení uživatele správce pro nového obchodního partnera](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Typ oznámení o schválení potenciálního zákazníka B2B podporuje následující další zástupné symboly.

| Název zástupného textu | Účel                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | Křestní jméno B2B potenciálního zákazníka tak, jak je zadáno v přihlášce. |
| `lastname`         | Příjmení B2B potenciálního zákazníka tak, jak je zadáno v přihlášce. |
| `company`          | Název společnosti žadatele tak, jak je zadáno v přihlášce. |
| `email`            | E-mailová adresa potenciálního zákazníka tak, jak je zadána v přihlášce.   |
| `zipcode`          | PSČ primární adresy potenciálního zákazníka. |
| `comments`         | Komentář, který zájemce zadal do přihlášky. |
| `storename`        | Název kanálu, kde byl potenciální zákazník vytvořen. |
| `storeurl`         | Ve výchozím nastavení prázdné. K použití tohoto zástupného symbolu je nutné vytvořit vlastní rozšíření. |

### <a name="b2b-prospect-rejected"></a>Potenciální zákazník B2B zamítnut

Typ oznámení *Potenciální zákazníka B2B zamítnut* se spustí, když je žádost potenciálního zákazníka o registraci zamítnuta v ústředí Commerce. Další informace o tom, jak schválit nebo zamítnout potenciální zákazníky B2B, viz [Nastavení uživatele správce pro nového obchodního partnera](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Typ oznámení o zamítnutí potenciálního zákazníka B2B podporuje následující další zástupné symboly.

| Název zástupného textu | Účel                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | Křestní jméno B2B potenciálního zákazníka tak, jak je zadáno v přihlášce. |
| `lastname`         | Příjmení B2B potenciálního zákazníka tak, jak je zadáno v přihlášce. |
| `company`          | Název společnosti žadatele tak, jak je zadáno v přihlášce. |

## <a name="create-an-email-template"></a>Vytvoření šablonu e-mailu

Než budete moci mapovat konkrétní transakční událost na e-mailovou šablonu, musíte ji vytvořit.

Šablonu e-mailu vytvoříte takto:

1. V centrále Commerce přejděte do nabídky **Retail a Commerce \> Nastavení centrály \> E-mailové šablony organizace** nebo **Správa organizace \> Nastavení \> E-mailové šablony organizace**.
1. Zvolte **Nové**.
1. Pod možností **Obecné** nastavte následující pole:

    - **ID e-mailu** – E-mailové ID je jedinečný identifikátor šablony. Je to hodnota, která se zobrazí, když vyberete šablonu pro mapování na událost.
    - **Popis e-mailu** - Pomocí tohoto volitelného pole můžete zadat popis šablony. Zadaná hodnota se zobrazí pouze v Commerce Headquarters.
    - **Jméno odesílatele** - Jméno, které zadáte, se objeví v poli „Odesílatel“ většiny e-mailových klientů.
    - **E-mail odesílatele** - Zadejte e-mailovou adresu, která má být použita pro e-maily odeslané pomocí této šablony.
    - **Výchozí kód jazyka** - Toto pole určuje lokalizovanou verzi e-mailu, který je odeslán ve výchozím nastavení, pokud kanál, který vyvolává tuto šablonu, neudává jazyk.

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

| Název zástupného textu     | Účel                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Jméno zákazníka, který vystavil objednávku.               |
| `customeraddress`      | Adresa zákazníka.                                 |
| `customeremailaddress` | E-mailová adresa, kterou zákazník zadal při placení.     |
| `salesid`              | ID prodejní objednávky.                                   |
| `orderconfirmationid`  | Mezikanálové ID, které bylo vygenerováno při vytváření objednávky.   |
| `channelid`            | ID maloobchodního nebo online kanálu, prostřednictvím kterého byla objednávka zadána. |
| `deliveryname`         | Název, který je uveden pro doručovací adresu.         |
| `deliveryaddress`      | Dodací adresa pro expedované objednávky.                     |
| `deliverydate`         | Datum dodání.                                           |
| `shipdate`             | Datum expedice.                                               |
| `modeofdelivery`       | Způsob doručení objednávky.                              |
| `ordernetamount`       | Celková částka objednávky snížená o celkovou daň.         |
| `discount`            | Celková sleva objednávky.                            |
| `charges`              | Celkové poplatky za objednávku.                             |
| `tax`                  | Celková daň objednávky.                                 |
| `total`                | Celková částka objednávky.                              |
| `storename`            | Název obchodu, kde byla vystavena objednávka.            |
| `storeaddress`         | Adresa obchodu, který vystavil objednávku.              |
| `storeopenfrom`        | Otevírací čas obchodu, který vystavil objednávku.         |
| `storeopento`          | Zavírací čas obchodu, který vystavil objednávku.         |
| `pickupstorename`      | Název obchodu, kde bude objednávka vyzvednuta.\*   |
| `pickupstoreaddress`   | Adresa obchodu, kde bude objednávka vyzvednuta.\* |
| `pickupopenstorefrom`  | Otevírací čas obchodu, kde bude objednávka vyzvednuta.\* |
| `pickupopenstoreto`    | Zavírací čas obchodu, kde bude objednávka vyzvednuta.\* |
| `pickupchannelid`     | ID kanálu obchodu, který je určen pro způsob vyzvednutí.\* |
| `packingslipid`        | ID dodacího listu, který byl vygenerován při zabalení řádků v objednávce.\* |

\* Tyto zástupné symboly vracejí data pouze v případě, že jsou použity pro typ oznámení **Objednávka připravena k vyzvednutí**. 

### <a name="order-line-placeholders-sales-line-level"></a>Zástupné texty řádku objednávky (úroveň řádku prodeje)

Následující zástupné texty získávají a zobrazují data pro jednotlivé produkty (řádky) v prodejní objednávce.

| Název zástupného textu               | Účel |
|--------------------------------|-------------------|
| `productid`                      | <p>ID produktu. Toto ID odpovídá variantám.</p><p><strong>Poznámka:</strong> Tento zástupný symbol byl nahrazen za `lineproductrecid`.</p> |
| `lineproductrecid`               | ID produktu. Toto ID odpovídá variantám. Jedinečně identifikuje položku na úrovni variant. |
| `lineitemid`                     | ID úrovně produktu. (Toto ID neodpovídá variantám.) |
| `lineproductvariantid`           | ID varianty produktu. |
| `lineproductname`                | Název produktu. |
| `lineproductdescription`         | Popis produktu. |
| `linequantity`                   | Počet jednotek, které byly objednány pro řádek, plus měrná jednotka (například **ks**, nebo **pár**). |
| `lineunit`                       | Měrná jednotka řádku. |
| `linequantity_withoutunit`       | Počet jednotek, které byly objednány pro řádek, bez měrné jednotky. |
| `linequantitypicked`             | Když je použita událost **PickOrder**, počet jednotek, které byly vydány. V opačném případě **0** (nula). |
| `linequantitypicked_withoutunit` | Když je použita událost **PickOrder**, počet jednotek, které byly vydány, bez měrné jednotky. V opačném případě **0** (nula). |
| `linequantitypacked`             | Když jsou použity události **PackOrder** a **Objednávka připravena k vyzvednutí**, počet jednotek, které byly zabaleny. V opačném případě **0** (nula). |
| `linequantitypacked_withoutuom`  | Když jsou použity události **PackOrder** a **Objednávka připravena k vyzvednutí**, počet jednotek, které byly zabaleny, bez měrné jednotky. V opačném případě **0** (nula). |
| `linequantityshipped`            | Vždy **0**, s výjimkou případů, kdy jsou použity konkrétní události, jak je popsáno v dalším řádku. |
| `linequantityshipped_withoutuom` | Když je použita událost **ShipOrder**, počet jednotek, které byly vydány, bez měrné jednotky. V opačném případě **0** (nula). |
| `lineprice`                      | Cena za jednotku. |
| `linenetamount`                  | Cena řádku po použití počtu jednotek a slevy. |
| `linediscount`                   | Sleva na jednotlivou jednotku. |
| `lineshipdate`                   | Datum expedice pro řádek. |
| `linedeliverydate`               | Datum dodání pro řádek. |
| `linedeliverymode`               | Způsob dodání pro řádek. |
| `linedeliveryaddress`            | Adresa dodání pro řádek. |
| `linepickupdate`                 | Datum vyzvednutí, které zákazník uvedl u objednávek, které používají způsob vyzvednutí. |
| `linepickuptimeslot`             | Časový rozsah vyzvednutí, které zákazník uvedl u objednávek, které používají způsob vyzvednutí. |
| `giftcardnumber`                 | Číslo dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardbalance`                | Zůstatek dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardmessage`                | Zpráva dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardpin`                    | PIN dárkové karty pro výrobky typu dárkového poukazu. (Tento zástupný text je specifický pro externí dárkové poukazy.) |
| `giftcardexpiration`             | Datum vypršení dárkového poukazu pro výrobky typu dárkového poukazu. (Tento zástupný text je specifický pro externí dárkové poukazy.) |
| `giftcardrecipientname`          | Jméno příjemce dárkového poukazu pro výrobky typu dárkového poukazu. |
| `giftcardbuyername`              | Jméno kupce dárkového poukazu pro výrobky typu dárkového poukazu. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Formát zástupných textů řádků objednávky v těle e-mailové zprávy

Když vytvoříte HTML pro jednotlivé řádky objednávky v těle e-mailové zprávy, ohraničte opakující se blok HTML a zástupné texty pro řádky s následujícími zástupnými texty. Všimněte si, že zástupné texty jsou uvnitř značek komentářů HTML.

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

- Zástupný text **%message%** se používá k vložení textu účtenky do e-mailu. Aby bylo zajištěno, že tělo účtenky je správně vykresleno, obklopte zástupný text **%message%** HTML značkami **&lt;pre&gt;** a **&lt;/pre&gt;**.
- Zástupný symbol **%receiptid%** lze použít k zobrazení QR kódu nebo čárového kódu, který představuje ID účtenky. (QR kódy a čárové kódy jsou dynamicky generovány a obsluhovány službou třetí strany.) Další informace o tom, jak zobrazit QR kód nebo čárový kód v e-mailovém potvrzení, najdete v části [Přidání QR kódu nebo čárového kód do transakčních a přijímacích e-mailů](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Odeslání HTML e-mailu

Poté, co jste vytvořili a otestovali HTML pro tělo své zprávy, musí být odesláno do Commerce Headquarters. V současné době nelze HTML e-mailu exportovat. Proto musíte zachovat hlavní kopii vašeho HTML mimo Commerce Headquarters.

Chcete-li nahrát novou nebo upravenou HTML e-mailovou šablonu, postupujte takto.

1. V Commerce Headquarters přejděte na **Retail a Commerce \> Nastavení Headquarters \> Šablony e-mailu organizace**.
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

[Nastavení účtenek e-mailem](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Odesílání účtenek e-mailem z Modern POS](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
