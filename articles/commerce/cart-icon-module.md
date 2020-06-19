---
title: Ikona modulu košíku
description: Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411082"
---
# <a name="cart-icon-module"></a><span data-ttu-id="8ced2-103">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="8ced2-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ced2-104">Tohle téma se zabývá modulem ikony košiku a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ced2-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ced2-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="8ced2-105">Overview</span></span>

<span data-ttu-id="8ced2-106">Ikona košíku – ikona košíku představuje košík v modulu záhlaví stránky a zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="8ced2-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="8ced2-107">Modul ikony košíku zobrazuje také souhrn nákupního košíku (označovaný také jako mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="8ced2-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="8ced2-108">Mini košík poskytuje uživateli souhrn položek v košíku, aniž by bylo nutné přejít na stránku košíku.</span><span class="sxs-lookup"><span data-stu-id="8ced2-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="8ced2-109">Kromě toho umožňuje uživateli přímo přejít na stránku pokadny, pokud jsou spokojeni se souhrnem.</span><span class="sxs-lookup"><span data-stu-id="8ced2-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="8ced2-110">Tato možnost snižuje počet navigačních stránek a provádí platbu rychleji.</span><span class="sxs-lookup"><span data-stu-id="8ced2-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="8ced2-111">Následující obrázek znázorňuje příklad modulu ikony vozíku, který zobrazuje mini vozík v záhlaví Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="8ced2-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Příklad modulu ikony košíku](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="8ced2-113">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="8ced2-113">Module properties</span></span>

- <span data-ttu-id="8ced2-114">**Zobrazit Mini košík** – je-li nastavena hodnota true, umožňuje tato vlastnost zobrazit souhrn nákupního košíku (mini košík) při přechodu na ikonu košíku.</span><span class="sxs-lookup"><span data-stu-id="8ced2-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="8ced2-115">Tato funkce je podporována pouze pro porty zobrazení na ploše.</span><span class="sxs-lookup"><span data-stu-id="8ced2-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="8ced2-116">Přidání modulu ikony košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="8ced2-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="8ced2-117">Chcete-li přidat modul ikony nákupního košíku, přečtěte si [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="8ced2-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8ced2-118">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="8ced2-118">Additional resources</span></span>

[<span data-ttu-id="8ced2-119">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="8ced2-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8ced2-120">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="8ced2-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8ced2-121">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="8ced2-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8ced2-122">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="8ced2-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8ced2-123">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="8ced2-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8ced2-124">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="8ced2-124">Footer module</span></span>](author-footer-module.md)
