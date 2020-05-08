---
title: Modul zápatí
description: Toto téma popisuje moduly zápatí a způsob jejich vytváření v řešení Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269624"
---
# <a name="footer-module"></a>Modul zápatí  


[!include [banner](includes/banner.md)]

Toto téma popisuje moduly zápatí a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul zápatí je speciální kontejner, který se používá k hostování modulů, které se zobrazují v zápatí stránky. Může se například jednat o odkazy na různé stránky na webu, například **O nás** a **Zásady obchodu**.

## <a name="footer-module-properties"></a>Vlastnosti modulu zápatí 

Podobně jako většina kontejnerů, modul zápatí podporuje vlastnosti pro nadpis a šířku. Podporuje také přidání modulů kategorií s více zápatími. Přidaný modul kategorie zápatí je vykreslen jako sloupec v modulu zápatí.

## <a name="modules-available-in-a-footer-module"></a>Moduly dostupné v modulu zápatí

**Položky zápatí** – Modul položek zápatí může obsahovat nadpis, obrázek a odkaz. Nadpis lze použít samostatně nebo v kombinaci s obrázkem a odkazem. Každý odkaz v zápatí lze nakonfigurovat tak, aby obsahoval pouze text (například odkazy „Kontaktujte nás“ a „Ochrana osobních údajů“), nebo aby měl text i obrázek (například odkazy na sociální média).

**Zpět na začátek** – Modul Zpět na začátek obsahuje odkaz pro rychlou navigaci na začátek stránky. Cíl je povinný. Výchozí hodnota cíle je #, která přesměruje uživatele na začátek stránky.

## <a name="author-a-footer-module"></a>Vytvoření modulu zápatí

1. V navigačním podokně vyberte **Fragmenty** a pak vyberte možnost **Nový fragment stránky**.
1. V dialogovém okně **Nový fragment stránky** vyberte modul zápatí, zadejte název fragmentu stránky a poté klepněte na tlačítko **OK**.
1. Ve stromové struktuře vlevo vyberte pro modul zápatí tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul kategorie zápatí a poté klikněte na tlačítko **OK**.
1. Ve stromové struktuře vyberte pro modul kategorie zápatí tlačítko se třemi tečkami a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul položky zápatí a poté klikněte na tlačítko **OK**.
1. Ve stromové strukřutě vyberte modul položky zápatí. Poté v podokně vlastností napravo nakonfigurujte nadpis, odkaz a text odkazu a požadovaný obrázek.
1. Chcete-li přidat další položky zápatí, opakujte kroky 5 až 7.
1. Chcete-li přidat do zápatí odkaz „zpět na začátek“, ve stromové struktuře vyberte pro modul kategorie zápatí tlačítko se třemi tečkami a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul Zpět na začátek a poté klikněte na tlačítko **OK**.
1. Ve stromové struktuře vyberte modul Zpět na začátek. Poté v podokně vlastností napravo nakonfigurujte modul Zpět na zaátek podle potřeby.
1. Chcete-li vrátit fragment stránky se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

U každé šablony stránky, která byla pro web vytvořena, postupujte takto.

1. V pozici **Hlavní** na výchozí stránce přidejte do modulu zápatí fragment zápatí, který jste vytvořili.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Přidáním fragmentu stránky do šablon stránek pomůžete zaručit, že zápatí bude vykresleno na každé stránce.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
