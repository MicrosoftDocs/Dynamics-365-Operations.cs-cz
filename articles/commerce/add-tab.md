---
title: Modul karty
description: Tohle téma se zabývá moduly karty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c9d897113442f14b95539efb9fec9482be96447a
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817027"
---
# <a name="tab-module"></a><span data-ttu-id="d69a3-103">Modul karty</span><span class="sxs-lookup"><span data-stu-id="d69a3-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d69a3-104">Tohle téma se zabývá moduly karty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d69a3-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d69a3-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d69a3-105">Overview</span></span>

<span data-ttu-id="d69a3-106">Moduly karet podobně jako moduly kontejnerů slouží k uspořádání informací na stránce webu pomocí karet.</span><span class="sxs-lookup"><span data-stu-id="d69a3-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="d69a3-107">Lze je použít na jakékoli stránce, kde je třeba informace prezentovat na kartách.</span><span class="sxs-lookup"><span data-stu-id="d69a3-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="d69a3-108">Do každého modulu karty lze přidat jeden nebo více modulů položek karty.</span><span class="sxs-lookup"><span data-stu-id="d69a3-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="d69a3-109">Každý modul položky karty představuje jednu kartu. Do každého modulu položky karty lze přidat jeden nebo více modulů.</span><span class="sxs-lookup"><span data-stu-id="d69a3-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="d69a3-110">Neexistují žádná omezení pro typy modulů, které mohou být přidány do modulu položky karty.</span><span class="sxs-lookup"><span data-stu-id="d69a3-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="d69a3-111">Následující obrázek znázorňuje příklad modulu karty na stránce webu.</span><span class="sxs-lookup"><span data-stu-id="d69a3-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="d69a3-112">V tomto příkladu je vybrána karta **Expedice**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-112">In this example, the **Shipping** tab selected.</span></span>

![Příklad modulu karty](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="d69a3-114">Vlastnosti modulu karty</span><span class="sxs-lookup"><span data-stu-id="d69a3-114">Tab module properties</span></span>

| <span data-ttu-id="d69a3-115">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="d69a3-115">Property name</span></span> | <span data-ttu-id="d69a3-116">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="d69a3-116">Values</span></span> | <span data-ttu-id="d69a3-117">popis</span><span class="sxs-lookup"><span data-stu-id="d69a3-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d69a3-118">Nadpis</span><span class="sxs-lookup"><span data-stu-id="d69a3-118">Heading</span></span> | <span data-ttu-id="d69a3-119">Text</span><span class="sxs-lookup"><span data-stu-id="d69a3-119">Text</span></span> | <span data-ttu-id="d69a3-120">Tato vlastnost určuje volitelný textový nadpis pro modul karty.</span><span class="sxs-lookup"><span data-stu-id="d69a3-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="d69a3-121">Index aktivních karet</span><span class="sxs-lookup"><span data-stu-id="d69a3-121">Active Tab Index</span></span> | <span data-ttu-id="d69a3-122">Počet</span><span class="sxs-lookup"><span data-stu-id="d69a3-122">Number</span></span> | <span data-ttu-id="d69a3-123">Tato vlastnost určuje kartu, která by měla být při načítání stránky ve výchozím nastavení aktivní.</span><span class="sxs-lookup"><span data-stu-id="d69a3-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="d69a3-124">Pokud není zadána žádná hodnota, je první položka ve výchozím nastavení aktivní.</span><span class="sxs-lookup"><span data-stu-id="d69a3-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="d69a3-125">Vlastnosti modulu položky karty</span><span class="sxs-lookup"><span data-stu-id="d69a3-125">Tab item module properties</span></span>

| <span data-ttu-id="d69a3-126">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="d69a3-126">Property name</span></span> | <span data-ttu-id="d69a3-127">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="d69a3-127">Values</span></span> | <span data-ttu-id="d69a3-128">popis</span><span class="sxs-lookup"><span data-stu-id="d69a3-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d69a3-129">Pozice</span><span class="sxs-lookup"><span data-stu-id="d69a3-129">Title</span></span> | <span data-ttu-id="d69a3-130">Text</span><span class="sxs-lookup"><span data-stu-id="d69a3-130">Text</span></span> | <span data-ttu-id="d69a3-131">Tato vlastnost určuje textový nadpis pro modul položky karty.</span><span class="sxs-lookup"><span data-stu-id="d69a3-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="d69a3-132">Přidání modulu karty na stránku</span><span class="sxs-lookup"><span data-stu-id="d69a3-132">Add a tab module to a page</span></span>

<span data-ttu-id="d69a3-133">Chcete-li přidat modul karty na stránku a nastavit vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d69a3-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="d69a3-134">Pomocí marketingové šablony Fabrikam (nebo jakékoli šablony, která nemá žádná omezení) vytvořte novou stránku s názvem **Stránka zásad obchodu**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="d69a3-135">V pozici **Hlavní** na **výchozí stránce** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d69a3-136">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d69a3-137">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d69a3-138">V dialogovém okně **Přidat modul** vyberte modul **Karta** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d69a3-139">V podokně vlastností modulu karty vyberte **Nadpis** vedle symbolu tužky.</span><span class="sxs-lookup"><span data-stu-id="d69a3-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d69a3-140">V dialogovém okně **Nadpis** pod **Text nadpisu** zadejte text záhlaví (například **Zásady**).</span><span class="sxs-lookup"><span data-stu-id="d69a3-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="d69a3-141">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-141">Then select **OK**.</span></span>
1. <span data-ttu-id="d69a3-142">V pozici **Karta** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d69a3-143">V dialogovém okně **Přidat modul** vyberte modul **Položka karty** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d69a3-144">V podokně vlastností modulu položky karty pod částí **Nadpis** zadejte text nadpisu (například **Dodání**).</span><span class="sxs-lookup"><span data-stu-id="d69a3-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="d69a3-145">V pozici **Položka karty** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d69a3-146">V dialogovém okně **Přidat modul** vyberte modul **Textový blok** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d69a3-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d69a3-147">V podokně vlastností modulu textového bloku v sekci **Formátovaný text** zadejte odstavec textu.</span><span class="sxs-lookup"><span data-stu-id="d69a3-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="d69a3-148">V pozici **Karta** přidejte několik dalších modulů karet, které mají názvy.</span><span class="sxs-lookup"><span data-stu-id="d69a3-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="d69a3-149">Do každého modulu položky karty přidejte modul textového bloku, který má obsah.</span><span class="sxs-lookup"><span data-stu-id="d69a3-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="d69a3-150">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="d69a3-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d69a3-151">Na stránce se zobrazí modul karty, který obsahuje moduly položek karty s obsahem, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="d69a3-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="d69a3-152">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="d69a3-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d69a3-153">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d69a3-153">Additional resources</span></span>

[<span data-ttu-id="d69a3-154">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="d69a3-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d69a3-155">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="d69a3-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d69a3-156">Modul ovládacího prvku Accordion</span><span class="sxs-lookup"><span data-stu-id="d69a3-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="d69a3-157">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="d69a3-157">Text block module</span></span>](add-content-rich-block.md)
