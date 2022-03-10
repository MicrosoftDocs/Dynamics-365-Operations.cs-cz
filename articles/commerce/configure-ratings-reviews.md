---
title: Konfigurace hodnocení a recenzí
description: V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3f9ff4b0654ec5fa7548ac62e16ae64f44383e7
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968095"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurace hodnocení a recenzí

[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.

Hodnocení a recenze na webech elektronických obchodů pomáhají zákazníkům lépe se seznámit s produkty před tím, než se je rozhodnou zakoupit, a to zobrazením, co si ostatní zákazníci o těchto produktech myslí. U webů elektronického obchodování jsou hodnocení a recenze také mechanismem pro shromažďování názorů o produktech od zákazníků. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurace webu pro zobrazení hodnocení a recenzí

Hodnoty konfigurace hodnocení a recenzí, jako je například ID klienta, délka textu recenze a délka názvu recenze, jsou konfigurovány na úrovni webu. 

Chcete-li nakonfigurovat web tak, aby zobrazoval hodnocení a recenze, postupujte podle následujících kroků. 

1. Přejděte do umístění **Domů \> Weby**.
1. Vyberte název webu. 
1. Přejděte na **Nastavení webu \> Rozšíření**. 
1. Do pole **Maximální délka textu recenze** zadejte maximální počet znaků textu recenze (například **1000**). 
1. Do pole **Maximální délka názvu recenze** zadejte maximální počet znaků názvu recenze (například **55**). 
1. Vyberte možnost **Uložit a publikovat**. 

Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.

![Konfigurace webu pro zobrazení hodnocení a recenzí.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu

Hodnocení produktu je uvedeno pod názvem produktu nahoře na stránce s podrobnostmi o produktu. Hodnocení produktu lze nakonfigurovat tak, aby bylo propojeno se sekcí **Recenze** na stejné stránce s podrobnostmi o produktu. 

Chcete-li propojit hodnocení produktu se sekcí **Recenze** na stránce s podrobnostmi o produktu, postupujte podle následujících kroků.

1. Otevřete šablonu stránky s podrobnostmi o produktu. 
1. Přejít na **Nastavení modulu kontejneru buy boxu**.
1. V části **Buy box** vyberte **Hodnocení produktu** a poté zaškrtněte políčko **Propojit kliknutí s úplným modulem recenzí**.

Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.

![Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurace odkazu na stránku ochrany osobních údajů a zásad

Chcete-li konfigurovat odkaz na stránku ochrany osobních údajů a zásad, postupujte následovně.

1. Přejděte do umístění **Domů \> Weby**.
1. Vyberte název webu. 
1. Přejděte na **Nastavení webu \> Rozšíření**.
1. Na kartě **Trasy** v části **Ochrana osobních údajů a zásady RNR** vyberte možnost **Přidat odkaz**. Je-li již zadán odkaz a chcete jej nahradit, vyberte odkaz. 
1. V dialogovém okně **Přidat odkaz** vyberte odkaz na stránku ochrany osobních údajů a zásad a poté klepněte na tlačítko **OK**. 
1. Vyberte možnost **Uložit a publikovat**. 

Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.

![Konfigurace odkazu na stránku ochrany osobních údajů a zásad.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Konfigurovat moduly hodnocení a recenzí na stránkách s podrobnostmi o produktu

Informace týkající se konfigurace hodnocení a recenzí na stránkách s podrobnostmi o produktu naleznete v tématu [Moduly hodnocení a recenzí](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Další zdroje

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Synchronizace hodnocení produktů v Dynamics 365 Retail](sync-product-ratings.md)

[Povolit ruční publikování hodnocení a recenzí moderátorem](manual-publish-rating-reviews.md)

[Import a export hodnocení a recenzí](import-export-reviews.md)

[Konfigurace ověřování mezi službami](service-to-service-auth.md)

[Nejčastější dotazy k hodnocení a recenzím](ratings-reviews-faq.md)

[Moduly hodnocení a recenzí](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
