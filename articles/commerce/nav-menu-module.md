---
title: Modul navigační nabídky
description: Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761373"
---
# <a name="navigation-menu-module"></a>Modul navigační nabídky

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Primárním účelem modulů navigační nabídky je umožnit uživatelům webu procházet produkty a stránky webu podle hierarchie navigace sítě definované v centrále Dynamics 365 Commerce. Položky konfigurované v modulu navigační nabídky se zobrazují jako navigace v záhlaví webu. Moduly navigační nabídky také podporují statické položky nabídky, které odkazují na jiné stránky na webu elektronického obchodu.

Modul navigační nabídky lze přidat do modulu záhlaví stránky. V motivu Fabrikam zobrazuje navigační nabídka ve výchozím nastavení dvě úrovně. V motivu Starter zobrazuje navigační nabídka ve výchozím nastavení tři úrovně. Chcete-li změnit počet úrovní, je u motivu vyžadováno rozšíření zobrazení.

Následující obrázek ukazuje příklad navigační nabídky pro web Fabrikam se dvěma úrovněmi hierarchie kategorií a některými položkami statické nabídky.
![Příklad modulu navigační nabídky](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Vlastnosti modulu navigační nabídky

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Zdroj                  | **Maloobchod**, **Ruční vytváření**, **Maloobchod a ruční vytváření** | Hodnota **Maloobchod** umožňuje v navigační nabídce zobrazit hierarchii navigace sítě z centrály Commerce. Hodnota **Ruční vytváření** umožňuje doporučovat statické položky nabídky. Hodnota **Maloobchod a ruční vyváření** umožňuje kombinaci obou. |
| Zobrazení obrázků kategorií | **Pravda** nebo **nepravda**    | Je-li povolena, tato vlastnost zobrazuje obrázky kategorií v navigační nabídce, jak je definováno v centrále Commerce pro každou kategorii. Přidáno v Comerce verze 10.0.14. |
| Statická položka nabídky| Pole hodnot| Statické položky nabídky, které přidružují název položky nabídky s odkazem na stránku statického webu. Položky nabídky můžete vytvořit pod dalšími položkami nabídky. Ve výchozím nastavení se statické nabídky zobrazují na kořenové úrovni a budou přidány do hierarchie navigace sítě, pokud existuje. |

Následující obrázek ukazuje příklad obrázku kategorie zobrazeného v navigační nabídce pro web Fabrikam.
![Příklad modulu navigační nabídky s obrázky kategorií](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Přidání modul navigační nabídky do modulu záhlaví

Podrobnosti, jak přidat modul navigační nabídky do modulu záhlaví, viz [Modul záhlaví](author-header-module.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled startovací sady](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Zásady zacházení se soubory cookie](cookie-compliance.md)

[Modul záhlaví](author-header-module.md)
