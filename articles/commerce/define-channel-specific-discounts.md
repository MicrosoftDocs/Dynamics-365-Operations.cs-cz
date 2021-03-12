---
title: Definovat slevy specifické pro kanál
description: Maloobchodní prodejci často nastavují různé slevy v různých kanálech. Toto téma popisuje koncepty, které je nutné znát k vytvoření slevy pro konkrétní kanál.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991383"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="f2842-104">Definování slev specifických pro kanál</span><span class="sxs-lookup"><span data-stu-id="f2842-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2842-105">Toto téma popisuje koncepty, které je nutné znát k vytvoření slevy pro konkrétní kanál.</span><span class="sxs-lookup"><span data-stu-id="f2842-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="f2842-106">Slevy specifické pro kanál</span><span class="sxs-lookup"><span data-stu-id="f2842-106">Channel-specific discounts</span></span>

<span data-ttu-id="f2842-107">Maloobchodní prodejci často nabízejí různé slevy v různých kanálech.</span><span class="sxs-lookup"><span data-stu-id="f2842-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="f2842-108">Činí tak z důvodu přizpůsobení místním tržním podmínkám nebo v rámci konkurenčního souboje s jinými maloobchodními prodejci.</span><span class="sxs-lookup"><span data-stu-id="f2842-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="f2842-109">Commerce používá cenové skupiny pro definování slev specifických pro kanál.</span><span class="sxs-lookup"><span data-stu-id="f2842-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="f2842-110">Cenové skupiny lze přiřadit následujícím entitám (jedné entitě nebo více entitám): kanály, katalogy, umístění a věrnostní programy.</span><span class="sxs-lookup"><span data-stu-id="f2842-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="f2842-111">V tomto článku jsou popsány kanály, ale stejné principy se týkají také slevových katalogů, slev podle umístění a věrnostních slev.</span><span class="sxs-lookup"><span data-stu-id="f2842-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="f2842-112">Cenové skupiny</span><span class="sxs-lookup"><span data-stu-id="f2842-112">Price groups</span></span>

<span data-ttu-id="f2842-113">[![Cenové skupiny](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="f2842-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="f2842-114">Ve výše uvedeném diagramu je znázorněn vztah mezi entitami, které mohou být v transakci (kanál, katalog, umístění, odběratel, věrnostní karta), a různými typy slev, které lze konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="f2842-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="f2842-115">Ke všem transakcím dochází v kanálu, takže přítomnost kanálu v transakci je zaručena.</span><span class="sxs-lookup"><span data-stu-id="f2842-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="f2842-116">Zbývající entity jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="f2842-116">The remaining entities are optional.</span></span> <span data-ttu-id="f2842-117">Na všech stránkách hlavních dat se nachází odkaz na související stránku cenové skupiny, na které si můžete prohlédnout cenové skupiny a v případě potřeby přidat další.</span><span class="sxs-lookup"><span data-stu-id="f2842-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="f2842-118">Cenová skupina se používá k propojení čtyř typů entit se slevami, úpravami cen a obchodními smlouvami.</span><span class="sxs-lookup"><span data-stu-id="f2842-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="f2842-119">Doporučujeme, abyste si naplánovali princip, jakým budete cenové skupiny pojmenovávat, aby se vám dobře spravovaly.</span><span class="sxs-lookup"><span data-stu-id="f2842-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="f2842-120">Jednou z možností je použít písmeno či číslo jako předponu nebo příponu, podle které bude možné rozlišit různé typy.</span><span class="sxs-lookup"><span data-stu-id="f2842-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="f2842-121">Název ve formátu „1-xxxxx“ může například odkazovat na cenové skupiny pro kanály a název ve formátu „2-xxxxx“ na cenové skupiny pro katalog.</span><span class="sxs-lookup"><span data-stu-id="f2842-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="f2842-122">Existují čtyři stránky s dotazy – každá z nich je zaměřená na entity commerce, které mohou mít přidruženy slevy.</span><span class="sxs-lookup"><span data-stu-id="f2842-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="f2842-123">**Cenové skupiny kanálů** – Na této stránce je uveden seznam kanálů a slev propojených pro každou cenovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="f2842-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="f2842-124">**Skupiny katalogových cen** – Na této stránce je uveden seznam katalogů a slev propojených pro každou cenovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="f2842-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="f2842-125">**Věrnostní cenové skupiny** – Na této stránce je uveden seznam věrnostních programů a slev propojených pro každou cenovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="f2842-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="f2842-126">**Cenové skupiny umístění** – Na této stránce je uveden seznam umístění a slev propojených pro každou cenovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="f2842-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="f2842-127">Příklad nastavení slevy pro kanál</span><span class="sxs-lookup"><span data-stu-id="f2842-127">Example channel discount set up</span></span>

<span data-ttu-id="f2842-128">Na následujícím příkladu jsou znázorněny úkoly zahrnuté do nastavování slevy pro kanál.</span><span class="sxs-lookup"><span data-stu-id="f2842-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="f2842-129">V tomto příkladu máte kanál nazvaný **Houston** a chystáte se vytvořit novou slevu nazvanou **Zpět do školy**.</span><span class="sxs-lookup"><span data-stu-id="f2842-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="f2842-130">Vzhledem k tomu, že strategie cen a slev zahrnuje možnost slev pro kanál, při vytvoření kanálu vždy vytvoříte cenovou skupinu specifickou pro kanál.</span><span class="sxs-lookup"><span data-stu-id="f2842-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="f2842-131">Máte cenovou skupinu **Houston-CS**, která je přiřazena ke kanálu **Houston**.</span><span class="sxs-lookup"><span data-stu-id="f2842-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="f2842-132">Po vytvoření nové slevy  **Zpět do školy** je nutné kliknout na tlačítko **Cenové skupiny** v horní části stránky **Sleva**.</span><span class="sxs-lookup"><span data-stu-id="f2842-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="f2842-133">Otevře se stránka **Skupiny slevových cen**.</span><span class="sxs-lookup"><span data-stu-id="f2842-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="f2842-134">Poté klikněte na tlačítko **Nový** a vyberte cenovou skupinu **Houston-CS**.</span><span class="sxs-lookup"><span data-stu-id="f2842-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="f2842-135">Nyní můžete povolit slevu a zadat ji do kanálu.</span><span class="sxs-lookup"><span data-stu-id="f2842-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2842-136">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f2842-136">Additional resources</span></span>

[<span data-ttu-id="f2842-137">Úpravy ceny a slevy</span><span class="sxs-lookup"><span data-stu-id="f2842-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
