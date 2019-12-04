---
title: Odpisové metody a způsoby odpisu
description: Tento článek poskytuje přehled odpisových zásad a metod, které jsou podporovány v aplikaci Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3370db28f551b5ce4a9b49342cb0c0b2f3945c0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769493"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="f0cf8-103">Odpisové metody a způsoby odpisu</span><span class="sxs-lookup"><span data-stu-id="f0cf8-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0cf8-104">Tento článek poskytuje přehled podporovaných odpisových zásad a metod.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="f0cf8-105">K dispozici máte několik metod a způsobů odpisu.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="f0cf8-106">Metody slouží k přidělení odpisové hodnoty dlouhodobého majetku jednotlivým fiskálním obdobím.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="f0cf8-107">Odpisová hodnota dlouhodobého majetku je pořizovací cena snížená o likvidační hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="f0cf8-108">Používáte-li určitý způsob odpisu a změníte poslední datum zahájení odpisu určitého majetku, které přeskočí některé odpisy, bude odpis za poslední rok pravděpodobně vyšší nebo nižší, než bylo očekáváno.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="f0cf8-109">Odpis je nastaven podle počtu období ovlivněných změnou posledního data zahájení odpisu.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="f0cf8-110">Pokud například používáte půlroční způsob odpisu déle než tři roky, trvá odpis běžně přes 3 a půl roku.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="f0cf8-111">Změníte-li během tohoto období poslední datum spuštění odpisu, nebude v posledním roce odpisu zahrnut počet ovlivněných období.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="f0cf8-112">Posunete-li toto datum o tři měsíce, bude pro odpis v posledním roce důležitých devět měsíců, přičemž za normálních okolností by to bylo šest.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="f0cf8-113">K dispozici máte následující způsoby odpisu.</span><span class="sxs-lookup"><span data-stu-id="f0cf8-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="f0cf8-114">Pololetí</span><span class="sxs-lookup"><span data-stu-id="f0cf8-114">Half year</span></span>
-   <span data-ttu-id="f0cf8-115">Celý měsíc</span><span class="sxs-lookup"><span data-stu-id="f0cf8-115">Full month</span></span>
-   <span data-ttu-id="f0cf8-116">Polovina čtvrtletí</span><span class="sxs-lookup"><span data-stu-id="f0cf8-116">Mid quarter</span></span>
-   <span data-ttu-id="f0cf8-117">Polovina měsíce (1. den v měsíci)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="f0cf8-118">Polovina měsíce (15. den v měsíci)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="f0cf8-119">Pololetí (počátek roku)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-119">Half year (start of year)</span></span>
-   <span data-ttu-id="f0cf8-120">Pololetí (příští rok)</span><span class="sxs-lookup"><span data-stu-id="f0cf8-120">Half year (next year)</span></span>

<span data-ttu-id="f0cf8-121">Můžete vybírat z následujících metod odpisování:</span><span class="sxs-lookup"><span data-stu-id="f0cf8-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="f0cf8-122">Lineární</span><span class="sxs-lookup"><span data-stu-id="f0cf8-122">Straight line service life</span></span>
-   <span data-ttu-id="f0cf8-123">Zrychleně</span><span class="sxs-lookup"><span data-stu-id="f0cf8-123">Reducing balance</span></span>
-   <span data-ttu-id="f0cf8-124">Ručně</span><span class="sxs-lookup"><span data-stu-id="f0cf8-124">Manual</span></span>
-   <span data-ttu-id="f0cf8-125">Koeficient</span><span class="sxs-lookup"><span data-stu-id="f0cf8-125">Factor</span></span>
-   <span data-ttu-id="f0cf8-126">Spotřeba</span><span class="sxs-lookup"><span data-stu-id="f0cf8-126">Consumption</span></span>
-   <span data-ttu-id="f0cf8-127">Lineární s vyrovnáním na konci životnosti</span><span class="sxs-lookup"><span data-stu-id="f0cf8-127">Straight line life remaining</span></span>
-   <span data-ttu-id="f0cf8-128">Degresivní 200 %</span><span class="sxs-lookup"><span data-stu-id="f0cf8-128">200% reducing balance</span></span>
-   <span data-ttu-id="f0cf8-129">Degresivní 175 %</span><span class="sxs-lookup"><span data-stu-id="f0cf8-129">175% reducing balance</span></span>
-   <span data-ttu-id="f0cf8-130">Degresivní 150 %</span><span class="sxs-lookup"><span data-stu-id="f0cf8-130">150% reducing balance</span></span>
-   <span data-ttu-id="f0cf8-131">Degresivní 125 %</span><span class="sxs-lookup"><span data-stu-id="f0cf8-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="f0cf8-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f0cf8-132">Additional resources</span></span>
--------

[<span data-ttu-id="f0cf8-133">Odpisy dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="f0cf8-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="f0cf8-134">Lineární odpisování</span><span class="sxs-lookup"><span data-stu-id="f0cf8-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="f0cf8-135">Degresivní odpis</span><span class="sxs-lookup"><span data-stu-id="f0cf8-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="f0cf8-136">Ruční odpis</span><span class="sxs-lookup"><span data-stu-id="f0cf8-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="f0cf8-137">Odpis koeficientem</span><span class="sxs-lookup"><span data-stu-id="f0cf8-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="f0cf8-138">Odpis spotřeby</span><span class="sxs-lookup"><span data-stu-id="f0cf8-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="f0cf8-139">Lineární odpis s vyrovnáním na konci životnosti</span><span class="sxs-lookup"><span data-stu-id="f0cf8-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="f0cf8-140">Degresivní odpis 125 procent</span><span class="sxs-lookup"><span data-stu-id="f0cf8-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="f0cf8-141">Degresivní odpis 150 procent</span><span class="sxs-lookup"><span data-stu-id="f0cf8-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="f0cf8-142">Degresivní odpis 175 procent</span><span class="sxs-lookup"><span data-stu-id="f0cf8-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="f0cf8-143">Degresivní odpis 200 procent</span><span class="sxs-lookup"><span data-stu-id="f0cf8-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



