--- 
title: "Ohlášení jako dokončené pro skladové místo bez řízení na základě registračních značek "
description: "Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="32470-103">Ohlášení jako dokončené pro skladové místo bez řízení na základě registračních značek </span><span class="sxs-lookup"><span data-stu-id="32470-103">Report as finished to a plate-controlled location</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32470-104">Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="32470-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="32470-105">Předpokladem pro tento úkol je příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="32470-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="32470-106">Předchozí průvodce úlohou popisoval nastavení pracovních zásad.</span><span class="sxs-lookup"><span data-stu-id="32470-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="32470-107">Tento průvodce úkolem vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="32470-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="32470-108">Nastavení výstupního umístění</span><span class="sxs-lookup"><span data-stu-id="32470-108">Set up an output location</span></span>
1. <span data-ttu-id="32470-109">Přejděte na nabídce Správa organizace > Zdroje > Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="32470-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="32470-110">V seznamu vyberte skupinu prostředků '5102'.</span><span class="sxs-lookup"><span data-stu-id="32470-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="32470-111">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="32470-111">Click Edit.</span></span>
4. <span data-ttu-id="32470-112">V poli Výstupní sklad vyberte 51.</span><span class="sxs-lookup"><span data-stu-id="32470-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="32470-113">V poli Výstupní umístění vyberte 001.</span><span class="sxs-lookup"><span data-stu-id="32470-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="32470-114">Umístění 001 není umístění řízené registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="32470-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="32470-115">Umístění výstupu bez registrační značky můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="32470-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="32470-116">Vytvoření výrobní zakázky a její ohlášení jako dokončené</span><span class="sxs-lookup"><span data-stu-id="32470-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="32470-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="32470-117">Close the page.</span></span>
2. <span data-ttu-id="32470-118">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="32470-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="32470-119">Klikněte na možnost Nová výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="32470-119">Click New production order.</span></span>
4. <span data-ttu-id="32470-120">V poli Číslo zboží zadejte 'L0101'.</span><span class="sxs-lookup"><span data-stu-id="32470-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="32470-121">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="32470-121">Click Create.</span></span>
6. <span data-ttu-id="32470-122">V podokně akcí klikněte na možnost Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="32470-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="32470-123">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="32470-123">Click Estimate.</span></span>
8. <span data-ttu-id="32470-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32470-124">Click OK.</span></span>
9. <span data-ttu-id="32470-125">Klepněte na tlačítko Start.</span><span class="sxs-lookup"><span data-stu-id="32470-125">Click Start.</span></span>
10. <span data-ttu-id="32470-126">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="32470-126">Click the General tab.</span></span>
11. <span data-ttu-id="32470-127">V poli Automatická spotřeba kusovníku vyberte hodnotu „Nikdy“.</span><span class="sxs-lookup"><span data-stu-id="32470-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="32470-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32470-128">Click OK.</span></span>
13. <span data-ttu-id="32470-129">Klepněte na možnost Vykázat jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="32470-129">Click Report as finished.</span></span>
14. <span data-ttu-id="32470-130">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="32470-130">Click the General tab.</span></span>
15. <span data-ttu-id="32470-131">Vyberte možnost Ano v poli Akceptovat chybu.</span><span class="sxs-lookup"><span data-stu-id="32470-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="32470-132">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32470-132">Click OK.</span></span>
17. <span data-ttu-id="32470-133">V podokně akcí klikněte na možnost Sklad.</span><span class="sxs-lookup"><span data-stu-id="32470-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="32470-134">Klepněte na tlačítko Podrobnosti práce.</span><span class="sxs-lookup"><span data-stu-id="32470-134">Click Work details.</span></span>
    * <span data-ttu-id="32470-135">Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena.</span><span class="sxs-lookup"><span data-stu-id="32470-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="32470-136">K tomu dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt L0101 ohlášen za dokončený v umístění 001.</span><span class="sxs-lookup"><span data-stu-id="32470-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  


