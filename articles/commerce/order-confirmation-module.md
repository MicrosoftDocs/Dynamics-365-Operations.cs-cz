---
title: Modul potvrzení objednávky
description: Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je vytvořit v aplikaci Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698319"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="30149-103">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="30149-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="30149-104">Toto téma popisuje moduly pro potvrzení objednávek a popisuje, jak je vytvořit v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30149-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30149-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="30149-105">Overview</span></span>

<span data-ttu-id="30149-106">Modul potvrzení objednávky slouží k zobrazení potvrzovací zprávy na stránce potvrzení objednávky poté, co byla objednávka vystavena.</span><span class="sxs-lookup"><span data-stu-id="30149-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="30149-107">V modulu potvrzení objednávky je zobrazeno číslo potvrzení objednávky a e-mailová adresa odběratele, která byla poskytnuta během rezervace.</span><span class="sxs-lookup"><span data-stu-id="30149-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="30149-108">Při zadání objednávky v průběhu rezervace je číslo potvrzení objednávky a e-mailová adresa odběratele předána na stránku potvrzení objednávky jako řetězec dotazu v adrese URL stránky.</span><span class="sxs-lookup"><span data-stu-id="30149-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="30149-109">Modul potvrzení objednávky tyto informace obdrží a uvede stav objednávky na stránce potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="30149-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="30149-110">Modul potvrzení objednávky vyžaduje, aby tento kontext stránky poskytoval stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="30149-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="30149-111">Vlastnosti modulu potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="30149-111">Order confirmation module properties</span></span>

| <span data-ttu-id="30149-112">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="30149-112">Property name</span></span> | <span data-ttu-id="30149-113">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="30149-113">Values</span></span> | <span data-ttu-id="30149-114">Popis</span><span class="sxs-lookup"><span data-stu-id="30149-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="30149-115">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="30149-115">Heading</span></span>       | <span data-ttu-id="30149-116">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="30149-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="30149-117">V modulu potvrzení objednávky může být k dispozici záhlaví.</span><span class="sxs-lookup"><span data-stu-id="30149-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="30149-118">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="30149-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="30149-119">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="30149-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="30149-120">Moduly, které lze použít v modulu stránky potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="30149-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="30149-121">**Doporučení** – modul doporučení může být uveden na stránce potvrzení objednávky s cílem navrhovat ostatní produkty odběrateli.</span><span class="sxs-lookup"><span data-stu-id="30149-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="30149-122">**Marketing** – modul marketingu může přidat marketingový obsah na stránku pro potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="30149-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="30149-123">Přidání modulu stránky potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="30149-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="30149-124">Vytvořte šablonu stránky s názvem **Šablona potvrzení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="30149-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="30149-125">V úseku **Hlavní** výchozí stránky přidejte modul potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="30149-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="30149-126">V modulu potvrzení objednávky přidejte modul doporučení.</span><span class="sxs-lookup"><span data-stu-id="30149-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="30149-127">Uložení a náhled šablony.</span><span class="sxs-lookup"><span data-stu-id="30149-127">Save and preview the template.</span></span> <span data-ttu-id="30149-128">Modul potvrzení objednávky by neměl být zobrazen, protože vyžaduje kontext pro číslo potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="30149-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="30149-129">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="30149-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="30149-130">Šablonu potvrzení objednávky, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **stránka potvrzení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="30149-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="30149-131">Přidejte výchozí stránku do osnovy stránky.</span><span class="sxs-lookup"><span data-stu-id="30149-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="30149-132">V oblasti **Záhlaví** přidejte fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="30149-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="30149-133">V oblasti **Zápatí** přidejte fragment zápatí.</span><span class="sxs-lookup"><span data-stu-id="30149-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="30149-134">V úseku **Hlavní** přidejte modul potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="30149-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="30149-135">V podokně vlastností modulu potvrzení objednávky přidejte **Potvrzení objednávky**pro záhlaví.</span><span class="sxs-lookup"><span data-stu-id="30149-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="30149-136">Pod modulem potvrzení objednávky přidejte modul doporučení a nakonfigurujte jej tak, aby používal nastavení **Nové** a **Nejlépe prodávané**.</span><span class="sxs-lookup"><span data-stu-id="30149-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="30149-137">Uložte a zobrazte náhled stránky, zarezervujte ji a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="30149-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30149-138">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="30149-138">Additional resources</span></span>

[<span data-ttu-id="30149-139">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="30149-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="30149-140">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="30149-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="30149-141">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="30149-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="30149-142">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="30149-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="30149-143">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="30149-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="30149-144">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="30149-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="30149-145">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="30149-145">Footer module</span></span>](author-footer-module.md)
