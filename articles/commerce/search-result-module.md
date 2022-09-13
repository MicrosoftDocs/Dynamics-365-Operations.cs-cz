---
title: Modul výsledků hledání
description: Tento článek se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405286"
---
# <a name="search-results-module"></a>Modul výsledků hledání

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul výsledků vyhledávání vrátí výsledky vyhledávání produktů a seznam příslušných zpřesnění pro produkty. Moduly výsledků hledání na webech Dynamics 365 Commerce lze použít k vykreslení stránek pro následující scénáře:

- Výsledky vyhledávání, které jsou spuštěny vyhledáváním uživatelů
- Výsledky vyhledávání, které zobrazují konkrétní sadu produktů, například „Nakupujte podobný vzhled“
- Seznamy produktů, které patří do kategorie

Další informace o kategoriích a stránkách s výsledky vyhledávání najdete v části [Výchozí cílová stránka kategorie a přehled stránky s výsledky vyhledávání](category-search-page-overview.md).

Následující obrázek ukazuje příklad stránky výsledků hledání pro kategorii na webu Fabrikam.

![Příklad stránky výsledků vyhledávání na webu Fabrikam.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Vlastnosti modulu výsledků hledání

V následující tabulce jsou uvedeny vlastnosti modulů výsledků hledání spolu s jejich hodnotami a popisy.

| Vlastnost | Hodnoty | popis |
|----------|--------|-------------|
| Počet položek na stránku | Celé číslo | Počet položek, které by měly být zobrazeny na každé stránce. |
| Povolit zpět na PDP | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, když uživatel vybere produkt na stránce s výsledky vyhledávání, navigace s popisem cesty na stránce s podrobnostmi o produktu (PDP), která je otevřena, zobrazí odkaz „Zpět na výsledky“. |
| Rozbalit zpřesnění | **Všechno**, **1**, **2**, **3** nebo **4** | Počet nejlepších upřesnění, které by se měly při načtení stránky rozšířit. Například, pokud je tato vlastnost nastavena na **3**, budou rozbaleny první tři upřesnění na stránce. |
| Skrýt zobrazení hierarchie kategorií | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, zobrazení hierarchie kategorií na stránce bude skryto. Tato vlastnost by měla být nastavena na **True**, pokud používáte [modul popisu cesty](add-breadcrumb.md) pro zobrazení hierarchie kategorií.|
| Zahrnout do výsledků vyhledávání atributy produktu | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, budou vráceny atributy produktů ve výsledcích hledání. Ačkoli tyto atributy lze zobrazit na webu Commerce, je nutné rozšíření.|
| Zobrazit ceny na pobočkách | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, ceny umístění pro produkty se zobrazí ve výsledcích vyhledávání, když přihlášený uživatel prochází stránku. |
| Aktualizujte panel zpřesnění | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, panel zpřesnění bude aktualizován, jakmile budou vybrána zpřesnění. V tomto režimu se některá zpřesnění s vícenásobným výběrem budou při aktualizaci panelu zpřesnění chovat jako zpřesnění s jedním výběrem. |

> [!IMPORTANT]
> V Commerce verze 10.0.16 a novější lze konfiguraci **Zobrazit ceny umístění** použít k zobrazení cen umístění na stránce.
>
> Ve verzi Commerce verze 10.0.20 a novějších lze konfiguraci **Aktualizujte panel zpřesnění** použít k aktualizaci panelu zpřesnění během výběru zpřesnění.

## <a name="supported-modules"></a>Podporované moduly

Modul výsledků vyhledávání podporuje [modul rychlého zobrazení](quick-view-module.md), který umožňuje uživatelům prohlížet informace o produktu a přidávat položky do košíku ze stránky výsledků vyhledávání.

## <a name="add-a-search-results-module-to-a-category-page"></a>Přidat modul výsledků vyhledávání na stránku kategorie

Chcete-li přidat modul výsledků vyhledávání na stránku kategorie v konfigurátoru webů, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** zadejte název **Výsledků vyhledávání** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (...) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Popis cesty** a poté klikněte na **OK**.
1. V podokně vlastností **Popis cesty** zadejte hodnotu **1** pro **Min. počet výskytů**.
1. V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Výsledky vyhledávání** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Výsledky vyhledávání** zadejte hodnotu **1** pro **Min. počet výskytů** a poté nastavte další požadované vlastnosti modulu výsledků hledání. Nastavením těchto vlastností v šabloně zajistíte, že veškerá přizpůsobení konkrétní stránce kategorie budou tato nastavení automaticky zahrnovat.
1. Chcete-li publikovat šablonu, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte **Stránka kategorie** a poté vyberte **Další**.
1. V části **Vyberte šablonu** vyberte vytvořenou šablonu **Výsledky vyhledávání** a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="inventory-aware-search-results-module"></a>Modul výsledků vyhledávání s ohledem na zásoby

Modul výsledků vyhledávání lze konfigurovat tak, aby zahrnoval data inventáře a poskytoval následující možnosti:

- Zobrazit vedle produktů štítky úrovně zásob.
- Skryjte produkty, které nejsou skladem, v seznamu produktů.
- Zobrazte produkty, které nejsou skladem, na konci seznamu výsledků vyhledávání.
- Podporovat filtrování produktů na základě zásob.

Chcete-li povolit tyto funkce, musíte nejprve povolit funkci **Vylepšené zjišťování produktů v elektronickém obchodování s ohledem na zásoby** a poté nakonfigurovat nutná nastavení v Commerce headquarters. Další informace viz [Zobrazení produktů s ohledem na zásoby](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul rychlého zobrazení](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
