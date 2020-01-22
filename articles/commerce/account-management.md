---
title: Stránky a moduly správy účtů
description: Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885802"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="34224-103">Stránky a moduly správy účtů</span><span class="sxs-lookup"><span data-stu-id="34224-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="34224-104">Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34224-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34224-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="34224-105">Overview</span></span>

<span data-ttu-id="34224-106">Správa účtů představuje skupinu stránek, které se používají ke správě informací o uživatelských účtech v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34224-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="34224-107">Stránky správy účtů zahrnují cílovou stránku správy účtu, stránku uživatelského profilu, stránku uživatelské adresy, stránku historie objednávek, stránku podrobností objednávky, věrnostní stránku a seznam přání.</span><span class="sxs-lookup"><span data-stu-id="34224-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="34224-108">Cílová stránka správy obchodního vztahu</span><span class="sxs-lookup"><span data-stu-id="34224-108">Account management landing page</span></span>

<span data-ttu-id="34224-109">Cílová stránka správy účtu používá následující moduly:</span><span class="sxs-lookup"><span data-stu-id="34224-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="34224-110">**Umístění obsahu** – Jedná se o modul kontejneru, který obsahuje všechny moduly na cílové stránce správy účtu.</span><span class="sxs-lookup"><span data-stu-id="34224-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="34224-111">**Položka přivítání v účtu**– Tento modul slouží k poskytnutí uvítací zprávy na stránce správy účtu.</span><span class="sxs-lookup"><span data-stu-id="34224-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="34224-112">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice.</span><span class="sxs-lookup"><span data-stu-id="34224-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="34224-113">Vlastnost **Velikost dlaždice** definuje šířku modulu v modulu umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="34224-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="34224-114">Hodnoty jsou v rozsahu **1** až **12**, kde **12** představuje celou šířku kontejneru umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="34224-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="34224-115">**Položka podání objednávky účtu** – Tento modul se používá k vytvoření souhrnu počtu objednávek, které byly podány uživatelským účtem.</span><span class="sxs-lookup"><span data-stu-id="34224-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="34224-116">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="34224-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="34224-117">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku historie objednávek.</span><span class="sxs-lookup"><span data-stu-id="34224-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="34224-118">**Položka umístění profilu účtu** – Tento modul slouží k poskytnutí souhrnu profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="34224-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="34224-119">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="34224-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="34224-120">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="34224-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="34224-121">**Požadovaná položka účtu** – Tento modul slouží k poskytnutí souhrnu položek v seznamu přání zákazníka.</span><span class="sxs-lookup"><span data-stu-id="34224-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="34224-122">Může například udávat „V seznamu přání máte 10 položek“.</span><span class="sxs-lookup"><span data-stu-id="34224-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="34224-123">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="34224-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="34224-124">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="34224-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="34224-125">**Položka adresy účtu** – Tento modul slouží k poskytnutí souhrnu adres uživatele.</span><span class="sxs-lookup"><span data-stu-id="34224-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="34224-126">Může například udávat „Ve vašem účtu byly přidány 2 adresy“.</span><span class="sxs-lookup"><span data-stu-id="34224-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="34224-127">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="34224-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="34224-128">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku adresy uživatele.</span><span class="sxs-lookup"><span data-stu-id="34224-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="34224-129">**Věrnostní položka účtu** – Tento modul slouží k zobrazení informací o věrnostních programech a odkazování na ně.</span><span class="sxs-lookup"><span data-stu-id="34224-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="34224-130">Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“ a další odkaz „stát se členem“.</span><span class="sxs-lookup"><span data-stu-id="34224-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="34224-131">Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na věrnostní stránku.</span><span class="sxs-lookup"><span data-stu-id="34224-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="34224-132">Odkaz "stát se členem" by měl být nakonfigurován pro přesměrování na stránku, na které se uživatelé mohou připojit k věrnostnímu programu.</span><span class="sxs-lookup"><span data-stu-id="34224-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="34224-133">Stránka historie objednávek</span><span class="sxs-lookup"><span data-stu-id="34224-133">Order history page</span></span>

