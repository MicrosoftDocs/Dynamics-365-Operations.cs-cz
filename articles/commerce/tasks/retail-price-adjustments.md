---
title: " Úpravy maloobchodních cen"
description: Tato procedura vás provede vytvořením úpravy velkoobchodní ceny.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7443f69473c0aad478d47f80f284b1156bad9c24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962978"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="6a501-103"> Úpravy maloobchodních cen</span><span class="sxs-lookup"><span data-stu-id="6a501-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a501-104">Tato procedura vás provede vytvořením úpravy velkoobchodní ceny.</span><span class="sxs-lookup"><span data-stu-id="6a501-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="6a501-105">Úpravou velkoobchodní ceny lze přímo nastavit prodejní cenu zboží, změnit jeho základní prodejní cenu nebo prodejní cenu obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6a501-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="6a501-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="6a501-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="6a501-107">Klikněte na Správa cen a slev.</span><span class="sxs-lookup"><span data-stu-id="6a501-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="6a501-108">Klikněte na kartu Úpravy ceny.</span><span class="sxs-lookup"><span data-stu-id="6a501-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="6a501-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6a501-109">Click New.</span></span>
    * <span data-ttu-id="6a501-110">Odtud můžete vytvořit všechna nejčastěji používaná pravidla pro ceny a slevy, včetně slev, úprav cen, deníků obchodních smluv a pravidel pro oceňování kategorií.</span><span class="sxs-lookup"><span data-stu-id="6a501-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="6a501-111">Klikněte na Úprava ceny.</span><span class="sxs-lookup"><span data-stu-id="6a501-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="6a501-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="6a501-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6a501-113">Rozbalte sekci Řádky.</span><span class="sxs-lookup"><span data-stu-id="6a501-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="6a501-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6a501-114">Click Add.</span></span>
    * <span data-ttu-id="6a501-115">V tomto příkladu zadejte v poli Produkt hodnotu „81126“.</span><span class="sxs-lookup"><span data-stu-id="6a501-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="6a501-116">Potom v poli Procento slevy zadat hodnotu „10,0“.</span><span class="sxs-lookup"><span data-stu-id="6a501-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="6a501-117">Úprava ceny typu procentní slevy sníží základní prodejní cenu nebo prodejní cenu pro obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6a501-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="6a501-118">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6a501-118">Click Add.</span></span>
    * <span data-ttu-id="6a501-119">V tomto příkladu zadejte v poli Produkt hodnotu „81125“.</span><span class="sxs-lookup"><span data-stu-id="6a501-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="6a501-120">V poli Metoda slevy, vyberte „Částka platební slevy“.</span><span class="sxs-lookup"><span data-stu-id="6a501-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="6a501-121">Nakonec zadejte do pole Částka platební slevy hodnotu „5,0“.</span><span class="sxs-lookup"><span data-stu-id="6a501-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="6a501-122">Typ slevy Částka platební slevy je částka převzatá ze základní ceny nebo ceny obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6a501-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="6a501-123">Klikněte na možnost Cenové skupiny.</span><span class="sxs-lookup"><span data-stu-id="6a501-123">Click Price groups.</span></span>
    * <span data-ttu-id="6a501-124">Vyberte v poli Cenová skupina hodnotu „RP-Houston“.</span><span class="sxs-lookup"><span data-stu-id="6a501-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="6a501-125">Tím bude úprava ceny přidružena obchodu Houston.</span><span class="sxs-lookup"><span data-stu-id="6a501-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="6a501-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6a501-126">Click Save.</span></span>
11. <span data-ttu-id="6a501-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6a501-127">Close the page.</span></span>
12. <span data-ttu-id="6a501-128">V poli Stav vyberte možnost „Povoleno“.</span><span class="sxs-lookup"><span data-stu-id="6a501-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="6a501-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6a501-129">Click Save.</span></span>
14. <span data-ttu-id="6a501-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6a501-130">Close the page.</span></span>
15. <span data-ttu-id="6a501-131">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="6a501-131">Refresh the page.</span></span>

