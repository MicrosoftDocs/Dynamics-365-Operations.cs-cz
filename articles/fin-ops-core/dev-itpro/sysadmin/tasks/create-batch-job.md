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
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143666"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="25226-103">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="25226-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25226-104">Dávková úloha představuje skupinu úkolů, které jsou odeslány k automatickému zpracování instancí aplikačního objektového serveru (AOS).</span><span class="sxs-lookup"><span data-stu-id="25226-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="25226-105">Dávkové úlohy jsou spouštěny s bezpečnostním pověřením uživatele, který je vytvořil.</span><span class="sxs-lookup"><span data-stu-id="25226-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="25226-106">Dávkovou úlohu můžete nastavit následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="25226-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="25226-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="25226-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="25226-108">Vytvoření dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="25226-108">Create the batch job</span></span>
1. <span data-ttu-id="25226-109">Přejděte do **navigačního podokna > Moduly > Správa systému > Dotazy > Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="25226-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="25226-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="25226-110">Click **New**.</span></span>
3. <span data-ttu-id="25226-111">Zadejte hodnotu do pole **Popis práce**.</span><span class="sxs-lookup"><span data-stu-id="25226-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="25226-112">Do pole **Plánované počáteční datum a čas** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="25226-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="25226-113">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25226-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="25226-114">Vytvoření opakování</span><span class="sxs-lookup"><span data-stu-id="25226-114">Create a recurrence</span></span>
1. <span data-ttu-id="25226-115">V podokně akcí klikněte na možnost **Dávková úloha**.</span><span class="sxs-lookup"><span data-stu-id="25226-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="25226-116">Klikněte na **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="25226-116">Click **Recurrence**.</span></span> <span data-ttu-id="25226-117">Pomocí těchto možností zadejte rozsah a vzor opakování.</span><span class="sxs-lookup"><span data-stu-id="25226-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="25226-118">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="25226-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="25226-119">Přidání výstrah</span><span class="sxs-lookup"><span data-stu-id="25226-119">Add alerts</span></span>
1. <span data-ttu-id="25226-120">V podokně akcí klikněte na možnost **Dávková úloha**.</span><span class="sxs-lookup"><span data-stu-id="25226-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="25226-121">Klikněte na **Výstrahy**.</span><span class="sxs-lookup"><span data-stu-id="25226-121">Click **Alerts**.</span></span> <span data-ttu-id="25226-122">Určete, zda chcete odeslat upozornění po dokončení dávkové úlohy, dojde-li k chybě nebo dojde ke zrušení.</span><span class="sxs-lookup"><span data-stu-id="25226-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="25226-123">Poté stanovte, zda chcete, aby se výstrahy zobrazily v místním okně.</span><span class="sxs-lookup"><span data-stu-id="25226-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="25226-124">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="25226-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="25226-125">Úprava stavu dávkové úlohy</span><span class="sxs-lookup"><span data-stu-id="25226-125">Adjust batch job status</span></span>
1. <span data-ttu-id="25226-126">Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="25226-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="25226-127">Vyberte odpovídající dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="25226-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="25226-128">V podokně akcí klikněte na možnost **Dávková úloha > Funkce > Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="25226-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="25226-129">Vyberte příslušný stav:</span><span class="sxs-lookup"><span data-stu-id="25226-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="25226-130">**Srážka**: Nastavte dávkovou úlohu jako **srážku** tak, aby byla zadržena plánovačem dávkových úloh.</span><span class="sxs-lookup"><span data-stu-id="25226-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="25226-131">Ekvivalent *zastavení*</span><span class="sxs-lookup"><span data-stu-id="25226-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="25226-132">**Čekání**: Nastavte dávkovou úlohu jako **čekání**, aby čekala na vyzvednutí plánovačem úloh.</span><span class="sxs-lookup"><span data-stu-id="25226-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="25226-133">Ekvivalent *přejít*</span><span class="sxs-lookup"><span data-stu-id="25226-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="25226-134">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="25226-134">Click **OK**.</span></span>
