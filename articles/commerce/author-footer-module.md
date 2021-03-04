---
title: Modul zápatí
description: Toto téma popisuje moduly zápatí a způsob jejich vytváření v řešení Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 42a71ea9498461febca80952acc3158517918332
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410763"
---
# <a name="footer-module"></a>Modul zápatí  

[!include [banner](includes/banner.md)]

Toto téma popisuje moduly zápatí a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul zápatí je speciální kontejner, který se používá k hostování modulů, které se zobrazují v zápatí stránky. Může se například jednat o odkazy na různé stránky na webu, například **O nás** a **Zásady obchodu**.

Následující obrázek znázorňuje příklad modulu zápatí na stránce webu.

![Příklad modulu zápatí](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Vlastnosti modulu zápatí 

Podobně jako většina kontejnerů, modul zápatí podporuje vlastnosti pro nadpis a šířku. Podporuje také přidání modulů kategorií s více zápatími. Přidaný modul kategorie zápatí je vykreslen jako sloupec v modulu zápatí.

## <a name="modules-available-in-a-footer-module"></a>Moduly dostupné v modulu zápatí

**Položky zápatí** – Modul položek zápatí může obsahovat nadpis, obrázek a odkaz. Nadpis lze použít samostatně nebo v kombinaci s obrázkem a odkazem. Každý odkaz v zápatí lze nakonfigurovat tak, aby obsahoval pouze text (například odkazy „Kontaktujte nás“ a „Ochrana osobních údajů“), nebo aby měl text i obrázek (například odkazy na sociální média).

**Zpět na začátek** – Modul Zpět na začátek obsahuje odkaz pro rychlou navigaci na začátek stránky. Cíl je povinný. Výchozí hodnota cíle je \#, která přesměruje uživatele na začátek stránky.

## <a name="create-a-footer-module"></a>Vytvoření modulu zápatí

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu a poté klepněte na tlačítko **OK**.
1. V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kategorie zápatí** a poté klikněte na tlačítko **OK**.
1. V pozici **Kategorie zápatí** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Položka zápatí** a poté klikněte na tlačítko **OK**.
1. Vyberte pozici **Položka zápatí** a poté v podokně vlastností napravo dle potřeb nakonfigurujte nadpis, odkaz a text odkazu a obrázek.
1. Chcete-li přidat další položky zápatí, opakujte kroky 5 až 7.
1. Chcete-li přidat do zápatí odkaz „zpět na začátek“, v pozici **Kategorie zápatí** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Zpět na začátek** a poté klikněte na tlačítko **OK**.
1. Vyberte pozici **Zpět na začátek** a poté v podokně vlastností napravo dle potřeb nakonfigurujte text a další vlastnosti modulu.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.

1. V pozici **Zápatí** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Přidáním fragmentu do šablon stránek pomůžete zaručit, že zápatí bude vykresleno na každé stránce.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]