---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: afdc12230ebad3d5db59c384b2f1066d2c7929339f282ed4880ff967b1fd2d8b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712783"
---
# <a name="header-module"></a>Modul záhlaví

[!include [banner](includes/banner.md)]

Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.

V Dynamics 365 Commerce je záhlaví stránky nakonfigurováno jako fragment stránky, který obsahuje moduly záhlaví, propagačního banneru a souhlasu se soubory cookie. 

Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, modul ikony košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel. Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení). Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).

Následující obrázek znázorňuje příklad modulu záhlaví na domovské stránce.

![Příklad modulu záhlaví.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Vlastnosti modulu záhlaví

Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**. 

Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce. Další informace naleznete v tématu [Přidat logo](add-logo.md). 

Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.

## <a name="modules-that-are-available-within-a-header-module"></a>Moduly, které jsou k dispozici v rámci modulu záhlaví

Následující moduly lze použít v modulu záhlaví:

- **Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy. Další informace naleznete v tématu [Modul navigační nabídky](nav-menu-module.md).

- **Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty. Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**. Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby. Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.

- **Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku. Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).

- **Selektor webu** - Modul pro výběr webů umožňuje uživatelům procházet různé předdefinované weby na základě trhu, regionů a národních prostředí. Další informace naleznete v tématu [Modul pro výběr webu](site-selector.md).

- **Výběr obchodu** - Modul pro výběr obchodu lze zahrnout do slotu pro výběr obchodu v modulu záhlaví. Umožňuje uživatelům procházet a vyhledávat obchody v okolí. Uživatelé mohou také určit preferovaný obchod. Tento obchod se poté zobrazí v záhlaví. Když je modul pro výběr obchodu zahrnut v modulu záhlaví, jeho vlastnost **Režim** musí být nastavena na **Najít obchody**. Další informace naleznete v tématu [Modul pro výběr obchodu](store-selector.md).

> [!NOTE]
> - Podpora pro použití modulu ikony košíku v modulech záhlaví je k dispozici od Dynamics 365 Commerce verze 10.0.11.
> - Podpora pro použití modulu voliče webu v modulech záhlaví je k dispozici od Dynamics 365 Commerce verze 10.0.14.
> - Podpora pro použití modulu voliče obchodu v modulech záhlaví je k dispozici od Dynamics 365 Commerce verze 10.0.15.

## <a name="header-module-in-the-adventure-works-theme"></a>Modul záhlaví v motivu Adventure Works

V motivu Adventure Works podporuje modul záhlaví vlastnost **Mobilní logo**. Tato vlastnost umožňuje zadat logo pro mobilní zobrazení. Vlastnost **Mobilní logo** je k dispozici jako rozšíření definice modulu.

> [!IMPORTANT]
> Motiv Adventure Works je k dispozici od Dynamics 365 Commerce verze 10.0.20.

## <a name="create-a-header-fragment-for-a-page"></a>Vytvoření fragmentu záhlaví stránky

Chcete-li vytvořit fragment záhlaví, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu a poté klepněte na tlačítko **OK**.
1. Vyberte pozici **Výchozí kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit obrazovku**.
1. V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte moduly **Souhlas se soubory cookie**, **Záhlaví** a **Propagační banner** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu **Propagační banner** vyberte **Přidat zprávu** a potom vyberte **Zpráva**.
1. V dialogovém okně **Zpráva** přidejte text a odkazy na propagační obsah a poté vyberte **OK**.
1. V podokně vlastností modulu **Souhlas se soubory cookie** přidejte a nakonfigurujte text a odkaz na stránku ochrany osobních údajů webu.
1. V pozici **Navigační nabídka** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Navigační nabídka** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu navigační nabídky v části **Zdroj pro navigační nabídku** vyberte **Server maloobchodu**.
1. V podokně vlastností modulu navigační nabídky v části **Statické položky nabídky** vyberte **Přidat položku nabídky** a potom vyberte **Položka nabídky**. 
1. V dialogovém okně **Položka nabídky** v části **Text položky nabídky** zadejte „Kontakt“.
1. V dialogovém okně **Položka nabídky** v části **Cíl odkazu na položku nabídky** vyberte **Přidat odkaz**.
1. V dialogovém okně **Přidat odkaz** vyberte adresu URL pro stránku „Kontakt“ na webu a vyberte tlačítko **OK**.  
1. V dialogovém okně **Položka nabídky** vyberte **OK**.
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

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul propagačního banneru](add-alert.md)

[Modul navigační nabídky](nav-menu-module.md) 

[Souhlas se soubory cookie](cookie-consent-module.md)

[Modul zápatí](author-footer-module.md)

[Modul volby webu](site-selector.md)

[Modul volby obchodu](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
