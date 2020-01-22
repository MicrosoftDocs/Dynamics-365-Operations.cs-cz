---
title: Práce s moduly
description: V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.
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
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914787"
---
# <a name="work-with-modules"></a><span data-ttu-id="39c3c-103">Práce s moduly</span><span class="sxs-lookup"><span data-stu-id="39c3c-103">Work with modules</span></span>

<span data-ttu-id="39c3c-104">V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="39c3c-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="39c3c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="39c3c-105">Overview</span></span>

<span data-ttu-id="39c3c-106">Moduly jsou logické stavební bloky, které tvoří strukturu stránek a mají různé účely a zaměření.</span><span class="sxs-lookup"><span data-stu-id="39c3c-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="39c3c-107">Některé moduly jsou kontejnery vysoké úrovně a jejich jediným účelem je obsahování a uspořádání dalších modulů (podřízených modulů).</span><span class="sxs-lookup"><span data-stu-id="39c3c-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="39c3c-108">Ostatní moduly, jako je například jednoduchý modul umístění obrázku, mají velmi specifický účel.</span><span class="sxs-lookup"><span data-stu-id="39c3c-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="39c3c-109">Mezi těmito dvěma kategoriemi patří i jiné moduly, například karuselový modul.</span><span class="sxs-lookup"><span data-stu-id="39c3c-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="39c3c-110">Ve výchozím nastavení váš web Dynamics 365 Commerce obsahuje knihovnu modulů startovní sady, která umožňuje dosáhnout většiny základních scénářů e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="39c3c-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="39c3c-111">Pomocí pouze těchto modulů by mělo být možné vytvořit komplexní web e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="39c3c-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="39c3c-112">Můžete však také přizpůsobit tyto moduly nebo sestavit nové, vlastní moduly pro specifické potřeby.</span><span class="sxs-lookup"><span data-stu-id="39c3c-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="39c3c-113">Chcete-li vytvořit vlastní moduly, je k dispozici sada SDK (Software Development Kit), která usnadňuje vytvoření vlastní knihovny modulů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="39c3c-114">Moduly a sloty kontejneru</span><span class="sxs-lookup"><span data-stu-id="39c3c-114">Container modules and slots</span></span>

<span data-ttu-id="39c3c-115">Jak bylo zmíněno dříve, některé moduly jsou navrženy pro uchovávání podřízených modulů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="39c3c-116">Tyto moduly jsou označovány jako *kontejnery* a umožňují hierarchie vnořených modulů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="39c3c-117">Kontejnerové moduly obsahují *sloty*.</span><span class="sxs-lookup"><span data-stu-id="39c3c-117">Container modules include *slots*.</span></span> <span data-ttu-id="39c3c-118">Sloty se používají k obsluze rozvržení a účelu podřízených modulů v kontejneru.</span><span class="sxs-lookup"><span data-stu-id="39c3c-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="39c3c-119">Příkladem může být základní modul kontejneru stránky (modul nejvyšší úrovně pro libovolnou stránku), který definuje několik důležitých slotů:</span><span class="sxs-lookup"><span data-stu-id="39c3c-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="39c3c-120">Slot záhlaví</span><span class="sxs-lookup"><span data-stu-id="39c3c-120">A header slot</span></span>
- <span data-ttu-id="39c3c-121">Slot obsahu</span><span class="sxs-lookup"><span data-stu-id="39c3c-121">A body slot</span></span>
- <span data-ttu-id="39c3c-122">Slot zápatí</span><span class="sxs-lookup"><span data-stu-id="39c3c-122">A footer slot</span></span>

<span data-ttu-id="39c3c-123">Vývojář modulu definuje tyto sloty a určuje, které podřízené moduly a kolik podřízených modulů je možné přímo do ní vložit.</span><span class="sxs-lookup"><span data-stu-id="39c3c-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="39c3c-124">Například slot záhlaví může podporovat pouze jeden modul typu **Modulu záhlaví**, zatímco slot obsahu může podporovat neomezený počet modulů typu (kromě jiných modulů kontejneru stránky).</span><span class="sxs-lookup"><span data-stu-id="39c3c-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="39c3c-125">V nástrojích pro vytváření obsahu nemusí autoři stránek předem vědět, které moduly lze a nelze vložit do jednotlivých slotů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="39c3c-126">Když autoři stránek vybírají slot a pak se pokusí vybrat modul, který se má přidat, uvidí filtrované zobrazení typů modulů, které jsou pro daný slot podporovány.</span><span class="sxs-lookup"><span data-stu-id="39c3c-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="39c3c-127">Moduly obsahu</span><span class="sxs-lookup"><span data-stu-id="39c3c-127">Content modules</span></span>

