---
title: "Ohlášení výrobní zakázky jako dokončené"
description: "Tato procedura popisuje způsob nahlásit výrobní zakázky jako dokončenou."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cdc133105f393544af4aee33269a30bc364752c3
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="c09de-103">Ohlášení výrobní zakázky jako dokončené</span><span class="sxs-lookup"><span data-stu-id="c09de-103">Report a production order as finished</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c09de-104">Tato procedura popisuje způsob nahlásit výrobní zakázky jako dokončenou.</span><span class="sxs-lookup"><span data-stu-id="c09de-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="c09de-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="c09de-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c09de-106">Jedná se o šestou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="c09de-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="c09de-107">Ohlášení výrobní zakázky jako dokončené</span><span class="sxs-lookup"><span data-stu-id="c09de-107">Report a production order as finished</span></span>
1. <span data-ttu-id="c09de-108">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="c09de-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="c09de-109">Vyberte výrobní zakázku, která má stav Zahájeno.</span><span class="sxs-lookup"><span data-stu-id="c09de-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="c09de-110">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="c09de-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="c09de-111">Klikněte na položku Oznámit jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="c09de-111">Click Report as finished.</span></span>
    * <span data-ttu-id="c09de-112">Na této stránce můžete potvrdit množství dokončeného produktu, které má být ohlášeno jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="c09de-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="c09de-113">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="c09de-113">Click the General tab.</span></span>
5. <span data-ttu-id="c09de-114">Nastavte Množství zboží na „18“.</span><span class="sxs-lookup"><span data-stu-id="c09de-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="c09de-115">Nastavte položku Chyba v množství na „2“.</span><span class="sxs-lookup"><span data-stu-id="c09de-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="c09de-116">Do pole Příčina chyby vyberte „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="c09de-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="c09de-117">Zaškrtněte nebo zrušte zaškrtnutí políčka Koncová práce.</span><span class="sxs-lookup"><span data-stu-id="c09de-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="c09de-118">Zaškrtněte políčko Akceptovat chybu nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="c09de-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="c09de-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c09de-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="c09de-120">Ověřte Deník dokončené výroby.</span><span class="sxs-lookup"><span data-stu-id="c09de-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="c09de-121">V podokně akcí klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="c09de-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="c09de-122">Klepněte na Ohlášeno jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="c09de-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="c09de-123">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c09de-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c09de-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c09de-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c09de-125">Je zaúčtován Deník dokončené výroby.</span><span class="sxs-lookup"><span data-stu-id="c09de-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="c09de-126">Podle potřeby můžete v deníku provádět úpravy, můžete ručně vytvořit nový deník, kde můžete provádět změny.</span><span class="sxs-lookup"><span data-stu-id="c09de-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

