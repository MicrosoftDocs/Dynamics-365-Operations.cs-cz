---
title: Práce s fragmenty
description: V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793938"
---
# <a name="work-with-fragments"></a><span data-ttu-id="a4578-103">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="a4578-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4578-104">V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a4578-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a4578-105">Fragmenty umožňují centralizované prostředí pro vytváření konfigurací modulu, které je nutné znovu použít v celém webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="a4578-106">Například záhlaví, zápatí a nápisy jsou často konfigurovány jako fragmenty, protože jsou sdíleny na více stránkách.</span><span class="sxs-lookup"><span data-stu-id="a4578-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="a4578-107">Fragmenty lze považovat za miniaturní webové stránky, které lze vložit do jiných stránek na vašem webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="a4578-108">Fragmenty mají vlastní životní cyklus.</span><span class="sxs-lookup"><span data-stu-id="a4578-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="a4578-109">Jinými slovy, jsou vytvořeny, odkazovány, aktualizovány a odstraněny jako nezávislé entity ve vývojových nástrojích.</span><span class="sxs-lookup"><span data-stu-id="a4578-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="a4578-110">Po dokončení konfigurace fragmentů lze použít všechny moduly, které mohou být použity ve struktuře webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="a4578-111">Fragmenty mohou odkazovat na stránkách, v rozvržení, v šablonách a v jiných fragmentech.</span><span class="sxs-lookup"><span data-stu-id="a4578-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="a4578-112">Fragmenty mohou být vnořeny do sedmi úrovní v jiných fragmentech.</span><span class="sxs-lookup"><span data-stu-id="a4578-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="a4578-113">Chcete-li například propagovat velké množství stránek na více stránkách na našem webu, můžete použít fragment.</span><span class="sxs-lookup"><span data-stu-id="a4578-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="a4578-114">Prvním krokem při vytváření nového fragmentu je výběr typu modulu, ze kterého chcete začít.</span><span class="sxs-lookup"><span data-stu-id="a4578-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="a4578-115">V tomto příkladu můžete vytvořit fragment z modulu Hero.</span><span class="sxs-lookup"><span data-stu-id="a4578-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="a4578-116">Fragmenty mohou být vytvořeny z libovolného typu modulu.</span><span class="sxs-lookup"><span data-stu-id="a4578-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="a4578-117">Poté můžete nakonfigurovat fragment Hero s konkrétním reklamním obsahem.</span><span class="sxs-lookup"><span data-stu-id="a4578-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="a4578-118">Můžete jej také lokalizovat podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="a4578-118">You can also localize it as you require.</span></span> <span data-ttu-id="a4578-119">Nový fragment Hero může být poté spotřebován jako předkonfigurovaný modul na vašem webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="a4578-120">Lze jej snadno přidat do šablon, na určité stránky nebo do jiných fragmentů, které mohou obsahovat Hero moduly.</span><span class="sxs-lookup"><span data-stu-id="a4578-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="a4578-121">Všechna místa, kde je fragment přidán, jsou odkazy na vytvořený centrální fragment Hero.</span><span class="sxs-lookup"><span data-stu-id="a4578-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="a4578-122">Pokud publikujete změny ve fragmentu, tyto změny se okamžitě projeví ve všech místech, kde je fragment odkazován na celém webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="a4578-123">Proto fragmenty poskytují výkonný a účinný prostředek pro opětovné použití a centrální správu konfigurací modulů na pracovišti.</span><span class="sxs-lookup"><span data-stu-id="a4578-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="a4578-124">Pomocí těchto funkcí můžete významně zvýšit pružnost a snížit náklady, které jsou spojeny s řízením obsahu webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="a4578-125">Na následujícím obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a4578-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Na obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="a4578-127">Vytvořit fragment</span><span class="sxs-lookup"><span data-stu-id="a4578-127">Create a fragment</span></span>

