---
title: Digitální dárkové karty elektronického obchodování
description: Toto téma popisuje, jak fungují digitální dárkové karty v implementaci elektronického obchodování Microsoft Dynamics 365 Commerce. Poskytuje také přehled důležitých konfiguračních kroků.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982659"
---
# <a name="e-commerce-digital-gift-cards"></a>Digitální dárkové karty elektronického obchodování

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje, jak fungují digitální dárkové karty v implementaci elektronického obchodování Microsoft Dynamics 365 Commerce. Poskytuje také přehled důležitých konfiguračních kroků.

V Dynamics 365 Commerce nákup digitálních dárkových karet dodržuje stejný postup jako nákup dalších produktů v systému. Není třeba konfigurovat žádné další moduly. Pokud je do košíku přidáno více dárkových karet, položky dárkových karet se neagregují na jednom řádku prodeje. Toto chování je povinné, protože každý řádek prodeje je fakturován pomocí samostatného čísla dárkové karty.

Nákup digitálních dárkových karet je podporován ve verzi Dynamics 365 Commerce 10.0.16 a novější.

Následující obrázek ukazuje příklad stránky s podrobnostmi o produktu (PDP) pro digitální dárkovou kartu na webu elektronického obchodování Fabrikam.

![Příklad PDP digitální dárkové karty na webu elektronického obchodu Fabrikam](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Zapnutí funkce digitální dárkové karty v centrále Commerce

Aby fungoval postupu nákupu digitálních dárkových karet v Dynamics 365 Commerce, funkce **Nákup dárkové karty v elektronické obchodu** musí být zapnutá v ústředí Commerce. Funkci naleznete v pracovním prostoru **Správa funkcí** centrále Commerce, jak je vidět na následujícím obrázku.

![Pracovní prostor správy funkcí v centrále Commerce](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Konfigurace digitální dárkové karty v centrále Commerce

Produkty digitální dárkové karty se konfigurují v centrále Commerce. Tento proces se podobá procesu pro jiné produkty. Následující důležité kroky jsou však specifické pro konfiguraci dárkových karet k nákupu. Další informace o tom, jak vytvářet a konfigurovat produkty, naleznete na stránce [Vytvoření nového produktu v Commerce](create-new-product-commerce.md).

- Když konfigurujete produkty digitálních dárkových karet v dialogovém okně **Nový produkt**, nastavte pole **Typ produktu** na **Služba**. (Chcete-li otevřít dialogové okno, přejděte na **Retail a Commerce \> Produkty a kategorie \> Produkty podle kategorie** a vyberte **Nový**.) Produkty typu **Služba** se před odesláním objednávky nekontrolují na dostupné skladové zásoby. Další informace naleznete v tématu [Vytvoření nového produktu](create-new-product-commerce.md#create-a-new-product).
- Na stránce **Parametry Commerce** na kartě **Zaúčtování** musí být pole **Produkt dárkové karty** nastaveno na **Digitální dárková karta**, jak je znázorněno na následujícím obrázku. Pokud je produkt externí dárkovou kartou, další informace naleznete v části [Podpora externích dárkových karet](./dev-itpro/gift-card.md).

    ![Pole produktu Dárkové karty v ústředí Commerce](./media/PostGiftcard.png)

- Pokud dárková karta musí podporovat více předdefinovaných částek (například $25, $50 a $100), rozměr **Velikost** se použije k nastavení těchto předdefinovaných částek. Každá předdefinovaná částka bude variantou. Další informace naleznete v tématu [Dimenze produktu](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).
- Pokud zákazníci musí být schopni určit vlastní částku pro dárkovou kartu, nejprve nastavte variantu, která umožňuje vlastní částku. Poté otevřete produkt ze stránky **Vydané produkty v kategorii** a poté na pevné kartě **Commerce** nastavte pole **Zadat cenu** na **Je třeba zadat novou cenu**, jak je znázorněno na následujícím obrázku. Toto nastavení zajišťuje, že zákazníci mohou zadat cenu, když procházejí produkt na PDP.

    ![Pole Zadat cenu v ústředí Commerce](./media/KeyInPrice.png)

- Režim doručování digitální dárkové karty musí být nastaven na **Elektronicky**. Na stránce **Způsoby dodání** (**Reatil a Commerce \> Nastavení kanálu \> Způsoby dodání**) vyberte způsob dodání **Elektronicky** v podokně se seznamem a poté přidejte produkt digitální dárkové karty do mřížky na pevné kartě **Produkty**, jak je znázorněno na následujícím obrázku. Další informace naleznete v tématu [Nastavení způsobů doručení](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Produkty digitálních dárkových karet na stránce Způsob doručení v ústředí Commerce](./media/ElectronicMode.PNG)

- Ujistěte se, že byl vytvořen profil online funkcí a přidružen k vašemu online obchodu v ústředí Commerce. V profilu funkce nastavte možnost **Agregovat produkty** na **Ano**. Toto nastavení zajišťuje agregaci všech položek kromě dárkových karet. Další informace viz [Vytvoření online funkčního profilu](online-functionality-profile.md).
- Abyste zajistili, že zákazníci obdrží e-mail po fakturaci dárkové karty, vytvořte nový typ e-mailového oznámení na stránce **Profily e-mailových oznámení** a nastavte pole **Typ e-mailového oznámení** na **Vydat dárkový poukaz**. Další informace viz [Nastavení profilu e-mailového oznámení](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Přidejte obrázky produktů do mediální knihovny nástroje konfigurátoru webů Commerce

Do mediální knihovny nástroje konfigurátoru webů Commerce musíte přidat obrázky produktů pro produkty digitálních dárkových karet. Ujistěte se, že názvy souborů obrazových souborů dárkových karet odpovídají konvencím názvů vašich stránek pro obrázky produktů. Další informace viz [Nahrát obrázky](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Konfigurace vlastní částky pro digitální dárkovou kartu v nástroji konfigurátoru webů Commerce

Pokud je digitální dárková karta nakonfigurována tak, aby umožňovala vlastní částku, musí být toto chování také povoleno v [modulu buy boxu](add-buy-box.md), který se používá na PDP vašeho webu. Modul buy boxu podporuje konfiguraci modulu, aby umožňoval vlastní částky. Můžete také definovat minimální a maximální částky, které jsou povoleny pro vlastní částky.

Ke konfiguraci vlastní částky pro digitální dárkovou kartu v nástroji konfigurátoru webů Commerce postupujte následovně.

1. Přejděte na modul buy box, který se používá v PDP vašeho webu. Tento modul nákupního boxu může být implementován ve fragmentu, v šabloně nebo na stránce.
1. Vyberte možnost **Upravit**.
1. V podokně vlastností vpravo zaškrtněte políčko **Povolit vlastní cenu**.
1. Volitelné: Chcete-li definovat minimální a maximální částky pro vlastní částky, zadejte částky pod **Minimální cena** a **Maximální cena**.
1. Vyberte **Dokončit úpravy** a potom vyberte **Zveřejnit**.

## <a name="additional-resources"></a>Další prostředky

[Modul buy boxu](add-buy-box.md)

[Modul pokladny](add-checkout-module.md)

[Modul košíku](add-cart-module.md)

[Vytvoření nového produktu v Commerce](create-new-product-commerce.md)

[Nastavit způsoby dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Dimenze produktu](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[Nastavení profilu oznámení e-mailem](email-notification-profiles.md)

[Vytvoření online funkčního profilu](online-functionality-profile.md)

[Podpora pro externí dárkové poukazy](./dev-itpro/gift-card.md)
