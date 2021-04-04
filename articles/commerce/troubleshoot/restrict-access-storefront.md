---
title: Omezení přístupu k výloze během testování nebo vývoje
description: Toto téma vysvětluje, jak omezit přístup k výloze Microsoft Dynamics 365 Commerce, zatímco probíhá interní testování nebo vývoj.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585235"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="545bc-103">Omezení přístupu k výloze během testování nebo vývoje</span><span class="sxs-lookup"><span data-stu-id="545bc-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="545bc-104">Toto téma vysvětluje, jak omezit přístup k výloze Microsoft Dynamics 365 Commerce, zatímco probíhá interní testování nebo vývoj.</span><span class="sxs-lookup"><span data-stu-id="545bc-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="545bc-105">popis</span><span class="sxs-lookup"><span data-stu-id="545bc-105">Description</span></span>

<span data-ttu-id="545bc-106">Během interního testování nebo aktivního vývoje možná budete chtít omezit přístup na svůj web, abyste zabránili externím uživatelům v přístupu k publikovaným stránkám výlohy.</span><span class="sxs-lookup"><span data-stu-id="545bc-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="545bc-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="545bc-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="545bc-108">Nastavení Azure AD B2C pomocí standardních toků uživatelů</span><span class="sxs-lookup"><span data-stu-id="545bc-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="545bc-109">Informace o konfiguraci Azure Active Directory B2C (Azure AD B2C) pro váš web elektronického obchodování, viz [Nastavení tenanta B2C v Commerce](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="545bc-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="545bc-110">Omezení přístupu uživatelů na hlavní stránky obchodu a zablokování vytváření nových uživatelů</span><span class="sxs-lookup"><span data-stu-id="545bc-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="545bc-111">Chcete-li omezit přístup uživatele na stránky výlohy v nástroji pro tvorbu webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="545bc-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="545bc-112">Přejděte na svůj web.</span><span class="sxs-lookup"><span data-stu-id="545bc-112">Go to your site.</span></span>
1. <span data-ttu-id="545bc-113">Vyberte **Stránky** a poté vyberte stránku, na kterou chcete omezit přístup uživatelů.</span><span class="sxs-lookup"><span data-stu-id="545bc-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="545bc-114">Vyberte slot modulu nebo fragmentu a poté vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="545bc-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="545bc-115">V podokně vlastností vyberte **Vyžaduje přihlášení?** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="545bc-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="545bc-116">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="545bc-116">Select **Publish**.</span></span>

<span data-ttu-id="545bc-117">Chcete-li blokovat vytváření nových uživatelů v Azure AD, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="545bc-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="545bc-118">Přejděte na [portál Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="545bc-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="545bc-119">Vyberte aplikaci Azure AD B2C, kterou jste vytvořili pro přístup na web.</span><span class="sxs-lookup"><span data-stu-id="545bc-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="545bc-120">V levém navigačním podokně vyberte položku **Toky uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="545bc-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="545bc-121">V horní části stránky **Toky uživatelů** vyberte možnost **Nový tok uživatele**.</span><span class="sxs-lookup"><span data-stu-id="545bc-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="545bc-122">Na stránce **Vybrat typ toku uživatele** vyberte **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="545bc-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="545bc-123">Uprostřed stránky vyberte **Přihlásit se v2**.</span><span class="sxs-lookup"><span data-stu-id="545bc-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="545bc-124">Poté postupujte podle pokynů v [Nastavení tenanta B2C v Commerce](../set-up-b2c-tenant.md) ke konfiguraci toku jako standardního toku uživatelů vašeho webu Azure AD B2C během testování nebo vývoje.</span><span class="sxs-lookup"><span data-stu-id="545bc-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="545bc-125">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="545bc-125">Additional resources</span></span>

[<span data-ttu-id="545bc-126">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="545bc-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="545bc-127">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="545bc-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
