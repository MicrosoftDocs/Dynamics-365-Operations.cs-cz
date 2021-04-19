---
title: Práce s přednastavenými rozloženími
description: Toto téma popisuje, jak pracovat s přednastavenými rozloženími v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793914"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="73270-103">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="73270-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="73270-104">Toto téma popisuje, jak pracovat s přednastavenými rozloženími v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="73270-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="73270-105">Před dokončením postupů uvedených v tomto tématu si přečtěte [Přednastavená a vlastní rozložení](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="73270-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="73270-106">Obecný přehled naleznete v tématu [Šablony a rozvržení – přehled](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73270-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="73270-107">Vytvoření nového přednastaveného rozvržení</span><span class="sxs-lookup"><span data-stu-id="73270-107">Create a new preset layout</span></span>

<span data-ttu-id="73270-108">Existují dva způsoby vytvoření přednastaveného rozvržení.</span><span class="sxs-lookup"><span data-stu-id="73270-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="73270-109">Existující vlastní rozvržení můžete uložit jako nové přednastavené rozvržení nebo můžete vytvořit přednastavené rozvržení zcela od začátku.</span><span class="sxs-lookup"><span data-stu-id="73270-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="73270-110">Vytvoření přednastaveného rozvržení z existujícího vlastního rozložení</span><span class="sxs-lookup"><span data-stu-id="73270-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="73270-111">Chcete-li vytvořit přednastavené rozvržení z existujícího vlastního rozložení, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="73270-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="73270-112">Otevře existující stránku, která aktuálně nepoužívá přednastavené rozvržení a má strukturu modulu, kterou chcete znovu použít pro ostatní stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="73270-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="73270-113">Stránku rezervujte výběrem možnosti **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="73270-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="73270-114">Vyberte **Uložit jako nové rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="73270-114">Select **Save as new layout**.</span></span> <span data-ttu-id="73270-115">Zobrazí se dialogové okno **Uložit jako nové rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="73270-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="73270-116">Zadejte název a popis vašeho přednastavevného rozložení.</span><span class="sxs-lookup"><span data-stu-id="73270-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="73270-117">Hodnoty, které zadáte, se zobrazí ostatním autorům při vytváření nových stránek z vašeho rozvržení nebo při přepnutí na ni.</span><span class="sxs-lookup"><span data-stu-id="73270-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="73270-118">Zadejte proto hodnoty, které budou užitečné pro autory stránek.</span><span class="sxs-lookup"><span data-stu-id="73270-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="73270-119">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="73270-119">Select **OK**.</span></span>

<span data-ttu-id="73270-120">Přednastavené rozvržení bude nyní k dispozici při vytvoření nových stránek nebo při výběru jiného rozložení pro stránku ve stejné hierarchii šablon.</span><span class="sxs-lookup"><span data-stu-id="73270-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="73270-121">Chcete-li rychle zjistit, zda je určitá stránka aktuálně svázána s přednastaveným rozvržením, vyberte stránku v zobrazení seznamu stránek a zkontrolujte metadata rozvržení v podokně vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="73270-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="73270-122">Vytvoření nového přednastaveného rozvržení</span><span class="sxs-lookup"><span data-stu-id="73270-122">Create a new preset layout</span></span>

<span data-ttu-id="73270-123">Chcete-li vytvořit přednastavené rozvržení od začátku, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="73270-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="73270-124">V navigačním podokně nalevo vyberte položku **Rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="73270-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="73270-125">Vyberte **Nové rozložení**.</span><span class="sxs-lookup"><span data-stu-id="73270-125">Select **New Layout**.</span></span> <span data-ttu-id="73270-126">Zobrazí se dialogové okno **Nové rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="73270-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="73270-127">Vyberte šablonu, kterou chcete použít pro vaše přednastavené rozvržení.</span><span class="sxs-lookup"><span data-stu-id="73270-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="73270-128">Zadejte název a popis vašeho přednastavevného rozložení.</span><span class="sxs-lookup"><span data-stu-id="73270-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="73270-129">Hodnoty, které zadáte, se zobrazí ostatním autorům při vytváření nových stránek z vašeho rozvržení nebo při přepnutí na ni.</span><span class="sxs-lookup"><span data-stu-id="73270-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="73270-130">Zadejte proto hodnoty, které budou užitečné pro autory stránek.</span><span class="sxs-lookup"><span data-stu-id="73270-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="73270-131">Chcete-li vytvořit nové přednastavené rozvržení a otevřít Editor rozložení, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="73270-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="73270-132">V editoru rozložení přidejte a nakonfigurujte moduly pomocí stromu osnovy v levé části a podokna vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="73270-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="73270-133">(Proces se podobá procesu přidávání a konfigurování modulů pro šablonu v editoru šablon.) Uspořádání modulů a všechna zamknutá výchozí nastavení se stanou centralizovanou konfigurací modulu pro všechny stránky, které používají toto rozvržení přednastavených položek.</span><span class="sxs-lookup"><span data-stu-id="73270-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="73270-134">Úprava přednastaveného rozložení</span><span class="sxs-lookup"><span data-stu-id="73270-134">Modify a preset layout</span></span>

<span data-ttu-id="73270-135">Chcete-li upravit přednastavené rozvržení, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="73270-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="73270-136">V navigačním podokně nalevo vyberte položku **Rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="73270-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="73270-137">V editoru rozvržení vyberte v levém stromu osnovy modul, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="73270-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="73270-138">Potom proveďte libovolný z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="73270-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="73270-139">Chcete-li přesunout modul nahoru nebo dolů uvnitř jeho nadřazeného objektu, vyberte tlačítko se třemi tečkami (**...**) pro modul a pak vyberte **Přesunout nahoru** nebo **Přesunout dolů.**</span><span class="sxs-lookup"><span data-stu-id="73270-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="73270-140">Chcete-li změnit výchozí nastavení modulu, zadejte výchozí hodnoty pomocí podokna vlastností a volitelně je uzamkněte pro všechny podřízené stránky.</span><span class="sxs-lookup"><span data-stu-id="73270-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="73270-141">Chcete-li přidat nové moduly nebo fragmenty do modulů kontejnerů, klepněte na tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul** nebo **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="73270-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="73270-142">Chcete-li odebrat modul z rozvržení, vyberte tlačítko se třemi tečkami a pak vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="73270-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="73270-143">Změna přednastaveného motivu rozložení</span><span class="sxs-lookup"><span data-stu-id="73270-143">Change a preset layout theme</span></span>

<span data-ttu-id="73270-144">Obvyklou praxí je nastavit výchozí motiv pro všechny stránky, které používají přednastavené rozvržení.</span><span class="sxs-lookup"><span data-stu-id="73270-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="73270-145">Chcete-li nastavit nebo změnit motiv pro všechny podřízené stránky, které používají předdefinované rozvržení, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="73270-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="73270-146">V editoru rozvržení vyberte v levém stromu osnovy modul kontejneru stránky.</span><span class="sxs-lookup"><span data-stu-id="73270-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="73270-147">(Tento modul je obvykle druhým uzlem a má název **Výchozí stránka**.)</span><span class="sxs-lookup"><span data-stu-id="73270-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="73270-148">V podokně vlastností vpravo v poli **Motiv** vyberte motiv.</span><span class="sxs-lookup"><span data-stu-id="73270-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="73270-149">Uložení, navrácení se změnami, náhled a publikování přednastaveného rozvržení</span><span class="sxs-lookup"><span data-stu-id="73270-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="73270-150">Chcete-li uložit a vrátit vaše přednastavené rozvržení se změnami, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="73270-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="73270-151">V horní části editoru rozvržení vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="73270-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="73270-152">Uložené změny nemají vliv na navazující stránky, dokud nejsou vráceny se změnami.</span><span class="sxs-lookup"><span data-stu-id="73270-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="73270-153">Vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="73270-153">Select **Finish editing**.</span></span> <span data-ttu-id="73270-154">Vaše změny jsou nyní zjistitelné pro navazující workflowy.</span><span class="sxs-lookup"><span data-stu-id="73270-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="73270-155">Chcete-li zobrazit náhled změn, buď otevřete existující stránku, která používá přednastavené rozvržení, nebo vytvořte novou stránku z rozvržení.</span><span class="sxs-lookup"><span data-stu-id="73270-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="73270-156">Po zobrazení náhledu změn v rozvržení přednastavených položek můžete publikovat rozvržení na aktivním webu podle jednoho z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="73270-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="73270-157">Přejděte na **Rozvržení**, vyberte rozvržení a pak vyberte **Publikovat.**</span><span class="sxs-lookup"><span data-stu-id="73270-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="73270-158">Vyberte název rozvržení pro otevření editoru rozložení a pak vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="73270-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="73270-159">Publikujte stránku, která odkazuje na nepublikované rozvržení.</span><span class="sxs-lookup"><span data-stu-id="73270-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="73270-160">Rozvržení bude automaticky publikováno.</span><span class="sxs-lookup"><span data-stu-id="73270-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="73270-161">Na přednastavená rozvržení lze odkazovat více stránek.</span><span class="sxs-lookup"><span data-stu-id="73270-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="73270-162">Při publikování přednastaveného rozložení si uvědomte, že může být ovlivněno rozvržení více stránek.</span><span class="sxs-lookup"><span data-stu-id="73270-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73270-163">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="73270-163">Additional resources</span></span>

[<span data-ttu-id="73270-164">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="73270-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="73270-165">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="73270-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
