---
title: Ikona modulu košíku
description: Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9e3850d98e716d1bbea2017f6e8c9d75f19adc9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637994"
---
# <a name="cart-icon-module"></a>Modul ikony košíku

[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Ikona košíku – ikona košíku představuje košík v modulu záhlaví stránky a zobrazuje počet položek v košíku v kterémkoli daném okamžiku. Modul ikony košíku zobrazuje také souhrn nákupního košíku (označovaný také jako mini košík) při přechodu na ikonu košíku. Mini košík poskytuje uživateli souhrn položek v košíku, aniž by bylo nutné přejít na stránku košíku. Kromě toho umožňuje uživateli přímo přejít na stránku pokadny, pokud jsou spokojeni se souhrnem. Tato možnost snižuje počet navigačních stránek a provádí platbu rychleji. 

Následující obrázek znázorňuje příklad modulu ikony vozíku, který zobrazuje mini vozík v záhlaví Fabrikam.

![Příklad modulu ikony košíku.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

- **Zobrazit Mini košík** – je-li nastavena hodnota true, umožňuje tato vlastnost zobrazit souhrn nákupního košíku (mini košík) při přechodu na ikonu košíku. Tato funkce je podporována pouze pro porty zobrazení na ploše.

## <a name="module-properties-in-the-adventure-works-theme"></a>Vlastnosti modulu v motivu Adventure Works

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
