---
title: Modul buy boxu
description: Tento článek se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5167aac784bb3ab6a63033590178c2eead627b96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863541"
---
# <a name="buy-box-module"></a>Modul buy boxu

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Termín *buy box* se obvykle vztahuje k oblasti stránky s podrobnostmi o produktu (PDP), která se nachází „above the fold“ a která je hostitelem nejdůležitějších informací vyžadovaných k provedení nákupu produktu. (Oblast „above the fold“ je viditelná po prvním načtení stránky, takže uživatelé nemusejí posouvat zobrazení směrem dolů, aby ji viděli.)

Modul buy boxu je speciální kontejner, který slouží k hostování všech modulů, které jsou zobrazeny v oblasti buy boxu na stránce podrobností produktu.

Adresa URL stránky s podrobnostmi o produktu obsahuje ID produktu. Všechny informace, které jsou požadovány pro vygenerování modulu buy boxu, jsou odvozeny z tohoto ID produktu. Není-li zadáno ID produktu, nebude modul buy boxu na stránce správně vykreslen. Modul buy boxu lze proto použít pouze na stránkách, které mají kontext produktu. Chcete-li použít položku na stránce, která nemá kontext produktu (například domovskou stránku nebo marketingovou stránku), je nutné provést další úpravy.

Následující obrázek ukazuje příklad modulu buy boxu na stránce s podrobnostmi o produktu.

![Příklad modulu buy boxu.](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Vlastnosti a pozice modulu buy boxu 

Na stránce s podrobnostmi o produktu je buy box rozdělen na dvě oblasti: oblast médií v levé části a oblast obsahu vpravo. Ve výchozím nastavení je poměr šířky sloupce oblasti médií k šířce sloupce oblast obsahu 2:1. Na mobilních zařízeních obě oblasti navrstveny, takže se jedna oblast zobrazí pod druhou oblastí. Motivy lze použít k přizpůsobení šířky sloupců a rozměru pro skládání.

Modul buy boxu vykreslí název, popis, cenu a hodnocení produktu. Dále odběratelům vybírá varianty produktu, které mají různé atributy produktu, například velikost, styl a barvu. Je-li vybrána varianta produktu, budou další vlastnosti v buy boxu (například popis a obrázky produktu) aktualizovány tak, aby odrážely informace o variantách. 

Výběr množství je k dispozici, takže zákazníci mohou určit množství položek, které mají být zakoupeny. Maximální množství, které lze koupit, lze definovat v nastavení pracoviště.

Z buy boxu mohou zákazníci také provádět akce, jako je přidání produktu do nákupního košíku, přidání produktu do svého seznamu přání a výběr místa výdeje. Tyto akce lze provést u produktu nebo varianty produktu. Chcete-li přidat produkt do seznamu přání, je nutné, aby byl přihlášen zákazník.

Pomocí motivů lze odebrat nebo změnit pořadí vlastností produktu a ovládacích prvků akcí pro buy box. 

## <a name="module-properties"></a>Vlastnosti modulu

- **Značka záhlaví** – Tato vlastnost definuje značku nadpisu produktu. Je-li buy box v horní části stránky, měla by být tato vlastnost nastavena na **H1**, aby vyhovovala standardům usnadnění. 

- **Povolit doporučení typu „podobný vzhled“** – Tato vlastnost umožňuje zobrazit v buy boxu odkazy na produkty, které vypadají podobně jako aktuálně zobrazená položka. Tato funkce je k dispozici v aplikaci Commerce verze 10.0.13 a novější.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduly, které lze použít v modulu buy boxu

- **Galerie médií** – Tento modul slouží k předvedení obrázků produktu na stránce s podrobnostmi o produktu. Další informace o tomto modulu naleznete v části [Modul galerie médií](media-gallery-module.md).
- **Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí. Další informace o tomto modulu naleznete v části [Modul volby obchodu](store-selector.md).
- **Sdílení na sociálních sítích** – Tento modul lze přidat do buy boxu, aby uživatelé mohli sdílet informace o produktu na sociálních médiích. Další informace naleznete v tématu [Modul pro sdílení na sociálních sítích](social-share-module.md).

## <a name="buy-box-module-settings"></a>Nastavení modulu buy boxu

Následující nastavení modulu buy boxu lze konfigurovat na **Nastavení webu \> Rozšíření**:

- **Limit množství na řádku košíku** – Tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).
- **Přidat produkt do košíku** – Informace o tom, jak použít nastavení **Přidat produkt do košíku**, viz [Nastavení přidání produktu do košíku](add-cart-settings.md).

## <a name="buy-box-module-definition-extensions-in-the-adventure-works-theme"></a>Rozšíření definice modulu buy boxu v motivu Adventure Works

Modul buy boxu, který poskytuje motiv Adventure Works, má rozšíření definice modulu, které podporuje implementaci modulu specifikací produktu v modulu Accordion v buy boxu PDP. Chcete-li předvést atributy specifikace produktu v buy boxu PDP, přidejte modul specifikace produktu do slotu modulu Accordion ve slotu buy boxu.


> [!IMPORTANT]
> Motiv Adventure Works je k dispozici od Dynamics 365 Commerce verze 10.0.20.


## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Modul buy boxu načítá informace o produktu pomocí rozhraní API Commerce Scale Unit. ID produktu ze stránky s podrobnostmi o produktu slouží k načtení všech informací.

## <a name="add-a-buy-box-module-to-a-page"></a>Přidání modulu buy boxu na stránku

Chcete-li přidat modul buy boxu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Buy box**.
1. V části **Název fragmentu** zadejte název pro **Fragment buy boxu** a poté vyberte **OK**.
1. V pozici **Galeria médií** modulu buy boxu vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Galerie médií** a poté klikněte na tlačítko **OK**.
1. V pozici **Volba obchodu** modulu buy boxu vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Výběr obchodů** a poté klikněte na **OK**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona stránky podrobností o produktu** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na výchozí stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Výběr fragmentu** vyberte **Fragment buy boxu**, který jste vytvořili, a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránka** zadejte **Stránku podrobností o produktu** a poté vyberte **Další**.
1. V části **Zvolit šablonu** vyberte **Šablona stránky podrobností o produktu** a pak vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**.
1. V pozici **Hlavní** na nové stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Výběr fragmentu** vyberte **Fragment buy boxu**, který jste vytvořili, a pak vyberte tlačítko **OK**.
1. Uložte stránku a zobrazte náhled. Do adresy URL stránky náhledu přidejte parametr řetězce dotazu **?productid=&lt;id produktu&gt;**. Tímto způsobem se pro načtení a vykreslení stránky náhledu použije kontext produktu.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte. Na stránce s podrobnostmi o produktu by se měl zobrazit buy box.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul volby obchodu](store-selector.md)

[Modul galerie médií](media-gallery-module.md)

[Modul kontejneru](add-container-module.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)

[Modul sdílení na sociálních sítích](social-share-module.md)

[Přidání produktu do nastavení košíku](add-cart-settings.md)

[Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
