---
title: Moduly kolekce produktů
description: V tomto článku je uveden přehled modulů kolekcí produktů v aplikaci Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 05/18/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 2ad50011e2f4c037a75c8c4b195c728bb58c3b47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269855"
---
# <a name="product-collection-modules"></a>Moduly kolekce produktů

[!include [banner](includes/banner.md)]

V tomto článku je uveden přehled modulů kolekcí produktů v aplikaci Microsoft Dynamics 365 Commerce.

Objevování produktů je primární nástroj, který maloobchodníci používají pro zapojení svých zákazníků na webu e-Commerce. Moduly kolekcí produktů pomáhají prodejcům vytvářet působivé možnosti nakupování poskytnutím intuitivního vizuálního rozhraní, které lze použít k rychlému vytváření kolekcí produktů.

Moduly kolekcí produktů představují fyzické produkty a služby na webu. Modul pro kolekci produktů je obvykle propojen se stránkou podrobností, kde mohou zákazníci nakupovat produkt nebo službu, nebo se o nich dozvědět více. 

Zdroje pro kolekce produktů mohou být seznamy následujících čtyř typů:

- Redakční seznamy produktů, které jsou ručně definovány v Dynamics 365 Commerce jako související produkty pro produkt nebo seznamy produktů
- Algoritmy, jako jsou seznamy nových, nejlépe prodávaných a trendových produktů
- Seznamy doporučení na základě strojového učení
- Seznamy přizpůsobení, které podporují individuální výsledky pro odběratele. K zobrazení individuálních výsledků je nutné, aby byli zákazníci přihlášeni k webu e-Commerce. Uživatelé typu Host nevidí individuální výsledky. Zákazníci se mohou odhlásit z vlastního nastavení na [stránce správy účtů](account-management.md).

Na následujícím obrázku jsou znázorněny různé typy kolekcí produktů, které se používají na webu e-Commerce.

