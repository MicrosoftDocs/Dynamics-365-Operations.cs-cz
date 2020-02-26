---
title: Konfigurace hodnocení a recenzí
description: V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002190"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurace hodnocení a recenzí


[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Hodnocení a recenze na webech elektronických obchodů pomáhají zákazníkům lépe se seznámit s produkty před tím, než se je rozhodnou zakoupit, a to zobrazením, co si ostatní zákazníci o těchto produktech myslí. U webů elektronického obchodování jsou hodnocení a recenze také mechanismem pro shromažďování názorů o produktech od zákazníků. 

Hodnocení se zobrazují na stránkách seznamů produktů, na stránkách se seznamem kategorií, na stránkách výsledků hledání a na dalších stránkách webu. Histogramy hodnocení a recenze produktů jsou zobrazeny na stránkách s podrobnostmi o produktu. Tlačítko **Napsat recenzi** umožňuje zákazníkům předkládat hodnocení a recenze produktu.

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

![Dialogové okno Napsat recenzi](media/rnr-eCommerce-write-review-module.png)

V následující tabulce je uvedena vlastnost modulu pro napsání recenze, kterou je nutné nakonfigurovat v nástroji pro tvorbu obsahu.

| Název vlastnosti | Hodnota        | Popis vlastnosti                 |
|---------------|--------------|--------------------------------------|
| Název          | Napsat recenzi | Název modulu pro napsání recenze. |

### <a name="ratings-histogram-module"></a>Modul histogramu hodnocení

V modulu histogramu hodnocení se zobrazuje histogram hodnocení. Tento modul se obvykle nachází mezi modulem pro napsání recenze a modulem seznamu recenzí produktu na stránce s podrobnostmi o produktu.

Modul histogramu hodnocení nevyžaduje žádnou konfiguraci. Stačí pouze přidat modul do šablony stránky s podrobnostmi o produktu. 

Následující ilustrace ukazuje, jak vypadá šablona stránky s podrobnostmi o produktu v řešení Dynamics 365 Commerce, když jsou moduly hodnocení a recenzí nakonfigurovány pro zobrazení na stránce s podrobnostmi o produktu.

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

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurace webu pro zobrazení hodnocení a recenzí

Hodnoty konfigurace hodnocení a recenzí, jako je například ID klienta, délka textu recenze a délka názvu recenze, jsou konfigurovány na úrovni webu. 

Chcete-li nakonfigurovat web tak, aby zobrazoval hodnocení a recenze, postupujte podle následujících kroků. 

1. Přejděte do umístění **Domů \> Weby**.
1. Vyberte název webu. 
1. Přejděte na **Správa webu \> Rozšiřitelnost**. 
1. Do pole **Maximální délka textu recenze** zadejte maximální počet znaků textu recenze (například **1000**). 
1. Do pole **Maximální délka názvu recenze** zadejte maximální počet znaků názvu recenze (například **55**). 
1. Vyberte možnost **Uložit a publikovat**. 

Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.

![Konfigurace webu pro zobrazení hodnocení a recenzí](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu

Hodnocení produktu je uvedeno pod názvem produktu nahoře na stránce s podrobnostmi o produktu. Hodnocení produktu lze nakonfigurovat tak, aby bylo propojeno se sekcí **Recenze** na stejné stránce s podrobnostmi o produktu. 

Chcete-li propojit hodnocení produktu se sekcí **Recenze** na stránce s podrobnostmi o produktu, postupujte podle následujících kroků.

1. Otevřete šablonu stránky s podrobnostmi o produktu. 
1. Přejít na **Nastavení modulu kontejneru buy boxu**.
1. V části **Buy box** vyberte **Hodnocení produktu** a poté zaškrtněte políčko **Propojit kliknutí s úplným modulem recenzí**.

Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.

![Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurace odkazu na stránku ochrany osobních údajů a zásad

Chcete-li konfigurovat odkaz na stránku ochrany osobních údajů a zásad, postupujte následovně.

1. Přejděte do umístění **Domů \> Weby**.
1. Vyberte název webu. 
1. Přejděte na **Správa webu \> Rozšiřitelnost**.
1. Na kartě **Trasy** v části **Ochrana osobních údajů a zásady RNR** vyberte možnost **Přidat odkaz**. Je-li již zadán odkaz a chcete jej nahradit, vyberte odkaz. 
1. V dialogovém okně **Přidat odkaz** vyberte odkaz na stránku ochrany osobních údajů a zásad a poté klepněte na tlačítko **OK**. 
1. Vyberte možnost **Uložit a publikovat**. 

Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.

![Konfigurace odkazu na stránku ochrany osobních údajů a zásad](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Další zdroje

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Synchronizace hodnocení produktů v Dynamics 365 Retail](sync-product-ratings.md)
