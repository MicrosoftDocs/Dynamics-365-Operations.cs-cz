---
title: " Cenová pravidla kategorií pro vytváření obchodních smluv"
description: Tato procedura ukazuje, jak vytvořit obchodní smlouvy o prodejních cenách pomocí kategorizace cenových pravidel.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21b1986aa36aab23f50a5af434435f9e93318e45
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141076"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="142f6-103"> Cenová pravidla kategorií pro vytváření obchodních smluv</span><span class="sxs-lookup"><span data-stu-id="142f6-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="142f6-104">Tato procedura ukazuje, jak vytvořit obchodní smlouvy o prodejních cenách pomocí kategorizace cenových pravidel.</span><span class="sxs-lookup"><span data-stu-id="142f6-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="142f6-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="142f6-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="142f6-106">Tento úkol je určen pro roli Manažer prodeje Commerce.</span><span class="sxs-lookup"><span data-stu-id="142f6-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="142f6-107">Klikněte na Správa cen a slev.</span><span class="sxs-lookup"><span data-stu-id="142f6-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="142f6-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="142f6-108">Click New.</span></span>
3. <span data-ttu-id="142f6-109">Klikněte na Cenové pravidlo kategorie.</span><span class="sxs-lookup"><span data-stu-id="142f6-109">Click Category price rule.</span></span>
4. <span data-ttu-id="142f6-110">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="142f6-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="142f6-111">Vyberte možnost v poli Kód účtu.</span><span class="sxs-lookup"><span data-stu-id="142f6-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="142f6-112">Kód typu účtu „Skupina“ se používá pro stanovení obchodních smluv o prodejních cenách, které jsou specifické pro kanály, věrnostní programy, katalogy a umístění.</span><span class="sxs-lookup"><span data-stu-id="142f6-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="142f6-113">V poli Výběr účtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="142f6-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="142f6-114">V poli Kategorie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="142f6-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="142f6-115">Zadejte číslo do pole Částka/procenta.</span><span class="sxs-lookup"><span data-stu-id="142f6-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="142f6-116">V poli Verze zaokrouhlování zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="142f6-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="142f6-117">Klikněte na možnost Generovat obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="142f6-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="142f6-118">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="142f6-118">Click Next.</span></span>
12. <span data-ttu-id="142f6-119">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="142f6-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="142f6-120">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="142f6-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="142f6-121">Vyberte možnost Ano v poli Najít další.</span><span class="sxs-lookup"><span data-stu-id="142f6-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="142f6-122">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="142f6-122">Click Next.</span></span>
16. <span data-ttu-id="142f6-123">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="142f6-123">Click Finish.</span></span>
    * <span data-ttu-id="142f6-124">Tím vytvoříte deník obchodních smluv a otevře jej pro kontrolu.</span><span class="sxs-lookup"><span data-stu-id="142f6-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="142f6-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="142f6-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="142f6-126">Deníky obchodních smluv, které jsou vytvořeny z Kategorizace cenových pravidel, nebudou zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="142f6-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="142f6-127">Můžete zkontrolovat a upravit ceny vygenerované před jejich zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="142f6-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="142f6-128">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="142f6-128">Click Edit.</span></span>
19. <span data-ttu-id="142f6-129">Zadejte číslo do pole Částka v měně.</span><span class="sxs-lookup"><span data-stu-id="142f6-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="142f6-130">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="142f6-130">Click Post.</span></span>
21. <span data-ttu-id="142f6-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="142f6-131">Click OK.</span></span>
22. <span data-ttu-id="142f6-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="142f6-132">Close the page.</span></span>
23. <span data-ttu-id="142f6-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="142f6-133">Close the page.</span></span>
24. <span data-ttu-id="142f6-134">Klikněte na kartu Cenová pravidla kategorie.</span><span class="sxs-lookup"><span data-stu-id="142f6-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="142f6-135">Kategorizace cenových pravidel specifická pro kanál se zobrazí na tomto seznamu.</span><span class="sxs-lookup"><span data-stu-id="142f6-135">Channel specific Category pricing rules will show in this list.</span></span>  

