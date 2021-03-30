---
title: Moduly a stránky správy obchodního vztahu
description: Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206624"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="2c04d-103">Moduly a stránky správy obchodního vztahu</span><span class="sxs-lookup"><span data-stu-id="2c04d-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c04d-104">Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c04d-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c04d-105">Správa účtů představuje skupinu stránek, které se používají ke správě informací o uživatelských účtech v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c04d-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="2c04d-106">Stránky správy účtů zahrnují cílovou stránku správy účtu, stránku uživatelského profilu, stránku uživatelské adresy, stránku historie objednávek, stránku podrobností objednávky, věrnostní stránku a seznam přání.</span><span class="sxs-lookup"><span data-stu-id="2c04d-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="2c04d-107">Cílová stránka správy obchodního vztahu</span><span class="sxs-lookup"><span data-stu-id="2c04d-107">Account management landing page</span></span>

<span data-ttu-id="2c04d-108">Cílová stránka správy účtu používá následující moduly:</span><span class="sxs-lookup"><span data-stu-id="2c04d-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="2c04d-109">**Kontejner** – všechny moduly cílových stránek správy účtů by měly být umístěny v rámci kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2c04d-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="2c04d-110">**Dlaždicce přivítání v účtu** – Tento modul slouží k poskytnutí uvítací zprávy na stránce správy účtu.</span><span class="sxs-lookup"><span data-stu-id="2c04d-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="2c04d-111">Obsahuje vlastnosti pro záhlaví.</span><span class="sxs-lookup"><span data-stu-id="2c04d-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="2c04d-112">**Obecná dlaždice účtu** – Tento modul lze použít k zadání záhlaví a odkazů na stránky pro správu účtů, jako jsou například stránky "Historie objednávek" nebo "Můj profil".</span><span class="sxs-lookup"><span data-stu-id="2c04d-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="2c04d-113">Pomocí generického modulu dlaždice lze konfigurovat dlaždici pro libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="2c04d-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="2c04d-114">Ve společnosti Fabrikam se tento modul používá pro odkazy na stránce Historie objednávek a můj profil na cílové stránce správy účtů.</span><span class="sxs-lookup"><span data-stu-id="2c04d-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="2c04d-115">**Dlaždice požadovanýcg položek účtu** – Tento modul slouží k poskytnutí souhrnu položek v seznamu přání zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2c04d-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="2c04d-116">Může například udávat „V seznamu přání máte 10 položek“.</span><span class="sxs-lookup"><span data-stu-id="2c04d-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="2c04d-117">Zahrnuje vlastnosti pro záhlaví a odkaz „Zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="2c04d-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="2c04d-118">Odkaz „Zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="2c04d-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="2c04d-119">**Dlaždice adresy účtu** – Tento modul slouží k poskytnutí souhrnu adres uživatele.</span><span class="sxs-lookup"><span data-stu-id="2c04d-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="2c04d-120">Může například udávat „Ve vašem účtu byly přidány 2 adresy“.</span><span class="sxs-lookup"><span data-stu-id="2c04d-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="2c04d-121">Zahrnuje vlastnosti pro záhlaví a odkaz „Zobrazit podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="2c04d-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="2c04d-122">Odkaz „Zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku adresy uživatele.</span><span class="sxs-lookup"><span data-stu-id="2c04d-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="2c04d-123">**Věrnostní dlaždice účtu** – Tento modul slouží k zobrazení informací o věrnostních programech a odkazování na ně.</span><span class="sxs-lookup"><span data-stu-id="2c04d-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="2c04d-124">Tato dlaždice má dva stavy: jeden z těchto stavů obsahuje odkazy na připojení k věrnostnímu programu, pokud uživatel již není členem.</span><span class="sxs-lookup"><span data-stu-id="2c04d-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="2c04d-125">Pokud je uživatel již členem, zobrazí se v poli jiný stav odkazy na stránku věrnostní podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="2c04d-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="2c04d-126">Vlastnosti zahrnují nadpis, odkaz "Registrace" a odkaz "Zobrazit věrnostní program".</span><span class="sxs-lookup"><span data-stu-id="2c04d-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="2c04d-127">Odkaz „Zobrazit věrnostní program“ by měl být nakonfigurován pro přesměrování na věrnostní stránku.</span><span class="sxs-lookup"><span data-stu-id="2c04d-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="2c04d-128">Odkaz "Registrace" by měl být nakonfigurován pro přesměrování na stránku, na které se uživatelé mohou připojit k věrnostnímu programu.</span><span class="sxs-lookup"><span data-stu-id="2c04d-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="2c04d-129">Stránka historie objednávek</span><span class="sxs-lookup"><span data-stu-id="2c04d-129">Order history page</span></span>

