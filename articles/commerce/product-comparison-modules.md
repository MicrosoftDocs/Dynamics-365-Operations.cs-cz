---
title: Moduly pro porovnání produktů
description: Tento článek popisuje moduly pro porovnání produktů a jak je implementovat, aby zákazníci mohli porovnávat produkty na webech elektronického obchodu Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 6fd851ce6b32d0772c3fe23c4d7bd4dae2616fdc
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474119"
---
# <a name="product-comparison-modules"></a>Moduly pro porovnání produktů

[!include [banner](../includes/banner.md)]

Tento článek popisuje moduly pro porovnání produktů a jak je implementovat, aby zákazníci mohli porovnávat produkty na webech elektronického obchodu Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Moduly tlačítek pro porovnání produktů a porovnání produktů jsou k dispozici od vydání Dynamics 365 Commerce verze 10.0.29. Lze je použít pro weby typu business-to-consumer (B2C) i business-to-business (B2B).

Funkce porovnávání produktů umožňuje nakupujícím porovnávat podrobnosti o produktech na stránce porovnání produktů, což jim pomůže lépe se rozhodovat o nákupu. Tato funkce se konfiguruje v nástroji na vytváření webu Commerce pomocí modulu porovnání produktů. Na stránkách se seznamem produktů (PLP), jako jsou výsledky kategorií, výsledky vyhledávání a stránky kolekcí produktů, můžete nakonfigurovat tlačítko pro porovnání produktů, které umožní nakupujícím přidávat produkty na srovnávací panel. Tato funkce se konfiguruje v nástroji pro tvorbu webu pomocí modulu tlačítka porovnání produktů, který funguje jako [modul rychlého náhledu](quick-view-module.md).

Když uživatelé webu přidají produkty pro srovnání jejich výběrem na dlaždicích produktů, ve spodní části stránky se zobrazí panel pro porovnání. Porovnávací panel zobrazuje produkty, které nakupující aktuálně porovnává, spolu s krátkými náhledy produktů. Uživatelé webu mohou také přidávat produkty ze stránek s údaji o produktu (PDP) a mohou přidávat konkrétní varianty produktu pro porovnání s hlavními produkty.

Poté, co zákazníci přidají několik produktů na srovnávací panel, mohou si vybrat **Porovnat** a budou přesměrováni na stránku porovnání produktů. Stránka porovnání produktů zobrazuje podrobnosti o produktu pro každý vybraný produkt, takže zákazníci mohou porovnat obrázky, ceny, rozměry produktu (velikost, styl a barva), souhrnné informace o hodnocení a další atributy produktu.

Následující obrázek ukazuje příklady tlačítka porovnat produkt, tlačítka odebrat z porovnání, srovnávacího panelu a stránky porovnání produktů.

