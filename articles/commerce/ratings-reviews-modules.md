---
title: Moduly hodnocení a recenzí
description: Toto téma popisuje moduly hodnocení a recenzí použité na stránkách s podrobnostmi o produktu v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: b17e986c2e30134c334cd547a85a1dd682172a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979796"
---
# <a name="ratings-and-reviews-modules"></a>Moduly hodnocení a recenzí

[!include [banner](includes/banner.md)]

Toto téma popisuje moduly hodnocení a recenzí použité na stránkách s podrobnostmi o produktu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Hodnocení a recenze na webech elektronických obchodů pomáhají zákazníkům lépe se seznámit s produkty před tím, než se je rozhodnou zakoupit, a představují také mechanismus ke shromažďování zpětné vazby uživatelů ohledně produktů. 

Hodnocení se zobrazují na stránkách seznamů produktů, na stránkách se seznamem kategorií, na stránkách výsledků hledání a na dalších stránkách webu. 

Histogramy hodnocení a recenze produktů jsou zobrazeny na stránkách s podrobnostmi o produktu. Tlačítko **Napsat recenzi** umožňuje zákazníkům předkládat hodnocení a recenze produktu. Tyto funkce jsou řízeny moduly hodnocení a recenzí.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Moduly hodnocení a recenzí na stránkách s podrobnostmi o produktu 

Ve třech modulech se zobrazuje souhrn hodnocení a recenzí na stránce s podrobnostmi o produktu:
- Modul pro napsání recenze
- Modul seznamu recenzí produktu
- Modul histogramu hodnocení
 
Následující obrázek ukazuje, jak vypadají moduly hodnocení a recenzí na stránce s podrobnostmi o produktu.

![Hodnocení a recenzí na stránce s podrobnostmi o produktu](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Informace, jak optimalizovat šablony a rozložení stránky s podrobnostmi o produktu tak, aby bylo možné sdílet konfigurace pro moduly hodnocení a recenzí mezi několika stránkami s podrobnostmi o produktu na vašem webu elektronického obchodu, naleznete v tématu [Přehled šablon a rozložení](templates-layouts-overview.md).

Následující obrázek ukazuje, jak dialogové okno **Přidat modul** zobrazuje moduly hodnocení a recenzí v aplikaci řešení Dynamics 365 Commerce.
![Dialogové okno Přidat modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Modul pro napsání recenze

Modul pro napsání recenze obsahuje tlačítko **Napsat recenzi**, které uživateli umožňuje přihlásit se, přiřadit hodnocení a napsat recenzi produktu. Tento modul dále umožňuje uživatelům upravit dříve odeslané hodnocení nebo recenzi. Tento modul se obvykle zobrazí nad moduly histogramu hodnocení a seznamu recenzí produktu na stránce s podrobnostmi o produktu.
Následující ilustrace znázorňuje dialogové okno **Napsat recenzi**, které se zobrazí, když zákazník vybere možnost **Napsat recenzi**. Zákazník může toto dialogové okno použít k odeslání hodnocení a recenze.
![Dialogové okno Napsat recenzi](media/rnr-eCommerce-write-review-module.png) V následující tabulce je uvedena vlastnost modulu pro napsání recenze, kterou je nutné nakonfigurovat v nástroji pro tvorbu obsahu.
| Název vlastnosti | Hodnota        | Popis vlastnosti                 |
|---------------|--------------|--------------------------------------|
| Název          | Napsat recenzi | Název modulu pro napsání recenze. |

### <a name="ratings-histogram-module"></a>Modul histogramu hodnocení

V modulu histogramu hodnocení se zobrazuje histogram hodnocení. Tento modul se obvykle nachází mezi modulem pro napsání recenze a modulem seznamu recenzí produktu na stránce s podrobnostmi o produktu.
Modul histogramu hodnocení nevyžaduje žádnou konfiguraci. Stačí pouze přidat modul do šablony stránky s podrobnostmi o produktu. Následující ilustrace ukazuje, jak vypadá šablona stránky s podrobnostmi o produktu v řešení Dynamics 365 Commerce, když jsou moduly hodnocení a recenzí nakonfigurovány pro zobrazení na stránce s podrobnostmi o produktu.
![Šablona stránky s podrobnostmi o produktu při konfiguraci hodnocení a recenzí na stránkách s podrobnostmi o produktu](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Modul seznamu recenzí produktu

V modulu seznam recenzí produktu se zobrazuje seznam recenzí produktů spolu s možnostmi řazení, filtrování a stránkování. Tento modul se obvykle zobrazuje za modulem histogramu hodnocení na stránce s podrobnostmi o produktu.
V následující tabulce jsou uvedeny vlastnosti modulu seznamu recenzí produktu, které je nutné nakonfigurovat v nástroji pro tvorbu obsahu.

| Název vlastnosti              | Hodnota | Popis vlastnosti |
|----------------------------|-------| ---------------------|
| Recenze zobrazené na každé stránce | 10    | Počet recenzí, které mají být zobrazeny v čase na stránce s podrobnostmi o produktu. Součástí jsou tlačítka **Další** a **Předchozí**, aby se uživatelé mohli pohybovat na stránkách recenzí. |

#### <a name="ratings-histogram--summary-view"></a>Histogram hodnocení – souhrnné zobrazení

Modul seznamu recenzí produktu obsahuje pozici, do níž lze přidat modul histogramu hodnocení. Následující obrázek znázorňuje, jak lze přidat modul histogramu hodnocení do modulu seznamu recenzí produktu v řešení Dynamics 365 Commerce.

![Přidání modulu histogramu hodnocení do modulu seznamu recenzí produktu](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
