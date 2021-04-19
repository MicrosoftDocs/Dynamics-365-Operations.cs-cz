---
title: Shoda souborů cookie
description: V tomto tématu jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796020"
---
# <a name="cookie-compliance"></a><span data-ttu-id="f7663-103">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="f7663-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7663-104">V tomto tématu jsou popsány důležité informace týkající se kompatibility souborů cookie a výchozích zásad obsažených v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7663-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f7663-105">Ochrana osobních údajů je důležitým faktorem při použití všech technologií sledování, které ovlivňují zákazníky elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="f7663-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="f7663-106">Z důvodu norem dodržování ochrany osobních údajů, jako je obecné nařízení o ochraně osobních údajů (GDPR) v Evropské unii (EU), je třeba zvážit elektronické zásady ochrany osobních údajů pro všechny weby, které jsou v současné době aktivní.</span><span class="sxs-lookup"><span data-stu-id="f7663-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="f7663-107">Vzhledem k tomu, že je většina webů elektronického obchodování ve výchozím nastavení globálně přístupná, je důležité prostudovat standardy kompatibility pro web elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="f7663-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="f7663-108">Chcete-li získat další informace o základních principech, které společnost Microsoft používá pro vyhovění souborů cookie, navštivte [centrum zabezpečení společnosti Microsoft](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="f7663-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="f7663-109">Na tomto webu můžete také získat další informace o oblastech dodržování předpisů a ochrany osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="f7663-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="f7663-110">Následující tabulka ukazuje aktuální referenční seznam souborů cookie, které vkládají weby Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7663-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="f7663-111">Název souboru cookie</span><span class="sxs-lookup"><span data-stu-id="f7663-111">Cookie name</span></span>                               | <span data-ttu-id="f7663-112">Použití</span><span class="sxs-lookup"><span data-stu-id="f7663-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="f7663-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="f7663-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="f7663-114">Uložit ověřovací soubory cookie Microsoft Azure Active Directory (Azure AD) pro jednotné přihlašovaní (SSO).</span><span class="sxs-lookup"><span data-stu-id="f7663-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="f7663-115">Ukládá šifrované základní informace o uživateli (jméno, příjmení, e-mail).</span><span class="sxs-lookup"><span data-stu-id="f7663-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="f7663-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="f7663-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="f7663-117">ID nákupního košíku použitého k získání seznamu produktů přidaných do instance košíku.</span><span class="sxs-lookup"><span data-stu-id="f7663-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="f7663-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="f7663-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="f7663-119">Sledování souhlasu se soubory cookies.</span><span class="sxs-lookup"><span data-stu-id="f7663-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="f7663-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="f7663-120">ai_session</span></span>                                  | <span data-ttu-id="f7663-121">Zjistí, kolik relací uživatelské aktivity zahrnovalo určité stránky a funkce aplikace.</span><span class="sxs-lookup"><span data-stu-id="f7663-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="f7663-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="f7663-122">ai_user</span></span>                                     | <span data-ttu-id="f7663-123">Zjistí, kolik lidí použilo aplikaci a její funkce.</span><span class="sxs-lookup"><span data-stu-id="f7663-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="f7663-124">Uživatelé se počítají pomocí anonymních ID.</span><span class="sxs-lookup"><span data-stu-id="f7663-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="f7663-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="f7663-125">b2cru</span></span>                                       | <span data-ttu-id="f7663-126">Dynamicky ukládá adresu URL přesměrování.</span><span class="sxs-lookup"><span data-stu-id="f7663-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="f7663-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="f7663-127">JSESSIONID</span></span>                                  | <span data-ttu-id="f7663-128">Používá platební konektor Adyen k uložení relace uživatele.</span><span class="sxs-lookup"><span data-stu-id="f7663-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="f7663-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="f7663-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="f7663-130">Ověřování</span><span class="sxs-lookup"><span data-stu-id="f7663-130">Authentication</span></span>                                               |
| <span data-ttu-id="f7663-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="f7663-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="f7663-132">Používá se pro udržování stavu žádosti.</span><span class="sxs-lookup"><span data-stu-id="f7663-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="f7663-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="f7663-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="f7663-134">Token CRSF používaný k ochraně před CRSF.</span><span class="sxs-lookup"><span data-stu-id="f7663-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="f7663-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="f7663-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="f7663-136">Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce.</span><span class="sxs-lookup"><span data-stu-id="f7663-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="f7663-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="f7663-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="f7663-138">Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce.</span><span class="sxs-lookup"><span data-stu-id="f7663-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="f7663-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="f7663-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="f7663-140">Používá se k směrování požadavků do příslušné instance serveru pro ověřování produkce.</span><span class="sxs-lookup"><span data-stu-id="f7663-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="f7663-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="f7663-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="f7663-142">Používá se k udržování relace SSO.</span><span class="sxs-lookup"><span data-stu-id="f7663-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="f7663-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="f7663-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="f7663-144">Používá se pro sledování transakcí (počet otevřených karet, které se autentizují proti webu typu B2C), včetně aktuální transakce.</span><span class="sxs-lookup"><span data-stu-id="f7663-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="f7663-145">Souhlas uživatele webu se soubory cookie na webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="f7663-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="f7663-146">Pokud funkce nebo modul webu elektronického obchodu používá nepodstatný soubor cookie, je nutné před sledováním souboru cookie získat souhlas uživatele webu.</span><span class="sxs-lookup"><span data-stu-id="f7663-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="f7663-147">Aby uživatelé webu mohli poskytovat souhlas se soubory cookie na webu elektronického obchodu, musí autor webu přidat a nakonfigurovat modul souhlasu se soubory cookie v modulu záhlaví stránky, aby bylo zajištěno zobrazení a přijetí souhlasu.</span><span class="sxs-lookup"><span data-stu-id="f7663-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="f7663-148">Před vykreslením funkce nebo modulu používajícího nepodstatný soubor cookie na stránce webu musí být udělen souhlas uživatele webu.</span><span class="sxs-lookup"><span data-stu-id="f7663-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7663-149">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f7663-149">Additional resources</span></span>

[<span data-ttu-id="f7663-150">Funkce a možnosti usnadnění přístupu</span><span class="sxs-lookup"><span data-stu-id="f7663-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="f7663-151">Přehled dodržování předpisů</span><span class="sxs-lookup"><span data-stu-id="f7663-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="f7663-152">Přidání stránky se zásadami ochrany osobních údajů</span><span class="sxs-lookup"><span data-stu-id="f7663-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="f7663-153">Nahrazení ID uživatelů přidružených ke změnám sledovaných obsahů</span><span class="sxs-lookup"><span data-stu-id="f7663-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="f7663-154">Modul souhlasu se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="f7663-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="f7663-155">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="f7663-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
