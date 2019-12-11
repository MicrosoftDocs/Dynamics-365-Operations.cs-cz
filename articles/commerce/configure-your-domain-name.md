---
title: Konfigurace názvu domény
description: Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770451"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="17751-103">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="17751-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="17751-104">Toto téma vysvětluje, jak nakonfigurovat název domény pro web elektronického obchodu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="17751-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="17751-105">Přidání domén při inicializaci elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="17751-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="17751-106">Chcete-li přidružit domény k prostředí elektronického obchodu, inicializujte elektronický obchod způsobem popsaným v tématu [Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="17751-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="17751-107">Během inicializace budete požádáni o poskytnutí informací, které budou použity k zajištění prostředí elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="17751-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="17751-108">V poli **Podporované názvy hostitelů** přidejte všechny domény, které chcete používat s tímto prostředím.</span><span class="sxs-lookup"><span data-stu-id="17751-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="17751-109">Více domén je třeba oddělit středníkem.</span><span class="sxs-lookup"><span data-stu-id="17751-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="17751-110">Tímto způsobem jsou domény konfigurovány ve všech požadovaných součástech elektronického obchodu a jsou připraveny k použití při přepnutí provozu ze sítě CDN (Content Delivery Network) nebo z webového serveru a ukazují na front-endy elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="17751-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="17751-111">Přidání domén po inicializaci elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="17751-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="17751-112">Chcete-li po inicializaci elektronického obchodu přidružit nové domény k prostředí elektronického obchodu, je nutné odeslat požadavek na službu.</span><span class="sxs-lookup"><span data-stu-id="17751-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17751-113">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="17751-113">Additional resources</span></span>

[<span data-ttu-id="17751-114">Přehled online obchodu</span><span class="sxs-lookup"><span data-stu-id="17751-114">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="17751-115">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="17751-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="17751-116">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="17751-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="17751-117">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="17751-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="17751-118">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="17751-118">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="17751-119">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="17751-119">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="17751-120">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="17751-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
