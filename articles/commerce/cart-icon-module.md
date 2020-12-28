---
title: Ikona modulu košíku
description: Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410942"
---
# <a name="cart-icon-module"></a><span data-ttu-id="0eb2a-103">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="0eb2a-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0eb2a-104">Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0eb2a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="0eb2a-105">Overview</span></span>

<span data-ttu-id="0eb2a-106">Ikona košíku – ikona košíku představuje košík v modulu záhlaví stránky a zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="0eb2a-107">Modul ikony košíku zobrazuje také souhrn nákupního košíku (označovaný také jako mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="0eb2a-108">Mini košík poskytuje uživateli souhrn položek v košíku, aniž by bylo nutné přejít na stránku košíku.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="0eb2a-109">Kromě toho umožňuje uživateli přímo přejít na stránku pokadny, pokud jsou spokojeni se souhrnem.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="0eb2a-110">Tato možnost snižuje počet navigačních stránek a provádí platbu rychleji.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="0eb2a-111">Podpora modulu ikony košíku je k dispozici v Dynamics 365 Commerce vydání 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="0eb2a-112">Následující obrázek znázorňuje příklad modulu ikony vozíku, který zobrazuje mini vozík v záhlaví Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Příklad modulu ikony košíku](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="0eb2a-114">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="0eb2a-114">Module properties</span></span>

- <span data-ttu-id="0eb2a-115">**Zobrazit Mini košík** – je-li nastavena hodnota true, umožňuje tato vlastnost zobrazit souhrn nákupního košíku (mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="0eb2a-116">Tato funkce je podporována pouze pro porty zobrazení na ploše.</span><span class="sxs-lookup"><span data-stu-id="0eb2a-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="0eb2a-117">Přidání modulu ikony košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="0eb2a-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="0eb2a-118">Chcete-li přidat modul ikony nákupního košíku, přečtěte si [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="0eb2a-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0eb2a-119">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0eb2a-119">Additional resources</span></span>

[<span data-ttu-id="0eb2a-120">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="0eb2a-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0eb2a-121">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="0eb2a-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0eb2a-122">Platební modul</span><span class="sxs-lookup"><span data-stu-id="0eb2a-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0eb2a-123">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="0eb2a-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0eb2a-124">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="0eb2a-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0eb2a-125">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="0eb2a-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="0eb2a-126">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="0eb2a-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0eb2a-127">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="0eb2a-127">Gift card module</span></span>](add-giftcard.md)
