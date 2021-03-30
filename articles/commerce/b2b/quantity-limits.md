---
title: Nastavte limity množství produktů pro weby B2B elektronického obchodování
description: Toto téma popisuje, jak nastavit limity množství produktu pro weby elektronického obchodování typu business-to-business (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211170"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Nastavte limity množství produktů pro weby B2B elektronického obchodování

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nastavit limity množství produktu pro weby elektronického obchodování typu business-to-business (B2B).

Většina produktů má měrnou jednotku, která definuje jejich seskupení. Seskupení ovlivňuje způsob prodeje produktů. Některé produkty mohou mít další seskupení pro množství. Toto seskupení určuje, zda lze produkty prodávat jako jednotlivé jednotky nebo násobky a zda existuje minimální nebo maximální limit množství objednávky, který je třeba dodržet.

Funkce omezení množství zajišťuje, že minimální, maximální, vícenásobné a standardní množství je nakonfigurováno v Microsoft Dynamics 365 Commerce (ve výchozím nastavení objednávky nebo nastavení webu konfigurátoru webu Commerce) se použijí na objednávky zákazníků, které jsou umístěny na webu elektronického obchodování. Omezení množství produktů nejsou aktuálně podporována pro pokladní místa (POS) a kontaktní střediska.

Celá řada maloobchodních prodejců poskytuje možnost objednávek odběratele (neboli speciálních objednávek), aby splnili různé požadavky týkající se produktu a plnění. Zde jsou některé typické scénáře:

- Zákazník chce, aby se produkty konkrétních variant prodávaly ve velkém množství.
- Zákazník chce vyzvednout výrobky ve skladu nebo z místa, které se liší od skladu nebo místa, kde zákazník tyto produkty zakoupil. Standardy balení pro obchody se však liší od standardů balení pro distribuci online prodeje.
- Zákazník chce koupit limitovaný produkt, který má maximální limit množství pro položky, které lze zakoupit.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>V centrále Commerce zapněte funkci výchozího nastavení objednávky

Než budete moci nastavit limity množství produktu, musí být v centrále Commerce zapnuta funkce výchozího nastavení objednávky.

Pomocí následujících kroků zapněte funkci výchozího nastavení objednávky.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Najděte a vyberte funkci **Podpora nastavení webu a výchozího nastavení v objednávce zákazníka**.
1. V dolní části pravého podokna vyberte **Povolit nyní**. 

## <a name="define-quantity-settings"></a>Definujte nastavení množství 

Výchozí množství můžete definovat na stránce **Výchozí nastavení objednávky**.

Chcete-li definovat nastavení množství, postupujte takto. 

1. Přejděte do nabídky **Retail a Commerce \> Produkty a kategorie \> Uvolněné produkty podle kategorie**.
1. Vyberte uvolněný produkt.
1. V podokně akcí, na kartě **Spravovat sklad**, ve skupině **Nastavení objednávky**, vyberte **Výchozí nastavení objednávky**. 
1. Na stránce **Výchozí nastavení objednávky**, na pevné záložce **Prodejní objednávka**, v sekci **Množství prodeje** nastavte množství prodeje produktu:

    - **Násobek** - Množství, ve kterém lze produkt zakoupit v násobcích.
    - **Minimální množství pro objednání** - Minimální počet produktů, které je třeba zakoupit.
    - **Maximální množství pro objednání** - Maximální počet produktů, které je možné zakoupit.
    - **Standardní objednané množství** - Výchozí množství, které se automaticky zadá při výběru produktu.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Zapněte funkci omezení počtu objednávek B2B v konfigurátoru webů Commerce

Chcete-li zapnout funkci omezení počtu objednávek B2B v konfigurátoru webů Commerce, postupujte takto.

1. Přejděte na **Nastavení webu \> Rozšíření**
1. V **Povolit limity množství objednávky** vyberte **Povoleno pro zákazníky B2B** v rozevírací nabídce. 

> [!NOTE] 
> Aktualizované nastavení konfigurátoru webu se projeví až po aktualizaci souboru app.settings.json. Další informace viz [Aktualizace knihoven SDK a modulů](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Další prostředky

[Nastavení webu elektronického obchodování B2B](set-up-b2b-site.md)

[Vytvářejte hierarchie modelování org pro organizace B2B](org-model.md)

[Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B](manage-b2b-users.md)

[Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]