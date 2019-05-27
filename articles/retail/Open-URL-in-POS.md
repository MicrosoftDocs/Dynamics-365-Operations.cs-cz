---
title: Otevření URL adresy v POS
description: Toto téma poskytuje přehled vylepšení, která byla provedena v aplikaci Microsoft Dynamics 365 for Retail ohledně funkce vyhledávání produktu a vyhledávání zákazníka.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556960"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="1a94c-103">Otevřít URL adresu v POS</span><span class="sxs-lookup"><span data-stu-id="1a94c-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a94c-104">Toto téma popisuje konfiguraci tlačítka v Retail POS pro otevření adresy URL.</span><span class="sxs-lookup"><span data-stu-id="1a94c-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="1a94c-105">Tato funkce nevyžaduje přizpůsobení kódu a může ji konfigurovat kdokoliv, i bez role vývojáře.</span><span class="sxs-lookup"><span data-stu-id="1a94c-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="1a94c-106">Tato funkce je k dispozici jako součást aplikace Dynamics 365 for Finance and Operations verze 8.1.3 (sestavení 8.1.227.10014) a novější.</span><span class="sxs-lookup"><span data-stu-id="1a94c-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="1a94c-107">Tato funkce umožňuje konfiguraci tlačítka v POS pomocí návrháře mřížky tlačítek pro otevření URL adresy.</span><span class="sxs-lookup"><span data-stu-id="1a94c-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="1a94c-108">To je v současné době podporováno v následujících konfiguracích:</span><span class="sxs-lookup"><span data-stu-id="1a94c-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="1a94c-109">Otevření v novém okně.</span><span class="sxs-lookup"><span data-stu-id="1a94c-109">Open in new window.</span></span>
- <span data-ttu-id="1a94c-110">Otevření v rámci POS.</span><span class="sxs-lookup"><span data-stu-id="1a94c-110">Open within POS.</span></span>
- <span data-ttu-id="1a94c-111">Otevření nativní aplikace.</span><span class="sxs-lookup"><span data-stu-id="1a94c-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="1a94c-112">Otevřít v novém okně</span><span class="sxs-lookup"><span data-stu-id="1a94c-112">Open in new window</span></span>

<span data-ttu-id="1a94c-113">Tato konfigurace určuje, zda má být otevřena adresa URL v novém okně nebo v rámci aplikace.</span><span class="sxs-lookup"><span data-stu-id="1a94c-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="1a94c-114">Když je webová URL adresa nakonfigurována k otevření v rámci aplikace, postranní navigační panel a horní lišta pokladního místa jsou viditelné a dostupné pro interakci uživatele.</span><span class="sxs-lookup"><span data-stu-id="1a94c-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="1a94c-115">Když je nakonfigurována k otevření v novém okně, URL adresa se otevře v novém okně aplikace na Modern POS pro Windows a na nové kartě prohlížeče ve všech ostatních klientech POS.</span><span class="sxs-lookup"><span data-stu-id="1a94c-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="1a94c-116">Chcete-li to povolit, je nutné konfigurovat adresu URL s vybranou možností **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="1a94c-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="1a94c-117">Otevření v rámci POS</span><span class="sxs-lookup"><span data-stu-id="1a94c-117">Open within POS</span></span>

<span data-ttu-id="1a94c-118">Otevření webové adresy URL v pokladním místě je momentálně podporováno pouze pro Modern POS v systému Windows.</span><span class="sxs-lookup"><span data-stu-id="1a94c-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="1a94c-119">Na dalších klientech se tato funkce vyvíjí a je plánována pro vydání v budoucích aktualizacích.</span><span class="sxs-lookup"><span data-stu-id="1a94c-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="1a94c-120">Chcete-li to povolit, je nutné konfigurovat adresu URL s nevybranou možností **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="1a94c-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="1a94c-121">Otevření nativní aplikace</span><span class="sxs-lookup"><span data-stu-id="1a94c-121">Open a native app</span></span>

