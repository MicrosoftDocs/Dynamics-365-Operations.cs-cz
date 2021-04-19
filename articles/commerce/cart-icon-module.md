---
title: Ikona modulu košíku
description: Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793074"
---
# <a name="cart-icon-module"></a><span data-ttu-id="ea508-103">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="ea508-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea508-104">Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea508-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ea508-105">Ikona košíku – ikona košíku představuje košík v modulu záhlaví stránky a zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="ea508-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="ea508-106">Modul ikony košíku zobrazuje také souhrn nákupního košíku (označovaný také jako mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="ea508-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="ea508-107">Mini košík poskytuje uživateli souhrn položek v košíku, aniž by bylo nutné přejít na stránku košíku.</span><span class="sxs-lookup"><span data-stu-id="ea508-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="ea508-108">Kromě toho umožňuje uživateli přímo přejít na stránku pokadny, pokud jsou spokojeni se souhrnem.</span><span class="sxs-lookup"><span data-stu-id="ea508-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="ea508-109">Tato možnost snižuje počet navigačních stránek a provádí platbu rychleji.</span><span class="sxs-lookup"><span data-stu-id="ea508-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea508-110">Podpora modulu ikony košíku je k dispozici v Dynamics 365 Commerce vydání 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="ea508-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="ea508-111">Následující obrázek znázorňuje příklad modulu ikony vozíku, který zobrazuje mini vozík v záhlaví Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="ea508-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Příklad modulu ikony košíku](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="ea508-113">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="ea508-113">Module properties</span></span>

- <span data-ttu-id="ea508-114">**Zobrazit Mini košík** – je-li nastavena hodnota true, umožňuje tato vlastnost zobrazit souhrn nákupního košíku (mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="ea508-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="ea508-115">Tato funkce je podporována pouze pro porty zobrazení na ploše.</span><span class="sxs-lookup"><span data-stu-id="ea508-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="ea508-116">Přidání modulu ikony košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="ea508-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="ea508-117">Chcete-li přidat modul ikony nákupního košíku, přečtěte si [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="ea508-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea508-118">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ea508-118">Additional resources</span></span>

[<span data-ttu-id="ea508-119">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="ea508-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ea508-120">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="ea508-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ea508-121">Platební modul</span><span class="sxs-lookup"><span data-stu-id="ea508-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="ea508-122">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="ea508-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="ea508-123">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="ea508-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="ea508-124">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="ea508-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="ea508-125">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="ea508-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ea508-126">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="ea508-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]