![Příklad různých typů kolekcí produktů na webu e-Commerce.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Vždy používat moduly kolekcí produktů k zobrazení skupiny produktů podobného typu.

## <a name="product-collection-modules-and-types"></a>Moduly kolekce produktů a typy

V následující tabulce jsou popsány různé typy modulů kolekcí produktů v Dynamics 365 Commerce.

| Modul kolekce produktů  | Typ | Popis |
|----------------------------|------|-------------|
| Kategorie                   | Kategorie | Tento modul zobrazuje seznam produktů v kategorii dle definice hierarchií kategorií navigace, kterou prodejce vytvořil pro kanál. |
| Související produkty           | Redakční | Tento modul zobrazuje seznam produktů, které správce zboží nakonfiguroval jako související produkty ve velkoobchodě, pro typ vztahu vybraný autorem. |
| Výsledky hledání             | Vyhledávání | Tento typ modulu kolekce produktů zobrazuje seznam produktů, které nejlépe vyhovují vyhledávacímu dotazu zadanému odběratelem. |
| Seznam doporučených produktů      | Redakční | Tento modul zobrazuje vlastní seznamy, které prodejci a redaktori vytvořili v aplikaci Commerce. |
| Nové                        | Algoritmický | Tento modul zobrazuje seznam nejnovějších produktů, které byly roztříděny do kanálů a katalogů. Tento seznam může zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu. |
| Nejprodávanější               | Algoritmický | Tento modul zobrazuje seznam produktů, které jsou seřazeny podle nejvyššího počtu prodejů. Tento seznam může zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu. |
| Trendy                   | Algoritmický | Tento modul zobrazuje seznam nejprodávanějších produktů za dané období. Tento seznam může zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu. |
| Často nakupované společně | Umělá inteligence/strojové učení | Tento modul používá strojní učení k analýze zákaznických vzorků a doporučí související položky, které jsou často nakoupeny spolu s daným produktem. Tento seznam může zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu. |
| Lidem se též líbí           | Umělá inteligence/strojové učení | Tento modul používá strojní učení k analýze zákaznických vzorků a doporučí položky, které souvisí s daným produktem. Tento seznam může zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu. |
| Výběry pro vás              | Umělá inteligence/strojové učení | Tento modul využívá strojového učení k analýze nákupních vzorců přihlášeného uživatele a k poskytnutí individuálních doporučení založených na těchto vzorcích nákupu. Pro uživatele typu host bude tento seznam sbalen. |

## <a name="supported-modules"></a>Podporované moduly 

Modul kolekce produktů podporuje [modul rychlého zobrazení](quick-view-module.md), který umožňuje uživatelům prohlížet informace o produktu a přidávat položky do košíku ze stránky kolekce produktů.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Přidání modulu kolekce produktů do stránky kategorie

Přidání modulu kolekce produktů do stránky kategorie provedete následovně.

1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte vhodný název stránky a poté vyberte **Další**.
1. V části **Zvolte šablonu** vyberte stejnou šablonu, jaká byla použita na výchozí stránce kategorie, a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**. 
1. V pozici **Dílčí zápatí** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Kolekce produkt** a poté klikněte na tlačítko **OK**.  
1. V podokně vlastnosti modulu kolekce produktů vyberte možnost **Přidat seznam produktů**.
1. V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte typ seznamu, zdroj seznamu a zadejte počet položek. Nakonfigurujte jakékoli další možnosti dostupné pro typ seznamu. Další informace o typech seznamu naleznete v následující tabulce. 
1. Vyberte **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

V následující tabulce jsou uvedeny typy seznamů, které jsou k dispozici pro výběr v dialogovém okně **Vybrat konfiguraci seznamu produktů**.

| Typ                       | Popis | Použití | Kontext stránky | Specifický kontext | Individuální nastavení |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Produkty podle kategorie       | Seznam produktů, které patří do dané kategorie. Tato kategorie je určena buď kontextem stránky, nebo kontextem, který autor poskytuje. | Tento typ seznamu lze použít na libovolné stránce (například na domovské stránce, na stránce kategorií, na marketingové stránce nebo na stránce s podrobnými informacemi o produktech \[PDP\]) k propagaci určité kategorie produktů. | Kategorie z kontextu stránky, kde je k dispozici (například stránka kategorie) | Autor může zadat specifickou kategorii jako kontext pro seznam. | Nelze použít |
| Související produkty           | Seznam produktů, které manažer prodeje nakonfiguroval jako související produkt pro typ vztahu v aplikaci Commerce. | Tento typ seznamu se primárně používá v PDP, ale lze jej použít na libovolné stránce, pokud je k dispozici nadřazený produkt. | Produkt ze stránky, typ vztahu (povinný) | Produkt lze zvolit ve výběru a je použit typ vztahu. | Nelze použít |
| Uspořádáno                    | Vlastní seznam, který prodejci a redaktori vytvořili v aplikaci Commerce. | Stránka rozšířené kategorie, domovská stránka, rezervace a stránky s košíkem a stránky s produktem | Nelze použít | Nelze použít | Nelze použít |
| Algoritmický                | <ul><li>**Nový** – seznam nejnovějších produktů, které byly roztříděny do kanálů a katalogů.</li><li>**Nejprodávanější** – seznam produktů, které jsou seřazeny podle nejvyššího počtu prodejů.</li><li>**Trendující** – seznam nejprodávanějších produktů za dané období.</li></ul> | Domovská stránka, stránka rozšířené kategorie a stránky s pokladnou a košíkem | Kategorie z kontextu stránky (například stránka kategorie) | Kategorie určená autorem webu. | Podporováno |
| Často nakupované společně | Seznam. který používá strojní učení k analýze zákaznických vzorků a doporučí související položky, které jsou často nakoupeny spolu s daným produktem. | Tento typ seznamu lze použít pouze na stránce nákupního košíku. | Košík | Nelze použít | Podporováno |
| Lidem se též líbí           | Seznam. který používá strojní učení k analýze zákaznických vzorků a doporučí položky, které souvisí s daným produktem. | Tento typ seznamu se používá v PDPs k zobrazení produktů zakoupených jinými zákazníky. | Kontext produktu ze stránky | Produkt poskytnutý autorem webu. | Podporováno |
| Výběry pro vás              | Seznam, který používá strojové učení k určení preferencí zákazníka. | Tento typ seznamu lze použít na libovolné stránce. | Nelze použít| Nelze použít | Podporováno | 

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Karuselový modul](add-carousel.md)

[Modul bloku bohatého na obsah](add-content-rich-block.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Přehled doporučení produktu](product-recommendations.md)

[Modul rychlého zobrazení](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
