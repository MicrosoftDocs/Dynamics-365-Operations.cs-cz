---
title: Práce s moduly
description: V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025872"
---
# <a name="work-with-modules"></a><span data-ttu-id="d80ad-103">Práce s moduly</span><span class="sxs-lookup"><span data-stu-id="d80ad-103">Work with modules</span></span>

<span data-ttu-id="d80ad-104">V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d80ad-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="d80ad-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d80ad-105">Overview</span></span>

<span data-ttu-id="d80ad-106">Moduly jsou logické stavební bloky, které tvoří strukturu stránek a mají různé účely a zaměření.</span><span class="sxs-lookup"><span data-stu-id="d80ad-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="d80ad-107">Některé moduly jsou kontejnery vysoké úrovně a jejich jediným účelem je obsahování a uspořádání dalších modulů (podřízených modulů).</span><span class="sxs-lookup"><span data-stu-id="d80ad-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="d80ad-108">Ostatní moduly, jako je například jednoduchý modul umístění obrázku, mají velmi specifický účel.</span><span class="sxs-lookup"><span data-stu-id="d80ad-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="d80ad-109">Mezi těmito dvěma kategoriemi patří i jiné moduly, například karuselový modul.</span><span class="sxs-lookup"><span data-stu-id="d80ad-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="d80ad-110">Ve výchozím nastavení váš web Dynamics 365 Commerce obsahuje knihovnu modulů startovní sady, která umožňuje dosáhnout většiny základních scénářů e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="d80ad-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="d80ad-111">Pomocí pouze těchto modulů by mělo být možné vytvořit komplexní web e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="d80ad-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="d80ad-112">Můžete však také přizpůsobit tyto moduly nebo sestavit nové, vlastní moduly pro specifické potřeby.</span><span class="sxs-lookup"><span data-stu-id="d80ad-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="d80ad-113">Chcete-li vytvořit vlastní moduly, je k dispozici sada SDK (Software Development Kit), která usnadňuje vytvoření vlastní knihovny modulů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="d80ad-114">Moduly a sloty kontejneru</span><span class="sxs-lookup"><span data-stu-id="d80ad-114">Container modules and slots</span></span>

<span data-ttu-id="d80ad-115">Jak bylo zmíněno dříve, některé moduly jsou navrženy pro uchovávání podřízených modulů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="d80ad-116">Tyto moduly jsou označovány jako *kontejnery* a umožňují hierarchie vnořených modulů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="d80ad-117">Kontejnerové moduly obsahují *sloty*.</span><span class="sxs-lookup"><span data-stu-id="d80ad-117">Container modules include *slots*.</span></span> <span data-ttu-id="d80ad-118">Sloty se používají k obsluze rozvržení a účelu podřízených modulů v kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d80ad-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="d80ad-119">Příkladem může být základní modul kontejneru stránky (modul nejvyšší úrovně pro libovolnou stránku), který definuje několik důležitých slotů:</span><span class="sxs-lookup"><span data-stu-id="d80ad-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="d80ad-120">Slot záhlaví</span><span class="sxs-lookup"><span data-stu-id="d80ad-120">A header slot</span></span>
- <span data-ttu-id="d80ad-121">Slot obsahu</span><span class="sxs-lookup"><span data-stu-id="d80ad-121">A body slot</span></span>
- <span data-ttu-id="d80ad-122">Slot zápatí</span><span class="sxs-lookup"><span data-stu-id="d80ad-122">A footer slot</span></span>

<span data-ttu-id="d80ad-123">Vývojář modulu definuje tyto sloty a určuje, které podřízené moduly a kolik podřízených modulů je možné přímo do ní vložit.</span><span class="sxs-lookup"><span data-stu-id="d80ad-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="d80ad-124">Například slot záhlaví může podporovat pouze jeden modul typu **Modulu záhlaví**, zatímco slot obsahu může podporovat neomezený počet modulů typu (kromě jiných modulů kontejneru stránky).</span><span class="sxs-lookup"><span data-stu-id="d80ad-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="d80ad-125">V nástrojích pro vytváření obsahu nemusí autoři stránek předem vědět, které moduly lze a nelze vložit do jednotlivých slotů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="d80ad-126">Když autoři stránek vybírají slot a pak se pokusí vybrat modul, který se má přidat, uvidí filtrované zobrazení typů modulů, které jsou pro daný slot podporovány.</span><span class="sxs-lookup"><span data-stu-id="d80ad-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="d80ad-127">Moduly obsahu</span><span class="sxs-lookup"><span data-stu-id="d80ad-127">Content modules</span></span>

