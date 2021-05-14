---
title: Modul dárkového poukazu
description: Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962756"
---
# <a name="gift-card-module"></a><span data-ttu-id="f1638-103">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="f1638-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1638-104">Tohle téma se zabývá moduly dárkového poukazu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1638-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f1638-105">Moduly dárkových poukazů lze použít v modulech pokladny pro příjem dárkových poukazů, což je běžná forma platby používaná při transakcích elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="f1638-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="f1638-106">Modul dárkových poukazů podporuje dárkové poukazy pro Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="f1638-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="f1638-107">SVS a Givex dárkové poukazy jsou uplatněny prostřednictvím poskytovatele plateb Adyen.</span><span class="sxs-lookup"><span data-stu-id="f1638-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="f1638-108">Další informace o podpoře externích dárkových poukazů, jako jsou například SVS a Givex, naleznete v tématu [Podpora externích dárkových poukazů](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="f1638-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f1638-109">Podpora pro uplatnění dárkových karet SVS a Givex během procesu placení je k dispozici ve vydání Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="f1638-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="f1638-110">K dispozici jsou dva moduly dárkových poukazů:</span><span class="sxs-lookup"><span data-stu-id="f1638-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="f1638-111">**Dárkový poukaz** – Tento modul lze použít na stránce pokladny k uplatnění dárkového poukazu jako úhrady.</span><span class="sxs-lookup"><span data-stu-id="f1638-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="f1638-112">**Kontrola zůstatku dárkového poukazu** – Tento modul lze použít na kterékoli stránce ke kontrole zůstatku dárkového poukazu.</span><span class="sxs-lookup"><span data-stu-id="f1638-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="f1638-113">Tento modul je k dispozici v aplikaci Commerce verze 10.0.14 a novější.</span><span class="sxs-lookup"><span data-stu-id="f1638-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="f1638-114">Podpora modulu kontroly zůstatku dárkové karty je k dispozici ve vydání Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="f1638-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="f1638-115">Následující obrázek znázorňuje příklad modulu dárkového poukazu na stránce pokladny.</span><span class="sxs-lookup"><span data-stu-id="f1638-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Příklad modulu dárkového poukazu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="f1638-117">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="f1638-117">Module properties</span></span>

- <span data-ttu-id="f1638-118">**Zobrazit další pole** – Tato vlastnost určuje, která pole mají být zobrazena pro dárkové poukazy kromě čísla dárkového poukazu, který je ve výchozím nastavení vždy zobrazen.</span><span class="sxs-lookup"><span data-stu-id="f1638-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="f1638-119">Některé dárkové poukazy například podporují zobrazení osobního identifikačního čísla (PIN) a další podporují zobrazování kódu PIN a data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="f1638-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="f1638-120">Druhou možností může být nastavení této vlastnosti na "none", která by zobrazila pouze číslo dárkového poukazu a žádná další pole.</span><span class="sxs-lookup"><span data-stu-id="f1638-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="f1638-121">Podporované hodnoty:</span><span class="sxs-lookup"><span data-stu-id="f1638-121">Supported values:</span></span>
-   <span data-ttu-id="f1638-122">PIN</span><span class="sxs-lookup"><span data-stu-id="f1638-122">PIN</span></span>
-   <span data-ttu-id="f1638-123">Datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="f1638-123">Expiration date</span></span>
-   <span data-ttu-id="f1638-124">PIN a datum konce platnosti</span><span class="sxs-lookup"><span data-stu-id="f1638-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="f1638-125">Žádní</span><span class="sxs-lookup"><span data-stu-id="f1638-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="f1638-126">Nastavení webu pro moduly dárkových poukazů</span><span class="sxs-lookup"><span data-stu-id="f1638-126">Site settings for gift card modules</span></span>

