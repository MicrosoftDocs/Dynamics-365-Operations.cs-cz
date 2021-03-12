---
title: Počáteční mimořádný odpis
description: Tento článek podává přehled o funkci počátečního mimořádného odpisu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41a59b9dfe0482c995cfefc7a70f63550794428d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969171"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="964dd-103">Počáteční mimořádný odpis</span><span class="sxs-lookup"><span data-stu-id="964dd-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="964dd-104">Tento článek podává přehled o funkci počátečního mimořádného odpisu.</span><span class="sxs-lookup"><span data-stu-id="964dd-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="964dd-105">U mimořádných odpisů můžete odepsat vedlejší nebo mimořádné částky během prvního roku, ve kterém se majetek začal používat a odepisovat.</span><span class="sxs-lookup"><span data-stu-id="964dd-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="964dd-106">Počáteční mimořádné odpisy musí být provedeny před veškerými jinými výpočty odpisů.</span><span class="sxs-lookup"><span data-stu-id="964dd-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="964dd-107">Proto doporučujeme použít počáteční mimořádné odpisy s knihami, kde je zakázána funkce zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="964dd-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="964dd-108">Můžete použít možnost **Odstranit transakce nezaúčtované do hlavní knihy** k odstranění historických transakcí pro knihy, které nechcete zaúčtovat do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="964dd-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="964dd-109">Počáteční mimořádný odpis pak můžete uzpůsobit v cyklu majetku odstraněním transakcí odpisů, které byly dříve zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="964dd-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="964dd-110">Počáteční mimořádný odpis lze vypočítat pomocí procesu navrhování nebo lze transakce počátečního mimořádného odpisu vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="964dd-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="964dd-111">Transakce počátečního mimořádného odpisu nelze vytvořit, pokud již odpisové transakce nebo transakce opravy odpisu pro danou knihu odpisů majetku existují.</span><span class="sxs-lookup"><span data-stu-id="964dd-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="964dd-112">Pokud pro výpočet počátečního mimořádného odpisu použijete proces navrhování, všechny existující transakce počátečního mimořádného budou zahrnuty do výpočtu základu.</span><span class="sxs-lookup"><span data-stu-id="964dd-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="964dd-113">Výpočet zahrnuje také všechny předchozí počáteční mimořádné odpisy, které jste pro daný majetek zadali ručně.</span><span class="sxs-lookup"><span data-stu-id="964dd-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="964dd-114">Pokud bude u majetku provedeno více počátečních mimořádných odpisů, zváží se jejich priorita.</span><span class="sxs-lookup"><span data-stu-id="964dd-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="964dd-115">Každý bonus snižuje základ majetku pro další počáteční mimořádný odpis.</span><span class="sxs-lookup"><span data-stu-id="964dd-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="964dd-116">Konečná zůstatková hodnota se v majetkovém základu pro výpočty počátečního mimořádného odpisu nebere v potaz a způsob odpisu se na počáteční mimořádný odpis nevztahuje.</span><span class="sxs-lookup"><span data-stu-id="964dd-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="964dd-117">Ve Spojených státech amerických je v současné době některý majetek považován za majetek podle paragrafu 179.</span><span class="sxs-lookup"><span data-stu-id="964dd-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="964dd-118">Pomocí odpočtu podle paragrafu 179 lze získat zpět část nebo celou hodnotu určitého majetku (až do určité výše).</span><span class="sxs-lookup"><span data-stu-id="964dd-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="964dd-119">Náklady lze získat zpět jejich odečtením v roce, ve kterém začal být majetek používán.</span><span class="sxs-lookup"><span data-stu-id="964dd-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="964dd-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="964dd-120">Example</span></span>
<span data-ttu-id="964dd-121">Předpokládejme, že následující počáteční mimořádné odpisy jsou přiřazeny ke knize odpisů majetku:</span><span class="sxs-lookup"><span data-stu-id="964dd-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="964dd-122">**Článek 179:** 1 000,00, priorita 1</span><span class="sxs-lookup"><span data-stu-id="964dd-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="964dd-123">**Volná zóna:** 30 procent, priorita 2</span><span class="sxs-lookup"><span data-stu-id="964dd-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="964dd-124">Předpokládejme, že pořizovací cena majetku je 5 000 USD.</span><span class="sxs-lookup"><span data-stu-id="964dd-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="964dd-125">Při výpočtu počátečního mimořádného odpisu bude pro odpis Článku 179 částka počátečního mimořádného odpisu 1 000 USD.</span><span class="sxs-lookup"><span data-stu-id="964dd-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="964dd-126">Další částka počátečního mimořádného odpisu - pro odpis ve volné zóně - se vypočítá pomocí následující kalkulace:</span><span class="sxs-lookup"><span data-stu-id="964dd-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="964dd-127">Pořizovací cena - 1 000 USD (odpis podle článku 179) x 30 procent = 1 200 USD.</span><span class="sxs-lookup"><span data-stu-id="964dd-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="964dd-128">Pokud je částka počátečního mimořádného odpisu větší než zbývající pořizovací cena, bude částka počátečního mimořádného odpisu výsledkem výpočtu pro počáteční mimořádný odpis nebo zbývající pořizovací cena podle toho, která je nižší.</span><span class="sxs-lookup"><span data-stu-id="964dd-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="964dd-129">Pokud se zbývající pořizovací cena rovná 0 (nule) nebo je nižší, nebudou se transakce počátečního mimořádného odpisu generovat.</span><span class="sxs-lookup"><span data-stu-id="964dd-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="964dd-130">Když se počáteční mimořádný odpis vypočítá pomocí procesu navrhování, vytvoří se transakce počátečního mimořádného odpisu pro všechny odpovídající záznamy počátečního mimořádného odpisu, které jsou přiřazeny ke knize odpisů majetku.</span><span class="sxs-lookup"><span data-stu-id="964dd-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="964dd-131">Lze vytvořit neomezený počet záznamů počátečního mimořádného odpisu.</span><span class="sxs-lookup"><span data-stu-id="964dd-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="964dd-132">Jakmile tyto záznamy přiřadíte ke knize odpisů skupiny majetku, použijí se i v knize odpisů majetku.</span><span class="sxs-lookup"><span data-stu-id="964dd-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="964dd-133">Počáteční mimořádný odpis se zadává buď jako procento, nebo jako pevná částka.</span><span class="sxs-lookup"><span data-stu-id="964dd-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="964dd-134">Při zaúčtování návrhů na odpisy budou transakce počátečního mimořádného odpisu zaúčtovány do knihy odpisů jako transakce, které jsou odděleny od odpisových transakcí.</span><span class="sxs-lookup"><span data-stu-id="964dd-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>



