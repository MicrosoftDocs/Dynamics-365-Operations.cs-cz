---
title: Modul potvrzení objednávky
description: Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je použít v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972729"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="0292e-103">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="0292e-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0292e-104">Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je použít v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0292e-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0292e-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="0292e-105">Overview</span></span>

<span data-ttu-id="0292e-106">Po zadání objednávky lze pomocí modulu potvrzení objednávky zobrazit podrobnosti o potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="0292e-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="0292e-107">Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách, možnosti vyzvednutí a způsob expedice.</span><span class="sxs-lookup"><span data-stu-id="0292e-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="0292e-108">Vlastnosti modulu potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="0292e-108">Order confirmation module properties</span></span>

| <span data-ttu-id="0292e-109">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="0292e-109">Property name</span></span>  | <span data-ttu-id="0292e-110">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="0292e-110">Values</span></span> | <span data-ttu-id="0292e-111">Popis</span><span class="sxs-lookup"><span data-stu-id="0292e-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0292e-112">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="0292e-112">Heading</span></span>        | <span data-ttu-id="0292e-113">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="0292e-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0292e-114">V modulu potvrzení objednávky může být k dispozici záhlaví.</span><span class="sxs-lookup"><span data-stu-id="0292e-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="0292e-115">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="0292e-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0292e-116">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="0292e-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0292e-117">Kontaktní číslo</span><span class="sxs-lookup"><span data-stu-id="0292e-117">Contact number</span></span> | <span data-ttu-id="0292e-118">Text</span><span class="sxs-lookup"><span data-stu-id="0292e-118">Text</span></span> | <span data-ttu-id="0292e-119">Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby.</span><span class="sxs-lookup"><span data-stu-id="0292e-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="0292e-120">Zobrazení informací o časovém úseku vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="0292e-120">Show pickup timeslot information</span></span> | <span data-ttu-id="0292e-121">Pravda nebo nepravda</span><span class="sxs-lookup"><span data-stu-id="0292e-121">True or False</span></span> | <span data-ttu-id="0292e-122">Tato vlastnost je k dispozici v aplikaci Dynamics 365 Commerce 10.0.15 a vyšší.</span><span class="sxs-lookup"><span data-stu-id="0292e-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="0292e-123">Pokud má hodnotu pravda, zobrazí informace o časovém úseku vyzvednutí, pokud je k dispozici pro položku vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="0292e-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="0292e-124">Moduly, které lze použít na stránce potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="0292e-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="0292e-125">Po vytvoření stránky potvrzení objednávky můžete kromě modulu potvrzení objednávky přidat další relevantní moduly.</span><span class="sxs-lookup"><span data-stu-id="0292e-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="0292e-126">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="0292e-126">Here are some examples:</span></span>

- <span data-ttu-id="0292e-127">**Modul doporučení** – modul doporučení lze přidat na stránku potvrzení objednávky s cílem navrhovat ostatní produkty odběrateli.</span><span class="sxs-lookup"><span data-stu-id="0292e-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="0292e-128">**Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku potvrzení objednávky a zobrazit tak marketingový obsah.</span><span class="sxs-lookup"><span data-stu-id="0292e-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="0292e-129">Přidání modulu potvrzení objednávky na stránku</span><span class="sxs-lookup"><span data-stu-id="0292e-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="0292e-130">Chcete-li přidat modul potvrzení objednávky na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="0292e-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0292e-131">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="0292e-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0292e-132">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název **šablony potvrzení objednávky** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0292e-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0292e-133">V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="0292e-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0292e-134">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0292e-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0292e-135">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="0292e-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0292e-136">V dialogovém okně **Přidat modul** vyberte modul **Potvrzení objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0292e-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0292e-137">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** k zobrazení náhledu šablony.</span><span class="sxs-lookup"><span data-stu-id="0292e-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="0292e-138">Modul potvrzení objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="0292e-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="0292e-139">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="0292e-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0292e-140">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="0292e-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0292e-141">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona potvrzení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="0292e-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="0292e-142">V části **Název stránky** zadejte **Stránka potvrzení objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0292e-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0292e-143">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="0292e-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0292e-144">V dialogovém okně **Přidat modul** vyberte modul **Potvrzení objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0292e-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0292e-145">V podokně podrobností modulu potvrzení objednávky vyberte **Nadpis** vedle symbolu tužky.</span><span class="sxs-lookup"><span data-stu-id="0292e-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="0292e-146">V poli **Text nadpisu** dialogového okna **Nadpis** zadejte text nadpisu **Potvrzení objednávky** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0292e-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="0292e-147">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="0292e-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0292e-148">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="0292e-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0292e-149">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0292e-149">Additional resources</span></span>

[<span data-ttu-id="0292e-150">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="0292e-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0292e-151">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="0292e-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0292e-152">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="0292e-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0292e-153">Platební modul</span><span class="sxs-lookup"><span data-stu-id="0292e-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0292e-154">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="0292e-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0292e-155">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="0292e-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0292e-156">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="0292e-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="0292e-157">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="0292e-157">Gift card module</span></span>](add-giftcard.md)