<span data-ttu-id="d80ad-128">Moduly obsahu obsahují obsah a multimediální prvky, například text (například nadpisy, odstavce a odkazy) nebo odkazy na materiály (například obrázky, video a PDF).</span><span class="sxs-lookup"><span data-stu-id="d80ad-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="d80ad-129">Příklady typických typů modulů obsahu jsou **Hero**, **Funkce** a **Banner**.</span><span class="sxs-lookup"><span data-stu-id="d80ad-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="d80ad-130">Moduly těchto tří typů mohou obsahovat text nebo média a nevyžadují žádné podřízené moduly, aby je bylo možné zobrazit na stránce.</span><span class="sxs-lookup"><span data-stu-id="d80ad-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="d80ad-131">Většina typických, každodenních aktivit vytváření stránek a obsahu zahrnuje moduly obsahu, především proto, že tyto moduly definují skutečný obsah, který je vykreslený v nadřazených modulech kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="d80ad-132">K dispozici je mnoho modulů obsahu a tyto moduly jsou obvykle posledními částmi, které přidáte do hierarchie vnořených modulů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="d80ad-133">Následující ilustrace znázorňuje, jak jsou moduly vnořené v nadřazených slotech modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d80ad-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Vnoření modulů](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="d80ad-135">Přidat nebo odebrat moduly</span><span class="sxs-lookup"><span data-stu-id="d80ad-135">Add or remove modules</span></span>

<span data-ttu-id="d80ad-136">Následující postupy popisují způsob přidávání a odebírání modulů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="d80ad-137">Přidat modul</span><span class="sxs-lookup"><span data-stu-id="d80ad-137">Add a module</span></span>

<span data-ttu-id="d80ad-138">Chcete-li přidat modul do slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d80ad-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="d80ad-139">V podokně osnovy vlevo vyberte kontejner nebo slot, do kterých lze přidávat podřízený modul.</span><span class="sxs-lookup"><span data-stu-id="d80ad-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d80ad-140">Návrhář modulů definuje seznam typů modulů, které lze přidat do určitého slotu modulu.</span><span class="sxs-lookup"><span data-stu-id="d80ad-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="d80ad-141">Autoři šablon pak mohou vylepšit povolené možnosti modulu, aby zajistily konzistentní optimalizaci vyhledávače (SEO) a efektivitu vytváření pro všechny stránky, které jsou vytvořeny z určité šablony.</span><span class="sxs-lookup"><span data-stu-id="d80ad-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="d80ad-142">Vyberte tlačítko se třemi tečkami (**...**) pro modul a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d80ad-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="d80ad-143">Zobrazí se dialogové okno **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d80ad-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="d80ad-144">Toto dialogové okno je automaticky filtrováno, takže zobrazuje pouze moduly, které jsou podporovány ve vybraném kontejneru nebo slotu.</span><span class="sxs-lookup"><span data-stu-id="d80ad-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="d80ad-145">Seznam modulů je určen šablonou stránky nebo definicí modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d80ad-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d80ad-146">Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat modul** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d80ad-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="d80ad-147">V dialogovém okně vyhledejte a vyberte modul, který chcete přidat na svoji stránku.</span><span class="sxs-lookup"><span data-stu-id="d80ad-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="d80ad-148">**Funkce** a **Hero** jsou dobrými typy modulů pro začátečníky.</span><span class="sxs-lookup"><span data-stu-id="d80ad-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="d80ad-149">Výběrem tlačítka **OK** přidáte vybraný modul do vybraného kontejneru nebo slotu na stránce.</span><span class="sxs-lookup"><span data-stu-id="d80ad-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="d80ad-150">Odebrání modulu</span><span class="sxs-lookup"><span data-stu-id="d80ad-150">Remove a module</span></span>