<span data-ttu-id="39c3c-128">Moduly obsahu obsahují obsah a multimediální prvky, například text (například nadpisy, odstavce a odkazy) nebo odkazy na materiály (například obrázky, video a PDF).</span><span class="sxs-lookup"><span data-stu-id="39c3c-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="39c3c-129">Příklady typických typů modulů obsahu jsou **Hero**, **Funkce** a **Banner**.</span><span class="sxs-lookup"><span data-stu-id="39c3c-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="39c3c-130">Moduly těchto tří typů mohou obsahovat text nebo média a nevyžadují žádné podřízené moduly, aby je bylo možné zobrazit na stránce.</span><span class="sxs-lookup"><span data-stu-id="39c3c-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="39c3c-131">Většina typických, každodenních aktivit vytváření stránek a obsahu zahrnuje moduly obsahu, především proto, že tyto moduly definují skutečný obsah, který je vykreslený v nadřazených modulech kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="39c3c-132">K dispozici je mnoho modulů obsahu a tyto moduly jsou obvykle posledními částmi, které přidáte do hierarchie vnořených modulů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="39c3c-133">Následující ilustrace znázorňuje, jak jsou moduly vnořené v nadřazených slotech modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="39c3c-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Vnoření modulů](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="39c3c-135">Přidat nebo odebrat moduly</span><span class="sxs-lookup"><span data-stu-id="39c3c-135">Add or remove modules</span></span>

<span data-ttu-id="39c3c-136">Následující postupy popisují způsob přidávání a odebírání modulů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="39c3c-137">Přidat modul</span><span class="sxs-lookup"><span data-stu-id="39c3c-137">Add a module</span></span>

<span data-ttu-id="39c3c-138">Chcete-li přidat modul do slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="39c3c-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="39c3c-139">V podokně osnovy vlevo vyberte kontejner nebo slot, do kterých lze přidávat podřízený modul.</span><span class="sxs-lookup"><span data-stu-id="39c3c-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39c3c-140">Návrhář modulů definuje seznam typů modulů, které lze přidat do určitého slotu modulu.</span><span class="sxs-lookup"><span data-stu-id="39c3c-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="39c3c-141">Autoři šablon pak mohou vylepšit povolené možnosti modulu, aby zajistily konzistentní optimalizaci vyhledávače (SEO) a efektivitu vytváření pro všechny stránky, které jsou vytvořeny z určité šablony.</span><span class="sxs-lookup"><span data-stu-id="39c3c-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="39c3c-142">Vyberte tlačítko se třemi tečkami (**...**) pro modul a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="39c3c-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="39c3c-143">Zobrazí se dialogové okno **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="39c3c-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="39c3c-144">Toto dialogové okno je automaticky filtrováno, takže zobrazuje pouze moduly, které jsou podporovány ve vybraném kontejneru nebo slotu.</span><span class="sxs-lookup"><span data-stu-id="39c3c-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="39c3c-145">Seznam modulů je určen šablonou stránky nebo definicí modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="39c3c-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39c3c-146">Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat modul** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="39c3c-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="39c3c-147">V dialogovém okně vyhledejte a vyberte modul, který chcete přidat na svoji stránku.</span><span class="sxs-lookup"><span data-stu-id="39c3c-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="39c3c-148">**Funkce** a **Hero** jsou dobrými typy modulů pro začátečníky.</span><span class="sxs-lookup"><span data-stu-id="39c3c-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="39c3c-149">Výběrem tlačítka **OK** přidáte vybraný modul do vybraného kontejneru nebo slotu na stránce.</span><span class="sxs-lookup"><span data-stu-id="39c3c-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="39c3c-150">Odebrání modulu</span><span class="sxs-lookup"><span data-stu-id="39c3c-150">Remove a module</span></span>

<span data-ttu-id="39c3c-151">Chcete-li odebrat modul ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="39c3c-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="39c3c-152">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu modulu, který chcete odebrat, a pak vyberte tlačítko odpadkového koše.</span><span class="sxs-lookup"><span data-stu-id="39c3c-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="39c3c-153">Až budete vyzváni k potvrzení odebrání modulu, vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="39c3c-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="39c3c-154">Konfigurace modulů</span><span class="sxs-lookup"><span data-stu-id="39c3c-154">Configure modules</span></span>

<span data-ttu-id="39c3c-155">Následující postupy popisují způsob konfigurace modulů obsahu a kontejneru.</span><span class="sxs-lookup"><span data-stu-id="39c3c-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="39c3c-156">Konfigurace modulu obsahu</span><span class="sxs-lookup"><span data-stu-id="39c3c-156">Configure a content module</span></span>

<span data-ttu-id="39c3c-157">Chcete-li konfigurovat modul obsahu na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="39c3c-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="39c3c-158">V podokně osnovy vlevo vyberte typ modulu obsahu (například **Funkce**, **Hero** nebo **Banner**).</span><span class="sxs-lookup"><span data-stu-id="39c3c-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="39c3c-159">V podokně vlastnosti vpravo rozbalte vnořené ovládací prvky výběrem záhlaví a nastavte požadované hodnoty ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="39c3c-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="39c3c-160">Pokud má podokno vlastností oddíl **Konfigurace dat**, vyberte jej a rozbalte jej.</span><span class="sxs-lookup"><span data-stu-id="39c3c-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="39c3c-161">V opačném případě přejděte ke kroku 5.</span><span class="sxs-lookup"><span data-stu-id="39c3c-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="39c3c-162">Pokud existuje tlačítko **Přidat zdroj dat**, vyberte je a poté vyberte položky obsahu, které chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="39c3c-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="39c3c-163">Zadejte nastavení pro všechny vyžadované nebo požadované ovládací prvky modulu.</span><span class="sxs-lookup"><span data-stu-id="39c3c-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="39c3c-164">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="39c3c-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="39c3c-165">Konfigurace modulu kontejneru</span><span class="sxs-lookup"><span data-stu-id="39c3c-165">Configure a container module</span></span>

<span data-ttu-id="39c3c-166">Chcete-li konfigurovat modul kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="39c3c-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="39c3c-167">Vyberte na stránce kontejnerový modul (například modul karuselového nebo tekutého kontejneru).</span><span class="sxs-lookup"><span data-stu-id="39c3c-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="39c3c-168">V podokně vlastnosti vpravo rozbalte vnořené ovládací prvky výběrem záhlaví a nastavte požadované hodnoty ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="39c3c-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="39c3c-169">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu kontejneru nebo slotu uvnitř kontejneru a pak vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="39c3c-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="39c3c-170">Poté přidejte do vybraného kontejneru podřízené moduly.</span><span class="sxs-lookup"><span data-stu-id="39c3c-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="39c3c-171">Další informace naleznete v tématu [Přidání modulu](#add-a-module) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="39c3c-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="39c3c-172">Pokud existuje více podřízených modulů v nadřazeném kontejneru na stejné úrovni, můžete změnit pořadí jejich zobrazení v nadřazeném kontejneru.</span><span class="sxs-lookup"><span data-stu-id="39c3c-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="39c3c-173">Vyberte tlačítko se třemi tečkami pro modul a pak použijte tlačítka se šipkou nahoru a dolů.</span><span class="sxs-lookup"><span data-stu-id="39c3c-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39c3c-174">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="39c3c-174">Additional resources</span></span>

[<span data-ttu-id="39c3c-175">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="39c3c-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="39c3c-176">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="39c3c-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="39c3c-177">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="39c3c-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="39c3c-178">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="39c3c-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="39c3c-179">Přidání modulu kontejneru na stránku</span><span class="sxs-lookup"><span data-stu-id="39c3c-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="39c3c-180">Přidání modulů umístění obsahu na stránku</span><span class="sxs-lookup"><span data-stu-id="39c3c-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="39c3c-181">Práce se skupinami publikování</span><span class="sxs-lookup"><span data-stu-id="39c3c-181">Work with publish groups</span></span>](publish-groups.md)

