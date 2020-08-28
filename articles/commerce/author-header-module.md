---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686615"
---
# <a name="header-module"></a>Modul záhlaví

[!include [banner](includes/banner.md)]

Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

V aplikaci Dynamics 365 Commerce se záhlaví stránky skládá z několika modulů, jako je například záhlaví, navigační nabídka, hledání, reklamní banner a moduly souhlasu se soubory cookie. 

Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, symbol košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel. Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení). Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).

Následující obrázek znázorňuje příklad modulu záhlaví na domovské stránce.

![Příklad modulu záhlaví](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Vlastnosti modulu záhlaví

Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**. 

Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce. Další informace naleznete v tématu [Přidat logo](add-logo.md). 

Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduly, které jsou k dispozici v modulu záhlaví

Následující moduly lze použít v modulu záhlaví:

- **Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy. Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Commerce. Navigační nabídka obsahuje vlastnost **Zdroj navigace**, která se používá k určení položek navigační nabídky serveru Retail a statických položek nabídky jako zdroje. Jsou-li statické položky nabídky určeny jako zdroj, lze poskytnout relativní odkazy na jiné stránky na webu. Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví. 

- **Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty. Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**. Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby. Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.

- **Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku. Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Vytvoření modulu záhlaví stránky

Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment stránky** vyberte modul **Kontejner**, zadejte název fragmentu stránky a poté klepněte na tlačítko **OK**.
1. Vyberte pozici **Výchozí kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte moduly **Propagační banner** a **Souhlas se soubory cookie** a poté klikněte na tlačítko **OK**.
1. V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. Vyberte pozici **Kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Záhlaví** a poté klikněte na tlačítko **OK**.
1. V pozici **Navigační nabídka** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Navigační nabídka** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu navigační nabídky dle potřeby nakonfigurujte vlastnosti.
1. V pozici **Vyhledávání** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Vyhledávání** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu vyhledávání dle potřeby nakonfigurujte vlastnosti.
1. V pozici **Ikona nákupního košíku** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Ikona nákupního košíku** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu ikony nákupního košíku dle potřeby nakonfigurujte vlastnosti. Pokud chcete, aby ikona nákupního košíku zobrazovala souhrn nákupního košíku (označovaný také jako mini košík), když na ni uživatelé umístí kurzor myši, vyberte **Zobrazit mini košík**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.

1. V pozici **Záhlaví** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Ikona modulu košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
