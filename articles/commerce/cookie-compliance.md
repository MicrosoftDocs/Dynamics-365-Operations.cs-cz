---
title: Shoda souborů cookie
description: V tomto tématu jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446906"
---
# <a name="cookie-compliance"></a><span data-ttu-id="708c6-103">Shoda souborů cookie</span><span class="sxs-lookup"><span data-stu-id="708c6-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="708c6-104">V tomto tématu jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="708c6-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="708c6-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="708c6-105">Overview</span></span>

<span data-ttu-id="708c6-106">Ochrana osobních údajů je důležitým faktorem při použití všech technologií sledování, které ovlivňují zákazníky elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="708c6-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="708c6-107">Z důvodu norem dodržování ochrany osobních údajů, jako je obecné nařízení o ochraně osobních údajů (GDPR) v Evropské unii (EU), je třeba zvážit elektronické zásady ochrany osobních údajů pro všechny weby, které jsou v současné době aktivní.</span><span class="sxs-lookup"><span data-stu-id="708c6-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="708c6-108">Vzhledem k tomu, že je většina webů elektronického obchodování ve výchozím nastavení globálně přístupná, je důležité prostudovat standardy kompatibility pro web elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="708c6-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="708c6-109">Chcete-li získat další informace o základních principech, které společnost Microsoft používá pro vyhovění souborů cookie, navštivte [centrum zabezpečení společnosti Microsoft](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="708c6-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="708c6-110">Na tomto webu můžete také získat další informace o oblastech dodržování předpisů a ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="708c6-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="708c6-111">Následující tabulka ukazuje aktuální referenční seznam souborů cookie, které vkládají weby Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="708c6-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="708c6-112">Název souboru cookie</span><span class="sxs-lookup"><span data-stu-id="708c6-112">Cookie name</span></span>                               | <span data-ttu-id="708c6-113">Použití</span><span class="sxs-lookup"><span data-stu-id="708c6-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="708c6-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="708c6-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="708c6-115">Uložit ověřovací soubory cookie Microsoft Azure Active Directory (Azure AD) pro jednotné přihlašovaní (SSO).</span><span class="sxs-lookup"><span data-stu-id="708c6-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="708c6-116">Ukládá šifrované základní informace o uživateli (jméno, příjmení, e-mail).</span><span class="sxs-lookup"><span data-stu-id="708c6-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="708c6-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="708c6-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="708c6-118">ID nákupního košíku použitého k získání seznamu produktů přidaných do instance košíku.</span><span class="sxs-lookup"><span data-stu-id="708c6-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="708c6-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="708c6-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="708c6-120">Sledování souhlasu se soubory cookies.</span><span class="sxs-lookup"><span data-stu-id="708c6-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="708c6-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="708c6-121">ai_session</span></span>                                  | <span data-ttu-id="708c6-122">Zjistí, kolik relací uživatelské aktivity zahrnovalo určité stránky a funkce aplikace.</span><span class="sxs-lookup"><span data-stu-id="708c6-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="708c6-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="708c6-123">ai_user</span></span>                                     | <span data-ttu-id="708c6-124">Zjistí, kolik lidí použilo aplikaci a její funkce.</span><span class="sxs-lookup"><span data-stu-id="708c6-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="708c6-125">Uživatelé se počítají pomocí anonymních ID.</span><span class="sxs-lookup"><span data-stu-id="708c6-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="708c6-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="708c6-126">b2cru</span></span>                                       | <span data-ttu-id="708c6-127">Dynamicky ukládá adresu URL přesměrování.</span><span class="sxs-lookup"><span data-stu-id="708c6-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="708c6-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="708c6-128">JSESSIONID</span></span>                                  | <span data-ttu-id="708c6-129">Používá platební konektor Adyen k uložení relace uživatele.</span><span class="sxs-lookup"><span data-stu-id="708c6-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="708c6-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="708c6-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="708c6-131">Ověřování</span><span class="sxs-lookup"><span data-stu-id="708c6-131">Authentication</span></span>                                               |
| <span data-ttu-id="708c6-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="708c6-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="708c6-133">Používá se pro udržování stavu žádosti.</span><span class="sxs-lookup"><span data-stu-id="708c6-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="708c6-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="708c6-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="708c6-135">Token CRSF používaný k ochraně před CRSF.</span><span class="sxs-lookup"><span data-stu-id="708c6-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="708c6-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="708c6-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="708c6-137">Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce.</span><span class="sxs-lookup"><span data-stu-id="708c6-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="708c6-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="708c6-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="708c6-139">Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce.</span><span class="sxs-lookup"><span data-stu-id="708c6-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="708c6-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="708c6-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="708c6-141">Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce.</span><span class="sxs-lookup"><span data-stu-id="708c6-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="708c6-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="708c6-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="708c6-143">Používá se k udržování relace SSO.</span><span class="sxs-lookup"><span data-stu-id="708c6-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="708c6-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="708c6-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="708c6-145">Používá se pro sledování transakcí (počet otevřených karet, které se autentizují proti webu typu B2C), včetně aktuální transakce.</span><span class="sxs-lookup"><span data-stu-id="708c6-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="708c6-146">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="708c6-146">Additional resources</span></span>

[<span data-ttu-id="708c6-147">Funkce a možnosti usnadnění přístupu</span><span class="sxs-lookup"><span data-stu-id="708c6-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="708c6-148">Přehled dodržování předpisů</span><span class="sxs-lookup"><span data-stu-id="708c6-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="708c6-149">Přidání stránky se zásadami ochrany osobních údajů</span><span class="sxs-lookup"><span data-stu-id="708c6-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="708c6-150">Nahrazení ID uživatelů přidružených ke změnám sledovaných obsahů</span><span class="sxs-lookup"><span data-stu-id="708c6-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