<span data-ttu-id="f1638-127">V konfigurátoru webů Commerce v **Nastavení webu \> Rozšíření** existuje nastavení modulu dárkového poukazu s názvem **Podporovaný typ dárkového poukazu**.</span><span class="sxs-lookup"><span data-stu-id="f1638-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="f1638-128">Toto nastavení podporuje tři hodnoty:</span><span class="sxs-lookup"><span data-stu-id="f1638-128">This setting supports three values:</span></span>
- <span data-ttu-id="f1638-129">**Dárkový pouikaz Dynamics 365** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f1638-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="f1638-130">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1638-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="f1638-131">**Dárkové poukazy SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje pouze dárkové poukazy SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="f1638-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="f1638-132">Toto nastavení je podporováno pro přihlášené i anonymní uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1638-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="f1638-133">**Dárkové poukazy Dynamics 365, SVS a Givex** - je-li použito toto nastavení, modul dárkového poukazu umožňuje dárkové poukazy Dynamics 365, SVS a Givex.</span><span class="sxs-lookup"><span data-stu-id="f1638-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="f1638-134">Toto nastavení je podporováno pouze pro přihlášené uživatele na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1638-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1638-135">Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.11 a jsou vyžadována, pouze pokud potřebujete podporu pro dárkové karty SVS nebo Givex.</span><span class="sxs-lookup"><span data-stu-id="f1638-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="f1638-136">Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="f1638-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f1638-137">Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="f1638-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="f1638-138">Rozšíření interních dárkových karet pro použití v elektronických obchodech</span><span class="sxs-lookup"><span data-stu-id="f1638-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="f1638-139">Ve výchozím nastavení nejsou interní dárkové karty optimalizovány pro použití v elektronických obchodech.</span><span class="sxs-lookup"><span data-stu-id="f1638-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="f1638-140">Než tedy povolíte použití interních dárkových karet k platbám, měli byste je nakonfigurovat pomocí rozšíření, která jim pomohou zajistit větší bezpečnost.</span><span class="sxs-lookup"><span data-stu-id="f1638-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="f1638-141">Tady jsou oblasti dárkových karet, které byste měli rozšířit, než povolíte použití interních dárkových karet ve výrobě:</span><span class="sxs-lookup"><span data-stu-id="f1638-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="f1638-142">**Číslo dárkové karty** – Číselné řady se používají ke generování čísel dárkových karet pro interní dárkové karty.</span><span class="sxs-lookup"><span data-stu-id="f1638-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="f1638-143">Protože lze snadno předvídat číselné řady, měli byste rozšířit generování čísel dárkových karet tak, aby se pro vydaná čísla dárkových karet používaly náhodné kryptograficky zabezpečené řetězce.</span><span class="sxs-lookup"><span data-stu-id="f1638-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="f1638-144">**GetBalance** – API **GetBalance** se používá k vyhledávání zůstatků dárkových karet.</span><span class="sxs-lookup"><span data-stu-id="f1638-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="f1638-145">Ve výchozím nastavení je toto rozhraní API veřejné.</span><span class="sxs-lookup"><span data-stu-id="f1638-145">By default, this API public.</span></span> <span data-ttu-id="f1638-146">Pokud k vyhledání zůstatků dárkových karet není vyžadován PIN, existuje riziko, že by útoky hrubou silou mohly použít API **GetBalance** k pokusu vyhledat čísla dárkových karet, které mají zůstatky.</span><span class="sxs-lookup"><span data-stu-id="f1638-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="f1638-147">Implementací požadavků na PIN pro interní dárkové karty a omezení API můžete pomoci zmírnit riziko.</span><span class="sxs-lookup"><span data-stu-id="f1638-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="f1638-148">**PIN** – Ve výchozím nastavení interní dárkové karty nepodporují kódy PIN.</span><span class="sxs-lookup"><span data-stu-id="f1638-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="f1638-149">Interní dárkové karty byste měli rozšířit tak, aby byl k vyhledání zůstatků vyžadován PIN.</span><span class="sxs-lookup"><span data-stu-id="f1638-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="f1638-150">Tuto funkci lze také použít k uzamčení dárkových karet po po sobě jdoucích nesprávných pokusech o zadání kódu PIN.</span><span class="sxs-lookup"><span data-stu-id="f1638-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="f1638-151">U pokladny pro hosty povolte platby dárkovou kartou</span><span class="sxs-lookup"><span data-stu-id="f1638-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="f1638-152">Ve výchozím nastavení nejsou platby pokladní kartou povoleny pro (anonymní) pokladnu hosta.</span><span class="sxs-lookup"><span data-stu-id="f1638-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="f1638-153">Pokud je chcete povolit, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="f1638-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="f1638-154">V centru Commerce přejděte na možnost **Retail a Commerce \> Nastavení kanáu \> Nastavení POS \> POS \> Operace POS**.</span><span class="sxs-lookup"><span data-stu-id="f1638-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="f1638-155">Vyberte a podržte (nebo klikněte pravým tlačítkem) záhlaví mřížky a poté vyberte **Vložit sloupce**.</span><span class="sxs-lookup"><span data-stu-id="f1638-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="f1638-156">V dialogovém okně **Vložit sloupce** zaškrtněte políčko **AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="f1638-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="f1638-157">Vyberte **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="f1638-157">Select **Update**.</span></span>
1. <span data-ttu-id="f1638-158">Pro operace **520** (Zůstatek dárkové karty) a **214**, nastavte hodnotu **AllowAnonymousAccess** na **1**.</span><span class="sxs-lookup"><span data-stu-id="f1638-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="f1638-159">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f1638-159">Select **Save**.</span></span>
1. <span data-ttu-id="f1638-160">Spusťte úlohu plánovače **1090** k synchronizování změn do databáze kanálů.</span><span class="sxs-lookup"><span data-stu-id="f1638-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="f1638-161">Přidání modulu dárkového poukazu na stránku</span><span class="sxs-lookup"><span data-stu-id="f1638-161">Add a gift card module to a page</span></span>

<span data-ttu-id="f1638-162">Pokyny k přidání modulu dárkového poukazu na stránku pokladny a nastavení požadovaných vlastností naleznete v tématu [Modul pokladny](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f1638-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1638-163">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f1638-163">Additional resources</span></span>

[<span data-ttu-id="f1638-164">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="f1638-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f1638-165">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="f1638-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f1638-166">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="f1638-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f1638-167">Platební modul</span><span class="sxs-lookup"><span data-stu-id="f1638-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f1638-168">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="f1638-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f1638-169">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="f1638-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f1638-170">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="f1638-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f1638-171">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="f1638-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f1638-172">Podpora pro externí dárkové poukazy</span><span class="sxs-lookup"><span data-stu-id="f1638-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="f1638-173">SDK a aktualizace knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="f1638-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
