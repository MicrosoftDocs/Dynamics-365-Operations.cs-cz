---
title: Modul platby
description: Toto téma popisuje modul platby a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661193"
---
# <a name="payment-module"></a><span data-ttu-id="def5e-103">Modul platby</span><span class="sxs-lookup"><span data-stu-id="def5e-103">Payment module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="def5e-104">Toto téma popisuje modul platby a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="def5e-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="def5e-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="def5e-105">Overview</span></span>

<span data-ttu-id="def5e-106">Platba – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí kreditní nebo debetní karty.</span><span class="sxs-lookup"><span data-stu-id="def5e-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="def5e-107">Integraci platby pro tento modul zajišťuje konektor plateb Dynamics 365 pro Adyen.</span><span class="sxs-lookup"><span data-stu-id="def5e-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="def5e-108">Další informace o nastavení a konfiguraci konektoru plateb pro online obchody naleznete v tématu [Konektor plateb Dynamics 365 pro Ayden](dev-itpro/adyen-connector.md)</span><span class="sxs-lookup"><span data-stu-id="def5e-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="def5e-109">Platební modul je hostitelem platebních informací, které jsou zobrazovány prostřednictvím služby Adyen, v rámci vloženého rámce HTML (iframe).</span><span class="sxs-lookup"><span data-stu-id="def5e-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="def5e-110">Platební modul spolupracuje s Commerce Scale Unit a získává informace o platbě Adyen.</span><span class="sxs-lookup"><span data-stu-id="def5e-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="def5e-111">V rámci interakce jednotky Commerce Scale Unit platební modul umožňuje, aby se informace o fakturační adrese zobrazovaly v prvku iframe nebo jako samostatný modul.</span><span class="sxs-lookup"><span data-stu-id="def5e-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="def5e-112">V tématu Fabrikam je fakturační adresa zobrazena v samostatném modulu.</span><span class="sxs-lookup"><span data-stu-id="def5e-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="def5e-113">Tento přístup umožňuje větší flexibilitu formátování, protože adresové řádky lze vykreslit tak, aby se podobaly řádkům dodací adresy.</span><span class="sxs-lookup"><span data-stu-id="def5e-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="def5e-114">Platební modul také umožňuje přihlášeným zákazníkům ukládat své platební informace.</span><span class="sxs-lookup"><span data-stu-id="def5e-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="def5e-115">Platební informace a fakturační adresa jsou ukládány a spravovány prostřednictvím platebního konektoru Adyen.</span><span class="sxs-lookup"><span data-stu-id="def5e-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="def5e-116">Platební modul pokrývá veškeré poplatky za objednávky, které již nejsou pokryty věrnostními body ani dárkovou kartou.</span><span class="sxs-lookup"><span data-stu-id="def5e-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="def5e-117">Pokud je celková částka objednávky plně pokryta věrnostními body nebo kredity dárkové karty, platební modul bude skrytý a zákazník bude moci objednávku zadat bez ní.</span><span class="sxs-lookup"><span data-stu-id="def5e-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="def5e-118">Konektor platby Adyen také podporuje silné ověření klienta (SCA).</span><span class="sxs-lookup"><span data-stu-id="def5e-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="def5e-119">Část směrnice Evropské unie (EU) o platebních službách 2.0 (PSD2.0) vyžaduje, aby nakupující byli autentizováni mimo online obchod, když používají elektronickou platební metodu.</span><span class="sxs-lookup"><span data-stu-id="def5e-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="def5e-120">Během procesu platby jsou zákazníci přesměrováni na své bankovní stránky.</span><span class="sxs-lookup"><span data-stu-id="def5e-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="def5e-121">Poté se po ověření přesměrují zpět do toku plateb Commerce.</span><span class="sxs-lookup"><span data-stu-id="def5e-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="def5e-122">Během tohoto přesměrování budou uloženy informace, které zákazník zadal v pokladně (například dodací adresa, možnosti doručení, informace o dárkových kartách a informace o věrnostním programu).</span><span class="sxs-lookup"><span data-stu-id="def5e-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="def5e-123">Před zapnutím této funkce musí být platební konektor nakonfigurován pro SCA v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="def5e-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="def5e-124">Další informace naleznete v článku [Silná autentizace zákazníků pomocí Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="def5e-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="def5e-125">Následující obrázek ukazuje příklad modulů dárkové karty, věrnostních bodů a plateb na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="def5e-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Příklad modulů dárkové karty, věrnostních bodů a plateb na stránce pokladny](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="def5e-127">Vlastnosti modulu platby</span><span class="sxs-lookup"><span data-stu-id="def5e-127">Payment module properties</span></span>

| <span data-ttu-id="def5e-128">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="def5e-128">Property name</span></span> | <span data-ttu-id="def5e-129">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="def5e-129">Values</span></span> | <span data-ttu-id="def5e-130">popis</span><span class="sxs-lookup"><span data-stu-id="def5e-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="def5e-131">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="def5e-131">Heading</span></span> | <span data-ttu-id="def5e-132">Text nadpisu</span><span class="sxs-lookup"><span data-stu-id="def5e-132">Heading text</span></span> | <span data-ttu-id="def5e-133">Volitelný nadpis pro modul platby.</span><span class="sxs-lookup"><span data-stu-id="def5e-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="def5e-134">Výška prvku iframe.</span><span class="sxs-lookup"><span data-stu-id="def5e-134">Height of the iframe</span></span> | <span data-ttu-id="def5e-135">Pixely</span><span class="sxs-lookup"><span data-stu-id="def5e-135">Pixels</span></span> | <span data-ttu-id="def5e-136">Výška prvku iframe v pixelech.</span><span class="sxs-lookup"><span data-stu-id="def5e-136">The iframe height, in pixels.</span></span> <span data-ttu-id="def5e-137">Velikost lze upravit podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="def5e-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="def5e-138">Zobrazit fakturační adresu</span><span class="sxs-lookup"><span data-stu-id="def5e-138">Show billing address</span></span> | <span data-ttu-id="def5e-139">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="def5e-139">**True** or **False**</span></span> | <span data-ttu-id="def5e-140">Pokud je tato vlastnost nastavena na **Pravda**, fakturační adresu doručí Adyen uvnitř prvku iframe platebního modulu.</span><span class="sxs-lookup"><span data-stu-id="def5e-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="def5e-141">Pokud je nastaveno na **Nepravda**, fakturační adresu nebude Adyen zobrazovat a uživatel Commerce bude muset nakonfigurovat modul tak, aby zobrazoval fakturační adresu na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="def5e-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="def5e-142">Přepsání stylu platby</span><span class="sxs-lookup"><span data-stu-id="def5e-142">Payment style override</span></span> | <span data-ttu-id="def5e-143">Kód kaskádových stylů (CSS)</span><span class="sxs-lookup"><span data-stu-id="def5e-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="def5e-144">Protože je platební modul hostován v prvku iframe, existuje omezená schopnost stylování.</span><span class="sxs-lookup"><span data-stu-id="def5e-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="def5e-145">Pomocí této vlastnosti můžete dosáhnout určitého stylu.</span><span class="sxs-lookup"><span data-stu-id="def5e-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="def5e-146">Chcete-li přepsat styly webů, musíte vložit CSS kód jako hodnotu této vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="def5e-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="def5e-147">Přepsání a styly CSS tvůrce stránek se na tento modul nevztahují.</span><span class="sxs-lookup"><span data-stu-id="def5e-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="def5e-148">Fakturační adresa</span><span class="sxs-lookup"><span data-stu-id="def5e-148">Billing address</span></span>

<span data-ttu-id="def5e-149">Platební modul umožňuje zákazníkům poskytnout fakturační adresu pro své platební informace.</span><span class="sxs-lookup"><span data-stu-id="def5e-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="def5e-150">Rovněž jim umožňuje použít jako fakturační adresu svou dodací adresu, aby usnadnili a urychlili tok plateb.</span><span class="sxs-lookup"><span data-stu-id="def5e-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="def5e-151">Pokud je **Zobrazit fakturační adresu** vlastnost nastavena na **Nepravda**, platební modul by měl být nakonfigurován na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="def5e-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="def5e-152">Na stránku pokladny přidejte modul platby a nastavte požadované vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="def5e-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="def5e-153">Modul platby lze přidat pouze do modulu pokladny.</span><span class="sxs-lookup"><span data-stu-id="def5e-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="def5e-154">Další informace o tom, jak nakonfigurovat modul platby pro stránku pokladny, naleznete v tématu [Modul platby](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="def5e-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="def5e-155">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="def5e-155">Additional resources</span></span>

[<span data-ttu-id="def5e-156">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="def5e-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="def5e-157">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="def5e-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="def5e-158">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="def5e-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="def5e-159">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="def5e-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="def5e-160">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="def5e-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="def5e-161">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="def5e-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="def5e-162">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="def5e-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="def5e-163">Platební konektor Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="def5e-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="def5e-164">Silné ověření klienta pomocí konektoru Adyen</span><span class="sxs-lookup"><span data-stu-id="def5e-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
