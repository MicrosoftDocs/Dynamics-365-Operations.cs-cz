---
title: Modul platby
description: Toto téma popisuje modul platby a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661193"
---
# <a name="payment-module"></a>Modul platby

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje modul platby a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Platba – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí kreditní nebo debetní karty. Integraci platby pro tento modul zajišťuje konektor plateb Dynamics 365 pro Adyen. Další informace o nastavení a konfiguraci konektoru plateb pro online obchody naleznete v tématu [Konektor plateb Dynamics 365 pro Ayden](dev-itpro/adyen-connector.md)

Platební modul je hostitelem platebních informací, které jsou zobrazovány prostřednictvím služby Adyen, v rámci vloženého rámce HTML (iframe). Platební modul spolupracuje s Commerce Scale Unit a získává informace o platbě Adyen. V rámci interakce jednotky Commerce Scale Unit platební modul umožňuje, aby se informace o fakturační adrese zobrazovaly v prvku iframe nebo jako samostatný modul. V tématu Fabrikam je fakturační adresa zobrazena v samostatném modulu. Tento přístup umožňuje větší flexibilitu formátování, protože adresové řádky lze vykreslit tak, aby se podobaly řádkům dodací adresy.

Platební modul také umožňuje přihlášeným zákazníkům ukládat své platební informace. Platební informace a fakturační adresa jsou ukládány a spravovány prostřednictvím platebního konektoru Adyen.

Platební modul pokrývá veškeré poplatky za objednávky, které již nejsou pokryty věrnostními body ani dárkovou kartou. Pokud je celková částka objednávky plně pokryta věrnostními body nebo kredity dárkové karty, platební modul bude skrytý a zákazník bude moci objednávku zadat bez ní.

Konektor platby Adyen také podporuje silné ověření klienta (SCA). Část směrnice Evropské unie (EU) o platebních službách 2.0 (PSD2.0) vyžaduje, aby nakupující byli autentizováni mimo online obchod, když používají elektronickou platební metodu. Během procesu platby jsou zákazníci přesměrováni na své bankovní stránky. Poté se po ověření přesměrují zpět do toku plateb Commerce. Během tohoto přesměrování budou uloženy informace, které zákazník zadal v pokladně (například dodací adresa, možnosti doručení, informace o dárkových kartách a informace o věrnostním programu). Před zapnutím této funkce musí být platební konektor nakonfigurován pro SCA v centrále Commerce. Další informace naleznete v článku [Silná autentizace zákazníků pomocí Adyen](adyen_redirect.md).

Následující obrázek ukazuje příklad modulů dárkové karty, věrnostních bodů a plateb na stránce pokladny.

![Příklad modulů dárkové karty, věrnostních bodů a plateb na stránce pokladny](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Vlastnosti modulu platby

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví | Text nadpisu | Volitelný nadpis pro modul platby. |
| Výška prvku iframe. | Pixely | Výška prvku iframe v pixelech. Velikost lze upravit podle potřeby. |
| Zobrazit fakturační adresu | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, fakturační adresu doručí Adyen uvnitř prvku iframe platebního modulu. Pokud je nastaveno na **Nepravda**, fakturační adresu nebude Adyen zobrazovat a uživatel Commerce bude muset nakonfigurovat modul tak, aby zobrazoval fakturační adresu na stránce pokladny. |
| Přepsání stylu platby | Kód kaskádových stylů (CSS) | Protože je platební modul hostován v prvku iframe, existuje omezená schopnost stylování. Pomocí této vlastnosti můžete dosáhnout určitého stylu. Chcete-li přepsat styly webů, musíte vložit CSS kód jako hodnotu této vlastnosti. Přepsání a styly CSS tvůrce stránek se na tento modul nevztahují. |

## <a name="billing-address"></a>Fakturační adresa

Platební modul umožňuje zákazníkům poskytnout fakturační adresu pro své platební informace. Rovněž jim umožňuje použít jako fakturační adresu svou dodací adresu, aby usnadnili a urychlili tok plateb. Pokud je **Zobrazit fakturační adresu** vlastnost nastavena na **Nepravda**, platební modul by měl být nakonfigurován na stránce pokladny.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Na stránku pokladny přidejte modul platby a nastavte požadované vlastnosti.

Modul platby lze přidat pouze do modulu pokladny. Další informace o tom, jak nakonfigurovat modul platby pro stránku pokladny, naleznete v tématu [Modul platby](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)

[Platební konektor Dynamics 365 pro Adyen](dev-itpro/adyen-connector.md)

[Silné ověření klienta pomocí konektoru Adyen](adyen_redirect.md)
