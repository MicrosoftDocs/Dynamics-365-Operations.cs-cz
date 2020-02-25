---
title: Práce s přednastavenými rozloženími
description: Toto téma popisuje, jak pracovat s přednastavenými rozloženími v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c8149c6e443c77dabfa641a698c931176bedbc98
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002629"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="a410c-103">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="a410c-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a410c-104">Toto téma popisuje, jak pracovat s přednastavenými rozloženími v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a410c-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a410c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="a410c-105">Overview</span></span>

<span data-ttu-id="a410c-106">Před dokončením postupů uvedených v tomto tématu si přečtěte [Přednastavená a vlastní rozložení](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="a410c-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="a410c-107">Obecný přehled naleznete v tématu [Šablony a rozvržení – přehled](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a410c-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="a410c-108">Vytvoření nového přednastaveného rozvržení</span><span class="sxs-lookup"><span data-stu-id="a410c-108">Create a new preset layout</span></span>

<span data-ttu-id="a410c-109">Existují dva způsoby vytvoření přednastaveného rozvržení.</span><span class="sxs-lookup"><span data-stu-id="a410c-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="a410c-110">Existující vlastní rozvržení můžete uložit jako nové přednastavené rozvržení nebo můžete vytvořit přednastavené rozvržení zcela od začátku.</span><span class="sxs-lookup"><span data-stu-id="a410c-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="a410c-111">Vytvoření přednastaveného rozvržení z existujícího vlastního rozložení</span><span class="sxs-lookup"><span data-stu-id="a410c-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="a410c-112">Chcete-li vytvořit přednastavené rozvržení z existujícího vlastního rozložení, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a410c-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="a410c-113">Otevře existující stránku, která aktuálně nepoužívá přednastavené rozvržení a má strukturu modulu, kterou chcete znovu použít pro ostatní stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="a410c-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="a410c-114">Vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="a410c-114">Select **Check out**.</span></span>
1. <span data-ttu-id="a410c-115">Vyberte **Uložit jako nové rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="a410c-115">Select **Save as new layout**.</span></span> <span data-ttu-id="a410c-116">Zobrazí se dialogové okno **Uložit jako nové rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="a410c-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="a410c-117">Zadejte název a popis vašeho přednastavevného rozložení.</span><span class="sxs-lookup"><span data-stu-id="a410c-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="a410c-118">Hodnoty, které zadáte, se zobrazí ostatním autorům při vytváření nových stránek z vašeho rozvržení nebo při přepnutí na ni.</span><span class="sxs-lookup"><span data-stu-id="a410c-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="a410c-119">Zadejte proto hodnoty, které budou užitečné pro autory stránek.</span><span class="sxs-lookup"><span data-stu-id="a410c-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="a410c-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a410c-120">Select **OK**.</span></span>

<span data-ttu-id="a410c-121">Přednastavené rozvržení bude nyní k dispozici při vytvoření nových stránek nebo při výběru jiného rozložení pro stránku ve stejné hierarchii šablon.</span><span class="sxs-lookup"><span data-stu-id="a410c-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="a410c-122">Chcete-li rychle zjistit, zda je určitá stránka aktuálně svázána s přednastaveným rozvržením, vyberte stránku v zobrazení seznamu stránek a zkontrolujte metadata rozvržení v podokně vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="a410c-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="a410c-123">Vytvoření nového přednastaveného rozvržení</span><span class="sxs-lookup"><span data-stu-id="a410c-123">Create a new preset layout</span></span>

<span data-ttu-id="a410c-124">Chcete-li vytvořit přednastavené rozvržení od začátku, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a410c-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="a410c-125">V navigačním podokně nalevo vyberte položku **Rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="a410c-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="a410c-126">Vyberte **Nové rozložení**.</span><span class="sxs-lookup"><span data-stu-id="a410c-126">Select **New Layout**.</span></span> <span data-ttu-id="a410c-127">Zobrazí se dialogové okno **Nové rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="a410c-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="a410c-128">Vyberte šablonu, kterou chcete použít pro vaše přednastavené rozvržení.</span><span class="sxs-lookup"><span data-stu-id="a410c-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="a410c-129">Zadejte název a popis vašeho přednastavevného rozložení.</span><span class="sxs-lookup"><span data-stu-id="a410c-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="a410c-130">Hodnoty, které zadáte, se zobrazí ostatním autorům při vytváření nových stránek z vašeho rozvržení nebo při přepnutí na ni.</span><span class="sxs-lookup"><span data-stu-id="a410c-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="a410c-131">Zadejte proto hodnoty, které budou užitečné pro autory stránek.</span><span class="sxs-lookup"><span data-stu-id="a410c-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="a410c-132">Chcete-li vytvořit nové přednastavené rozvržení a otevřít Editor rozložení, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a410c-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="a410c-133">V editoru rozložení přidejte a nakonfigurujte moduly pomocí stromu osnovy v levé části a podokna vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="a410c-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="a410c-134">(Proces se podobá procesu přidávání a konfigurování modulů pro šablonu v editoru šablon.) Uspořádání modulů a všechna zamknutá výchozí nastavení se stanou centralizovanou konfigurací modulu pro všechny stránky, které používají toto rozvržení přednastavených položek.</span><span class="sxs-lookup"><span data-stu-id="a410c-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="a410c-135">Úprava přednastaveného rozložení</span><span class="sxs-lookup"><span data-stu-id="a410c-135">Modify a preset layout</span></span>

<span data-ttu-id="a410c-136">Chcete-li upravit přednastavené rozvržení, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a410c-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="a410c-137">V navigačním podokně nalevo vyberte položku **Rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="a410c-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="a410c-138">V editoru rozvržení vyberte v levém stromu osnovy modul, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="a410c-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="a410c-139">Potom proveďte libovolný z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="a410c-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="a410c-140">Chcete-li přesunout modul nahoru nebo dolů uvnitř jeho nadřazeného objektu, vyberte tlačítko se třemi tečkami (**...**) pro modul a pak vyberte **Přesunout nahoru** nebo **Přesunout dolů.**</span><span class="sxs-lookup"><span data-stu-id="a410c-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="a410c-141">Chcete-li změnit výchozí nastavení modulu, zadejte výchozí hodnoty pomocí podokna vlastností a volitelně je uzamkněte pro všechny podřízené stránky.</span><span class="sxs-lookup"><span data-stu-id="a410c-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="a410c-142">Chcete-li přidat nové moduly nebo fragmenty do modulů kontejnerů, klepněte na tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul** nebo **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="a410c-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="a410c-143">Chcete-li odebrat modul z rozvržení, vyberte tlačítko se třemi tečkami a pak vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="a410c-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="a410c-144">Změna přednastaveného motivu rozložení</span><span class="sxs-lookup"><span data-stu-id="a410c-144">Change a preset layout theme</span></span>

<span data-ttu-id="a410c-145">Obvyklou praxí je nastavit výchozí motiv pro všechny stránky, které používají přednastavené rozvržení.</span><span class="sxs-lookup"><span data-stu-id="a410c-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="a410c-146">Chcete-li nastavit nebo změnit motiv pro všechny podřízené stránky, které používají předdefinované rozvržení, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a410c-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="a410c-147">V editoru rozvržení vyberte v levém stromu osnovy modul kontejneru stránky.</span><span class="sxs-lookup"><span data-stu-id="a410c-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="a410c-148">(Tento modul je obvykle druhým uzlem a má název **Výchozí stránka**.)</span><span class="sxs-lookup"><span data-stu-id="a410c-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="a410c-149">V podokně vlastností vpravo v poli **Motiv** vyberte motiv.</span><span class="sxs-lookup"><span data-stu-id="a410c-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="a410c-150">Uložení, navrácení se změnami, náhled a publikování přednastaveného rozvržení</span><span class="sxs-lookup"><span data-stu-id="a410c-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="a410c-151">Chcete-li uložit a vrátit vaše přednastavené rozvržení se změnami, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a410c-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="a410c-152">V horní části editoru rozvržení vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a410c-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="a410c-153">Uložené změny nemají vliv na navazující stránky, dokud nejsou vráceny se změnami.</span><span class="sxs-lookup"><span data-stu-id="a410c-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="a410c-154">Vyberte **Vrátit se změnami**.</span><span class="sxs-lookup"><span data-stu-id="a410c-154">Select **Check In**.</span></span> <span data-ttu-id="a410c-155">Vaše změny jsou nyní zjistitelné pro navazující workflowy.</span><span class="sxs-lookup"><span data-stu-id="a410c-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="a410c-156">Chcete-li zobrazit náhled změn, buď otevřete existující stránku, která používá přednastavené rozvržení, nebo vytvořte novou stránku z rozvržení.</span><span class="sxs-lookup"><span data-stu-id="a410c-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="a410c-157">Po zobrazení náhledu změn v rozvržení přednastavených položek můžete publikovat rozvržení na aktivním webu podle jednoho z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="a410c-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="a410c-158">Přejděte na **Rozvržení**, vyberte rozvržení a pak vyberte **Publikovat.**</span><span class="sxs-lookup"><span data-stu-id="a410c-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="a410c-159">V editoru rozvržení vyberte možnost **Publikovat.**</span><span class="sxs-lookup"><span data-stu-id="a410c-159">In the layout editor, select **Publish**.</span></span>
* <span data-ttu-id="a410c-160">Publikujte stránku, která odkazuje na nepublikované rozvržení.</span><span class="sxs-lookup"><span data-stu-id="a410c-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="a410c-161">Rozvržení bude automaticky publikováno.</span><span class="sxs-lookup"><span data-stu-id="a410c-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="a410c-162">Na přednastavená rozvržení lze odkazovat více stránek.</span><span class="sxs-lookup"><span data-stu-id="a410c-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="a410c-163">Při publikování přednastaveného rozložení si uvědomte, že může být ovlivněno rozvržení více stránek.</span><span class="sxs-lookup"><span data-stu-id="a410c-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a410c-164">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a410c-164">Additional resources</span></span>

[<span data-ttu-id="a410c-165">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="a410c-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a410c-166">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="a410c-166">Work with templates</span></span>](work-with-templates.md)
