---
title: Připojení k používání hodnocení a recenzí
description: V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 481a8750b2333d5dd5de2c05e175569804a6046f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985829"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="fa27a-103">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="fa27a-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa27a-104">V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fa27a-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="fa27a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="fa27a-105">Overview</span></span>

<span data-ttu-id="fa27a-106">Řešení hodnocení a recenzí je omnikanálové řešení, které lze zpřístupnit v Dynamics 365 Commerce pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fa27a-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fa27a-107">LCS je portál pro správu, který maloobchodní prodejci používají ke správě svého prostředí od zařazení po vyřazení z provozu.</span><span class="sxs-lookup"><span data-stu-id="fa27a-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="fa27a-108">Chcete-li použít řešení hodnocení a recenze na webu obchodu, musíte při nasazení vašeho webu pro elektronický obchod v aplikaci souhlasit s hodnocením a recenzemi Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fa27a-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="fa27a-109">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="fa27a-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="fa27a-110">Chcete-li se přihlásit k používání hodnocení a recenzí na vašem webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="fa27a-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="fa27a-111">Postupujte podle kroků v [nasazení nového webu e-Commerce](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="fa27a-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="fa27a-112">Zatímco jste stále v LCS, přejděte na **Nastavení nasazení Retail \> Další nastavení**.</span><span class="sxs-lookup"><span data-stu-id="fa27a-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="fa27a-113">Nastavte možnost **Povolit službu hodnocení a recenzování** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fa27a-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="fa27a-114">V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí (ID objektu skupiny zabezpečení)** zadejte ID skupiny zabezpečení Microsoft Azure Active Directory (Azure AD), která obsahuje moderátory hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="fa27a-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Připojení k používání hodnocení a recenzí](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="fa27a-116">Dokončete proces inicializace e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="fa27a-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="fa27a-117">Jste-li existujícím zákazníkem Dynamics 365 Commerce, který již nasadil server elektronického obchodu bez přijetí hodnocení a recenze a nyní chcete použít hodnocení a recenze z balíčku Dynamics 365 Commerce, odešlete požadavek na službu.</span><span class="sxs-lookup"><span data-stu-id="fa27a-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="fa27a-118">Informace o postupu při odesílání žádostí o služby naleznete v tématu [Proces odeslání požadavků na službu](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fa27a-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="fa27a-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="fa27a-119">Additional resources</span></span>

[<span data-ttu-id="fa27a-120">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="fa27a-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="fa27a-121">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="fa27a-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="fa27a-122">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="fa27a-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="fa27a-123">Synchronizace hodnocení produktů v Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fa27a-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


