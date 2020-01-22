---
title: Práce s fragmenty
description: V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914693"
---
# <a name="work-with-fragments"></a><span data-ttu-id="c9677-103">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="c9677-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c9677-104">V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9677-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9677-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="c9677-105">Overview</span></span>

<span data-ttu-id="c9677-106">Fragmenty umožňují centralizované prostředí pro vytváření konfigurací modulu, které je nutné znovu použít v celém webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="c9677-107">Například záhlaví, zápatí a nápisy jsou často konfigurovány jako fragmenty, protože jsou sdíleny na více stránkách.</span><span class="sxs-lookup"><span data-stu-id="c9677-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="c9677-108">Fragmenty lze považovat za miniaturní webové stránky, které lze vložit do jiných stránek na vašem webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="c9677-109">Fragmenty mají vlastní životní cyklus.</span><span class="sxs-lookup"><span data-stu-id="c9677-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="c9677-110">Jinými slovy, jsou vytvořeny, odkazovány, aktualizovány a odstraněny jako nezávislé entity ve vývojových nástrojích.</span><span class="sxs-lookup"><span data-stu-id="c9677-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="c9677-111">Po dokončení konfigurace fragmentů lze použít všechny moduly, které mohou být použity ve struktuře webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="c9677-112">Fragmenty mohou odkazovat na stránkách, v rozvržení, v šablonách a v jiných fragmentech.</span><span class="sxs-lookup"><span data-stu-id="c9677-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="c9677-113">Fragmenty mohou být vnořeny do sedmi úrovní v jiných fragmentech.</span><span class="sxs-lookup"><span data-stu-id="c9677-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="c9677-114">Chcete-li například propagovat velké množství stránek na více stránkách na našem webu, můžete použít fragment.</span><span class="sxs-lookup"><span data-stu-id="c9677-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="c9677-115">Prvním krokem při vytváření nového fragmentu je výběr typu modulu, ze kterého chcete začít.</span><span class="sxs-lookup"><span data-stu-id="c9677-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="c9677-116">V tomto příkladu můžete vytvořit fragment z modulu Hero.</span><span class="sxs-lookup"><span data-stu-id="c9677-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="c9677-117">Fragmenty mohou být vytvořeny z libovolného typu modulu.</span><span class="sxs-lookup"><span data-stu-id="c9677-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="c9677-118">Poté můžete nakonfigurovat fragment Hero s konkrétním reklamním obsahem.</span><span class="sxs-lookup"><span data-stu-id="c9677-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="c9677-119">Můžete jej také lokalizovat podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="c9677-119">You can also localize it as you require.</span></span> <span data-ttu-id="c9677-120">Nový fragment Hero může být poté spotřebován jako předkonfigurovaný modul na vašem webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="c9677-121">Lze jej snadno přidat do šablon, na určité stránky nebo do jiných fragmentů, které mohou obsahovat Hero moduly.</span><span class="sxs-lookup"><span data-stu-id="c9677-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="c9677-122">Všechna místa, kde je fragment přidán, jsou odkazy na vytvořený centrální fragment Hero.</span><span class="sxs-lookup"><span data-stu-id="c9677-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="c9677-123">Pokud publikujete změny ve fragmentu, tyto změny se okamžitě projeví ve všech místech, kde je fragment odkazován na celém webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="c9677-124">Proto fragmenty poskytují výkonný a účinný prostředek pro opětovné použití a centrální správu konfigurací modulů na pracovišti.</span><span class="sxs-lookup"><span data-stu-id="c9677-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="c9677-125">Pomocí těchto funkcí můžete významně zvýšit pružnost a snížit náklady, které jsou spojeny s řízením obsahu webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="c9677-126">Na následujícím obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9677-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Na obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="c9677-128">Vytvořit fragment</span><span class="sxs-lookup"><span data-stu-id="c9677-128">Create a fragment</span></span>

<span data-ttu-id="c9677-129">Můžete vytvořit nový fragment nebo uložit existující konfiguraci modulu jako fragment.</span><span class="sxs-lookup"><span data-stu-id="c9677-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="c9677-130">Vytvořit nový fragment</span><span class="sxs-lookup"><span data-stu-id="c9677-130">Create a new fragment</span></span>

<span data-ttu-id="c9677-131">Při vytváření nového fragmentu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="c9677-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="c9677-132">V navigačním podokně nalevo vyberte položku **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="c9677-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c9677-133">Zvolte **Nový fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="c9677-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="c9677-134">Zobrazí se dialogové okno s informacemi o všech dostupných typech modulů.</span><span class="sxs-lookup"><span data-stu-id="c9677-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="c9677-135">Jak bylo zmíněno dříve, fragmenty mohou být vytvořeny z libovolného typu modulu.</span><span class="sxs-lookup"><span data-stu-id="c9677-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="c9677-136">Vyberte typ modulu pro svůj fragment a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9677-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="c9677-137">Výběrem generického typu kontejnerového modulu získáte maximální pružnost při aktualizaci a konfiguraci fragmentu později.</span><span class="sxs-lookup"><span data-stu-id="c9677-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="c9677-138">Uložit existující konfiguraci modulu jako fragment</span><span class="sxs-lookup"><span data-stu-id="c9677-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="c9677-139">Chcete-li převést dříve konfigurovaný modul na opakovaně použitelný fragment, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="c9677-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="c9677-140">Otevřete stránku nebo šablonu obsahující modul, který chcete převést na fragment.</span><span class="sxs-lookup"><span data-stu-id="c9677-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="c9677-141">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu a pak vyberte možnost **Uložit jako fragment.**</span><span class="sxs-lookup"><span data-stu-id="c9677-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="c9677-142">Zobrazí se dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c9677-142">A dialog box appears.</span></span>
1. <span data-ttu-id="c9677-143">Zadejte název a metadata fragmentu.</span><span class="sxs-lookup"><span data-stu-id="c9677-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="c9677-144">Chcete-li uložit konfiguraci modulu jako fragment, který lze přidat na jiné stránky, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9677-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="c9677-145">Přidání, odebrání nebo úprava fragmentů na stránce</span><span class="sxs-lookup"><span data-stu-id="c9677-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="c9677-146">Následující postupy popisují způsob přidávání, odebírání a úprav fragmentů.</span><span class="sxs-lookup"><span data-stu-id="c9677-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="c9677-147">Přidat fragment</span><span class="sxs-lookup"><span data-stu-id="c9677-147">Add a fragment</span></span>

