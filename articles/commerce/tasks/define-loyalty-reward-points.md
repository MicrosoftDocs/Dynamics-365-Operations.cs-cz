---
title: " Definování bodů věrnostních odměn"
description: Tato procedura vás provede definováním bodů věrnostních odměn.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9557b25af0fba6429d34564e1a3e158b6258698a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021859"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="651b2-103"> Definování bodů věrnostních odměn</span><span class="sxs-lookup"><span data-stu-id="651b2-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="651b2-104">Tato procedura vás provede definováním bodů věrnostních odměn.</span><span class="sxs-lookup"><span data-stu-id="651b2-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="651b2-105">Body věrnostní odměny byste měli nastavit ještě před nastavením věrnostního programu.</span><span class="sxs-lookup"><span data-stu-id="651b2-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="651b2-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="651b2-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="651b2-107">Přejděte do nabídky Retail and Commerce > Odběratelé > Věrnost > Body věrnostní odměny.</span><span class="sxs-lookup"><span data-stu-id="651b2-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="651b2-108">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="651b2-108">Click New.</span></span>
3. <span data-ttu-id="651b2-109">Zadejte hodnotu do pole ID bodu odměny.</span><span class="sxs-lookup"><span data-stu-id="651b2-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="651b2-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="651b2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="651b2-111">Vyberte možnost v poli Typ bodu odměny.</span><span class="sxs-lookup"><span data-stu-id="651b2-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="651b2-112">Vyberte Množství, pokud chcete věrnostní body zaokrouhlit na nejbližší celé číslo.</span><span class="sxs-lookup"><span data-stu-id="651b2-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="651b2-113">Pokud chcete, aby body odměny byly zaokrouhlování podle pravidel zaokrouhlení měny, vyberte Množství.</span><span class="sxs-lookup"><span data-stu-id="651b2-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="651b2-114">Vyberete-li možnost Množství, přeskočte další krok této procedury.</span><span class="sxs-lookup"><span data-stu-id="651b2-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="651b2-115">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="651b2-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="651b2-116">Pro typ částky bodů odměny budou mít všechny udělené body vybranou měnu.</span><span class="sxs-lookup"><span data-stu-id="651b2-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="651b2-117">Pro body odměny pro typ množství toto pole nelze použít – vynechejte tento krok.</span><span class="sxs-lookup"><span data-stu-id="651b2-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="651b2-118">Zaškrtněte nebo zrušte zaškrtnutí políčka Lze uplatnit.</span><span class="sxs-lookup"><span data-stu-id="651b2-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="651b2-119">Zadejte číslo do pole Uplatnit hodnocení.</span><span class="sxs-lookup"><span data-stu-id="651b2-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="651b2-120">Uplatnit hodnocení se používá, když dvě nebo více uplatnitelných bodových odměn je možné použít pro zaplacení produktů.</span><span class="sxs-lookup"><span data-stu-id="651b2-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="651b2-121">Pokud dva body odměny mají stejné hodnocení pro uplatnění, pak se použije ten, který vyžaduje snížení počtu bodů.</span><span class="sxs-lookup"><span data-stu-id="651b2-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="651b2-122">Zadejte číslo do pole Hodnota času konce platnosti.</span><span class="sxs-lookup"><span data-stu-id="651b2-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="651b2-123">Body odměny vyprší za zadaný počet dní, měsíců nebo roků po jejich vydání.</span><span class="sxs-lookup"><span data-stu-id="651b2-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="651b2-124">Hodnota „0“ znamená, že body věrnostní odměny nikdy nevyprší.</span><span class="sxs-lookup"><span data-stu-id="651b2-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="651b2-125">Vyberte možnost v poli Jednotka času konce platnosti.</span><span class="sxs-lookup"><span data-stu-id="651b2-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="651b2-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="651b2-126">Click Save.</span></span>

