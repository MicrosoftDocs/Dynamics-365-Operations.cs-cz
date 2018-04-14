---
title: "Vykázat výrobní zakázky jako dokončené"
description: "Vykázat jako dokončené je ve fázi výroby. V této fázi je vykázán hotový výrobek a je přesunut z výrobní zakázky do zásob."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fa40733e3f1310869ead8b0ac774bb621637e250
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="1a8ff-104">Vykázat výrobní zakázky jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1a8ff-104">Report production orders as finished</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1a8ff-105">Vykázat jako dokončené je ve fázi výroby.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-105">Report as finished is a production stage.</span></span> <span data-ttu-id="1a8ff-106">V této fázi je vykázán hotový výrobek a je přesunut z výrobní zakázky do zásob.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="1a8ff-107">Je-li výrobní zakázka vykázána jako dokončená, jsou ve skladu zásob aktualizována množství dokončeného zboží.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="1a8ff-108">Částečné množství původně plánovaného množství objednávky může být hlášeno jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="1a8ff-109">Je také možné nahlásit množství chyb se přidruženými důvody chyb při vykazování množství jako dokončeného.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="1a8ff-110">Když výrobní zakázka dosáhne stavu Ohlášeno jako dokončené, znamená to, že ve výrobní zakázce nebude uváděné žádné další množství.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="1a8ff-111">Tyto následující vlastnosti jsou také přidruženy k procesu **Ohlásit jako dokončené**:</span><span class="sxs-lookup"><span data-stu-id="1a8ff-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="1a8ff-112">Je možné nastavit spotřebu surovin a času, který je úměrný hodnotě hlášeného množství (zpětné vyprázdnění)</span><span class="sxs-lookup"><span data-stu-id="1a8ff-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="1a8ff-113">Odloženou práci lze generovat pro položky, které jsou povoleny pro procesy skladu.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="1a8ff-114">Plánované nebo standardní náklady dokončeného zboží lze nastavit k vykazovaní do účtů hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="1a8ff-115">Objednávku kvality lze vytvořit pro vykázané množství na základě nastavení přidružení kvality.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="1a8ff-116">Množství je vykazováno do výstupní umístění.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="1a8ff-117">Poté se vytvoří práce skladu pro převedení množství z výstupního umístění do cílového umístění definovaného směrnicí umístění místa pro odloženou práci.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="1a8ff-118">Objednávku kvality lze vytvořit se po ohlášení dokončení výrobní zakázky, pokud bylo nastaveno přidružení kvality.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="1a8ff-119">Nastavené výrobní zakázky na Hlášeno jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1a8ff-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="1a8ff-120">K nastavení stavu výrobní zakázky na **Hlášeno jako dokončené** můžete použít standardní funkci aktualizace výrobní zakázky nebo deníky technických postupů a karet úloh, nebo pomocí deníku **Hlášeno jako dokončené**.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="1a8ff-121">Můžete také aktualizovat stav na **Hlášeno jako dokončené** prostřednictvím terminálu karty úloh a stránek zařízení karty úloh, když vykazujete poslední práce výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="1a8ff-122">V závěru můžete povolit možnost **Hlášeno jako dokončené** jako proces pro řešení zařízení ručně ovládaného skladu.</span><span class="sxs-lookup"><span data-stu-id="1a8ff-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




