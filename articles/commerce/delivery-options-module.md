---
title: Modul možností doručení
description: Toto téma popisuje moduly možností dodání a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e55ce327e2c8ab714eb5e2fa14b3830b9171688
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020672"
---
# <a name="delivery-options-module"></a><span data-ttu-id="aa272-103">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="aa272-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="aa272-104">Toto téma popisuje moduly možností dodání a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa272-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aa272-105">Moduly možností doručení umožňují zákazníkům vybrat způsob doručení, jako je například dopravce nebo vyzvednutí pro jejich online objednávku.</span><span class="sxs-lookup"><span data-stu-id="aa272-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="aa272-106">Pro určení způsobu doručení je vyžadována dodací adresa.</span><span class="sxs-lookup"><span data-stu-id="aa272-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="aa272-107">Pokud se změní dodací adresa, je nutné znovu načíst možnosti dodání.</span><span class="sxs-lookup"><span data-stu-id="aa272-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="aa272-108">Pokud objednávka obsahuje pouze položky, které budou vydány v obchodě, bude tento modul automaticky skrytý.</span><span class="sxs-lookup"><span data-stu-id="aa272-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="aa272-109">Informace o tom, jak konfigurovat režimy doručení, naleznete v části [Nastavení online kanálu](channel-setup-online.md) a [Nastavení způsobů dodání](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="aa272-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="aa272-110">Každý režim dodání může mít související poplatek.</span><span class="sxs-lookup"><span data-stu-id="aa272-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="aa272-111">Informace o tom, jak nakonfigurovat náklady pro online obchod, naleznete v tématu [Omnikanál – pokročilé automatické náklady](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="aa272-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="aa272-112">V Commerce verze 10.0.13 byl aktualizován modul voleb doručení, aby podporoval **Náklady záhlaví bez proměrného** a **Doprava jako náklad řádku** funkce.</span><span class="sxs-lookup"><span data-stu-id="aa272-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="aa272-113">Pokud je prorace vypnutá, očekává se, že pracovní postup elektronického obchodování neumožňuje smíšený způsob doručení pro položky v košíku (to znamená, že některé položky jsou vybrány pro odeslání, jiné jsou vybrány pro vyzvednutí).</span><span class="sxs-lookup"><span data-stu-id="aa272-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="aa272-114">Funkce **Náklady záhlaví bez proměrného** vyžaduje, aby byl příznak **Povolit konzistentní zpracování způsobu doručení v kanálu** zapnuta v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa272-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="aa272-115">Pokud je příznak funkce zapnutý, bude přepravní poplatky budou účtovány buď na úrovni záhlaví, nebo úrovni řádku, podle konfigurace centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa272-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="aa272-116">Téma Fabrikam podporuje smíšený způsob doručení, kdy jsou některé položky vybrány pro odeslání, jiné jsou vybrány pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="aa272-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="aa272-117">V tomto režimu budou poplatky za přepravu poměrné pro všechny položky, které jsou vybrány pro způsob doručení.</span><span class="sxs-lookup"><span data-stu-id="aa272-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="aa272-118">Aby smíšený režim doručení fungoval, musíte nejprve nakonfigurovat **Náklady záhlaví s proměrným** funkci v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa272-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="aa272-119">Další informace o této konfiguraci naleznete v části [Poměrné poplatky za záhlaví odpovídají řádkům prodeje](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="aa272-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="aa272-120">Pokud se na řádkové položky vztahují poplatky za dopravu, mohou být pro každou položku zobrazeny v řádku košíku.</span><span class="sxs-lookup"><span data-stu-id="aa272-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="aa272-121">Tato funkce vyžaduje, aby **Zobrazit poplatky pro položky řádku** vlastnost byla zapnuta jak pro zboží pro modul košíku i modul pokladny.</span><span class="sxs-lookup"><span data-stu-id="aa272-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="aa272-122">Další informace viz [Modul košíku](add-cart-module.md) a [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="aa272-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="aa272-123">Následující obrázek ukazuje příklad modulu možností dodání na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="aa272-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Příklad modulu možností dodání na stránce pokladny](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="aa272-125">Vlastnosti modulu možností dodání</span><span class="sxs-lookup"><span data-stu-id="aa272-125">Delivery options module properties</span></span>

