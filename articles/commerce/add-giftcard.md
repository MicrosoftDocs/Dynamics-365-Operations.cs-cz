---
title: Modul dárkového poukazu
description: Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206288"
---
# <a name="gift-card-module"></a><span data-ttu-id="b89fa-103">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="b89fa-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b89fa-104">Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b89fa-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b89fa-105">Moduly dárkových poukazů lze použít v modulech pokladny pro příjem dárkových poukazů, což je běžná forma platby používaná při transakcích elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="b89fa-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b89fa-106">Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="b89fa-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b89fa-107">SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen.</span><span class="sxs-lookup"><span data-stu-id="b89fa-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b89fa-108">Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="b89fa-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b89fa-109">Podpora pro uplatnění dárkových karet SVS a Givex během procesu placení je k dispozici ve vydání Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="b89fa-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="b89fa-110">K dispozici jsou dva moduly dárkových poukazů:</span><span class="sxs-lookup"><span data-stu-id="b89fa-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="b89fa-111">**Dárkový poukaz** – Tento modul lze použít na stránce pokladny k uplatnění dárkového poukazu jako úhrady.</span><span class="sxs-lookup"><span data-stu-id="b89fa-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b89fa-112">**Kontrola zůstatku dárkového poukazu** – Tento modul lze použít na kterékoli stránce ke kontrole zůstatku dárkového poukazu.</span><span class="sxs-lookup"><span data-stu-id="b89fa-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b89fa-113">Tento modul je k dispozici v aplikaci Commerce verze 10.0.14 a novější.</span><span class="sxs-lookup"><span data-stu-id="b89fa-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="b89fa-114">Podpora modulu kontroly zůstatku dárkové karty je k dispozici ve vydání Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="b89fa-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="b89fa-115">Následující obrázek znázorňuje příklad modulu dárkového poukazu na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="b89fa-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Příklad modulu dárkového poukazu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b89fa-117">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="b89fa-117">Module properties</span></span>

- <span data-ttu-id="b89fa-118">**Zobrazit další pole** – Tato vlastnost určuje, která pole mají být zobrazena pro dárkové poukazy kromě čísla dárkového poukazu, který je ve výchozím nastavení vždy zobrazen.</span><span class="sxs-lookup"><span data-stu-id="b89fa-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b89fa-119">Některé dárkové poukazy například podporují zobrazení osobního identifikačního čísla (PIN) a další podporují zobrazování kódu PIN a data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="b89fa-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b89fa-120">Druhou možností může být nastavení této vlastnosti na "none", která by zobrazila pouze číslo dárkového poukazu a žádná další pole.</span><span class="sxs-lookup"><span data-stu-id="b89fa-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b89fa-121">Podporované hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b89fa-121">Supported values:</span></span>
-   <span data-ttu-id="b89fa-122">PIN</span><span class="sxs-lookup"><span data-stu-id="b89fa-122">PIN</span></span>
-   <span data-ttu-id="b89fa-123">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="b89fa-123">Expiration date</span></span>
-   <span data-ttu-id="b89fa-124">PIN a datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="b89fa-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="b89fa-125">Žádní</span><span class="sxs-lookup"><span data-stu-id="b89fa-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b89fa-126">Nastavení webu pro moduly dárkových poukazů</span><span class="sxs-lookup"><span data-stu-id="b89fa-126">Site settings for gift card modules</span></span>

<span data-ttu-id="b89fa-127">V konfigurátoru webů Commerce v **Nastavení webu \> Rozšíření** existuje nastavení modulu dárkového poukazu s názvem **Podporovaný typ dárkového poukazu**.</span><span class="sxs-lookup"><span data-stu-id="b89fa-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b89fa-128">Toto nastavení podporuje tři hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b89fa-128">This setting supports three values:</span></span>
- <span data-ttu-id="b89fa-129">**Dárkový pouikaz Dynamics 365** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b89fa-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b89fa-130">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b89fa-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b89fa-131">**Dárkové poukazy SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="b89fa-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b89fa-132">Toto nastavení je podporováno pro přihlášené i anonymní uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b89fa-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b89fa-133">**Dárkové poukazy Dynamics 365, SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje dárkové poukazy Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="b89fa-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b89fa-134">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b89fa-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b89fa-135">Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.11 a jsou vyžadována, pouze pokud potřebujete podporu pro dárkové karty SVS nebo Givex.</span><span class="sxs-lookup"><span data-stu-id="b89fa-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="b89fa-136">Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="b89fa-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b89fa-137">Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="b89fa-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b89fa-138">Přidání modulu dárkového poukazu na stránku</span><span class="sxs-lookup"><span data-stu-id="b89fa-138">Add a gift card module to a page</span></span>

<span data-ttu-id="b89fa-139">Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b89fa-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b89fa-140">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b89fa-140">Additional resources</span></span>

[<span data-ttu-id="b89fa-141">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="b89fa-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b89fa-142">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="b89fa-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b89fa-143">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="b89fa-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b89fa-144">Platební modul</span><span class="sxs-lookup"><span data-stu-id="b89fa-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b89fa-145">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="b89fa-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b89fa-146">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="b89fa-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b89fa-147">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="b89fa-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b89fa-148">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="b89fa-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b89fa-149">Podpora pro externí dárkové poukazy</span><span class="sxs-lookup"><span data-stu-id="b89fa-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="b89fa-150">SDK a aktualizace knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="b89fa-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]