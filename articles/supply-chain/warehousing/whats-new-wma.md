---
title: Co je nového nebo změněného v mobilní aplikaci Warehouse Management
description: Toto téma uvádí nové a změněné funkce pro každou vydanou verzi mobilní aplikace Warehouse Management pro Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261766"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="74d9f-103">Co je nového nebo změněného v mobilní aplikaci Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="74d9f-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74d9f-104">Toto téma uvádí nové funkce, opravy, vylepšení a známé problémy pro každou vydanou verzi mobilní aplikace Warehouse Management pro Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="74d9f-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="74d9f-105">Verze 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="74d9f-106">Nové funkce, opravy a vylepšení ve verzi 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="74d9f-107">Tato verze představuje následující nové funkce, opravy a vylepšení:</span><span class="sxs-lookup"><span data-stu-id="74d9f-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="74d9f-108">Ukázkový režim nyní zobrazuje všechny štítky v jazyce zařízení.</span><span class="sxs-lookup"><span data-stu-id="74d9f-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="74d9f-109">Je méně pravděpodobné, že se zobrazí následující chybová zpráva: „Nelze najít vhodné zobrazení pro zadanou velikost.“</span><span class="sxs-lookup"><span data-stu-id="74d9f-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="74d9f-110">Minimální výška pro pracovní karty byla zvýšena (pro případy, kdy jsou v pracovním seznamu nakonfigurována tři nebo méně polí).</span><span class="sxs-lookup"><span data-stu-id="74d9f-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="74d9f-111">Okraje (vyblednutí) ve spodní části karet podrobností byly vylepšeny.</span><span class="sxs-lookup"><span data-stu-id="74d9f-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="74d9f-112">S neplatnými symboly v souborech XML, které jsou vyměňovány se serverem, se nyní pracuje elegantně.</span><span class="sxs-lookup"><span data-stu-id="74d9f-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="74d9f-113">(Například netisknutelné znaky jsou nyní řešeny elegantně a již nezpůsobují, že aplikace přestane reagovat.)</span><span class="sxs-lookup"><span data-stu-id="74d9f-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="74d9f-114">Chyby HTTP (například „chyba 503“), když je odeslán požadavek serveru, jsou nyní řešeny elegantně.</span><span class="sxs-lookup"><span data-stu-id="74d9f-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="74d9f-115">Během zobrazování chyby se seznam možností pro ovládací prvky se seznamem již automaticky nezobrazuje.</span><span class="sxs-lookup"><span data-stu-id="74d9f-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="74d9f-116">Aplikace již nepřestává reagovat kvůli orientaci displeje, která je vybrána v uživatelském nastavení.</span><span class="sxs-lookup"><span data-stu-id="74d9f-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="74d9f-117">Obrázky produktů se nyní zobrazují v samoobslužných prostředích.</span><span class="sxs-lookup"><span data-stu-id="74d9f-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="74d9f-118">(Tato změna se týká pouze verzí s nízkým rozlišením.</span><span class="sxs-lookup"><span data-stu-id="74d9f-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="74d9f-119">Služba správy souborů nepodporuje obrázky v plné velikosti v samoobslužných prostředích.)</span><span class="sxs-lookup"><span data-stu-id="74d9f-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="74d9f-120">Problém, který zahrnoval krátké výběry nulového množství, byl opraven.</span><span class="sxs-lookup"><span data-stu-id="74d9f-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="74d9f-121">Aplikace již nepřestane reagovat, když se na kartě podrobností zobrazí více identických polí.</span><span class="sxs-lookup"><span data-stu-id="74d9f-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="74d9f-122">Známé problémy ve verzi 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="74d9f-123">V této verzi existují následující známé problémy:</span><span class="sxs-lookup"><span data-stu-id="74d9f-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="74d9f-124">Aplikace (zejména pracovní seznam) se časem zpomalí.</span><span class="sxs-lookup"><span data-stu-id="74d9f-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="74d9f-125">**Verze pro Windows:** Pokud se pro skenování v systému Windows používá pistole USB, nekonzistentní výsledky způsobí, že budou naskenované symboly smíchány.</span><span class="sxs-lookup"><span data-stu-id="74d9f-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="74d9f-126">Verze 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-126">Version 2.0.5.0</span></span>

