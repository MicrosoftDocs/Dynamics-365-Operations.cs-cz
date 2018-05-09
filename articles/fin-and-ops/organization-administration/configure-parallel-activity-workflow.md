---
title: "Konfigurace paralelních aktivit ve workflowu"
description: "Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3e0cf27c7932415c822843b3376894ba172578b9
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="0aef0-103">Konfigurace paralelních aktivit ve workflowu</span><span class="sxs-lookup"><span data-stu-id="0aef0-103">Configure a parallel activity in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aef0-104">Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="0aef0-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="0aef0-105">Paralelní aktivita je tvořena větvemi workflowu, které běží ve stejnou dobu.</span><span class="sxs-lookup"><span data-stu-id="0aef0-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="0aef0-106">Pojmenování paralelní aktivity</span><span class="sxs-lookup"><span data-stu-id="0aef0-106">Name a parallel activity</span></span>
<span data-ttu-id="0aef0-107">Pomocí následujících kroků zadejte název paralelní aktivity.</span><span class="sxs-lookup"><span data-stu-id="0aef0-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="0aef0-108">Klikněte pravým tlačítkem na paralelní aktivitu a poté klikněte na tlačítko **Vlastnosti** k otevření formuláře **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="0aef0-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="0aef0-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="0aef0-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="0aef0-110">V poli **Název** zadejte jedinečný název paralelní aktivity.</span><span class="sxs-lookup"><span data-stu-id="0aef0-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="0aef0-111">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="0aef0-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="0aef0-112">Konfigurace větví paralelní aktivity</span><span class="sxs-lookup"><span data-stu-id="0aef0-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="0aef0-113">Pomocí následujících kroků přidejte a nakonfigurujte větve této paralelní aktivity.</span><span class="sxs-lookup"><span data-stu-id="0aef0-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1. <span data-ttu-id="0aef0-114">Poklikejte na paralelní aktivitu, aby se zobrazily její větve.</span><span class="sxs-lookup"><span data-stu-id="0aef0-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="0aef0-115">Pokud chcete přidat pobočku, přetáhněte prvek **Větev** z oblasti **Prvky workflowu** do oblasti vložení na plátně.</span><span class="sxs-lookup"><span data-stu-id="0aef0-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="0aef0-116">Následující obrázek znázorňuje oblast vložení.![Oblast vložení](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="0aef0-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>

   |                                              <span data-ttu-id="0aef0-117"><strong>Poznámka</strong></span><span class="sxs-lookup"><span data-stu-id="0aef0-117"><strong>Note</strong></span></span>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | <span data-ttu-id="0aef0-118">Pořadí větví není důležité, protože všechny větve paralelní aktivity běží současně.</span><span class="sxs-lookup"><span data-stu-id="0aef0-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |


3. <span data-ttu-id="0aef0-119">Informace o konfiguraci jednotlivých větví uvádí téma [Konfigurace paralelní větve](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="0aef0-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






