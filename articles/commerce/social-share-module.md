---
title: Modul sdílení na sociálních sítích
description: Tento článek se zabývá moduly pro sdílení na sociálních sítích a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88bc5469e3072b625836cc942efbd2206f6dd6ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284677"
---
# <a name="social-share-module"></a>Modul sdílení na sociálních sítích

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly pro sdílení na sociálních sítích a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly pro sdílení na sociálních sítích umožňují uživatelům sdílet adresy URL webových stránek e-Commerce na sociálních médiích, jako je Facebook , Twitter, Pinterest a LinkedIn. Adresy URL webových stránek lze také sdílet prostřednictvím e-mailu. Moduly pro sdílení na sociálních sítích se běžně používají na stránkách s podrobnostmi o produktu (PDP), které uživatelům pomáhají sdílet informace o produktu.

Každý modul pro sdílení na sociálních sítích je kontejnerem pro moduly položek pro sdílení na sociálních sítích. Každý modul položky pro sdílení na sociálních sítích lze nakonfigurovat tak, aby odkazoval na konkrétní web sociálních médií. Integrace se službami Facebook, Twitter, Pinterest, LinkedIn a e-mailem jsou podporovány ihned z výroby. Když uživatel webu vybere symbol sociálního média, spustí se iframe HTML pro příslušný web sociálního média. V rámci iframe se uživatel může přihlásit a zveřejnit obsah stránky, kterou prohlížel.

Každá platforma sociálních médií může sledovat soubory cookie, takže tento modul vyžaduje, aby uživatelé stránek přijali zprávu s oznámením o souhlasu se soubory cookie. Pokud souhlas se soubory cookies nebude přijat, bude modul na stránce skrytý. Další informace viz [Zásady zacházení se soubory cookie](cookie-compliance.md).

Následující obrázek znázorňuje příklad modulu pro sdílení na sociálních sítích použitého na stránce s podrobnostmi o produktu.

![Příklad modulu pro sdílení na sociálních sítích.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Vlastnosti modulu pro sdílení na sociálních sítích

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Titulek                  | Text | Tato vlastnost určuje titulek modulu. |
| Orientace | **Horizontální** nebo **Vertikální**  | Tato vlastnost definuje orientaci rozložení pro položky sociálních médií. |

## <a name="social-share-item-module-properties"></a>Vlastnosti modulu položky pro sdílení na sociálních sítích
| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Sociální média              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail** | Rozbalovací nabídka se seznamem platforem sociálních médií. |
| Ikona |Obrázek    | Toto bude obrázek, který se zobrazí pro příslušné sociální médium. Doporučujeme použít SDK platformy sociálních médií pro výběr doporučeného obrázku jednotlivých platforem. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Přidání modulu pro sdílení na sociálních sítích do modulu buy boxu

Chcete-li přidat modul pro sdílení na sociálních sítích do modulu buy boxu, postupujte takto.

1. Na webu Fabrikam vyberte **Stránky** a potom vyberte stránku **DefaultPDP** pro otevření stránky s podrobnostmi o produktu. 
1. V pozici **Buybox (povinné)** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Sdílení na sociálních sítích** a poté klikněte na tlačítko **OK**.
1. V pozici **Sdílení na sociálních sítích** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **SocialShare** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu **SocialShare** v sekci **Orientace** vyberte **Horizontální** . Podle potřeby přidejte titulek.
1. V pozici **SocialShare** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **SocialShareItem** a poté klikněte na **OK**.
1. V podokně vlastností modulu **SocialShareItem** v sekci **SocialMedia** vyberte **Facebook**.
1. V podokně vlastností modulu **SocialShareItem** v sekci **Ikona** vyberte **+ Přidat obrázek**.
1. V dialogovém okně **Výběr média** vyberte obrázek loga Facebook a poté klikněte na tlačítko **OK**. Jestli není dostupný obrázek s logem Facebook, volbou **Odeslat novou mediální položku** jej nahrajte.
1. Přidejte a nakonfigurujte další moduly **SocialShareItem** podle potřeby.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Na stránce se zobrazí modul pro sdílení na sociálních sítích.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Zásady zacházení se soubory cookie](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
