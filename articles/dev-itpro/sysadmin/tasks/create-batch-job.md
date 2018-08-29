--- 
title: "Vytvořit dávkové úlohy"
description: "Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS)."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b32c16a0c0045e22128746f81c6e9fd03370ac1f
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="create-batch-jobs"></a><span data-ttu-id="23a84-103">Vytvořit dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="23a84-103">Create batch jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23a84-104">Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).</span><span class="sxs-lookup"><span data-stu-id="23a84-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="23a84-105">Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil.</span><span class="sxs-lookup"><span data-stu-id="23a84-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="23a84-106">Dávkovou úlohu můžete nastavit následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="23a84-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="23a84-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="23a84-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="23a84-108">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="23a84-108">Create the batch job</span></span>
1. <span data-ttu-id="23a84-109">Přejděte na Správa systému > Dotazy > Dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="23a84-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="23a84-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="23a84-110">Click New.</span></span>
3. <span data-ttu-id="23a84-111">Zadejte hodnotu do pole Popis práce.</span><span class="sxs-lookup"><span data-stu-id="23a84-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="23a84-112">Do pole Plánované počáteční datum a čas zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="23a84-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="23a84-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="23a84-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="23a84-114">Vytvoření opakování</span><span class="sxs-lookup"><span data-stu-id="23a84-114">Create a recurrence</span></span>
1. <span data-ttu-id="23a84-115">V podokně akcí klikněte na možnost Dávková úloha.</span><span class="sxs-lookup"><span data-stu-id="23a84-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="23a84-116">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="23a84-116">Click Recurrence.</span></span>
    * <span data-ttu-id="23a84-117">Pomocí těchto možností zadejte rozsah a vzor opakování.</span><span class="sxs-lookup"><span data-stu-id="23a84-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="23a84-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="23a84-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="23a84-119">Přidání výstrah</span><span class="sxs-lookup"><span data-stu-id="23a84-119">Add alerts</span></span>
1. <span data-ttu-id="23a84-120">V podokně akcí klikněte na možnost Dávková úloha.</span><span class="sxs-lookup"><span data-stu-id="23a84-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="23a84-121">Klepněte na tlačítko Výstrahy.</span><span class="sxs-lookup"><span data-stu-id="23a84-121">Click Alerts.</span></span>
    * <span data-ttu-id="23a84-122">Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="23a84-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="23a84-123">Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.</span><span class="sxs-lookup"><span data-stu-id="23a84-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="23a84-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="23a84-124">Click OK.</span></span>


