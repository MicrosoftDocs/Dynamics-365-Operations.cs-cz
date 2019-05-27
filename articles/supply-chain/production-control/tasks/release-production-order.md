---
title: Uvolnění výrobní zakázky
description: Tato procedura popisuje způsob uvolnění výrobní zakázky.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917fe1ef826c9b112be29ebce78ebd750652db64
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562966"
---
# <a name="release-a-production-order"></a><span data-ttu-id="46344-103">Uvolnění výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="46344-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46344-104">Tato procedura popisuje způsob uvolnění výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="46344-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="46344-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="46344-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="46344-106">Jedná se o čtvrtou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="46344-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="46344-107">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="46344-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="46344-108">V mřížce vyberte výrobní zakázku, která má stav Naplánováno.</span><span class="sxs-lookup"><span data-stu-id="46344-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="46344-109">V podokně akcí klikněte na možnost Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="46344-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="46344-110">Klikněte na Uvolnit</span><span class="sxs-lookup"><span data-stu-id="46344-110">Click Release.</span></span>
    * <span data-ttu-id="46344-111">Na této stránce můžete potvrdit uvolnění vybraného rozsahu výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="46344-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="46344-112">Klepněte na tlačítko Vybrat, pokud chcete přidat objednávky.</span><span class="sxs-lookup"><span data-stu-id="46344-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="46344-113">Krok Uvolnění určuje, kdy je výrobní zakázka uvolněna do výrobní dílny, aby operátoři dílny mohli ohlásit postup ve výrobních úlohách.</span><span class="sxs-lookup"><span data-stu-id="46344-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="46344-114">Je možné vydat výrobní doklady mohou obsahovat důležité informace o zpracování úlohy.</span><span class="sxs-lookup"><span data-stu-id="46344-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="46344-115">Skladová práce pro výdej suroviny je vytvořena pro položky, které jsou nastaveny pro skladový proces.</span><span class="sxs-lookup"><span data-stu-id="46344-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="46344-116">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="46344-116">Click the General tab.</span></span>
    * <span data-ttu-id="46344-117">Vyberte výrobní sestavy, které mají být vytištěny.</span><span class="sxs-lookup"><span data-stu-id="46344-117">Select which production reports should be printed.</span></span> <span data-ttu-id="46344-118">Sestava úkolových lístků vytiskne stránku pro každou naplánovanou úlohu a vyžaduje, aby byla výrobní zakázka plánována na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="46344-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="46344-119">Sestava obsahuje informace o plánovaném počátečním a koncovém čase, množství k výrobě, a informaci o zdrojích, které zpracovávají úlohu.</span><span class="sxs-lookup"><span data-stu-id="46344-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="46344-120">Sestava Úloha postupu shromažďuje stejné informace na stejné stránce, ale nevytiskne stránku pro každou úlohu.</span><span class="sxs-lookup"><span data-stu-id="46344-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="46344-121">Sestava Karta postupu zobrazí pouze operace, ale nikoli úlohy.</span><span class="sxs-lookup"><span data-stu-id="46344-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="46344-122">Tato sestava tedy nevyžaduje plánování úloh, ale lze ji použít při plánování výrobních zakázek na úrovni operací.</span><span class="sxs-lookup"><span data-stu-id="46344-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="46344-123">Klikněte na pole Tisk karty postupu.</span><span class="sxs-lookup"><span data-stu-id="46344-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="46344-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="46344-124">Click OK.</span></span>
7. <span data-ttu-id="46344-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="46344-125">Close the page.</span></span>

