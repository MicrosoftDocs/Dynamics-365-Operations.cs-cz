---
title: Modul navigační nabídky
description: Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b112bb453e0840120c63038bf8d6897fbf5ff288
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798746"
---
# <a name="navigation-menu-module"></a>Modul navigační nabídky

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Primárním účelem modulů navigační nabídky je umožnit uživatelům webu procházet produkty a stránky webu podle hierarchie navigace sítě definované v centrále Dynamics 365 Commerce. Položky konfigurované v modulu navigační nabídky se zobrazují jako navigace v záhlaví webu. Moduly navigační nabídky také podporují statické položky nabídky, které odkazují na jiné stránky na webu elektronického obchodu.

Modul navigační nabídky lze přidat do modulu záhlaví stránky. V motivu Fabrikam zobrazuje navigační nabídka ve výchozím nastavení dvě úrovně. V motivu Starter zobrazuje navigační nabídka ve výchozím nastavení tři úrovně. Chcete-li změnit počet úrovní, je u motivu vyžadováno rozšíření zobrazení.

Následující obrázek ukazuje příklad navigační nabídky pro web Fabrikam se dvěma úrovněmi hierarchie kategorií a některými položkami statické nabídky.
![Příklad modulu navigační nabídky](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Vlastnosti modulu navigační nabídky

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Zdroj                  | **Maloobchod**, **Ruční vytváření**, **Maloobchod a ruční vytváření** | Hodnota **Maloobchod** umožňuje v navigační nabídce zobrazit hierarchii navigace sítě z centrály Commerce. Hodnota **Ruční vytváření** umožňuje doporučovat statické položky nabídky. Hodnota **Maloobchod a ruční vyváření** umožňuje kombinaci obou. |
| Zobrazení obrázků kategorií | **Pravda** nebo **nepravda**    | Je-li povolena, tato vlastnost zobrazuje obrázky kategorií v navigační nabídce, jak je definováno v centrále Commerce pro každou kategorii. Přidáno v Comerce verze 10.0.14. |
| Zobrazit propagační akce | **Pravda** nebo **nepravda** | Když je tato vlastnost povolena, lze propagační akce konfigurovat pomocí obrázků, odkazů a textu. Tato vlastnost byla přidána ve verzi Commerce verze 10.0.17. |
| Přidejte propagační akce | Text, obrázek nebo odkaz | Když je povolena vlastnost **Zobrazit propagační akce**, můžete v navigační nabídce přidat text, obrázek nebo odkaz jako propagační obsah. |
| Povolení navigační nabídky s více úrovněmi | **Pravda** nebo **nepravda** | Když je tato vlastnost povolena, navigační nabídka může zobrazit více úrovní navigační hierarchie. Tato funkce je k dispozici v aplikaci Commerce verze 10.0.15. |
| Počet úrovní | Celé číslo | Tato vlastnost definuje počet úrovní, které se mají zobrazit, pokud je vlastnost **Povolit navigační nabídku s více úrovněmi** je nastavena na **Pravda**. |
| Statická položka nabídky| Pole hodnot| Statické položky nabídky, které přidružují název položky nabídky s odkazem na stránku statického webu. Položky nabídky můžete vytvořit pod dalšími položkami nabídky. Ve výchozím nastavení se statické nabídky zobrazují na kořenové úrovni a budou přidány do hierarchie navigace sítě, pokud existuje. |
| Zobrazení kořenové nabídky | **Pravda** nebo **nepravda** | Když je tato vlastnost povolena, lze navigační nabídku definovat pod vlastním kořenem (například **Koupit**). Tato funkce je k dispozici ve vydání Dynamics 365 Commerce 10.0.15. |
| Kořenová nabídka | řetězec | Tuto vlastnost lze použít k definování textu pro vlastní kořen, pokud je vlastnost **Zobrazit kořenovou nabídku** nastavena na **Pravda**. |

Následující obrázek ukazuje příklad obrázku kategorie zobrazeného v navigační nabídce pro web Fabrikam.
![Příklad modulu navigační nabídky s obrázky kategorií](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Přidání modul navigační nabídky do modulu záhlaví

Podrobnosti, jak přidat modul navigační nabídky do modulu záhlaví, viz [Modul záhlaví](author-header-module.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul popisu cesty](add-breadcrumb.md)

[Modul volby lokality](site-selector.md)

[Modul buy boxu](add-buy-box.md)

[Zásady zacházení se soubory cookie](cookie-compliance.md)

[Modul záhlaví](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
