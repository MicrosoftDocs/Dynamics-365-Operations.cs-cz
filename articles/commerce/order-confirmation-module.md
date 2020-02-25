---
title: Modul Detaily objednávky
description: Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026010"
---
# <a name="order-details-module"></a><span data-ttu-id="4a6d7-103">Modul Detaily objednávky</span><span class="sxs-lookup"><span data-stu-id="4a6d7-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4a6d7-104">Toto téma popisuje moduly pro detaily objednávek a popisuje, jak je používat v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4a6d7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="4a6d7-105">Overview</span></span>

<span data-ttu-id="4a6d7-106">Po zadání objednávky lze pomocí modulu detailů objednávky zobrazit podrobnosti o potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="4a6d7-107">Zobrazuje ID potvrzení objednávky, kontaktní informace z objednávky a další podrobnosti o objednávce, jako jsou například zakoupené položky, informace o platbách a způsob expedice.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="4a6d7-108">Vlastnosti modulu potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="4a6d7-108">Order confirmation module properties</span></span>

| <span data-ttu-id="4a6d7-109">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="4a6d7-109">Property name</span></span>  | <span data-ttu-id="4a6d7-110">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="4a6d7-110">Values</span></span> | <span data-ttu-id="4a6d7-111">Popis</span><span class="sxs-lookup"><span data-stu-id="4a6d7-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4a6d7-112">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="4a6d7-112">Heading</span></span>        | <span data-ttu-id="4a6d7-113">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="4a6d7-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4a6d7-114">V modulu potvrzení objednávky může být k dispozici záhlaví.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="4a6d7-115">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="4a6d7-116">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="4a6d7-117">Kontaktní číslo</span><span class="sxs-lookup"><span data-stu-id="4a6d7-117">Contact number</span></span> | <span data-ttu-id="4a6d7-118">Text</span><span class="sxs-lookup"><span data-stu-id="4a6d7-118">Text</span></span> | <span data-ttu-id="4a6d7-119">Pro případ otázek souvisejících s objednávkami lze použít číslo kontaktní osoby.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="4a6d7-120">Moduly, které lze použít na stránce potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="4a6d7-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="4a6d7-121">Po vytvoření stránky s podrobnostmi objednávky můžete kromě modulu podrobností objednávky přidat další relevantní moduly.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="4a6d7-122">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="4a6d7-122">Here are some examples:</span></span>

- <span data-ttu-id="4a6d7-123">**Modul doporučení** – modul doporučení lze přidat na stránku detailů objednávky s cílem navrhovat ostatní produkty odběrateli.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="4a6d7-124">**Marketingové moduly** – kterýkoliv marketingový modul lze přidat na stránku podrobnosti objednávky a zobrazit tak marketingový obsah.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="4a6d7-125">Vytvoření modulu stránky detailů objednávky</span><span class="sxs-lookup"><span data-stu-id="4a6d7-125">Create an order details page module</span></span>

1. <span data-ttu-id="4a6d7-126">Vytvořte šablonu stránky s názvem **Šablona Detaily objednávky**.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="4a6d7-127">V úseku **Hlavní** výchozí stránky přidejte modul detailů objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="4a6d7-128">V modulu detailů objednávky přidejte modul doporučení.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="4a6d7-129">Uložení a náhled šablony.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-129">Save and preview the template.</span></span> <span data-ttu-id="4a6d7-130">Modul detailů objednávky nebude zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="4a6d7-131">Dokončete úpravy šablony a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="4a6d7-132">Šablonu detailů objednávky, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **stránka detailů objednávky**.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="4a6d7-133">Přidejte výchozí stránku do osnovy stránky.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="4a6d7-134">V oblasti **Záhlaví** přidejte fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="4a6d7-135">V oblasti **Zápatí** přidejte fragment zápatí.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="4a6d7-136">V úseku **Hlavní** přidejte modul detailů objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="4a6d7-137">V podokně vlastností modulu detailů objednávky přidejte záhlaví **Detaily objednávky**.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="4a6d7-138">Pod modulem detailů objednávky přidejte modul doporučení a nakonfigurujte jej tak, aby používal nastavení **Nové** a **Nejlépe prodávané**.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="4a6d7-139">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-139">Save and preview the page.</span></span>
1. <span data-ttu-id="4a6d7-140">Dokončete úpravy stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="4a6d7-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a6d7-141">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4a6d7-141">Additional resources</span></span>

[<span data-ttu-id="4a6d7-142">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="4a6d7-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4a6d7-143">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="4a6d7-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4a6d7-144">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="4a6d7-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4a6d7-145">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="4a6d7-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4a6d7-146">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="4a6d7-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4a6d7-147">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="4a6d7-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4a6d7-148">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="4a6d7-148">Footer module</span></span>](author-footer-module.md)
