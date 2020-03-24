---
title: Konfigurace názvu domény
description: Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096813"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="9061f-103">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="9061f-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9061f-104">Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9061f-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="9061f-105">Přidání domén při inicializaci elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="9061f-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="9061f-106">Chcete-li přidružit domény k prostředí elektronického obchodu, inicializujte elektronický obchod způsobem popsaným v tématu [Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9061f-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="9061f-107">Během inicializace budete požádáni o poskytnutí informací, které budou použity k zajištění prostředí elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="9061f-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="9061f-108">V poli **Podporované názvy hostitelů** přidejte všechny domény, které chcete používat s tímto prostředím.</span><span class="sxs-lookup"><span data-stu-id="9061f-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="9061f-109">Více domén je třeba oddělit středníkem.</span><span class="sxs-lookup"><span data-stu-id="9061f-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="9061f-110">Tímto způsobem jsou domény konfigurovány ve všech požadovaných součástech elektronického obchodu a jsou připraveny k použití při přepnutí provozu ze sítě CDN (Content Delivery Network) nebo z webového serveru a ukazují na front-endy elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="9061f-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="9061f-111">Přidání domén po inicializaci elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="9061f-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="9061f-112">Chcete-li po inicializaci elektronického obchodu přidružit nové domény k prostředí elektronického obchodu, je nutné odeslat požadavek na službu.</span><span class="sxs-lookup"><span data-stu-id="9061f-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9061f-113">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9061f-113">Additional resources</span></span>

[<span data-ttu-id="9061f-114">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="9061f-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9061f-115">Nastavení kanálu online obchodu</span><span class="sxs-lookup"><span data-stu-id="9061f-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="9061f-116">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="9061f-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9061f-117">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="9061f-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9061f-118">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="9061f-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9061f-119">Nahrání souborů pro hromadné přesmerování adres URL</span><span class="sxs-lookup"><span data-stu-id="9061f-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9061f-120">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="9061f-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9061f-121">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="9061f-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9061f-122">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="9061f-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9061f-123">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="9061f-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9061f-124">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="9061f-124">Enable location-based store detection</span></span>](enable-store-detection.md)
