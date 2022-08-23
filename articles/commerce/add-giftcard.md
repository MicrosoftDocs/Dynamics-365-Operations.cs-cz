---
title: Modul dárkového poukazu
description: Tento článek se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 93e2a6608b6d3190df7df1d8f85fd9d7e1c18692
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280551"
---
# <a name="gift-card-module"></a>Modul dárkového poukazu

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly dárkových poukazů lze použít v modulech pokladny pro příjem dárkových poukazů, což je běžná forma platby používaná při transakcích elektronického obchodování. Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex. SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen. Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md).

> [!NOTE]
> Podpora pro uplatnění dárkových karet SVS a Givex během procesu placení je k dispozici ve vydání Dynamics 365 Commerce 10.0.11. 

K dispozici jsou dva moduly dárkových poukazů:

- **Dárkový poukaz** – Tento modul lze použít na stránce pokladny k uplatnění dárkového poukazu jako úhrady. 
- **Kontrola zůstatku dárkového poukazu** – Tento modul lze použít na kterékoli stránce ke kontrole zůstatku dárkového poukazu. Tento modul je k dispozici v aplikaci Commerce verze 10.0.14 a novější.

> [!NOTE]
> Podpora modulu kontroly zůstatku dárkové karty je k dispozici ve vydání Dynamics 365 Commerce 10.0.14.

Následující obrázek znázorňuje příklad modulu dárkového poukazu na stránce pokladny.

![Příklad modulu dárkového poukazu.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

- **Zobrazit další pole** – Tato vlastnost určuje, která pole mají být zobrazena pro dárkové poukazy kromě čísla dárkového poukazu, který je ve výchozím nastavení vždy zobrazen. Některé dárkové poukazy například podporují zobrazení osobního identifikačního čísla (PIN) a další podporují zobrazování kódu PIN a data vypršení platnosti. Druhou možností může být nastavení této vlastnosti na "none", která by zobrazila pouze číslo dárkového poukazu a žádná další pole.

    Podporovány jsou následující hodnoty:

    - PIN
    - Datum konce platnosti
    - PIN a datum konce platnosti 
    - Neomezeno

- **Povolit pro uživatele typu host** - Když je tato vlastnost povolena, mohou uživatelé typu host uplatnit nebo zkontrolovat zůstatky na dárkových kartách. Tato vlastnost vyžaduje, aby byl v Commerce Headquarters povolen anonymní přístup (hosta) pro dárkové karty. Další informace viz [Povolení plateb dárkovými kartami pro hosty na pokladně](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> Vlastnost **Povolit pro uživatele typu host** je k dispozici od verze Commerce 10.0.21. Vyžaduje instalaci balíčku knihovny modulů Commerce verze 9.31.

## <a name="site-settings-for-gift-card-modules"></a>Nastavení webu pro moduly dárkových poukazů

V konfigurátoru webů Commerce v **Nastavení webu \> Rozšíření** existuje nastavení modulu dárkového poukazu s názvem **Podporovaný typ dárkového poukazu**. Toto nastavení podporuje tři hodnoty:
- **Dárkový pouikaz Dynamics 365** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy aplikace Dynamics 365. Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.
- **Dárkové poukazy SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy SVS a Givex. Toto nastavení je podporováno pro přihlášené i anonymní uživatele na webu e-Commerce.
- **Dárkové poukazy Dynamics 365, SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje dárkové poukazy Dynamics 365, SVS a Givex. Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.

> [!IMPORTANT]
> Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.11 a jsou vyžadována, pouze pokud potřebujete podporu pro dárkové karty SVS nebo Givex. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Rozšíření interních dárkových karet pro použití v elektronických obchodech

Ve výchozím nastavení nejsou interní dárkové karty optimalizovány pro použití v elektronických obchodech. Než tedy povolíte použití interních dárkových karet k platbám, měli byste je nakonfigurovat pomocí rozšíření, která jim pomohou zajistit větší bezpečnost. Tady jsou oblasti dárkových karet, které byste měli rozšířit, než povolíte použití interních dárkových karet ve výrobě:

- **Číslo dárkové karty** – Číselné řady se používají ke generování čísel dárkových karet pro interní dárkové karty. Protože lze snadno předvídat číselné řady, měli byste rozšířit generování čísel dárkových karet tak, aby se pro vydaná čísla dárkových karet používaly náhodné kryptograficky zabezpečené řetězce.
- **GetBalance** – API **GetBalance** se používá k vyhledávání zůstatků dárkových karet. Ve výchozím nastavení je toto rozhraní API veřejné. Pokud k vyhledání zůstatků dárkových karet není vyžadován PIN, existuje riziko, že by útoky hrubou silou mohly použít API **GetBalance** k pokusu vyhledat čísla dárkových karet, které mají zůstatky. Implementací požadavků na PIN pro interní dárkové karty a omezení API můžete pomoci zmírnit riziko.
- **PIN** – Ve výchozím nastavení interní dárkové karty nepodporují kódy PIN. Interní dárkové karty byste měli rozšířit tak, aby byl k vyhledání zůstatků vyžadován PIN. Tuto funkci lze také použít k uzamčení dárkových karet po po sobě jdoucích nesprávných pokusech o zadání kódu PIN.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>U pokladny pro hosty povolte platby dárkovou kartou

Ve výchozím nastavení nejsou platby pokladní kartou povoleny pro (anonymní) pokladnu hosta. Pokud je chcete povolit, postupujte následovně.

1. V centru Commerce přejděte na možnost **Retail a Commerce \> Nastavení kanáu \> Nastavení POS \> POS \> Operace POS**.
1. Vyberte a podržte (nebo klikněte pravým tlačítkem) záhlaví mřížky a poté vyberte **Vložit sloupce**.
1. V dialogovém okně **Vložit sloupce** zaškrtněte políčko **AllowAnonymousAccess**.
1. Vyberte **Aktualizovat**.
1. Pro operace **520** (Zůstatek dárkové karty) a **214**, nastavte hodnotu **AllowAnonymousAccess** na **1**.
1. Zvolte **Uložit**.
1. Spusťte úlohu plánovače **1090** k synchronizování změn do databáze kanálů. 

## <a name="add-a-gift-card-module-to-a-page"></a>Přidání modulu dárkového poukazu na stránku

Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Podpora pro externí dárkové poukazy](./dev-itpro/gift-card.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