<span data-ttu-id="1a94c-122">Tato funkce také umožňuje zadat newebovou adresu URL pro otevření nativní aplikace.</span><span class="sxs-lookup"><span data-stu-id="1a94c-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="1a94c-123">Můžete například určit URL protokoly, např. MailTo, SIP, IM nebo MSTEAMS, které lze pak zpracovat pomocí příslušných nativní aplikací na zařízení hostitele.</span><span class="sxs-lookup"><span data-stu-id="1a94c-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="1a94c-124">Chcete-li to povolit, je nutné konfigurovat adresu URL s vybranou možností **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="1a94c-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="1a94c-125">U počítačů se systémem Windows nahlédněte do části [Export nebo import výchozích přidružení aplikace](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) a nastavte výchozí přidružení protokolu, pokud nastavujete svůj počítač pomocí Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="1a94c-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="1a94c-126">Pokud používáte MDM, jako je například Intune, pro správu počítačů Windows, nahlédněte do [Zásady zprostředkovatele kryptografických služeb - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="1a94c-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="1a94c-127">Pokud jste vývojář vytvářející vlastní web, nahlédněte do tématu [Spuštění výchozí aplikace pro identifikátor URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="1a94c-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="1a94c-128">Snadné otevření nativní aplikace</span><span class="sxs-lookup"><span data-stu-id="1a94c-128">Open a native app seamlessly</span></span>

<span data-ttu-id="1a94c-129">Windows, iOS a Android povolují snadnější otevření aplikací, na základě přidružení protokolu aplikace.</span><span class="sxs-lookup"><span data-stu-id="1a94c-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="1a94c-130">Pokud vaše aplikace není již nakonfigurována k tomu, aby zvládla otevírání z webového prohlížeče, budete možná potřebovat pro tuto konfiguraci vývojáře.</span><span class="sxs-lookup"><span data-stu-id="1a94c-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="1a94c-131">Pro systém Windows nahlédněte do části [Povolení aplikací pro weby s použitím obslužných rutin URI aplikace](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="1a94c-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="1a94c-132">U systému iOS nahlédněte do tématu [Univerzální odkazy pro vývojáře](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="1a94c-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="1a94c-133">U systému Android nahlédněte do části [Zpracování odkazů aplikace Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="1a94c-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="1a94c-134">Klient</span><span class="sxs-lookup"><span data-stu-id="1a94c-134">Client</span></span>                | <span data-ttu-id="1a94c-135">Otevřít v novém okně</span><span class="sxs-lookup"><span data-stu-id="1a94c-135">Open in new window</span></span> | <span data-ttu-id="1a94c-136">Otevření nativní aplikace</span><span class="sxs-lookup"><span data-stu-id="1a94c-136">Open native app</span></span> | <span data-ttu-id="1a94c-137">Otevření v rámci POS</span><span class="sxs-lookup"><span data-stu-id="1a94c-137">Open within POS</span></span> | <span data-ttu-id="1a94c-138">Podrobnosti</span><span class="sxs-lookup"><span data-stu-id="1a94c-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="1a94c-139">Moderní POS na systému Windows</span><span class="sxs-lookup"><span data-stu-id="1a94c-139">Modern POS on Windows</span></span> | <span data-ttu-id="1a94c-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="1a94c-140">✓\*</span></span>                | <span data-ttu-id="1a94c-141">✓</span><span class="sxs-lookup"><span data-stu-id="1a94c-141">✓</span></span>               | <span data-ttu-id="1a94c-142">✓</span><span class="sxs-lookup"><span data-stu-id="1a94c-142">✓</span></span>              | <span data-ttu-id="1a94c-143">\* Otevře se v novém okně Modern POS</span><span class="sxs-lookup"><span data-stu-id="1a94c-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="1a94c-144">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="1a94c-144">Cloud POS</span></span>             | <span data-ttu-id="1a94c-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="1a94c-145">✓\*</span></span>                | <span data-ttu-id="1a94c-146">✓</span><span class="sxs-lookup"><span data-stu-id="1a94c-146">✓</span></span>               | <span data-ttu-id="1a94c-147">X</span><span class="sxs-lookup"><span data-stu-id="1a94c-147">X</span></span>              | <span data-ttu-id="1a94c-148">\* Otevře se na nové kartě prohlížeče</span><span class="sxs-lookup"><span data-stu-id="1a94c-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="1a94c-149">Modern POS na iOS</span><span class="sxs-lookup"><span data-stu-id="1a94c-149">Modern POS on iOS</span></span>     | <span data-ttu-id="1a94c-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="1a94c-150">✓\*</span></span>                | <span data-ttu-id="1a94c-151">✓</span><span class="sxs-lookup"><span data-stu-id="1a94c-151">✓</span></span>               | <span data-ttu-id="1a94c-152">X</span><span class="sxs-lookup"><span data-stu-id="1a94c-152">X</span></span>              | <span data-ttu-id="1a94c-153">\* Otevře se na nové kartě prohlížeče</span><span class="sxs-lookup"><span data-stu-id="1a94c-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="1a94c-154">Modern POS na systému Android</span><span class="sxs-lookup"><span data-stu-id="1a94c-154">Modern POS on Android</span></span> | <span data-ttu-id="1a94c-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="1a94c-155">✓\*</span></span>                | <span data-ttu-id="1a94c-156">✓</span><span class="sxs-lookup"><span data-stu-id="1a94c-156">✓</span></span>               | <span data-ttu-id="1a94c-157">X</span><span class="sxs-lookup"><span data-stu-id="1a94c-157">X</span></span>              | <span data-ttu-id="1a94c-158">\* Otevře se na nové kartě prohlížeče</span><span class="sxs-lookup"><span data-stu-id="1a94c-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="1a94c-159">Než začnete</span><span class="sxs-lookup"><span data-stu-id="1a94c-159">Before you begin</span></span>

<span data-ttu-id="1a94c-160">Než začnete, zkontrolujte způsob konfigurace v části [Rozvržení obrazovky pro pokladní místo](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="1a94c-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="1a94c-161">Otevření URL adresy v POS</span><span class="sxs-lookup"><span data-stu-id="1a94c-161">Open URL in POS</span></span>

<span data-ttu-id="1a94c-162">Chcete-li nakonfigurovat, aby se URL adresa otevřela v pokladním místě, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="1a94c-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="1a94c-163">V ústředí přejděte na **Maloobchod \> Nastavení kanálu \> Nastavení POS \> POS \> Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="1a94c-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="1a94c-164">Vyberte **Mřížky tlačítek \> Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="1a94c-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="1a94c-165">Vytvořte nové tlačítko.</span><span class="sxs-lookup"><span data-stu-id="1a94c-165">Create a new button.</span></span>
4. <span data-ttu-id="1a94c-166">Vyberte vlastnosti **tlačítka**.</span><span class="sxs-lookup"><span data-stu-id="1a94c-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="1a94c-167">Vyberte **Otevřít adresu URL** jako akci.</span><span class="sxs-lookup"><span data-stu-id="1a94c-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="1a94c-168">Zadejte adresu URL, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="1a94c-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="1a94c-169">Nakonfigurujte, zda otevřít adresu URL v novém okně.</span><span class="sxs-lookup"><span data-stu-id="1a94c-169">Configure whether to open the URL in a new window.</span></span>
