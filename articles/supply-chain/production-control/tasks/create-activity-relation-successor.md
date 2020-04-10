---
title: Vytvoření relace aktivity - následník
description: Tok aktivit ve štíhlém výrobním toku je zaznamenán prostřednictvím vztahů aktivity.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfd9d515b9417ce0142b7bf5db3485902968e4de
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149290"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="492b2-103">Vytvoření relace aktivity - následník</span><span class="sxs-lookup"><span data-stu-id="492b2-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="492b2-104">Tok aktivit ve štíhlém výrobním toku je zaznamenán prostřednictvím vztahů aktivity.</span><span class="sxs-lookup"><span data-stu-id="492b2-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="492b2-105">Tento záznam ukazuje, jak vytvořit relaci aktivity.</span><span class="sxs-lookup"><span data-stu-id="492b2-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="492b2-106">Požadavky:</span><span class="sxs-lookup"><span data-stu-id="492b2-106">Prerequisites:</span></span>

- <span data-ttu-id="492b2-107">Výrobní tok a verze v režimu konceptu.</span><span class="sxs-lookup"><span data-stu-id="492b2-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="492b2-108">Dvě aktivity, které po sobě navzájem následují ve výrobním toku, jsou vytvořeny, ale nesouvisí.</span><span class="sxs-lookup"><span data-stu-id="492b2-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="492b2-109">Najděte verzi výrobního toku</span><span class="sxs-lookup"><span data-stu-id="492b2-109">Find the production flow version</span></span> 
1. <span data-ttu-id="492b2-110">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="492b2-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="492b2-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="492b2-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="492b2-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="492b2-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="492b2-113">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="492b2-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="492b2-114">V seznamu vyberte verzi konceptu.</span><span class="sxs-lookup"><span data-stu-id="492b2-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="492b2-115">Vztahy aktivit lze přidat do konceptu nebo aktivních verzí výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="492b2-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="492b2-116">Otevřete přehled aktivit</span><span class="sxs-lookup"><span data-stu-id="492b2-116">Open the activity overview</span></span>
1. <span data-ttu-id="492b2-117">Klepněte na aktivity.</span><span class="sxs-lookup"><span data-stu-id="492b2-117">Click Activities.</span></span>
    * <span data-ttu-id="492b2-118">Nezapomeňte, že ve formuláři se zobrazují všechny aktivity výrobního toku přidělené k verzi výrobního toku, ve kterém pracujete.</span><span class="sxs-lookup"><span data-stu-id="492b2-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="492b2-119">Přidejte následníka</span><span class="sxs-lookup"><span data-stu-id="492b2-119">Add a Successor</span></span>
1. <span data-ttu-id="492b2-120">Klepněte na Přidat následníka.</span><span class="sxs-lookup"><span data-stu-id="492b2-120">Click Add successor.</span></span>
2. <span data-ttu-id="492b2-121">V poli Aktivita klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="492b2-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="492b2-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="492b2-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="492b2-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="492b2-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="492b2-124">Zaškrtněte políčko Omezení.</span><span class="sxs-lookup"><span data-stu-id="492b2-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="492b2-125">V poli Hodnota omezení zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="492b2-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="492b2-126">Omezení času je čas naplánovaný mezi naplánovaným koncem předchůdce (datum splatnosti a čas) a plánovaným začátkem nástupce.</span><span class="sxs-lookup"><span data-stu-id="492b2-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="492b2-127">Zadejte hodnotu do pole Jednotky.</span><span class="sxs-lookup"><span data-stu-id="492b2-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="492b2-128">Do pole Poměr času cyklu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="492b2-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="492b2-129">Pokud obě aktivity běží ve stejném taktu, poměr času cyklu musí být 1.</span><span class="sxs-lookup"><span data-stu-id="492b2-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="492b2-130">Pokud předchůdce běží dvojnásobnou rychlostí následníka, poměr musí být 2.</span><span class="sxs-lookup"><span data-stu-id="492b2-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="492b2-131">Poměry času cyklu se používají pro výpočet jednotlivých časů cyklu aktivit výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="492b2-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="492b2-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="492b2-132">Click OK.</span></span>
10. <span data-ttu-id="492b2-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="492b2-133">Close the page.</span></span>
11. <span data-ttu-id="492b2-134">Klepněte na kartu panel mřížky.</span><span class="sxs-lookup"><span data-stu-id="492b2-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="492b2-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="492b2-135">Close the page.</span></span>
13. <span data-ttu-id="492b2-136">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="492b2-136">Refresh the page.</span></span>

