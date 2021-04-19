---
title: Přehled knihovny modulů
description: Toto téma poskytuje přehled o knihovně modulů Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795326"
---
# <a name="module-library-overview"></a><span data-ttu-id="01905-103">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="01905-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01905-104">Toto téma poskytuje přehled o knihovně modulů Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="01905-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="01905-105">Knihovna modulů Dynamics 365 Commerce je kolekce modulů, které lze použít k vytvoření webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="01905-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="01905-106">Moduly mají aspekty uživatelského rozhraní (UI) a aspekty funkčního chování.</span><span class="sxs-lookup"><span data-stu-id="01905-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="01905-107">Motivy lze použít pro moduly v knihovně modulů ke změně jejich vzhledu.</span><span class="sxs-lookup"><span data-stu-id="01905-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="01905-108">Motivy používají soubor Cascading Style Sheets (CSS).</span><span class="sxs-lookup"><span data-stu-id="01905-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="01905-109">Motiv fiktivního webu e-Commerce s názvem Fabrikam je poskytován jako součást knihovny modulů a lze jej použít jako odkaz.</span><span class="sxs-lookup"><span data-stu-id="01905-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="01905-110">Moduly knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="01905-110">Module library modules</span></span>

<span data-ttu-id="01905-111">V knihovně modulů jsou uvedeny následující typy modulů:</span><span class="sxs-lookup"><span data-stu-id="01905-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="01905-112">**Moduly kontejneru** – modul kontejneru je jednoduchý modul, který funguje jako hostitel pro ostatní moduly.</span><span class="sxs-lookup"><span data-stu-id="01905-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="01905-113">Řídí rozvržení modulů, které jsou v něm obsažené.</span><span class="sxs-lookup"><span data-stu-id="01905-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="01905-114">**Marketingové moduly** – marketingové moduly zahrnují blok obsahu, blok textu, přehrávač videa a karuselové moduly.</span><span class="sxs-lookup"><span data-stu-id="01905-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="01905-115">Všechny tyto moduly lze použít k předvedení obsahu.</span><span class="sxs-lookup"><span data-stu-id="01905-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="01905-116">Lze je umístit na jakoukoliv stránku a jsou řízeny daty ze systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="01905-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="01905-117">**Moduly záhlaví a zápatí** – moduly záhlaví a zápatí se zobrazí v záhlaví a zápatí všech stránek webu.</span><span class="sxs-lookup"><span data-stu-id="01905-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="01905-118">Tyto moduly lze konfigurovat podle požadavků pomocí vlastností.</span><span class="sxs-lookup"><span data-stu-id="01905-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="01905-119">**Moduly vyhledávání** – produkty mohou být zjištěny pomocí vyhledávacího modulu v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="01905-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="01905-120">Výsledky hledání se zobrazí na stránce výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="01905-120">Search results appear on the search results page.</span></span> <span data-ttu-id="01905-121">Produkty lze také nalézt na stránkách kategorie, což jsou vyhrazené stránky pro každou kategorii, která je podporována v hierarchii navigace kanálu.</span><span class="sxs-lookup"><span data-stu-id="01905-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="01905-122">Kromě toho lze pomocí zpřesnění modulů dále vyfiltrovat výsledky hledání ve výsledcích vyhledávání a na stránkách kategorií.</span><span class="sxs-lookup"><span data-stu-id="01905-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="01905-123">**Moduly stránek podrobností produktu** – stránky podrobností produktu používají k zobrazení informací o produktu několik modulů.</span><span class="sxs-lookup"><span data-stu-id="01905-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="01905-124">Modul buy boxu umožňuje zákazníkům zobrazit produkty a přidat je do košíku.</span><span class="sxs-lookup"><span data-stu-id="01905-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="01905-125">Další moduly, jako například modul technické specifikace, zobrazují podrobné informace o produktu.</span><span class="sxs-lookup"><span data-stu-id="01905-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="01905-126">Modul hodnocení a recenze slouží k zobrazení a zajištění recenzí.</span><span class="sxs-lookup"><span data-stu-id="01905-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="01905-127">**Modul nákup online, vyzvednutí v obchodě** – Modul nákup online, vyzvednutí v obchodě je integrován se službou Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="01905-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="01905-128">Lze jej použít k vyhledání blízkých obchodů, kde si zákazníci mohou vyzvednout zakoupené produkty.</span><span class="sxs-lookup"><span data-stu-id="01905-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="01905-129">**Moduly nákupu** – moduly nákupu zahrnují modul košíku, který lze použít pro přidání položek do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="01905-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="01905-130">V modulu pokladny je zachycena dodací adresa, možnosti dodání a informace o dárkových poukazech, věrnostních programech a kreditních kartách, takže objednávku lze zpracovat.</span><span class="sxs-lookup"><span data-stu-id="01905-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="01905-131">Po umístění objednávky lze pomocí modulu potvrzení objednávky zobrazit podrobnosti o potvrzení.</span><span class="sxs-lookup"><span data-stu-id="01905-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="01905-132">**Moduly správy účtů** – modul přihlášení umožňuje zákazníkům přihlásit se k existujícímu účtu a modul přihlášení jim umožňuje vytvořit nový účet.</span><span class="sxs-lookup"><span data-stu-id="01905-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="01905-133">Po vytvoření účtu lze pomocí modulu historie objednávek zobrazit nedávné objednávky a pomocí modulu podrobnosti objednávky lze zobrazit podrobnosti objednávky.</span><span class="sxs-lookup"><span data-stu-id="01905-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="01905-134">**Modul doporučení** – doporučení se zobrazují pomocí modulu umístění produktu.</span><span class="sxs-lookup"><span data-stu-id="01905-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="01905-135">Tento modul podporuje seznamy s algoritmy a redakčními moduly, které lze prezentovat na libovolné stránce.</span><span class="sxs-lookup"><span data-stu-id="01905-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01905-136">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="01905-136">Additional resources</span></span>

[<span data-ttu-id="01905-137">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="01905-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="01905-138">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="01905-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="01905-139">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="01905-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="01905-140">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="01905-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="01905-141">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="01905-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="01905-142">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="01905-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="01905-143">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="01905-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]