---
title: Nastavení služby Apple Pay s terminálem Adyen v Dynamics 365 Commerce
description: Tento článek popisuje, jak nastavit Apple Pay s Adyen v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780358"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Nastavení služby Apple Pay s terminálem Adyen v Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tento článek popisuje, jak nastavit Apple Pay s Adyen v Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| Apple Pay | Apple Pay, známé také jako „tlačítko Apple Pay“, je nabídka plateb peněženkou, která je podporována prostřednictvím konektoru Adyen. Umožňuje prostředí zákazníků a integrace, které podporuje konektor Microsoft Dynamics 365 Apple Pay Connector. |
| Peněženka | Typ platby, který nezahrnuje tradiční platební charakteristiky, jako je rozsah bankovního identifikačního čísla (BIN) a datum vypršení platnosti, které se používají k rozlišení typů kreditních a debetních karet. |

Dynamics 365 Commerce nabízí okamžitou integraci pro Apple Pay při použití služby platební brány Adyen. Apple Pay je platební metoda digitální peněženky, která využívá účet obchodníka Apple Pay v koordinaci s platební službou Adyen. Po nakonfigurování je tlačítko Apple Pay dostupné jako volitelná platební metoda, která je součástí stránky placení objednávky prodejny. Tlačítko Apple Pay se zobrazuje jako možnost platby pouze pro podporovaná zařízení Apple Pay. Když uživatelé vyberou **Apple Pay** v podporovaném prohlížeči nebo zařízení, jsou přesměrováni k dokončení platby přímo pomocí služby Apple Pay. Poté se vrátí do online obchodu k dokončení objednávky.

Odkaz na konektor Dynamics 365 Payment Connector pro Apple Pay se použije vedle konektoru Dynamics 365 Payment Connector pro Adyen k umožnění Apple Pay a plateb kreditní kartou na webu. Apple Pay lze také nakonfigurovat pro použití v obchodech, které mají platební terminály Adyen, které používají Dynamics 365 Payment Connector for Adyen s pokladním místem (POS) Commerce. V tomto případě Dynamics 365 Payment Connector for Adyen zpracovává přiložení zařízení Apple Payment přes terminál.

## <a name="prerequisites"></a>Předpoklady

