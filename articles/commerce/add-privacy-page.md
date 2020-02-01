---
title: Přidání stránky se zásadami ochrany osobních údajů
description: Toto téma popisuje, jak přidat stránku se zásadami ochrany osobních údajů na web v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945983"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="7efa4-103">Přidání stránky se zásadami ochrany osobních údajů</span><span class="sxs-lookup"><span data-stu-id="7efa4-103">Add a privacy policy page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7efa4-104">Toto téma popisuje, jak přidat stránku se zásadami ochrany osobních údajů na web v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7efa4-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7efa4-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="7efa4-105">Overview</span></span>

<span data-ttu-id="7efa4-106">Soulad s ochranou osobních údajů zahrnuje organizační opatření, která uživatele webu informují o způsobu sběru a zpracování jejich dat.</span><span class="sxs-lookup"><span data-stu-id="7efa4-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="7efa4-107">Uživatelé se pak mohou rozhodnout, jak budou chtít zpracovat své osobní údaje, a mohou podniknout příslušné kroky.</span><span class="sxs-lookup"><span data-stu-id="7efa4-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="7efa4-108">Projděte si prohlášení společnosti Microsoft o zásadách ochrany osobních údajů v Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7efa4-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="7efa4-109">Pokud se chcete podívat na prohlášení o ochraně osobních údajů společnosti Microsoft, když jste přihlášení do vývojových nástrojů Dynamics 365 Commerce, klikněte na tlačítko **Nápověda** (**?**) v pravém horním rohu a pak vyberte **Zásady ochrany osobních údajů a soubory cookie**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="7efa4-110">Otevře se nová záložka, která obsahuje odkaz na [prohlášení o ochraně osobních údajů společnosti Microsoft](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="7efa4-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="7efa4-111">Vytvoření stránky zásad ochrany osobních údajů pro váš web</span><span class="sxs-lookup"><span data-stu-id="7efa4-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="7efa4-112">V aplikaci Dynamics 365 Commerce existuje několik způsobů, jak poskytnout uživatelům přístup k vašim zásadám ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="7efa4-113">V této části je uveden postup vytvoření stránky zásad ochrany osobních údajů a následné odkazování na stránku pomocí fragmentu zápatí.</span><span class="sxs-lookup"><span data-stu-id="7efa4-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="7efa4-114">Následující pokyny ukazují, jak vytvořit obecnou stránku zásad ochrany osobních údajů pro web Commerce.</span><span class="sxs-lookup"><span data-stu-id="7efa4-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="7efa4-115">Jste zodpovědní za navržení a implementaci řešení stránky zásad ochrany osobních údajů, které nejlépe odpovídá právním požadavkům vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="7efa4-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="7efa4-116">Chcete-li začít, přejděte ve vývojových nástrojích na web, pro který chcete vytvořit stránku zásad ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="7efa4-117">Vytvořit šablonu</span><span class="sxs-lookup"><span data-stu-id="7efa4-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="7efa4-118">Pokud šablona, kterou lze použít pro stránku zásad ochrany osobních údajů, již byla vytvořena, přeskočte na část [Vytvoření stránky zásad ochrany osobních údajů](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="7efa4-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="7efa4-119">Při vytváření šablony postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7efa4-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="7efa4-120">Přejděte na **Šablony \> Nová šablona**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="7efa4-121">Zadejte název šablony a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="7efa4-122">V šabloně přidejte všechny požadované moduly do požadovaných úseků stránky.</span><span class="sxs-lookup"><span data-stu-id="7efa4-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="7efa4-123">Pokud chcete získat pokyny, najeďte ukazatelem myši na červené vykřičníky.</span><span class="sxs-lookup"><span data-stu-id="7efa4-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="7efa4-124">Úsek **Záhlaví HTML** může například vyžadovat modul **Výchozí externí skript**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="7efa4-125">Do úseku **Tělo** přidejte modul **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="7efa4-126">V modulu **Výchozí stránka** v úseku **Hlavní** přidejte modul **Blok s formátovaným obsahem**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="7efa4-127">Do modulu **Blok s formátovaným obsahem** přidejte modul **Položka bloku s formátovaným obsahem**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="7efa4-128">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="7efa4-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="7efa4-129">Sestavení stránky se zásadami ochrany osobních údajů</span><span class="sxs-lookup"><span data-stu-id="7efa4-129">Build a privacy policy page</span></span>

<span data-ttu-id="7efa4-130">Chcete-li vytvořit stránku se zásadami ochrany osobních údajů, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="7efa4-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="7efa4-131">Přejděte na **Stránky \> Nová stránka**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="7efa4-132">Vyberte šablonu pro stránku zásad ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="7efa4-133">Zadejte název a adresu URL šablony a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="7efa4-134">V pozici **Hlavní** na nové stránce přidejte modul **Blok s formátovaným obsahem**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="7efa4-135">Do modulu **Blok s formátovaným obsahem** přidejte modul **Položka bloku s formátovaným obsahem**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="7efa4-136">V podokně vlastností modulu **Blok s formátovaným obsahem** vyberte **Přidat zdroj dat** a pak vyberte **obsah ve formátu RTF**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="7efa4-137">V editoru formátovaného textu zadejte obsah stránky zásad ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="7efa4-138">Podle potřeby rozbalte Editor RTF do režimu celé obrazovky.</span><span class="sxs-lookup"><span data-stu-id="7efa4-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="7efa4-139">Po dokončení zadávání obsahu vyberte **náhled** k zobrazení náhledu stránky ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="7efa4-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="7efa4-140">Dokončete všechny zbývající dodatky k vlastnostem stránky a modulů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="7efa4-141">Vraťte stránku se zásadami ochrany osobních údajů a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="7efa4-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="7efa4-142">Chcete-li publikovat adresu URL pro stránku zásad ochrany osobních údajů, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="7efa4-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="7efa4-143">Přejděte na **Adresy URL** a vyberte adresu URL stránky zásady ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="7efa4-144">Publikujte vybranou adresu URL.</span><span class="sxs-lookup"><span data-stu-id="7efa4-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="7efa4-145">Vytvoření odkazu na stránku zásad ochrany osobních údajů v zápatí</span><span class="sxs-lookup"><span data-stu-id="7efa4-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="7efa4-146">Do fragmentu můžete přidat odkaz na stránku zásad ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="7efa4-147">Tímto způsobem můžete odkaz sdílet a aktualizovat na více stránkách webu pomocí odkazu na fragment.</span><span class="sxs-lookup"><span data-stu-id="7efa4-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="7efa4-148">Tento příklad ukazuje, jak přidat odkaz na stránku zásad ochrany osobních údajů do fragmentu zápatí.</span><span class="sxs-lookup"><span data-stu-id="7efa4-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="7efa4-149">Chcete-li přidat odkaz na fragment zápatí, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7efa4-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="7efa4-150">Přejděte na **Fragmenty stránky \> Nový fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="7efa4-151">Vyberte modul **zápatí** a pak zadejte název do pole **Název fragmentu stránky**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="7efa4-152">Do úseku **Kategorie zápatí** přidejte modul **Položka zápatí**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="7efa4-153">V podokně vlastností vpravo vyberte možnost **Text odkazu**.</span><span class="sxs-lookup"><span data-stu-id="7efa4-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="7efa4-154">V dialogovém okně **Text odkazu** zadejte text odkazu a cíl odkazu na stránce Zásady ochrany osobních údajů a klikněte na tlačítko **OK.**</span><span class="sxs-lookup"><span data-stu-id="7efa4-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="7efa4-155">Chcete-li získat adresu URL stránky zásad ochrany osobních údajů, přejděte na **Stránky**, přejděte na stránku zásady ochrany osobních údajů a zkopírujte adresu URL z podokna vlastností.</span><span class="sxs-lookup"><span data-stu-id="7efa4-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="7efa4-156">Uložte fragment stránky, vraťte jej se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="7efa4-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="7efa4-157">Zobrazte náhled fragmentu a otestujte odkaz na stránku zásad ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="7efa4-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="7efa4-158">Na fragment lze nyní odkazovat v šabloně pro jiné stránky webu.</span><span class="sxs-lookup"><span data-stu-id="7efa4-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="7efa4-159">Pokud je na tento fragment odkazováno v modulu **Zápatí** šablony, reference odkazu se zobrazí na všech stránkách, které jsou vytvořeny pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="7efa4-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7efa4-160">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7efa4-160">Additional resources</span></span>

[<span data-ttu-id="7efa4-161">Přehled dodržování předpisů</span><span class="sxs-lookup"><span data-stu-id="7efa4-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="7efa4-162">Funkce a možnosti usnadnění přístupu</span><span class="sxs-lookup"><span data-stu-id="7efa4-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="7efa4-163">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="7efa4-163">Cookie compliance</span></span>](cookie-compliance.md)