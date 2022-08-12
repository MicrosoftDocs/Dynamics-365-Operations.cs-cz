---
title: Konfigurace Google Pay s Adyen
description: Tento článek popisuje, jak nakonfigurovat Google Pay s Adyen v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115024"
---
# <a name="configure-google-pay-with-adyen"></a>Konfigurace Google Pay s Adyen

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat Google Pay s Adyen v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce nabízí okamžitou integraci pro Google Pay při použití služby platební brány Adyen. Google Pay je platební metoda digitální peněženky, která využívá účet obchodníka Google Pay v koordinaci s platební službou Adyen. Po nakonfigurování je tlačítko Google Pay dostupné jako volitelná platební metoda při online placení objednávky. Když uživatelé vyberou **Google Pay** v podporovaném prohlížeči nebo zařízení, jsou přesměrováni k dokončení platby přímo pomocí služby Google Pay. Poté se vrátí do online obchodu k dokončení objednávky.

Když je služba Google Pay používána s modulem expresní platby v Commerce, informace o platebním účtu uživatele se automaticky předvyplní do formuláře platby, aby uživatel rychleji prošel procesem platby. Commerce obsahuje modul pro expresní platby, který umožňuje chování expresních pokladen. Modul pro expresní platby lze použít ve fragmentu, který lze zahrnout na stránku pokladny nebo košíku. Odkaz na konektor Dynamics 365 Payment Connector pro Google Pay se použije vedle konektoru Dynamics 365 Payment Connector pro Adyen jak pro expresní, tak pro běžnou platbu, když je nakonfigurován PayPal. Google Pay lze také nakonfigurovat s platebními terminály Adyen a obchodním místem prodeje (POS) pro použití v obchodě.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| Google Pay | Google Pay, známé také jako „tlačítko Google Pay“, je nabídka plateb peněženkou, která je podporována prostřednictvím konektoru Adyen. Umožňuje prostředí zákazníků a integrace, které podporuje konektor Dynamics Google Pay Connector. |
| Peněženka | Typ platby, který nezahrnuje tradiční platební charakteristiky, jako je rozsah bankovního identifikačního čísla (BIN) a datum vypršení platnosti, které se používají k rozlišení typů kreditních a debetních karet. |
| Modul expresní platby | Modul Dynamics 365 Commerce, který podporuje rychlejší zaplacení při použití podporovaných platebních metod. |

## <a name="prerequisites"></a>Předpoklady

