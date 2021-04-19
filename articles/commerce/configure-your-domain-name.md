---
title: Konfigurace názvu domény
description: Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796044"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="3987c-103">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="3987c-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3987c-104">Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3987c-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="3987c-105">Přidání domén při inicializaci elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3987c-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="3987c-106">Chcete-li přidružit domény k prostředí elektronického obchodu Dynamics 365 Commerce, inicializujte elektronický obchod způsobem popsaným v tématu [Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="3987c-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="3987c-107">Během inicializace budete požádáni o poskytnutí informací, které budou použity k zajištění prostředí elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="3987c-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="3987c-108">V poli **Podporované názvy hostitelů** přidejte všechny domény, které chcete používat s tímto prostředím.</span><span class="sxs-lookup"><span data-stu-id="3987c-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="3987c-109">Více domén je třeba oddělit středníkem.</span><span class="sxs-lookup"><span data-stu-id="3987c-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="3987c-110">Tímto způsobem jsou domény konfigurovány ve všech požadovaných součástech elektronického obchodu a jsou připraveny k použití při přepnutí provozu ze sítě CDN (Content Delivery Network) nebo z webového serveru a ukazují na front-endy elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="3987c-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="3987c-111">Přidání domén po inicializaci elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3987c-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="3987c-112">Chcete-li po inicializaci elektronického obchodu přidružit nové domény k prostředí elektronického obchodu, je nutné odeslat požadavek na službu.</span><span class="sxs-lookup"><span data-stu-id="3987c-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3987c-113">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3987c-113">Additional resources</span></span>

[<span data-ttu-id="3987c-114">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3987c-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3987c-115">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="3987c-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3987c-116">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="3987c-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3987c-117">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="3987c-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3987c-118">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="3987c-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="3987c-119">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="3987c-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3987c-120">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="3987c-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3987c-121">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="3987c-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="3987c-122">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="3987c-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3987c-123">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="3987c-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]