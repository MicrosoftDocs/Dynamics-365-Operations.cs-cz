---
title: Vytvoření webu elektronického obchodu
description: V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu e-Commerce v Konfigurátoru webu Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096767"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="64d84-103">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="64d84-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="64d84-104">V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu e-Commerce v Konfigurátoru webu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="64d84-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="64d84-105">Než začnete vyvíjet svůj web e-Commerce, je nutné nejprve vytvořit nový web v Konfugurátoru webu.</span><span class="sxs-lookup"><span data-stu-id="64d84-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="64d84-106">Chcete-li začít vyvíjet svůj web elektronického obchodu, je nutné nejprve vytvořit nový web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="64d84-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="64d84-107">Než bude možné vytvořit nový web, musí být v aplikaci Commerce vytvořen alespoň jeden online obchod.</span><span class="sxs-lookup"><span data-stu-id="64d84-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="64d84-108">Zřízení webu</span><span class="sxs-lookup"><span data-stu-id="64d84-108">Set up your site</span></span>

<span data-ttu-id="64d84-109">Při zřízení webu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="64d84-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="64d84-110">Otevřete prostředí konfigurátoru webu.</span><span class="sxs-lookup"><span data-stu-id="64d84-110">Open the site builder environment.</span></span> <span data-ttu-id="64d84-111">Odkaz na konfigurátor webu v Microsoft Lifecycle Services (LCS) naleznete na stránce funkcí prostředí pro Commerce.</span><span class="sxs-lookup"><span data-stu-id="64d84-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="64d84-112">Na domovské stránce vývojového prostředí webu vyberte možnost **Nový web**.</span><span class="sxs-lookup"><span data-stu-id="64d84-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="64d84-113">V dialogovém okně **Nový web** zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="64d84-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="64d84-114">Pole</span><span class="sxs-lookup"><span data-stu-id="64d84-114">Field</span></span>                               | <span data-ttu-id="64d84-115">Popis</span><span class="sxs-lookup"><span data-stu-id="64d84-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="64d84-116">Název webu</span><span class="sxs-lookup"><span data-stu-id="64d84-116">Site name</span></span>                           | <span data-ttu-id="64d84-117">Zadejte zobrazovaný název, který má být použit pro váš web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="64d84-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="64d84-118">Tento název je viditelný pouze ve vývojovém prostředí a nebude zobrazen zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="64d84-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="64d84-119">Skupina zabezpečení správce webu</span><span class="sxs-lookup"><span data-stu-id="64d84-119">Site administrator's security group</span></span> | <span data-ttu-id="64d84-120">Zadejte skupinu zabezpečení Microsoft Azure Active Directory (Azure AD), která spravuje uživatele s rolí správce webu na tomto webu.</span><span class="sxs-lookup"><span data-stu-id="64d84-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="64d84-121">Výchozí kanál (číslo provozní jednotky)</span><span class="sxs-lookup"><span data-stu-id="64d84-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="64d84-122">Vyberte online obchod, který bude pro tento web sloužit jako webová výkladní skříň.</span><span class="sxs-lookup"><span data-stu-id="64d84-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="64d84-123">Chcete-li, aby váš web elektronického obchodu podporoval více online obchodů, je třeba po zřízení webu k němu přiřadit obchody v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="64d84-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="64d84-124">Výchozí jazyk</span><span class="sxs-lookup"><span data-stu-id="64d84-124">Default language</span></span>                            | <span data-ttu-id="64d84-125">Zadejte výchozí jazyk pro tento online obchod a trh.</span><span class="sxs-lookup"><span data-stu-id="64d84-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="64d84-126">Online obchod může podporovat více jazyků.</span><span class="sxs-lookup"><span data-stu-id="64d84-126">An online store can support multiple languages.</span></span> <span data-ttu-id="64d84-127">Chcete-li podporu více jazyků pro tento online obchod nebo jiný online obchod, můžete tuto podporu nakonfigurovat v **Nastavení webu** po zřízení tohoto webu.</span><span class="sxs-lookup"><span data-stu-id="64d84-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="64d84-128">Doména</span><span class="sxs-lookup"><span data-stu-id="64d84-128">Domain</span></span>                              | <span data-ttu-id="64d84-129">Vyberte název domény, který bude pro tento online obchod sloužit jako doména.</span><span class="sxs-lookup"><span data-stu-id="64d84-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="64d84-130">Pokud nejsou nakonfigurovány žádné domény pro LCS, můžete toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="64d84-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="64d84-131">Poté, co je doména konfigurována v LCS, je nutné ji přidat do online obchodu v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="64d84-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="64d84-132">Cesta</span><span class="sxs-lookup"><span data-stu-id="64d84-132">Path</span></span>                              | <span data-ttu-id="64d84-133">Pokud web podporuje více jazyků pro daný název domény, použijte pole cesty k vytvoření jedinečné adresy URL webu pro tuto kombinaci domény a jazyka.</span><span class="sxs-lookup"><span data-stu-id="64d84-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="64d84-134">Pokud je jazyk, který jste zadali v poli **Výchozí jazyk**, jediným jazykem, který bude pro tuto doménu podporován, nebo bude po lokalizaci webu do dalších jazyků i nadále výchozím jazykem, doporučujeme toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="64d84-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="64d84-135">Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu.</span><span class="sxs-lookup"><span data-stu-id="64d84-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="64d84-136">Chcete-li přistupovat k přiděleným produktům podle kategorie, můžete použít také rozevírací nabídku v levé horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="64d84-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64d84-137">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="64d84-137">Additional resources</span></span>

[<span data-ttu-id="64d84-138">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="64d84-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="64d84-139">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="64d84-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="64d84-140">Nastavení kanálu online obchodu</span><span class="sxs-lookup"><span data-stu-id="64d84-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="64d84-141">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="64d84-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="64d84-142">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="64d84-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="64d84-143">Nahrání souborů pro hromadné přesmerování adres URL</span><span class="sxs-lookup"><span data-stu-id="64d84-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="64d84-144">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="64d84-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="64d84-145">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="64d84-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="64d84-146">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="64d84-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="64d84-147">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="64d84-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="64d84-148">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="64d84-148">Enable location-based store detection</span></span>](enable-store-detection.md)
