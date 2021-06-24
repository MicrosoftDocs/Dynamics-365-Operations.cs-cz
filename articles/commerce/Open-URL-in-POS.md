---
title: Otevření URL adresy v POS
description: Toto téma poskytuje přehled vylepšení, která byla provedena u funkce vyhledávání produktu a vyhledávání zákazníka v aplikaci Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193196"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="8bbba-103">Otevření URL adresy v POS</span><span class="sxs-lookup"><span data-stu-id="8bbba-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8bbba-104">Toto téma popisuje konfiguraci tlačítka v pokladním místě Dynamics 365 Commerce pro otevření adresy URL.</span><span class="sxs-lookup"><span data-stu-id="8bbba-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="8bbba-105">Tato funkce nevyžaduje přizpůsobení kódu a může ji konfigurovat kdokoliv, i bez role vývojáře.</span><span class="sxs-lookup"><span data-stu-id="8bbba-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="8bbba-106">Tato funkce umožňuje konfiguraci tlačítka v POS pomocí návrháře mřížky tlačítek pro otevření URL adresy.</span><span class="sxs-lookup"><span data-stu-id="8bbba-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="8bbba-107">To je v současné době podporováno v následujících konfiguracích:</span><span class="sxs-lookup"><span data-stu-id="8bbba-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="8bbba-108">Otevření v novém okně.</span><span class="sxs-lookup"><span data-stu-id="8bbba-108">Open in new window.</span></span>
- <span data-ttu-id="8bbba-109">Otevření v rámci POS.</span><span class="sxs-lookup"><span data-stu-id="8bbba-109">Open within POS.</span></span>
- <span data-ttu-id="8bbba-110">Otevření nativní aplikace.</span><span class="sxs-lookup"><span data-stu-id="8bbba-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="8bbba-111">Otevřít v novém okně</span><span class="sxs-lookup"><span data-stu-id="8bbba-111">Open in new window</span></span>

<span data-ttu-id="8bbba-112">Tato konfigurace určuje, zda má být otevřena adresa URL v novém okně nebo v rámci aplikace.</span><span class="sxs-lookup"><span data-stu-id="8bbba-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="8bbba-113">Když je webová URL adresa nakonfigurována k otevření v rámci aplikace, postranní navigační panel a horní lišta pokladního místa jsou viditelné a dostupné pro interakci uživatele.</span><span class="sxs-lookup"><span data-stu-id="8bbba-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="8bbba-114">Když je nakonfigurována k otevření v novém okně, URL adresa se otevře v novém okně aplikace na Modern POS pro Windows a na nové kartě prohlížeče ve všech ostatních klientech POS.</span><span class="sxs-lookup"><span data-stu-id="8bbba-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="8bbba-115">Chcete-li to povolit, je nutné konfigurovat adresu URL s vybranou možností **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="8bbba-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="8bbba-116">Otevření v rámci POS</span><span class="sxs-lookup"><span data-stu-id="8bbba-116">Open within POS</span></span>

<span data-ttu-id="8bbba-117">Otevření webové adresy URL v pokladním místě je momentálně podporováno pouze pro Modern POS v systému Windows.</span><span class="sxs-lookup"><span data-stu-id="8bbba-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="8bbba-118">Na dalších klientech se tato funkce vyvíjí a je plánována pro vydání v budoucích aktualizacích.</span><span class="sxs-lookup"><span data-stu-id="8bbba-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="8bbba-119">Chcete-li to povolit, je nutné konfigurovat adresu URL s nevybranou možností **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="8bbba-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="8bbba-120">Otevření nativní aplikace</span><span class="sxs-lookup"><span data-stu-id="8bbba-120">Open a native app</span></span>