Používání služby Apple Pay s Adyen v obchodě vyžaduje účet obchodníka Apple. Informace o tom, jak nastavit Apple Pay ve vaší testovací zákaznické oblasti, viz [Integrace Apple Pay Drop-in](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Informace o tom, co dělat, když jste připraveni začít pracovat ve vašem produkčním prostředí, viz [Spuštění naostro](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Platební metoda Apple Pay musí být také integrována s vaším účtem Adyen. Adyen vám může pomoci nastavit platební metodu a může také pomoci zajistit, že domény, pro které budete certifikát používat, jsou přiřazeny k použití s certifikátem.

Chcete-li zapnout příznak vylepšené funkce peněženky v Commerce headquarters, přejděte na **Pracovní prostory \> Správa funkcí** a vyhledejte funkci **Vylepšená podpora peněženky a vylepšení plateb**. Vyberte funkci a poté vyberte tlačítko **Zapnout**. Po aktivaci funkce spusťte distribuční plán **1110**, aby byla změna dostupná ve všech kanálech.

## <a name="map-the-apple-pay-payment-method"></a>Mapování platební metody Apple Pay

Apple Pay je platební metoda digitální peněženky. Informace o tom, jak nastavit mapování plateb pro Apple Pay, viz [Podpora plateb peněženkou](../wallets.md).

Mapování metody platby Apple Pay v Commerce headquarters provedete následovně.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Platební metody \> Typy karet**.
1. Pro přidání řádku pro Apple Pay, klikněte na **Nový** a zadejte následující hodnoty:

    - **ID:** ApplePay
    - **Název elektronické platby:** Apple Pay
    - **Typ:** Peněženka
    - **Vydavatel:** Apple

1. Vyberte **Mapování procesoru** a otevřete dialogové okno **Metody mapování plateb zpracovatele**. Sloupec **Nemapované platební metody zpracovatele** uvádí podporované platební metody pro každý dostupný konektor (Adyen, PayPal a Apple).
1. Namapujte nepodporované platební metody, které chcete pro konektor **Dynamics 365 Payment Connector pro Adyen** (pro použití v POS) i konektor **Dynamics 365 Payment Connector pro Apple Pay** (pro použití v online kanálech).
1. Pro každý řádek mapování ve sloupci **Nemapované platební metody zpracovatele** vyberte řádek na podporu a poté vyberte **Přidat** pro přesunutí výběru do sloupce **Mapované způsoby platby zprostředkovatele**.
1. Vyberte **OK** a poté na stránce **Typy karet** vyberte **Uložit**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Nastavení certifikátu Apple Pay pro web

Pro každý web musíte nahrát soubor přidružení domény (označovaný také jako certifikát Apple Pay), jak je popsáno v [Dokumentaci Adyen Apple Pay](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). K nahrání souboru přidružení domény do knihovny médií pro váš web můžete použít tvůrce webů Commerce.

K nastavení certifikátu Apple Pay v nástroji pro tvorbu webů postupujte takto.

1. Stáhněte si certifikát (soubor přidružení domény) z [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Přidejte příponu .txt do souboru přidružení domény.
1. V nástroji pro tvorbu stránek [nahrajte](../upload-serve-static-files.md) soubor přidružení domény do knihovny médií vašeho webu.
1. Přejděte na **Adresy URL**.
1. Zvolte **Nový \> Nová adresa URL**.
1. V dialogovém okně **Nová adresa URL** vyberte **Prostředek knihovny médií**.
1. V poli **cesta adresy URL** zadejte cestu URL (pokud již není zadána). Po základní adrese URL domény zadejte následující požadovaný řetězec Apple: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Zvolte **Další**. Knihovna médií zobrazuje se všechny nahrané prostředky médií typu **dokument** (.txt).
1. Vyberte soubor přiřazení domény, který má být obsloužen požadavky na adresu URL, kterou jste definovali dříve.
1. Vyberte **Vytvořit**.

V tomto okamžiku se vytvořená adresa URL nachází ve stavu konceptu. K dokončení procesu publikujte adresu URL. Soubor, na který adresa URL odkazuje, nebude vrácen, dokud adresu URL nepublikujete.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Konfigurace internetového obchodu Commerce pro Apple Pay

Chcete-li nakonfigurovat internetový obchod Commerce pro používání Apple Pay, postupujte takto.

1. V Commerce headquarters přejděte na možnost **Maloobchodní a velkoobchodní prodej \> Kanály \> Online obchody**.
1. Vyberte hodnotu **ID maloobchodního kanálu** kanálu internetového obchodu webu.
1. Na pevné záložce **Platební účty** přidejte konektor **Dynamics 365 Payment Connector pro Adyen**, pokud již není nastaven, podle pokynů v části [Nastavení konektoru Dynamics 365 Payment Connector pro Adyen](adyen-connector-setup.md).
1. Po nakonfigurování konektoru Adyen vyberte **Přidat** pro přidání konektoru **Dynamics 365 Payment Connector pro Apple Pay**.
1. Zadejte hodnoty pro vlastnosti obchodníka konektoru.

    | Vlastnost               | Popis | Povinný | Automaticky nastavit | Ukázková hodnota |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Název sestavení          | Název sestavení pro Dynamics 365 Payment Connector pro Apple Pay. | Ano | Ano | Binární název |
    | ID účtu služby     | Jedinečný identifikátor pro nastavení vlastností obchodníka. Tento identifikátor je vyznačen na platebních transakcích a identifikuje vlastnosti obchodníka, které by měly následné procesy (jako je fakturace) používat. | Ano | Ano | Guid |
    | ID účtu obchodníka    | Zadejte jedinečný identifikátoru obchodníka Adyen. Tato hodnota je poskytnuta, když se zaregistrujete u Adyen, jak je popsáno v části [Zaregistrovat se u Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ano | Číslo | MerchantIdentifier |
    | Klíč Cloud API          | Zadejte klíč Adyen cloud API. Můžete získat tento klíč postupováním podle pokynů v [Jak získat klíč API](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ano | Číslo | abcdefg |
    | Prostředí brány    | Zadejte prostředí brány Adyen k mapování. Možné hodnoty jsou **Testovací** a **Živé**. Toto pole byste měli nastavit na **Živé** pouze pro produkční zařízení a transakce. | Ano | Ano | Aktivní |
    | Podporované měny   | Zadejte měny, které by měl konektor zpracovat. Ve scénářích přítomnosti karet může Adyen podporovat další měny prostřednictvím [dynamické konverze měn](https://www.adyen.com/pos-payments/dynamic-currency-conversion) po odeslání požadavku transakce na platební terminál. Chcete-li získat seznam podporovaných měn, kontaktujte podporu Adyen. | Ano | Ano | USD;EUR |
    | Podporované typy úhrad | Zadejte typy platidel, které by měl konektor zpracovat. | Ano | Ano | ApplePay |

1. Po zadání informací o obchodníkovi spusťte plánovanou úlohu distribuce konfiguraci kanálu **1070**.

## <a name="configure-commerce-pos-for-apple-pay"></a>Konfigurace POS Commerce na Apple Pay

Konfigurace POS využívá konfigurace pole **Služba EFT** hardwarového profilu pro Dynamics 365 Payment Connector for Adyen. V Commerce headquarters nakonfigurujte službu elektronického převodu prostředků (EFT) pro konektor Dynamics 365 Payment Connector pro Adyen, jak je popsáno v tématu [Nastavení sekce hardwarového profilu Dynamics 365 POS](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Ujistěte se, že přidáte **ApplePay** do seznamu typů platidel v poli **Podporované typy platidel**. Pro oddělení typů platidel v seznamu použijte středníky (;).

Mapování zpracovatele pro konektor Adyen zachycuje typy karet peněženky, které Apple Pay používá na terminálu POS.

### <a name="configure-content-security-policies-in-site-builder"></a>Konfigurace zásad zabezpečení obsahu v nástroji pro tvorbu webu

Než nakonfigurujete své fragmenty nebo stránky pomocí Apple Pay, musíte zajistit, aby byly vaše zásady zabezpečení obsahu (CSP) nakonfigurovány ve tvůrci webů Commerce pro váš web.

Ke konfiguraci zásad zabezpečení obsahu v konfigurátoru webu postupujte takto.

1. Přejděte na **Nastavení webu \> Rozšíření**.
1. Na kartě **Zásady zabezpečení obsahu** vyberte **Přidat** pro přidání řádku, který má `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js`, do částí **child-src**, **connect-src**, **frame-src**, **img-src**, **script-src** a **style-src**.
1. Po dokončení vyberte **Uložit a pulikovat** pro uložení změn.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Nastavení Apple Pay jako možnosti platby u pokladny

Chcete-li nastavit Apple Pay jako platební možnost na stránce (neexpresní) pokladny vašeho webu, postupujte takto.

1. V konfigurátoru webů vyberte **Fragmenty** a poté vyberte fragment pokladny vašeho webu.
1. Vyberte možnost **Upravit**.
1. Ve slotu **Kontejner sekce poklady** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Výběr modulů** vyberte modul **Apple Pay** a poté klikněte na tlačítko **OK**.
1. Zvolte možnost **Uložit**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Nastavení pro modul **Apple Pay** jsou zabudována do modulu a propojují se s nakonfigurovaným konektorem Dynamics 365 Payment Connector pro Apple Pay, který je nastaven pro online kanál v Commerce headquarters.

### <a name="apple-pay-payment-behavior"></a>Chování plateb Apple Pay

Tlačítko platby **Apple Pay** se zobrazuje pouze na podporovaných zařízeních Apple Pay (iPhony, iPady a prohlížeče Safari, které podporují Apple Pay). Pokud uživatel nepoužívá jedno z těchto zařízení, tlačítko platby **Apple Pay** je skryto.

Když uživatel vybere tlačítko platby **Apple Pay**, zobrazí se dialogové okno **Apple Pay**. Tam se uživatel může ověřit proti svému zařízení nebo prohlížeči Apple Pay. Dialogové okno **Apple Pay** zobrazuje souhrn částky objednávky a platební metodu, kterou uživatel nakonfiguroval pro svou Apple Wallet. Uživatel si může tyto údaje prohlédnout a poté vybrat **Zaplatit** pro provedení platby. Po dokončení platby je uživatel přesměrován na stránku webu **Objednávka byla provedena**, která zobrazuje podrobné shrnutí objednávky pro dokončenou transakci.

## <a name="additional-resources"></a>Další prostředky

[Časté dotazy k platbám](payments-retail.md)

[Modul pokladny](../add-checkout-module.md)

[Platební modul](../payment-module.md)
