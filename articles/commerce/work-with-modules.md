---
title: Práce s moduly
description: V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210892"
---
# <a name="work-with-modules"></a><span data-ttu-id="48136-103">Práce s moduly</span><span class="sxs-lookup"><span data-stu-id="48136-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48136-104">V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48136-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="48136-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="48136-105">Overview</span></span>

<span data-ttu-id="48136-106">Moduly jsou logické stavební bloky, které tvoří strukturu stránek a mají různé účely a zaměření.</span><span class="sxs-lookup"><span data-stu-id="48136-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="48136-107">Některé moduly jsou kontejnery vysoké úrovně a jejich jediným účelem je obsahování a uspořádání dalších modulů (podřízených modulů).</span><span class="sxs-lookup"><span data-stu-id="48136-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="48136-108">Ostatní moduly, jako je například jednoduchý modul umístění obrázku, mají velmi specifický účel.</span><span class="sxs-lookup"><span data-stu-id="48136-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="48136-109">Mezi těmito dvěma kategoriemi patří i jiné moduly, například karuselový modul.</span><span class="sxs-lookup"><span data-stu-id="48136-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="48136-110">Ve výchozím nastavení váš web Dynamics 365 Commerce obsahuje knihovnu modulů, která umožňuje dosáhnout většiny základních scénářů e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="48136-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="48136-111">Pomocí pouze těchto modulů by mělo být možné vytvořit komplexní web e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="48136-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="48136-112">Můžete však také přizpůsobit tyto moduly nebo sestavit nové, vlastní moduly pro specifické potřeby.</span><span class="sxs-lookup"><span data-stu-id="48136-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="48136-113">Chcete-li vytvořit vlastní moduly, je k dispozici sada SDK (Software Development Kit), která usnadňuje vytvoření vlastní knihovny modulů.</span><span class="sxs-lookup"><span data-stu-id="48136-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="48136-114">Moduly a sloty kontejneru</span><span class="sxs-lookup"><span data-stu-id="48136-114">Container modules and slots</span></span>

<span data-ttu-id="48136-115">Jak bylo zmíněno dříve, některé moduly jsou navrženy pro uchovávání podřízených modulů.</span><span class="sxs-lookup"><span data-stu-id="48136-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="48136-116">Tyto moduly jsou označovány jako *kontejnery* a umožňují hierarchie vnořených modulů.</span><span class="sxs-lookup"><span data-stu-id="48136-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="48136-117">Kontejnerové moduly obsahují *sloty*.</span><span class="sxs-lookup"><span data-stu-id="48136-117">Container modules include *slots*.</span></span> <span data-ttu-id="48136-118">Sloty se používají k obsluze rozvržení a účelu podřízených modulů v kontejneru.</span><span class="sxs-lookup"><span data-stu-id="48136-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="48136-119">Příkladem může být základní modul kontejneru stránky (modul nejvyšší úrovně pro libovolnou stránku), který definuje několik důležitých slotů:</span><span class="sxs-lookup"><span data-stu-id="48136-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="48136-120">Slot záhlaví</span><span class="sxs-lookup"><span data-stu-id="48136-120">A header slot</span></span>
- <span data-ttu-id="48136-121">Slot dílčího záhlaví</span><span class="sxs-lookup"><span data-stu-id="48136-121">A sub-header slot</span></span>
- <span data-ttu-id="48136-122">Hlavní slot</span><span class="sxs-lookup"><span data-stu-id="48136-122">A main slot</span></span>
- <span data-ttu-id="48136-123">Slot zápatí</span><span class="sxs-lookup"><span data-stu-id="48136-123">A footer slot</span></span>
- <span data-ttu-id="48136-124">Slot dílčího zápatí</span><span class="sxs-lookup"><span data-stu-id="48136-124">A sub-footer slot</span></span>

<span data-ttu-id="48136-125">Vývojář modulu definuje tyto sloty a určuje, které podřízené moduly a kolik podřízených modulů je možné přímo do ní vložit.</span><span class="sxs-lookup"><span data-stu-id="48136-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="48136-126">Například slot záhlaví může podporovat pouze jeden modul typu **Modulu záhlaví**, zatímco slot obsahu může podporovat neomezený počet modulů typu (kromě jiných modulů kontejneru stránky).</span><span class="sxs-lookup"><span data-stu-id="48136-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="48136-127">V nástrojích pro vytváření obsahu nemusí autoři stránek předem vědět, které moduly lze a nelze vložit do jednotlivých slotů.</span><span class="sxs-lookup"><span data-stu-id="48136-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="48136-128">Když autoři stránek vybírají slot a pak se pokusí vybrat modul, který se má přidat, uvidí filtrované zobrazení typů modulů, které jsou pro daný slot podporovány.</span><span class="sxs-lookup"><span data-stu-id="48136-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="48136-129">Moduly obsahu</span><span class="sxs-lookup"><span data-stu-id="48136-129">Content modules</span></span>