<span data-ttu-id="2c04d-130">Stránka historie objednávek využívá modul historie objednávek k zobrazení všech nedávných objednávek, které uživatel podal.</span><span class="sxs-lookup"><span data-stu-id="2c04d-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="2c04d-131">Stránka podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="2c04d-131">Order details page</span></span>

<span data-ttu-id="2c04d-132">Stránka podrobností objednávky poskytuje podrobné informace pro každou objednávku a je přístupná ze stránky historie objednávek.</span><span class="sxs-lookup"><span data-stu-id="2c04d-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="2c04d-133">Používá modul podrobností objednávek, který vyžaduje ID prodeje nebo ID transakce k načtení podrobností objednávky.</span><span class="sxs-lookup"><span data-stu-id="2c04d-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="2c04d-134">Stránka profilu uživatele</span><span class="sxs-lookup"><span data-stu-id="2c04d-134">User profile page</span></span>

<span data-ttu-id="2c04d-135">Na stránce profilu uživatele se zobrazují podrobnosti o účtu uživatele, jako je jméno nebo e-mailová adresa uživatele.</span><span class="sxs-lookup"><span data-stu-id="2c04d-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="2c04d-136">Používá podrobnosti profilu uživatele a moduly úprav profilu uživatele.</span><span class="sxs-lookup"><span data-stu-id="2c04d-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="2c04d-137">Ačkoli e-mailovou adresu nelze odebrat, je možné ji upravit.</span><span class="sxs-lookup"><span data-stu-id="2c04d-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="2c04d-138">Stránka profilu uživatele také zobrazuje uživatelské předvolby, které umožňují uživateli přihlásit nebo odhlásit odběr některých funkcí, jako je přizpůsobení seznamů doporučení.</span><span class="sxs-lookup"><span data-stu-id="2c04d-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="2c04d-139">Stránka adresy uživatele</span><span class="sxs-lookup"><span data-stu-id="2c04d-139">User address page</span></span>

<span data-ttu-id="2c04d-140">Stránka adresy uživatele zobrazuje seznam adres, které jsou přidruženy k danému uživatelskému účtu.</span><span class="sxs-lookup"><span data-stu-id="2c04d-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="2c04d-141">Uživatel buď tyto adresy poskytl na pokladně, nebo je přidal přímo na tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="2c04d-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="2c04d-142">Modul adresy uživatele se používá k přidávání a úpravám adres, k nastavení primární adresy a k vykreslení existujících adres na stránce.</span><span class="sxs-lookup"><span data-stu-id="2c04d-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="2c04d-143">Stránka seznamu přání</span><span class="sxs-lookup"><span data-stu-id="2c04d-143">Wish list page</span></span>

<span data-ttu-id="2c04d-144">Na stránce seznamu přání se zobrazují položky, které byly přidány do seznamu přání zákazníků.</span><span class="sxs-lookup"><span data-stu-id="2c04d-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="2c04d-145">Pomocí modulu seznamu přání lze vykreslit položky v seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="2c04d-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="2c04d-146">Stránka věrnostního programu</span><span class="sxs-lookup"><span data-stu-id="2c04d-146">Loyalty page</span></span>

<span data-ttu-id="2c04d-147">Věrnostní stránka umožňuje zákazníkům zobrazit podrobnosti věrnostního programu v případě, že již jsou členy věrnostního programu.</span><span class="sxs-lookup"><span data-stu-id="2c04d-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="2c04d-148">Mohou také zobrazit body, které získali a které byly uplatněny v posledních transakcích.</span><span class="sxs-lookup"><span data-stu-id="2c04d-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="2c04d-149">Stránka využívá modul podrobnosti věrnostního programu k předvedení podrobností věrnostního programu.</span><span class="sxs-lookup"><span data-stu-id="2c04d-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="2c04d-150">Chcete-li se připojit k věrnostnímu programu, můžete vytvořit marketingovou stránku s moduly věrnostních zápisů a věrnostních podmínek.</span><span class="sxs-lookup"><span data-stu-id="2c04d-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="2c04d-151">Pokud uživatel není členem věrnostního programu, tyto moduly umožní uživateli, aby se přihlásil.</span><span class="sxs-lookup"><span data-stu-id="2c04d-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c04d-152">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2c04d-152">Additional resources</span></span>

[<span data-ttu-id="2c04d-153">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="2c04d-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2c04d-154">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="2c04d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2c04d-155">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="2c04d-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2c04d-156">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="2c04d-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2c04d-157">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="2c04d-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2c04d-158">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="2c04d-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2c04d-159">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="2c04d-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2c04d-160">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="2c04d-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]