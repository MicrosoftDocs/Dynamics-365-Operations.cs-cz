--- 
title: "Přidání předchůdce k aktivitě výrobního toku"
description: "Ve verzi výrobního toku musí být všechny aktivity seřazeny."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9acb1c2672af70f535f3dce1c8f5a97e8d479158
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="b4a69-103">Přidání předchůdce k aktivitě výrobního toku</span><span class="sxs-lookup"><span data-stu-id="b4a69-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4a69-104">Ve verzi výrobního toku musí být všechny aktivity seřazeny.</span><span class="sxs-lookup"><span data-stu-id="b4a69-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="b4a69-105">Aktivita může mít jednoho nebo více předchůdců nebo následníků.</span><span class="sxs-lookup"><span data-stu-id="b4a69-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="b4a69-106">Tato procedura ukazuje, jak přidružit předchůdce k aktivitě.</span><span class="sxs-lookup"><span data-stu-id="b4a69-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="b4a69-107">K provedení tohoto úkolu potřebujete výrobní tok, který má verzi konceptu s alespoň dvěma aktivitami, které mohou být propojeny.</span><span class="sxs-lookup"><span data-stu-id="b4a69-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="b4a69-108">Další informace naleznete v dokumentu white paper "Production flows and activities in lean manufacturing." (Výrobní toky a aktivity v lean manufacturing.)</span><span class="sxs-lookup"><span data-stu-id="b4a69-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="b4a69-109">Vyhledání výrobního toku a verze</span><span class="sxs-lookup"><span data-stu-id="b4a69-109">Find the production flow and version</span></span>
1. <span data-ttu-id="b4a69-110">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="b4a69-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b4a69-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b4a69-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b4a69-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b4a69-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b4a69-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b4a69-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b4a69-114">Klepněte na aktivity.</span><span class="sxs-lookup"><span data-stu-id="b4a69-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="b4a69-115">Výběr aktivity a přidání předchůdce</span><span class="sxs-lookup"><span data-stu-id="b4a69-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="b4a69-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b4a69-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="b4a69-117">Klikněte na Přidat předchůdce.</span><span class="sxs-lookup"><span data-stu-id="b4a69-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="b4a69-118">V poli Aktivita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4a69-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="b4a69-119">Do pole Poměr času cyklu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b4a69-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="b4a69-120">Výchozí poměr času cyklu relace aktivity je 1.</span><span class="sxs-lookup"><span data-stu-id="b4a69-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="b4a69-121">Předpokladem je, aby obě aktivity byly spuštěna stejným tempem nebo ve stejné délce výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="b4a69-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="b4a69-122">Pokud předchůdce běží vyšším tempem (nižší délka výrobního taktu), poměr by měl být nižší než 1, jestliže předchůdce pracuje pomalejším tempem (vyšším délka výrobního taktu), poměr času cyklu je vyšší než 1.</span><span class="sxs-lookup"><span data-stu-id="b4a69-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="b4a69-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b4a69-123">Click OK.</span></span>


