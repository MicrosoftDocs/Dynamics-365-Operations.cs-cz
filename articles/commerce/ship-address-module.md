---
title: Modul dodací adresy
description: Toto téma popisuje modul dodací adresy a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410944"
---
# <a name="shipping-address-module"></a>Modul dodací adresy

[!include [banner](includes/banner.md)]

Toto téma popisuje modul dodací adresy a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul dodací adresy umožňuje zákazníkovi přidat nebo vybrat dodací adresu objednávky během procesu platby. Je-li zákazník přihlášen, zobrazí se všechny adresy, které byly pro daného zákazníka dříve uloženy, a zákazník si z nich může vybírat. Zákazník může také přidat novou adresu. Modul dodací adresy se použije pro všechny položky v objednávce, které vyžadují dodání.

Formáty dodacích adres lze definovat v centrále Commerce pro každou zemi nebo oblast a modul dodací adresy pak vynucuje pravidla specifická pro danou zemi/oblast.

Když zákazníci během procesu platby zadají dodací adresu, mají možnost tuto adresu uložit jako primární adresu. Tato možnost je zobrazena pouze v případě, že je zákazník přihlášen.

Přestože modul dodací adresy neposkytuje ověřování adres, tuto funkci lze implementovat prostřednictvím vlastního nastavení.

Následující obrázek ukazuje příklad nového modulu dodací adresy na stránce pokladny.

![Příklad modulu dodací adresy na stránce pokladny](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Volitelný nadpis pro modul dodací adresy. |
| Zobrazit typ adresy | **Pravda** nebo **nepravda** | Pokud je tato volitelná vlastnost nastavena na **Pravda**, zobrazí se typ adresy, například **Domov** nebo **Podnik**. Pokud není zadán žádný typ adresy, bude adresa automaticky uložena jako **Typ**=**Jiný**. |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Na stránku pokladny přidejte modul dodací adresy a nastavte požadované vlastnosti.

Modul dodací adresy lze přidat pouze do modulu pokladny. Další informace o konfiguraci modulu dodací adresy a jeho přidání na stránku pokladny naleznete na stránce [Modul pokladny](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul informací o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)
