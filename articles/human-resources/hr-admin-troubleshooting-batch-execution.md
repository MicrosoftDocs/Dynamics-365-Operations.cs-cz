---
title: Reset zablokovaných dávkových úloh
description: Toto téma vysvětluje, jak vyřešit problémy s dávkovými úlohami, které se zasekly.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 01ef0bf8ccc486614eec42d3fb6f0b2941fc47c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794942"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="ac99c-103">Reset zablokovaných dávkových úloh</span><span class="sxs-lookup"><span data-stu-id="ac99c-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="ac99c-104">Výdej</span><span class="sxs-lookup"><span data-stu-id="ac99c-104">Issue</span></span>

<span data-ttu-id="ac99c-105">V aplikaci Microsoft Dynamics 365 Human Resources může dojít k problémům s dávkovými úlohami, které se zasekly v jednom ze stavů **Provádění** nebo **Ruší se** a nedokončí se.</span><span class="sxs-lookup"><span data-stu-id="ac99c-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="ac99c-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="ac99c-106">Resolution</span></span>

<span data-ttu-id="ac99c-107">Když je dávková úloha zaseknutá ve stavu **Provádění** nebo **Ruší se**, můžete stav resetovat vynuceným zrušením úlohy.</span><span class="sxs-lookup"><span data-stu-id="ac99c-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="ac99c-108">Po zrušení můžete dávkovou úlohu resetovat nastavením na do stavu **Čekání**.</span><span class="sxs-lookup"><span data-stu-id="ac99c-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="ac99c-109">Poté bude znovu vyzvednuta k provedení v příštím plánovaném běhu dávek.</span><span class="sxs-lookup"><span data-stu-id="ac99c-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="ac99c-110">V pracovním prostoru **Správa systému** vyberte stránku **Odkazy** a v ní vyberte **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ac99c-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="ac99c-111">Na stránce se seznamem **Dávkové úlohy** vyberte úlohu, kterou je třeba resetovat.</span><span class="sxs-lookup"><span data-stu-id="ac99c-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="ac99c-112">Na pásu karet akcí vyberte **Vynutit zrušení** a akci potvrďte.</span><span class="sxs-lookup"><span data-stu-id="ac99c-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ac99c-113">Akce **Vynutit zrušení** je k dispozici pouze pokud má vybraná dávková úloha stav buď **Provádění** nebo **Ruší se** a pro úlohu nejsou spuštěny žádné dávkové procesy spuštění nebo zrušení.</span><span class="sxs-lookup"><span data-stu-id="ac99c-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="ac99c-114">Na pásu karet akcí vyberte možnost **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="ac99c-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="ac99c-115">Na stránce **Vyberte nový stav** vyberte **Čekání** a potom vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac99c-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Vyberte nový stav dávkové úlohy](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="ac99c-117">Viz také</span><span class="sxs-lookup"><span data-stu-id="ac99c-117">See also</span></span>

[<span data-ttu-id="ac99c-118">Optimalizace výkonu naplánováním dávkových úloh po hodinách</span><span class="sxs-lookup"><span data-stu-id="ac99c-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="ac99c-119">Optimalizace výkonu pomocí úloh automatického vyčištění</span><span class="sxs-lookup"><span data-stu-id="ac99c-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
