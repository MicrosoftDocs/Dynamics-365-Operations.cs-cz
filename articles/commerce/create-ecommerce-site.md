---
title: Vytvoření webu elektronického obchodu
description: V tomto tématu jsou popsány úlohy, které souvisí s vytvořením nového serveru elektronického obchodu v řešení Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697122"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="0af81-103">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="0af81-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0af81-104">V tomto tématu jsou popsány úlohy, které souvisí s vytvořením nového serveru elektronického obchodu v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0af81-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0af81-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="0af81-105">Overview</span></span>

<span data-ttu-id="0af81-106">Chcete-li začít vyvíjet svůj web elektronického obchodu, je nutné nejprve vytvořit nový web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="0af81-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="0af81-107">Než bude možné vytvořit nový web, musí být v aplikaci Dynamics 365 Retail vytvořen alespoň jeden online obchod.</span><span class="sxs-lookup"><span data-stu-id="0af81-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="0af81-108">Zřízení webu</span><span class="sxs-lookup"><span data-stu-id="0af81-108">Set up your site</span></span>

<span data-ttu-id="0af81-109">Při zřízení webu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="0af81-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="0af81-110">Ve službách Microsoft Lifecycle Services (LCS) vyberte odkaz na vývojové prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="0af81-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="0af81-111">Na domovské stránce vývojového prostředí webu vyberte možnost **Nový web**.</span><span class="sxs-lookup"><span data-stu-id="0af81-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="0af81-112">V dialogovém okně **Nový web** zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="0af81-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="0af81-113">Pole</span><span class="sxs-lookup"><span data-stu-id="0af81-113">Field</span></span>                               | <span data-ttu-id="0af81-114">Popis</span><span class="sxs-lookup"><span data-stu-id="0af81-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="0af81-115">Název webu</span><span class="sxs-lookup"><span data-stu-id="0af81-115">Site name</span></span>                           | <span data-ttu-id="0af81-116">Zadejte zobrazovaný název, který má být použit pro váš web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="0af81-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="0af81-117">Tento název je viditelný pouze ve vývojovém prostředí a nebude zobrazen zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="0af81-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="0af81-118">Skupina zabezpečení správce webu</span><span class="sxs-lookup"><span data-stu-id="0af81-118">Site administrator's security group</span></span> | <span data-ttu-id="0af81-119">Zadejte skupinu zabezpečení Microsoft Azure Active Directory (Azure AD), která spravuje uživatele s rolí správce webu na tomto webu.</span><span class="sxs-lookup"><span data-stu-id="0af81-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="0af81-120">Výchozí kanál (číslo provozní jednotky)</span><span class="sxs-lookup"><span data-stu-id="0af81-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="0af81-121">Vyberte online obchod, který bude pro tento web sloužit jako webová výkladní skříň.</span><span class="sxs-lookup"><span data-stu-id="0af81-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="0af81-122">Chcete-li, aby váš web elektronického obchodu podporoval více online obchodů, je třeba po zřízení webu k němu přiřadit obchody v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="0af81-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="0af81-123">Výchozí jazyk</span><span class="sxs-lookup"><span data-stu-id="0af81-123">Default language</span></span>                            | <span data-ttu-id="0af81-124">Zadejte výchozí jazyk pro tento online obchod a trh.</span><span class="sxs-lookup"><span data-stu-id="0af81-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="0af81-125">Online obchod může podporovat více jazyků.</span><span class="sxs-lookup"><span data-stu-id="0af81-125">An online store can support multiple languages.</span></span> <span data-ttu-id="0af81-126">Chcete-li podporu více jazyků pro tento online obchod nebo jiný online obchod, můžete tuto podporu nakonfigurovat v **Nastavení webu** po zřízení tohoto webu.</span><span class="sxs-lookup"><span data-stu-id="0af81-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="0af81-127">Doména</span><span class="sxs-lookup"><span data-stu-id="0af81-127">Domain</span></span>                              | <span data-ttu-id="0af81-128">Vyberte název domény, který bude pro tento online obchod sloužit jako doména.</span><span class="sxs-lookup"><span data-stu-id="0af81-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="0af81-129">Pokud nejsou nakonfigurovány žádné domény pro LCS, můžete toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="0af81-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="0af81-130">Poté, co je doména konfigurována v LCS, je nutné ji přidat do online obchodu v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="0af81-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="0af81-131">Cesta</span><span class="sxs-lookup"><span data-stu-id="0af81-131">Path</span></span>                              | <span data-ttu-id="0af81-132">Pokud web podporuje více jazyků pro daný název domény, použijte pole cesty k vytvoření jedinečné adresy URL webu pro tuto kombinaci domény a jazyka.</span><span class="sxs-lookup"><span data-stu-id="0af81-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="0af81-133">Pokud je jazyk, který jste zadali v poli **Výchozí jazyk**, jediným jazykem, který bude pro tuto doménu podporován, nebo bude po lokalizaci webu do dalších jazyků i nadále výchozím jazykem, doporučujeme toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="0af81-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="0af81-134">Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu.</span><span class="sxs-lookup"><span data-stu-id="0af81-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="0af81-135">Chcete-li přistupovat k přiděleným produktům podle kategorie, můžete použít také rozevírací nabídku v levé horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="0af81-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0af81-136">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0af81-136">Additional resources</span></span>

[<span data-ttu-id="0af81-137">Přehled online obchodu</span><span class="sxs-lookup"><span data-stu-id="0af81-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="0af81-138">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="0af81-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0af81-139">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="0af81-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0af81-140">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="0af81-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0af81-141">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="0af81-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="0af81-142">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="0af81-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="0af81-143">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="0af81-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="0af81-144">Přehled domovské stránky pro tvorbu</span><span class="sxs-lookup"><span data-stu-id="0af81-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="0af81-145">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="0af81-145">Add a new site page</span></span>](add-new-page.md)
