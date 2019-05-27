---
title: Vytvoření dávkové úlohy
description: Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562874"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="18eaf-103">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="18eaf-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18eaf-104">Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).</span><span class="sxs-lookup"><span data-stu-id="18eaf-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="18eaf-105">Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil.</span><span class="sxs-lookup"><span data-stu-id="18eaf-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="18eaf-106">Dávkovou úlohu můžete nastavit následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="18eaf-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="18eaf-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="18eaf-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="18eaf-108">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="18eaf-108">Create the batch job</span></span>
1. <span data-ttu-id="18eaf-109">Přejděte na Správa systému > Dotazy > Dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="18eaf-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="18eaf-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="18eaf-110">Click New.</span></span>
3. <span data-ttu-id="18eaf-111">Zadejte hodnotu do pole Popis práce.</span><span class="sxs-lookup"><span data-stu-id="18eaf-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="18eaf-112">Do pole Plánované počáteční datum a čas zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="18eaf-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="18eaf-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="18eaf-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="18eaf-114">Vytvoření opakování</span><span class="sxs-lookup"><span data-stu-id="18eaf-114">Create a recurrence</span></span>
1. <span data-ttu-id="18eaf-115">V podokně akcí klikněte na možnost Dávková úloha.</span><span class="sxs-lookup"><span data-stu-id="18eaf-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="18eaf-116">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="18eaf-116">Click Recurrence.</span></span>
    * <span data-ttu-id="18eaf-117">Pomocí těchto možností zadejte rozsah a vzor opakování.</span><span class="sxs-lookup"><span data-stu-id="18eaf-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="18eaf-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="18eaf-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="18eaf-119">Přidání výstrah</span><span class="sxs-lookup"><span data-stu-id="18eaf-119">Add alerts</span></span>
1. <span data-ttu-id="18eaf-120">V podokně akcí klikněte na možnost Dávková úloha.</span><span class="sxs-lookup"><span data-stu-id="18eaf-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="18eaf-121">Klepněte na tlačítko Výstrahy.</span><span class="sxs-lookup"><span data-stu-id="18eaf-121">Click Alerts.</span></span>
    * <span data-ttu-id="18eaf-122">Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="18eaf-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="18eaf-123">Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.</span><span class="sxs-lookup"><span data-stu-id="18eaf-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="18eaf-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="18eaf-124">Click OK.</span></span>