![Přehled porovnání produktu zobrazující tlačítko porovnat produkt, tlačítka odebrat z porovnání, srovnávacího panelu a stránky porovnání produktů.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Stránka porovnání produktů porovnává výchozí sadu vlastností produktu a všechny atributy, které lze pro daný produkt zobrazit na PDP.
> - Vlastnosti, jako je režim dodání, zásoby na skladě a měrná jednotka, nelze zobrazit na stránce porovnání produktů.
> - Zákazníci mohou do srovnávacího panelu přidávat produkty z různých kategorií za předpokladu, že produkty jsou ze stejného katalogu.
> - Funkce porovnávání produktů je v současné době omezena na porovnávání produktů v jednotlivém katalogu. Uživatelé webu nemohou provádět srovnání napříč katalogy.
> - Měli byste zajistit, aby vlastnost **Vykreslit modul na straně klienta** byla vymazána pro všechny moduly porovnání produktů.
> - Měli byste zajistit, aby bylo ukládání do mezipaměti na úrovni stránky zakázáno pro všechny stránky, na kterých se používá modul porovnání produktů. Tyto stránky zahrnují PDP, PLP a stránky srovnání produktů. Další informace získáte v tématu [Konfigurace ukládání stránek do mezipaměti](e-commerce-extensibility/page-caching.md).

Následující obrázek znázorňuje příklad stránky se srovnáním produktů.

![Stránka s porovnáním produktů.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Přidejte modul porovnání produktů na novou stránku porovnání produktů

Můžete vytvořit vyhrazenou stránku pro porovnání produktů přidáním modulu porovnání produktů do těla stránky. Kromě toho, že zákazníkům umožníte porovnávat údaje různých produktů, můžete modul porovnání produktů nakonfigurovat tak, aby zákazníci měli možnost rychle provést nákup po porovnání produktů. Modul pro porovnání produktů také obsahuje slot **Prázdné srovnání**, kam můžete přidat modul bloku obsahu, který popisuje prázdný stav (například „Vaše porovnání produktů je prázdné“).

Chcete-li přidat modul pro porovnání produktů na novou stránku porovnání produktů, postupujte následujícím způsobem.

1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte vhodný název stránky (například **Porovnání produktů**) a poté vyberte **Další**.
1. V části **Zvolte šablonu** vyberte vhodnou šablonu (například šablonu, která byla použita na výchozí stránce kategorie) a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**.
1. V pozici **Hlavní** vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Porovnání produktu** a poté klikněte na tlačítko **OK**.
1. V pozici **Tlačítko rychlého zobrazení** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Rychlé zobrazení produktu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu napravo nakonfigurujte vlastnosti modulu **Rychlé zobrazení produktu**.
1. V pozici **Prázdné porovnání** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Blok obsahu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu nakonfigurujte vlastnosti modulu **Blok obsahu**: 
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Následující obrázek ukazuje příklad prázdné stránky pro porovnání v konfigurátoru webů.

![Modul pro porovnání produktů.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Přidání tlačítka pro porovnání produktů na dlaždice produktů na stránkách s výsledky vyhledávání a kategorií

Tlačítko porovnání produktů umožňuje uživatelům rychle přidat produkt na panel porovnání, když prochází produkty na stránce seznamu. Může přidat jeden nebo více produktů na porovnávací panel ze stránky seznamu, aniž by musel přejít do PDP.

Tlačítko porovnání produktu podporuje moduly kolekce produktů, výsledků vyhledávání a buy box PDP.

Chcete-li přidat tlačítko pro porovnání produktů na dlaždice produktů na stránkách s výsledky vyhledávání a kategorií, postupujte následovně.

1. V konfigurátoru webu přejděte na **Stránky** a otevřete stránku kategorie, na kterou chcete přidat tlačítko srovnání produktů.
1. V pozici **Hlavní** vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Výsledky vyhledávání** a poté klikněte na tlačítko **OK**.
1. V pozici **Tlačítko pro porovnání produktů** modulu **Výsledky vyhledávání** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Tlačítko pro porovnání produktu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu napravo nakonfigurujte vlastnosti modulu **Tlačítko pro porovnání produktů**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Zadejte maximální počet produktů, které se mají zobrazit na srovnávacím panelu

Můžete zadat maximální počet produktů, které se mají zobrazit v porovnávacím panelu, tím, že přejdete na **Nastavení webu \> Rozšíření** v konfigurátoru webu. Můžete nakonfigurovat samostatné maximální limity pro zobrazení na počítači a zobrazení pro mobily/tablety. Ve výchozím nastavení nebude vynucován žádný limit, pokud není definován žádný maximální limit.

> [!NOTE]
> Pro optimální procházení doporučujeme nastavit maximální počet produktů ve srovnávacím panelu na **2** pro mobilní zobrazení a **4** pro zobrazení na počítači, abyste snížili množství potřebného vodorovného posouvání.

Chcete-li zadat maximální počet produktů, které se mají zobrazit na srovnávacím panelu, postupujte takto.

1. V konfigurátoru webu přejděte na **Nastavení webu \> Rozšíření**.
1. U vlastnosti **Produkty v limitu srovnání – stolní zařízení** zadejte maximální počet produktů, které by se měly zobrazit na panelu porovnání pro zobrazení stolního počítače.
1. U vlastnosti **Produkty v limitu srovnání – mobilní zařízení a tablety** zadejte maximální počet produktů, které by se měly zobrazit na panelu porovnání pro zobrazení mobilního zařízení a tabletu.
1. Na příkazovém řádku vyberte možnost **Uložit a publikovat**.

![Nastavení webu pro omezení produktů ve srovnávacím panelu.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
