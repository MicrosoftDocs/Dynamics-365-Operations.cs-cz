---
title: Moduly kolekce produktů
description: V tomto tématu je uveden přehled modulů kolekcí produktů v aplikaci Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785460"
---
# <a name="product-collection-modules"></a>Moduly kolekce produktů  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu je uveden přehled modulů kolekcí produktů v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Objevování produktů je primární nástroj, který maloobchodníci používají pro zapojení svých zákazníků na webu e-Commerce. Moduly kolekcí produktů pomáhají prodejcům vytvářet působivé možnosti nakupování poskytnutím intuitivního vizuálního rozhraní, které lze použít k rychlému vytváření kolekcí produktů.

Moduly kolekcí produktů představují fyzické produkty a služby na webu. Modul pro kolekci produktů je obvykle propojen se stránkou podrobností, kde mohou zákazníci nakupovat produkt nebo službu, nebo se o nich dozvědět více. 

Zdroje pro kolekce produktů mohou být seznamy tří typů:

- Redakční seznamy produktů, které jsou ručně definovány v Dynamics 365 Retail jako související produkty pro produkt nebo seznamy produktů
- Algoritmy, jako jsou seznamy nových, nejlépe prodávaných a trendových produktů
- Seznamy doporučení na základě strojového učení

Na následujícím obrázku jsou znázorněny různé typy kolekcí produktů, které se používají na webu e-Commerce.

![Příklad různých typů kolekcí produktů na webu e-Commerce](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Vždy používat moduly kolekcí produktů k zobrazení skupiny produktů podobného typu nebo motivu.

## <a name="product-collection-modules-and-types"></a>Moduly kolekce produktů a typy

V následující tabulce jsou popsány různé typy modulů kolekcí produktů v Dynamics 365 Commerce.

| Modul kolekce produktů  | Typ | Popis |
|----------------------------|------|-------------|
| Procházení kategorií            | Redakční | Tento typ modulu kolekce produktů používá hierarchii navigačních kategorií, kterou maloobchodní prodejce vytvořil pro maloobchodní kanál, aby zobrazila tok procházení pro produkty nabízené v určité kategorii webů. |
| Výsledky hledání             | Vyhledávání | Tento typ modulu kolekce produktů zobrazuje seznam produktů, které nejlépe vyhovují vyhledávacímu dotazu zadanému odběratelem. |
| Související produkty           | Redakční | Tento typ modulu pro sběr produktů zobrazuje seznam produktů, které správce zboží nakonfiguroval jako související produkty v maloobchodě, pro typ vztahu vybraný autorem. |
| Seznam doporučených produktů      | Redakční | Tento typ modulu kolekce produktů zobrazuje vlastní seznamy, které prodejci a editoři vytvořili v aplikaci Retail. |
| Nové                        | Algoritmický | Tento typ modulu pro kolekci produktů zobrazuje seznam nejnovějších produktů, které byly roztříděny do kanálů a katalogů. |
| Nejprodávanější               | Algoritmický | Tento typ modulu kolekce produktů zobrazuje seznam produktů, které jsou seřazeny podle nejvyššího počtu prodejů. |
| Trendy                   | Algoritmický | Tento typ modulu kolekce produktů zobrazuje seznam nejprodávanějších produktů za dané období. |
| Často nakupované společně | Umělá inteligence/strojové učení | Tento typ modulu kolekce produktů používá strojní učení k analýze zákaznických vzorků a doporučí související položky, které jsou často nakoupeny spolu s daným produktem. |
| Lidem se též líbí           | Umělá inteligence/strojové učení | Tento typ modulu kolekce produktů používá strojní učení k analýze zákaznických vzorků a doporučí související položky, které souvisí s daným produktem. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Přidání modulu kolekce produktů do stránky kategorie

Přidání modulu kolekce produktů do stránky kategorie provedete následovně.

1. V Dynamics 365 Commerce přejděte na web a vytvořte stránku, která používá stejnou šablonu jako výchozí stránka kategorie.
1. V osnově stránky vyberte pozici **podzápatí**, vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte **Kontejner** a pak vyberte možnost **OK**.
1. V modulu kontejner vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte **Kolekce produktů** a pak vyberte možnost **OK**.
1. Nakonfigurujte nastavení výběrem odpovídajícího zdroje dat a vstupů pro kolekci produktů.
1. V podokně vlastnosti modulu kolekce produktů vyberte možnost **Přidat seznam produktů**.
1. V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte typ seznamu, zadejte počet položek a vyberte libovolné další možnosti, které jsou k dispozici pro daný typ seznamu. Další informace o typech seznamu naleznete v následující tabulce. 
1. Vyberte **OK**.
1. Uložit stránku a zarezervovat ji.

V následující tabulce jsou uvedeny typy seznamů, které jsou k dispozici pro výběr v dialogovém okně **Vybrat konfiguraci seznamu produktů**.
   
| Typ                       | Popis | Obecný postup | Kontext, který lze odvodit z kontextu stránky | Kontext, kterým může autor přepsat kontext stránky |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Produkty podle kategorie       | Seznam produktů, které patří do dané kategorie. Tato kategorie je určena buď kontextem stránky, nebo kontextem, který autor poskytuje. | Stránka rozšířené kategorie, domovská stránka, rezervace a stránky s košíkem a stránky s produktem | Kategorie | Kategorie určená autorem |
| Související produkty           | Seznam produktů, které manažer prodeje nakonfiguroval jako související produkt v aplikaci Retail pro typ vztahu. | Stránky produktů, stránky s pokladnou a košíkem, seznam požadovaných položek a stránka zákaznického účtu. | Produkt, typ vztahů (povinný)  | Produkt, typ vztahů |
| Uspořádáno                    | Vlastní seznam, který prodejci a redaktori vytvořili v aplikaci Retail. | Stránka rozšířené kategorie, domovská stránka, rezervace a stránky s košíkem a stránky s produktem | Nelze použít | Výběr seznamu |
| Algoritmický                | <ul><li>**Nový** – seznam nejnovějších produktů, které byly roztříděny do kanálů a katalogů.</li><li>**Nejprodávanější** – seznam produktů, které jsou seřazeny podle nejvyššího počtu prodejů.</li><li>**Trendující** – seznam nejprodávanějších produktů za dané období.</li></ul> | Domovská stránka, stránka rozšířené kategorie a stránky s pokladnou a košíkem | Kategorie | Kategorie určená autorem |
| Často nakupované společně | Seznam. který používá strojní učení k analýze zákaznických vzorků a doporučí související položky, které jsou často nakoupeny spolu s daným produktem. | Stránky produktů a stránky pokladny a košíku | Produkt, košík | Zahrnout košík |
| Lidem se též líbí           | Seznam. který používá strojní učení k analýze zákaznických vzorků a doporučí položky, které souvisí s daným produktem. | Stránky produktů a stránky pokladny a košíku | Produkt, košík | Nelze použít |

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Karuselový modul](add-carousel.md)

[Modul bloku s formátovaným obsahem](add-content-rich-block.md)

[Modul umístění obsahu](add-content-placement-modules.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

