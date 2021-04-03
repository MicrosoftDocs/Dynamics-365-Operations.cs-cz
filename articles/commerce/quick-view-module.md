---
title: Modul rychlého zobrazení
description: Tohle téma se zabývá moduly rychlého zobrazení a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 07fbf8d4115561808b7c61489b343e1c72dd1b6d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243786"
---
# <a name="quick-view-module"></a><span data-ttu-id="65e73-103">Modul rychlého zobrazení</span><span class="sxs-lookup"><span data-stu-id="65e73-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="65e73-104">Tohle téma se zabývá moduly rychlého zobrazení a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="65e73-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="65e73-105">Modul rychlého zobrazení umožňuje uživatelům rychle zobrazit informace o produktu při procházení produktů na stránce seznamu a přidat jeden nebo více produktů do košíku ze stránky seznamu, aniž by museli přejít na stránku s podrobnostmi o produktu (PDP).</span><span class="sxs-lookup"><span data-stu-id="65e73-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="65e73-106">Modul rychlého zobrazení poskytuje přehled informací o produktu, které uživatelé potřebují, aby se mohli rozhodnout „přidat do košíku“.</span><span class="sxs-lookup"><span data-stu-id="65e73-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="65e73-107">Poskytuje také odkaz na PDP, aby si uživatelé mohli prohlédnout další podrobnosti o produktu a možnosti nákupu.</span><span class="sxs-lookup"><span data-stu-id="65e73-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="65e73-108">Modul rychlého zobrazení podporuje moduly [kolekce produktů](product-collection-module-overview.md) a [výsledky vyhledávání](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="65e73-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65e73-109">Modul rychlého zobrazení je k dispozici od verze Commerce verze 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="65e73-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="65e73-110">Následující obrázek ukazuje příklad modulu rychlého zobrazení na stránce se seznamem produktů.</span><span class="sxs-lookup"><span data-stu-id="65e73-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Příklad modulu rychlého zobrazení na stránce se seznamem produktů](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="65e73-112">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="65e73-112">Module properties</span></span>

<span data-ttu-id="65e73-113">Modul rychlého zobrazení podporuje některé ze stejných funkcí jako modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="65e73-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="65e73-114">Vlastnosti modulu rychlého zobrazení se tedy podobají vlastnostem modulu buy boxu.</span><span class="sxs-lookup"><span data-stu-id="65e73-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="65e73-115">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="65e73-115">Property</span></span> | <span data-ttu-id="65e73-116">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="65e73-116">Values</span></span> | <span data-ttu-id="65e73-117">popis</span><span class="sxs-lookup"><span data-stu-id="65e73-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="65e73-118">Značka záhlaví</span><span class="sxs-lookup"><span data-stu-id="65e73-118">Heading tag</span></span> | <span data-ttu-id="65e73-119">**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**</span><span class="sxs-lookup"><span data-stu-id="65e73-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="65e73-120">Tato vlastnost definuje značku nadpisu produktu.</span><span class="sxs-lookup"><span data-stu-id="65e73-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="65e73-121">Je-li modul rychlého zobrazení v horní části stránky, měla by být tato vlastnost nastavena na **H1**, aby vyhovovala standardům usnadnění.</span><span class="sxs-lookup"><span data-stu-id="65e73-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="65e73-122">Povolit vlastní cenu</span><span class="sxs-lookup"><span data-stu-id="65e73-122">Allow custom price</span></span> | <span data-ttu-id="65e73-123">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="65e73-123">**True** or **False**</span></span> | <span data-ttu-id="65e73-124">Pokud je tato vlastnost nastavena na **True**, může uživatel zadat vlastní cenu.</span><span class="sxs-lookup"><span data-stu-id="65e73-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="65e73-125">Minimální cena</span><span class="sxs-lookup"><span data-stu-id="65e73-125">Minimum price</span></span> | <span data-ttu-id="65e73-126">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="65e73-126">Integer</span></span> | <span data-ttu-id="65e73-127">Tato vlastnost je použitelná pouze v případě, že je vlastnost **Povolit vlastní cenu** nastavena na **True**.</span><span class="sxs-lookup"><span data-stu-id="65e73-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="65e73-128">Definuje minimální cenu, kterou může uživatel zadat (například 1 USD).</span><span class="sxs-lookup"><span data-stu-id="65e73-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="65e73-129">Maximální cena</span><span class="sxs-lookup"><span data-stu-id="65e73-129">Maximum price</span></span> | <span data-ttu-id="65e73-130">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="65e73-130">Integer</span></span> | <span data-ttu-id="65e73-131">Tato vlastnost je použitelná pouze v případě, že je vlastnost **Povolit vlastní cenu** nastavena na **True**.</span><span class="sxs-lookup"><span data-stu-id="65e73-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="65e73-132">Definuje maximální cenu, kterou může uživatel zadat (například 1 000 USD).</span><span class="sxs-lookup"><span data-stu-id="65e73-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="65e73-133">Nastavení konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="65e73-133">Commerce site builder settings</span></span>

<span data-ttu-id="65e73-134">Stejně jako modul buy boxu, modul rychlého zobrazení respektuje nastavení na **Nastavení webu \> Rozšíření \> Přidat produkt do košíku**.</span><span class="sxs-lookup"><span data-stu-id="65e73-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="65e73-135">Nastavení **Přejít na stránku košíku** je však ignorováno, protože je v rozporu s účelem modulu rychlého zobrazení, kterým je umožnit uživatelům procházet více produktů na stránce seznamu a přidávat je do košíku, aniž by se vzdalovali od stránky seznamu.</span><span class="sxs-lookup"><span data-stu-id="65e73-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="65e73-136">Přidání modulu rychlého zobrazení do modulu kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="65e73-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="65e73-137">Modul rychlého zobrazení lze přidat do modulů kolekce produktů a výsledky vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="65e73-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="65e73-138">Chcete-li přidat modul rychlého zobrazení do modulu kolekce produktů v konfigurátoru webů Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="65e73-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="65e73-139">Přejděte na **Stránky** a poté vyberte domovskou stránku webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="65e73-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="65e73-140">Přejděte na libovolný modul **Kolekce produktů** na domovské stránce, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="65e73-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65e73-141">V dialogovém okně **Přidat modul** vyberte modul **Rychlé zobrazení** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="65e73-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65e73-142">V podokně vlastností modulu **Rychlé zobrazení**, vyberte **Nadpis**.</span><span class="sxs-lookup"><span data-stu-id="65e73-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="65e73-143">V dialogovém okně **Nadpis**, nastavte pole **Úroveň nadpisu** na **H2** a potom vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="65e73-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="65e73-144">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="65e73-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65e73-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="65e73-145">Additional resources</span></span>

[<span data-ttu-id="65e73-146">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="65e73-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="65e73-147">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="65e73-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="65e73-148">Modul kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="65e73-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="65e73-149">Modul výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="65e73-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]