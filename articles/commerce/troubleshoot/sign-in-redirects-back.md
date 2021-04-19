---
title: Odkaz na přihlášení přesměruje zpět na web elektronického obchodování
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se přihlašovací odkaz přesměruje zpět na web elektronického obchodování, místo aby přešel na přihlašovací stránku.
author: Reza-Assadi
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
ms.openlocfilehash: ee2ac8636dad8d31719971b2cc17c8b923f07959
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801452"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="a03b9-103">Odkaz na přihlášení přesměruje zpět na web elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="a03b9-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a03b9-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se přihlašovací odkaz přesměruje zpět na web elektronického obchodování, místo aby přešel na přihlašovací stránku.</span><span class="sxs-lookup"><span data-stu-id="a03b9-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="a03b9-105">popis</span><span class="sxs-lookup"><span data-stu-id="a03b9-105">Description</span></span>

<span data-ttu-id="a03b9-106">Po konfiguraci nového tenanta Microsoft Azure Active Directory B2C (Azure AD B2C)v nástroji pro tvorbu webů Connect uživatelé, kteří vyberou odkaz **Přihlásit se**, jsou přesměrováni zpět na hlavní vstupní stránku elektronického obchodu, aniž by přešli na přihlašovací stránku.</span><span class="sxs-lookup"><span data-stu-id="a03b9-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="a03b9-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="a03b9-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="a03b9-108">Zkontrolujte, zda je adresa URL odpovědi správně nakonfigurována v aplikaci Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="a03b9-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="a03b9-109">Pro kontrolu, zda je adresa URL odpovědi správně nakonfigurována v aplikaci Azure AD B2C, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a03b9-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="a03b9-110">Přejděte na [portál Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="a03b9-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="a03b9-111">Vyberte aplikaci Azure AD B2C, kterou jste vytvořili pro přístup na web.</span><span class="sxs-lookup"><span data-stu-id="a03b9-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="a03b9-112">Vyberte aplikaci, kterou jste vytvořili během nastavení Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a03b9-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="a03b9-113">V poli **URL pro odpověď** zkontrolujte, že seznam obsahuje položky pro adresu URL domény webu i adresu URL generovanou elektronickým obchodem, jak je znázorněno v příkladu na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="a03b9-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Záznamy adresy URL pro odpověď Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="a03b9-115">Adresa URL domény webu i adresa generovaná elektronickým obchodem musí být v platném formátu adresy URL, který neobsahuje úvodní ani koncová lomítka.</span><span class="sxs-lookup"><span data-stu-id="a03b9-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a03b9-116">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a03b9-116">Additional resources</span></span>

[<span data-ttu-id="a03b9-117">Registrace připojené aplikace v Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="a03b9-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="a03b9-118">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="a03b9-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
