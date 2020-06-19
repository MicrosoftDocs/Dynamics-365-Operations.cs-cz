---
title: Modul ovládacího prvku Accordion
description: Tohle téma se zabývá moduly ovládacího prvku Accordion a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417247"
---
# <a name="accordion-module"></a><span data-ttu-id="33359-103">Modul ovládacího prvku Accordion</span><span class="sxs-lookup"><span data-stu-id="33359-103">Accordion module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="33359-104">Tohle téma se zabývá moduly ovládacího prvku Accordion a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="33359-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="33359-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="33359-105">Overview</span></span>

<span data-ttu-id="33359-106">Moduly ovládacího prvku Accordion jsou moduly podobné kontejnerům, které slouží k uspořádání informací nebo modulů na stránce díky možnosti sbalení podobně jako u zásuvek.</span><span class="sxs-lookup"><span data-stu-id="33359-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="33359-107">Modul ovládacího prvku Accordion lze použít na jakékoli stránce.</span><span class="sxs-lookup"><span data-stu-id="33359-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="33359-108">Do každého modulu ovládacího prvku Accordion lze přidat jeden nebo více modulů položky ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="33359-109">Každý modul položky ovládacího prvku Accordion představuje sbalitelnou zásuvku.</span><span class="sxs-lookup"><span data-stu-id="33359-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="33359-110">Do každého modulu položky ovládacího prvku Accordion lze přidat jeden nebo více modulů.</span><span class="sxs-lookup"><span data-stu-id="33359-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="33359-111">Neexistují žádná omezení pro typy modulů, které mohou být přidány do modulu položky ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="33359-112">Následující obrázek znázorňuje příklad modulu ovládacího prvku Accordion, který slouží k uspořádání informací na stránce často kladených otázek (FAQ) v obchodě.</span><span class="sxs-lookup"><span data-stu-id="33359-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Příklad modulu ovládacího prvku Accordion](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="33359-114">Vlastnosti modulu ovládacího prvku Accordion</span><span class="sxs-lookup"><span data-stu-id="33359-114">Accordion module properties</span></span>

| <span data-ttu-id="33359-115">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="33359-115">Property name</span></span> | <span data-ttu-id="33359-116">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="33359-116">Values</span></span> | <span data-ttu-id="33359-117">popis</span><span class="sxs-lookup"><span data-stu-id="33359-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="33359-118">Nadpis</span><span class="sxs-lookup"><span data-stu-id="33359-118">Heading</span></span> | <span data-ttu-id="33359-119">Text</span><span class="sxs-lookup"><span data-stu-id="33359-119">Text</span></span> | <span data-ttu-id="33359-120">Tato vlastnost určuje volitelný textový nadpis pro modul ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="33359-121">Rozbalit vše</span><span class="sxs-lookup"><span data-stu-id="33359-121">Expand All</span></span> | <span data-ttu-id="33359-122">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="33359-122">**True** or **False**</span></span> | <span data-ttu-id="33359-123">Pokud je hodnota nastavena jako **pravda**, je zapnuta funkce rozbalení/sbalení, takže všechny položky v modulu ovládacího prvku Accordion lze rozbalit a sbalit.</span><span class="sxs-lookup"><span data-stu-id="33359-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="33359-124">Styl interakce</span><span class="sxs-lookup"><span data-stu-id="33359-124">Interaction Style</span></span> | <span data-ttu-id="33359-125">**Nezávislý** nebo **Rozbalit pouze jednu položku**</span><span class="sxs-lookup"><span data-stu-id="33359-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="33359-126">Tato vlastnost definuje styl interakce pro položky modulu ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="33359-127">Pokud je hodnota nastavena na **Nezávislý**, lze každou položku modulu ovládacího prvku Accordion nezávisle rozbalit nebo sbalit.</span><span class="sxs-lookup"><span data-stu-id="33359-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="33359-128">Pokud je hodnota nastavena na **Rozbalit pouze jednu položku**, současně lze rozbalit pouze jednu položku.</span><span class="sxs-lookup"><span data-stu-id="33359-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="33359-129">Po rozbalení položek se dříve rozbalené položky sbalí.</span><span class="sxs-lookup"><span data-stu-id="33359-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="33359-130">Vlastnosti modulu položky ovládacího prvku Accordion</span><span class="sxs-lookup"><span data-stu-id="33359-130">Accordion item module properties</span></span>

