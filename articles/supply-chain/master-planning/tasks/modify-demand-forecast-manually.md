--- 
title: "Ruční úprava prognózy poptávky"
description: "Tento postup popisuje postup úpravy prognózy pro položku."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 911245eea967126686564b24bdccba48de075929
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="fbb36-103">Ruční úprava prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="fbb36-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbb36-104">Tento postup popisuje postup úpravy prognózy pro položku.</span><span class="sxs-lookup"><span data-stu-id="fbb36-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="fbb36-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="fbb36-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fbb36-106">Tento záznam je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="fbb36-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="fbb36-107">Upravení prognózy pro zboží</span><span class="sxs-lookup"><span data-stu-id="fbb36-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="fbb36-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="fbb36-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="fbb36-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fbb36-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fbb36-110">Vyberte položku, u které chcete změnit typ prognózu.</span><span class="sxs-lookup"><span data-stu-id="fbb36-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="fbb36-111">Můžete vybrat zboží D0001.</span><span class="sxs-lookup"><span data-stu-id="fbb36-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="fbb36-112">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="fbb36-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="fbb36-113">Klikněte na položku Prognóza poptávky.</span><span class="sxs-lookup"><span data-stu-id="fbb36-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="fbb36-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="fbb36-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fbb36-115">Pokud neexistují žádné řádky prognózy, vytvořte nový řádek</span><span class="sxs-lookup"><span data-stu-id="fbb36-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="fbb36-116">klepnutím na panelu aplikací na Nový.</span><span class="sxs-lookup"><span data-stu-id="fbb36-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="fbb36-117">V poli Prod. množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fbb36-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="fbb36-118">Toto číslo představuje předpovídané množství položky.</span><span class="sxs-lookup"><span data-stu-id="fbb36-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="fbb36-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fbb36-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="fbb36-120">Upravení prognózy v aplikaci Excel</span><span class="sxs-lookup"><span data-stu-id="fbb36-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="fbb36-121">Klikněte na Otevřít v systému Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="fbb36-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="fbb36-122">Klikněte na Upravit prognózy poptávky v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="fbb36-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="fbb36-123">V aplikaci Excel lze přidat, odstranit a upravit řádky prognózy poptávky.</span><span class="sxs-lookup"><span data-stu-id="fbb36-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="fbb36-124">Pokud nejsou vidět data v aplikaci Excel, je třeba přihlásit se v aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise, s aktivní možností "Zůstat přihlášeni", a je nutné důvěřovat datovému spojení.</span><span class="sxs-lookup"><span data-stu-id="fbb36-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


