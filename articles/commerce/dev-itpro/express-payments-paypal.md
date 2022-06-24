---
title: Konfigurace expresních plateb pro PayPal
description: Tento článek popisuje, jak nakonfigurovat expresní platby pro PayPal, abyste umožnili rychlejší zaplacení v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905275"
---
# <a name="configure-express-payments-for-paypal"></a>Konfigurace expresních plateb pro PayPal

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat expresní platby pro PayPal, abyste umožnili rychlejší zaplacení v Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| PayPal peněženka | Prostředí zákazníků a integrace, které podporuje konektor PayPal. Je také známá jako tlačítko PayPal. |
| Peněženka | Typ platby, který nezahrnuje tradiční platební charakteristiky, jako je rozsah bankovního identifikačního čísla (BIN) a datum vypršení platnosti, které se používají k rozlišení typů kreditních a debetních karet. |
| Expresní platba | Modul Commerce, který podporuje rychlejší zaplacení při použití podporovaných platebních metod. Tento článek se zabývá používáním modulu pro expresní platby přes PayPal. |

Dynamics 365 Commerce nabízí okamžitou integraci pro PayPal peněženku. Když je konfigurován Dynamics 365 Payment Connector pro Paypal, zobrazí se tlačítko PayPal jako volitelná platební metoda během online rezervace objednávky. Když si uživatelé vyberou PayPal, jsou přesměrováni k dokončení platby přímo na PayPal a poté jsou vráceni do online obchodu k dokončení objednávky. Přechod nákupního košíku do PayPalu umožňuje zákazníkům použít informace o svém platebním účtu k předvyplnění formuláře rezervace, aby mohli proces platby dokončit rychleji.

Commerce přidal modul pro expresní platby, který usnadňuje expresní odbavení. Modul pro expresní platby lze použít ve fragmentu, který lze zahrnout na stránku pokladny nebo košíku. Když je konfigurována platba přes PayPal, použije se stejný odkaz na konektor Dynamics 365 Payment Connector pro Paypal jak pro expresní, tak pro běžnou platbu.

## <a name="paypal-checkout-in-commerce"></a>Zaplacení přes PayPal v Commerce

### <a name="prerequisites"></a>Předpoklady

Nastavte PayPal peněženku ve vašem prostředí dle popisu v článku [Dynamics 365 Payment Connector pro PayPal](../paypal.md).

