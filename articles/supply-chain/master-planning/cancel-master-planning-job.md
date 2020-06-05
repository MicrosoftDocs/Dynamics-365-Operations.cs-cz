---
title: Zrušení hlavní plánovací úlohy
description: Toto téma vysvětluje způsob zrušení aktivní plánovací úlohy, která používá integrovanou funkci plánování.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e38b1bb84414dde603dbf5bcda0e8253a12e40b
ms.sourcegitcommit: 78a1aa37f9a1565135b139e36501b759e7b2f849
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/14/2020
ms.locfileid: "3374789"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="79159-103">Zrušení hlavní plánovací úlohy</span><span class="sxs-lookup"><span data-stu-id="79159-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79159-104">V aplikaci Microsoft Dynamics 365 Supply Chain Management existuje několik možností zrušení hlavní plánovací úlohy.</span><span class="sxs-lookup"><span data-stu-id="79159-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="79159-105">Hlavní plánovací úlohu můžete například chtít zrušit, pokud byla spuštěna omylem nebo pokud je spuštěna déle, než bylo očekáváno, a chcete ji ukončit.</span><span class="sxs-lookup"><span data-stu-id="79159-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="79159-106">Nejlepší způsob, jak zrušit plánovací úlohu, je ze stránky **nedokončené procesy plánování**.</span><span class="sxs-lookup"><span data-stu-id="79159-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="79159-107">Alternativní možnosti ze stránek **Dávkové úlohy** a **Pokročilé dávkové úlohy** by se měly použít pouze v případě, že zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy** neskončilo během pár minut.</span><span class="sxs-lookup"><span data-stu-id="79159-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="79159-108">Preferovaná možnost zrušení</span><span class="sxs-lookup"><span data-stu-id="79159-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="79159-109">Zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy**</span><span class="sxs-lookup"><span data-stu-id="79159-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="79159-110">Přejděte na **Hlavní plánování > Dotazy a sestavy > Hlavní plánování > Nedokončené plánovací procesy**.</span><span class="sxs-lookup"><span data-stu-id="79159-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="79159-111">Vyberte řádek s plánovacím procesem, který chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="79159-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="79159-112">Klepněte na možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="79159-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="79159-113">Další možnosti zrušení</span><span class="sxs-lookup"><span data-stu-id="79159-113">Additional cancel options</span></span>
<span data-ttu-id="79159-114">Tyto operace by měly být použity pouze v případě, že zrušení hlavní plánovací úlohy ze stránky **Nedokončené plánovací procesy** nebylo dokončeno během pár minut.</span><span class="sxs-lookup"><span data-stu-id="79159-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="79159-115">Odstranění hlavní plánovací úlohy ze stránky **Dávkové úlohy**</span><span class="sxs-lookup"><span data-stu-id="79159-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="79159-116">Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="79159-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="79159-117">Vyberte řádek s plánovací úlohou, který chcete odstranit.</span><span class="sxs-lookup"><span data-stu-id="79159-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="79159-118">Klepněte na tlačítko **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="79159-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="79159-119">Zrušení hlavní plánovací úlohy ze stránky **Pokročilé dávkové úlohy**</span><span class="sxs-lookup"><span data-stu-id="79159-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="79159-120">Přejděte na **Správa systému > Dotazy > Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="79159-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="79159-121">Pokud není ID úlohy v seznamu zobrazeno, klikněte na tlačítko **Přepnout do rozšířeného formuláře**, jinak pokračujte dalším krokem.</span><span class="sxs-lookup"><span data-stu-id="79159-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="79159-122">Otevřete dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="79159-122">Open the batch job.</span></span> <span data-ttu-id="79159-123">Kikněte na **ID úlohy** u dávkové úlohy s úkoly, které chcete ukončit.</span><span class="sxs-lookup"><span data-stu-id="79159-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="79159-124">V okně **Dávkové úkoly** vyberte úkoly, které chcete ukončit.</span><span class="sxs-lookup"><span data-stu-id="79159-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="79159-125">Klikněte na **Změnit stav**, vyberte **Zrušení** a klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="79159-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="79159-126">Na pevné záložce **Dávkové úkoly** klikněte na **Ukončit**.</span><span class="sxs-lookup"><span data-stu-id="79159-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
