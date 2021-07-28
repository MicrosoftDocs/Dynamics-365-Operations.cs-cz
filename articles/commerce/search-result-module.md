---
title: Modul výsledků hledání
description: Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 04ffa8e56b72727c079db07f38bfae675ae2abb1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344949"
---
# <a name="search-results-module"></a>Modul výsledků hledání

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

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

Chcete-li přidat modul výsledků vyhledávání na stránku kategorie, postupujte podle následujících kroků.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** zadejte název **Výsledků vyhledávání** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (...) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Popis cesty** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Popis cesty** zadejte hodnotu **1** pro **Min. počet výskytů**.
1. V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výsledky vyhledávání** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Výsledky vyhledávání** zadejte hodnotu **1** pro **Min. počet výskytů** a poté nastavte další požadované vlastnosti modulu výsledků hledání. Nastavením těchto vlastností v šabloně zajistíte, že veškerá přizpůsobení konkrétní stránce kategorie budou tato nastavení automaticky zahrnovat.
1. Chcete-li publikovat šablonu, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu **Výsledky vyhledávání**, kterou jste vytvořili, zadejte **Stránku kategorie** pro **Název stranky** a pak vyberte tlačítko **OK**. Protože jsou všechny hodnoty nastaveny v šabloně, je stránka připravena k publikování.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul rychlého zobrazení](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