Používání služby Google Pay s Adyen v obchodě vyžaduje účet Google Merchant. Informace o tom, jak nastavit účet Google Merchant, naleznete v [dokumentaci Adyen ve službě Google Pay](https://docs.adyen.com/payment-methods/google-pay/) [kontrolním seznamu integrace](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist) Google.

Platební metoda Google Pay musí být také integrována s vaším účtem Adyen. Pokyny pro integraci odkazu viz [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Musíte také povolit vylepšenou funkci peněženky v Dynamics 365 Commerce headquarters. Přejděte na **Pracovní prostory \> Správa funkcí**, vyhledejte funkci **Vylepšená podpora peněženky a vylepšení plateb**, funkci vyberte a poté vyberte **Aktivovat**. Po aktivaci funkce spusťte distribuční plán **1110**, aby byla změna dostupná ve všech kanálech.

## <a name="map-the-google-pay-payment-method"></a>Mapování platební metody Google Pay

Google Pay je platební metoda digitální peněženky. Informace o tom, jak nastavit mapování plateb pro Google Pay, viz [Podpora plateb peněženkou](../wallets.md).

Chcete-li namapovat platební metodu Google Pay na typy karetních nabídek pro POS i online kanály, postupujte takto.

1. V Commerce Headquarters přejděte na možnost **Retail a Commerce \> Nastavení kanálu \> Platební metody \> Typy karet**.
1. Vyberte **Nový** pro přidání řádku pro Google Pay.
1. Do pole **ID** zadejte **Google Pay**.
1. Do pole **Název elektronické platby** zadejte **Google Pay**.
1. Do pole **Typ** zadejte **Peněženka**.
1. Do pole **Vydavatel** zadejte **Google**.
1. V podokně akcí vyberte **Mapování procesoru** a otevřete dialogové okno **Metody mapování plateb zpracovatele**.
1. Pod **Nemapované platební metody zpracovatele** se zobrazí seznam nenamapovaných metod platby za zpracovatele, z nichž každá je spárována s příslušným konektorem. Chcete-li namapovat nemapované platební metody zpracovatele Google Pay k typům nabídek karet, postupujte pro každý typ nabídky karty takto:

    1. V části **Typy karetních platebních metod** vyberte typ karetní metody.
    1. Ve sloupci **Nemapované platební metody zpracovatele** vyberte konektor **Dynamics 365 Payment Connector pro Adyen** (pro použití na POS) i konektor **Dynamics 365 Payment Connector pro Google Pay** (pro použití v online kanálech).
    1. Vyberte **přidat**. Výběry jsou přidány do sloupce **Mapované způsoby platby zpracovatele**.

1. Po dokončení mapování platebních metod zvolte **Uložit**.
1. Na stránce **Typy karet** vyberte **Uložit**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Konfigurace internetového obchodu Commerce pro Google Pay

Chcete-li nakonfigurovat internetový obchod Commerce pro používání Google Pay, postupujte takto.

1. V Commerce headquarters přejděte na možnost **Maloobchodní a velkoobchodní prodej \> Kanály \> Online obchody**.
1. Vyberte kanál internetového obchodu webu výběrem hodnoty **ID maloobchodního kanálu** kanálu.
1. Na pevné záložce **Platební účty** pod **Konektor** potvrďte, že je uveden konektor **Dynamics 365 Payment Connector pro Adyen**. Pokud není uveden, postupujte podle pokynů v části [Nastavení Dynamics 365 Payment Connector pro Adyen](adyen-connector-setup.md) a přidejte ho.

    > [!NOTE]
    > Ve většině případů konektor **Dynamics 365 Payment Connector pro Adyen** musí být uveden jako první konektor pro váš kanál (první konektor je se také nazývá primární konektor). Poté musí následovat další konektory, které budou použity, jako např. konektory **Dynamics 365 Payment Connector pro PayPal** a **Dynamics 365 Payment Connector pro GooglePay**.

1. Po přidání konektoru **Dynamics 365 Payment Connector pro Adyen** vyberte **Přidat** pro přidání konektoru **Dynamics 365 Payment Connector pro GooglePay**. Potom nastavte následující vlastnosti konektoru.

    | Pole                  | Popis | Povinný | Automaticky nastavit | Ukázková hodnota |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Název sestavení          | Název sestavení pro Dynamics 365 Payment Connector pro GooglePay. | Ano | Ano | *Binární název* |
    | ID účtu služby     | Jedinečný identifikátor pro nastavení vlastností obchodníka. Tento identifikátor je vyznačen na platebních transakcích a identifikuje vlastnosti obchodníka, které by měly následné procesy (jako je fakturace) používat. | Ano | Ano | *GUID* |
    | ID Google Merchant     | Zadejte ID Google Merchant, které je přiřazeno k vašemu účtu Google Merchant. Tato vlastnost je vyžadována pro produkční prostředí, ale pro testovací prostředí je volitelná. Další informace naleznete v tématu <https://pay.google.com/>. | Ano | Číslo | *Číselný identifikátor* |
    | ID účtu obchodníka    | Zadejte jedinečný identifikátoru obchodníka Adyen. Tato hodnota je poskytnuta, když se zaregistrujete u Adyen, jak je popsáno v části [Zaregistrovat se u Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ano | Číslo | *Identifikátor obchodníka* |
    | Klíč Cloud API          | Zadejte klíč Adyen cloud API. Chcete-li získat tento klíč, postupujte podle pokynů v [Jak získat klíč API](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ano | Číslo | "abcdefg" |
    | Prostředí brány    | Prostředí brány Adyen k mapování. Možné hodnoty jsou **Testovací** a **Živé**. Toto pole byste měli nastavit na **Živé** pouze pro produkční zařízení a transakce. | Ano | Ano | "Živé" |
    | Podporované měny   | Měny, které by měl konektor zpracovat. Ve scénářích přítomnosti karet může Adyen podporovat další měny prostřednictvím [dynamické konverze měn](https://www.adyen.com/pos-payments/dynamic-currency-conversion) po odeslání požadavku transakce na platební terminál. Chcete-li získat seznam podporovaných měn, kontaktujte podporu Adyen. | Ano | Ano | "USD;EUR" |
    | Podporované typy úhrad | Typy metod, které by měl konektor zpracovat. | Ano | Ano | "GooglePay" |

1. Po dokončení nastavení vlastností konektoru spusťte úlohu distribučního plánu **1070 (konfigurace kanálu**).

## <a name="configure-commerce-pos-for-google-pay"></a>Konfigurace POS Commerce na Google Pay

Konfigurace POS využívá nastavení pole **Služba EFT** hardwarového profilu pro Dynamics 365 Payment Connector for Adyen. Informace o tom, jak nakonfigurovat službu elektronického převodu prostředků (EFT) pro Dynamics 365 Payment Connector pro Adyen v Commerce headquarters, naleznete v tématu [Nastavení sekce hardwarového profilu Dynamics 365 POS](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Mapování zpracovatele pro konektor Adyen zachycuje typy karet peněženky, které Google Pay používá na terminálu POS.

### <a name="use-the-payment-express-module-with-google-pay"></a>Použití modulu pro expresní platby přes Google Pay

Modul pro expresní platby Commerce spolupracuje s podpůrnými platebními metodami a nabízí zákazníkům webu možnost rychlejšího odbavení použitím informací o jejich účtu platební služby během procesu platby. Modul pro expresní platby odkazuje na nakonfigurované tlačítko konektoru a vrací uživatelem vybrané údaje objednávky (adresa, kontaktní údaje a vybraný způsob platby) k předvyplnění pokladního formuláře.

Když je se službou Google Pay použit expresní modul, pokud zákazníci zvolí tlačítko Google Pay v **Expresní platba**, otevře okno Google Pay iframe. Uživatelé se poté mohou přihlásit ke svému účtu Google a použije k zaplacení transakce doručovací adresu, fakturační adresu, e-mailovou adresu a způsob platby Google Pay.

Když uživatel provede akci v okně Google Pay, je přesměrován zpět na stránku s pokladnou webu Commerce, kde je formulář pokladny předvyplněný údaji z účtu Google Pay. Poté, co se uživatelé vrátí z okna Google Pay na stránku pokladny, uvidí následující údaje:

- V expresním toku platby bude uživateli předem vybrána první možnost doručení, která je k dispozici pro vrácenou dodací adresu.
- Při použití Google Pay se nevrací žádná kontaktní e-mailová adresa. Uživatelé pokladny jako host budou muset zadat e-mailovou adresu do sekce kontaktů na stránce pokladny. Přihlášeným uživatelům se automaticky vyplní kontaktní údaje z jejich zákaznického účtu Dynamics (primární e-mailová adresa, kterou použili k ověření).

Zákazníci mají možnost zkontrolovat objednávky a změnit údaje objednávky na pokladně, než vybere příkaz **Odeslat objednávku** a dokončí objednávku.

### <a name="configure-google-pay-in-site-builder"></a>Konfigurace Google Pay v konfigurátoru webů 

Než nakonfigurujete své fragmenty nebo stránky pomocí Google Pay, musíte zajistit, aby byly vaše zásady zabezpečení obsahu pro váš web nastaveny v konfigurátoru webů Commerce.

Chcete-li zajistit, aby byly vaše zásady zabezpečení obsahu nastaveny v konfigurátoru webu, postupujte takto.

1. Na svém webu přejděte na **Nastavení webu \> Rozšíření**.
1. Na kartě **Zásady zabezpečení obsahu** přidejte řádek `*.google.com` do směrnic **child-src**, **connect-src**, **frame-ancestors**, **frame-src**, **img-src**, **script-src** a **style-src**.
1. Po dokončení zvolte **Vybrat a publikovat**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Konfigurace fragment expresní platby s Google Pay v konfigurátoru webů

Chcete-li nastavit fragment expresní platby s Google Pay pro internetový obchod, postupujte takto.

1. V konfigurátoru webů přejděte na **Fragmenty**.
1. Zvolte **Nové**.
1. V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu (například **Expresní platba**) a poté vyberte tlačítko **OK**. 
1. Vyberte slot **Výchozí kontejner** nového fragmentu.
1. V podokně vlastností modulu nastavte vlastnosti pro modulu kontejneru:

    - **Nadpis** – Zadejte nadpis, který se zobrazí pro sekci expresní platby vašeho webu (např. **Expresní platba**).
    - **Rozložení kontejneru** – Vyberte **Tok**.
    - **Šířka** – Vyberte **Vyplnit kontejner**.
    - **Zobrazené podřízené položky** – Vyberte **Tři** k určení počtu podřízených položek, které se vejdou do řádku v sekci expresní platby na stránce pokladny (například textové pole, expresní platba pro PayPal a expresní platba pro Google Pay).
    - **Název třídy CSS** – Zadejte **msc-express-payment-container** (požadované).

    > [!IMPORTANT]
    > - Hodnota **Název třídy CSS** musí být nastavena na **msc-express-payment-container** pro kontrolu chování kontejneru při placení. Toto chování zahrnuje skrytí, sbalení a další akce, které se vztahují na sekci expresní platby během toku pokladny. Třída **msc-express-payment-container** pracuje s výchozími operacemi, které jsou uvolněny s modulem pokladny knihovny modulů.
    > - Další styly mohou být zahrnuty proti **jménu třídy CSS**. Pokud přizpůsobíte chování modulu, křížově zkontrolujte ovládací prvky stylu, pokud používáte stejné chování kódované knihovnou modulů v modulu pokladny pro chování expresní platby.

1. V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Expresní platba** a poté klikněte na **OK**.
1. V podokně vlastností modulu **Expresní platba** nastavte nebo upravte hodnotu **Výška prvku iFrame** v pixelech (např. **60**).
1. V poli **Podporované typy úhrad** zadejte **GooglePay**. Hodnota musí odpovídat řetězci **Podporované typy platebních metod** v konektoru, který je nastaven pro kanál (jak je popsáno v sekci [Konfigurace internetového obchodu Commerce pro Google Pay](#configure-a-commerce-online-store-for-google-pay) výše v tomto článku).

    > [!NOTE]
    > Opakováním kroků 6 až 9 můžete přidat moduly **Expresní platba** pro jiné platební metody. Zadejte hodnotu **Podporované typy výběrových řízení** hodnotu pro další nakonfigurované typy plateb (např. **Paypal**).

1. Volitelné: Do výchozího modulu kontejneru můžete přidat modul textového bloku, aby obsahoval pokyny nebo informace o zveřejnění. Po přidání modulu zadejte v podokně vlastností požadovaný text do pole **Formátovaný text** pole. Text můžete umístit nad nebo pod moduly pro expresní platby výběrem tří teček (**…**) ve slotu **Textový blok** a poté vybrat **Posunout nahoru** nebo **Posunout dolů**.
1. Vyberte **Uložit** k uložení a potom vyberte **Dokončit úpravy**.
1. Vyberte **Publikovat** a publikujte fragment.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Přidání fragmentu expresní platby na stránku pokladny

Chcete-li přidat fragment expresní platby na stránku pokladny, postupujte takto.

1. V konfigurátoru webů vyberte **Stránky** a poté vyberte stránku pokladny vašeho webu.
1. Vyberte možnost **Upravit**.
1. V pozici **Hlavní** vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V podokně vlastností modulu nastavte vlastnosti pro modulu kontejneru:

    - **Rozložení kontejneru** – Vyberte **Skládané**.
    - **Šířka** – Vyberte **Vyplnit kontejner**.
    - **Zobrazené podřízené položky** – Vyberte **Tři** k určení počtu podřízených položek, které se vejdou do řádku v sekci expresní platby na stránce pokladny (například textové pole, expresní platba pro PayPal a expresní platba pro Google Pay).

1. Ve slotu modulu **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Výběr fragmentu** vyberte fragment expresní platby, který jste vytvořili, a pak vyberte tlačítko **OK**.
1. Vyberte **Uložit** k uložení a potom vyberte **Dokončit úpravy**.
1. Výběrem možnosti **Publikovat** publikujte stránku.

> [!NOTE]
> Pokud stránka pokladny již obsahuje kontejner s fragmentem pokladny a chcete, aby byl modul pro expresní platby vykreslen nad normálním kontejnerem pokladny, můžete jej umístit nad nebo pod stávající pokladnu výběrem tří teček (**...**) v **Hlavní slot** a poté vybrat **Posunout nahoru** nebo **Posunout dolů**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Přidání fragmentu expresní platby na stránku košíku

Chcete-li přidat fragment expresní platby na stránku košíku, postupujte takto.

1. V konfigurátoru webů vyberte **Stránky** a poté vyberte stránku košíku vašeho webu.
2. Vyberte možnost **Upravit**.
3. V zobrazení osnovy rozbalte **Hlavní slot** ve stromovém zobrazení a najděte kontejner, který obsahuje modul **Košík**.
4. V modulu **Košík** vyberte slot **Expresní platba**, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
5. V dialogovém okně **Vybrat moduly** vyberte modul **Expresní platba** a poté klikněte na **OK**.
6. Vyberte slot modulu **Expresní platba**. Poté v podokně vlastností vpravo pod **Podporované typy platebních metod** zadejte **GooglePay**. Hodnota musí odpovídat řetězci **Podporované typy platebních metod** v konektoru, který byl nastaven pro kanál (jak je popsáno v sekci [Konfigurace internetového obchodu Commerce pro Google Pay](#configure-a-commerce-online-store-for-google-pay) výše v tomto článku).
1. Vyberte **Uložit** k uložení a potom vyberte **Dokončit úpravy**.
1. Výběrem možnosti **Publikovat** publikujte stránku.

Uživatelé mohou zahrnovat až tři podporované moduly **Expresní platba** moduly (jinými slovy tři dostupné podporované možnosti platby) ve slotu **Expresní platba** košíku.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Nastavení Google Pay jako možnosti v sekci platby u pokladny

Službu Google Pay můžete nastavit jako možnost v sekci plateb u pokladny pro neexpresní funkce pouze pro platby. Pokladní formulář vyplní uživatel a platební stránka Google Pay pouze připraví pokladnu pro platbu prostřednictvím Google Pay. K přepsání vyplněných platebních údajů nebudou použity žádné informace o účtu Google.

> [!NOTE]
> Následující postup předpokládá, že váš web používá fragment pokladny, který je nakonfigurován s informacemi o vyzvednutí, dodací adresou, možnostmi doručení, kontaktními informacemi, volitelnými podmínkami a částí pro prvky pokladny. Výchozí modul pokladny knihovny modulů je uvolněn s kontejnerem sekce pokladny, který obsahuje textový blok, věrnostní body, dárkové karty a platební moduly. Další informace naleznete v tématu [Platební modul](../payment-module.md).

Chcete-li nastavit Google Pay jako běžnou platební možnost v části **Způsob platby** stránky pokladny, postupujte takto.

1. V konfigurátoru webů vyberte **Fragmenty** a poté vyberte fragment pokladny vašeho webu.
1. Vyberte možnost **Upravit**.
1. V pozici **Informace o pokladně** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Platba** a poté klikněte na **OK**.
1. V podokně vlastností modulu **Platba** nastavte vlastnosti pro modulu kontejneru:

    - **Nadpis** – Zadejte nadpis, který se zobrazí pro sekci expresní platby vašeho webu (např. **Google Pay**).
    - **Výška prvku iFrame** – Změňte hodnotu na preferovanou výšku návrhu v pixelech (např. **75**). 
    - **Podporované typy platebních metod** – Zadejte **GooglePay**, aby odpovídala konfiguraci konektoru Google Pay v Commerce headquarters.
    - **Je primární platba** – Nechte zaškrtávací políčko prázdné. (Tato vlastnost je obvykle povolena pro modul pokladny Adyen.)
    - **Přepsání stylu platby** – Tato vlastnost není u konfigurace Google Pay podporována.
    - **Použít ID konektoru** – Tato vlastnost musí být vybrána, pokud je na stránce použito více platebních konektorů.

1. Umístěte text nad nebo pod moduly pro ostatní platby výběrem tří teček (**…**) ve slotu **Platba** a poté vybrat **Posunout nahoru** nebo **Posunout dolů**.
1. Vyberte **Uložit** k uložení a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

### <a name="modes-of-delivery"></a>Způsoby dodání

S modulem pro expresní platby, který využívá Google Pay, bude předvyplněna první možnost doručení, která se vrátí pro dodací adresu, která byla vybrána pro účet Google Pay. Uživatelé mají možnost upravit dodací adresu na jinou možnost, pokud chtějí.

Pořadí, ve kterém se způsoby doručení zobrazují v modulu expresní platby, se konfiguruje na stránku **Způsoby doručení** kanálu v Commerce headquarters. V Commerce headquarters přejděte na **Maloobchod a obchod \> Kanály \> Online obchody** a vyberte hodnotu **ID maloobchodního kanálu** pro svůj obchod. V podokně akcí na kartě **Nastavení** zvolte **Způsoby dodání**. Způsoby doručení, které jsou uvedeny, se zobrazí ve stejné objednávce v modulu expresní platby. Chcete-li přidat nebo odebrat způsoby doručení pro maloobchodní kanál nebo produkt, vyberte v podokně akcí **Správa způsobů dodání**. Další informace o nastavení metod dodání naleznete v tématu [Nastavení způsobů dodání](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Modul pokladny také používá modul možností doručení, když jsou způsoby doručení vykresleny během placení. Další informace naleznete v části [Modul možností doručení](../delivery-options-module.md).

Způsoby doručení se zobrazí, když jsou přidány do seznamu **Způsoby doručení** v internetovém obchodě.

## <a name="additional-resources"></a>Další prostředky

[Časté dotazy k platbám](payments-retail.md)

[Modul pokladny](../add-checkout-module.md)

[Platební modul](../payment-module.md)
