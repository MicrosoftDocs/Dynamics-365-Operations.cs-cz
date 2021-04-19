---
title: Spuštění výrobní zakázky
description: Tento postup ukazuje, jak začít výrobní zakázku v dílenském řízení.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be1c389bc4193ef080dbeb1639b69acf466ef0de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831859"
---
# <a name="start-a-production-order"></a><span data-ttu-id="189c9-103">Spuštění výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="189c9-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="189c9-104">Tento postup ukazuje, jak začít výrobní zakázku v dílenském řízení.</span><span class="sxs-lookup"><span data-stu-id="189c9-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="189c9-105">V tomto procesu je uveden čas a spotřeba materiálu.</span><span class="sxs-lookup"><span data-stu-id="189c9-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="189c9-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="189c9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="189c9-107">Jedná se o pátou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="189c9-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="189c9-108">Spuštění výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="189c9-108">Start a production order</span></span>
1. <span data-ttu-id="189c9-109">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="189c9-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="189c9-110">Vyberte výrobní zakázku, která má stav Vydáno.</span><span class="sxs-lookup"><span data-stu-id="189c9-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="189c9-111">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="189c9-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="189c9-112">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="189c9-112">Click Start.</span></span>
    * <span data-ttu-id="189c9-113">Na této stránce můžete potvrdit zahájení výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="189c9-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="189c9-114">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="189c9-114">Click the General tab.</span></span>
5. <span data-ttu-id="189c9-115">Zadejte číslo „10“ do pole</span><span class="sxs-lookup"><span data-stu-id="189c9-115">In the From Oper.</span></span> <span data-ttu-id="189c9-116">Č.</span><span class="sxs-lookup"><span data-stu-id="189c9-116">No.</span></span> <span data-ttu-id="189c9-117">pole zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="189c9-117">field, enter '10'.</span></span>
6. <span data-ttu-id="189c9-118">V poli Automatická spotřeba postupu vyberte hodnotu „Vždy“.</span><span class="sxs-lookup"><span data-stu-id="189c9-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="189c9-119">Zaškrtněte pole Zaúčtovat kartu postupu karty postupu.</span><span class="sxs-lookup"><span data-stu-id="189c9-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="189c9-120">V poli Automatická spotřeba kusovníku vyberte hodnotu „Vždy“.</span><span class="sxs-lookup"><span data-stu-id="189c9-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="189c9-121">Klepněte na zaškrtávací pole Zaúčtovat výdejku.</span><span class="sxs-lookup"><span data-stu-id="189c9-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="189c9-122">Klepněte na zaškrtávací pole Tisk výdejky.</span><span class="sxs-lookup"><span data-stu-id="189c9-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="189c9-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="189c9-123">Click OK.</span></span>
    * <span data-ttu-id="189c9-124">Toto je vytištěná výdejku zobrazující materiály použité pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="189c9-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="189c9-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="189c9-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="189c9-126">Ověření výdejky</span><span class="sxs-lookup"><span data-stu-id="189c9-126">Validate the picking list</span></span>
1. <span data-ttu-id="189c9-127">V podokně akcí klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="189c9-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="189c9-128">Klepněte na Výdejka.</span><span class="sxs-lookup"><span data-stu-id="189c9-128">Click Picking list.</span></span>
3. <span data-ttu-id="189c9-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="189c9-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="189c9-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="189c9-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="189c9-131">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="189c9-131">Click Edit.</span></span>
6. <span data-ttu-id="189c9-132">Zadejte číslo do pole Spotřeba.</span><span class="sxs-lookup"><span data-stu-id="189c9-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="189c9-133">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="189c9-133">Click Post.</span></span>
8. <span data-ttu-id="189c9-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="189c9-134">Click OK.</span></span>
    * <span data-ttu-id="189c9-135">V deníku výdejek jsou zaúčtovány materiály spotřebovány výrobní zakázkou.</span><span class="sxs-lookup"><span data-stu-id="189c9-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="189c9-136">Před zaúčtováním deníku můžete provádět úpravy, pokud existuje rozdíl mezi odhadovaným množstvím a skutečným spotřebovaným množstvím.</span><span class="sxs-lookup"><span data-stu-id="189c9-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="189c9-137">Klepněte na kartu panel mřížky.</span><span class="sxs-lookup"><span data-stu-id="189c9-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="189c9-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="189c9-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="189c9-139">Ověření deníku karet postupů</span><span class="sxs-lookup"><span data-stu-id="189c9-139">Verify the route card journal</span></span>
1. <span data-ttu-id="189c9-140">V podokně akcí klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="189c9-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="189c9-141">Klepněte na Karta postupu.</span><span class="sxs-lookup"><span data-stu-id="189c9-141">Click Route card.</span></span>
3. <span data-ttu-id="189c9-142">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="189c9-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="189c9-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="189c9-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="189c9-144">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="189c9-144">Click Edit.</span></span>
6. <span data-ttu-id="189c9-145">Do pole Hodiny zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="189c9-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="189c9-146">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="189c9-146">Click Post.</span></span>
8. <span data-ttu-id="189c9-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="189c9-147">Click OK.</span></span>
    * <span data-ttu-id="189c9-148">V deníku karet postupu je zaznamenáván čas strávený na jednotlivých operacích.</span><span class="sxs-lookup"><span data-stu-id="189c9-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="189c9-149">Může být rovněž uvedeno dobré a chybné množství.</span><span class="sxs-lookup"><span data-stu-id="189c9-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]