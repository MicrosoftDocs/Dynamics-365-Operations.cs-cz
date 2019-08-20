---
title: Vytvoření dávkové úlohy
description: Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851280"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="c9e68-103">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="c9e68-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9e68-104">Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).</span><span class="sxs-lookup"><span data-stu-id="c9e68-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="c9e68-105">Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil.</span><span class="sxs-lookup"><span data-stu-id="c9e68-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="c9e68-106">Dávkovou úlohu můžete nastavit následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="c9e68-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="c9e68-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="c9e68-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="c9e68-108">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="c9e68-108">Create the batch job</span></span>
1. <span data-ttu-id="c9e68-109">Přejděte do **navigačního podokna > Moduly > Správa systému > Dotazy > Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c9e68-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-110">Click **New**.</span></span>
3. <span data-ttu-id="c9e68-111">Zadejte hodnotu do pole **Popis práce**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="c9e68-112">Do pole **Plánované počáteční datum a čas** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c9e68-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="c9e68-113">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="c9e68-114">Vytvoření opakování</span><span class="sxs-lookup"><span data-stu-id="c9e68-114">Create a recurrence</span></span>
1. <span data-ttu-id="c9e68-115">V podokně akcí klikněte na možnost **Dávková úloha**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c9e68-116">Klikněte na **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-116">Click **Recurrence**.</span></span> <span data-ttu-id="c9e68-117">Pomocí těchto možností zadejte rozsah a vzor opakování.</span><span class="sxs-lookup"><span data-stu-id="c9e68-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="c9e68-118">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="c9e68-119">Přidání výstrah</span><span class="sxs-lookup"><span data-stu-id="c9e68-119">Add alerts</span></span>
1. <span data-ttu-id="c9e68-120">V podokně akcí klikněte na možnost **Dávková úloha**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c9e68-121">Klikněte na **Výstrahy**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-121">Click **Alerts**.</span></span> <span data-ttu-id="c9e68-122">Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="c9e68-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="c9e68-123">Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.</span><span class="sxs-lookup"><span data-stu-id="c9e68-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="c9e68-124">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="c9e68-125">Úprava stavu dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="c9e68-125">Adjust batch job status</span></span>
1. <span data-ttu-id="c9e68-126">Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c9e68-127">Vyberte odpovídající dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="c9e68-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="c9e68-128">V podokně akcí klikněte na možnost **Dávková úloha > Funkce > Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="c9e68-129">Vyberte příslušný stav:</span><span class="sxs-lookup"><span data-stu-id="c9e68-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="c9e68-130">**Srážka**: Nastavte dávkovou úlohu jako **srážku** tak, aby byla zadržena plánovačem dávkových úloh.</span><span class="sxs-lookup"><span data-stu-id="c9e68-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="c9e68-131">Ekvivalent *zastavení*</span><span class="sxs-lookup"><span data-stu-id="c9e68-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="c9e68-132">**Čekání**: Nastavte dávkovou úlohu jako **čekání**, aby čekala na vyzvednutí plánovačem úloh.</span><span class="sxs-lookup"><span data-stu-id="c9e68-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="c9e68-133">Ekvivalent *přejít*</span><span class="sxs-lookup"><span data-stu-id="c9e68-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="c9e68-134">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9e68-134">Click **OK**.</span></span>
