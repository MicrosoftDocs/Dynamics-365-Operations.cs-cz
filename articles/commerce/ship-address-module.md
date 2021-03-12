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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985629"
---
# <a name="shipping-address-module"></a><span data-ttu-id="27d21-103">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="27d21-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27d21-104">Toto téma popisuje modul dodací adresy a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27d21-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27d21-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="27d21-105">Overview</span></span>

<span data-ttu-id="27d21-106">Modul dodací adresy umožňuje zákazníkovi přidat nebo vybrat dodací adresu objednávky během procesu platby.</span><span class="sxs-lookup"><span data-stu-id="27d21-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="27d21-107">Je-li zákazník přihlášen, zobrazí se všechny adresy, které byly pro daného zákazníka dříve uloženy, a zákazník si z nich může vybírat.</span><span class="sxs-lookup"><span data-stu-id="27d21-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="27d21-108">Zákazník může také přidat novou adresu.</span><span class="sxs-lookup"><span data-stu-id="27d21-108">The customer can also add a new address.</span></span> <span data-ttu-id="27d21-109">Modul dodací adresy se použije pro všechny položky v objednávce, které vyžadují dodání.</span><span class="sxs-lookup"><span data-stu-id="27d21-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="27d21-110">Formáty dodacích adres lze definovat v centrále Commerce pro každou zemi nebo oblast a modul dodací adresy pak vynucuje pravidla specifická pro danou zemi/oblast.</span><span class="sxs-lookup"><span data-stu-id="27d21-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="27d21-111">Když zákazníci během procesu platby zadají dodací adresu, mají možnost tuto adresu uložit jako primární adresu.</span><span class="sxs-lookup"><span data-stu-id="27d21-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="27d21-112">Tato možnost je zobrazena pouze v případě, že je zákazník přihlášen.</span><span class="sxs-lookup"><span data-stu-id="27d21-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="27d21-113">Přestože modul dodací adresy neposkytuje ověřování adres, tuto funkci lze implementovat prostřednictvím vlastního nastavení.</span><span class="sxs-lookup"><span data-stu-id="27d21-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="27d21-114">Následující obrázek ukazuje příklad nového modulu dodací adresy na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="27d21-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Příklad modulu dodací adresy na stránce pokladny](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="27d21-116">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="27d21-116">Module properties</span></span>

| <span data-ttu-id="27d21-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="27d21-117">Property name</span></span> | <span data-ttu-id="27d21-118">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="27d21-118">Values</span></span> | <span data-ttu-id="27d21-119">popis</span><span class="sxs-lookup"><span data-stu-id="27d21-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="27d21-120">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="27d21-120">Heading</span></span> | <span data-ttu-id="27d21-121">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="27d21-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="27d21-122">Volitelný nadpis pro modul dodací adresy.</span><span class="sxs-lookup"><span data-stu-id="27d21-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="27d21-123">Zobrazit typ adresy</span><span class="sxs-lookup"><span data-stu-id="27d21-123">Show address type</span></span> | <span data-ttu-id="27d21-124">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="27d21-124">**True** or **False**</span></span> | <span data-ttu-id="27d21-125">Pokud je tato volitelná vlastnost nastavena na **Pravda**, zobrazí se typ adresy, například **Domov** nebo **Podnik**.</span><span class="sxs-lookup"><span data-stu-id="27d21-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="27d21-126">Pokud není zadán žádný typ adresy, bude adresa automaticky uložena jako **Typ**=**Jiný**.</span><span class="sxs-lookup"><span data-stu-id="27d21-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="27d21-127">Na stránku pokladny přidejte modul dodací adresy a nastavte požadované vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="27d21-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="27d21-128">Modul dodací adresy lze přidat pouze do modulu pokladny.</span><span class="sxs-lookup"><span data-stu-id="27d21-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="27d21-129">Další informace o konfiguraci modulu dodací adresy a jeho přidání na stránku pokladny naleznete na stránce [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="27d21-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27d21-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="27d21-130">Additional resources</span></span>

[<span data-ttu-id="27d21-131">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="27d21-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="27d21-132">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="27d21-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="27d21-133">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="27d21-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="27d21-134">Platební modul</span><span class="sxs-lookup"><span data-stu-id="27d21-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="27d21-135">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="27d21-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="27d21-136">Modul informací o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="27d21-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="27d21-137">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="27d21-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="27d21-138">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="27d21-138">Gift card module</span></span>](add-giftcard.md)
