--- 
title: " Úpravy maloobchodních cen"
description: "Tato procedura vás provede vytvořením úpravy maloobchodní ceny."
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: ba6301329b23b8b4e167e292c1126806bf07d3ba
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="d997f-103"> Úpravy maloobchodních cen</span><span class="sxs-lookup"><span data-stu-id="d997f-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d997f-104">Tato procedura vás provede vytvořením úpravy maloobchodní ceny.</span><span class="sxs-lookup"><span data-stu-id="d997f-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="d997f-105">Úpravou maloobchodní ceny lze přímo nastavit prodejní cenu zboží, změnit jeho základní prodejní cenu nebo prodejní cenu obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="d997f-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="d997f-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="d997f-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="d997f-107">Klikněte na Správa cen a slev.</span><span class="sxs-lookup"><span data-stu-id="d997f-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="d997f-108">Klikněte na kartu Úpravy ceny.</span><span class="sxs-lookup"><span data-stu-id="d997f-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="d997f-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d997f-109">Click New.</span></span>
    * <span data-ttu-id="d997f-110">Odtud můžete vytvořit všechna nejčastěji používaná pravidla pro ceny a slevy, včetně maloobchodních slev, úprav cen, deníků obchodních smluv a pravidel pro oceňování kategorií.</span><span class="sxs-lookup"><span data-stu-id="d997f-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="d997f-111">Klikněte na Úprava ceny.</span><span class="sxs-lookup"><span data-stu-id="d997f-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="d997f-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d997f-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d997f-113">Rozbalte sekci Řádky.</span><span class="sxs-lookup"><span data-stu-id="d997f-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="d997f-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d997f-114">Click Add.</span></span>
    * <span data-ttu-id="d997f-115">V tomto příkladu zadejte v poli Produkt hodnotu „81126“.</span><span class="sxs-lookup"><span data-stu-id="d997f-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="d997f-116">Potom v poli Procento slevy zadat hodnotu „10,0“.</span><span class="sxs-lookup"><span data-stu-id="d997f-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="d997f-117">Úprava ceny typu procentní slevy sníží základní prodejní cenu nebo prodejní cenu pro obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="d997f-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="d997f-118">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="d997f-118">Click Add.</span></span>
    * <span data-ttu-id="d997f-119">V tomto příkladu zadejte v poli Produkt hodnotu „81125“.</span><span class="sxs-lookup"><span data-stu-id="d997f-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="d997f-120">V poli Metoda slevy, vyberte „Částka platební slevy“.</span><span class="sxs-lookup"><span data-stu-id="d997f-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="d997f-121">Nakonec zadejte do pole Částka platební slevy hodnotu „5,0“.</span><span class="sxs-lookup"><span data-stu-id="d997f-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="d997f-122">Typ slevy Částka platební slevy je částka převzatá ze základní ceny nebo ceny obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="d997f-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="d997f-123">Klikněte na možnost Cenové skupiny.</span><span class="sxs-lookup"><span data-stu-id="d997f-123">Click Price groups.</span></span>
    * <span data-ttu-id="d997f-124">Vyberte v poli Cenová skupina hodnotu „RP-Houston“.</span><span class="sxs-lookup"><span data-stu-id="d997f-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="d997f-125">Tím bude úprava ceny přidružena obchodu Houston.</span><span class="sxs-lookup"><span data-stu-id="d997f-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="d997f-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d997f-126">Click Save.</span></span>
11. <span data-ttu-id="d997f-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d997f-127">Close the page.</span></span>
12. <span data-ttu-id="d997f-128">V poli Stav vyberte možnost „Povoleno“.</span><span class="sxs-lookup"><span data-stu-id="d997f-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="d997f-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d997f-129">Click Save.</span></span>
14. <span data-ttu-id="d997f-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d997f-130">Close the page.</span></span>
15. <span data-ttu-id="d997f-131">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="d997f-131">Refresh the page.</span></span>


