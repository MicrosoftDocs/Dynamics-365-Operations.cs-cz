---
title: Přehled hodnocení a recenzí
description: Toto téma se týká hodnocení a recenzí v aplikaci Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 49587bb497288fc6f3ce77f04a378fc67056ecf2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002859"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="21027-103">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="21027-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="21027-104">Toto téma se týká hodnocení a recenzí v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21027-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="21027-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="21027-105">Overview</span></span>

<span data-ttu-id="21027-106">Hodnocení a recenze jsou rozhodující pro zákazníky v elektronickém obchodu, kteří chtějí vědět, jak ostatní zákazníci vnímali produkt.</span><span class="sxs-lookup"><span data-stu-id="21027-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="21027-107">Mohou také pomoci spotřebitelům provádět nákupní rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="21027-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="21027-108">V Dynamics 365 Commerce řešení hodnocení a recenzí umožňuje prodejcům zachytit recenze a hodnocení produktů od zákazníků.</span><span class="sxs-lookup"><span data-stu-id="21027-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="21027-109">Maloobchodní prodejci pak mohou zobrazit průměrné hodnocení a zkontrolovat informace na webu e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="21027-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="21027-110">Průměrné hodnocení je uvedeno v pokladním místě (POS) a v kanálech kontaktních center.</span><span class="sxs-lookup"><span data-stu-id="21027-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="21027-111">Proto je můžou zaměstnanci obchodů využít k tomu, aby pomohli uživatelům učinit rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="21027-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="21027-112">Hodnocení a recenze mohou také sloužit jako mechanismus zpětné vazby, který maloobchodní prodejci mohou použít ke zlepšení kvality produktu, a proto zvyšují prodej.</span><span class="sxs-lookup"><span data-stu-id="21027-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="21027-113">Funkce hodnocení a recenzí v aplikaci Dynamics 365 Commerce je omnikanálovým řešením a je nativně k dispozici jako součást platformy.</span><span class="sxs-lookup"><span data-stu-id="21027-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="21027-114">Řešení hodnocení a recenzí je postaveno nad Microsoft Azure, což poskytuje vysokou škálovatelnost a spolehlivost.</span><span class="sxs-lookup"><span data-stu-id="21027-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="21027-115">Následující ilustrace znázorňuje, jak funguje řešení hodnocení a recenzí v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21027-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Hodnocení a recenze v Dynamics 365 for Commerce](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="21027-117">Řešení hodnocení a recenzí v Dynamics 365 Commerce používá služby Azure Cognitive Services, které nabízí automatické moderování slov ve 40 jazycích.</span><span class="sxs-lookup"><span data-stu-id="21027-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="21027-118">Vzhledem k tomu, že lidské schválení není vyžadováno, dojde ke snížení nákladů moderování.</span><span class="sxs-lookup"><span data-stu-id="21027-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="21027-119">Systém také nabízí nástroje moderátorů, které lze použít k odpovědi na požadavky zákazníků, zpětnou vazbu a vyhlášení, a k adresování datových požadavků od uživatelů.</span><span class="sxs-lookup"><span data-stu-id="21027-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="21027-120">Řešení hodnocení a recenze poskytuje widgety, které zobrazují souhrny hodnocení v seznamech produktů, ve výsledcích vyhledávání, na stránce Podrobnosti produktu a na jiných místech.</span><span class="sxs-lookup"><span data-stu-id="21027-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="21027-121">V seznamech jsou uvedeny kompletní kontrolní seznamy, které také poskytují možnosti řazení a filtrování.</span><span class="sxs-lookup"><span data-stu-id="21027-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="21027-122">Řešení hodnocení a recenze také poskytuje šablonu Business Intelligence (BI), která obsahuje sadu metrik, která poskytuje přehledy hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="21027-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="21027-123">Data hodnocení a recenze lze exportovat pro další analýzu.</span><span class="sxs-lookup"><span data-stu-id="21027-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21027-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="21027-124">Additional resources</span></span>

[<span data-ttu-id="21027-125">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="21027-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="21027-126">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="21027-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="21027-127">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="21027-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="21027-128">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="21027-128">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
