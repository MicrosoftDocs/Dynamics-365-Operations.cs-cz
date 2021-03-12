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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 138c256b56593c4fafb20050a97e614fa584597c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997818"
---
# <a name="cart-icon-module"></a><span data-ttu-id="8eda4-103">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="8eda4-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8eda4-104">Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8eda4-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8eda4-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="8eda4-105">Overview</span></span>

<span data-ttu-id="8eda4-106">Ikona košíku – ikona košíku představuje košík v modulu záhlaví stránky a zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="8eda4-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="8eda4-107">Modul ikony košíku zobrazuje také souhrn nákupního košíku (označovaný také jako mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="8eda4-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="8eda4-108">Mini košík poskytuje uživateli souhrn položek v košíku, aniž by bylo nutné přejít na stránku košíku.</span><span class="sxs-lookup"><span data-stu-id="8eda4-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="8eda4-109">Kromě toho umožňuje uživateli přímo přejít na stránku pokadny, pokud jsou spokojeni se souhrnem.</span><span class="sxs-lookup"><span data-stu-id="8eda4-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="8eda4-110">Tato možnost snižuje počet navigačních stránek a provádí platbu rychleji.</span><span class="sxs-lookup"><span data-stu-id="8eda4-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="8eda4-111">Podpora modulu ikony košíku je k dispozici v Dynamics 365 Commerce vydání 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="8eda4-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="8eda4-112">Následující obrázek znázorňuje příklad modulu ikony vozíku, který zobrazuje mini vozík v záhlaví Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="8eda4-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Příklad modulu ikony košíku](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="8eda4-114">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="8eda4-114">Module properties</span></span>

- <span data-ttu-id="8eda4-115">**Zobrazit Mini košík** – je-li nastavena hodnota true, umožňuje tato vlastnost zobrazit souhrn nákupního košíku (mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="8eda4-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="8eda4-116">Tato funkce je podporována pouze pro porty zobrazení na ploše.</span><span class="sxs-lookup"><span data-stu-id="8eda4-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="8eda4-117">Přidání modulu ikony košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="8eda4-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="8eda4-118">Chcete-li přidat modul ikony nákupního košíku, přečtěte si [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="8eda4-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8eda4-119">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="8eda4-119">Additional resources</span></span>

[<span data-ttu-id="8eda4-120">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="8eda4-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8eda4-121">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="8eda4-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8eda4-122">Platební modul</span><span class="sxs-lookup"><span data-stu-id="8eda4-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8eda4-123">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="8eda4-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="8eda4-124">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="8eda4-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8eda4-125">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="8eda4-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="8eda4-126">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="8eda4-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8eda4-127">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="8eda4-127">Gift card module</span></span>](add-giftcard.md)