| <span data-ttu-id="aa272-126">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="aa272-126">Property</span></span> | <span data-ttu-id="aa272-127">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="aa272-127">Values</span></span> | <span data-ttu-id="aa272-128">popis</span><span class="sxs-lookup"><span data-stu-id="aa272-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="aa272-129">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="aa272-129">Heading</span></span> | <span data-ttu-id="aa272-130">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="aa272-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="aa272-131">Volitelný nadpis pro modul možností dodání.</span><span class="sxs-lookup"><span data-stu-id="aa272-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="aa272-132">Vlastní název třídy CSS</span><span class="sxs-lookup"><span data-stu-id="aa272-132">Custom CSS class name</span></span> | <span data-ttu-id="aa272-133">Text</span><span class="sxs-lookup"><span data-stu-id="aa272-133">Text</span></span> | <span data-ttu-id="aa272-134">Vlastní název třídy kaskádových stylů (CSS), ktera bude použita k vykreslení tohoto modulu, je-li to relevantní.</span><span class="sxs-lookup"><span data-stu-id="aa272-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="aa272-135">Možnost režimu filtrování doručení</span><span class="sxs-lookup"><span data-stu-id="aa272-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="aa272-136">**Nefiltrovat** nebo **Režimy bez dopravy**</span><span class="sxs-lookup"><span data-stu-id="aa272-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="aa272-137">Hodnota, která určuje, zda by modul voleb doručení měl odfiltrovat všechny režimy doručení bez dodání.</span><span class="sxs-lookup"><span data-stu-id="aa272-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="aa272-138">Automaticky vybrat možnost doručení</span><span class="sxs-lookup"><span data-stu-id="aa272-138">Auto select a delivery option</span></span> | <span data-ttu-id="aa272-139">**Nefiltrovat**, **Automaticky vybrat možnost doručení a zobrazit souhrn** nebo **Možnost automatického výběru doručení a nezobrazovat souhrn**</span><span class="sxs-lookup"><span data-stu-id="aa272-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="aa272-140">Tato vlastnost automaticky použije první dostupnou možnost doručení k pokladně, aniž by vyžadovala, aby ji uživatel vybral.</span><span class="sxs-lookup"><span data-stu-id="aa272-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="aa272-141">Mělo by se používat pouze v případě, že je k dispozici jedna možnost doručení.</span><span class="sxs-lookup"><span data-stu-id="aa272-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="aa272-142">Tato vlastnosti je podporována od Commerce verze 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="aa272-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="aa272-143">Na stránku pokladny přidejte modul dodání a nastavte požadované vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="aa272-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="aa272-144">Modul možností dodání lze přidat pouze do modulu pokladny.</span><span class="sxs-lookup"><span data-stu-id="aa272-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="aa272-145">Další informace o konfiguraci modulu voleb dodání a jeho přidání na stránku pokladny naleznete na stránce [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="aa272-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa272-146">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="aa272-146">Additional resources</span></span>

[<span data-ttu-id="aa272-147">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="aa272-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="aa272-148">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="aa272-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="aa272-149">Platební modul</span><span class="sxs-lookup"><span data-stu-id="aa272-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="aa272-150">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="aa272-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="aa272-151">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="aa272-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="aa272-152">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="aa272-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="aa272-153">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="aa272-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="aa272-154">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="aa272-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="aa272-155">Omnikanálové rozšířené automatické náklady</span><span class="sxs-lookup"><span data-stu-id="aa272-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="aa272-156">Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje</span><span class="sxs-lookup"><span data-stu-id="aa272-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="aa272-157">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="aa272-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
