---
title: Práce se soubory přepisu CSS
description: Toto téma vysvětluje proč, kdy a jak používat soubory přepisu šablon Cascading Style Sheets (CSS) v produktu Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 41fb0be51f7af25faba1b860319aea84ae7a8b56
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207792"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="bec16-103">Práce s CSS soubory přepisující výchozí styl</span><span class="sxs-lookup"><span data-stu-id="bec16-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bec16-104">Toto téma vysvětluje proč, kdy a jak používat soubory přepisu šablon Cascading Style Sheets (CSS) v produktu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bec16-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bec16-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="bec16-105">Overview</span></span>

<span data-ttu-id="bec16-106">Trvalé styly webu by obvykle měly být zpracovávány prostřednictvím motivu webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="bec16-107">Motivy poskytují základní nastavení šablon CSS a stylu pro moduly na libovolné stránce webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="bec16-108">Motivy jsou vytvářeny pomocí sady SDK Dynamics 365 Commerce (Software Development Kit) online a jsou nasazeny na vaše weby prostřednictvím aplikace Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bec16-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="bec16-109">Možnosti ladění motivu a konfigurace rozhraní modulu v sadě SDK usnadňují vývojářům webu vytváření upravitelných a kohezivních balíčků návrhu webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="bec16-110">Pokud jsou tyto balíčky návrhu nasazeny na web, mohou se autoři webu zaměřit na vytváření, úpravy a publikování obsahu namísto vývoje webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="bec16-111">Vzhledem k obvyklému životním cyklu motivu může být závislost na tom, aby vývojáři prováděli změny stylu prostřednictvím kanálu nasazení SDK a LCS, v některých scénářích příliš vysoká.</span><span class="sxs-lookup"><span data-stu-id="bec16-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="bec16-112">Prototypy nebo opravy hotfix webů se mohou zdát těžko ovladatelné, pokud není konfigurovaná sada SDK nebo pokud nemáte čas čekat na nasazení LCS.</span><span class="sxs-lookup"><span data-stu-id="bec16-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="bec16-113">V těchto scénářích mohou pomoci soubory přepisu CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="bec16-114">V nástrojích pro vytváření obchodních dat mohou ověření uživatelé odeslat soubor CSS, zobrazit jeho náhled a potom jej aktivovat, aby přepsal motiv webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="bec16-115">Nejsou nutné režijní náklady nasazení SDK nebo LCS.</span><span class="sxs-lookup"><span data-stu-id="bec16-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="bec16-116">Přepisy, které jsou zadány v souboru přepisu CSS mohou být stejně malé jako změna jednoho stylu textu nebo rozsáhlé jako úplná revize značky.</span><span class="sxs-lookup"><span data-stu-id="bec16-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="bec16-117">Před použitím souborů přepisu CSS je třeba mít na zřeteli následující omezení:</span><span class="sxs-lookup"><span data-stu-id="bec16-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="bec16-118">Na webu může být aktivní vždy pouze jeden soubor přepisu CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="bec16-119">Proto musí být všechny aktivní přepisy přítomny v jediném souboru přepisu.</span><span class="sxs-lookup"><span data-stu-id="bec16-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="bec16-120">Přestože můžete zobrazit náhled přepisů v nástrojích pro vytváření Commerce, nejsou k dispozici žádné vyhrazené funkce ladění, které by pomohly identifikovat chyby, jsou zavedeny při přepisech.</span><span class="sxs-lookup"><span data-stu-id="bec16-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="bec16-121">Jinými slovy, pokud použijete soubory přepisu CSS, nemáte stejnou sadu nástrojů, kterou sada SDK poskytuje pro modul a pro ověření obsahu.</span><span class="sxs-lookup"><span data-stu-id="bec16-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="bec16-122">Soubory přepisu CSS však poskytují rychlý způsob navržení prototypu designu nebo implementace opravy hotfix před vyvinutím a nasazením aktualizace celého motivu.</span><span class="sxs-lookup"><span data-stu-id="bec16-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="bec16-123">Vytvoření souboru přepisu CSS</span><span class="sxs-lookup"><span data-stu-id="bec16-123">Create a CSS override file</span></span>

<span data-ttu-id="bec16-124">Chcete-li vytvořit soubor přepisu CSS, můžete použít jakékoli integrované vývojové prostředí (IDE), textový editor nebo editor zdrojového kódu.</span><span class="sxs-lookup"><span data-stu-id="bec16-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="bec16-125">Typickým přístupem je použití standardních webových souborů ladění v prohlížeči k identifikaci selektorů, vlastností a hodnot stylu na existujícím webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="bec16-126">Většina prohlížečů umožňuje měnit hodnoty a zobrazovat jejich náhled v nástroji ladění.</span><span class="sxs-lookup"><span data-stu-id="bec16-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="bec16-127">Po identifikaci změn, které chcete provést, můžete tyto změny uložit do vlastního souboru CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="bec16-128">Odeslání souboru přepisu CSS</span><span class="sxs-lookup"><span data-stu-id="bec16-128">Upload a CSS override file</span></span>

