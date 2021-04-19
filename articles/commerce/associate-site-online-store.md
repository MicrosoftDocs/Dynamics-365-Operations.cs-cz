---
title: Přidružení webu Dynamics 365 Commerce k online kanálu
description: V tomto tématu je vysvětleno, jak svázat váš web Microsoft Dynamics 365 Commerce s jedním nebo více online obchody.
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7ceef55bac11ae8a1f7d9dafbddc45d67b836504
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797298"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="052ec-103">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="052ec-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="052ec-104">V tomto tématu je vysvětleno, jak svázat váš web Microsoft Dynamics 365 Commerce s jedním nebo více online obchody.</span><span class="sxs-lookup"><span data-stu-id="052ec-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="052ec-105">Po zřízení prostředí elektronického obchodu Dynamics 365 Commerce pomocí portálu Microsoft Dynamics Lifecycle Services (LCS) jste připraveni na vytvoření prvního webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="052ec-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="052ec-106">V rámci počátečního vytváření webu přidružíte web k online obchodu, který byl dříve vytvořen.</span><span class="sxs-lookup"><span data-stu-id="052ec-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="052ec-107">Tento krok sváže web s online kanálem a umožní webu zobrazit hierarchii navigace, produkty, kategorie, ceny, možnosti expedice a vše, co jste definovali v online obchodě.</span><span class="sxs-lookup"><span data-stu-id="052ec-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="052ec-108">Chcete-li vytvořit nový web a přidružit k němu online obchod, v poli LCS vyberte odkaz na vývojové prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="052ec-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="052ec-109">Poté na stránce vývojového prostředí webu vyberte možnost **Nový web**.</span><span class="sxs-lookup"><span data-stu-id="052ec-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="052ec-110">V dialogovém okně **Nový web** je nutné zadat určité základní informace o vašem webu.</span><span class="sxs-lookup"><span data-stu-id="052ec-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="052ec-111">Úplné vysvětlení informací, které je třeba zadat, naleznete v tématu [Vytvoření nového webu elektronického obchodu](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="052ec-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="052ec-112">Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu.</span><span class="sxs-lookup"><span data-stu-id="052ec-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="052ec-113">Chcete-li přistupovat k produktům podle kategorie, můžete použít také rozevírací pole v levé horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="052ec-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="052ec-114">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="052ec-114">Additional resources</span></span>

[<span data-ttu-id="052ec-115">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="052ec-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="052ec-116">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="052ec-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="052ec-117">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="052ec-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="052ec-118">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="052ec-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="052ec-119">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="052ec-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="052ec-120">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="052ec-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="052ec-121">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="052ec-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="052ec-122">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="052ec-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="052ec-123">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="052ec-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="052ec-124">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="052ec-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]