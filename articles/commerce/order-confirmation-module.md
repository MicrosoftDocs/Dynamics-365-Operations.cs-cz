---
title: Modul Detaily objednávky
description: Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015173"
---
# <a name="order-details-module"></a><span data-ttu-id="35680-103">Modul Detaily objednávky</span><span class="sxs-lookup"><span data-stu-id="35680-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="35680-104">Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="35680-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35680-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="35680-105">Overview</span></span>

<span data-ttu-id="35680-106">Po zadání objednávky lze pomocí modulu detailů objednávky zobrazit podrobnosti o potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="35680-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="35680-107">Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách a způsob expedice.</span><span class="sxs-lookup"><span data-stu-id="35680-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="35680-108">Vlastnosti modulu podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="35680-108">Order details module properties</span></span>

| <span data-ttu-id="35680-109">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="35680-109">Property name</span></span>  | <span data-ttu-id="35680-110">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="35680-110">Values</span></span> | <span data-ttu-id="35680-111">popis</span><span class="sxs-lookup"><span data-stu-id="35680-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="35680-112">Nadpis</span><span class="sxs-lookup"><span data-stu-id="35680-112">Heading</span></span>        | <span data-ttu-id="35680-113">Text a značka nadpisu ( **H1** , **H2** , **H3** , **H4** , **H5** nebo **H6** )</span><span class="sxs-lookup"><span data-stu-id="35680-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="35680-114">V modulu podrobností objednávky může být k dispozici záhlaví.</span><span class="sxs-lookup"><span data-stu-id="35680-114">The order details module can have a heading.</span></span> <span data-ttu-id="35680-115">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="35680-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="35680-116">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="35680-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="35680-117">Kontaktní číslo</span><span class="sxs-lookup"><span data-stu-id="35680-117">Contact number</span></span> | <span data-ttu-id="35680-118">Text</span><span class="sxs-lookup"><span data-stu-id="35680-118">Text</span></span> | <span data-ttu-id="35680-119">Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby.</span><span class="sxs-lookup"><span data-stu-id="35680-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="35680-120">Moduly, které lze použít na stránce potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="35680-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="35680-121">Po vytvoření stránky s podrobnostmi objednávky můžete kromě modulu podrobností objednávky přidat další relevantní moduly.</span><span class="sxs-lookup"><span data-stu-id="35680-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="35680-122">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="35680-122">Here are some examples:</span></span>

- <span data-ttu-id="35680-123">**Modul doporučení** – modul doporučení lze přidat na stránku detailů objednávky s cílem navrhovat ostatní produkty odběrateli.</span><span class="sxs-lookup"><span data-stu-id="35680-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="35680-124">**Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku podrobnosti objednávky a zobrazit tak marketingový obsah.</span><span class="sxs-lookup"><span data-stu-id="35680-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="35680-125">Přidání modulu podrobností objednávky na stránku</span><span class="sxs-lookup"><span data-stu-id="35680-125">Add an order details module to a page</span></span>

<span data-ttu-id="35680-126">Chcete-li přidat modul podrobností objednávky na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="35680-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="35680-127">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="35680-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="35680-128">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název **šablony podrobností objednávky** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="35680-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="35680-129">V pozici **Tělo** vyberte tři tečky ( **...** ) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="35680-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="35680-130">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35680-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="35680-131">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami ( **...** ) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="35680-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="35680-132">V dialogovém okně **Přidat modul** vyberte modul **Podrobnosti objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35680-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="35680-133">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** k zobrazení náhledu šablony.</span><span class="sxs-lookup"><span data-stu-id="35680-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="35680-134">Modul detailů objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="35680-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="35680-135">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="35680-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="35680-136">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="35680-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="35680-137">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona podrobností objednávky**.</span><span class="sxs-lookup"><span data-stu-id="35680-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="35680-138">V části **Název stránky** zadejte **Stránka podrobností objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35680-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="35680-139">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami ( **...** ) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="35680-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="35680-140">V dialogovém okně **Přidat modul** vyberte modul **Podrobnosti objednávky** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35680-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="35680-141">V podokně podrobností modulu podrobností objednávky vyberte **Nadpis** vedle symbolu tužky.</span><span class="sxs-lookup"><span data-stu-id="35680-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="35680-142">V poli **Text nadpisu** dialogového okna **Nadpis** zadejte text nadpisu **Podrobnosti o objednávce** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="35680-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="35680-143">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled** , chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="35680-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="35680-144">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="35680-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35680-145">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="35680-145">Additional resources</span></span>

[<span data-ttu-id="35680-146">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="35680-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="35680-147">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="35680-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="35680-148">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="35680-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="35680-149">Modul platby</span><span class="sxs-lookup"><span data-stu-id="35680-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="35680-150">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="35680-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="35680-151">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="35680-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="35680-152">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="35680-152">Gift card module</span></span>](add-giftcard.md)
