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
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945828"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="3c045-103">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3c045-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3c045-104">V tomto tématu jsou popsány úlohy, které souvisí s vytvořením nového serveru elektronického obchodu v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c045-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3c045-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3c045-105">Overview</span></span>

<span data-ttu-id="3c045-106">Chcete-li začít vyvíjet svůj web elektronického obchodu, je nutné nejprve vytvořit nový web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="3c045-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="3c045-107">Než bude možné vytvořit nový web, musí být v aplikaci Dynamics 365 Retail vytvořen alespoň jeden online obchod.</span><span class="sxs-lookup"><span data-stu-id="3c045-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="3c045-108">Zřízení webu</span><span class="sxs-lookup"><span data-stu-id="3c045-108">Set up your site</span></span>

<span data-ttu-id="3c045-109">Při zřízení webu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="3c045-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="3c045-110">Ve službách Microsoft Lifecycle Services (LCS) vyberte odkaz na vývojové prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="3c045-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="3c045-111">Na domovské stránce vývojového prostředí webu vyberte možnost **Nový web**.</span><span class="sxs-lookup"><span data-stu-id="3c045-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="3c045-112">V dialogovém okně **Nový web** zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="3c045-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="3c045-113">Pole</span><span class="sxs-lookup"><span data-stu-id="3c045-113">Field</span></span>                               | <span data-ttu-id="3c045-114">Popis</span><span class="sxs-lookup"><span data-stu-id="3c045-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="3c045-115">Název webu</span><span class="sxs-lookup"><span data-stu-id="3c045-115">Site name</span></span>                           | <span data-ttu-id="3c045-116">Zadejte zobrazovaný název, který má být použit pro váš web ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="3c045-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="3c045-117">Tento název je viditelný pouze ve vývojovém prostředí a nebude zobrazen zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="3c045-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="3c045-118">Skupina zabezpečení správce webu</span><span class="sxs-lookup"><span data-stu-id="3c045-118">Site administrator's security group</span></span> | <span data-ttu-id="3c045-119">Zadejte skupinu zabezpečení Microsoft Azure Active Directory (Azure AD), která spravuje uživatele s rolí správce webu na tomto webu.</span><span class="sxs-lookup"><span data-stu-id="3c045-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="3c045-120">Výchozí kanál (číslo provozní jednotky)</span><span class="sxs-lookup"><span data-stu-id="3c045-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="3c045-121">Vyberte online obchod, který bude pro tento web sloužit jako webová výkladní skříň.</span><span class="sxs-lookup"><span data-stu-id="3c045-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="3c045-122">Chcete-li, aby váš web elektronického obchodu podporoval více online obchodů, je třeba po zřízení webu k němu přiřadit obchody v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="3c045-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="3c045-123">Výchozí jazyk</span><span class="sxs-lookup"><span data-stu-id="3c045-123">Default language</span></span>                            | <span data-ttu-id="3c045-124">Zadejte výchozí jazyk pro tento online obchod a trh.</span><span class="sxs-lookup"><span data-stu-id="3c045-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="3c045-125">Online obchod může podporovat více jazyků.</span><span class="sxs-lookup"><span data-stu-id="3c045-125">An online store can support multiple languages.</span></span> <span data-ttu-id="3c045-126">Chcete-li podporu více jazyků pro tento online obchod nebo jiný online obchod, můžete tuto podporu nakonfigurovat v **Nastavení webu** po zřízení tohoto webu.</span><span class="sxs-lookup"><span data-stu-id="3c045-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="3c045-127">Doména</span><span class="sxs-lookup"><span data-stu-id="3c045-127">Domain</span></span>                              | <span data-ttu-id="3c045-128">Vyberte název domény, který bude pro tento online obchod sloužit jako doména.</span><span class="sxs-lookup"><span data-stu-id="3c045-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="3c045-129">Pokud nejsou nakonfigurovány žádné domény pro LCS, můžete toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="3c045-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="3c045-130">Poté, co je doména konfigurována v LCS, je nutné ji přidat do online obchodu v **Nastavení webu**.</span><span class="sxs-lookup"><span data-stu-id="3c045-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="3c045-131">Cesta</span><span class="sxs-lookup"><span data-stu-id="3c045-131">Path</span></span>                              | <span data-ttu-id="3c045-132">Pokud web podporuje více jazyků pro daný název domény, použijte pole cesty k vytvoření jedinečné adresy URL webu pro tuto kombinaci domény a jazyka.</span><span class="sxs-lookup"><span data-stu-id="3c045-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="3c045-133">Pokud je jazyk, který jste zadali v poli **Výchozí jazyk**, jediným jazykem, který bude pro tuto doménu podporován, nebo bude po lokalizaci webu do dalších jazyků i nadále výchozím jazykem, doporučujeme toto pole ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="3c045-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="3c045-134">Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu.</span><span class="sxs-lookup"><span data-stu-id="3c045-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="3c045-135">Chcete-li přistupovat k přiděleným produktům podle kategorie, můžete použít také rozevírací nabídku v levé horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="3c045-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c045-136">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3c045-136">Additional resources</span></span>

[<span data-ttu-id="3c045-137">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="3c045-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3c045-138">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3c045-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3c045-139">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="3c045-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3c045-140">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="3c045-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3c045-141">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="3c045-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3c045-142">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="3c045-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3c045-143">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="3c045-143">Enable location-based store detection</span></span>](enable-store-detection.md)