<span data-ttu-id="bec16-129">Pokud chcete odeslat soubor CSS na svůj web v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bec16-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bec16-130">Ve nástrojích pro tvorbu obsahu přejděte na svůj web.</span><span class="sxs-lookup"><span data-stu-id="bec16-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="bec16-131">V navigačním podokně nalevo vyberte položku **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="bec16-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bec16-132">V závislosti na verzi nástrojů pro vytváření obchodních dokumentů, kterou používáte, bude pravděpodobně nutné rozbalit **Nastavení** v navigačním podokně, aby bylo možné vybrat **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="bec16-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="bec16-133">V horní části hlavního podokna návrhu vyberte kartu **Přepis CSS**, pokud již není vybraná.</span><span class="sxs-lookup"><span data-stu-id="bec16-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="bec16-134">V části **Dostupné přepisy CSS** vyberte **Nahrát soubor CSS**.</span><span class="sxs-lookup"><span data-stu-id="bec16-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="bec16-135">Zobrazí se okno průzkumníka souborů.</span><span class="sxs-lookup"><span data-stu-id="bec16-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="bec16-136">V Průzkumníku souborů vyhledejte a vyberte soubor CSS a pak vyberte **otevřít**.</span><span class="sxs-lookup"><span data-stu-id="bec16-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="bec16-137">Nahraný soubor CSS se nyní zobrazí v části **Dostupné přepisy CSS**.</span><span class="sxs-lookup"><span data-stu-id="bec16-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="bec16-138">Náhled souboru přepisu CSS</span><span class="sxs-lookup"><span data-stu-id="bec16-138">Preview a CSS override file</span></span>

<span data-ttu-id="bec16-139">Chcete-li zobrazit náhled CSS před tím, než soubor na aktivním webu aktivujete, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="bec16-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="bec16-140">V navigačním podokně vlevo vyberte **Návrh** a na kartě **Přepis CSS** v části **Dostupné přepisy CSS** vyhledejte soubor CSS, jehož náhled chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="bec16-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="bec16-141">Vedle názvu souboru CSS vyberte **Web náhledu**.</span><span class="sxs-lookup"><span data-stu-id="bec16-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="bec16-142">V dialogovém okně **Vybrat adresu URL** vyberte adresu URL webu, na němž chcete zobrazit použitý přepis, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bec16-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="bec16-143">Pokud pro vybranou adresu URL existuje více variant, vyberte požadovanou variantu v dialogovém okně **Varianty návrhu**, které se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="bec16-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="bec16-144">Otevře se nová karta nebo okno prohlížeče, kde můžete ověřit přepisy stylu vůči webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="bec16-145">Potom můžete tuto adresu URL sdílet s jinými ověřenými uživateli Commerce pro kontrolu a zpětnou vazbu.</span><span class="sxs-lookup"><span data-stu-id="bec16-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="bec16-146">Aktivace souboru přepisu CSS na živém webu</span><span class="sxs-lookup"><span data-stu-id="bec16-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="bec16-147">Poté, co jste zobrazili náhled souboru přepisu CSS a schválili ho, můžete ho aktivovat na živém webu.</span><span class="sxs-lookup"><span data-stu-id="bec16-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="bec16-148">Na webu může být aktivní vždy pouze jeden soubor přepisu CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="bec16-149">Pokud aktivujete nový soubor přepisu, předchozí soubor přepisu je deaktivován.</span><span class="sxs-lookup"><span data-stu-id="bec16-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="bec16-150">Proto se ujistěte, že jsou všechny požadované přepisy přítomny v jednom souboru přepisu CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="bec16-151">Pokud chcete aktivovat soubor přepisu CSS, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="bec16-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="bec16-152">V navigačním podokně vlevo vyberte **Návrh** a na kartě **Přepis CSS** v části **Dostupné přepisy CSS** vyhledejte soubor CSS, jehož náhled chcete aktivovat.</span><span class="sxs-lookup"><span data-stu-id="bec16-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="bec16-153">Pod názvem souboru CSS vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="bec16-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="bec16-154">Soubor přepisu se okamžitě na vašem webu okamžitě aktivuje.</span><span class="sxs-lookup"><span data-stu-id="bec16-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="bec16-155">Deaktivace souboru přepisu CSS na živém webu</span><span class="sxs-lookup"><span data-stu-id="bec16-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="bec16-156">Chcete-li deaktivovat soubor přepisu CSS na vašem webu, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bec16-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="bec16-157">V navigačním podokně vlevo vyberte **Návrh** a na kartě **Přepis CSS** v části **Dostupné přepisy CSS** vyhledejte soubor CSS, jehož náhled chcete deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="bec16-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="bec16-158">Pod názvem souboru CSS vyberte **Deaktivovat**.</span><span class="sxs-lookup"><span data-stu-id="bec16-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="bec16-159">Soubor přepisu se okamžitě na vašem webu okamžitě deaktivuje.</span><span class="sxs-lookup"><span data-stu-id="bec16-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="bec16-160">Chcete-li získat přístup k dalším možnostem souborů přepisu CSS, vyberte tři tečky (**...**) vedle názvu souboru CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="bec16-161">Možnosti **Stáhnout**, **Přejmenovat** a **Nahradit** jsou užitečné pro rychlé změny stávajícího souboru přepisu CSS.</span><span class="sxs-lookup"><span data-stu-id="bec16-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bec16-162">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="bec16-162">Additional resources</span></span>

[<span data-ttu-id="bec16-163">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="bec16-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="bec16-164">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="bec16-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="bec16-165">Práce s předvolbami stylu</span><span class="sxs-lookup"><span data-stu-id="bec16-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="bec16-166">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="bec16-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="bec16-167">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="bec16-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="bec16-168">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="bec16-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="bec16-169">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="bec16-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="bec16-170">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="bec16-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]