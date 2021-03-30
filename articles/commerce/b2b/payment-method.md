---
title: Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B
description: Toto téma popisuje, jak nakonfigurovat platební metodu zákaznického účtu pro weby elektronického obchodování typu business-to-business (B2B).
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
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211194"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nakonfigurovat platební metodu zákaznického účtu pro weby elektronického obchodování typu business-to-business (B2B).

Maloobchodní prodejci mohou přijímat různé typy plateb za výrobky a služby, které prodávají v kanálu elektronického obchodování. Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému v aplikaci Microsoft Dynamics 365 Commerce. Platební metoda zákaznického účtu (nebo „na účet“) musí být podporována na webech B2B elektronického obchodování. 

## <a name="prerequisites"></a>Předpoklady

1. Přidejte platební metodu zákaznického účtu v centrále Commerce.
2. Přiřaďte platební metodu zákaznického účtu ke kanálu elektronického obchodování.
3. Ujistěte se, že je povolena funkce **Povolit na účet** pro zákazníka povoleno v **Retail a Commerce \> Zákazníci \> Všichni zákazníci \> Výchozí nastavení plateb** v centrále Commerce. Ujistěte se také, že jsou parametry **Úvěrový limit** pro zákazníka nastaveny vhodně v **Retail a Commerce \> Zákazníci \> Všichni zákazníci \> Úvěr a inkasa** v centrále Commerce. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Povolte způsob platby zákaznického účtu v konfigurátoru webů Commerce 

Chcete-li povolit způsob platby zákaznického účtu v konfigurátoru webů Commerce, postupujte takto.

1. Přejděte na **Nastavení webu \> Rozšíření**.
1. Nastavte vlastnost **Povolit platby na zákaznický účet** na **Povoleno pro zákazníky B2B**. 
1. Vyberte možnost **Uložit a publikovat**.

> [!NOTE]
> Nové nastavení webu se projeví až po aktualizaci souboru app.settings.json. Další informace viz [Aktualizace knihoven SDK a modulů](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Povolte platební metodu zákaznického účtu na stránce pokladny pro web elektronického obchodování B2B

Chcete-li povolit platební metodu zákaznického účtu na stránce pokladny pro web elektronického obchodování B2B, postupujte takto.

1. V konfigurátoru webů Commerce vyhledejte a upravte stránku pokladny nebo fragment, který obsahuje modul pokladny pro web elektronického obchodování B2B.
1. Ve slotu **Kontejner sekce pokladny** vyberte **Přidat modul** a pak přidejte modul **Platba na účet zákazníka**.
1. Umístěte modul **Platba na účet zákazníka** výběrem třech teček (**...**) a poté vyberte **Posunout nahoru** nebo **Posunout dolů** podle potřeby.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Potvrďte, že byla povolena a zveřejněna platební metoda zákaznického účtu

Chcete-li potvrdit, že byla povolena a zveřejněna platební metoda zákaznického účtu, postupujte takto.

1. Přihlaste se do webu elektronického obchodování.
1. Přidejte produkt do košíku.
1. Přejděte na stránku pokladny. Měli byste vidět novou platební metodu **Zákaznický účet**.

## <a name="additional-resources"></a>Další prostředky

[Nastavení webu elektronického obchodování B2B](set-up-b2b-site.md)

[Vytvářejte hierarchie modelování org pro organizace B2B](org-model.md)

[Spravujte uživatele - obchodní partnery - na webech B2B elektronického obchodování](manage-b2b-users.md)

[Nastavte limity množství produktů pro weby B2B elektronického obchodování](quantity-limits.md)

[SDK a aktualizace knihovny modulů](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]