<span data-ttu-id="34224-134">Stránka historie objednávek využívá modul historie objednávek k zobrazení všech nedávných objednávek, které uživatel podal.</span><span class="sxs-lookup"><span data-stu-id="34224-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="34224-135">Stránka podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="34224-135">Order details page</span></span>

<span data-ttu-id="34224-136">Stránka podrobností objednávky poskytuje podrobné informace pro každou objednávku a je přístupná ze stránky historie objednávek.</span><span class="sxs-lookup"><span data-stu-id="34224-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="34224-137">Používá modul podrobností objednávek, který vyžaduje ID prodeje nebo ID transakce k načtení podrobností objednávky.</span><span class="sxs-lookup"><span data-stu-id="34224-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="34224-138">Stránka profilu uživatele</span><span class="sxs-lookup"><span data-stu-id="34224-138">User profile page</span></span>

<span data-ttu-id="34224-139">Na stránce profilu uživatele se zobrazují podrobnosti o účtu uživatele, jako je jméno nebo e-mailová adresa uživatele.</span><span class="sxs-lookup"><span data-stu-id="34224-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="34224-140">Používá modul profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="34224-140">It uses the user profile module.</span></span> <span data-ttu-id="34224-141">Ačkoli e-mailovou adresu nelze odebrat, je možné ji upravit.</span><span class="sxs-lookup"><span data-stu-id="34224-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="34224-142">Stránka profilu uživatele také zobrazuje uživatelské předvolby, které umožňují uživateli přihlásit nebo odhlásit odběr některých funkcí, jako je přizpůsobení seznamů doporučení.</span><span class="sxs-lookup"><span data-stu-id="34224-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="34224-143">Stránka adresy uživatele</span><span class="sxs-lookup"><span data-stu-id="34224-143">User address page</span></span>

<span data-ttu-id="34224-144">Stránka adresy uživatele zobrazuje seznam adres, které jsou přidruženy k danému uživatelskému účtu.</span><span class="sxs-lookup"><span data-stu-id="34224-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="34224-145">Uživatel buď tyto adresy poskytl na pokladně, nebo je přidal přímo na tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="34224-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="34224-146">Modul adresy uživatele se používá k přidávání a úpravám adres, k nastavení primární adresy a k vykreslení existujících adres na stránce.</span><span class="sxs-lookup"><span data-stu-id="34224-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="34224-147">Stránka seznamu přání</span><span class="sxs-lookup"><span data-stu-id="34224-147">Wish list page</span></span>

<span data-ttu-id="34224-148">Na stránce seznamu přání se zobrazují položky, které byly přidány do seznamu přání zákazníků.</span><span class="sxs-lookup"><span data-stu-id="34224-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="34224-149">Pomocí modulu seznamu přání lze vykreslit položky v seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="34224-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="34224-150">Stránka věrnostního programu</span><span class="sxs-lookup"><span data-stu-id="34224-150">Loyalty page</span></span>

<span data-ttu-id="34224-151">Věrnostní stránka umožňuje zákazníkům připojit se k věrnostnímu programu, nebo v případě, že již jsou členy věrnostního programu, zobrazit podrobné informace o programu.</span><span class="sxs-lookup"><span data-stu-id="34224-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="34224-152">Mohou také zobrazit body, které získali a které byly uplatněny v posledních transakcích.</span><span class="sxs-lookup"><span data-stu-id="34224-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34224-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="34224-153">Additional resources</span></span>

[<span data-ttu-id="34224-154">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="34224-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="34224-155">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="34224-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="34224-156">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="34224-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="34224-157">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="34224-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="34224-158">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="34224-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="34224-159">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="34224-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="34224-160">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="34224-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="34224-161">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="34224-161">Footer module</span></span>](author-footer-module.md)
