---
title: Modul potvrzení objednávky
description: Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je použít v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804570"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="bb469-103">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="bb469-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb469-104">Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je použít v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb469-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bb469-105">Po zadání objednávky lze pomocí modulu potvrzení objednávky zobrazit podrobnosti o potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="bb469-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="bb469-106">Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách, možnosti vyzvednutí a způsob expedice.</span><span class="sxs-lookup"><span data-stu-id="bb469-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="bb469-107">Vlastnosti modulu potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="bb469-107">Order confirmation module properties</span></span>

| <span data-ttu-id="bb469-108">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="bb469-108">Property name</span></span>  | <span data-ttu-id="bb469-109">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="bb469-109">Values</span></span> | <span data-ttu-id="bb469-110">Popis</span><span class="sxs-lookup"><span data-stu-id="bb469-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="bb469-111">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="bb469-111">Heading</span></span>        | <span data-ttu-id="bb469-112">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="bb469-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="bb469-113">V modulu potvrzení objednávky může být k dispozici záhlaví.</span><span class="sxs-lookup"><span data-stu-id="bb469-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="bb469-114">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="bb469-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="bb469-115">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="bb469-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="bb469-116">Kontaktní číslo</span><span class="sxs-lookup"><span data-stu-id="bb469-116">Contact number</span></span> | <span data-ttu-id="bb469-117">Text</span><span class="sxs-lookup"><span data-stu-id="bb469-117">Text</span></span> | <span data-ttu-id="bb469-118">Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby.</span><span class="sxs-lookup"><span data-stu-id="bb469-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="bb469-119">Zobrazení informací o časovém úseku vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="bb469-119">Show pickup timeslot information</span></span> | <span data-ttu-id="bb469-120">Pravda nebo nepravda</span><span class="sxs-lookup"><span data-stu-id="bb469-120">True or False</span></span> | <span data-ttu-id="bb469-121">Tato vlastnost je k dispozici v aplikaci Dynamics 365 Commerce 10.0.15 a vyšší.</span><span class="sxs-lookup"><span data-stu-id="bb469-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="bb469-122">Pokud má hodnotu pravda, zobrazí informace o časovém úseku vyzvednutí, pokud je k dispozici pro položku vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="bb469-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="bb469-123">Moduly, které lze použít na stránce potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="bb469-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="bb469-124">Po vytvoření stránky potvrzení objednávky můžete kromě modulu potvrzení objednávky přidat další relevantní moduly.</span><span class="sxs-lookup"><span data-stu-id="bb469-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="bb469-125">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="bb469-125">Here are some examples:</span></span>

- <span data-ttu-id="bb469-126">**Modul doporučení** – modul doporučení lze přidat na stránku potvrzení objednávky s cílem navrhovat ostatní produkty odběrateli.</span><span class="sxs-lookup"><span data-stu-id="bb469-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="bb469-127">**Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku potvrzení objednávky a zobrazit tak marketingový obsah.</span><span class="sxs-lookup"><span data-stu-id="bb469-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="bb469-128">Přidání modulu potvrzení objednávky na stránku</span><span class="sxs-lookup"><span data-stu-id="bb469-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="bb469-129">Chcete-li přidat modul potvrzení objednávky na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="bb469-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="bb469-130">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="bb469-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="bb469-131">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název **šablony potvrzení objednávky** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb469-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="bb469-132">V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="bb469-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bb469-133">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb469-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bb469-134">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="bb469-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bb469-135">V dialogovém okně **Přidat modul** vyberte modul **Potvrzení objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb469-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bb469-136">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** k zobrazení náhledu šablony.</span><span class="sxs-lookup"><span data-stu-id="bb469-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="bb469-137">Modul potvrzení objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="bb469-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="bb469-138">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="bb469-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="bb469-139">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="bb469-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="bb469-140">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona potvrzení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="bb469-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="bb469-141">V části **Název stránky** zadejte **Stránka potvrzení objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb469-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="bb469-142">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="bb469-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bb469-143">V dialogovém okně **Přidat modul** vyberte modul **Potvrzení objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb469-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bb469-144">V podokně podrobností modulu potvrzení objednávky vyberte **Nadpis** vedle symbolu tužky.</span><span class="sxs-lookup"><span data-stu-id="bb469-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="bb469-145">V poli **Text nadpisu** dialogového okna **Nadpis** zadejte text nadpisu **Potvrzení objednávky** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb469-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="bb469-146">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="bb469-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="bb469-147">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="bb469-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb469-148">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="bb469-148">Additional resources</span></span>

[<span data-ttu-id="bb469-149">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="bb469-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bb469-150">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="bb469-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bb469-151">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="bb469-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bb469-152">Platební modul</span><span class="sxs-lookup"><span data-stu-id="bb469-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="bb469-153">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="bb469-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="bb469-154">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="bb469-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="bb469-155">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="bb469-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="bb469-156">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="bb469-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]