---
title: Modul buy boxu
description: Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: dce3c8adcd2926e60d001bddb5c278fac6860268
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796215"
---
# <a name="buy-box-module"></a>Modul buy boxu

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Termín *buy box* se obvykle vztahuje k oblasti stránky s podrobnostmi o produktu, která se nachází „above the fold“ a která je hostitelem nejdůležitějších informací vyžadovaných k provedení nákupu produktu. (Oblast „above the fold“ je viditelná po prvním načtení stránky, takže uživatelé nemusejí posouvat zobrazení směrem dolů, aby ji viděli.)

Modul buy boxu je speciální kontejner, který slouží k hostování všech modulů, které jsou zobrazeny v oblasti buy boxu na stránce podrobností produktu.

Adresa URL stránky s podrobnostmi o produktu obsahuje ID produktu. Všechny informace, které jsou požadovány pro vygenerování modulu buy boxu, jsou odvozeny z tohoto ID produktu. Není-li zadáno ID produktu, nebude modul buy boxu na stránce správně vykreslen. Modul buy boxu lze proto použít pouze na stránkách, které mají kontext produktu. Chcete-li použít položku na stránce, která nemá kontext produktu (například domovskou stránku nebo marketingovou stránku), je nutné provést další úpravy.

Následující obrázek ukazuje příklad modulu buy boxu na stránce s podrobnostmi o produktu.

![Příklad modulu buy boxu](./media/ecommerce-pdp-buybox.PNG)

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
- **Přidat produkt do nákupního košíku** – Tato vlastnost se používá ke specifikaci chování po přidání položky do košíku. Možné hodnoty jsou **Přejít na stránku nákupního košíku**, **Nepřecházet na stránku nákupního košíku** a **Zobrazit oznámení**. Když je tato hodnota nastavena na **Přejít na stránku nákupního košíku**, uživatelé jsou po přidání položky přesměrováni na stránku nákupního košíku. Když je tato hodnota nastavena na **Nepřecházet na stránku nákupního košíku**, uživatelé nejsou po přidání položky přesměrováni na stránku nákupního košíku. Když je hodnota nastavena na **Zobrazit oznámení**, uživatelům se zobrazí potvrzovací oznámení a poté mohou nadále procházet stránku podrobností o produktu. 

> [!IMPORTANT]
> Nastavení webu **Přidat produkt do nákupního košíku** jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.11. Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json. Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

Následující obrázek ukazuje příklad potvrzovacího oznámení „přidáno do košíku“ na webu Fabrikam.

![Příklad modulu oznámení](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Modul buy boxu načítá informace o produktu pomocí rozhraní API Commerce Scale Unit. ID produktu ze stránky s podrobnostmi o produktu slouží k načtení všech informací.

## <a name="add-a-buy-box-module-to-a-page"></a>Přidání modulu buy boxu na stránku

Chcete-li přidat modul buy boxu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Buy box**.
1. V části **Název fragmentu** zadejte název pro **Fragment buy boxu** a poté vyberte **OK**.
1. V pozici **Galeria médií** modulu buy boxu vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Galerie médií** a poté klikněte na tlačítko **OK**.
1. V pozici **Volba obchodu** modulu buy boxu vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona stránky podrobností o produktu** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na výchozí stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Výběr fragmentu** vyberte **Fragment buy boxu**, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona stránky podrobností o produktu**. V části **Název stránky** zadejte **Stránka podrobností o produktu** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Výběr fragmentu** vyberte **Fragment buy boxu**, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.
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

[Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md)

[SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]