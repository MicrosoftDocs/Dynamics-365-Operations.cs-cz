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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eda7fbaeea8d3c1a07f7b43cafe44886d149a211
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027258"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="0d8e9-103">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="0d8e9-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d8e9-104">V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="0d8e9-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="0d8e9-105">Overview</span></span>

<span data-ttu-id="0d8e9-106">Řešení hodnocení a recenzí je omnikanálové řešení, které lze zpřístupnit v Dynamics 365 Commerce pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0d8e9-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0d8e9-107">LCS je portál pro správu, který maloobchodní prodejci používají ke správě svého prostředí od zařazení po vyřazení z provozu.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="0d8e9-108">Chcete-li použít řešení hodnocení a recenze na webu obchodu, musíte při nasazení vašeho webu pro elektronický obchod v aplikaci souhlasit s hodnocením a recenzemi Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="0d8e9-109">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="0d8e9-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="0d8e9-110">Chcete-li se přihlásit k používání hodnocení a recenzí na vašem webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="0d8e9-111">Postupujte podle kroků v [nasazení nového webu e-Commerce](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="0d8e9-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="0d8e9-112">Zatímco jste stále v LCS, přejděte na **Nastavení nasazení Retail \> Další nastavení**.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="0d8e9-113">Nastavte možnost **Povolit službu hodnocení a recenzování** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="0d8e9-114">V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí (ID objektu skupiny zabezpečení)** zadejte ID skupiny zabezpečení Microsoft Azure Active Directory (Azure AD), která obsahuje moderátory hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Připojení k používání hodnocení a recenzí](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="0d8e9-116">Dokončete proces inicializace e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="0d8e9-117">Jste-li existujícím zákazníkem Dynamics 365 Commerce, který již nasadil server elektronického obchodu bez přijetí hodnocení a recenze a nyní chcete použít hodnocení a recenze z balíčku Dynamics 365 Commerce, odešlete požadavek na službu.</span><span class="sxs-lookup"><span data-stu-id="0d8e9-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="0d8e9-118">Informace o postupu při odesílání žádostí o služby naleznete v tématu [Proces odeslání požadavků na službu](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="0d8e9-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0d8e9-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0d8e9-119">Additional resources</span></span>

[<span data-ttu-id="0d8e9-120">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="0d8e9-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0d8e9-121">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="0d8e9-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="0d8e9-122">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="0d8e9-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="0d8e9-123">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="0d8e9-123">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


