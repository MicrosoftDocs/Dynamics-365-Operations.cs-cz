---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411266"
---
# <a name="cart-module"></a>Modul košíku

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul košíku zobrazuje položky, které byly přidány do košíku, než odběratel pokračuje v rezervaci. Modul také zobrazuje souhrn objednávky a umožňuje odběrateli použití nebo odebrání propagačních kódů.

Modul košíku podporuje přihlášené uživatele i hosty. Také podporuje odkaz **Zpět na nákupy**. Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.

Modul košíku vykresluje data založená na ID košíku, což je soubor cookie prohlížeče dostupný v rámci celého webu. 

Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.

![Příklad modulu nákupního košíku](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Vlastnosti a pozice modulu košíku

Modul košíku má vlastnost **Záhlaví**, kterou lze nastavit na hodnoty, jako je **Nákupní taška** a **Položky v košíku**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduly, které lze použít v modulu košíku

- **Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku. Zprávy řídí systém správy obsahu (CMS). Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.
- **Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí. Další informace o tomto modulu naleznete v tématu [Modul volič obchodů](store-selector.md).

## <a name="module-properties"></a>Vlastnosti modulu

Následující nastavení modulu nákupního košíku lze konfigurovat na **Nastavení webu \> Rozšíření**:

- **Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).
- **Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**. Postup lze konfigurovat na úrovni webu a umožnit maloobchodním prodejcům, aby se odběratel mohl vrátit na domovskou stránku nebo na jakoukoli jinou stránku na webu.

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit. ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Přidání modulu košíku na stránku

Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty stránky** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment stránky** vyberte modul **Nákupní košík**.
1. V části **Název fragmentu stránky** zadejte název pro **Fragment nákupního košíku** a poté vyberte **OK**.
1. Vyberte pozici **Nákupní košík**.
1. V podokně vlastností vpravo vyberte symbol tužky, do pole zadejte text záhlaví a poté zaškrtněte symbol zaškrtnutí.
1. V pozici **Nákupní košík** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název šablony.
1. Ve stromové struktuře vyberte pozici **Obsah**, vyberte tři tečky (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat fragment stránky** vyberte **Fragment nákupního košíku** a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu, kterou jste vytvořili, zadejte název stránky a pak vyberte tlačítko **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul volby obchodu](store-selector.md)

[Modul buy boxu](add-buy-box.md)

[Ikona modulu košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)

[Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md)
