---
title: Stránky a moduly správy účtů
description: Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785369"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="2e3ed-103">Stránky a moduly správy účtů</span><span class="sxs-lookup"><span data-stu-id="2e3ed-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2e3ed-104">Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e3ed-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="2e3ed-105">Overview</span></span>

<span data-ttu-id="2e3ed-106">Správa účtů představuje skupinu stránek, které se používají ke správě informací o uživatelských účtech v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="2e3ed-107">Stránky správy účtů zahrnují cílovou stránku správy účtu, stránku uživatelského profilu, stránku uživatelské adresy, stránku historie objednávek, stránku podrobností objednávky, věrnostní stránku a seznam přání.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="2e3ed-108">Cílová stránka správy obchodního vztahu</span><span class="sxs-lookup"><span data-stu-id="2e3ed-108">Account management landing page</span></span>

<span data-ttu-id="2e3ed-109">Cílová stránka správy účtu používá následující moduly:</span><span class="sxs-lookup"><span data-stu-id="2e3ed-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="2e3ed-110">**Umístění obsahu** – Jedná se o modul kontejneru, který obsahuje všechny moduly na cílové stránce správy účtu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="2e3ed-111">**Položka přivítání v účtu**– Tento modul slouží k poskytnutí uvítací zprávy na stránce správy účtu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="2e3ed-112">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="2e3ed-113">Vlastnost **Velikost dlaždice** definuje šířku modulu v modulu umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="2e3ed-114">Hodnoty jsou v rozsahu **1** až **12**, kde **12** představuje celou šířku kontejneru umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="2e3ed-115">**Položka podání objednávky účtu** – Tento modul se používá k vytvoření souhrnu počtu objednávek, které byly podány uživatelským účtem.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="2e3ed-116">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="2e3ed-117">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku historie objednávek.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="2e3ed-118">**Položka umístění profilu účtu** – Tento modul slouží k poskytnutí souhrnu profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="2e3ed-119">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="2e3ed-120">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="2e3ed-121">**Požadovaná položka účtu** – Tento modul slouží k poskytnutí souhrnu položek v seznamu přání zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="2e3ed-122">Může například udávat „V seznamu přání máte 10 položek“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="2e3ed-123">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="2e3ed-124">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="2e3ed-125">**Položka adresy účtu** – Tento modul slouží k poskytnutí souhrnu adres uživatele.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="2e3ed-126">Může například udávat „Ve vašem účtu byly přidány 2 adresy“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="2e3ed-127">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="2e3ed-128">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku adresy uživatele.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="2e3ed-129">**Věrnostní položka účtu** – Tento modul slouží k zobrazení informací o věrnostních programech a odkazování na ně.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="2e3ed-130">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“ a další odkaz „stát se členem“.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="2e3ed-131">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na věrnostní stránku.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="2e3ed-132">Odkaz "stát se členem" by měl být nakonfigurován pro přesměrování na stránku, na které se uživatelé mohou připojit k věrnostnímu programu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="2e3ed-133">Stránka historie objednávek</span><span class="sxs-lookup"><span data-stu-id="2e3ed-133">Order history page</span></span>

<span data-ttu-id="2e3ed-134">Stránka historie objednávek využívá modul historie objednávek k zobrazení všech nedávných objednávek, které uživatel podal.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="2e3ed-135">Stránka podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="2e3ed-135">Order details page</span></span>

<span data-ttu-id="2e3ed-136">Stránka podrobností objednávky poskytuje podrobné informace pro každou objednávku a je přístupná ze stránky historie objednávek.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="2e3ed-137">Používá modul podrobností objednávek, který vyžaduje ID prodeje nebo ID transakce k načtení podrobností objednávky.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="2e3ed-138">Stránka profilu uživatele</span><span class="sxs-lookup"><span data-stu-id="2e3ed-138">User profile page</span></span>

<span data-ttu-id="2e3ed-139">Na stránce profilu uživatele se zobrazují podrobnosti o účtu uživatele, jako je jméno nebo e-mailová adresa uživatele.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-139">The user profile page shows user account details, such as user's name and email address.</span></span> <span data-ttu-id="2e3ed-140">Používá modul profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-140">It uses the user profile module.</span></span> <span data-ttu-id="2e3ed-141">Ačkoli e-mailovou adresu nelze odebrat, je možné ji upravit.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-141">Although the email address can't be removed, it can be edited.</span></span>

### <a name="user-address-page"></a><span data-ttu-id="2e3ed-142">Stránka adresy uživatele</span><span class="sxs-lookup"><span data-stu-id="2e3ed-142">User address page</span></span>

<span data-ttu-id="2e3ed-143">Stránka adresy uživatele zobrazuje seznam adres, které jsou přidruženy k danému uživatelskému účtu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-143">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="2e3ed-144">Uživatel buď tyto adresy poskytl na pokladně, nebo je přidal přímo na tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-144">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="2e3ed-145">Modul adresy uživatele se používá k přidávání a úpravám adres, k nastavení primární adresy a k vykreslení existujících adres na stránce.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-145">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="2e3ed-146">Stránka seznamu přání</span><span class="sxs-lookup"><span data-stu-id="2e3ed-146">Wish list page</span></span>

<span data-ttu-id="2e3ed-147">Na stránce seznamu přání se zobrazují položky, které byly přidány do seznamu přání zákazníků.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-147">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="2e3ed-148">Pomocí modulu seznamu přání lze vykreslit položky v seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-148">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="2e3ed-149">Stránka věrnostního programu</span><span class="sxs-lookup"><span data-stu-id="2e3ed-149">Loyalty page</span></span>

<span data-ttu-id="2e3ed-150">Věrnostní stránka umožňuje zákazníkům připojit se k věrnostnímu programu, nebo v případě, že již jsou členy věrnostního programu, zobrazit podrobné informace o programu.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-150">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="2e3ed-151">Mohou také zobrazit body, které získali a které byly uplatněny v posledních transakcích.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-151">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e3ed-152">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2e3ed-152">Additional resources</span></span>

[<span data-ttu-id="2e3ed-153">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="2e3ed-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2e3ed-154">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="2e3ed-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2e3ed-155">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="2e3ed-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2e3ed-156">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="2e3ed-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2e3ed-157">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="2e3ed-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2e3ed-158">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="2e3ed-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2e3ed-159">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="2e3ed-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2e3ed-160">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="2e3ed-160">Footer module</span></span>](author-footer-module.md)
