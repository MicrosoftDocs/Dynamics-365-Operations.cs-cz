---
title: Modul ikony košíku
description: Tento článek se zabývá modulem ikony košíku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e35b0ee5341b8b5531ad2c80c868ca4c07ebd315
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280494"
---
# <a name="cart-icon-module"></a>Modul ikony košíku

[!include [banner](includes/banner.md)]

Tento článek se zabývá modulem ikony košíku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Ikona košíku – ikona košíku představuje košík v modulu záhlaví stránky a zobrazuje počet položek v košíku v kterémkoli daném okamžiku. Modul ikony košíku zobrazuje také souhrn nákupního košíku (označovaný také jako mini košík) při přechodu na ikonu košíku. Mini košík poskytuje uživateli souhrn položek v košíku, aniž by bylo nutné přejít na stránku košíku. Kromě toho umožňuje uživateli přímo přejít na stránku pokadny, pokud jsou spokojeni se souhrnem. Tato možnost snižuje počet navigačních stránek a provádí platbu rychleji. 

Následující obrázek znázorňuje příklad modulu ikony vozíku, který zobrazuje mini vozík v záhlaví Fabrikam.

![Příklad modulu ikony košíku.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

- **Zobrazit Mini košík** – je-li vlastnost nastavena na **true**, zobrazí se souhrn nákupního košíku (mini košík) při přechodu myší na ikonu košíku. Tato funkce je podporována pouze pro porty zobrazení na ploše.
- **Povolit anonymní pokladnu** - Když je tato vlastnost nastavena na **True**, mini košík umožňuje uživatelům, kteří nejsou přihlášeni, provést pokladnu pro hosty. Tato vlastnost je k dispozici ve verzi Commerce verze 10.0.21 jako součást balíčku knihovny modulů Commerce.
- **Pořadí položek** - Tato vlastnost určuje pořadí, ve kterém se položky zobrazují v mini košíku. Když je vybrána možnost **Nové položky přidány na začátek seznamu**, nové položky přidané do košíku se zobrazí v horní části seznamu položek mini košíku. Když je vybrána výchozí možnost **Nové položky přidány na konec seznamu**, nové položky přidané do košíku se zobrazí ve spodní části seznamu položek mini košíku. Tato vlastnost je k dispozici ve verzi Commerce verze 10.0.21 jako součást balíčku knihovny modulů Commerce.

> [!IMPORTANT]
> Vlastnosti **Povolit anonymní pokladnu** a **Pořadí položek** jsou k dispozici od vydání Commerce verze 10.0.21. Vyžadují instalaci balíčku knihovny modulů Commerce verze 9.31.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Vlastnosti modulu a sloty v motivu Adventure Works

V motivu Adventure Works obsahuje modul ikony košíku dvě další místa pro minikošík. Tato místa jsou zahrnuta jako rozšíření definice modulu.

- **Propagace prázdného košíku** – Toto místo přijímá modul blokování obsahu. Když je košík prázdný, zobrazí se zadaný modul blokování obsahu. Modul bloku obsahu lze použít pro propagační akce, marketingový obsah a odkazy na stránky kategorií, aby zákazníci mohli pokračovat v cestě nakupováním.
- **Propagační obsah** – Toto místo lze použít k prezentaci propagačních akcí, například „Doprava zdarma u objednávek nad 100 $.“ V bloku propagačního obsahu lze použít moduly obsahu bloku, textového bloku a seznamu obrázků.

Následující obrázek ukazuje příklad modulu ikony košíku v motivu Adventure Works, který zobrazuje propagační obsah na minikošíku.

![Příklad modulu ikony košíku v motivu Adventure Works](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Místa motivu Adventure Works jsou k dispozici od Dynamics 365 Commerce verze 10.0.20.

## <a name="add-a-cart-icon-module-to-a-page"></a>Přidání modulu ikony košíku na stránku

Chcete-li přidat modul ikony nákupního košíku, přečtěte si [Modul záhlaví](author-header-module.md).

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
