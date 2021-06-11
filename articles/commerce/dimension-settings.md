---
title: Použít nastavení zobrazení pro rozměry produktu
description: Toto téma popisuje nastavení zobrazení pro rozměry produktu a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117213"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="c7865-103">Použít nastavení zobrazení pro rozměry produktu</span><span class="sxs-lookup"><span data-stu-id="c7865-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c7865-104">Toto téma popisuje nastavení zobrazení pro rozměry produktu a popisuje, jak je použít v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7865-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c7865-105">Dynamics 365 Commerce podporuje rozměry, styl a barevné rozměry k rozlišení variant produktu.</span><span class="sxs-lookup"><span data-stu-id="c7865-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="c7865-106">Rozměry se obvykle zobrazují jako textové hodnoty, například „Malé“, „Střední“ a „Velké“ pro velikosti a „Černé“ a „Hnědé“ pro barvy.</span><span class="sxs-lookup"><span data-stu-id="c7865-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="c7865-107">Pokud však produkt podporuje mnoho variant, může být obtížné procházet varianty produktu, protože k zobrazení obrázku pro každou variantu je zapotřebí více výběrů.</span><span class="sxs-lookup"><span data-stu-id="c7865-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="c7865-108">Aby bylo snazší procházet varianty produktů, může verze Commerce verze 10.0.20 používat obrázky a hexadecimální (hex) kódy k zobrazení dimenzí jako políček.</span><span class="sxs-lookup"><span data-stu-id="c7865-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="c7865-109">V nástroji pro tvorbu webu Commerce je nastavení dimenzí definováno v **Nastavení webu \> Rozšíření \> Nastavení dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="c7865-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="c7865-110">Následující obrázek ukazuje příklad nastavení dimenze v nástroji pro tvorbu webů.</span><span class="sxs-lookup"><span data-stu-id="c7865-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Příklad nastavení webu v nástroji pro tvorbu webů Commerce](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="c7865-112">K dispozici jsou dvě nastavení dimenze:</span><span class="sxs-lookup"><span data-stu-id="c7865-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="c7865-113">**Rozměry k zobrazení jako obrázek** - Určete, které dimenze by se měly objevit jako vzorník na stránkách webu elektronického obchodování, jako jsou stránky s podrobnostmi o produktu (PDP) a stránky se seznamem výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="c7865-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="c7865-114">Jakoukoli kombinaci barev, velikostí a rozměrů stylu lze zobrazit jako vzorník.</span><span class="sxs-lookup"><span data-stu-id="c7865-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="c7865-115">Pokud je vybrána dimenze pro zobrazení jako vzorník, vykreslení modulu Commerce bude hledat dostupnou konfiguraci vzorníku hexadecimálního kódu.</span><span class="sxs-lookup"><span data-stu-id="c7865-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="c7865-116">Pokud není nakonfigurován žádný hexadecimální kód, systémová logika bude hledat konfiguraci vzorníku adresy URL obrázku.</span><span class="sxs-lookup"><span data-stu-id="c7865-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="c7865-117">Pokud není nakonfigurován hexadecimální kód ani adresa URL obrázku, zobrazí se text.</span><span class="sxs-lookup"><span data-stu-id="c7865-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="c7865-118">Následující ilustrace ukazuje příklad, kdy PDP na webu elektronického obchodování zahrnuje vzorníky barev a velikostí.</span><span class="sxs-lookup"><span data-stu-id="c7865-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="c7865-119">V tomto příkladu je hexadecimální kód nakonfigurován pro barevnou dimenzi.</span><span class="sxs-lookup"><span data-stu-id="c7865-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="c7865-120">Vzorník se proto zobrazuje jako barvy.</span><span class="sxs-lookup"><span data-stu-id="c7865-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="c7865-121">Pro dimenzi velikosti však není nakonfigurován hexadecimální kód ani adresa URL obrázku.</span><span class="sxs-lookup"><span data-stu-id="c7865-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="c7865-122">Proto se zobrazí text.</span><span class="sxs-lookup"><span data-stu-id="c7865-122">Therefore, text is shown.</span></span>

    ![Příklad barevné dimenze zobrazené jako vzorky na stránce s podrobnostmi o produktu elektronického obchodování](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="c7865-124">**Rozměry k zobrazení na kartě produktu** - Určete, jaké rozměry by se měly objevit na produktových kartách, které se zobrazují v seznamech a na stránkách seznamů.</span><span class="sxs-lookup"><span data-stu-id="c7865-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="c7865-125">Než se dimenze může zobrazit na produktové kartě, musí být pro tuto dimenzi povoleno toto nastavení.</span><span class="sxs-lookup"><span data-stu-id="c7865-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="c7865-126">Nastavení **Rozměry k zobrazení jako obrázek** by mělo být také povoleno.</span><span class="sxs-lookup"><span data-stu-id="c7865-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="c7865-127">Chování výběru vzorků na produktových kartách je optimalizováno pro barevnou dimenzi.</span><span class="sxs-lookup"><span data-stu-id="c7865-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="c7865-128">U jiných dimenzí může být vyžadováno rozšíření pohledu k přizpůsobení chování výběru vzorků.</span><span class="sxs-lookup"><span data-stu-id="c7865-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="c7865-129">Následující obrázek ukazuje příklad, kdy stránka seznamu na webu elektronického obchodování obsahuje karty produktů, které obsahují vzorníky barev.</span><span class="sxs-lookup"><span data-stu-id="c7865-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Příklad barevné dimenze zobrazené jako vzorky na stránce se seznamem elektronického obchodování](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="c7865-131">Informace o tom, jak nakonfigurovat dimenze produktu tak, aby se na stránkách webu zobrazovaly jako vzorník, najdete v části [Nakonfigurujte hodnoty dimenze produktu tak, aby se zobrazovaly jako vzorky](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="c7865-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7865-132">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="c7865-132">Additional resources</span></span>

[<span data-ttu-id="c7865-133">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="c7865-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c7865-134">Modul výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="c7865-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="c7865-135">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="c7865-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c7865-136">Nakonfigurujte hodnoty dimenze produktu tak, aby se zobrazovaly jako vzorky</span><span class="sxs-lookup"><span data-stu-id="c7865-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