<span data-ttu-id="a4578-128">Můžete vytvořit nový fragment nebo uložit existující konfiguraci modulu jako fragment.</span><span class="sxs-lookup"><span data-stu-id="a4578-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="a4578-129">Uložit existující konfiguraci modulu jako fragment</span><span class="sxs-lookup"><span data-stu-id="a4578-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="a4578-130">Chcete-li převést dříve konfigurovaný modul na opakovaně použitelný fragment v tvůrci webů Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="a4578-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a4578-131">Otevřete stránku nebo šablonu obsahující modul, který chcete převést na fragment.</span><span class="sxs-lookup"><span data-stu-id="a4578-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="a4578-132">V podokně osnovy vlevo nebo přímo ve vizuálním tvůrci stránek vyberte dříve nakonfigurovaný modul.</span><span class="sxs-lookup"><span data-stu-id="a4578-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="a4578-133">Vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu v podokně osnovy nebo na panelu nástrojů vybraného modulu ve vizuálním tvůrci stránek.</span><span class="sxs-lookup"><span data-stu-id="a4578-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="a4578-134">Vyberte možnost **Sdílet jako fragment**.</span><span class="sxs-lookup"><span data-stu-id="a4578-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="a4578-135">V dialogovém okně **Uložit jako fragment** zadejte název fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a4578-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="a4578-136">Chcete-li uložit konfiguraci modulu jako fragment, který lze přidat na jiné stránky, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4578-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="a4578-137">Vytvořit nový fragment</span><span class="sxs-lookup"><span data-stu-id="a4578-137">Create a new fragment</span></span>

<span data-ttu-id="a4578-138">Nový fragment vytvoříte v konfigurátoru webů Commerce tímto postupem.</span><span class="sxs-lookup"><span data-stu-id="a4578-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a4578-139">V navigačním podokně nalevo vyberte položku **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="a4578-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a4578-140">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a4578-140">Select **New**.</span></span> <span data-ttu-id="a4578-141">Zobrazí se dialogové okno **Nový fragment** s informacemi o všech dostupných typech modulů.</span><span class="sxs-lookup"><span data-stu-id="a4578-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="a4578-142">Jak bylo zmíněno dříve, fragmenty mohou být vytvořeny z libovolného typu modulu.</span><span class="sxs-lookup"><span data-stu-id="a4578-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="a4578-143">Vyberte typ modulu pro váš fragment.</span><span class="sxs-lookup"><span data-stu-id="a4578-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="a4578-144">Výběrem generického typu kontejnerového modulu získáte maximální pružnost při aktualizaci a konfiguraci fragmentu později.</span><span class="sxs-lookup"><span data-stu-id="a4578-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="a4578-145">Přidání, odebrání nebo úprava fragmentů na stránce</span><span class="sxs-lookup"><span data-stu-id="a4578-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="a4578-146">Následující postupy popisují způsob přidávání, odebírání a úprav fragmentů.</span><span class="sxs-lookup"><span data-stu-id="a4578-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="a4578-147">Přidat fragment</span><span class="sxs-lookup"><span data-stu-id="a4578-147">Add a fragment</span></span>

<span data-ttu-id="a4578-148">Fragment přidáte na stránku v konfigurátoru webů Commerce tímto postupem.</span><span class="sxs-lookup"><span data-stu-id="a4578-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a4578-149">V podokně osnovy vlevo nebo přímo ve vizuálním tvůrci stránek vyberte kontejner nebo slot, do kterých lze přidávat podřízené moduly.</span><span class="sxs-lookup"><span data-stu-id="a4578-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="a4578-150">Vyberte tři tečky (**...**) vedle názvu kontejneru nebo slotu.</span><span class="sxs-lookup"><span data-stu-id="a4578-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="a4578-151">Případně, pokud používáte vizuální tvůrce stránek, vyberte symbol plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="a4578-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="a4578-152">Vyberte **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="a4578-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="a4578-153">Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat fragment** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a4578-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="a4578-154">V dialogovém okně **Vybrat fragment** vyhledejte a vyberte fragment, který chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="a4578-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="a4578-155">Nejsou-li v seznamu uvedeny žádné fragmenty, bude pravděpodobně nutné nejprve vytvořit fragment z typu modulu, který podporuje vybraný kontejner nebo slot.</span><span class="sxs-lookup"><span data-stu-id="a4578-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="a4578-156">Výběrem přidáte požadovaný fragment do vybraného kontejneru nebo slotu na stránce.</span><span class="sxs-lookup"><span data-stu-id="a4578-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="a4578-157">Moduly, které jsou povoleny v kontejneru nebo slotu, jsou definovány šablonou stránky nebo vlastními definicemi modulů.</span><span class="sxs-lookup"><span data-stu-id="a4578-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="a4578-158">Odebrání fragmentu</span><span class="sxs-lookup"><span data-stu-id="a4578-158">Remove a fragment</span></span>

