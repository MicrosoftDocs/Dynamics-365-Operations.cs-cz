---
title: Modul dárkového poukazu
description: Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761074"
---
# <a name="gift-card-module"></a><span data-ttu-id="a04ca-103">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="a04ca-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a04ca-104">Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a04ca-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a04ca-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="a04ca-105">Overview</span></span>

<span data-ttu-id="a04ca-106">Moduly dárkových poukazů lze použít v modulech pokladny pro příjem dárkových poukazů, což je běžná forma platby používaná při transakcích elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="a04ca-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="a04ca-107">Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="a04ca-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="a04ca-108">SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen.</span><span class="sxs-lookup"><span data-stu-id="a04ca-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="a04ca-109">Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="a04ca-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="a04ca-110">K dispozici jsou dva moduly dárkových poukazů:</span><span class="sxs-lookup"><span data-stu-id="a04ca-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="a04ca-111">**Dárkový poukaz** – Tento modul lze použít na stránce pokladny k uplatnění dárkového poukazu jako úhrady.</span><span class="sxs-lookup"><span data-stu-id="a04ca-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="a04ca-112">**Kontrola zůstatku dárkového poukazu** – Tento modul lze použít na kterékoli stránce ke kontrole zůstatku dárkového poukazu.</span><span class="sxs-lookup"><span data-stu-id="a04ca-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="a04ca-113">Tento modul je k dispozici v aplikaci Commerce verze 10.0.14 a novější.</span><span class="sxs-lookup"><span data-stu-id="a04ca-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="a04ca-114">Následující obrázek znázorňuje příklad modulu dárkového poukazu na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="a04ca-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Příklad modulu dárkového poukazu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="a04ca-116">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="a04ca-116">Module properties</span></span>

- <span data-ttu-id="a04ca-117">**Zobrazit další pole** – Tato vlastnost určuje, která pole mají být zobrazena pro dárkové poukazy kromě čísla dárkového poukazu, který je ve výchozím nastavení vždy zobrazen.</span><span class="sxs-lookup"><span data-stu-id="a04ca-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="a04ca-118">Některé dárkové poukazy například podporují zobrazení osobního identifikačního čísla (PIN) a další podporují zobrazování kódu PIN a data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="a04ca-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="a04ca-119">Druhou možností může být nastavení této vlastnosti na "none", která by zobrazila pouze číslo dárkového poukazu a žádná další pole.</span><span class="sxs-lookup"><span data-stu-id="a04ca-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="a04ca-120">Podporované hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a04ca-120">Supported values:</span></span>
-   <span data-ttu-id="a04ca-121">PIN</span><span class="sxs-lookup"><span data-stu-id="a04ca-121">PIN</span></span>
-   <span data-ttu-id="a04ca-122">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="a04ca-122">Expiration date</span></span>
-   <span data-ttu-id="a04ca-123">PIN a datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="a04ca-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="a04ca-124">Žádní</span><span class="sxs-lookup"><span data-stu-id="a04ca-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="a04ca-125">Nastavení webu pro moduly dárkových poukazů</span><span class="sxs-lookup"><span data-stu-id="a04ca-125">Site settings for gift card modules</span></span>

<span data-ttu-id="a04ca-126">V konfigurátoru webů Commerce v **Nastavení webu \> Rozšíření** existuje nastavení modulu dárkového poukazu s názvem **Podporovaný typ dárkového poukazu**.</span><span class="sxs-lookup"><span data-stu-id="a04ca-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="a04ca-127">Toto nastavení podporuje tři hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a04ca-127">This setting supports three values:</span></span>
- <span data-ttu-id="a04ca-128">**Dárkový pouikaz Dynamics 365** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a04ca-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="a04ca-129">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a04ca-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="a04ca-130">**Dárkové poukazy SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="a04ca-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="a04ca-131">Toto nastavení je podporováno pro přihlášené i anonymní uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a04ca-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="a04ca-132">**Dárkové poukazy Dynamics 365, SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje dárkové poukazy Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="a04ca-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="a04ca-133">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a04ca-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="a04ca-134">Přidání modulu dárkového poukazu na stránku</span><span class="sxs-lookup"><span data-stu-id="a04ca-134">Add a gift card module to a page</span></span>

<span data-ttu-id="a04ca-135">Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="a04ca-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a04ca-136">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a04ca-136">Additional resources</span></span>

[<span data-ttu-id="a04ca-137">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="a04ca-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a04ca-138">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="a04ca-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a04ca-139">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="a04ca-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a04ca-140">Modul platby</span><span class="sxs-lookup"><span data-stu-id="a04ca-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a04ca-141">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="a04ca-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a04ca-142">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="a04ca-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a04ca-143">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="a04ca-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a04ca-144">Podpora pro externí dárkové poukazy</span><span class="sxs-lookup"><span data-stu-id="a04ca-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
