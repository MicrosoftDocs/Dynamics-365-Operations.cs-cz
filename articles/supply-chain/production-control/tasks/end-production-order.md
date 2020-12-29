---
title: Ukončení výrobní zakázky
description: Tato procedura popisuje způsob ukončení výrobní zakázky.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423512"
---
# <a name="end-a-production-order"></a><span data-ttu-id="2eaa3-103">Ukončení výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="2eaa3-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2eaa3-104">Tato procedura popisuje způsob ukončení výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="2eaa3-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2eaa3-106">Jedná se o poslední proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="2eaa3-107">Ukončení výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="2eaa3-107">End a production order</span></span>
1. <span data-ttu-id="2eaa3-108">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="2eaa3-109">Vyberte výrobní zakázku, která má stav Vykázáno jako dokončený.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="2eaa3-110">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="2eaa3-111">Klepněte na tlačítko Konec.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-111">Click End.</span></span>
    * <span data-ttu-id="2eaa3-112">Na této stránce můžete potvrdit, že chcete ukončit výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="2eaa3-113">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-113">Click the General tab.</span></span>
5. <span data-ttu-id="2eaa3-114">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="2eaa3-115">V poli Metoda odpadu vyberte „Přidělení“</span><span class="sxs-lookup"><span data-stu-id="2eaa3-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="2eaa3-116">Pokud vyberete Metodu přidělení, náklady za sešrotovaný materiál budou přidány k dokončenému zboží.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="2eaa3-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="2eaa3-118">Ověření výsledků výpočtu</span><span class="sxs-lookup"><span data-stu-id="2eaa3-118">Validate calculation results</span></span>
1. <span data-ttu-id="2eaa3-119">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="2eaa3-120">Klikněte na Zobrazit porovnání nákladů.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="2eaa3-121">Po ukončení výrobní zakázky budete mít můžete porovnat odhadovanou cenu nákladu proti skutečné ceně nákladů, abyste získali přehled o výrobních odchylkách.</span><span class="sxs-lookup"><span data-stu-id="2eaa3-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