<span data-ttu-id="a4578-159">Chcete-li odebrat fragment ze slotu nebo kontejneru na stránce v tvůrci webů Commerce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a4578-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a4578-160">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami (**...**) vedle názvu fragmentu, který chcete odebrat, a pak vyberte symbol odpadkového koše.</span><span class="sxs-lookup"><span data-stu-id="a4578-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="a4578-161">Alternativně můžete vybrat fragment ve vizuálním tvůrci stránek a vybrat symbol koše na panelu nástrojů fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a4578-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="a4578-162">Až budete vyzváni k potvrzení odebrání fragmentu, vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="a4578-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a4578-163">Odeberete-li fragment ze stránky, odstraníte z něj pouze odkaz na něj.</span><span class="sxs-lookup"><span data-stu-id="a4578-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="a4578-164">**Neodstraníte** fragment z vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="a4578-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="a4578-165">Chcete-li odstranit fragmenty z webu, je nutné použít uživatelské rozhraní inspektoru fragmentů.</span><span class="sxs-lookup"><span data-stu-id="a4578-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="a4578-166">Fragmenty z webu lze odstranit pouze v případě, že na ně aktuálně neodkazují žádné stránky, šablony nebo jiné fragmenty.</span><span class="sxs-lookup"><span data-stu-id="a4578-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="a4578-167">Upravit fragment</span><span class="sxs-lookup"><span data-stu-id="a4578-167">Edit a fragment</span></span>

<span data-ttu-id="a4578-168">Chcete-li upravit fragmenty, je nutné použít uživatelské rozhraní editoru fragmentů.</span><span class="sxs-lookup"><span data-stu-id="a4578-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="a4578-169">Toto omezení je záměrné.</span><span class="sxs-lookup"><span data-stu-id="a4578-169">This restriction is by design.</span></span> <span data-ttu-id="a4578-170">Pomáhá zajistit, aby autoři neměnili proces úpravy modulů pro konkrétní stránku s procesem úprav fragmentů, které mohou být sdíleny na více stránkách.</span><span class="sxs-lookup"><span data-stu-id="a4578-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="a4578-171">Fragment upravíte v konfigurátoru webů Commerce tímto postupem.</span><span class="sxs-lookup"><span data-stu-id="a4578-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a4578-172">V navigačním podokně nalevo vyberte položku **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="a4578-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a4578-173">Mezi **Fragmenty** vyberte fragment, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="a4578-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="a4578-174">Upravte vlastnosti a strukturu modulu fragmentu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="a4578-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="a4578-175">Proces se podobá procesu úpravy modulů v zobrazení editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="a4578-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="a4578-176">Fragment můžete také upravit tak, že jej vyberete na stránce, v šabloně nebo v nadřazeném fragmentu a poté vyberete **Upravit fragment** v podokně vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="a4578-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4578-177">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a4578-177">Additional resources</span></span>

[<span data-ttu-id="a4578-178">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="a4578-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a4578-179">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="a4578-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="a4578-180">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="a4578-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="a4578-181">Práce se skupinami publikování</span><span class="sxs-lookup"><span data-stu-id="a4578-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
