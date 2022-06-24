---
title: Modul popisu cesty
description: Tento článek se zabývá moduly popisu cesty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5f28fa563398773fb714576c3a80d65aec91cee1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862274"
---
# <a name="breadcrumb-module"></a>Modul popisu cesty

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly popisu cesty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly popisu cesty se používají k zajištění sekundární navigace na stránkách webu. Obvykle se zobrazují v horní části stránky pod záhlavím. Přestože lze moduly popisu cesty přidat na jakoukoli stránku, nejčastěji se používají na stránkách podrobností o produktu, aby zobrazovaly hierarchii kategorií produktů a poskytovaly rychlý způsob, jak se pohybovat po webu. Modul popisu cesty lze také použít k zobrazení odkazu „Zpět na výsledky“, když uživatelé otevřou stránku podrobností o produktu ze stránky vyhledávání nebo seznamu. Tímto způsobem se uživatelé mohou rychle vrátit na svou stránku filtrovaného seznamu a pokračovat v nakupování.

Na stránkách, které mají kontext kategorie produktu, jako jsou stránky podrobností o produktu a stránky kategorií, ukazují moduly popisu cesty hierarchii kategorií. Na stránkách, které nemají kontext kategorie, zobrazí moduly popisu cesty standardně **&lt;Kořen webu&gt; / &lt;Aktuální stránka&gt;**. Moduly popisu cesty lze také ručně konfigurovat na jiných typech webových stránek, aby zobrazovaly odkazy na konkrétní stránky na webu.

> [!NOTE]
> Modul popisu cesty je k dispozici v Dynamics 365 Commerce vydání 10.0.12.

Následující obrázek znázorňuje příklad modulu popisu cesty, který zobrazuje hierarchii kategorií na stránce podrobností o produktu.

![Příklad modulu popisu cesty.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Nastavení modulu popisu cesty

Modul popisu cesty řídí nastavení **Typ zobrazení popisu cesty na stránce podrobností o produktu**, které je definováno v **Nastavení webu \> Rozšíření** v tvůrci webů. Toto nastavení má tři mezi možné hodnoty:

- **Zobrazit hierarchii kategorií** – Je-li tato hodnota vybrána, modul popisu cesty zobrazí hierarchii celé kategorie produktu, který je zobrazen na stránce s podrobnostmi o produktu.
- **Zobrazit odkaz Zpět na výsledky** – Když je tato hodnota vybrána, modul popisu cesty zobrazí na stránce podrobností o produktu odkaz „Zpět na výsledky“, pokud uživatel otevřel stránku podrobností o produktu z modulu, který podporuje odkaz „Zpět na výsledky“. Tato funkce je k dispozici, když uživatelé přecházejí ze stránek kategorií, vyhledávání, seznamu a seznamů doporučení. Pro podporu této funkce mají moduly kolekce produktů a výsledků vyhledávání vlastnost, která je pojmenována **Povolit odkaz Zpět na výsledky na stránce podrobností o produktu**. Tato vlastnost vám poskytuje flexibilitu při definování, které moduly by měly podporovat funkci odkazu „Zpět na výsledky“ na stránce podrobností o produktu. Například když je vybrána možnost **Zobrazit odkaz Zpět na výsledky** pro nastavení **Typ zobrazení popisu cesty na stránce podrobností o produktu** a možnost **Povolit odkaz Zpět na výsledky na stránce podrobností o produktu** pro modul výsledků vyhledávání na stránce vyhledávání, odkaz „Zpět na výsledky“ se zobrazí, když uživatelé přejdou ze stránky vyhledávání na stránku podrobností o produktu.
- **Zobrazit hierarchii kategorií a odkaz Zpět na výsledky** – Tato hodnota je kombinací předchozích dvou. Když je tato hodnota vybrána, modul popisu cesty zobrazí na stránce podrobností o produktu jak hierarchii celé kategorie, tak i odkaz „Zpět na výsledky“ (pokud je nakonfigurován).

> [!IMPORTANT]
> Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.12. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Vlastnosti modulu popisu cesty

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Kořen | Text nebo odkaz| Tato volitelná vlastnost určuje text odkazu a cíl odkazu pro kořen webu popisu cesty. Pokud tato vlastnost není nakonfigurována, nebude definován žádný kořen. |
| Odkaz popisu cesty | Propojení | Tato volitelná vlastnost definuje odkazy na ručně konfigurovaný popis cesty, pokud jsou tyto odkazy vyžadovány. Odkazy se zobrazí v pořadí, v jakém jsou uvedeny. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Přidání modulu popisu cesty na novou stránku

Chcete-li přidat modul popisu cesty na stránku podrobností o produktu a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Nastavení webu \> Rozšíření** a pak pro nastavení **Typ zobrazení popisu cesty** na stránce podrobností o produktu vyberte **Zobrazit hierarchii kategorií**.
1. Přejděte na **Šablony** a vyberte šablonu stránky podrobností o produktu.
1. V pozici **Kontejner**, který obsahuje modul buy box, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Popis cesty** a poté klikněte na **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a otevřete stránku podrobností o produktu, která používá šablonu stránky podrobností o produktu. Pokud stránka podrobností o produktu ještě neexistuje, vytvořte ji.
1. V pozici **Kontejner**, který obsahuje modul buy box, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Popis cesty** a poté klikněte na **OK**.
1. V podokně vlastností pozice **Popis cesty** v sekci **Kořen** vyberte **Text odkazu**.
1. V dialogovém okně **Text odkazu** zadejte **Domů** a poté v sekci **Cíl odkazu** vyberte **Přidat odkaz**.
1. V dialogovém okně **Přidat odkaz** vyberte odkaz pro kořen popisu cesty a poté klepněte na tlačítko **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul navigační nabídky](nav-menu-module.md)

[Modul pro výběr lokality](site-selector.md)

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Moduly kolekce produktů](product-collection-module-overview.md)

[Modul buy boxu](add-buy-box.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