<span data-ttu-id="8bbba-121">Tato funkce také umožňuje zadat newebovou adresu URL pro otevření nativní aplikace.</span><span class="sxs-lookup"><span data-stu-id="8bbba-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="8bbba-122">Můžete například určit URL protokoly, např. MailTo, SIP, IM nebo MSTEAMS, které lze pak zpracovat pomocí příslušných nativní aplikací na zařízení hostitele.</span><span class="sxs-lookup"><span data-stu-id="8bbba-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="8bbba-123">Chcete-li to povolit, je nutné konfigurovat adresu URL s vybranou možností **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="8bbba-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="8bbba-124">U počítačů se systémem Windows nahlédněte do části [Export nebo import výchozích přidružení aplikace](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) a nastavte výchozí přidružení protokolu, pokud nastavujete svůj počítač pomocí Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="8bbba-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="8bbba-125">Pokud používáte MDM, jako je například Intune, pro správu počítačů Windows, nahlédněte do [Zásady zprostředkovatele kryptografických služeb - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="8bbba-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="8bbba-126">Pokud jste vývojář vytvářející vlastní web, nahlédněte do tématu [Spuštění výchozí aplikace pro identifikátor URI](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="8bbba-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="8bbba-127">Snadné otevření nativní aplikace</span><span class="sxs-lookup"><span data-stu-id="8bbba-127">Open a native app seamlessly</span></span>

<span data-ttu-id="8bbba-128">Windows, iOS a Android povolují snadnější otevření aplikací, na základě přidružení protokolu aplikace.</span><span class="sxs-lookup"><span data-stu-id="8bbba-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="8bbba-129">Pokud vaše aplikace není již nakonfigurována k tomu, aby zvládla otevírání z webového prohlížeče, budete možná potřebovat pro tuto konfiguraci vývojáře.</span><span class="sxs-lookup"><span data-stu-id="8bbba-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="8bbba-130">Pro systém Windows nahlédněte do části [Povolení aplikací pro weby s použitím obslužných rutin URI aplikace](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="8bbba-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="8bbba-131">U systému iOS nahlédněte do tématu [Univerzální odkazy pro vývojáře](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="8bbba-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="8bbba-132">U systému Android nahlédněte do části [Zpracování odkazů aplikace Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="8bbba-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="8bbba-133">Klient</span><span class="sxs-lookup"><span data-stu-id="8bbba-133">Client</span></span>                | <span data-ttu-id="8bbba-134">Otevřít v novém okně</span><span class="sxs-lookup"><span data-stu-id="8bbba-134">Open in new window</span></span> | <span data-ttu-id="8bbba-135">Otevření nativní aplikace</span><span class="sxs-lookup"><span data-stu-id="8bbba-135">Open native app</span></span> | <span data-ttu-id="8bbba-136">Otevření v rámci POS</span><span class="sxs-lookup"><span data-stu-id="8bbba-136">Open within POS</span></span> | <span data-ttu-id="8bbba-137">Podrobnosti</span><span class="sxs-lookup"><span data-stu-id="8bbba-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="8bbba-138">Moderní POS na systému Windows</span><span class="sxs-lookup"><span data-stu-id="8bbba-138">Modern POS on Windows</span></span> | <span data-ttu-id="8bbba-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="8bbba-139">✓\*</span></span>                | <span data-ttu-id="8bbba-140">✓</span><span class="sxs-lookup"><span data-stu-id="8bbba-140">✓</span></span>               | <span data-ttu-id="8bbba-141">✓</span><span class="sxs-lookup"><span data-stu-id="8bbba-141">✓</span></span>              | <span data-ttu-id="8bbba-142">\* Otevře se v novém okně Modern POS</span><span class="sxs-lookup"><span data-stu-id="8bbba-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="8bbba-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="8bbba-143">Cloud POS</span></span>             | <span data-ttu-id="8bbba-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="8bbba-144">✓\*</span></span>                | <span data-ttu-id="8bbba-145">✓</span><span class="sxs-lookup"><span data-stu-id="8bbba-145">✓</span></span>               | <span data-ttu-id="8bbba-146">X</span><span class="sxs-lookup"><span data-stu-id="8bbba-146">X</span></span>              | <span data-ttu-id="8bbba-147">\* Otevře se na nové kartě prohlížeče</span><span class="sxs-lookup"><span data-stu-id="8bbba-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="8bbba-148">Modern POS na iOS</span><span class="sxs-lookup"><span data-stu-id="8bbba-148">Modern POS on iOS</span></span>     | <span data-ttu-id="8bbba-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="8bbba-149">✓\*</span></span>                | <span data-ttu-id="8bbba-150">✓</span><span class="sxs-lookup"><span data-stu-id="8bbba-150">✓</span></span>               | <span data-ttu-id="8bbba-151">X</span><span class="sxs-lookup"><span data-stu-id="8bbba-151">X</span></span>              | <span data-ttu-id="8bbba-152">\* Otevře se na nové kartě prohlížeče</span><span class="sxs-lookup"><span data-stu-id="8bbba-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="8bbba-153">Modern POS na systému Android</span><span class="sxs-lookup"><span data-stu-id="8bbba-153">Modern POS on Android</span></span> | <span data-ttu-id="8bbba-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="8bbba-154">✓\*</span></span>                | <span data-ttu-id="8bbba-155">✓</span><span class="sxs-lookup"><span data-stu-id="8bbba-155">✓</span></span>               | <span data-ttu-id="8bbba-156">X</span><span class="sxs-lookup"><span data-stu-id="8bbba-156">X</span></span>              | <span data-ttu-id="8bbba-157">\* Otevře se na nové kartě prohlížeče</span><span class="sxs-lookup"><span data-stu-id="8bbba-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="8bbba-158">Než začnete</span><span class="sxs-lookup"><span data-stu-id="8bbba-158">Before you begin</span></span>

<span data-ttu-id="8bbba-159">Než začnete, zkontrolujte způsob konfigurace v části [Rozvržení obrazovky pro pokladní místo](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="8bbba-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="8bbba-160">Otevření URL adresy v POS</span><span class="sxs-lookup"><span data-stu-id="8bbba-160">Open URL in POS</span></span>

<span data-ttu-id="8bbba-161">Chcete-li nakonfigurovat, aby se URL adresa otevřela v pokladním místě, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="8bbba-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="8bbba-162">V ústředí přejděte na **Maloobchod a velkoobchod \> Nastavení kanálu \> Nastavení POS \> POS \> Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="8bbba-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="8bbba-163">Vyberte **Mřížky tlačítek \> Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="8bbba-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="8bbba-164">Vytvořte nové tlačítko.</span><span class="sxs-lookup"><span data-stu-id="8bbba-164">Create a new button.</span></span>
4. <span data-ttu-id="8bbba-165">Vyberte vlastnosti **tlačítka**.</span><span class="sxs-lookup"><span data-stu-id="8bbba-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="8bbba-166">Vyberte **Otevřít adresu URL** jako akci.</span><span class="sxs-lookup"><span data-stu-id="8bbba-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="8bbba-167">Zadejte adresu URL, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="8bbba-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="8bbba-168">Nakonfigurujte, zda otevřít adresu URL v novém okně.</span><span class="sxs-lookup"><span data-stu-id="8bbba-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
