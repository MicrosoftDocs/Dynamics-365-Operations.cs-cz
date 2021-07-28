---
title: Možnost vyzvednout se nezobrazí na stránkách podrobností košíku nebo produktu
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se možnost vyzvednutí v obchodě nezobrazí na stránce košíku nebo na stránkách s podrobnostmi o produktu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3dd4eb576f234e4d75c08b0b5e2fe967500c8c93
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347289"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Možnost „vyzvednout“ se nezobrazí na stránkách podrobností košíku nebo produktu

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se možnost vyzvednutí v obchodě nezobrazí na stránce košíku nebo na stránkách s podrobnostmi o produktu.

## <a name="description"></a>popis

Tlačítko **Vyzvednout** se nezobrazí na stránkách podrobností košíku nebo produktu.

Následující obrázek ukazuje příklad stránky, která obsahuje tlačítko **Vyzvednout**.

![Tlačítko Vyzvednout.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Řešení

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Povolte rozšíření BOPIS v Tvůrci webů Commerce

Chcete-li povolit rozšíření „koupit online, vyzvednout v obchodě“ (BOPIS) v nástroji pro tvorbu webů Commerce, postupujte takto.

1. Vyberte web.
1. Vyberte **Nastavení webu** a pak vyberte **Rozšíření**.
1. Ujistěte se, že není vybrána možnost **Zakázat BOPIS**.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Konfigurace způsobů doručení v centrále Commerce

Konfiguraci režimu doručení v centrále Commerce provedete následovně.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Způsoby dodání**.
1. Ujistěte se, že byl vytvoření režim doručení **Vyzvednutí zákazníkem** a k němu jsou přiřazeny produkty a adresy.
1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry**.
1. V levém navigačním podokně vyberte položku **Objednávky zákazníka**.
1. Ujistěte se, že je **Způsob doručení vyzvednutím** správně nakonfigurován.

### <a name="configure-customer-orders-payments"></a>Konfigurace plateb objednávek zákazníků

Chcete-li nakonfigurovat platby objednávek zákazníků v centrále Commerce, postupujte následovně.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry**.
1. V levém navigačním podokně vyberte položku **Objednávky zákazníka**.
1. Na kartě s náhledem **Platby** zkontrolujte se, že pole **Platební podmínky** a **Způsob platby** jsou správně nastavena.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace BOPIS](../cpe-bopis.md)

[Povolení více způsobů vyzvednutí/doručení objednávek zákazníků](../multiple-pickup-modes.md)

[Omnikanálové platby objednávek Commerce](../dev-itpro/commerce-payments.md)

[Modul volby obchodu](../store-selector.md)