Pokud používáte PayPal jako možnost v běžném pokladním toku (kde uživatelé ručně zadávají informace o svém účtu bez použití akcí předvyplnění expresní platby), postupujte podle pokynů k nastavení v článku [Platební modul](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Modul pro expresní platby přes PayPal

Modul pro expresní platby spolupracuje s podpůrnými platebními metodami a nabízí zákazníkům webu možnost rychlejšího odbavení předvyplněním informací o jejich účtu platební služby během procesu platby. Modul pro expresní platby používá nakonfigurovaný platební konektor k předvyplnění pokladního formuláře podrobnostmi o uživatelském účtu, jako je adresa, kontaktní údaje a vybraný způsob platby.

Když se použije expresní pokladna PayPal a uživatel vybere tlačítko PayPal v sekci expresní platby na stránce pokladny, otevře se okno iFrame pro platbu přes PayPal. Uživatel se poté přihlásí ke svému účtu PayPal a použije k zaplacení transakce doručovací adresu, fakturační adresu, e-mailovou adresu a způsob platby PayPal.

Poté, co uživatel dokončí akci v okně PayPal, je přesměrován zpět na stránku s pokladnou webu Commerce, kde je formulář pokladny předvyplněný vybranými údaji. V expresním toku platby bude uživateli předvyplněna první možnost doručení, která je k dispozici pro vrácenou dodací adresu. Uživatel má poté možnost zkontrolovat objednávku a změnit podrobnosti objednávky na pokladně, než vybere příkaz **Odeslat objednávku** a dokončí objednávku.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Přidání modulu pro expresní platby přes PayPal do fragmentu

Chcete-li přidat modul pro expresní platby přes PayPal do fragmentu v nástroji Commerce Site Builder, postupujte takto.

1. Přejděte na web.
1. V levém navigačním podokně vyberte **Fragmenty** a pak vyberte **Nový**.
1. V dialogovém okně **Nový fragment** najděte a vyberte modul **Expresní platba**, a pak v poli **Název fragmentu** zadejte název (například **Expresní zaplacení**).
1. Tlačítkem **OK** vytvořte fragment.
1. V zobrazení osnovy vyberte pozici modulu pro expresní platby, který jste vytvořili.
1. V podokně vlastností vyberte **Nadpis**.
1. V dialogu **Nadpis** v poli **Text nadpisu** zadejte text nadpisu, který chcete zobrazit pro sekci expresní pokladny vašeho webu (např. **Expresní zaplacení**).
1. V části **Úroveň nadpisu** vyberte úroveň nadpisu (např. **H2**).
1. Vyberte **OK**.
1. V podokně vlastností v poli **Výška prvku iFrame** zadejte nebo upravte výšku prvku iFrame (např. **60**).
1. V poli **Podporované typy úhrad** zadejte **PayPal**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Přidání fragmentu expresní platby na stránku pokladny

Chcete-li přidat fragment expresní platby na stránku pokladny v nástroji pro tvorbu webu, postupujte takto.

1. Přejděte na web.
1. V levém navigačním podokně vyberte **Stránky** a poté vyberte stránku pokladny vašeho webu.
1. Chcete-li aplikaci upravit, vyberte příkaz **Upravit**.
1. V pozici **Hlavní** vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.

    > [!NOTE]
    > Pokud modul kontejneru, který obsahuje fragment pokladny, již existuje, přesuňte sekci expresní platby tak, aby se objevila nad existujícím kontejnerem pokladny v pozici **Hlavní**. Sekce pro expresní platby se poté zobrazí nad normálním pokladním kontejnerem. Chcete-li přesunout modul kontejneru nahoru nebo dolů, vyberte tři tečky (**...**) a pak vyberte **Přesunout nahoru** nebo **Přesunout dolů**.

1. V podokně vlastností **Kontejner** doporučujeme konfigurovat vlastnosti následujícím způsobem:

    - **Rozložení kontejneru** – Vyberte **Skládané**.
    - **Šířka** – Vyberte **Vyplnit kontejner**.
    - **Zobrazené podřízené položky** – Vyberte **Tři**.

1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Výběr fragmentu** najděte a vyberte fragment expresní platby, který jste vytvořili, a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Přidání fragmentu expresní platby na stránku košíku

Chcete-li přidat fragment expresní platby na stránku košíku v nástroji pro tvorbu webu, postupujte takto.

1. Přejděte na web.
1. V levém navigačním podokně vyberte **Stránky** a poté vyberte stránku košíku vašeho webu.
1. Chcete-li aplikaci upravit, vyberte příkaz **Upravit**.
1. V pozici **Hlavní** najděte kontejner, který obsahuje modul **Košík**. Modul **Košík** bude obsahovat pozici **Expresní platba**.
1. Vyberte pozici **Expresní platba**, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Expresní platba** a poté klikněte na **OK**.
1. V podokně vlastností v poli **Podporované typy úhrad** zadejte **Paypal**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="modes-of-delivery"></a>Způsoby dodání

Když je modul pro expresní platby nakonfigurován pro použití PayPalu, bude předvyplněna první možnost doručení, která se vrátí pro dodací adresu, která byla vybrána pro účet PayPal. Uživatelé budou moci změnit dodací adresu, pokud chtějí.

Pořadí způsobu doručení se konfiguruje v sekci **Způsoby doručení** pro kanál v ústředí Commerce. Další informace naleznete v tématu [Nastavení způsobů doručení](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Modul pokladny také použije modul možností doručení, když jsou způsoby doručení vykresleny během placení. Další informace naleznete v části [Modul možností doručení](../delivery-options-module.md).

Způsoby doručení jsou přidány do seznamu pro internetový obchod v centrále Commerce. Přejděte do nabídky **Maloobchod a obchod \> Kanály \> Internetové obchody** a vyberte ID kanálu pro váš obchod. Poté vyberte **Nastavení \> Způsoby doručení**. Způsoby doručení, které jsou uvedeny v konfiguraci, se na webu objeví podobným způsobem. Chcete-li přidat nebo odebrat způsoby doručení pro maloobchodní kanál nebo produkt, vyberte v podokně akcí **Správa způsobů dodání**.

## <a name="additional-resources"></a>Další prostředky

[Časté dotazy k platbám](payments-retail.md)

[Modul pokladny](../add-checkout-module.md)

[Platební modul](../payment-module.md)

[Nastavit způsoby dodání](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Modul možností doručení](../delivery-options-module.md)
