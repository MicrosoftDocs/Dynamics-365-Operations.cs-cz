---
title: Připojení k používání hodnocení a recenzí
description: V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697973"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="def8c-103">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="def8c-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="def8c-104">V tomto tématu je vysvětleno, jak se lze přihlásit k používání hodnocení a recenzí na vašem webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="def8c-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="def8c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="def8c-105">Overview</span></span>

<span data-ttu-id="def8c-106">Řešení hodnocení a recenzí je omnikanálové řešení, které lze zpřístupnit v Dynamics 365 Commerce pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="def8c-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="def8c-107">LCS je portál pro správu, který maloobchodní prodejci používají ke správě svého prostředí od zařazení po vyřazení z provozu.</span><span class="sxs-lookup"><span data-stu-id="def8c-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="def8c-108">Chcete-li použít řešení hodnocení a recenze na webu služby Commerce, musíte se nejprve přihlásit.</span><span class="sxs-lookup"><span data-stu-id="def8c-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="def8c-109">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="def8c-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="def8c-110">Chcete-li se přihlásit k používání hodnocení a recenzí na vašem webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="def8c-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="def8c-111">Postupujte podle kroků v [nasazení nového webu e-Commerce](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="def8c-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="def8c-112">Zatímco jste stále v LCS, přejděte na **Nastavení nasazení Retail \> Další nastavení**.</span><span class="sxs-lookup"><span data-stu-id="def8c-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="def8c-113">Nastavte možnost **Povolit službu hodnocení a recenzování** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="def8c-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="def8c-114">V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí (ID objektu skupiny zabezpečení)** zadejte ID skupiny zabezpečení Microsoft Azure Active Directory (Azure AD), která obsahuje moderátory hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="def8c-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Připojení k používání hodnocení a recenzí](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="def8c-116">Dokončete proces inicializace e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="def8c-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="def8c-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="def8c-117">Additional resources</span></span>

[<span data-ttu-id="def8c-118">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="def8c-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="def8c-119">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="def8c-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="def8c-120">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="def8c-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="def8c-121">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="def8c-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
