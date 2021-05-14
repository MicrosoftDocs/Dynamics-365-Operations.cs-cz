---
title: Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat volitelné funkce prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a93429e836d818458f11f6f6821fda237edc291
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936973"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak konfigurovat volitelné funkce prostředí vyhodnocení Microsoft Dynamics 365 Commerce.

## <a name="prerequisites"></a>Předpoklady

Chcete-li vyhodnotit funkce transakčního e-mailu, musí být splněny následující předpoklady:

- Máte k dispozici e-mailový server (Simple Mail Transfer Protocol \[SMTP\]), který lze použít z předplatného Microsoft Azure, kde jste zřídili prostředí vyhodnocení.
- Máte k dispozici plně kvalifikovaný název domény (FQDN)/IP adresu, číslo portu SMTP a podrobnosti o ověřování.

## <a name="configure-the-image-back-end"></a>Konfigurace back-endu bitové kopie

### <a name="find-your-media-base-url"></a>Hledání základní adresy URL média

> [!NOTE]
> Před provedením tohoto postupu je třeba provést kroky uvedené v tématu [nastavení webu v Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).

1. Přihlaste se k nástroji pro tvorbu webu Commerce pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Otevřete stránku **Fabrikam**.
1. V nabídce vlevo vyberte **Mediální knihovna**.
1. Vyberte libovolný obrázek.
1. V inspektoru vlastnosti vpravo najděte vlastnost **Veřejná adresa URL**. Hodnota je URL. Následuje příklad:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Nahraďte poslední identifikátor v adrese URL (**MA1nQC** v předchozím příkladu) s řetězcem **search?fileName=**. Takto vypadá adresa URL po provedení této změny:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Tato adresa URL je základní adresa URL média. Poznamenejte si ji.

### <a name="update-the-media-base-url"></a>Aktualizace základní adresy URL média

1. Přihlaste se do centrály Commerce.
1. Pomocí nabídky v levé části přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Profily kanálu**.
1. Vyberte možnost **Upravit**.
1. V části **Vlastnosti profilu** nahraďte hodnotu vlastnosti **Základní adresa URL serveru médií** základní adresou URL médií, kterou jste vytvořili dříve.
1. Vyberte kanál, který je nazvaný **scXXXXXXXXX**.
1. Ve **Vlastnostech profilu** vyberte **Přidat**.
1. U vlastnosti, která byla přidána, vyberte **Základní adresa URL serveru médií** jako klíč vlastnosti. Jako hodnotu vlastnosti zadejte adresu URL základních médií, kterou jste vytvořili dříve.
1. Zvolte **Uložit**.

## <a name="configure-and-test-the-email-server"></a>Konfigurace a test e-mailového serveru

> [!NOTE]
> Server SMTP nebo zadaná e-mailová služba musí být v rámci předplatného Azure, které používáte pro dané prostředí, přístupné.

1. Přihlaste se do centrály Commerce.
1. Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení centrály \> Parametry \> Parametry e-mailu**.
1. Na kartě **Nastavení SMTP** do pole **Server odchozí pošty** zadejte FQDN nebo IP adresu serveru SMTP nebo e-mailové služby.
1. Do pole **Číslo portu SMTP** zadejte číslo portu. (Pokud nepoužíváte protokol Secure Sockets Layer \[SSL\], je výchozí číslo portu **25**.)
1. Pokud je vyžadováno ověření, zadejte hodnoty do polí **Uživatelské jméno** a **Heslo**.
1. Zvolte **Uložit**.
1. Vyberte **Aktualizovat**.
1. Na kartě **Testovací e-mail** v poli **Poskytovatel e-mailu** vyberte **SMTP**.
1. V poli **Příjemce** zadejte e-mailovou adresu, na kterou má být doručen testovací e-mail.
1. Vyberte **Odeslat testovací e-mail**.

## <a name="configure-email-templates"></a>Konfigurace e-mailových šablon

Pro každou transakční událost, pro kterou chcete odeslat e-maily, musíte aktualizovat e-mailovou šablonu platnou adresou odesílatele.

1. Přihlaste se do centrály Commerce.
1. Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení centrály \> Parametry \> Šablony e-mailu organizace**.
1. Vyberte možnost **Zobrazit seznam**.
1. Pro každou šablonu v seznamu postupujte takto:

    1. Do pole **Adresa odesílatele** zadejte e-mailovou adresu odesílatele.
    1. Volitelné: Do pole **Jméno odesílatele** zadejte jméno, které má být použito jako jméno odesílatele.

