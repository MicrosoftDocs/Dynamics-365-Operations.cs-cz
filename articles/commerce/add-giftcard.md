---
title: Modul dárkového poukazu
description: Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661235"
---
# <a name="gift-card-module"></a><span data-ttu-id="ba4c0-103">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="ba4c0-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba4c0-104">Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ba4c0-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="ba4c0-105">Overview</span></span>

<span data-ttu-id="ba4c0-106">Dárkové poukazy jsou běžnou formou plateb a modul dárkových poukazů lze použít v modulu pokladny pro příjem dárkových poukazů.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="ba4c0-107">Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="ba4c0-108">SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="ba4c0-109">Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="ba4c0-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="ba4c0-110">Následující obrázek znázorňuje příklad modulu dárkového poukazu na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Příklad modulu dárkového poukazu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="ba4c0-112">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="ba4c0-112">Module properties</span></span>

- <span data-ttu-id="ba4c0-113">**Zobrazit další pole** – Tato vlastnost určuje, která pole mají být zobrazena pro dárkové poukazy kromě čísla dárkového poukazu, který je ve výchozím nastavení vždy zobrazen.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="ba4c0-114">Některé dárkové poukazy například podporují zobrazení osobního identifikačního čísla (PIN) a další podporují zobrazování kódu PIN a data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="ba4c0-115">Druhou možností může být nastavení této vlastnosti na "none", která by zobrazila pouze číslo dárkového poukazu a žádná další pole.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="ba4c0-116">Podporované hodnoty:</span><span class="sxs-lookup"><span data-stu-id="ba4c0-116">Supported values:</span></span>
-   <span data-ttu-id="ba4c0-117">PIN</span><span class="sxs-lookup"><span data-stu-id="ba4c0-117">PIN</span></span>
-   <span data-ttu-id="ba4c0-118">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="ba4c0-118">Expiration date</span></span>
-   <span data-ttu-id="ba4c0-119">PIN a datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="ba4c0-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="ba4c0-120">Žádní</span><span class="sxs-lookup"><span data-stu-id="ba4c0-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="ba4c0-121">Nastavení webu pro moduly dárkových poukazů</span><span class="sxs-lookup"><span data-stu-id="ba4c0-121">Site settings for gift card modules</span></span>

<span data-ttu-id="ba4c0-122">V konfigurátoru webů Commerce v **Nastavení webu \> Rozšíření** existuje nastavení modulu dárkového poukazu s názvem **Podporovaný typ dárkového poukazu**.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="ba4c0-123">Toto nastavení podporuje tři hodnoty:</span><span class="sxs-lookup"><span data-stu-id="ba4c0-123">This setting supports three values:</span></span>
- <span data-ttu-id="ba4c0-124">**Dárkový pouikaz Dynamics 365** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="ba4c0-125">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="ba4c0-126">**Dárkové poukazy SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="ba4c0-127">Toto nastavení je podporováno pro přihlášené i anonymní uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="ba4c0-128">**Dárkové poukazy Dynamics 365, SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje dárkové poukazy Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="ba4c0-129">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="ba4c0-130">Přidání modulu dárkového poukazu na stránku</span><span class="sxs-lookup"><span data-stu-id="ba4c0-130">Add a gift card module to a page</span></span>

<span data-ttu-id="ba4c0-131">Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="ba4c0-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba4c0-132">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ba4c0-132">Additional resources</span></span>

[<span data-ttu-id="ba4c0-133">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="ba4c0-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ba4c0-134">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="ba4c0-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="ba4c0-135">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="ba4c0-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ba4c0-136">Modul platby</span><span class="sxs-lookup"><span data-stu-id="ba4c0-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="ba4c0-137">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="ba4c0-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="ba4c0-138">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="ba4c0-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="ba4c0-139">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="ba4c0-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ba4c0-140">Podpora pro externí dárkové poukazy</span><span class="sxs-lookup"><span data-stu-id="ba4c0-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
