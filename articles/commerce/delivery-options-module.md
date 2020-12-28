---
title: Modul možností doručení
description: Toto téma popisuje moduly možností dodání a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f9e8df576efd1e58fde235828823f31e87ed58bf
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410949"
---
# <a name="delivery-options-module"></a><span data-ttu-id="31526-103">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="31526-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31526-104">Toto téma popisuje moduly možností dodání a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31526-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31526-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="31526-105">Overview</span></span>

<span data-ttu-id="31526-106">Moduly možností doručení umožňují zákazníkům vybrat způsob doručení, jako je například dopravce nebo vyzvednutí pro jejich online objednávku.</span><span class="sxs-lookup"><span data-stu-id="31526-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="31526-107">Pro určení způsobu doručení je vyžadována dodací adresa.</span><span class="sxs-lookup"><span data-stu-id="31526-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="31526-108">Pokud se změní dodací adresa, je nutné znovu načíst možnosti dodání.</span><span class="sxs-lookup"><span data-stu-id="31526-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="31526-109">Pokud objednávka obsahuje pouze položky, které budou vydány v obchodě, bude tento modul automaticky skrytý.</span><span class="sxs-lookup"><span data-stu-id="31526-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="31526-110">Informace o tom, jak konfigurovat režimy doručení, naleznete v části [Nastavení online kanálu](channel-setup-online.md) a [Nastavení způsobů dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="31526-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="31526-111">Každý režim dodání může mít související poplatek.</span><span class="sxs-lookup"><span data-stu-id="31526-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="31526-112">Informace o tom, jak nakonfigurovat náklady pro online obchod, naleznete v tématu [Omnikanál – pokročilé automatické náklady](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="31526-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="31526-113">V Commerce verze 10.0.13 byl aktualizován modul voleb doručení, aby podporoval **Náklady záhlaví bez proměrného** a **Doprava jako náklad řádku** funkce.</span><span class="sxs-lookup"><span data-stu-id="31526-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="31526-114">Pokud je prorace vypnutá, očekává se, že pracovní postup elektronického obchodování neumožňuje smíšený způsob doručení pro položky v košíku (to znamená, že některé položky jsou vybrány pro odeslání, jiné jsou vybrány pro vyzvednutí).</span><span class="sxs-lookup"><span data-stu-id="31526-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="31526-115">**Náklady záhlaví bez proměrného** funkce vyžaduje, aby **Povolit konzistentní zpracování způsobu doručení v kanálu** vlajka zapnuta v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="31526-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="31526-116">Pokud je funkce zapnuta, bude přepravní poplatky budou účtovány buď na úrovni záhlaví, nebo úrovni řádku, podle konfigurace centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="31526-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="31526-117">Téma Fabrikam podporuje smíšený způsob doručení, kdy jsou některé položky vybrány pro odeslání, jiné jsou vybrány pro vyzvednutí.</span><span class="sxs-lookup"><span data-stu-id="31526-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="31526-118">V tomto režimu budou poplatky za přepravu poměrné pro všechny položky, které jsou vybrány pro způsob doručení.</span><span class="sxs-lookup"><span data-stu-id="31526-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="31526-119">Aby smíšený režim doručení fungoval, musíte nejprve nakonfigurovat **Náklady záhlaví s proměrným** funkci v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="31526-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="31526-120">Další informace o této konfiguraci naleznete v části [Poměrné poplatky za záhlaví odpovídají řádkům prodeje](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="31526-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="31526-121">Pokud se na řádkové položky vztahují poplatky za dopravu, mohou být pro každou položku zobrazeny v řádku košíku.</span><span class="sxs-lookup"><span data-stu-id="31526-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="31526-122">Tato funkce vyžaduje, aby **Zobrazit poplatky pro položky řádku** vlastnost byla zapnuta jak pro zboží pro modul košíku i modul pokladny.</span><span class="sxs-lookup"><span data-stu-id="31526-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="31526-123">Další informace viz [Modul košíku](add-cart-module.md) a [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="31526-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="31526-124">Následující obrázek ukazuje příklad modulu možností dodání na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="31526-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Příklad modulu možností dodání na stránce pokladny](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="31526-126">Vlastnosti modulu možností dodání</span><span class="sxs-lookup"><span data-stu-id="31526-126">Delivery options module properties</span></span>

| <span data-ttu-id="31526-127">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="31526-127">Property</span></span> | <span data-ttu-id="31526-128">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="31526-128">Values</span></span> | <span data-ttu-id="31526-129">popis</span><span class="sxs-lookup"><span data-stu-id="31526-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="31526-130">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="31526-130">Heading</span></span> | <span data-ttu-id="31526-131">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="31526-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="31526-132">Volitelný nadpis pro modul možností dodání.</span><span class="sxs-lookup"><span data-stu-id="31526-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="31526-133">Vlastní název třídy CSS</span><span class="sxs-lookup"><span data-stu-id="31526-133">Custom CSS class name</span></span> | <span data-ttu-id="31526-134">Text</span><span class="sxs-lookup"><span data-stu-id="31526-134">Text</span></span> | <span data-ttu-id="31526-135">Vlastní název třídy kaskádových stylů (CSS), ktera bude použita k vykreslení tohoto modulu, je-li to relevantní.</span><span class="sxs-lookup"><span data-stu-id="31526-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="31526-136">Možnost režimu filtrování doručení</span><span class="sxs-lookup"><span data-stu-id="31526-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="31526-137">**Nefiltrovat** nebo **Režimy bez dopravy**</span><span class="sxs-lookup"><span data-stu-id="31526-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="31526-138">Hodnota, která určuje, zda by modul voleb doručení měl odfiltrovat všechny režimy doručení bez dodání.</span><span class="sxs-lookup"><span data-stu-id="31526-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="31526-139">Na stránku pokladny přidejte modul dodání a nastavte požadované vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="31526-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="31526-140">Modul možností dodání lze přidat pouze do modulu pokladny.</span><span class="sxs-lookup"><span data-stu-id="31526-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="31526-141">Další informace o konfiguraci modulu voleb dodání a jeho přidání na stránku pokladny naleznete na stránce [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="31526-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31526-142">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="31526-142">Additional resources</span></span>

[<span data-ttu-id="31526-143">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="31526-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="31526-144">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="31526-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="31526-145">Platební modul</span><span class="sxs-lookup"><span data-stu-id="31526-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="31526-146">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="31526-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="31526-147">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="31526-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="31526-148">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="31526-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="31526-149">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="31526-149">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="31526-150">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="31526-150">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="31526-151">Omnikanálové rozšířené automatické náklady</span><span class="sxs-lookup"><span data-stu-id="31526-151">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="31526-152">Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje</span><span class="sxs-lookup"><span data-stu-id="31526-152">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="31526-153">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="31526-153">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
