---
title: Ohlášení za dokončené pro umístění bez řízení na základě registračních značek (aplikace, květen 2016)
description: Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562920"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="27991-103">Ohlášení za dokončené pro umístění bez řízení na základě registračních značek (aplikace, květen 2016)</span><span class="sxs-lookup"><span data-stu-id="27991-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27991-104">Tento průvodce úkolem obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="27991-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="27991-105">Předpokladem pro tento úkol je příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="27991-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="27991-106">Předchozí průvodce úlohou popisoval nastavení pracovních zásad.</span><span class="sxs-lookup"><span data-stu-id="27991-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="27991-107">Tento průvodce úkolem vyžaduje aplikaci Dynamics AX 7.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="27991-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="27991-108">Nastavení výstupního umístění</span><span class="sxs-lookup"><span data-stu-id="27991-108">Set up an output location</span></span>
1. <span data-ttu-id="27991-109">Přejděte na nabídce Správa organizace > Zdroje > Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="27991-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="27991-110">V seznamu vyberte skupinu prostředků '5102'.</span><span class="sxs-lookup"><span data-stu-id="27991-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="27991-111">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="27991-111">Click Edit.</span></span>
4. <span data-ttu-id="27991-112">V poli Výstupní sklad vyberte 51.</span><span class="sxs-lookup"><span data-stu-id="27991-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="27991-113">V poli Výstupní umístění vyberte 001.</span><span class="sxs-lookup"><span data-stu-id="27991-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="27991-114">Umístění 001 není umístění řízené registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="27991-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="27991-115">Umístění výstupu bez registrační značky můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="27991-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="27991-116">Vytvoření výrobní zakázky a její ohlášení jako dokončené</span><span class="sxs-lookup"><span data-stu-id="27991-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="27991-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="27991-117">Close the page.</span></span>
2. <span data-ttu-id="27991-118">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="27991-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="27991-119">Klikněte na možnost Nová výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="27991-119">Click New production order.</span></span>
4. <span data-ttu-id="27991-120">V poli Číslo zboží zadejte 'L0101'.</span><span class="sxs-lookup"><span data-stu-id="27991-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="27991-121">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="27991-121">Click Create.</span></span>
6. <span data-ttu-id="27991-122">V podokně akcí klikněte na možnost Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="27991-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="27991-123">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="27991-123">Click Estimate.</span></span>
8. <span data-ttu-id="27991-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="27991-124">Click OK.</span></span>
9. <span data-ttu-id="27991-125">Klepněte na tlačítko Start.</span><span class="sxs-lookup"><span data-stu-id="27991-125">Click Start.</span></span>
10. <span data-ttu-id="27991-126">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="27991-126">Click the General tab.</span></span>
11. <span data-ttu-id="27991-127">V poli Automatická spotřeba kusovníku vyberte hodnotu „Nikdy“.</span><span class="sxs-lookup"><span data-stu-id="27991-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="27991-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="27991-128">Click OK.</span></span>
13. <span data-ttu-id="27991-129">Klepněte na možnost Vykázat jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="27991-129">Click Report as finished.</span></span>
14. <span data-ttu-id="27991-130">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="27991-130">Click the General tab.</span></span>
15. <span data-ttu-id="27991-131">Vyberte možnost Ano v poli Akceptovat chybu.</span><span class="sxs-lookup"><span data-stu-id="27991-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="27991-132">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="27991-132">Click OK.</span></span>
17. <span data-ttu-id="27991-133">V podokně akcí klikněte na možnost Sklad.</span><span class="sxs-lookup"><span data-stu-id="27991-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="27991-134">Klepněte na tlačítko Podrobnosti práce.</span><span class="sxs-lookup"><span data-stu-id="27991-134">Click Work details.</span></span>
    * <span data-ttu-id="27991-135">Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena.</span><span class="sxs-lookup"><span data-stu-id="27991-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="27991-136">K tomu dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt L0101 ohlášen za dokončený v umístění 001.</span><span class="sxs-lookup"><span data-stu-id="27991-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