<span data-ttu-id="d80ad-151">Chcete-li odebrat modul ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d80ad-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="d80ad-152">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu modulu, který chcete odebrat, a pak vyberte tlačítko odpadkového koše.</span><span class="sxs-lookup"><span data-stu-id="d80ad-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="d80ad-153">Až budete vyzváni k potvrzení odebrání modulu, vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="d80ad-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="d80ad-154">Konfigurace modulů</span><span class="sxs-lookup"><span data-stu-id="d80ad-154">Configure modules</span></span>

<span data-ttu-id="d80ad-155">Následující postupy popisují způsob konfigurace modulů obsahu a kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d80ad-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="d80ad-156">Konfigurace modulu obsahu</span><span class="sxs-lookup"><span data-stu-id="d80ad-156">Configure a content module</span></span>

<span data-ttu-id="d80ad-157">Chcete-li konfigurovat modul obsahu na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d80ad-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="d80ad-158">V podokně osnovy vlevo rozbalte stromovou strukturu a vyberte libovolný modul obsahu (například **Funkce**, **Hero** nebo **Banner**).</span><span class="sxs-lookup"><span data-stu-id="d80ad-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="d80ad-159">V podokně vlastností vpravo vyhledejte ovládací prvky s obsahem a nastavením modulu.</span><span class="sxs-lookup"><span data-stu-id="d80ad-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="d80ad-160">Zadejte vlastnosti pro jakékoli požadované ovládací prvky modulu.</span><span class="sxs-lookup"><span data-stu-id="d80ad-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="d80ad-161">Na příkazovém řádku vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d80ad-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="d80ad-162">Tím se také obnoví plátno náhledu.</span><span class="sxs-lookup"><span data-stu-id="d80ad-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="d80ad-163">Konfigurace modulu kontejneru</span><span class="sxs-lookup"><span data-stu-id="d80ad-163">Configure a container module</span></span>

<span data-ttu-id="d80ad-164">Chcete-li konfigurovat modul kontejneru na stránce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d80ad-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="d80ad-165">Vyberte na stránce kontejnerový modul (například modul karuselového nebo tekutého kontejneru).</span><span class="sxs-lookup"><span data-stu-id="d80ad-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="d80ad-166">V podokně vlastnosti vpravo rozbalte vnořené ovládací prvky výběrem záhlaví a nastavte požadované hodnoty ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="d80ad-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="d80ad-167">V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu kontejneru nebo slotu uvnitř kontejneru a pak vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d80ad-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="d80ad-168">Poté přidejte do vybraného kontejneru podřízené moduly.</span><span class="sxs-lookup"><span data-stu-id="d80ad-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="d80ad-169">Další informace naleznete v oddílu [Práce s moduly](#add-a-module) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="d80ad-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="d80ad-170">Pokud existuje více podřízených modulů v nadřazeném kontejneru na stejné úrovni, můžete změnit pořadí jejich zobrazení v nadřazeném kontejneru.</span><span class="sxs-lookup"><span data-stu-id="d80ad-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="d80ad-171">Vyberte tlačítko se třemi tečkami pro modul a pak použijte tlačítka se šipkou nahoru a dolů.</span><span class="sxs-lookup"><span data-stu-id="d80ad-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d80ad-172">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d80ad-172">Additional resources</span></span>

[<span data-ttu-id="d80ad-173">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="d80ad-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d80ad-174">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="d80ad-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d80ad-175">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="d80ad-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="d80ad-176">Práce s fragmenty</span><span class="sxs-lookup"><span data-stu-id="d80ad-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="d80ad-177">Přidání modulu kontejneru na stránku</span><span class="sxs-lookup"><span data-stu-id="d80ad-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="d80ad-178">Práce s publikovacími skupinami</span><span class="sxs-lookup"><span data-stu-id="d80ad-178">Work with publish groups</span></span>](publish-groups.md)

