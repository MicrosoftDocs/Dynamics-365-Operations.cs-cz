---
title: Modul pokladny
description: Tohle téma popisuje, jak na stránku přidat modul pokladny a jak nastavit požadované vlastnosti.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 28d58caba71ea98ccf163e756e879587aa254bb3
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410941"
---
# <a name="checkout-module"></a>Modul pokladny

[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak na stránku přidat modul pokladny a jak nastavit požadované vlastnosti.

## <a name="overview"></a>Přehled

Modul poklady je speciální kontejner, který je hostitelem všech modulů, které jsou nutné k vytvoření objednávky. Modul poklady představuje podrobný tok, který zákazník používá k zadání všech relevantních informací za účelem provedení nákupu. Zachycuje doručovací adresu, způsob přepravy a informace o fakturaci. Poskytuje také souhrn objednávky a další informace, které souvisejí s objednávkou odběratele.

Modul pokladny vykresluje data na základě ID košíku. ID košíku je uloženo jako soubor cookie prohlížeče. ID košíku je nutné k vykreslení informací v modulu pokladny, jako jsou například položky v objednávce, celková částka a slevy. 

Následující obrázek ukazuje příklad modulu poklady Fabrikam na stránce pokladny.

![Příklad modulu pokladny](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Vlastnosti modulu pokladny

V modulu pokladny se zobrazí souhrn objednávek a funkce pro zadání objednávky. Chcete-li shromáždit všechny informace o odběrateli, které jsou požadovány před tím, než může být objednávka vystavena, je nutné přidat další moduly do modulu pokladny. Maloobchodní prodejci proto mají flexibilitu přidávat vlastní moduly do toku pokladny nebo vyloučit moduly na základě jejich požadavků.

| Název vlastnosti | Hodnoty | popis |
|----------------|--------|-------------|
| Záhlaví pokladny | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Nadpis modulu pokladny. |
| Záhlaví souhrnu objednávky | Text nadpisu | Nadpis sekce souhrnu objednávek modulu. |
| Nadpis řádkových položek košíku | Text nadpisu | Nadpis pro řádkové položky košíku, které jsou zobrazeny v modulu pokladny. |
| Zobrazit poplatky za dopravu online | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, řádkové položky košíku ke kterým lze přiřadit přepravné se zobrazí v řádcích nákupního košíku. Pokud je funkce **Náklady záhlaví bez proměrného** zapnuta v centrále Commerce, bude přepravní poplatek účtován na úrovni záhlaví, nikoli na úrovni řádku. Tato funkce byla přidána v Commerce verzi 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduly, které lze použít v modulu pokladny

- **Dodací adresa** – Tento modul umožňuje zákazníkovi přidat nebo vybrat dodací adresu objednávky. Další informace o tomto modulu naleznete v části [Modul dodací adresy](ship-address-module.md).

    Následující obrázek ukazuje příklad modulu dodací adresy na stránce pokladny.

    ![Příklad modulu dodací adresy](./media/ecommerce-shippingaddress.PNG)

- **Možnosti dodání** – Tento modul umožňuje zákazníkovi vybrat způsob dodání pro objednávku. Další informace o tomto modulu naleznete v části [Modul možností doručení](delivery-options-module.md).

    Následující obrázek ukazuje příklad modulu možností dodání na stránce pokladny.
 
    ![Příklad modulu možností dodání](./media/ecommerce-deliveryoptions.PNG)

- **Kontejner sekce pokladny** – Tento modul je kontejner, do kterého můžete vložit více modulů a vytvořit sekci v rámci toku pokladny. Všechny moduly související s platbou v tomto kontejneru můžete například vložit do jedné sekce. Tento modul má vliv pouze na rozložení toku.

- **Dárkový poukaz** – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí dárkového poukazu. Další informace o tomto modulu naleznete v části [Modul dárkového poukazu](add-giftcard.md).

- **Věrnostní body** – Tento modul umožňuje odběrateli zaplatit za objednávku pomocí věrnostních bodů. Poskytuje souhrn dostupných bodů a bodů s končící platností a umožňuje zákazníkovi vybrat počet bodů, které chce uplatnit. Pokud zákazník není přihlášen nebo není věrnostní člen, nebo pokud je celková částka nákupního košíku 0 (nula), bude tento modul automaticky skryt.

- **Platba** – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí kreditní nebo debetní karty. Zákazníci mohou také zadat fakturační adresu pro platební možnost, kterou si vyberou. Další informace o tomto modulu naleznete v části [Modul platby](payment-module.md).

    Následující obrázek ukazuje příklad modulů dárkové karty, věrnostních bodů a plateb na stránce pokladny.

    ![Příklad modulů dárkové karty, věrnostních bodů a plateb na stránce pokladny](./media/ecommerce-payments.PNG)

- **Kontaktní informace** – Tento modul umožňuje zákazníkovi přidat nebo změnit kontaktní informace (e-mailovou adresu) na objednávce.

- **Textový blok** – Tento modul zahrnuje veškerá zasílání zpráv, která jsou řízena systémem správy obsahu (CMS). Může například obsahovat zprávu ve znění „V případě problémů s objednávkou volejte 1-800-Fabrikam“. 

- **Platební podmínky** - Tento modul zobrazuje formátovaný text, který obsahuje smluvní podmínky a zaškrtávací políčko pro vstup zákazníka. Zaškrtávací políčko je volitelné a konfigurovatelné. Vstup je zachycen modulem a může být použit jako kontrola před spuštěním umístění objednávky, ale není zahrnut do souhrnných informací o objednávce. Tento modul lze přidat do kontejneru pokladny, kontejneru sekce pokladny nebo do slotu smluvních podmínek, podle obchodních potřeb. Pokud je přidán do kontejneru pokladny nebo do slotu kontejneru sekce pokladny, zobrazí se jako krok v procesu platby. Pokud je přidán do slotu smluvních podmínek, zobrazí se poblíž tlačítka pro umístění objednávky.

    Následující obrázek znázorňuje příklad smluvních podmínek na stránce pokladny.

    ![Příklad smluvních podmínek na stránce pokladny](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Většina informací o pokladně, například dodací adresa a způsob dodání, je uložena v nákupním košíku a zpracována jako součást objednávky. Jedinou výjimkou jsou informace o kreditní kartě. Tyto informace jsou zpracovávány přímo pomocí konektoru platby Adyen. Platba je autorizována, ale nebude účtována, dokud nebude objednávka splněna.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Na stránku přidejte modul pokladny a nastavte požadované vlastnosti.

Chcete-li přidat modul pokladny na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Pokladna**.
1. V části **Název fragmentu** zadejte název pro **Fragment pokladny** a poté vyberte **OK**.
1. Vyberte pozici **Modul pokladny**.
1. V podokně vlastností vpravo vyberte symbol tužky, do pole zadejte text záhlaví a poté zaškrtněte symbol zaškrtnutí.
1. V pozici **Informace o pokladně** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte moduly **Dodací adresa**, **Možnosti dodání**, **Kontejner sekce pokladny** a **Kontaktní informace** a vyberte **OK**.
1. V modulu **Kontejner sekce poklady** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte moduly **Dárkový poukaz**, **Věrnostní program** a **Platba** a poté klikněte na tlačítko **OK**. Tímto způsobem zajistíte, že se všechny způsoby platby budou v sekci zobrazovat společně.
1. Ve slotu **Smluvní podmínky**, přidejte **Platební podmínky** modul, pokud je to požadováno. V podokně vlastností modulu nakonfigurujte podle potřeby text podmínek.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled fragmentu. Některé moduly, které nemají kontext nákupního košíku, nemusí být v náhledu vykresleny.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Vytvořte šablonu která používá nový fragment pokladny.
1. Vytvořte stránku pokladny, která používá novou šablonu.

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Platební modul](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]