<span data-ttu-id="74d9f-127">Tato verze představuje následující nové funkce, opravy a vylepšení:</span><span class="sxs-lookup"><span data-stu-id="74d9f-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="74d9f-128">Tajný kód klienta již není v nastavení připojení skryt.</span><span class="sxs-lookup"><span data-stu-id="74d9f-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="74d9f-129">Nyní můžete dlouhým stisknutím libovolného textu zobrazit celý text.</span><span class="sxs-lookup"><span data-stu-id="74d9f-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="74d9f-130">Chybová zpráva, když chybí oprávnění úložiště, byla vylepšena.</span><span class="sxs-lookup"><span data-stu-id="74d9f-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="74d9f-131">Pro některé toky byly přidány nové kontrolní sekvence.</span><span class="sxs-lookup"><span data-stu-id="74d9f-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="74d9f-132">Tlačítko Odeslat již není nesprávně dostupné kvůli velikosti okna.</span><span class="sxs-lookup"><span data-stu-id="74d9f-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="74d9f-133">Posuvníky nyní mohou pokračovat na menších obrazovkách, když se použijí větší velikosti tlačítek.</span><span class="sxs-lookup"><span data-stu-id="74d9f-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="74d9f-134">Překrytí čtyřmi tlačítky již není oříznuto.</span><span class="sxs-lookup"><span data-stu-id="74d9f-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="74d9f-135">Klávesnice nyní podporuje tlačítko mazání.</span><span class="sxs-lookup"><span data-stu-id="74d9f-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="74d9f-136">Byl vyřešen problém s jasem, ke kterému mohlo dojít při stisknutí klávesnice.</span><span class="sxs-lookup"><span data-stu-id="74d9f-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="74d9f-137">Byly opraveny různé problémy s demo daty.</span><span class="sxs-lookup"><span data-stu-id="74d9f-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="74d9f-138">Problém, který ovlivnil číselná pole na stránce podrobností, byl opraven.</span><span class="sxs-lookup"><span data-stu-id="74d9f-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="74d9f-139">Na některých zařízeních již klávesnice na obrazovce občas nezmizí.</span><span class="sxs-lookup"><span data-stu-id="74d9f-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="74d9f-140">Byly opraveny různé chyby uživatelského rozhraní (UI), například chyby, které ovlivnily barvu pozadí a umístění.</span><span class="sxs-lookup"><span data-stu-id="74d9f-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="74d9f-141">Vylepšeno uživatelské rozhraní v ruštině.</span><span class="sxs-lookup"><span data-stu-id="74d9f-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="74d9f-142">Byly opraveny různé problémy, které způsobily, že systém přestal reagovat.</span><span class="sxs-lookup"><span data-stu-id="74d9f-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="74d9f-143">Problém související s opětovným otevřením kalkulačky byl opraven.</span><span class="sxs-lookup"><span data-stu-id="74d9f-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="74d9f-144">**Verze Android:** Problém, který způsobil, že Android 4.4 přestal reagovat při spuštění, byl opraven.</span><span class="sxs-lookup"><span data-stu-id="74d9f-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="74d9f-145">**Verze Android:** Minimální měřítko bylo sníženo na 50 procent.</span><span class="sxs-lookup"><span data-stu-id="74d9f-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="74d9f-146">Verze 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-146">Version 2.0.4.0</span></span>

<span data-ttu-id="74d9f-147">Verze 2.0.4.0 byla první obecně dostupnou verzí mobilní aplikace Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="74d9f-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="74d9f-148">Nové funkce, opravy a vylepšení ve verzi 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="74d9f-149">Tato verze zavádí následující nové funkce, opravy a vylepšení, které nebyly k dispozici ve verzi náhledu:</span><span class="sxs-lookup"><span data-stu-id="74d9f-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="74d9f-150">Pokud karta s podrobnostmi obsahuje dva štítky, které mají stejná data, jeden z štítků je skrytý.</span><span class="sxs-lookup"><span data-stu-id="74d9f-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="74d9f-151">Ve výchozím nastavení se nyní zobrazují speciální znaky a možnost jejich skrytí byla z uživatelského nastavení odstraněna.</span><span class="sxs-lookup"><span data-stu-id="74d9f-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="74d9f-152">Zakázaná tlačítka pro odeslání se nyní zobrazují jako nedostupná v kompaktním pohledu z ruky.</span><span class="sxs-lookup"><span data-stu-id="74d9f-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="74d9f-153">Změna logiky sekvenování pro ovládací prvky zajišťuje plynulejší škálování napříč zařízeními.</span><span class="sxs-lookup"><span data-stu-id="74d9f-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="74d9f-154">Proto není nutné upravovat měřítko písem nebo tlačítek.</span><span class="sxs-lookup"><span data-stu-id="74d9f-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="74d9f-155">Výchozí barevný motiv byl změněn na *Tmavý*.</span><span class="sxs-lookup"><span data-stu-id="74d9f-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="74d9f-156">V zobrazení pásu karet byla přidána chybějící ikona pro deaktivované tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="74d9f-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="74d9f-157">Výjimky vypršení časového limitu vás nyní místo zobrazení in-line chyby přenesou na stránku připojení.</span><span class="sxs-lookup"><span data-stu-id="74d9f-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="74d9f-158">Pokud není k dispozici žádná akce pro odeslání (např **OK**, **Ano**, **Akceptovat**, **Hotovo** nebo **Dokončeno**), tlačítko Odeslat bude deaktivováno.</span><span class="sxs-lookup"><span data-stu-id="74d9f-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="74d9f-159">Byla vylepšena stabilita aplikace.</span><span class="sxs-lookup"><span data-stu-id="74d9f-159">App stability has been improved.</span></span>
- <span data-ttu-id="74d9f-160">Je opravena chyba zabezpečení [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="74d9f-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="74d9f-161">**Verze pro Windows:** Problém ve Windows, kdy nabídky nereagovaly po změně velikosti okna, byl opraven.</span><span class="sxs-lookup"><span data-stu-id="74d9f-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="74d9f-162">Známý problém ve verzi 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="74d9f-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="74d9f-163">V této verzi existuje následující známý problém:</span><span class="sxs-lookup"><span data-stu-id="74d9f-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="74d9f-164">Tato verze má problém se zařízeními, která používají Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="74d9f-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="74d9f-165">Při používání aplikace s touto verzí Android se mohou vyskytnout problémy.</span><span class="sxs-lookup"><span data-stu-id="74d9f-165">You might experience issues when you use the app on this Android version.</span></span>
