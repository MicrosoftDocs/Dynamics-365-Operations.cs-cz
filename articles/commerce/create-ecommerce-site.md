---
title: Vytvoření webu elektronického obchodu
description: V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu elektronického obchodu v Konfigurátoru webu Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 465154ef7209547481c8598d5eaefb434359b1fd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207963"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="4d1ed-103">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="4d1ed-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d1ed-104">V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu elektronického obchodu v Konfigurátoru webu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="4d1ed-105">Když si pořídíte licenci na funkce Dynamics 365 Commerce, bude konfigurátor webu obsahovat startovací web, který můžete použít jako základ pro svůj vlastní web.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="4d1ed-106">Pokud však chcete začít úplně od začátku nebo pokud si chcete vytvořit druhý web, budete si muset ve vývojovém prostředí webu založit nový web.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="4d1ed-107">Zřízení webu</span><span class="sxs-lookup"><span data-stu-id="4d1ed-107">Set up your site</span></span>

<span data-ttu-id="4d1ed-108">Při zřízení webu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="4d1ed-109">Otevřete prostředí konfigurátoru webu.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-109">Open the site builder environment.</span></span> <span data-ttu-id="4d1ed-110">Odkaz na konfigurátor webu v Microsoft Lifecycle Services (LCS) naleznete na stránce funkcí prostředí pro Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="4d1ed-111">Na domovské stránce vývojového prostředí webu vyberte možnost **Nový web**.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="4d1ed-112">V dialogovém okně **Nový web** zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="4d1ed-113">Pole</span><span class="sxs-lookup"><span data-stu-id="4d1ed-113">Field</span></span>                               | <span data-ttu-id="4d1ed-114">Popis</span><span class="sxs-lookup"><span data-stu-id="4d1ed-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="4d1ed-115">Název webu</span><span class="sxs-lookup"><span data-stu-id="4d1ed-115">Site name</span></span>                           | <span data-ttu-id="4d1ed-116">Zadejte zobrazovaný název, který má být použit pro váš web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="4d1ed-117">Tento název je viditelný pouze ve vývojovém prostředí a nebude zobrazen zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="4d1ed-118">Skupina zabezpečení správce webu</span><span class="sxs-lookup"><span data-stu-id="4d1ed-118">Site administrator's security group</span></span> | <span data-ttu-id="4d1ed-119">Zadejte skupinu zabezpečení Microsoft Azure Active Directory (Azure AD), která spravuje uživatele s rolí správce webu na tomto webu.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="4d1ed-120">Výchozí kanál (číslo provozní jednotky)</span><span class="sxs-lookup"><span data-stu-id="4d1ed-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="4d1ed-121">Vyberte online obchod, který bude pro tento web sloužit jako webová výkladní skříň.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="4d1ed-122">Chcete-li, aby váš web elektronického obchodu podporoval více online obchodů, je třeba po zřízení webu k němu přiřadit obchody v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="4d1ed-123">Výchozí jazyk</span><span class="sxs-lookup"><span data-stu-id="4d1ed-123">Default language</span></span>                            | <span data-ttu-id="4d1ed-124">Zadejte výchozí jazyk pro tento online obchod a trh.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="4d1ed-125">Online obchod může podporovat více jazyků.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-125">An online store can support multiple languages.</span></span> <span data-ttu-id="4d1ed-126">Chcete-li podporu více jazyků pro tento online obchod nebo jiný online obchod, můžete tuto podporu nakonfigurovat v **Nastavení webu** po zřízení tohoto webu.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="4d1ed-127">Doména</span><span class="sxs-lookup"><span data-stu-id="4d1ed-127">Domain</span></span>                              | <span data-ttu-id="4d1ed-128">Vyberte název domény, který bude pro tento online obchod sloužit jako doména.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="4d1ed-129">Pokud nejsou nakonfigurovány žádné domény pro LCS, můžete toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="4d1ed-130">Poté, co je doména konfigurována v LCS, je nutné ji přidat do online obchodu v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="4d1ed-131">Cesta</span><span class="sxs-lookup"><span data-stu-id="4d1ed-131">Path</span></span>                              | <span data-ttu-id="4d1ed-132">Pokud web podporuje více jazyků pro daný název domény, použijte pole cesty k vytvoření jedinečné adresy URL webu pro tuto kombinaci domény a jazyka.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="4d1ed-133">Pokud je jazyk, který jste zadali v poli **Výchozí jazyk**, jediným jazykem, který bude pro tuto doménu podporován, nebo bude po lokalizaci webu do dalších jazyků i nadále výchozím jazykem, doporučujeme toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="4d1ed-134">Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="4d1ed-135">Chcete-li přistupovat k přiděleným produktům podle kategorie, můžete použít také rozevírací nabídku v levé horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="4d1ed-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d1ed-136">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4d1ed-136">Additional resources</span></span>

[<span data-ttu-id="4d1ed-137">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="4d1ed-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4d1ed-138">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="4d1ed-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4d1ed-139">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="4d1ed-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4d1ed-140">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="4d1ed-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4d1ed-141">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="4d1ed-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4d1ed-142">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="4d1ed-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4d1ed-143">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="4d1ed-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4d1ed-144">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="4d1ed-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4d1ed-145">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="4d1ed-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4d1ed-146">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="4d1ed-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]