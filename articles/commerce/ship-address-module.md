---
title: Modul dodací adresy
description: Toto téma popisuje modul dodací adresy a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
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
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234406"
---
# <a name="shipping-address-module"></a><span data-ttu-id="df88b-103">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="df88b-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df88b-104">Toto téma popisuje modul dodací adresy a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="df88b-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="df88b-105">Modul dodací adresy umožňuje zákazníkovi přidat nebo vybrat dodací adresu objednávky během procesu platby.</span><span class="sxs-lookup"><span data-stu-id="df88b-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="df88b-106">Je-li zákazník přihlášen, zobrazí se všechny adresy, které byly pro daného zákazníka dříve uloženy, a zákazník si z nich může vybírat.</span><span class="sxs-lookup"><span data-stu-id="df88b-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="df88b-107">Zákazník může také přidat novou adresu.</span><span class="sxs-lookup"><span data-stu-id="df88b-107">The customer can also add a new address.</span></span> <span data-ttu-id="df88b-108">Modul dodací adresy se použije pro všechny položky v objednávce, které vyžadují dodání.</span><span class="sxs-lookup"><span data-stu-id="df88b-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="df88b-109">Formáty dodacích adres lze definovat v centrále Commerce pro každou zemi nebo oblast a modul dodací adresy pak vynucuje pravidla specifická pro danou zemi/oblast.</span><span class="sxs-lookup"><span data-stu-id="df88b-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="df88b-110">Když zákazníci během procesu platby zadají dodací adresu, mají možnost tuto adresu uložit jako primární adresu.</span><span class="sxs-lookup"><span data-stu-id="df88b-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="df88b-111">Tato možnost je zobrazena pouze v případě, že je zákazník přihlášen.</span><span class="sxs-lookup"><span data-stu-id="df88b-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="df88b-112">Přestože modul dodací adresy neposkytuje ověřování adres, tuto funkci lze implementovat prostřednictvím vlastního nastavení.</span><span class="sxs-lookup"><span data-stu-id="df88b-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="df88b-113">Následující obrázek ukazuje příklad nového modulu dodací adresy na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="df88b-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Příklad modulu dodací adresy na stránce pokladny](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="df88b-115">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="df88b-115">Module properties</span></span>

| <span data-ttu-id="df88b-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="df88b-116">Property name</span></span> | <span data-ttu-id="df88b-117">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="df88b-117">Values</span></span> | <span data-ttu-id="df88b-118">popis</span><span class="sxs-lookup"><span data-stu-id="df88b-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="df88b-119">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="df88b-119">Heading</span></span> | <span data-ttu-id="df88b-120">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="df88b-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="df88b-121">Volitelný nadpis pro modul dodací adresy.</span><span class="sxs-lookup"><span data-stu-id="df88b-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="df88b-122">Zobrazit typ adresy</span><span class="sxs-lookup"><span data-stu-id="df88b-122">Show address type</span></span> | <span data-ttu-id="df88b-123">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="df88b-123">**True** or **False**</span></span> | <span data-ttu-id="df88b-124">Pokud je tato volitelná vlastnost nastavena na **Pravda**, zobrazí se typ adresy, například **Domov** nebo **Podnik**.</span><span class="sxs-lookup"><span data-stu-id="df88b-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="df88b-125">Pokud není zadán žádný typ adresy, bude adresa automaticky uložena jako **Typ**=**Jiný**.</span><span class="sxs-lookup"><span data-stu-id="df88b-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="df88b-126">Povolit automatické návrhy</span><span class="sxs-lookup"><span data-stu-id="df88b-126">Enable auto suggestion</span></span>| <span data-ttu-id="df88b-127">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="df88b-127">**True** or **False**</span></span> | <span data-ttu-id="df88b-128">Pokud je tato volitelná vlastnost nastavena na **True**, budou poskytnuty automatické návrhy adres.</span><span class="sxs-lookup"><span data-stu-id="df88b-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="df88b-129">Tyto návrhy jsou založeny na Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="df88b-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="df88b-130">Informace o tom, jak nastavit integraci Bing Maps pro váš web, najdete v části [Modul pro výběr obchodu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="df88b-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="df88b-131">Tato funkce je k dispozici v aplikaci Commerce od verze 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="df88b-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="df88b-132">Možnosti automatického navrhování</span><span class="sxs-lookup"><span data-stu-id="df88b-132">Auto suggest options</span></span>| <span data-ttu-id="df88b-133">Číslo</span><span class="sxs-lookup"><span data-stu-id="df88b-133">A number</span></span>| <span data-ttu-id="df88b-134">Pokud jsou povoleny automatické návrhy adres, můžete určit další možnosti, například maximální počet návrhů, které by měly být poskytnuty.</span><span class="sxs-lookup"><span data-stu-id="df88b-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="df88b-135">Na stránku pokladny přidejte modul dodací adresy a nastavte požadované vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="df88b-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="df88b-136">Modul dodací adresy lze přidat pouze do modulu pokladny.</span><span class="sxs-lookup"><span data-stu-id="df88b-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="df88b-137">Další informace o konfiguraci modulu dodací adresy a jeho přidání na stránku pokladny naleznete na stránce [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="df88b-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df88b-138">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="df88b-138">Additional resources</span></span>

[<span data-ttu-id="df88b-139">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="df88b-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="df88b-140">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="df88b-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="df88b-141">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="df88b-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="df88b-142">Platební modul</span><span class="sxs-lookup"><span data-stu-id="df88b-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="df88b-143">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="df88b-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="df88b-144">Modul informací o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="df88b-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="df88b-145">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="df88b-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="df88b-146">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="df88b-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="df88b-147">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="df88b-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]