<span data-ttu-id="48136-130">Moduly obsahu obsahují obsah a multimediální prvky, například text (například nadpisy, odstavce a odkazy) nebo odkazy na materiály (například obrázky, video a PDF).</span><span class="sxs-lookup"><span data-stu-id="48136-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="48136-131">Typické typy modulů obsahu zahrnují moduly obsahu, blok textu a propagační bannerové moduly.</span><span class="sxs-lookup"><span data-stu-id="48136-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="48136-132">Moduly těchto tří typů mohou obsahovat text nebo média a nevyžadují žádné podřízené moduly, aby je bylo možné zobrazit na stránce.</span><span class="sxs-lookup"><span data-stu-id="48136-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="48136-133">Většina typických, každodenních aktivit vytváření stránek a obsahu zahrnuje moduly obsahu, především proto, že tyto moduly definují skutečný obsah, který je vykreslený v nadřazených modulech kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="48136-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="48136-134">K dispozici je mnoho modulů obsahu a tyto moduly jsou obvykle posledními částmi, které přidáte do hierarchie vnořených modulů.</span><span class="sxs-lookup"><span data-stu-id="48136-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="48136-135">Následující ilustrace znázorňuje, jak jsou moduly vnořené v nadřazených slotech modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="48136-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Vnoření modulů](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="48136-137">Přidat nebo odebrat moduly</span><span class="sxs-lookup"><span data-stu-id="48136-137">Add or remove modules</span></span>

<span data-ttu-id="48136-138">Následující postupy popisují způsob přidávání a odebírání modulů.</span><span class="sxs-lookup"><span data-stu-id="48136-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="48136-139">Přidat modul</span><span class="sxs-lookup"><span data-stu-id="48136-139">Add a module</span></span>

<span data-ttu-id="48136-140">Chcete-li přidat modul do slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="48136-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="48136-141">V podokně obrysu vlevo nebo přímo na hlavním plátně vyberte kontejner nebo slot, do kterých lze přidat podřízený modul.</span><span class="sxs-lookup"><span data-stu-id="48136-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48136-142">Návrhář modulů definuje seznam typů modulů, které lze přidat do určitého slotu modulu.</span><span class="sxs-lookup"><span data-stu-id="48136-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="48136-143">Autoři šablon pak mohou vylepšit povolené možnosti modulu, aby zajistily konzistentní optimalizaci vyhledávače (SEO) a efektivitu vytváření pro všechny stránky, které jsou vytvořeny z určité šablony.</span><span class="sxs-lookup"><span data-stu-id="48136-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="48136-144">Při přidání modulu do slotu je automaticky filtrováno dialogové okno **Přidat modul**, takže zobrazuje pouze moduly, které jsou podporovány ve vybraném kontejneru nebo slotu.</span><span class="sxs-lookup"><span data-stu-id="48136-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="48136-145">Tento seznam povolených modulů je určen šablonou stránky nebo definicí modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="48136-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="48136-146">Pokud používáte podokno obrysu, vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="48136-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="48136-147">Pokud používáte ovládací prvky přímo na plátně, vyberte symbol plus (**+**) v prázdném slotu nebo v sousedství aktuálně vybraného modulu a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="48136-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48136-148">Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat modul** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="48136-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="48136-149">V dialogovém okně **Přidat modul** vyhledejte a vyberte modul, který chcete přidat na svoji stránku.</span><span class="sxs-lookup"><span data-stu-id="48136-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="48136-150">**Blok obsahu** je dobrým typem modulu pro začátečníky.</span><span class="sxs-lookup"><span data-stu-id="48136-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="48136-151">Výběrem tlačítka **OK** přidáte vybraný modul do vybraného kontejneru nebo slotu na stránce.</span><span class="sxs-lookup"><span data-stu-id="48136-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="48136-152">Odebrání modulu</span><span class="sxs-lookup"><span data-stu-id="48136-152">Remove a module</span></span>

<span data-ttu-id="48136-153">Chcete-li odebrat modul ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="48136-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="48136-154">V podokně obrysu vlevo vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu, který chcete odebrat, a pak vyberte symbol odpadkového koše.</span><span class="sxs-lookup"><span data-stu-id="48136-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="48136-155">Alternativně můžete na hlavním plátně vybrat symbol koše na panelu nástrojů vybraného modulu.</span><span class="sxs-lookup"><span data-stu-id="48136-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="48136-156">Až budete vyzváni k potvrzení odebrání modulu, vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="48136-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="48136-157">Přesunutí modulu na novou pozici</span><span class="sxs-lookup"><span data-stu-id="48136-157">Move a module to a new position</span></span>

<span data-ttu-id="48136-158">Chcete-li přesunout modul na nové místo na stránce, použijte některou z následujících metod.</span><span class="sxs-lookup"><span data-stu-id="48136-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="48136-159">Přesuňte modul pomocí podokna obrysu</span><span class="sxs-lookup"><span data-stu-id="48136-159">Move a module using the outline pane</span></span>

<span data-ttu-id="48136-160">Chcete-li přesunout modul pomocí podokna obrysu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="48136-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="48136-161">Vyberte a podržte modul, který chcete přesunout, v podokně obrysu, a poté modul přetáhněte na nové místo v obrysu.</span><span class="sxs-lookup"><span data-stu-id="48136-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="48136-162">Modrá čára v obrysu a na plátně označuje, kam lze modul umístit.</span><span class="sxs-lookup"><span data-stu-id="48136-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="48136-163">Uvolněte modul a přemístěte jej do nové polohy.</span><span class="sxs-lookup"><span data-stu-id="48136-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="48136-164">Přesuňte modul přímo na plátno</span><span class="sxs-lookup"><span data-stu-id="48136-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="48136-165">Chcete-li přesunout modul přímo v rámci plátna, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="48136-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="48136-166">Vyberte modul, který chcete na plátně přesunout.</span><span class="sxs-lookup"><span data-stu-id="48136-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="48136-167">Na panelu nástrojů modulu vyberte buď symbol šipky směřující nahoru nebo dolů a potom přetáhněte šipku na nové místo na stránce.</span><span class="sxs-lookup"><span data-stu-id="48136-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="48136-168">Modrá čára v obrysu a na plátně označuje, kam lze modul umístit.</span><span class="sxs-lookup"><span data-stu-id="48136-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="48136-169">Pokud nelze modul posunout nahoru nebo dolů, bude symbol šipky zobrazen šedě.</span><span class="sxs-lookup"><span data-stu-id="48136-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="48136-170">Uvolněte modul a přemístěte jej do nové polohy.</span><span class="sxs-lookup"><span data-stu-id="48136-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="48136-171">Přesuňte modul pomocí nabídky se třemi tečkami</span><span class="sxs-lookup"><span data-stu-id="48136-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="48136-172">Chcete-li přesunout modul pomocí nabídky se třemi tečkami, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="48136-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="48136-173">Vyberte modul v obrysu nebo na plátně.</span><span class="sxs-lookup"><span data-stu-id="48136-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="48136-174">Vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu v podokně obrysu nebo na panelu nástrojů vybraného modulu na plátně.</span><span class="sxs-lookup"><span data-stu-id="48136-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="48136-175">Pokud lze modul pohybovat nahoru nebo dolů v kontejneru nebo slotu, zobrazí se možnosti pro **Posunout nahoru** nebo **Posunout dolů**.</span><span class="sxs-lookup"><span data-stu-id="48136-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="48136-176">Vyberte požadovanou možnost přesunu pro přesun modulu nahoru nebo dolů vzhledem k jeho sourozencům.</span><span class="sxs-lookup"><span data-stu-id="48136-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="48136-177">Konfigurace modulů</span><span class="sxs-lookup"><span data-stu-id="48136-177">Configure modules</span></span>

<span data-ttu-id="48136-178">Následující postupy popisují způsob konfigurace modulů obsahu a kontejneru.</span><span class="sxs-lookup"><span data-stu-id="48136-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="48136-179">Konfigurace modulu obsahu</span><span class="sxs-lookup"><span data-stu-id="48136-179">Configure a content module</span></span>

<span data-ttu-id="48136-180">Chcete-li konfigurovat modul obsahu na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="48136-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="48136-181">V podokně osnovy vlevo rozbalte stromovou strukturu a vyberte libovolný modul obsahu (například **Blok obsahu**).</span><span class="sxs-lookup"><span data-stu-id="48136-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="48136-182">Případně vyberte modul, který chcete na hlavním plátně přesunout.</span><span class="sxs-lookup"><span data-stu-id="48136-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="48136-183">V podokně vlastností modulu vpravo zadejte vlastnosti pro všechny požadované ovládací prvky modulu.</span><span class="sxs-lookup"><span data-stu-id="48136-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="48136-184">Na příkazovém řádku vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="48136-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="48136-185">Tím se také obnoví plátno náhledu.</span><span class="sxs-lookup"><span data-stu-id="48136-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="48136-186">Úprava textových vlastností modulu</span><span class="sxs-lookup"><span data-stu-id="48136-186">Edit module text properties</span></span>

<span data-ttu-id="48136-187">Vlastnosti textu modulu, které nejsou jen pro čtení, lze upravovat přímo na plátně.</span><span class="sxs-lookup"><span data-stu-id="48136-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="48136-188">Chcete-li upravit vlastnosti textu modulu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="48136-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="48136-189">Vyberte ovládací prvek textu na plátně a umístěte kurzor na místo, kde chcete text upravit.</span><span class="sxs-lookup"><span data-stu-id="48136-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="48136-190">Zadejte obsah textu.</span><span class="sxs-lookup"><span data-stu-id="48136-190">Enter your text content.</span></span>
1. <span data-ttu-id="48136-191">Chcete-li pokračovat v úpravách jiného obsahu, vyberte místo kdekoli mimo textový obsah.</span><span class="sxs-lookup"><span data-stu-id="48136-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="48136-192">Výběr vloženého obrázku</span><span class="sxs-lookup"><span data-stu-id="48136-192">Inline image selection</span></span>

<span data-ttu-id="48136-193">Vlastnosti obrázku modulu, které nejsou jen pro čtení, lze měnit přímo na plátně.</span><span class="sxs-lookup"><span data-stu-id="48136-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="48136-194">Chcete-li zvolit nový obrázek pro modul obsahu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="48136-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="48136-195">Na plátně dvakrát klikněte na obrázek.</span><span class="sxs-lookup"><span data-stu-id="48136-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="48136-196">Otevře se okno pro výběr média.</span><span class="sxs-lookup"><span data-stu-id="48136-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="48136-197">Vyhledejte a vyberte nový obrázek, který chcete použít, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="48136-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="48136-198">Nový obrázek je nyní vykreslen na plátně.</span><span class="sxs-lookup"><span data-stu-id="48136-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="48136-199">Konfigurace modulu kontejneru</span><span class="sxs-lookup"><span data-stu-id="48136-199">Configure a container module</span></span>

<span data-ttu-id="48136-200">Chcete-li konfigurovat modul kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="48136-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="48136-201">Vyberte na stránce kontejnerový modul (například modul karuselového nebo tekutého kontejneru).</span><span class="sxs-lookup"><span data-stu-id="48136-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="48136-202">V podokně vlastnosti vpravo rozbalte vnořené ovládací prvky výběrem záhlaví a nastavte požadované hodnoty ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="48136-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="48136-203">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu kontejneru nebo slotu uvnitř kontejneru a pak vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="48136-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="48136-204">Poté přidejte do vybraného kontejneru podřízené moduly.</span><span class="sxs-lookup"><span data-stu-id="48136-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="48136-205">Další informace naleznete v oddílu [Práce s moduly](#add-a-module) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="48136-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="48136-206">Pokud existuje více podřízených modulů v nadřazeném kontejneru na stejné úrovni, můžete změnit pořadí jejich zobrazení v nadřazeném kontejneru.</span><span class="sxs-lookup"><span data-stu-id="48136-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="48136-207">Vyberte tlačítko se třemi tečkami pro modul a pak použijte tlačítka se šipkou nahoru a dolů.</span><span class="sxs-lookup"><span data-stu-id="48136-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48136-208">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="48136-208">Additional resources</span></span>

[<span data-ttu-id="48136-209">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="48136-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="48136-210">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="48136-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="48136-211">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="48136-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="48136-212">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="48136-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="48136-213">Přidání modulu kontejneru na stránku</span><span class="sxs-lookup"><span data-stu-id="48136-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="48136-214">Práce s publikovacími skupinami</span><span class="sxs-lookup"><span data-stu-id="48136-214">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]