1. Zvolte **Uložit**.

## <a name="customize-email-templates"></a>Přizpůsobení šablon e-mailu

Šablony e-mailů je vhodné přizpůsobit tak, aby používaly různé obrázky. Nebo můžete chtít aktualizovat odkazy v šablonách tak, aby byly v prostředí vyhodnocení. Tento postup vysvětluje, jak stáhnout výchozí šablony, přizpůsobit je a aktualizovat šablony v systému.

1. Ve webovém prohlížeči můžete stáhnout [soubor zip vyhodnocení výchozích šablon e-mailu Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) do místního počítače. Tento soubor obsahuje následující dokumenty HTML:

    - Šablona potvrzení objednávky
    - Šablona dárkového poukazu
    - Šablona nové objednávky
    - Šablona objednávky balení
    - Šablona objednávky výdeje

1. Přizpůsobte šablony pomocí textu nebo editoru HTML. Další informace naleznete v části [podporované tokeny](#supported-tokens-in-the-email-template) dále v tomto tématu.
1. Přihlášení do Commerce.
1. Pomocí nabídky v levé části přejděte na **Moduly \> Správa organizace \> Nastavení \> Šablony e-mailu organizace**.
1. Rozbalením seznamu v levé části zobrazíte všechny šablony.
1. U každé šablony, kterou chcete přizpůsobit, postupujte následujícím způsobem:

    1. Vyberte šablonu v seznamu.
    1. V části **Obsah e-mailové zprávy** vyberte odpovídající jazykovou verzi ze seznamu. (Výchozí kód jazyka je **en-us**.)
    1. V části **Obsah e-mailové zprávy** vyberte **Upravit**. Zobrazí se podokno **Odeslat šablonu e-mailu**.
    1. Vyberte **Procházet** a najděte soubor HTML, který má přizpůsobený obsah.
    1. Vyberte **Odeslat**. Šablona se nahraje do systému a zobrazí se náhled.
    1. Vyberte **OK**.
    1. Volitelné: Upravte vlastnost **Předmět** šablony.
    1. Zvolte **Uložit**.

### <a name="supported-tokens-in-the-email-template"></a>Podporované tokeny v šabloně e-mailu

Když je e-mail vykreslován, budou tyto tokeny nahrazeny skutečnými hodnotami, které platí pro zákazníka a jeho objednávku.

#### <a name="sales-order"></a>Prodejní objednávka

Následující tokeny se vztahují na celkovou prodejní objednávku.

| Název tokenu | Token |
|-------------------|-------|
| Číslo objednávky      | %salesid% |
| Jméno zákazníka   | %customername% |
| Adresa dodání  | %deliveryaddress% |
| Fakturační adresa   | %customeraddress% |
| Datum objednávky        | %shipdate% |
| Způsob doručení     | %modeofdelivery% |
| Sleva          | %discount% |
| DPH         | %tax% |
| Celková hodnota objednávky       | %total% |

#### <a name="sales-line"></a>Řádek prodeje

Následující tokeny jsou nahrazeny hodnotami pro každý produkt v objednávce.

> [!NOTE]
> Token **Product list - start** vložte na začátek bloku HTML, který se opakuje u každého produktu, a token **Product list - end** na konec bloku.

| Název tokenu      | Token |
|------------------------|-------|
| Seznam produktů - začátek   | \<!--%tablebegin.salesline% --\> |
| Seznam produktů - konec     | \<!--%tableend.salesline%--\> |
| Název produktu           | %lineproductname% |
| popis            | %lineproductdescription% |
| Množství               | %linequantity% |
| Cena řádkové jednotky        | %lineprice% (ověřit) |
| celkem řádkových položek        | %linenetamount% |
| řádková sleva          | %linediscount% |
| Datum expedice              | %lineshipdate% |
| Způsob zásobování     | %linedeliverymode% |
| adresa dodání       | %linedeliveryaddress% |
| Prodejní jednotka řádku | %lineunit% |

## <a name="additional-resources"></a>Další prostředky

[Přehled prostředí vyhodnocení Dynamics 365 Commerce](cpe-overview.md)

[Zřízení prostředí vyhodnocení Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace prostředí vyhodnocení Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](cpe-bopis.md)

[Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]