<span data-ttu-id="c9677-148">Chcete-li přidat fragment na stránku, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="c9677-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="c9677-149">V podokně osnovy vlevo vyberte kontejner nebo slot, do kterých lze přidávat podřízené moduly.</span><span class="sxs-lookup"><span data-stu-id="c9677-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="c9677-150">Vyberte tlačítko se třemi tečkami názvu kontejneru nebo slotu a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="c9677-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="c9677-151">Zobrazí se dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c9677-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9677-152">Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat fragment** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="c9677-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="c9677-153">V dialogovém okně vyhledejte a vyberte fragment, který chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="c9677-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="c9677-154">Nejsou-li v seznamu uvedeny žádné fragmenty, bude pravděpodobně nutné nejprve vytvořit fragment z typu modulu, který podporuje vybraný kontejner nebo slot.</span><span class="sxs-lookup"><span data-stu-id="c9677-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="c9677-155">Výběrem tlačítka **OK** přidáte vybraný fragment do vybraného kontejneru nebo slotu na stránce.</span><span class="sxs-lookup"><span data-stu-id="c9677-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="c9677-156">Moduly, které jsou povoleny v kontejneru nebo slotu, jsou definovány šablonou stránky nebo vlastními definicemi modulů.</span><span class="sxs-lookup"><span data-stu-id="c9677-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="c9677-157">Odebrání fragmentu</span><span class="sxs-lookup"><span data-stu-id="c9677-157">Remove a fragment</span></span>

<span data-ttu-id="c9677-158">Chcete-li odebrat fragment ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="c9677-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="c9677-159">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu modulu, který chcete odebrat, a pak vyberte tlačítko odpadkového koše.</span><span class="sxs-lookup"><span data-stu-id="c9677-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="c9677-160">Až budete vyzváni k potvrzení odebrání fragmentu, vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="c9677-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="c9677-161">Odeberete-li fragment ze stránky, odstraníte z něj pouze odkaz na něj.</span><span class="sxs-lookup"><span data-stu-id="c9677-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="c9677-162">**Neodstraníte** fragment z vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="c9677-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="c9677-163">Chcete-li odstranit fragmenty z webu, je nutné použít uživatelské rozhraní inspektoru fragmentů.</span><span class="sxs-lookup"><span data-stu-id="c9677-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="c9677-164">Fragmenty z webu lze odstranit pouze v případě, že na ně aktuálně neodkazují žádné stránky, šablony nebo jiné fragmenty.</span><span class="sxs-lookup"><span data-stu-id="c9677-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="c9677-165">Upravit fragment</span><span class="sxs-lookup"><span data-stu-id="c9677-165">Edit a fragment</span></span>

<span data-ttu-id="c9677-166">Chcete-li upravit fragmenty, je nutné použít uživatelské rozhraní editoru fragmentů.</span><span class="sxs-lookup"><span data-stu-id="c9677-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="c9677-167">Toto omezení je záměrné.</span><span class="sxs-lookup"><span data-stu-id="c9677-167">This restriction is by design.</span></span> <span data-ttu-id="c9677-168">Pomáhá zajistit, aby autoři neměnili proces úpravy modulů pro konkrétní stránku s procesem úprav fragmentů, které mohou být sdíleny na více stránkách.</span><span class="sxs-lookup"><span data-stu-id="c9677-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="c9677-169">Při editaci fragmentu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="c9677-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="c9677-170">V navigačním podokně nalevo vyberte položku **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="c9677-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c9677-171">Mezi **Fragmenty** vyberte fragment, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="c9677-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="c9677-172">Upravte vlastnosti a strukturu modulu fragmentu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="c9677-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="c9677-173">Proces se podobá procesu úpravy modulů v zobrazení editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="c9677-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="c9677-174">Fragment můžete také upravit tak, že jej vyberete na stránce, v šabloně nebo v nadřazeném fragmentu a poté vyberete **Upravit fragment** v podokně vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="c9677-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9677-175">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c9677-175">Additional resources</span></span>

[<span data-ttu-id="c9677-176">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="c9677-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c9677-177">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="c9677-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="c9677-178">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="c9677-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="c9677-179">Práce se skupinami publikování</span><span class="sxs-lookup"><span data-stu-id="c9677-179">Work with publish groups</span></span>](publish-groups.md)