| <span data-ttu-id="33359-131">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="33359-131">Property name</span></span> | <span data-ttu-id="33359-132">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="33359-132">Values</span></span> | <span data-ttu-id="33359-133">popis</span><span class="sxs-lookup"><span data-stu-id="33359-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="33359-134">Pozice</span><span class="sxs-lookup"><span data-stu-id="33359-134">Title</span></span> | <span data-ttu-id="33359-135">Text</span><span class="sxs-lookup"><span data-stu-id="33359-135">Text</span></span> | <span data-ttu-id="33359-136">Tato vlastnost určuje textový nadpis pro modul položky ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="33359-137">Výběrem oblasti nadpisu mohou uživatelé sekci rozbalit nebo sbalit.</span><span class="sxs-lookup"><span data-stu-id="33359-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="33359-138">Rozbalit ve výchozím nastavení</span><span class="sxs-lookup"><span data-stu-id="33359-138">Expand by default</span></span> | <span data-ttu-id="33359-139">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="33359-139">**True** or **False**</span></span> | <span data-ttu-id="33359-140">Pokud je hodnota nastavena jako **pravda**, při načtení stránky se ve výchozím nastavení sbalí položka modulu ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="33359-141">Přidání modulu ovládacího prvku Accordion na stránku často kladených otázek</span><span class="sxs-lookup"><span data-stu-id="33359-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="33359-142">Chcete-li přidat modul ovládacího prvku Accordion na stránku často kladených otázek a nastavit jeho vlastnosti v tvůrci webů, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="33359-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="33359-143">Přejděte na **Stránky** a pomocí marketingové šablony Fabrikam (nebo jakékoli šablony, která nemá žádná omezení) vytvořte novou pojmenovanou stránku **Často kladené otázky ohledně obchodu**.</span><span class="sxs-lookup"><span data-stu-id="33359-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="33359-144">V pozici **Hlavní** na **výchozí stránce** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="33359-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33359-145">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="33359-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33359-146">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="33359-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33359-147">V dialogovém okně **Přidat modul** vyberte modul **Ovládací prvek Accordion** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="33359-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33359-148">V podokně vlastností modulu ovládacího prvku Accordion vyberte **Nadpis** vedle symbolu tužky.</span><span class="sxs-lookup"><span data-stu-id="33359-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="33359-149">V dialogovém okně **Nadpis** pod volbou **Text nadpisu** zadejte **Často kladené otázky**.</span><span class="sxs-lookup"><span data-stu-id="33359-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="33359-150">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="33359-150">Then select **OK**.</span></span>
1. <span data-ttu-id="33359-151">V podokně vlastností modulu ovládacího prvku Accordion zaškrtněte políčko **Rozbalit vše** a poté v poli **Styl interakce** vyberte pole **Nezávislý**.</span><span class="sxs-lookup"><span data-stu-id="33359-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="33359-152">V pozici **Ovládací prvek Accordion** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="33359-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33359-153">V dialogovém okně **Přidat modul** vyberte modul **Položka ovládacího prvku Accordion** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="33359-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33359-154">V podokně vlastností modulu položky ovládacího prvku Accordion pod částí **Nadpis** zadejte text nadpisu (například **Jak funguje vrácení peněz?**).</span><span class="sxs-lookup"><span data-stu-id="33359-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="33359-155">V pozici **Položka ovládacího prvku Accordion** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="33359-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33359-156">V dialogovém okně **Přidat modul** vyberte modul **Textový blok** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="33359-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33359-157">V podokně vlastností modulu textového bloku zadejte odstavec textu (například **Vratky musí být zpracovány prostřednictvím kontaktního střediska. Pro vrácení kontaktujte 1-800-FABRIKAM. Produkty mají 30denní zásadu vrácení. Vrácení musí být zahájeno v tomto časovém rámci.**).</span><span class="sxs-lookup"><span data-stu-id="33359-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="33359-158">V pozici **Ovládací prvek Accordion** přidejte několik dalších modulů ovládacího prvku Accordion.</span><span class="sxs-lookup"><span data-stu-id="33359-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="33359-159">Do každého modulu položky ovládacího prvku Accordion přidejte modul textového bloku, který má obsah.</span><span class="sxs-lookup"><span data-stu-id="33359-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="33359-160">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="33359-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="33359-161">Na stránce se zobrazí modul ovládacího prvku Accordion s obsahem, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="33359-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="33359-162">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="33359-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33359-163">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="33359-163">Additional resources</span></span>

[<span data-ttu-id="33359-164">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="33359-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="33359-165">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="33359-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="33359-166">Modul karty</span><span class="sxs-lookup"><span data-stu-id="33359-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="33359-167">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="33359-167">Text block module</span></span>](add-content-rich-block.md)
