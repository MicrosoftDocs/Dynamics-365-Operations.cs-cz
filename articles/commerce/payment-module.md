---
title: Modul platby
description: Toto téma popisuje modul platby a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 303b5f0bdfdb00accab2598acc2545bca69660412e170202152303c8ed81314e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774550"
---
# <a name="payment-module"></a>Platební modul

[!include [banner](includes/banner.md)]

Toto téma popisuje modul platby a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

Platba – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí kreditní nebo debetní karty. Integraci platby pro tento modul zajišťuje konektor plateb Dynamics 365 pro Adyen. Další informace o nastavení a konfiguraci konektoru plateb pro online obchody naleznete v tématu [Konektor plateb Dynamics 365 pro Ayden](dev-itpro/adyen-connector.md)  

Od verze Commerce 10.0.14 je platební modul také integrován s konektorem platby Dynamics 365 pro PayPal, aby zákazníci mohli platit za objednávky pomocí PayPal. Další informace o nastavení a konfiguraci konektoru platby Dynamics 365 pro Paypal naleznete v tématu [Konektor platby Dynamics 365 pro PayPal](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Platební konektor Dynamics 365 pro Adyen 

Platební modul je hostitelem platebních informací, které jsou zobrazovány prostřednictvím služby Adyen, v rámci vloženého rámce HTML (iframe). Platební modul spolupracuje s Commerce Scale Unit a získává informace o platbě Adyen. V rámci interakce jednotky Commerce Scale Unit platební modul umožňuje, aby se informace o fakturační adrese zobrazovaly v prvku iframe přes Ayden nebo jako samostatný modul. V tématu Fabrikam je fakturační adresa povolena jako samostatný modul. Tento přístup umožňuje větší flexibilitu formátování, protože adresové řádky lze vykreslit tak, aby se podobaly řádkům dodací adresy.

Platební modul také umožňuje přihlášeným zákazníkům ukládat své platební informace. Platební informace a fakturační adresa jsou ukládány a spravovány prostřednictvím platebního konektoru Adyen.

Platební modul pokrývá veškeré poplatky za objednávky, které již nejsou pokryty věrnostními body ani dárkovou kartou. Pokud je celková částka objednávky plně pokryta věrnostními body nebo kredity dárkové karty, platební modul bude skrytý a zákazník bude moci objednávku zadat bez ní.

Konektor platby Adyen také podporuje silné ověření klienta (SCA). Část revidované směrnice Evropské unie (EU) o platebních službách (PSD2) vyžaduje, aby nakupující byli autentizováni mimo online obchod, když používají elektronickou platební metodu. Během toku pokladny jsou zákazníci přesměrováni na svůj bankovní web a poté jsou po ověření přesměrováni zpět do procesu toku pokladny Commerce. Během tohoto přesměrování budou uloženy informace, které zákazník zadal v pokladně (například dodací adresa, možnosti doručení, informace o dárkových kartách a informace o věrnostním programu). Před zapnutím funkce konektoru platby Adyen musí být konektor platby nakonfigurován pro SCA v centrále Commerce. Další informace naleznete v článku [Silná autentizace zákazníků pomocí Adyen](adyen_redirect.md). Tato funkce byla povolena v Commerce verze 10.0.12.

> [!NOTE]
> U platebního konektoru Adyen lze modul iframe v platebním modulu vykreslit pouze v případě, že přidáte adresu Adyen URL do seznamu povolených stránek. Chcete-li tento krok provést , přidejte **\*.adyen.com** do směrnic **child-src**, **connect-src**, **img-src**, **script-src** a **style-src** pro zásady zabezpečení obsahu webu. Další informace viz [Správa zásad zabezpečení obsahu](manage-csp.md). 

Následující obrázek ukazuje příklad modulů dárkové karty, věrnostních bodů a plateb Ayden na stránce pokladny.

![Příklad modulů dárkové karty, věrnostních bodů a plateb Ayden na stránce pokladny.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector pro PayPal

Od Commerce verze 10.0.14 je platební modul také integrován v konektoru platby Dynamics 365 pro PayPal. Další informace o nastavení a konfiguraci konektoru platby pro online obchody naleznete v tématu [Konektor platby Dynamics 365 pro PayPal](paypal.md).
 
Na stránce pokladny můžete mít nakonfigurované konektory Adyen i PayPal. Platební modul byl vylepšen o další vlastnosti, které pomáhají identifikovat, s jakým konektorem by měl pracovat. Podrobnosti viz vlastnosti modulu **Podporované typy úhrad** a **Je primární platba** v následující tabulce.
  
Když je platební modul nakonfigurován pro použití konektoru platby PayPal, na stránce pokladny se zobrazí tlačítko PayPal. Po vyvolání zákazníkem platební modul vykreslí prvek iframe obsahující informace o PayPal. Zákazník se může v rámci tohoto prvku iframe přihlásit a poskytnout své údaje k účtu PayPal k dokončení své transakce. Když se zákazník rozhodne platit přes PayPal, zbývající částka z objednávky bude účtována přes PayPal.

Konektor platby PayPal nevyžaduje modul fakturační adresy, protože všechny informace související s fakturací zpracovává PayPal v rámci svého prvku iframe. Jsou však potřeba moduly dodací adresy a doručení.

Následující obrázek ukazuje příklad dvou platebních modulů na stránce pokladny, jeden konfigurovaný s platebním konektorem Adyen a druhý s platebním konektorem PayPal.
![Příklad modulů platby Ayden a PayPal na stránce pokladny.](./media/ecommerce-paypal.png)

Následující obrázek ukazuje příklad prvku iframe PayPal vyvolaného pomocí tlačítka PayPal. 
![Příklad prvku iframe Paypal na stránce pokladny.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Vlastnosti modulu platby

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví | Text nadpisu | Volitelný nadpis pro modul platby. |
| Výška prvku iframe. | Pixely | Výška prvku iframe v pixelech. Velikost lze upravit podle potřeby. |
| Zobrazit fakturační adresu | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, fakturační adresu doručí Adyen uvnitř prvku iframe platebního modulu. Pokud je nastavena na **Nepravda**, fakturační adresu nebude Adyen zobrazovat a uživatel Commerce bude muset nakonfigurovat modul tak, aby zobrazoval fakturační adresu na stránce pokladny. U platebního konektoru PayPal nemá toto pole žádný dopad, protože fakturační adresa je plně zpracována v rámci služby PayPal. |
| Přepsání stylu platby | Kód kaskádových stylů (CSS) | Protože je platební modul hostován v prvku iframe, existuje omezená schopnost stylování. Pomocí této vlastnosti můžete dosáhnout určitého stylu. Chcete-li přepsat styly webů, musíte vložit CSS kód jako hodnotu této vlastnosti. Přepsání a styly CSS tvůrce stránek se na tento modul nevztahují. |
|Podporované typy úhrad| Řetězec| Pokud je nakonfigurováno více konektorů platby, měli byste zadat řetězec podporovaného typu úhrady, jak je definován v konfiguraci konektoru platby v centrále Commerce (viz následující obrázek). Pokud je prázdný, použije se výchozí konektor platby Adyen. Přidáno v Comerce verze 10.0.14.|
|Je primární platba|  **Pravda** nebo **nepravda** | Má-li hodnotu **Pravda**, jakékoli chybové zprávy budou generovány z primárního konektoru platby na stránce pokladny. Pokud jsou nakonfigurovány konektory platby Adyen i PayPal, nastavte Adyen na **Pravda**, což bylo přidáno ve verzi Commerce 10.0.14.|

Následující obrázek ukazuje příklad hodnoty **Podporované typy úhrad** nastavené na „PayPal“ v konfiguraci konektoru platby v centrále Commerce.
![Příklad podporovaných typů úhrad v centrále Commerce.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Fakturační adresa

Na stránce pokladny lze použít modul fakturační adresy, pokud řádky fakturační adresy konektoru platby Adyen dostatečně neodpovídají vzhledu zbytku webu. 

Chcete-li použít modul fakturační adresy na stránce pokladny, když je platební modul integrován s konektorem platby Adyen, nastavte vlastnost **Zobrazit fakturační adresu** na **Nepravda**, takže místo výchozí fakturační adresy Adyen lze použít vyhrazený modul fakturační adresy. V takovém případě by autor webu měl na stránce pokladny zahrnout modul fakturační adresy. Konektor platby Adyen také umožňuje používat dodací adresu jako fakturační adresu, aby se minimalizoval počet kroků pro uživatele webu.

Podobně jako u platebních modulů byla přidána vlastnost **Podporované typy úhrad** do modulu fakturační adresy v Commerce verze 10.0.14. Hodnota této vlastnosti by měla být totožná s hodnotou uvedenou v platebním modulu, aby byla zajištěna jejich vzájemná spolupráce. U konektoru platby Adyen by měl platební modul i modul fakturační adresy nechat tuto hodnotu prázdnou (výchozí stav). U konektoru PayPal není vyžadován modul vyhrazené fakturační adresy. U ostatních typů konektorů platby by měl být řetězec zadán tak, jak je nakonfigurován v centrále Commerce.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Na stránku pokladny přidejte modul platby a nastavte požadované vlastnosti.

Modul platby lze přidat pouze do modulu pokladny. Další informace o tom, jak nakonfigurovat modul platby pro stránku pokladny, naleznete v tématu [Modul platby](add-checkout-module.md).

Pokud jsou zapotřebí konektory platby Adyen i PayPal, přidejte oba moduly do sekce platby. Zajistěte, aby hodnota vlastnosti **Podporované typy úhrady** byla nakonfigurována pro PayPal a ponechte ji prázdnou pro Adyen. Také nastavte vlastnost **Je primární platba** na **Pravda** pro Adyen.

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)

[Platební konektor Dynamics 365 pro Adyen](dev-itpro/adyen-connector.md)

[Konektor platby Dynamics 365 pro PayPal](paypal.md)

[Silné ověření klienta pomocí konektoru Adyen](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]